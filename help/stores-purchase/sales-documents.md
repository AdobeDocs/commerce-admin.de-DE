---
title: Verkaufsdokumente
description: Erfahren Sie, wie Sie Verkaufsdokumente konfigurieren, um Kundenbestellungen und die Erfüllung Ihrer Commerce-Geschäfte zu unterstützen.
exl-id: 869d79ca-688a-4032-a95c-c66ebf7f2775
feature: Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Verkaufsdokumente

Um den Bestellworkflow zu unterstützen und Ihren Kunden Dokumentation zu den von ihnen gesendeten Bestellungen bereitzustellen, konfigurieren Sie die entsprechenden Verkaufsdokumente so, dass sie Ihre Store-Marke widerspiegeln und Referenzinformationen enthalten.

## Rechnungen und Packungsbeilagen konfigurieren

Im Gegensatz zu den Logobildern, die in Schaufensterseiten verwendet werden, kann das Logo für PDF-Rechnungen und andere Verkaufsdokumente ein hochauflösendes 300-dpi-Bild sein. Achten Sie darauf, das Seitenverhältnis beizubehalten, wenn Sie die Größe des Logos ändern. Ändern Sie die Größe des Logos so, dass es der Höhe entspricht, und sorgen Sie sich nicht um ungenutzten Platz auf der rechten Seite.

![Beispiellogo](./assets/logo-pdf.png){width="200"}

Eine Möglichkeit, die Größe Ihres Logos an die gewünschte Größe anzupassen, besteht darin, ein neues, leeres Bild mit den richtigen Abmessungen zu erstellen. Fügen Sie dann Ihr Logo-Bild ein und passen Sie die Größe an die Höhe an. Bei den meisten Bildbearbeitungsprogrammen können Sie das Seitenverhältnis entweder um einen Prozentwert skalieren oder die Umschalttaste gedrückt halten und die Größe des Bildes manuell ändern.

**_So aktualisieren Sie das Logo:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Sales]** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Invoice and Packing Slip Design]** und führen Sie folgende Schritte aus:

   ![Vertriebskonfiguration - Verkaufsrechnung und Entwurf der Verpackungsauszüge](../configuration-reference/sales/assets/sales-invoice-packing-slip-design.png){width="600" zoomable="yes"}

   - So laden Sie die **[!UICONTROL Logo for PDF Print-outs]** klicken **[!UICONTROL Choose File]**, suchen Sie das von Ihnen vorbereitete Logo und klicken Sie auf **[!UICONTROL Open]**.

   - So laden Sie die **[!UICONTROL Logo for HTML Print View]** klicken **[!UICONTROL Choose File]**, suchen Sie das von Ihnen vorbereitete Logo und klicken Sie auf **[!UICONTROL Open]**.

   - Geben Sie Ihre Adresse so ein, wie sie auf den Rechnungen und Packstücken erscheinen soll.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

   Als Referenz wird vor jedem Feld eine Miniaturansicht des hochgeladenen Bildes angezeigt. Machen Sie sich keine Gedanken, ob die Miniaturansicht verzerrt angezeigt wird. Der Anteil des Logos ist auf der Rechnung korrekt.

### Ersetzen eines Bildes

1. Klicks **[!UICONTROL Choose File]** und wählen Sie eine andere Logodatei aus.

1. Wählen Sie die **[!UICONTROL Delete Image]** für das Bild, das Sie ersetzen möchten.

1. Klicken **[!UICONTROL Save Config]**.

### Bildformate

| Format | Voraussetzungen |
|--- |------------------------------------------|
| **_PDF_** |  |
| Dateiformat | JPG (JPEG), PNG, TIF (TIFF) |
| Bildgröße | Bis zu 1080 Pixel breit x 270 Pixel hoch |
| Auflösung | 300 DPI empfohlen |
| **_HTML_** |  |
| Dateiformat | JPG (JPEG), PNG, GIF |
| Bildgröße | Ermittelt durch Design. |
| Auflösung | 72 oder 96 DPI |

{style="table-layout:auto"}

## Referenz-IDs hinzufügen

Die Bestell-ID und die Kunden-IP-Adresse können in der Kopfzeile von Verkaufsdokumenten enthalten sein, die eine Bestellung begleiten. Standardmäßig werden sowohl die Bestell-ID als auch die Kunden-IP-Adresse in der Kopfzeile von Rechnungen, Lieferpackungen und Kreditkarten angezeigt.

![Vertriebskonfiguration - PDF-Print-outs](./assets/config-sales-pdf-print-outs.png){width="600" zoomable="yes"}

**_So ändern Sie die Bestell-ID-Einstellung:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL PDF Print-outs]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **Rechnung** Abschnitt.

1. Satz **[!UICONTROL Display Order ID in Header]** nach Ihren Wünschen.

1. Wiederholen Sie diesen Vorgang für die **[!UICONTROL Shipment]** und **[!UICONTROL Credit Memo]** Abschnitte.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

**_So ändern Sie die Einstellung der Kunden-IP-Adresse:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Sales]** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL General]** Abschnitt.

   ![Vertriebskonfiguration - Allgemeine Verkaufseinstellungen](../configuration-reference/sales/assets/sales-general.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Hide Customer IP]** nach Ihren Wünschen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
