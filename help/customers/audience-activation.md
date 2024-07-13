---
title: "[!DNL Audience Activation]"
description: Erfahren Sie, wie Sie Real-Time CDP-Zielgruppen in Adobe Commerce aktivieren, um die Personalisierung in Ihrem Store zu fördern.
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
source-git-commit: c9eb7f2b0b28f39ee9039be1e0fba4fe282ba7b3
workflow-type: tm+mt
source-wordcount: '1482'
ht-degree: 0%

---

# [!DNL Audience Activation]

Mit der Erweiterung [!DNL Audience Activation] können Sie Real-Time CDP-Zielgruppen in Adobe Commerce aktivieren, um eindeutige Angebote im Warenkorb zu erstellen. Zu diesen Angeboten und Anreizen gehören gängige E-Commerce-Merchandising-Techniken, wie z. B. _Kauf 2 erhält 1 kostenlose_, Hero-Banner, die auf diesen Kunden ausgerichtet sind, und modifizierte Produktpreise über verschiedene Angebote. Die in Real-Time CDP erstellten Zielgruppen basieren auf Daten aus verschiedenen Unternehmenssystemen, z. B. Enterprise Resource Planning (ERP), Customer Relationship Management (CRM), Point of Sale und Marketing-Systemen. Da Kundensegmentinformationen ständig aktualisiert werden, können Kunden beim Einkauf in Ihrem Geschäft mit einem Segment verknüpft und von diesem getrennt werden.

Sie können Zielgruppen in einer Luma-Storefront oder einer [Headless](#headless-support) Storefront aktivieren. In einer Luma-Storefront werden Zielgruppendaten (Segmentzugehörigkeit) in einem Cookie auf Commerce-Seite gespeichert. In einer Headless-Storefront werden Zielgruppendaten in der GraphQL-API-Kopfzeile als Parameter mit dem Namen `aep-segments-membership` übergeben.

## Versionshinweise

Dieser Abschnitt enthält Informationen zu Aktualisierungen der Audience Activation-Erweiterung und umfasst:

![Neu](../assets/new.svg) - Neue Funktionen
![Korrektur](../assets/fix.svg) - Fehlerbehebungen und Verbesserungen
![Fehler](../assets/bug.svg) - Bekannte Probleme

Unter [Bevorstehende Versionen](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) erfahren Sie mehr über die Veröffentlichungszeitpläne und die Unterstützung.

Weitere Informationen zur Produktkompatibilität finden Sie in der Entwicklerdokumentation zu [.](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html)

## Unterstützte Dienstaktualisierungen

In diesen Versionshinweisen werden Funktionsänderungen und Fehlerbehebungen im Zusammenhang mit von Audience Activation verwendeten Erweiterungen beschrieben.

+++Unterstützte Dienstaktualisierungen

_15. August 2023_

![Fehlerbehebung](../assets/fix.svg) - Aktualisierung des Dashboards [Real-Time CDP-Zielgruppen](#real-time-cdp-audiences-dashboard) zur Vereinfachung der Filterung.

_27. Juni 2023_

![Korrektur](../assets/fix.svg) - Unterstützung für PHP 8.2 im `magento/module-data-services-graphql`-Paket hinzugefügt.

_30. Mai 2023_

![Neu](../assets/new.svg) - Das Dashboard [Real-Time CDP-Zielgruppen](#real-time-cdp-audiences-dashboard) wurde aktualisiert und bietet nun die Möglichkeit, die aktiven Zielgruppen in Ihrer Adobe Commerce-Instanz zu sortieren, zu suchen und zu filtern.

+++

### 2,2,0

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

_12. Juni 2024_

![Neu](../assets/new.svg) - GA-Version für [verwandte Produktregeln](../merchandising-promotions/product-related-rule-create.md), die von Zielgruppen informiert werden.

### 2.1.1

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

_4. April 2024_

![Neu](../assets/new.svg) - Unterstützung für PHP 8.3 hinzugefügt.

### 2.2.0-beta1

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

_16. Februar 2024_

![Neu](../assets/new.svg) - Wenn Sie an der Beta-Phase teilnehmen, stellen Sie sicher, dass Ihre `composer.json`-Datei auf der Stammebene Folgendes aufweist: ` "minimum-stability": "beta"`.
![Neu](../assets/new.svg) - (**Beta**) Es wurde die Möglichkeit hinzugefügt, durch Zielgruppen informierte [verwandte Produktregeln](../merchandising-promotions/product-related-rule-create.md) zu erstellen.

### 2.1.0

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

_24. Januar 2024_

![Neu](../assets/new.svg) - Das Dashboard [Real-Time CDP-Zielgruppen](#real-time-cdp-audiences-dashboard) wurde aktualisiert und enthält nun auch die Websites mit den Zielgruppen sowie die zur Verwendung dieser Zielgruppen konfigurierten dynamischen Bausteine und Warenkorbpreisregeln.

### 2,0,1

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

_16. November 2023_

![Fix](../assets/fix.svg) - Verbesserte Stabilität.

### 2,0,0

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

_10. Oktober 2023_

![Neu](../assets/new.svg) - Unterstützung für OAuth 2.0 wurde hinzugefügt, wenn Sie die Audience Activation-Erweiterung [konfigurieren](#configure-the-extension).
![Fix](../assets/fix.svg) - Verbesserte Stabilität.

### 1,2,0

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

_15. August 2023_

![Fehlerbehebung](../assets/fix.svg) - Aktualisierung der Komponentenversion der Benutzeroberfläche.

### 1.1.0

_30. Mai 2023_

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

![Neu](../assets/new.svg) - Unterstützung für [dynamische Blöcke](#headless-support) in einer Headless-Storefront hinzugefügt.

### 1,0,1

_11. Mai 2023_

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

![Korrektur](../assets/fix.svg) - Es wurde ein Problem behoben, bei dem keine dynamische Block- oder Warenkorbpreisregel auf die Storefront angewendet wurde.
![Korrektur](../assets/fix.svg) - Es wurde ein Problem behoben, bei dem eine nicht konfigurierte Installation der Audience Activation-Erweiterung einen Fehler verursachte, wenn ein Händler versuchte, einen dynamischen Block zu erstellen oder zu aktualisieren.

### 1,0,0

_31. März 2023_

[!BADGE Kompatibilität]{type=Informative tooltip="Kompatibilität"}

![Neu](../assets/new.svg) - Allgemeine Verfügbarkeitsversion

## Implementierung

Die folgenden Aufgaben gelten sowohl für die Implementierung von Luma als auch für die Implementierung von Headless-Storefront. Um Zielgruppen in Adobe Commerce zu aktivieren, müssen Sie:

- Installieren Sie Adobe Commerce-Version 2.4.4 oder höher
- [Aktivieren](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce als Ziel in Real-Time CDP
- [Installieren](#install-the-extension) Sie die Erweiterung [!DNL Audience Activation] im Admin
- [Konfigurieren Sie](#configure-the-extension) die Erweiterung [!DNL Audience Activation] im Admin

### Installieren der Erweiterung

Installieren Sie die Erweiterung [!DNL Audience Activation] vom [Marketplace](https://commercemarketplace.adobe.com/magento-audiences.html) oder führen Sie den folgenden Befehl aus:

```bash
composer require magento/audiences
```

### Konfigurieren der Erweiterung

Nach der Installation der Erweiterung [!DNL Audience Activation] müssen Sie sich bei Ihrem Commerce-Administrator anmelden und Folgendes ausführen:

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**.

1. [Melden Sie sich bei Ihrem Adobe-Konto an und wählen Sie Ihre Organisations-ID aus.](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#organizationid)

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**.

1. Fügen Sie im Feld **[!UICONTROL Datastream ID]** die ID des Datastreams ein, den Sie beim [Aktivieren](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) von Adobe Commerce als Ziel in Real-Time CDP erstellt haben.

   Dieser Datastream sendet Daten von Ihrer Commerce-Website an Real-Time CDP, um festzustellen, ob ein Käufer zu einer Zielgruppe gehört. Wenn Sie noch keinen Datastream erstellt haben, erstellen Sie [einen in der Experience Platform, [fügen Sie ](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) ihn zum Commerce-Ziel in Real-Time CDP und zur Erweiterung [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) im Admin hinzu.](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create)

   >[!NOTE]
   >
   >Wenn Sie eine Datastraam-ID angeben, verknüpfen Sie sie [mit einer bestimmten Website](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) in der Erweiterung [!DNL Data Connection] . Wenn Ihr Commerce-Store über mehrere Websites verfügt, erstellen Sie in Real-Time CDP für jede Website ein Ziel ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) und verwenden Sie für jede Website eine andere Datastraam-ID.[

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie **[!UICONTROL Services]** und wählen Sie **[!UICONTROL [!DNL Data Connection]]** aus.

1. [Fügen Sie das Dienstkonto und die Anmeldeinformationen hinzu.](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#add-service-account-and-credential-details)

## Verwendung von Real-Time CDP-Zielgruppen in Commerce

Wenn die [!DNL Audience Activation] -Erweiterung aktiviert ist, können Sie:

- [Erstellen einer Preisregel für den Warenkorb](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences), die von Zielgruppen informiert wird
- [Dynamischen Block erstellen](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks), der von Zielgruppen informiert wird
- [Erstellen einer verwandten Produktregel](../merchandising-promotions/product-related-rule-create.md), die von Zielgruppen informiert wird

>[!TIP]
>
>Ein vollständiges Nutzungsszenario zum Exportieren von [!DNL Commerce] -Daten in Real-Time CDP, Erstellen einer Zielgruppe und Aktivieren dieser Zielgruppe für [!DNL Commerce] finden Sie unter [Erstellen einer Zielgruppe in Real-Time CDP mithilfe von [!DNL Commerce] Ereignisdaten](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/create-audience).

## Dashboard für Real-Time CDP-Zielgruppen

Sie können alle [aktiven](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) Zielgruppen anzeigen, die in Ihrer Adobe Commerce-Instanz mithilfe des Dashboards **Real-Time CDP-Zielgruppen** personalisiert werden können.

Um auf das Dashboard **Real-Time CDP-Zielgruppen** zuzugreifen, wechseln Sie zur Seitenleiste _Admin_ und dann zu **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**.

![Real-Time CDP-Zielgruppen-Dashboard](./assets/real-time-cdp-dashboard.png){width="700" zoomable="yes"}

Das Dashboard enthält die folgenden Felder:

| Spalte | Beschreibung |
|--- |--- |
| `Hide filters` | Ermöglicht das Anzeigen oder Verbergen von Filtern, die Sie auf das Dashboard anwenden können. Derzeit ist der einzige Filter, den Sie anwenden können, `Last updated`. Mit diesem Filter können Sie einen Datumsbereich für Zielgruppen auswählen, basierend auf dem Zeitpunkt der letzten Aktualisierung. |
| `Search` | Ermöglicht die Suche nach aktiven Zielgruppen in Ihrer Commerce-Instanz. |
| `Name` | Name der Audience in Real-Time CDP. |
| `Origin` | Gibt an, woher die Zielgruppe stammt, z. B. `Experience Platform`. |
| `Websites` | Gibt an, welche Websites für die Verwendung der Zielgruppen konfiguriert sind. |
| `Dynamic Blocks` | Gibt an, welche dynamischen Blöcke für die Verwendung der Zielgruppen konfiguriert sind. |
| `Cart Price Rules` | Gibt an, welche Regeln für den Warenkorbpreis für die Verwendung der Zielgruppen konfiguriert sind. |
| `Related Product Rules` | Gibt an, welche verwandten Produktregeln für die Verwendung der Zielgruppen konfiguriert sind. |
| `Last updated` | Gibt an, wann die Zielgruppe in Real-Time CDP geändert wurde. |
| `Sync now` | Ruft neue oder aktualisierte Zielgruppen aus Real-Time CDP ab. |
| `Customize table` | Hiermit können Sie die Spalten `Origin`, `Websites`, `Dynamic Blocks`, `Cart Price Rules` und `Last updated` ein- oder ausblenden. |

{style="table-layout:auto"}

## Headless-Unterstützung

Sie können Zielgruppen in einer Headless-Adobe Commerce-Instanz aktivieren, z. B. AEM und PWA, um Warenkorbpreisregeln, zugehörige Produktregeln oder dynamische Bausteine basierend auf den Zielgruppen anzuzeigen.

### Preisregeln für Warenkorb und zugehörige Produktregeln

Bei Warenkorbpreisregeln und damit zusammenhängenden Produktregeln kommuniziert eine Headless-Storefront über die [Commerce integration framework (CIF)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html) an die Experience Platform. Das Framework stellt eine serverseitige API bereit, die mithilfe von GraphQL implementiert wird. Zielgruppendaten wie das Segment eines Käufers werden über einen GraphQL-Header-Parameter mit dem Namen `aep-segments-membership` an Commerce übergeben.

Die Gesamtarchitektur sieht wie folgt aus:

![Senden von Daten von Headless-Storefront an Backend](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

Nachdem Sie die Erweiterung [install](#install-the-extension) und [configure](#configure-the-extension) installiert haben, enthält das Experience Platform Web SDK die Zielgruppeninformationen in Form einer Segmentmitgliedschaft.

Informationen zum Erfassen dieser Segmentmitgliedschaften vom SDK finden Sie in diesem [Codeausschnitt](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

Nachdem sie abgerufen wurde, können Sie diese Segmente im GraphQL-Header an Commerce übergeben. Beispiel:

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### Dynamische Blöcke

Bei dynamischen Bausteinen können GraphQL `dynamicBlocks`-Abfragen das Eingabeattribut `audience_id` enthalten. Wenn Sie in einer `dynamicBlocks` -Abfrage einen oder mehrere `audience_id` -Werte angeben, wird eine Liste mit dynamischen Bausteinen zurückgegeben, die diesen Zielgruppen zugewiesen sind.

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

Weitere Informationen zur Abfrage von `dynamicBlocks` GraphQL finden Sie in der [Entwicklerdokumentation](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/).

## Abrufen von Zielgruppen mit dem Adobe Experience Platform Mobile SDK

Sie können Real-Time CDP-Zielgruppen mit dem Adobe Experience Platform Mobile SDK abrufen.

1. [Installieren Sie](#install-the-extension) die Audience Activation-Erweiterung.
1. [Installieren und Konfigurieren des SDK für Ihre mobile Commerce-Site](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/mobile-sdk-epc.html).

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

Nachdem die Daten abgerufen wurden, können Sie sie verwenden, um zielgruppenbezogene [Warenkorbpreisregeln](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences), [dynamische Bausteine](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) und [zugehörige Produktregeln](../merchandising-promotions/product-related-rule-create.md) in der Commerce-App zu erstellen.

## Zielgruppen werden nicht in Commerce angezeigt

Wenn Real-Time CDP-Zielgruppen nicht in Commerce angezeigt werden, kann dies folgende Gründe haben:

- Falscher Authentifizierungstyp, der auf der Konfigurationsseite **Datenverbindung** ausgewählt wurde
- Unzureichende Berechtigungen für generiertes Token

In den folgenden beiden Abschnitten wird beschrieben, wie Sie in beiden Fällen eine Fehlerbehebung durchführen.

### Falscher Authentifizierungstyp in der Konfiguration ausgewählt

1. Öffnen Sie Ihre Commerce-Instanz.
1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. Erweitern Sie **[!UICONTROL Services]** und wählen Sie **[!UICONTROL [!DNL Data Connection]]** aus.
1. Vergewissern Sie sich, dass die von Ihnen im Feld **[!UICONTROL Authentication Type]** angegebene Server-zu-Server-Autorisierungsmethode korrekt ist. Adobe empfiehlt die Verwendung von **OAuth**. JWT ist veraltet. [Weitere Infos](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).

### Unzureichende Berechtigungen für generiertes Token

Dieses Problem kann durch unzureichende API-Berechtigungen für das generierte Token verursacht werden. So stellen Sie sicher, dass das Token über die richtigen Berechtigungen verfügt:

1. Identifizieren Sie den Systemadministrator für Adobe Experience Platform in Ihrem Unternehmen.
1. Suchen Sie das Projekt und die Anmeldeinformationen, die Sie verwenden werden.
1. Geben Sie die E-Mail-Adresse des technischen Kontos an, z. B. `fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com`.
1. Lassen Sie den Systemadministrator Adobe Experience Platform starten und gehen Sie zu &quot;**[!UICONTROL Permissions]** -> **[!UICONTROL Users]** -> **[!UICONTROL API credentials]**&quot;.
1. Suchen Sie mithilfe der E-Mail-Adresse des technischen Kontos oben nach den zu ändernden Anmeldeinformationen.
1. Öffnen Sie die Anmeldeinformationen und wählen Sie dann **[!UICONTROL Roles]** -> **[!UICONTROL Add roles]** aus.
1. Fügen Sie die Rolle hinzu, die die Berechtigung **[!UICONTROL Manage destinations]** enthält.
1. Klicken Sie auf **[!UICONTROL Save]**.
1. [Regenerieren](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html#generate-access-token) Sie das Zugriffstoken in der Konsole.
1. Stellen Sie sicher, dass das Token mithilfe der [Target-Verbindungs-API](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections) eine gültige Antwort bereitstellt.
