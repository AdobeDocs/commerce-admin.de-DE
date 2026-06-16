---
title: Bestellung versenden
description: Erfahren Sie, wie Sie die Versandinformationen für einen Verarbeitungsauftrag ausfüllen und Versand- und Tracking-Informationen anzeigen.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
TQID: https://experienceleague.adobe.com/w1MPvqsRVfsRwEcRB5uClGM3vnwAda3sOtkZzuLBKAA
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 453
ht-degree: 0%

---

# Bestellung versenden

Eine Bestellung, die bezahlt wurde, aber auf den Versand wartet, hat den Status `Processing`. Der Lieferdatensatz enthält eine detaillierte Historie des Erfüllungsprozesses, der mit der Bestellung verbunden ist. Teillieferungen können bis zur Erfüllung der Bestellung erfolgen.

1. Wählen Sie in der _Admin_-Seitenleiste **[!UICONTROL Sales]** > **[!UICONTROL Orders]** aus.

1. Suchen Sie in der _[!UICONTROL Orders]_die zu versendende Bestellung und klicken Sie darauf, um sie zu öffnen.

1. Klicken Sie oben rechts auf die Schaltfläche **[!UICONTROL Ship]** .

1. Wenn Sie die Rechnungs- oder Lieferadresse aktualisieren möchten, klicken Sie auf den **[!UICONTROL Edit]** Link in der oberen rechten Ecke des Abschnitts.

   Nehmen Sie die erforderlichen Änderungen vor, und klicken Sie auf **[!UICONTROL Save Order Address]**.

1. Um vom Spediteur einen Versandtitel erstellen zu lassen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Create Shipping Label]** und legen Sie die Optionen fest:

   - Um eine Tracking-Nummer hinzuzufügen, scrollen Sie nach unten zum Abschnitt _[!UICONTROL Shipping Information]_und klicken Sie auf **[!UICONTROL Add Tracking Number]**.

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
>Wenn eine Bestellung als „In-Store-Versand“ aufgegeben wird, sind keine Versandoptionen verfügbar. Klicken Sie auf **[!UICONTROL Notify Order is Ready for Pickup]** , um dem Kunden eine E-Mail zu senden. Der Status der Bestellung wird dann in `Complete` geändert.

## Lieferdetails anzeigen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Suchen Sie die Sendung in der Liste und klicken Sie, um den Datensatz zu öffnen.

1. Wenn Sie der Bestellung einen Kommentar hinzufügen möchten, scrollen Sie zum Abschnitt _[!UICONTROL Comments History]_und geben Sie den Kommentar in das Feld ein.

   - Um den Kommentar per E-Mail an den Kunden zu senden, aktivieren Sie das Kontrollkästchen **[!UICONTROL Notify Customer by Email]** .

   - Um den Kommentar im Konto des Kunden zu posten, aktivieren Sie das Kontrollkästchen **[!UICONTROL Visible on Frontend]** .

1. Klicken Sie auf **[!UICONTROL Update]**.

## Verfolgen der Sendung

**Methode 1:** Auf der Registerkarte „Bestellinformationen“

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie den Versandauftrag im Raster und klicken Sie auf **[!UICONTROL View]**.

1. Scrollen Sie nach unten zum Abschnitt _[!UICONTROL Shipping & Handling Information]_und klicken Sie auf **[!UICONTROL Track Order]**.

   Alle verfügbaren Tracking-Informationen werden in einem Popup-Fenster angezeigt.

1. Wenn Sie bereit sind, klicken Sie auf **[!UICONTROL Close Window]**.

**Methode 2:** auf der Registerkarte „Bestellversand“

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Suchen Sie die Sendung in der Liste und klicken Sie, um den Datensatz zu öffnen.

1. Klicken Sie auf **[!UICONTROL Track this Shipment]**.

   Alle verfügbaren Tracking-Informationen werden in einem Popup-Fenster angezeigt.

1. Wenn Sie bereit sind, klicken Sie auf **[!UICONTROL Close Window]**.
