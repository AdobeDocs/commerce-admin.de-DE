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

![Bereitstellungsmethode im Speicher beim Checkout](./assets/luma-in-store-example.png){width="700" zoomable="yes"}

Während des Checkouts an der Storefront:

1. Der Kunde klickt auf **[!UICONTROL Pick In Store]** oder wählt die Versandmethode _[!UICONTROL In-Store Pickup Delivery]_aus.
1. Der Tab _[!UICONTROL Pick In Store]_Checkout wird geöffnet.

Wenn der Kunde über eine Adresse verfügt oder zuvor das Formular für die Versandadresse ausgefüllt hat, bevor er zum Tab _[!UICONTROL Pick In Store]_wechselt:

- Die Quelle, die der Kundenadresse im konfigurierten Radius am nächsten ist, wird automatisch als Abholspeicher vorausgewählt.
- Wenn der Kunde auf **[!UICONTROL Select Other]** klickt, wird das Suchformular _[!UICONTROL Select Store]_geöffnet. In der Liste werden nur Stores angezeigt, die innerhalb des konfigurierten Abstands (Radius) zum vorausgewählten Store liegen. Alle Geschäfte in der Liste werden nach der Entfernung zum vorgewählten Store sortiert.
- Wenn der Kunde eine Postleitzahl oder einen Stadt-Namen in das Suchfeld eingibt, werden nur Geschäfte innerhalb der konfigurierten Entfernung (Radius) zum gesuchten Ort in der Liste angezeigt. Alle Läden in der Liste sind nach der Entfernung zum gesuchten Ort sortiert.
- Wenn der Kunde die Postleitzahl oder den Stadt-Namen aus dem Suchfeld löscht, werden alle Abholgeschäfte, die den Produkten im Warenkorb zugewiesen sind, dem Kunden angezeigt. Alle Geschäfte in der Liste sind in aufsteigender Reihenfolge der Quellcodes sortiert, ohne dass die Entfernung (Radius) begrenzt wird.

Wenn der Kunde keine Adresse hat oder zuvor das Formular für die Versandadresse nicht ausgefüllt hat, bevor er zum Tab _[!UICONTROL Pick In Store]_wechselt:

- Auf der Seite wird die Meldung _Wir konnten den Abholort nicht anhand der verfügbaren Informationen vorab auswählen_.
- Wenn der Kunde auf **[!UICONTROL Select Store]** klickt, wird das Suchformular _[!UICONTROL Select Store]_geöffnet.
- Alle Abholgeschäfte, die den Produkten im Warenkorb zugeordnet sind, werden in aufsteigender Reihenfolge der Quellcodes angezeigt, ohne dass die Entfernung (Radius) begrenzt wird.
- Wenn der Kunde eine Postleitzahl oder einen Stadt-Namen in das Suchfeld eingibt, werden nur Geschäfte innerhalb der konfigurierten Entfernung (Radius) zum gesuchten Ort in der Liste angezeigt. Alle Läden in der Liste sind nach der Entfernung zum gesuchten Ort sortiert.

## Vor der Einrichtung

- Stellen Sie sicher, dass Sie über einen nicht standardmäßigen Lager und eine nicht standardmäßige Quelle verfügen. Weitere Informationen zum Konfigurieren einer Quelle als Pickup-Speicherort finden Sie unter [Hinzufügen einer Quelle](../inventory-management/sources-add.md).
- Stellen Sie sicher, dass Sie einen Distance Priority Algorithm konfiguriert haben. Weitere Informationen finden Sie unter [Konfigurieren des Distance Priority Algorithm](../inventory-management/distance-priority-algorithm.md).
- Vergewissern Sie sich, dass [alle erforderlichen Geocodes für die Offline-Berechnung heruntergeladen und importiert hat](../inventory-management/cli.md#import-geocodes).
- Stellen Sie sicher, dass Sie die Einstellungen für die [Standardeinstellung für die Berechnung des Steuerziels](../configuration-reference/sales/tax.md#default-tax-destination-calculation) konfiguriert haben.

>[!IMPORTANT]
>
>**In der Storefront werden Suchergebnisse nach Entfernung (Radius) gefiltert, um relevante Ergebnisse anzuzeigen:**<br><br>
>Wenn der Kunde über eine Lieferadresse verfügt, wird der Basisstandort zur Berechnung der Entfernung (Radius) von der Lieferadresse übernommen.<br><br>
>Wenn der Kunde nicht über eine Lieferadresse verfügt, wird der Basisstandort zur Berechnung der Entfernung aus den Einstellungen für die [Standardsteuerziel-Berechnung](../configuration-reference/sales/tax.md#default-tax-destination-calculation) entnommen. Diese Einstellungen werden für jede Store-Ansicht festgelegt. Sie müssen die Einstellungen für die Berechnung des standardmäßigen Steuerziels konfigurieren, um sicherzustellen, dass die Suche in einem Pick-up-Store ordnungsgemäß funktioniert.

## In-store-Versand einrichten

Überprüfen Sie zunächst, ob die In-Store-Bereitstellung aktiviert ist.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Delivery Methods]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL In-Store Delivery]** .

   ![ In-store-Bereitstellung](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Enabled]** auf `Yes`.

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** , um die Standardeinstellung für jedes Feld zu ändern.

1. Geben Sie den Wert **[!UICONTROL Method Name]** ein, der die Berechnungsmethode beschreibt, mit der eine Versandschätzung erstellt wird.

   Der Name der Methode wird neben der berechneten geschätzten Rate im Warenkorb angezeigt.

1. Geben Sie den **[!UICONTROL Title]** ein, der beim Checkout für den Abschnitt _In-Store-Versand_ angezeigt werden soll.

   Der Standardtitel ist `In-Store Pickup Delivery`.

1. Um Kunden für den In-store-Abholdienst zu berechnen, geben Sie die Gebühr in das Feld **[!UICONTROL Price]** ein.

1. Geben Sie den Wert **[!UICONTROL Search Radius]** in Kilometern für die Standortsuche beim Storefront-Checkout ein.

1. Geben Sie für &quot;**[!UICONTROL Displayed Error Message]**&quot;die Meldung ein, die angezeigt wird, wenn ein In-Store-Versand nicht mehr verfügbar ist.

   Die Standardmeldung lautet `In-Store Delivery is not available. To use this delivery method, please contact us.`

1. Klicken Sie auf **[!UICONTROL Save Config]**.
