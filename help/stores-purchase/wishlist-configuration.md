---
title: Wunschlisten konfigurieren
description: Erfahren Sie, wie Sie die Funktion für Wunschlisten für Ihre Store-Kunden konfigurieren.
exl-id: 479455f1-282f-4277-b132-45c5867fb21c
feature: Customers, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# Wunschlisten konfigurieren

Die Konfiguration der Wunschliste ermöglicht Wunschlisten und bestimmt die E-Mail-Vorlage sowie den Absender von E-Mail-Nachrichten, die bei der Freigabe einer Wunschliste verwendet werden.

## Funktion &quot;Wunschliste aktivieren&quot;

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen **[!UICONTROL Wish List]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL General Options]** und führen Sie folgende Schritte aus:

   ![Kundenkonfiguration - Allgemeine Einstellungen der Wunschliste](../configuration-reference/customers/assets/wishlist-general-options.png){width="600" zoomable="yes"}

   - Umschalten **[!UICONTROL Enabled]** nach `Yes`, wodurch das Wunschlisten-Modul für den Store aktiviert wird.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Umschalten **[!UICONTROL Enable Multiple Wish Lists]** nach `Yes`, wodurch Kunden mehrere Wunschlisten erstellen und verwalten können.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Um die Anzahl der Wunschlisten zu begrenzen, die Kunden ihrem Konto zugeordnet haben können, geben Sie einen Wert für **[!UICONTROL Number of Multiple Wish Lists]**.

   - Umschalten **[!UICONTROL Show in Sidebar]** nach `Yes`, wodurch die Wunschlisten in der Seitenleiste angezeigt werden.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Share Options]** und führen Sie folgende Schritte aus:

   ![Kundenkonfiguration - Optionen zum Freigeben von Wunschlisten](../configuration-reference/customers/assets/wishlist-share-options.png){width="600" zoomable="yes"}

   - Legen Sie die **[!UICONTROL Email Sender]** an den Store-Kontakt, der als Absender der Nachricht angezeigt werden soll. Optionen: Allgemeiner Kontakt, Vertriebsmitarbeiter, Kundensupport, benutzerdefinierte E-Mail.

   - Legen Sie die **[!UICONTROL Email Template]** verwendet werden, wenn ein Kunde eine Wunschliste teilt.

   - Um die Gesamtzahl der E-Mails zu begrenzen, die ein Kunde senden kann, geben Sie einen **[!UICONTROL Max Emails Allowed to be Sent]** -Wert. Der Standardwert ist 10 und der maximal zulässige Wert ist 10.000.

   - Geben Sie einen Wert für **[!UICONTROL Email Text Length Limit]**. Der Standardwert ist 255.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL My Wish List Link]** Abschnitt und Satz **[!UICONTROL Display Wish List Summary]** auf einen der folgenden Werte zu:

   - `Display number of items in wish list`
   - `Display item quantities`

   ![Kundenkonfiguration - Anzeige der Wunschliste](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Suche nach Wunschlisten hinzufügen

![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce)

Jede öffentliche Wunschliste kann mithilfe der Wunschlisten-Suche gefunden werden. [Widget](../content-design/widgets.md). Das Widget ermöglicht es einem Kunden, nach dem Namen oder der E-Mail-Adresse des Eigentümers der Wunschliste zu suchen. Store-Kunden können Wunschlisten anderer Kunden finden, diese anzeigen und Produkte von ihnen bestellen oder die Produkte zu ihren eigenen Wunschlisten hinzufügen. Wenn ein Artikel von einem anderen Kunden aus einer öffentlichen Wunschliste gekauft wird, wird er nicht aus der ursprünglichen Wunschliste entfernt. Die _Suche nach Listen_ -Widget kann auf jeder Seite Ihres Stores hinzugefügt werden, um es den Kunden zu erleichtern, die Wunschlisten von Freunden und Familienmitgliedern zu finden.

![Beispiel-Storefront - Suche nach Wunschlisten](./assets/storefront-wishlist-search.png){width="700" zoomable="yes"}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Widget]**.

1. Im _[!UICONTROL Settings]_Gehen Sie wie folgt vor:

   - Satz **[!UICONTROL Type]** nach `Wish List Search`.

   - Satz **[!UICONTROL Design Theme]** zum Design des Stores, in dem die Wunschliste hinzugefügt wird.

   - Klicken **[!UICONTROL Continue]**.

1. Führen Sie die _[!UICONTROL Storefront Properties]_:

   - Geben Sie die **[!UICONTROL Widget Title]**.

   - Satz **[!UICONTROL Assign to Store Views]** in die Ansicht oder Website, auf der das Widget verwendet werden soll.

   - Für **[!UICONTROL Sort Order]** eingeben, geben Sie eine Zahl ein, um die Platzierung des Widgets in seinem Container zu bestimmen.

     `0` = first (Standard), `1` = Sekunde, `2` = drittes Element usw.

1. Im _[!UICONTROL Layout Updates]_Abschnitt, klicken Sie auf **[!UICONTROL Add Layout Update]**und **[!UICONTROL Display on]**auf einen der folgenden Werte zu:

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

1. Im **[!UICONTROL Container]** wählen Sie den Bereich des Seitenlayouts aus, in dem er platziert werden soll.

   ![Widget zur Listensuche - Layout](./assets/widget-wishlist-search-storefront.png){width="700" zoomable="yes"}

1. Wählen Sie im linken Bereich die Option **[!UICONTROL Widget Options]**.

1. Satz **[!UICONTROL Quick Search Form Types]** auf einen der folgenden Werte zu:

   - `All Forms` - Kunden können nach allen verfügbaren Parametern suchen.
   - `Owner Name` - Kunden können nach Wunschlisten anhand des Namens des Eigentümers suchen.
   - `Owner Email` - Kunden können nach Wunschlisten nach der E-Mail-Adresse des Eigentümers suchen.

   >[!NOTE]
   >
   >Versandadressen sind nicht in Wunschlisten enthalten.

1. Konfigurieren Sie die restlichen Widget-Eigenschaften nach Bedarf entsprechend dem Standard [instructions](../content-design/widget-create.md).

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

1. Wenn Sie dazu aufgefordert werden, aktualisieren Sie alle ungültigen Caches.
