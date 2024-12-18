---
title: Steuerklassen
description: Erfahren Sie, wie Sie die Steuerklassen konfigurieren, die für Steuerregeln verwendet werden.
exl-id: dd867eba-3f1e-45a8-9332-9e668a2092e1
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# Steuerklassen

Steuerklassen können Kunden, Produkten und Versand zugeordnet werden. Commerce analysiert den Warenkorb jedes Kunden und berechnet die entsprechende Steuer entsprechend der Klasse des Kunden, der Klasse der Produkte im Warenkorb und der Region. Die Region wird durch die Lieferadresse des Kunden, die Rechnungsadresse oder die Versandherkunft bestimmt. Neue Steuerklassen können erstellt werden, wenn eine [Steuerregel](tax-rules.md) definiert wird.

- **Kunde** - Sie können beliebig viele Debitorensteuerklassen erstellen und sie &quot;[&quot; ](../customers/customer-groups.md). So werden beispielsweise in einigen Steuergebieten Großhandelsumsätze nicht besteuert, wohl aber Einzelhandelsumsätze. Sie können Mitglieder der Gruppe „Großkunden“ mit der Steuerklasse „Großhandel“ verknüpfen.

- **Produkt** - Produktklassen werden in Berechnungen verwendet, um den korrekten Steuersatz zu bestimmen, der im Warenkorb angewendet wird. Wenn Sie ein Produkt erstellen, wird es einer bestimmten Steuerklasse zugewiesen. Beispielsweise dürfen Lebensmittel möglicherweise nicht oder anders besteuert werden.

- **Versand** - Wenn Ihr Geschäft eine zusätzliche Versandsteuer berechnet, sollten Sie eine bestimmte Produktsteuerklasse für den Versand angeben. Geben Sie sie dann in der Konfiguration als Steuerklasse an, die für den Versand verwendet wird.

## Steuerklassen konfigurieren

Die Steuerklasse, die für den Versand verwendet wird, und die standardmäßigen Steuerklassen für [Produkte und Kunden](#add-a-product-tax-class) werden in der _[!UICONTROL Sales]_Konfiguration festgelegt.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Tax]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Tax Classes]** .

   ![Konfiguration - Steuerklassen](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. Wählen Sie die Steuerklasse für jede der folgenden Kategorien:

   - **[!UICONTROL Set Tax Class for Shipping]**
   - **[!UICONTROL Tax Class for Gift Options]**
   - **[!UICONTROL Default Tax Class for Product]**
   - **[!UICONTROL Default Tax Class for Customer]**

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Steuerklassen hinzufügen

Steuerklassen für Kunden und Produkte können einfach hinzugefügt und dann einzelnen Kunden und Produkten zugewiesen und in Steuerregeln verwendet werden.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Klicken Sie auf **[!UICONTROL Add New Tax Rule]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Additional Settings]** .

   ![Neue Steuerklasse hinzufügen](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Klicken _unter &quot;_&quot; auf **[!UICONTROL Add New Tax Class]**.

1. Geben Sie den **[!UICONTROL Name]** der neuen Steuerklasse in das Textfeld ein.

   ![Neue Steuerklasse hinzufügen](./assets/tax-class-customer-add-new.png){width="600" zoomable="yes"}

1. Um die neue Klasse zur Liste der verfügbaren Debitorensteuerklassen hinzuzufügen, klicken Sie auf das Häkchen.

   ![Neue Steuerklassen](./assets/tax-classes-updated.png){width="600" zoomable="yes"}

## Hinzufügen einer Produktsteuerklasse

1. Klicken _unter „Produktsteuerklasse_ auf **[!UICONTROL Add New Tax Class]**.

1. Geben Sie den **[!UICONTROL Name]** der neuen Steuerklasse in das Textfeld ein.

1. Um die neue Klasse zur Liste der verfügbaren Produktsteuerklassen hinzuzufügen, klicken Sie auf das Häkchen.

1. Klicken Sie abschließend in der Schaltflächenleiste auf **[!UICONTROL Back]** , um zum Raster _Steuerregeln_ zurückzukehren.

## Standard-Steuerziel

Die standardmäßigen Zieleinstellungen für die Steuer bestimmen das Land, das Bundesland sowie die Postleitzahl, die als Grundlage für Steuerberechnungen verwendet werden.

**_So konfigurieren Sie das standardmäßige Steuerziel für Berechnungen:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Tax]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Default Tax Destination Calculation]** .

   ![Standardmäßige Zielberechnung der Steuer](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Default Country]** auf das Land fest, auf dem die Steuerberechnungen basieren.

1. Legen Sie **[!UICONTROL Default State]** auf das Bundesland fest, das als Grundlage für Steuerberechnungen verwendet wird.

1. Legen Sie **[!UICONTROL Default Post Code]** auf die Postleitzahl fest, die als Grundlage für lokale Steuerberechnungen verwendet wird.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
