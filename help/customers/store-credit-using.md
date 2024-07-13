---
title: Anwenden von Store-Gutschriften
description: Store-Administratoren können eine Store-Gutschrift auf einen Kauf anwenden.
exl-id: 97b6b206-71db-435c-8736-a781437bb0b4
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Anwenden von Store-Gutschriften

{{ee-feature}}

Store-Administratoren können das Guthaben und den Verlauf aus dem Kundenkonto anzeigen und auch eine Speichernutzung auf einen Kauf anwenden.

![Kundenkreditkonto und -verlauf](assets/store-credit-balance-history.png){width="600" zoomable="yes"}

## Guthaben anzeigen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden im Raster.

1. Klicken Sie in der Spalte _Aktion_ auf **[!UICONTROL Edit]**.

1. Scrollen Sie auf der Seite _[!UICONTROL Customer View]_nach unten und sehen Sie sich die **[!UICONTROL Store Credit Balance]**unten an.

![Guthabenkonto speichern](assets/store-credit-balance.png){width="600" zoomable="yes"}

## Aktualisieren des Kontoguthaben des Stores

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > _Vorgänge_ > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden im Raster.

1. Klicken Sie in der Spalte _Aktion_ auf **[!UICONTROL Edit]**.

1. Wählen Sie im linken Bereich **[!UICONTROL Store Credit]** aus.

1. Wählen Sie die Website (Storefront) aus, die Sie mit dem Saldo verbinden möchten.

1. Geben Sie für &quot;**[!UICONTROL Update Balance]**&quot;den neuen Wert ein.

1. Um den Kunden über die Aktualisierung des Kontostands zu informieren, aktivieren Sie das Kontrollkästchen **[!UICONTROL Notify Customer by Email]** und wählen Sie die Store-Ansicht unter **[!UICONTROL Send Email Notification From the Following Store View]** aus.

1. Geben Sie eine **[!UICONTROL Comment]** für die Änderung ein.

1. Wenn die Aktualisierungen abgeschlossen sind, klicken Sie auf **[!UICONTROL Save and Continue Edit]** oder **[!UICONTROL Save Customer]**.

Der aktualisierte Saldo sollte in **[!UICONTROL Balance History]** angezeigt werden.

## Anwenden eines Kontos auf eine Bestellung als Store-Administrator

Als Store-Administrator können Sie verschiedene Aufgaben im Namen eines Kunden ausführen, z. B. die Übermittlung von Bestellungen. Wenn Sie [eine Bestellung erstellen](../stores-purchase/customer-account-create-order.md), können Sie einen Store-Guthabenkonto anwenden, der dem Kunden zusteht. Der verfügbare Restbetrag wird im Abschnitt _Zahlungs- und Versandinformationen_ angezeigt. Aktivieren Sie das Kontrollkästchen **[!UICONTROL Use Store Credit]** , um den Restbetrag anzuwenden, oder einen Teil des Restbetrags, wenn die Bestellsumme kleiner ist.

![Wenden Sie das Konto für den Store-Kredit auf die Bestellung an](assets/store-credit-apply.png){width="500" zoomable="yes"}

## Anwenden von Store-Gutschriften während des Checkout

Wenn ein Guthaben für die Site vorhanden ist, kann der Kunde die Gutschrift für den Store auf den Bestellstand anwenden, bevor er die Bestellung auf die Storefront stellt.

1. Der Kunde sieht sich den Betrag des verfügbaren Store-Guthabens an.

   Während des Schritts _Überprüfung und Zahlungen_ wird der verfügbare Betrag unter _[!UICONTROL Store Credit]_angezeigt.

1. Um den Betrag auf die Bestellung anzuwenden, klicken Sie auf **[!UICONTROL Use Store Credit]**.

   >[!INFO]
   >
   >Die Bestellsumme wird neu berechnet und der Betrag der angewendeten Store-Gutschriften wird in der _[!UICONTROL Order Summary]_angezeigt.

   ![Auf die Bestellung angewendeter Kontostand speichern](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. Wenn fertig, klickt auf **[!UICONTROL Place Order]**.
