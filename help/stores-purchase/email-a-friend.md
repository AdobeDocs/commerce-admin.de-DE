---
title: Freund per E-Mail benachrichtigen
description: Erfahren Sie, wie Sie einen E-Mail-Link bereitstellen, mit dem Ihre Kunden Links zu Produkten für ihre Freunde freigeben können.
exl-id: 46cf9994-6490-4cb4-85b7-9a7cab7783e0
feature: Storefront, Configuration
TQID: https://experienceleague.adobe.com/a75E4X5mTDXeCQKysvIecdU3OhsICiWTtwh7k-oK9cw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 0%

---

# Freund per E-Mail benachrichtigen

Der E-Mail-Link erleichtert es Ihren Kunden, Links zu Produkten für ihre Freunde freizugeben. Im Demo-Luma-Store wird der E-Mail-Link als Umschlagsymbol angezeigt. Die Nachrichtenvorlage kann für Ihre Stimme und Marke angepasst werden. Um Spamming zu verhindern, können Sie die Anzahl der Empfänger für jede E-Mail und die Anzahl der Produkte, die über einen Zeitraum von einer Stunde geteilt werden können, begrenzen.

![Beispiel einer Storefront - E-Mail an einen Freund](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## Konfigurieren von email-a-friend

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie **[!UICONTROL Email to a Friend]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Email Templates]** und legen Sie die Optionen fest:

   ![Katalogkonfiguration - E-Mail-Vorlagen](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung jeder dieser Konfigurationseinstellungen finden Sie unter [E-Mail-](../configuration-reference/catalog/email-to-a-friend.md)) im _Konfigurationsreferenzhandbuch_.

   Um die Standardeinstellung eines Felds zu ändern, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** , damit das Feld bearbeitet werden kann.

   - Legen Sie **[!UICONTROL Enabled]** auf `Yes` fest.

   - Legen Sie **[!UICONTROL Select Email Template]** auf die Vorlage fest, die Sie als Grundlage für die Nachrichten verwenden möchten.

   - Wenn Sie verlangen möchten, dass nur registrierte Kunden E-Mails an Freunde senden können, setzen Sie **[!UICONTROL Allow for Guests]** auf `No`.

   - Geben Sie **[!UICONTROL Max Recipients]** die maximale Anzahl an Freunden ein, die sich für eine einzelne Nachricht auf der Verteilerliste befinden dürfen.

   - Geben Sie **[!UICONTROL Max Products Sent in 1 Hour]** die maximale Anzahl von Produkten ein, die von einem einzelnen Benutzer mit Freunden über einen Zeitraum von einer Stunde geteilt werden können.

   - Legen Sie **[!UICONTROL Limit Sending By]** auf eine der folgenden Methoden fest, um den Absender von E-Mails zu identifizieren:

     `IP Address` - (Empfohlen) Identifiziert den Absender anhand der IP-Adresse des Computers, der zum Senden der E-Mails verwendet wird.

     `Cookie (unsafe)` - Identifiziert den Absender anhand des Browser-Cookies. Diese Methode ist weniger effektiv, da der Absender das Cookie löschen kann, um das Limit zu umgehen.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## E-Mail an einen Freund in der Storefront senden

Wenn diese Funktion konfiguriert ist, führen Store-Kunden diese Schritte aus, um Produktinformationen für Freunde freizugeben.

1. Auf einer Katalogseite klickt der Kunde auf den Link **[!UICONTROL Email]** .

1. Wenn die Funktion nur für registrierte Benutzer konfiguriert ist, führt eine der folgenden Aktionen aus:

   - Melden Sie sich bei Ihrem Kundenkonto an.
   - Meldet sich für ein neues Konto an.

1. Schließt die **[!UICONTROL Message]** ab und gibt die **[!UICONTROL Name]** und **[!UICONTROL Email Address]** der Empfänger ein.

   Bei Bedarf kann der Kunde weitere Empfänger hinzufügen:

   - Klicks **[!UICONTROL Add Invitee]**.

   - Gibt den **[!UICONTROL Name]** und die **[!UICONTROL Email Address]** der zusätzlichen Person an.

     Sie können die Nachricht an so viele zusätzliche Personen senden, wie die Konfiguration zulässt. Sie können die hinzugefügten Einladungen entfernen, indem sie auf den Link **[!DNL Remove]** klicken.

1. Wenn Sie bereit sind, die Nachricht zu senden, klicken Sie auf **[!UICONTROL Send Email]**.

   ![Beispiel einer Storefront - E-Mail an einen Freund](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}
