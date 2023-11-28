---
title: Konfigurieren der Commerce Admin-Integration mit der ID
description: Befolgen Sie dieses optionale Verfahren zur Integration der Adobe Commerce Admin-Benutzerkontoanmeldungen in Adobe ID.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
source-git-commit: 20b2560ce2b8071c740907292544519f8b1c3ddf
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 1%

---

# Konfigurieren der Commerce Admin-Integration mit Adobe ID

{{ee-feature}}

Diese Integration unterstützt Commerce-Händler mit Admin-Benutzern, die über eine Adobe ID verfügen und die die Anmeldung bei Adobe Commerce und Adobe Business-Produkten optimieren möchten. Sie ist optional und wird pro Instanz aktiviert. Nur Admin-Benutzer-Workflows sind bei Aktivierung betroffen. 

>[!IMPORTANT]
>
>Admin-Benutzer sollten ihre Commerce Admin-Anmeldeinformationen (Benutzername und Kennwort) und 2FA-Anmeldeinformationen speichern, bevor sie diese Integration aktivieren. Diese Anmeldeinformationen werden benötigt, wenn die IMS-Integration deaktiviert ist.

## Voraussetzungen

* Adobe Commerce 2.4.5 oder höher
* Ein Adobe.com -Konto mit Zugriff auf [Adobe Admin Console](https://adminconsole.adobe.com/).

Der Administrator, der diese Integration konfiguriert, benötigt bei der Aktivierung des Moduls die folgenden Anmeldeinformationen:

* Organisations-ID (abgerufen von [Adobe Admin Console](https://adminconsole.adobe.com/)), die mindestens 24 Zeichen lang sein muss. Der authentifizierte Benutzer muss zu dieser IMS-Organisation gehören. Informationen zum Auffinden Ihrer Organisations-ID finden Sie unter [Organisationen im Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* 2FA sollte auf Organisationsebene in Adobe Admin Console erzwungen werden, um das Modul zu aktivieren. Überprüfen [Authentifizierungseinstellungen](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* Client-ID
* Client-Geheimschlüssel
* Client-ID und Client-Geheimnis sind verfügbar, nachdem API-Schlüssel aus dem [Adobe Developer-Konsole](https://developer.adobe.com/developer-console/docs/guides/credentials/).

Commerce-Admin-Benutzer müssen ein Konto mit einer Adobe ID erstellen, um sich anzumelden.

## Allgemeine Schritte

* Adobe-Organisations-ID von der [Adobe Admin Console](https://adminconsole.adobe.com/)
* Generieren Sie ein neues Projekt, IMS-API-Schlüssel und einen geheimen Schlüssel aus dem [Adobe Developer-Konsole](https://developer.adobe.com/)
* Aktivieren Sie die `AdminAdobeIms` Modul
* Konfigurieren Sie Adobe Commerce-Benutzer in der Adobe Admin Console.

Für eine erfolgreiche Integration müssen alle Adobe Commerce-Benutzer über Admin-Benutzerkonten mit demselben Namen und derselben primären E-Mail-Adresse verfügen. Wenn kein übereinstimmendes Admin-Benutzerkonto vorhanden ist, muss ein Benutzer mit den erforderlichen Berechtigungen (normalerweise mit der Administratorrolle) manuell [Admin-Benutzerkonto erstellen](../systems/permissions-users-all.md#create-a-user) mit demselben Namen und derselben E-Mail-Adresse.

## Integration konfigurieren

Nachdem die folgenden Schritte von einem Administrator oder Entwickler mit Systemzugriff abgeschlossen wurden, wird die _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_wird auf der Anmeldeseite &quot;Commerce Admin&quot;für alle Admin-Benutzer angezeigt.

### Schritt 1: Abrufen der Adobe-Organisations-ID

Um diese Funktion zu aktivieren, ist die Mitgliedschaft in mindestens einer IMS-Organisation erforderlich. Wenn Sie über eine Adobe ID verfügen, gehören Sie standardmäßig mindestens einer Adobe-Organisation an. Melden Sie sich bei [Adobe Admin Console](https://adminconsole.adobe.com/) , um Ihre Organisations-ID abzurufen.

### Schritt 2: Neues Projekt, IMS-API-Schlüssel und geheime Schlüssel erstellen

Um Projekte für eine Organisation zu erstellen, muss das Adobe-Administratorkonto für die Organisation über die Systemadministrator- oder Entwicklerrolle verfügen. Siehe [Entwicklerkonsole - Handbuch](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. Anmelden bei [Adobe Developer-Konsole](https://developer.adobe.com/).
1. Navigieren Sie zu **[!UICONTROL Projects]** tab (adobe.io/projects) und klicken Sie auf **[!UICONTROL Create a new project]**.
1. Klicks **[!UICONTROL Add API]** auf der neu erstellten Projektseite.
1. Auswählen **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. Auswählen **[!UICONTROL Oauth 2.0 Web]**.
1. Geben Sie die **[!UICONTROL Redirect URI]**: `https://<hostname>/`
1. Geben Sie die **[!UICONTROL Redirect URI pattern]**: `https://<hostname>/.*`

   Lassen Sie alle Punkte im Hostnamen maskieren, indem Sie den Punkten vorangehen mit `\\`. Durch Hinzufügen eines Platzhalters am Ende der URL wird der geheime Adobe Commerce-Administratorschlüssel unterstützt.

1. Klicken **[!UICONTROL Save configured API]**.
1. Kopieren Sie die [!UICONTROL Client ID] und [!UICONTROL Client Secret] Schlüssel aus dem erstellten Projekt.

### Schritt 3: Aktivieren des AdminAdobeIms-Moduls

Die `AdminAdobeIms` ist für die Adobe Commerce/Adobe IMS-Integration verantwortlich. Nachdem Sie das neue Projekt eingerichtet und Ihre Organisations-ID, Client-ID und Ihr Client-Geheimnis kopiert haben, können Sie die `AdminAdobeIms` -Modul.

Eingabe `bin/magento admin:adobe-ims:enable`. Sie werden aufgefordert, die folgenden Parameter einzugeben. Verwenden Sie die Werte, die bei der Projekterstellung generiert wurden.

* Organisations-ID
* Client-ID
* Client-Geheimschlüssel
* 2FA aktiviert

Adobe Commerce zeigt eine Meldung an, die angibt, ob die Aktivierung erfolgreich war oder fehlgeschlagen ist.

Nach der erfolgreichen Aktivierung dieser Funktion können Sie andere Adobe Commerce-Benutzerkonten in Adobe IMS-Konten übertragen. Adobe Commerce-Benutzer müssen zur konfigurierten Adobe-Organisation gehören, um sich mit einer Adobe ID anzumelden.

### Schritt 4: Konfigurieren von Adobe Commerce-Benutzern in Adobe Admin Console

Nach der erfolgreichen Aktivierung dieser Funktion können Sie andere Adobe Commerce-Benutzerkonten in Adobe IMS-Konten übertragen. Adobe Commerce-Benutzer müssen mindestens einer Adobe-Organisation angehören, um sich mit einer Adobe ID anzumelden.

1. Im [Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html), navigieren Sie zu **[!UICONTROL Users]**  > **[!UICONTROL Users]**.

1. Klicken **[!UICONTROL Add User]**.

1. Geben Sie die E-Mail-Adresse des Benutzers ein.

   Falls zutreffend, wird der empfohlene ID-Typ automatisch ausgefüllt. Sie können diese Einstellung auf eine der Produkt-IDs in der Liste ändern, die auf dem Kaufplan Ihres Unternehmens basiert.

   Sie können bis zu zehn Benutzer gleichzeitig hinzufügen. Um weitere hinzuzufügen, wiederholen Sie die vorherigen Schritte nach dem Speichern Ihrer Änderungen.

1. Klicken **[!UICONTROL Save]**.

Der Benutzer wird hinzugefügt und im [!UICONTROL Users] Liste.
