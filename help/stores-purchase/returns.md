---
title: Rückgabe
description: Erfahren Sie mehr über den Workflow für die Rückgabe und die Ausstellung einer zurückgegebenen Merchandising-Autorisierung.
exl-id: 9dde0360-aa99-4fc4-92ff-976d9874ffec
feature: Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Rückgabe

A _Zurückgegebene Warenautorisierung_ (RMA) können Kunden gewährt werden, die eine Rücksendung für Ersatz oder Rückerstattung beantragen. In der Regel kontaktiert der Kunde den Händler, um eine Rückerstattung zu verlangen. Bei Genehmigung wird eine eindeutige RMA-Nummer zugewiesen, um das zurückgegebene Produkt zu identifizieren. In der Konfiguration können Sie entweder RMA für alle Produkte aktivieren oder RMA nur für bestimmte Produkte zulassen. Die _[!UICONTROL Returns]_grid listet die aktuellen zurückgegebenen Merchandise-Anfragen (RMAs) auf und wird zur Eingabe neuer Rückgabeanforderungen verwendet.

![Gibt Raster zurück](./assets/return.png){width="600" zoomable="yes"}

RMAs können für einfache, gruppierte, konfigurierbare und gebündelte Produktarten ausgestellt werden. RMAs sind jedoch nicht für virtuelle Produkte, herunterladbare Produkte und Geschenkkarten verfügbar.

## Spaltenbeschreibungen

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Select] | Aktivieren Sie die Kontrollkästchen für die Rückgaben, die einer Aktion unterzogen werden sollen, oder verwenden Sie das Auswahlsteuerelement in der Spaltenüberschrift. Optionen: `Select All` / `Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL RMA] | Eine eindeutige numerische Kennung, die jedem Rückgabe zugewiesen wird |
| [!UICONTROL Requested] | Datum und Uhrzeit der Platzierung der Rückgabe |
| [!UICONTROL Order] | Eine eindeutige Nummer der ursprünglichen Bestellung |
| [!UICONTROL Ordered] | Datum und Uhrzeit der Bestellung |
| [!UICONTROL Customer] | Name des Kunden oder Käufers, der die Bestellung aufgegeben hat |
| [!UICONTROL Status] | Status der Rückgabe . Optionen: `Pending` / `Authorized` / `Partially Authorized` / `Approved` / `Rejected` / `Processed and Closed` / `Closed` |
| [!UICONTROL Action] | **[!UICONTROL View]** öffnet die Rückgabe im Bearbeitungsmodus. |

{style="table-layout:auto"}

## RMA- und Rückkehr-Workflow

1. **Anfrage empfangen** - Wenn [enabled](rma-configure.md#enable-rmas-for-your-store) für die Storefront können sowohl registrierte Kunden als auch Gäste eine RMA anfordern. Sie können auch [Senden einer RMA-Anfrage in der Admin-Konsole](#create-a-return-request-in-the-admin).

2. **RMA-Ausgabe** - Nachdem Sie die Anfrage geprüft haben, können Sie sie teilweise, vollständig oder abbrechen. Wenn Sie die Rücksendung genehmigen und zustimmen, für die Rücksendung zu zahlen, können Sie einen Versandauftrag vom Administrator mit einem unterstützten Frachtführer erstellen.

3. **Empfangsbestätigungen und verarbeitete Produktempfehlungen** - Das folgende Flussdiagramm beschreibt die Betriebsreihenfolge zum Abschließen des Rückgabeverfahrens:

   ![Workflow zur Produktrückgabe](./assets/workflow-customer-returns.png){width="500"}

## RMA-Status

Während seines Lebenszyklus kann einer zurückgegebenen Warenautorisierung (RMA) viele zugewiesene Status zugewiesen sein (z. B. Ausstehend oder Autorisiert). Der RMA-Status gibt den Fortschritt einer RMA-Anfrage an, die vom Benutzer oder Händler ausgelöst wurde.

| Status | Beschreibung |
|--- |--- |
| [!UICONTROL Pending] | Der ursprüngliche Status, der einer RMA-Anfrage zugewiesen wird, wenn sie von einem Benutzer in der Storefront oder vom Händler in der Admin-Konsole ausgelöst wird. |
| [!UICONTROL Authorized] | Dieser Status wird der RMA zugewiesen, wenn alle angeforderten Elemente vom Händler im Admin für die Rückgaben autorisiert werden. |
| [!UICONTROL Partially Authorized] | Dieser Status wird der RMA zugewiesen, wenn eine der angeforderten Elemente abgelehnt und andere Produkte zugelassen wurden. |
| [!UICONTROL Denied] | Dieser Status wird der RMA zugewiesen, wenn alle angeforderten Elemente vom Händler im Admin für die Rückgaben abgelehnt werden. |
| [!UICONTROL Return Received] | Dieser Status wird dem RMA vom Händler zugewiesen, wenn die angeforderten Elemente vom Benutzer empfangen werden. |
| [!UICONTROL Return Partially Received] | Dieser Status wird dem RMA vom Händler zugewiesen, wenn die angeforderten Elemente teilweise zurückgegeben und einige der Elemente nicht verarbeitet werden. |
| [!UICONTROL Approved] | Dieser Status wird dem RMA vom Händler zugewiesen, wenn die angeforderten Elemente zur weiteren Verarbeitung genehmigt werden. |
| [!UICONTROL Rejected] | Dieser Status wird dem RMA vom Händler zugewiesen, wenn die angeforderten Elemente zur weiteren Verarbeitung abgelehnt werden. |
| [!UICONTROL Processed and Closed] | Dieser Status wird dem RMA vom Händler zugewiesen, wenn alle angeforderten Elemente zur weiteren Verarbeitung genehmigt wurden. |
| [!UICONTROL Closed] | Dieser Status wird dem RMA vom Händler zugewiesen, wenn die angeforderten Elemente nicht zur Rückgabe verarbeitet werden können. |

{style="table-layout:auto"}

## Erstellen einer Rückkehranfrage in der Admin-Konsole

Ein Händler kann vom Administrator eine Rückkehranfrage im Namen des Kunden erstellen. Kunden können [eine Rückgabeanforderung erstellen](rma-customer-experience.md) auf der Storefront für einen Adobe Commerce Store.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > **[!UICONTROL Returns]**.

1. Klicken **[!UICONTROL New Return Request]**.

1. Um eine Rückgabeanforderung zu erstellen, klicken Sie auf eine Bestellung mit einer `Complete` -Status.

1. Unter dem _[!UICONTROL Return Information]_auswählen, wählen Sie die **[!UICONTROL Return Items]**Registerkarte.

1. Um Elemente hinzuzufügen, die zurückgegeben werden sollen, klicken Sie auf **[!UICONTROL Add Items]**.

1. Aktivieren Sie das Kontrollkästchen für das gewünschte Produkt und klicken Sie auf **[!UICONTROL Add Selected Product to returns]**.

1. Für **[!UICONTROL Requested]**, geben Sie die Anzahl der zurückzugebenden Elemente an.

1. Satz **[!UICONTROL Return Reason]** auf einen der folgenden Werte zu:

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   Wenn sich der Grund für die Rückkehr von den aufgelisteten Optionen unterscheidet, können Sie Ihre eigene eingeben, wenn Sie die `Other` -Option.

1. Satz **[!UICONTROL Item Condition]** auf einen der folgenden Werte zu:

   - `Unopened`
   - `Opened`
   - `Damaged`

1. Satz **[!UICONTROL Resolution]** auf einen der folgenden Werte zu:

   - `Exchange`
   - `Refund`
   - `Store Credit`

1. Klicken Sie auf , um eine Rückgabe zu erstellen **[!UICONTROL Submit Returns]**.

   ![Beantragte RMA-Elemente](./assets/return-item-request.png){width="600" zoomable="yes"}

   Die neu gesendete RMA-Anfrage wird auf der Seite **[!UICONTROL Returns]** Seite mit einer `Pending` -Status.
