---
title: E-Mail-Vorlagen anpassen
description: Erfahren Sie, wie Sie E-Mail-Vorlagen für jede Website-, Store- oder Store-Ansicht anpassen können.
exl-id: d328b84d-fab7-4956-9071-2d8848f7c21e
feature: Communications, Configuration
source-git-commit: c0d6523f820558c8cd6cfa6b745568784b9e784c
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 0%

---

# E-Mail-Vorlagen anpassen

Commerce enthält eine Standard-E-Mail-Vorlage für den Hauptteil jeder vom System gesendeten Nachricht. Die Vorlage für den Textinhalt wird mit der Kopf- und Fußzeilenvorlage kombiniert, um die gesamte Nachricht zu erstellen. Der Inhalt ist mit HTML und CSS formatiert und kann einfach bearbeitet und angepasst werden, indem [Variablen](variables-predefined.md) hinzugefügt werden. E-Mail-Vorlagen können für jede Website-, Store- oder Store-Ansicht angepasst werden. Achten Sie bei Verwendung benutzerdefinierter Vorlagen darauf, die [Systemkonfiguration](email-templates.md#configure-email-templates) zu aktualisieren, um sicherzustellen, dass die richtige Vorlage verwendet wird. Informationen dazu, wie Sie bedingte Anweisungen beim Anpassen der E-Mail-Vorlage verwenden können, finden Sie in der [Entwicklerdokumentation](https://developer.adobe.com/commerce/frontend-core/guide/templates/email/#theme-based-customizations-1) .

![Beispiel - Begrüßungs-E-Mail-Vorschau](./assets/email-template-preview.png){width="500" zoomable="yes"}

Die Standardvorlagen enthalten Ihr Logo und Ihre Store-Informationen und können ohne weitere Anpassung verwendet werden. Als Best Practice sollten Sie jedoch jede Vorlage anzeigen und alle erforderlichen Änderungen vornehmen, bevor Sie sie an Kunden senden.

- [Kopfzeilenvorlage](email-template-custom.md#header-template)
- [Fußzeilenvorlage](email-template-custom.md#footer-template)
- [Nachrichtenvorlagen](email-template-custom.md#message-templates)

![E-Mail-Vorlagen](./assets/email-templates.png){width="700" zoomable="yes"}

## Vorlageninformationen

| Feld | Beschreibung |
| ----- | ----------- |
| [!UICONTROL Template Name] | Der Name Ihrer benutzerdefinierten Vorlage. |
| [!UICONTROL Insert Variable] | Fügt eine Variable an der Cursorposition in die Vorlage ein. |
| [!UICONTROL Template Subject] | Der Vorlagenbetreff wird in der Spalte Betreff angezeigt und kann zum Sortieren und Filtern der Vorlagen in der Liste verwendet werden. |
| [!UICONTROL Template Content] | Der Inhalt der Vorlage in HTML. |
| [!UICONTROL Template Styles] | Alle CSS-Stildeklarationen, die zum Formatieren der Vorlage erforderlich sind, können in das Feld _[!UICONTROL Template Styles]_eingegeben werden. |

{style="table-layout:auto"}

## Kopfzeilenvorlage

Nach Abschluss der [Konfiguration](email-templates.md#configure-email-templates) enthält die E-Mail-Kopfzeilenvorlage Ihr Logo, das mit Ihrem Store verknüpft ist. Wenn Sie über Grundkenntnisse im HTML verfügen, können Sie einfach [vordefinierte Variablen](variables-predefined.md) verwenden, um Store-Kontaktdaten zum Header hinzuzufügen.

### Schritt 1. Laden der Standardvorlage

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Klicken Sie auf **[!UICONTROL Add New Template]**.

1. Klicken Sie im Abschnitt **[!UICONTROL Load default template]** auf den Selektor **[!UICONTROL Template]** und wählen Sie `Magento_Email` > `Header`.

   ![E-Mail-Vorlagenkopfzeile - Laden der Standardvorlage](./assets/email-template-select-default-header.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Load Template]**.

   Der HTML-Code und die Variablen aus der Vorlage werden im Formular angezeigt.

### Schritt 2. Vorlage anpassen

1. Geben Sie den **[!UICONTROL Template Name]** für Ihre benutzerdefinierte Kopfzeile ein.

1. Geben Sie einen **[!UICONTROL Template Subject]** ein, um die Vorlagen zu organisieren.

   Im Raster kann die Liste der Vorlagen nach der Spalte _[!UICONTROL Subject]_sortiert und gefiltert werden.

   ![Kopfzeileninformationen der E-Mail-Vorlage](./assets/email-template-information.png){width="600" zoomable="yes"}

1. Ändern Sie im Feld **[!UICONTROL Template Content]** die HTML nach Bedarf.

   >[!NOTE]
   >
   >Achten Sie bei der Arbeit mit dem Vorlagencode darauf, keine doppelten Klammern zu überschreiben.

1. Um eine [Variable](variables-reference.md) einzufügen, positionieren Sie den Cursor an der Stelle im Code, an der die Variable platziert werden soll, und klicken Sie auf **[!UICONTROL Insert Variable]**.

1. Wählen Sie die einzufügende Variable aus.

   ![Kopfzeilenvorlage - Variable einfügen](./assets/email-template-insert-variable.png){width="600" zoomable="yes"}

   Wenn eine Variable ausgewählt ist, wird ein [Markup-Tag](markup-tags.md) für die Variable in den Code eingefügt.

   Auch wenn die Variablen &quot;E-Mail-Adresse speichern&quot;am häufigsten in der Kopfzeile enthalten sind, können Sie den Code für jedes System oder jede [benutzerdefinierte Variable](variables-custom.md) direkt in die Vorlage eingeben.

1. Wenn Sie CSS-Deklarationen vornehmen müssen, geben Sie die Stile in das Feld **[!UICONTROL Template Styles]** ein.

1. Wenn Sie bereit sind, Ihre Arbeit zu überprüfen, klicken Sie auf **[!UICONTROL Preview Template]**.

   Nehmen Sie die erforderlichen Änderungen an der Vorlage vor.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Template]**.

   Ihr benutzerdefinierter Header wird nun in der Liste der verfügbaren E-Mail-Vorlagen angezeigt.

### Schritt 3. Konfiguration aktualisieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie im Raster die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Transactional Emails]** um den ![Erweiterungsselektor](../assets/icon-display-expand.png).

1. Wählen Sie den für E-Mail-Benachrichtigungen standardmäßig verwendeten Wert **[!UICONTROL Header Template]** aus.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

![Konfiguration des E-Mail-Entwurfs für Transaktionen - Kopfzeilenvorlage](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## Fußzeilenvorlage

Die Fußzeile der E-Mail-Vorlage enthält die schließende Zeile und die Unterschriftszeile der E-Mail-Nachricht. Sie können das Schließen an Ihren Stil anpassen und zusätzliche Informationen hinzufügen, wie z. B. den Firmennamen und die Adresse unter Ihrem Namen.

### Schritt 1. Laden der Standardvorlage

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Klicken Sie auf **[!UICONTROL Add New Template]**.

1. Klicken Sie im Abschnitt **[!UICONTROL Load default template]** auf den Selektor **[!UICONTROL Template]** und wählen Sie `Magento_Email` > `Footer`.

1. Klicken Sie auf **[!UICONTROL Load Template]**.

   Der HTML-Code und die Variablen aus der Vorlage werden im Formular angezeigt.

### Schritt 2. Vorlage anpassen und in der Vorschau anzeigen

1. Geben Sie die **[!UICONTROL Template Name]** für Ihre benutzerdefinierte Fußzeile ein.

1. Geben Sie einen **[!UICONTROL Template Subject]** ein, um die Vorlagen zu organisieren.

   Im Raster können die Vorlagen nach der Spalte _[!UICONTROL Subject]_sortiert und gefiltert werden.

   ![Fußzeile der E-Mail-Vorlage - Informationen](./assets/email-template-footer-information.png){width="600" zoomable="yes"}

1. Ändern Sie im Feld **[!UICONTROL Template Content]** die HTML nach Bedarf.

   >[!NOTE]
   >
   >Achten Sie bei der Arbeit mit dem Vorlagencode darauf, keine doppelten Klammern zu überschreiben.

1. Um eine [Variable](variables-reference.md) einzufügen, positionieren Sie den Cursor an der Stelle im Code, an der die Variable platziert werden soll, und klicken Sie auf **[!UICONTROL Insert Variable]**.

1. Wählen Sie die einzufügende Variable aus.

   Wenn eine Variable ausgewählt ist, wird ein [Markup-Tag](markup-tags.md) für die Variable in den Code eingefügt.

   Obwohl die Variablen &quot;Store Contact&quot;am häufigsten in der Fußzeile enthalten sind, können Sie den Code für jedes System oder jede [benutzerdefinierte Variable](variables-custom.md) direkt in die Vorlage eingeben.

1. Wenn Sie CSS-Deklarationen vornehmen müssen, geben Sie die Stile in das Feld **[!UICONTROL Template Styles]** ein.

### Schritt 3. Konfiguration aktualisieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie im Raster die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Transactional Emails]** um den ![Erweiterungsselektor](../assets/icon-display-expand.png).

1. Wählen Sie die **[!UICONTROL Footer Template]** aus, die in E-Mail-Benachrichtigungen als Standardfußzeile verwendet wird.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

![Konfiguration des E-Mail-Entwurfs für Transaktionen - Fußzeilenvorlage](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## Nachrichtenvorlagen

Der Prozess der Anpassung des Hauptteils jeder Nachricht entspricht dem der Kopf- oder Fußzeile. Der einzige Unterschied besteht in der Nachrichtenvorlage für jede Aktivität oder jedes Ereignis, bei der eine Benachrichtigung Trigger wird. Sie können die Vorlagen unverändert verwenden oder sie an Ihre Stimme und Marke anpassen. Neben dem Vorlagentext gibt es eine große Auswahl an zulässigen [vordefinierten](variables-predefined.md) Variablen und [benutzerdefinierten](variables-custom.md) Variablen, die Sie erstellen und in die Vorlage integrieren können.

### Schritt 1. Laden der Standardvorlage

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Klicken Sie auf **[!UICONTROL Add New Template]**.

   ![E-Mail-Vorlagen - Laden der Standardvorlage](./assets/email-templates-message-load-default.png){width="600" zoomable="yes"}

1. Gehen Sie wie folgt vor:

   - Wählen Sie unter **[!UICONTROL Load default template]** die **[!UICONTROL Template]** aus, die Sie anpassen möchten.

   - Klicken Sie auf **[!UICONTROL Load Template]**.

### Schritt 2. Vorlage anpassen

1. Geben Sie für &quot;**[!UICONTROL Template Name]**&quot;einen Namen für Ihre benutzerdefinierte Vorlage ein.

1. Ändern Sie bei Bedarf die **[!UICONTROL Template Subject]**.

   Dies ist die erste Zeile der Nachricht, die standardmäßig als Anrede bezeichnet wird. Sie können es wie besehen lassen oder eine aussagekräftigere Eingabe vornehmen.

1. Notieren Sie sich den Pfad **[!UICONTROL Currently Used For]** zur Vorlage, der zum Aktualisieren der Konfiguration verwendet wird.

   ![E-Mail-Vorlagen - Vorlageninformationen](./assets/email-template-message-information.png){width="600" zoomable="yes"}

1. Ändern Sie im Feld **[!UICONTROL Template Content]** die HTML nach Bedarf.

   Der Inhalt besteht aus einer Kombination aus HTML-Tags, CSS-Anweisungen, Variablen und Text.

   >[!NOTE]
   >
   >Achten Sie bei der Arbeit mit dem Vorlagencode darauf, nicht versehentlich den Code einzugeben, der in doppelte Klammern eingeschlossen ist.

1. Um eine Variable einzufügen, positionieren Sie den Cursor im Code an der Stelle, an der die Variable angezeigt werden soll.

   Die Variablenauswahl variiert je nach Vorlage und umfasst die zulässigen [vordefinierten](variables-predefined.md) und [benutzerdefinierten](variables-custom.md) Variablen, sofern verfügbar.

1. Klicken Sie auf **[!UICONTROL Insert Variable]** und wählen Sie die Variable aus, die Sie einfügen möchten.

   Ein Befehl zum Einfügen der Variablen ist in geschweifte Klammern eingeschlossen und dem Code an der Cursorposition hinzugefügt. Beispiel:

   `customVar code=my_custom_variable`

1. Um CSS-Deklarationen vorzunehmen, geben Sie die Stile in **[!UICONTROL Template Styles]** ein.

   ![E-Mail-Vorlagen - benutzerdefinierte Stile hinzufügen](./assets/email-template-add-custom-styles-min.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Benutzerdefinierte Stile werden nur dann auf die E-Mail angewendet, wenn `{{template config_path="design/email/header_template"}}` im _[!UICONTROL Template Styles]_vorhanden ist. Um benutzerdefiniertes CSS ohne standardmäßige Kopfzeilenvorlage zu verwenden, müssen Sie diese hier im HTML-Tag `<style>` angeben.

### Schritt 3. Konfiguration aktualisieren

Die Breadcrumb-Leiste _[!UICONTROL Currently Used For]_zeigt an, wo die Vorlage verwendet wird. In diesem Beispiel befindet sich die Vorlagenkonfiguration auf der Seite &quot;_[!UICONTROL Customer Configuration]_&quot;, im Abschnitt &quot;_[!UICONTROL Create New Account Options]_&quot; und im Feld &quot;_[!UICONTROL Default Welcome Email]_&quot;.

- Seite - [!UICONTROL Customer Configuration]
- Abschnitt - [!UICONTROL Create New Account Options]
- Feld - [!UICONTROL Default Welcome Email]

1. Klicken Sie im Breadcrumb-Pfad **[!UICONTROL Currently Used For]** auf den Link, um die Seite mit der Vorlagenkonfiguration zu öffnen.

   ![Aktuelle E-Mail-Vorlage](./assets/email-template-new-currently-used-for.png){width="600" zoomable="yes"}

1. Erweitern Sie den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) und suchen Sie das Feld für die von Ihnen angepasste E-Mail-Vorlage.

1. Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** und klicken Sie auf den Namen Ihrer benutzerdefinierten Vorlage.

   ![Kundenkonfiguration - standardmäßige Begrüßungs-E-Mail-Vorlage](./assets/email-template-message-configuration-default-template.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

1. Klicken Sie in der Meldung oben im Arbeitsbereich auf **[!UICONTROL Cache Management]** und löschen Sie den ungültigen Cache.

### Schritt 4. Vorschau erstellen und speichern

1. Wenn Sie bereit sind, Ihre Arbeit zu überprüfen, klicken Sie auf **[!UICONTROL Preview Template]**.

1. Aktualisieren Sie die Vorlage nach Bedarf.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Template]**.

   Ihre benutzerdefinierte Vorlage ist jetzt in der Liste der E-Mail-Vorlagen verfügbar.
