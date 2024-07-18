---
title: Commerce Admin-Integration mit Adobe ID deaktivieren
description: Befolgen Sie dieses optionale Verfahren zum Deaktivieren der Adobe Commerce Admin-Integration mit Adobe IMS.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
source-git-commit: 53c3b6c9fa9c152e6619528a43580b0acc71a2a5
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Commerce Admin-Integration mit Adobe ID deaktivieren

{{ee-feature}}

Merchants, die ihre Commerce-Instanz mit dem Adobe IMS-Authentifizierungs-Workflow integriert haben, müssen diese optionale Integration möglicherweise deaktivieren.

Commerce-Implementierungen kehren zum standardmäßigen Commerce-Authentifizierungs-Workflow und zu den Kennwortrichtlinien zurück, nachdem die IMS-Integration deaktiviert wurde. Nur Admin-Benutzer-Workflows sind betroffen, wenn diese Integration aktiviert oder deaktiviert ist.

Unter [Ihr Admin-Konto](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html) finden Sie einen Überblick über die Commerce Admin-Anmeldung.

## Schritt 1: Integration deaktivieren

Sie können diese Integration nicht über den Administrator deaktivieren. Um die Adobe IMS-Integration in Commerce zu deaktivieren und die Commerce-Authentifizierung auf ihren Standardstatus zurückzusetzen, müssen Sie die Integration über die Befehlszeilenschnittstelle deaktivieren.

So deaktivieren Sie die Integration:

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerce zeigt bei Erfolg die folgende Meldung an:

```
Admin Adobe IMS integration is disabled.
```

## Schritt 2: Erstellen oder Abrufen Ihres Commerce-Kennworts

Nach dem Deaktivieren der Integration müssen Admin-Benutzer ein Commerce-Kennwort verwenden, um sich beim Admin anzumelden.

* Commerce-Admin-Benutzer, die sich ihr bereits vorhandenes Commerce-Kennwort (d. h. ein Commerce-Kennwort, das vor der IMS-Integration erstellt wurde) merken, können sich mit diesem Kennwort beim Administrator anmelden.

* Commerce-Administratoren, die entweder kein bereits vorhandenes Commerce-Kennwort haben oder vergessen haben, dass sie dieses vergessen haben, müssen ein neues Kennwort erstellen. Um ein neues Kennwort zu erstellen, können Admin-Benutzer die Funktion [!UICONTROL Forgot your password?] auf der Commerce-Anmeldeseite verwenden, um ein neues Kennwort zu erstellen. Siehe [Zurücksetzen von Kundenkennwörtern](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html). Commerce akzeptiert kein leeres Kennwortfeld.

## Nach dem Deaktivieren der Integration

Der standardmäßige Commerce-Authentifizierungs-Workflow wird fortgesetzt, nachdem die IMS-Integration deaktiviert wurde und Admin-Benutzer erneut nach ihrem Kennwort gefragt werden.

Durch Deaktivieren der IMS-Integration werden die Anmeldeinformationen, die bei Aktivierung der Integration eingegeben wurden (`Organization ID`, `Client ID` und `Client Secret` Werte), aus den Commerce-Konfigurationsdateien gelöscht.
