---
title: Deaktivieren der Commerce Admin-Integration mit Adobe ID
description: Befolgen Sie dieses optionale Verfahren zur Deaktivierung der Adobe Commerce Admin-Integration mit Adobe IMS.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/KL6Cx3ymElo7ROx5SUJtlqtKivnw7-heqPWGksGP-pg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 351
ht-degree: 0%

---

# Deaktivieren der Commerce Admin-Integration mit Adobe ID

{{ee-feature}}

Händler, die ihre Commerce-Instanz mit dem Adobe IMS-Authentifizierungs-Workflow integriert haben, müssen diese optionale Integration möglicherweise deaktivieren.

Commerce-Bereitstellungen werden auf den standardmäßigen Commerce-Authentifizierungs-Workflow und die standardmäßigen Kennwortrichtlinien zurückgesetzt, nachdem die IMS-Integration deaktiviert wurde. Wenn diese Integration aktiviert oder deaktiviert ist, sind nur Workflows für Admin-Benutzer betroffen.

Unter [Ihr Administratorkonto](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html) finden Sie einen Überblick über die Commerce Admin-Anmeldung.

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

* Commerce-Admin-Benutzende, die entweder kein bereits vorhandenes Commerce-Kennwort haben oder es vergessen haben, müssen ein neues Kennwort erstellen. Um ein neues Kennwort zu erstellen, können Admin-Benutzer die [!UICONTROL Forgot your password?] Funktion auf der Commerce-Anmeldeseite verwenden, um ein neues Kennwort zu erstellen. Siehe [Zurücksetzen von Kundenkennwörtern](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html). Commerce akzeptiert kein leeres Kennwortfeld.

## Nach der Deaktivierung der Integration

Der standardmäßige Commerce-Authentifizierungs-Workflow wird fortgesetzt, nachdem die IMS-Integration deaktiviert wurde und Admin-Benutzer erneut zur Eingabe ihres Kennworts aufgefordert werden.

Durch Deaktivieren der IMS-Integration werden die Anmeldeinformationen, die eingegeben wurden, als die Integration aktiviert wurde (`Organization ID`-, `Client ID`- und `Client Secret`), aus den Commerce-Konfigurationsdateien gelöscht.
