---
title: Admin Security konfigurieren
description: Erfahren Sie, wie Sie die Sicherheit für Ihren Store-Administrator konfigurieren.
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
source-git-commit: e301cfaeec3a8427fff6138ba041bdbd7433c137
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# Admin Security konfigurieren

Es wird empfohlen, einen facettenreichen Ansatz zu wählen, um die Sicherheit Ihres Stores zu schützen. Sie können mit einer [benutzerdefinierten Admin-URL](../stores-purchase/store-urls.md#use-a-custom-admin-url) beginnen, die nicht einfach zu erraten ist, anstatt mit dem offensichtlichen &quot;Admin&quot;oder &quot;Backend&quot;. Standardmäßig müssen Kennwörter, die für die [Anmeldung beim Administrator](../getting-started/admin-signin.md) verwendet werden, mindestens sieben Zeichen lang sein und sowohl Buchstaben als auch Zahlen enthalten. Verwenden Sie als Best Practice für [ nur sichere Admin-Passwörter, die eine Kombination aus Buchstaben, Zahlen und Symbolen enthalten. ](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) Adobe Commerce und Magento Open Source lassen die Wiederverwendung der vier letzten dem Konto zugewiesenen Passwörter nicht zu.

Die Konfiguration der Admin-Sicherheit bietet Ihnen folgende Möglichkeiten:

- Einen geheimen Schlüssel zu URLs hinzufügen
- Passwörter müssen zwischen Groß- und Kleinschreibung unterscheiden
- Länge von Admin-Sitzungen begrenzen
- Lebensdauer von Kennwörtern begrenzen
- Begrenzen Sie die Anzahl der Anmeldeversuche, die unternommen werden können, bevor das Admin-Benutzerkonto [gesperrt](permissions-users-all.md#locked-users) ist.

Um die Sicherheit zu erhöhen, können Sie die Dauer der Tastaturinaktivität konfigurieren, bevor die aktuelle Sitzung abläuft, und verlangen, dass beim Benutzernamen und Kennwort die Groß- und Kleinschreibung beachtet wird.

Zusätzlich zu den Sicherheitseinstellungen in diesem Abschnitt ist die zweifaktorielle Authentifizierung](security-two-factor-authentication.md) (2FA) erforderlich, um die Identität der Benutzer mit einem einmaligen Kennwort zu überprüfen, das von einer App oder einem Gerät generiert wird. [ Sie werden beim ersten Anmelden bei Admin aufgefordert, 2FA einzurichten. Für zusätzliche Sicherheit kann die Admin-Anmeldung auch so konfiguriert werden, dass eine [CAPTCHA](security-captcha.md) erforderlich ist.

>[!NOTE]
>
>Bei Stores, für die die Authentifizierung mit [!DNL Adobe Identity Management Services] (IMS) aktiviert wurde, sind native Adobe Commerce und Magento Open Source 2FA deaktiviert. Admin-Benutzer, die mit ihren Adobe-Anmeldeinformationen bei ihrer Commerce-Instanz angemeldet sind, müssen sich nicht für viele Administratoraufgaben erneut authentifizieren. Die Authentifizierung wird von Adobe IMS verarbeitet, wenn sich der Administrator in seiner aktuellen Sitzung anmeldet. Siehe [[!DNL Adobe Identity Management Service]  (IMS)-Integrationsübersicht](../getting-started/adobe-ims-integration-overview.md).

Technische Informationen finden Sie unter [Sicherheitsübersicht](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target=&quot;_blank&quot;} in der Entwicklerdokumentation.

![Sicherheit des Administrators](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Admin Security konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich unter _[!UICONTROL Advanced]_die Option **[!UICONTROL Admin]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Security]** .

1. Um zu verhindern, dass sich Admin-Benutzer von demselben Konto auf verschiedenen Geräten aus anmelden, setzen Sie **[!UICONTROL Admin Account Sharing]** auf `No`.

1. Um die Methode zu bestimmen, mit der Kennwortrücksetzanforderungen verwaltet werden, setzen Sie **[!UICONTROL Password Reset Protection Type]** auf eine der folgenden Optionen:

   - `By IP and Email` - Das Kennwort kann online zurückgesetzt werden, nachdem eine Antwort von der Benachrichtigung erhalten wurde und an die mit dem Admin-Konto verknüpfte E-Mail-Adresse gesendet wurde.
   - `By IP` - Das Kennwort kann ohne zusätzliche Bestätigung online zurückgesetzt werden.
   - `By Email` - Das Kennwort kann nur zurückgesetzt werden, indem eine E-Mail-Antwort auf die Benachrichtigung gesendet wird, die an die mit dem Admin-Konto verknüpfte E-Mail-Adresse gesendet wird.
   - `None` - Das Kennwort kann nur vom Store-Administrator zurückgesetzt werden.

1. Legen Sie Anmeldesicherheitsoptionen fest:

   - Geben Sie für &quot;**[!UICONTROL Recovery Link Expiration Period (hours)]**&quot;die Anzahl der Stunden ein, in denen ein Link zur Passwortwiederherstellung gültig bleibt.

   - Geben Sie die Zahl für &quot;**[!UICONTROL Max Number of Password Reset Requests]**&quot; ein, um die maximale Anzahl von Kennwortanfragen zu bestimmen, die pro Stunde gesendet werden können.

   - Geben Sie für &quot;**[!UICONTROL Min Time Between Password Reset Requests]**&quot;die Mindestanzahl von Minuten ein, die zwischen den Anforderungen zum Zurücksetzen des Kennworts übergeben werden müssen.

   - Um einen geheimen Schlüssel an die Admin-URL anzuhängen, als Vorsichtsmaßnahme gegen Exploits, setzen Sie **[!UICONTROL Add Secret Key to URLs]** auf `Yes`. Diese Einstellung ist standardmäßig aktiviert.

   - Damit die Verwendung von Groß- und Kleinbuchstaben in eingegebenen Anmeldedaten mit den im System gespeicherten Werten übereinstimmt, setzen Sie **[!UICONTROL Login is Case Sensitive]** auf `Yes`.

   - Geben Sie die Dauer einer Admin-Sitzung vor Ablauf der Sitzung in Sekunden für das Feld **[!UICONTROL Admin Session Lifetime (seconds)]** ein. Der Wert muss mindestens 60 Sekunden betragen.

   - Geben Sie für &quot;**[!UICONTROL Maximum Login Failures to Lockout Account]**&quot;an, wie oft ein Benutzer versuchen kann, sich beim Administrator anzumelden, bevor das Konto gesperrt wird. Standardmäßig sind sechs Versuche zulässig. Lassen Sie das Feld für unbegrenzte Anmeldeversuche leer.

   - Geben Sie für &quot;**[!UICONTROL Lockout Time (minutes)]**&quot;die Anzahl der Minuten ein, die ein Admin-Konto gesperrt wird, wenn die maximale Anzahl von Versuchen erreicht ist.

1. Kennwortoptionen festlegen:

   - Um die Lebensdauer von Admin-Passwörtern zu begrenzen, geben Sie die Anzahl der Tage ein, für die ein Passwort für **[!UICONTROL Password Lifetime (days)]** gültig ist. Lassen Sie das Feld für eine unbegrenzte Lebensdauer leer.

   - Setzen Sie **[!UICONTROL Password Change]** auf einen der folgenden Werte:

      - `Forced` - Erfordert, dass Admin-Benutzer ihr Passwort nach der Kontoeinrichtung ändern.
      - `Recommended` - Empfiehlt Admin-Benutzern, ihr Passwort nach der Kontoeinrichtung zu ändern.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Passwortanforderungen für Administratoren

Standardmäßig muss ein Admin-Kennwort aus sieben oder mehr Zeichen bestehen und sowohl Buchstaben als auch Zahlen enthalten.
