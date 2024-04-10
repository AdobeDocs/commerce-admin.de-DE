---
title: Konfigurieren von Versandkennzeichnungen
description: Erfahren Sie, wie Sie den Store zum Generieren von Versandkennzeichnungen konfigurieren.
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# Konfigurieren von Versandkennzeichnungen

Die folgenden Einstellungen müssen auf Produktebene und in der Konfiguration jedes Trägers vorgenommen werden, der zum Drucken von Etiketten verwendet wird. Um Etiketten zu drucken, müssen alle Anbieter ein Konto eröffnen. Schließen Sie dann die Konfiguration in Ihrem Geschäft für jeden Provider ab, den Sie verwenden möchten.

## Anforderungen an den Beförderer

| [!UICONTROL Carrier] | Anforderungen |
|-------|--------|
| [USPS](usps.md) | Erfordert ein USPS-Konto. Seit dem 23. Februar 2018 verlangt USPS, dass alle Versandaufkleber Porto enthalten müssen. |
| [USV](ups.md) | Erfordert ein UPS-Konto. Versandetiketten sind nur für Sendungen verfügbar, die aus den US-spezifischen Anmeldedaten stammen, die für Geschäfte außerhalb der USA erforderlich sind. |
| [FedEx](fedex.md) | Erfordert ein FedEx-Konto. Bei Geschäften außerhalb der USA werden Versandaufkleber nur für internationale Sendungen unterstützt. FedEx erlaubt keine Inlandslieferungen, die außerhalb der USA stammen |
| [DHL](dhl.md) | Erfordert ein DHL-Konto. Versandetiketten werden nur für Sendungen unterstützt, die ihren Ursprung in den USA haben. |

{style="table-layout:auto"}

## Schritt 1: Überprüfen Sie das Herstellungsland

Für alle Produkte, die von USPS und FedEx international versendet werden, ist das Herstellungsland erforderlich. Wenn Sie über viele Produkte verfügen, die aktualisiert werden sollten, haben Sie folgende Möglichkeiten [importieren](../systems/data-import.md) aktualisiert oder verwendet das Inventarraster, um mehrere Datensätze zu aktualisieren.

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Aktualisieren Sie den Versandetiketten-Datensatz mit einer der folgenden Methoden.

### Methode 1: Aktualisieren eines einzelnen Datensatzes

1. Suchen Sie im Raster das zu aktualisierende Produkt und öffnen Sie es im Bearbeitungsmodus.

1. Aktualisieren von **Herstellungsland** nach Bedarf.

   ![Herstellungsland](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. Klick **[!UICONTROL Save]**.

### Methode 2: Aktualisieren mehrerer Datensätze

1. Aktivieren Sie im Raster das Kontrollkästchen jedes zu aktualisierenden Produkts.

   Zum Beispiel alle Produkte, die in China hergestellt werden.

1. Legen Sie die **[!UICONTROL Actions]** steuern auf `Update Attributes` und klicken Sie auf **[!UICONTROL Submit]**.

1. In der _Attribute aktualisieren_ Formular, suchen **Herstellungsland** und wählen Sie aus **Änderung** Kontrollkästchen.

1. Wählen Sie das Land.

1. Klick **[!UICONTROL Save]**.

## Schritt 2 Überprüfen der Store-Informationen

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich . **[!UICONTROL Sales]** und wählen **[!UICONTROL Shipping Settings]**.

1. Expand ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL Origin]** und überprüfen, ob die folgenden Felder vollständig sind:

   - **[!UICONTROL Street Address]** - Die Straßenadresse des Ortes, von dem aus die Sendungen gesendet werden. Beispiel: der Standort Ihres Unternehmens oder Lagers. Dieses Feld ist für Versandkennzeichnungen erforderlich.
   - **[!UICONTROL Street Address Line 2]** - Alle zusätzlichen Adressangaben, wie das Stockwerk oder der Eingang. Die Verwendung dieses Felds wird empfohlen.

   ![Ursprung](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. In der _Verkauf_ im linken Bereich auswählen **[!UICONTROL Delivery Methods]**.

1. Expand ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL USPS]** und überprüfen, ob die folgenden Felder vollständig sind:

   - **[!UICONTROL Secure Gateway URL]** - Das System gibt automatisch die Gateway-URL ein.
   - **[!UICONTROL Password]** - Das Passwort wird von USPS bereitgestellt und ermöglicht Ihnen den Zugriff auf ihr System über Web-Services.
   - **Länge, Breite, Höhe, Breite** - Die Standardabmessungen des Pakets. Damit diese Felder angezeigt werden, legen Sie Folgendes fest **[!UICONTROL Size]** bis `Large`.

1. Expand ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **FedEx** und überprüfen Sie, ob die folgenden Felder vollständig sind:

   - Zählernummer
   - Schlüssel
   - Kennwort

   Diese Informationen werden vom Provider bereitgestellt und sind erforderlich, um über Web-Services Zugriff auf sein System zu erhalten.

1. Erweitern Sie im linken Bereich . **[!UICONTROL General]** und wählen **[!UICONTROL General]** Darunter.

1. Expand ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL Store Information]** und überprüfen Sie, ob die folgenden Felder vollständig sind:

   - **[!UICONTROL Store Name]** - Der Name des Stores oder der Store-Ansicht.
   - **[!UICONTROL Store Contact Telephone]** - Die Telefonnummer des primären Kontakts für den Store oder die Store-Ansicht.
   - **[!UICONTROL Country]** - Das Land, in dem Ihr Geschäft seinen Sitz hat.
   - **[!UICONTROL VAT Number]** - Gegebenenfalls die Umsatzsteuer-Nummer Ihres Geschäfts. (Nicht erforderlich für Geschäfte mit Sitz in den USA)
   - **[!UICONTROL Store Contact Address]** - Die Straßenadresse des primären Kontakts für die Store- oder Store-Ansicht.

1. Wenn Sie über mehrere Stores verfügen und sich die Kontaktinformationen von der Standardeinstellung unterscheiden, legen Sie Folgendes fest **[!UICONTROL Store View]** und überprüfen, ob die Informationen vollständig sind.

   Wenn die Informationen fehlen, wird beim Versuch, die Beschriftungen zu drucken, ein Fehler angezeigt.

   ![Informationen speichern](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Klick **[!UICONTROL Save Config]**.
