---
title: Verkaufsdokumente
description: Erfahren Sie, wie Sie Verkaufsdokumente konfigurieren, um Kundenbestellungen und die Erfüllung Ihrer Commerce-Geschäfte zu unterstützen.
exl-id: 869d79ca-688a-4032-a95c-c66ebf7f2775
feature: Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Verkaufsdokumente

Um den Bestellworkflow zu unterstützen und Ihren Kunden Dokumentation zu den von ihnen gesendeten Bestellungen bereitzustellen, konfigurieren Sie die entsprechenden Verkaufsdokumente so, dass sie Ihre Store-Marke widerspiegeln und Referenzinformationen enthalten.

## Rechnungen und Packungsbeilagen konfigurieren

Im Gegensatz zu den Logobildern, die in Schaufensterseiten verwendet werden, kann das Logo für PDF-Rechnungen und andere Verkaufsdokumente ein hochauflösendes 300-dpi-Bild sein. Achten Sie darauf, das Seitenverhältnis beizubehalten, wenn Sie die Größe des Logos ändern. Ändern Sie die Größe des Logos so, dass es der Höhe entspricht, und sorgen Sie sich nicht um ungenutzten Platz auf der rechten Seite.

![Beispiellogo](./assets/logo-pdf.png){width="200"}

Eine Möglichkeit, die Größe Ihres Logos an die gewünschte Größe anzupassen, besteht darin, ein neues, leeres Bild mit den richtigen Abmessungen zu erstellen. Fügen Sie dann Ihr Logo-Bild ein und passen Sie die Größe an die Höhe an. Bei den meisten Bildbearbeitungsprogrammen können Sie das Seitenverhältnis entweder um einen Prozentwert skalieren oder die Umschalttaste gedrückt halten und die Größe des Bildes manuell ändern.

**_So aktualisieren Sie das Logo:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Sales]** und wählen Sie unter &quot;**[!UICONTROL Sales]**&quot;.

1. Erweitern Sie den Abschnitt **[!UICONTROL Invoice and Packing Slip Design]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   ![Verkaufskonfiguration - Entwurf der Verkaufsrechnung und des Verpackungsformulars](../configuration-reference/sales/assets/sales-invoice-packing-slip-design.png){width="600" zoomable="yes"}

   - Um die **[!UICONTROL Logo for PDF Print-outs]** hochzuladen, klicken Sie auf **[!UICONTROL Choose File]**, suchen Sie das von Ihnen vorbereitete Logo und klicken Sie auf **[!UICONTROL Open]**.

   - Um die **[!UICONTROL Logo for HTML Print View]** hochzuladen, klicken Sie auf **[!UICONTROL Choose File]**, suchen Sie das von Ihnen vorbereitete Logo und klicken Sie auf **[!UICONTROL Open]**.

   - Geben Sie Ihre Adresse so ein, wie sie auf den Rechnungen und Packstücken erscheinen soll.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

   Als Referenz wird vor jedem Feld eine Miniaturansicht des hochgeladenen Bildes angezeigt. Machen Sie sich keine Gedanken, ob die Miniaturansicht verzerrt angezeigt wird. Der Anteil des Logos ist auf der Rechnung korrekt.

### Ersetzen eines Bildes

1. Klicken Sie auf **[!UICONTROL Choose File]** und wählen Sie eine andere Logodatei aus.

1. Aktivieren Sie das Kontrollkästchen **[!UICONTROL Delete Image]** für das Bild, das Sie ersetzen möchten.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

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

![Verkaufskonfiguration - PDF print-outs](./assets/config-sales-pdf-print-outs.png){width="600" zoomable="yes"}

**_So ändern Sie die Reihenfolge-ID-Einstellung:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL PDF Print-outs]** aus.

1. Erweitern Sie den Abschnitt **Rechnung** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png).

1. Legen Sie **[!UICONTROL Display Order ID in Header]** entsprechend Ihrer Voreinstellung fest.

1. Wiederholen Sie diese Schritte für die Abschnitte **[!UICONTROL Shipment]** und **[!UICONTROL Credit Memo]**.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

**_So ändern Sie die Einstellung der Kunden-IP-Adresse:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Sales]** und wählen Sie unter &quot;**[!UICONTROL Sales]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL General]** .

   ![Verkaufskonfiguration - Allgemeine Verkaufseinstellungen](../configuration-reference/sales/assets/sales-general.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Hide Customer IP]** auf Ihre Voreinstellung fest.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
