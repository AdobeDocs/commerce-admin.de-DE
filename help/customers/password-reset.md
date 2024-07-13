---
title: Zurücksetzen von Kundenkennwörtern
description: Kunden setzen ihre Passwörter in der Regel aus dem Storefront zurück, aber ein Store-Administrator kann entweder eine Kennwortzurücksetzung oder eine erzwungene Anmeldung vom Administrator einleiten.
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Zurücksetzen von Kundenkennwörtern

Kunden setzen ihre Kennwörter für gewöhnlich aus dem Schaufenster zurück, indem sie auf _[!UICONTROL Forgot Your Password?]_klicken. Der Store-Administrator kann jedoch entweder eine Kennwortrücksetzung oder eine erzwungene Anmeldung vom Administrator starten.

| Funktion | Beschreibung |
| --- | --- |
| Kennwort zurücksetzen | Eine E-Mail zum Zurücksetzen des Kennworts wird direkt an das E-Mail-Konto des Kunden gesendet. Der Store-Administrator kann keinen Zugriff auf das Kennwort des Kunden erhalten. |
| Anmeldung erzwingen | Ruft die OAuth-Zugriffstoken auf, die mit dem Kundenkonto verknüpft sind. Dies kann nur mit Kundenkonten verwendet werden, denen OAuth-Token im Rahmen einer Web-API [integration](../systems/integrations.md) zugewiesen wurden. Weitere Informationen finden Sie unter [OAuth-basierte Authentifizierung](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) in der Entwicklerdokumentation. <br/><br/>Standardmäßige Kundenkonten, die über die Storefront oder vom Administrator erstellt wurden, verfügen nicht über OAuth-Token. |

{style="table-layout:auto"}

## Zurücksetzen eines Kennworts aus der Storefront

1. Auf der Anmeldeseite klickt der Kunde auf **[!UICONTROL Forgot Your Password?]**.

1. Wenn Sie dazu aufgefordert werden, gibt den **[!UICONTROL Email Address]** ein, der mit ihrem Konto verknüpft ist, und klickt auf **[!UICONTROL Reset My Password]**.

   ![Kennwort vergessen](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >Wenn die eingegebene E-Mail-Adresse mit der des Kontos übereinstimmt, erhält der Kunde eine E-Mail-Benachrichtigung zur Passwortrücksetzbestätigung mit einem Link zum Zurücksetzen seines Kennworts.

1. Wenn die E-Mail ankommt, klickt der Kunde auf den Link _Passwort zurücksetzen_ und gibt seinen **[!UICONTROL New Password]** ein, wenn er dazu aufgefordert wird.

1. Fügt es erneut ein, um es zu bestätigen, und klickt auf **[!UICONTROL Reset Password]**.

   >[!IMPORTANT]
   >
   >Das neue Kennwort muss mindestens sechs Zeichen lang sein und darf keine Leerzeichen enthalten. Wenn er eine Bestätigung erhält, dass das Kennwort aktualisiert wurde, kann er sich mit dem neuen Kennwort bei seinem Konto anmelden. Standardmäßig ist der Link _Kennwort zurücksetzen_ 24 Stunden lang gültig.

## Zurücksetzen eines Kennworts vom Administrator

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie das Kundenkonto im Raster und klicken Sie in der Spalte _Aktion_ auf **[!UICONTROL Edit]** .

1. Klicken Sie im Satz der Optionen oben auf der Seite auf **[!UICONTROL Reset Password]**.

   Die Anzahl der Anforderungen zum Zurücksetzen des Kennworts, die innerhalb einer Stunde zulässig sind, wird im Thema [Konfiguration](../configuration-reference/customers/customer-configuration.md) festgelegt.

## OAuth-Token eines Kunden widerrufen

>[!IMPORTANT]
>
>Fahren Sie nur fort, wenn Sie mit der API-Authentifizierung vertraut sind.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie das Kundenkonto im Raster und klicken Sie in der Spalte _Aktion_ auf **[!UICONTROL Edit]** .

1. Klicken Sie im Satz der Optionen oben auf der Seite auf **[!UICONTROL Force Sign In]**.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **OK**.
