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

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Catalog]** und wählen Sie unter &quot;**[!UICONTROL Catalog]**&quot;.

1. Erweitern Sie den Abschnitt **[!UICONTROL Catalog Events]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   ![Katalogkonfiguration - Katalogereignisse](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - Setzen Sie **[!UICONTROL Enable Catalog Events Functionality]** auf `Yes`.

   - Setzen Sie **[!UICONTROL Enable Catalog Event Widget on Storefront]** auf `Yes`.

   - Geben Sie den Wert **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]** ein. Standardmäßig ist dieser Wert auf `5` gesetzt. Wenn Sie immer nur ein Ereignis im Regler anzeigen möchten, geben Sie `1` ein.

   - Geben Sie die Anzahl von **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]** ein. Standardmäßig ist dieser Wert auf `2` gesetzt. Wenn der Regler beim Klicken das nächste Ereignis in Folge anzeigen soll, geben Sie `1` ein.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Zugriffsbeschränkungen

Der Zugriff auf einen privaten Verkauf, ein privates Ereignis oder eine Site kann auf registrierte Kunden beschränkt werden, die sich anmelden oder auf nicht registrierte Kunden erweitert werden, die sich vor dem Zugriff registrieren müssen.

![Allgemeine Konfiguration - Website-Beschränkungen](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### Zugriff beschränken

Der Zugriff auf einen privaten Verkauf, ein privates Ereignis oder eine Site kann auf registrierte Kunden beschränkt werden, die sich anmelden oder auf nicht registrierte Kunden erweitert werden, die sich vor dem Zugriff registrieren müssen.

![Allgemeine Konfiguration - Website-Beschränkungen](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL General]** und wählen Sie unter &quot;**[!UICONTROL General]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Website Restrictions]** .

1. Setzen Sie **[!UICONTROL Access Restriction]** auf `Yes`.

1. Setzen Sie **[!UICONTROL Restriction Mode]** auf einen der folgenden Werte:

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. Setzen Sie **[!UICONTROL Startup Page]** auf einen der folgenden Werte:

   - `To login form (302 Found)` - Benutzer werden zum Anmeldeformular weitergeleitet, bevor sie Zugriff auf die Site erhalten.

   - `To landing page (302 Found)` - Benutzer werden bis zur Anmeldung zur angegebenen Landingpage weitergeleitet.

     >[!IMPORTANT]
     >
     >Stellen Sie sicher, dass Sie von der Landingpage aus einen Link zur Anmeldeseite einfügen, damit sich Kunden anmelden und auf die Site zugreifen können.

1. Wählen Sie die **[!UICONTROL Landing Page]** aus, die angezeigt wird, bevor sich Kunden bei der privaten Verkaufs-Site anmelden.

1. Damit Bots und Spider von Suchmaschinen wissen, dass die Landingpage korrekt ist und keine anderen Seiten auf der Site indiziert werden können, setzen Sie **[!UICONTROL HTTP Response]** auf `200 OK`.

   In allen anderen Fällen auf `503 Service Unavailable` gesetzt.

   >[!NOTE]
   >
   >Gilt nur, wenn der Beschränkungsmodus auf _Website geschlossen_ gesetzt ist. Die Landingpage wird als rohe HTML gerendert.

1. Wenn Sie möchten, dass die Felder in der Kundenanmeldung automatisch ausgefüllt werden und die Kennwortformulare aus früheren Einträgen nicht ausgefüllt werden, setzen Sie **[!UICONTROL Enable Autocomplete on login/forgot password forms]** auf `Yes`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

### Verkäufe beschränken

Standardmäßig sind Produkte, die in bevorstehenden oder geschlossenen Ereignissen angezeigt werden, nicht für den allgemeinen Verkauf verfügbar und die Schaltfläche &quot;_[!UICONTROL Add to Cart]_&quot; wird nicht auf der Produktliste oder Produktseite angezeigt.

Um die Schaltfläche _[!UICONTROL Add to Cart]_für ein geschlossenes Ereignis wiederherzustellen, muss das Ereignis gelöscht werden (siehe [Ereignisse aktualisieren](event-create.md#update-events)). Wenn ein Produkt jedoch einer anderen Kategorie zugeordnet ist, die keine Verkaufsbeschränkungen aufweist, ist die Schaltfläche auf der Produktseite verfügbar. Auf ähnliche Weise wird der Ticker-Block nicht auf der Produktseite angezeigt, wenn das Produkt einer anderen Kategorie zugeordnet ist, die keine Verkaufsbeschränkungen aufweist.
