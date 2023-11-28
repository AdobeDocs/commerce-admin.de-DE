---
title: Steuervorschriften
description: Erfahren Sie, wie Sie die Steuerregeln mithilfe der Produktklasse, der Kundenklasse und des Steuersatzes definieren.
exl-id: 38d65998-7769-49ce-9814-e65df9d77bba
feature: Taxes, Currency
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# Steuervorschriften

Die Steuerregeln beinhalten eine Kombination aus Produktklasse, Kundenklasse und Steuersatz. Jeder Kunde wird einer Kundenklasse zugewiesen und jedem Produkt wird eine Produktklasse zugewiesen. Commerce analysiert den Warenkorb jedes Kunden und berechnet die entsprechende Steuer entsprechend den Kunden- und Produktklassen sowie der Region. Die Region basiert auf der Lieferadresse des Kunden, der Rechnungsadresse oder dem Versandursprung.

>[!NOTE]
>
>Wenn zahlreiche Steuersätze definiert werden müssen, können Sie den Prozess durch Importieren vereinfachen.

![Steuervorschriften](./assets/tax-rules.png){width="600" zoomable="yes"}

## Schritt 1: Ausfüllen der Informationen zur Steuerregel

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add New Tax Rule]**.

1. under _Informationen zu Steuerregeln_ eingeben, **[!UICONTROL Name]** für die neue Regel.

   ![Informationen zu Steuerregeln](./assets/tax-rule-information.png){width="600" zoomable="yes"}

1. Wählen Sie die **[!UICONTROL Tax Rate]** , die für die Regel gilt.

   Gehen Sie wie folgt vor, um einen bestehenden Steuersatz zu bearbeiten:

   - Bewegen Sie den Mauszeiger über den Steuersatz und klicken Sie auf _Bearbeiten_ ![Stiftsymbol](../assets/icon-edit-pencil.png) Symbol.

   - Aktualisieren Sie das Formular nach Bedarf und klicken Sie auf **[!UICONTROL Save]**.

1. Verwenden Sie eine der folgenden Methoden, um Steuersätze einzuführen:

### Methode 1: Steuern manuell eingeben

1. Klicken **[!UICONTROL Add New Tax Rate]**.

1. Füllen Sie das Formular nach Bedarf aus (siehe [Steuergebiete und Steuersätze](tax-zones-rates.md)).

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

   ![Neuer Steuersatz](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

### Methode 2: Einfuhrsteuersätze

1. Scrollen Sie nach unten zum Abschnitt am unteren Rand der Seite.

1. Gehen Sie wie folgt vor, um Steuersätze zu importieren:

   - Klicks **[!UICONTROL Choose File]** und navigieren Sie zur CSV-Datei mit den zu importierenden Steuersätzen.

   - Klicken **[!UICONTROL Import Tax Rates]**.

1. Um Steuersätze zu exportieren, klicken Sie auf **[!UICONTROL Export Tax Rates]** (siehe [Einfuhr-/Ausfuhrsteuersätze](../systems/data-transfer-tax-rates.md)).

![Einfuhr- und Ausfuhrsteuersätze](./assets/tax-rule-new-import-export.png){width="600" zoomable="yes"}

## Schritt 2: Zusätzliche Einstellungen durchführen

1. Um den Abschnitt zu öffnen, klicken Sie auf **[!UICONTROL Additional Settings]**.

   ![Zusätzliche Einstellungen für die Steuerregel](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Wählen Sie die **[!UICONTROL Customer Tax Class]** für die die Regel gilt.

   - Um eine Kundensteuerklasse zu bearbeiten, klicken Sie auf das _Bearbeiten_ ![Stiftsymbol](../assets/icon-edit-pencil.png) , aktualisieren Sie das Formular nach Bedarf und klicken Sie auf **[!UICONTROL Save]**.

   - Um eine Steuerklasse zu erstellen, klicken Sie auf **[!UICONTROL Add New Tax Class]**, füllen Sie das Formular nach Bedarf aus und klicken Sie auf **[!UICONTROL Save]**.

1. Wählen Sie die **[!UICONTROL Product Tax Class]** für die die Regel gilt.

   - Um eine Produktsteuerklasse zu bearbeiten, klicken Sie auf das _Bearbeiten_ ![Stiftsymbol](../assets/icon-edit-pencil.png) , aktualisieren Sie das Formular nach Bedarf und klicken Sie auf **[!UICONTROL Save]**.

   - Um eine Steuerklasse zu erstellen, klicken Sie auf **[!UICONTROL Add New Tax Class]**, füllen Sie das Formular nach Bedarf aus und klicken Sie auf **[!UICONTROL Save]**.

1. Wenn mehrere Steuern erhoben werden, geben Sie eine Zahl ein, um die Priorität dieser Steuer für **[!UICONTROL Priority]**.

   Wenn zwei Steuervorschriften mit derselben Priorität gelten, werden die Steuern hinzugefügt. Wenn zwei Steuern mit unterschiedlichen Prioritätseinstellungen zutreffen, werden die Steuern addiert.

1. Wenn Steuern auf der Bestellteilsumme basieren sollen, wählen Sie die **[!UICONTROL Calculate off Subtotal Only]** aktivieren.

1. Für **[!UICONTROL Sort Order]** Geben Sie eine Zahl ein, um die Reihenfolge dieser Steuerregel anzugeben, wenn diese mit anderen aufgelistet ist.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Rule]**.

## Demo zu Währungs- und Steuerregeln

In diesem Video erfahren Sie mehr über die Verwaltung von Währungs- und Steuerregeln:

>[!VIDEO](https://video.tv.adobe.com/v/343657/?quality=12)
