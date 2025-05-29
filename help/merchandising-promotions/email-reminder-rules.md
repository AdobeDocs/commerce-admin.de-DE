---
title: E-Mail-Erinnerungen
description: Erfahren Sie mehr über E-Mail-Erinnerungen, die automatisch an Kunden gesendet werden können, wenn ein bestimmter Satz von Bedingungen erfüllt ist.
exl-id: 3293caca-9dd3-4d64-a80c-58c92a9208e5
feature: Merchandising, Communications
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# E-Mail-Erinnerungen

{{ee-feature}}

Der Zweck einer E-Mail-Erinnerung ist es, Personen, die Ihren Shop besucht haben, dazu zu ermutigen, eine Promotion zu nutzen und einen Kauf zu tätigen. E-Mail-Erinnerungen können automatisch an Kunden gesendet werden, wenn ein bestimmter Satz von Bedingungen erfüllt ist. Beispielsweise können Sie eine Erinnerung an Kunden senden, die etwas zum Warenkorb oder zur Wunschliste hinzugefügt, aber noch keinen Kauf getätigt haben. Sie können E-Mail-Erinnerungen verwenden, um Kundinnen und Kunden zur Rückkehr in Ihr Geschäft zu ermutigen, und einen [Gutscheincode](price-rules-cart-coupon.md) als Anreiz angeben. Couponcodes können automatisch für jeden Batch von E-Mail-Erinnerungen generiert werden, um Ihnen die Kontrolle über die Angebote zu geben, die jedem Batch zugeordnet sind.

E-Mail-Erinnerungen können ausgelöst werden, nachdem eine bestimmte Anzahl von Tagen seit dem Verlassen eines Warenkorbs vergangen ist oder für eine beliebige andere Bedingung, die Sie definieren möchten. Häufige Bedingungen umfassen den Gesamtwert für den Warenkorb, die Menge, die Artikel im Warenkorb usw.

>[!NOTE]
>
>Wenn ein Kunde über mehr als einen übereinstimmenden, nicht mehr in den Warenkorb gelegten Warenkorb, eine Wunschliste oder eine Kombination aus beidem verfügt, wird die E-Mail-Erinnerung nur einmal für diesen Kunden ausgelöst. Um dieselbe E-Mail-Erinnerung erneut Trigger, legen Sie im Feld _[!UICONTROL Repeat Schedule]_&#x200B;die Anzahl der Tage zwischen den E-Mails fest.

![E-Mail-Erinnerungen](./assets/email-reminders.png){width="700" zoomable="yes"}

## Konfigurieren von E-Mail-Erinnerungen

E-Mail-Erinnerungsregeln können in regelmäßigen Abständen nach Minute, Stunde oder Tag gesendet werden. Die Konfiguration bestimmt, wie viele E-Mails in einem Batch gesendet werden, und die Speicheridentität, die als Absender der Nachricht angezeigt wird.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Promotions]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Automated Email Reminder Rules]** und führen Sie folgende Schritte aus:

   ![Kundenkonfiguration - Regeln für automatische E-Mail-Erinnerungen](../configuration-reference/customers/assets/promotions-automated-email-reminder-rules.png){width="600" zoomable="yes"}

   - Legen Sie **[!UICONTROL Enable Reminder Emails]** auf `Yes` fest.

   - Um festzulegen, wie oft Prüfungen für neue Kunden durchgeführt werden sollen, die sich für automatische E-Mail-Erinnerungen qualifizieren, **[!UICONTROL Frequency]** Sie auf einen der folgenden Werte:

      - `Minute Intervals`
      - `Hourly`
      - `Daily`

   - Legen Sie die entsprechende **[!UICONTROL Interval]** basierend auf der _[!UICONTROL Frequency]_&#x200B;fest.

   - Legen Sie **[!UICONTROL Start Time]** auf die Stunde, Minute und Sekunde fest, zu der die E-Mail gesendet wird, basierend auf einer 24-Stunden-Zeit.

   - Geben Sie die Zahl in das Feld **[!UICONTROL Maximum Emails per One Run]** ein, um die Anzahl der E-Mails zu begrenzen, die in einem Batch gesendet werden können.

   - Um wiederholte Versandversuche für fehlgeschlagene E-Mails zu vermeiden, geben Sie die maximale Anzahl an Versandversuchen in das Feld **[!UICONTROL Email Send Failure Threshold]** ein.

   - Legen Sie **[!UICONTROL Reminder Email Sender]** auf den [Store-Kontakt](../getting-started/store-details.md#store-email-addresses) fest, der als Absender der Erinnerungs-E-Mail angezeigt wird.

   Eine detaillierte Liste dieser Optionen finden Sie unter [Regeln für automatisierte E-Mail](../configuration-reference/customers/promotions.md#automated-email-reminder-rules) in _Konfigurationsreferenz_.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## E-Mail-Erinnerungsvorlagen

Die standardmäßige E-Mail-Erinnerungsvorlage kann angepasst und zusätzliche Vorlagen für verschiedene Promotions erstellt werden. E-Mail-Erinnerungen verfügen über eine Auswahl bestimmter Variablen, die in die Nachricht integriert werden können. Die Informationen in diesen Variablen werden durch die von Ihnen eingerichtete E-Mail-Erinnerungsregel und die mit dem Coupon verknüpfte Warenkorbpreisregel bestimmt. Mit der Schaltfläche „Variable einfügen“ können Sie das Markup-Tag mit der Variablen in die Vorlage einfügen. Weitere Informationen finden Sie unter [Email](../systems/email-templates.md).

![E-Mail-Erinnerungsvorschau](./assets/email-reminder-preview-promotion-template.png){width="600" zoomable="yes"}

### Anpassen einer E-Mail-Erinnerungsvorlage

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Klicken Sie auf **[!UICONTROL Add New Template]**.

1. Wählen Sie in der **[!UICONTROL Template]** unter `Magento_Reminder` die **[!UICONTROL Promotion Notification/Reminder]** Vorlage aus.

1. Klicken Sie auf **[!UICONTROL Load Template]**.

Befolgen Sie die [Anweisungen](../systems/email-template-custom.md), um die Vorlage anzupassen.

### E-Mail-Erinnerungsvariablen

#### Couponcode

```
{{var coupon.getCode()|escape}}
```

#### Couponnutzung

```
{{var coupon.usage_limit|escape}}
```

#### Couponnutzung pro Kunde

```
{{var coupon.usage_per_customer|escape}}
```

#### Kundenkonto-URL

```
{{var this.getUrl($store,'customer/account/',[_nosid:1])}}
```

#### Kundenname

```
{{var customer_data.name|escape}}
```

#### E-Mail-Fußzeilen-Vorlage

```
{{template config_path="design/email/footer_template"}}
```

#### E-Mail-Header-Vorlage

```
{{template config_path="design/email/header_template"}}
```

#### E-Mail-Logo Bild Alt

```
{{var logo_alt}}
```

#### URL des E-Mail-Logos

```
{{var logo_url}}
```

#### Beschreibung der Promotion

```
{{var promotion_description|escape|nl2br}}
```

#### Name der Promotion

```
{{var promotion_name|escape}}
```

#### Name speichern

```
{{var store.frontend_name}}
```

#### URL speichern

```
{{store url=""}}
```
