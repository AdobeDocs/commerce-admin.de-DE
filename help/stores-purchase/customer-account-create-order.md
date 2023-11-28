---
title: Bestellung erstellen
description: Erfahren Sie, wie Sie im Commerce Admin eine Bestellung für einen Kunden erstellen.
exl-id: 8a766a5b-55d6-4d78-859e-38937e0183d3
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 1%

---

# Bestellung erstellen

Für registrierte Kunden, die Hilfe benötigen, können Sie direkt vom Administrator eine gesamte Bestellung erstellen. Die _[!UICONTROL Create New Order]_-Formular enthält alle Informationen, die für den normalen Checkout-Prozess erforderlich sind, mit Aktivitätszusammenfassungen aus dem Konto-Dashboard des Kunden.

![Erstellen einer Bestellung für einen Kunden](./assets/create-new-order.png){width="700" zoomable="yes"}

## Schritt 1: Bestellung erstellen

1. Im _Admin_ Seitenleiste, klicken Sie **[!UICONTROL Customers]**.

1. Suchen Sie den Kunden im Raster.

1. Im _Aktion_ Spalte, klicken **[!UICONTROL Edit]**.

1. Klicken Sie in der Workspace-Kopfzeile auf **[!UICONTROL Create Order]**.

   ![Workspace-Kopfzeile](./assets/order-create-buttons.png){width="700" zoomable="yes"}

   Sie können auch eine Bestellung im [Auftragsarbeitsbereich](orders.md#orders-workspace) durch Klicken auf **[!UICONTROL Create New Order]**.

## Schritt 2: Produkte hinzufügen

Wenn Ihr Store mehrere Ansichten hat, wählen Sie die Store-Ansicht, in der die Bestellung platziert werden soll.

### Fügen Sie Produkte aus der [!UICONTROL Customer's Activities] Seitenleiste

Sie können Artikel aus der Wunschliste eines Kunden oder aus kürzlich angezeigten, verglichenen oder bestellten Artikeln in den Warenkorb übertragen.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) einen der folgenden Abschnitte:

   - **[!UICONTROL Wish List]**
   - **[!UICONTROL Last Ordered Items]**
   - **[!UICONTROL Products in Comparison List]**
   - **[!UICONTROL Recently Compared Products]**
   - **[!UICONTROL Recently Viewed Products]**

1. Aktivieren Sie im linken Bereich das Kontrollkästchen jedes Produkts.

1. Scrollen Sie nach unten und klicken Sie auf **[!UICONTROL Update Changes]**.

   Das Element wird im Bestellformular angezeigt.

   ![Zum Warenkorb hinzufügen](./assets/create-order-add-wishlist.png){width="600" zoomable="yes"}

### Produkte aus dem Katalog hinzufügen

1. Klicken **[!UICONTROL Add Products]**.

   ![Produkte hinzufügen](./assets/account-add-wishlist-product.png){width="600" zoomable="yes"}

1. Aktivieren Sie im Raster das Kontrollkästchen der einzelnen Produkte, die dem Warenkorb hinzugefügt werden sollen, und geben Sie die **[!UICONTROL Qty]** zu erwerben.

   ![Produkte auswählen](./assets/create-order-from-catalog.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Das Produktauswahlraster zeigt stets die regulären Basispreise für Produkte ohne Rabatte und ohne angewendete Warenkorb- oder Gruppenpreisregeln an. Der Endproduktpreis wird nur berechnet, wenn das Produkt einer Bestellung/einem Warenkorb hinzugefügt wird.

1. Konfigurieren der verfügbaren Produktoptionen:

   - Klicken **[!UICONTROL Configure]**.

   - Füllen Sie die Optionen nach Bedarf aus.

   - Klicken **[!UICONTROL OK]**.

   - Klicks **[!UICONTROL Add Selected Product(s) to Order]** , um den Warenkorb zu aktualisieren.

1. Wenn ein Produkt für [Geschenkoptionen](../catalog/product-gift-options.md), legen Sie die Optionen nach Bedarf fest.

1. Den Preis eines Artikels bei Bedarf überschreiben:

   - Wählen Sie die **[!UICONTROL Custom Price]** und geben Sie den neuen Preis in das unten stehende Feld ein.

   - Um die Warenkorbsummen zu aktualisieren, klicken Sie auf **[!UICONTROL Update Items and Quantities]**.

   ![Benutzerspezifischer Preis](./assets/create-order-custom-price.png){width="600" zoomable="yes"}

1. Füllen Sie nach Bedarf die folgenden Abschnitte für die Bestellung aus:

   - [!UICONTROL Order Currency]
   - [!UICONTROL Apply Coupon Codes / Gift Card Code]
   - [!UICONTROL Payment Method]
   - [!UICONTROL Shipping Method]
   - [!UICONTROL Order Comments]

>[!NOTE]
>
>Siehe [Handbuch für Zahlungsdienste](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/create-order.html) für weitere Informationen zu Zahlungsmethoden, die diese Funktionalität unterstützen, wenn die Zahlungsdiensterweiterung installiert und konfiguriert ist.

## Schritt 3: Bestellung absenden

Klicken **[!UICONTROL Submit Order]**.

Eine Bestätigung wird an den Kunden gesendet und der Kunde kann die Bestelldetails über sein Konto anzeigen.
