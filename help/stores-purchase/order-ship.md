---
title: Auftrag versenden
description: Erfahren Sie, wie Sie die Versandinformationen für einen Verarbeitungsauftrag vervollständigen und die Versand- und Trackinginformationen anzeigen können.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Auftrag versenden

Eine Bestellung, die zwar bezahlt wurde, aber auf eine Sendung wartet, hat den Status `Processing`. Der Versanddatensatz enthält einen detaillierten Verlauf des mit der Bestellung verbundenen Ausführungsprozesses. Teillieferungen können bis zur Erfüllung der Bestellung erfolgen.

1. Wählen Sie in der Seitenleiste _Admin_ **[!UICONTROL Sales]** > **[!UICONTROL Orders]** aus.

1. Suchen Sie in der Liste &quot;_[!UICONTROL Orders]_&quot; die zu versendende Bestellung und klicken Sie auf , um sie zu öffnen.

1. Klicken Sie in der oberen rechten Ecke auf die Schaltfläche **[!UICONTROL Ship]** .

1. Wenn Sie die Abrechnungs- oder Lieferadresse aktualisieren möchten, klicken Sie auf den Link **[!UICONTROL Edit]** in der oberen rechten Ecke des Abschnitts.

   Nehmen Sie die erforderlichen Änderungen vor und klicken Sie auf **[!UICONTROL Save Order Address]**.

1. Um den Netzbetreiber dazu zu bewegen, einen Versandtitel zu erstellen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Create Shipping Label]** und legen Sie die Optionen fest:

   - Um eine Tracking-Nummer hinzuzufügen, scrollen Sie nach unten zum Abschnitt _[!UICONTROL Shipping Information]_und klicken Sie auf **[!UICONTROL Add Tracking Number]**.

   - Führen Sie einen der folgenden Schritte aus:

      - Wählen Sie den Wert **[!UICONTROL Carrier]** aus und geben Sie das Tracking **[!UICONTROL Number]** ein.

      - Setzen Sie **[!UICONTROL Carrier]** auf `Custom Value`, geben Sie einen **[!UICONTROL Title]** für den benutzerdefinierten Träger ein und geben Sie das Tracking **[!UICONTROL Number]** ein.

      - [Tracking-Informationen anzeigen](#track-the-shipment).

1. Um eine Teillieferung vorzunehmen, scrollen Sie nach unten zum Abschnitt Artikel zum Schiff und geben Sie für jedes Element den Wert **[!UICONTROL Qty to Ship]** ein.

1. Gehen Sie wie folgt vor, um die Kunden per E-Mail über die Lieferung zu informieren:

   - Geben Sie alle Kommentare ein, die Sie in das Feld **[!UICONTROL Shipment Comments]** aufnehmen möchten.

   - Um die Kommentare in die Benachrichtigungs-E-Mail einzuschließen, die an den Kunden gesendet wird, aktivieren Sie das Kontrollkästchen **[!UICONTROL Append Comments]** .

   - Um Ihnen eine Kopie der Versand-E-Mail zu senden, aktivieren Sie das Kontrollkästchen **[!UICONTROL Email Copy of Shipment]** .

     Neben der Rechnungsnummer der ausgefüllten Rechnung erscheint der Status einer E-Mail zur Rechnung, entweder als gesendet oder nicht gesendet.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Submit Shipment]**.

   Der Status der Reihenfolge ändert sich von `Processing` in `Complete`.

>[!NOTE]
>
>Wenn eine Bestellung als &quot;In-store-Versand&quot;platziert wird, sind keine Versandoptionen verfügbar. Klicken Sie auf **[!UICONTROL Notify Order is Ready for Pickup]** , um eine E-Mail an den Kunden Trigger. Der Status der Bestellung wird dann in `Complete` geändert.

## Versanddetails anzeigen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Suchen Sie die Sendung in der Liste und klicken Sie auf , um den Datensatz zu öffnen.

1. Wenn Sie der Bestellung einen Kommentar hinzufügen möchten, scrollen Sie nach unten zum Abschnitt &quot;_[!UICONTROL Comments History]_&quot;und geben Sie den Kommentar in das Feld ein.

   - Um den Kommentar per E-Mail an den Kunden zu senden, aktivieren Sie das Kontrollkästchen **[!UICONTROL Notify Customer by Email]** .

   - Um den Kommentar im Kundenkonto zu posten, aktivieren Sie das Kontrollkästchen **[!UICONTROL Visible on Frontend]** .

1. Klicken Sie auf **[!UICONTROL Submit Comment]**.

## Versand verfolgen

**Methode 1:** Registerkarte &quot;Bestellinformationen&quot;

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie die Versandreihenfolge im Raster und klicken Sie auf **[!UICONTROL View]**.

1. Scrollen Sie nach unten zum Abschnitt _[!UICONTROL Shipping & Handling Information]_und klicken Sie auf **[!UICONTROL Track Order]**.

   Alle verfügbaren Tracking-Informationen werden in einem Popup-Fenster angezeigt.

1. Wenn Sie bereit sind, klicken Sie auf **[!UICONTROL Close Window]**.

**Methode 2:** Von der Registerkarte &quot;Bestellversand&quot;

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Suchen Sie die Sendung in der Liste und klicken Sie auf , um den Datensatz zu öffnen.

1. Klicken Sie auf **[!UICONTROL Track this Shipment]**.

   Alle verfügbaren Tracking-Informationen werden in einem Popup-Fenster angezeigt.

1. Wenn Sie bereit sind, klicken Sie auf **[!UICONTROL Close Window]**.
