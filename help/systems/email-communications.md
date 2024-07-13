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

Mit den _E-Mail-Versandeinstellungen_ können Sie zurückgegebene E-Mails oder Antworten an eine bestimmte Adresse weiterleiten. Wenn Ihr Store auf einem SMTP- oder Windows-Server ausgeführt wird, können Sie die Host- und Port-Einstellungen überprüfen.

>[!IMPORTANT]
>
>**Sicherheitshinweis** Alle Händler sollten ihre E-Mail-Versandkonfiguration sofort festlegen, um sie vor einer kürzlich identifizierten potenziellen Remote-Codeausführungsauswertung zu schützen. Bis dieses Problem behoben ist, wird dringend empfohlen, [!DNL Sendmail] nicht für E-Mail-Nachrichten zu verwenden. Stellen Sie im _[!UICONTROL Mail Sending Settings]_sicher, dass_[!UICONTROL Set Return Path]_ auf `No` gesetzt ist.

Eine detaillierte Liste der Konfigurationseinstellungen finden Sie unter [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) in der _Konfigurationsreferenz_.

## E-Mail-Kommunikation konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]** aus.

1. Erweitern Sie den Abschnitt **[!UICONTROL Mail Sending Settings]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   ![Erweiterte Konfiguration - Einstellungen für den E-Mail-Versand](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - Setzen Sie bei Bedarf **[!UICONTROL Disable Email Communications]** auf `No`.

   - Wählen Sie für **[!UICONTROL Transport]** den Transporttyp für E-Mail-Nachrichten aus dem Speicher aus: `Sendmail` oder `SMTP`

   - Überprüfen Sie bei Ausführung auf einem SMTP- oder Windows-Server die folgenden Einstellungen:

      - **[!UICONTROL Host]** - `localhost` oder andere

      - **[!UICONTROL Port (25)]** - `25` oder andere

   - Wählen Sie für **[!UICONTROL Set Return Path]** eine der folgenden Optionen:

      - `No` - (Empfohlene Sicherheitsmaßnahme) Routen gaben E-Mail an die Standard-E-Mail-Adresse des Stores zurück.
      - `Yes` - Routen geben E-Mail-Adresse an die Standard-Store-E-Mail-Adresse zurück.
      - `Specified` - Routen geben E-Mail an die in **[!UICONTROL Return Path Email]** angegebene E-Mail-Adresse zurück.

   - Bei Ausführung auf einem SMTP-Server konfigurieren Sie die Verbindung:

      - **[!UICONTROL Username]** - Geben Sie den Anmeldenamen des Benutzers für den SMTP-Server ein.
      - **[!UICONTROL Password]** - Geben Sie das Kennwort für die Anmeldung des SMTP-Servers ein.
      - **[!UICONTROL Auth]** - Wählen Sie den Authentifizierungstyp für die SMTP-Serververbindung aus: `NONE` , `PLAIN` oder `LOGIN`
      - **[!UICONTROL SSL]** - Wählen Sie den Verifizierungstyp für das Serversicherheitszertifikat aus: `SSL` oder `TLS`

     ![Erweiterte Konfiguration - Einstellungen für den E-Mail-Versand](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Sales Emails]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL General Settings]** .

1. Setzen Sie **[!UICONTROL Asynchronous sending]** auf `Enable`.

   ![Verkaufskonfiguration - Allgemeine E-Mail-Einstellungen](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Eine detaillierte Liste der Konfigurationseinstellungen finden Sie unter [_Allgemeine Einstellungen_](../configuration-reference/sales/sales-emails.md) in der _Konfigurationsreferenz_.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
