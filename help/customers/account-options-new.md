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

Im Abschnitt _[!UICONTROL Create New Account Options]_der Konfiguration werden die grundlegenden Kontooptionen mit erweiterten Optionen kombiniert, die sich auf die Validierung der MwSt.-ID und benutzerdefinierte Integrationen beziehen. Die folgenden Anweisungen decken nur die am häufigsten verwendeten Optionen ab. Informationen zu automatischen Kundengruppenzuweisungen finden Sie unter [MwSt.-Validierung](../stores-purchase/vat.md).

![Neue Kontooptionen erstellen](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## Einrichten der grundlegenden Optionen für das Kundenkonto

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Customer Configuration]**.

1. Erweitern Sie den Abschnitt **[!UICONTROL Create New Account Options]** :

   ![Standardeinstellungen für Optionen für neues Konto erstellen](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. Legen Sie jede der Optionen entsprechend dem Kundenerlebnis fest, das Sie in Ihrer Storefront unterstützen müssen:

   - Legen Sie **[!UICONTROL Default Group]** auf die Kundengruppe fest, die neuen Kunden zugewiesen wird, wenn ein Konto erstellt wird.

   - Wenn Sie eine _Umsatzsteuer_-Nummer haben und diese für Kunden sichtbar sein soll, setzen Sie **[!UICONTROL Show VAT Number on Storefront]** auf `Yes`.

   - Um die E-Mail-Adresse eines Kunden während der Erstellung einer Admin-Bestellung für einen Kunden anzufordern, setzen Sie **[!UICONTROL Email is required field for Admin order creation]** auf `Yes`.

   - Geben Sie die **[!UICONTROL Default Email Domain]** für den Store ein, z. B. `mystore.com`

   - Legen Sie **[!UICONTROL Default Welcome Email]** auf die Vorlage fest, die für die Begrüßungs-E-Mail verwendet wird, die an neue Kundinnen und Kunden gesendet wird.

   - Wenn Sie Kunden auffordern möchten, ihre Anforderung zum Öffnen eines Kontos in Ihrem Geschäft zu bestätigen, setzen Sie **[!UICONTROL Require Emails Confirmation]** auf `Yes`. Legen Sie dann **[!UICONTROL Confirmation Link Email]** auf die Vorlage fest, die für die Bestätigungs-E-Mail verwendet wird.

     >[!NOTE]
     >
     >Ab Version 2.4.7 müssen Kundinnen und Kunden unabhängig vom Browser ihre E-Mail-Adresse und ihr Passwort erneut eingeben, um sich nach der E-Mail-Bestätigung bei ihrem Konto anzumelden.

   - Legen Sie **[!UICONTROL Welcome Email]** auf die Vorlage fest, die für die Begrüßungsnachricht verwendet wird, die gesendet wird, nachdem das Konto bestätigt wurde.

   - Legen Sie **[!UICONTROL Default Welcome Email without Password]** auf die Vorlage fest, die verwendet wird, wenn ein Kundenkonto erstellt wird, das noch kein Kennwort hat. Einem von Admin erstellten Kundenkonto wurde beispielsweise noch kein Passwort zugewiesen.

   - Legen Sie **[!UICONTROL Email Sender]** auf den Store-Kontakt fest, der als Absender der Begrüßungs-E-Mail angezeigt wird.

   - Wenn Sie Kunden auffordern möchten, ihre Anforderung zum Öffnen eines Kontos in Ihrem Geschäft zu bestätigen, setzen Sie **[!UICONTROL Require Emails Confirmation]** auf `Yes`. Legen Sie dann **[!UICONTROL Confirmation Link Email]** auf die Vorlage fest, die für die Bestätigungs-E-Mail verwendet wird.

   ![Erstellen neuer Kontooptionen mit aktivierter MwSt.-Nummer](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

   Detaillierte Informationen zu den einzelnen in diesem Konfigurationsoptionssatz verfügbaren Optionen finden Sie unter _Neue Kontooptionen erstellen_ [Konfigurationsreferenz](../configuration-reference/customers/customer-configuration.md).

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
