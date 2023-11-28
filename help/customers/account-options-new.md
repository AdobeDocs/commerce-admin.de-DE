---
title: Neue Optionen für Kundenkonten
description: Erfahren Sie mehr über die Konfigurationsoptionen für neue Kundenkonten in Ihrem Store.
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Neue Optionen für Kundenkonten

Im _[!UICONTROL Create New Account Options]_-Abschnitt der Konfiguration werden die grundlegenden Kontooptionen mit erweiterten Optionen kombiniert, die sich auf die Überprüfung der MwSt-ID und benutzerdefinierte Integrationen beziehen. Die folgenden Anweisungen behandeln nur die am häufigsten verwendeten Optionen. Weitere Informationen zu automatischen Kundengruppenzuweisungen finden Sie unter [Mehrwertsteuervalidierung](../stores-purchase/vat.md).

{{beta-updates}}

![Neue Kontooptionen erstellen](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## Einrichten der grundlegenden Kundenkontooptionen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen **[!UICONTROL Customer Configuration]**.

1. Erweitern Sie die **[!UICONTROL Create New Account Options]** Abschnitt:

   ![Standardeinstellungen für neue Kontooptionen erstellen](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. Legen Sie die einzelnen Optionen entsprechend dem Kundenerlebnis fest, das Sie in Ihrer Storefront unterstützen müssen:

   - Satz **[!UICONTROL Default Group]** der Kundengruppe, die bei der Erstellung eines Kontos neuen Kunden zugewiesen wird.

   - Wenn Sie _Mehrwertsteuer_ number und möchten, dass sie für Kunden sichtbar ist, legen Sie **[!UICONTROL Show VAT Number on Storefront]** nach `Yes`.

   - Um die E-Mail eines Kunden bei der Erstellung einer Admin-Bestellung für einen Kunden zu benötigen, legen Sie **[!UICONTROL Email is required field for Admin order creation]** nach `Yes`.

   - Geben Sie die **[!UICONTROL Default Email Domain]** für den Store, beispielsweise `mystore.com`

   - Satz **[!UICONTROL Default Welcome Email]** der Vorlage, die für die an neue Kunden gesendete Begrüßungs-E-Mail verwendet wird.

   - Satz **[!UICONTROL Default Welcome Email without Password]** in die Vorlage, die verwendet wird, wenn ein Kundenkonto erstellt wird, das noch kein Kennwort hat. Beispielsweise ist einem vom Administrator erstellten Kundenkonto noch kein Kennwort zugewiesen.

   - Satz **[!UICONTROL Email Sender]** an den Store-Kontakt, der als Absender der Begrüßungs-E-Mail angezeigt wird.

   - Wenn Kunden aufgefordert werden sollen, ihre Anfrage zum Öffnen eines Kontos für Ihren Store zu bestätigen, legen Sie **[!UICONTROL Require Emails Confirmation]** nach `Yes`. Legen Sie anschließend **[!UICONTROL Confirmation Link Email]** der Vorlage, die für die Bestätigungs-E-Mail verwendet wird.

   - Satz **[!UICONTROL Welcome Email]** der Vorlage, die für die Willkommensnachricht verwendet wird, die nach der Bestätigung des Kontos gesendet wird.

     ![Neue Kontooptionen mit aktivierter Mehrwertsteuer erstellen](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

     Detaillierte Informationen zu den einzelnen in diesem Konfigurationssatz verfügbaren Optionen finden Sie in der _Neue Kontooptionen erstellen_ [Konfigurationsreferenz](../configuration-reference/customers/customer-configuration.md).

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
