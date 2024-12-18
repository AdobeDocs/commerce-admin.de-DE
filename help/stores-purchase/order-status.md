---
title: Bestellstatus
description: Erfahren Sie mehr über die vordefinierten Bestellstatus und wie Sie benutzerdefinierte Bestellstatus definieren können, um sie an Ihre betrieblichen Anforderungen anzupassen.
exl-id: d1153558-a721-4643-a70c-7fc20072983c
feature: Orders
source-git-commit: c2d5e9b41a76ba58d1343a8b3ee5122104d5bfe0
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Bestellstatus

Alle Bestellungen haben einen Bestellstatus, der mit einem Schritt in der Auftragsverarbeitung (Workflow[ verknüpft ](order-processing.md).\
Der Unterschied zwischen Bestellstatus und Bestellstatus besteht darin, dass **[!UICONTROL order states]** programmgesteuert verwendet werden. Sie sind es nicht
Sichtbar für Kunden oder Admin-Benutzer. Sie bestimmen den Ablauf eines Auftrags und welche Vorgänge für einen Auftrag möglich sind
Bestellung in einem bestimmten Zustand.\
**[!UICONTROL Order statuses]** werden verwendet, um den Status einer Bestellung Kunden und Admin-Benutzern mitzuteilen.
Sie können zusätzliche Bestellstatus entsprechend Ihren betrieblichen Anforderungen erstellen. Der Bestellstatus lässt sich bequem anzeigen
Fortschritt außerhalb von Adobe Commerce, z. B. Kommissionierung und Versandfortschritt. Sie haben keine Auswirkungen auf die Bestellung
Verarbeitungs-Workflow.\
Jeder Bestellstatus ist mit einem Bestellstatus verknüpft. Ihr Store verfügt über einen Satz vordefinierter Bestellstatus und
Einstellungen für den Bestellstatus.

![Bestellstatus und -status](./assets/order-states-and-statuses.png){width="700" zoomable="yes"}

Der Status jeder Bestellung wird in der Spalte _Status_ des Rasters _Bestellungen_ angezeigt.

![Bestellstatus](./assets/stores-order-status-column.png){width="700" zoomable="yes"}

>[!TIP]
>
>Eine teilweise zurückerstattete Bestellung verbleibt im `Processing`, bis **_alle_** bestellten Artikel (einschließlich zurückerstatteter Artikel) versendet werden. Der Bestellstatus ändert sich erst dann in `Complete`, wenn jeder Artikel der Bestellung versendet wurde.

## Workflow für den Bestellstatus

![Workflow Bestellstatus](./assets/order-state-workflow.png)

## Vordefinierter Status

| Bestellstatus | Statuscode |                                                                                                                                                                                                                                                                                        |
|--------------------------|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Received | `received` | Dieser Status ist der Anfangsstatus für Bestellungen, die aufgegeben werden, wenn die asynchrone Auftragserteilung aktiviert ist. |
| Betrugsverdacht | `fraud` | Manchmal werden Bestellungen, die über PayPal oder ein anderes Zahlungs-Gateway bezahlt werden, als &quot;_Betrug“_. Dieser Status bedeutet, dass für die Bestellung keine Rechnung ausgestellt wurde und die Bestätigungs-E-Mail ebenfalls nicht gesendet wird. |
| Verarbeitung läuft | `processing` | Wenn der Status neuer Bestellungen auf „Verarbeitung“ gesetzt ist, wird die Option _Alle Artikel automatisch fakturieren_ in der Konfiguration verfügbar. Für Bestellungen, die mit Geschenkkarte, Store-Guthaben, Belohnungspunkten oder anderen Offline-Zahlungsmethoden aufgegeben werden, werden keine Rechnungen automatisch erstellt. |
| Zahlung ausstehend | `pending_payment` | Dieser Status wird verwendet, wenn die Bestellung erstellt wird und PayPal oder eine ähnliche Zahlungsmethode verwendet wird. Dies bedeutet, dass der Kunde zur Zahlungs-Gateway-Website weitergeleitet wurde, aber noch keine Rückgabeinformationen eingegangen sind. Dieser Status ändert sich, wenn der Kunde bezahlt. |
| Zahlungsüberprüfung | `payment_review` | Dieser Status wird angezeigt, wenn die Überprüfung der PayPal-Zahlung aktiviert ist. |
| Ausstehend | `pending` | Dieser Status gibt an, dass keine Rechnung und Lieferungen eingereicht wurden. |
| Zurückgestellt | `holded` | Dieser Status kann nur manuell zugewiesen werden. Sie können jede Bestellung zurückstellen. |
| Abgeschlossen | `complete` | Dieser Status bedeutet, dass die Bestellung erstellt, bezahlt und an den Kunden versendet wird. |
| geschlossen | `closed` | Dieser Status zeigt an, dass einer Bestellung eine Gutschrift zugewiesen wurde und der Kunde eine Rückerstattung erhalten hat. |
| Abgebrochen | `canceled` | Dieser Status wird manuell im Administrator zugewiesen oder bei einigen Zahlungs-Gateways, wenn der Kunde nicht innerhalb der angegebenen Zeit zahlt. |
| abgelehnt | `rejected` | Dieser Status bedeutet, dass eine Bestellung bei der asynchronen Auftragsverarbeitung abgelehnt wurde. Dies geschieht, wenn während der asynchronen Auftragserteilung ein Fehler auftritt. |
| PayPal stornierte die Rückbuchung | `paypay_canceled_reversal` | Dieser Status bedeutet, dass PayPal die Rückbuchung storniert hat. |
| Pending PayPal | `pending_paypal` | Dieser Status bedeutet, dass die Bestellung bei PayPal eingegangen ist, die Zahlung jedoch noch nicht bearbeitet wurde. |
| PayPal umgekehrt | `paypal_reversed` | Dieser Status bedeutet, dass PayPal die Transaktion rückgängig gemacht hat. |

{style="table-layout:auto"}

## Benutzerdefinierter Bestellstatus

Zusätzlich zu den voreingestellten Bestellstatus-Einstellungen können Sie eigene benutzerdefinierte Bestellstatus-Einstellungen erstellen, diese den Bestellstatus zuweisen und Standardbestellungsstatus für den Bestellstatus festlegen. Der Bestellstatus gibt die Position der Bestellung innerhalb des Auftragsverarbeitungs-Workflows an und der Bestellstatus weist der Position der Bestellung eine aussagekräftige übersetzbare Beschriftung zu. Möglicherweise benötigen Sie beispielsweise einen benutzerdefinierten Bestellstatus wie `packaging"`, `backordered` oder einen Status, der speziell auf Ihre Anforderungen zugeschnitten ist. Sie können einen beschreibenden Namen für den benutzerdefinierten Status erstellen und ihn dem zugehörigen Bestellstatus im Workflow zuweisen.

>[!NOTE]
>
>Im Auftrags-Workflow werden nur standardmäßige benutzerdefinierte Auftragsstatuswerte verwendet. Benutzerdefinierte Statuswerte, die nicht als Standard festgelegt sind, können nur im Kommentarbereich der Bestellung verwendet werden.

![Einstellungen für den Bestellstatus](./assets/order-status.png){width="700" zoomable="yes"}

### Erstellen eines benutzerdefinierten Bestellstatus

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Order Status]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Create New Status]**.

   ![Neuen Bestellstatus erstellen](./assets/order-status-new.png){width="600" zoomable="yes"}

1. Aktualisieren Sie den Abschnitt _[!UICONTROL Order Status Information]_:

   - Geben Sie eine **[!UICONTROL Status Code]** als interne Referenz ein. Das erste Zeichen muss ein Buchstabe (a-z) sein, der Rest kann eine beliebige Kombination aus Buchstaben und Zahlen (0-9) sein. Verwenden Sie den Unterstrich anstelle eines Leerzeichens.

   - Geben Sie **[!UICONTROL Status Label]** einen Titel ein, der die Statuseinstellung sowohl in der Admin- als auch in der Storefront identifiziert.

1. Geben Sie im Abschnitt _[!UICONTROL Store View Specific Labels]_alle Beschriftungen ein, die für verschiedene Store-Ansichten erforderlich sind.

1. Klicken Sie auf **[!UICONTROL Save Status]**.

### Zuweisen eines Bestellstatus zu einem Status

1. Klicken Sie auf der _Bestellstatus_-Seite auf **[!UICONTROL Assign Status to State]**.

   ![Status zuweisen](./assets/store-status-assign-status.png){width="600" zoomable="yes"}

1. Aktualisieren Sie den Abschnitt **[!UICONTROL Assignment Information]** und gehen Sie folgendermaßen vor:

   - Wählen Sie die **[!UICONTROL Order Status]** aus, die Sie zuweisen möchten. Sie werden nach Statuslabel aufgelistet.

   - Setzen Sie **[!UICONTROL Order State]** auf die Stelle im Workflow, an die der Bestellstatus gehört.

     >[!NOTE]
     >
     >**_[!UICONTROL Order State]_** Liste enthält die standardmäßig zugewiesenen Bestellstatus. Beispielsweise wird der `Pending` Standardbestellungsstatus anstelle des `New` Bestellstatus angezeigt.

   - Um diesen Status als Standard für den Bestellstatus festzulegen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Use Order Status as Default]** .

     >[!NOTE]
     >
     >Im Auftrags-Workflow werden nur die standardmäßigen Bestellstatus verwendet. Nicht standardmäßige Statuswerte können nur im Abschnitt **[!UICONTROL Order Comments]** in der Admin-Liste festgelegt werden.

   - Um diesen Status in der Storefront sichtbar zu machen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Visible On Storefront]** .

   ![Status dem Status zuweisen](./assets/order-status-assign-state.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Status Assignment]**.

### Bearbeiten eines vorhandenen Bestellstatus

1. Öffnen Sie im _[!UICONTROL Order Status]_den Statusdatensatz im Bearbeitungsmodus.

1. Statuseinstellungen nach Bedarf aktualisieren.

1. Klicken Sie auf **[!UICONTROL Save Status]**.

### Entfernen eines Bestellstatus aus einem zugewiesenen Status

>[!NOTE]
>
>Die Zuweisung einer Statuseinstellung zu einem Status kann nicht aufgehoben werden, wenn der Status in Verwendung ist.

1. Suchen Sie im _[!UICONTROL Order Status]_Raster nach dem Datensatz mit dem Bestellstatus, dessen Zuweisung aufgehoben werden soll.

1. Klicken Sie in der Spalte _[!UICONTROL Action]_ganz rechts in der Zeile auf den Link **[!UICONTROL Unassign]**.

   Oben im Arbeitsbereich wird eine Meldung angezeigt, dass die Zuweisung des Bestellstatus aufgehoben wurde. Obwohl die Beschriftung Bestellstatus weiterhin in der Liste angezeigt wird, ist sie keinem Status mehr zugewiesen. Einstellungen zum Bestellstatus können nicht gelöscht werden.

>[!NOTE]
>
>Wenn die Zuweisung des Standardbestellungsstatus zum Bestellstatus aufgehoben wird, wird _**ein anderer**_ Bestellstatus _**automatisch festgelegt**_ als Standard für diesen Bestellstatus festgelegt.

## Benachrichtigung

Kunden können den Status ihrer Bestellungen über [RSS-Feed](../merchandising-promotions/social-rss.md) verfolgen, wenn der RSS-Feed für die Bestellung in der Konfiguration aktiviert ist. Wenn diese Option aktiviert ist, wird bei jeder Bestellung ein Link zum RSS-Feed angezeigt.

### Benachrichtigung zum Bestellstatus aktivieren

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie darunter **[!UICONTROL RSS Feeds]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Order]** .

1. Legen Sie **[!UICONTROL Customer Order Status Notification]** auf `Enable` fest.

   ![Benachrichtigung zum Bestellstatus des Kunden](../configuration-reference/catalog/assets/rss-feeds-order.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

### Konfigurieren von E-Mail-Benachrichtigungen für neue Bestellungen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie darunter **[!UICONTROL Sales Emails]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Order]** .

   ![Konfiguration - Bestelloptionen](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL New Order Confirmation Email Sender]** auf eine der folgenden Einstellungen fest:

   - `General Contact`
   - `Sales Representative`
   - `Customer Support`
   - `Custom Email 1`
   - `Custom Email 2`

1. Wählen Sie die Vorlagen aus, die Sie für jeden Kundentyp verwenden möchten:

   - **[!UICONTROL New Order Confirmation Template]** : Wählen Sie eine Vorlage aus, die für Kunden mit einem registrierten Store-Konto verwendet werden soll.
   - **[!UICONTROL New Order Confirmation Template for Guest]** : Wählen Sie eine Vorlage aus, die für Gastkunden ohne registriertes Store-Konto verwendet werden soll.

1. Um eine andere Person (z. B. einen Business Manager) über die neue Bestellung zu informieren, geben Sie die E-Mail-Adresse ein, die **[!UICONTROL Send Order Email Copy To]** werden soll.

   Sie können mehrere E-Mail-Adressen hinzufügen, wenn mehr als ein Empfänger erforderlich ist.

1. Legen Sie die **[!UICONTROL Send Order Email Copy Method]** auf einen der folgenden Werte fest:

   - `Bcc` - Sowohl an den Kunden als auch an den zusätzlichen Empfänger wird nur eine E-Mail über die neue Bestellung gesendet, der Kunde sieht jedoch nicht, dass die empfangene E-Mail auch an den zusätzlichen Empfänger gesendet wurde.
   - `Separate Email` - Zwei separate E-Mails werden gesendet, eine an den Empfänger und eine an den Kunden.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
