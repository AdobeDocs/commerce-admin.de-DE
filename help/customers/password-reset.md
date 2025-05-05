---
title: Kundenkennwörter zurücksetzen
description: Kunden setzen ihre Kennwörter in der Regel über die Storefront zurück, aber ein Store-Administrator kann entweder ein Zurücksetzen des Kennworts oder eine erzwungene Anmeldung vom Administrator einleiten.
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Kundenkennwörter zurücksetzen

Kunden setzen ihre Kennwörter in der Regel aus der Storefront zurück, indem sie auf _[!UICONTROL Forgot Your Password?]_&#x200B;klicken. Der Store-Administrator kann jedoch entweder das Zurücksetzen des Kennworts oder eine erzwungene Anmeldung vom Administrator initiieren.

| Funktion | Beschreibung |
| --- | --- |
| Passwort zurücksetzen | Eine E-Mail zum Zurücksetzen des Kennworts wird direkt an das E-Mail-Konto des Kunden gesendet. Der Store-Administrator kann keinen Zugriff auf das Kennwort des Kunden erhalten. |
| Anmeldung erzwingen | Widerruft die OAuth-Zugriffstoken, die mit dem Kundenkonto verknüpft sind. Dies kann nur mit Kundenkonten verwendet werden, denen OAuth-Token als Teil einer Web-API ([) zugewiesen ](../systems/integrations.md). Weitere Informationen finden Sie unter [OAuth-basierte Authentifizierung](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) in der Entwicklerdokumentation. <br/><br/>Standardkundenkonten, die aus der Storefront oder vom Administrator erstellt wurden, haben keine OAuth-Token. |

{style="table-layout:auto"}

## Zurücksetzen eines Kennworts aus der Storefront

1. Auf der Anmeldeseite klickt der Kunde auf **[!UICONTROL Forgot Your Password?]**.

1. Wenn Sie dazu aufgefordert werden, geben Sie die **[!UICONTROL Email Address]** ein, die mit ihrem Konto verknüpft ist, und klicken Sie auf **[!UICONTROL Reset My Password]**.

   ![Kennwort vergessen](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >Wenn die eingegebene E-Mail-Adresse mit der dem Konto zugeordneten übereinstimmt, erhält der Kunde eine E-Mail zur Bestätigung des Kennwortzurücksetzens mit einem Link zum Zurücksetzen seines Kennworts.

1. Wenn die E-Mail eingeht, klickt der Kunde auf den Link _Kennwort zurücksetzen_ und gibt bei Aufforderung seinen **[!UICONTROL New Password]** ein.

1. Geben Sie sie zur Bestätigung erneut ein und klicken Sie auf **[!UICONTROL Reset Password]**.

   >[!IMPORTANT]
   >
   >Das neue Kennwort muss mindestens sechs Zeichen lang sein und keine Leerzeichen enthalten. Wenn sie die Bestätigung erhalten, dass das Kennwort aktualisiert wurde, können sie das neue Kennwort verwenden, um sich bei ihrem Konto anzumelden. Standardmäßig ist der Link _Kennwort zurücksetzen_ 24 Stunden lang gültig.

## Zurücksetzen eines Kennworts über den Administrator

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie das Kundenkonto im Raster und klicken Sie in der Spalte _Aktion_ auf **[!UICONTROL Edit]**.

1. Klicken Sie in den Optionen oben auf der Seite auf **[!UICONTROL Reset Password]**.

   Die Anzahl der Anfragen zum Zurücksetzen des Kennworts, die innerhalb einer Stunde zulässig sind, wird im Thema [Konfiguration](../configuration-reference/customers/customer-configuration.md) festgelegt.

## Widerrufen der OAuth-Token eines Kunden

>[!IMPORTANT]
>
>Fahren Sie nicht fort, es sei denn, Sie kennen die API-Authentifizierung vollständig.

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie das Kundenkonto im Raster und klicken Sie in der Spalte _Aktion_ auf **[!UICONTROL Edit]**.

1. Klicken Sie in den Optionen oben auf der Seite auf **[!UICONTROL Force Sign In]**.

1. Wenn Sie zur Bestätigung aufgefordert werden, klicken Sie auf **OK**.
