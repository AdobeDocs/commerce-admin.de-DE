---
title: Sitzungsverwaltung
description: Erfahren Sie, wie Sie die Sitzungsverwaltung konfigurieren, um den Administrator und die Storefront zu schützen.
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Sitzungsverwaltung

[Sitzungsverwaltung](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) ist eine Best Practice gegen die Denial of Service (DoS) für die API-Sicherheit. Eine Sitzung stellt die Zeit dar, die ein Besucher auf Ihrer Site verbringt, und ist nicht abhängig davon, wie lange Admin-Benutzer oder -Kunden bei ihren Konten angemeldet sind.

Eine Sitzung ist eine Sequenz von Netzwerk-HTTP-Anforderungs- und Antworttransaktionen, die mit demselben Benutzer verknüpft sind. Es ist eine Möglichkeit, einen Client (Admin) mit seinen Daten zu verknüpfen, wenn er auf den Server zugreift. Sitzungen werden verwendet, um Variablen wie Zugriffsberechtigungen und Lokalisierungseinstellungen festzulegen, die für jede Interaktion eines Benutzers mit einer Webanwendung während der Sitzung gelten.

## Sitzungsgröße

Verwenden Sie die folgenden Konfigurationseinstellungen, um die maximale Sitzungsgröße für Admin-Benutzer und Storefront-Besucher zu begrenzen:

- **[!UICONTROL Max Session Size in Admin]**—Begrenzen Sie die maximale Sitzungsgröße in Byte. Verwendung `0` , um zu deaktivieren.
- **[!UICONTROL Max Session Size in Storefront]**—Begrenzen Sie die maximale Sitzungsgröße in Byte. Verwendung `0` , um zu deaktivieren.

>[!TIP]
>
>Beide Einstellungen werden in Byte gemessen und standardmäßig auf `256000` Byte (oder 256 KB).

**_So konfigurieren Sie die maximale Sitzungsgröße:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]**  > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL System]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Security]** -Abschnitt, um auf die Sitzungseinstellungen zuzugreifen.

   ![Sitzungseinstellungen](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. Geben Sie neue Sitzungsgrößen in Byte ein.

   >[!WARNING]
   >
   >Das Festlegen eines zu niedrigen Werts kann zu Problemen führen. Wenn Sie eine der Optionen unter den Standardwert von 256000 Byte setzen, wird eine Warnmeldung angezeigt. Wenn Sie auf **[!UICONTROL No]**, ändert das System den Wert in `256000`.

1. Klicken **[!UICONTROL Save Config]**.

### Admin-Sitzungen

Wenn Sie die maximale Sitzungsgröße überschreiten, wird eine Fehlermeldung angezeigt und das System protokolliert die Sitzungsgrößenbegrenzung auf `var/log` Verzeichnis.

Wenn Sie den Zugriff auf den Admin verlieren, nachdem Sie die Sitzungsgröße zu niedrig eingestellt haben, verwenden Sie die CLI, um die Konfiguration zurückzusetzen:

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### Storefront-Sitzungen

Wenn Sie die maximale Sitzungsgröße überschreiten, wird kein Fehler angezeigt, aber das System protokolliert die Sitzungsgrößenbegrenzung auf `var/log` Verzeichnis.

## Sitzungsvalidierung

Mit Adobe Commerce und Magento Open Source können Sie Sitzungsvariablen als Schutzmaßnahme gegen mögliche Sitzungsfixierungsangriffe oder Versuche überprüfen, Benutzersitzungen zu vergiften oder zu verbergen. Die Sitzungsvalidierungseinstellungen bestimmen, wie Sitzungsvariablen bei jedem Store-Besuch validiert werden und ob die Sitzungs-ID in der URL des Stores enthalten ist.

Technische Informationen finden Sie unter [Verwenden von Redizes für die Sitzungsspeicherung](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html) im _Konfigurationshandbuch_.

![Allgemeine Konfiguration - Validierung von Websitzungen](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

Die Validierung überprüft, ob Besucher die sind, für die sie sich entscheiden, indem der Wert in den Validierungsvariablen mit den Sitzungsdaten verglichen wird, die in `$_SESSION` Daten für den Benutzer. Die Validierung schlägt fehl, wenn die Informationen nicht erwartungsgemäß übermittelt werden und die entsprechende Variable leer ist. Wenn eine Sitzungsvariable den Validierungsprozess je nach Sitzungsvalidierungseinstellungen nicht durchführt, wird die Client-Sitzung sofort beendet.

Die Aktivierung aller Validierungsvariablen kann dazu beitragen, Angriffe zu verhindern, aber auch die Leistung des Servers beeinträchtigen. Standardmäßig ist die Validierung aller Sitzungsvariablen deaktiviert. Es wird empfohlen, mit den Einstellungen zu experimentieren, um die beste Kombination für Ihre Adobe Commerce- oder Magento Open Source-Installation zu finden. Die Aktivierung aller Validierungsvariablen kann sich als übermäßig restriktiv erweisen und den Zugriff auf Kunden verhindern, die Internetverbindungen haben, die über einen Proxy-Server weitergeleitet werden oder von einer Firewall stammen. Weitere Informationen zu Sitzungsvariablen und deren Verwendung finden Sie in der Dokumentation zur Systemadministration für Ihr Linux®-System.

**_So konfigurieren Sie die Sitzungsvalidierung:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich _[!UICONTROL General]_und wählen **[!UICONTROL Web]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Session Validation Settings]** Abschnitt.

1. Legen Sie die einzelnen Konfigurationsoptionen fest:

   - **[!UICONTROL Validate REMOTE_ADDR]** — Legen Sie `Yes` , um zu überprüfen, ob die IP-Adresse einer Anfrage mit der in der `$_SESSION` -Variable.

   - **[!UICONTROL Validate HTTP_VIA]** — Legen Sie `Yes` , um zu überprüfen, ob die Proxy-Adresse einer eingehenden Anfrage mit der in der `$_SESSION` -Variable.

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]** — Legen Sie `Yes` , um zu überprüfen, ob die weitergeleitete Adresse einer Anfrage mit der in der `$_SESSION` -Variable.

   - **[!UICONTROL Validate HTTP_USER_AGENT]** — Legen Sie `Yes` , um zu überprüfen, ob der Browser oder das Gerät, mit dem während einer Sitzung auf den Store zugegriffen wird, mit dem übereinstimmt, was in der `$_SESSION` -Variable.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Lebensdauer der Admin-Sitzung

Als Sicherheitsmaßnahme wird die _Admin_ nach 900 Sekunden (15 Minuten) Tastaturinaktivität zunächst auf eine Zeitüberschreitung eingestellt ist. Sie können die Lebensdauer der Sitzung an Ihren Arbeitsstil anpassen.

**_So passen Sie die Lebensdauer der Admin-Sitzung an:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Hinunter scrollen und erweitern **[!UICONTROL Advanced]** im linken Seitenbereich.

1. Klicken **[!UICONTROL Admin]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die _[!UICONTROL Security]_Abschnitt.

1. Für **[!UICONTROL Admin Session Lifetime (seconds)]** eingeben, geben Sie die Anzahl der Sekunden ein, die eine Sitzung aktiv bleibt, bevor eine Zeitüberschreitung eintritt.

   ![Erweiterte Konfiguration - Admin-Sicherheitseinstellungen](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.## Lebensdauer der Admin-Sitzung

Als Sicherheitsmaßnahme wird die _Admin_ nach 900 Sekunden (15 Minuten) Tastaturinaktivität zunächst auf eine Zeitüberschreitung eingestellt ist. Sie können die Lebensdauer der Sitzung an Ihren Arbeitsstil anpassen.

**_So passen Sie die Lebensdauer der Admin-Sitzung an:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Hinunter scrollen und erweitern **[!UICONTROL Advanced]** im linken Seitenbereich.

1. Klicken **[!UICONTROL Admin]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die _Sicherheit_ Abschnitt.

1. Für **[!UICONTROL Admin Session Lifetime (seconds)]** eingeben, geben Sie die Anzahl der Sekunden ein, die eine Sitzung aktiv bleibt, bevor eine Zeitüberschreitung eintritt.

   ![Erweiterte Konfiguration - Admin-Sicherheitseinstellungen](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
