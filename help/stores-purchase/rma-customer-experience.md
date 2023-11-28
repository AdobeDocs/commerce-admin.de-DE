---
title: Gibt storefront-Erlebnis zurück
description: Erfahren Sie, wie Ihre Kunden ihre Produktrenditen aus ihrem -Konto auf der Storefront verwalten können.
exl-id: c276ca2c-3d8b-4019-a9aa-e7631080f331
feature: Returns, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# Gibt storefront-Erlebnis zurück

{{ee-feature}}

Kunden können eine der folgenden Funktionen verwenden, um eine RMA von der Storefront anzufordern:

- [Widget &quot;Bestellungen&quot;und &quot;Rückgaben&quot;](../content-design/widget-orders-returns.md) in der Seitenleiste
- _Bestellungen und Rückgaben_ Link in der Fußzeile

Als Best Practice sollten Sie eine Beschreibung Ihrer RMA-Anforderungen und -Prozesse in die Richtlinie für den Kundendienst aufnehmen.

>[!NOTE]
>
>Wenn Sie zusätzliche Informationen zu Rückgaben erfassen möchten, können Sie Ihre eigenen benutzerdefinierten [gibt Attribute zurück](attributes-returns.md).

Alle Kunden-RMA-Informationen werden auf der Seite **[!UICONTROL My Returns]** im Dashboard des Kundenkontos angezeigt.

![Meine Rückgabe](./assets/my-returns-page.png){width="700" zoomable="yes"}

## Anfordern einer RMA

Der Kunde führt die folgenden Schritte in der Storefront aus, um eine RMA zu senden:

1. Klicken Sie in der Fußzeile auf **[!UICONTROL Orders and Returns]**.

1. Fügt die Bestellinformationen ein:

   - Auftrags-ID
   - Nachname der Abrechnung
   - E-Mail

1. Klicks **[!UICONTROL Continue]**.

   ![Bestellungen und Rückgaben](./assets/storefront-orders-and-returns.png){width="700" zoomable="yes"}

1. Klicks unterhalb des Bestelldatums **[!UICONTROL Return]**.

   ![Bestelldetails](./assets/storefront-orders-and-returns-order-information.png){width="700" zoomable="yes"}

1. Wählen Sie das zurückzugebende Element aus und geben Sie die **[!UICONTROL Quantity to Return]**.

1. Sets **[!UICONTROL Resolution]** auf einen der folgenden Werte zu:

   - Exchange
   - [Erstattung](../customers/refunds-customer-account.md)
   - [Store-Guthaben](../customers/store-credit-using.md)

1. Sets **[!UICONTROL Item Condition]** auf einen der folgenden Werte zu:

   - `Unopened`
   - `Opened`
   - `Damaged`

1. Sets **[!UICONTROL Reason to Return]** auf einen der folgenden Werte zu:

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   ![Neue Rückgabe erstellen](./assets/storefront-orders-and-returns-create-new-return.png){width="700" zoomable="yes"}

1. Bei Bedarf Sets **[!UICONTROL Contact Email Address]** und **[!UICONTROL Comments]**.

   >[!NOTE]
   >
   >Wenn die Bestellung mehrere Artikel enthält und der Kunde ein anderes Element zurückgeben möchte, kann er auf **[!UICONTROL Add Item To Return]**, wählen Sie das Element aus und legen Sie dann alle erwähnten Optionen fest.

1. Klicks **[!UICONTROL Submit]**.
