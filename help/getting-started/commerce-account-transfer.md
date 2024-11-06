---
title: Übertragen eines Commerce-Kontos
description: Erfahren Sie, wie Sie Ihr Commerce-Konto an einen anderen Eigentümer oder eine andere E-Mail-Adresse übertragen können.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: 00994f506056bf5504df758a44a7cd56f590750d
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 0%

---

# Übertragen eines Commerce-Kontos

Wenn sich die Verantwortlichkeiten der Unternehmen ändern, müssen Sie möglicherweise das Eigentum an Ihrem bestehenden Commerce-Konto an einen neuen Eigentümer oder an eine andere E-Mail-Adresse übertragen. Diese Übertragung erfordert eine Änderung der primären Benutzer-E-Mail, die mit dem Konto verknüpft ist.

Die folgenden Informationen beschreiben die Übertragung eines Commerce-Kontos (MAGEID). Es enthält keine Änderungen für das Eigentum an Cloud-Konten (Cloud-Projekt oder New Relic). Weitere Informationen zum Zugriff auf Cloud-Projekte finden Sie unter [Verwalten des Benutzerzugriffs](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) im _Commerce on Cloud Infrastructure Guide_.

## Transfertyp identifizieren

Wie Sie diese Übertragung durchführen, hängt davon ab, in welchen der folgenden Szenarien Ihre Situation als aktueller Kontoinhaber und neuer Eigentümer (E-Mail-Adresse) beschrieben wird, an den Sie das Konto übertragen möchten:

| Transfertyp | Aktueller Eigentümer | Neuer Eigentümer |
| ------------- | ------------- | --------- |
| [Neue Adobe ID- und E-Mail-Änderung](#new-adobe-id-and-email-change) | Hat eine MAGEID, die **_nicht mit_** mit einem Adobe-Anmeldekonto verbunden ist. | Hat keine MAGEID und ist nicht mit einem Adobe-Anmeldekonto verbunden. |
| [E-Mail-Änderung](#email-change) | Hat eine MAGEID, die **_verbunden_** ist, mit einem Adobe-Anmeldekonto ohne andere Adobe-Produkte/-Dienste. | Hat keine MAGEID und ist nicht mit einem Adobe-Anmeldekonto verbunden. |
| [Adobe ID-Switch](#adobe-id-account-switch) | Hat eine MAGEID, die **_verbunden_** ist, mit einem Adobe-Anmeldekonto ohne andere Adobe-Produkte/-Dienste. | Hat eine MAGEID und ist mit einem Adobe-Login-Konto verbunden, ohne dass andere Adobe-Produkte/Dienstleistungen zugeordnet sind. |

{style="table-layout:auto"}

>[!NOTE]
>
>Da Adobe Commerce weiterhin mit anderen Adobe-Lösungen integriert wird, erfordert ein Commerce-Konto (MAGEID) jetzt eine Verknüpfung mit einer Adobe-Anmeldung. Diese Adobe ID verwendet dieselbe E-Mail-Adresse, die mit Ihrem Commerce-Konto verbunden ist.

## Neue Adobe ID- und E-Mail-Änderung

>[!IMPORTANT]
>
>Überprüfen Sie die [Transfertypen](#identify-your-transfer-type) und stellen Sie sicher, dass Sie die Voraussetzungen für diese Schrittfolge erfüllen.

Für diesen Transfertyp müssen Sie zunächst einen zugehörigen Adobe ID erstellen und dieses Konto dann in die E-Mail-Adresse des neuen Eigentümers ändern.

1. Rufen Sie Ihr [Commerce-Konto](https://account.magento.com/customer/account/login/) auf.

1. Klicken Sie auf **[!UICONTROL Sign in with Adobe ID]**.

1. Klicken Sie auf **[!UICONTROL Create an account]**.

1. Geben Sie die E-Mail-Adresse des aktuellen Eigentümers und ein Kennwort ein.

1. Klicken Sie auf **[!UICONTROL Continue]**.

   Dadurch wird eine Adobe ID erstellt und mit dem aktuellen Commerce-Konto (MAGEID) verknüpft. Mit diesem Konto-Link wird das Feld _[!UICONTROL Email]_für alle Änderungen blockiert. Die zugehörige E-Mail-Adresse wird vom Adobe ID-Konto verwaltet.

1. Navigieren Sie zu [account.adobe.com](https://account.adobe.com/).

1. Klicken Sie auf **[!UICONTROL Change Email]**.

1. Geben Sie die E-Mail-Adresse des neuen Eigentümers ein.

1. Klicken Sie auf **[!UICONTROL Change]**.

   Dadurch wird eine Verifizierungs-E-Mail an die neue E-Mail-Adresse gesendet. Die E-Mail enthält einen Bestätigungscode, der zum Abschließen der Änderung der E-Mail-Adresse erforderlich ist.

1. Geben Sie den Bestätigungscode ein, der an die neue E-Mail-Adresse gesendet wird.

1. Klicken Sie auf **[!UICONTROL Verify]**.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## Email change

>[!IMPORTANT]
>
>Überprüfen Sie die [Transfertypen](#identify-your-transfer-type) und stellen Sie sicher, dass Sie die Voraussetzungen für diese Schrittfolge erfüllen.

1. Navigieren Sie zu [account.adobe.com](https://account.adobe.com/) und schließen Sie die Adobe-Anmeldung ab.

1. Klicken Sie unter Ihrem Kontonamen und Avatar auf **[!UICONTROL Change Email]**.

1. Geben Sie im Dialogfeld die E-Mail-Adresse des neuen Eigentümers ein.

1. Klicken Sie auf **[!UICONTROL Change]**.

   Dadurch wird eine Verifizierungs-E-Mail an die neue E-Mail-Adresse gesendet. Die E-Mail enthält einen Bestätigungscode, der zum Abschließen der Änderung der E-Mail-Adresse erforderlich ist.

1. Geben Sie den Bestätigungscode ein, der an die neue E-Mail-Adresse gesendet wird.

1. Klicken Sie auf **[!UICONTROL Verify]**.

## Adobe ID-Kontowechsel

>[!IMPORTANT]
>
>Überprüfen Sie die [Transfertypen](#identify-your-transfer-type) und stellen Sie sicher, dass Sie die Voraussetzungen für diese Schrittfolge erfüllen.

Wenn der aktuelle Eigentümer und der neue Eigentümer über vorhandene Adobe-IDs verfügen, sollten beide Konten beibehalten werden, E-Mail-Adressen müssen jedoch zwischen ihnen umgeschaltet werden. Dies erfordert die Verwendung einer _temporären_ E-Mail-Adresse, die gültig ist, aber nicht mit und Adobe ID verknüpft ist.

### Änderung an einem temporären Konto

Der aktuelle Eigentümer führt diese Schritte aus, um seinen Adobe ID mit einer anderen temporären E-Mail-Adresse zu verknüpfen.

1. Navigieren Sie zu [account.adobe.com](https://account.adobe.com/) und schließen Sie die Adobe-Anmeldung ab.

1. Klicken Sie unter Ihrem Kontonamen und Avatar auf **[!UICONTROL Change Email]**.

1. Geben Sie im Dialogfeld eine gültige temporäre E-Mail-Adresse ein, die von einer Adobe ID nicht verwendet wird.

   Sie müssen Zugriff auf die E-Mail-Adresse haben, damit Sie die E-Mail mit dem Bestätigungscode abrufen können.

1. Klicken Sie auf **[!UICONTROL Change]**.

   Dadurch wird eine Verifizierungs-E-Mail an die temporäre E-Mail-Adresse gesendet. Die E-Mail enthält einen Bestätigungscode, der zum Abschließen der Änderung der E-Mail-Adresse erforderlich ist.

1. Geben Sie den Bestätigungscode ein, der an die temporäre E-Mail-Adresse gesendet wird.

1. Klicken Sie auf **[!UICONTROL Verify]**.

1. Melden Sie sich vom Adobe-Konto ab.

### Neue Eigentümerschritte

Nachdem der aktuelle Eigentümer die Übertragung an eine temporäre E-Mail-Adresse abgeschlossen hat, führen Sie diese Schritte aus, um Ihr Konto auf den aktuellen Eigentümer zu ändern.

1. Navigieren Sie zu [account.adobe.com](https://account.adobe.com/) und schließen Sie die Adobe-Anmeldung ab.

1. Klicken Sie unter Ihrem Kontonamen und Avatar auf **[!UICONTROL Change Email]**.

1. Geben Sie im Dialogfeld die ursprüngliche E-Mail-Adresse des aktuellen Eigentümers ein.

1. Klicken Sie auf **[!UICONTROL Change]**.

   Dadurch wird eine Verifizierungs-E-Mail an diese E-Mail-Adresse gesendet. Die E-Mail enthält einen Bestätigungscode, der zum Abschließen der Änderung der E-Mail-Adresse erforderlich ist.

1. Geben Sie den Bestätigungscode ein, der an den aktuellen Eigentümer gesendet wird.

1. Klicken Sie auf **[!UICONTROL Verify]**.

1. Melden Sie sich vom Adobe-Konto ab.

### Schritte im Anschluss

Nachdem der neue Eigentümer sein Adobe-Konto erfolgreich an den aktuellen (jetzt vorherigen) Eigentümer übertragen hat, führen Sie diese Schritte aus, um das Eigentum zu übertragen.

1. Navigieren Sie zu [account.adobe.com](https://account.adobe.com/) (erstes Konto, das in der Schrittfolge verwendet wurde) und schließen Sie die Adobe-Anmeldung ab.

   Diese Anmeldung erfordert die Verwendung der temporären E-Mail-Adresse.

1. Klicken Sie unter dem Kontonamen und dem Avatar auf **[!UICONTROL Change Email]**.

1. Geben Sie im Dialogfeld die E-Mail-Adresse des neuen Eigentümers ein.

1. Klicken Sie auf **[!UICONTROL Change]**.

   Dadurch wird eine Verifizierungs-E-Mail an diese E-Mail-Adresse gesendet. Die E-Mail enthält einen Bestätigungscode, der zum Abschließen der Änderung der E-Mail-Adresse erforderlich ist.

1. Geben Sie den Bestätigungscode ein, der an den neuen Eigentümer gesendet wird.

1. Klicken Sie auf **[!UICONTROL Verify]**.

1. **Senden Sie eine Support-Anfrage** , um das Supportteam darüber zu informieren, dass Sie die E-Mail-Adresse des Kontoinhabers aktualisiert haben. Fügen Sie die E-Mail-Adresse des früheren Kontoinhabers in Ihre Anfrage ein.

Der Support muss weitere Schritte durchführen, z. B. die Aktualisierung der E-Mail-Adresse in Ihrem [Commerce Marketplace](https://commercemarketplace.adobe.com/) -Profil.
