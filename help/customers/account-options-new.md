---
title: Optionen für neues Kundenkonto
description: Erfahren Sie mehr über die Konfigurationsoptionen für neue Kundenkonten in Ihrem Geschäft.
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Optionen für neues Kundenkonto

In der _[!UICONTROL Create New Account Options]_Im Abschnitt der Konfiguration werden die grundlegenden Kontooptionen mit erweiterten Optionen kombiniert, die sich auf die Validierung der MwSt.-ID und benutzerdefinierte Integrationen beziehen. Die folgenden Anweisungen decken nur die am häufigsten verwendeten Optionen ab. Weitere Informationen zu automatischen Kundengruppenzuweisungen finden Sie unter [Validierung der MwSt](../stores-purchase/vat.md).

![Neue Kontooptionen erstellen](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## Einrichten der grundlegenden Optionen für das Kundenkonto

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich . **[!UICONTROL Customers]** und wählen **[!UICONTROL Customer Configuration]**.

1. Erweitern Sie die **[!UICONTROL Create New Account Options]** Bereich:

   ![Standardeinstellungen für Optionen für neues Konto erstellen](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. Legen Sie jede der Optionen entsprechend dem Kundenerlebnis fest, das Sie in Ihrer Storefront unterstützen müssen:

   - set **[!UICONTROL Default Group]** der Kundengruppe, die neuen Kunden bei der Kontoerstellung zugewiesen wird.

   - Wenn Sie eine _Mehrwertsteuer_ und für Kunden sichtbar sein sollen, setzen Sie **[!UICONTROL Show VAT Number on Storefront]** bis `Yes`.

   - Um die E-Mail-Adresse eines Kunden während der Erstellung einer Admin-Bestellung für einen Kunden anzufordern, legen Sie Folgendes fest: **[!UICONTROL Email is required field for Admin order creation]** bis `Yes`.

   - Geben Sie die **[!UICONTROL Default Email Domain]** für den Store, z. B. `mystore.com`

   - set **[!UICONTROL Default Welcome Email]** zur Vorlage, die für die Begrüßungs-E-Mail verwendet wird, die an neue Kunden gesendet wird.

   - Um Kundinnen und Kunden aufzufordern, ihre Anfrage zur Eröffnung eines Kontos bei Ihrem Geschäft zu bestätigen, legen Sie Folgendes fest **[!UICONTROL Require Emails Confirmation]** bis `Yes`. Legen Sie dann fest **[!UICONTROL Confirmation Link Email]** in die Vorlage, die für die Bestätigungs-E-Mail verwendet wird.

     >[!NOTE]
     >
     >Ab Version 2.4.7 müssen Kundinnen und Kunden unabhängig vom Browser ihre E-Mail-Adresse und ihr Passwort erneut eingeben, um sich nach der E-Mail-Bestätigung bei ihrem Konto anzumelden.

   - set **[!UICONTROL Welcome Email]** zur Vorlage, die für die Begrüßungsnachricht verwendet wird, die nach der Bestätigung des Kontos gesendet wird.

   - set **[!UICONTROL Default Welcome Email without Password]** zu der Vorlage hinzufügen, die verwendet wird, wenn ein Kundenkonto erstellt wird, das noch kein Kennwort hat. Einem Kundenkonto, das über die Administratorrechte erstellt wurde, wurde beispielsweise noch kein Kennwort zugewiesen.

   - set **[!UICONTROL Email Sender]** an den Store-Kontakt, der als Absender der Willkommens-E-Mail angezeigt wird.

   - Um Kundinnen und Kunden aufzufordern, ihre Anfrage zur Eröffnung eines Kontos bei Ihrem Geschäft zu bestätigen, legen Sie Folgendes fest **[!UICONTROL Require Emails Confirmation]** bis `Yes`. Legen Sie dann fest **[!UICONTROL Confirmation Link Email]** in die Vorlage, die für die Bestätigungs-E-Mail verwendet wird.

   ![Neue Kontooptionen mit aktivierter MwSt. erstellen](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

   Detaillierte Informationen zu den einzelnen in diesem Konfigurationssatz verfügbaren Optionen finden Sie unter _Neue Kontooptionen erstellen_ [Konfigurationsreferenz](../configuration-reference/customers/customer-configuration.md).

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
