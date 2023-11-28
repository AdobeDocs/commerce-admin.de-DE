---
title: Deaktivieren der Commerce Admin-Integration mit Adobe ID
description: Befolgen Sie dieses optionale Verfahren zum Deaktivieren der Adobe Commerce Admin-Integration mit Adobe IMS.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# Deaktivieren der Commerce Admin-Integration mit Adobe ID

{{ee-feature}}

Merchants, die ihre Commerce-Instanz mit dem Adobe IMS-Authentifizierungs-Workflow integriert haben, müssen diese optionale Integration möglicherweise deaktivieren.

Commerce-Implementierungen kehren zum standardmäßigen Commerce-Authentifizierungs-Workflow und zu Passwortrichtlinien zurück, nachdem die IMS-Integration deaktiviert wurde. Nur Admin-Benutzer-Workflows sind betroffen, wenn diese Integration aktiviert oder deaktiviert ist.

Siehe [Ihr Admin-Konto](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html) für einen Überblick über die Commerce Admin-Anmeldung.

## Schritt 1: Integration deaktivieren

Sie können diese Integration nicht über den Administrator deaktivieren. Um die Adobe IMS-Integration in Commerce zu deaktivieren und die Commerce-Authentifizierung auf ihren Standardstatus zurückzusetzen, müssen Sie die Integration über die Befehlszeilenschnittstelle deaktivieren.

So deaktivieren Sie die Integration:

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerce zeigt bei Erfolg die folgende Meldung an:

```terminal
Admin Adobe IMS integration is disabled.
```

## Schritt 2: Erstellen oder Abrufen Ihres Commerce-Passworts

Nach der Deaktivierung der Integration müssen Admin-Benutzer ein Commerce-Kennwort verwenden, um sich beim Admin anzumelden.

* Commerce-Admin-Benutzer, die sich ihr bereits vorhandenes Commerce-Passwort merken (d. h. ein Commerce-Passwort, das vor der IMS-Integration erstellt wurde), können sich mit diesem bei Admin anmelden.

* Commerce-Admin-Benutzer, die entweder kein bereits vorhandenes Commerce-Passwort haben oder vergessen haben, müssen ein neues Passwort erstellen. Um ein neues Kennwort zu erstellen, können Admin-Benutzer die [!UICONTROL Forgot your password?] auf der Commerce-Anmeldeseite , um ein neues Kennwort zu erstellen. Siehe [Zurücksetzen von Kundenkennwörtern](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html). Commerce akzeptiert kein leeres Kennwortfeld.

## Nach dem Deaktivieren der Integration

Der standardmäßige Commerce-Authentifizierungs-Workflow wird fortgesetzt, nachdem die IMS-Integration deaktiviert wurde und Admin-Benutzer erneut nach ihrem Kennwort gefragt werden.

Durch Deaktivieren der IMS-Integration werden die Anmeldeinformationen gelöscht, die bei Aktivierung der Integration eingegeben wurden (`Organization ID`, `Client ID`, und `Client Secret` -Werte) aus den Commerce-Konfigurationsdateien.
