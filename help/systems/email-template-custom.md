---
title: E-Mail-Vorlagen anpassen
description: Erfahren Sie, wie Sie E-Mail-Vorlagen für jede Website, jeden Store oder jede Store-Ansicht anpassen.
exl-id: d328b84d-fab7-4956-9071-2d8848f7c21e
feature: Communications, Configuration
source-git-commit: c0d6523f820558c8cd6cfa6b745568784b9e784c
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 0%

---

# E-Mail-Vorlagen anpassen

Commerce enthält eine standardmäßige E-Mail-Vorlage für den Hauptteil jeder Nachricht, die vom System gesendet wird. Die Vorlage für den Hauptteil des Inhalts wird mit den Kopf- und Fußzeilenvorlagen kombiniert, um die vollständige Nachricht zu erstellen. Der Inhalt ist mit HTML und CSS formatiert und kann einfach bearbeitet und angepasst werden, indem [Variablen](variables-predefined.md) hinzugefügt werden. E-Mail-Vorlagen können für jede Website, jeden Store oder jede Store-Ansicht angepasst werden. Wenn Sie benutzerdefinierte Vorlagen verwenden, aktualisieren Sie die [Systemkonfiguration](email-templates.md#configure-email-templates) um sicherzustellen, dass die richtige Vorlage verwendet wird. Informationen dazu, wie Sie bedingte Anweisungen zum Anpassen der E-Mail-Vorlage verwenden können, finden Sie unter [Entwicklerdokumentation](https://developer.adobe.com/commerce/frontend-core/guide/templates/email/#theme-based-customizations-1).

![Beispiel - Vorschau für Willkommens-E-Mails](./assets/email-template-preview.png){width="500" zoomable="yes"}

Die Standardvorlagen enthalten Ihr Logo und Store-Informationen und können ohne weitere Anpassung verwendet werden. Als Best Practice sollten Sie jedoch jede Vorlage anzeigen und alle erforderlichen Änderungen vornehmen, bevor Sie sie an Kunden senden.

- [Kopfzeilenvorlage](email-template-custom.md#header-template)
- [Footer-Vorlage](email-template-custom.md#footer-template)
- [Nachrichtenvorlagen](email-template-custom.md#message-templates)

![E-Mail-Vorlagen](./assets/email-templates.png){width="700" zoomable="yes"}

## Vorlageninformationen

| Feld | Beschreibung |
| ----- | ----------- |
| [!UICONTROL Template Name] | Der Name Ihrer benutzerdefinierten Vorlage. |
| [!UICONTROL Insert Variable] | Fügt an der Cursorposition eine Variable in die Vorlage ein. |
| [!UICONTROL Template Subject] | Der Vorlagenbetreff wird in der Spalte Betreff angezeigt und kann zum Sortieren und Filtern der Vorlagen in der Liste verwendet werden. |
| [!UICONTROL Template Content] | Der Inhalt der Vorlage auf HTML. |
| [!UICONTROL Template Styles] | Alle CSS-Stildeklarationen, die zum Formatieren der Vorlage erforderlich sind, können in das _[!UICONTROL Template Styles]_eingegeben werden. |

{style="table-layout:auto"}

## Kopfzeilenvorlage

Nach Abschluss der [Konfiguration](email-templates.md#configure-email-templates) enthält die E-Mail-Header-Vorlage Ihr Logo, das mit Ihrem Store verknüpft ist. Wenn Sie über Grundkenntnisse im HTML verfügen, können Sie einfach [vordefinierte Variablen](variables-predefined.md) verwenden, um dem Header Kontaktinformationen für den Store hinzuzufügen.

### Schritt 1. Standardvorlage laden

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Klicken Sie auf **[!UICONTROL Add New Template]**.

1. Klicken Sie im Abschnitt **[!UICONTROL Load default template]** auf die **[!UICONTROL Template]** und wählen Sie `Magento_Email` > `Header`.

   ![Kopfzeile einer E-Mail-Vorlage - Standardvorlage laden](./assets/email-template-select-default-header.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Load Template]**.

   Der HTML-Code und die Variablen aus der Vorlage werden im Formular angezeigt.

### Schritt 2. Anpassen der Vorlage

1. Geben Sie die **[!UICONTROL Template Name]** für Ihre benutzerdefinierte Kopfzeile ein.

1. Geben Sie eine **[!UICONTROL Template Subject]** ein, um die Vorlagen zu organisieren.

   Im Raster kann die Liste der Vorlagen sortiert und nach der _[!UICONTROL Subject]_Spalte gefiltert werden.

   ![Kopfzeileninformationen der E-Mail-Vorlage](./assets/email-template-information.png){width="600" zoomable="yes"}

1. Ändern Sie im **[!UICONTROL Template Content]** die HTML nach Bedarf.

   >[!NOTE]
   >
   >Achten Sie beim Arbeiten im Vorlagen-Code darauf, keine Elemente zu überschreiben, die in doppelte Klammern eingeschlossen sind.

1. Um eine [Variable](variables-reference.md) einzufügen, positionieren Sie den Cursor in dem Code, in dem Sie die Variable platzieren möchten, und klicken Sie auf **[!UICONTROL Insert Variable]**.

1. Wählen Sie die Variable aus, die Sie einfügen möchten.

   ![Kopfzeilenvorlage - Variable einfügen](./assets/email-template-insert-variable.png){width="600" zoomable="yes"}

   Wenn eine Variable ausgewählt wird[ wird ein „Markup](markup-tags.md)Tag“ für die Variable in den Code eingefügt.

   Obwohl die Store-E-Mail-Adressvariablen die am häufigsten in der Kopfzeile enthaltenen Variablen sind, können Sie den Code für jedes System oder [benutzerdefinierte Variable](variables-custom.md) direkt in die Vorlage eingeben.

1. Wenn Sie CSS-Deklarationen vornehmen müssen, geben Sie die Stile in das **[!UICONTROL Template Styles]** ein.

1. Wenn Sie bereit sind, Ihre Arbeit zu überprüfen, klicken Sie auf **[!UICONTROL Preview Template]**.

   Nehmen Sie die erforderlichen Änderungen an der Vorlage vor.

1. Klicken Sie abschließend auf **[!UICONTROL Save Template]**.

   Ihre benutzerdefinierte Kopfzeile wird jetzt in der Liste der verfügbaren E-Mail-Vorlagen angezeigt.

### Schritt 3. Aktualisieren der Konfiguration

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie im Raster die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Scrollen Sie nach unten und erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Transactional Emails]** .

1. Wählen Sie die **[!UICONTROL Header Template]** aus, die als Standard für E-Mail-Benachrichtigungen verwendet werden soll.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

![Konfiguration des Transaktions-E-Mail-Designs - Kopfzeilenvorlage](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## Footer-Vorlage

Die Fußzeile der E-Mail-Vorlage enthält die schließende und die Signaturzeile der E-Mail-Nachricht. Sie können den Abschluss an Ihren Stil anpassen und zusätzliche Informationen hinzufügen, z. B. den Firmennamen und die Adresse unter Ihrem Namen.

### Schritt 1. Standardvorlage laden

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Klicken Sie auf **[!UICONTROL Add New Template]**.

1. Klicken Sie im Abschnitt **[!UICONTROL Load default template]** auf die **[!UICONTROL Template]** und wählen Sie `Magento_Email` > `Footer`.

1. Klicken Sie auf **[!UICONTROL Load Template]**.

   Der HTML-Code und die Variablen aus der Vorlage werden im Formular angezeigt.

### Schritt 2. Anpassen und Vorschau der Vorlage

1. Geben Sie die **[!UICONTROL Template Name]** für Ihre benutzerdefinierte Fußzeile ein.

1. Geben Sie eine **[!UICONTROL Template Subject]** ein, um die Vorlagen zu organisieren.

   Im Raster können die Vorlagen anhand der Spalte _[!UICONTROL Subject]_sortiert und gefiltert werden.

   ![Fußzeile der E-Mail-Vorlage - Informationen](./assets/email-template-footer-information.png){width="600" zoomable="yes"}

1. Ändern Sie im **[!UICONTROL Template Content]** die HTML nach Bedarf.

   >[!NOTE]
   >
   >Achten Sie beim Arbeiten im Vorlagen-Code darauf, keine Elemente zu überschreiben, die in doppelte Klammern eingeschlossen sind.

1. Um eine [Variable](variables-reference.md) einzufügen, positionieren Sie den Cursor in dem Code, in dem Sie die Variable platzieren möchten, und klicken Sie auf **[!UICONTROL Insert Variable]**.

1. Wählen Sie die Variable aus, die Sie einfügen möchten.

   Wenn eine Variable ausgewählt wird[ wird ein „Markup](markup-tags.md)Tag“ für die Variable in den Code eingefügt.

   Obwohl die Store-Kontaktvariablen die am häufigsten in der Fußzeile enthaltenen sind, können Sie den Code für jedes System oder [benutzerdefinierte Variable](variables-custom.md) direkt in die Vorlage eingeben.

1. Wenn Sie CSS-Deklarationen vornehmen müssen, geben Sie die Stile in das **[!UICONTROL Template Styles]** ein.

### Schritt 3. Aktualisieren der Konfiguration

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie im Raster die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Scrollen Sie nach unten und erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Transactional Emails]** .

1. Wählen Sie die **[!UICONTROL Footer Template]**, die in E-Mail-Benachrichtigungen als Standardfußzeile verwendet werden soll.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

![Konfiguration des Transaktions-E-Mail-Designs - Fußzeilenvorlage](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## Nachrichtenvorlagen

Der Prozess zum Anpassen des Textkörpers jeder Nachricht ist derselbe wie beim Anpassen der Kopf- oder Fußzeile. Der einzige Unterschied besteht in der Nachrichtenvorlage für jede Aktivität oder jedes Ereignis, die bzw. das eine Benachrichtigung Trigger. Sie können die Vorlagen so verwenden, wie sie sind, oder sie an Ihre Stimme und Marke anpassen. Zusätzlich zum Vorlagentext gibt es eine breite Auswahl an zulässigen [vordefinierten](variables-predefined.md) Variablen und [benutzerdefinierten](variables-custom.md) Variablen, die Sie erstellen und in die Vorlage integrieren können.

### Schritt 1. Standardvorlage laden

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Klicken Sie auf **[!UICONTROL Add New Template]**.

   ![E-Mail-Vorlagen - Standardvorlage laden](./assets/email-templates-message-load-default.png){width="600" zoomable="yes"}

1. Gehen Sie folgendermaßen vor:

   - Wählen Sie unter **[!UICONTROL Load default template]** die **[!UICONTROL Template]** aus, die Sie anpassen möchten.

   - Klicken Sie auf **[!UICONTROL Load Template]**.

### Schritt 2. Anpassen der Vorlage

1. Geben Sie **[!UICONTROL Template Name]** einen Namen für Ihre benutzerdefinierte Vorlage ein.

1. Ändern Sie bei Bedarf die **[!UICONTROL Template Subject]**.

   Dies ist die erste Zeile der Nachricht, die standardmäßig die Anrede ist. Sie können es unverändert lassen oder etwas Beschreibenderes eingeben.

1. Notieren Sie sich den **[!UICONTROL Currently Used For]** Pfad zur Vorlage. Dies ist der Pfad, der zum Aktualisieren der Konfiguration verwendet wird.

   ![E-Mail-Vorlagen - Vorlageninformationen](./assets/email-template-message-information.png){width="600" zoomable="yes"}

1. Ändern Sie im **[!UICONTROL Template Content]** die HTML nach Bedarf.

   Der Inhalt besteht aus einer Kombination aus HTML-Tags, CSS-Anweisungen, Variablen und Text.

   >[!NOTE]
   >
   >Achten Sie beim Arbeiten im Vorlagen-Code darauf, nicht versehentlich den Code einzugeben, der in doppelte Klammern eingeschlossen ist.

1. Um eine Variable einzufügen, positionieren Sie den Cursor in dem Code, in dem die Variable angezeigt werden soll.

   Die Variablenauswahl variiert je nach Vorlage und umfasst zulässige [vordefinierte](variables-predefined.md) und [benutzerdefinierte](variables-custom.md) Variablen, falls verfügbar.

1. Klicken Sie auf **[!UICONTROL Insert Variable]** und wählen Sie die Variable aus, die Sie einfügen möchten.

   Ein Befehl zum Einfügen der Variablen wird in geschweifte Klammern eingeschlossen und dem Code an der Cursorposition hinzugefügt. Beispiel:

   `customVar code=my_custom_variable`

1. Um CSS-Deklarationen vorzunehmen, geben Sie die Stile in **[!UICONTROL Template Styles]** ein.

   ![E-Mail-Vorlagen - Hinzufügen benutzerdefinierter Stile](./assets/email-template-add-custom-styles-min.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Benutzerdefinierte Stile werden nur dann auf die E-Mail angewendet, wenn `{{template config_path="design/email/header_template"}}` im _[!UICONTROL Template Styles]_vorhanden ist. Um benutzerdefiniertes CSS ohne Standard-Header-Vorlage zu verwenden, müssen Sie sie hier im `<style>` HTML-Tag angeben.

### Schritt 3. Aktualisieren der Konfiguration

Die _[!UICONTROL Currently Used For]_Breadcrumb-Spur zeigt an, wo die Vorlage verwendet wird. In diesem Beispiel befindet sich die Vorlagenkonfiguration auf der_[!UICONTROL Customer Configuration]_ Seite, im _[!UICONTROL Create New Account Options]_Abschnitt und im Feld_[!UICONTROL Default Welcome Email]_ .

- Seite - [!UICONTROL Customer Configuration]
- Abschnitt - [!UICONTROL Create New Account Options]
- Feld - [!UICONTROL Default Welcome Email]

1. Klicken Sie im **[!UICONTROL Currently Used For]**-Breadcrumb-Protokoll auf den Link, um die Seite Vorlagenkonfiguration zu öffnen.

   ![Aktuelle E-Mail-Vorlage](./assets/email-template-new-currently-used-for.png){width="600" zoomable="yes"}

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt und suchen Sie das Feld für die E-Mail-Vorlage, die Sie angepasst haben.

1. Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** und klicken Sie auf den Namen Ihrer benutzerdefinierten Vorlage.

   ![Kundenkonfiguration - Standard-Willkommens-E-Mail-Vorlage](./assets/email-template-message-configuration-default-template.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

1. Klicken Sie in der Meldung oben im Arbeitsbereich auf **[!UICONTROL Cache Management]** und löschen Sie alle ungültigen Cache-Einträge.

### Schritt 4. Vorschau anzeigen und Vorlage speichern

1. Wenn Sie bereit sind, Ihre Arbeit zu überprüfen, klicken Sie auf **[!UICONTROL Preview Template]**.

1. Aktualisieren Sie die Vorlage nach Bedarf.

1. Klicken Sie abschließend auf **[!UICONTROL Save Template]**.

   Ihre benutzerdefinierte Vorlage ist jetzt in der Liste der E-Mail-Vorlagen verfügbar.
