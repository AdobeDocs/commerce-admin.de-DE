---
title: Sitzungsverwaltung
description: Erfahren Sie, wie Sie die Sitzungsverwaltung konfigurieren, um den Administrator und die Storefront zu schützen.
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# Sitzungsverwaltung

[Sitzungsverwaltung](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) ist eine Best Practice gegen die Denial of Service (DoS) für die API-Sicherheit. Eine Sitzung stellt die Zeit dar, die ein Besucher auf Ihrer Site verbringt, und ist nicht abhängig davon, wie lange Admin-Benutzer oder -Kunden bei ihren Konten angemeldet sind.

Eine Sitzung ist eine Sequenz von Netzwerk-HTTP-Anforderungs- und Antworttransaktionen, die mit demselben Benutzer verknüpft sind. Es ist eine Möglichkeit, einen Client (Admin) mit seinen Daten zu verknüpfen, wenn er auf den Server zugreift. Sitzungen werden verwendet, um Variablen wie Zugriffsberechtigungen und Lokalisierungseinstellungen festzulegen, die für jede Interaktion eines Benutzers mit einer Webanwendung während der Sitzung gelten.

## Sitzungsgröße

Verwenden Sie die folgenden Konfigurationseinstellungen, um die maximale Sitzungsgröße für Admin-Benutzer und Storefront-Besucher zu begrenzen:

- **[!UICONTROL Max Session Size in Admin]** - Begrenzen Sie die maximale Sitzungsgröße in Byte. Verwenden Sie `0` , um zu deaktivieren.
- **[!UICONTROL Max Session Size in Storefront]** - Begrenzen Sie die maximale Sitzungsgröße in Byte. Verwenden Sie `0` , um zu deaktivieren.

>[!TIP]
>
>Beide Einstellungen werden in Byte gemessen und standardmäßig in `256000` Byte (oder 256 KB).

**_So konfigurieren Sie die maximale Sitzungsgröße:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Security]** , um auf die Sitzungseinstellungen zuzugreifen.

   ![Sitzungseinstellungen](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. Geben Sie neue Sitzungsgrößen in Byte ein.

   >[!WARNING]
   >
   >Das Festlegen eines zu niedrigen Werts kann zu Problemen führen. Wenn Sie eine der Optionen unter den Standardwert von 256000 Byte setzen, wird eine Warnmeldung angezeigt. Wenn Sie auf **[!UICONTROL No]** klicken, ändert das System den Wert in `256000`.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

### Admin-Sitzungen

Wenn Sie die maximale Sitzungsgröße überschreiten, wird eine Fehlermeldung angezeigt und das System protokolliert die Sitzungsgrößenbegrenzung in den Ordner &quot;`var/log`&quot;.

Wenn Sie den Zugriff auf den Admin verlieren, nachdem Sie die Sitzungsgröße zu niedrig eingestellt haben, verwenden Sie die CLI, um die Konfiguration zurückzusetzen:

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### Storefront-Sitzungen

Wenn Sie die maximale Sitzungsgröße überschreiten, wird kein Fehler angezeigt, aber das System protokolliert die Sitzungsgrößenbegrenzung in den Ordner &quot;`var/log`&quot;.

## Sitzungsvalidierung

Mit Adobe Commerce und Magento Open Source können Sie Sitzungsvariablen als Schutzmaßnahme gegen mögliche Sitzungsfixierungsangriffe oder Versuche überprüfen, Benutzersitzungen zu vergiften oder zu verbergen. Die Sitzungsvalidierungseinstellungen bestimmen, wie Sitzungsvariablen bei jedem Store-Besuch validiert werden und ob die Sitzungs-ID in der URL des Stores enthalten ist.

Technische Informationen finden Sie unter [Verwenden von Redis für die Sitzungsspeicherung](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html) im _Konfigurationshandbuch_.

![Allgemeine Konfiguration - Validierung der Websitzung](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

Durch die Validierung wird überprüft, ob Besucher die von ihnen angegebenen sind, indem der Wert in den Validierungsvariablen mit den Sitzungsdaten verglichen wird, die für den Benutzer in `$_SESSION` -Daten gespeichert sind. Die Validierung schlägt fehl, wenn die Informationen nicht erwartungsgemäß übermittelt werden und die entsprechende Variable leer ist. Wenn eine Sitzungsvariable den Validierungsprozess je nach Sitzungsvalidierungseinstellungen nicht durchführt, wird die Client-Sitzung sofort beendet.

Die Aktivierung aller Validierungsvariablen kann dazu beitragen, Angriffe zu verhindern, aber auch die Leistung des Servers beeinträchtigen. Standardmäßig ist die Validierung aller Sitzungsvariablen deaktiviert. Es wird empfohlen, mit den Einstellungen zu experimentieren, um die beste Kombination für Ihre Adobe Commerce- oder Magento Open Source-Installation zu finden. Die Aktivierung aller Validierungsvariablen kann sich als übermäßig restriktiv erweisen und den Zugriff auf Kunden verhindern, die Internetverbindungen haben, die über einen Proxy-Server weitergeleitet werden oder von einer Firewall stammen. Weitere Informationen zu Sitzungsvariablen und deren Verwendung finden Sie in der Dokumentation zur Systemadministration für Ihr Linux®-System.

**_So konfigurieren Sie die Sitzungsvalidierung:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert _[!UICONTROL General]_und wählen Sie **[!UICONTROL Web]**aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Session Validation Settings]** .

1. Legen Sie die einzelnen Konfigurationsoptionen fest:

   - **[!UICONTROL Validate REMOTE_ADDR]** - Auf `Yes` setzen, um sicherzustellen, dass die IP-Adresse einer Anforderung mit der in der Variable `$_SESSION` gespeicherten übereinstimmt.

   - **[!UICONTROL Validate HTTP_VIA]** - Auf `Yes` setzen, um sicherzustellen, dass die Proxy-Adresse einer eingehenden Anfrage mit der in der Variable `$_SESSION` gespeicherten übereinstimmt.

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]** - Auf `Yes` setzen, um sicherzustellen, dass die weitergeleitete Adresse einer Anfrage mit der in der Variable `$_SESSION` gespeicherten übereinstimmt.

   - **[!UICONTROL Validate HTTP_USER_AGENT]** - Auf `Yes` setzen, um zu überprüfen, ob der Browser oder das Gerät, mit dem während einer Sitzung auf den Store zugegriffen wird, mit dem übereinstimmt, was in der Variable `$_SESSION` gespeichert ist.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Lebensdauer der Admin-Sitzung

Als Sicherheitsmaßnahme wird der _Admin_ zunächst auf eine Zeitüberschreitung nach 900 Sekunden (15 Minuten) Tastaturinaktivität eingestellt. Sie können die Lebensdauer der Sitzung an Ihren Arbeitsstil anpassen.

**_So passen Sie die Lebensdauer der Admin-Sitzung an:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Scrollen Sie nach unten und erweitern Sie **[!UICONTROL Advanced]** im linken Seitenbereich.

1. Klicken Sie auf **[!UICONTROL Admin]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt _[!UICONTROL Security]_.

1. Geben Sie für &quot;**[!UICONTROL Admin Session Lifetime (seconds)]**&quot;die Anzahl der Sekunden ein, die eine Sitzung aktiv bleibt, bevor eine Zeitüberschreitung eintritt.

   ![Erweiterte Konfiguration - Sicherheitseinstellungen für Administratoren](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.## Lebensdauer der Admin-Sitzung

Als Sicherheitsmaßnahme wird der _Admin_ zunächst auf eine Zeitüberschreitung nach 900 Sekunden (15 Minuten) Tastaturinaktivität eingestellt. Sie können die Lebensdauer der Sitzung an Ihren Arbeitsstil anpassen.

**_So passen Sie die Lebensdauer der Admin-Sitzung an:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Scrollen Sie nach unten und erweitern Sie **[!UICONTROL Advanced]** im linken Seitenbereich.

1. Klicken Sie auf **[!UICONTROL Admin]**.

1. Erweitern Sie den Abschnitt _Sicherheit_ um ![Erweiterungsauswahl](../assets/icon-display-expand.png).

1. Geben Sie für &quot;**[!UICONTROL Admin Session Lifetime (seconds)]**&quot;die Anzahl der Sekunden ein, die eine Sitzung aktiv bleibt, bevor eine Zeitüberschreitung eintritt.

   ![Erweiterte Konfiguration - Sicherheitseinstellungen für Administratoren](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
