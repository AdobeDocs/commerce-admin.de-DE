---
title: Kundenadressattribute
description: Erfahren Sie mehr über die Kundenadressenattribute und wie Sie diese Attributeigenschaften konfigurieren.
exl-id: 637a0f81-4d8f-40cb-a1b6-537229b2ce5b
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1495'
ht-degree: 0%

---

# Kundenadressattribute

{{ee-feature}}

Das Kundenadressenattribut bestimmt die Eigenschaften von Straßenadressen, die vom Konto des Kunden oder [Checkout](account-dashboard-address-book.md) in das [Adressbuch](../stores-purchase/checkout-process.md) eingegeben werden.

Benutzerdefinierte Adressattribute können eingerichtet werden, um zusätzliche Informationen bereitzustellen, z. B. eine optionale E-Mail-Adresse, ein Skype-Konto, eine alternative Telefonnummer, ein Gebäude oder ein Land. Das benutzerdefinierte Attribut kann dann in die [Adressvorlage“ integriert &#x200B;](address-templates.md), die zur Erstellung von Verkaufsdokumenten verwendet wird. Der Prozess zum Erstellen eines benutzerdefinierten Adressenattributs ist fast identisch mit dem Erstellen eines [Kundenattributs](attribute-properties.md).

Kundenadressattribute werden in den folgenden Formen verwendet:

- [Registrierung der Kundenadresse](account-create.md)
- [Adresse des Kundenkontos](account-dashboard-address-book.md)

![Admin - Kundenadressattribute](./assets/attributes-customer-address.png){width="700" zoomable="yes"}

## Schritt 1: Vervollständigen Sie die Attributeigenschaften

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer Address]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add New Attribute]**.

   ![Kundenattribut-Eigenschaften](./assets/attribute-customer-address-new.png){width="600" zoomable="yes"}

1. Gehen Sie im Abschnitt **[!UICONTROL Attribute Properties]** wie folgt vor:

   - Geben Sie einen **[!UICONTROL Default Label]** ein, der das Attribut während der Dateneingabe identifiziert.

   - Geben Sie eine **[!UICONTROL Attribute Code]** ein, die das Attribut innerhalb des Systems identifiziert.

     Der Attributcode muss mit einem Buchstaben beginnen und kann eine beliebige Kombination aus Kleinbuchstaben (a-z) und Zahlen (0-9) enthalten. Der Code muss weniger als 30 Zeichen lang sein und darf keine Sonderzeichen oder Leerzeichen enthalten. Der Unterstrich (_) kann zur Angabe eines Leerzeichens verwendet werden.

     >[!TIP]
     >
     >**_Tastaturbefehl_** Um nur die erforderlichen Felder auszufüllen, scrollen Sie nach unten zu [!UICONTROL Storefront Properties], geben Sie den [!UICONTROL Sort Order] ein und speichern Sie.

1. Um den Typ des Eingabedialogs zu bestimmen, der für die Dateneingabe verwendet wird, legen Sie **[!UICONTROL Input Type]** auf einen der folgenden Werte fest:

   - `Text Field`: Ein einzeiliges Textfeld.
   - `Text Area` : Ein mehrzeiliger Textbereich.
   - `Multiple Line` - Erstellt mehrere Textzeilen für das Attribut, ähnlich einer mehrzeiligen Straßenadresse. Die Anzahl der separaten Dateneintragszeilen kann von 2 bis 20 betragen. Verwenden Sie die `Default Value` , um den Anfangswert des Felds anzugeben.
   - `Date` : Zeigt ein Datumsfeld mit einem Popup-Kalender an. Zusätzliche Eigenschaften: Verwenden Sie `Default Value`, um den Anfangswert des Felds anzugeben. <br/>Verwenden Sie `Minimal Value`, um das früheste Datum anzugeben, das eingegeben werden kann.  Verwenden Sie `Maximum Value`, um das Datum anzugeben, das zuletzt eingegeben werden kann.
   - `Dropdown` - Eine Dropdown-Liste, die nur einen auszuwählenden Wert akzeptiert.
   - `Multiple Select` : Eine Dropdown-Liste, in der mehrere Werte ausgewählt werden können.
   - `Yes/No` : Ein Feld, das nur eine Auswahl aus `Yes` oder `No` Werten bietet.
   - `File (attachment)` : Ein Feld, mit dem eine Datei hochgeladen und mit dem Kundenattribut als Anlage verknüpft werden kann.
   - `Image File` : Ein Feld, mit dem ein Bild in die Galerie hochgeladen und mit dem Kundenattribut verknüpft werden kann.

1. Wenn der Kunde einen Wert in das Feld eingeben muss, setzen Sie **[!UICONTROL Values Required]** auf `Yes`.

1. Um dem Feld einen Anfangswert zuzuweisen, geben Sie einen **[!UICONTROL Default Value]** ein.

1. Um die Genauigkeit der in das Feld eingegebenen Daten zu überprüfen, bevor der Datensatz gespeichert wird, setzen Sie **[!UICONTROL Input Validation]** auf den Typ der Daten, die in dem Feld zulässig sein sollen. Die verfügbaren Werte hängen von der angegebenen _[!UICONTROL Input Type]_&#x200B;ab.

   - `None` - Das Feld hat bei der Dateneingabe keine Eingabevalidierung.
   - `Alphanumeric` - Akzeptiert eine beliebige Kombination von Zahlen (0-9) und alphabetischen Zeichen (a-z, A-Z) bei der Dateneingabe. Informationen zum Einschließen von Sonderzeichen finden Sie unter [!UICONTROL Escape HTML Entities] im nächsten Schritt.
   - `Alphanumeric with Space` - Akzeptiert eine beliebige Kombination von Zahlen (0-9), alphabetischen Zeichen (a-z, A-Z) und Leerzeichen bei der Dateneingabe.
   - `Numeric Only` - Akzeptiert bei der Dateneingabe nur Zahlen (0-9).
   - `Alpha Only` - Akzeptiert bei der Dateneingabe nur alphabetische Zeichen (a-z, A-Z).
   - `URL` - Akzeptiert bei der Dateneingabe nur eine URL.
   - `Email` - Akzeptiert bei der Dateneingabe nur eine E-Mail-Adresse.
   - `Length Only`: Überprüft die Eingabe anhand der Länge der in das Feld eingegebenen Daten.

1. Um einen Vorverarbeitungsfilter auf Werte anzuwenden, die in ein Textfeld, einen Textbereich oder einen mehrzeiligen Eingabetyp eingegeben werden, setzen Sie **[!UICONTROL Input/Output Filter]** auf einen der folgenden Werte:

   - `None` - Wendet keinen Filter auf Text an, der in das Feld eingegeben wird.
   - `Strip HTML Tags` - Entfernt HTML-Tags aus dem Text. Dieser Filter kann dabei helfen, Daten zu bereinigen, die in ein Feld aus einer anderen Quelle eingefügt werden, die HTML-Tags enthält.
   - `Escape  HTML Entities` - Konvertiert Sonderzeichen aus dem Text in eine gültige HTML-Escapesequenz, z. B. `&;`. Escape-Sequenzen sind zwischen einem kaufmännischen Und-Zeichen und einem Semikolon eingeschlossen und werden häufig für typografische Anführungszeichen, Copyright- und Markensymbole verwendet. Escape-Sequenzen werden auch verwendet, um Zeichen wie die Zeichen kleiner als (`<`) und größer als (`>`) sowie das kaufmännische Und-Zeichen zu identifizieren, die auch im Code verwendet werden. Dieser Filter kann dazu beitragen, Sonderzeichen zu bereinigen, die manchmal von Textverarbeitungsprogrammen in Datenbankfelder eingefügt werden.

1. Vervollständigen Sie das Kundenraster und die Segmenteigenschaften:

   - Um die Spalte in das Raster Kunden einbeziehen zu können, legen Sie **[!UICONTROL Add to Column Options]** auf `Yes` fest.

   - Um das Kundenraster nach diesem Attribut zu filtern, setzen Sie **[!UICONTROL Use in Filter Options]** auf `Yes`.

   - Um das Kundenraster nach Texteigenschaften mit unterschiedlichen Filterzuordnungsbedingungen zu filtern, legen Sie **[!UICONTROL Grid Filter Condition Type]** auf `Partial Match`, `Prefix Match` oder `Full Match` fest. Das Feld _Nach Keyword suchen_ für das Raster ist davon nicht betroffen.

   - Um das Raster Kunden nach diesem Attribut zu durchsuchen, setzen Sie **[!UICONTROL Use in Search Options]** auf `Yes`.

   - Um dieses Attribut für „Kundensegmente[&#x200B; verfügbar zu machen, &#x200B;](customer-segments.md) Sie **[!UICONTROL Use in Customer Segment]** auf `Yes`.

## Schritt 2: Vervollständigen Sie die Eigenschaften der Storefront

1. Scrollen Sie nach unten zum Abschnitt **[!UICONTROL Storefront Properties]** .

   ![Kundenadressattribute - Storefront-Eigenschaften](./assets/attribute-customer-address-storefront-properties.png){width="600" zoomable="yes"}

1. Um das -Attribut für Kunden sichtbar zu machen, setzen Sie **[!UICONTROL Show on Storefront]** auf `Yes`.

1. Geben Sie eine Zahl in das Feld **[!UICONTROL Sort Order]** ein, die die Reihenfolge bestimmt, in der sie angezeigt wird, wenn sie mit anderen Attributen aufgelistet wird.

1. Legen Sie **[!UICONTROL Forms to Use]** auf jedes Formular fest, das das Attribut enthalten soll.

   Um beide Optionen auszuwählen, halten Sie die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt, während Sie auf die einzelnen Formulare klicken.

   - [Registrierung der Kundenadresse](account-create.md)
   - [Kundenkonto-Adresse](account-dashboard-address-book.md)

## Schritt 3: Titel ausfüllen und speichern

1. Wählen Sie im Bedienfeld auf der linken Seite **[!UICONTROL Manage Labels/Options]**.

1. Geben Sie unter **[!UICONTROL Manage Titles]** einen Titel ein, um das Attribut für jede [Store-Ansicht“ &#x200B;](../getting-started/websites-stores-views.md).

1. Klicken Sie abschließend auf **[!UICONTROL Save Attribute]**.

   ![Kundenadressattribute - Beschriftungen/Optionen](./assets/attribute-customer-address-new-manage-label-options.png){width="600" zoomable="yes"}

## Feldbeschreibungen

### [!UICONTROL Attribute Properties]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Default Label] | Die Standardbeschriftung, die das Attribut in der Admin- und Storefront identifiziert. |
| [!UICONTROL Attribute Code] | Ein eindeutiger Code, der das Attribut im System identifiziert. Der Code kann bis zu 21 Zeichen lang sein und darf keine Leerzeichen oder Sonderzeichen enthalten. Das Unterstrichsymbol kann anstelle eines Leerzeichens verwendet werden. |
| [!UICONTROL Input Type] | Bestimmt das [Eingabesteuerelement](../catalog/attributes-input-types.md) das für die Dateneingabe verwendet wird. Optionen: <br/>**`Text Field`**: Ein einzeiliges Textfeld.<br/>**`Text Area`** : Ein mehrzeiliger Textbereich. <br/>**`Multiple Line`**- Erstellt mehrere Textzeilen für das Attribut, ähnlich einer mehrzeiligen Straßenadresse. Die Anzahl der separaten Dateneintragszeilen kann von 2 bis 20 betragen.<br/>**`Date`** : Zeigt ein Datumsfeld mit einem Popup-Kalender an.<br/>**`Dropdown`**- Eine Dropdown-Liste, die nur einen auszuwählenden Wert akzeptiert.<br/>**`Multiple Select`** : Eine Dropdown-Liste, in der mehrere Werte ausgewählt werden können. <br/>**`Yes/No`**: Ein Feld, das nur eine Auswahl aus `Yes` oder `No` Werten bietet.<br/>**`File (attachment)`** : Ein Feld, mit dem eine Datei hochgeladen und mit dem Kundenattribut als Anlage verknüpft werden kann. <br/>**`Image File`**: Ein Feld, mit dem ein Bild in die Galerie hochgeladen und mit dem Kundenattribut verknüpft werden kann. |
| [!UICONTROL Values Required] | Legt fest, ob ein Wert in das Feld eingegeben werden muss. Optionen: `Yes` / `No` |
| [!UICONTROL Default Value] | Gibt den Anfangswert des Attributs an. |
| [!UICONTROL Input Validation] | Die Auswahl der Optionen wird durch den Eingabetyp bestimmt. Optionen: <br/>**`None`**: Das Feld verfügt während der Dateneingabe über keine Eingabevalidierung.<br/>**`Alphanumeric`** - Akzeptiert eine beliebige Kombination von Zahlen (0-9) und alphabetischen Zeichen (a-z, A-Z) bei der Dateneingabe. <br/>**`Alphanumeric with Space`**- Ermöglicht Räumen in der Straße Adresse, um die Anforderungen der maximalen Länge des Trägers zu erfüllen. Während des Checkouts kann der Kunde eine beliebige Kombination aus Zahlen (0-9), alphabetischen Zeichen (a-z, A-Z) und Leerzeichen in die Straße des Empfängers und des Absenders eingeben. Zusätzliche Leerzeichen werden beim Speichern der Adresse entfernt.<br/>**`Numeric Only`** - Akzeptiert bei der Dateneingabe nur Zahlen (0-9). <br/>**`Alpha Only`**- Akzeptiert bei der Dateneingabe nur alphabetische Zeichen (a-z, A-Z).<br/>**&#x200B; URL &#x200B;**- Akzeptiert bei der Dateneingabe nur eine URL.<br/>**`Email`** - Akzeptiert bei der Dateneingabe nur eine E-Mail-Adresse. <br/>**`Length Only`**: Überprüft die Eingabe anhand der Länge der in das Feld eingegebenen Daten. |
| [!UICONTROL Input/Output Filter] | Wendet einen Vorverarbeitungsfilter auf Werte an, die in ein Textfeld, einen Textbereich oder einen mehrzeiligen Eingabetyp eingegeben wurden, bevor der Datensatz gespeichert wird. Optionen: <br/>**`None`**- Wendet keinen Filter auf Text an, der in das Feld eingegeben wird.<br/>**`Strip HTML Tags`** - Entfernt HTML-Tags aus dem Text. Dieser Filter kann dabei helfen, Daten zu bereinigen, die in ein Feld aus einer anderen Quelle eingefügt werden, die HTML-Tags enthält. <br/>**`Escape HTML Entities`**- Konvertiert Sonderzeichen aus dem Text in eine gültige HTML-Escapesequenz, z. B. `amp;`. Escape-Sequenzen sind zwischen einem kaufmännischen Und-Zeichen und einem Semikolon eingeschlossen und werden häufig für typografische Anführungszeichen, Urheberrechtssymbole und Markensymbole verwendet. Escape-Sequenzen werden auch verwendet, um Zeichen wie die Zeichen kleiner als (`<`) und größer als (`>`) sowie das kaufmännische Und-Zeichen zu identifizieren, die auch im Code verwendet werden. Dieser Filter kann dazu beitragen, Sonderzeichen zu bereinigen, die manchmal von Textverarbeitungsprogrammen in Datenbankfelder eingefügt werden. |
| [!UICONTROL Add to Column Options] | Gibt an, ob das Attribut als Spalte im Raster [Kunden](./customers-all.md) enthalten ist. Optionen: `Yes` / `No` |
| Verwenden von in Filteroptionen | Gibt an, ob das Attribut als Filter für Suchvorgänge über das Raster verwendet werden kann. Optionen: `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | Gibt Filterzuordnungsbedingungen für Attribute in Suchvorgängen aus dem Raster an. Das _[!UICONTROL Search by keyword]_&#x200B;Feld für das Raster ist davon nicht betroffen. Optionen: `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | Gibt an, ob der Attributwert bei Suchvorgängen als Keyword verwendet werden kann. Optionen: `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | Bestimmt, ob das Attribut in Bedingungen [Kundensegment](./customer-segments.md) enthalten ist. Optionen: `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Show on Storefront] | Bestimmt, ob das Attribut als Feld in den Kundeninformationen in der Storefront angezeigt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Sort Order] | Gibt die Sortierreihenfolge dieses Attributs in Bezug auf andere Kundenattribute an. Die Sortierreihenfolge bestimmt die Reihenfolge, in der Felder bei der Dateneingabe unter Verwendung der Tastaturnavigation den Fokus erhalten. |
| [!UICONTROL Forms to Use in] | Bestimmt die Seiten mit Dateneingabeformularen, auf denen das Attribut angezeigt wird. Optionen: <br/>[`Customer Address Registration`](account-create.md) <br/>[`Customer Account Address`](account-dashboard-address-book.md) |
