---
title: Steuergebiete und Steuersätze
description: Erfahren Sie, wie Sie Steuersätze für jedes geografische Gebiet festlegen, in dem Sie Steuern erheben und begrenzen.
exl-id: d8eb0743-d277-438d-91ed-fc711a6ba3ae
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Steuergebiete und Steuersätze

Die Steuersätze gelten im Allgemeinen für Umsätze, die innerhalb eines bestimmten geografischen Gebiets stattfinden. Verwenden Sie das Tool _Steuerzonen und Steuersätze_ , um den Steuersatz für jedes geografische Gebiet anzugeben, aus dem Sie Steuern erfassen und beschränken. Da jede Steuerzone und jeder Steuersatz über eine eindeutige Kennung verfügt, können Sie für ein bestimmtes geografisches Gebiet mehrere Steuersätze haben (z. B. Orte, die keine Lebensmittel oder Medikamente besteuern, aber andere Elemente besteuern).

Die Speichersteuer wird auf der Grundlage der Adresse des Stores berechnet. Die tatsächliche Kundensteuer für eine Bestellung wird berechnet, nachdem der Kunde die Bestellinformationen abgeschlossen hat. Commerce berechnet dann die Steuer entsprechend der Steuerkonfiguration des Stores.

![Steuerzonen und Steuersätze](./assets/tax-zones-rates.png){width="600" zoomable="yes"}

## Neuen Steuersatz definieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add New Tax Rate]**.

   ![Neuer Steuersatz](./assets/tax-rate-new.png){width="600" zoomable="yes"}

1. Geben Sie einen **[!UICONTROL Tax Identifier]** ein.

1. Um den Steuersatz auf eine einzelne Postleitzahl anzuwenden, geben Sie den Code für **[!UICONTROL Zip/Post Code]** ein.

   Der Sternchen-Platzhalter (`*`) kann verwendet werden, um bis zu zehn Zeichen im Code abzugleichen. Beispiel: `90*` stellt alle Postleitzahlen von 90000 bis 90999 dar.

1. Gehen Sie wie folgt vor, um den Steuersatz auf eine Reihe von Postleitzahlen anzuwenden:

   - Aktivieren Sie das Kontrollkästchen **[!UICONTROL Zip/Post is Range]** und definieren Sie den Bereich, indem Sie die erste und letzte Postleitzahl für **[!UICONTROL Range From]** und **[!UICONTROL Range To]** eingeben.

     ![ZIP/Post ist Bereich](./assets/tax-rate-new-zip-post-range.png){width="600" zoomable="yes"}

   - Wählen Sie die **[!UICONTROL State]** aus, für die der Steuersatz gilt.

   - Wählen Sie die **[!UICONTROL Country]** aus, für die der Steuersatz gilt.

   - Geben Sie den für die Berechnung des Steuersatzes verwendeten Wert ein.**[!UICONTROL Rate Percent]**

1. Wenn mehrere Stores vorhanden sind, können Sie für jede Store-Ansicht den Wert &quot;**[!UICONTROL Tax Titles]**&quot;festlegen.

   >[!NOTE]
   >
   >Lassen Sie dieses Feld leer, wenn Sie die Steuerkennung verwenden möchten.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Rate]**.

## Vorhandenen Steuersatz bearbeiten

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Suchen Sie den Steuersatz im Raster _[!UICONTROL Tax Zones and Rates]_und öffnen Sie den Datensatz im Bearbeitungsmodus.

   Wenn die Liste viele Raten enthält, verwenden Sie die [Filtersteuerelemente](../getting-started/admin-grid-controls.md), um die benötigte Rate zu ermitteln.

1. Nehmen Sie die erforderlichen Änderungen am **[!UICONTROL Tax Rate Information]** vor.

1. Aktualisieren Sie die **[!UICONTROL Tax Titles]** nach Bedarf.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Rate]**.

## Steuersatz löschen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Suchen Sie den zu löschenden Steuersatz und öffnen Sie ihn im Bearbeitungsmodus.

1. Klicken Sie in der Menüleiste auf **[!UICONTROL Delete Rate]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.
