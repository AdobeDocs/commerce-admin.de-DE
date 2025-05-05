---
title: Bestellung versenden
description: Erfahren Sie, wie Sie die Versandinformationen für einen Verarbeitungsauftrag ausfüllen und Versand- und Tracking-Informationen anzeigen.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: abd125cc6e61850db55fb31dbcbd9dc38ac0fca5
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Bestellung versenden

Eine Bestellung, die bezahlt wurde, aber auf den Versand wartet, hat den Status `Processing`. Der Lieferdatensatz enthält eine detaillierte Historie des Erfüllungsprozesses, der mit der Bestellung verbunden ist. Teillieferungen können bis zur Erfüllung der Bestellung erfolgen.

1. Wählen Sie in der _Admin_-Seitenleiste **[!UICONTROL Sales]** > **[!UICONTROL Orders]** aus.

1. Suchen Sie in der _[!UICONTROL Orders]_&#x200B;die zu versendende Bestellung und klicken Sie darauf, um sie zu öffnen.

1. Klicken Sie oben rechts auf die Schaltfläche **[!UICONTROL Ship]** .

1. Wenn Sie die Rechnungs- oder Lieferadresse aktualisieren möchten, klicken Sie auf den **[!UICONTROL Edit]** Link in der oberen rechten Ecke des Abschnitts.

   Nehmen Sie die erforderlichen Änderungen vor, und klicken Sie auf **[!UICONTROL Save Order Address]**.

1. Um vom Spediteur einen Versandtitel erstellen zu lassen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Create Shipping Label]** und legen Sie die Optionen fest:

   - Um eine Tracking-Nummer hinzuzufügen, scrollen Sie nach unten zum Abschnitt _[!UICONTROL Shipping Information]_&#x200B;und klicken Sie auf **[!UICONTROL Add Tracking Number]**.

   - Führen Sie einen der folgenden Schritte aus:

      - Wählen Sie die **[!UICONTROL Carrier]** aus und geben Sie die Tracking-**[!UICONTROL Number]** ein.

      - Legen Sie **[!UICONTROL Carrier]** auf `Custom Value` fest, geben Sie einen **[!UICONTROL Title]** für den benutzerdefinierten Provider ein und geben Sie die Tracking-**[!UICONTROL Number]** ein.

      - [Tracking-Informationen anzeigen](#track-the-shipment).

1. Um eine Teillieferung vorzunehmen, blättern Sie nach unten zum Abschnitt Artikel an Versand und geben Sie die **[!UICONTROL Qty to Ship]** für jeden Artikel ein.

1. Gehen Sie wie folgt vor, um Kundinnen und Kunden per E-Mail über den Versand zu informieren:

   - Geben Sie alle Kommentare ein, die Sie in das **[!UICONTROL Shipment Comments]** aufnehmen möchten.

   - Um die Kommentare in die an den Kunden gesendete Benachrichtigungs-E-Mail einzuschließen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Append Comments]** .

   - Um eine Kopie der Versand-E-Mail an sich selbst zu senden, aktivieren Sie das Kontrollkästchen **[!UICONTROL Email Copy of Shipment]** .

     Der Status einer Rechnungs-E-Mail wird neben der Rechnungsnummer der abgeschlossenen Rechnung entweder als gesendet oder nicht gesendet angezeigt.

1. Klicken Sie abschließend auf **[!UICONTROL Submit Shipment]**.

   Der Status der Bestellung ändert sich von `Processing` zu `Complete`.

>[!NOTE]
>
>Wenn eine Bestellung als „In-Store-Versand“ aufgegeben wird, sind keine Versandoptionen verfügbar. Trigger Klicken Sie auf **[!UICONTROL Notify Order is Ready for Pickup]** , um dem Kunden eine E-Mail zu senden. Der Status der Bestellung wird dann in `Complete` geändert.

## Lieferdetails anzeigen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Suchen Sie die Sendung in der Liste und klicken Sie, um den Datensatz zu öffnen.

1. Wenn Sie der Bestellung einen Kommentar hinzufügen möchten, scrollen Sie zum Abschnitt _[!UICONTROL Comments History]_&#x200B;und geben Sie den Kommentar in das Feld ein.

   - Um den Kommentar per E-Mail an den Kunden zu senden, aktivieren Sie das Kontrollkästchen **[!UICONTROL Notify Customer by Email]** .

   - Um den Kommentar im Konto des Kunden zu posten, aktivieren Sie das Kontrollkästchen **[!UICONTROL Visible on Frontend]** .

1. Klicken Sie auf **[!UICONTROL Update]**.

## Verfolgen der Sendung

**Methode 1:** Auf der Registerkarte „Bestellinformationen“

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie den Versandauftrag im Raster und klicken Sie auf **[!UICONTROL View]**.

1. Scrollen Sie nach unten zum Abschnitt _[!UICONTROL Shipping & Handling Information]_&#x200B;und klicken Sie auf **[!UICONTROL Track Order]**.

   Alle verfügbaren Tracking-Informationen werden in einem Popup-Fenster angezeigt.

1. Wenn Sie bereit sind, klicken Sie auf **[!UICONTROL Close Window]**.

**Methode 2:** auf der Registerkarte „Bestellversand“

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Suchen Sie die Sendung in der Liste und klicken Sie, um den Datensatz zu öffnen.

1. Klicken Sie auf **[!UICONTROL Track this Shipment]**.

   Alle verfügbaren Tracking-Informationen werden in einem Popup-Fenster angezeigt.

1. Wenn Sie bereit sind, klicken Sie auf **[!UICONTROL Close Window]**.
