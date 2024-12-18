---
title: Unternehmens-E-Mail konfigurieren
description: Erfahren Sie mehr über die E-Mail-Optionen und -Vorlagen, die zum Senden von Nachrichten an Unternehmenskonten verwendet werden.
exl-id: fd61c0c6-0887-4ff2-8002-906ff615bad9
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# Konfigurieren von E-Mail-Optionen für Unternehmen

Der [Vertriebsmitarbeiter](account-company-manage.md) der als primärer Kontakt für eine Firma zugewiesen ist, ist standardmäßig als Absender vieler automatisierter E-Mail-Nachrichten konfiguriert, die an die Firma gesendet werden.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Company Configuration]**.

1. Legen Sie bei Bedarf **[!UICONTROL Store View]** auf die Store-Ansicht fest, um den [Umfang](../getting-started/websites-stores-views.md#scope-settings) der Konfiguration zu definieren.

1. Füllen Sie den **[!UICONTROL Company Registration]** Abschnitt aus:

   >[!NOTE]
   >
   >Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** , damit das Feld bearbeitet werden kann.

   - Legen Sie **[!UICONTROL Company Registration Email Recipient]** auf den [Store-Kontakt](../getting-started/store-details.md#store-email-addresses) fest, der benachrichtigt werden soll, wenn eine neue Anforderung zur Unternehmensregistrierung empfangen wird.

   - Geben Sie im Feld **[!UICONTROL Send Company Registration Email Copy To]** die E-Mail-Adresse jeder Person ein, die eine Kopie der Registrierungsbenachrichtigung erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch ein Komma.

   - Legen Sie **[!UICONTROL Send Email Copy Method]** auf eine der folgenden Einstellungen fest, um zu bestimmen, wie die Kopie der Benachrichtigung gesendet wird:

      - `Bcc` - Sendet eine _Blinde Höflichkeitskopie_ indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
      - `Separate Email` - Sendet die Kopie als separate E-Mail.

   - Wenn Sie eine E-Mail-Vorlage vorbereitet haben, die anstelle der Standardvorlage verwendet werden soll, legen Sie **[!UICONTROL Default Company Registration Email]** auf den Namen der Vorlage fest. Standardmäßig wird die `Company Registration Request` verwendet.

     ![Kundenkonfiguration - Unternehmensregistrierung](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. Füllen Sie den **[!UICONTROL Customer-Related Emails]** Abschnitt aus:

   Wenn Sie alternative E-Mail-Vorlagen vorbereitet haben, die anstelle der Standardvorlagen verwendet werden sollen, wählen Sie die Vorlage aus, die Sie für jede der folgenden Aktionen verwenden möchten:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Kundenkonfiguration - Kundenbezogene E-Mails](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. Füllen Sie den **[!UICONTROL Company Status Change]** Abschnitt aus:

   - Legen Sie **[!UICONTROL Company Status Change for Email Recipient]** auf den [Store-Kontakt](../getting-started/store-details.md#store-email-addresses) fest, der benachrichtigt werden soll, wenn sich der Status eines Unternehmens ändert.

   - Geben Sie im Feld **[!UICONTROL Send Company Status Change Email Copy To]** die E-Mail-Adresse jeder Person ein, die eine Kopie der Statusänderungsbenachrichtigung erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch ein Komma.

   - Legen Sie **[!UICONTROL Send Email Copy Method]** auf eine der folgenden Einstellungen fest, um zu bestimmen, wie die Kopie der Benachrichtigung gesendet wird:

      - `Bcc` - Sendet eine _Blinde Höflichkeitskopie_ indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
      - `Separate Email` - Sendet die Kopie als separate E-Mail.

   - Wenn Sie über eine vorbereitete E-Mail-Vorlage verfügen, die anstelle der Standardvorlage verwendet werden soll, wenn sich der Unternehmensstatus von `Pending Approval` in `Active` ändert, legen Sie **[!UICONTROL Default 'Company Status Change to Active 1' Email]** auf diese Vorlage fest. Standardmäßig wird die `Company Status Active 1` verwendet.

   - Wenn Sie über eine vorbereitete E-Mail-Vorlage verfügen, die anstelle der Standardvorlage verwendet werden soll, wenn sich der Unternehmensstatus von `Rejected` oder `Blocked` in `Active` ändert, legen Sie **[!UICONTROL Default 'Company Status Change to Active 2' Email]** auf diese Vorlage fest. Standardmäßig wird die `Company Status Active 2` verwendet.

   - Wenn Sie über eine vorbereitete E-Mail-Vorlage verfügen, die anstelle der Standardvorlage verwendet werden soll, wenn sich der Unternehmensstatus in `Rejected` ändert, legen Sie **[!UICONTROL Default 'Company Status Change to Rejected' Email]** auf diese Vorlage fest. Standardmäßig wird die `Company Status Rejected` verwendet.

   - Wenn Sie über eine vorbereitete E-Mail-Vorlage verfügen, die anstelle der Standardvorlage verwendet werden soll, wenn sich der Unternehmensstatus in `Blocked` ändert, legen Sie **[!UICONTROL Default 'Company Status Change to Blocked' Email]** auf diese Vorlage fest. Standardmäßig wird die `Company Status Blocked` verwendet.

   - Wenn Sie über eine vorbereitete E-Mail-Vorlage verfügen, die anstelle der Standardvorlage verwendet werden soll, wenn sich der Unternehmensstatus in `Pending Approval` ändert, legen Sie **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** auf diese Vorlage fest. Standardmäßig wird die `Company Status Pending Approval` verwendet.

     ![Konfiguration des Kunden - Änderung des Unternehmensstatus](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. Füllen Sie den **[!UICONTROL Company Credit Emails]** Abschnitt aus:

   - Legen Sie **[!UICONTROL Company Credit Change Email Sender]** auf den [Store-](../getting-started/store-details.md#store-email-addresses) fest, der benachrichtigt werden soll, wenn das einem Unternehmen zugewiesene Kreditlimit geändert wird. Standardmäßig wird die Benachrichtigung an den _Vertriebsmitarbeiter_ gesendet.

   - Geben Sie in das Feld **[!UICONTROL Send Company Credit Change Email Copy To]** die E-Mail-Adresse jeder Person ein, die eine Kopie der Gutschriftsänderungsbenachrichtigung erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch ein Komma.

   - Legen Sie **[!UICONTROL Send Email Copy Method]** auf eine der folgenden Einstellungen fest, um zu bestimmen, wie die Kopie der Benachrichtigung gesendet wird:

      - `Bcc` - Sendet eine _Blinde Höflichkeitskopie_ indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
      - `Separate Email` - Sendet die Kopie als separate E-Mail.

   - Wenn Sie E-Mail-Vorlagen vorbereitet haben, die anstelle der Standardvorlagen verwendet werden sollen, wählen Sie die Vorlage für jede der folgenden Benachrichtigungen aus, die an den Unternehmensadministrator gesendet werden.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Kundenkonfiguration - E-Mails zu Firmenkrediten](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
