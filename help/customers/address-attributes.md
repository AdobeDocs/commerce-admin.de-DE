---
title: Attribute der Kundenadressen
description: Erfahren Sie mehr über die Attribute der Kundenadresse und wie Sie diese Attributeigenschaften konfigurieren.
exl-id: 637a0f81-4d8f-40cb-a1b6-537229b2ce5b
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1471'
ht-degree: 0%

---

# Attribute der Kundenadressen

{{ee-feature}}

Der Attributsatz Kundenadresse bestimmt die Eigenschaften von Straßenadressen, die in die Variablen [Adressbuch](account-dashboard-address-book.md) vom Kundenkonto oder während der [Kasse](../stores-purchase/checkout-process.md).

Benutzerdefinierte Adressattribute können eingerichtet werden, um zusätzliche Informationen bereitzustellen, wie eine optionale E-Mail-Adresse, ein Skype-Konto, eine alternative Telefonnummer, ein Gebäude oder ein Bezirk. Das benutzerdefinierte Attribut kann dann in die [Adressenvorlage](address-templates.md) die zur Erstellung von Verkaufsdokumenten verwendet wird. Das Erstellen eines benutzerdefinierten Adressattributs entspricht fast dem Erstellen eines [Kundenattribut](attribute-properties.md).

Kundenadressattribute werden in den folgenden Formularen verwendet:

- [Registrierung der Kundenadresse](account-create.md)
- [Kundenkontoadresse](account-dashboard-address-book.md)

![Admin - Attribute der Kundenadressen](./assets/attributes-customer-address.png){width="700" zoomable="yes"}

## Schritt 1: Ausfüllen der Attributeigenschaften

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer Address]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add New Attribute]**.

   ![Kundenattributeigenschaften](./assets/attribute-customer-address-new.png){width="600" zoomable="yes"}

1. Im **[!UICONTROL Attribute Properties]** führen Sie folgende Schritte aus:

   - Geben Sie einen **[!UICONTROL Default Label]** , das das Attribut während der Dateneingabe angibt.

   - Geben Sie eine **[!UICONTROL Attribute Code]** , das das Attribut im System angibt.

     Der Attributcode muss mit einem Buchstaben beginnen und kann eine beliebige Kombination aus Kleinbuchstaben (a-z) und Zahlen (0-9) enthalten. Der Code muss weniger als 30 Zeichen lang sein und darf keine Sonderzeichen oder Leerzeichen enthalten. Das Unterstrichzeichen (_) kann zur Angabe eines Leerzeichens verwendet werden.

     >[!TIP]
     >
     >**_Tastaturbefehl:_** Um nur die erforderlichen Felder auszufüllen, scrollen Sie nach unten zu [!UICONTROL Storefront Properties], geben Sie die [!UICONTROL Sort Order]und speichern Sie.

1. Um den Typ des Eingabeditors zu bestimmen, der für die Dateneingabe verwendet wird, legen Sie **[!UICONTROL Input Type]** auf einen der folgenden Werte zu:

   - `Text Field` - Ein einzeiliges Textfeld.
   - `Text Area` - Ein mehrzeiliger Textbereich.
   - `Multiple Line` - Erstellt mehrere Textzeilen für das Attribut, ähnlich einer mehrzeiligen Straßenadresse. Die Anzahl der einzelnen Dateneintragszeilen kann zwischen 2 und 20 liegen. Verwenden Sie die `Default Value` , um den Anfangswert des Felds anzugeben.
   - `Date` - Zeigt ein Datumsfeld mit einem Popup-Kalender an. Zusätzliche Eigenschaften: Verwenden Sie `Default Value` , um den Anfangswert des Felds anzugeben. <br/>Verwendung `Minimal Value` um das früheste Datum anzugeben, das eingegeben werden kann.  Verwendung `Maximum Value` um das Datum anzugeben, das zuletzt eingegeben werden kann.
   - `Dropdown` - Eine Dropdownliste, in der nur ein auszuwählender Wert zulässig ist.
   - `Multiple Select` - Eine Dropdown-Liste, in der mehrere Werte ausgewählt werden können.
   - `Yes/No` - Ein Feld, das nur eine Auswahl an `Yes` oder `No` -Werte.
   - `File (attachment)` - Ein Feld, in das eine Datei hochgeladen und dem Kundenattribut als Anhang zugeordnet werden kann.
   - `Image File` - Ein Feld, in das ein Bild in die Galerie hochgeladen und dem Kundenattribut zugeordnet werden kann.

1. Wenn der Kunde einen Wert in das Feld eingeben muss, legen Sie **[!UICONTROL Values Required]** nach `Yes`.

1. Um dem Feld einen Anfangswert zuzuweisen, geben Sie einen **[!UICONTROL Default Value]**.

1. Um die Genauigkeit der in das Feld eingegebenen Daten vor dem Speichern des Datensatzes zu überprüfen, legen Sie **[!UICONTROL Input Validation]** zum Datentyp hinzu, der im Feld zulässig sein soll. Die verfügbaren Werte hängen von der _[!UICONTROL Input Type]_angegeben.

   - `None` - Das Feld hat während der Dateneingabe keine Eingabevalidierung.
   - `Alphanumeric` - Akzeptiert eine beliebige Kombination von Zahlen (0-9) und Buchstaben (a-z, A-Z) während der Dateneingabe. Informationen zum Einschließen von Sonderzeichen finden Sie unter [!UICONTROL Escape HTML Entities] im nächsten Schritt.
   - `Alphanumeric with Space` - Akzeptiert alle Kombinationen aus Zahlen (0-9), alphabetischen Zeichen (a-z, A-Z) und Leerzeichen während der Dateneingabe.
   - `Numeric Only` - Akzeptiert nur Zahlen (0-9) während der Dateneingabe.
   - `Alpha Only` - Akzeptiert während der Dateneingabe nur Buchstaben (a-z, A-Z).
   - `URL` - Akzeptiert nur eine URL während der Dateneingabe.
   - `Email` - Akzeptiert nur eine E-Mail-Adresse während der Dateneingabe.
   - `Length Only` - Validiert die Eingabe anhand der Länge der in das Feld eingegebenen Daten.

1. Um einen Vorverarbeitungsfilter auf Werte anzuwenden, die in ein Textfeld, einen Textbereich oder einen mehrzeiligen Eingabetyp eingegeben werden, legen Sie **[!UICONTROL Input/Output Filter]** auf einen der folgenden Werte zu:

   - `None` - Wendet keinen Filter auf den in das Feld eingegebenen Text an.
   - `Strip HTML Tags` - Entfernt HTML-Tags aus dem Text. Dieser Filter kann beim Bereinigen von Daten helfen, die aus einer anderen Quelle, die HTML-Tags enthält, in ein Feld eingefügt werden.
   - `Escape  HTML Entities`  - Konvertiert die im Text gefundenen Sonderzeichen in eine gültige HTML-Escape-Sequenz, z. B. `&;`. Escape-Sequenzen sind zwischen einem kaufmännischen Und und einem Semikolon umschlossen und werden häufig für typografische Anführungszeichen, Copyright- und Markenzeichensymbole verwendet. Escape-Sequenzen werden auch verwendet, um Zeichen wie das Kleiner als (`<`) und größer als (`>`) und das kaufmännische Und-Zeichen, die auch im Code verwendet werden. Dieser Filter kann dazu beitragen, Sonderzeichen zu bereinigen, die manchmal aus Textverarbeitungen in Datenbankfelder eingefügt werden.

1. Füllen Sie die Kundenraster- und Segmenteigenschaften aus:

   - Um die Spalte in das Kundenraster einbeziehen zu können, legen Sie **[!UICONTROL Add to Column Options]** nach `Yes`.

   - Um das Kundenraster nach diesem Attribut zu filtern, legen Sie **[!UICONTROL Use in Filter Options]** nach `Yes`.

   - Um das Kundenraster nach Textattribut mit unterschiedlichen Filterübereinstimmungsbedingungen zu filtern, legen Sie **[!UICONTROL Grid Filter Condition Type]** nach `Partial Match`, `Prefix Match`oder `Full Match`. Sie wirkt sich nicht auf die _Suche nach Keyword_ -Feld für das Raster.

   - Um das Kundenraster nach diesem Attribut zu durchsuchen, legen Sie **[!UICONTROL Use in Search Options]** nach `Yes`.

   - So stellen Sie dieses Attribut zur Verfügung [Kundensegmente](customer-segments.md), set **[!UICONTROL Use in Customer Segment]** nach `Yes`.

## Schritt 2: Ausfüllen der Storefront-Eigenschaften

1. Scrollen Sie nach unten zum **[!UICONTROL Storefront Properties]** Abschnitt.

   ![Attribute der Kundenadresse - Storefront-Eigenschaften](./assets/attribute-customer-address-storefront-properties.png){width="600" zoomable="yes"}

1. Um das Attribut für Kunden sichtbar zu machen, legen Sie **[!UICONTROL Show on Storefront]** nach `Yes`.

1. Geben Sie im Feld **[!UICONTROL Sort Order]** -Feld, das die Reihenfolge des Erscheinungsbilds bestimmt, wenn es mit anderen Attributen aufgeführt wird.

1. Satz **[!UICONTROL Forms to Use]** zu jedem Formular hinzu, das das Attribut enthalten soll.

   Um beide Optionen auszuwählen, halten Sie beim Klicken auf die einzelnen Formulare die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt.

   - [Registrierung von Kundenadressen](account-create.md)
   - [Kundenkontoadresse](account-dashboard-address-book.md)

## Schritt 3: Titel ausfüllen und speichern

1. Wählen Sie im Bedienfeld auf der linken Seite **[!UICONTROL Manage Labels/Options]**.

1. under **[!UICONTROL Manage Titles]**, geben Sie einen Titel ein, um das Attribut für jede [Store-Ansicht](../getting-started/websites-stores-views.md).

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Attribute]**.

   ![Attribute der Kundenadresse - Beschriftungen/Optionen](./assets/attribute-customer-address-new-manage-label-options.png){width="600" zoomable="yes"}

## Feldbeschreibungen

### [!UICONTROL Attribute Properties]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Default Label] | Die Standardbeschriftung, mit der das Attribut in der Admin- und Storefront identifiziert wird. |
| [!UICONTROL Attribute Code] | Ein eindeutiger Code, der das Attribut im System identifiziert. Der Code kann bis zu 21 Zeichen lang sein und darf keine Leerzeichen oder Sonderzeichen enthalten. Anstelle eines Leerzeichens kann das Unterstrichsymbol verwendet werden. |
| [!UICONTROL Input Type] | Bestimmt die [Eingabefeld](../catalog/attributes-input-types.md) wird für die Dateneingabe verwendet. Optionen: <br/>**`Text Field`**- Ein einzeiliges Textfeld.<br/>**`Text Area`** - Ein mehrzeiliger Textbereich. <br/>**`Multiple Line`**- Erstellt mehrere Textzeilen für das Attribut, ähnlich einer mehrzeiligen Straßenadresse. Die Anzahl der einzelnen Dateneintragszeilen kann zwischen 2 und 20 liegen.<br/>**`Date`** - Zeigt ein Datumsfeld mit einem Popup-Kalender an.<br/>**`Dropdown`**- Eine Dropdownliste, in der nur ein auszuwählender Wert zulässig ist.<br/>**`Multiple Select`** - Eine Dropdown-Liste, in der mehrere Werte ausgewählt werden können. <br/>**`Yes/No`**- Ein Feld, das nur eine Auswahl an `Yes` oder `No` -Werte.<br/>**`File (attachment)`** - Ein Feld, in das eine Datei hochgeladen und dem Kundenattribut als Anhang zugeordnet werden kann. <br/>**`Image File`**- Ein Feld, in das ein Bild in die Galerie hochgeladen und dem Kundenattribut zugeordnet werden kann. |
| [!UICONTROL Values Required] | Bestimmt, ob ein Wert in das Feld eingegeben werden muss. Optionen: `Yes` / `No` |
| [!UICONTROL Default Value] | Gibt den Anfangswert des Attributs an. |
| [!UICONTROL Input Validation] | Die Auswahl der Optionen wird vom Eingabetyp bestimmt. Optionen: <br/>**`None`**- Das Feld hat während der Dateneingabe keine Eingabevalidierung.<br/>**`Alphanumeric`** - Akzeptiert eine beliebige Kombination von Zahlen (0-9) und Buchstaben (a-z, A-Z) während der Dateneingabe. <br/>**`Alphanumeric with Space`**- Ermöglicht es, dass die Räume in der Straßenadresse den maximalen Längenanforderungen des Beförderers entsprechen. Beim Checkout kann der Kunde eine beliebige Kombination aus Zahlen (0-9), Buchstaben (a-z, A-Z) und Leerzeichen in die Straßenadresse des Empfängers und Absenders eingeben. Alle zusätzlichen Leerzeichen werden beim Speichern der Adresse abgeschnitten.<br/>**`Numeric Only`** - Akzeptiert nur Zahlen (0-9) während der Dateneingabe. <br/>**`Alpha Only`**- Akzeptiert während der Dateneingabe nur Buchstaben (a-z, A-Z).<br/>** URL **- Akzeptiert nur eine URL während der Dateneingabe.<br/>**`Email`** - Akzeptiert nur eine E-Mail-Adresse während der Dateneingabe. <br/>**`Length Only`**- Validiert die Eingabe anhand der Länge der in das Feld eingegebenen Daten. |
| [!UICONTROL Input/Output Filter] | Wendet einen Vorverarbeitungsfilter auf Werte an, die in ein Textfeld, einen Textbereich oder einen mehrzeiligen Eingabetyp eingegeben wurden, bevor der Datensatz gespeichert wird. Optionen: <br/>**`None`**- Wendet keinen Filter auf den in das Feld eingegebenen Text an.<br/>**`Strip HTML Tags`** - Entfernt HTML-Tags aus dem Text. Dieser Filter kann beim Bereinigen von Daten helfen, die aus einer anderen Quelle, die HTML-Tags enthält, in ein Feld eingefügt werden. <br/>**`Escape HTML Entities`**- Konvertiert die im Text gefundenen Sonderzeichen in eine gültige HTML-Escape-Sequenz, z. B. `amp;`. Escape-Sequenzen sind zwischen einem kaufmännischen Und und einem Semikolon eingeschlossen und werden häufig für typografische Anführungszeichen, Copyright-Symbole und Markenzeichensymbole verwendet. Escape-Sequenzen werden auch verwendet, um Zeichen wie das Kleiner als (`<`) und größer als (`>`) und das kaufmännische Und-Zeichen, die auch im Code verwendet werden. Dieser Filter kann dazu beitragen, Sonderzeichen zu bereinigen, die manchmal aus Textverarbeitungen in Datenbankfelder eingefügt werden. |
| [!UICONTROL Add to Column Options] | Gibt an, ob das Attribut als Spalte im [Kunden](./customers-all.md) Gitter. Optionen: `Yes` / `No` |
| Verwenden in Filteroptionen | Gibt an, ob das Attribut als Filter für Suchvorgänge aus dem Raster verwendet werden kann. Optionen: `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | Gibt Filterübereinstimmungsbedingungen für Attribute in Suchvorgängen aus dem Raster an. Sie wirkt sich nicht auf die _[!UICONTROL Search by keyword]_-Feld für das Raster. Optionen: `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | Gibt an, ob der Attributwert bei Suchvorgängen als Keyword verwendet werden kann. Optionen: `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | Bestimmt, ob das Attribut in [Kundensegment](./customer-segments.md) Bedingungen. Optionen: `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Show on Storefront] | Bestimmt, ob das Attribut als Feld in den Kundeninformationen in der Storefront angezeigt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Sort Order] | Gibt die Sortierreihenfolge dieses Attributs in Bezug auf andere Kundenattribute an. Die Sortierreihenfolge bestimmt die Reihenfolge, in der Felder während der Dateneingabe bei Verwendung der Tastaturnavigation den Fokus erhalten. |
| [!UICONTROL Forms to Use in] | Bestimmt die Seiten mit Dateneingabeformularen, auf denen das Attribut angezeigt wird. Optionen: <br/>[`Customer Address Registration`](account-create.md) <br/>[`Customer Account Address`](account-dashboard-address-book.md) |
