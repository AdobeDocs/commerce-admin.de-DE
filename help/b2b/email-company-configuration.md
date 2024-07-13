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

Der [Vertriebsmitarbeiter](account-company-manage.md), der als Hauptkontakt für ein Unternehmen zugewiesen ist, ist standardmäßig als Absender vieler automatisierter E-Mail-Nachrichten konfiguriert, die an das Unternehmen gesendet werden.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Company Configuration]** aus.

1. Stellen Sie bei Bedarf **[!UICONTROL Store View]** auf die Store-Ansicht ein, um den [Perimeter](../getting-started/websites-stores-views.md#scope-settings) der Konfiguration zu definieren.

1. Füllen Sie den Abschnitt **[!UICONTROL Company Registration]** aus:

   >[!NOTE]
   >
   >Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** , um das Feld bearbeitbar zu machen.

   - Setzen Sie **[!UICONTROL Company Registration Email Recipient]** auf den [Speicherkontakt](../getting-started/store-details.md#store-email-addresses) , der benachrichtigt werden soll, wenn eine neue Registrierungsanfrage für ein Unternehmen empfangen wird.

   - Geben Sie im Feld **[!UICONTROL Send Company Registration Email Copy To]** die E-Mail-Adresse jeder Person ein, die eine Kopie der Registrierungsbenachrichtigung erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch Kommas.

   - Um zu bestimmen, wie die Kopie der Benachrichtigung gesendet wird, setzen Sie **[!UICONTROL Send Email Copy Method]** auf einen der folgenden Werte:

      - `Bcc` - Sendet eine _Blinde höfliche Kopie_, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
      - `Separate Email` - Sendet die Kopie als separate E-Mail.

   - Wenn Sie eine E-Mail-Vorlage vorbereitet haben, die anstelle der Standardvorlage verwendet werden soll, setzen Sie &quot;**[!UICONTROL Default Company Registration Email]**&quot;auf den Namen der Vorlage. Standardmäßig wird die Vorlage `Company Registration Request` verwendet.

     ![Kundenkonfiguration - Unternehmensregistrierung](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. Füllen Sie den Abschnitt **[!UICONTROL Customer-Related Emails]** aus:

   Wenn Sie alternative E-Mail-Vorlagen für die Verwendung anstelle der Standardeinstellungen vorbereitet haben, wählen Sie die Vorlage aus, die Sie für jeden der folgenden Schritte verwenden möchten:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Kundenkonfiguration - kundenbezogene E-Mails](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. Füllen Sie den Abschnitt **[!UICONTROL Company Status Change]** aus:

   - Setzen Sie **[!UICONTROL Company Status Change for Email Recipient]** auf den [Speicherkontakt](../getting-started/store-details.md#store-email-addresses) , der benachrichtigt werden soll, wenn sich der Status eines Unternehmens ändert.

   - Geben Sie im Feld **[!UICONTROL Send Company Status Change Email Copy To]** die E-Mail-Adresse jeder Person ein, die eine Kopie der Benachrichtigung über die Statusänderung erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch Kommas.

   - Um zu bestimmen, wie die Kopie der Benachrichtigung gesendet wird, setzen Sie **[!UICONTROL Send Email Copy Method]** auf einen der folgenden Werte:

      - `Bcc` - Sendet eine _Blinde höfliche Kopie_, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
      - `Separate Email` - Sendet die Kopie als separate E-Mail.

   - Wenn Sie über eine vorbereitete E-Mail-Vorlage verfügen, die anstelle der Standardvorlage verwendet werden soll, wenn sich der Unternehmensstatus von `Pending Approval` in `Active` ändert, legen Sie **[!UICONTROL Default 'Company Status Change to Active 1' Email]** auf diese Vorlage fest. Standardmäßig wird die Vorlage `Company Status Active 1` verwendet.

   - Wenn Sie über eine vorbereitete E-Mail-Vorlage verfügen, die anstelle der Standardvorlage verwendet werden soll, wenn sich der Unternehmensstatus von `Rejected` oder `Blocked` in `Active` ändert, legen Sie **[!UICONTROL Default 'Company Status Change to Active 2' Email]** auf diese Vorlage fest. Standardmäßig wird die Vorlage `Company Status Active 2` verwendet.

   - Wenn Sie über eine vorbereitete E-Mail-Vorlage verfügen, die anstelle der Standardvorlage verwendet werden soll, wenn sich der Unternehmensstatus in `Rejected` ändert, setzen Sie **[!UICONTROL Default 'Company Status Change to Rejected' Email]** auf diese Vorlage. Standardmäßig wird die Vorlage `Company Status Rejected` verwendet.

   - Wenn Sie über eine vorbereitete E-Mail-Vorlage verfügen, die anstelle der Standardvorlage verwendet werden soll, wenn sich der Unternehmensstatus in `Blocked` ändert, setzen Sie **[!UICONTROL Default 'Company Status Change to Blocked' Email]** auf diese Vorlage. Standardmäßig wird die Vorlage `Company Status Blocked` verwendet.

   - Wenn Sie über eine vorbereitete E-Mail-Vorlage verfügen, die anstelle der Standardvorlage verwendet werden soll, wenn sich der Unternehmensstatus in `Pending Approval` ändert, setzen Sie **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** auf diese Vorlage. Standardmäßig wird die Vorlage `Company Status Pending Approval` verwendet.

     ![Kundenkonfiguration - Änderung des Unternehmensstatus](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. Füllen Sie den Abschnitt **[!UICONTROL Company Credit Emails]** aus:

   - Setzen Sie **[!UICONTROL Company Credit Change Email Sender]** auf den [Speicherkontakt](../getting-started/store-details.md#store-email-addresses) , der benachrichtigt werden soll, wenn eine Änderung an der einem Unternehmen zugewiesenen Kreditbeschränkung vorgenommen wird. Standardmäßig wird die Benachrichtigung an den _Kundenbetreuer_ gesendet.

   - Geben Sie im Feld **[!UICONTROL Send Company Credit Change Email Copy To]** die E-Mail-Adresse jeder Person ein, die eine Kopie der Benachrichtigung über eine Kreditänderung erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch Kommas.

   - Um zu bestimmen, wie die Kopie der Benachrichtigung gesendet wird, setzen Sie **[!UICONTROL Send Email Copy Method]** auf einen der folgenden Werte:

      - `Bcc` - Sendet eine _Blinde höfliche Kopie_, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
      - `Separate Email` - Sendet die Kopie als separate E-Mail.

   - Wenn Sie E-Mail-Vorlagen für die Verwendung anstelle der Standardwerte vorbereitet haben, wählen Sie die Vorlage für jede der folgenden Benachrichtigungen aus, die an den Unternehmensadministrator gesendet werden.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Kundenkonfiguration - E-Mails zu Firmenkrediten](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
