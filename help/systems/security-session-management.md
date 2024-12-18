---
title: Sitzungsverwaltung
description: Erfahren Sie, wie Sie das Sitzungsmanagement konfigurieren, um die Admin- und Storefront zu schützen.
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
source-git-commit: aabbf6d37a2c7fa730e1f3673edfb414685008b6
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 0%

---

# Sitzungsverwaltung

[Sitzungsverwaltung](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) ist eine Best Practice für die Verwendung von DoS (Anti-Denial of Service) für die API-Sicherheit. Eine Sitzung gibt die Zeit an, die eine Besucherin oder ein Besucher auf Ihrer Website verbringt, und hängt nicht damit zusammen, wie lange Admin-Benutzende oder -Kunden bei ihren Konten angemeldet sind.

Eine Sitzung ist eine Sequenz von HTTP-Anfrage- und -Antworttransaktionen im Netzwerk, die demselben Benutzer zugeordnet sind. Es ist eine Möglichkeit, einen Client (Administrator) mit seinen Daten zu verknüpfen, wenn er auf den Server zugreift. Sitzungen werden verwendet, um Variablen wie Zugriffsrechte und Lokalisierungseinstellungen festzulegen, die für jede Interaktion eines Benutzers mit einer Web-Anwendung während der Sitzung gelten.

## Sitzungsgröße

Verwenden Sie die folgenden Konfigurationseinstellungen, um die maximale Sitzungsgröße für Admin-Benutzer und Storefront-Besucher zu begrenzen:

- **[!UICONTROL Max Session Size in Admin]** - Begrenzt die maximale Sitzungsgröße in Byte. `0` zum Deaktivieren verwenden.
- **[!UICONTROL Max Session Size in Storefront]** - Begrenzt die maximale Sitzungsgröße in Byte. `0` zum Deaktivieren verwenden.

>[!TIP]
>
>Beide Einstellungen werden in Byte gemessen und standardmäßig auf `256000` Byte (oder 256 KB) eingestellt.

**_So konfigurieren Sie die maximale Sitzungsgröße:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Security]** , um auf die Sitzungseinstellungen zuzugreifen.

   ![Sitzungseinstellungen](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. Geben Sie neue Sitzungsgrößen in Byte ein.

   >[!WARNING]
   >
   >Ein zu niedriger Wert kann Probleme verursachen. Wenn Sie eine der Optionen unter dem Standardwert von 256000 Byte festlegen, wird eine Warnmeldung angezeigt. Wenn Sie auf **[!UICONTROL No]** klicken, ändert das System den Wert in `256000`.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

### Admin-Sitzungen

Wenn Sie die maximale Sitzungsgröße überschreiten, wird eine Fehlermeldung angezeigt und das System protokolliert die Sitzungsgrößenbeschränkung im `var/log`.

Wenn Sie den Zugriff auf den Administrator verlieren, nachdem Sie die Sitzungsgröße auf einen zu niedrigen Wert festgelegt haben, verwenden Sie die CLI, um die Konfiguration zurückzusetzen:

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### Storefront-Sitzungen

Wenn Sie die maximale Sitzungsgröße überschreiten, wird kein Fehler angezeigt, aber das System protokolliert die Sitzungsgrößenbeschränkung im `var/log`.

## Sitzungsvalidierung

Adobe Commerce und Magento Open Source ermöglichen es Ihnen, Sitzungsvariablen zu validieren, um vor möglichen Sitzungsfixierungsangriffen oder Versuchen zu schützen, Benutzersitzungen zu vergiften oder zu entführen. Die Sitzungsvalidierungseinstellungen bestimmen, wie Sitzungsvariablen bei jedem Store-Besuch validiert werden und ob die Sitzungs-ID in der URL des Stores enthalten ist.

Technische Informationen finden Sie unter [Verwenden von Redis für ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html) Sitzungsspeicherung) im _Konfigurationshandbuch_.

![Allgemeine Konfiguration - Validierung von Web-Sitzungen](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

Die Validierung prüft, ob Besucher sich selbst ausgeben, indem der Wert in den Validierungsvariablen mit den Sitzungsdaten verglichen wird, die in `$_SESSION` Daten für den Benutzer gespeichert sind. Die Validierung schlägt fehl, wenn die Informationen nicht erwartungsgemäß übermittelt werden und die entsprechende Variable leer ist. Abhängig von den Einstellungen für die Sitzungsvalidierung wird die Clientsitzung sofort beendet, wenn der Validierungsprozess einer Sitzungsvariablen fehlschlägt.

Die Aktivierung aller Validierungsvariablen kann Angriffe verhindern, aber auch die Leistung des Servers beeinträchtigen. Standardmäßig ist die Validierung aller Sitzungsvariablen deaktiviert. Es wird empfohlen, mit den Einstellungen zu experimentieren, um die beste Kombination für Ihre Adobe Commerce- oder Magento Open Source-Installation zu finden. Die Aktivierung aller Validierungsvariablen kann sich als unangemessen restriktiv erweisen und den Zugriff auf Kunden mit Internetverbindungen, die einen Proxy-Server durchlaufen oder hinter einer Firewall stammen, verhindern. Weitere Informationen zu Sitzungsvariablen und deren Verwendung finden Sie in der Systemadministrationsdokumentation für Ihr Linux®-System.

**_So konfigurieren Sie die Sitzungsvalidierung:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich _[!UICONTROL General]_und wählen Sie **[!UICONTROL Web]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Session Validation Settings]** .

1. Legen Sie jede der Konfigurationsoptionen fest:

   - **[!UICONTROL Validate REMOTE_ADDR]** - Mit `Yes` überprüfen Sie, ob die IP-Adresse einer Anfrage mit dem übereinstimmt, was in der `$_SESSION`-Variablen gespeichert ist.

   - **[!UICONTROL Validate HTTP_VIA]** - Mit `Yes` stellen Sie sicher, dass die Proxy-Adresse einer eingehenden Anfrage mit der in der `$_SESSION` gespeicherten übereinstimmt.

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]** - Wird auf `Yes` gesetzt, um zu überprüfen, ob die weitergeleitete Adresse einer Anfrage mit dem übereinstimmt, was in der `$_SESSION`-Variablen gespeichert ist.

   - **[!UICONTROL Validate HTTP_USER_AGENT]** - Legen Sie hierfür `Yes` fest, um sicherzustellen, dass der Browser oder das Gerät, der/das während einer Sitzung auf den Store zugreift, mit dem übereinstimmt, was in der `$_SESSION`-Variablen gespeichert ist.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Lebensdauer der Admin-Sitzung

Als Sicherheitsmaßnahme ist _Admin_ zunächst auf eine Zeitüberschreitung nach 900 Sekunden (15 Minuten) Tastaturinaktivität eingestellt. Sie können die Lebensdauer der Sitzung an Ihren Arbeitsstil anpassen.

**_So passen Sie die Lebensdauer der Admin-Sitzung an:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Scrollen Sie nach unten und erweitern Sie **[!UICONTROL Advanced]** im linken Seitenbereich.

1. Klicken Sie auf **[!UICONTROL Admin]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Security]** .

1. Geben Sie **[!UICONTROL Admin Session Lifetime (seconds)]** die Anzahl der Sekunden ein, nach denen eine Sitzung aktiv bleibt, bevor eine Zeitüberschreitung eintritt.

   ![Erweiterte Konfiguration - Admin-Sicherheitseinstellungen](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
