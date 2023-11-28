---
title: Auftrag versenden
description: Erfahren Sie, wie Sie die Versandinformationen für einen Verarbeitungsauftrag vervollständigen und die Versand- und Trackinginformationen anzeigen können.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Auftrag versenden

Eine Bestellung, die zwar bezahlt wurde, aber auf eine Lieferung wartet, hat die `Processing` -Status. Der Versanddatensatz enthält einen detaillierten Verlauf des mit der Bestellung verbundenen Ausführungsprozesses. Teillieferungen können bis zur Erfüllung der Bestellung erfolgen.

1. Im _Admin_ Seitenleiste auswählen **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Im _[!UICONTROL Orders]_Liste, suchen Sie die zu versendende Bestellung und klicken Sie auf , um sie zu öffnen.

1. Klicken Sie oben rechts auf die **[!UICONTROL Ship]** Schaltfläche.

1. Wenn Sie die Abrechnungs- oder Lieferadresse aktualisieren möchten, klicken Sie auf das **[!UICONTROL Edit]** in der oberen rechten Ecke des Abschnitts.

   Nehmen Sie die erforderlichen Änderungen vor und klicken Sie auf **[!UICONTROL Save Order Address]**.

1. Um den Anbieter zu veranlassen, einen Versandtitel zu erstellen, wählen Sie die **[!UICONTROL Create Shipping Label]** und legen Sie die Optionen fest:

   - Um eine Trackingnummer hinzuzufügen, scrollen Sie nach unten zum _[!UICONTROL Shipping Information]_und klicken Sie auf **[!UICONTROL Add Tracking Number]**.

   - Führen Sie einen der folgenden Schritte aus:

      - Wählen Sie die **[!UICONTROL Carrier]** und geben Sie das Tracking ein **[!UICONTROL Number]**.

      - Satz **[!UICONTROL Carrier]** nach `Custom Value`eingeben, **[!UICONTROL Title]** für den benutzerdefinierten Netzbetreiber und geben Sie das Tracking ein. **[!UICONTROL Number]**.

      - [Tracking-Informationen anzeigen](#track-the-shipment).

1. Um eine Teillieferung vorzunehmen, scrollen Sie nach unten zum Abschnitt &quot;Artikel zum Schiff&quot;und geben Sie die **[!UICONTROL Qty to Ship]** für jedes Element.

1. Gehen Sie wie folgt vor, um die Kunden per E-Mail über die Lieferung zu informieren:

   - Geben Sie alle Kommentare ein, die Sie in die **[!UICONTROL Shipment Comments]** ankreuzen.

   - Um die Kommentare in die Benachrichtigungs-E-Mail einzuschließen, die an den Kunden gesendet wird, wählen Sie die **[!UICONTROL Append Comments]** aktivieren.

   - Um Ihnen eine Kopie der Versandemail zu senden, wählen Sie die **[!UICONTROL Email Copy of Shipment]** aktivieren.

     Neben der Rechnungsnummer der ausgefüllten Rechnung erscheint der Status einer E-Mail zur Rechnung, entweder als gesendet oder nicht gesendet.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Submit Shipment]**.

   Der Status der Bestellung ändert sich von `Processing` nach `Complete`.

>[!NOTE]
>
>Wenn eine Bestellung als &quot;In-store-Versand&quot;platziert wird, sind keine Versandoptionen verfügbar. Klicks **[!UICONTROL Notify Order is Ready for Pickup]** , um eine E-Mail an den Kunden Trigger. Der Status der Bestellung wird dann in `Complete`.

## Versanddetails anzeigen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Suchen Sie die Sendung in der Liste und klicken Sie auf , um den Datensatz zu öffnen.

1. Wenn Sie der Reihenfolge einen Kommentar hinzufügen möchten, scrollen Sie nach unten zum _[!UICONTROL Comments History]_und geben Sie den Kommentar in das Feld ein.

   - Um den Kommentar per E-Mail an den Kunden zu senden, wählen Sie die **[!UICONTROL Notify Customer by Email]** aktivieren.

   - Um den Kommentar im Kundenkonto zu posten, wählen Sie die **[!UICONTROL Visible on Frontend]** aktivieren.

1. Klicken **[!UICONTROL Submit Comment]**.

## Versand verfolgen

**Methode 1:** Registerkarte &quot;Bestellinformationen&quot;

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie die Versandreihenfolge im Raster und klicken Sie auf **[!UICONTROL View]**.

1. Scrollen Sie nach unten zum _[!UICONTROL Shipping & Handling Information]_und klicken Sie auf **[!UICONTROL Track Order]**.

   Alle verfügbaren Tracking-Informationen werden in einem Popup-Fenster angezeigt.

1. Wenn Sie bereit sind, klicken Sie auf **[!UICONTROL Close Window]**.

**Methode 2:** Tab Bestellung

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Suchen Sie die Sendung in der Liste und klicken Sie auf , um den Datensatz zu öffnen.

1. Klicken **[!UICONTROL Track this Shipment]**.

   Alle verfügbaren Tracking-Informationen werden in einem Popup-Fenster angezeigt.

1. Wenn Sie bereit sind, klicken Sie auf **[!UICONTROL Close Window]**.
