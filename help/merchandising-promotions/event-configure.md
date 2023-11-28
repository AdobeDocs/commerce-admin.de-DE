---
title: Ereignisse konfigurieren
description: Erfahren Sie, wie Sie die grundlegende Konfiguration abschließen, um Ereignisse zu aktivieren und den Ereignisblock in der Storefront-Seitenleiste einzurichten.
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
source-git-commit: 084d2c3381f57a8a4c7e8ffde9da1abd4d8af670
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Ereignisse konfigurieren

{{ee-feature}}

Bevor Sie ein Ereignis erstellen können, müssen Sie die grundlegende Konfiguration abschließen, um Ereignisse zu aktivieren und den Ereignisblock in der Seitenleiste einzurichten.

## Ereignisse aktivieren und konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Catalog Events]** und führen Sie folgende Schritte aus:

   ![Katalogkonfiguration - Katalogereignisse](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - Satz **[!UICONTROL Enable Catalog Events Functionality]** nach `Yes`.

   - Satz **[!UICONTROL Enable Catalog Event Widget on Storefront]** nach `Yes`.

   - Geben Sie die **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**. Standardmäßig ist dieser Wert auf `5`. Wenn Sie immer nur ein Ereignis im Regler anzeigen möchten, geben Sie `1`.

   - Geben Sie die Anzahl der **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**. Standardmäßig ist dieser Wert auf `2`. Wenn der Regler das nächste Ereignis nach Klicken anzeigen soll, geben Sie `1`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Zugriffsbeschränkungen

Der Zugriff auf einen privaten Verkauf, ein privates Ereignis oder eine Site kann auf registrierte Kunden beschränkt werden, die sich anmelden oder auf nicht registrierte Kunden erweitert werden, die sich vor dem Zugriff registrieren müssen.

![Allgemeine Konfiguration - Website-Beschränkungen](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### Zugriff beschränken

Der Zugriff auf einen privaten Verkauf, ein privates Ereignis oder eine Site kann auf registrierte Kunden beschränkt werden, die sich anmelden oder auf nicht registrierte Kunden erweitert werden, die sich vor dem Zugriff registrieren müssen.

![Allgemeine Konfiguration - Website-Beschränkungen](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL General]** und wählen **[!UICONTROL General]** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Website Restrictions]** Abschnitt.

1. Satz **[!UICONTROL Access Restriction]** nach `Yes`.

1. Satz **[!UICONTROL Restriction Mode]** auf einen der folgenden Werte zu:

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. Satz **[!UICONTROL Startup Page]** auf einen der folgenden Werte zu:

   - `To login form (302 Found)` - Benutzer werden zum Anmeldeformular weitergeleitet, bevor sie Zugriff auf die Site erhalten.

   - `To landing page (302 Found)` - Benutzer werden bis zur Anmeldung zur angegebenen Landingpage weitergeleitet.

     >[!IMPORTANT]
     >
     >Stellen Sie sicher, dass Sie von der Landingpage aus einen Link zur Anmeldeseite einfügen, damit sich Kunden anmelden und auf die Site zugreifen können.

1. Wählen Sie die **[!UICONTROL Landing Page]** wird angezeigt, bevor sich Kunden bei der privaten Verkaufs-Site anmelden.

1. Damit Bots und Spider von Suchmaschinen wissen, dass die Landingpage korrekt ist und keine anderen Seiten auf der Site indiziert werden können, legen Sie **[!UICONTROL HTTP Response]** nach `200 OK`.

   In allen anderen Fällen auf `503 Service Unavailable`.

   >[!NOTE]
   >
   >Gilt nur, wenn der Beschränkungsmodus auf _Website geschlossen_. Die Landingpage wird als rohe HTML gerendert.

1. Wenn Sie möchten, dass die Felder in der Kundenanmeldung automatisch ausgefüllt werden und die Passwortformulare von früheren Einträgen vergessen werden, legen Sie **[!UICONTROL Enable Autocomplete on login/forgot password forms]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### Verkäufe beschränken

Standardmäßig sind Produkte, die in anstehenden oder geschlossenen Ereignissen angezeigt werden, nicht für den allgemeinen Verkauf verfügbar und die _[!UICONTROL Add to Cart]_-Schaltfläche nicht in der Produktliste oder Produktseite angezeigt.

So stellen Sie die _[!UICONTROL Add to Cart]_-Schaltfläche für ein geschlossenes Ereignis verwenden, muss das Ereignis gelöscht werden (siehe [Ereignisse aktualisieren](event-create.md#update-events)). Wenn ein Produkt jedoch einer anderen Kategorie zugeordnet ist, die keine Verkaufsbeschränkungen aufweist, ist die Schaltfläche auf der Produktseite verfügbar. Auf ähnliche Weise wird der Ticker-Block nicht auf der Produktseite angezeigt, wenn das Produkt einer anderen Kategorie zugeordnet ist, die keine Verkaufsbeschränkungen aufweist.
