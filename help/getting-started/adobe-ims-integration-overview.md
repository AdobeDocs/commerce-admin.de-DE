---
title: Übersicht über die Integration von Adobe Identity Management Service (IMS)
description: Einführung der optionalen Integration der Adobe Commerce Admin-Anmeldung mit Adobe IMS
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# Übersicht über die Integration von Adobe Identity Management Service (IMS)

{{ee-feature}}

Adobe Commerce-Administratoren, die über ein Adobe-Konto verfügen, können sich jetzt mit ihrer Adobe ID bei Adobe Commerce anmelden. Adobe Identity Management Service (IMS) ist eine auf Adobe Outh 2.0 basierende Identitätsverwaltungsfunktion, die die Authentifizierung unterstützt. Durch die Integration der Commerce Admin-Authentifizierung in den IMS-Authentifizierungs-Workflow von Adobe Business Product kann der Authentifizierungsprozess für Benutzer optimiert werden, die mit anderen Adobe-Produkten arbeiten. Diese Integration ist optional und wird pro Instanz aktiviert. Nur Admin-Benutzer-Workflows sind betroffen, wenn diese Integration aktiviert ist. 

Die für die Integration von Commerce Admin IMS erforderlichen Module sind in  `adobe-ims-metapackage`, das mit den Kernversionen von Adobe Commerce integriert ist.

Informationen zur Implementierung dieser Integration finden Sie unter [Konfigurieren der Commerce Admin-Integration mit IMS](./adobe-ims-config.md).

## Änderungen an Admin-Workflows und -Benutzeroberfläche nach der Integration mit IMS

Wenn diese Integration aktiviert ist, erfahren Commerce-Admin-Benutzer Änderungen an der standardmäßigen Commerce Admin-Anmeldung und dem Authentifizierungs-Workflow, da sie Routineaufgaben im Admin ausführen, für die eine erneute Authentifizierung erforderlich ist, z. B. die Erstellung eines Admin-Benutzers. Für die Modulaktivierung ist eine zweifakultative Authentifizierung (2FA) auf der Ebene der Adobe-Organisation erforderlich. Die standardmäßigen Admin-Anmeldedaten und 2FA sind deaktiviert und die _[!UICONTROL Sign In with Adobe ID]_-Schaltfläche ersetzt das standardmäßige Formular Admin Sign in . Berechtigungen werden weiterhin vom Administrator verwaltet.

## Auswirkungen der Admin-Integration mit IMS auf Commerce-Passwörter

Für Commerce-Implementierungen, die mit Adobe IMS integriert wurden, ist ein Adobe ID-Konto mit Zugriff auf die Adobe IMS-Organisation erforderlich, die während des IMS-Aktivierungsprozesses für die Commerce-Anwendung konfiguriert ist.  Wenn die IMS-Integration aktiviert ist, authentifizieren sich Admin-Benutzer über die Adobe-Anmeldeseite mit ihren Adobe-Anmeldeinformationen. Die Commerce-Kennwörter und Benutzernamen für Admin-Benutzer werden nicht mehr für die Authentifizierung verwendet, solange die Adobe IMS-Integration aktiviert ist.

Wenn die IMS-Integration deaktiviert ist, müssen sich Admin-Benutzer über Adobe Commerce erneut mit ihrem Commerce-Benutzernamen und -Kennwort authentifizieren. Admin-Benutzer sollten ihre Commerce Admin-Anmeldeinformationen (Benutzername und Kennwort) und 2FA-Anmeldeinformationen speichern, bevor sie diese Integration aktivieren.

Bestimmte Backend-Komponenten, die an der Benutzerauthentifizierung beteiligt sind, benötigen weiterhin ein Kennwort, das nicht null ist. Um diese Anforderung zu erfüllen, erstellt Commerce zufällige Kennwörter für neu erstellte Admin-Benutzer in der `admin_user` Tabelle.

Benutzerkonten und Rollenberechtigungen für die Commerce-Anwendung werden weiterhin vom Commerce Admin verwaltet.


## Generierung von Web-API-Token mit IMS-Anmeldeinformationen

Commerce-Admin-APIs sind betroffen, wenn die Admin-Authentifizierung mit Adobe IMS in einer Commerce-Instanz aktiviert ist. Admin-Benutzer können die von der Commerce-Instanz ausgestellten Anmeldeinformationen nicht mehr verwenden. Dies sind die Anmeldeinformationen, die zum Anmelden beim Administrator und zum Abrufen von Zugriffstoken erforderlich sind, mit denen Dienste Anfragen an die Admin REST- und SOAP-APIs senden können.

Nachdem die Adobe IMS-Integration aktiviert wurde, müssen Administratoren [Adobe IMS OAuth-Token](https://developer.adobe.com/developer-console/docs/guides/authentication/OAuthIntegration/) für Adobe Commerce-API-Endpunkte, für die eine Authentifizierung erforderlich ist. Client-Lösungen rufen die Token dynamisch für die Verwendung der Web-API ab. Dieser Authentifizierungsmechanismus ist für REST- und SOAP-Web-API-Bereiche im Rahmen der Konfiguration dieser Integration aktiviert.

Siehe [Token-basierte Authentifizierung](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/) für einen Überblick darüber, wie Web-APIs Commerce-Zugriffstoken verwenden, einschließlich IMS-Zugriffstoken.

## Commerce-Sitzungsverwaltung und Adobe IMS-Zugriffstoken

Zugriffstoken enthalten sowohl Benutzeranmeldeinformationen als auch Sitzungsinformationen. Nachdem ein Benutzer authentifiziert wurde und eine Sitzung begonnen wurde, werden diese beiden Variablen zur Benutzersitzung hinzugefügt:

`token_last_check_time`. Identifiziert die aktuelle Zeit und wird von der `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` Plug-in.

`adobe_access_token` - Identifiziert die `ACCESS_TOKEN` Wert, der während der Zulassung erhalten wurde.

Die `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` Plug-in prüft, ob die `token_last_check_time` wurde vor 10 Minuten aktualisiert. Wenn die Variable `token_last_check_time` vor zehn Minuten überprüft wurde, führt der Authentifizierungs-Workflow einen API-Aufruf an IMS durch, um das Zugriffstoken zu validieren. Die Sitzung wird fortgesetzt. Wenn das Zugriffstoken gültig ist, wird die `token_last_check_time` -Wert auf die aktuelle Zeit aktualisiert. Wenn das Token nicht gültig ist, wird die Sitzung beendet.

## Wichtige Dateien

`adminAdobeIms` - Bietet eine Implementierung der Admin-Anmeldung basierend auf der `AdobeImsApi` -Modul.

`admin_adobe_ims_webapi` - Verwaltet einen Datensatz aller validierten Zugriffstoken. Wenn ein Token validiert oder ungültig gemacht wird, wird in dieser Tabelle ein Datensatz mit seinem Status beibehalten.

`adobeIms` - Implementiert die gesamte Geschäftslogik im Zusammenhang mit der Integration mit Adobe IMS (beibehalten, um Abwärtskompatibilitäten zu vermeiden).

`adobeImsApi` - Deklariert die Schnittstellen, die die Integration mit Adobe IMS unterstützen.

`adminadobe-ims.log` - Fehlerprotokolldatei.

## Integration aktivieren

Das Adobe IMS-Metapaket wird mit Adobe Commerce 2.4.5 und höher installiert, muss jedoch für die Verwendung konfiguriert werden. Sie erweitert die `AdobeIms` -Modul zur Unterstützung des Moduls, das die Authentifizierungslogik (`AdminAdobeIms`).

Weitere Informationen zum Aktivieren der Integration finden Sie unter [Konfigurieren der Commerce Admin-Integration mit Adobe IMS](./adobe-ims-config.md).
