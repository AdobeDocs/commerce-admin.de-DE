---
title: Verwalten von Admin-Benutzerkonten
description: Erfahren Sie, wie Sie Admin-Benutzerkonten erstellen und Rollen zuweisen, um Berechtigungen für Admin-Funktionen zu erteilen.
exl-id: 65cca7a8-3d44-4c8c-a758-c0de03d53e11
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: ad75c77ada34c4d66b1a58a666edadd44d054e17
workflow-type: tm+mt
source-wordcount: '1012'
ht-degree: 0%

---

# Verwalten von Admin-Benutzerkonten

Bei der Erstinstallation Ihres Stores wird ein standardmäßiges Admin-Konto mit Anmeldedaten erstellt, über das Sie vollständigen Administratorzugriff erhalten. Als Best Practice sollten Sie ein weiteres Benutzerkonto mit vollem Administratorzugriff erstellen. Auf diese Weise können Sie ein Konto für Ihre alltäglichen administrativen Aktivitäten verwenden und das andere als „Superadmin“-Konto reservieren. Dies kann hilfreich sein, wenn Sie Ihre regulären Anmeldedaten vergessen haben oder diese irgendwie unbrauchbar werden.

Wenn andere Team-Mitglieder oder Dienstleister Zugriff benötigen, können Sie für sie individuelle Benutzerkonten erstellen und entsprechend ihren spezifischen Geschäftsanforderungen eingeschränkten Zugriff zuweisen. Um die Websites oder Geschäfte einzuschränken, auf die Benutzer im Admin zugreifen können, müssen Sie zunächst [eine Rolle erstellen](permissions-user-roles.md) mit begrenztem Umfang und nur den ausgewählten erforderlichen Ressourcen. Anschließend können Sie die Rolle einem bestimmten Benutzerkonto zuweisen. Admin-Benutzende, denen eine eingeschränkte Rolle zugewiesen ist, können Daten nur für Websites oder Stores sehen und ändern, die mit der Rolle verknüpft sind. Sie können jedoch keine globalen Einstellungen oder Daten ändern.

>[!NOTE]
>
>Adobe Commerce-Händler, die über eine Adobe ID verfügen und eine optimierte Anmeldung bei Adobe Commerce- und Adobe Business-Produkten wünschen, können die Commerce-Authentifizierung mit dem Adobe IMS-Authentifizierungs-Workflow integrieren. Nachdem diese Integration für Ihren Commerce Store aktiviert wurde, muss sich jeder Admin-Benutzer mit seinen Adobe-Anmeldeinformationen, nicht mit seinen Commerce-Anmeldeinformationen anmelden. Siehe Übersicht über die Integration von [Adobe Identity Management Service (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

Für temporäre Benutzer oder Rollen können Sie auch ein Ablaufdatum für das Benutzerkonto festlegen.

<!--  update this to a better info-graphic ![User types for your Admin](./assets/merchant-admin-users.png) -->

## Benutzer erstellen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add New User]**.

   Um einen vorhandenen Benutzer zu bearbeiten, klicken Sie auf einen Benutzernamen im Raster. Sie können die Abschnitte _[!UICONTROL User Info]_und_[!UICONTROL User Role]_ nach Bedarf ändern.

1. Gehen Sie im Abschnitt _[!UICONTROL Account Information]_wie folgt vor:

   ![Informationen zum Benutzerkonto](./assets/permissions-user-new.png){width="600" zoomable="yes"}

   - Geben Sie die **[!UICONTROL User Name]** für das Konto ein.

     Der Benutzername sollte leicht zu merken sein. Dabei wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn der Benutzername beispielsweise `John` ist, kann er sich auch als `john` anmelden.

   - Füllen Sie die folgenden Informationen aus:

      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**
      - **[!UICONTROL Email address]**

     Jedes Benutzerkonto muss über eine eindeutige E-Mail-Adresse verfügen.

   - Geben Sie einen **[!UICONTROL Password]** für das Konto ein.

     >[!NOTE]
     >
     >Ein Administratorkennwort muss mindestens sieben Zeichen lang sein und sowohl Buchstaben als auch Zahlen enthalten. Weitere Kennwortoptionen finden Sie unter [Konfigurieren der Admin Security](security-admin.md).

   - Geben Sie **[!UICONTROL Password Confirmation]** das Kennwort erneut ein, um sicherzustellen, dass es korrekt eingegeben wurde.

   - Wenn Ihr Store mehrere Sprachen hat, legen Sie **[!UICONTROL Interface Locale]** auf die Sprache fest, die für die Admin-Benutzeroberfläche verwendet werden soll.

1. Legen Sie **[!UICONTROL This Account is]** auf `Active` fest.

1. Klicken Sie auf das Kalendersymbol, um die **[!UICONTROL Expiration Date]** für das Benutzerkonto festzulegen.

   Das Definieren eines Ablaufdatums ist hilfreich, wenn ein Benutzer oder eine Rolle temporär ist. Nach dem Ablaufdatum ändert sich der Benutzerkontenstatus in `Inactive` und kann bei Bedarf aktualisiert werden.

1. Geben Sie unter _[!UICONTROL Current User Identity Verification]_Ihr Benutzerkonto-Kennwort ein.

>[!IMPORTANT]
>
>Wenn der Abschnitt _[!UICONTROL Account Information]_abgeschlossen ist, können Sie den Benutzer speichern. Der neue Benutzer wird im_[!UICONTROL Users]_ angezeigt, der Benutzername kann sich jedoch erst anmelden, wenn ihm eine Rolle zugewiesen wurde.

## Benutzerrolle zuweisen

1. Klicken Sie im linken Bedienfeld auf **[!UICONTROL User Role]**.

   Das Raster listet alle vorhandenen Benutzerrollen auf. Für einen neuen Store ist _[!UICONTROL Administrators]_die einzige verfügbare Rolle.

   ![Admin - Add new user role](./assets/permissions-user-roles.png){width="600" zoomable="yes"}

1. Wählen Sie in der Spalte _[!UICONTROL Assigned]_eine Benutzerrolle aus.

   Sie können [vorhandene Benutzerrollen anzeigen oder zusätzliche Benutzerrollen definieren](permissions-user-roles.md). Nachdem eine Rolle definiert wurde, müssen Sie das Benutzerkonto bearbeiten, um die neue Rolle zuzuweisen.

## Überprüfen oder Zurücksetzen von 2FA-Anbietern

1. Öffnen Sie das Admin-Benutzerkonto.

1. Klicken Sie im linken Bedienfeld auf **[!UICONTROL 2FA]**.

   ![Admin - Add new user role](./assets/permissions-user-2fa.png){width="600" zoomable="yes"}

1. Überprüfen Sie die 2FA-Lösungen, die _Admin_-Benutzern zur Verfügung stehen, und empfehlen Sie jedem Benutzer, die Lösungen zu installieren, die er verwenden möchte, bevor er sich anmeldet.

   Die Authentifizierung mit nur einer 2FA-Lösung ist erforderlich, um sich beim _Administrator_ anzumelden.

1. Wenn der Benutzer die 2FA-Lösung neu installieren muss, können Sie die aktuelle 2FA-Konfiguration zurücksetzen.

   Dazu muss der Benutzer den Einrichtungsprozess wiederholen, bevor er sich erneut anmelden kann. Beispielsweise könnte der/die Benutzende über ein neues Smartphone verfügen und muss Google Authenticator neu installieren. Um die aktuelle 2FA-Einrichtung des Benutzers zu löschen, klicken Sie für jede Lösung, die Sie löschen möchten, auf **[!UICONTROL Reset (Provider)]**. Wenn Sie dazu aufgefordert werden, klicken Sie zur Bestätigung auf **[!UICONTROL OK]** .

   Der Benutzer erhält eine E-Mail mit einem Link zu [Konfigurieren von 2FA](security-two-factor-authentication.md). Der Link kann nur einmal verwendet werden. Wenn Benutzende mehrmals versuchen, sich anzumelden, wird nach jedem Versuch ein neuer Link gesendet.

1. Klicken Sie auf **[!UICONTROL Save User]**.

1. Geben Sie bei Aufforderung Ihr Kennwort ein, um Ihre Identität zu bestätigen, und klicken Sie erneut auf **[!UICONTROL Save User]**.

   Das _[!UICONTROL Users]_Raster öffnet und listet alle Benutzer auf.

## Admin-Benutzer löschen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Suchen Sie das Benutzerkonto mithilfe von Filtern über dem Raster und klicken Sie auf den Benutzernamen.

1. Geben Sie bei Aufforderung Ihr Kennwort ein, um Ihre Identität zu bestätigen.

1. Klicken Sie oben rechts auf **[!UICONTROL Delete User]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

## E-Mails zu vergessenem Kennwort und Zurücksetzen

Die Konfiguration der Admin-E-Mail-Vorlage bestimmt, welche E-Mails gesendet werden, wenn Benutzer ihre Passwörter vergessen und zurücksetzen. Diese Konfiguration gibt den Speicherkontakt an, der als Absender der Nachricht angezeigt wird, und wie lange der Link zur Passwortwiederherstellung gültig bleibt.

**_So konfigurieren Sie die Admin-E-Mail-Vorlagen:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Setting]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Seitenbereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL Admin]**.

1. Erweitern Sie ![Erweiterungs-Umschalter](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Admin User Emails]** .

   ![Erweiterte Konfiguration - Admin-E-Mail-Vorlageneinstellungen](../configuration-reference/advanced/assets/admin-admin-user-emails.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Forgot Password Email Template]** auf die Vorlage fest, die gesendet wird, wenn ein Administrator bzw. eine Administratorin seine bzw. ihre Passwörter vergisst.

1. Legen Sie **[!UICONTROL Forgot and Reset Email Sender]** auf den Store-Kontakt fest, der als Absender der Nachricht angezeigt wird.

1. Legen Sie **[!UICONTROL User Notification Template]** auf die E-Mail-Vorlage fest, die als Standard für Admin-Benachrichtigungen verwendet wird.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Gesperrte Benutzer

Aus Sicherheitsgründen werden Benutzerkonten standardmäßig nach sechs fehlgeschlagenen Versuchen gesperrt, sich beim Administrator [anzumelden](../getting-started/admin-signin.md). Jedes Benutzerkonto, das derzeit gesperrt ist, wird im Raster Gesperrte Benutzer angezeigt. Ein Konto kann von jedem anderen Benutzer mit vollständigen Administratorberechtigungen entsperrt werden.

Weitere Maßnahmen zur Passwortsicherheit können in der Konfiguration [Erweiterter Admin](../configuration-reference/advanced/admin.md#security) implementiert werden. Siehe [Admin-](security-admin.md).

![Warnhinweis im Anmeldebildschirm - Konto ist vorübergehend deaktiviert](./assets/admin-login-locked-out-message.png){width="300"}

**_So entsperren Sie ein Administratorkonto:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL Locked Users]**.

1. Aktivieren Sie im Raster das Kontrollkästchen des gesperrten Kontos.

   ![Berechtigungen - Gesperrte Benutzerkonten](./assets/permissions-locked-users-grid.png){width="600" zoomable="yes"}

1. Setzen Sie in der oberen linken Ecke **[!UICONTROL Actions]** auf `Unlock`.

1. Klicken Sie auf **[!UICONTROL Submit]** , um das Konto zu entsperren.
