---
title: Mindestpreis
description: Erfahren Sie, wie Sie mit der Funktion "Mindest-Werbepreis" (MAP) die Herstelleranforderungen mit Sonderpreisen erfüllen können.
exl-id: ccd44cfe-3967-4d82-b5b2-3f92701d152e
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 0%

---

# Mindestpreis

Händler dürfen manchmal keinen Preis anzeigen, der unter dem vom Hersteller empfohlenen Einzelhandelspreis liegt. Der Mindestpreis für Werbeanzeigen (MAP) bietet Ihnen die Möglichkeit, die Anforderungen des Herstellers zu erfüllen und gleichzeitig Ihren Kunden einen besseren Preis zu bieten. Da die Anforderungen von Hersteller zu Hersteller unterschiedlich sind, können Sie Ihren Store so konfigurieren, dass der tatsächliche Preis nicht auf Seiten angezeigt wird, auf denen er nicht zulässig ist.

Die MAP-Funktion fügt anstelle des regulären Produktpreises einen speziellen Link _Klicks für Preis_ hinzu. Wenn der Preis in Ihrem Geschäft unter dem Mindestpreis für dieses Produkt liegt, gibt es zwei Möglichkeiten, die Preisinformationen auf der Storefront zu behandeln. Der erste Weg ist, dass der Preis nicht angezeigt wird. Wenn der Käufer auf die Schaltfläche _Für Preis klicken_ klickt, wird nur der tatsächliche Preis, zu dem Sie das Produkt verkaufen, sichtbar. Der zweite Weg besteht darin, dass der Listenpreis/Marktpreis mit einer durchgreifenden Darstellung angezeigt wird, um zu betonen, dass Ihr Preis niedriger ist.

Außerdem können Sie mit der MAP-Funktion einige Verbesserungen vorschlagen. Wenn beispielsweise ein Kunde ein solches Produkt zum Warenkorb hinzufügt, wird er nicht zum Warenkorb umgeleitet, sondern es werden Angebote angezeigt, die es dem Käufer ermöglichen,

- Entfernen Sie einen Artikel aus dem Warenkorb (kann durchgeführt werden, wenn der Käufer nur den Preis klären möchte und noch keine Kaufentscheidung getroffen hat)

- Lassen Sie es im Warenkorb und behalten Sie den Einkauf bei

- Begeben Sie sich zum Checkout

## MAP-Logik

Einige Produkte verfügen über Preise, die von einer ausgewählten Option abhängen, z. B. benutzerspezifische Optionen oder einfache Produkte mit eigenen SKUs und Lagerverwaltung). Für diese Produkte wird je nach Produkttyp und Preiseinstellung die folgende Logik angewendet. Der tatsächliche Preis wird von der Auftragsverwaltung, den Tools für das Kundenmanagement und Berichten verwendet.

## Verwenden von MAP mit Produktarten

| Produkttyp | Beschreibung |
|--- |--- |
| [Einfach](product-create-simple.md), [Virtual](product-create-virtual.md) | Der tatsächliche Preis wird nicht automatisch auf der Katalogliste und den Produktseiten angezeigt, sondern nur gemäß der Einstellung [!UICONTROL Display Actual Price] . Die Preise für benutzerdefinierte Optionen werden normal angezeigt. |
| [Grouped](product-create-grouped.md) | Die Preise verknüpfter einfacher Produkte werden nicht automatisch auf der Katalogliste und den Produktseiten angezeigt, sondern werden nur gemäß der Einstellung [!UICONTROL Display Actual Price] eingeschlossen. |
| [Konfigurierbar](product-create-configurable.md) | Der tatsächliche Preis wird nicht automatisch auf der Katalogliste und den Produktseiten angezeigt, sondern nur gemäß der Einstellung [!UICONTROL Display Actual Price] . Optionspreise erscheinen normal. |
| [Bundle](product-create-bundle.md) (mit festem Preis) | Der tatsächliche Preis wird nicht automatisch auf Katalogseiten angezeigt, sondern nur gemäß der Einstellung [!UICONTROL Display Actual Price] . Die Preise der Bundle-Artikel erscheinen normal. MAP ist nicht für Bundle-Produkte mit dynamischen Preisen verfügbar. |
| [herunterladbar](product-create-downloadable.md) | Der tatsächliche Preis wird nicht automatisch auf der Katalogliste und den Produktseiten angezeigt, sondern nur gemäß der Einstellung [!UICONTROL Display Actual Price] . Der Preis für jeden Downloadlink wird normal angezeigt. |

{style="table-layout:auto"}

## Verwenden von MAP mit Preiseinstellungen

| Preiseinstellung | Beschreibung |
|--- |--- |
| Hauptpreis | Wenn MAP auf den Hauptpreis angewendet wird, erscheinen die Preise von Optionen, Bundle-Artikeln und zugehörigen Produkten (die zum Hauptpreis hinzukommen oder von ihm abgezogen werden) normal. |
| Zugehöriger Produktpreis | Wenn ein Produkt keinen Hauptpreis hat und sein Preis von den verbundenen Produktpreisen abgeleitet wird (z. B. in einem gruppierten Produkt), werden die MAP-Einstellungen der zugehörigen Produkte angewendet. |
| [MSRP](product-price-minimum-advertised.md) | Wenn für ein Produkt im Warenkorb der vom Hersteller vorgeschlagene Einzelhandelspreis (MSRP) angegeben ist, wird der Preis nicht überschritten. |
| [Tierpreis](product-price-tier.md) | Wenn die Ebenenpreise festgelegt sind, wird die Information über die Ebenenpreise nicht im Katalog angezeigt. Auf der Produktseite wird eine Benachrichtigung angezeigt, die anzeigt, dass der Preis bei mehr als einer bestimmten Menge niedriger sein kann, der Rabatt jedoch nur in Prozentsätzen angezeigt wird. Bei verknüpften Produkten eines gruppierten Produkts werden die Rabatte nicht auf der Produktseite angezeigt. Der Stufenpreis wird entsprechend der Einstellung &quot;Tatsächlichen Preis anzeigen&quot;angezeigt. |
| [Sonderpreis](product-price-special.md) | Wenn der Sonderpreis angegeben ist, wird der Sonderpreis entsprechend der Einstellung &quot;Tatsächlichen Preis anzeigen&quot;angezeigt. |

## MAP-Konfiguration

Die Funktion &quot;Mindest-Werbepreis (MAP)&quot;ist standardmäßig nicht aktiviert. Wenn Sie diese Funktion zu Ihrem Store hinzufügen möchten, müssen Sie sie aktivieren und die MAP-Einstellungen für Ihre Produkte konfigurieren. Die MAP-Einstellungen können auf alle Produkte in Ihrem Katalog angewendet oder für bestimmte Produkte konfiguriert werden. Wenn MAP global aktiviert ist, werden alle Produktpreise in der Storefront ausgeblendet. Es gibt verschiedene Konfigurationsoptionen, die Sie verwenden können, um die Bedingungen Ihrer Vereinbarung mit dem Hersteller einzuhalten und Ihren Kunden weiterhin einen besseren Preis zu bieten.

![Tatsächlicher Preis wird &quot;Auf Geste&quot;](./assets/storefront-msrp-on-gesture.png){width="700" zoomable="yes"} angezeigt

Auf globaler Ebene können Sie MAP aktivieren oder deaktivieren, sie auf alle Produkte anwenden und definieren, wie der tatsächliche Preis angezeigt wird. Sie können auch den Text der zugehörigen Nachrichten und Informationstipps bearbeiten, die im Store angezeigt werden.

Wenn MAP aktiviert ist, werden die MAP-Einstellungen auf Produktebene verfügbar. Sie können die Zuordnungspunkte auf ein einzelnes Produkt anwenden, indem Sie den MSRP eingeben und auswählen, wie der tatsächliche Preis im Store angezeigt werden soll. MAP-Einstellungen auf Produktebene überschreiben die globalen MAP-Einstellungen.

![Für Preis klicken](./assets/storefront-price-map.png){width="700" zoomable="yes"}

### Schritt 1: Aktivieren Sie die ZUORDNUNGS-Komponente für die Store-Ansicht.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Falls zutreffend, setzen Sie **[!UICONTROL Store View]** in der oberen rechten Ecke auf die Ansicht, für die die Konfiguration gilt.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Sales]** und wählen Sie unter &quot;**[!UICONTROL Sales]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt _[!UICONTROL Minimum Advertised Price]_.

1. Falls nötig, setzen Sie **MAP** aktivieren auf `Yes`.

   ![MAP-Konfiguration](./assets/sales-minimum-advertised-price.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Konfigurationsoptionen finden Sie unter [_Mindestpreis für Werbung_](../configuration-reference/sales/sales.md#minimum-advertised-price) in der _Konfigurationsreferenz_.

### Schritt 2: MAP-Einstellungen konfigurieren

Verwenden Sie eine der folgenden Methoden, um die MAP-Einstellungen zu konfigurieren:

#### Methode 1: MAP für alle Produkte konfigurieren

1. Gehen Sie wie folgt vor, um zu bestimmen, wann und wo der tatsächliche Preis für Kunden sichtbar sein soll:

   - Um den Standardwert zu ändern, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** .

   - Stellen Sie **Tatsächlichen Preis anzeigen** auf einen der folgenden Werte ein:
      - `In Cart`
      - `Before Order Confirmation`
      - `On Gesture (on click)`

1. Geben Sie den Text ein, der im **[!UICONTROL Default Popup Text Message]** angezeigt werden soll.

1. Geben Sie eine zusätzliche Erklärung ein, die Sie in den **[!UICONTROL Default "What's This" Text Message]** finden möchten.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

#### Methode 2: MAP für ein einzelnes Produkt konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Inventory]** > **[!UICONTROL Products]**.

1. Öffnen Sie das Produkt im Modus **[!UICONTROL Edit]** .

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Advanced Settings]** und wählen Sie **[!UICONTROL Advanced Pricing]** aus.

   >[!NOTE]
   >
   >Die Felder [!UICONTROL Manufacturer's Suggested Retail Price] und [!UICONTROL Display Actual Price] werden nur angezeigt, wenn in der Konfiguration die Option [Mindestpreis für Werbung](../configuration-reference/sales/sales.md#minimum-advertised-price) aktiviert ist.

1. Geben Sie den Wert **[!UICONTROL Manufacturer's Suggested Retail Price]** (MSRP) ein.

   In diesem Beispiel beträgt der Produktpreis 54,00 USD, der MSRP 59,95.

   ![Vorgeschlagener Einzelhandelspreis des Herstellers](./assets/product-price-msrp.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Display Actual Price]** auf einen der folgenden Werte:

   - `Use config` - (Standard) Wendet die Anzeigeeinstellungen für den Store auf [konfigurierte](../configuration-reference/sales/sales.md#minimum-advertised-price) an. |
   - `On Gesture` - Zeigt den tatsächlichen Produktpreis in einem Popup an, wenn der Kunde auf den Link _Zum Preis klicken_ oder _Was ist das?_ -Link.
   - `In Cart` - Zeigt den tatsächlichen Produktpreis im Warenkorb an.
   - `Before Order Confirmation` - Zeigt den tatsächlichen Produktpreis am Ende des Checkout-Prozesses an, kurz bevor die Bestellung bestätigt wird.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Done]** und dann auf **[!UICONTROL Save]**.
