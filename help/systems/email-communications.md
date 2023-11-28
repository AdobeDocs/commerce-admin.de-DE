---
title: E-Mail-Kommunikation konfigurieren
description: Erfahren Sie, wie Sie E-Mail-Nachrichten konfigurieren, einschließlich der Weiterleitung zurückgegebener E-Mails oder Antworten auf eine bestimmte E-Mail-Adresse.
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# E-Mail-Kommunikation konfigurieren

Die _E-Mail-Sendeeinstellungen_ Sie können zurückgegebene E-Mails oder Antworten auf E-Mails an eine bestimmte Adresse weiterleiten. Wenn Ihr Store auf einem SMTP- oder Windows-Server ausgeführt wird, können Sie die Host- und Port-Einstellungen überprüfen.

>[!IMPORTANT]
>
>**Sicherheitshinweis** Alle Händler sollten sofort ihre E-Mail-Versandkonfiguration einstellen, um sich vor einer kürzlich identifizierten potenziellen Remote-Code-Ausführungsauswertung zu schützen. Bis dieses Problem behoben ist, wird dringend empfohlen, [!DNL Sendmail] für E-Mail-Kommunikation. Im _[!UICONTROL Mail Sending Settings]_, stellen Sie sicher, dass_[!UICONTROL Set Return Path]_ auf `No`.

Eine detaillierte Liste der Konfigurationseinstellungen finden Sie unter [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) im _Konfigurationsreferenz_.

## E-Mail-Kommunikation konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL System]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Mail Sending Settings]** und führen Sie folgende Schritte aus:

   ![Erweiterte Konfiguration - E-Mail-Sendeeinstellungen](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - Legen Sie bei Bedarf **[!UICONTROL Disable Email Communications]** nach `No`.

   - Für **[!UICONTROL Transport]** wählen Sie den Transporttyp für E-Mail-Nachrichten aus dem Speicher aus: `Sendmail` oder `SMTP`

   - Überprüfen Sie bei Ausführung auf einem SMTP- oder Windows-Server die folgenden Einstellungen:

      - **[!UICONTROL Host]** - `localhost` oder andere

      - **[!UICONTROL Port (25)]** - `25` oder andere

   - Für **[!UICONTROL Set Return Path]** wählen Sie eine der folgenden Optionen aus:

      - `No` - (Empfohlene Sicherheitsmaßnahme) Routen gaben E-Mail an die Standard-E-Mail-Adresse des Stores zurück.
      - `Yes` - Routen, die E-Mail an die Standard-Store-E-Mail-Adresse zurückgegeben haben.
      - `Specified` - Routen, die E-Mail an die in **[!UICONTROL Return Path Email]**.

   - Bei Ausführung auf einem SMTP-Server konfigurieren Sie die Verbindung:

      - **[!UICONTROL Username]** - Geben Sie den Anmeldenamen des Benutzers für den SMTP-Server ein.
      - **[!UICONTROL Password]** - Geben Sie das Kennwort für die SMTP-Serveranmeldung ein.
      - **[!UICONTROL Auth]** - Wählen Sie den Authentifizierungstyp für die SMTP-Serververbindung aus: `NONE` , `PLAIN`oder `LOGIN`
      - **[!UICONTROL SSL]** - Wählen Sie den Überprüfungstyp für das Serversicherheitszertifikat aus: `SSL` oder `TLS`

     ![Erweiterte Konfiguration - E-Mail-Sendeeinstellungen](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Sales Emails]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL General Settings]** Abschnitt.

1. Satz **[!UICONTROL Asynchronous sending]** nach `Enable`.

   ![Vertriebskonfiguration - Allgemeine E-Mail-Einstellungen](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Eine detaillierte Liste der Konfigurationseinstellungen finden Sie unter [_Allgemeine Einstellungen_](../configuration-reference/sales/sales-emails.md) im _Konfigurationsreferenz_.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
