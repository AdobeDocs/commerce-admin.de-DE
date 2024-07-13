---
title: Konfigurieren der Commerce Admin-Integration mit der ID
description: Befolgen Sie dieses optionale Verfahren zur Integration der Adobe Commerce Admin-Benutzerkontoanmeldungen in Adobe ID.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
source-git-commit: 9a9106cde5184823755fb1f44fe7eae300442abc
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# Konfigurieren der Commerce Admin-Integration mit Adobe ID

{{ee-feature}}

Diese Integration unterstützt Commerce-Händler mit Admin-Benutzern, die über eine Adobe ID verfügen und die die Anmeldung bei Adobe Commerce und Adobe Business-Produkten optimieren möchten. Sie ist optional und wird pro Instanz aktiviert. Nur Admin-Benutzer-Workflows sind bei Aktivierung betroffen. 

>[!IMPORTANT]
>
>Admin-Benutzer sollten ihre Commerce Admin-Anmeldeinformationen (Benutzername und Kennwort) und 2FA-Anmeldeinformationen speichern, bevor sie diese Integration aktivieren. Diese Anmeldeinformationen werden benötigt, wenn die IMS-Integration deaktiviert ist.

## Voraussetzungen

* Adobe Commerce 2.4.5 oder höher
* Ein Adobe.com -Konto mit Zugriff auf den [Adobe Admin Console](https://adminconsole.adobe.com/).

Der Administrator, der diese Integration konfiguriert, benötigt bei der Aktivierung des Moduls die folgenden Anmeldeinformationen:

* Organisations-ID (von [Adobe Admin Console](https://adminconsole.adobe.com/) abgerufen), die mindestens 24 Zeichen lang sein muss. Der authentifizierte Benutzer muss zu dieser IMS-Organisation gehören. Informationen zum Auffinden Ihrer Organisations-ID finden Sie unter [Organisationen in Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* 2FA sollte auf Organisationsebene in Adobe Admin Console erzwungen werden, um das Modul zu aktivieren. Überprüfen Sie die [Authentifizierungseinstellungen](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* Client-ID
* Client-Geheimschlüssel
* Client-ID und Client-Geheimnis sind verfügbar, nachdem API-Schlüssel aus dem [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/credentials/) abgerufen wurden.

Commerce-Administratoren müssen ein Konto mit einer Adobe ID erstellen, um sich anzumelden.

## Allgemeine Schritte

* Adobe-Organisations-ID von [Adobe Admin Console](https://adminconsole.adobe.com/) abrufen
* Erstellen Sie ein neues Projekt, IMS-API-Schlüssel und einen geheimen Schlüssel aus dem [Adobe Developer Console](https://developer.adobe.com/)
* Konfigurieren von Adobe Commerce-Benutzern in Adobe Admin Console
* Aktivieren Sie das Modul `AdminAdobeIms` .

Für eine erfolgreiche Integration müssen alle Adobe Commerce-Benutzer über Admin-Benutzerkonten mit demselben Namen und derselben primären E-Mail-Adresse verfügen. Wenn kein übereinstimmendes Admin-Benutzerkonto vorhanden ist, muss ein Benutzer mit den erforderlichen Berechtigungen (normalerweise mit der Administratorrolle zugewiesen) manuell [das Admin-Benutzerkonto](../systems/permissions-users-all.md#create-a-user) mit demselben Namen und derselben E-Mail erstellen.

## Integration konfigurieren

Nachdem die folgenden Schritte von einem Administrator oder Entwickler mit Systemzugriff abgeschlossen wurden, wird die Schaltfläche &quot;_[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_&quot;auf der Anmeldeseite für Commerce-Administratoren für alle Admin-Benutzer angezeigt.

### Schritt 1: Abrufen der Adobe-Organisations-ID

Um diese Funktion zu aktivieren, ist die Mitgliedschaft in mindestens einer IMS-Organisation erforderlich. Wenn Sie über eine Adobe ID verfügen, gehören Sie standardmäßig mindestens einer Adobe-Organisation an. Melden Sie sich bei [Adobe Admin Console](https://adminconsole.adobe.com/) an, um Ihre Organisations-ID abzurufen.

### Schritt 2: Neues Projekt, IMS-API-Schlüssel und geheime Schlüssel erstellen

Um Projekte für eine Organisation zu erstellen, muss das Adobe-Administratorkonto für die Organisation über die Systemadministrator- oder Entwicklerrolle verfügen. Weitere Informationen finden Sie im [Developer Console-Handbuch](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. Melden Sie sich bei [Adobe Developer Console](https://developer.adobe.com/) an.
1. Gehen Sie zur Registerkarte &quot;**[!UICONTROL Projects]**&quot;(adobe.io/projects) und klicken Sie auf &quot;**[!UICONTROL Create a new project]**&quot;.
1. Klicken Sie auf der neu erstellten Projektseite auf **[!UICONTROL Add API]** .
1. Wählen Sie **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]** aus.
1. Wählen Sie **[!UICONTROL Oauth 2.0 Web]** aus.
1. Geben Sie den **[!UICONTROL Redirect URI]**: `https://<hostname>/` an.
1. Geben Sie den **[!UICONTROL Redirect URI pattern]**: `https://<hostname>/.*` an.

   Lassen Sie alle Punkte im Hostnamen maskieren, indem Sie vor den Punkten den Wert `\\` drücken. Durch Hinzufügen eines Platzhalters am Ende der URL wird der geheime Adobe Commerce-Administratorschlüssel unterstützt.

1. Klicken Sie auf **[!UICONTROL Save configured API]**.
1. Kopieren Sie die Schlüssel [!UICONTROL Client ID] und [!UICONTROL Client Secret] aus dem erstellten Projekt.

### Schritt 3: Konfigurieren von Adobe Commerce-Benutzern in Adobe Admin Console

Bevor Sie die Integration aktivieren, stellen Sie sicher, dass jedes Adobe Commerce Admin-Benutzerkonto über ein entsprechendes Adobe IMS-Konto verfügt. Adobe Commerce-Benutzer müssen einer bestimmten Adobe-Organisation angehören, um sich mit einer Adobe ID anzumelden.

>[!TIP]
>
>Sie können mehrere Benutzerkonten erstellen, indem Sie die Benutzerinformationen aus einer CSV-Datei hochladen. Siehe [Mehrere Benutzer verwalten](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. Navigieren Sie in der [Adobe Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html) zu **[!UICONTROL Users]** > **[!UICONTROL Users]**.

1. Klicken Sie auf **[!UICONTROL Add User]**.

1. Geben Sie die E-Mail-Adresse des Benutzers ein.

   Falls zutreffend, wird der empfohlene ID-Typ automatisch ausgefüllt. Sie können diese Einstellung auf eine der Produkt-IDs in der Liste ändern, die auf dem Kaufplan Ihres Unternehmens basiert.

   Sie können bis zu zehn Benutzer gleichzeitig hinzufügen. Um weitere hinzuzufügen, wiederholen Sie die vorherigen Schritte nach dem Speichern Ihrer Änderungen.

1. Klicken Sie auf **[!UICONTROL Save]**.

Der Benutzer wird hinzugefügt und in der Liste [!UICONTROL Users] angezeigt.

### Schritt 4: Aktivieren des AdminAdobeIms-Moduls

Das Modul `AdminAdobeIms` ist für die Adobe Commerce/Adobe IMS-Integration verantwortlich. Nachdem Sie das neue Projekt eingerichtet und Ihre Organisations-ID, Client-ID und Ihr Client-Geheimnis kopiert haben, können Sie das Modul `AdminAdobeIms` aktivieren.

Geben Sie `bin/magento admin:adobe-ims:enable` ein. Sie werden aufgefordert, die folgenden Parameter einzugeben. Verwenden Sie die Werte, die bei der Projekterstellung generiert wurden.

* Organisations-ID
* Client-ID
* Client-Geheimschlüssel
* 2FA aktiviert

Adobe Commerce zeigt eine Meldung an, die angibt, ob die Aktivierung erfolgreich war oder fehlgeschlagen ist.

Nach der erfolgreichen Aktivierung dieser Funktion können Sie andere Adobe Commerce-Benutzerkonten in Adobe IMS-Konten übertragen. Adobe Commerce-Benutzer müssen zur konfigurierten Adobe-Organisation gehören, um sich mit einer Adobe ID anzumelden.
