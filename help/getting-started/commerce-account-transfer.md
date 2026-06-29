---
title: Übertragen eines Adobe Commerce-Kontos
description: Erfahren Sie, wie Sie ein Adobe Commerce-Konto an einen neuen Eigentümer oder eine neue E-Mail-Adresse übertragen, den richtigen Übertragungstyp auswählen, E-Mail-Änderungen überprüfen und sich an den Support wenden.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
TQID: https://experienceleague.adobe.com/CIyzus4f8WcBH-jW9R1nCL-gkl065DLTHbjNn0K6e7E
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
source-git-commit: e01cba363eb149286479718e660f8cdf6526e826
workflow-type: tm+mt
source-wordcount: 1553
ht-degree: 0%

---

# Übertragen eines Adobe Commerce-Kontos

Wenn sich die geschäftlichen Zuständigkeiten ändern, müssen Sie möglicherweise Ihr Adobe Commerce-Konto an einen neuen Eigentümer oder an eine andere E-Mail-Adresse übertragen. Diese Übertragung erfordert eine Änderung der mit dem Konto verknüpften E-Mail-Adresse des primären Benutzers.

Die folgenden Informationen beschreiben den Prozess zur Übertragung eines Adobe Commerce-Accounts (MAGEID). Sie umfasst keine Änderungen an Adobe Commerce in Bezug auf die Eigentümerschaft an Cloud-Infrastrukturprojekten oder die [!DNL New Relic]. Weitere Informationen zum Zugriff auf Cloud-Projekte finden Sie unter [Verwalten des Benutzerzugriffs](https://experienceleague.adobe.com/de/docs/commerce-cloud-service/user-guide/project/user-access) im Handbuch _Commerce in Cloud-Infrastruktur_.

>[!IMPORTANT]
>
>Wenn der neue Kontoinhaber mithilfe von Shared Access Erweiterungen erworben hat, geht der Zugriff auf diese Erweiterungen verloren, sobald die Kontoübertragung beginnt.
>
>Bevor Sie die Kontoübertragung anfordern, stellen Sie sicher, dass der neue Eigentümer die Bestell-IDs für die Käufe von [&#x200B; [!DNL Commerce Marketplace] Konto](https://commercemarketplace.adobe.com/sales/order/history/) abruft und eine Rückerstattung vom [[!DNL Commerce Marketplace] Team](https://experienceleague.adobe.com/de/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) anfordert. Erweiterungskäufe können nicht auf ein anderes Konto übertragen werden.

## Art der Übertragung angeben

Der geeignete Adobe Commerce-Kontoübertragungsprozess hängt vom Kontostatus des aktuellen Inhabers und des neuen Inhabers ab und davon, ob die E-Mail-Adresse des aktuellen Inhabers noch zugänglich ist. Wenn beispielsweise der aktuelle Eigentümer das Unternehmen verlassen hat, benötigen Sie möglicherweise weiterhin Zugriff auf E-Mails, die an diese Adresse gesendet werden.

In den folgenden Szenarien werden die verfügbaren Übertragungsoptionen anhand dieser Bedingungen beschrieben.

| Übertragungstyp | Derzeitiger Besitzer | Neuer Besitzer |
| ------------- | ------------- | --------- |
| [Neue Adobe ID- und E-Mail-Änderung](#new-adobe-id-and-email-change) | Hat eine MAGEID, die nicht mit einer Adobe ID verbunden wurde | Hat keine MAGEID und keine Adobe ID. |
| [Nur E-Mail-Änderung](#email-change) | Hat eine MAGEID, die mit einer Adobe ID verbunden ist. | Hat eine Adobe ID, aber keine mit dem Account verbundene MAGEID. |
| [Adobe ID-Kontowechsel](#adobe-id-account-switch) | Hat eine MAGEID, die mit einer Adobe ID verbunden ist. | Hat eine MAGEID und ist mit einer Adobe ID verbunden. |

{style="table-layout:auto"}

>[!NOTE]
>
>Da Adobe Commerce weiterhin mit anderen Adobe-Lösungen integriert wird, ist für ein Adobe Commerce-Konto (MAGEID) jetzt eine Verknüpfung mit einer Adobe ID erforderlich. Der Adobe ID verwendet dieselbe E-Mail-Adresse, die mit Ihrem [Adobe Commerce-Konto verbunden &#x200B;](https://experienceleague.adobe.com/de/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).

## Überprüfen einer Adobe ID-E-Mail-Änderung

Mehrere Übertragungspfade verwenden denselben Verifizierungs-Workflow auf [account.adobe.com](https://account.adobe.com/). Nachdem Sie die Ziel-E-Mail-Adresse eingegeben und auf **[!UICONTROL Change]** geklickt haben, führen Sie die folgenden Schritte aus:

1. Öffnen Sie die Bestätigungs-E-Mail an die eingegebene Adresse und suchen Sie den Bestätigungscode.

1. Geben Sie den Bestätigungscode ein.

1. Klicken Sie auf **[!UICONTROL Verify]**.

## Neue Adobe ID- und E-Mail-Änderung

>[!IMPORTANT]
>
>Überprüfen Sie die [Übertragungstypen](#identify-your-transfer-type) und bestätigen Sie, dass dieser Pfad Ihrer Situation entspricht:
>
>- Der aktuelle Besitzer ist immer noch bei der Firma.
>- Der aktuelle Besitzer hat entweder keine Adobe ID oder eine Adobe ID, die nicht mit seinem [Adobe Commerce-Konto (MAGEID) verbunden ist](https://experienceleague.adobe.com/de/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- Der neue Besitzer hat keine Adobe ID und kein Adobe Commerce-Konto.

Verwenden Sie diesen Pfad, wenn der aktuelle Besitzer über eine MAGEID verfügt, die noch nicht mit einer Adobe ID verknüpft ist. Der aktuelle Eigentümer erstellt und verknüpft zunächst eine Adobe ID und ändert dann diese Adobe ID-E-Mail-Adresse in die E-Mail-Adresse des neuen Eigentümers.

1. Navigieren Sie zur Anmeldeseite des Adobe Commerce-Kontos &lbrace;0[&#128279;](https://account.magento.com/customer/account/login/).

1. Klicken Sie auf **[!UICONTROL Sign in with Adobe ID]**.

1. Klicken Sie auf **[!UICONTROL Create an account]**.

1. Geben Sie die E-Mail-Adresse und das Passwort des aktuellen Besitzers ein.

1. Klicken Sie auf **[!UICONTROL Continue]**.

   In diesem Schritt wird eine Adobe ID erstellt und mit dem aktuellen Adobe Commerce-Konto (MAGEID) verknüpft. Mit diesem Konto-Link wird das Feld _[!UICONTROL Email]_&#x200B;für alle Änderungen gesperrt. Die Konfiguration der zugehörigen E-Mail-Adresse wird über das Adobe ID-Konto verwaltet.

1. Navigieren Sie zu [account.adobe.com](https://account.adobe.com/).

1. Klicken Sie auf **[!UICONTROL Change Email]**.

1. Geben Sie die E-Mail-Adresse des neuen Besitzers ein.

   Wenn die neue E-Mail-Adresse bereits mit einem anderen Konto im System verknüpft ist, kann sie nicht direkt für die Übertragung verwendet werden. Folgen Sie stattdessen dem Pfad des [Adobe ID](#adobe-id-account-switch)Kontowechsels und verwenden Sie eine [temporäre E-Mail-Adresse](#change-to-a-temporary-account).

1. Führen Sie die [E-Mail-Verifizierungsschritte](#verify-an-adobe-id-email-change) aus.

Nachdem der neue Eigentümer die E-Mail-Adresse überprüft hat, fahren Sie mit [Letzte Schritte](#final-steps) fort, damit der Adobe Commerce-Support Kontodatensätze wie das [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/) aktualisieren kann.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on){transcript=true}

## Nur E-Mail-Änderung {#email-change}

>[!IMPORTANT]
>
>Überprüfen Sie die [Übertragungstypen](#identify-your-transfer-type) und bestätigen Sie, dass dieser Pfad Ihrer Situation entspricht:
>
>- Der aktuelle Besitzer ist immer noch bei der Firma.
>- Der aktuelle Besitzer hat eine Adobe ID, die mit seinem [Adobe Commerce-Konto (MAGEID) verbunden ist](https://experienceleague.adobe.com/de/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- Der neue Besitzer hat einen Adobe ID, der nicht mit einem Adobe Commerce-Konto verbunden ist.

Bevor Sie beginnen, beachten Sie, dass dieser Übertragungstyp dazu führt, dass der aktuelle Kontoinhaber den Zugriff auf andere Adobe-Produkte verliert, die mit dieser Adobe ID verknüpft sind.

1. Navigieren Sie zu [account.adobe.com](https://account.adobe.com/) und melden Sie sich bei Adobe an.

1. Klicken Sie unter Ihrem Kontonamen und Avatar auf **[!UICONTROL Change Email]**.

1. Geben Sie im Dialogfeld die E-Mail-Adresse des neuen Besitzers ein.

   Wenn die neue E-Mail-Adresse bereits mit einem anderen Konto im System verknüpft ist, kann sie nicht direkt für die Übertragung verwendet werden. Folgen Sie stattdessen dem Pfad des [Adobe ID](#adobe-id-account-switch)Kontowechsels und verwenden Sie eine [temporäre E-Mail-Adresse](#change-to-a-temporary-account).

1. Führen Sie die [E-Mail-Verifizierungsschritte](#verify-an-adobe-id-email-change) aus.

Nachdem der neue Eigentümer die E-Mail-Adresse überprüft hat, fahren Sie mit [Letzte Schritte](#final-steps) fort, damit der Adobe Commerce-Support Kontodatensätze wie das [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/) aktualisieren kann.

## Adobe ID-Kontowechsel

>[!IMPORTANT]
>
>Überprüfen Sie die [Übertragungstypen](#identify-your-transfer-type) und bestätigen Sie, dass dieser Pfad Ihrer Situation entspricht:
>
>- Der aktuelle Eigentümer ist nicht mehr mit dem Unternehmen verbunden, aber E-Mails, die an die E-Mail-Adresse des aktuellen Eigentümers gesendet werden, sind weiterhin zugänglich, oder Ihr IT-Team kann diese E-Mails an einen autorisierten Kontakt weiterleiten.
>- Der aktuelle Besitzer hat eine Adobe ID, die mit seinem [Adobe Commerce-Konto (MAGEID) verbunden ist](https://experienceleague.adobe.com/de/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- Der neue Eigentümer verfügt über eine Adobe ID, die mit seinem Adobe Commerce-Konto verbunden ist.

Dieser Übertragungstyp verwendet eine temporäre E-Mail-Adresse, um den Kontoeigentümer zu wechseln, wenn sowohl der aktuelle als auch der neue Eigentümer über vorhandene Adobe-IDs verfügen und Sie beide Adobe-IDs beibehalten möchten. Um die Übertragung der Verantwortung abzuschließen, müssen Sie eine temporäre E-Mail-Adresse verwenden, die nicht mit einer Adobe ID verknüpft ist.

### Wechsel zu einem temporären Konto

Führen Sie diese Schritte aus, um die Adobe ID des aktuellen Besitzers mit einer temporären E-Mail-Adresse zu verknüpfen. Sie müssen Zugriff auf diese E-Mail-Adresse haben, damit Sie den Bestätigungscode abrufen können.

>[!NOTE]
>
>Wenn Sie nicht auf die E-Mail-Adresse des aktuellen Besitzers zugreifen können, bitten Sie Ihr IT-Team, die E-Mail-Weiterleitung für die E-Mail-Adresse des Kontos in Ihrem E-Mail-System des Unternehmens einzurichten. Wenn die E-Mail-Weiterleitung nicht konfiguriert werden kann, stellen Sie sicher, dass der neue Kontoinhaber über eine Adobe ID verfügt, und [senden Sie dann eine Support-Anfrage](https://experienceleague.adobe.com/de/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) mit allen erforderlichen Details, um die Kontoübertragung einzuleiten.

1. Navigieren Sie zu [account.adobe.com](https://account.adobe.com/) und melden Sie sich bei Adobe an.

1. Klicken Sie unter Ihrem Kontonamen und Avatar auf **[!UICONTROL Change Email]**.

1. Geben Sie im Dialogfeld eine gültige temporäre E-Mail-Adresse ein, die nicht von einer Adobe ID verwendet wird.

1. Führen Sie die [E-Mail-Verifizierungsschritte](#verify-an-adobe-id-email-change) aus.

1. Melden Sie sich beim Adobe-Konto ab.

### Schritte für neuen Verantwortlichen

Nachdem der aktuelle Inhaber die Übertragung an eine temporäre E-Mail-Adresse abgeschlossen hat, muss der neue Inhaber diese Schritte ausführen, um seine Adobe ID-E-Mail-Adresse in die ursprüngliche E-Mail-Adresse des aktuellen Inhabers zu ändern.

1. Navigieren Sie zu [account.adobe.com](https://account.adobe.com/) und melden Sie sich bei Adobe an.

1. Klicken Sie unter Ihrem Kontonamen und Avatar auf **[!UICONTROL Change Email]**.

1. Geben Sie im Dialogfeld die ursprüngliche E-Mail-Adresse des aktuellen Besitzers ein.

1. Führen Sie die [E-Mail-Verifizierungsschritte](#verify-an-adobe-id-email-change) aus.

1. Melden Sie sich beim Adobe-Konto ab.

### Folgeschritte

Nachdem der neue Eigentümer seine Adobe ID erfolgreich mit der ursprünglichen E-Mail-Adresse des aktuellen Eigentümers konfiguriert hat, führen Sie diese Schritte aus, um diese E-Mail-Adresse dem neuen Eigentümer zuzuweisen.

1. Navigieren Sie zu [account.adobe.com](https://account.adobe.com/) und füllen Sie die Adobe-Anmeldung mit der E-Mail-Adresse für das [temporäre Konto](#change-to-a-temporary-account) aus.

1. Klicken Sie unter dem Kontonamen und Avatar auf **[!UICONTROL Change Email]**.

1. Geben Sie im Dialogfeld die E-Mail-Adresse des neuen Besitzers ein.

1. Führen Sie die [E-Mail-Verifizierungsschritte](#verify-an-adobe-id-email-change) aus.

Nachdem der neue Eigentümer die E-Mail-Adresse überprüft hat, fahren Sie mit [Letzte Schritte](#final-steps) fort, damit der Adobe Commerce-Support Kontodatensätze wie das [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/) aktualisieren kann.

## Letzte Schritte

Führen Sie diese Schritte nach Abschluss des Prozesses [Neue Adobe ID- und E](#new-adobe-id-and-email-change)Mail-Änderung[, Nur E-Mail-Änderung](#email-change) oder [Wechsel des Adobe ID-](#adobe-id-account-switch) aus.

1. Als neuer Eigentümer [&#x200B; Sie (eine Support-Anfrage einreichen](https://experienceleague.adobe.com/de/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case).

   Fügen Sie die folgenden Details hinzu:

   - Die E-Mail-Adresse des früheren Kontoinhabers
   - Die E-Mail-Adresse des neuen Inhabers
   - Hinweis, dass Sie die Adobe Commerce-Kontoübertragung abgeschlossen und die Adobe ID-E-Mail-Adresse aktualisiert haben

1. Warten Sie, bis der Adobe Commerce-Support die Aktualisierung bestätigt.

   Der Support aktualisiert auch zugehörige Datensätze, wie die E-Mail-Adresse in Ihrem [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

Nachdem der Support die Anfrage abgeschlossen hat, kann sich der neue Eigentümer mit seinem Adobe ID beim Adobe Commerce-Konto anmelden. Die MAGEID bleibt die Berechtigungskennung für das Konto.
