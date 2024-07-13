---
title: Beispiel einer Preisregel für den Warenkorb - Rabatt mit Erstkauf
description: Sehen Sie sich ein Beispiel für die Verwendung einer Preisregel für den Warenkorb an, um Erstkunden einen Rabatt anzubieten.
exl-id: 46add769-6fa9-40e0-9f4f-af2215f36283
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: dbe31fa6e7b83ac852e6e4988ac61627e30d9089
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# Beispiel einer Preisregel für den Warenkorb - Rabatt mit Erstkauf

{{ee-feature}}

Mit den Preisregeln für Warenkorb können Kunden automatisch einen Rabatt auf ihren ersten Kauf anbieten, ohne dass ein Gutschein erforderlich ist.

Um einen Rabatt für Erstkunden anzubieten, können Sie:

- Erstellen Sie ein Kundensegment, das als _Käufer ohne Bestellungen_ definiert ist, und dann
- Erstellen Sie eine Warenkorbpreisregel, die auf das neue Kundensegment ausgerichtet ist.

>[!NOTE]
>
>Stellen Sie sicher, dass die Funktion Kundensegmente aktiviert ist. Siehe [Kundensegment erstellen](../customers/customer-segment-create.md).

## Schritt 1. Kundensegment erstellen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add Segment]**.

1. Definieren Sie die **[!UICONTROL General Properties]**.

   - Geben Sie einen **[!UICONTROL Segment Name]** ein, um das Kundensegment zu identifizieren (Beispiel: _Erstmaliger Kunde_).

   - Wählen Sie für **[!UICONTROL Assigned to Website]** die Website aus, auf der das Kundensegment verwendet werden kann.

   - Wählen Sie für **[!UICONTROL Status]** `Active` aus.

   - Wählen Sie für **[!UICONTROL Apply to]** `Visitors and Registered Customers` aus.

   - Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save and Continue Edit]**.

     Im Bedienfeld auf der linken Seite stehen zusätzliche Optionen zur Verfügung.

   ![Eigenschaften des Kundensegments](./assets/customer-segment-first-time.png){width="600" zoomable="yes"}

1. Definieren Sie die **[!UICONTROL Conditions]**.

   In diesem Beispiel zielt die Bedingung auf Kunden ab, für die die Gesamtanzahl der Bestellungen kleiner als 1 _&quot;Wahr&quot;ist._

   - Wählen Sie im Bedienfeld auf der linken Seite **[!UICONTROL Conditions]** aus.

     Die Standardbedingung beginnt mit &quot;Wenn ALLE dieser Bedingungen TRUE sind:&quot;

   - Klicken Sie auf _Hinzufügen_ (![Symbol hinzufügen](../assets/icon-add-green-circle.png)) und wählen Sie `Number of Orders` aus.

   - Klicken Sie auf **[!UICONTROL is]** und wählen Sie `less than` aus.

   - Klicken Sie auf **..** und geben Sie `1` in das Feld ein.

   - Klicken Sie auf das grüne Häkchen ( ![grünes Häkchen](../assets/icon-checkmark-green-circle.png) ), um die Bedingungseinstellung zu speichern.

   ![Bedingung für Kundensegment](./assets/customer-segment-first-time-condition.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save]**.

Das Kundensegment wird im Raster _[!UICONTROL Customer Segments]_erstellt und angezeigt.

>[!TIP]
>
>Notieren Sie sich die Segment-ID. Sie verwenden diese ID-Nummer, um die Preisregel für den Warenkorb zu erstellen.

## Schritt 2. Erstellen der Preisregel für den Warenkorb

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rule]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add New Rule]**.

   Der Abschnitt **[!UICONTROL Rule Information]** wird standardmäßig mit erweiterbaren Abschnitten für **[!UICONTROL Conditions]** und **[!UICONTROL Conditions]** angezeigt.

1. Definieren Sie die **[!UICONTROL Rule Information]**.

   - Füllen Sie die Felder **[!UICONTROL Rule Name]** und **[!UICONTROL Description]** aus. Diese Felder dienen nur Ihrer internen Referenz.

   - Wählen Sie für &quot;**[!UICONTROL Websites]**&quot;die Website aus, auf der die Regel verfügbar sein soll.

   - Wählen Sie für **[!UICONTROL Customer Groups]** die Kundengruppe aus, für die diese Regel gilt.

     Um mehrere Gruppen auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

     >[!NOTE]
     >
     >Die Optionen in dieser Liste hängen von den in **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]** erstellten und verwalteten Kundengruppen ab.

   - Wählen Sie für **[!UICONTROL Coupon]** `No Coupon` aus.

   - Geben Sie für **[!UICONTROL Uses per Customer]** den Wert `1` ein.

   - Geben Sie für **[!UICONTROL Priority]** eine Zahl ein, um die Priorität dieser Regel im Vergleich zu anderen Regeln festzulegen.

     >[!NOTE]
     >
     >Die Einstellung Priorität ist wichtig, wenn dasselbe Katalogprodukt die Bedingungen für mehr als eine Preisregel erfüllt. Die Regel mit der Einstellung &quot;höchste Priorität&quot;wird für den Kunden aktiv. Die höchste Priorität ist 1. In diesem Beispiel bedeutet die Eingabe von `1`, dass diese Regel vor jeder anderen Preisregel angewendet wird. Dieser Wert wird von der Einstellung **[!UICONTROL Discard Subsequent Rules]** im Abschnitt **[!UICONTROL Action]** verwendet.

   - Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save and Continue Edit]**.

     Im Bedienfeld auf der linken Seite stehen zusätzliche Optionen zur Verfügung.

   ![Informationen zur Preisregel für Warenkorb](./assets/rule-information-first-time.png){width="600" zoomable="yes"}

1. Definieren Sie die **[!UICONTROL Conditions]**.

   - Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Conditions]** um den ![Erweiterungsselektor](../assets/icon-display-expand.png).

     Die Standardregel beginnt mit &quot;Wenn ALLE dieser Bedingungen TRUE sind:&quot;.

   - Klicken Sie auf _Hinzufügen_ (![Symbol hinzufügen](../assets/icon-add-green-circle.png)) und wählen Sie `Customer Segment` aus.

     Das Qualifikationsfeld ist standardmäßig auf `matches` eingestellt.

   - Klicken Sie auf &quot;**..**&quot;und geben Sie die Segment-ID des Kundensegments ein, das Sie als Ziel auswählen möchten.

     In diesem Beispiel lautet die Segment-ID für das neue Segment, das in Schritt 1 erstellt wurde, `2`.

     >[!NOTE]
     >
     >Wenn Sie die Segment-ID nicht kennen, klicken Sie auf das Auswahlsymbol ( ![Listensymbol](../assets/icon-list-chooser.png) ), um die Liste Kundensegment anzuzeigen. Sie können die ID manuell in das Feld eingeben oder das Kontrollkästchen für das gewünschte Segment aktivieren, um das Feld automatisch auszufüllen.

   - Klicken Sie auf das grüne Häkchen ( ![grünes Häkchen](../assets/icon-checkmark-green-circle.png) ), um die Bedingungseinstellung zu speichern.

   - Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save and Continue Edit]**.

     Diese Zeile der Regel gilt für alle Kunden, die mit der Kundensegment-ID 2 übereinstimmen.

   ![Bedingung für Kundensegment](./assets/customer-segment-matches.png){width="400"}

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png)im Abschnitt **[!UICONTROL Conditions]** und definieren Sie die Aktionen für die Regel.

   In diesem Abschnitt definieren Sie die Art des Rabatts und den Wert/Betrag des Rabatts, den Sie für Erstkunden anwenden möchten. In diesem Beispiel wird ein Rabatt von 10 % für alle Kunden definiert, die die definierte Bedingung erfüllen. Weitere Informationen zu anderen verfügbaren Optionen finden Sie unter [Erstellen einer Warenkorbpreisregel](price-rules-cart-create.md).

   - Wählen Sie für &quot;**[!UICONTROL Apply]**&quot;Prozent des Produktpreisrabatts aus.

   - Geben Sie für **[!UICONTROL Discount Amount]** den Wert `10` ein.

   - Um diese Preisregel nur auf Produktmengen anzuwenden, setzen Sie **[!UICONTROL Apply to Shipping Amount]** auf `No`.

   - Um zu verhindern, dass das System mehrere Preisregeln auf dasselbe Produkt anwendet, setzen Sie **[!UICONTROL Discard Subsequent Rules]** auf `Yes`.

   - Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

   ![Aktionen der Preisregel für Warenkorb](./assets/actions-first-time.png){width="600" zoomable="yes"}

Die neue Regel ist normalerweise innerhalb einer Stunde verfügbar. Testen Sie die Regel, um sicherzustellen, dass sie wie definiert funktioniert.

## Schritt 3: Speichern und testen Sie die Regel

{{new-price-rule}}

1. Klicken Sie nach Abschluss der Regel auf **[!UICONTROL Save Rule]**.

1. Testen Sie die Regel, um sicherzustellen, dass sie ordnungsgemäß funktioniert.
