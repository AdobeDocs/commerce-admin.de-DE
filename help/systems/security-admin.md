---
title: Konfigurieren der Admin-Sicherheit
description: Erfahren Sie, wie Sie die Sicherheit für Ihren Store-Administrator konfigurieren.
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Konfigurieren der Admin-Sicherheit

Wir empfehlen Ihnen, einen vielseitigen Ansatz zu wählen, um die Sicherheit Ihres Geschäfts zu schützen. Sie können mit einer [benutzerdefinierten Admin-URL](../stores-purchase/store-urls.md#use-a-custom-admin-url) beginnen, die nicht einfach zu erraten ist, anstatt mit dem offensichtlichen „Admin“ oder „Backend“. Standardmäßig müssen Kennwörter, die für die [ beim ](../getting-started/admin-signin.md) verwendet werden, mindestens sieben Zeichen lang sein und sowohl Buchstaben als auch Zahlen enthalten. Verwenden [ als Best ](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) nur sichere Administratorkennwörter, die aus einer Kombination aus Buchstaben, Zahlen und Symbolen bestehen. Adobe Commerce und Magento Open Source erlauben nicht die Wiederverwendung der letzten vier dem Konto zugewiesenen Kennwörter.

Die Admin-Sicherheitskonfiguration bietet folgende Möglichkeiten:

- Hinzufügen eines geheimen Schlüssels zu URLs
- Kennwörter müssen zwischen Groß- und Kleinschreibung unterscheiden
- Länge der Admin-Sitzungen begrenzen
- Lebensdauer von Kennwörtern begrenzen
- Anzahl der Anmeldeversuche begrenzen, die unternommen werden können, bevor das Admin-Benutzerkonto [gesperrt](permissions-users-all.md#locked-users) wird

Um die Sicherheit zu erhöhen, können Sie die Dauer der Tastaturinaktivität konfigurieren, bevor die aktuelle Sitzung abläuft, und dabei die Groß-/Kleinschreibung bei Benutzernamen und Kennwort berücksichtigen.

Zusätzlich zu den Sicherheitseinstellungen in diesem Abschnitt ist eine [Zwei-Faktor-Authentifizierung](security-two-factor-authentication.md) (2FA) erforderlich, um die Identität von Benutzern mit einem einmaligen Kennwort zu überprüfen, das von einer App oder einem Gerät generiert wird. Beim ersten Anmelden beim Administrator werden Sie aufgefordert, 2FA einzurichten. Zur zusätzlichen Sicherheit kann die Admin-Anmeldung auch so konfiguriert werden, dass ein [CAPTCHA“ erforderlich ](security-captcha.md).

>[!NOTE]
>
>Bei Stores mit aktivierter [!DNL Adobe Identity Management Services]-Authentifizierung (IMS) sind die native Adobe Commerce und Magento Open Source 2FA deaktiviert. Admin-Benutzende, die mit ihren Adobe-Anmeldeinformationen bei ihrer Commerce-Instanz angemeldet sind, müssen sich für viele Admin-Aufgaben nicht erneut authentifizieren. Die Authentifizierung wird von Adobe IMS durchgeführt, wenn sich der Administrator bei seiner aktuellen Sitzung anmeldet. Siehe Übersicht über die [[!DNL Adobe Identity Management Service] (IMS)-Integration](../getting-started/adobe-ims-integration-overview.md).

Technische Informationen finden Sie unter [Sicherheitsübersicht](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target="_blank"} in der Entwicklerdokumentation.

![Admin-Sicherheit](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Konfigurieren der Admin-Sicherheit

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bedienfeld unter _[!UICONTROL Advanced]_&#x200B;die Option **[!UICONTROL Admin]**&#x200B;aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Security]** .

1. Um zu verhindern, dass sich Admin-Benutzer über dasselbe Konto auf verschiedenen Geräten anmelden, setzen Sie **[!UICONTROL Admin Account Sharing]** auf `No`.

1. Legen Sie **[!UICONTROL Password Reset Protection Type]** auf eine der folgenden Einstellungen fest, um die Methode zur Verwaltung von Anfragen zum Zurücksetzen von Kennwörtern zu bestimmen:

   - `By IP and Email` - Das Kennwort kann online zurückgesetzt werden, nachdem eine Antwort von der Benachrichtigung an die mit dem Admin-Konto verknüpfte E-Mail-Adresse gesendet wurde.
   - `By IP` — Das Passwort kann online ohne zusätzliche Bestätigung zurückgesetzt werden.
   - `By Email` - Das Kennwort kann nur zurückgesetzt werden, indem per E-Mail auf die Benachrichtigung geantwortet wird, die an die mit dem Admin-Konto verknüpfte E-Mail-Adresse gesendet wird.
   - `None` - Das Kennwort kann nur vom Store-Administrator zurückgesetzt werden.

1. Sicherheitsoptionen für die Anmeldung festlegen:

   - Geben Sie **[!UICONTROL Recovery Link Expiration Period (hours)]** die Anzahl der Stunden ein, für die ein Link zur Passwortwiederherstellung gültig bleibt.

   - Um die maximale Anzahl von Passwortanfragen zu ermitteln, die pro Stunde gesendet werden können, geben Sie die Anzahl für **[!UICONTROL Max Number of Password Reset Requests]** ein.

   - Geben Sie **[!UICONTROL Min Time Between Password Reset Requests]** die Mindestanzahl von Minuten ein, die zwischen den Anforderungen zum Zurücksetzen des Kennworts vergehen muss.

   - Um einen geheimen Schlüssel zur Admin-URL als Vorsichtsmaßnahme gegen Exploits anzuhängen, setzen Sie **[!UICONTROL Add Secret Key to URLs]** auf `Yes`. Diese Einstellung ist standardmäßig aktiviert.

   - Um festzulegen, dass die Verwendung von Groß- und Kleinbuchstaben in den eingegebenen Anmeldedaten mit den im System gespeicherten Zeichen übereinstimmen muss, setzen Sie **[!UICONTROL Login is Case Sensitive]** auf `Yes`.

   - Um die Länge einer Admin-Sitzung vor der Zeitüberschreitung zu ermitteln, geben Sie die Dauer der Sitzung in Sekunden für **[!UICONTROL Admin Session Lifetime (seconds)]** Feld ein. Der Wert muss 60 Sekunden oder länger betragen.

   - Geben Sie **[!UICONTROL Maximum Login Failures to Lockout Account]** an, wie oft sich ein Benutzer beim Administrator anmelden kann, bevor das Konto gesperrt wird. Standardmäßig sind sechs Versuche zulässig. Lassen Sie das Feld für unbegrenzte Anmeldeversuche leer.

   - Geben Sie **[!UICONTROL Lockout Time (minutes)]** die Anzahl der Minuten ein, die ein Admin-Konto gesperrt ist, wenn die maximale Anzahl an Versuchen erreicht wird.

1. Kennwortoptionen festlegen:

   - Um die Lebensdauer von Admin-Kennwörtern zu begrenzen, geben Sie die Anzahl der Tage ein, für die ein Kennwort gültig ist **[!UICONTROL Password Lifetime (days)]**. Lassen Sie das Feld für eine unbegrenzte Lebensdauer leer.

   - Legen Sie **[!UICONTROL Password Change]** auf eine der folgenden Einstellungen fest:

      - `Forced` - Erfordert, dass Admin-Benutzer ihr Passwort nach der Einrichtung des Kontos ändern.
      - `Recommended` - empfiehlt Admin-Benutzern, ihre Kennwörter nach der Einrichtung des Kontos zu ändern.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Administratorkennwort-Anforderungen

Standardmäßig muss ein Administratorkennwort mindestens sieben Zeichen lang sein und sowohl Buchstaben als auch Zahlen enthalten.
