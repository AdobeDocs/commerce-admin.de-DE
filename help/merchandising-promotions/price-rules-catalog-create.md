---
title: Erstellen einer Katalogpreisregel
description: Erfahren Sie, wie Sie eine Katalogpreisregel erstellen, die einen Rabatt auf bestimmte Produkte anwendet, sobald eine Reihe von Bedingungen erfüllt ist.
exl-id: 53c5745b-f1c4-4ee8-b995-d2c70f639c7d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1639'
ht-degree: 0%

---

# Erstellen einer Katalogpreisregel

Befolgen Sie diese Anweisungen, um einen Rabatt auf bestimmte Produkte anzuwenden, wenn bestimmte Bedingungen erfüllt sind. Rabatte für die Katalogpreisregel werden wirksam, bevor das Produkt in den Warenkorb gelegt wird.

## Schritt 1: Hinzufügen einer Regel

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rule]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add New Rule]**.

   Die _[!UICONTROL Rule Information]_Abschnitt enthält erweiterbare Abschnitte für **[!UICONTROL Conditions]**und **[!UICONTROL Actions]**.

   ![Katalogpreisregel - Informationen](./assets/price-rule-catalog-new-ee.png){width="700" zoomable="yes"}

1. Führen Sie die **[!UICONTROL Rule Name]** und **[!UICONTROL Description]** -Felder.

   Diese Felder dienen nur Ihrer internen Referenz.

1. Legen Sie die **[!UICONTROL Status]** der Preisregel nach Bedarf.

   Standardmäßig lautet der Status `Inactive`.

   >[!NOTE]
   >
   >Nachdem die Regel erstellt wurde, kann ihr Status aktualisiert werden, indem der Status in `Active` oder `Inactive` nach Bedarf.

1. Wählen Sie die **[!UICONTROL Websites]** wo die Regel verfügbar sein soll.

1. Wählen Sie die **[!UICONTROL Customer Groups]** für die diese Regel gilt.

   Um mehrere Gruppen auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

   >[!NOTE]
   >
   >Die Optionen in dieser Liste hängen von den in _Kunden_ > _Kundengruppen_.

1. ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Geben Sie die **[!UICONTROL From]** und **[!UICONTROL To]** Daten, um zu bestimmen, wann die Preisregel in Kraft ist.

   Sie können Datumsangaben eingeben oder die **[!UICONTROL Calendar]** (![Kalendersymbol](../assets/icon-calendar.png)), um die Daten auszuwählen. Wenn Sie die Daten leer lassen, wird die Regel beim Speichern der Preisregel aktiviert.

1. Geben Sie eine Zahl ein, um die **[!UICONTROL Priority]** dieser Regel in Bezug auf andere Regeln.

   >[!NOTE]
   >
   >Die _[!UICONTROL Priority]_-Einstellung ist wichtig, wenn dasselbe Katalogprodukt die Bedingungen für mehr als eine Preisregel erfüllt. Die Regel mit der Einstellung mit der höchsten Priorität (1 ist die höchste) wird für das Produkt aktiv.

## Schritt 2: Bedingungen definieren

Die meisten verfügbaren Bedingungen basieren auf vorhandenen Attributwerten. Lassen Sie die Bedingungen leer, um die Regel auf alle Produkte anzuwenden.

>[!NOTE]
>
>Wenn mindestens ein bedingtes Produktattribut einen leeren Wert hat, wird die Katalogpreisregel nicht auf das Produkt angewendet.

>[!NOTE]
>
>So wenden Sie eine `Category` Produktattributbedingung für jede [Bundle](../catalog/product-create-bundle.md) oder [grouped](../catalog/product-create-grouped.md) -Produkt, müssen alle untergeordneten Produkte derselben Kategorie zugeordnet werden, damit die Regel korrekt angewendet wird. Wenn nicht, können Sie eine [Preisregel für Warenkorb](price-rules-cart-create.md) Promotion.

1. Hinunter scrollen und erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Conditions]** Abschnitt.

   Die erste Bedingung wird standardmäßig und in den folgenden Status angezeigt:

   `If **ALL** of these conditions are **TRUE**:`

   ![Katalogpreisregel - Bedingungszeile 1](./assets/catalog-condition1.png){width="400"}

   Die Anweisung enthält zwei fette Links, auf die Sie klicken können, um die Auswahl der Optionen für diesen Teil der Anweisung anzuzeigen. Sie können unterschiedliche Bedingungen erstellen, indem Sie die Kombination dieser Werte ändern.

1. Ändern Sie die Anweisung auf eine der folgenden Arten:

   - Klicks **[!UICONTROL ALL]** und wählen `ALL` oder `ANY`.
   - Klicks **[!UICONTROL TRUE]** und wählen `TRUE` oder `FALSE`.
   - Lassen Sie die Bedingung unverändert, um die Regel auf alle Produkte anzuwenden.

   Sie können unterschiedliche Bedingungen erstellen, indem Sie die Kombination dieser Werte ändern. Für dieses Beispiel wird die Standardbedingung verwendet.

1. Klicken Sie auf _Hinzufügen_ (![Symbol &quot;Hinzufügen&quot;](../assets/icon-add-green-circle.png)) am Anfang der nächsten Zeile und wählen Sie eine Option für die Bedingung aus, z. B. ein Produktattribut oder eine Kombination.

1. In der Liste unter **[!UICONTROL Product Attribute]**, wählen Sie das Attribut aus, das Sie als Grundlage für die Bedingung verwenden möchten.

   In diesem Beispiel lautet die Bedingung `Attribute Set`.

   ![Katalogpreisregel - Bedingungszeile 2](./assets/catalog-condition2.png){width="400"}

   >[!NOTE]
   >
   >Damit ein Attribut in der Liste angezeigt wird, muss es für die Verwendung in Bedingungen für Werberegeln konfiguriert werden. Weitere Informationen finden Sie unter [Produktattribute](../catalog/product-attributes.md).

   >[!NOTE]
   >
   >Bei Verwendung von `is not one of` mit einer _SKU_ Produktattribut und konfigurierbares Produkt, müssen sowohl die übergeordneten als auch untergeordneten Produkt-SKUs ausgewählt werden. Um zu vermeiden, dass alle untergeordneten SKUs in der Regel aufgelistet werden, können Sie die `does not contain` -Bedingung mit gängigen SKU-Teilen eines konfigurierbaren Produkts und seinen untergeordneten Produkten.

   Die ausgewählte Bedingung wird in der Anweisung angezeigt, gefolgt von zwei weiteren fett gedruckten Links. Die Optionen variieren je nach ausgewähltem Bedingungsattribut. In der Erklärung heißt es nun:

   `If **ALL** of these conditions are **TRUE**: <br/>Attribute Set **is** …`

1. Klicks **[!UICONTROL is]** und wählen Sie den Vergleichsoperator aus, der die zu erfüllende Bedingung beschreibt.

   Diese Optionen können eine Option für verschiedene Vergleiche enthalten. In diesem Beispiel sind die Optionen `is` und `is not`.

1. Wählen Sie Werte für die Bedingung aus oder geben Sie Werte ein.

   Je nach Bedingung können Sie Produkte aus einem Raster oder einer Liste auswählen, einen numerischen Wert eingeben usw.

   ![Katalogpreisregel - Bedingungszeile 2](./assets/catalog-condition3.png){width="400"}

   Das ausgewählte Element wird in der Anweisung angezeigt, um die Bedingung abzuschließen.

   `If **ALL** of these conditions are **TRUE**: <br/> Attribute Set **is Default**`

1. Um der Anweisung eine weitere Bedingungszeile hinzuzufügen, klicken Sie auf die _Hinzufügen_ (![Symbol &quot;Hinzufügen&quot;](../assets/icon-add-green-circle.png)) und wählen Sie eine der folgenden Optionen aus:

   - `Conditions Combination`
   - `Product Attribute`

   Wiederholen Sie den Vorgang, bis alle gewünschten Bedingungen abgeschlossen sind.

   Wenn Sie jederzeit einen Teil der Bedingungsanweisung löschen möchten, klicken Sie auf die **[!UICONTROL Delete]** (![Löschsymbol](../assets/icon-delete-red-circle.png) -Symbol am Ende der Zeile.

## Schritt 3: Aktionen definieren

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png)die **[!UICONTROL Actions]** und führen Sie folgende Schritte aus:

   ![Katalogpreisregel - Aktionen](./assets/price-rule-catalog-actions.png){width="600" zoomable="yes"}

1. under **[!UICONTROL Pricing Structure Rules]**, set **[!UICONTROL Apply]** auf einen der folgenden Werte zu:

   - `Apply as percentage of original` - Rabattartikel durch Abzug eines Prozentsatzes des regulären Preises. Beispiel: Geben Sie 10 in Rabattbetrag für einen Endpreis ein, der 10 % vom regulären Preis abweicht.
   - `Apply as fixed amount` - Ermäßigung durch Abzug eines festen Betrags vom regulären Preis. Beispiel: Geben Sie 10 in Rabattbetrag ein, wenn der Endpreis 10 USD unter dem regulären Preis liegt.
   - `Adjust final price to this percentage` - Passt den Endpreis um einen Prozentsatz des regulären Preises an. Beispiel: Geben Sie 25 in Rabattbetrag für einen Endpreis ein, der um 75 % vom regulären Preis abgeschnitten ist.
   - `Adjust final price to discount value` - Legt den Endpreis auf einen festen, abgezinsten Betrag fest. Beispiel: Geben Sie 20 in Rabattbetrag für einen Endpreis von 20,00 $ ein.

   >[!NOTE]
   >
   >_Regelpreis_ bezieht sich auf den Basisproduktpreis ohne fortgeschrittene Preise (spezielle/Tier/Gruppe) oder Sonderrabatte. _Endpreis_ bezeichnet den ermäßigten Preis, der im Warenkorb angezeigt wird. <br/>Die **_final_** Der Produktpreis wird als **_Minimum_** relevanter Preis nach folgender Formel: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

   >[!NOTE]
   >
   >**_Festpreis_** Anpassbare Produktoptionen sind _not_ beeinflusst von den Regeln für Gruppenpreis, Tier-Preis, Sonderpreis oder Katalogpreis.

1. Geben Sie die **[!UICONTROL Discount Amount]**.

1. Um die Verarbeitung anderer Regeln nach der Anwendung dieser Regel zu stoppen, legen Sie **[!UICONTROL Discard Subsequent Rules]** nach `Yes`.

   >[!NOTE]
   >
   >Setzen Sie dies auf `Yes` ist eine Schutzmaßnahme, um zu verhindern, dass das System mehrere Rabatte (Regeln) auf ein und dieselbe Ware anwendet.

## Schritt 4: Zugehörige dynamische Bausteine hinzufügen

{{ee-feature}}

[Dynamische Blöcke](../content-design/dynamic-blocks.md) die mit einer Katalogpreisregel verknüpft sind, werden in der Storefront angezeigt, sobald die Bedingungen erfüllt sind. Dies ist ein optionaler Schritt.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png)die **[!UICONTROL Related Dynamic Blocks]** Abschnitt.

1. Verwenden Sie die [Suchfilter](../getting-started/admin-workspace.md) , um die dynamischen Blöcke zu finden, die Sie mit der Regel verknüpfen möchten.

1. Aktivieren Sie das Kontrollkästchen in der ersten Spalte, um den dynamischen Block mit der Regel zu verknüpfen.

   ![Katalogpreisregel - zugehörige dynamische Blöcke](./assets/price-rule-catalog-related-dynamic-blocks.png){width="600" zoomable="yes"}

1. Klicken **[!UICONTROL Save and Continue Edit]**.

## Schritt 5: Regel planen

{{ee-feature}}

>[!NOTE]
>
>Das Festlegen der Regel auf &quot;aktiv&quot;muss als geplante Aktualisierung hinzugefügt werden. Weitere Informationen finden Sie unter [Geplante Änderungen](price-rule-catalog-scheduled-changes.md).

1. Im _Geplante Änderungen_ Feld, klicken Sie auf **[!UICONTROL Schedule New Update]** am oberen Rand des Feldes).

   Wenn die Regel bereits über eine geplante Aktualisierung verfügt, können Sie auf **[!UICONTROL View/Edit]** rechts neben der aufgelisteten Änderung.

   Sie können entweder die vorhandene Aktualisierung bearbeiten oder die Katalogpreisregel einer anderen Kampagne zuweisen. Die **Vorhandene Aktualisierung bearbeiten** ist standardmäßig aktiviert.

1. Um die Regel zu planen, geben Sie die **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** dass die Preisregel aktiv sein soll.

   Sie können entweder das Datum eingeben oder die Daten aus dem _Kalender_ (![Kalendersymbol](../assets/icon-calendar.png)).

   ![Katalogpreisregel - Aktualisierungszeitplan](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

1. Klicken **[!UICONTROL Save]**.

1. Im _Regelinformationen_ festlegen, legen Sie die **[!UICONTROL Status]** nach `active`.

## Schritt 6: Speichern und testen Sie die Regel

1. Wenn Sie fertig sind, speichern Sie die Regel.

   - ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Klicken Sie auf **[!UICONTROL Save and Apply]**.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Klicken Sie auf **[!UICONTROL Save]**.

     Auf der Seite Regelinformationen wird eine aktualisierte Timeline in den geplanten Änderungen für die Regel angezeigt.

     ![Katalogpreisregeln - Geplante Änderungen](./assets/price-rule-scheduled-changes-updated.png){width="600" zoomable="yes"}

1. Eigenschaften für eine Regel aktualisieren:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Klicken Sie auf **[!UICONTROL Edit]** , um _[!UICONTROL Rule Information]_Seite.

   - ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Klicken Sie auf die Regel in der Liste, um die _[!UICONTROL Rule Information]_Seite.

1. Testen Sie die Regel, um sicherzustellen, dass sie ordnungsgemäß funktioniert.

   Preisregeln werden jede Nacht automatisch mit anderen Systemregeln verarbeitet. Wenn Sie eine Preisregel erstellen, lassen Sie genügend Zeit, um in das System zu gelangen, bevor Sie die Regel testen, um sicherzustellen, dass sie ordnungsgemäß funktioniert. Da neue Regeln hinzugefügt werden, berechnet der Handel die Preise und Prioritäten entsprechend neu.

## Demo zu Katalogpreisregeln

Sehen Sie sich dieses Video an, um mehr über das Erstellen von Katalogpreisregeln zu erfahren:

>[!VIDEO](https://video.tv.adobe.com/v/343834?quality=12)

## Feldbeschreibungen

### [!UICONTROL Rule Information]

| Feld | Beschreibung |
|-----|-----------|
| [!UICONTROL Rule name] | (Erforderlich) Der Name der Regel dient als interne Referenz. |
| [!UICONTROL Description] | Eine Beschreibung der Regel sollte den Zweck der Regel enthalten und erläutern, wie sie verwendet wird. |
| [!UICONTROL Websites] | (Erforderlich) Identifiziert die Websites, auf denen die Regel verwendet werden kann. |
| [!UICONTROL Customer Groups] | (Erforderlich) Identifiziert die Kundengruppen, für die die Regel gilt. |
| [!UICONTROL Priority] | Eine Zahl, die die Priorität dieser Regel im Verhältnis zu anderen angibt. Die höchste Priorität ist Nummer 1. |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Bestimmt, ob die Regel im Store aktiv ist. Optionen: `Yes` / `No` |
| [!UICONTROL From] | ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Gibt den ersten Tag an, an dem die Preisregel in Kraft ist. Wenn Sie das Feld leer lassen, wird die Preisregel beim Speichern wirksam. |
| [!UICONTROL To] | ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Gibt den letzten Tag an, an dem die Preisregel in Kraft ist. Wenn Sie das Feld leer lassen, wird die Preisregel auf unbestimmte Zeit fortgesetzt. |

{style="table-layout:auto"}

### [!UICONTROL Conditions]

Gibt die Bedingungen an, die erfüllt sein müssen, bevor die Katalogpreisregel in Kraft tritt. Wenn Sie das Feld leer lassen, gilt die Regel für alle Produkte.

### [!UICONTROL Actions]

| Feld | Beschreibung |
|-----|-----------|
| [!UICONTROL Apply] | Bestimmt den Berechnungstyp, der auf den Kauf angewendet wird. Optionen: <br/>**[!UICONTROL Apply as percentage of original]**- Rabattartikel durch Abzug eines Prozentsatzes des regulären Preises.<br/>**[!UICONTROL Apply as fixed amount]** - Ermäßigung durch Abzug eines festen Betrags vom regulären Preis. <br/>**[!UICONTROL Adjust final price to this percentage]**- Passt den Endpreis um einen Prozentsatz des regulären Preises an.<br/>**[!UICONTROL Adjust final price to discount value]** - Legt den Endpreis auf einen festen, abgezinsten Betrag fest. <br/><br/>**_Hinweis:_**Der reguläre Preis bezieht sich auf den Basisproduktpreis ohne fortgeschrittene Preise (spezielle/Tier/Gruppe) oder Sonderrabatte. Der endgültige Preis bezieht sich auf den ermäßigten Preis, der im Warenkorb angezeigt wird. <br/>Die**_final _**Der Produktpreis wird als**_Minimum _**relevanter Preis nach folgender Formel: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)` |
| [!UICONTROL Discount Amount] | (Erforderlich) Die Höhe des angebotenen Rabatts. |
| [!UICONTROL Discard Subsequent Rules] | Bestimmt, ob zusätzliche Regeln auf diesen Kauf angewendet werden können. Um zu verhindern, dass mehrere Rabatte auf denselben Kauf angewendet werden, wählen Sie `Yes`. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Related Dynamic Blocks]

{{ee-feature}}

Identifiziert alle [dynamische Blöcke](../content-design/dynamic-blocks.md) die mit der Regel verknüpft sind.
