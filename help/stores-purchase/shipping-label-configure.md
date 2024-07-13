---
title: Konfigurieren von Versandbeschriftungen
description: Erfahren Sie, wie Sie den Store zum Generieren von Versandbeschriftungen konfigurieren.
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# Konfigurieren von Versandbeschriftungen

Die folgenden Einstellungen müssen auf Produktebene und in der Konfiguration der einzelnen Träger vorgenommen werden, die zum Drucken von Beschriftungen verwendet werden. Zum Drucken von Etiketten müssen alle Anbieter ein Konto öffnen. Schließen Sie dann die Konfiguration in Ihrem Store für jeden Mobilnetzbetreiber ab, den Sie verwenden möchten.

## Beförderungsanforderungen

| [!UICONTROL Carrier] | Voraussetzungen |
|-------|--------|
| [USPS](usps.md) | Erfordert ein USPS-Konto. Ab dem 23. Februar 2018 verlangt USPS, dass alle Versandbeschriftungen Postsendungen enthalten. |
| [UPS](ups.md) | Erfordert ein UPS-Konto. Versandbeschriftungen sind nur für Sendungen verfügbar, die aus den USA stammen und für Geschäfte außerhalb der USA erforderlich sind. |
| [FedEx](fedex.md) | Erfordert ein FedEx-Konto. Bei Geschäften außerhalb der USA werden Versandetiketten nur für internationale Sendungen unterstützt. FedEx erlaubt inländische Sendungen, die außerhalb der USA erfolgen, nicht |
| [DHL](dhl.md) | Erfordert ein DHL-Konto. Versandbeschriftungen werden nur für Sendungen unterstützt, die aus den USA stammen. |

{style="table-layout:auto"}

## Schritt 1: Überprüfen des Herstellungslandes

Das Herstellungsland ist für alle Produkte erforderlich, die von USPS und FedEx international versandt werden. Wenn Sie über viele Produkte verfügen, die aktualisiert werden sollen, können Sie entweder die Aktualisierungen [importieren](../systems/data-import.md) oder das Inventarraster verwenden, um mehrere Datensätze zu aktualisieren.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Aktualisieren Sie den Versandbeschriftungsdatensatz mit einer der folgenden Methoden.

### Methode 1: Aktualisieren eines einzelnen Datensatzes

1. Suchen Sie im Raster das zu aktualisierende Produkt und öffnen Sie es im Bearbeitungsmodus.

1. Aktualisieren Sie das **Land der Produktion** nach Bedarf.

   ![Herstellungsland](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save]**.

### Methode 2: Mehrere Datensätze aktualisieren

1. Aktivieren Sie im Raster das Kontrollkästchen der zu aktualisierenden Produkte.

   Zum Beispiel alle Produkte, die in China hergestellt werden.

1. Setzen Sie das Steuerelement **[!UICONTROL Actions]** auf `Update Attributes` und klicken Sie auf **[!UICONTROL Submit]**.

1. Suchen Sie im Formular _Attribute aktualisieren_ das Feld **Herstellungsland** und aktivieren Sie das Kontrollkästchen **Ändern** .

1. Wählen Sie das Land aus.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Schritt 2: Überprüfen der Store-Informationen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Shipping Settings]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Origin]** und überprüfen Sie, ob die folgenden Felder ausgefüllt sind:

   - **[!UICONTROL Street Address]** - Die Straßenadresse des Ortes, von dem aus Sendungen durchgeführt werden. Zum Beispiel der Speicherort Ihres Unternehmens oder Lagers. Dieses Feld ist für Versandbeschriftungen erforderlich.
   - **[!UICONTROL Street Address Line 2]** - Alle zusätzlichen Adressinformationen, wie der Fußboden oder der Eingang. Es wird empfohlen, dieses Feld zu verwenden.

   ![Origin](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Wählen Sie im Abschnitt _Verkauf_ im linken Bereich die Option **[!UICONTROL Delivery Methods]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL USPS]** und überprüfen Sie, ob die folgenden Felder ausgefüllt sind:

   - **[!UICONTROL Secure Gateway URL]** - Das System gibt automatisch die Gateway-URL ein.
   - **[!UICONTROL Password]** - Das Kennwort wird von USPS bereitgestellt und ermöglicht Ihnen den Zugriff auf das System über Web Services.
   - **Länge, Breite, Höhe, Mädchen** - Die Standarddimensionen des Pakets. Damit diese Felder angezeigt werden, setzen Sie **[!UICONTROL Size]** auf `Large`.

1. Erweitern Sie den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) des Abschnitts **FedEx** und überprüfen Sie, ob die folgenden Felder ausgefüllt sind:

   - Zähleranzahl
   - Schlüssel
   - Kennwort

   Diese Informationen werden vom Netzbetreiber bereitgestellt und sind erforderlich, um über Web Services Zugriff auf sein System zu erhalten.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL General]** und wählen Sie unter &quot;**[!UICONTROL General]**&quot;.

1. Erweitern Sie den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) um den Abschnitt **[!UICONTROL Store Information]** und stellen Sie sicher, dass die folgenden Felder ausgefüllt sind:

   - **[!UICONTROL Store Name]** - Der Name der Store- oder Store-Ansicht.
   - **[!UICONTROL Store Contact Telephone]** - Die Telefonnummer des Hauptkontakts für die Store- oder Store-Ansicht.
   - **[!UICONTROL Country]** - Das Land, in dem Ihr Store basiert.
   - **[!UICONTROL VAT Number]** - Falls zutreffend, die Mehrwertsteuernummer Ihres Geschäfts. (Nicht erforderlich für Geschäfte in den USA)
   - **[!UICONTROL Store Contact Address]** - Die Straßenadresse des Hauptkontakts für die Store- oder Store-Ansicht.

1. Wenn mehrere Stores vorhanden sind und sich die Kontaktinformationen von der Standardeinstellung unterscheiden, setzen Sie für jeden Speicher den Wert &quot;**[!UICONTROL Store View]**&quot;und stellen Sie sicher, dass die Informationen vollständig sind.

   Wenn die Informationen fehlen, wird beim Drucken der Beschriftungen ein Fehler angezeigt.

   ![Store-Informationen](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.
