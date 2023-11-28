---
title: Optionen für Kundenkennwörter
description: Die Optionen für das Kundenkennwort bestimmen das Sicherheitsniveau für verschiedene Kundenfunktionen Ihres Stores.
exl-id: 84dec8e8-3363-4133-bbcc-9e58467749c4
feature: Customers, Configuration, Security
source-git-commit: ea9eeea0fc5213de2787e0b7ea2aed825ca3a9de
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Optionen für Kundenkennwörter

Die Optionen für das Kundenkennwort bestimmen die Sicherheitsstufe, die für Anforderungen zum Zurücksetzen des Kennworts verwendet wird, die für die Kundenbenachrichtigung verwendeten E-Mail-Vorlagen und die Lebensdauer des Kennwortwiederherstellungs-Links. Sie können Kunden gestatten, ihre eigenen Kennwörter zu ändern oder verlangen, dass nur Store-Administratoren dies tun können.

## Optionen für das Kundenkennwort konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen **[!UICONTROL Customer Configuration]**.

1. Erweitern Sie die **[!UICONTROL Password Options]** Abschnitt.

   ![Kennwortoptionen](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. Legen Sie die **[!UICONTROL Password Reset Protection Type]** zu der Methode hinzu, die Sie zum Überprüfen von Anforderungen zum Zurücksetzen des Kennworts verwenden möchten:

   - `By IP and Email` - Prüfen Sie, ob Sie zuvor versucht haben, das Kennwort für eine bestimmte E-Mail oder von einer bestimmten IP-Adresse zurückzusetzen.
   - `By IP` - Überprüfen Sie, ob Sie zuvor versucht haben, das Kennwort von einer bestimmten IP-Adresse zurückzusetzen.
   - `By Email` - Prüfen Sie, ob Sie versucht haben, das Kennwort für eine bestimmte E-Mail zurückzusetzen.
   - `None` - Schutz deaktiviert (keine Beschränkungen für das Zurücksetzen des Kennworts).

   Die **[!UICONTROL Max Number of Password Reset Requests]** und **[!UICONTROL Min Time Between Password Reset Requests]** werden anhand dieser Konfiguration berechnet.

1. Gehen Sie wie folgt vor, um die Anzahl der pro Stunde gesendeten Anforderungen zum Zurücksetzen des Kennworts zu begrenzen:

   - Für **[!UICONTROL Max Number of Password Reset Requests]** Geben Sie die maximale Anzahl von Anforderungen zum Zurücksetzen des Kennworts ein, die pro Stunde gesendet werden können.

   - Für **[!UICONTROL Min Time Between Password Reset Requests]**, geben Sie die Mindestanzahl von Minuten an, die zwischen den Anforderungen verstreichen muss.

1. Gehen Sie wie folgt vor, um die E-Mail-Benachrichtigung zum Zurücksetzen des Kennworts zu konfigurieren:

   - Satz **[!UICONTROL Forgot Email Template]** der Vorlage, die für die E-Mail verwendet wird, die an Kunden gesendet wird, die ihr Passwort vergessen haben.

   - Satz **[!UICONTROL Remind Email Template]** auf die Vorlage zu setzen, die verwendet wird, wenn ein Kundenkennwort von einem Admin-Benutzer zurückgesetzt wird.

   - Satz **[!UICONTROL Reset Password Template]** der Vorlage, die verwendet wird, wenn Kunden ihr Passwort ändern.

   - Satz **[!UICONTROL Password Template Email Sender]** der [Store-Kontakt](../getting-started/store-details.md) , der als Absender kennwortbezogener Benachrichtigungen erscheint.

1. Führen Sie die folgenden Sicherheitsoptionen für das Zurücksetzen des Kennworts aus:

   - Für **[!UICONTROL Recovery Link Expiration Period (hours)]** Geben Sie die Anzahl der Stunden ein, bevor der Passwortwiederherstellungs-Link abläuft.

   - Wenn Sie möchten, dass die Felder in der Kundenanmeldung automatisch ausgefüllt werden und die Passwortformulare von früheren Einträgen vergessen werden, legen Sie **[!UICONTROL Enable Autocomplete on login/forgot password forms]** nach `Yes`.

   - Für **[!UICONTROL Number of Required Character Classes]** Geben Sie die Anzahl der verschiedenen Zeichentypen ein, die in ein Kennwort einbezogen werden müssen, basierend auf den folgenden Zeichenklassen:

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - Für **[!UICONTROL Maximum Login Failures to Lockout Account]** eingeben, geben Sie die Anzahl fehlgeschlagener Anmeldeversuche ein, bis das Kundenkonto gesperrt ist. Geben Sie für unbegrenzte Versuche null (`0`).

   - Für **[!UICONTROL Minimum Password Length]** Geben Sie die Mindestanzahl von Zeichen ein, die in einem Kennwort verwendet werden können. Die Zahl muss größer als null sein.

   - Für **[!UICONTROL Lockout Time (minutes)]** eingeben, geben Sie die Anzahl der Minuten ein, in denen ein Kundenkonto nach zu vielen fehlgeschlagenen Anmeldeversuchen gesperrt wird.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
