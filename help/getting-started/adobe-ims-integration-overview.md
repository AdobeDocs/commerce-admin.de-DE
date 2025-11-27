---
title: Übersicht über die Integration von Adobe Identity Management Service (IMS)
description: Einführung in die optionale Integration der Adobe Commerce Admin-Anmeldung mit Adobe IMS
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 15118877bb8cc533b2323819db34da0513899e25
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 0%

---

# Übersicht über die Integration von Adobe Identity Management Service (IMS)

{{ee-feature}}

Adobe Commerce-Admin-Benutzende mit einem Adobe-Konto können sich jetzt mit ihrer Adobe ID bei Adobe Commerce anmelden. Adobe Identity Management Service (IMS) ist die auf OAuth 2.0 basierende Identitätsverwaltungsfunktion von Adobe, die die Authentifizierung unterstützt. Die Integration der Commerce-Admin-Authentifizierung in den IMS-Authentifizierungs-Workflow des Adobe-Geschäftsprodukts kann den Authentifizierungsprozess für Benutzende optimieren, die mit anderen Adobe-Produkten arbeiten. Diese Integration ist optional und wird für jede Instanz aktiviert. Wenn diese Integration aktiviert ist, sind nur Workflows für Admin-Benutzer betroffen. 

Die für die Commerce Admin IMS-Integration erforderlichen Module sind in `adobe-ims-metapackage` zusammengefasst, das mit den Adobe Commerce-Hauptversionen gebündelt ist.

Informationen zum Implementieren dieser Integration finden Sie unter [Konfigurieren der Commerce Admin-Integration mit IMS](./adobe-ims-config.md).

## Änderungen an Admin-Workflows und der Benutzeroberfläche nach der Integration mit IMS

Wenn diese Integration aktiviert ist, erleben Commerce-Admin-Benutzerinnen und -Benutzer Änderungen am standardmäßigen Commerce-Admin-Anmelde- und Authentifizierungs-Workflow, während sie im Admin-Bereich Routineaufgaben ausführen, für die eine erneute Authentifizierung erforderlich ist, z. B. das Erstellen eines Admin-Benutzers. Für die Modulaktivierung ist eine Durchsetzung der Zwei-Faktor-Authentifizierung (2FA) auf Adobe-Organisationsebene erforderlich. Die standardmäßige Admin-Anmeldung und 2FA sind deaktiviert und die Schaltfläche _[!UICONTROL Sign In with Adobe ID]_ersetzt das standardmäßige Admin-Anmeldeformular. Berechtigungen werden weiterhin vom Administrator verwaltet.

## Auswirkungen der Admin-Integration mit IMS auf Commerce-Kennwörter

Commerce-Bereitstellungen, die mit Adobe IMS integriert wurden, erfordern ein Adobe ID-Konto mit Zugriff auf die Adobe IMS-Organisation, die für die Commerce-Anwendung während des IMS-Aktivierungsprozesses konfiguriert ist.  Wenn die IMS-Integration aktiviert ist, authentifizieren sich Admin-Benutzer über die Anmeldeseite von Adobe mit ihren Adobe-Anmeldeinformationen. Die Commerce-Kennwörter und -Benutzernamen für Admin-Benutzende werden für die Authentifizierung nicht mehr verwendet, solange die Adobe IMS-Integration aktiviert ist.

Wenn die IMS-Integration deaktiviert ist, müssen sich Admin-Benutzer mithilfe ihres Commerce-Benutzernamens und -Kennworts erneut über Adobe Commerce authentifizieren. Admin-Benutzer sollten ihre Commerce-Admin-Anmeldedaten (Benutzername und Kennwort) und 2FA-Anmeldedaten speichern, bevor sie diese Integration aktivieren.

Bestimmte Backend-Komponenten, die an der Benutzerauthentifizierung beteiligt sind, erfordern weiterhin ein Kennwort, das nicht null ist. Um diese Anforderung zu erfüllen, erstellt Commerce in der `admin_user` zufällige Kennwörter für neu erstellte Admin-Benutzer.

Benutzerkonten und Rollenberechtigungen für das Commerce-Programm werden weiterhin vom Commerce-Administrator verwaltet.


## Generieren von Web-API-Token mit IMS-Anmeldeinformationen

Commerce Admin-APIs sind betroffen, wenn die Admin-Authentifizierung mit Adobe IMS in einer Commerce-Instanz aktiviert ist. Admin-Benutzer können die von der Commerce-Instanz ausgestellten Anmeldeinformationen nicht mehr verwenden. Dies sind die Anmeldeinformationen, die erforderlich sind, um sich beim Admin anzumelden und Zugriffstoken abzurufen, die Services für Anfragen an die Admin-REST- und SOAP-APIs verwenden können.

Nachdem die Adobe IMS-Integration aktiviert wurde, müssen Admin-Benutzer [Adobe IMS OAuth-Token](https://developer.adobe.com/developer-console/docs/guides/authentication/) für Adobe Commerce-API-Endpunkte verwenden, für die eine Authentifizierung erforderlich ist. Client-Lösungen erhalten die Token dynamisch für die Web-API-Verwendung. Dieser Authentifizierungsmechanismus ist für REST- und SOAP-Web-API-Bereiche im Rahmen der Konfiguration dieser Integration aktiviert.

Unter [Token-basierte Authentifizierung](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/) finden Sie einen Überblick darüber, wie Web-APIs Commerce-Zugriffstoken, einschließlich IMS-Zugriffstoken, verwenden.

## Commerce-Sitzungsverwaltung und Adobe IMS-Zugriffstoken

Zugriffstoken enthalten sowohl Benutzeranmeldeinformationen als auch Informationen zur Anmeldesitzung. Nachdem ein Benutzer authentifiziert und eine Sitzung gestartet wurde, werden diese beiden Variablen zur Sitzung des Benutzers hinzugefügt:

`token_last_check_time`. Identifiziert die aktuelle Zeit und wird vom `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin`-Plug-in verwendet.

`adobe_access_token` - Identifiziert den während der Autorisierung empfangenen `ACCESS_TOKEN`.

Das `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin`-Plug-in prüft, ob die `token_last_check_time` vor 10 Minuten aktualisiert wurde. Wenn die `token_last_check_time` vor zehn Minuten überprüft wurde, führt der Authentifizierungs-Workflow einen API-Aufruf an IMS durch, um das Zugriffs-Token zu validieren, und die Sitzung wird fortgesetzt. Wenn das Zugriffstoken gültig ist, wird der `token_last_check_time` auf die aktuelle Zeit aktualisiert. Wenn das Token ungültig ist, wird die Sitzung beendet.

## Wichtige Dateien

`adminAdobeIms` - Stellt eine Implementierung der Admin-Anmeldung bereit, die auf dem `AdobeImsApi` basiert.

`admin_adobe_ims_webapi` : Erfasst einen Datensatz aller validierten Zugriffstoken. Wenn ein Token validiert oder ungültig gemacht wird, wird ein Datensatz seines Status in dieser Tabelle beibehalten.

`adobeIms` - Implementiert die gesamte Geschäftslogik im Zusammenhang mit der Integration mit Adobe IMS (wird beibehalten, um Abwärtsinkompatibilitäten zu vermeiden).

`adobeImsApi` - Deklariert die Schnittstellen, die die Integration mit Adobe IMS unterstützen.

`adminadobe-ims.log` - Fehlerprotokolldatei.

## Integration aktivieren

Das Adobe IMS-Metapaket wird mit Adobe Commerce 2.4.5 und höher installiert, muss jedoch für die Verwendung konfiguriert werden. Es erweitert das `AdobeIms`-Modul, um das Modul zu unterstützen, das die Authentifizierungslogik (`AdminAdobeIms`) aktiviert.

Weitere Informationen zur Aktivierung der Integration finden Sie unter [Konfigurieren der Commerce Admin-Integration mit Adobe IMS](./adobe-ims-config.md).
