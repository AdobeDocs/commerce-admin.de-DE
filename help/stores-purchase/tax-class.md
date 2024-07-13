---
title: Steuerklassen
description: Erfahren Sie, wie Sie die für Steuerregeln verwendeten Steuerklassen konfigurieren.
exl-id: dd867eba-3f1e-45a8-9332-9e668a2092e1
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# Steuerklassen

Steuerklassen können Kunden, Produkten und Sendungen zugewiesen werden. Commerce analysiert den Warenkorb jedes Kunden und berechnet die entsprechende Steuer anhand der Kundenklasse, der Produktklasse im Warenkorb und der Region. Die Region wird durch die Lieferadresse, Rechnungsadresse oder Versandurkunde des Kunden bestimmt. Neue Steuerklassen können erstellt werden, wenn eine [Steuerregel](tax-rules.md) definiert ist.

- **Kunde** - Sie können so viele Kundensteuerklassen erstellen, wie Sie benötigen, und sie [Kundengruppen](../customers/customer-groups.md) zuweisen. So werden beispielsweise in einigen Rechtsordnungen Großkundengeschäfte nicht besteuert, aber Einzelhandelstransaktionen. Sie können Mitglieder der Gruppe Großkunden mit der Klasse Großhandelssteuer verknüpfen.

- **Produkt** - Produktklassen werden in Berechnungen verwendet, um zu ermitteln, welcher Steuersatz im Warenkorb korrekt angewandt wird. Wenn Sie ein Produkt erstellen, wird es einer bestimmten Steuerklasse zugewiesen. So kann es beispielsweise vorkommen, dass Nahrungsmittel nicht besteuert oder zu einem anderen Satz besteuert werden.

- **Versand** - Wenn Ihr Geschäft eine zusätzliche Versandsteuer in Rechnung stellt, sollten Sie eine bestimmte Produktsteuerklasse für den Versand angeben. Geben Sie es dann in der Konfiguration als die für den Versand verwendete Steuerklasse an.

## Konfigurieren von Steuerklassen

Die für den Versand verwendete Steuerklasse und die Standardsteuerklassen für [Produkte und Kunden](#add-a-product-tax-class) werden in der _[!UICONTROL Sales]_-Konfiguration festgelegt.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Tax]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Tax Classes]** .

   ![Konfiguration - Steuerklassen](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. Wählen Sie die Steuerklasse für jeden der folgenden Punkte aus:

   - **[!UICONTROL Set Tax Class for Shipping]**
   - **[!UICONTROL Tax Class for Gift Options]**
   - **[!UICONTROL Default Tax Class for Product]**
   - **[!UICONTROL Default Tax Class for Customer]**

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Hinzufügen von Steuerklassen

Steuerklassen für Kunden und Produkte können einfach hinzugefügt, dann einzelnen Kunden und Produkten zugewiesen und in Steuervorschriften verwendet werden.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Klicken Sie auf **[!UICONTROL Add New Tax Rule]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Additional Settings]** .

   ![Neue Steuerklasse hinzufügen](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Klicken Sie unter _Kundensteuerklasse_ auf **[!UICONTROL Add New Tax Class]**.

1. Geben Sie die **[!UICONTROL Name]** der neuen Steuerklasse in das Textfeld ein.

   ![Neue Steuerklasse hinzufügen](./assets/tax-class-customer-add-new.png){width="600" zoomable="yes"}

1. Um die neue Klasse zur Liste der verfügbaren Kundensteuerklassen hinzuzufügen, klicken Sie auf das Häkchen.

   ![Neue Steuerklassen](./assets/tax-classes-updated.png){width="600" zoomable="yes"}

## Produktsteuerklasse hinzufügen

1. Klicken Sie unter _Produktsteuerklasse_ auf **[!UICONTROL Add New Tax Class]**.

1. Geben Sie die **[!UICONTROL Name]** der neuen Steuerklasse in das Textfeld ein.

1. Um die neue Klasse zur Liste der verfügbaren Produktsteuerklassen hinzuzufügen, klicken Sie auf das Häkchen.

1. Klicken Sie nach Abschluss in der Schaltflächenleiste auf **[!UICONTROL Back]** , um zum Raster _Steuerregeln_ zurückzukehren.

## Standardsteuerziel

Die Standardeinstellungen für das Steuerziel bestimmen das Land, den Bundesstaat und die Postleitzahl, die als Grundlage für Steuerberechnungen verwendet werden.

**_So konfigurieren Sie das standardmäßige Steuerziel für Berechnungen:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Tax]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Default Tax Destination Calculation]** .

   ![Berechnung des steuerlichen Ziels ](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Default Country]** auf das Land, auf dem die Steuerberechnungen basieren.

1. Setzen Sie **[!UICONTROL Default State]** auf den Bundesstaat oder die Provinz, der/die als Grundlage für Steuerberechnungen verwendet wird.

1. Setzen Sie **[!UICONTROL Default Post Code]** auf die Postleitzahl, die als Grundlage für lokale Steuerberechnungen verwendet wird.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
