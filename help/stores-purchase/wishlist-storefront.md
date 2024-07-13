---
title: Erlebnis in Listen-Storefront wünschen
description: Erfahren Sie mehr über die Tools zur Verwaltung von Wunschlisten, die Ihren Kunden auf der Storefront zur Verfügung stehen.
exl-id: df8cf89a-c897-4a9a-9e84-3bae946683a4
feature: Customers, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---

# Erlebnis in Listen-Storefront wünschen

Eine Wunschliste ist eine bequeme Möglichkeit für Kunden, sich an Produkte zu erinnern, die sie mögen, aber noch nicht zum Kauf bereit sind. Artikel aus einer Wunschliste können für andere freigegeben oder dem Warenkorb hinzugefügt werden. Wenn der Kunde über mehrere Wunschlisten verfügt, wird der Name der aktuellen Wunschliste oben auf der Seite angezeigt. Kunden können ihre Wunschlisten über ihr Konto-Dashboard verwalten. Store-Administratoren können Kunden auch bei der Verwaltung ihrer Wunschlisten über den Administrator unterstützen.

![Beispiel-Storefront - Meine Wunschliste](./assets/storefront-my-wishlist.png){width="700" zoomable="yes"}

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce unterstützt die Verwendung mehrerer Wunschlisten pro Kundenkonto.

![Magento Open Source](../assets/open-source.svg) Die Codebasis der Magento Open Source unterstützt die Verwendung einer einzigen Wunschliste pro Kundenkonto.

## Erstellen einer Wunschliste

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

Im Storefront kann ein Kunde eine Wunschliste aus seinem Konto-Dashboard, einer Produktseite, einer Katalogseite und dem Warenkorb erstellen.

### Methode 1: Aus einem Kundenkonto

1. In der Seitenleiste des Konto-Dashboards wählt der Kunde **[!UICONTROL My Wish List]** aus.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Create New Wish List]**.

1. Geben Sie den Namen der Wunschliste ein.

1. Um anderen die Anzeige ihrer Wunschliste zu ermöglichen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Public Wish List]** .

   >[!NOTE]
   >
   >Der Hauptunterschied zwischen den Wunschlisten `Public` und `Private` besteht darin, dass private Wunschlisten nicht durch Wunschlisten [durchsuchbar](wishlist-configuration.md#add-wish-list-search) sind.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

   ![Neue Wunschliste erstellen](./assets/account-dashboard-wishlist-create-new.png){width="700" zoomable="yes"}

### Methode 2: Auf der Katalogseite

1. Der Kunde ruft von der Storefront die Katalogseite auf, die das Produkt enthält, das er einer Wunschliste hinzufügen möchte.

1. Bewegen Sie die Maus über das Produkt.

1. Der Kunde klickt auf den Pfeil neben dem Symbol _Zur Wunschliste hinzufügen_ und wählt **[!UICONTROL Create New Wish List]** aus.

1. Fügt den Namen der Wunschliste ein.

1. Um anderen die Anzeige ihrer Wunschliste zu ermöglichen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Public Wish List]** .

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

### Methode 3: Auf der Produktdetailseite

1. Der Kunde ruft von der Storefront die Detailseite des Produkts auf, das er einer Wunschliste hinzufügen möchte.

1. Klicken Sie auf den Pfeil neben **[!UICONTROL Add to Wish List]** und wählen Sie **[!UICONTROL Create New Wish List]** aus.

1. Fügt den Wert **[!UICONTROL Wish List Name]** ein.

1. Um anderen die Anzeige ihrer Wunschliste zu ermöglichen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Public Wish List]** .

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

   ![Erstellen einer neuen Wunschliste von der Produktdetailseite](./assets/account-dashboard-wishlist-create-from-pdp.png){width="700" zoomable="yes"}

### Methode 4: Aus dem Warenkorb

1. Der Kunde öffnet die Seite &quot;**[!UICONTROL Shopping Cart]**&quot;.

1. Klicken Sie unter dem Element auf den Pfeil neben **[!UICONTROL Move to Wishlist]** und wählen Sie **[!UICONTROL Create New Wish List]** aus.

1. Fügt den Wert **[!UICONTROL Wish List Name]** ein.

1. Um anderen die Anzeige ihrer Wunschliste zu ermöglichen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Public Wish List]** .

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

![Erstellen einer neuen Wunschliste von der Seite &quot;Warenkorb&quot;](./assets/account-dashboard-wishlist-create-from-cart.png){width="700" zoomable="yes"}

## Aktualisieren der Produktliste

1. Aus der Wunschliste verweist der Kunde auf das Produkt, um die Optionen anzuzeigen.

1. Um eine **[!UICONTROL Comment]** für das Produkt hinzuzufügen, geben Sie den Text in das Feld unter dem Preis ein.

   ![Bearbeitungsoptionen](./assets/account-dashboard-wishlist-edit-options.png){width="700" zoomable="yes"}

1. Um die Auswahl der Produktoptionen zu ändern, klicken Sie auf **[!UICONTROL Edit]** und gehen wie folgt vor:

   - Aktualisiert die Optionen auf der Produktdetailseite.
   - Klicks **[!UICONTROL Update Wish List]**.

## Hinzufügen eines Wunschlistenprodukts zum Warenkorb

1. In der Wunschliste verweist der Kunde auf das Produkt, das Sie hinzufügen möchten.

1. Aktualisiert die **[!UICONTROL Qty]** und bearbeitet die anderen Optionen nach Bedarf.

1. Klicks **[!UICONTROL Add to Cart]**.

## Wunschliste freigeben

1. Der Kunde klickt auf **[!UICONTROL Share Wishlist]**.

1. Fügt die E-Mail-Adresse jeder Person ein, die die Wunschliste erhalten soll, getrennt durch Kommas.

1. Fügt einen **[!UICONTROL Message]** hinzu, der in die E-Mail aufgenommen werden soll.

1. Klicks **[!UICONTROL Share Wish List]**.

   ![Geben Sie Ihre Wunschliste frei](./assets/account-dashboard-wishlist-sharing.png){width="700" zoomable="yes"}

   Die Nachricht wird von Ihrem primären [Store-Kontakt](../getting-started/store-details.md#store-email-addresses) gesendet und enthält ein Miniaturbild jedes Produkts mit Links zu Ihrem Store.

   ![Freigegebene Wunschlisten-E-Mail](./assets/account-dashboard-wishlist-sharing-email.png){width="500" zoomable="yes"}

## Bearbeiten von Wunschlisten

Kunden können ihre Wunschliste auf verschiedene Weise über ihr Konto-Dashboard ändern.

### Verschieben von Elementen in eine andere Liste

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

1. Der Kunde wählt das Kontrollkästchen jedes zu verschiebenden Elements aus.

1. klickt auf **[!UICONTROL Move Selected to Wish List]** und führt einen der folgenden Schritte aus:

   - Auswahl einer existierenden Wunschliste.
   - Klicks **[!UICONTROL Create New Wish List]**.

### Elemente in eine andere Liste kopieren

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

1. Aktivieren Sie das Kontrollkästchen der zu verschiebenden Elemente.

1. klickt auf **[!UICONTROL Copy Selected to Wish List]** und führt einen der folgenden Schritte aus:

   - Auswahl einer existierenden Wunschliste.
   - Klicks **[!UICONTROL Create New Wish List]**.

## Wunschliste löschen

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

1. Der Kunde öffnet die zu löschende Wunschliste.

1. Klicks **[!UICONTROL Delete Wish List]**.

1. Wenn Sie zur Bestätigung aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.

>[!IMPORTANT]
>
>Diese Aktion kann nicht rückgängig gemacht werden.

## Übertragen von Wunschlistenelementen in den Warenkorb

Um alle Wunschlisteneinträge in den Warenkorb zu übertragen, klickt der Kunde auf **[!UICONTROL Add All to Cart]**.

Um ein einzelnes Element hinzuzufügen, führt der Kunde folgende Schritte durch:

1. Bewegen Sie den Mauszeiger über das Element und geben Sie den **[!UICONTROL Qty]** ein, den sie zum Warenkorb hinzufügen möchten.

1. Klicks **[!UICONTROL Add to Cart]**.

## Kundenwunschliste suchen

Wenn das Widget [Wunschlisten-Suche](wishlist-configuration.md#add-wish-list-search) in Ihren Store-Seiten enthalten ist, können Kunden nach dem Namen oder der E-Mail-Adresse des Eigentümers der Wunschliste suchen.

1. Im Widget zur Wunschlisten-Suche wählt der Kunde eine Suchoption aus.

1. Fügt den Namen oder die E-Mail-Adresse des Eigentümers der Wunschliste ein und klickt auf **[!UICONTROL Search]**.

   Die Seite _Suche nach Listen_ wird geöffnet und alle entsprechenden Wunschlisten werden im Abschnitt mit den Suchergebnissen angezeigt.

   >[!NOTE]
   >
   >In den Suchergebnissen werden nur öffentliche Wunschlisten angezeigt - die privaten Wunschlisten der Kunden sind nicht öffentlich sichtbar.

1. Um die Liste der gewünschten Listenelemente anzuzeigen, klicken Sie auf **[!UICONTROL View]**.

   Der Name des Eigentümers und das Datum der letzten Aktualisierung werden für jede Wunschliste angezeigt.

1. Um ein Produkt zum Warenkorb hinzuzufügen, markiert der Kunde das Kontrollkästchen unter dem Produkt und klickt auf **[!UICONTROL Add to Cart]**.

   Sie können auch von der Wunschliste eines anderen Kunden gewünschte Artikel hinzufügen.
