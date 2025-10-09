---
title: '[!DNL Audience Activation]'
description: Erfahren Sie, wie Sie Real-Time CDP-Zielgruppen in Adobe Commerce aktivieren, um die Personalisierung in Ihrem Store zu fördern.
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 5929a2ff26dadda40ecfa9e435a73343caef3cde
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 1%

---

# [!DNL Audience Activation]

Mit der [!DNL Audience Activation]-Erweiterung können Sie Real-Time CDP-Zielgruppen in Adobe Commerce aktivieren, um individuelle Angebote im Warenkorb zu erstellen. Zu diesen Angeboten und Incentives gehören gängige E-Commerce-Merchandising-Techniken wie _Buy 2 get 1 free_, Hero-Banner, die auf diesen Kunden zugeschnitten sind, und modifizierte Produktpreise durch verschiedene Angebote. Die in Real-Time CDP erstellten Zielgruppen basieren auf Daten aus verschiedenen Unternehmenssystemen, z. B. Enterprise Resource Planning (ERP), Customer Relationship Management (CRM), Point-of-Sale und Marketing-Systemen. Da Kundensegmentinformationen ständig aktualisiert werden, können Kunden mit einem Segment verknüpft und von ihm getrennt werden, wenn sie in Ihrem Geschäft einkaufen.

Sie können Zielgruppen in einer Luma-Storefront oder einer [Headless](#headless-support)-Storefront aktivieren. In einer Luma-Storefront werden Zielgruppeninformationen (Segmentzugehörigkeit) in einem Cookie auf der Commerce-Seite gespeichert. In einer Headless-Storefront werden Zielgruppeninformationen im GraphQL-API-Header als Parameter mit dem Namen `aep-segments-membership` übergeben.

## Versionshinweise

Dieser Abschnitt enthält Informationen zu Aktualisierungen der Audience Activation-Erweiterung und umfasst:

![Neu](../assets/new.svg) - Neue Funktionen
![Fehlerbehebung](../assets/fix.svg) - Fehlerbehebungen und Verbesserungen
![Bug](../assets/bug.svg) - Bekannte Probleme

Unter [Kommende Versionen](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) erfahren Sie mehr über Versionspläne und Support.

Weitere Informationen zur Produktkompatibilität finden [&#x200B; in der Entwicklerdokumentation &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html).

## Unterstützte Service-Updates

In diesen Versionshinweisen werden Funktionsänderungen und Fehlerbehebungen im Zusammenhang mit den von Audience Activation verwendeten Erweiterungen beschrieben.

+++Unterstützte Service-Updates

_15. August 2023_

![Korrigieren](../assets/fix.svg) - Das Dashboard [Real-Time CDP-Zielgruppen](#real-time-cdp-audiences-dashboard) wurde aktualisiert, um die Filterung zu vereinfachen.

_27. Juni 2023_

![Fix](../assets/fix.svg) - Unterstützung für PHP 8.2 im `magento/module-data-services-graphql`-Paket wurde hinzugefügt.

_30. Mai 2023_

![Neu](../assets/new.svg) - Das Dashboard [Real-Time CDP-Zielgruppen](#real-time-cdp-audiences-dashboard) wurde aktualisiert, um die Möglichkeit zum Sortieren, Suchen und Filtern der aktiven Zielgruppen in Ihrer Adobe Commerce-Instanz einzuschließen.

+++

### 2,4,0

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"} Adobe Commerce-Versionen 2.4.4 und höher

_24. März 2025_

![Neu](../assets/new.svg) - PHP 8.4-Unterstützung hinzugefügt.

### 2,3,1

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"} Adobe Commerce-Versionen 2.4.4 und höher

_12. November 2024_

![Korrigieren](../assets/fix.svg) - Es wurde ein Problem beim Filtern der verfügbaren Real-Time CDP-Zielgruppen zur Auswahl behoben.

### 2,3,0

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"} Adobe Commerce-Versionen 2.4.4 und höher

_29. Juli 2024_

![Neu](../assets/new.svg) - Es wurde eine Befehlszeilensyntax hinzugefügt, mit der Sie [Anmeldedaten testen](#validate-the-connection) um festzustellen, ob sie aktualisiert werden müssen, um Zielgruppendaten aus Adobe Experience Platform abzurufen.

### 2,2,0

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"} Adobe Commerce-Versionen 2.4.4 und höher

_12. Juni 2024_

![Neu](../assets/new.svg) - GA-Version für [Produktregeln](../merchandising-promotions/product-related-rule-create.md) mit Informationen von Zielgruppen.

### 2.1.1

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"} Adobe Commerce-Versionen 2.4.4 und höher

_4. April 2024_

![Neu](../assets/new.svg) - PHP 8.3 wird nun unterstützt.

### 2.2.0-beta1

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"} Adobe Commerce-Versionen 2.4.4 und höher

_16. Februar 2024_

![Neu](../assets/new.svg) - Wenn Sie die Betaversion verwenden, stellen Sie sicher, dass Ihre `composer.json`-Datei auf der Stammebene Folgendes enthält: ` "minimum-stability": "beta"`.
![Neu](../assets/new.svg) - (**Beta**) Es besteht nun die Möglichkeit, [verwandte Produktregeln“ &#x200B;](../merchandising-promotions/product-related-rule-create.md) Zielgruppen zu erstellen.

### 2,1,0

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"} Adobe Commerce-Versionen 2.4.4 und höher

_24. Januar 2024_

![Neu](../assets/new.svg) - Das Dashboard [Real-Time CDP-Zielgruppen](#real-time-cdp-audiences-dashboard) wurde aktualisiert, um die Websites einzuschließen, die die Zielgruppen enthalten, und um anzugeben, welche dynamischen Blöcke und Warenkorbpreisregeln für die Verwendung dieser Zielgruppen konfiguriert sind.

### 2,0,1

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"} Adobe Commerce-Versionen 2.4.4 und höher

_16. November 2023_

![Fix](../assets/fix.svg) - Verbesserte Stabilität.

### 2,0,0

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"} Adobe Commerce-Versionen 2.4.4 und höher

_10. Oktober 2023_

![Neu](../assets/new.svg) - Es wurde Unterstützung für OAuth 2.0 beim [&#x200B; (Konfigurieren](#configure-the-extension) der Audience Activation-Erweiterung hinzugefügt.
![Fix](../assets/fix.svg) - Verbesserte Stabilität.

### 1,2,0

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"} Adobe Commerce-Versionen 2.4.4 und höher

_15. August 2023_

![Beheben](../assets/fix.svg) - Die Version der Benutzeroberflächenkomponenten wurde aktualisiert.

### 1,1,0

_30. Mai 2023_

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"} Adobe Commerce-Versionen 2.4.4 und höher

![Neu](../assets/new.svg) - Unterstützung für [dynamische Blöcke](#headless-support) in einer Headless-Storefront hinzugefügt.

### 1,0,1

_11. Mai 2023_

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"} Adobe Commerce-Versionen 2.4.4 und höher

![Beheben](../assets/fix.svg) - Es wurde ein Problem behoben, bei dem eine dynamische Block- oder Warenkorb-Preisregel nicht auf die Storefront angewendet wurde.
![Beheben](../assets/fix.svg) - Es wurde ein Problem behoben, bei dem eine nicht konfigurierte Installation der Audience Activation-Erweiterung einen Fehler verursachte, wenn ein Händler versuchte, einen dynamischen Block zu erstellen oder zu aktualisieren.

### 1,0,0

_31. März 2023_

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"} Adobe Commerce-Versionen 2.4.4 und höher

![Neu](../assets/new.svg) - Allgemeine Verfügbarkeitsversion

## Implementierung

Die folgenden Aufgaben gelten sowohl für Luma- als auch für Headless-Storefront-Implementierungen. Zum Aktivieren von Zielgruppen in Adobe Commerce ist Folgendes erforderlich:

- Installieren Sie Adobe Commerce Version 2.4.4 oder höher
- [Aktivieren](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce als Ziel in Real-Time CDP
- [Installieren](#install-the-extension) Sie die [!DNL Audience Activation]-Erweiterung in der Admin Console.
- [Konfigurieren](#configure-the-extension) der [!DNL Audience Activation]-Erweiterung in der Admin Console

### Installieren der Erweiterung

Installieren Sie die [!DNL Audience Activation]-Erweiterung über [Marketplace](https://commercemarketplace.adobe.com/magento-audiences.html) oder führen Sie den folgenden Befehl aus:

```bash
composer require magento/audiences
```

### Konfigurieren der Erweiterung

Nachdem Sie die [!DNL Audience Activation]-Erweiterung installiert haben, müssen Sie sich bei Ihrem Commerce-Administrator anmelden und Folgendes ausführen:

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**.

1. [Melden Sie sich bei &#x200B;](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html#organizationid) Adobe-Konto an und wählen Sie Ihre Organisations-ID aus.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**.

1. Fügen Sie im Feld **[!UICONTROL Datastream ID]** die ID des Datenstroms ein, den Sie beim Aktivieren [&#x200B; Adobe Commerce &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) Ziel in Real-Time CDP erstellt haben.

   Dieser Datenstrom sendet Daten von Ihrer Commerce-Website an Real-Time CDP, um festzustellen, ob ein Erstkäufer zu einer Zielgruppe gehört. Wenn Sie noch keinen Datenstrom erstellt haben, [&#x200B; Sie &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) Datenstrom in Experience Platform [hinzufügen](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) zum Commerce-Ziel in Real-Time CDP und zur [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html#data-collection)-Erweiterung in der Admin.

   >[!NOTE]
   >
   >Wenn Sie eine Datenstrom-ID angeben[&#x200B; verknüpfen Sie sie mit einer bestimmten Website &#x200B;](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html#data-collection) der [!DNL Data Connection]. Wenn Ihr Commerce-Store über mehrere Websites verfügt[&#x200B; erstellen Sie &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) für jede Website in Real-Time CDP ein Ziel und verwenden Sie für jede eine andere Datenstrom-ID.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie **[!UICONTROL Services]** und wählen Sie **[!UICONTROL [!DNL Data Connection]]**.

1. [Hinzufügen](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html#add-service-account-and-credential-details) Details zum Service-Konto und den Anmeldedaten.

## Verwendung von Real-Time CDP-Zielgruppen in Commerce

Wenn die [!DNL Audience Activation] aktiviert ist, können Sie:

- [Erstellen einer Warenkorb-Preisregel](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) informiert durch Zielgruppen
- [Erstellen eines dynamischen Blocks](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) basierend auf Audiences
- [Erstellen einer zugehörigen Produktregel](../merchandising-promotions/product-related-rule-create.md) informiert durch Zielgruppen

>[!TIP]
>
>Einen vollständigen Anwendungsfall zum Exportieren von [!DNL Commerce] nach Real-Time CDP, Erstellen einer Zielgruppe und anschließendem Aktivieren dieser Zielgruppe für die [!DNL Commerce] finden Sie unter &quot;[&#x200B; einer Zielgruppe in Real-Time CDP mithilfe von  [!DNL Commerce] -Ereignisdaten](https://experienceleague.adobe.com/en/docs/commerce/data-connection/use-cases/create-audience).

## Real-Time CDP-Zielgruppen-Dashboard

Sie können alle [aktiven](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) Zielgruppen anzeigen, die in Ihrer Adobe Commerce-Instanz mithilfe des Dashboards **Real-Time CDP-Zielgruppen** personalisiert werden können.

Um auf das Dashboard **Real-Time CDP** Zielgruppen zuzugreifen, gehen Sie zur Seitenleiste _Admin_ und dann zu **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**.

![Real-Time CDP-Zielgruppen-Dashboard](./assets/real-time-cdp-dashboard.png){width="700" zoomable="yes"}

Das Dashboard enthält die folgenden Felder:

| Spalte | Beschreibung |
|--- |--- |
| `Hide filters` | Hiermit können Sie alle Filter ein- oder ausblenden, die Sie auf das Dashboard anwenden können. Derzeit ist der einzige Filter, den Sie anwenden können, `Last updated`. Mit diesem Filter können Sie einen Datumsbereich für Zielgruppen basierend auf dem Zeitpunkt ihrer letzten Aktualisierung auswählen. |
| `Search` | Ermöglicht die Suche nach aktiven Zielgruppen in Ihrer Commerce-Instanz. |
| `Name` | Name, der der Zielgruppe in Real-Time CDP zugewiesen wurde. |
| `Origin` | Gibt an, woher die Zielgruppe stammt, z. B. `Experience Platform`. |
| `Websites` | Gibt an, welche Websites für die Verwendung der Zielgruppen konfiguriert sind. |
| `Dynamic Blocks` | Gibt an, welche dynamischen Blöcke für die Verwendung der Zielgruppen konfiguriert sind. |
| `Cart Price Rules` | Gibt an, welche Warenkorbpreisregeln für die Verwendung der Zielgruppen konfiguriert sind. |
| `Related Product Rules` | Gibt an, welche zugehörigen Produktregeln für die Verwendung der Zielgruppen konfiguriert sind. |
| `Last updated` | Gibt an, wann die Zielgruppe in Real-Time CDP geändert wurde. |
| `Sync now` | Ruft neue oder aktualisierte Zielgruppen aus Real-Time CDP ab. |
| `Customize table` | Ermöglicht das Ein- oder Ausblenden der Spalten `Origin`, `Websites`, `Dynamic Blocks`, `Cart Price Rules` und `Last updated`. |

{style="table-layout:auto"}

## Headless-Unterstützung

Sie können Zielgruppen in einer Headless-Adobe Commerce-Instanz wie AEM und PWA aktivieren, um Warenkorbpreisregeln, zugehörige Produktregeln oder dynamische Blöcke basierend auf den Zielgruppen anzuzeigen.

### Regeln für Warenkorbpreise und zugehörige Produkte

Für Regeln zum Warenkorbpreis und zugehörige Produktregeln kommuniziert eine Headless-Storefront über die [Commerce integration framework (CIF) mit der Experience Platform](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). Das Framework bietet eine Server-seitige API, die mithilfe von GraphQL implementiert wird. Zielgruppeninformationen, wie z. B. das Segment eines Käufers, werden über einen GraphQL-Kopfzeilenparameter namens `aep-segments-membership` an Commerce übergeben.

Die Gesamtarchitektur sieht wie folgt aus:

![Senden von Daten von der Headless-Storefront an das Backend](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

Nach dem [Installieren](#install-the-extension) und [Konfigurieren](#configure-the-extension) der Erweiterung enthält die Experience Platform Web SDK die Zielgruppeninformationen in Form von Segmentzugehörigkeit.

Informationen zum Erfassen dieser Segmentzugehörigkeiten aus der SDK finden Sie in diesem [Code-Snippet](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

Nach dem Abrufen können Sie diese Segmente im GraphQL-Header an Commerce übergeben. Beispiel:

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### Dynamische Blöcke

Bei dynamischen Blöcken können GraphQL-`dynamicBlocks`-Abfragen das `audience_id` Eingabeattribut enthalten. Wenn Sie einen oder mehrere `audience_id` Werte in einer `dynamicBlocks` Abfrage angeben, wird eine Liste der dynamischen Blöcke zurückgegeben, die diesen Zielgruppen zugewiesen sind.

#### Beispielverwendung

Die folgende Abfrage gibt alle dynamischen Blöcke zurück, die mit mehreren Zielgruppen-IDs verknüpft sind.

**Anfrage:**

```graphql
{
  dynamicBlocks(input:
  {
    type: SPECIFIED
    audience_id: {
      in: [
        "cd29a789-9be8-40ad-a1ef-640c33b3742e"
        "92c3e14d-c72b-40d0-96b7-b96801dcc135"
      ]
    }
  })
  {
    items {
      uid
      audience_id
      content {
        html
      }
    }
    page_info {
      current_page
      page_size
      total_pages
    }
    total_count
  }
}
```

**Antwort:**

```json
{
  "data": {
    "dynamicBlocks": {
      "items": [
        {
          "uid": "MQ==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e"
          ],
          "content": {
            "html": "<h2><strong>SAVE 20%</strong></h2>\r\n<p>(some restrictions apply)</p>\r\n<p>&nbsp;</p>"
          }
        },
        {
          "uid": "Mg==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e",
            "92c3e14d-c72b-40d0-96b7-b96801dcc135"
          ],
          "content": {
            "html": "<p><img src=\"{{media url=&quot;wysiwyg/save20.png&quot;}}\" alt=\"save 20% red\"></p>"
          }
        }
      ],
      "page_info": {
        "current_page": 1,
        "page_size": 20,
        "total_pages": 1
      },
      "total_count": 2
    }
  }
}
```

Weitere Informationen zur `dynamicBlocks` GraphQL-Abfrage finden Sie in der [Entwicklerdokumentation](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/).

## Abrufen von Zielgruppen mit der Adobe Experience Platform Mobile SDK

Sie können Real-Time CDP-Zielgruppen mit der Mobile SDK von Adobe Experience Platform abrufen.

1. [Installieren](#install-the-extension) der Audience Activation-Erweiterung.
1. [Installieren und konfigurieren Sie die SDK für Ihre mobile Commerce-Site](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/mobile-sdk-epc.html).

>[!IMPORTANT]
>
>Adobe Experience Platform Mobile SDK für iOS unterstützt iOS 11 oder höher.

Verwenden Sie nach Abschluss der Konfiguration mobile SDK-Vorgänge, um die Zielgruppendaten abzurufen. Beispiel:

```swift
Edge.sendEvent(experienceEvent: experienceEvent) { (handles: [EdgeEventHandle]) in
    for handle in handles {
        if handle.type == "activation:pull" {
        let payloadItems = handle.payload ?? []
            for payloadItem in payloadItems {
                if let segments = payloadItem["segments"] as? any Sequence {
                    var segmentsArr = [Any]()
                    for segment in segments {
                        let response = segment as AnyObject?
                        segmentsArr.append(response?.object(forKey: "id")! ?? "")
                    }
                    print("Saving segments ->  \(segments)")
                    storage.set(segmentsArr, forKey: "segments")
                    print("End saving segments")
                }
         
                // Show segments
                let rSegments = storage.object(forKey: "segments") ?? nil;
                print("Retrieving segments -> \(rSegments)")
            }
        }
    }
}
```

Nachdem die Daten abgerufen wurden, können Sie sie verwenden, um zielgruppenorientierte [Warenkorbpreisregeln](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences), [dynamische Blöcke](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) und [verwandte Produktregeln](../merchandising-promotions/product-related-rule-create.md) in der Commerce-App zu erstellen.

## Zielgruppen werden in Commerce nicht angezeigt

Wenn Real-Time CDP-Zielgruppen nicht in Commerce angezeigt werden, kann dies folgende Ursachen haben:

- Ungültige Verbindung
- Falscher Authentifizierungstyp auf der Konfigurationsseite **Datenverbindung** ausgewählt
- Unzureichende Berechtigungen für generiertes Token

In den folgenden Abschnitten wird beschrieben, wie Sie diese Probleme beheben können.

### Verbindung validieren

Führen Sie den folgenden Befehl aus, um die Anmeldeinformationen und die Antwort von Adobe Experience Platform zu überprüfen:

```bash
bin/magento audiences:config:status
```

Dieser Befehl gibt den Verbindungsstatus zurück. Fügen Sie das Flag `-v` hinzu, um eine zusätzliche Ausführlichkeit zu erzielen:

```
./bin/magento audiences:config:status -v  
```

Beispiel:

```
+----------------------------------+---------------+---------------------------------------------+---------------------------------------------------------+--------------+
| Client ID                        | Client secret | Technical account ID                        | Technical account email                                 | Sandbox name |
+----------------------------------+---------------+---------------------------------------------+---------------------------------------------------------+--------------+
| 1234bd57fac8497d8933327c535347d8 | *****         | 12341E116638D6B00A495C80@techacct.adobe.com | 12345-b95b-4894-a41c-a4130d26bd80@techacct.adobe.com | dev          |
```

### Falscher Authentifizierungstyp in Konfiguration ausgewählt

1. Öffnen Sie Ihre Commerce-Instanz.
1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. Erweitern Sie **[!UICONTROL Services]** und wählen Sie **[!UICONTROL [!DNL Data Connection]]**.
1. Stellen Sie sicher, dass die im Feld **[!UICONTROL Authentication Type]** angegebene Server-zu-Server-Autorisierungsmethode korrekt ist. Adobe empfiehlt die Verwendung von **OAuth**. JWT wird nicht mehr unterstützt. [Weitere Informationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).

### Unzureichende Berechtigungen für generiertes Token

Dieses Problem kann durch unzureichende API-Berechtigungen für das generierte Token verursacht werden. So stellen Sie sicher, dass das Token über die richtigen Berechtigungen verfügt:

1. Bestimmen Sie den Systemadministrator für Adobe Experience Platform in Ihrem Unternehmen.
1. Suchen Sie das Projekt und die Anmeldeinformationen, die Sie verwenden werden.
1. Identifizieren Sie die E-Mail-Adresse des technischen Kontos, zum Beispiel: `fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com`.
1. Bitten Sie den Systemadministrator, Adobe Experience Platform zu starten und zu **[!UICONTROL Permissions]** -> **[!UICONTROL Users]** -> **[!UICONTROL API credentials]** zu gehen.
1. Suchen Sie mithilfe der E-Mail-Adresse des technischen Kontos von oben nach den Anmeldedaten, die geändert werden sollen.
1. Öffnen Sie die Anmeldeinformationen und wählen Sie **[!UICONTROL Roles]** -> **[!UICONTROL Add roles]** aus.
1. Fügen Sie die Rolle hinzu, die **[!UICONTROL Manage destinations]** Berechtigung enthält.
1. Klicken Sie auf **[!UICONTROL Save]**.
1. [Erneutes &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html#generate-access-token) des Zugriffstokens in der Konsole.
1. Vergewissern Sie sich mithilfe der „Target Connections [&quot;, dass das Token eine gültige Antwort &#x200B;](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections).
