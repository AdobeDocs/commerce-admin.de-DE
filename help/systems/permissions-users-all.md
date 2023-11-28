---
title: Verwalten von Admin-Benutzerkonten
description: Erfahren Sie, wie Sie Admin-Benutzerkonten erstellen und Rollen zuweisen, um Administratorfunktionen Berechtigungen zu erteilen.
exl-id: 65cca7a8-3d44-4c8c-a758-c0de03d53e11
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Verwalten von Admin-Benutzerkonten

Wenn Ihr Store zum ersten Mal installiert wird, wird ein standardmäßiges Admin-Konto mit Anmeldedaten erstellt, über das Sie vollen Administratorzugriff erhalten. Als Best Practice sollten Sie ein weiteres Benutzerkonto mit vollem Administratorzugriff erstellen. Auf diese Weise können Sie ein Konto für Ihre alltäglichen Verwaltungsaktivitäten verwenden und das andere als &quot;Super Admin&quot;-Konto reservieren. Dies kann hilfreich sein, wenn Sie Ihre regulären Anmeldedaten vergessen haben oder sie irgendwie unbrauchbar werden.

Wenn andere Mitarbeiter in Ihrem Team oder bei Service Providern Zugriff benötigen, können Sie für jede Gruppe ein eigenes Benutzerkonto erstellen und eingeschränkten Zugriff je nach geschäftlichen Anforderungen zuweisen. Um die Websites oder Stores zu beschränken, auf die Benutzer im Admin zugreifen können, müssen Sie zunächst [Rolle erstellen](permissions-user-roles.md) mit begrenztem Umfang und nur ausgewählten Ressourcen. Anschließend können Sie die Rolle einem bestimmten Benutzerkonto zuweisen. Admin-Benutzer, die einer eingeschränkten Rolle zugewiesen sind, können Daten nur für Websites oder Stores anzeigen und ändern, die mit der Rolle verknüpft sind. Sie können jedoch keine globalen Einstellungen oder Daten ändern.

>[!NOTE]
>
>Adobe Commerce-Händler, die über eine Adobe ID verfügen und sich bei Adobe Commerce anmelden möchten, und Adobe Business-Produkte können die Commerce-Authentifizierung mit dem Adobe IMS-Authentifizierungsarbeitsablauf integrieren. Nachdem diese Integration für Ihren Commerce-Store aktiviert wurde, muss sich jeder Admin-Benutzer mit seinen Adobe-Anmeldeinformationen (nicht mit seinen Commerce-Anmeldeinformationen) anmelden. Siehe [Integrationsübersicht für Adobe Identity Management Service (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

Für temporäre Benutzer oder Rollen können Sie auch ein Ablaufdatum für das Benutzerkonto festlegen.

<!--  update this to a better info-graphic ![User types for your Admin](./assets/merchant-admin-users.png) -->

## Benutzer erstellen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add New User]**.

   Um einen vorhandenen Benutzer zu bearbeiten, klicken Sie auf einen Benutzernamen im Raster. Sie können _[!UICONTROL User Info]_und_[!UICONTROL User Role]_ nach Bedarf.

1. Im _[!UICONTROL Account Information]_führen Sie folgende Schritte aus:

   ![Informationen zu Benutzerkonten](./assets/permissions-user-new.png){width="600" zoomable="yes"}

   - Geben Sie die **[!UICONTROL User Name]** für -Konto.

     Der Benutzername sollte leicht zu merken sein. Dabei wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn der Benutzername beispielsweise `John`kann sich auch anmelden als `john`.

   - Füllen Sie die folgenden Informationen aus:

      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**
      - **[!UICONTROL Email address]**

     Jedes Benutzerkonto muss über eine eindeutige E-Mail-Adresse verfügen.

   - Geben Sie einen **[!UICONTROL Password]** für das Konto.

     >[!NOTE]
     >
     >Ein Administratorkennwort muss mindestens sieben Zeichen lang sein und sowohl Buchstaben als auch Zahlen enthalten. Weitere Kennwortoptionen finden Sie unter [Konfigurieren der Admin Security](security-admin.md).

   - Für **[!UICONTROL Password Confirmation]**, geben Sie das Kennwort erneut ein, um sicherzustellen, dass es korrekt eingegeben wurde.

   - Wenn Ihr Store mehrere Sprachen hat, legen Sie **[!UICONTROL Interface Locale]** in die Sprache, die für die Admin-Oberfläche verwendet werden soll.

1. Satz **[!UICONTROL This Account is]** nach `Active`.

1. Klicken Sie auf das Kalendersymbol, um die **[!UICONTROL Expiration Date]** für das Benutzerkonto.

   Die Definition eines Ablaufdatums ist hilfreich, wenn ein Benutzer oder eine Rolle temporär ist. Nach dem Ablaufdatum ändert sich der Benutzerkontenstatus in `Inactive` und bei Bedarf aktualisiert werden.

1. under _[!UICONTROL Current User Identity Verification]_, geben Sie Ihr Passwort für Ihr Benutzerkonto ein.

>[!IMPORTANT]
>
>Mit dem _[!UICONTROL Account Information]_abschließen, können Sie den Benutzer speichern. Der neue Benutzer wird im_[!UICONTROL Users]_ -Raster, aber der Benutzername kann sich erst anmelden, wenn eine Rolle zugewiesen wurde.

## Zuweisen einer Benutzerrolle

1. Klicken Sie im linken Bereich auf **[!UICONTROL User Role]**.

   Das Raster listet alle vorhandenen Benutzerrollen auf. Für einen neuen Store: _[!UICONTROL Administrators]_ist die einzige verfügbare Rolle.

   ![Admin - Hinzufügen neuer Benutzerrollen](./assets/permissions-user-roles.png){width="600" zoomable="yes"}

1. Im _[!UICONTROL Assigned]_-Spalte eine Benutzerrolle.

   Sie können [Anzeigen vorhandener oder Definition zusätzlicher Benutzerrollen](permissions-user-roles.md). Nachdem eine Rolle definiert wurde, müssen Sie das Benutzerkonto bearbeiten, um die neue Rolle zuzuweisen.

## 2FA-Anbieter überprüfen oder zurücksetzen

1. Öffnen Sie das Admin-Benutzerkonto.

1. Klicken Sie im linken Bereich auf **[!UICONTROL 2FA]**.

   ![Admin - Hinzufügen neuer Benutzerrollen](./assets/permissions-user-2fa.png){width="600" zoomable="yes"}

1. Überprüfen der für verfügbaren 2FA-Lösungen _Admin_ -Benutzer verwenden und jedem Benutzer raten, die Lösungen zu installieren, die er verwenden möchte, bevor er sich anmeldet.

   Die Authentifizierung durch nur eine 2FA-Lösung ist erforderlich, um sich bei der _Admin_.

1. Wenn der Benutzer die 2FA-Lösung neu installieren muss, können Sie die aktuelle 2FA-Konfiguration zurücksetzen.

   Dazu muss der Benutzer den Einrichtungsprozess wiederholen, bevor er sich erneut anmelden kann. Beispielsweise könnte der Benutzer über ein neues Smartphone verfügen und muss Google Authenticator neu installieren. Um das aktuelle 2FA-Setup des Benutzers zu löschen, klicken Sie auf **[!UICONTROL Reset (Provider)]** für jede Lösung, die Sie löschen möchten. Klicken Sie bei Aufforderung auf **[!UICONTROL OK]** zur Bestätigung.

   Der Benutzer erhält eine E-Mail mit einem Link zu [2FA konfigurieren](security-two-factor-authentication.md). Der Link kann nur einmal verwendet werden. Wenn der Benutzer versucht, sich mehrmals anzumelden, wird nach jedem Versuch ein neuer Link gesendet.

1. Klicken **[!UICONTROL Save User]**.

1. Geben Sie bei Aufforderung Ihr Kennwort zur Bestätigung Ihrer Identität ein und klicken Sie erneut auf **[!UICONTROL Save User]**.

   Die _[!UICONTROL Users]_-Raster geöffnet und listet alle Benutzer auf.

## Löschen eines Admin-Benutzers

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Suchen Sie das Benutzerkonto mithilfe von Filtern über dem Raster und klicken Sie auf den Benutzernamen.

1. Geben Sie bei Aufforderung Ihr Kennwort zur Bestätigung Ihrer Identität ein.

1. Klicken Sie oben rechts auf **[!UICONTROL Delete User]**.

1. Klicken Sie zur Bestätigung der Aktion auf **[!UICONTROL OK]**.

## Vergessenes Passwort und Zurücksetzen von E-Mails

Die Konfiguration der E-Mail-Vorlage &quot;Admin&quot;bestimmt die E-Mails, die gesendet werden, wenn Benutzer ihr Passwort vergessen und zurücksetzen. Diese Konfiguration gibt den Store-Kontakt an, der als Absender der Nachricht erscheint, und wie lange der Link zur Passwortwiederherstellung gültig bleibt.

**_So konfigurieren Sie die Admin-E-Mail-Vorlagen:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Setting]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Seitenbereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL Admin]**.

1. Erweitern ![Erweiterungs-Umschalter](../assets/icon-display-expand.png) die **[!UICONTROL Admin User Emails]** Abschnitt.

   ![Erweiterte Konfiguration - Einstellungen der Admin-E-Mail-Vorlage](../configuration-reference/advanced/assets/admin-admin-user-emails.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Forgot Password Email Template]** in die Vorlage, die gesendet wird, wenn ein Administrator sein Passwort vergisst.

1. Satz **[!UICONTROL Forgot and Reset Email Sender]** an den Store-Kontakt, der als Absender der Nachricht angezeigt wird.

1. Satz **[!UICONTROL User Notification Template]** zur E-Mail-Vorlage hinzu, die als Standard für Admin-Benachrichtigungen verwendet wird.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Gesperrte Benutzer

Aus Sicherheitsgründen Ihres Unternehmens werden Benutzerkonten standardmäßig nach sechs fehlgeschlagenen Versuchen gesperrt, [Anmelden](../getting-started/admin-signin.md) an den Administrator. Alle Benutzerkonten, die derzeit gesperrt sind, werden im Raster Gesperrte Benutzer angezeigt. Ein Konto kann von jedem anderen Benutzer mit vollständigen Administratorberechtigungen entsperrt werden.

Zusätzliche Maßnahmen zur Passwortsicherheit können im Abschnitt [Erweiterter Admin](../configuration-reference/advanced/admin.md#security) Konfiguration. Siehe [Admin Security](security-admin.md).

![Warnung bei Anmeldebildschirm - Konto ist vorübergehend deaktiviert](./assets/admin-login-locked-out-message.png){width="300"}

**_So entsperren Sie ein Admin-Konto:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL Locked Users]**.

1. Aktivieren Sie im Raster das Kontrollkästchen des gesperrten Kontos.

   ![Berechtigungen - gesperrte Benutzerkonten](./assets/permissions-locked-users-grid.png){width="600" zoomable="yes"}

1. Legen Sie in der oberen linken Ecke **[!UICONTROL Actions]** nach `Unlock`.

1. Klicks **[!UICONTROL Submit]** , um das Konto zu entsperren.
