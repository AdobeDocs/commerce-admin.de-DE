---
title: Erstellen einer Preisregel für den Warenkorb
description: Erfahren Sie, wie Sie eine Preisregel für den Warenkorb auf der Grundlage von Warenkorb oder Produktattributen erstellen.
exl-id: 7260e7c3-3b1e-43e5-9c09-c40538e37378
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 6ac8d41de0f97767296216f8239311bc6fbf168e
workflow-type: tm+mt
source-wordcount: '3320'
ht-degree: 0%

---

# Erstellen einer Preisregel für den Warenkorb

Führen Sie die folgenden Schritte aus, um eine Regel hinzuzufügen, die Bedingungen zu beschreiben und die Aktionen zu definieren. Füllen Sie auch die Beschriftungen aus und testen Sie die Regel. Preisregelbedingungen können auf dem Warenkorb oder [Produktattribute](../catalog/product-attributes.md) oder [Real-Time CDP-Zielgruppen](#use-real-time-cdp-audiences-to-set-a-condition), jedoch nicht auf [anpassbare Optionen](../catalog/settings-advanced-custom-options.md).

## Schritt 1: Hinzufügen einer Regel

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

1. Klicks **[!UICONTROL Add New Rule]** und gehen Sie wie folgt vor:

   - under _[!UICONTROL Rule Information]_, beenden Sie die **[!UICONTROL Rule Name]**und **[!UICONTROL Description]**.

   - Wenn die Regel nicht sofort in Kraft treten soll, legen Sie **[!UICONTROL Active]** nach `No`.

   ![Warenkorbpreisregel - Regelinformationen](./assets/price-rule-cart-new.png){width="600" zoomable="yes"}

1. Zur Festlegung der [Umfang](../getting-started/websites-stores-views.md#scope-settings) Führen Sie folgende Schritte aus:

   - Wählen Sie die **[!UICONTROL Websites]** wo die Promotion verfügbar sein soll.

   - Wählen Sie die **[!UICONTROL Customer Groups]** für die die Promotion gilt.

     Wenn Sie möchten, dass die Promotion nur registrierten Kunden zur Verfügung steht, **_nicht_** die `NOT LOGGED IN` -Option.

1. Legen Sie die Regel fest, die mit oder ohne [Coupon](price-rules-cart-coupon.md) wie folgt:

   - Um die Warenkorbregel ohne Verwendung eines Gutscheincodes anzuwenden, legen Sie **[!UICONTROL Coupon]** nach `No Coupon` und fahren Sie mit Schritt 5 fort.

   - Um einen Gutschein mit einer Preisregel zu verknüpfen, legen Sie **[!UICONTROL Coupon]** nach `Specific Coupon` und gehen Sie wie folgt vor:

      - Freitext eingeben **[!UICONTROL Coupon Code]** dass der Kunde eingeben muss, um den Rabatt zu erhalten.

      - Um die Anzahl der Verwendungsmöglichkeiten des Gutscheins zu begrenzen, führen Sie die folgenden Optionen aus:

     | Option | Beschreibung |
     |------|-----------|
     | `Uses per Coupon` | Bestimmt, wie oft der Gutscheincode verwendet werden kann. Wenn keine Begrenzung vorhanden ist, lassen Sie das Feld leer. |
     | `Uses per Customer` | Bestimmt, wie oft die Warenkorbpreisregel von demselben registrierten Kunden verwendet werden kann, der zu einer der ausgewählten Kundengruppen gehört. Die Einstellung gilt nicht für Gastkäufer, die Mitglieder der NOT LOGGED IN-Kundengruppe sind, oder für Kunden, die einkaufen, ohne sich bei ihren Konten anzumelden. Wenn keine Begrenzung vorhanden ist, lassen Sie das Feld leer. |

     {style="table-layout:auto"}

     Weitere Informationen finden Sie unter [Coupon-Codes](price-rules-cart-coupon.md).

     ![Preisregel für Warenkorb - Couponeinstellungen](./assets/price-rule-cart-coupon-settings-ee.png){width="600" zoomable="yes"}

   - ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Verwenden Sie die _Kalender_ (![Kalendersymbol](../assets/icon-calendar.png)), um die **[!UICONTROL From]** und **[!UICONTROL To]** Datumsbereich für die Promotion.

1. Geben Sie eine Zahl ein, um die **[!UICONTROL Priority]** dieser Preisregel in Bezug auf die Aktionseinstellungen anderer Preisregeln, die gleichzeitig aktiv sind.

   >[!NOTE]
   >
   >Die Einstellung Priorität ist wichtig, wenn zwei Warenkorbregeln/Couponcodes für dasselbe Produkt gleichzeitig gültig sind. Die Regel mit der Einstellung für die höchste Priorität (`1` die höchste) steuert die Warenkorbaktion. Siehe _Nachfolgende Preisregeln verwerfen_ im _Definieren der Aktionen_ Schritt.

   >[!NOTE]
   >
   >Preisregeln für Warenkorb mit derselben Priorität führen nicht zu einem kombinierten Rabatt. Jede Regel wird einzeln auf übereinstimmende Produkte angewendet, und zwar einzeln.

1. So wenden Sie die Regel auf die veröffentlichte [RSS-Feeds](social-rss.md#rss-feeds), set **Öffentlich im RSS-Feed** nach `Yes`.

1. Klicks **[!UICONTROL Save and Continue Edit]**.

   - ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Nach dem Speichern der Regel wird der Name der Warenkorbpreisregel oben auf der Seite angezeigt.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Nach dem Speichern der Regel werden der Name der Warenkorbpreisregel und die [Geplante Änderungen](price-rule-cart-scheduled-changes.md) wird oben auf der Seite angezeigt.

     ![Preisregel für Warenkorb - Geplante Änderungen](./assets/price-rule-cart-scheduled-changes.png){width="600" zoomable="yes"}

## Schritt 2: Beschreibung der Bedingungen

In diesem Schritt werden die Bedingungen beschrieben, die erfüllt sein müssen, damit eine Bestellung für die Promotion qualifiziert wird. Die Regel wird immer dann aktiv, wenn der Bedingungssatz erfüllt ist.

Wenn Sie Zielgruppen aus Real-Time CDP verwenden, überspringen Sie [diesem Abschnitt](#use-real-time-cdp-audiences-to-set-a-condition).

>[!NOTE]
>
>Die Preisregel für den Warenkorb wird auf **_each_** Produkt im Warenkorb immer dann, wenn die Bedingungen im _[!UICONTROL Conditions]_-Registerkarte erfüllt ist. Hinzufügen von Bedingungen in der_[!UICONTROL Actions]_ um die Anzahl der von der Regel für den Warenkorbpreis betroffenen Produkte zu begrenzen.

>[!NOTE]
>
>Wenn mindestens ein bedingtes Produktattribut einen leeren Wert hat, wird die Preisregel für den Warenkorb nicht auf das Produkt angewendet.

1. Wählen Sie im linken Bereich die Option **[!UICONTROL Conditions]**.

   ![Preisregel für Warenkorb - Bedingungen](./assets/conditions.png){width="600" zoomable="yes"}

   Die erste Bedingung wird standardmäßig und in den folgenden Status angezeigt:

   `If **ALL** of these conditions are **TRUE**:`

   Die Anweisung enthält zwei fette Links, auf die Sie klicken können, um die Auswahl der Optionen für diesen Teil der Anweisung anzuzeigen. Sie können unterschiedliche Bedingungen erstellen, indem Sie die Kombination dieser Werte ändern. Führen Sie einen der folgenden Schritte aus:

   - Klicks **[!UICONTROL ALL]** und wählen `ALL` oder `ANY`.
   - Klicks **[!UICONTROL TRUE]** und wählen `TRUE` oder `FALSE`.
   - Lassen Sie die Bedingung unverändert, um die Regel auf alle Produkte anzuwenden.

1. Klicks _Hinzufügen_ (![Symbol &quot;Hinzufügen&quot;](../assets/icon-add-green-circle.png)) am Anfang der nächsten Zeile und wählen Sie eine Option für die Bedingung aus, z. B. ein Warenkorbattribut, eine Unterauswahl des Produkts oder eine Kombination.

   Führen Sie für dieses Beispiel den nächsten Teil der Bedingung wie folgt aus:

   - Wenn Sie dazu aufgefordert werden **[!UICONTROL Choose the condition to add]** auswählen `Products Subselection`.

     ![Preisregel für Warenkorb - Unterauswahl von Produkten](./assets/price-rule-cart-condition-products-subselection.png){width="600" zoomable="yes"}

   - Klicken Sie in der Bedingungsanweisung auf **[!UICONTROL total quantity]** und wählen `total quantity` oder `total amount`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Total amount] ist eine Zeilensumme, sodass Steuern nicht im `total amount` für die [!UICONTROL Products Subselection] Preisregel für den Warenkorb. Verwenden Sie die [!UICONTROL Subtotal (Incl. Tax)] -Bedingung, um Steuern einzubeziehen.

   - Klicken Sie in der Bedingungsanweisung auf **[!UICONTROL is]** und wählen `greater than`.

1. Wenn der nächste Teil der Bedingung angezeigt wird, klicken Sie auf die Elemente der Anweisung, damit Sie sehen können, wo sich jeder Link mit Variablenwerten befindet.

1. Klicken Sie auf den Link &quot;Mehr&quot;(..) und geben Sie `100`.

   Diese Bedingung setzt voraus, dass die Gesamtmenge des Warenkorbs `101` oder höher.

   ![Preisregel für Warenkorb - Gesamtmengenwert](./assets/condition-products-subselection3.png){width="600" zoomable="yes"}

1. Klicks **Hinzufügen** (![Symbol &quot;Hinzufügen&quot;](../assets/icon-add-green-circle.png)) am Anfang der nächsten Zeile und fügen Sie dann eine Bedingung hinzu, die auf **Kategorie**.

   ![Preisregel für Warenkorb - Produktattributkategorie](./assets/condition-products-subselection4.png){width="600" zoomable="yes"}

1. Klicken Sie im nächsten Teil der Bedingung auf die _more_ (**...**), um das Eingabefeld anzuzeigen, und öffnen Sie dann die _Auswahl_ (![Listen-Symbol](../assets/icon-list-chooser.png)), um die Kategorienstruktur anzuzeigen.

1. Aktivieren Sie das Kontrollkästchen der Kategorie, die Sie als Bedingung für die Preisregel verwenden möchten, und klicken Sie auf ![Symbol &quot;Hinzufügen&quot;](../assets/icon-checkmark-green-circle.png) -Symbol, um die Kategorieauswahlen zu akzeptieren.

   Die Bedingung kann auf jeder Kategorie basieren, die ein untergeordnetes Element der [Stammkategorie](../catalog/category-root.md).

   ![Preisregel für Warenkorb - Produktkategorie](./assets/subselection-category.png){width="600" zoomable="yes"}

1. Um weitere Bedingungen hinzuzufügen, klicken Sie auf _Hinzufügen_ (![Symbol &quot;Hinzufügen&quot;](../assets/icon-add-green-circle.png)) und definieren Sie eine andere Bedingung.

   Sie können den Prozess so oft wie nötig wiederholen, um die Bedingungen zu beschreiben, die für die Preisregel erfüllt sein müssen. Im Folgenden finden Sie einige Beispiele:

   **Beispiel 1:** Regionale Preisregel

   Verwenden Sie eines der folgenden Warenkorbattribute, um eine regionale Preisregel zu erstellen:

   - `Shipping Postcode`
   - `Shipping Region`
   - `Shipping State/Province`
   - `Shipping Country`

   **Beispiel 2:** Warenkorbsummen

   Verwenden Sie eines der folgenden Warenkorbattribute, um die Bedingung auf den Gesamtwerten des Warenkorbs zu basieren:

   - `Subtotal`
   - `Total Items Quantity`
   - `Total Weight`

>[!NOTE]
>
>Bei mehreren parallelen Promotions muss die _Zwischensumme_ -Bedingung auf die _base_ Warenkorb-Zwischensumme **_before_** alle Rabatte.

>[!IMPORTANT]
>
>**Nur für Bestellungen**: Wenn eine Preisregel für den Warenkorb auf der Basis einer oder mehrerer spezifischer Zahlungsmethoden festgelegt wird, wird der Rabatt bei der Erstellung einer Bestellung auf den Gesamtbetrag angewendet. Nach der Erstellung der Bestellung bleibt der Rabatt auf den Gesamtbetrag angewendet, wenn die Zahlungsmethode in eine Methode geändert wird, die nicht von der Preisregel des Warenkorbs abgedeckt wird.

### Produktattribut zu Preisregeln für Warenkorb hinzufügen

1. Navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**und öffnen Sie das Produktattribut.

1. Wählen Sie im linken Bereich die Option **[!UICONTROL Storefront Properties]**.

1. Satz **[!UICONTROL Use for Promo Rule Conditions]** nach `Yes`.

1. Klicks **[!UICONTROL Save Attribute]**.

1. Navigieren Sie zu **[!UICONTROL Marketing]** > **[!UICONTROL Cart Price Rules]** und öffnen Sie die gewünschte Preisregel für den Warenkorb.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Condition]** und wählen Sie **[!UICONTROL Product attribute combination]**.

1. Legen Sie diese Bedingung auf einen der folgenden Werte fest:

   - Klicks **[!UICONTROL FOUND]** und wählen `FOUND` oder `NOT FOUND`.

   - Klicks **[!UICONTROL ALL]** und wählen `ALL` oder `ANY`.

1. Klicken Sie auf _Hinzufügen_ (![Symbol &quot;Hinzufügen&quot;](../assets/icon-add-green-circle.png)) und wählen Sie die **[!UICONTROL Product Attribute]** , die Sie für Bedingungen von Werberegeln eingerichtet haben.

1. Klicks **[!UICONTROL Save]**.

>[!NOTE]
>
>Bei Verwendung von `is not one of` mit einer _SKU_ Produktattribut und konfigurierbares Produkt, müssen sowohl die übergeordneten als auch untergeordneten Produkt-SKUs ausgewählt werden. Um zu vermeiden, dass alle untergeordneten SKUs in der Regel aufgelistet werden, können Sie die `does not contain` -Bedingung mit gängigen SKU-Teilen eines konfigurierbaren Produkts und seinen untergeordneten Produkten.

### Verwenden von Real-Time CDP-Zielgruppen zum Festlegen einer Bedingung

Sie können eine auf einer Real-Time CDP basierende Bedingung für eine Warenkorbpreisregel festlegen [audience](../customers/audience-activation.md).

1. Erweitern **[!UICONTROL Conditions]**, klicken Sie auf das &quot;+&quot;-Symbol und wählen Sie **[!UICONTROL Real-Time CDP Audience]** aus der Liste.

   ![Real-Time CDP-Zielgruppenbedingung auswählen](./assets/rtcdp-conditions.png){width="300"}

1. Wählen Sie die _Mehr_ (**...**), klicken Sie auf **[!UICONTROL Open Chooser]** und alle verfügbaren Real-Time CDP-Zielgruppen anzeigen.

   ![Anzeigen von Real-Time CDP-Zielgruppen](./assets/rtcdp-conditions-chooser.png){width="600" zoomable="yes"}

1. Wählen Sie die Real-Time CDP-Zielgruppe aus, die Sie für die Preisregel des Warenkorbs verwenden möchten.

   | Option | Beschreibung |
   |------|-----------|
   | `ID` | Interne Kennung der Audience, die innerhalb des Administrators verwendet wird |
   | `Real-Time CDP Audience ID` | Eindeutige Kennung der Audience bei ihrer Erstellung in Experience Platform |
   | `Name` | Name der Zielgruppe, z. B. `Orders over $50` |
   | `Description` | Beschreibung der Zielgruppe, z. B. `People who placed an order over $50 in the last month.`. |
   | `Source` | Gibt an, woher die Zielgruppe stammt, beispielsweise `Experience Platform`. |
   | `Website` | Gibt an, welche Website Sie mit dem Datastream verknüpft haben, der die Zielgruppen enthält. Sie erstellen diesen Link, wenn Sie Ihre Commerce-Instanz über die Experience Platform mit dem [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html) -Erweiterung. |

   {style="table-layout:auto"}

Im nächsten Schritt definieren Sie die Aktion, die ausgeführt werden soll, wenn die Bedingung erfüllt ist.

## Schritt 3: Aktionen definieren

Die Aktionen der Preisregel für Warenkorb beschreiben, wie Preise aktualisiert werden, wenn die Bedingungen erfüllt sind.

1. Nach unten scrollen zu **[!UICONTROL Actions]** und erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt.

   ![Preisregel für Warenkorb - Aktionen ](./assets/price-rule-cart-actions.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Apply]** auf eine der folgenden Rabattoptionen klicken:

   | Option | Beschreibung |
   |------|-----------|
   | `Percent of product price discount` | Rabattartikel durch Abzug eines Prozentsatzes vom ursprünglichen Preis. Der Rabatt gilt für jeden qualifizierenden Artikel im Warenkorb. Beispiel: Eingabe `10` in [!UICONTROL Discount Amount] für einen aktualisierten Preis, der 10 % unter dem ursprünglichen Preis liegt. |
   | `Fixed amount discount` | Rabattartikel durch Abzug eines festen Betrags vom ursprünglichen Preis jedes qualifizierten Artikels im Warenkorb. Beispiel: Eingabe `10` in [!UICONTROL Discount Amount] für einen aktualisierten Preis, der 10 USD unter dem ursprünglichen Preis liegt. |
   | Fester Rabatt auf den gesamten Warenkorb | Ermäßigt den gesamten Warenkorb durch Abzug eines festen Betrags von der Gesamtsumme des Warenkorbs. Beispiel: Geben Sie 10 ein in [!UICONTROL Discount Amount] um 10 USD von der Gesamtsumme des Warenkorbs abzuziehen. Standardmäßig gilt der Rabatt nur für die Zwischensumme des Warenkorbs. Um den Rabatt auf die Zwischensumme und den Versand separat anzuwenden, verwenden Sie die _[!UICONTROL Apply to Shipping Amount]_-Option. |
   | `Buy X get Y free` | Definiert eine Menge X, die der Kunde kaufen muss, um eine Menge Y zu erhalten **des gleichen Produkts/der gleichen Variante** kostenlos. (Die [!UICONTROL Discount Amount] ist Y.) Damit der Rabatt angewendet werden kann, muss eine Gesamtmenge von X+Y desselben Artikels im Warenkorb vorhanden bzw. im Warenkorb hinzugefügt werden. |

   {style="table-layout:auto"}

   - Geben Sie die **[!UICONTROL Discount Amount]** als Zahl, ohne Symbole. Beispielsweise kann die Zahl 1 je nach ausgewählter Rabattoption einen Prozentsatz, einen festen Betrag oder eine Menge an Artikeln angeben.

   - Für _Kauf X erhalten Y Free_ den Rabatt, geben Sie die Menge im **[!UICONTROL Discount Qty Step (Buy X)]** -Feld eines einzelnen Produkts/einer SKU/eines Zeileneintrags, den der Kunde kaufen muss, um den Rabatt auf die Y-Menge zu erhalten. Sowohl X als auch Y beziehen sich auf Mengen derselben SKU, und diese spezifische Menge (Variationen konfigurierbarer Produkte werden separat gezählt) des Artikels muss manuell zum Warenkorb hinzugefügt werden.

   - Im **[!UICONTROL Maximum Qty Discount is Applied To]** Geben Sie die Höchstmenge des Produkts ein, für das der Rabatt im selben Kauf gewährt werden kann.

   - Satz **[!UICONTROL Apply to Shipping Amount]** (![Optionsschalter](../assets/toggle-yes.png)) wie folgt:

     | Option | Beschreibung |
     |------|-----------|
     | `Yes` | Wendet den Rabattbetrag getrennt auf die Zwischensumme und die Versandkosten an. |
     | `No` | Wendet den Rabattbetrag nur auf die Zwischensumme an. |

     {style="table-layout:auto"}

   - Um die Verarbeitung anderer Regeln nach der Anwendung dieser Regel zu stoppen, legen Sie **[!UICONTROL Discard Subsequent Rules]** (![Optionsschalter](../assets/toggle-yes.png)) zu `Yes`. Diese Einstellung verhindert, dass mehrere Rabatte auf dasselbe Produkt angewendet werden.

     | Option | Beschreibung |
     |------|-----------|
     | `Yes` | Verhindert die Anwendung anderer Preisregeln, die für ein Produkt gelten. Wenn mehrere Preisregeln für dasselbe Produkt gelten, gilt nur die Preisregel mit der höchsten definierten Priorität (in einer Regel [!UICONTROL Priority] -Feld) auf das qualifizierende Produkt angewendet. Dadurch wird verhindert, dass mehrere Preisregeln stapeln und unbeabsichtigte zusätzliche Rabatte bieten. |
     | `No` | Ermöglicht die Anwendung mehrerer Preisregeln auf dasselbe Produkt. Dies kann zu einer Stapelung und zur Bereitstellung mehrerer Rabatte führen, die auf Ihren Listenpreis angewendet werden. |

     {style="table-layout:auto"}

     >[!IMPORTANT]
     >
     >Um nachfolgende Regeln zu verwerfen, muss eine Preisregel die definierten Prioritäten verwenden, die im Feld Priorität jeder Regel festgelegt sind, und mehrere Regeln sollten nicht dieselbe Priorität haben. Siehe **[!UICONTROL Priority]** im _Neue Regel hinzufügen_ Schritt.

1. So definieren Sie die **_exact_** Produkte im Warenkorb, die von der Warenkorbpreisregel betroffen sind, hinzufügen Sie die **_additional_** Bedingungen, die für die Aktion erforderlich sind.

   Um festzustellen, ob der kostenlose Versand auf Bestellungen angewendet wird, die die Bedingungen erfüllen, legen Sie **[!UICONTROL Free Shipping]** auf einen der folgenden Werte zu:

   | Option | Beschreibung |
   |------|-----------|
   | `No` | Kostenloser Versand ist nicht verfügbar. |
   | `For matching items only` | Kostenloser Versand ist nur für Artikel verfügbar, die den Bedingungen der Regel entsprechen. |
   | `For shipment with matching items` | Kostenloser Versand ist für jede Lieferung verfügbar, die die entsprechenden Artikel enthält. Die [Kostenloser Versand](../stores-purchase/shipping-free.md) -Versandmethode muss aktiviert sein, damit diese Option verwendet werden kann. |

   {style="table-layout:auto"}

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Für **[!UICONTROL Add Rewards Points]**, geben Sie die feste Anzahl von Punkten ein, die der Kunde erhält **_once_** pro Bestellung, wenn die Preisregel des Warenkorbs angewendet wird.

   Wenn die Belohnungspunkte nicht aktiviert sind, lassen Sie dieses Feld leer.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save and Continue Edit]**.

## Schritt 4: Bezeichnungen ausfüllen

Der Titel wird im Abschnitt &quot;Gesamtsummen&quot;der Bestellung angezeigt, um den Rabatt zu ermitteln. Der Beschriftungstext wird in Klammern hinter dem Wort eingefügt `Discount`. Sie können eine Standardbeschriftung für alle Store-Ansichten eingeben oder für jede Ansicht eine andere Beschriftung eingeben.

![Storefront-Warenkorb - Discount-Bezeichnungen](./assets/order-totals-section-discount-special.png){width="600"}

1. Nach unten scrollen zu **[!UICONTROL Labels]** und erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png)den Abschnitt.

1. Geben Sie den Text ein, den Sie als **[!UICONTROL Default Rule Label for All Store Views]**.

   ![Preisregel für Warenkorb - Standardbeschriftung](./assets/label-default.png){width="600" zoomable="yes"}

1. Wenn Ihr Store mehrere Ansichten oder mehrere Websites mit mehreren Ansichten hat, geben Sie den entsprechenden Beschriftungstext für jede Seite ein.

   Wenn sich beispielsweise jede Store-Ansicht in einer anderen Sprache befindet, geben Sie die Übersetzung der Beschriftung für jede Ansicht ein.

   ![Store-spezifische Beschriftungen](./assets/label-store-specific.png){width="600" zoomable="yes"}

## Schritt 5: Zugehörige dynamische Bausteine hinzufügen (optional)

{{ee-feature}}

[Dynamische Blöcke](../content-design/dynamic-blocks.md) die mit der Regel verknüpft sind, werden in der Storefront angezeigt, sobald die Bedingungen erfüllt sind.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Related Dynamic Blocks]** Abschnitt.

1. Verwenden Sie die [Suchfilter](../getting-started/admin-workspace.md) , um die Blöcke zu finden, die Sie mit der Regel verknüpfen möchten.

1. Aktivieren Sie das Kontrollkästchen in der ersten Spalte, um den Block mit der Regel zu verknüpfen.

   Weitere Informationen finden Sie unter [Dynamische Blöcke in Preisregeln](../content-design/dynamic-blocks-price-rules.md).

## Schritt 6: Speichern und testen Sie die Regel

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Rule]**.

1. Testen Sie die Regel, um sicherzustellen, dass sie ordnungsgemäß funktioniert.

   Preisregeln werden jede Nacht automatisch mit anderen Systemregeln verarbeitet. Wenn Sie eine Preisregel erstellen, lassen Sie genügend Zeit, um in das System zu gelangen. Testen Sie auch die Regel, um sicherzustellen, dass sie ordnungsgemäß funktioniert. Da neue Regeln hinzugefügt werden, berechnet Commerce die Preise und Prioritäten entsprechend neu.

## Demo zur Warenkorbpreisregel

Sehen Sie sich dieses Video an, um mehr über das Erstellen von Preisregeln für Warenkorb zu erfahren:

>[!VIDEO](https://video.tv.adobe.com/v/343835?quality=12)

## Feldbeschreibungen

### [!UICONTROL Rule Information]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Rule Name] | (Erforderlich) Der Name der Regel dient als interne Referenz. |
| [!UICONTROL Description] | Eine Beschreibung der Regel sollte den Zweck der Regel enthalten und erläutern, wie sie verwendet wird. |
| [!UICONTROL Active] | (Erforderlich) Bestimmt, ob die Regel im Store aktiv ist. Optionen: `Yes` / `No` |
| [!UICONTROL Websites] | (Erforderlich) Identifiziert die Websites, auf denen die Regel verwendet werden kann. |
| [!UICONTROL Customer Groups] | (Erforderlich) Identifiziert die Kundengruppen, für die die Regel gilt. |
| [!UICONTROL Coupon] | (Erforderlich) Gibt an, ob ein Coupon mit der Regel verknüpft ist. Optionen: <br/>**[!UICONTROL No Coupon]**- Der Regel ist kein Coupon zugeordnet.<br/>**[!UICONTROL Specific Coupon]** - Ein bestimmter Coupon ist mit der Regel verknüpft. <br/>**[!UICONTROL Coupon Code]**- Geben Sie bei Aufforderung den Coupon-Code ein, den der Kunde eingeben muss, um die Promotion nutzen zu können.<br/>**[!UICONTROL Use Auto Generation]** - Aktivieren Sie das Kontrollkästchen, um automatisch mehrere Coupon-Codes zu generieren, die mit der Promotion verwendet werden können. <br/>**[!UICONTROL Auto]**- Zeigt die _[!UICONTROL Manage Coupon Codes]_-Abschnitt, um das Format der zu erzeugenden Couponcodes zu definieren. |
| [!UICONTROL Uses per Coupon] | Bestimmt, wie oft der Gutscheincode verwendet werden kann. Wenn keine Begrenzung vorhanden ist, lassen Sie das Feld leer. |
| [!UICONTROL Uses per Customer] | Bestimmt, wie oft die Warenkorbpreisregel von demselben registrierten Kunden verwendet werden kann, der zu einer ausgewählten Kundengruppe gehört. Gilt nicht für Gastkäufer, die Mitglieder der NOT LOGGED IN-Kundengruppe sind, oder für Kunden, die einkaufen, ohne sich bei ihren Konten anzumelden. Lassen Sie das Feld leer, wenn keine Beschränkung festgelegt wurde. |
| [!UICONTROL Priority] | Eine Zahl, die die Priorität dieser Regel im Verhältnis zu anderen angibt. Die höchste Priorität ist die Zahl `1`. |
| [!UICONTROL Public in RSS Feed] | Bestimmt, ob die Promotion im öffentlichen RSS-Feed Ihres Stores enthalten ist. Optionen:  `Yes` / `No` |
| [!UICONTROL From] | ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Das erste Datum, an dem der Gutschein verwendet werden kann. |
| [!UICONTROL To] | ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Das letzte Datum, an dem der Gutschein verwendet werden kann. |

{style="table-layout:auto"}

### [!UICONTROL Conditions]

Gibt die Bedingungen an, die erfüllt sein müssen, bevor die Preisregel für den Warenkorb in Kraft tritt. Wenn Sie das Feld leer lassen, gilt die Regel für alle Produkte im Warenkorb. Bedingungen können auf einer beliebigen Kombination von Warenkorb- und Produktattributen basieren. Allerdings [anpassbare Optionen](../catalog/settings-advanced-custom-options.md) kann nicht in den Bedingungen der Preisregel des Warenkorbs referenziert werden.

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL **Warenkorbelement-Attribut**] |  |
| [!UICONTROL Price in cart] | Produktpreis. Die Regel gilt, wenn der Produktpreis in Warenkorbbedingungen erfüllt ist. |
| [!UICONTROL Quantity in cart] | Produktmenge. Die Regel gilt, wenn die Produktmenge in Warenkorbbedingungen erfüllt ist. |
| [!UICONTROL Row total in cart] | Gesamtsumme der Produktzeilen. Die Regel gilt, wenn die Gesamtsumme der Produktzeile in der Warenkorbbedingung erfüllt ist. |
| [!UICONTROL **Produktattribut**] |  |
| [!UICONTROL Attribute Set] | Produktattributsatz. Die Regel gilt, wenn das Produkt die Produktattributbedingung erfüllt. |
| [!UICONTROL Category] | Produktkategorie. Die Regel gilt, wenn entweder das Produkt selbst oder sein untergeordnetes Produkt die Kategoriebedingung erfüllt. |
| [!UICONTROL Category (Children Only)] | Untergeordnete Produktkategorie. Die Regel gilt, wenn nur die untergeordneten Produktelemente die Kategoriebedingung erfüllen (das Produkt selbst ist hier nicht überprüft). |
| [!UICONTROL Category (Parent Only)] | Übergeordnete Produktkategorie. Die Regel gilt, wenn nur das Produkt selbst die Kategoriebedingung erfüllt (untergeordnete Produkte werden hier nicht überprüft). |
| [!UICONTROL **Warenkorbattribut**] |  |
| [!UICONTROL Subtotal (Excl. Tax)] | Teilsumme Warenkorb (ohne Steuern). Die Regel gilt, wenn der Warenkorb die Bedingung der Zwischensumme (ohne Steuern) erfüllt. |
| [!UICONTROL Subtotal (Incl. Tax)] | Untersumme Warenkorb (inkl. Steuer). Die Regel gilt, wenn der Warenkorb die Bedingung der Zwischensumme (einschließlich Steuern) erfüllt. |
| [!UICONTROL Subtotal] | Zwischensumme Warenkorb. Die Regel gilt, wenn der Warenkorb eine Zwischenbedingung erfüllt. Durch die Option wird die Steuer entsprechend den aktuellen Steuereinstellungen ein- oder ausgeschlossen. |
| [!UICONTROL Total Items Quantity] | Gesamtmenge aller Produkte im Warenkorb. Die Regel gilt, wenn der Warenkorb eine Bedingung für die Gesamtmenge der Artikel erfüllt. |
| [!UICONTROL Total Weight] | Gesamtgewicht aller Produkte im Warenkorb. Die Regel gilt, wenn der Warenkorb die Gesamtgewichtsbedingung erfüllt. |
| [!UICONTROL Payment Method] | Zahlungsmethode beim Checkout ausgewählt. Die Regel gilt, wenn die Zahlungsmethode-Bedingung erfüllt ist. |
| [!UICONTROL Shipping Method] | Versandmethode beim Checkout ausgewählt. Die Regel gilt, wenn die Versandmethodenbedingung erfüllt ist. |
| [!UICONTROL Shipping Postcode] | Postleitzahl der Versandadresse. Die Regel gilt, wenn die Lieferadresse die Postleitzahl-Bedingung erfüllt. |
| [!UICONTROL Shipping Region] | Versandadressenbereich. Die Regel gilt, wenn die Lieferadresse die Regionsbedingung erfüllt. |
| [!UICONTROL Shipping State/Province] | Versandadresse Bundesland/-staat Die Regel gilt, wenn die Lieferadresse die Bundesland-/Bundesbedingung erfüllt. |
| [!UICONTROL Shipping Country] | Land der Versandadresse. Die Regel gilt, wenn die Lieferadresse den Landesbedingungen entspricht. |
| [!UICONTROL Customer Segment] | Die Regel gilt, wenn ein registrierter oder Gastkunden die Bedingung für das Kundensegment erfüllt. |

### [!UICONTROL Actions]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Apply] | Bestimmt den Berechnungstyp, der auf den Kauf angewendet wird. Optionen: <br/>**[!UICONTROL Percent of product price discount]**- Ermäßigung durch Abzug eines Prozentsatzes vom ursprünglichen Preis. Beispiel: Eingabe `10` in _[!UICONTROL Discount Amount]_für einen aktualisierten Preis, der 10 % unter dem ursprünglichen Preis liegt.<br/>**[!UICONTROL Fixed amount discount]**- Rabattartikel durch Abzug eines festen Betrags vom ursprünglichen Preis jedes qualifizierten Artikels im Warenkorb. Beispiel: Eingabe `10` in_[!UICONTROL Discount Amount]_ für einen aktualisierten Preis, der 10 USD unter dem ursprünglichen Preis liegt. <br/>**[!UICONTROL Fixed amount discount for whole cart]**- Ermäßigt den gesamten Warenkorb durch Abzug eines festen Betrags von der Teilsumme des Warenkorbs. Beispiel: Eingabe `10` in _[!UICONTROL Discount Amount]_um 10 USD von der Teilsumme des Warenkorbs abzuziehen. Standardmäßig gilt der Rabatt nur für die Zwischensumme des Warenkorbs. Informationen zur getrennten Anwendung des Rabatts auf die Zwischensumme und den Versand finden Sie unter_Auf Versandbetrag anwenden _.<br/>**[!UICONTROL Buy X Get Y Free (discount amount is Y)]**- Definiert eine Menge, die der Kunde kaufen muss, um eine Menge kostenlos zu erhalten. (Die_[!UICONTROL Discount Amount]_ ist Y.) |
| [!UICONTROL Discount Amount] | (Erforderlich) Die Höhe des angebotenen Rabatts. |
| [!UICONTROL Maximum Qty Discount is Applied To] | Legt die maximale Anzahl von Produkten fest, auf die der Rabatt im selben Kauf angewendet werden kann. |
| [!UICONTROL Discount Qty Step (Buy X)] | Legt die Anzahl der Produkte fest, die durch `X` in einer `Buy X Get Y Free` Förderung. Außerdem wird definiert, wie viele Produkte in Stapeln zum Warenkorb hinzugefügt werden müssen, damit sie angewendet werden `Fixed amount discount` und `Percent of product price discount` Promotions. |
| [!UICONTROL Apply to Shipping Amount] | Bestimmt, ob der Rabatt getrennt auf die Zwischensumme und die Versandbeträge angewendet wird. Andernfalls wird sie nur auf die Zwischensumme angewendet. Optionen: `Yes` / `No` |
| [!UICONTROL Discard Subsequent Rules] | Bestimmt, ob Regeln mit niedrigerer Priorität (1 ist die höchste Priorität) auf das Produkt angewendet werden können, wenn diese Preisregel für den Warenkorb eine Übereinstimmung ist. Aktivieren Sie diese Option, um zu verhindern, dass mehrere Rabatte auf dasselbe Produkt angewendet werden. Optionen: `Yes` / `No` |
| [!UICONTROL Free Shipping] | Bestimmt, ob die kostenlose Lieferung in der Promotion enthalten ist und wenn ja, für welche Artikel. Optionen: <br/>**[!UICONTROL No]**- Kostenloser Versand ist für die aktuelle Regel nicht verfügbar.<br/>**[!UICONTROL For matching items only]** - Kostenloser Versand ist nur für bestimmte Artikel im Warenkorb verfügbar, die der Regel entsprechen. <br/>**[!UICONTROL For shipment with matching items]**- Kostenloser Versand ist für alle Artikel im Warenkorb verfügbar. Die [Kostenloser Versand](../stores-purchase/shipping-free.md) -Versandmethode muss aktiviert sein, damit diese Option verwendet werden kann. |
| [!UICONTROL Add Reward Points] | ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Gibt die Anzahl der [Belohnungspunkte](rewards-loyalty.md) die der Kunde bei Anwendung der Preisregel verdient. |

{style="table-layout:auto"}

### [!UICONTROL Labels]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Default Rule Label for All Store Views] | Eine Standardbeschriftung, die den Rabatt angibt und für alle Store-Ansichten verwendet werden kann. |
| [!UICONTROL Store View Specific Labels] | Gibt ggf. eine andere Bezeichnung an, um den Rabatt für jede Store-Ansicht zu identifizieren. |

{style="table-layout:auto"}

### [!UICONTROL Related Dynamic Blocks]

{{ee-feature}}

Identifiziert alle [dynamische Blöcke](../content-design/dynamic-blocks.md) die mit der Regel verknüpft sind.
