---
title: Konfigurieren der Commerce Admin-Integration mit der ID
description: Folgen Sie dieser optionalen Anleitung zur Integration von Adobe Commerce Admin-Benutzerkonto-Anmeldungen in Adobe ID.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
source-git-commit: 8589444a126c82f033c5b852b20493d1cf83c338
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# Konfigurieren der Commerce Admin-Integration mit Adobe ID

{{ee-feature}}

Diese Integration unterstützt Commerce-Händler mit Admin-Benutzern, die über eine Adobe ID verfügen und die Anmeldung bei Adobe Commerce- und Adobe Business-Produkten optimieren möchten. Sie ist optional und wird pro Instanz aktiviert. Wenn diese Option aktiviert ist, sind nur Workflows für Admin-Benutzer betroffen. 

>[!IMPORTANT]
>
>Admin-Benutzer sollten ihre Commerce-Admin-Anmeldedaten (Benutzername und Kennwort) und 2FA-Anmeldedaten speichern, bevor sie diese Integration aktivieren. Diese Anmeldeinformationen werden benötigt, wenn die IMS-Integration deaktiviert ist.

## Voraussetzungen

* Adobe Commerce 2.4.5 oder höher
* Ein Adobe.com -Konto mit Zugriff auf die [Adobe Admin Console](https://adminconsole.adobe.com/).

Der Administrator, der diese Integration konfiguriert, benötigt während der Aktivierung des Moduls die folgenden Anmeldeinformationen:

* Organisations-ID (bezogen von [Adobe Admin Console](https://adminconsole.adobe.com/)), die mindestens 24 Zeichen lang sein muss. Der authentifizierte Benutzer muss zu dieser IMS-Organisation gehören. Informationen zum Ermitteln Ihrer Organisations-ID finden Sie unter [Organisationen in Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* 2FA sollte auf Organisationsebene in Adobe Admin Console erzwungen werden, um das Modul zu aktivieren. Überprüfen Sie [Authentifizierungseinstellungen](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* Client-ID
* Client-Geheimnis
* Client-ID und Client-Geheimnis sind verfügbar, nachdem die API-Schlüssel von der [Adobe Developer Console abgerufen ](https://developer.adobe.com/developer-console/docs/guides/credentials/).

Commerce-Admin-Benutzende müssen ein Konto mit einer Adobe ID erstellen, um sich anzumelden.

## Allgemeine Schritte

* Adobe-Organisations-ID aus dem [Adobe Admin Console abrufen](https://adminconsole.adobe.com/)
* Generieren eines neuen Projekts, von IMS-API-Schlüsseln und Geheimnissen aus der [Adobe Developer Console](https://developer.adobe.com/)
* Konfigurieren von Adobe Commerce-Benutzern in der Adobe Admin Console
* Aktivieren Sie das `AdminAdobeIms`.

Für eine erfolgreiche Integration müssen alle Adobe Commerce-Benutzer über Admin-Benutzerkonten mit demselben Namen und derselben primären E-Mail-Adresse verfügen. Wenn kein entsprechendes Admin-Benutzerkonto vorhanden ist, muss ein Benutzer mit den erforderlichen Berechtigungen (in der Regel die Administratorrolle zugewiesen) manuell [das Admin-Benutzerkonto erstellen](../systems/permissions-users-all.md#create-a-user) mit demselben Namen und derselben E-Mail-Adresse.

## Integration konfigurieren

Nachdem die folgenden Schritte von einem Administrator oder Entwickler mit Systemzugriff ausgeführt wurden, wird die Schaltfläche _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_auf der Commerce Admin-Anmeldeseite für alle Admin-Benutzenden angezeigt.

### Schritt 1: Adobe-Organisations-ID abrufen

Die Mitgliedschaft in mindestens einer IMS-Organisation ist erforderlich, um diese Funktion zu aktivieren. Wenn Sie über eine Adobe ID verfügen, gehören Sie standardmäßig mindestens einer Adobe-Organisation an. Melden Sie sich bei der [Adobe Admin Console](https://adminconsole.adobe.com/) an, um Ihre Organisations-ID abzurufen.

### Schritt 2: Neues Projekt, IMS-API-Schlüssel und Geheimnis generieren

Um Projekte für eine Organisation zu erstellen, muss das Adobe-Administratorkonto für die Organisation über die Rolle Systemadministrator oder Entwickler verfügen. Siehe das Handbuch zu [Developer Console](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. Anmelden bei [Adobe Developer Console](https://developer.adobe.com/).
1. Wechseln Sie zur Registerkarte **[!UICONTROL Projects]** (adobe.io/projects) und klicken Sie auf **[!UICONTROL Create a new project]**.
1. Klicken Sie auf der neu erstellten Projektseite auf **[!UICONTROL Add API]** .
1. Wählen Sie **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]** aus.
1. Wählen Sie **[!UICONTROL Oauth 2.0 Web]** aus.
1. Geben Sie die **[!UICONTROL Redirect URI]** an: `https://<commerce_base_url>/`
1. Geben Sie die **[!UICONTROL Redirect URI pattern]** an: `https://<commerce_base_url>/.*`

   Lassen Sie alle Punkte im Host-Namen unangetastet, indem Sie den Punkten `\\` voranstellen. Das Hinzufügen eines Platzhalters am Ende der URL unterstützt den Adobe Commerce Admin-Geheimschlüssel.

1. Klicken Sie auf **[!UICONTROL Save configured API]**.
1. Kopieren Sie die [!UICONTROL Client ID]- und [!UICONTROL Client Secret] aus dem erstellten Projekt.

### Schritt 3: Konfigurieren von Adobe Commerce-Benutzern in der Adobe Admin Console

Stellen Sie vor der Aktivierung der Integration sicher, dass jedes Adobe Commerce Admin-Benutzerkonto über ein entsprechendes Adobe IMS-Konto verfügt. Adobe Commerce-Benutzer müssen zu einer bestimmten Adobe-Organisation gehören, um sich mit einer Adobe ID anmelden zu können.

>[!TIP]
>
>Sie können mehrere Benutzerkonten erstellen, indem Sie die Benutzerinformationen aus einer CSV-Datei hochladen. Siehe [Verwalten mehrerer Benutzer](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. Navigieren Sie in der [](https://helpx.adobe.com/de/enterprise/using/admin-console.html)Adobe Admin Console **[!UICONTROL Users]** zu > **[!UICONTROL Users]**.

1. Klicken Sie auf **[!UICONTROL Add User]**.

1. Geben Sie die E-Mail-Adresse des Benutzers ein.

   Falls zutreffend, wird der empfohlene ID-Typ automatisch ausgefüllt. Sie können diese Einstellung in eine der Produkt-IDs in der Liste ändern, die auf dem Kaufplan Ihres Unternehmens basiert.

   Sie können bis zu zehn Benutzer gleichzeitig hinzufügen. Um weitere hinzuzufügen, wiederholen Sie die vorherigen Schritte, nachdem Sie Ihre Änderungen gespeichert haben.

1. Klicken Sie auf **[!UICONTROL Save]**.

Der Benutzer wird hinzugefügt und in der [!UICONTROL Users] angezeigt.

### Schritt 4: AdminAdobeIms-Modul aktivieren

Das `AdminAdobeIms` Modul ist für die Adobe Commerce/Adobe IMS-Integration verantwortlich. Nachdem Sie das neue Projekt eingerichtet und Ihre Organisations-ID, Client-ID und Ihr Client-Geheimnis kopiert haben, können Sie das `AdminAdobeIms`-Modul aktivieren.

`bin/magento admin:adobe-ims:enable` eingeben. Sie werden aufgefordert, die folgenden Parameter einzugeben. Verwenden Sie die Werte, die bei der Projekterstellung generiert wurden.

* Organisations-ID
* Client-ID
* Client-Geheimnis
* 2FA aktiviert

Adobe Commerce zeigt eine Meldung an, die angibt, ob die Aktivierung erfolgreich war oder fehlgeschlagen ist.

Nach erfolgreicher Aktivierung dieser Funktion können Sie andere Adobe Commerce-Benutzerkonten auf Adobe IMS-Konten umstellen. Adobe Commerce-Benutzer müssen zur konfigurierten Adobe-Organisation gehören, um sich mit einer Adobe ID anzumelden.
