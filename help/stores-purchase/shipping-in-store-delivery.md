---
title: In-store-Versand
description: Erfahren Sie, wie Sie eine Option für einen In-Store-Versand für Ihren Store einrichten.
exl-id: bd64b110-5c39-41c6-8a0c-38561b2a5bf4
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# In-store-Versand

Mit der Bereitstellungsmethode im Geschäft kann der Kunde eine Quelle auswählen, die beim Checkout als Abholort verwendet werden soll.

![Bereitstellungsmethode im Geschäft beim Checkout](./assets/luma-in-store-example.png){width="700" zoomable="yes"}

Während des Checkouts an der Storefront:

1. Der Kunde klickt auf **[!UICONTROL Pick In Store]** oder wählt die _[!UICONTROL In-Store Pickup Delivery]_Versandmethode.
1. Die _[!UICONTROL Pick In Store]_Die Registerkarte &quot;Checkout&quot;wird geöffnet.

Wenn der Kunde über eine Adresse verfügt oder zuvor das Versandadressenformular ausgefüllt hat, bevor er zum _[!UICONTROL Pick In Store]_tab:

- Die Quelle, die der Kundenadresse im konfigurierten Radius am nächsten ist, wird automatisch als Abholspeicher vorausgewählt.
- Wenn der Kunde klickt **[!UICONTROL Select Other]**, die _[!UICONTROL Select Store]_Suchformular geöffnet. In der Liste werden nur Stores angezeigt, die innerhalb des konfigurierten Abstands (Radius) zum vorausgewählten Store liegen. Alle Geschäfte in der Liste werden nach der Entfernung zum vorgewählten Store sortiert.
- Wenn der Kunde eine Postleitzahl oder einen Stadt-Namen in das Suchfeld eingibt, werden nur Geschäfte innerhalb der konfigurierten Entfernung (Radius) zum gesuchten Ort in der Liste angezeigt. Alle Läden in der Liste sind nach der Entfernung zum gesuchten Ort sortiert.
- Wenn der Kunde die Postleitzahl oder den Stadt-Namen aus dem Suchfeld löscht, werden alle Abholgeschäfte, die den Produkten im Warenkorb zugewiesen sind, dem Kunden angezeigt. Alle Geschäfte in der Liste sind in aufsteigender Reihenfolge der Quellcodes sortiert, ohne dass die Entfernung (Radius) begrenzt wird.

Wenn der Kunde keine Adresse hat oder zuvor das Versandadressenformular nicht ausgefüllt hat, bevor er zum _[!UICONTROL Pick In Store]_tab:

- Die Seite zeigt die _Wir konnten den Abholort nicht anhand der verfügbaren Informationen vorab auswählen_ Nachricht.
- Wenn der Kunde klickt **[!UICONTROL Select Store]**, die _[!UICONTROL Select Store]_Suchformular geöffnet.
- Alle Abholgeschäfte, die den Produkten im Warenkorb zugeordnet sind, werden in aufsteigender Reihenfolge der Quellcodes angezeigt, ohne dass die Entfernung (Radius) begrenzt wird.
- Wenn der Kunde eine Postleitzahl oder einen Stadt-Namen in das Suchfeld eingibt, werden nur Geschäfte innerhalb der konfigurierten Entfernung (Radius) zum gesuchten Ort in der Liste angezeigt. Alle Läden in der Liste sind nach der Entfernung zum gesuchten Ort sortiert.

## Vor der Einrichtung

- Stellen Sie sicher, dass Sie über einen nicht standardmäßigen Lager und eine nicht standardmäßige Quelle verfügen. Weitere Informationen zum Konfigurieren einer Quelle als Pickup-Speicherort finden Sie unter [Quelle hinzufügen](../inventory-management/sources-add.md).
- Stellen Sie sicher, dass Sie einen Distance Priority Algorithm konfiguriert haben. Weitere Informationen finden Sie unter [Konfigurieren des Distance Priority-Algorithmus](../inventory-management/distance-priority-algorithm.md).
- Stellen Sie sicher, dass [heruntergeladen und importiert](../inventory-management/cli.md#import-geocodes) alle erforderlichen Geocodes für die Offline-Berechnung.
- Stellen Sie sicher, dass Sie [Standardmäßige Berechnung des Steuerziels](../configuration-reference/sales/tax.md#default-tax-destination-calculation) -Einstellungen.

>[!IMPORTANT]
>
>**In der Storefront werden Suchergebnisse nach Entfernung (Radius) gefiltert, um relevante Ergebnisse anzuzeigen:**<br><br>
>Wenn der Kunde über eine Lieferadresse verfügt, wird der Basisstandort zur Berechnung der Entfernung (Radius) von der Lieferadresse übernommen.<br><br>
>Wenn der Kunde keine Lieferadresse hat, wird der Basisstandort zur Berechnung der Entfernung vom [Standardmäßige Berechnung des Steuerziels](../configuration-reference/sales/tax.md#default-tax-destination-calculation) -Einstellungen. Diese Einstellungen werden für jede Store-Ansicht festgelegt. Sie müssen die Einstellungen für die Berechnung des standardmäßigen Steuerziels konfigurieren, um sicherzustellen, dass die Suche in einem Pick-up-Store ordnungsgemäß funktioniert.

## In-store-Versand einrichten

Überprüfen Sie zunächst, ob die In-Store-Bereitstellung aktiviert ist.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Delivery Methods]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL In-Store Delivery]** Abschnitt.

   ![In-store-Bereitstellung](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Enabled]** nach `Yes`.

   >[!NOTE]
   >
   >Falls erforderlich, löschen Sie die **[!UICONTROL Use system value]** aktivieren, um die Standardeinstellung für jedes Feld zu ändern.

1. Geben Sie die **[!UICONTROL Method Name]** beschreibt die Berechnungsmethode, die zur Erstellung einer Versandschätzung verwendet wird.

   Der Name der Methode wird neben der berechneten geschätzten Rate im Warenkorb angezeigt.

1. Geben Sie die **[!UICONTROL Title]** , für die Sie angezeigt werden möchten _In-Store-Bereitstellung_ während des Checkouts.

   Der Standardtitel lautet `In-Store Pickup Delivery`.

1. Geben Sie die Gebühr in das Feld ein, um Kunden für den In-Store-Abholdienst zu berechnen. **[!UICONTROL Price]** -Feld.

1. Geben Sie die **[!UICONTROL Search Radius]** in Kilometern für die Standortsuche beim Storefront-Checkout.

1. Für **[!UICONTROL Displayed Error Message]** Geben Sie die Nachricht ein, die angezeigt wird, wenn der In-Store-Versand nicht mehr verfügbar ist.

   Die Standardnachricht lautet `In-Store Delivery is not available. To use this delivery method, please contact us.`

1. Klicken **[!UICONTROL Save Config]**.
