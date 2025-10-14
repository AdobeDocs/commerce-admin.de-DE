---
title: Seiten-Setup
description: Erfahren Sie, wie Sie die Standardeinstellungen für die Hauptbestandteile einer Shop-Seite konfigurieren.
exl-id: a4310940-0d4f-4948-a271-382f03905bfd
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 0%

---

# Seiten-Setup

Die Hauptabschnitte der Seite werden teilweise durch eine Reihe von standardmäßigen HTML-Tags gesteuert. Einige dieser Tags können verwendet werden, um die Auswahl von Schriftarten, Farbe, Größe, Hintergrundfarben und Bildern zu bestimmen, die in jedem Abschnitt der Seite verwendet werden. Andere Einstellungen steuern Seitenelemente wie das Logo in der Kopfzeile und den Copyright-Hinweis in der Fußzeile. Diese Abschnitte entsprechen der zugrunde liegenden Struktur der HTML-Seite, und viele der grundlegenden Eigenschaften können von der Admin festgelegt werden.

- [HTML Head](#html-head)
- [Kopfzeile](#header)
- [Footer](#footer)

![HTML-Seitenabschnitte](./assets/storefront-home-html-inspect.png){width="700" zoomable="yes"}

## HTML Head

Die Einstellungen im Abschnitt HTML-Kopfzeile entsprechen dem `<head>`-Tag einer HTML-Seite und können für jede Shop-Ansicht konfiguriert werden. Zusätzlich zu Metadaten für Seitentitel, Beschreibung und Schlüsselwörter enthält der Abschnitt einen Link zum Favicon und verschiedene Skripte. Anleitungen für Suchmaschinenroboter und die Anzeige des Demohinweises zum Store werden ebenfalls in diesem Abschnitt konfiguriert.

### Konfigurieren des HTML-Headers

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_&#x200B;auf **[!UICONTROL Edit]**.

1. Erweitern _unter_ Weitere Einstellungen![&#x200B; den Abschnitt **[!UICONTROL HTML Head]** Erweiterungsauswahl](../assets/icon-display-expand.png).

   ![Einstellungen für HTML Head](./assets/configuration-html-head.png){width="500" zoomable="yes"}

1. Aktualisieren Sie [favicon](../getting-started/storefront-branding.md#add-a-favicon) falls erforderlich.

1. Aktualisieren Sie die Einstellungen für den Seitentitel Ihren Anforderungen entsprechend:

   - **[!UICONTROL Default Page Title]**
   - **[!UICONTROL Page Title Prefix]**
   - **[!UICONTROL Page Title Suffix]**

   Sie können ein Suffix und/oder ein Präfix mit dem Standardtitel verwenden, um einen zwei- oder dreiteiligen Titel zu erstellen. Sie können einen vertikalen Balken oder Doppelpunkt als Trennzeichen zwischen dem Präfix oder Suffix und dem Standardtitel hinzufügen.

1. Fügen Sie Metadaten hinzu oder ändern Sie diese, um Suchmaschinenoptimierung (SEO) zu unterstützen und Kunden von Suchergebnissen an Ihren Store zu leiten:

   - **[!UICONTROL Default Meta Description]**
   - **[!UICONTROL Default Meta Keywords]**

1. Geben Sie bei Bedarf **[!UICONTROL Scripts and Style Sheets]** ein.

   >[!NOTE]
   >
   >Alle im Feld [!UICONTROL Scripts and Style Sheets] eingegebenen JavaScript müssen in den Einstellungen der Content Security Policy (CSP) auf die Whitelist gesetzt werden. Andernfalls wird sie nicht auf den Checkout-Seiten ausgeführt. Weitere Informationen finden Sie unter [Content Security Policy](https://developer.adobe.com/commerce/php/development/security/content-security-policies).


1. Aktivieren oder deaktivieren Sie [Demo-Store-Hinweis](../getting-started/storefront-branding.md#set-the-store-demo-notice) falls erforderlich.

1. Klicken Sie abschließend auf **[!UICONTROL Save Configuration]**.

### HTML Head-Feldbeschreibungen

| Feld | Umfang | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Favicon Icon] | Shop-Ansicht | Lädt das kleine Grafikbild hoch, das in der Adressleiste und auf der Registerkarte des Browsers angezeigt wird. Zulässige Dateitypen: ICO, PNG, APNG, GIF und JPG (JPEG). Nicht alle Browser unterstützen diese Formate. |
| [!UICONTROL Default Page Title] | Shop-Ansicht | Der Titel, der in der Titelleiste jeder Seite angezeigt wird, wenn sie in einem Browser angezeigt wird. Der Standardtitel wird für alle Seiten verwendet, es sei denn, für einzelne Seiten wird ein anderer Titel angegeben. |
| [!UICONTROL Page Title Prefix] | Shop-Ansicht | Um einen zwei- oder dreiteiligen Titel zu erstellen, können Sie vor dem Titel ein Präfix hinzufügen. Ein vertikaler Balken oder Doppelpunkt kann als Trennzeichen am Ende des Präfixes verwendet werden, um ihn vom Text des Haupttitels zu unterscheiden. |
| [!UICONTROL Page Title Suffix] | Shop-Ansicht | Ein Suffix kann nach dem Titel hinzugefügt werden, um einen zwei- oder dreiteiligen Titel zu erstellen. Ein vertikaler Balken oder Doppelpunkt kann als Trennzeichen am Ende des Präfixes verwendet werden, um ihn vom Text des Haupttitels zu unterscheiden. |
| [!UICONTROL Default Meta Description] | Shop-Ansicht | Die Beschreibung bietet eine Zusammenfassung Ihrer Site für Suchmaschinenauflistungen und sollte nicht mehr als 160 Zeichen lang sein. |
| [!UICONTROL Default Meta Keywords] | Shop-Ansicht | Eine Reihe von Schlüsselwörtern, die Ihren Store beschreiben, wobei jedes durch ein Komma getrennt ist. |
| [!UICONTROL Scripts and Style Sheets] | Shop-Ansicht | Enthält Skripte, die vor dem schließenden `<head>`-Tag in HTML enthalten sein müssen. Hier können Sie beispielsweise alle JavaScript von Drittanbietern eingeben, die vor dem `<body>`-Tag platziert werden müssen. |
| [!UICONTROL Display Demo Store Notice] | Shop-Ansicht | Steuert die Anzeige der Demo-Store-Benachrichtigung oben auf der Seite. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## Kopfzeile

Die Header-Konfiguration identifiziert den Pfad zu Ihrem Store-Logo und gibt den Logo-Alternativtext und die Begrüßungsnachricht an.

![Header-Konfigurationseinstellungen](./assets/configuration-header.png){width="400" zoomable="yes"}

### Konfigurieren der Kopfzeile

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_&#x200B;auf **[!UICONTROL Edit]**.

1. Erweitern _unter_ Weitere Einstellungen![&#x200B; den Abschnitt **[!UICONTROL Header]** Erweiterungsauswahl](../assets/icon-display-expand.png).

1. Nehmen Sie die für die Store-Ansicht erforderlichen Änderungen vor:

   - [Logo](../getting-started/storefront-branding.md#upload-your-logo) Einstellungen
   - Einstellungen [Willkommensnachricht](../getting-started/storefront-branding.md#change-the-welcome-message)

1. Klicken Sie abschließend auf **[!UICONTROL Save Configuration]**.

### Beschreibungen der Header-Felder

| Feld | Umfang | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Logo Image] | Shop-Ansicht | Gibt den Pfad zum Logo an, das in der Kopfzeile angezeigt wird. Unterstützte Dateitypen: PNG, GIF, JPG (JPEG) |
| [!UICONTROL Logo Attribute Width] | Shop-Ansicht | Die Breite Ihres Logobilds in Pixel. |
| [!UICONTROL Logo Attribute Height] | Shop-Ansicht | Die Höhe des Logobilds in Pixel. |
| [!UICONTROL Welcome Text] | Shop-Ansicht | Die Begrüßungsnachricht wird in der Kopfzeile der Seite angezeigt und enthält den Namen der angemeldeten Kunden. |
| [!UICONTROL Logo Image Alt] | Shop-Ansicht | Der Alternativtext, der mit dem Logo verknüpft ist. |
| [!UICONTROL Translate Title] | Shop-Ansicht | Legt fest, ob die `Page Title` oder `Meta Title` übersetzt werden sollen. |

{style="table-layout:auto"}

## Footer

Im Abschnitt „Konfiguration der Fußzeile“ können Sie den [Copyright-Hinweis](../getting-started/storefront-branding.md#change-the-copyright-notice), der unten auf der Seite angezeigt wird, aktualisieren und verschiedene Skripte eingeben, die vor dem schließenden `<body>`-Tag positioniert werden müssen.

![Footer-Konfigurationseinstellungen](./assets/configuration-footer.png){width="400" zoomable="yes"}

### Konfigurieren der Fußzeile

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_&#x200B;auf **[!UICONTROL Edit]**.

1. Erweitern _unter_ Weitere Einstellungen![&#x200B; den Abschnitt **[!UICONTROL Footer]** Erweiterungsauswahl](../assets/icon-display-expand.png).

1. Nehmen Sie die erforderlichen Änderungen an den Einstellungen **[!UICONTROL Copyright]** und **[!UICONTROL Miscellaneous HTML]** vor.

   >[!NOTE]
   >
   >Alle im Feld [!UICONTROL Miscellaneous HTML] eingegebenen JavaScript müssen in den Einstellungen der Content Security Policy (CSP) auf die Whitelist gesetzt werden. Andernfalls wird sie nicht auf den Checkout-Seiten ausgeführt. Weitere Informationen finden Sie unter [Content Security Policy](https://developer.adobe.com/commerce/php/development/security/content-security-policies).

1. Klicken Sie abschließend auf **[!UICONTROL Save Configuration]**.

## Beschreibung der Fußzeilenfelder

| Feld | Umfang | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Miscellaneous HTML] | Shop-Ansicht | Ein Eingabefeld, in das Sie verschiedene Skripte auf den Server hochladen können, die unmittelbar vor dem schließenden `<body>`-Tag platziert werden müssen. |
| [!UICONTROL Copyright] | Shop-Ansicht | Die Copyright-Erklärung, die unten auf jeder Seite angezeigt wird. Um das Copyright-Symbol einzuschließen, verwenden Sie den HTML-Zeichenentitäts-`\&copy;` wie folgt: `\&copy; 2021 Commerce Demo Store. All Rights Reserved.` Achten Sie darauf, den Beispiel-Copyright-Hinweis durch Ihren eigenen zu ersetzen. |
| [!UICONTROL Display Report Bugs Link] | Shop-Ansicht | Bestimmt, ob der Link zum Fehlerbericht (unterstützt für einige Designs) aktiviert oder deaktiviert ist. |

{style="table-layout:auto"}
