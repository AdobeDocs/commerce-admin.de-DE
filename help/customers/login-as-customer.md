---
title: Unterstützung von Käufern
description: Wenn Sie die Funktion Als Kunde anmelden verwenden, können Sie sehen, was die Kunden sehen, und in ihrem Namen Aktualisierungen vornehmen.
exl-id: 6842ae7a-6440-45f1-af18-e6427088d29d
feature: Customers, Customer Service
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Unterstützung von Käufern

Manchmal benötigen Kunden Hilfe bei ihrer Bestellung. Store-Administratoren können _Als Kunde anmelden_ verwenden, damit sie sehen können, was der Kunde sieht, und Aktualisierungen vornehmen können, um ihn zu unterstützen.

Alle Aktionen, die bei der Anmeldung als Kunde durchgeführt werden, werden auf das Konto des tatsächlichen Kunden angewendet.

Wenn sie für einen Benutzer vom Typ _Admin_ aktiviert ist, wird die Schaltfläche _[!UICONTROL Login as Customer]_auf mehreren Seiten angezeigt:

* [Seite &quot;Kundenbearbeitung&quot;](../customers/update-account.md)
* [Seite &quot;Auftragsansicht&quot;](../stores-purchase/order-processing.md)
* [Rechnungsansichtsseite](../stores-purchase/invoices.md)
* [Seite &quot;Versandansicht&quot;](../stores-purchase/shipments.md)
* [Seite &quot;Credit Memo-Ansicht&quot;](../stores-purchase/credit-memo-create.md)

![Als Kunde anmelden](assets/login-as-customer.png){width="600" zoomable="yes"}

## Aktivieren Sie die Anmeldung als Kunde .

Für die Aktivierung von _Als Kunde anmelden_ müssen Sie die Funktion in Ihrer Commerce-Instanz aktivieren und dann den Zugriff für Admin-Benutzer in den Benutzerrollenberechtigungen aktivieren.

### Funktion aktivieren

1. Wechseln Sie in der Admin-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Login as Customer]** aus.

   ![Konfigurationsoptionen - Als Kunde anmelden](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Enable Login as Customer]** auf `Yes`.

1. _(Optional)_ Legen Sie **[!UICONTROL Disable Page Cache for Admin User]** auf `No` fest, um den Seiten-Cache zu aktivieren, wenn sich der Admin-Benutzer als Kunde anmeldet.

   >[!WARNING]
   >
   > Durch Deaktivieren des Seiten-Caches (`Yes` - Standard) wird sichergestellt, dass der Benutzer, der sich beim Kunden anmeldet, neue, nicht zwischengespeicherte Daten erhält.

1. _(Optional)_ Legen Sie **[!UICONTROL Store View to Log in]** auf `Manual Selection` fest, wenn Sie eine Multi-Site- und/oder Multi-Store-Einrichtung haben und der Administrator die Store-Ansicht beim Anmelden als Kunde auswählen soll.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

### Zugriff für Admin-Benutzer aktivieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _Berechtigungen_ > **[!UICONTROL User Roles]**.

1. Klicken Sie auf die Rolle in der Liste.

1. Klicken Sie im linken Bereich [!UICONTROL _Rolleninformationen_] auf **[!UICONTROL Role Resources]**.

1. Ändern Sie **[!UICONTROL Role Resources]** auf der Seite in `Custom`.

   >[!INFO]
   >
   > Wenn diese Option aktiviert ist, wird die Ressourcenhierarchie auf der Seite angezeigt.

1. Scrollen Sie zum übergeordneten Element **[!UICONTROL Customers]** und zum Element **[!UICONTROL Login as Customer]** darunter. Wählen Sie dann die Ressourcen aus, die Sie für die Rolle aktivieren möchten:

   * **[!UICONTROL Allow Login as Customer]** - Ermöglicht dem Admin-Benutzer die Verwendung der Funktion _Als Kunde anmelden_ .
   * **[!UICONTROL View Login as Customer Log]** - Ermöglicht dem Admin-Benutzer, das Protokoll _Als Kunde anmelden_ anzuzeigen.

   ![Rollenressourcen - Als Kunde anmelden](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Role]**.

## Melden Sie sich vom Administrator als Kunde an

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > [!UICONTROL _Alle Kunden_].

1. Öffnen Sie einen Benutzer im Bearbeitungsmodus.

1. Wählen Sie im Bedienfeld **[!UICONTROL Customer Information]** den Abschnitt **[!UICONTROL Account Information]** aus.

1. Setzen Sie die **[!UICONTROL Allow remote shopping assistance]** auf `Yes`.

   >[!INFO]
   >
   >Der Administrator kann sich jetzt als Benutzer ohne seine Berechtigung von der Storefront aus anmelden.

## Berechtigung für Kundenkonto für Remote-Shopping-Hilfe

Um den Kontozugriff für Mitarbeiter des Store-Supports über den Administrator zu aktivieren, muss ein Kunde die Funktion für sein Konto aktivieren:

1. Der Kunde besucht die Seite &quot;**[!UICONTROL Account Information]**&quot;.

1. Aktiviert das Kontrollkästchen **[!UICONTROL Allow remote shopping assistance]** .

1. Der Kunde klickt auf **[!UICONTROL Save]**.

![Seite mit Kontoinformationen](assets/permission.png){width="700" zoomable="yes"}

>[!WARNING]
>
>Ohne diese Berechtigung kann sich ein Administrator nicht als dieser Kunde anmelden.

## Als Kunde anmelden

>[!INFO]
>
>Um _Als Kunde anmelden_ zu verwenden, stellen Sie sicher, dass Ihr Administrator wie zuvor beschrieben konfiguriert ist.

Mit _Als Kunde anmelden_ können Sie die Site genau so anzeigen, wie der Kunde es tut, und Sie können Fehler beheben und andere Aktionen für den Kunden durchführen. Wenn Sie über eine zugewiesene Benutzerrolle mit den erforderlichen Berechtigungen verfügen:

1. Sie können auf den im vorherigen Abschnitt aufgelisteten Seiten auf &quot;**[!UICONTROL Login as Customer]**&quot;klicken.
1. Die Aktionen Als Kunde anmelden sind im Aktionsbericht verfügbar.

>[!WARNING]
>
>Alle Aktionen, die bei der Anmeldung bei [!UICONTROL _als Kunde_] durchgeführt werden (z. B. Produkte hinzufügen/entfernen), werden auf die tatsächliche Bestellung des Kunden angewendet. Auf der Storefront wird ein Banner angezeigt, wenn Sie `logged in as customer_name` sind, um eine Erinnerung an den speziellen Status zu geben.

## Als Kundenprotokollierung anmelden

{{ee-feature}}

Adobe Commerce stellt eine Protokollierung für die Aktionen _Als Kunde anmelden_ bereit. Er listet alle Sitzungen auf, in denen ein Admin-Benutzer auf die Funktion zugreift. Um auf die protokollierten Aktionen zuzugreifen, gehen Sie zum Bericht [Admin-Aktionen](../systems/action-log-report.md).

Sie können die Berichtseinstellung **[!UICONTROL Action Group]** nach `Login As Customer` oben auf der Seite filtern und auf **[!UICONTROL Search]** klicken.

![Den Aktionsbericht filtern](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}
