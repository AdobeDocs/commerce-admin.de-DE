---
title: Couponcodes
description: Erfahren Sie, wie Sie Coupons-Codes mit Warenkorbpreisregeln verwenden können, um einen Rabatt anzuwenden, wenn eine Reihe von Bedingungen erfüllt ist.
exl-id: 4f2e6203-0de2-44eb-a5f7-edd7b5f714d1
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1816'
ht-degree: 0%

---

# Couponcodes

Coupons-Codes werden mit [Warenkorbpreisregeln](price-rules-cart.md) , um einen Rabatt anzuwenden, wenn eine Reihe von Bedingungen erfüllt ist. So kann beispielsweise ein Gutscheincode für eine bestimmte Kundengruppe oder für jeden Benutzer erstellt werden, der einen Kauf über einen bestimmten Betrag tätigt. Um den Gutschein auf einen Kauf anzuwenden, kann der Kunde den Gutscheincode im Warenkorb oder möglicherweise in der Kasse Ihres Kontos eingeben _Backstein und Mörtel_ speichern. Im Folgenden finden Sie einige Möglichkeiten, Gutscheine in Ihrem Geschäft zu verwenden:

- E-Mail-Gutscheine an Kunden
- Generieren gedruckter Gutscheine
- Erstellen von In-Store-Gutscheinen für Mobilbenutzer

Couponcodes können per E-Mail oder in Newslettern, Katalogen und Anzeigen versendet werden. Die Liste der Gutscheincodes kann exportiert und an einen kommerziellen Drucker gesendet werden. Sie können auch In-Store-Gutscheine mit einem Schnellantwort-Code erstellen, den Kunden mit ihren Smartphones scannen können. Der QR-Code kann mit einer Seite auf Ihrer Site verlinken, die weitere Informationen zur Promotion enthält.

## Gutscheincodes konfigurieren

Die Länge und das Format der automatisch generierten Couponcodes werden durch die Konfiguration gesteuert. Die Zeichen können auf alle Zahlen, alle Buchstaben oder eine Kombination gesetzt werden. Sie können einen Bindestrich in festgelegten Intervallen einfügen, um das Lesen zu vereinfachen, und ein Präfix und Suffix hinzufügen, um den Code mit einer bestimmten Kampagne oder Initiative zu verknüpfen.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen **[!UICONTROL Promotions]**.

   ![Kundenkonfiguration - automatisch generierte spezifische Gutscheincodes](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Erweitern Sie die **[!UICONTROL Auto Generated Specific Coupon Codes]** Abschnitt.

   ![Kundenkonfiguration - automatisch generierte spezifische Gutscheincodes](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Geben Sie die **[!UICONTROL Code Length]**, einschließlich Präfix, Suffix und Trennzeichen.

1. Legen Sie die **[!UICONTROL Code Format]** auf einen der folgenden Werte zu:

   - `Alphanumeric`
   - `Alphabetical`
   - `Numeric`

1. Für **[!UICONTROL Code Prefix]** eingeben, geben Sie den Wert ein, der am Anfang aller Couponcodes angezeigt werden soll.

1. Für **[!UICONTROL Code Suffix]** eingeben, geben Sie den Wert ein, der am Ende aller Gutscheincodes angezeigt werden soll.

1. Für **[!UICONTROL Dash Every X Characters]**, geben Sie die Anzahl der Zeichen zwischen den einzelnen Bindestrichen an.

   Couponcodes mit unterschiedlichen Bindestrichmustern werden als unterschiedliche Codes betrachtet, auch wenn die Zahlen identisch sind.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Gutscheine erstellen

>[!NOTE]
>
>Bevor Sie Gutscheine erstellen, verwenden Sie die `bin/magento cron:run` -Befehl, um zu überprüfen, ob Cron ausgeführt wird. Siehe [Ausführen von cron über die Befehlszeile](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html#run-cron-from-the-command-line) im _Konfigurationshandbuch_ für weitere Informationen.

### Methode 1: Erstellen eines bestimmten Gutscheins

1. Befolgen Sie die Anweisungen zum Erstellen einer [Warenkorbpreisregel](price-rules-cart.md).

1. Im **[!UICONTROL Rule Information]** Abschnitt, festlegen **[!UICONTROL Coupon]** nach `Specific Coupon`.

1. Geben Sie einen **[!UICONTROL Coupon Code]** zur Verwendung mit der Promotion.

   Das Format des Codes (numerisch, alphanumerisch oder alphabetisch) wird durch die Variable [Konfiguration](#configure-coupon-codes).

1. Gehen Sie wie folgt vor, um die Anzahl der Verwendungsmöglichkeiten des Gutscheins zu begrenzen:

   - Geben Sie die Anzahl der **[!UICONTROL Uses per Coupon]**.
   - Geben Sie die Anzahl der **[!UICONTROL Uses per Customer]**.

   Lassen Sie diese Felder für eine unbegrenzte Verwendung leer.

   ![Warenkorbpreisregel - Couponinformationen](./assets/coupon-info.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Wenn derselbe Gutschein gleichzeitig von mehreren Kunden verwendet wird, kann es sein, dass die festgelegte Nutzungsbeschränkung aufgrund einer verzögerten Couponverarbeitung überschritten werden kann.

1. Gehen Sie wie folgt vor, um den Gutschein für einen Zeitraum gültig zu machen:

   - ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Führen Sie die **Von** und **nach** Daten. Klicken Sie auf das **Kalender** (![Kalendersymbol](../assets/icon-calendar.png)) neben jedem Feld. Wenn Sie den Datumsbereich leer lassen, läuft die Regel nicht ab.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Führen Sie einen der folgenden Schritte aus:

     **Option 1:** Eine neue Aktualisierung planen

      - Klicks **[!UICONTROL Schedule New Update]** in der oberen rechten Ecke der Seite.

        ![Planung aktualisieren](./assets/coupon-schedule-new-update.png){width="600" zoomable="yes"}

      - Geben Sie die **[!UICONTROL Update Name]** und **[!UICONTROL Description]**.

      - Wählen Sie die **Startdatum** und **[!UICONTROL End Date]** aus dem Kalender ( ![Kalendersymbol](../assets/icon-calendar.png) ). Wenn Sie den Datumsbereich leer lassen, läuft die Regel nicht ab.

      - Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

        ![Preisregel für Warenkorb - Geplante Änderung](./assets/coupon-scheduled-change.png){width="600" zoomable="yes"}

     **Option 2:** Einer vorhandenen Aktualisierung zuweisen:

      - Auswählen **[!UICONTROL Assign to Another Update]**.

      - Suchen Sie die Aktualisierung in der Liste und klicken Sie auf **[!UICONTROL Select]**.

1. Führen Sie die [Warenkorbpreisregel](price-rules-cart.md) nach Bedarf.

### Methode 2: Generieren eines Gutscheinstapels

Die Generierung von Discount-Gutscheinen ist ein asynchroner Vorgang, der im Hintergrund ausgeführt wird, sodass Sie die Arbeit im Admin fortsetzen können, ohne auf den Abschluss des Vorgangs warten zu müssen. Das System zeigt eine Meldung an, wenn die Aufgabe abgeschlossen ist.

1. Befolgen Sie die Anweisungen zum Erstellen einer [Warenkorbpreisregel](price-rules-cart.md).

1. under **[!UICONTROL Coupon Code]**, wählen Sie die **[!UICONTROL Use Auto Generation]** aktivieren.

1. Geben Sie die Anzahl der **[!UICONTROL Uses per Customer]**.

   ![Preisregel für Warenkorb - Erstellen von automatisch nummerierten Gutscheinen](./assets/coupon-auto.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Wenn derselbe Gutschein gleichzeitig von mehreren Kunden verwendet wird, kann es sein, dass die festgelegte Nutzungsbeschränkung aufgrund einer verzögerten Couponverarbeitung überschritten werden kann.

1. Hinunter scrollen und erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Manage Coupon Codes]** und führen Sie folgende Schritte aus:

   ![Preisregel für Warenkorb - Verwaltung von Coupon-Codes](./assets/manage-coupon-codes.png){width="600" zoomable="yes"}

   - Für **[!UICONTROL Coupons Qty]** Geben Sie die Anzahl der Gutscheine ein, die Sie generieren möchten.

   - Geben Sie die **[!UICONTROL Code Length]**, ohne Präfix, Suffix oder Trennzeichen.

   - Legen Sie die **[!UICONTROL Code Format]** auf einen der folgenden Werte zu:

      - `Alphanumeric`
      - `Alphabetical`
      - `Numeric`

   - (Optional) Geben Sie einen **[!UICONTROL Code Prefix]** am Anfang des Codes hinzugefügt.

   - (Optional) Geben Sie einen **[!UICONTROL Code Suffix]** am Ende des Codes hinzugefügt.

   - (Optional) Für **[!UICONTROL Dash Every X Characters]**, geben Sie die Anzahl der Zeichen zwischen den einzelnen Bindestrichen an. Wenn der Code beispielsweise 12 Zeichen lang ist und alle vier Zeichen einen Bindestrich enthält, sieht er wie `xxxx-xxxx-xxxx`. Gedankenstriche erleichtern das Lesen und Eingeben von Codes.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Generate]**.

   Das System wird angezeigt `Message is added to queue, wait to get your coupons soon`.

   Nach Abschluss des Cron-Auftrags wird die Liste der generierten Codes angezeigt.

   | Feld | Beschreibung |
   |-------------|-------------|
   | [!UICONTROL Coupon Code] | Ein eindeutiger Couponcode, der erstellt wurde und für den Empfang von Sonderbedingungen verwendet werden kann. |
   | [!UICONTROL Created] | Das Datum der Erstellung des Gutscheincodes. |
   | [!UICONTROL Used] | Gibt an, ob der Coupon verwendet wurde. |
   | [!UICONTROL Times Used] | Gibt an, wie oft der Couponcode verwendet wurde. |

   {style="table-layout:auto"}

Sie können Gutscheincodes in eine CSV- oder Excel-XML-Datei exportieren, indem Sie das Dateiformat auswählen und auf **[!UICONTROL Export]**.

Um Couponcodes zu löschen, wählen Sie einen oder mehrere Codes aus der Liste aus. Auswählen `Delete` aus dem **[!UICONTROL Actions]**  und klicken Sie dann auf **[!UICONTROL Submit]**.

>[!NOTE]
>
>Obwohl Commerce die Konfiguration mehrerer Couponcodes ermöglicht, kann ein Kunde nur einen Couponcode im Warenkorb verwenden. Um die gleichzeitige Verwendung von mehr als einem Couponcode im Warenkorb zu ermöglichen, können Sie eine entsprechende Erweiterung von [Commerce Marketplace](https://marketplace.magento.com/).

## Couponbericht

Die _Coupons_ aggregiert Daten aus jedem Gutschein, der in einem bestimmten Datumsbereich verwendet wird. Da Gutscheine aus dem Warenkorb angewendet werden, enthält der Bericht Daten aus allen eingelösten Gutscheinen, unabhängig von [Bestellstatus](../stores-purchase/order-status.md). Daher kann der Bericht sowohl projizierte als auch tatsächliche Summen enthalten. Der Bericht kann nach einer bestimmten Store-Ansicht, einem bestimmten Zeitraum, einem bestimmten Bestellstatus und einer bestimmten Preisregel für den Warenkorb gefiltert werden.

Im folgenden Beispiel wurde der Gutscheincode &quot;H20&quot;von zwei Kunden verwendet. Eine der Bestellungen wird in Rechnung gestellt, die andere jedoch noch _pending_. In den Spalten &quot;Zwischensumme der Verkäufe&quot;, &quot;Rabatt&quot;und &quot;Gesamtverkäufe&quot;werden die aggregierten Beträge aus beiden Bestellungen angezeigt, aber in den Spalten &quot;Zwischensumme&quot;, &quot;Rabatt&quot;und &quot;Gesamtsumme&quot;wird nur die tatsächlich in Rechnung gestellte Bestellung angezeigt. Jede Zeile im Bericht stellt eine einzelne Coupon-Promotion dar.

![Couponbericht](./assets/reports-coupons.png){width="600" zoomable="yes"}

### Bericht ausführen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**.

1. Wenn Sie mehrere Store-Ansichten haben, legen Sie **[!DNL Store View]** oben links, um den Umfang des Berichts festzulegen.

1. So aktualisieren Sie den Umsatz [statistics](../getting-started/sales-reports.md#refresh-statistics) Klicken Sie für den Tag auf die _Zuletzt aktualisiert_ -Meldung am oberen Rand des Arbeitsbereichs.

   Klicken Sie anschließend auf , um die **[!UICONTROL Coupons]** aktivieren und auf **[!UICONTROL Refresh]**.

   ![Couponbericht - Aktualisierungsstatistiken](./assets/reports-coupons-refresh-statistics.png){width="600" zoomable="yes"}

1. Gehen Sie wie folgt vor, um die Daten zu filtern:

   ![Couponbericht - Filter](./assets/reports-coupons-filters.png){width="600" zoomable="yes"}

   - Satz **[!UICONTROL Date Used]** auf einen der folgenden Werte zu:

      - `Order Created`
      - `Order Updated`

     Die _Bestellung aktualisiert_ wird in Echtzeit erstellt und erfordert keine Aktualisierung.

   - Um den Berichtszeitraum festzulegen, legen Sie **[!UICONTROL Period]** auf einen der folgenden Werte zu:

      - `Day`
      - `Month`
      - `Year`

   - Um den Datumsbereich des Berichts festzulegen, geben Sie **Von** und **nach** Daten im Format M/D/YY.

   - So drucken Sie einen Bericht für eine bestimmte [Bestellstatus](../stores-purchase/order-status.md), set **[!UICONTROL Order Status]** nach `Specified` und wählen Sie den Bestellstatus aus der Liste aus.

   - Wenn Sie Zeilen ohne Daten aus dem Bericht auslassen möchten, legen Sie **[!UICONTROL Empty Rows]** nach `No`.

   - Führen Sie einen der folgenden Schritte aus, um die im Bericht enthaltene Gutscheinaktivität zu definieren:

      - Um alle Gutscheinaktivitäten aus allen Preisregeln einzubeziehen, legen Sie **[!UICONTROL Cart Price Rule]** nach `Any`.
      - Um nur Aktivitäten einzubeziehen, die sich auf eine bestimmte Preisregel beziehen, legen Sie **[!UICONTROL Cart Price Rule]** nach `Specified` und wählen Sie die Regel für den Warenkorbpreis in der Liste aus.

1. Wenn der Bericht ausgeführt werden soll, klicken Sie auf **[!UICONTROL Show Report]**.

   Der Bericht wird unten auf der Seite angezeigt.

### Filteroptionen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Date Used] | Identifiziert das Datumsfeld, das als Berichtsgrundlage verwendet wird. Optionen:<br/>**[!UICONTROL Order Created]**: Generiert den Bericht basierend auf dem Datum, an dem die Bestellung vom Kunden aufgegeben wurde. Um sicherzustellen, dass die aktuellsten Daten enthalten sind, klicken Sie auf den Link in der Nachricht, um die Statistiken zu aktualisieren.<br/>**[!UICONTROL Order Updated]**: Erzeugt den Bericht basierend auf dem Datum, an dem die Bestellungen zuletzt aktualisiert wurden. Dieser Bericht verwendet Echtzeitdaten und erfordert keine Aktualisierung von Statistiken. |
| [!UICONTROL Period] | Bestimmt den Typ des Datumsbereichs, der für den Bericht verwendet wird. Optionen: `Day` / `Month` / `Year` |
| [!UICONTROL From] | Gibt das erste Datum im Bereich der Bestelldaten an, das im Bericht enthalten ist. |
| [!UICONTROL To] | Gibt das letzte Datum im Bereich der Bestelldaten an, die im Bericht enthalten sind. |
| [!UICONTROL Order Status] | Filtert den Bericht nach Bestellstatus. Der Bericht kann für alle Bestellungen generiert oder auf einen bestimmten Bestellstatus beschränkt werden. Optionen: <br/>**[!UICONTROL Any]**: Umfasst alle Bestellungen unabhängig vom Status.<br/>**[!UICONTROL Specified]**: Umfasst nur Bestellungen mit dem angegebenen Status. Abgebrochene Bestellungen sind nicht im Bericht enthalten. |
| [!UICONTROL Empty Rows] | Bestimmt, ob der Bericht Zeilen mit leeren Daten enthält, die möglicherweise abgerufen werden. Optionen: `Yes` / `No` |
| [!UICONTROL Cart Price Rules] | Bestimmt, welche Coupon-Promotions im Bericht enthalten sind. Optionen:<br/>**[!UICONTROL Any]**: Enthält Bestellinformationen für jede Coupon-Promotion, die innerhalb des angegebenen Datumsbereichs verwendet wurde.<br/>**[!UICONTROL Specified]**: Enthält nur Bestellinformationen für die ausgewählte Coupon-Promotion im angegebenen Datumsbereich. |

{style="table-layout:auto"}

### Berichtsspalten

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Interval] | Gibt den Datumsbereich der Gutscheinnutzung an, der in den Bericht aufgenommen werden soll. Das Intervall kann ein bestimmter Tag, Monat, Jahr oder Datumsbereich sein. Das Intervalldatum wird gemäß dem in **[!UICONTROL Period]** Einstellung:<br/>`Day`21.06.19<br/>`Month`: 6/2019<br/>`Year`: 2019 |
| [!UICONTROL Coupon Code] | Der Rabattcode, der von Kunden in den Warenkorb eingegeben wird, um den Rabatt zu erhalten. |
| [!UICONTROL Price Rule] | Der Name der Preisregel, die mit dem Coupon verknüpft ist. |
| [!UICONTROL Uses] | Die Häufigkeit, mit der der Gutschein in dem für den Bericht angegebenen Datumsbereich verwendet wurde. |
| [!UICONTROL Sales Subtotal] | Die projizierte Zwischensumme aller Bestellungen, die mit dem Gutschein platziert wurden. <br/>Die Zwischensumme der Verkäufe stellt die aggregierte Zwischensumme aller qualifizierten Bestellungen dar und schließt `Pending` Verkaufsaufträge, die noch nicht in Rechnung gestellt wurden. |
| [!UICONTROL Sales Discount] | Der prognostizierte Rabattbetrag aus allen Bestellungen, die mit dem Gutschein platziert wurden. <br/>Der Rabatt stellt den aggregierten Abzinsungsbetrag aus allen qualifizierten Bestellungen dar und umfasst `Pending` Verkaufsaufträge, die noch nicht in Rechnung gestellt wurden. |
| [!UICONTROL Sales Total] | Die prognostizierte Gesamtsumme aus allen Bestellungen, die mit dem Gutschein platziert wurden. Die Gesamtverkaufskosten beinhalten alle Versand- und Bearbeitungsgebühren abzüglich des Rabatts. <br/>Die Gesamtsumme der Verkäufe stellt den aggregierten Gesamtwert aller qualifizierten Bestellungen dar und umfasst `Pending` Verkaufsaufträge, die noch nicht in Rechnung gestellt wurden. Der Wert enthält die Zwischensumme zuzüglich Versand- und Bearbeitungskosten abzüglich des Rabatts zuzüglich Steuern. <br/> Berechnet durch: `((Subtotal + Shipping & Handling) - Discount) + Tax` |
| [!UICONTROL Subtotal] | Die aggregierte Zwischensumme aller fakturierten Bestellungen, die den Gutschein verwendet haben. |
| [!UICONTROL Discount] | Der aggregierte Rabatt von allen fakturierten Bestellungen, die den Gutschein verwendet haben. |
| [!UICONTROL Total] | Die aggregierte Bestellsumme aller fakturierten Bestellungen, die den Gutschein verwendet haben. |

{style="table-layout:auto"}
