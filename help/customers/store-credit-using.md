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

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden im Raster.

1. Im _Aktion_ Spalte, klicken **[!UICONTROL Edit]**.

1. Scrollen _[!UICONTROL Customer View]_Seite und Ansicht des **[!UICONTROL Store Credit Balance]**unten.

![Guthaben-Geschäft](assets/store-credit-balance.png){width="600" zoomable="yes"}

## Aktualisieren des Kontoguthaben des Stores

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > _Aktivitäten_ > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden im Raster.

1. Im _Aktion_ Spalte, klicken **[!UICONTROL Edit]**.

1. Wählen Sie im linken Bereich die Option **[!UICONTROL Store Credit]**.

1. Wählen Sie die Website (Storefront) aus, die Sie mit dem Saldo verbinden möchten.

1. Für **[!UICONTROL Update Balance]**, geben Sie den neuen Wert ein.

1. Um den Kunden über die Bilanzaktualisierung zu informieren, wählen Sie die **[!UICONTROL Notify Customer by Email]** und wählen Sie die Store-Ansicht aus **[!UICONTROL Send Email Notification From the Following Store View]**.

1. Geben Sie einen **[!UICONTROL Comment]** über die Änderung.

1. Klicken Sie nach Abschluss der Aktualisierungen auf **[!UICONTROL Save and Continue Edit]** oder **[!UICONTROL Save Customer]**.

Der aktualisierte Saldo sollte in **[!UICONTROL Balance History]**.

## Anwenden eines Kontos auf eine Bestellung als Store-Administrator

Als Store-Administrator können Sie verschiedene Aufgaben im Namen eines Kunden ausführen, z. B. die Übermittlung von Bestellungen. Wenn Sie [Bestellung erstellen](../stores-purchase/customer-account-create-order.md), können Sie einen Store-Guthaben, der dem Kunden zusteht, verwenden. Der verfügbare Saldo wird im Abschnitt _Zahlungs- und Versandinformationen_ Abschnitt. Wählen Sie die **[!UICONTROL Use Store Credit]** das Kontrollkästchen, um den Saldo anzuwenden, oder einen Teil des Saldos, wenn die Bestellsumme kleiner ist.

![Anwenden des Guthabens des Geschäfts auf die Bestellung](assets/store-credit-apply.png){width="500" zoomable="yes"}

## Anwenden von Store-Gutschriften während des Checkout

Wenn ein Guthaben für die Site vorhanden ist, kann der Kunde die Gutschrift für den Store auf den Bestellstand anwenden, bevor er die Bestellung auf die Storefront stellt.

1. Der Kunde sieht sich den Betrag des verfügbaren Store-Guthabens an.

   Während _Überprüfung und Zahlungen_ Schritt, wird der verfügbare Betrag unter _[!UICONTROL Store Credit]_.

1. Um den Betrag auf die Bestellung anzuwenden, klicken Sie auf **[!UICONTROL Use Store Credit]**.

   >[!INFO]
   >
   >Die Bestellsumme wird neu berechnet und der Betrag des angewendeten Store-Guthabens wird im _[!UICONTROL Order Summary]_.

   ![Auf die Bestellung angewendeter Kreditbetrag speichern](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. Klicks **[!UICONTROL Place Order]**.
