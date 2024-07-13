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

Im Abschnitt _[!UICONTROL My Invitations]_des Kundenkontos werden alle vom Kunden gesendeten Einladungen aufgelistet. Kunden können Einladungen an Freunde und Familie zu Geschenkveranstaltungen, Geschenkregistern, Wunschlisten usw. senden.

![Meine Einladungen](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### Einladungs-Workflow

1. **Kunde bereitet Einladungen vor**: Im Konto-Dashboard bereitet der Kunde die Empfängerliste vor und schließt die Einladung ab. Je nach Konfiguration kann eine benutzerdefinierte Nachricht eingefügt werden.
1. **Kunde sendet Einladungen**: Wenn diese bereit sind, klickt der Kunde auf die Schaltfläche _[!UICONTROL Send Invitations]_.
1. **System verwaltet die Übertragung**: Das System sendet Einladungen in Stapeln entsprechend der in der Konfiguration festgelegten Zahl.
1. **Kunde überwacht Antwort**: Der Kunde überwacht den Status jeder Einladung aus dem Konto-Dashboard als `Sent`, `Accepted` oder `Canceled`.

### Einladung senden

1. In der Seitenleiste ihres Kontos auf der Storefront wählt der Kunde **[!UICONTROL My Invitations]** aus.

1. Klicken Sie auf der Seite _Meine Einladung_ auf **[!UICONTROL Send Invitation]**.

1. Definiert das neue Einladungselement:

   - Fügt die E-Mail-Informationen ein.

   - (Optional) Erstellt eine Einladung mit mehreren Adressen, indem Sie auf **+** klicken und eine weitere E-Mail-Adresse hinzufügen.

     Eine Einladung hat eine Grenze von fünf E-Mail-Adressen.

   - (Optional) Fügt eine Begleitnachricht ein.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Send Invitation]**.

Eine Einladungs-Benachrichtigung wird an die E-Mail-Adresse des eingeladenen Benutzers mit einem Link mit Anweisungen zum Festlegen des Kontos gesendet.

>[!NOTE]
>
>Ein Benutzer kann nur eine Einladung an eine bestimmte E-Mail-Adresse senden. Wenn Sie versuchen, eine Einladung an dieselbe E-Mail-Adresse erneut zu senden, wird eine Fehlermeldung angezeigt und die Einladung wird nicht gesendet.

## Einladungen für Ihren Store aktivieren

Die Einladungskonfiguration ermöglicht Einladungen für den Store und bestimmt, wie sie gesendet werden.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Invitations]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL General]** .

   ![Kundenkonfiguration - Allgemeine Optionen für Einladungen](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Enable Invitations Functionality]** auf `Yes`.

1. Damit Kunden Einladungen von der Storefront aus verwalten können, setzen Sie **Einladungen in die Storefront aktivieren** auf `Yes`.

1. Setzen Sie **[!UICONTROL Referred Customer Group]** auf einen der folgenden Werte:

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. Setzen Sie **[!UICONTROL New Accounts Registration]** auf einen der folgenden Werte:

   - `By Invitation Only`
   - `Available to All`

1. Wählen Sie &quot;**[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]**&quot;aus.`Yes`

1. Um die Anzahl der Einladungen zu begrenzen, die gleichzeitig gesendet werden können, geben Sie die Zahl in das Feld **[!UICONTROL Max Invitations Allowed to be Sent at One Time]** ein.

1. Erweitern Sie den Abschnitt **[!UICONTROL Email]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   ![Kundenkonfiguration - E-Mail-Optionen für Einladungen](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - Wählen Sie die Store-Identität aus, die als **[!UICONTROL Customer Invitation Email Sender]** verwendet werden soll.

   - Wählen Sie den für gesendete Einladungen verwendeten Wert **[!UICONTROL Customer Invitation Email Template]** aus.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Einladungen in den Admin senden und verwalten

Im Abschnitt [Private Verkaufsberichte](../getting-started/private-sales-reports.md) können Sie die Anzahl der Einladungen sehen, die während eines bestimmten Zeitraums gesendet wurden, oder Kunden, an die Sie Einladungen gesendet haben.

### Einladung in Admin erstellen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add Invitations]**.

1. Geben Sie im nächsten Bildschirm E-Mail-Adressen ein, um neue Kunden einzuladen, fügen Sie eine benutzerdefinierte Nachricht hinzu, wählen Sie einen Absender aus und wählen Sie eine eingeladene Gruppe aus.

   Wenn Sie mehrere Store-Ansichten haben, verwenden Sie die Option **[!UICONTROL Send From]** , um die Store-Ansicht anzugeben, von der aus eine Einladung gesendet wird.

   ![Einladungsinformationen](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

### Einladungen für einzelne Entitäten verwerfen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Suchen Sie die gewünschte Einladung mithilfe von Filtern und öffnen Sie sie im Bearbeitungsmodus.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Discard Invitation]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

### Einladungen für mehrere Entitäten verwerfen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Suchen Sie nach den Einladungen, die verworfen werden sollen, und wählen Sie sie aus.

1. Verwenden Sie oben links das Menü **[!UICONTROL Actions]** , um **[!UICONTROL Discard Selected]** auszuwählen, und klicken Sie auf **[!UICONTROL Submit]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

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
