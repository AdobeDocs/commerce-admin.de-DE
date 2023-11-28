---
title: Konfigurieren von Versandbeschriftungen
description: Erfahren Sie, wie Sie den Store zum Generieren von Versandbeschriftungen konfigurieren.
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '595'
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

Das Herstellungsland ist für alle Produkte erforderlich, die von USPS und FedEx international versandt werden. Wenn Sie über viele Produkte verfügen, die aktualisiert werden sollen, können Sie entweder [importieren](../systems/data-import.md) die Aktualisierungen oder verwenden Sie das Inventarraster, um mehrere Datensätze zu aktualisieren.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Aktualisieren Sie den Versandbeschriftungsdatensatz mit einer der folgenden Methoden.

### Methode 1: Aktualisieren eines einzelnen Datensatzes

1. Suchen Sie im Raster das zu aktualisierende Produkt und öffnen Sie es im Bearbeitungsmodus.

1. Aktualisieren Sie die **Land der Produktion** nach Bedarf.

   ![Land der Produktion](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. Klicken **[!UICONTROL Save]**.

### Methode 2: Mehrere Datensätze aktualisieren

1. Aktivieren Sie im Raster das Kontrollkästchen der zu aktualisierenden Produkte.

   Zum Beispiel alle Produkte, die in China hergestellt werden.

1. Legen Sie die **[!UICONTROL Actions]** Kontrolle an `Update Attributes` und klicken **[!UICONTROL Submit]**.

1. Im _Attribute aktualisieren_ Formular, suchen Sie die **Land der Produktion** und wählen Sie die **Änderung** aktivieren.

1. Wählen Sie das Land aus.

1. Klicken **[!UICONTROL Save]**.

## Schritt 2: Überprüfen der Store-Informationen

{{beta2-updates}}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Shipping Settings]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Origin]** und stellen Sie sicher, dass die folgenden Felder ausgefüllt sind:

   - **[!UICONTROL Street Address]** - Straße und Hausanschrift des Ortes, von dem aus Sendungen durchgeführt werden. Zum Beispiel der Speicherort Ihres Unternehmens oder Lagers. Dieses Feld ist für Versandbeschriftungen erforderlich.
   - **[!UICONTROL Street Address Line 2]** - alle zusätzlichen Adressangaben, wie z.B. Fußboden oder Eingang. Es wird empfohlen, dieses Feld zu verwenden.

   ![Origin](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Im _Vertrieb_ im linken Bereich wählen Sie **[!UICONTROL Delivery Methods]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL USPS]** und stellen Sie sicher, dass die folgenden Felder ausgefüllt sind:

   - **[!UICONTROL Secure Gateway URL]** - Das System gibt automatisch die Gateway-URL ein.
   - **[!UICONTROL Password]** - Das Passwort wird von USPS bereitgestellt und ermöglicht Ihnen den Zugriff auf das System über Web Services.
   - **Länge, Breite, Höhe, Mädchen** - Die Standarddimensionen des Pakets. Um diese Felder anzuzeigen, legen Sie **[!UICONTROL Size]** nach `Large`.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **FedEx** und stellen Sie sicher, dass die folgenden Felder ausgefüllt sind:

   - Zähleranzahl
   - Schlüssel
   - Kennwort

   Diese Informationen werden vom Netzbetreiber bereitgestellt und sind erforderlich, um über Web Services Zugriff auf sein System zu erhalten.

1. Erweitern Sie im linken Bereich **[!UICONTROL General]** und wählen **[!UICONTROL General]** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Store Information]** und stellen Sie sicher, dass die folgenden Felder ausgefüllt sind:

   - **[!UICONTROL Store Name]** - Der Name der Store- oder Store-Ansicht.
   - **[!UICONTROL Store Contact Telephone]** - Die Telefonnummer des Hauptkontakts für die Store- oder Store-Ansicht.
   - **[!UICONTROL Country]** - Das Land, in dem Ihr Geschäft seinen Sitz hat.
   - **[!UICONTROL VAT Number]** - Falls zutreffend, die Mehrwertsteuernummer Ihres Stores. (Nicht erforderlich für Geschäfte in den USA)
   - **[!UICONTROL Store Contact Address]** - Die Straßenadresse des Hauptkontakts für die Store- oder Store-Ansicht.

1. Wenn mehrere Stores vorhanden sind und sich die Kontaktinformationen von der Standardeinstellung unterscheiden, legen Sie **[!UICONTROL Store View]** und überprüfen Sie, ob die Informationen vollständig sind.

   Wenn die Informationen fehlen, wird beim Drucken der Beschriftungen ein Fehler angezeigt.

   ![Store-Informationen](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Klicken **[!UICONTROL Save Config]**.
