---
title: "[!DNL Audience Activation]"
description: Erfahren Sie, wie Sie Real-Time CDP-Zielgruppen in Adobe Commerce aktivieren, um die Personalisierung in Ihrem Store zu fördern.
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
source-git-commit: db8344ab8890c20bb0b3c7d25da95b6007858d6a
workflow-type: tm+mt
source-wordcount: '1409'
ht-degree: 0%

---

# [!DNL Audience Activation]

Die [!DNL Audience Activation] ermöglicht Ihnen die Aktivierung von Real-Time CDP-Zielgruppen in Adobe Commerce, um eindeutige Angebote im Warenkorb zu erstellen. Zu diesen Angeboten und Anreizen gehören gängige E-Commerce-Merchandising-Techniken wie _Kauf 2 erhalten 1 gratis_, Hero-Banner, die auf diesen Kunden ausgerichtet sind, und geänderte Produktpreise über verschiedene Angebote. Die in Real-Time CDP erstellten Zielgruppen basieren auf Daten aus verschiedenen Unternehmenssystemen, z. B. Enterprise Resource Planning (ERP), Customer Relationship Management (CRM), Point of Sale und Marketing-Systemen. Da Kundensegmentinformationen ständig aktualisiert werden, können Kunden beim Einkauf in Ihrem Geschäft mit einem Segment verknüpft und von diesem getrennt werden.

Sie können Zielgruppen in einer Luma-Storefront aktivieren oder [Headless](#headless-support) Storefront. In einer Luma-Storefront werden Zielgruppendaten (Segmentmitgliedschaft) in einem Cookie auf der Seite &quot;Commerce&quot;gespeichert. In einer Headless-Storefront werden Zielgruppendaten in der GraphQL-API-Kopfzeile als Parameter mit dem Namen übergeben: `aep-segments-membership`.

## Versionshinweise

Dieser Abschnitt enthält Informationen zu Aktualisierungen der Audience Activation-Erweiterung und umfasst:

![Neu](../assets/new.svg) - Neue Funktionen
![Fehlerbehebung](../assets/fix.svg) - Fehlerbehebungen und Verbesserungen
![Fehler](../assets/bug.svg) - Bekannte Probleme

Siehe [Bevorstehende Versionen](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) , um mehr über die Veröffentlichungszeitpläne und die Unterstützung zu erfahren.

Siehe die Entwicklerdokumentation zu [Informationen zur Produktkompatibilität](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html).

## Unterstützte Dienstaktualisierungen

In diesen Versionshinweisen werden Funktionsänderungen und Fehlerbehebungen im Zusammenhang mit von Audience Activation verwendeten Erweiterungen beschrieben.

+++Unterstützte Dienstaktualisierungen

_15. August 2023_

![Fehlerbehebung](../assets/fix.svg) - Die [Dashboard für Real-Time CDP-Zielgruppen](#real-time-cdp-audiences-dashboard) zur Vereinfachung der Filterung.

_27. Juni 2023_

![Fehlerbehebung](../assets/fix.svg) - Unterstützung für PHP 8.2 im `magento/module-data-services-graphql` Paket.

_30. Mai 2023_

![Neu](../assets/new.svg) - Die [Dashboard für Real-Time CDP-Zielgruppen](#real-time-cdp-audiences-dashboard) , um die Möglichkeit zur Sortierung, Suche und Filterung der aktiven Zielgruppen in Ihrer Adobe Commerce-Instanz einzuschließen.

+++

### 2.2.0-beta1

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

_16. Februar 2024_

![Neu](../assets/new.svg) - Wenn Sie an der Beta-Phase teilnehmen, stellen Sie sicher, dass Ihre `composer.json` -Datei hat Folgendes auf der Stammebene: ` "minimum-stability": "beta"`.
![Neu](../assets/new.svg) - (**Beta**) Zusätzliche Funktion zum Erstellen [verwandte Produktregeln](../merchandising-promotions/product-related-rule-create.md) durch Zielgruppen informiert werden.

### 2.1.0

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

_24. Januar 2024_

![Neu](../assets/new.svg) - Die [Dashboard für Real-Time CDP-Zielgruppen](#real-time-cdp-audiences-dashboard) , um die Websites einzubeziehen, die die Zielgruppen enthalten, und anzugeben, welche dynamischen Bausteine und Warenkorbpreisregeln für die Verwendung dieser Zielgruppen konfiguriert sind.

### 2,0,1

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

_16. November 2023_

![Fehlerbehebung](../assets/fix.svg) - Verbesserung der Stabilität.

### 2,0,0

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

_10. Oktober 2023_

![Neu](../assets/new.svg) - Unterstützung für OAuth 2.0 bei [konfigurieren](#configure-the-extension) die Audience Activation-Erweiterung.
![Fehlerbehebung](../assets/fix.svg) - Verbesserung der Stabilität.

### 1,2,0

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

_15. August 2023_

![Fehlerbehebung](../assets/fix.svg) - Aktualisierung der Komponentenversion der Benutzeroberfläche.

### 1.1.0

_30. Mai 2023_

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

![Neu](../assets/new.svg) - Unterstützung für [dynamische Blöcke](#headless-support) in einer Headless-Storefront.

### 1,0,1

_11. Mai 2023_

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

![Fehlerbehebung](../assets/fix.svg) - Es wurde ein Problem behoben, bei dem eine dynamische Block- oder Warenkorbpreisregel nicht auf die Storefront angewendet wurde.
![Fehlerbehebung](../assets/fix.svg) - Es wurde ein Problem behoben, bei dem eine nicht konfigurierte Installation der Audience Activation-Erweiterung einen Fehler verursachte, wenn ein Händler versuchte, einen dynamischen Block zu erstellen oder zu aktualisieren.

### 1,0,0

_31. März 2023_

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

![Neu](../assets/new.svg) - Allgemeine Verfügbarkeitsversion

## Implementierung

Die folgenden Aufgaben gelten sowohl für die Implementierung von Luma als auch für die Implementierung von Headless-Storefront. Um Zielgruppen in Adobe Commerce zu aktivieren, müssen Sie:

- Installieren Sie Adobe Commerce-Version 2.4.4 oder höher
- [Aktivieren](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce als Ziel in Real-Time CDP
- [Installieren](#install-the-extension) die [!DNL Audience Activation] Erweiterung in der Admin-Konsole
- [Konfigurieren](#configure-the-extension) die [!DNL Audience Activation] Erweiterung in der Admin-Konsole

### Installieren der Erweiterung

Installieren Sie die [!DNL Audience Activation] -Erweiterung aus der [Marketplace](https://commercemarketplace.adobe.com/magento-audiences.html)oder führen Sie den folgenden Befehl aus:

```bash
composer require magento/audiences
```

### Konfigurieren der Erweiterung

Nach der Installation [!DNL Audience Activation] müssen Sie sich bei Ihrem Commerce Admin anmelden und Folgendes ausführen:

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**.

1. [Anmelden](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#organizationid) auf Ihr Adobe-Konto klicken und Ihre Organisations-ID auswählen.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**.

1. Im **[!UICONTROL Datastream ID]** -Feld die Kennung des von Ihnen erstellten Datastreams ein. [enabled](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) Adobe Commerce als Ziel in Real-Time CDP.

   Dieser Datastream sendet Daten von Ihrer Commerce-Website an Real-Time CDP, um festzustellen, ob ein Käufer zu einer Zielgruppe gehört. Wenn Sie noch keinen Datastream erstellt haben, [erstellen](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) eine in Experience Platform, [add](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) an das Commerce-Ziel in Real-Time CDP und an die [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) -Erweiterung in Admin.

   >[!NOTE]
   >
   >Wenn Sie eine Datastream-ID angeben, müssen Sie [Zuordnung zu einer bestimmten Website](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) im [!DNL Data Connection] -Erweiterung. Wenn Ihr Commerce-Store über mehrere Websites verfügt, [Ziel erstellen](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) für jede Website in Real-Time CDP verwenden und jeweils eine andere Datastream-ID verwenden.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern **[!UICONTROL Services]** und wählen **[!UICONTROL [!DNL Data Connection]]**.

1. [Hinzufügen](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#add-service-account-and-credential-details) Dienstkonto und Anmeldedaten.

## Verwendung von Real-Time CDP-Zielgruppen in Commerce

Mit dem [!DNL Audience Activation] -Erweiterung aktiviert haben, können Sie:

- [Erstellen einer Preisregel für den Warenkorb](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) durch Zielgruppen informiert
- [Dynamischen Baustein erstellen](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) durch Zielgruppen informiert
- [(**Beta**) Erstellen einer verwandten Produktregel](../merchandising-promotions/product-related-rule-create.md) durch Zielgruppen informiert

## Dashboard für Real-Time CDP-Zielgruppen

Alle [active](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) Zielgruppen, die in Ihrer Adobe Commerce-Instanz mithilfe der **Real-Time CDP-Zielgruppen** Dashboard.

So greifen Sie auf die **Real-Time CDP-Zielgruppen** Dashboard, navigieren Sie zum _Admin_ Seitenleiste, dann zu **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**.

![Dashboard für Real-Time CDP-Zielgruppen](./assets/real-time-cdp-dashboard.png){width="700" zoomable="yes"}

Das Dashboard enthält die folgenden Felder:

| Spalte | Beschreibung |
|--- |--- |
| `Hide filters` | Ermöglicht das Anzeigen oder Verbergen von Filtern, die Sie auf das Dashboard anwenden können. Derzeit ist der einzige Filter, den Sie anwenden können `Last updated`. Mit diesem Filter können Sie einen Datumsbereich für Zielgruppen auswählen, basierend auf dem Zeitpunkt der letzten Aktualisierung. |
| `Search` | Ermöglicht die Suche nach aktiven Zielgruppen in Ihrer Commerce-Instanz. |
| `Name` | Name der Audience in Real-Time CDP. |
| `Origin` | Gibt an, woher die Zielgruppe stammt, beispielsweise `Experience Platform`. |
| `Websites` | Gibt an, welche Websites für die Verwendung der Zielgruppen konfiguriert sind. |
| `Dynamic Blocks` | Gibt an, welche dynamischen Blöcke für die Verwendung der Zielgruppen konfiguriert sind. |
| `Cart Price Rules` | Gibt an, welche Regeln für den Warenkorbpreis für die Verwendung der Zielgruppen konfiguriert sind. |
| `Last updated` | Gibt an, wann die Zielgruppe in Real-Time CDP geändert wurde. |
| `Sync now` | Ruft neue oder aktualisierte Zielgruppen aus Real-Time CDP ab. |
| `Customize table` | Ermöglicht das Anzeigen oder Verbergen der `Origin`, `Websites`, `Dynamic Blocks`, `Cart Price Rules`, und `Last updated` Spalten. |

{style="table-layout:auto"}

## Headless-Unterstützung

Sie können Zielgruppen in einer Headless-Adobe Commerce-Instanz aktivieren, z. B. AEM und PWA, um Warenkorbpreisregeln, zugehörige Produktregeln oder dynamische Bausteine basierend auf den Zielgruppen anzuzeigen.

### Preisregeln für Warenkorb und zugehörige Produktregeln

Bei Warenkorbpreisregeln und damit zusammenhängenden Produktregeln kommuniziert eine Headless-Storefront über die [Commerce integration framework (CIF)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). Das Framework stellt eine serverseitige API bereit, die mithilfe von GraphQL implementiert wird. Zielgruppendaten wie das Segment eines Käufers werden über einen GraphQL-Header-Parameter mit dem Namen an Commerce übergeben: `aep-segments-membership`.

Die Gesamtarchitektur sieht wie folgt aus:

![Senden von Daten von Headless-Storefront an Backend](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

Nach [install](#install-the-extension) und [konfigurieren](#configure-the-extension) In der -Erweiterung enthält das Experience Platform Web SDK die Zielgruppeninformationen in Form einer Segmentmitgliedschaft.

Informationen zum Erfassen dieser Segmentmitgliedschaften vom SDK finden Sie in diesem [Codeausschnitt](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

Nachdem sie abgerufen wurde, können Sie diese Segmente im GraphQL-Header an Commerce übergeben. Beispiel:

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### Dynamische Blöcke

Bei dynamischen Bausteinen: GraphQL `dynamicBlocks` -Abfragen können `audience_id` Eingabeattribut. Wenn Sie eine oder mehrere `audience_id` Werte in einer `dynamicBlocks` -Abfrage eine Liste mit dynamischen Bausteinen zurückgibt, die diesen Zielgruppen zugewiesen sind.

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

Weitere Informationen zum `dynamicBlocks` GraphQL-Abfrage im [Entwicklerdokumentation](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/).

## Abrufen von Zielgruppen mit dem Adobe Experience Platform Mobile SDK

Bevor Sie Real-Time CDP-Zielgruppen mit dem Adobe Experience Platform Mobile SDK abrufen können, müssen Sie Folgendes tun: [SDK für Ihre mobile Commerce-Site installieren und konfigurieren](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/mobile-sdk-epc.html).

>[!IMPORTANT]
>
>Das Adobe Experience Platform Mobile SDK für iOS unterstützt iOS 11 oder höher.

Nachdem Sie die Konfiguration abgeschlossen haben, verwenden Sie mobile SDK-Vorgänge zum Abrufen der Zielgruppendaten. Beispiel:

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

Nachdem die Daten abgerufen wurden, können Sie sie verwenden, um zielgruppeninformierte [Warenkorbpreisregeln](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences), [dynamische Blöcke](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) und  [verwandte Produktregeln](../merchandising-promotions/product-related-rule-create.md) in der Commerce-App.

## Zielgruppen werden nicht in Commerce angezeigt

Wenn Real-Time CDP-Zielgruppen nicht in Commerce angezeigt werden, kann dies folgende Gründe haben:

- Falscher Authentifizierungstyp, der in der **Datenverbindung** Konfigurationsseite
- Unzureichende Berechtigungen für generiertes Token

In den folgenden beiden Abschnitten wird beschrieben, wie Sie in beiden Fällen eine Fehlerbehebung durchführen.

### Falscher Authentifizierungstyp in der Konfiguration ausgewählt

1. Öffnen Sie Ihre Commerce-Instanz.
1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. Erweitern **[!UICONTROL Services]** und wählen **[!UICONTROL [!DNL Data Connection]]**.
1. Stellen Sie sicher, dass die von Ihnen in der Variablen **[!UICONTROL Authentication Type]** korrekt ist. Adobe empfiehlt, **OAuth**. JWT ist veraltet. [Weitere Infos](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).

### Unzureichende Berechtigungen für generiertes Token

Dieses Problem kann durch unzureichende API-Berechtigungen für das generierte Token verursacht werden. So stellen Sie sicher, dass das Token über die richtigen Berechtigungen verfügt:

1. Identifizieren Sie den Systemadministrator für Adobe Experience Platform in Ihrem Unternehmen.
1. Suchen Sie das Projekt und die Anmeldeinformationen, die Sie verwenden werden.
1. Geben Sie die E-Mail-Adresse des technischen Kontos an, z. B.: `fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com`.
1. Lassen Sie den Systemadministrator Adobe Experience Platform starten und navigieren Sie zu **[!UICONTROL Permissions]** -> **[!UICONTROL Users]** -> **[!UICONTROL API credentials]**.
1. Suchen Sie mithilfe der E-Mail-Adresse des technischen Kontos oben nach den zu ändernden Anmeldeinformationen.
1. Öffnen Sie die Anmeldeinformationen und wählen Sie **[!UICONTROL Roles]** -> **[!UICONTROL Add roles]**.
1. Hinzufügen **Zugriff auf alle Produktionen**.
1. Klicks **[!UICONTROL Save]**.
1. [Regenerieren](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html#generate-access-token) das Zugriffstoken in der Konsole.
1. Stellen Sie sicher, dass das Token eine gültige Antwort mit der [Target-Verbindungs-API](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections).
