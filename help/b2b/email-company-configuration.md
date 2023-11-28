---
title: Unternehmens-E-Mail konfigurieren
description: Erfahren Sie mehr über die E-Mail-Optionen und -Vorlagen, mit denen Nachrichten für Unternehmenskonten gesendet werden.
exl-id: fd61c0c6-0887-4ff2-8002-906ff615bad9
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# E-Mail-Optionen für Unternehmen konfigurieren

Die [Vertriebsmitarbeiter](account-company-manage.md) wird als Hauptkontakt für ein Unternehmen zugewiesen und ist standardmäßig als Absender vieler automatisierter E-Mail-Nachrichten konfiguriert, die an das Unternehmen gesendet werden.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen **[!UICONTROL Company Configuration]**.

1. Legen Sie bei Bedarf **[!UICONTROL Store View]** in die Store-Ansicht, um die [Umfang](../getting-started/websites-stores-views.md#scope-settings) der Konfiguration.

1. Führen Sie die **[!UICONTROL Company Registration]** Abschnitt:

   >[!NOTE]
   >
   >Löschen Sie die **[!UICONTROL Use system value]** aktivieren, damit das Feld bearbeitbar ist.

   - Satz **[!UICONTROL Company Registration Email Recipient]** der [Store-Kontakt](../getting-started/store-details.md#store-email-addresses) der benachrichtigt werden soll, wenn ein neuer Antrag auf Eintragung einer Unternehmensregistrierung eingeht.

   - Im **[!UICONTROL Send Company Registration Email Copy To]** geben Sie die E-Mail-Adresse jeder Person ein, die eine Kopie der Registrierungsbenachrichtigung erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch Kommas.

   - Um zu bestimmen, wie die Kopie der Benachrichtigung gesendet wird, legen Sie **[!UICONTROL Send Email Copy Method]** auf einen der folgenden Werte zu:

      - `Bcc` - Sendet eine _Blind Höflichkeitskopie_ indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
      - `Separate Email` - Sendet die Kopie als separate E-Mail.

   - Wenn Sie eine E-Mail-Vorlage vorbereitet haben, die anstelle der Standardeinstellung verwendet werden soll, legen Sie **[!UICONTROL Default Company Registration Email]** zum Namen der Vorlage. Standardmäßig wird die Variable `Company Registration Request` verwendet.

     ![Kundenkonfiguration - Registrierung des Unternehmens](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. Führen Sie die **[!UICONTROL Customer-Related Emails]** Abschnitt:

   Wenn Sie alternative E-Mail-Vorlagen für die Verwendung anstelle der Standardeinstellungen vorbereitet haben, wählen Sie die Vorlage aus, die Sie für jeden der folgenden Schritte verwenden möchten:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Kundenkonfiguration - kundenbezogene E-Mails](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. Führen Sie die **[!UICONTROL Company Status Change]** Abschnitt:

   - Satz **[!UICONTROL Company Status Change for Email Recipient]** der [Store-Kontakt](../getting-started/store-details.md#store-email-addresses) der benachrichtigt werden soll, wenn sich der Status eines Unternehmens ändert.

   - Im **[!UICONTROL Send Company Status Change Email Copy To]** Geben Sie die E-Mail-Adresse jeder Person ein, die eine Kopie der Benachrichtigung über die Statusänderung erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch Kommas.

   - Um zu bestimmen, wie die Kopie der Benachrichtigung gesendet wird, legen Sie **[!UICONTROL Send Email Copy Method]** auf einen der folgenden Werte zu:

      - `Bcc` - Sendet eine _Blind Höflichkeitskopie_ indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
      - `Separate Email` - Sendet die Kopie als separate E-Mail.

   - Wenn Sie über eine vorbereitete E-Mail-Vorlage verfügen, die anstelle der Standardvorlage verwendet werden soll, wenn sich der Unternehmensstatus ändert von `Pending Approval` nach `Active`, set **[!UICONTROL Default 'Company Status Change to Active 1' Email]** zu dieser Vorlage hinzufügen. Standardmäßig wird die Variable `Company Status Active 1` verwendet.

   - Wenn Sie über eine vorbereitete E-Mail-Vorlage verfügen, die anstelle der Standardvorlage verwendet werden soll, wenn sich der Unternehmensstatus ändert von `Rejected` oder `Blocked` nach `Active`, set **[!UICONTROL Default 'Company Status Change to Active 2' Email]** zu dieser Vorlage hinzufügen. Standardmäßig wird die Variable `Company Status Active 2` verwendet.

   - Wenn Sie über eine vorbereitete E-Mail-Vorlage verfügen, die anstelle der Standardvorlage verwendet werden soll, wenn sich der Unternehmensstatus in `Rejected`, set **[!UICONTROL Default 'Company Status Change to Rejected' Email]** zu dieser Vorlage hinzufügen. Standardmäßig wird die Variable `Company Status Rejected` verwendet.

   - Wenn Sie über eine vorbereitete E-Mail-Vorlage verfügen, die anstelle der Standardvorlage verwendet werden soll, wenn sich der Unternehmensstatus in `Blocked`, set **[!UICONTROL Default 'Company Status Change to Blocked' Email]** zu dieser Vorlage hinzufügen. Standardmäßig wird die Variable `Company Status Blocked` verwendet.

   - Wenn Sie über eine vorbereitete E-Mail-Vorlage verfügen, die anstelle der Standardvorlage verwendet werden soll, wenn sich der Unternehmensstatus in `Pending Approval`, set **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** zu dieser Vorlage hinzufügen. Standardmäßig wird die Variable `Company Status Pending Approval` verwendet.

     ![Kundenkonfiguration - Änderung des Unternehmensstatus](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. Führen Sie die **[!UICONTROL Company Credit Emails]** Abschnitt:

   - Satz **[!UICONTROL Company Credit Change Email Sender]** der [Store-Kontakt](../getting-started/store-details.md#store-email-addresses) der benachrichtigt werden soll, wenn eine Änderung an der einem Unternehmen zugewiesenen Kreditbeschränkung vorgenommen wird. Standardmäßig wird die Benachrichtigung an _Vertriebsmitarbeiter_.

   - Im **[!UICONTROL Send Company Credit Change Email Copy To]** Geben Sie die E-Mail-Adresse jeder Person ein, die eine Kopie der Benachrichtigung über eine Kreditänderung erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch Kommas.

   - Um zu bestimmen, wie die Kopie der Benachrichtigung gesendet wird, legen Sie **[!UICONTROL Send Email Copy Method]** auf einen der folgenden Werte zu:

      - `Bcc` - Sendet eine _Blind Höflichkeitskopie_ indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
      - `Separate Email` - Sendet die Kopie als separate E-Mail.

   - Wenn Sie E-Mail-Vorlagen für die Verwendung anstelle der Standardwerte vorbereitet haben, wählen Sie die Vorlage für jede der folgenden Benachrichtigungen aus, die an den Unternehmensadministrator gesendet werden.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Kundenkonfiguration - E-Mails zu Firmenkrediten](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
