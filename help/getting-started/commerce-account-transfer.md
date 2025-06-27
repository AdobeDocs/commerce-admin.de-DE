---
title: Übertragen eines Commerce-Kontos
description: Erfahren Sie, wie Sie Ihr Commerce-Konto an einen anderen Eigentümer oder eine andere E-Mail-Adresse übertragen.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: e44ebfab5b9505098405b005051f110b689c3f4f
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 0%

---

# Übertragen eines Commerce-Kontos

Wenn sich die geschäftlichen Zuständigkeiten ändern, müssen Sie möglicherweise Ihr Commerce-Konto an einen neuen Eigentümer oder an eine andere E-Mail-Adresse übertragen. Diese Übertragung erfordert eine Änderung der mit dem Konto verknüpften E-Mail-Adresse des primären Benutzers.

Die folgenden Informationen beschreiben den Prozess zur Übertragung eines Commerce-Kontos (MAGEID). Sie enthält keine Änderungen für die Eigentümerschaft des Cloud-Kontos (Cloud-Projekt oder New Relic). Weitere Informationen zum Zugriff auf Cloud-Projekte finden Sie unter [Verwalten des Benutzerzugriffs](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) im Handbuch _Commerce in Cloud-Infrastruktur_.

>[!IMPORTANT]
>
>Wenn der neue Kontoinhaber Erweiterungen mithilfe von Shared Access erworben hat, geht der Zugriff auf diese Erweiterungen verloren, sobald der Prozess zur Kontoübertragung gestartet wurde. Bevor Sie die Kontoübertragung anfordern, stellen Sie sicher, dass der neue Eigentümer die Bestell-IDs für die Käufe von [seinem Marketplace-Konto](https://commercemarketplace.adobe.com/sales/order/history/) abruft und eine Erstattung für diese Erweiterungen vom [Marketplace-Team](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) anfordert. Es ist nicht möglich, Erweiterungskäufe auf ein anderes Konto zu übertragen.

## Art der Übertragung angeben

Die Art der Commerce-Kontoübertragung hängt von den Anmeldedaten für das Commerce-Konto ab, die dem aktuellen und dem neuen Eigentümer zur Verfügung stehen. In den folgenden Szenarien werden die verschiedenen Übertragungstypen beschrieben, die auf diesen Anmeldeinformationen basieren.

| Übertragungstyp | Derzeitiger Besitzer | Neuer Besitzer |
| ------------- | ------------- | --------- |
| [Neue Adobe ID- und E-Mail-Änderung](#new-adobe-id-and-email-change) | Hat eine MAGEID, die **_nicht verbunden_** mit einem Adobe-Anmeldekonto ist. | Hat keine MAGEID und ist nicht mit einem Adobe-Anmeldekonto verbunden. |
| [E-Mail-](#email-change) | Hat eine MAGEID, **_mit_** Adobe-Anmeldekonto verbunden ist. | Hat keine MAGEID und ist nicht mit einem Adobe-Anmeldekonto verbunden. |
| [Adobe ID-Switch](#adobe-id-account-switch) | Hat eine MAGEID, **_mit_** Adobe-Anmeldekonto verbunden ist. | Hat eine MAGEID und ist mit einem Adobe-Anmeldekonto verbunden, mit dem keine anderen Adobe-Produkte/-Services verbunden sind. |

{style="table-layout:auto"}

>[!NOTE]
>
>Da Adobe Commerce weiterhin mit anderen Adobe-Lösungen integriert wird, ist für ein Commerce-Konto (MAGEID) jetzt eine Verknüpfung mit einer Adobe-Anmeldung erforderlich. Diese Adobe ID verwendet dieselbe E-Mail-Adresse, die mit Ihrem Commerce-Konto verbunden ist.

## Neue Adobe ID- und E-Mail-Änderung

>[!IMPORTANT]
>
>Überprüfen Sie die [Übertragungstypen](#identify-your-transfer-type) und stellen Sie sicher, dass Sie die Voraussetzungen für diese Sequenz von Schritten erfüllen.

Dieser Übertragungstyp erfordert, dass Sie zunächst eine zugehörige Adobe ID erstellen und dieses Konto dann in die E-Mail-Adresse des neuen Eigentümers ändern.

1. Zu Ihrem [Commerce-Konto](https://account.magento.com/customer/account/login/).

1. Klicken Sie auf **[!UICONTROL Sign in with Adobe ID]**.

1. Klicken Sie auf **[!UICONTROL Create an account]**.

1. Geben Sie die E-Mail-Adresse des aktuellen Besitzers und ein Passwort ein.

1. Klicken Sie auf **[!UICONTROL Continue]**.

   In diesem Schritt wird eine Adobe ID erstellt und mit dem aktuellen Commerce-Konto (MAGEID) verknüpft. Mit diesem Konto-Link wird das Feld _[!UICONTROL Email]_&#x200B;für alle Änderungen gesperrt. Die Konfiguration der zugehörigen E-Mail-Adresse wird über das Adobe ID-Konto verwaltet.

1. Navigieren Sie zu [account.adobe.com](https://account.adobe.com/).

1. Klicken Sie auf **[!UICONTROL Change Email]**.

1. Geben Sie die E-Mail-Adresse des neuen Besitzers ein.

1. Klicken Sie auf **[!UICONTROL Change]**.

   Dieser Schritt generiert eine Bestätigungs-E-Mail, die an die neue E-Mail-Adresse gesendet wird. Die E-Mail enthält einen Bestätigungs-Code, der zum Abschließen der E-Mail-Adressänderung erforderlich ist.

1. Geben Sie den Bestätigungscode ein, der an die neue E-Mail-Adresse gesendet wurde.

1. Klicken Sie auf **[!UICONTROL Verify]**.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## E-Mail-Änderung

>[!IMPORTANT]
>
>Überprüfen Sie die [Übertragungstypen](#identify-your-transfer-type) und stellen Sie sicher, dass Sie die Voraussetzungen für diese Sequenz von Schritten erfüllen.

1. Navigieren Sie zu [account.adobe.com](https://account.adobe.com/) und melden Sie sich bei Adobe an.

1. Klicken Sie unter Ihrem Kontonamen und Avatar auf **[!UICONTROL Change Email]**.

1. Geben Sie im Dialogfeld die E-Mail-Adresse des neuen Besitzers ein.

1. Klicken Sie auf **[!UICONTROL Change]**.

   Dieser Schritt generiert eine Bestätigungs-E-Mail, die an die neue E-Mail-Adresse gesendet wird. Die E-Mail enthält einen Bestätigungs-Code, der zum Abschließen der E-Mail-Adressänderung erforderlich ist.

1. Geben Sie den Bestätigungscode ein, der an die neue E-Mail-Adresse gesendet wurde.

1. Klicken Sie auf **[!UICONTROL Verify]**.

## Adobe ID-Kontowechsel

>[!IMPORTANT]
>
>Überprüfen Sie die [Übertragungstypen](#identify-your-transfer-type) und stellen Sie sicher, dass Sie die Voraussetzungen für diese Sequenz von Schritten erfüllen.

Wenn sowohl der aktuelle als auch der neue Eigentümer bereits über Adobe-IDs verfügen, sollten beide Konten bestehen bleiben, aber die E-Mail-Adressen müssen zwischen ihnen gewechselt werden. Dies erfordert die Verwendung einer _temporären_ E-Mail-Adresse, die gültig ist, aber nicht mit einer Adobe ID verknüpft ist.

### Wechsel zu einem temporären Konto

Der aktuelle Inhaber führt diese Schritte aus, um seine Adobe ID mit einer anderen, temporären E-Mail-Adresse zu verknüpfen.

1. Navigieren Sie zu [account.adobe.com](https://account.adobe.com/) und melden Sie sich bei Adobe an.

1. Klicken Sie unter Ihrem Kontonamen und Avatar auf **[!UICONTROL Change Email]**.

1. Geben Sie im Dialogfeld eine gültige temporäre E-Mail-Adresse ein, die nicht von einer Adobe ID verwendet wird.

   Sie müssen Zugriff auf die E-Mail-Adresse haben, damit Sie die E-Mail mit dem Bestätigungscode abrufen können.

1. Klicken Sie auf **[!UICONTROL Change]**.

   Dieser Schritt generiert eine Bestätigungs-E-Mail, die an die temporäre E-Mail-Adresse gesendet wird. Die E-Mail enthält einen Bestätigungs-Code, der zum Abschließen der E-Mail-Adressänderung erforderlich ist.

1. Geben Sie den Bestätigungscode ein, der an die temporäre E-Mail-Adresse gesendet wurde.

1. Klicken Sie auf **[!UICONTROL Verify]**.

1. Melden Sie sich beim Adobe-Konto ab.

### Schritte für neuen Verantwortlichen

Nachdem der aktuelle Inhaber die Übertragung an eine temporäre E-Mail-Adresse abgeschlossen hat, muss der neue Inhaber diese Schritte ausführen, um seine Kontokonfiguration so zu ändern, dass sie auf die ursprüngliche E-Mail-Adresse des aktuellen Inhabers verweist.

1. Navigieren Sie zu [account.adobe.com](https://account.adobe.com/) und melden Sie sich bei Adobe an.

1. Klicken Sie unter Ihrem Kontonamen und Avatar auf **[!UICONTROL Change Email]**.

1. Geben Sie im Dialogfeld die ursprüngliche E-Mail-Adresse des aktuellen Besitzers ein.

1. Klicken Sie auf **[!UICONTROL Change]**.

   Dieser Schritt generiert eine Bestätigungs-E-Mail, die an die ursprüngliche E-Mail-Adresse des aktuellen Besitzers gesendet wird. Die E-Mail enthält einen Bestätigungs-Code, der zum Abschließen der E-Mail-Adressänderung erforderlich ist.

1. Geben Sie den Bestätigungscode ein, der an die ursprüngliche E-Mail-Adresse des aktuellen Besitzers gesendet wurde.

1. Klicken Sie auf **[!UICONTROL Verify]**.

1. Melden Sie sich beim Adobe-Konto ab.

### Folgeschritte

Nachdem der neue Besitzer sein Adobe-Konto erfolgreich mit der ursprünglichen E-Mail-Adresse des aktuellen (jetzt vorherigen) Besitzers konfiguriert hat, führen Sie diese Schritte aus, um den Besitz zu übertragen.

1. Navigieren Sie zu [account.adobe.com](https://account.adobe.com/) und füllen Sie die Adobe-Anmeldung mit der E-Mail-Adresse für das [temporäre Konto](#change-to-a-temporary-account) aus.

1. Klicken Sie unter dem Kontonamen und Avatar auf **[!UICONTROL Change Email]**.

1. Geben Sie im Dialogfeld die E-Mail-Adresse des neuen Besitzers ein.

1. Klicken Sie auf **[!UICONTROL Change]**.

   Dieser Schritt generiert eine Bestätigungs-E-Mail, die an die E-Mail-Adresse des neuen Besitzers gesendet wird. Die E-Mail enthält einen Bestätigungs-Code, der zum Abschließen der E-Mail-Adressänderung erforderlich ist.

1. Geben Sie den Bestätigungscode ein, der an die E-Mail-Adresse des neuen Besitzers gesendet wurde.

1. Klicken Sie auf **[!UICONTROL Verify]**.

>[!IMPORTANT]
>
>Senden Sie eine Support-Anfrage , um das Support-Team darüber zu informieren, dass Sie die E-Mail-Adresse des Kontoinhabers aktualisiert haben. Das Team muss zusätzliche Schritte ausführen, um die Aktualisierung abzuschließen, z. B. die E-Mail-Adresse in Ihrem [Commerce Marketplace](https://commercemarketplace.adobe.com/)-Profil aktualisieren. Fügen Sie die E-Mail-Adresse des früheren Kontoinhabers in Ihre Anfrage ein.
