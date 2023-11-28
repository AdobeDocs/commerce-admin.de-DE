---
title: Ereigniseinladungen
description: Erfahren Sie, wie Kunden Einladungen zu Ereignissen und zum privaten Vertrieb über das Dashboard ihrer Kundenkonten senden und anzeigen können.
exl-id: 6a9123a0-bdb4-4cd6-99cd-658f728aa90c
feature: Promotions/Events, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Ereigniseinladungen

{{ee-feature}}

Wenn Einladungen aktiviert sind, können Kunden Einladungen über das Dashboard ihrer Kundenkonten senden und anzeigen. Die Einladungs-E-Mail enthält einen Link zur Kundenanmeldeseite Ihres Stores.

## Meine Einladungen

Die _[!UICONTROL My Invitations]_im Kundenkonto werden alle vom Kunden gesendeten Einladungen aufgelistet. Kunden können Einladungen an Freunde und Familie zu Geschenkveranstaltungen, Geschenkregistern, Wunschlisten usw. senden.

![Meine Einladungen](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### Einladungs-Workflow

1. **Der Kunde bereitet Einladungen vor**: Im Konto-Dashboard bereitet der Kunde die Empfängerliste vor und schließt die Einladung ab. Je nach Konfiguration kann eine benutzerdefinierte Nachricht eingefügt werden.
1. **Der Kunde sendet Einladungen**: Wenn der Kunde bereit ist, klickt er auf die _[!UICONTROL Send Invitations]_Schaltfläche.
1. **System verwaltet Übertragung**: Das System sendet Einladungen in Stapeln entsprechend der in der Konfiguration festgelegten Nummer.
1. **Reaktion des Kunden**: Der Kunde überwacht den Status jeder Einladung im Konto-Dashboard wie folgt: `Sent`, `Accepted`oder `Canceled`.

### Einladung senden

1. In der Seitenleiste seines Kontos im Storefront wählt der Kunde **[!UICONTROL My Invitations]**.

1. Im _Meine Einladung_ Seite, Klicks **[!UICONTROL Send Invitation]**.

1. Definiert das neue Einladungselement:

   - Fügt die E-Mail-Informationen ein.

   - (Optional) Erstellt eine Einladung mit mehreren Adressen durch Klicken auf **+** und eine weitere E-Mail-Adresse hinzufügen.

     Eine Einladung hat eine Grenze von fünf E-Mail-Adressen.

   - (Optional) Fügt eine Begleitnachricht ein.

1. Klicken Sie nach Abschluss **[!UICONTROL Send Invitation]**.

Eine Einladungs-Benachrichtigung wird an die E-Mail-Adresse des eingeladenen Benutzers mit einem Link mit Anweisungen zum Festlegen des Kontos gesendet.

>[!NOTE]
>
>Ein Benutzer kann nur eine Einladung an eine bestimmte E-Mail-Adresse senden. Wenn Sie versuchen, eine Einladung an dieselbe E-Mail-Adresse erneut zu senden, wird eine Fehlermeldung angezeigt und die Einladung wird nicht gesendet.

## Einladungen für Ihren Store aktivieren

Die Einladungskonfiguration ermöglicht Einladungen für den Store und bestimmt, wie sie gesendet werden.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen **[!UICONTROL Invitations]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL General]** Abschnitt.

   ![Kundenkonfiguration - Allgemeine Optionen für Einladungen](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Enable Invitations Functionality]** nach `Yes`.

1. Damit Kunden Einladungen von der Storefront aus verwalten können, legen Sie **Einladungen in Storefront aktivieren** nach `Yes`.

1. Satz **[!UICONTROL Referred Customer Group]** auf einen der folgenden Werte zu:

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. Satz **[!UICONTROL New Accounts Registration]** auf einen der folgenden Werte zu:

   - `By Invitation Only`
   - `Available to All`

1. nach **[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]** auswählen `Yes`.

1. Um die Anzahl der Einladungen zu begrenzen, die gleichzeitig gesendet werden können, geben Sie die Zahl in das Feld **[!UICONTROL Max Invitations Allowed to be Sent at One Time]** -Feld.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Email]** und führen Sie folgende Schritte aus:

   ![Kundenkonfiguration - E-Mail-Optionen für Einladungen](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - Wählen Sie die Store-Identität aus, die als **[!UICONTROL Customer Invitation Email Sender]**.

   - Wählen Sie die **[!UICONTROL Customer Invitation Email Template]** verwendet für gesendete Einladungen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Einladungen in den Admin senden und verwalten

Im [Berichte zu privaten Verkäufen](../getting-started/private-sales-reports.md) angezeigt, können Sie die Anzahl der Einladungen sehen, die während eines bestimmten Zeitraums gesendet wurden, oder die Kunden, an die Sie Einladungen gesendet haben.

### Einladung in Admin erstellen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Invitations]**.

1. Geben Sie im nächsten Bildschirm E-Mail-Adressen ein, um neue Kunden einzuladen, fügen Sie eine benutzerdefinierte Nachricht hinzu, wählen Sie einen Absender aus und wählen Sie eine eingeladene Gruppe aus.

   Wenn Sie mehrere Store-Ansichten haben, verwenden Sie die **[!UICONTROL Send From]** -Option, um die Store-Ansicht anzugeben, von der aus eine Einladung gesendet wird.

   ![Einladungsinformationen](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

### Einladungen für einzelne Entitäten verwerfen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Suchen Sie die gewünschte Einladung mithilfe von Filtern und öffnen Sie sie im Bearbeitungsmodus.

1. Klicken Sie oben rechts auf **[!UICONTROL Discard Invitation]**.

1. Klicken Sie zur Bestätigung der Aktion auf **[!UICONTROL OK]**.

### Einladungen für mehrere Entitäten verwerfen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Suchen Sie nach den Einladungen, die verworfen werden sollen, und wählen Sie sie aus.

1. Verwenden Sie oben links den **[!UICONTROL Actions]** Menü auswählen **[!UICONTROL Discard Selected]** und klicken **[!UICONTROL Submit]**.

1. Klicken Sie zur Bestätigung der Aktion auf **[!UICONTROL OK]**.

### Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Select] | Aktivieren Sie das Kontrollkästchen, um die Einladungen auszuwählen, die einer Aktion unterzogen werden sollen, oder verwenden Sie das Auswahlsteuerelement in der Spaltenüberschrift. Optionen: `Select All` /` Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL ID] | Die interne ID einer Einladung |
| [!UICONTROL Email] | Eine entsprechende Kunden-E-Mail-Adresse |
| [!UICONTROL Invitee] | E-Mail für eingeladene Benutzer |
| [!UICONTROL Sent] | Uhrzeit und Datum des Versands einer Einladung |
| [!UICONTROL Registered] | Zeitpunkt und Daten der Registrierung eines Kunden |
| [!UICONTROL Status] | Einladungsstatus. Optionen: `Sent` / `Not Sent` / `Accepted` / `Discarded` |
| [!UICONTROL Valid Website] | Die entsprechende Website |
| [!UICONTROL Invitee Group] | Eine Kundengruppe einer Einladung |

{style="table-layout:auto"}
