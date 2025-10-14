---
title: B2B-Funktionen aktivieren
description: Erfahren Sie mehr über die Aktivierung von B2B-Funktionen für Ihren Adobe Commerce-Store, einschließlich Firmenkonten, standardmäßigen Zahlungs- und Versandmethoden, Bestellungen und Bestellgenehmigungen.
exl-id: aed203ef-f39b-4f7e-b32f-ded53eca09a8
feature: B2B, Configuration
role: Admin
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '1635'
ht-degree: 0%

---

# B2B-Funktionen aktivieren

Standardmäßig sind alle B2B-Funktionen zunächst deaktiviert. Ein Store-Administrator kann die B2B-Funktionen nach Bedarf für Commerce-Stores aktivieren oder deaktivieren. Eine vollständige Liste der B2B-Konfigurationseinstellungen finden Sie in der Konfigurationsreferenz zu [B2B-Funktionen](../configuration-reference/general/b2b-features.md).

Wenn Sie den Support für Kundenunternehmen aktivieren, werden zusätzliche B2B-Funktionen automatisch aktiviert:

- [[!DNL Shared Catalog]](catalog-shared.md)

  Unterstützt benutzerdefinierte Preiskonfigurationen für verschiedene Unternehmen und aktiviert auch Kategorieberechtigungen für alle Stores.

- [!DNL Enable Shared Catalog direct products price assigning]

  Verbessert die Site-Performance, indem nur Produkte gespeichert werden, die einem freigegebenen Katalog im Preisindex zugewiesen sind. Die Aktivierung dieser Funktion ist eine Best Practice für Händler, die viele freigegebene Kataloge haben, um benutzerdefinierte Preise für verschiedene Unternehmen zu verwalten.

- [[!DNL B2B Quotes]](quotes.md)

  Bietet Verkäufern und Unternehmenskäufern die Möglichkeit, Preise auszuhandeln.

- [!DNL B2B default payment and shipping methods]

  Bestimmt die Auswahl der Zahlungs- und Versandoptionen, die B2B-Käufern in der Storefront zur Verfügung stehen.

Konfigurationseinstellungen für diese Funktionen sind nur sichtbar, wenn [!DNL Enable Company] auf `Yes` gesetzt ist.

Die B2B-[[!DNL Quick Order]](quick-order.md) und -[[!DNL Requisition List]](requisition-lists.md) können unabhängig voneinander aktiviert und deaktiviert werden.

## Konfigurieren von B2B-Funktionen

Die Optionen zum Konfigurieren von Adobe Commerce B2B-Funktionen sind nur für Commerce-Projekte verfügbar, in denen die [Adobe Commerce B2B-Erweiterung installiert ist](install.md).

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   Wenn Sie eine Multi-Site-Installation haben, legen Sie das **[!UICONTROL Store View]**-Steuerelement in der oberen linken Ecke auf die Website fest, für die die Konfiguration gilt.

1. Wählen Sie im linken Bedienfeld unter _[!UICONTROL General]_&#x200B;die Option **[!UICONTROL B2B Features]**:

   ![B2B-Konfiguration - allgemein](./assets/b2b-features.png){width="600"}

   - Kunden ermöglichen, ihre eigenen Unternehmenskonten zu verwalten und Unterstützung für zusätzliche B2B-Funktionen zu aktivieren, indem **[!UICONTROL Enable Company]** auf `Yes` gesetzt wird.

     Wenn Sie den Unternehmens-Support aktivieren, werden der freigegebene Katalog, das B2B-Angebot, die B2B-Zahlungsmethoden und die B2B-Versandmethoden automatisch aktiviert.

     ![B2B-Konfiguration - Unternehmensfunktionen](assets/b2b-additional-features.png){width="600"}

   - Damit Kunden und Gäste schnell Bestellungen basierend auf der SKU oder dem Produktnamen aufgeben können, legen Sie **[!UICONTROL Enable Quick Order]** auf `Yes` fest.

   - Damit Kundinnen und Kunden Anforderungslisten über ihr Konto-Dashboard erstellen und verwalten können, setzen Sie **[!UICONTROL Enable Requisition List]** auf `Yes`.

     Sie können auch [die maximale Anzahl von Listen konfigurieren](configure-requisition-lists.md) die eine Kundin oder ein Kunde für sein Konto haben kann.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Konfigurieren der standardmäßigen B2B-Zahlungs- und Versandmethoden

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Default B2B Payment Methods]** .

1. Um die Standardzahlungsmethoden für B2B-Bestellungen festzulegen, legen Sie **[!UICONTROL Applicable Payment Methods]** auf eine der folgenden Optionen fest:

   - `All Payment Methods`

   - `Selected Payment Methods`

     Wählen Sie für die spezifische Option die **[!UICONTROL Payment Methods]** aus, die Sie Ihren Kunden zur Verfügung stellen möchten, indem Sie die Strg -Taste (PC) oder die Befehlstaste (Mac) gedrückt halten, während Sie auf die jeweilige Option klicken.

   Die Liste der [Zahlungsmethoden](../configuration-reference/sales/payment-methods.md) zeigt, welche Optionen derzeit in Ihrem Store aktiviert oder deaktiviert sind. Neben den Standardzahlungsmethoden umfasst die Liste auch Folgendes:

   - Es sind keine Zahlungsinformationen erforderlich
   - [Anzahlung](#configure-payment-on-account)
   - Gespeicherte Konten
   - Gespeicherte Karten

   ![B2B-Konfiguration - Standardeinstellungen für Zahlungsmethoden](./assets/b2b-features-default-payment-methods.png){width="600"}

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Default B2B Shipping Methods]** .

1. Um die standardmäßigen Versandmethoden für B2B-Bestellungen anzugeben, legen Sie **[!UICONTROL Applicable Shipping Methods]** auf eine der folgenden Optionen fest:

   - `All Shipping Methods`
   - `Selected Shipping Methods`

     Wählen Sie für die spezifische Option die **[!UICONTROL Shipping Methods]** aus, die Sie Ihren Kunden zur Verfügung stellen möchten, indem Sie die Strg -Taste (PC) oder die Befehlstaste (Mac) gedrückt halten, während Sie auf die jeweilige Option klicken.

     Die Liste der Versandmethoden zeigt, welche derzeit [aktiviert oder deaktiviert](../configuration-reference/sales/delivery-methods.md) sind.

   ![B2B-Konfiguration - Standard-Versandmethoden](./assets/b2b-features-shipping-methods.png){width="600"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Konfigurieren von E-Mail-Optionen für Unternehmen

Der [Vertriebsmitarbeiter](account-company-manage.md#assign-a-sales-representative) der als primärer Kontakt für eine Firma zugewiesen ist, ist standardmäßig als Absender vieler automatisierter E-Mail-Nachrichten konfiguriert, die an die Firma gesendet werden.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Company Configuration]**.

1. Legen Sie bei Bedarf **[!UICONTROL Store View]** auf die Store-Ansicht fest, um den [Umfang](../getting-started/websites-stores-views.md#scope-settings) der Konfiguration zu definieren.

1. Füllen Sie den **[!UICONTROL Company Registration]** Abschnitt aus:

   >[!NOTE]
   >
   >Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** , damit das Feld bearbeitet werden kann.

   - Legen Sie **[!UICONTROL Company Registration Email Recipient]** auf den [Store-Kontakt](../getting-started/store-details.md#store-email-addresses) fest, der benachrichtigt werden soll, wenn eine neue Anforderung zur Unternehmensregistrierung empfangen wird.

   - Geben Sie **[!UICONTROL Send Company Registration Email Copy To]** die E-Mail-Adresse jeder Person ein, die eine Kopie der Registrierungsbenachrichtigung erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch ein Komma.

   - Um zu bestimmen, wie die Kopie der Benachrichtigung gesendet wird, setzen Sie **E-Mail-Kopiermethode senden** auf einen der folgenden Werte:

      - `Bcc` - Sendet eine _Blinde Höflichkeitskopie_ indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
      - `Separate Email` - Sendet die Kopie als separate E-Mail.

   - Wenn Sie eine E-Mail-Vorlage vorbereitet haben, die anstelle der Standardvorlage verwendet werden soll, legen Sie **[!UICONTROL Default Company Registration Email]** auf den Namen der Vorlage fest. Standardmäßig wird die `Company Registration Request` verwendet.

     ![Kundenkonfiguration - Unternehmensregistrierung](./assets/company-email-options-company-registration.png){width="600"}

1. Füllen Sie den **[!UICONTROL Customer-Related Emails]** Abschnitt aus:

   Wenn Sie alternative E-Mail-Vorlagen vorbereitet haben, die anstelle der Standardvorlagen verwendet werden sollen, wählen Sie die Vorlage aus, die Sie für jede der folgenden Aktionen verwenden möchten:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Kundenkonfiguration - Kundenbezogene E-Mails](./assets/company-email-options-customer-related-emails.png){width="600"}

1. Füllen Sie den **[!UICONTROL Company Status Change]** Abschnitt aus:

   - Geben Sie **[!UICONTROL Send Company Status Change Email Copy To]** die E-Mail-Adresse jeder Person ein, die eine Kopie der Statusänderungsbenachrichtigung erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch ein Komma.

   - Um zu bestimmen, wie die Kopie der Benachrichtigung gesendet wird, setzen Sie **E-Mail-Kopiermethode senden** auf einen der folgenden Werte:

      - `Bcc` - Sendet eine _Blinde Höflichkeitskopie_ indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
      - `Separate Email` - Sendet die Kopie als separate E-Mail.

   - Wenn Sie eine E-Mail-Vorlage vorbereitet haben, die verwendet werden soll, wenn sich der Unternehmensstatus von `Pending Approval` in `Active` ändert, legen Sie **[!UICONTROL Default 'Company Status Change to Active 1' Email]** auf den Namen der Vorlage fest. Standardmäßig wird die `Company Status Active 1` verwendet.

   - Wenn Sie eine E-Mail-Vorlage vorbereitet haben, die verwendet werden soll, wenn sich der Unternehmensstatus von `Rejected` oder `Blocked` in `Active` ändert, legen Sie **[!UICONTROL Default 'Company Status Change to Active 2' Email]** auf den Namen der Vorlage fest. Standardmäßig wird die `Company Status Active 2` verwendet.

   - Wenn Sie eine E-Mail-Vorlage vorbereitet haben, die verwendet werden soll, wenn sich der Unternehmensstatus in `Rejected` ändert, legen Sie **[!UICONTROL Default 'Company Status Change to Rejected' Email]** auf den Namen der Vorlage fest. Standardmäßig wird die `Company Status Rejected` verwendet.

   - Wenn Sie eine E-Mail-Vorlage vorbereitet haben, die verwendet werden soll, wenn sich der Unternehmensstatus in `Blocked` ändert, legen Sie **[!UICONTROL Default 'Company Status Change to Blocked' Email]** auf den Namen der Vorlage fest. Standardmäßig wird die `Company Status Blocked` verwendet.

   - Wenn Sie eine E-Mail-Vorlage vorbereitet haben, die verwendet werden soll, wenn sich der Unternehmensstatus in `Pending Approval` ändert, legen Sie **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** auf den Namen der Vorlage fest. Standardmäßig wird die `Company Status Pending Approval` verwendet.

   ![Konfiguration des Kunden - Änderung des Unternehmensstatus](./assets/company-email-options-company-status-change.png){width="600"}

1. Füllen Sie den **[!UICONTROL Company Credit Emails]** Abschnitt aus:

   - Legen Sie **[!UICONTROL Company Credit Change Email Sender]** auf den [Store-](../getting-started/store-details.md#store-email-addresses) fest, der benachrichtigt werden soll, wenn das einem Unternehmen zugewiesene Kreditlimit geändert wird. Standardmäßig wird die Benachrichtigung an den _Vertriebsmitarbeiter_ gesendet.

   - Geben Sie **[!UICONTROL Send Company Credit Change Email Copy To]** die E-Mail-Adresse jeder Person ein, die eine Kopie der Gutschriftsänderungsbenachrichtigung erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch ein Komma.

   - Um zu bestimmen, wie die Kopie der Benachrichtigung gesendet wird, setzen Sie **E-Mail-Kopiermethode senden** auf einen der folgenden Werte:

      - `Bcc` - Sendet eine _Blinde Höflichkeitskopie_ indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
      - `Separate Email` - Sendet die Kopie als separate E-Mail.

   - Wenn Sie E-Mail-Vorlagen vorbereitet haben, die anstelle der Standardvorlagen verwendet werden sollen, wählen Sie die Vorlage für jede der folgenden Benachrichtigungen aus, die an den Unternehmensadministrator gesendet werden.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Kundenkonfiguration - E-Mails zu Firmenkrediten](./assets/company-email-options-company-credit.png){width="600"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Konfigurieren der Bestellvalidierung

Die Möglichkeit, die Auftragsverarbeitung und Bestellungen zu verfolgen, gibt Unternehmensadministratoren Kontrolle über die Aktionen der Käufer des Unternehmens. Die Funktion für die Bestellvalidierung ist verfügbar, wenn die Funktion „Bestellungen“ von einem Store-Administrator aktiviert wurde.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL General]** und wählen Sie **[!UICONTROL B2B Features]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Order Approval Configuration]** .

   ![Konfiguration der Bestellgenehmigung](./assets/b2b-features-order-approval.png){width="600"}

1. Damit Unternehmen ihre eigenen Bestellungen erstellen können, legen Sie **[!UICONTROL Enable Purchase Orders]** auf `Yes` fest.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

   Die Bestellfunktion wird auf Website-Ebene aktiviert. Um diesen Auftragstyp für eine Firma zu aktivieren, gehen Sie genauso vor mit den entsprechenden Einstellungen in jedem [Unternehmensprofil](account-company-manage.md).

## Konfigurieren von Bestellungen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Suchen Sie das Unternehmen in der Liste und klicken Sie auf **[!UICONTROL Edit]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Advanced Settings]** .

1. Legen Sie **[!UICONTROL Enable Purchase Orders]** auf `Yes` fest.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

Nach der Aktivierung wird der Abschnitt &quot;**[!UICONTROL Approval Rules]**&quot; auf der Storefront [Konto-Dashboard](../customers/account-dashboard.md) für einen Unternehmensadministrator angezeigt.

>[!NOTE]
>
>Der Zugriff auf Bestellungen für die Storefront muss vom Unternehmensadministrator auf der Grundlage von [Berechtigungen der Unternehmensbenutzerrolle) gewährt &#x200B;](account-company-roles-permissions.md).

## Konfigurieren der Zahlung auf Konto

Die Zahlung auf Konto ist eine Offline-Zahlungsmethode, mit der Unternehmen Käufe bis zu dem in ihrem Profil angegebenen Kreditlimit tätigen können. Die Zahlung auf Konto kann global oder pro Unternehmen aktiviert werden und wird beim Checkout nur angezeigt, wenn sie aktiviert ist. Wenn _Zahlung auf Konto_ als Zahlungsmethode verwendet wird, wird oben in der Bestellung eine Meldung angezeigt, die den Status des Kontos angibt. Informationen zum Konfigurieren dieser Zahlungsmethode für eine bestimmte Firma finden Sie unter [Verwalten von Unternehmenskonten](account-company-manage.md).

>[!NOTE]
>
>Die Zahlung auf Konto wird für Bestellungen mit [mehreren Versandadressen](../stores-purchase/shipping-settings.md#multiple-addresses) nicht unterstützt und wird nicht unter den Zahlungsoptionen für diese Bestellungen angezeigt.

So aktivieren Sie die Zahlung auf Konto für Ihren Store:

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Payment Methods]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Payment on Account]** .

   ![Zahlung auf Rechnung](./assets/payment-methods-payment-on-account.png){width="600"}

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Einstellungen zu ändern.

1. Um die Zahlung auf Rechnung zu ermöglichen, setzen Sie **[!UICONTROL Enabled]** auf `Yes`.

1. Geben Sie einen **[!UICONTROL Title]** ein, der die Zahlungsmethode beim Checkout identifiziert, oder Sie können den `Payment on Account` Standardtitel akzeptieren.

1. Wenn Bestellungen in der Regel auf die Genehmigung warten, akzeptieren Sie die **[!UICONTROL New Order Status]** als `Pending`, bis sie genehmigt wird.

   Wenn Sie es vorziehen, können Sie den `Processing`- oder `Suspected Fraud` für neue Bestellungen mit dieser Zahlungsmethode verwenden.

1. Legen Sie **[!UICONTROL Payment from Applicable Countries]** auf eine der folgenden Einstellungen fest:

   - `All Allowed Countries` - Kunden aus allen [Ländern](../getting-started/store-details.md#country-options) die in Ihrer Store-Konfiguration angegeben sind, können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nachdem Sie diese Option ausgewählt haben, wird die _[!UICONTROL Payment from Specific Countries]_&#x200B;angezeigt. Zur Auswahl mehrerer Länder halten Sie die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken auf die einzelnen Optionen.

1. Legen Sie **[!UICONTROL Minimum Order Total]** und **[!UICONTROL Maximum Order Total]** auf die Bestellbeträge fest, die für diese Zahlungsmethode erforderlich sind.

   >[!NOTE]
   >
   >Eine Bestellung ist dann geeignet, wenn die Summe zwischen den minimalen oder maximalen Gesamtwerten liegt oder genau mit diesen übereinstimmt.

1. Geben Sie eine **[!UICONTROL Sort Order]** ein, die die Position dieses Artikels in der Liste der Zahlungsmethoden festlegt, die beim Checkout angezeigt wird.

   Der Wert ist relativ zu den anderen Zahlungsmethoden. (`0` = First, `1` = Second, `2` = Third usw.)

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
