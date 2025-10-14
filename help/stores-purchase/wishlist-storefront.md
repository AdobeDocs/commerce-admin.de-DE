---
title: Wunschliste Storefront-Erlebnis
description: Erfahren Sie mehr über die Tools zur Verwaltung von Wunschlisten, die Ihren Kunden in der Storefront zur Verfügung stehen.
exl-id: df8cf89a-c897-4a9a-9e84-3bae946683a4
feature: Customers, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---

# Wunschliste Storefront-Erlebnis

Eine Wunschliste ist eine praktische Möglichkeit für Kunden, Produkte zurückzurufen, die ihnen gefallen, aber nicht kaufbereit sind. Artikel aus einer Wunschliste können mit anderen geteilt oder zum Warenkorb hinzugefügt werden. Wenn der Kunde mehrere Wunschlisten hat, wird der Name der aktuellen Wunschliste oben auf der Seite angezeigt. Kunden können ihre Wunschlisten über ihr Konto-Dashboard verwalten. Store-Administratoren können Kunden auch bei der Verwaltung ihrer Wunschlisten über den Administrator helfen.

![Beispiel-Storefront - Meine Wunschliste](./assets/storefront-my-wishlist.png){width="700" zoomable="yes"}

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce unterstützt die Verwendung mehrerer Wunschlisten pro Kundenkonto.

![Magento Open Source &#x200B;](../assets/open-source.svg) Die Magento Open Source-Code-Basis unterstützt die Verwendung einer einzigen Wunschliste pro Kundenkonto.

## Erstellen einer Wunschliste

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

In der Storefront kann eine Kundin oder ein Kunde eine Wunschliste aus seinem bzw. seinem Konto-Dashboard, einer Produktseite, einer Katalogseite und dem Warenkorb erstellen.

### Methode 1: Von einem Kundenkonto

1. In der Seitenleiste des Konto-Dashboards wählt der Kunde **[!UICONTROL My Wish List]** aus.

1. Klicken Sie oben rechts auf **[!UICONTROL Create New Wish List]**.

1. Geben Sie den Namen der Wunschliste ein.

1. Damit andere Benutzer ihre Wunschliste sehen können, aktivieren Sie das Kontrollkästchen **[!UICONTROL Public Wish List]** .

   >[!NOTE]
   >
   >Der Hauptunterschied zwischen `Public` und `Private` Wunschlisten besteht darin, dass private Wunschlisten nicht [&#x200B; durchsuchbar &#x200B;](wishlist-configuration.md#add-wish-list-search).

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

   ![Neue Wunschliste erstellen](./assets/account-dashboard-wishlist-create-new.png){width="700" zoomable="yes"}

### Methode 2: Von der Katalogseite aus

1. Von der Storefront aus navigiert der Kunde zur Katalogseite, die das Produkt enthält, das er einer Wunschliste hinzufügen möchte.

1. Bewegen Sie den Mauszeiger über das Produkt.

1. Der Kunde klickt auf den Pfeil neben dem Symbol _Zur Wunschliste hinzufügen_ und wählt die **[!UICONTROL Create New Wish List]** aus.

1. Gibt den Namen der Wunschliste ein.

1. Damit andere Benutzer ihre Wunschliste sehen können, aktivieren Sie das Kontrollkästchen **[!UICONTROL Public Wish List]** .

1. Wenn Sie fertig sind, klicken Sie **[!UICONTROL Save]**.

### Methode 3: Von der Produktdetailseite

1. Von der Storefront aus navigiert der Kunde zur Detailseite des Produkts, das er einer Wunschliste hinzufügen möchte.

1. Klicken Sie auf den Pfeil neben **[!UICONTROL Add to Wish List]** und wählen Sie **[!UICONTROL Create New Wish List]** aus.

1. Betritt die **[!UICONTROL Wish List Name]**.

1. Damit andere Benutzer ihre Wunschliste sehen können, aktivieren Sie das Kontrollkästchen **[!UICONTROL Public Wish List]** .

1. Wenn Sie fertig sind, klicken Sie **[!UICONTROL Save]**.

   ![Erstellen Sie eine neue Wunschliste auf der Produktdetailseite](./assets/account-dashboard-wishlist-create-from-pdp.png){width="700" zoomable="yes"}

### Methode 4: Aus dem Warenkorb

1. Kunde öffnet die **[!UICONTROL Shopping Cart]**.

1. Klicken Sie unter dem Element auf den Pfeil neben **[!UICONTROL Move to Wishlist]** und wählen Sie **[!UICONTROL Create New Wish List]** aus.

1. Betritt die **[!UICONTROL Wish List Name]**.

1. Damit andere Benutzer ihre Wunschliste sehen können, aktivieren Sie das Kontrollkästchen **[!UICONTROL Public Wish List]** .

1. Wenn Sie fertig sind, klicken Sie **[!UICONTROL Save]**.

![Erstellen Sie eine neue Wunschliste von der Warenkorbseite aus](./assets/account-dashboard-wishlist-create-from-cart.png){width="700" zoomable="yes"}

## Aktualisieren der Produktliste

1. Der Kunde verweist in der Wunschliste auf das Produkt, um die Optionen anzuzeigen.

1. Um eine **[!UICONTROL Comment]** über das Produkt hinzuzufügen, geben Sie den Text in das Feld unter dem Preis ein.

   ![Optionen bearbeiten](./assets/account-dashboard-wishlist-edit-options.png){width="700" zoomable="yes"}

1. Um die Auswahl der Produktoptionen zu ändern, klicken Sie auf **[!UICONTROL Edit]** und führen Sie folgende Schritte aus:

   - Aktualisiert die Optionen auf der Produktdetailseite.
   - Klicks **[!UICONTROL Update Wish List]**.

## Wunschzettel-Produkt zum Warenkorb hinzufügen

1. In der Wunschliste verweist der Kunde auf das Produkt, das Sie hinzufügen möchten.

1. Aktualisiert den **[!UICONTROL Qty]** und bearbeitet die anderen Optionen nach Bedarf.

1. Klicks **[!UICONTROL Add to Cart]**.

## Teilen Sie die Wunschliste

1. Der Kunde klickt auf **[!UICONTROL Share Wishlist]**.

1. Gibt die E-Mail-Adresse jeder Person ein, die die Wunschliste erhalten soll, getrennt durch ein Komma.

1. Fügt eine **[!UICONTROL Message]** hinzu, die in die E-Mail aufgenommen werden soll.

1. Klicks **[!UICONTROL Share Wish List]**.

   ![Teilen Sie Ihre Wunschliste](./assets/account-dashboard-wishlist-sharing.png){width="700" zoomable="yes"}

   Die Nachricht wird von Ihrem primären [Store-Kontakt](../getting-started/store-details.md#store-email-addresses) gesendet und enthält ein Miniaturbild jedes Produkts mit Links zu Ihrem Store.

   ![Freigegebene Wunschliste - E-Mail](./assets/account-dashboard-wishlist-sharing-email.png){width="500" zoomable="yes"}

## Wunschlisten bearbeiten

Kunden können ihre Wunschliste über ihr Konto-Dashboard auf verschiedene Arten ändern.

### Elemente in eine andere Liste verschieben

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

1. Der Kunde aktiviert das Kontrollkästchen jedes zu verschiebenden Elements.

1. Klicken Sie auf **[!UICONTROL Move Selected to Wish List]** und führen Sie einen der folgenden Schritte aus:

   - Wählt eine vorhandene Wunschliste aus.
   - Klicks **[!UICONTROL Create New Wish List]**.

### Elemente in eine andere Liste kopieren

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

1. Markiert das Kontrollkästchen jedes zu verschiebenden Elements.

1. Klicken Sie auf **[!UICONTROL Copy Selected to Wish List]** und führen Sie einen der folgenden Schritte aus:

   - Wählt eine vorhandene Wunschliste aus.
   - Klicks **[!UICONTROL Create New Wish List]**.

## Wunschliste löschen

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

1. Kunde öffnet die Wunschliste zur Löschung.

1. Klicks **[!UICONTROL Delete Wish List]**.

1. Wenn Sie zur Bestätigung aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.

>[!IMPORTANT]
>
>Diese Aktion kann nicht rückgängig gemacht werden.

## Artikel der Wunschliste in den Warenkorb legen

Um alle Artikel der Wunschliste in den Warenkorb zu legen, klickt der Kunde auf **[!UICONTROL Add All to Cart]**.

Um ein einzelnes Element hinzuzufügen, führt der Kunde Folgendes aus:

1. Bewegen Sie den Mauszeiger über den Artikel und geben Sie die **[!UICONTROL Qty]** ein, die zum Warenkorb hinzugefügt werden sollen.

1. Klicks **[!UICONTROL Add to Cart]**.

## Suchen einer Kunden-Wunschliste

Wenn das [Widget „Wunschliste - Suche](wishlist-configuration.md#add-wish-list-search) in Ihren Store-Seiten enthalten ist, können Kunden nach dem Namen oder der E-Mail-Adresse des Wunschlisteneigentümers suchen.

1. Im Suchwidget der Wunschliste wählt der Kunde eine Suchoption aus.

1. Gibt den Namen oder die E-Mail-Adresse des Besitzers der Wunschliste ein und klickt **[!UICONTROL Search]**.

   Die _Wunschlistensuche_ wird geöffnet und alle passenden Wunschlisten werden im Suchergebnisabschnitt angezeigt.

   >[!NOTE]
   >
   >In den Suchergebnissen werden nur öffentliche Wunschlisten angezeigt. Die privaten Wunschlisten von Kunden können nicht öffentlich eingesehen werden.

1. Um die Liste der Wunschlistenelemente anzuzeigen, klicken Sie auf **[!UICONTROL View]**.

   Für jede Wunschliste werden der Name des Inhabers und das Datum der letzten Aktualisierung angezeigt.

1. Um ein Produkt zu seinem Warenkorb hinzuzufügen, wählt der Kunde das Kontrollkästchen unter dem Produkt aus und klickt auf **[!UICONTROL Add to Cart]**.

   Sie können auch Artikel, die Ihnen gefallen, von der Wunschliste eines anderen Kunden zu Ihren eigenen hinzufügen.
