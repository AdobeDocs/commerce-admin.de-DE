---
title: Neue Optionen für Kundenkonten
description: Erfahren Sie mehr über die Konfigurationsoptionen für neue Kundenkonten in Ihrem Store.
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Neue Optionen für Kundenkonten

Im Abschnitt _[!UICONTROL Create New Account Options]_der Konfiguration werden die grundlegenden Kontooptionen mit erweiterten Optionen kombiniert, die sich auf die Überprüfung der MwSt-ID und benutzerdefinierte Integrationen beziehen. Die folgenden Anweisungen behandeln nur die am häufigsten verwendeten Optionen. Weitere Informationen zur automatischen Zuweisung von Kundengruppen finden Sie unter [Mehrwertsteuervalidierung](../stores-purchase/vat.md).

![Neue Kontooptionen erstellen](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## Einrichten der grundlegenden Kundenkontooptionen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Customer Configuration]** aus.

1. Erweitern Sie den Abschnitt **[!UICONTROL Create New Account Options]** :

   ![Standardeinstellungen für neue Kontooptionen erstellen](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. Legen Sie die einzelnen Optionen entsprechend dem Kundenerlebnis fest, das Sie in Ihrer Storefront unterstützen müssen:

   - Setzen Sie **[!UICONTROL Default Group]** auf die Kundengruppe, die neuen Kunden bei der Erstellung eines Kontos zugewiesen wird.

   - Wenn Sie eine _Wertzuwachs-Steuer_ -Nummer haben und möchten, dass sie für Kunden sichtbar ist, setzen Sie **[!UICONTROL Show VAT Number on Storefront]** auf `Yes`.

   - Wenn Sie die E-Mail eines Kunden bei der Erstellung einer Admin-Bestellung für einen Kunden benötigen möchten, setzen Sie **[!UICONTROL Email is required field for Admin order creation]** auf `Yes`.

   - Geben Sie den **[!UICONTROL Default Email Domain]** für den Store ein, z. B. `mystore.com`

   - Setzen Sie **[!UICONTROL Default Welcome Email]** auf die Vorlage, die für die Begrüßungs-E-Mail verwendet wird, die an neue Kunden gesendet wird.

   - Damit Kunden ihre Anfrage bestätigen müssen, ein Konto bei Ihrem Store zu öffnen, setzen Sie **[!UICONTROL Require Emails Confirmation]** auf `Yes`. Setzen Sie dann **[!UICONTROL Confirmation Link Email]** auf die Vorlage, die für die Bestätigungs-E-Mail verwendet wird.

     >[!NOTE]
     >
     >Ab Version 2.4.7 müssen Kunden ihre E-Mail-Adresse und ihr Kennwort erneut eingeben, um sich nach einer E-Mail-Bestätigung bei ihrem Konto anzumelden, unabhängig vom Browser.

   - Setzen Sie **[!UICONTROL Welcome Email]** auf die Vorlage, die für die Willkommensnachricht verwendet wird, die nach der Bestätigung des Kontos gesendet wird.

   - Setzen Sie **[!UICONTROL Default Welcome Email without Password]** auf die Vorlage, die verwendet wird, wenn ein Kundenkonto erstellt wird, das noch kein Kennwort hat. Beispielsweise ist einem vom Administrator erstellten Kundenkonto noch kein Kennwort zugewiesen.

   - Setzen Sie **[!UICONTROL Email Sender]** auf den Store-Kontakt, der als Absender der Begrüßungs-E-Mail angezeigt wird.

   - Damit Kunden ihre Anfrage bestätigen müssen, ein Konto bei Ihrem Store zu öffnen, setzen Sie **[!UICONTROL Require Emails Confirmation]** auf `Yes`. Setzen Sie dann **[!UICONTROL Confirmation Link Email]** auf die Vorlage, die für die Bestätigungs-E-Mail verwendet wird.

   ![Neue Kontooptionen mit aktivierter Mehrwertsteuer erstellen](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

   Ausführliche Informationen zu den einzelnen Optionen, die in diesem Konfigurationssatz verfügbar sind, finden Sie in der Konfigurationsreferenz _Neue Kontooptionen erstellen_ [3}.](../configuration-reference/customers/customer-configuration.md)

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
