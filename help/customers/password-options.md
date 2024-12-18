---
title: Optionen für Kundenkennwörter
description: Die Kennwortoptionen für Kunden bestimmen das Sicherheitsniveau für verschiedene kundenorientierte Funktionen Ihres Stores.
exl-id: 84dec8e8-3363-4133-bbcc-9e58467749c4
feature: Customers, Configuration, Security
source-git-commit: ea9eeea0fc5213de2787e0b7ea2aed825ca3a9de
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Optionen für Kundenkennwörter

Die Optionen für das Kundenkennwort bestimmen die Sicherheitsstufe, die für Anfragen zum Zurücksetzen des Kennworts verwendet wird, die E-Mail-Vorlagen, die für die Kundenbenachrichtigung verwendet werden, und die Lebensdauer des Links zur Passwortwiederherstellung. Sie können Kunden erlauben, ihre eigenen Kennwörter zu ändern, oder vorschreiben, dass nur Store-Administratoren dies tun können.

## Konfigurieren von Optionen für Kundenkennwörter

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Customer Configuration]**.

1. Erweitern Sie den Abschnitt **[!UICONTROL Password Options]** .

   ![Kennwortoptionen](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. Legen Sie die **[!UICONTROL Password Reset Protection Type]** auf die Methode fest, die Sie zum Überprüfen von Anfragen zum Zurücksetzen des Kennworts verwenden möchten:

   - `By IP and Email` - Prüfen Sie, ob zuvor versucht wurde, das Kennwort für eine bestimmte E-Mail oder eine bestimmte IP-Adresse zurückzusetzen.
   - `By IP` - Prüfen Sie, ob bereits versucht wurde, ein Kennwort von einer bestimmten IP-Adresse zurückzusetzen.
   - `By Email` - Prüfen Sie, ob zuvor versucht wurde, das Kennwort für eine bestimmte E-Mail zurückzusetzen.
   - `None` - Schutz deaktiviert (keine Beschränkungen für das Zurücksetzen des Passworts).

   **[!UICONTROL Max Number of Password Reset Requests]** und **[!UICONTROL Min Time Between Password Reset Requests]** werden anhand dieser Konfiguration berechnet.

1. Gehen Sie wie folgt vor, um die Anzahl der pro Stunde gesendeten Anfragen zum Zurücksetzen des Kennworts zu begrenzen:

   - Geben Sie **[!UICONTROL Max Number of Password Reset Requests]** die maximale Anzahl von Anfragen zum Zurücksetzen des Passworts ein, die pro Stunde gesendet werden können.

   - Geben Sie **[!UICONTROL Min Time Between Password Reset Requests]** die Mindestanzahl von Minuten ein, die zwischen den Anforderungen verstreichen muss.

1. Gehen Sie wie folgt vor, um die E-Mail-Benachrichtigung zum Zurücksetzen des Kennworts zu konfigurieren:

   - Legen Sie **[!UICONTROL Forgot Email Template]** auf die Vorlage fest, die für die E-Mail verwendet wird, die an Kunden gesendet wird, die ihre Passwörter vergessen haben.

   - Legen Sie **[!UICONTROL Remind Email Template]** auf die Vorlage fest, die verwendet wird, wenn ein Kundenkennwort von einem Administrator zurückgesetzt wird.

   - Legen Sie **[!UICONTROL Reset Password Template]** auf die Vorlage fest, die verwendet wird, wenn Kundinnen und Kunden ihr Passwort ändern.

   - Legen Sie **[!UICONTROL Password Template Email Sender]** auf den [Store-Kontakt](../getting-started/store-details.md) fest, der als Absender kennwortbezogener Benachrichtigungen angezeigt wird.

1. Führen Sie die folgenden Sicherheitsoptionen zum Zurücksetzen des Kennworts aus:

   - Geben Sie **[!UICONTROL Recovery Link Expiration Period (hours)]** die Anzahl der Stunden ein, nach denen der Link zur Passwortwiederherstellung abläuft.

   - Wenn Sie möchten, dass die Felder in den Kundenanmelde- und Kennwortformularen automatisch aus vorherigen Einträgen ausgefüllt werden, setzen Sie **[!UICONTROL Enable Autocomplete on login/forgot password forms]** auf `Yes`.

   - Geben Sie **[!UICONTROL Number of Required Character Classes]** die Anzahl der verschiedenen Zeichentypen ein, die in einem Kennwort enthalten sein müssen, das auf den folgenden Zeichenklassen basiert:

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - Geben Sie **[!UICONTROL Maximum Login Failures to Lockout Account]** die Anzahl fehlgeschlagener Anmeldeversuche ein, bis das Kundenkonto gesperrt ist. Geben Sie für unbegrenzte Versuche null (`0`) ein.

   - Geben Sie **[!UICONTROL Minimum Password Length]** die Mindestanzahl von Zeichen ein, die in einem Kennwort verwendet werden können. Die Zahl muss größer als null sein.

   - Geben Sie **[!UICONTROL Lockout Time (minutes)]** die Anzahl der Minuten ein, die ein Kundenkonto nach zu vielen fehlgeschlagenen Anmeldeversuchen gesperrt ist.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
