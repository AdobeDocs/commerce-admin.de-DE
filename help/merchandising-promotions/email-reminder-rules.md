---
title: E-Mail-Erinnerungen
description: Erfahren Sie mehr über E-Mail-Erinnerungen, die automatisch an Kunden gesendet werden können, wenn bestimmte Bedingungen erfüllt sind.
exl-id: 3293caca-9dd3-4d64-a80c-58c92a9208e5
feature: Merchandising, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# E-Mail-Erinnerungen

{{ee-feature}}

Eine E-Mail-Erinnerung soll Personen, die Ihren Laden besucht haben, dazu anregen, von einer Promotion zu profitieren und einen Kauf zu tätigen. E-Mail-Erinnerungen können automatisch an Kunden gesendet werden, wenn bestimmte Bedingungen erfüllt sind. Sie können beispielsweise eine Erinnerung an Kunden senden, die etwas zu ihrem Warenkorb oder ihrer Wunschliste hinzugefügt, aber noch keinen Kauf getätigt haben. Sie können E-Mail-Erinnerungen verwenden, um Kunden dazu anzuregen, zu Ihrem Geschäft zurückzukehren und eine [Coupon-Code](price-rules-cart-coupon.md) als Anreiz. Gutscheincodes können automatisch für jeden Batch von E-Mail-Erinnerungen generiert werden, um Ihnen die Kontrolle über die Angebote zu geben, die mit jedem Batch verknüpft sind.

E-Mail-Erinnerungen können ausgelöst werden, nachdem eine bestimmte Anzahl von Tagen vergangen ist, seit ein Warenkorb abgebrochen wurde, oder für jede andere Bedingung, die Sie definieren möchten. Zu den gebräuchlichen Bedingungen gehören der Gesamtwert des Warenkorbs, die Menge, Artikel im Warenkorb usw.

>[!NOTE]
>
>Wenn einem Kunden mehr als eine übereinstimmende aufgegebene Warenkorb-, Wunschliste oder Kombination aus beiden vorliegt, wird die E-Mail-Erinnerung nur einmal für diesen Kunden ausgelöst. Um dieselbe E-Mail-Erinnerung erneut Trigger, verwenden Sie die _[!UICONTROL Repeat Schedule]_um die Anzahl der Tage zwischen E-Mails festzulegen.

![E-Mail-Erinnerungen](./assets/email-reminders.png){width="700" zoomable="yes"}

## E-Mail-Erinnerungen konfigurieren

E-Mail-Erinnerungsregeln können in regelmäßigen Abständen nach Minute, Stunde oder Tag gesendet werden. Die Konfiguration bestimmt, wie viele E-Mails in einem Batch gesendet werden, sowie die Store-Identität, die als Absender der Nachricht angezeigt wird.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen **[!UICONTROL Promotions]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Automated Email Reminder Rules]** und führen Sie folgende Schritte aus:

   ![Kundenkonfiguration - automatisierte E-Mail-Erinnerungsregeln](../configuration-reference/customers/assets/promotions-automated-email-reminder-rules.png){width="600" zoomable="yes"}

   - Satz **[!UICONTROL Enable Reminder Emails]** nach `Yes`.

   - Um festzulegen, wie oft Prüfungen für neue Kunden durchgeführt werden, die automatisierte E-Mail-Erinnerungen qualifizieren, legen Sie **[!UICONTROL Frequency]** auf einen der folgenden Werte zu:

      - `Minute Intervals`
      - `Hourly`
      - `Daily`

   - Legen Sie die entsprechende **[!UICONTROL Interval]**, basierend auf der _[!UICONTROL Frequency]_-Einstellung.

   - Satz **[!UICONTROL Start Time]** auf die Stunde, Minute und Sekunde, an der die E-Mail gesendet wird, basierend auf einer 24-Stunden-Zeit.

   - Um die Anzahl der E-Mails zu begrenzen, die in einem Batch gesendet werden können, geben Sie die Zahl in **[!UICONTROL Maximum Emails per One Run]** -Feld.

   - Um wiederholte Versuche zum Senden fehlgeschlagener E-Mails zu vermeiden, geben Sie die maximale Anzahl von Versuchen in die **[!UICONTROL Email Send Failure Threshold]** -Feld.

   - Satz **[!UICONTROL Reminder Email Sender]** der [Store-Kontakt](../getting-started/store-details.md#store-email-addresses) , der als Absender der Erinnerungsmail angezeigt wird.

   Eine detaillierte Liste dieser Optionen finden Sie unter [Automatisierte E-Mail-Erinnerungsregeln](../configuration-reference/customers/promotions.md#automated-email-reminder-rules) im _Konfigurationsreferenz_.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## E-Mail-Erinnerungsvorlagen

Die Standard-E-Mail-Erinnerungsvorlage kann angepasst und zusätzliche Vorlagen für verschiedene Promotions erstellt werden. E-Mail-Erinnerungen verfügen über eine Auswahl spezifischer Variablen, die in die Nachricht integriert werden können. Die Informationen in diesen Variablen werden durch die von Ihnen eingerichtete E-Mail-Erinnerungsregel und die mit dem Gutschein verknüpfte Warenkorbpreisregel bestimmt. Mit der Schaltfläche Variable einfügen können Sie das Markup-Tag mit der Variablen in die Vorlage einfügen. Weitere Informationen finden Sie unter [Email](../systems/email-templates.md).

![E-Mail-Erinnerungsvorschau](./assets/email-reminder-preview-promotion-template.png){width="600" zoomable="yes"}

### E-Mail-Erinnerungsvorlage anpassen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Klicken **[!UICONTROL Add New Template]**.

1. Im **[!UICONTROL Template]** Liste unter `Magento_Reminder`, wählen Sie die **[!UICONTROL Promotion Notification/Reminder]** Vorlage.

1. Klicken **[!UICONTROL Load Template]**.

Befolgen Sie den Standard [instructions](../systems/email-template-custom.md) , um die Vorlage anzupassen.

### E-Mail-Erinnerungsvariablen

#### Coupon-Code

```
{{var coupon.getCode()|escape}}
```

#### Verwendungsgrenze des Gutscheins

```
{{var coupon.usage_limit|escape}}
```

#### Nutzung des Gutscheins pro Kunde

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

#### Email Footer Template

```
{{template config_path="design/email/footer_template"}}
```

#### Email Header Template

```
{{template config_path="design/email/header_template"}}
```

#### Bild-Alt für E-Mail-Logo

```
{{var logo_alt}}
```

#### URL des E-Mail-Logos

```
{{var logo_url}}
```

#### Beschreibung der Werbeaktion

```
{{var promotion_description|escape|nl2br}}
```

#### Name der Promotion

```
{{var promotion_name|escape}}
```

#### Speichername

```
{{var store.frontend_name}}
```

#### Store-URL

```
{{store url=""}}
```
