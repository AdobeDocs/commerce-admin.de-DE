---
title: B2B-Funktionen aktivieren
description: Erfahren Sie mehr über die Aktivierung von B2B-Funktionen für Ihren Adobe Commerce-Store, einschließlich Unternehmenskonten, standardmäßigen Zahlungs- und Versandmethoden, Bestellungen und Bestellgenehmigungen.
exl-id: aed203ef-f39b-4f7e-b32f-ded53eca09a8
feature: B2B, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '1629'
ht-degree: 0%

---

# B2B-Funktionen aktivieren

Standardmäßig sind alle B2B-Funktionen zunächst deaktiviert. Ein Store-Administrator kann die B2B-Funktionen nach Bedarf für Commerce Stores aktivieren oder deaktivieren. Eine vollständige Liste der B2B-Konfigurationseinstellungen finden Sie unter [Referenz zur Konfiguration von B2B-Funktionen](../configuration-reference/general/b2b-features.md).

Wenn Sie den Support für Kundenunternehmen aktivieren, werden automatisch zusätzliche B2B-Funktionen aktiviert:

- [!DNL Shared Catalog]

  Unterstützt benutzerdefinierte Preiskonfigurationen für verschiedene Unternehmen und ermöglicht zudem Kategorieberechtigungen für alle Stores.

- [!DNL Enable Shared Catalog direct products price assigning]

  Verbessert die Site-Leistung, indem nur Produkte gespeichert werden, die einem freigegebenen Katalog im Preisindex zugewiesen sind. Die Aktivierung dieser Funktion ist eine Best Practice für Händler, die über viele freigegebene Kataloge verfügen, um benutzerdefinierte Preise für verschiedene Unternehmen zu verwalten.

- [!DNL B2B Quotes]

  Bietet Verkäufern und Firmenkäufern die Möglichkeit, Preise zu verhandeln.

- [!DNL B2B default payment and shipping methods]

  Bestimmt die Auswahl der Zahlungs- und Versandoptionen, die B2B-Käufern auf der Storefront zur Verfügung stehen.

Konfigurationseinstellungen für diese Funktionen sind nur sichtbar, wenn [!DNL Enable Company] auf `Yes`.

B2B [!DNL Quick Order] und [!DNL Requisition List] -Funktionen können unabhängig aktiviert und deaktiviert werden.

## B2B-Funktionen konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   Wenn Sie über eine Installation mit mehreren Sites verfügen, legen Sie die **[!UICONTROL Store View]** -Steuerung in der linken oberen Ecke der Website, auf der die Konfiguration angewendet wird.

1. Im linken Bereich unter _[!UICONTROL General]_auswählen **[!UICONTROL B2B Features]**:

   ![B2B-Konfiguration - Allgemein](./assets/b2b-features.png){width="600"}

   - Kunden die Verwaltung ihrer eigenen Unternehmenskonten ermöglichen und die Unterstützung für zusätzliche B2B-Funktionen aktivieren, indem Sie **[!UICONTROL Enable Company]**  nach `Yes`.

     Wenn Sie die Unternehmensunterstützung aktivieren, werden der freigegebene Katalog, das B2B-Angebot, die B2B-Zahlungsmethoden und die B2B-Versandmethoden automatisch aktiviert.

   - Damit Kunden und Gäste schnell Bestellungen basierend auf der SKU oder dem Produktnamen aufgeben können, legen Sie **[!UICONTROL Enable Quick Order]** nach `Yes`.

   - Um Kunden die Erstellung und Verwaltung von Anforderungslisten über ihr Konto-Dashboard zu ermöglichen, legen Sie **[!UICONTROL Enable Requisition List]** nach `Yes`.

     Sie können auch [die maximale Anzahl von Listen konfigurieren](configure-requisition-lists.md) ein Kunde sein Konto haben kann.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Standardmäßige B2B-Zahlungs- und Versandmethoden konfigurieren

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Default B2B Payment Methods]** Abschnitt.

1. Um die Zahlungsmethoden für B2B-Bestellungen festzulegen, legen Sie **[!UICONTROL Applicable Payment Methods]** auf einen der folgenden Werte zu:

   - `All Payment Methods`

   - `Selected Payment Methods`

     Wählen Sie für die jeweilige Option die **[!UICONTROL Payment Methods]** die Sie Ihren Kunden zur Verfügung stellen möchten, indem Sie beim Klicken auf die einzelnen Optionen die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt halten.

   Die Liste der [Zahlungsmethoden](../configuration-reference/sales/payment-methods.md) zeigt an, welche Optionen derzeit in Ihrem Store aktiviert oder deaktiviert sind. Neben den Standardzahlungsmethoden enthält die Liste auch folgende Elemente:

   - Keine Zahlungsinformationen erforderlich
   - [Kontozahlung](#configure-payment-on-account)
   - Gespeicherte Konten
   - Stored Cards

   ![B2B-Konfiguration - Standardeinstellungen für Zahlungsmethoden](./assets/b2b-features-default-payment-methods.png){width="600"}

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Default B2B Shipping Methods]** Abschnitt.

1. Um die standardmäßigen Versandmethoden für B2B-Bestellungen anzugeben, legen Sie **[!UICONTROL Applicable Shipping Methods]** auf einen der folgenden Werte zu:

   - `All Shipping Methods`
   - `Selected Shipping Methods`

     Wählen Sie für die jeweilige Option die **[!UICONTROL Shipping Methods]** die Sie Ihren Kunden zur Verfügung stellen möchten, indem Sie beim Klicken auf die einzelnen Optionen die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt halten.

     Die Liste der Versandmethoden zeigt an, welche [aktiviert oder deaktiviert](../configuration-reference/sales/delivery-methods.md).

   ![B2B-Konfiguration - standardmäßige Versandmethoden](./assets/b2b-features-shipping-methods.png){width="600"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## E-Mail-Optionen für Unternehmen konfigurieren

Die [Vertriebsmitarbeiter](account-company-manage.md#assign-a-sales-representative) wird als Hauptkontakt für ein Unternehmen zugewiesen und ist standardmäßig als Absender vieler automatisierter E-Mail-Nachrichten konfiguriert, die an das Unternehmen gesendet werden.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen **[!UICONTROL Company Configuration]**.

1. Legen Sie bei Bedarf **[!UICONTROL Store View]** in die Store-Ansicht, um die [Umfang](../getting-started/websites-stores-views.md#scope-settings) der Konfiguration.

1. Führen Sie die **[!UICONTROL Company Registration]** Abschnitt:

   >[!NOTE]
   >
   >Löschen Sie die **[!UICONTROL Use system value]** aktivieren, damit das Feld bearbeitbar ist.

   - Satz **[!UICONTROL Company Registration Email Recipient]** der [Store-Kontakt](../getting-started/store-details.md#store-email-addresses) der benachrichtigt werden soll, wenn ein neuer Antrag auf Eintragung einer Unternehmensregistrierung eingeht.

   - Für **[!UICONTROL Send Company Registration Email Copy To]** die E-Mail-Adresse jeder Person eingeben, die eine Kopie der Registrierungsbenachrichtigung erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch Kommas.

   - Um zu bestimmen, wie die Kopie der Benachrichtigung gesendet wird, legen Sie **Email Copy-Methode senden** auf einen der folgenden Werte zu:

      - `Bcc` - Sendet eine _Blind Höflichkeitskopie_ indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
      - `Separate Email` - Sendet die Kopie als separate E-Mail.

   - Wenn Sie eine E-Mail-Vorlage vorbereitet haben, die anstelle der Standardeinstellung verwendet werden soll, legen Sie **[!UICONTROL Default Company Registration Email]** zum Namen der Vorlage. Standardmäßig wird die Variable `Company Registration Request` verwendet.

     ![Kundenkonfiguration - Registrierung des Unternehmens](./assets/company-email-options-company-registration.png){width="600"}

1. Führen Sie die **[!UICONTROL Customer-Related Emails]** Abschnitt:

   Wenn Sie alternative E-Mail-Vorlagen für die Verwendung anstelle der Standardeinstellungen vorbereitet haben, wählen Sie die Vorlage aus, die Sie für jeden der folgenden Schritte verwenden möchten:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Kundenkonfiguration - kundenbezogene E-Mails](./assets/company-email-options-customer-related-emails.png){width="600"}

1. Führen Sie die **[!UICONTROL Company Status Change]** Abschnitt:

   - Für **[!UICONTROL Send Company Status Change Email Copy To]** eingeben, geben Sie die E-Mail-Adresse jeder Person ein, die eine Kopie der Benachrichtigung über die Statusänderung erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch Kommas.

   - Um zu bestimmen, wie die Kopie der Benachrichtigung gesendet wird, legen Sie **Email Copy-Methode senden** auf einen der folgenden Werte zu:

      - `Bcc` - Sendet eine _Blind Höflichkeitskopie_ indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
      - `Separate Email` - Sendet die Kopie als separate E-Mail.

   - Wenn Sie eine E-Mail-Vorlage vorbereitet haben, die verwendet werden soll, wenn sich der Unternehmensstatus ändert von `Pending Approval` nach `Active`, set **[!UICONTROL Default 'Company Status Change to Active 1' Email]** zum Namen der Vorlage. Standardmäßig wird die Variable `Company Status Active 1` verwendet.

   - Wenn Sie eine E-Mail-Vorlage vorbereitet haben, die verwendet werden soll, wenn sich der Unternehmensstatus ändert von `Rejected` oder `Blocked` nach `Active`, set **[!UICONTROL Default 'Company Status Change to Active 2' Email]** zum Namen der Vorlage. Standardmäßig wird die Variable `Company Status Active 2` verwendet.

   - Wenn Sie eine E-Mail-Vorlage vorbereitet haben, die verwendet werden soll, wenn sich der Unternehmensstatus in `Rejected`, set **[!UICONTROL Default 'Company Status Change to Rejected' Email]** zum Namen der Vorlage. Standardmäßig wird die Variable `Company Status Rejected` verwendet.

   - Wenn Sie eine E-Mail-Vorlage vorbereitet haben, die verwendet werden soll, wenn sich der Unternehmensstatus in `Blocked`, set **[!UICONTROL Default 'Company Status Change to Blocked' Email]** zum Namen der Vorlage. Standardmäßig wird die Variable `Company Status Blocked` verwendet.

   - Wenn Sie eine E-Mail-Vorlage vorbereitet haben, die verwendet werden soll, wenn sich der Unternehmensstatus in `Pending Approval`, set **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** zum Namen der Vorlage. Standardmäßig wird die Variable `Company Status Pending Approval` verwendet.

   ![Kundenkonfiguration - Änderung des Unternehmensstatus](./assets/company-email-options-company-status-change.png){width="600"}

1. Führen Sie die **[!UICONTROL Company Credit Emails]** Abschnitt:

   - Satz **[!UICONTROL Company Credit Change Email Sender]** der [Store-Kontakt](../getting-started/store-details.md#store-email-addresses) der benachrichtigt werden soll, wenn eine Änderung an der einem Unternehmen zugewiesenen Kreditbeschränkung vorgenommen wird. Standardmäßig wird die Benachrichtigung an _Vertriebsmitarbeiter_.

   - Für **[!UICONTROL Send Company Credit Change Email Copy To]** eingeben, geben Sie die E-Mail-Adresse jeder Person ein, die eine Kopie der Benachrichtigung über eine Kreditänderung erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch Kommas.

   - Um zu bestimmen, wie die Kopie der Benachrichtigung gesendet wird, legen Sie **Email Copy-Methode senden** auf einen der folgenden Werte zu:

      - `Bcc` - Sendet eine _Blind Höflichkeitskopie_ indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
      - `Separate Email` - Sendet die Kopie als separate E-Mail.

   - Wenn Sie E-Mail-Vorlagen für die Verwendung anstelle der Standardwerte vorbereitet haben, wählen Sie die Vorlage für jede der folgenden Benachrichtigungen aus, die an den Unternehmensadministrator gesendet werden.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Kundenkonfiguration - E-Mails zu Firmenkrediten](./assets/company-email-options-company-credit.png){width="600"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Bestellvalidierung konfigurieren

Die Möglichkeit, die Auftragsverarbeitung und Bestellungen zu verfolgen, gibt Unternehmensadministratoren die Kontrolle über die Handlungen der Käufer des Unternehmens. Die Funktion zur Bestellvalidierung ist verfügbar, wenn die Funktion für Bestellungen von einem Store-Administrator aktiviert wurde.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL General]** und wählen **[!UICONTROL B2B Features]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Order Approval Configuration]** Abschnitt.

   ![Konfiguration der Bestellbestätigung](./assets/b2b-features-order-approval.png){width="600"}

1. Um es Unternehmen zu ermöglichen, eigene Bestellungen zu erstellen, legen Sie **[!UICONTROL Enable Purchase Orders]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

   Die Funktion &quot;Bestellungen&quot;ist auf Website-Ebene aktiviert. Um diese Art von Bestellung für ein Unternehmen zu aktivieren, verwenden Sie die entsprechenden Einstellungen in jedem [Firmenprofil](account-company-manage.md).

## Konfigurieren von Kaufaufträgen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Suchen Sie das Unternehmen in der Liste und klicken Sie auf **[!UICONTROL Edit]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Advanced Settings]** Abschnitt.

1. Satz **[!UICONTROL Enable Purchase Orders]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

Nach der Aktivierung wird die **[!UICONTROL Approval Rules]** wird auf der Storefront angezeigt [Konto-Dashboard](../customers/account-dashboard.md) für einen Unternehmensadministrator.

>[!NOTE]
>
>Der Zugriff auf die Lagerergänzungen muss vom Administrator des Unternehmens auf der Grundlage von [Benutzerrollenberechtigungen für Unternehmen](account-company-roles-permissions.md).

## Konfigurieren der Zahlung auf dem Konto

&quot;Payment on Account&quot;ist eine Offline-Zahlungsmethode, mit der Unternehmen bis zu dem in ihrem Profil angegebenen Kreditlimit Einkäufe tätigen können. Die Zahlung auf Konto kann global oder pro Unternehmen aktiviert werden und wird beim Checkout nur angezeigt, wenn sie aktiviert ist. Wann _Kontozahlung_ als Zahlungsmethode verwendet wird, wird oben in der Bestellung eine Meldung angezeigt, die den Status des Kontos angibt. Informationen zur Konfiguration dieser Zahlungsmethode für ein bestimmtes Unternehmen finden Sie unter [Verwalten von Unternehmenskonten](account-company-manage.md).

>[!NOTE]
>
>Die Zahlung auf Konto wird bei Bestellungen mit [mehrere Versandadressen](../stores-purchase/shipping-settings.md#multiple-addresses) und erscheint nicht unter den Zahlungsoptionen für diese Bestellungen.

So aktivieren Sie die Option Zahlung auf Konto für Ihren Store:

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Payment Methods]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Payment on Account]** Abschnitt.

   ![Kontozahlung](./assets/payment-methods-payment-on-account.png){width="600"}

   >[!NOTE]
   >
   >Heben Sie bei Bedarf die Auswahl der **[!UICONTROL Use system value]** aktivieren, um diese Einstellungen zu ändern.

1. Um die Zahlung auf Rechnung zu ermöglichen, legen Sie **[!UICONTROL Enabled]** nach `Yes`.

1. Geben Sie einen **[!UICONTROL Title]** die die Zahlungsmethode während des Checkouts identifiziert, oder Sie können die `Payment on Account` Standardtitel.

1. Wenn Bestellungen in der Regel auf die Validierung warten, akzeptieren Sie die Standardeinstellung **[!UICONTROL New Order Status]** as `Pending` bis zur Genehmigung.

   Wenn Sie es bevorzugen, können Sie die `Processing` oder `Suspected Fraud` Status für neue Bestellungen mit dieser Zahlungsmethode.

1. Satz **[!UICONTROL Payment from Applicable Countries]** auf einen der folgenden Werte zu:

   - `All Allowed Countries` - Kunden von allen [Länder](../getting-started/store-details.md#country-options) Diese Zahlungsmethode kann in Ihrer Store-Konfiguration verwendet werden.
   - `Specific Countries` - Wenn Sie diese Option ausgewählt haben, wird die _[!UICONTROL Payment from Specific Countries]_angezeigt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

1. Satz **[!UICONTROL Minimum Order Total]** und **[!UICONTROL Maximum Order Total]** auf die Bestellbeträge, die für diese Zahlungsmethode erforderlich sind.

   >[!NOTE]
   >
   >Eine Bestellung qualifiziert sich, wenn der Gesamtwert zwischen den minimalen oder maximalen Gesamtwerten liegt oder genau damit übereinstimmt.

1. Geben Sie einen **[!UICONTROL Sort Order]** Zahl, die die Position dieses Elements in der Liste der Zahlungsmethoden festlegt, die beim Checkout angezeigt werden.

   Der Wert ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = Sekunde, `2` = drittes Element usw.)

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
