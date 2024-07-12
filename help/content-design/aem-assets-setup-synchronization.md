---
title: Einrichten des Synchronisierungsdienstes
description: "Erfahren Sie, wie Sie Ihre Adobe Commerce- und Experience Manager Assets-Projekte mit dem Assets Rule Engine Service verbinden, um die Asset-Synchronisierung zwischen diesen beiden Systemen zu ermöglichen."
feature: CMS, Media
source-git-commit: 9d7b1b58b472a99196213e5ab109142bc57b1692
workflow-type: tm+mt
source-wordcount: '1309'
ht-degree: 0%

---


# Einrichten des Synchronisierungsdienstes

Der Asset Rules Engine Service (ARES) ist ein Dienst mit mehreren Mandanten, der AEM Assets in Adobe Commerce integriert. Dieser Dienst synchronisiert Assets zwischen Adobe Commerce und Experience Manager. Der ARES-Dienst ordnet Assets in AEM basierend auf der SKU oder anderen Schlüsselattributen automatisch Produkten in Adobe Commerce zu. Außerdem wird sichergestellt, dass die neuesten Produkt-Assets und Varianten immer auf der E-Commerce-Site verfügbar sind.

Um den Dienst einzurichten, müssen Sie Ihre Mandantenkennung mit der ARES GraphQL-API registrieren und die entsprechende Regel zum Synchronisieren von Assets auswählen.

## Auswählen einer passenden Strategie

Die AEM Assets-Integration für Commerce unterstützt zwei Übereinstimmungsstrategien für die Synchronisierung von Assets zwischen Adobe Commerce und AEM Assets.

- **MatchBySku** - Dies ist die standardmäßige Übereinstimmungsregel, die Assets auf Grundlage der Bestandseinheit (Stock Keeping Unit, SKU) des Produkts abgleicht. Die SKU ist eine eindeutige Kennung für jedes Produkt. Diese Regel stimmt die SKU in den Asset-Metadaten mit der Commerce-Produkt-SKU überein, um sicherzustellen, dass Assets mit den richtigen Produkten verknüpft sind.

- **ExternalMatcher** - Diese Übereinstimmungsregel dient für komplexere Szenarien oder spezifische Geschäftsanforderungen, für die eine benutzerdefinierte Übereinstimmungslogik erforderlich ist. Um diese Regel verwenden zu können, müssen Sie benutzerdefinierten Code in Adobe Developer App Builder implementieren, der definiert, wie Assets mit Produkten abgeglichen werden.

Verwenden Sie für das erstmalige Onboarding die `MatchBySku` -Strategie. Bei Bedarf können Sie die passende Strategie später ändern.

## Mandanten registrieren

>[!BEGINSHADEBOX]

**Voraussetzung**

- [Das AEM Assets-Projekt wurde mit Commerce-Metadaten konfiguriert, die für die Zuordnung von Assets erforderlich sind](aem-assets-configure-aem.md).

- [Installieren und konfigurieren Sie die Experience Manager Assets-Integration in Adobe Commerce](aem-assets-configure-commerce.md).

>[!ENDSHADEBOX]

## Sammeln von Anmeldeinformationen

Sie benötigen die folgenden Anmeldeinformationen, um Ihre Commerce-Projektumgebung und AEM Assets-Projektumgebung zu authentifizieren und mit Commerce SaaS-Diensten zu verbinden.

| Erforderliche Daten | Source | Wo finde ich sie? |
| ---------- | ------ | ------------- |
| API-Schlüssel aus dem Magento-Konto | Commerce | Stellen Sie den öffentlichen API-Schlüssel für die Commerce-Umgebung bereit, die Sie verwenden, Staging oder Produktion. Die API-Schlüssel für die Produktions- und Staging-Umgebungen finden Sie auf der Seite [Einrichten des Commerce Service Connector](aem-assets-configure-commerce.md#configure-the-commerce-services-connector) im Admin-Menü oder auf der Seite [!UICONTROL My Account] im Abschnitt [!UICONTROL API Portal] . |
| Commerce SaaS-Projektkennung <ul><li>`magento-environment-Id`</li><li>`Project ID`</li></ul> | Commerce Admin | Diese Werte geben die Commerce-Umgebung sowie den SaaS-Datenraum und das Projekt an, mit dem eine Verbindung hergestellt werden soll. Die Werte stammen aus der Konfiguration [Commerce Services Connector SaaS Identifier].(aem-assets-configure-commerce.md#configure-the-commerce-services-connector). |
| AEM `programId`<br>`environmentId` | [AEM Assets-Autorenumgebung](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) | Öffnen Sie die AEM Sites-Seite und wählen Sie **[!UICONTROL Assets]** aus.  Kopieren Sie die Projekt- und Umgebungs-IDs aus der URL: `https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/` |
| baseURL | Commerce-Storefront | Die [Basis-URL](../stores-purchase/store-urls.md) für Ihre Commerce-Storefront. |
| OAuth-Anmeldeinformationen für den API-Zugriff | Commerce Admin | Sie finden diese Anmeldeinformationen in den Commerce [Konfigurationseinstellungen für die Assets-Integration](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release). |

## Mandant registrieren

Schließen Sie die Mandantenregistrierung ab, indem Sie eine Anfrage an den Assets Rule Engine Service senden, um Authentifizierungsberechtigungen und Mandanten-IDs hinzuzufügen. Die Anfrage enthält Anmeldeinformationen und Projektkennungen, die zum Herstellen der Verbindungen zwischen dem Dienst, dem Commerce-Projekt und dem Experience Manager Assets-Projekt erforderlich sind.

Senden Sie die Anforderung mit einem GraphQL-Client oder einer cURL.

>[!BEGINTABS]

>[!TAB GraphQL-Anfrage]

Verwenden eines GraphQL-Clients zum Senden einer POST-Anfrage an den API-Endpunkt `https://commerce.adobe.io/assets-integration/graphql`

**Erforderliche Kopfzeilen**

Geben Sie die folgenden HTTP-Header für die Anfrage an:

- `x-api-key`: API-Schlüssel aus Ihrem Magento-Konto
- `magento-environment-Id`: SaaS-Kennung
- `x-gw-signature`: JWT-Token, das mit der MAGEID verknüpft ist

**Anfrage:**

**Syntax**

```graphql
mutation registerTenant($tenantInput: TenantInput!) {
   registerTenant(tenantInput: $tenantInput) {
      tenantId
      userErrors {
         message
         path
      }
    }
}
```

**Beispielverwendung**

Registrieren Sie einen Mandanten und wählen Sie die Regel `matchBySku` aus, um Assets zwischen Adobe Commerce und dem AEM Assets-Projekt zuzuordnen.

**Anfrage:**

```graphql
   {
      "tenantInput": {
         "enabled": true,
         "projectId": "8231afb6-90cd-65e8-84ba-d9abac0f94e6",
         "aem": {
               "programId": "11111",
               "environmentId": "222222"
         },
         "commerce": {
               "baseUrl": "***",
               "credentials": {
                  "consumerKey": "***",
                  "consumerSecret": "***",
                  "accessToken": "***",
                  "accessTokenSecret": "***"
               }
         },
         "rule": {
            "type": "matchBySKU"
            "matchBySkuRule": {
               "metadataField": "commerce:skus"
            }
         }
      }
   }
```

**Antwort**

```graphql
{
    "data": {
        "registerTenant": {
            "tenantId": "b65d5da7-2756-46a1-9ff1-14fb5d925fee",
            "userErrors": []
        }
    }
}
```

>[!TAB cURL-Anfrage]

```shell
curl --request POST \
  --url https://commerce.adobe.io/assets-integration/graphql \
  --header 'Content-Type: application/json' \
  --header 'Magento-Environment-Id: ****' \
  --header 'x-api-key: ****' \
  --header 'x-gw-signature: *****' \
  --data '{"query":"mutation registerTenant($tenantInput: TenantInput!) {\n\tregisterTenant(tenantInput: $tenantInput) {\n\t\ttenantId\n\t\tuserErrors {\n\t\t\tmessage\n\t\t\tpath\n\t\t}\n\t}\n}\n","operationName":"registerTenant","variables":{"tenantInput":{"enabled":true,"threshold":100,"projectId":"5d6faa03-e200-4623-9008-da144e4eefd8","aem":{"programId":"***","environmentId":"***"},"commerce":{"version":"2.4.6-p2","extensionVersion":"0.0.1","baseUrl":"***","credentials":{"consumerKey":"***","consumerSecret":"***","accessToken":"***","accessTokenSecret":"***"}},"rule":{"type":"matchBySKU","matchBySkuRule":{"metadataField":"commerce:skus"}}}}}'
```

>[!ENDTABS]

### Eingabefelder

#### AemInput

Identifiziert die AEM Assets-Instanz zum Speichern von Commerce-Assets. Sie erhalten diese Informationen über die Ansicht &quot;Cloud Manager My Programs&quot;oder über die URL zur Inhaltserstellung.

| Feld | Datentyp | Beschreibung |
| ----- | --------- | ----------- |
| `programId` | String! | Eindeutige Kennung für Ihr Projekt in AEM Cloud Service |
| `environmentId` | String! | ID für die verwendete Projektumgebung, z. B. Produktion, Staging oder Entwicklung |

#### CommerceInput

Dieses Eingabefeld stellt die OAuth-Authentifizierungsberechtigungen für den API-Zugriff auf den Commerce-Katalog bereit. Sie finden diese Anmeldeinformationen in den Commerce [Konfigurationseinstellungen für die Assets-Integration](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release).

| Feld | Datentyp | Beschreibung |
| ----- | --------- | ----------- |
| `baseUrl` | Zeichenfolge | Die [Basis-URL](../stores-purchase/store-urls.md) für Ihre Commerce-Storefront. |
| `credentials` | [CommerceCredentialsInput](#commercecredentialsinput)! | Gibt die Anmeldeinformationen für den Zugriff auf die Commerce-Instanz an. |
| `extensionVersion` | Zeichenfolge | Optional. Die Version der AEM Assets-Integration für die Commerce-Erweiterung, die auf der Commerce-Instanz installiert ist. |
| `version` | Zeichenfolge | Optional. Die auf der Commerce-Instanz installierte Version der Commerce-Anwendung. |

#### CommerceCredentialsInput

Dieses Eingabefeld stellt die OAuth-Anmeldeinformationen für den API-Zugriff auf den Commerce-Katalog bereit. Sie finden diese Anmeldeinformationen in den Commerce [Konfigurationseinstellungen für die Assets-Integration](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release).

| Feld | Datentyp | Beschreibung |
| ----- | --------- | ----------- |
| `accessToken` | String! | Das für die Assets-Integration generierte Zugriffstoken. |
| `accessTokenSecret` | String! | Das für die Assets-Integration generierte Zugriffstoken-Geheimnis. |
| `consumerKey` | String! | Der für die Assets-Integration generierte Consumer-Schlüssel. |
| `consumerSecret` | String! | Das für die Assets-Integration generierte Verbrauchergeheimnis. |

#### ExternalMatcherInput

| Feld | Datentyp | Beschreibung |
| ----- | --------- | ----------- |
| assetToProductUrl | String! | <!--Add field description--> |
| productToAssetUrl | String! | <!--Add field description--> |
| Anmeldeinformationen | [ExternalMatcherCredentialsInput](#externalmatchercredentials)! | Anmeldeinformationen für den Zugriff auf das App Builder-Projekt für die AEM Assets-Integration für Commerce. |

#### ExternalMatcherCredentials

| Feld | Datentyp | Beschreibung |
| ----- | --------- | ----------- |
| `oauthServerUrl` | String! |    |
| `clientId` | String! |      |
| `clientSecret` | String! |    |
| `imsOrgId` | String! | Die IMS-Organisation, für die AEM Assets und Adobe Commerce bereitgestellt wurden. |

#### MatchBySkuRuleInput

| Feld | Datentyp | Beschreibung |
| ----- | --------- | ----------- |
| metadataField | String! | Geben Sie das Asset-Metadatenfeld an, das für die Zuordnung verwendet werden soll. Verwenden Sie `commerce:skus` |

#### RuleInput

Gibt die passende Regel zum Synchronisieren von Assets zwischen Adobe Commerce und AEM Assets an.

| Feld | Datentyp | Beschreibung |
| ----- | --------- | ----------- |
| externalMatcher | [ExternalMatcherInput](#externalmatcherinput) | Wählt die Regel externalMatcher für die Asset-Zuordnung aus und legt die Daten fest, die erforderlich sind, um sie zu verwenden. |
| MatchBySkuRule | [MatchBySkuRuleInput](#matchbyskuruleinput) | Wählt die MatchBySkuRule für die Asset-Übereinstimmung aus und gibt die Daten an, die erforderlich sind, um sie zu verwenden. |

#### RuleTypeInput

| Feld | Datentyp | Beschreibung |
| ----- | --------- | ----------- |
| RuleType | enum | Gibt eine Liste der Asset-Übereinstimmungsregeln an, die für die AEM Assets-Integration für Commerce verfügbar sind. Verfügbare Werte sind `matchBySKU` oder `externalMatcher`. |

#### TenantInput

| Feld | Datentyp | Beschreibung |
| ----- | --------- | ----------- |
| `aem` | [AEMInput!](#aeminput) | Identifiziert die AEM Assets-Instanz in der AEM Cloud Service, in der Sie die Commerce-Assets speichern. |
| `commerce` | [CommerceInput!](#commerceinput) | Bietet Commerce-Projektinformationen und Anmeldeinformationen für den API-Zugriff |
| `enabled` | Boolesch! | Aktivieren oder deaktivieren Sie die Asset-Synchronisierung zwischen Adobe Commerce und AEM Assets. |
| `projectId` | String! | Die SaaS-Projekt-ID aus der Konfiguration [Commerce Services Connector-SaaS-ID](aem-assets-configure-commerce.md#configure-the-commerce-services-connector). |
| `rule` | [RuleInput!](#ruleinput) | Gibt die passende Regel zum Synchronisieren von Assets zwischen Adobe Commerce und AEM Assets an. Geben Sie entweder `[matchBySkuRule](#matchbyskuruleinput)` oder `[externalMatcher](#externalmatcherinput)` an. |

### Ausgabefelder

| Feld | Datentyp | Beschreibung |
| ----- | --------- | ----------- |
| data | [registerTenant] | Gibt die Registrierungsinformationen des Mandanten sowie alle Fehlermeldungen vom Server zurück. |

#### RegisterTenantResponse

| Feld | Datentyp | Beschreibung |
| ----- | --------- | ----------- |
| tenantId | String! | Gibt die registrierte Mandanten-ID zurück. Diese ID stellt sicher, dass Daten für die AEM Assets-Integration für Commerce aus dem SaaS-Datenraum gespeichert und abgerufen werden, der mit der Commerce-Umgebung verknüpft ist. |
| userErrors | [[userError!]!](#usererror) | Gibt von der Anfrage erzeugte Fehlermeldungen zurück. |

#### UserError

| Fehler | Beschreibung |
|:------|:------------|
| `IMS Org ID not associated to this Commerce` | Dieser Fehler tritt auf, wenn die in der Kopfzeile `Magento-Environment-Id` angegebene Umgebungs-ID nicht dem IMS-Konto zugewiesen ist. Dieser Fehler kann auftreten, da das IMS-Konto nicht verbunden war, als der [Commerce Services Connector](aem-assets-configure-commerce.md#configure-the-commerce-services-connector) für die Commerce-Instanz konfiguriert wurde. |
| `Client ID is invalid` | Die Kopfzeile `x-api-key` ist falsch. |
| `Client ID is missing` | Die Kopfzeile `x-api-key` wurde nicht bereitgestellt. |
| `JWT is required` | Die Kopfzeile `x-gw-signature` wurde nicht bereitgestellt. |
| `JWT is invalid` | Die Kopfzeile `x-gw-signature` wurde nicht bereitgestellt. |
| `Tenant already exists` | Ein Mandant mit den angegebenen `mageID` (aus dem JWT-Token genommen) und `saasId` (bereitgestellt von der `Magento-Environment-Id` -Kopfzeile) wurde bereits registriert. |
| `Unexpected error when connecting with AEM Assets` | Dieser Fehler tritt aufgrund ungültiger oder nicht vorhandener `programId` - oder `environmentId` -Werte auf. |
| `Unable to connect with AEM Assets` | Es gibt zwei mögliche Gründe für diesen Fehler:<br>1. Das AEM Asset-Konto ist mit einer anderen IMS-Organisations-ID als der für Adobe Commerce bereitgestellten verknüpft.<br>2. Die `commerce:isCommerce` -Metadaten sind nicht in AEM Assets vorhanden und geben an, dass keine genehmigten Assets von AEM Assets an die Commerce-Instanz gesendet werden können. |
| `Unexpected error when connecting with Commerce` | Dieser Fehler tritt auf, wenn ein ungültiger Commerce-Wert `baseURL` angegeben wird. |
| `Unable to connect with Commerce, unauthorized` | Es wurden ungültige Commerce-Anmeldedaten bereitgestellt, was zu einem unbefugten Zugriff führte. |
| `Invalid rule. The value must be matchBySKU or externalMatcher` | Das Feld `Rule` enthält einen falschen Wert. Für die Request RegisterTenant werden die verfügbaren Regeltypen durch den Enum [RuleTypeInput](#ruletypeinput) definiert. |

## Experience Manager Assets-Integration aktivieren

Nach der Registrierung des Mandanten wird die Experience Manager Assets Integration für Commerce-Erweiterung im letzten Schritt des Onboarding-Prozesses in Admin aktiviert.

1. Aktivieren Sie die Erweiterung.

   1. Navigieren Sie zu **Stores** > Einstellungen > **Konfiguration** > **Katalog**.

   1. Öffnen Sie die Katalogkonfiguration durch Auswahl von **[!UICONTROL Catalog]**.

   1. Erweitern Sie **[!UICONTROL AEM Assets integration]**.

   1. Setzen Sie **[!UICONTROL Integration enabled]** auf `yes`.

      ![AEM Assets-Integration für die Commerce-Admin-Konfiguration](assets/aem-integration-admin-enable.png){width="600" zoomable="yes"}
