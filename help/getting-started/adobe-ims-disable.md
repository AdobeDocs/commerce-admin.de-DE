---
title: Deaktivieren der Commerce Admin-Integration mit Adobe ID
description: Befolgen Sie dieses optionale Verfahren zur Deaktivierung der Adobe Commerce Admin-Integration mit Adobe IMS.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
source-git-commit: 53c3b6c9fa9c152e6619528a43580b0acc71a2a5
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Deaktivieren der Commerce Admin-Integration mit Adobe ID

{{ee-feature}}

Händler, die ihre Commerce-Instanz mit dem Adobe IMS-Authentifizierungs-Workflow integriert haben, müssen diese optionale Integration möglicherweise deaktivieren.

Commerce-Bereitstellungen werden auf den standardmäßigen Commerce-Authentifizierungs-Workflow und die standardmäßigen Kennwortrichtlinien zurückgesetzt, nachdem die IMS-Integration deaktiviert wurde. Wenn diese Integration aktiviert oder deaktiviert ist, sind nur Workflows für Admin-Benutzer betroffen.

Unter [Ihr Administratorkonto](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html?lang=de) finden Sie einen Überblick über die Commerce Admin-Anmeldung.

## Schritt 1: Integration deaktivieren

Sie können diese Integration nicht über den Administrator deaktivieren. Um die Adobe IMS-Integration mit Commerce zu deaktivieren und die Commerce-Authentifizierung wieder in den Standardzustand zu versetzen, müssen Sie die Integration über die Befehlszeilenschnittstelle deaktivieren.

So deaktivieren Sie die Integration:

```bash
bin/magento admin:adobe-ims:disable
```

Bei erfolgreicher Ausführung zeigt Adobe Commerce die folgende Meldung an:

```
Admin Adobe IMS integration is disabled.
```

## Schritt 2: Commerce-Kennwort erstellen oder abrufen

Nach der Deaktivierung der Integration müssen sich Admin-Benutzer mit einem Commerce-Kennwort bei Admin anmelden.

* Commerce-Admin-Benutzende, die sich an ihr bereits vorhandenes Commerce-Kennwort erinnern (d. h. ein Commerce-Kennwort, das vor der IMS-Integration erstellt wurde), können es verwenden, um sich beim Admin anzumelden.

* Commerce-Admin-Benutzende, die entweder kein bereits vorhandenes Commerce-Kennwort haben oder es vergessen haben, müssen ein neues Kennwort erstellen. Um ein neues Kennwort zu erstellen, können Admin-Benutzer die [!UICONTROL Forgot your password?] Funktion auf der Commerce-Anmeldeseite verwenden, um ein neues Kennwort zu erstellen. Siehe [Zurücksetzen von Kundenkennwörtern](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html?lang=de). Commerce akzeptiert kein leeres Kennwortfeld.

## Nach der Deaktivierung der Integration

Der standardmäßige Commerce-Authentifizierungs-Workflow wird fortgesetzt, nachdem die IMS-Integration deaktiviert wurde und Admin-Benutzer erneut zur Eingabe ihres Kennworts aufgefordert werden.

Durch Deaktivieren der IMS-Integration werden die Anmeldeinformationen, die eingegeben wurden, als die Integration aktiviert wurde (`Organization ID`-, `Client ID`- und `Client Secret`), aus den Commerce-Konfigurationsdateien gelöscht.
