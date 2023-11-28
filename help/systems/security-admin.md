---
title: Admin Security konfigurieren
description: Erfahren Sie, wie Sie die Sicherheit für Ihren Store-Administrator konfigurieren.
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
source-git-commit: e301cfaeec3a8427fff6138ba041bdbd7433c137
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# Admin Security konfigurieren

Es wird empfohlen, einen facettenreichen Ansatz zu wählen, um die Sicherheit Ihres Stores zu schützen. Sie können mit der Verwendung eines [benutzerdefinierte Admin-URL](../stores-purchase/store-urls.md#use-a-custom-admin-url) das nicht einfach zu erraten ist, anstatt das offensichtliche &quot;Admin&quot;oder &quot;Backend&quot;. Standardmäßig werden Kennwörter verwendet, um [Anmelden](../getting-started/admin-signin.md) für den Administrator muss mindestens sieben Zeichen lang sein und sowohl Buchstaben als auch Zahlen enthalten. Als [Best Practice](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html)verwenden Sie nur sichere Admin-Passwörter, die eine Kombination aus Buchstaben, Zahlen und Symbolen enthalten. Adobe Commerce und Magento Open Source lassen die Wiederverwendung der vier letzten dem Konto zugewiesenen Passwörter nicht zu.

Die Konfiguration der Admin-Sicherheit bietet Ihnen folgende Möglichkeiten:

- Einen geheimen Schlüssel zu URLs hinzufügen
- Passwörter müssen zwischen Groß- und Kleinschreibung unterscheiden
- Länge von Admin-Sitzungen begrenzen
- Lebensdauer von Kennwörtern begrenzen
- Beschränken Sie die Anzahl der Anmeldeversuche, die unternommen werden können, bevor das Admin-Benutzerkonto [locked](permissions-users-all.md#locked-users).

Um die Sicherheit zu erhöhen, können Sie die Dauer der Tastaturinaktivität konfigurieren, bevor die aktuelle Sitzung abläuft, und verlangen, dass beim Benutzernamen und Kennwort die Groß- und Kleinschreibung beachtet wird.

Zusätzlich zu den Sicherheitseinstellungen in diesem Abschnitt gilt Folgendes: [Zweifaktorauthentifizierung](security-two-factor-authentication.md) (2FA) ist erforderlich, um die Identität der Benutzer mit einem einmaligen Kennwort zu überprüfen, das von einer App oder einem Gerät generiert wird. Sie werden beim ersten Anmelden bei Admin aufgefordert, 2FA einzurichten. Für zusätzliche Sicherheit kann die Administratoranmeldung auch so konfiguriert werden, dass eine [CAPTCHA](security-captcha.md).

>[!NOTE]
>
>Stores, die aktiviert wurden [!DNL Adobe Identity Management Services] (IMS)-Authentifizierung, bei der die native Adobe Commerce und Magento Open Source 2FA deaktiviert sind. Admin-Benutzer, die mit ihren Adobe-Anmeldedaten in ihrer Commerce-Instanz angemeldet sind, müssen sich nicht für viele Admin-Aufgaben erneut authentifizieren. Die Authentifizierung wird von Adobe IMS verarbeitet, wenn sich der Administrator in seiner aktuellen Sitzung anmeldet. Siehe [[!DNL Adobe Identity Management Service] (IMS) Integrationsübersicht](../getting-started/adobe-ims-integration-overview.md).

Technische Informationen finden Sie unter [Sicherheitsübersicht](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target=&quot;_blank&quot;} in der Entwicklerdokumentation.

![Administratorsicherheit](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Admin Security konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Bereich unter _[!UICONTROL Advanced]_auswählen **[!UICONTROL Admin]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Security]** Abschnitt.

1. Um zu verhindern, dass sich Admin-Benutzer von demselben Konto auf verschiedenen Geräten aus anmelden, legen Sie **[!UICONTROL Admin Account Sharing]** nach `No`.

1. Um die Methode zu bestimmen, mit der Kennwortrücksetzanforderungen verwaltet werden, legen Sie **[!UICONTROL Password Reset Protection Type]** auf einen der folgenden Werte zu:

   - `By IP and Email` — Das Kennwort kann online zurückgesetzt werden, nachdem eine Antwort von der Benachrichtigung an die mit dem Admin-Konto verknüpfte E-Mail-Adresse gesendet wurde.
   - `By IP` — Das Passwort kann online ohne zusätzliche Bestätigung zurückgesetzt werden.
   - `By Email` — Das Kennwort kann nur zurückgesetzt werden, indem eine E-Mail-Antwort auf die Benachrichtigung gesendet wird, die an die mit dem Admin-Konto verknüpfte E-Mail-Adresse gesendet wird.
   - `None` — Das Kennwort kann nur vom Store-Administrator zurückgesetzt werden.

1. Legen Sie Anmeldesicherheitsoptionen fest:

   - Für **[!UICONTROL Recovery Link Expiration Period (hours)]** Geben Sie die Anzahl der Stunden ein, in denen ein Link zur Passwortwiederherstellung gültig bleibt.

   - Um die maximale Anzahl von Kennwortanfragen zu bestimmen, die pro Stunde gesendet werden können, geben Sie die Zahl für **[!UICONTROL Max Number of Password Reset Requests]**.

   - Für **[!UICONTROL Min Time Between Password Reset Requests]** Geben Sie die Mindestanzahl von Minuten ein, die zwischen den Anforderungen zum Zurücksetzen des Kennworts übergeben werden müssen.

   - Um einen geheimen Schlüssel an die Admin-URL anzuhängen und so eine Vorsichtsmaßnahme gegen Exploits zu treffen, legen Sie **[!UICONTROL Add Secret Key to URLs]** nach `Yes`. Diese Einstellung ist standardmäßig aktiviert.

   - Um zu verlangen, dass die Verwendung von Groß- und Kleinbuchstaben in eingegebenen Anmeldedaten mit der im System gespeicherten übereinstimmt, legen Sie **[!UICONTROL Login is Case Sensitive]** nach `Yes`.

   - Geben Sie die Dauer einer Admin-Sitzung in Sekunden an, bevor eine Zeitüberschreitung eintritt. **[!UICONTROL Admin Session Lifetime (seconds)]** -Feld. Der Wert muss mindestens 60 Sekunden betragen.

   - Für **[!UICONTROL Maximum Login Failures to Lockout Account]** eingeben, wie oft ein Benutzer versuchen kann, sich beim Administrator anzumelden, bevor das Konto gesperrt wird. Standardmäßig sind sechs Versuche zulässig. Lassen Sie das Feld für unbegrenzte Anmeldeversuche leer.

   - Für **[!UICONTROL Lockout Time (minutes)]** eingeben, geben Sie die Anzahl der Minuten ein, die ein Admin-Konto gesperrt wird, wenn die maximale Anzahl von Versuchen erreicht ist.

1. Kennwortoptionen festlegen:

   - Geben Sie zur Begrenzung der Lebensdauer von Admin-Passwörtern die Anzahl der Tage ein, für die ein Passwort gültig ist. **[!UICONTROL Password Lifetime (days)]**. Lassen Sie das Feld für eine unbegrenzte Lebensdauer leer.

   - Satz **[!UICONTROL Password Change]** auf einen der folgenden Werte zu:

      - `Forced` — Erfordert, dass Admin-Benutzer ihr Passwort nach der Kontoeinrichtung ändern.
      - `Recommended` - empfiehlt Admin-Benutzern, ihr Passwort nach der Kontoeinrichtung zu ändern.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Passwortanforderungen für Administratoren

Standardmäßig muss ein Admin-Kennwort aus sieben oder mehr Zeichen bestehen und sowohl Buchstaben als auch Zahlen enthalten.
