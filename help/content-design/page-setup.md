---
title: Seiteneinrichtung
description: Erfahren Sie, wie Sie die Standardeinstellungen für die Hauptteile einer Store-Seite konfigurieren.
exl-id: a4310940-0d4f-4948-a271-382f03905bfd
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Seiteneinrichtung

Die Hauptabschnitte der Seite werden teilweise durch eine Reihe von Standard-HTML-Tags gesteuert. Einige dieser Tags können verwendet werden, um die Auswahl von Schriftarten, Farbe, Größe, Hintergrundfarben und Bildern zu bestimmen, die in den einzelnen Abschnitten der Seite verwendet werden. Andere Einstellungen steuern Seitenelemente wie das Logo in der Kopfzeile und den Copyright-Hinweis in der Fußzeile. Diese Abschnitte entsprechen der zugrunde liegenden Struktur der HTML-Seite und viele der grundlegenden Eigenschaften können vom Administrator festgelegt werden.

- [HTML-Head](#html-head)
- [Kopfzeile](#header)
- [Fußzeile](#footer)

![HTML-Seitenabschnitte](./assets/storefront-home-html-inspect.png){width="700" zoomable="yes"}

## HTML-Head

Die Einstellungen im Bereich HTML-Head entsprechen dem `<head>` -Tag einer HTML-Seite und kann für jede Store-Ansicht konfiguriert werden. Zusätzlich zu den Metadaten für Seitentitel, Beschreibung und Keywords enthält der Abschnitt einen Link zum Favicon sowie verschiedene Skripte. Anweisungen für Suchmaschinen-Roboter und die Anzeige des Store-Demohinweises werden ebenfalls in diesem Abschnitt konfiguriert.

### Konfigurieren des HTML-Head

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie auf **[!UICONTROL Edit]** im _[!UICONTROL Action]_Spalte.

1. under _Andere Einstellungen_, erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL HTML Head]** Abschnitt.

   ![HTML-Head-Konfigurationseinstellungen](./assets/configuration-html-head.png){width="500" zoomable="yes"}

1. Aktualisieren Sie die [favicon](../getting-started/storefront-branding.md#add-a-favicon) bei Bedarf.

1. Aktualisieren Sie die Einstellungen für den Seitentitel entsprechend Ihren Anforderungen:

   - **[!UICONTROL Default Page Title]**
   - **[!UICONTROL Page Title Prefix]**
   - **[!UICONTROL Page Title Suffix]**

   Sie können ein Suffix und/oder Präfix mit dem Standardtitel verwenden, um einen zweiteiligen oder dreiteiligen Titel zu erstellen. Sie können einen vertikalen Balken oder Doppelpunkt als Trennzeichen zwischen dem Präfix oder Suffix und dem Standardtitel hinzufügen.

1. Fügen Sie Metadaten hinzu oder ändern Sie sie, die die Suchmaschinenoptimierung (SEO) unterstützen und Kunden von Suchergebnissen aus zu Ihrem Store führen:

   - **[!UICONTROL Default Meta Description]**
   - **[!UICONTROL Default Meta Keywords]**

1. Beliebige eingeben **[!UICONTROL Scripts and Style Sheets]** nach Bedarf.

1. Aktivieren oder deaktivieren Sie die [Demostore-Hinweis](../getting-started/storefront-branding.md#set-the-store-demo-notice) bei Bedarf.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Configuration]**.

### Feldbeschreibungen für HTML-Kopfzeilen

| Feld | Anwendungsbereich | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Favicon Icon] | Store-Ansicht | Lädt das kleine grafische Bild hoch, das in der Adressleiste und auf der Registerkarte des Browsers angezeigt wird. Zulässige Dateitypen: ICO, PNG, APNG, GIF und JPG (JPEG). Diese Formate werden nicht von allen Browsern unterstützt. |
| [!UICONTROL Default Page Title] | Store-Ansicht | Der Titel, der in der Titelleiste jeder Seite angezeigt wird, wenn er in einem Browser angezeigt wird. Der Standardtitel wird für alle Seiten verwendet, es sei denn, für einzelne Seiten wird ein anderer Titel angegeben. |
| [!UICONTROL Page Title Prefix] | Store-Ansicht | Vor dem Titel kann ein Präfix hinzugefügt werden, um einen zweiteiligen oder dreiteiligen Titel zu erstellen. Ein vertikaler Balken oder Doppelpunkt kann als Trennzeichen am Ende des Präfixes verwendet werden, um ihn vom Text des Haupttitels zu unterscheiden. |
| [!UICONTROL Page Title Suffix] | Store-Ansicht | Nach dem Titel kann ein Suffix hinzugefügt werden, um einen zweiteiligen oder dreiteiligen Titel zu erstellen. Ein vertikaler Balken oder Doppelpunkt kann als Trennzeichen am Ende des Präfixes verwendet werden, um ihn vom Text des Haupttitels zu unterscheiden. |
| [!UICONTROL Default Meta Description] | Store-Ansicht | Die Beschreibung bietet eine Zusammenfassung Ihrer Site für Suchmaschinenlisten mit einer Länge von maximal 160 Zeichen. |
| [!UICONTROL Default Meta Keywords] | Store-Ansicht | Eine Reihe von Suchbegriffen, die Ihren Store beschreiben, von denen jeder durch ein Komma getrennt ist. |
| [!UICONTROL Scripts and Style Sheets] | Store-Ansicht | Enthält Skripte, die vor dem schließenden HTML in den -Abschnitt eingefügt werden müssen `<head>` -Tag. Beispielsweise alle JavaScript-Dateien von Drittanbietern, die vor dem `<body>` -Tag können hier eingegeben werden. |
| [!UICONTROL Display Demo Store Notice] | Store-Ansicht | Steuert die Anzeige des Demospeicherhinweises oben auf der Seite. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## Kopfzeile

Die Kopfzeilenkonfiguration identifiziert den Pfad zu Ihrem Store-Logo und gibt den ALT-Text und die Willkommensnachricht des Logos an.

![Einstellungen für die Kopfzeilenkonfiguration](./assets/configuration-header.png){width="400" zoomable="yes"}

### Konfigurieren der Kopfzeile

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie auf **[!UICONTROL Edit]** im _[!UICONTROL Action]_Spalte.

1. under _Andere Einstellungen_, erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Header]** Abschnitt.

1. Nehmen Sie alle für die Store-Ansicht erforderlichen Änderungen vor:

   - [Logo](../getting-started/storefront-branding.md#upload-your-logo) settings
   - [Willkommensnachricht](../getting-started/storefront-branding.md#change-the-welcome-message) settings

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Configuration]**.

### Beschreibungen der Kopfzeilenfelder

| Feld | Anwendungsbereich | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Logo Image] | Store-Ansicht | Gibt den Pfad zum Logo an, das in der Kopfzeile angezeigt wird. Unterstützte Dateitypen: PNG, GIF, JPG (JPEG) |
| [!UICONTROL Logo Attribute Width] | Store-Ansicht | Die Breite des Logobilds in Pixel. |
| [!UICONTROL Logo Attribute Height] | Store-Ansicht | Die Höhe des Logobilds in Pixel. |
| [!UICONTROL Welcome Text] | Store-Ansicht | Die Willkommensnachricht wird in der Kopfzeile der Seite angezeigt und enthält den Namen der angemeldeten Kunden. |
| [!UICONTROL Logo Image Alt] | Store-Ansicht | Der Alt-Text, der mit dem Logo verknüpft ist. |
| [!UICONTROL Translate Title] | Store-Ansicht | Bestimmt, ob die `Page Title` oder `Meta Title` übersetzt werden. |

{style="table-layout:auto"}

## Fußzeile

Im Abschnitt zur Fußzeilenkonfiguration können Sie die [Copyright-Hinweis](../getting-started/storefront-branding.md#change-the-copyright-notice) die unten auf der Seite angezeigt wird, und geben Sie verschiedene Skripte ein, die vor dem schließenden `<body>` -Tag.

![Fußzeilenkonfigurationseinstellungen](./assets/configuration-footer.png){width="400" zoomable="yes"}

### Fußzeile konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie auf **[!UICONTROL Edit]** im _[!UICONTROL Action]_Spalte.

1. under _Andere Einstellungen_, erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Footer]** Abschnitt.

1. Nehmen Sie die erforderlichen Änderungen an der **[!UICONTROL Copyright]** und **[!UICONTROL Miscellaneous HTML]** -Einstellungen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Configuration]**.

## Beschreibung der Fußzeilen

| Feld | Anwendungsbereich | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Miscellaneous HTML] | Store-Ansicht | Ein Eingabefeld, in das Sie verschiedene Skripte auf den Server hochladen können, die direkt vor dem schließenden `<body>` -Tag. |
| [!UICONTROL Copyright] | Store-Ansicht | Die Urheberrechtserklärung, die unten auf jeder Seite angezeigt wird. Verwenden Sie die Entität für HTML-Zeichen, um das Copyright-Symbol einzuschließen. `\&copy;` wie folgt: `\&copy; 2021 Commerce Demo Store. All Rights Reserved.` Stellen Sie sicher, dass Sie den Beispiel-Copyright-Hinweis durch Ihren eigenen ersetzen. |
| [!UICONTROL Display Report Bugs Link] | Store-Ansicht | Bestimmt, ob der Link zum Fehlerbericht (der für einige Designs unterstützt wird) aktiviert oder deaktiviert ist. |

{style="table-layout:auto"}
