---
title: Couponcodes
description: Erfahren Sie, wie Sie Gutscheincodes mit Warenkorbpreisregeln verwenden können, um einen Rabatt anzuwenden, wenn eine Reihe von Bedingungen erfüllt ist.
exl-id: 4f2e6203-0de2-44eb-a5f7-edd7b5f714d1
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 7407df02ca62e36b4dd60dba418eae3e6aa34491
workflow-type: tm+mt
source-wordcount: '1839'
ht-degree: 0%

---

# Couponcodes

Couponcodes werden verwendet mit [Preisregeln für Warenkorb](price-rules-cart.md) , um einen Rabatt anzuwenden, wenn eine Reihe von Bedingungen erfüllt ist. Beispielsweise kann ein Gutscheincode für eine bestimmte Kundengruppe oder für jeden erstellt werden, der einen Kauf über einen bestimmten Betrag tätigt. Um den Coupon auf einen Kauf anzuwenden, kann der Kunde den Couponcode im Warenkorb oder möglicherweise an der Kasse Ihrer Bestellung eingeben _Mauerwerk_ Speichern. Im Folgenden finden Sie einige Möglichkeiten, wie Sie Gutscheine in Ihrem Geschäft verwenden können:

- Gutscheine per E-Mail an Kunden senden
- Produzieren gedruckter Coupons
- Erstellen von Gutscheinen für mobile Benutzer im Geschäft

Gutscheincodes können per E-Mail gesendet oder in Newslettern, Katalogen und Werbeanzeigen eingeschlossen werden. Die Liste der Gutscheincodes kann exportiert und an eine kommerzielle Druckerei gesendet werden. Sie können auch Gutscheine im Geschäft mit einem schnellen Antwort-Code erstellen, den Käufer mit ihren Smartphones scannen können. Der QR-Code kann auf eine Seite auf Ihrer Website mit weiteren Informationen über die Promotion verlinken.

Ab Commerce 2.4.7 können Käufer mehrere Gutscheine auf einen Warenkorb anwenden. Händler können auch mehrere Gutscheine mit Shopping-Hilfe beantragen.

## Gutscheincodes konfigurieren

Die Länge und das Format der automatisch generierten Couponcodes werden von der Konfiguration gesteuert. Die Zeichen können auf alle Zahlen, alle Buchstaben oder eine Kombination festgelegt werden. Sie können in festgelegten Abständen einen Bindestrich einfügen, um die Lesbarkeit zu verbessern, und ein Präfix und ein Suffix hinzufügen, um den Code mit einer bestimmten Kampagne oder Initiative zu verknüpfen.

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich . **[!UICONTROL Customers]** und wählen **[!UICONTROL Promotions]**.

   ![Konfiguration des Kunden - automatisch generierte spezifische Gutscheincodes](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Erweitern Sie die **[!UICONTROL Auto Generated Specific Coupon Codes]** -Abschnitt.

   ![Konfiguration des Kunden - automatisch generierte spezifische Gutscheincodes](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Geben Sie die **[!UICONTROL Code Length]**, einschließlich Präfix, Suffix und Trennzeichen.

1. Legen Sie die **[!UICONTROL Code Format]** eine der folgenden Möglichkeiten:

   - `Alphanumeric`
   - `Alphabetical`
   - `Numeric`

1. für **[!UICONTROL Code Prefix]**, geben Sie den Wert ein, der am Anfang aller Gutscheincodes angezeigt werden soll.

1. für **[!UICONTROL Code Suffix]**, geben Sie den Wert ein, der am Ende aller Gutscheincodes angezeigt werden soll.

1. für **[!UICONTROL Dash Every X Characters]**, geben Sie die Anzahl der Zeichen zwischen den einzelnen Bindestrichen ein.

   Couponcodes mit unterschiedlichen Bindestrichmustern werden als unterschiedliche Codes betrachtet, auch wenn die Zahlen gleich sind.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Erstellen von Gutscheinen

>[!NOTE]
>
>Bevor Sie Gutscheine erstellen, verwenden Sie die `bin/magento cron:run` Befehl, um zu überprüfen, ob Cron ausgeführt wird. Siehe [Ausführen von cron über die Befehlszeile](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html#run-cron-from-the-command-line) in der _Konfigurationshandbuch_ für weitere Informationen.

### Methode 1: Erstellen eines bestimmten Coupons

1. Befolgen Sie die Anweisungen zum Erstellen eines [Warenkorb-Preisregel](price-rules-cart.md).

1. In der **[!UICONTROL Rule Information]** Abschnitt, festgelegt **[!UICONTROL Coupon]** bis `Specific Coupon`.

1. Geben Sie ein **[!UICONTROL Coupon Code]** Zur Verwendung mit der Promotion.

   Das Format des Codes (numerisch, alphanumerisch oder alphabetisch) wird bestimmt durch [Konfiguration](#configure-coupon-codes).

1. Gehen Sie wie folgt vor, um zu begrenzen, wie oft der Coupon verwendet werden kann:

   - Geben Sie die Anzahl der **[!UICONTROL Uses per Coupon]**.
   - Geben Sie die Anzahl der **[!UICONTROL Uses per Customer]**.

   Lassen Sie diese Felder leer, um sie unbegrenzt zu verwenden.

   ![Warenkorb-Preisregel - Couponinformationen](./assets/coupon-info.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Wenn ein und derselbe Coupon von mehreren Kunden gleichzeitig verwendet wird, kann es sein, dass die festgelegte Nutzungsbeschränkung aufgrund einer verzögerten Couponbearbeitung überschritten wird.

1. Gehen Sie wie folgt vor, um den Gutschein für einen bestimmten Zeitraum gültig zu machen:

   - ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Vervollständigen Sie **Von** und **bis** Daten. Um das Datum auszuwählen, klicken Sie **Kalender** (![Kalendersymbol](../assets/icon-calendar.png)) neben jedem Feld angezeigt. Wenn Sie den Datumsbereich leer lassen, läuft die Regel nicht ab.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Führen Sie einen der folgenden Schritte aus:

     **Option 1:** Neue Aktualisierung planen

      - Klick **[!UICONTROL Schedule New Update]** in der rechten oberen Ecke der Seite.

        ![Aktualisierung planen](./assets/coupon-schedule-new-update.png){width="600" zoomable="yes"}

      - Geben Sie die **[!UICONTROL Update Name]** und **[!UICONTROL Description]**.

      - Wählen Sie die **Startdatum** und **[!UICONTROL End Date]** aus dem Kalender ( ![Kalendersymbol](../assets/icon-calendar.png) ). Wenn Sie den Datumsbereich leer lassen, läuft die Regel nicht ab.

      - Klicken Sie abschließend auf **[!UICONTROL Save]**.

        ![Warenkorb-Preisregel - Geplante Änderung](./assets/coupon-scheduled-change.png){width="600" zoomable="yes"}

     **Option 2:** Einem vorhandenen Update zuweisen:

      - Auswählen **[!UICONTROL Assign to Another Update]**.

      - Suchen Sie die Aktualisierung in der Liste und klicken Sie auf **[!UICONTROL Select]**.

1. Vervollständigen Sie das [Warenkorb-Preisregel](price-rules-cart.md) nach Bedarf.

### Methode 2: Erzeugen eines Couponbatches

Die Erstellung von Rabattgutscheinen ist ein asynchroner Vorgang, der im Hintergrund ausgeführt wird, damit Sie in der Admin weiterarbeiten können, ohne auf den Abschluss des Vorgangs zu warten. Wenn die Aufgabe abgeschlossen ist, wird eine Meldung angezeigt.

1. Befolgen Sie die Anweisungen zum Erstellen eines [Warenkorb-Preisregel](price-rules-cart.md).

1. Unter **[!UICONTROL Coupon Code]**, wählen Sie die **[!UICONTROL Use Auto Generation]** Kontrollkästchen.

1. Um zu begrenzen, wie oft jeder Kunde den Coupon verwenden kann, geben Sie die Anzahl der **[!UICONTROL Uses per Customer]**.

   ![Warenkorb-Preisregel - Erstellt automatisch nummerierte Coupons](./assets/coupon-auto.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Wenn ein und derselbe Coupon von mehreren Kunden gleichzeitig verwendet wird, kann es sein, dass die festgelegte Nutzungsbeschränkung aufgrund einer verzögerten Couponbearbeitung überschritten wird.

1. Nach unten scrollen und erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL Manage Coupon Codes]** und gehen Sie folgendermaßen vor:

   ![Warenkorb-Preisregel - Verwalten von Gutscheincodes](./assets/manage-coupon-codes.png){width="600" zoomable="yes"}

   - für **[!UICONTROL Coupons Qty]**, geben Sie die Anzahl der Coupons ein, die Sie generieren möchten.

   - Geben Sie die **[!UICONTROL Code Length]**, ohne Präfix, Suffix oder Trennzeichen.

   - Legen Sie die **[!UICONTROL Code Format]** eine der folgenden Möglichkeiten:

      - `Alphanumeric`
      - `Alphabetical`
      - `Numeric`

   - (Optional) Geben Sie ein **[!UICONTROL Code Prefix]** , die am Anfang des Codes hinzugefügt werden sollen.

   - (Optional) Geben Sie ein **[!UICONTROL Code Suffix]** wird am Ende des Codes hinzugefügt.

   - (Optional) Für **[!UICONTROL Dash Every X Characters]**, geben Sie die Anzahl der Zeichen zwischen den einzelnen Bindestrichen ein. Wenn der Code beispielsweise 12 Zeichen lang ist und alle vier Zeichen ein Bindestrich vorhanden ist, sieht es wie folgt aus `xxxx-xxxx-xxxx`. Bindestriche erleichtern das Lesen und die Eingabe von Codes.

1. Klicken Sie abschließend auf **[!UICONTROL Generate]**.

   Das System zeigt `Message is added to queue, wait to get your coupons soon`.

   Nach Abschluss des Cron-Vorgangs wird die Liste der generierten Codes angezeigt.

   | Feld | Beschreibung |
   |-------------|-------------|
   | [!UICONTROL Coupon Code] | Ein eindeutiger Couponcode, der erstellt wurde und für den Erhalt spezieller Bedingungen verwendet werden kann. |
   | [!UICONTROL Created] | Das Datum, an dem der Couponcode erstellt wurde. |
   | [!UICONTROL Used] | Gibt an, ob der Coupon verwendet wurde. |
   | [!UICONTROL Times Used] | Gibt an, wie oft der Couponcode verwendet wurde. |

   {style="table-layout:auto"}

Sie können Gutscheincodes in eine CSV- oder Excel-XML-Datei exportieren, indem Sie das Dateiformat auswählen und auf klicken. **[!UICONTROL Export]**.

Um Gutscheincodes zu löschen, wählen Sie einen oder mehrere Codes aus der Liste aus. Auswählen `Delete` vom **[!UICONTROL Actions]**  auswählen, und klicken Sie dann auf **[!UICONTROL Submit]**.

>[!NOTE]
>
>Obwohl Commerce die Konfiguration mehrerer Gutscheincodes ermöglicht, kann ein Kunde nur einen Gutscheincode im Warenkorb verwenden. Um die gleichzeitige Verwendung von mehr als einem Couponcode im Warenkorb zu ermöglichen, können Sie eine entsprechende Erweiterung von verwenden. [Commerce Marketplace](https://marketplace.magento.com/).

## Bericht zu Coupons

Die _Coupons_ Der Bericht aggregiert Daten aus jedem Coupon, der während eines bestimmten Datumsbereichs verwendet wird. Da Gutscheine aus dem Warenkorb angewendet werden, enthält der Bericht Daten aus allen eingelösten Gutscheinen, unabhängig davon, [Bestellstatus](../stores-purchase/order-status.md). Daher kann der Bericht sowohl die projizierten als auch die tatsächlichen Gesamtwerte enthalten. Der Bericht kann nach einer bestimmten Store-Ansicht, einem bestimmten Zeitraum, einem Bestellstatus und einer Warenkorb-Preisregel gefiltert werden.

Im folgenden Beispiel wurde der Couponcode „H20“ von zwei Kunden verwendet. Eine der Bestellungen wird fakturiert, die andere ist immer noch _ausstehend_. Die Spalten Projizierte Umsatzzwischensumme, Verkaufsrabatt und Verkaufssumme zeigen die aggregierten Beträge aus beiden Aufträgen an, aber nur der tatsächlich fakturierte Auftrag wird in den Spalten Zwischensumme, Rabatt und Gesamtsumme angezeigt. Jede Zeile im Bericht stellt eine einzelne Gutscheinaktion dar.

![Bericht zu Coupons](./assets/reports-coupons.png){width="600" zoomable="yes"}

### Bericht ausführen

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**.

1. Wenn Sie über mehrere Store-Ansichten verfügen, legen Sie Folgendes fest **[!DNL Store View]** in der oberen linken Ecke, um den Umfang des Berichts festzulegen.

1. So aktualisieren Sie die Verkäufe [Statistik](../getting-started/sales-reports.md#refresh-statistics) Klicken Sie für den Tag auf die Schaltfläche _Zuletzt aktualisiert_ Nachricht oben im Arbeitsbereich.

   Klicken Sie als Nächstes auf , um den **[!UICONTROL Coupons]** Kontrollkästchen und klicken Sie auf **[!UICONTROL Refresh]**.

   ![Couponbericht - Statistiken aktualisieren](./assets/reports-coupons-refresh-statistics.png){width="600" zoomable="yes"}

1. Gehen Sie wie folgt vor, um die Daten zu filtern:

   ![Coupon-Bericht - Filter](./assets/reports-coupons-filters.png){width="600" zoomable="yes"}

   - set **[!UICONTROL Date Used]** eine der folgenden Möglichkeiten:

      - `Order Created`
      - `Order Updated`

     Die _Aktualisierte Bestellung_ Der Bericht wird in Echtzeit erstellt und erfordert keine Aktualisierung.

   - Um den Zeitraum zu definieren, der vom Bericht abgedeckt wird, legen Sie Folgendes fest **[!UICONTROL Period]** eine der folgenden Möglichkeiten:

      - `Day`
      - `Month`
      - `Year`

   - Um den Datumsbereich des Berichts zu definieren, geben Sie Folgendes ein: **Von** und **bis** Daten im M/D/YY-Format.

   - So drucken Sie einen Bericht für eine bestimmte [Bestellstatus](../stores-purchase/order-status.md), festlegen **[!UICONTROL Order Status]** bis `Specified` und wählen Sie den Bestellstatus aus der Liste aus.

   - Um Zeilen ohne Daten aus dem Bericht wegzulassen, legen Sie Folgendes fest **[!UICONTROL Empty Rows]** bis `No`.

   - Um die im Bericht enthaltenen Couponaktivitäten zu definieren, führen Sie einen der folgenden Schritte aus:

      - Um alle Couponaktivitäten aus allen Preisregeln einzubeziehen, setzen Sie **[!UICONTROL Cart Price Rule]** bis `Any`.
      - Um nur Aktivitäten einzubeziehen, die sich auf eine bestimmte Preisregel beziehen, setzen Sie **[!UICONTROL Cart Price Rule]** bis `Specified` und wählen Sie die Warenkorb-Preisregel in der Liste aus.

1. Wenn Sie den Bericht ausführen möchten, klicken Sie auf **[!UICONTROL Show Report]**.

   Der Bericht wird unten auf der Seite angezeigt.

### Filteroptionen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Date Used] | Gibt das Datumsfeld an, das als Grundlage für den Bericht verwendet wird. Optionen:<br/>**[!UICONTROL Order Created]**: Generiert den Bericht basierend auf dem Datum, an dem die Bestellung vom Kunden aufgegeben wurde. Um sicherzustellen, dass die aktuellen Daten enthalten sind, klicken Sie auf den Link in der Nachricht, um die Statistiken zu aktualisieren.<br/>**[!UICONTROL Order Updated]**: Generiert den Bericht basierend auf dem Datum der letzten Aktualisierung der Bestellungen. Dieser Bericht verwendet Echtzeitdaten und erfordert keine Aktualisierung von Statistiken. |
| [!UICONTROL Period] | Bestimmt den Typ des Datumsbereichs, der für den Bericht verwendet wird. Optionen: `Day` / `Month` / `Year` |
| [!UICONTROL From] | Gibt das erste Datum im Bereich der Bestelldaten an, die im Bericht enthalten sind. |
| [!UICONTROL To] | Gibt das letzte Datum im Bereich der Bestelldaten an, die im Bericht enthalten sind. |
| [!UICONTROL Order Status] | Filtert den Bericht nach Bestellstatus. Der Bericht kann für alle Bestellungen generiert oder auf einen bestimmten Bestellstatus beschränkt werden. Optionen: <br/>**[!UICONTROL Any]**: Umfasst alle Bestellungen unabhängig vom Status.<br/>**[!UICONTROL Specified]**: Umfasst nur Bestellungen mit dem angegebenen Status. Stornierte Bestellungen sind nicht im Bericht enthalten. |
| [!UICONTROL Empty Rows] | Bestimmt, ob der Bericht Zeilen mit leeren Daten enthält, die möglicherweise abgerufen werden. Optionen: `Yes` / `No` |
| [!UICONTROL Cart Price Rules] | Legt fest, welche Gutscheinaktionen in den Bericht aufgenommen werden. Optionen:<br/>**[!UICONTROL Any]**: Enthält Bestellinformationen für jede Gutscheinaktion, die während des angegebenen Datumsbereichs verwendet wurde.<br/>**[!UICONTROL Specified]**: Enthält nur Bestellinformationen für die ausgewählte Couponaktion während des angegebenen Datumsbereichs. |

{style="table-layout:auto"}

### Berichtsspalten

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Interval] | Gibt den Datumsbereich der Couponnutzung an, die in den Bericht aufgenommen werden soll. Das Intervall kann ein bestimmter Tag, Monat, Jahr oder Datumsbereich sein. Das Intervalldatum wird entsprechend dem in festgelegten Wert wie in den folgenden Beispielen formatiert **[!UICONTROL Period]** Einstellung:<br/>`Day`: 6/21/19<br/>`Month`: 6/2019<br/>`Year`: 2019 |
| [!UICONTROL Coupon Code] | Der Rabattcode, den Kunden in den Warenkorb eingeben, um den Rabatt zu erhalten. |
| [!UICONTROL Price Rule] | Der Name der Preisregel, die mit dem Coupon verknüpft ist. |
| [!UICONTROL Uses] | Die Häufigkeit, mit der der Coupon im für den Bericht angegebenen Datumsbereich verwendet wurde. |
| [!UICONTROL Sales Subtotal] | Die voraussichtliche Zwischensumme aller Bestellungen, die mit dem Coupon aufgegeben wurden. <br/>Die Zwischensumme Umsatz stellt die aggregierte Zwischensumme aller qualifizierten Aufträge dar und umfasst `Pending` Aufträge, die noch nicht fakturiert wurden. |
| [!UICONTROL Sales Discount] | Der voraussichtliche Rabattbetrag aus allen Bestellungen, die mit dem Coupon aufgegeben wurden. <br/>Der Rabatt stellt den aggregierten Rabattbetrag aus allen qualifizierten Aufträgen dar und umfasst `Pending` Aufträge, die noch nicht fakturiert wurden. |
| [!UICONTROL Sales Total] | Die prognostizierte Gesamtsumme aller Bestellungen, die mit dem Coupon aufgegeben wurden. Die Verkaufssumme beinhaltet alle Versand- und Bearbeitungsgebühren abzüglich des Rabattbetrags. <br/>Die Umsatzsumme stellt den aggregierten Gesamtbetrag aller qualifizierten Bestellungen dar und umfasst `Pending` Aufträge, die noch nicht fakturiert wurden. Der Wert beinhaltet die Zwischensumme plus Versand und Bearbeitung, abzüglich des Rabatts, plus Steuer. <br/> Berechnet von: `((Subtotal + Shipping & Handling) - Discount) + Tax` |
| [!UICONTROL Subtotal] | Die aggregierte Zwischensumme aller fakturierten Aufträge, die den Coupon verwendet haben. |
| [!UICONTROL Discount] | Der aggregierte Rabatt aller fakturierten Bestellungen, die den Coupon verwendet haben. |
| [!UICONTROL Total] | Die aggregierte Bestellsumme aller fakturierten Bestellungen, die den Coupon verwendet haben. |

{style="table-layout:auto"}
