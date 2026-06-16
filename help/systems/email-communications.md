---
title: Konfigurieren von E-Mail-Nachrichten
description: Erfahren Sie, wie Sie E-Mail-Nachrichten konfigurieren, einschließlich des Routings zurückgegebener E-Mails oder Antworten auf eine bestimmte E-Mail-Adresse.
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
feature: Communications, Configuration
TQID: https://experienceleague.adobe.com/0spSxu59rF2KomOWVI5iR9pcg2r-VLm-GiXvJvatnww
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 310
ht-degree: 0%

---

# Konfigurieren von E-Mail-Nachrichten

Mit _E-Mail-_ können Sie zurückgegebene E-Mails oder Antworten auf E-Mails an eine bestimmte Adresse weiterleiten. Wenn Ihr Store auf einem SMTP- oder Windows-Server ausgeführt wird, können Sie die Host- und Port-Einstellungen überprüfen.

>[!IMPORTANT]
>
>**Sicherheitshinweis** Alle Händler sollten sofort ihre E-Mail-Versandkonfiguration einstellen, um sich vor einem kürzlich identifizierten potenziellen Remote-Code-Ausführungsangriff zu schützen. Solange dieses Problem nicht behoben ist, wird dringend empfohlen, [!DNL Sendmail] nicht für E-Mail-Nachrichten zu verwenden. Stellen Sie in der _[!UICONTROL Mail Sending Settings]_&#x200B;sicher, dass&#x200B;_[!UICONTROL Set Return Path]_ auf `No` gesetzt ist.

Eine detaillierte Liste der Konfigurationseinstellungen finden Sie unter [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) in der _Konfigurationsreferenz_.

## Konfigurieren von E-Mail-Nachrichten

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Mail Sending Settings]** und führen Sie folgende Schritte aus:

   ![Erweiterte Konfiguration - Einstellungen für den E-Mail-Versand](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - Falls erforderlich, setzen Sie **[!UICONTROL Disable Email Communications]** auf `No`.

   - Wählen Sie **[!UICONTROL Transport]** den Transporttyp für E-Mail-Nachrichten aus dem Store aus: `Sendmail` oder `SMTP`

   - Wenn er auf einem SMTP- oder Windows-Server ausgeführt wird, überprüfen Sie die folgenden Einstellungen:

      - **[!UICONTROL Host]** - `localhost` oder andere

      - **[!UICONTROL Port (25)]** - `25` oder andere

   - Wählen Sie **[!UICONTROL Set Return Path]** eine der folgenden Optionen:

      - `No` - (Empfohlene Sicherheitsmaßnahme) Routes hat die E-Mail an die Standard-Store-E-Mail-Adresse zurückgegeben.
      - `Yes` - Routet die zurückgegebene E-Mail an die Standard-Store-E-Mail-Adresse.
      - `Specified` - Routet die zurückgesendete E-Mail an die in **[!UICONTROL Return Path Email]** angegebene E-Mail-Adresse.

   - Konfigurieren Sie die Verbindung, wenn sie auf einem SMTP-Server ausgeführt wird:

      - **[!UICONTROL Username]** - Geben Sie den Anmeldenamen für den SMTP-Server ein.
      - **[!UICONTROL Password]** - Geben Sie das Passwort für die SMTP-Server-Anmeldung ein.
      - **[!UICONTROL Auth]** : Wählen Sie den Authentifizierungstyp für die SMTP-Server-Verbindung aus: `NONE` , `PLAIN` oder `LOGIN`
      - **[!UICONTROL SSL]** : Wählen Sie den Verifizierungstyp für das Server-Sicherheitszertifikat aus: `SSL` oder `TLS`

     ![Erweiterte Konfiguration - Einstellungen für den E-Mail-Versand](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Sales Emails]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL General Settings]** .

1. Legen Sie **[!UICONTROL Asynchronous sending]** auf `Enable` fest.

   ![Verkaufskonfiguration - Allgemeine E-Mail-Einstellungen](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Eine detaillierte Liste der Konfigurationseinstellungen finden Sie unter [_Allgemeine Einstellungen_](../configuration-reference/sales/sales-emails.md) in _Konfigurationsreferenz_.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
