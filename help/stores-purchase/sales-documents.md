---
title: Verkaufsunterlagen
description: Erfahren Sie, wie Sie Vertriebsdokumente konfigurieren, um Kundenbestellungen und die Erfüllung Ihrer Anforderungen an Ihren Commerce-Store zu unterstützen.
exl-id: 869d79ca-688a-4032-a95c-c66ebf7f2775
feature: Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Verkaufsunterlagen

Um den Auftrags-Workflow zu unterstützen und Ihren Kunden Dokumentation zu den von ihnen gesendeten Bestellungen bereitzustellen, konfigurieren Sie die zugehörigen Verkaufsdokumente so, dass sie Ihre Shop-Marke widerspiegeln, und geben Sie Referenzinformationen an.

## Konfigurieren von Rechnungen und Lieferscheinen

Im Gegensatz zu den Logo-Bildern, die auf Storefront-Seiten verwendet werden, kann das Logo zum PDF von Rechnungen und anderen Verkaufsdokumenten ein hochauflösendes 300-dpi-Bild sein. Achten Sie darauf, das Seitenverhältnis beizubehalten, wenn Sie die Größe des Logos ändern. Ändern Sie die Größe des Logos so, dass es der Höhe entspricht, und sorgen Sie sich nicht um ungenutzten Platz auf der rechten Seite.

![Beispiellogo](./assets/logo-pdf.png){width="200"}

Eine Möglichkeit, die Größe Ihres Logos an die erforderliche Größe anzupassen, besteht darin, ein neues, leeres Bild mit den richtigen Abmessungen zu erstellen. Fügen Sie dann Ihr Logo-Bild ein und passen Sie die Größe an die Höhe an. Bei den meisten Bildbearbeitungsprogrammen können Sie das Bild entweder prozentual skalieren, um das Seitenverhältnis beizubehalten, oder bei gedrückter Umschalttaste die Bildgröße manuell ändern.

**_So aktualisieren Sie das Logo:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie darunter **[!UICONTROL Sales]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Invoice and Packing Slip Design]** und führen Sie folgende Schritte aus:

   ![Verkaufskonfiguration - Verkaufsrechnungs- und Lieferscheinentwurf](../configuration-reference/sales/assets/sales-invoice-packing-slip-design.png){width="600" zoomable="yes"}

   - Um die **[!UICONTROL Logo for PDF Print-outs]** hochzuladen, klicken Sie auf **[!UICONTROL Choose File]**, suchen Sie das von Ihnen vorbereitete Logo und klicken Sie auf **[!UICONTROL Open]**.

   - Um die **[!UICONTROL Logo for HTML Print View]** hochzuladen, klicken Sie auf **[!UICONTROL Choose File]**, suchen Sie das von Ihnen vorbereitete Logo und klicken Sie auf **[!UICONTROL Open]**.

   - Geben Sie Ihre Adresse so ein, wie sie auf Rechnungen und Lieferscheinen erscheinen soll.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

   Als Referenz wird vor jedem Feld eine Miniaturansicht des hochgeladenen Bildes angezeigt. Machen Sie sich keine Gedanken, wenn die Miniaturansicht verzerrt erscheint. Der Anteil des Logos ist auf der Rechnung korrekt.

### Ersetzen eines Bildes

1. Klicken Sie auf **[!UICONTROL Choose File]** und wählen Sie eine andere Logodatei.

1. Aktivieren Sie das Kontrollkästchen **[!UICONTROL Delete Image]** für das Bild, das Sie ersetzen möchten.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

### Bildformate

| Format | Anforderungen |
|--- |------------------------------------------|
| **_PDF_** |  |
| Dateiformat | JPG (JPEG), PNG, TIF (TIFF) |
| Bildgröße | Bis zu 1080 Pixel breit x 270 Pixel hoch |
| Auflösung | 300 DPI empfohlen |
| **_HTML_** |  |
| Dateiformat | JPG (JPEG), PNG, GIF |
| Bildgröße | Wird durch das Design bestimmt. |
| Auflösung | 72 oder 96 DPI |

{style="table-layout:auto"}

## Hinzufügen von Referenz-IDs

Die Auftrags-ID und die Kunden-IP-Adresse können in die Kopfzeile der Verkaufsdokumente aufgenommen werden, die einer Bestellung beiliegen. Standardmäßig werden sowohl die Auftrags-ID als auch die Kunden-IP-Adresse in der Kopfzeile von Rechnungen, Lieferscheinen und Gutschriften angezeigt.

![Verkaufskonfiguration - PDF-Ausdrucke](./assets/config-sales-pdf-print-outs.png){width="600" zoomable="yes"}

**_So ändern Sie die Einstellung der Auftrags-ID:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL PDF Print-outs]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **Rechnung** .

1. Stellen Sie **[!UICONTROL Display Order ID in Header]** entsprechend Ihren Anforderungen ein.

1. Wiederholen Sie diesen Vorgang für die **[!UICONTROL Shipment]** und **[!UICONTROL Credit Memo]** Abschnitte.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

**_So ändern Sie die Einstellung der Kunden-IP-Adresse:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie darunter **[!UICONTROL Sales]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL General]** .

   ![Verkaufskonfiguration - Allgemeine Verkaufseinstellungen](../configuration-reference/sales/assets/sales-general.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Hide Customer IP]** auf Ihre Voreinstellung fest.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
