---
title: E-Mail-Erinnerungen erstellen
description: Erfahren Sie, wie Sie eine E-Mail-Erinnerungsregel einrichten, die eine vorhandene Warenkorb-Preisregel verwendet.
exl-id: b04dc8a3-5daa-43f2-bf52-d85bfd2554b7
feature: Merchandising, Communications
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# E-Mail-Erinnerungen erstellen

Bevor Sie eine E-Mail-Erinnerungsregel einrichten, müssen Sie zunächst [Warenkorb-Preisregel einrichten](price-rules-cart-create.md) um die angebotene Promotion zu definieren. Regelbedingungen, die den Trigger einer E-Mail-Erinnerung ermöglichen, können auf Warenkorbeigenschaften, Wunschlisteneigenschaften oder beidem basieren.

>[!NOTE]
>
>E-Mail-Erinnerungen fördern möglicherweise eine Warenkorb-Preisregel mit oder ohne Coupon. Eine Warenkorb-Preisregel, die einen automatisch generierten Coupon definiert, generiert einen zufälligen Couponcode für jeden Kunden.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Reminder Rules]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add New Rule]**.

1. Vervollständigen Sie die _[!UICONTROL Rule Information]_&#x200B;wie folgt:

   ![E-Mail-Erinnerungsregel](./assets/email-reminder-new.png){width="700" zoomable="yes"}

   - Geben Sie einen **[!UICONTROL Rule Name]** ein, um die Regel intern zu identifizieren.

   - Geben Sie einen kurzen **[!UICONTROL Description]** der Regel ein.

   - Um die **[!UICONTROL Cart Price Rule]** Promotion auszuwählen, für die diese Erinnerung angekündigt werden soll, klicken Sie auf **[!UICONTROL Select Rule…]** und wählen Sie die Regel aus.

     ![Warenkorbregel - Auswählen](./assets/email-reminder-select-rule.png){width="600" zoomable="yes"}

   - Wenn die Regel sofort in Kraft treten soll, setzen Sie **[!UICONTROL Status]** auf `Active`.

   - Um einen Datumsbereich einzurichten, in dem die Regel aktiv sein soll, geben Sie das **[!UICONTROL From]** und **[!UICONTROL To]** ein.

     Sie können das Datum auch im Kalender auswählen ( ![Kalendersymbol](../assets/icon-calendar.png) ).

   - Um die Erinnerung mehr als einmal zu senden, geben Sie die Anzahl der Tage vor der nächsten E-Mail-Explosion in das Feld **[!UICONTROL Repeat Schedule]** ein.

1. Wählen Sie im Bedienfeld auf der linken Seite **[!UICONTROL Conditions]**.

   Für die Regel muss mindestens eine Bedingung definiert sein. Der Prozess ähnelt dem Erstellen [ Katalogpreisregel](price-rules-catalog.md)

   ![E-Mail-Erinnerungsbedingungen](./assets/email-reminder-conditions.png){width="600" zoomable="yes"}

   Klicken Sie _Hinzufügen_ (![Symbol hinzufügen](../assets/icon-add-green-circle.png)), um die Liste der Optionen anzuzeigen, und wählen Sie dann eine der folgenden Bedingungen aus:

   - Wunschliste
   - Warenkorb

   >[!NOTE]
   >
   >Wenn ein Kunde über mehr als einen übereinstimmenden, nicht mehr in den Warenkorb gelegten Warenkorb, eine Wunschliste oder eine Kombination aus beidem verfügt, wird die E-Mail-Erinnerung nur einmal für diesen Kunden ausgelöst. Um dieselbe E-Mail-Erinnerung erneut Trigger, legen Sie im Feld _[!UICONTROL Repeat Schedule]_&#x200B;die Anzahl der Tage zwischen den E-Mails fest. <br/>
   >
   >Dieselbe E-Mail-Erinnerung **_nicht erneut ausgelöst_** für denselben Kunden für **_neue_** abgebrochene Warenkörbe und Wunschlisten **_nach_** der _[!UICONTROL Repeat Schedule]_&#x200B;ist vorbei.

   Füllen Sie die Bedingung aus, um das Szenario zu beschreiben, in dem die E-Mail-Erinnerung Trigger wird.

   ![Beispiel für E-Mail-Erinnerungsbedingungen](./assets/email-reminder-condition-example.png){width="600" zoomable="yes"}

1. Wählen Sie im Bedienfeld auf der linken Seite **[!UICONTROL Emails and Labels]**.

   ![E-Mail-Erinnerungsregel - E-Mails und Beschriftungsvorlagen ](./assets/email-reminder-rule-emails-labels-email-templates.png){width="600" zoomable="yes"}

1. Wählen Sie im Abschnitt **[!UICONTROL Email Templates]** die E-Mail-Vorlage aus, die für jede Website und Store-Ansicht in Ihrer [Store-Hierarchie“ verwendet ](../getting-started/websites-stores-views.md) soll.

   Wenn Sie die Erinnerungs-E-Mail nicht an Kunden einer Store-Ansicht senden möchten, lassen Sie den Wert `Not Selected`.

1. Gehen Sie _Abschnitt „Standardtitel und_&quot; wie folgt vor:

   - Geben Sie die **[!UICONTROL Rule Title for All Store Views]** ein.

     >[!NOTE]
     >
     >Dieser Wert kann mithilfe der Variablen `promotion_name` in E-Mail-Vorlagen integriert werden.

   - Geben Sie die **[!UICONTROL Rule Description for All Store Views]** ein.

     ![E-Mail-Erinnerungen - Titel und Beschreibungen](./assets/email-reminders-emails-and-labels-default-titles-description.png){width="500" zoomable="yes"}

   - Geben Sie im Abschnitt _[!UICONTROL Titles and Descriptions Per Store View]_&#x200B;den **[!UICONTROL Rule Title]**&#x200B;und die **[!UICONTROL Description]**&#x200B;für die_ Store-Standardansicht“ _. Geben Sie für mehrere Store-Ansichten den entsprechenden Titel und die entsprechende Beschreibung für jede Ansicht ein.

     >[!NOTE]
     >
     >Die Beschreibung kann mithilfe der Variablen PROMOTION_DESCRIPTION in E-Mail-Vorlagen integriert werden.

     ![Titel und Beschreibungen - Store-Ansicht](./assets/email-reminder-rules-title-descriptions-per-store-view.png){width="500" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

## Trigger-Bedingungen

| Source | Trigger |
|--- |--- |
| [!UICONTROL Wish List] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Sharing]<br/>[!UICONTROL Number of Items]<br/>[!UICONTROL Items Sub selection] |
| [!UICONTROL Shopping Cart] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Coupon Code]<br/>[!UICONTROL Cart Line Items]<br/>[!UICONTROL Items Quantity]<br/>[!UICONTROL Virtual Only]<br/>[!UICONTROL Total Amount]<br/>[!UICONTROL Items Subselection] |

{style="table-layout:auto"}

## Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Rule Name] | Der Name der automatischen Erinnerungsregel identifiziert die Regel intern. |
| [!UICONTROL Description] | Eine Beschreibung der Regel als interne Referenz. |
| [!UICONTROL Shopping Cart Price Rule] | Die Warenkorbregel, die mit dieser E-Mail-Erinnerung verknüpft ist. Erinnerungs-E-Mails können eine Preisregel für einen Warenkorb mit oder ohne Coupon bewerben. Wenn eine Preisregel für den Warenkorb einen automatisch generierten Coupon enthält, generiert die Regel Erinnerung einen zufälligen, eindeutigen Couponcode für jeden Kunden. |
| [!UICONTROL Assigned to Website] | Die Websites, die auf dieser Regel basierende automatische Erinnerungs-E-Mails erhalten. |
| [!UICONTROL Status] | Aktiviert die Regel. Wenn der Status „Inaktiv“ ist, werden alle anderen Einstellungen ignoriert und die Regel wird nicht ausgelöst. Optionen: `Active` / `Inactive` |
| [!UICONTROL From Date] | Das Startdatum für diese automatische Erinnerungsregel. Wenn kein Datum angegeben wird, wird die Regel sofort aktiv. |
| [!UICONTROL To Date] | Das Enddatum für diese automatische Erinnerungsregel. Wenn kein Datum angegeben wird, wird die Regel auf unbestimmte Zeit aktiv. |
| [!UICONTROL Repeat Schedule] | Die Anzahl der Tage, bevor die Regel ausgelöst wird, und die Erinnerungs-E-Mail, sofern die Bedingungen erfüllt sind, erneut gesendet. Wenn Sie die Regel mehrmals Trigger anzeigen möchten, geben Sie die Anzahl der Tage vor der nächsten E-Mail-Explosion ein (durch ein Komma getrennt). Geben Sie beispielsweise `7` ein, damit die Regel sieben Tage später erneut ausgelöst wird. Geben Sie `7,14` ein, damit die Regel in sieben Tagen ausgelöst wird, und erneut 14 Tage später. |
| [!UICONTROL Email Templates] | Bestimmt die E-Mail-Vorlage, die für jede Store-Ansicht verwendet werden soll. |
| [!UICONTROL Rule Title for All Store Views] | Bestimmt den Titel der Regel für jede Store-Ansicht. |
| [!UICONTROL Rule Description for All Store Views] | Bestimmt die Beschreibung der Regel für jede Store-Ansicht. |

{style="table-layout:auto"}
