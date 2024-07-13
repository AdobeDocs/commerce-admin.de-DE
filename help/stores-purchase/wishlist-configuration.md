---
title: Wunschlisten konfigurieren
description: Erfahren Sie, wie Sie die Funktion für Wunschlisten für Ihre Store-Kunden konfigurieren.
exl-id: 479455f1-282f-4277-b132-45c5867fb21c
feature: Customers, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Wunschlisten konfigurieren

Die Konfiguration der Wunschliste ermöglicht Wunschlisten und bestimmt die E-Mail-Vorlage sowie den Absender von E-Mail-Nachrichten, die bei der Freigabe einer Wunschliste verwendet werden.

## Funktion &quot;Wunschliste aktivieren&quot;

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Wish List]** aus.

1. Erweitern Sie den Abschnitt **[!UICONTROL General Options]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   ![Kundenkonfiguration - Allgemeine Einstellungen der Wunschliste](../configuration-reference/customers/assets/wishlist-general-options.png){width="600" zoomable="yes"}

   - Schalten Sie **[!UICONTROL Enabled]** auf `Yes` um, wodurch das Wunschlisten-Modul für den Store aktiviert wird.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Schalten Sie **[!UICONTROL Enable Multiple Wish Lists]** in `Yes` um, wodurch Kunden mehrere Wunschlisten erstellen und verwalten können.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Geben Sie den Wert für **[!UICONTROL Number of Multiple Wish Lists]** ein, um die Anzahl der Wunschlisten zu begrenzen, die Kunden mit ihrem Konto verknüpft haben können.

   - Umschalten von **[!UICONTROL Show in Sidebar]** auf `Yes`, wodurch die Wunschlisten in der Seitenleiste angezeigt werden.

1. Erweitern Sie den Abschnitt **[!UICONTROL Share Options]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   ![Kundenkonfiguration - Optionen zum Freigeben der Wunschliste](../configuration-reference/customers/assets/wishlist-share-options.png){width="600" zoomable="yes"}

   - Setzen Sie &quot;**[!UICONTROL Email Sender]**&quot;auf den Store-Kontakt, der als Absender der Nachricht angezeigt werden soll. Optionen: Allgemeiner Kontakt, Vertriebsmitarbeiter, Kundensupport, benutzerdefinierte E-Mail.

   - Legen Sie den **[!UICONTROL Email Template]** fest, der verwendet werden soll, wenn ein Kunde eine Wunschliste teilt.

   - Geben Sie einen **[!UICONTROL Max Emails Allowed to be Sent]** -Wert ein, um die Gesamtzahl der E-Mails zu begrenzen, die ein Kunde senden kann. Der Standardwert ist 10 und der maximal zulässige Wert ist 10.000.

   - Geben Sie den Wert für **[!UICONTROL Email Text Length Limit]** ein, um die Nachrichtengröße zu begrenzen. Der Standardwert ist 255.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL My Wish List Link]** und legen Sie **[!UICONTROL Display Wish List Summary]** auf einen der folgenden Werte fest:

   - `Display number of items in wish list`
   - `Display item quantities`

   ![Kundenkonfiguration - Anzeige der Wunschliste](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Suche nach Wunschlisten hinzufügen

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

Jede öffentliche Wunschliste kann mit dem Widget [widget](../content-design/widgets.md) gefunden werden. Das Widget ermöglicht es einem Kunden, nach dem Namen oder der E-Mail-Adresse des Eigentümers der Wunschliste zu suchen. Store-Kunden können Wunschlisten anderer Kunden finden, diese anzeigen und Produkte von ihnen bestellen oder die Produkte zu ihren eigenen Wunschlisten hinzufügen. Wenn ein Artikel von einem anderen Kunden aus einer öffentlichen Wunschliste gekauft wird, wird er nicht aus der ursprünglichen Wunschliste entfernt. Das Widget _Wunschlisten-Suche_ kann zu jeder Seite Ihres Stores hinzugefügt werden, um es Kunden zu erleichtern, die Wunschlisten von Freunden und Familienmitgliedern zu finden.

![Beispiel-Storefront - Wunschlisten-Suche](./assets/storefront-wishlist-search.png){width="700" zoomable="yes"}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add Widget]**.

1. Gehen Sie auf der Registerkarte _[!UICONTROL Settings]_wie folgt vor:

   - Setzen Sie **[!UICONTROL Type]** auf `Wish List Search`.

   - Setzen Sie **[!UICONTROL Design Theme]** auf das Design des Stores, in dem die Wunschliste hinzugefügt wird.

   - Klicken Sie auf **[!UICONTROL Continue]**.

1. Vervollständigen Sie die _[!UICONTROL Storefront Properties]_:

   - Geben Sie den Wert **[!UICONTROL Widget Title]** ein.

   - Setzen Sie **[!UICONTROL Assign to Store Views]** auf die Ansicht oder Website, auf der das Widget verwendet werden soll.

   - Geben Sie für **[!UICONTROL Sort Order]** eine Zahl ein, um die Platzierung des Widgets in seinem Container zu bestimmen.

     `0` = first (Standard), `1` = second, `2` = third usw.

1. Klicken Sie im Abschnitt _[!UICONTROL Layout Updates]_auf **[!UICONTROL Add Layout Update]**und legen Sie **[!UICONTROL Display on]**auf einen der folgenden Werte fest:

   - _[!UICONTROL Categories]_

      - `Anchor Categories`
      - `Non-Anchor Categories`

   - _[!UICONTROL Products]_

      - `All Product Type`
      - `Simple Product`
      - `Virtual Product`
      - `Bundle Product`
      - `Configurable Product`
      - `Downloadable Product`
      - `Gift Card`
      - `Grouped Product`

   - _[!UICONTROL Generic Page]_

      - `All Pages`
      - `Specified Page`
      - `Page Layouts`

1. Wählen Sie in der Liste **[!UICONTROL Container]** den Bereich des Seitenlayouts aus, in dem er platziert werden soll.

   ![Listen-Suchwidget wünschen - layout](./assets/widget-wishlist-search-storefront.png){width="700" zoomable="yes"}

1. Wählen Sie im linken Bereich **[!UICONTROL Widget Options]** aus.

1. Setzen Sie **[!UICONTROL Quick Search Form Types]** auf einen der folgenden Werte:

   - `All Forms` - Kunden können nach allen verfügbaren Parametern suchen.
   - `Owner Name` - Kunden können nach Wunschlisten anhand des Namens des Eigentümers suchen.
   - `Owner Email` - Kunden können nach Wunschlisten anhand der E-Mail-Adresse des Eigentümers suchen.

   >[!NOTE]
   >
   >Versandadressen sind nicht in Wunschlisten enthalten.

1. Konfigurieren Sie alle verbleibenden Widget-Eigenschaften nach Bedarf entsprechend den standardmäßigen [Anweisungen](../content-design/widget-create.md).

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

1. Wenn Sie dazu aufgefordert werden, aktualisieren Sie alle ungültigen Caches.
