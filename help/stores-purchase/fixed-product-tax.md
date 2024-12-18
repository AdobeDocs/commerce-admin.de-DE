---
title: Feste Produktsteuer (FPT)
description: Erfahren Sie, wie Sie eine feste Produktsteuer (FPT) einrichten können, die zu bestimmten Produktarten hinzugefügt werden muss.
exl-id: f1b475cb-a6fe-4b51-a0c3-7d0a202bd332
feature: Checkout, Invoices, Taxes, Products
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 0%

---

# Feste Produktsteuer (FPT)

Einige Steuergebiete haben eine feste Steuer, die auf bestimmte Produktarten erhoben werden muss. Sie können eine _feste Produktsteuer)_ Bedarf für die Steuerberechnungen Ihres Stores einrichten. In einigen Ländern kann die FTP zur Einführung einer Steuer auf Elektro- und Elektronik-Altgeräte (EEAG) verwendet werden. Diese Steuer wird auch als _Umweltsteuer_ oder _Ökosteuer_ bezeichnet und wird auf bestimmte Arten von Elektronik erhoben, um die Recyclingkosten auszugleichen. Es handelt sich um einen festen Betrag und nicht um einen Prozentsatz des Produktpreises.

Feste Produktsteuern gelten auf Artikelebene, basierend auf dem Produkt. In einigen Ländern unterliegt diese Steuer einer zusätzlichen prozentualen Steuerberechnung. Ihr Steuergebiet kann auch Regeln darüber enthalten, wie der Produktpreis für Kunden dargestellt wird, entweder mit oder ohne Steuer. Vergewissern Sie sich, dass Sie die Regeln verstehen und Ihre FTP-Anzeigeoptionen entsprechend einstellen.

Seien Sie vorsichtig, wenn Sie FPT-Preise in E-Mails angeben, da der Preisunterschied das Vertrauen der Kunden in ihre Bestellungen beeinträchtigen kann. Wenn Sie z. B. Bestellüberprüfungspreise anzeigen, ohne den VZÄ anzuzeigen, sehen Kunden, die Artikel mit zugehörigen VZÄ kaufen, eine Summe, die den VZÄ-Steuerbetrag enthält, jedoch ohne eine Aufschlüsselung nach Einzelposten. Der Preisunterschied kann dazu führen, dass einige Kunden ihren Warenkorb aufgeben, da sich der Gesamtbetrag von dem erwarteten Betrag unterscheidet.

## FPT Preise anzeigen

| FPT | Anzeigeeinstellung und Berechnung | |
|--- |--- |---|
| Nicht besteuert | **[!UICONTROL Excluding FPT]** | FPT wird als separate Zeile im Warenkorb angezeigt und der Wert wird in entsprechenden Steuerberechnungen verwendet. |
| | **[!UICONTROL Including FPT]** | Die fpt wird zum Grundpreis eines Artikels addiert, ist aber nicht in steuerregelbasierten Berechnungen enthalten. |
| | **[!UICONTROL Excluding FPT, FPT Description, Final Price]** | Preise erscheinen ohne FPT-Betrag oder Beschreibung. FPT ist nicht in steuerregelbasierten Berechnungen enthalten. |
| steuerpflichtig | **[!UICONTROL Excluding FPT]** | FPT wird als separate Zeile im Warenkorb angezeigt und der Wert wird in entsprechenden Steuerberechnungen verwendet. |
| | **[!UICONTROL Including FPT]** | FPT ist im Preis eines Artikels enthalten, und es ist keine Änderung der Steuerberechnungen erforderlich. |
| | **[!UICONTROL Excluding FPT, FPT Description, Final Price]** | Die Preise erscheinen ohne den FPT-Betrag oder die Beschreibung. FPT ist jedoch in steuerregelbasierten Berechnungen enthalten. |

{style="table-layout:auto"}

## Konfigurieren von FPT

Mit der FPT (Fixed Product Tax[ (Eingabetyp](../catalog/attributes-input-types.md) wird ein Abschnitt mit Feldern für die Steuerverwaltung für jede Region erstellt.

Die folgenden Anweisungen zeigen, wie Sie am Beispiel „Ökosteuer“ eine feste Produktsteuer für Ihr Geschäft einrichten. Nachdem Sie den Umfang der Steuer und die Länder und Bundesstaaten festgelegt haben, in denen die Steuer gilt, und je nach den von Ihnen gewählten Optionen können sich die Eingabefelder entsprechend den lokalen Anforderungen ändern. Weitere Informationen finden Sie unter [Produktattribute erstellen](../catalog/attribute-product-create.md).

### Schritt 1: Feste Produktsteuer aktivieren

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Tax]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Fixed Product Taxes]** .

1. Legen Sie **[!UICONTROL Enable FPT]** auf `Yes` fest.

1. Um zu bestimmen, wie feste Produktsteuern in den Ladenpreisen verwendet werden, wählen Sie die FTP-Einstellung für jeden der folgenden Preisanzeigestellen:

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Prices on Product View Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   Optionen (jeweils gleich):

   - `Including FPT Only`
   - `Including FPT and FPT description`
   - `Excluding FPT. Including FPT description and final price`
   - `Excluding FPT`

1. **[!UICONTROL Apply Tax to FPT]** nach Bedarf festlegen.

1. **[!UICONTROL Include FPT in Subtotal]** nach Bedarf festlegen.

   ![Feste Produktsteuern](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung jeder dieser Konfigurationseinstellungen finden Sie unter [Feste Produktsteuern](../configuration-reference/sales/tax.md#fixed-product-taxes) im _Konfigurationsreferenzhandbuch_.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

### Schritt 2: Erstellen eines FPT-Attributs

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add New Attribute]** und führen Sie folgende Schritte aus:

   - Geben Sie **[!UICONTROL Default Label]** einen Titel ein, der das Attribut identifiziert.

   - Legen Sie **[!UICONTROL Catalog Input for Store Owner]** auf `Fixed Product Tax` fest.

   ![Attributeigenschaften](./assets/tax-fpt-attribute-properties.png){width="600" zoomable="yes"}

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Advanced Attribute Properties]** und legen Sie die Eigenschaftsoptionen fest:

   - **[!UICONTROL Attribute Code]** - Geben Sie eine eindeutige Kennung in Kleinbuchstaben ein, ohne Leerzeichen oder Sonderzeichen. Die maximale Länge beträgt 30 Zeichen. Sie können das Feld leer lassen, um den Text aus dem Feld Standardbezeichnung zu übernehmen.

   - **[!UICONTROL Add to Column Options]** : Wenn das FPT-Feld in der [Produktliste“ angezeigt werden soll](../catalog/products-list.md) legen Sie auf `Yes` fest.

   - **[!UICONTROL Use in Filter Options]** : Wenn Sie Produkte im Raster basierend [ dem Wert des FPT](../getting-started/admin-workspace.md)Felds filtern möchten, legen Sie auf `Yes` fest.

   ![Erweiterte Attributeigenschaften](./assets/tax-fpt-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. (Optional) Wählen Sie im linken Bereich die Option **[!UICONTROL Manage Labels]** und geben Sie einen Titel ein, der anstelle des Standardtitels für jede Shop-Ansicht verwendet werden soll.

   ![Kennzeichnungen verwalten](./assets/attribute-new-manage-labels.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Attribute]**.

1. Aktualisieren Sie bei Aufforderung den [Cache](../systems/cache-management.md).

### Schritt 3: Hinzufügen des FPT-Attributs zu einem Attributsatz

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Klicken Sie in der Liste auf das Attribut set , um den Datensatz im Bearbeitungsmodus zu öffnen.

   ![Liste der Attributsätze](./assets/attribute-sets-list.png){width="600" zoomable="yes"}

1. Ziehen Sie das FPT -Attribut aus der Liste der **[!UICONTROL Unassigned Attributes]** rechts in die Liste der **[!UICONTROL Groups]** in der mittleren Spalte.

   Jeder Gruppenordner entspricht einem Abschnitt mit Produktinformationen. Sie können das Attribut an einer beliebigen Stelle platzieren, an der es angezeigt werden soll, wenn das Produkt im Bearbeitungsmodus geöffnet ist.

   ![Attributsatz bearbeiten](./assets/tax-fpt-attribute-set-drag.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

1. Wiederholen Sie diesen Schritt für jeden Attributsatz, der eine feste Produktsteuer enthalten soll.

### Schritt 4: Anwendung von FTP auf bestimmte Produkte

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Öffnen Sie das Produkt, für das eine feste Produktsteuer benötigt wird, im Bearbeitungsmodus.

1. Suchen Sie den **[!UICONTROL FPT]** Abschnitt der Felder, die Sie dem Attributsatz hinzugefügt haben, und klicken Sie auf **[!UICONTROL Add Tax]**.

1. Geben Sie die anzuwendende Steuer für das Produkt an:

   ![Feste Produktsteuer für Kanada](./assets/tax-product-fpt-canada.png){width="600" zoomable="yes"}

   - Wenn Ihre Commerce-Instanz über mehrere Websites verfügt, wählen Sie die entsprechende **[!UICONTROL Website]** und Basiswährung aus. In diesem Beispiel ist das Feld standardmäßig auf `All Websites [USD]` festgelegt.

   - Legen Sie **[!UICONTROL Country/State]** auf die Region fest, in der die feste Produktsteuer gilt.

   - Geben Sie **[!UICONTROL Tax]** die feste Produktsteuer als Dezimalbetrag ein.

1. Um weitere feste Produktsteuern hinzuzufügen, klicken Sie auf **[!UICONTROL Add Tax]** und wiederholen Sie den Vorgang.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.
