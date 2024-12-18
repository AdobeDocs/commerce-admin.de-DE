---
title: Kundenattribut-Eigenschaften
description: Erfahren Sie, wie Sie Kundenattributeigenschaften konfigurieren.
exl-id: d464f846-6a1f-43bd-876a-6834605ef794
feature: Customers, Configuration
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '1796'
ht-degree: 0%

---

# Kundenattribut-Eigenschaften

{{ee-feature}}

Kundenattribute liefern die Informationen, die zur Unterstützung der Auftrags-, Erfüllungs- und Kundenverwaltungsprozesse erforderlich sind. Da Ihr Unternehmen eindeutig ist, benötigen Sie möglicherweise Felder zusätzlich zu den vom System bereitgestellten Standardelementen. Sie können den Abschnitten Kontoinformationen, Adressbuch und Rechnungsinformationen des Kontos des Kunden benutzerdefinierte Attribute hinzufügen. Kunden[Adressattribute](address-attributes.md) können auch im Abschnitt _Rechnungsinformationen_ während des Checkouts oder bei der Registrierung für ein Konto verwendet werden.

![Kundenattribute](./assets/attributes-customer.png){width="700" zoomable="yes"}

## Schritt 1: Vervollständigen Sie die Attributeigenschaften

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add New Attribute]**.

   ![Kundenattribut-Eigenschaften](./assets/attribute-customer-new.png){width="600" zoomable="yes"}

1. Gehen Sie im Abschnitt **[!UICONTROL Attribute Properties]** wie folgt vor:

   - Geben Sie einen **[!UICONTROL Default Label]** ein, der das Attribut während der Dateneingabe identifiziert.

   - Geben Sie eine **[!UICONTROL Attribute Code]** ein, die das Attribut innerhalb des Systems identifiziert.

   Der Attributcode muss mit einem Buchstaben beginnen und kann eine beliebige Kombination aus Kleinbuchstaben (a-z) und Zahlen (0-9) enthalten. Der Code muss weniger als 30 Zeichen lang sein und darf keine Sonderzeichen oder Leerzeichen enthalten. Der Unterstrich (`_`) kann zur Angabe eines Leerzeichens verwendet werden.

   >[!TIP]
   >
   >**Tastaturbefehl** Um nur die erforderlichen Felder auszufüllen, scrollen Sie nach unten zu _[!UICONTROL Storefront Properties]_, geben Sie den_[!UICONTROL Sort Order]_ ein und speichern Sie.

1. Vervollständigen Sie die Dateneingabeeigenschaften:

   - Um den Typ des Eingabedialogs zu bestimmen, der für die Dateneingabe verwendet wird, legen Sie **[!UICONTROL Input Type]** auf einen der folgenden Werte fest:

     | Typ | Beschreibung |
     |----|-----------|
     | `Text Field` | Ein einzeiliges Textfeld. |
     | `Text Area` | Ein mehrzeiliges Eingabefeld zum Eingeben von Textabsätzen, z. B. eine Produktbeschreibung. Sie können den WYSIWYG-Editor verwenden, um den Text mit HTML-Tags zu formatieren, oder die Tags direkt in den Text eingeben. |
     | `Multiple Line` | Erstellt mehrere Textzeilen für das Attribut, ähnlich einer mehrzeiligen Straßenadresse. Die Anzahl der separaten Dateneintragszeilen kann von zwei bis 20 betragen. Verwenden Sie die `Default Value` , um den Anfangswert des Felds anzugeben. |
     | `Date` | Zeigt einen Datumswert im bevorzugten Datumsformat und in der bevorzugten Zeitzone an. Datumswerte können aus einer Liste oder einem Kalender ausgewählt werden ( ![Kalendersymbol](../assets/icon-calendar.png) ). <br/><br/>**_Hinweis _**Je nach Systemkonfiguration können_Admin _-Benutzer Datumsangaben direkt in ein Feld eingeben oder ein Datum aus dem Kalender oder der Liste auswählen. Weitere Informationen zum Angeben von Datums- und Uhrzeitwerten finden Sie unter [Optionen für Datum und Uhrzeit](../catalog/attributes-input-types.md#date-and-time-options). |
     | `Yes/No` | Zeigt eine Dropdown-Liste mit vordefinierten Optionen `Yes` und `No` an. |
     | `Dropdown` | Zeigt eine Dropdown-Liste mit Werten an, die nur eine einzige Auswahl akzeptieren. Der Dropdown-Eingabetyp ist eine Schlüsselkomponente von [konfigurierbaren Produkten](../catalog/product-create-configurable.md). |
     | `Multiple Select` | Eine Dropdown-Liste, die die Auswahl mehrerer Werte akzeptiert. |
     | `File (attachment)` | Ein Feld, mit dem eine Datei hochgeladen und mit dem Kundenattribut als Anlage verknüpft werden kann. |
     | `Image File` | Ein Feld, mit dem ein Bild in die Galerie hochgeladen und mit dem Kundenattribut verknüpft werden kann. |

   - Wenn der Kunde einen Wert in das Feld eingeben muss, setzen Sie **[!UICONTROL Values Required]** auf `Yes`.

   - Um dem Feld einen Anfangswert zuzuweisen, geben Sie einen **[!UICONTROL Default Value]** ein.

   - Um die Genauigkeit der in das Feld eingegebenen Daten zu überprüfen, bevor der Datensatz gespeichert wird, setzen Sie **[!UICONTROL Input Validation]** auf den Typ der Daten, die in dem Feld zulässig sein sollen. Die verfügbaren Werte hängen von der angegebenen [!UICONTROL Input Type] ab.

     | Wert | Beschreibung |
     |-----|-----------|
     | `None` | Das Feld hat bei der Dateneingabe keine Eingabevalidierung. |
     | `Alphanumeric` | Akzeptiert bei der Dateneingabe eine beliebige Kombination aus Zahlen (0-9) und alphabetischen Zeichen (a-z, A-Z). Informationen zum Einschließen von Sonderzeichen finden Sie unter _Escape-HTML-Entitäten_. |
     | `Alphanumeric with Space` | Akzeptiert eine beliebige Kombination von Zahlen (0-9), alphabetischen Zeichen (a-z, A-Z) und Leerzeichen bei der Dateneingabe. |
     | `Numeric Only` | Akzeptiert bei der Dateneingabe nur Zahlen (0-9). |
     | `Alpha Only` | Akzeptiert bei der Dateneingabe nur alphabetische Zeichen (a-z, A-Z). |
     | `URL` | Akzeptiert bei der Dateneingabe nur eine URL. |
     | `Email` | Akzeptiert bei der Dateneingabe nur eine E-Mail-Adresse. |
     | `Length Only` | Validiert die Eingabe auf Grundlage der Länge der in das Feld eingegebenen Daten. |

   - Um die Größe von Eingabetypen für Textfelder und Textbereiche zu begrenzen, geben Sie den **[!UICONTROL Minimum Text Length]** und die **[!UICONTROL Maximum Text Length]** ein.

   - Um einen Vorverarbeitungsfilter auf Werte anzuwenden, die in ein Textfeld, einen Textbereich oder einen mehrzeiligen Eingabetyp eingegeben werden, setzen Sie **[!UICONTROL Input/Output Filter]** auf einen der folgenden Werte:

     | Wert | Beschreibung |
     |-----|-----------|
     | `None` | Wendet keinen Filter auf Text an, der in das Feld eingegeben wird. |
     | `Strip HTML Tags` | Entfernt HTML-Tags aus dem Text. Dieser Filter kann dabei helfen, Daten zu bereinigen, die in ein Feld aus einer anderen Quelle eingefügt werden, die HTML-Tags enthält. |
     | `Escape  HTML Entities` | Konvertiert Sonderzeichen aus dem Text in eine gültige HTML-Escapesequenz, z. B. `&;`. Escape-Sequenzen sind zwischen einem kaufmännischen Und-Zeichen und einem Semikolon eingeschlossen und werden häufig für typografische Anführungszeichen, Copyright- und Markensymbole verwendet. Escape-Sequenzen werden auch verwendet, um Zeichen wie die Zeichen kleiner als (`<`) und größer als (`>`) sowie das kaufmännische Und-Zeichen zu identifizieren, die auch im Code verwendet werden. Dieser Filter kann dazu beitragen, Sonderzeichen zu bereinigen, die manchmal von Textverarbeitungsprogrammen in Datenbankfelder eingefügt werden. |

1. Vervollständigen Sie das Kundenraster und die Segmenteigenschaften:

   - Um die Spalte in das Raster Kunden einbeziehen zu können, legen Sie **[!UICONTROL Add to Column Options]** auf `Yes` fest.

   - Um das Kundenraster nach diesem Attribut zu filtern, setzen Sie **[!UICONTROL Use in Filter Options]** auf `Yes`.

   - Um das Kundenraster nach Texteigenschaften mit unterschiedlichen Filterzuordnungsbedingungen zu filtern, legen Sie **[!UICONTROL Grid Filter Condition Type]** auf `Partial Match`, `Prefix Match` oder `Full Match` fest. Das Feld _Nach Keyword suchen_ für das Raster ist davon nicht betroffen.

   - Um das Raster Kunden nach diesem Attribut zu durchsuchen, setzen Sie **[!UICONTROL Use in Search Options]** auf `Yes`.

   - Um dieses Attribut für „Kundensegmente[ verfügbar zu machen, ](customer-segments.md) Sie **[!UICONTROL Use in Customer Segment]** auf `Yes`.

## Schritt 2: Vervollständigen Sie die Eigenschaften der Storefront

1. Scrollen Sie nach unten zum Abschnitt **[!UICONTROL Storefront Properties]** .

   ![Kundenattribute - Storefront-Eigenschaften](./assets/attribute-customer-storefront-properties.png){width="600" zoomable="yes"}

1. Um das -Attribut für Kunden sichtbar zu machen, setzen Sie **[!UICONTROL Show on Storefront]** auf `Yes`.

1. Geben Sie eine Zahl in das Feld **[!UICONTROL Sort Order]** ein, die die Reihenfolge bestimmt, in der sie angezeigt wird, wenn sie mit anderen Attributen aufgelistet wird.

1. Legen Sie **[!UICONTROL Forms to Use]** auf jedes Formular fest, das das Attribut enthalten soll. Um mehrere Optionen auszuwählen, halten Sie die Strg -Taste gedrückt und klicken Sie auf die einzelnen Formulare.

   - [`Kundenregistrierung`](customer-sign-in.md)
   - [`Kundenkonto bearbeiten`](account-create.md)
   - [`Admin Checkout`](../stores-purchase/checkout-process.md)

## Schritt 3: Titel ausfüllen und speichern

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Manage Labels/Options]** aus.

1. Geben Sie unter **[!UICONTROL Manage Titles]** einen Titel ein, um das Attribut für jede [Store-Ansicht“ ](../getting-started/websites-stores-views.md).

1. Klicken Sie abschließend auf **[!UICONTROL Save Attribute]**.

   ![Kundenattribute - Beschriftungen/Optionen](./assets/attribute-customer-manage-label-options.png){width="600" zoomable="yes"}

## Feldbeschreibungen

### [!UICONTROL Attribute Properties]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Default Label] | Die Standardbeschriftung, die das Attribut in der Admin- und Storefront identifiziert. |
| [!UICONTROL Attribute Code] | Ein eindeutiger Code, der das Attribut im System identifiziert. Der Code kann bis zu 60 Zeichen lang sein und darf keine Leerzeichen oder Sonderzeichen enthalten. Das Unterstrichsymbol kann anstelle eines Leerzeichens verwendet werden. |
| [!UICONTROL Input Type] | Bestimmt das Eingabesteuerelement, das für die Dateneingabe verwendet wird. Optionen: <br/>**`Text Field`**: Ein einzeiliges Textfeld.<br/>**`Text Area`** : Ein mehrzeiliger Textbereich. <br/>**`Multiple Line`**- Erstellt mehrere Textzeilen für das Attribut, ähnlich einer mehrzeiligen Straßenadresse. Die Anzahl der separaten Dateneintragszeilen kann von 2 bis 20 betragen.<br/>**`Date`** : Zeigt ein Datumsfeld mit einem Popup-Kalender an.<br/>**`Dropdown`**- Eine Dropdown-Liste, die nur einen auszuwählenden Wert akzeptiert.<br/>**`Multiple Select`** : Eine Dropdown-Liste, in der mehrere Werte ausgewählt werden können. <br/>**`Yes/No`**: Ein Feld, das nur eine Auswahl aus `Yes` oder `No` Werten bietet.<br/>**`File (attachment)`** : Ein Feld, mit dem eine Datei hochgeladen und mit dem Kundenattribut als Anlage verknüpft werden kann. <br/>**`Image File`**: Ein Feld, mit dem ein Bild in die Galerie hochgeladen und mit dem Kundenattribut verknüpft werden kann. |
| [!UICONTROL Values Required] | Legt fest, ob ein Wert in das Feld eingegeben werden muss. Optionen: `Yes` / `No` |
| [!UICONTROL Default Value] | Gibt den Anfangswert des Attributs an. |
| [!UICONTROL Input Validation] | Die Auswahl der Optionen wird durch den Eingabetyp bestimmt. Optionen: <br/>**`None`**: Das Feld verfügt während der Dateneingabe über keine Eingabevalidierung.<br/>**`Alphanumeric`** - Akzeptiert eine beliebige Kombination von Zahlen (0-9) und alphabetischen Zeichen (a-z, A-Z) bei der Dateneingabe. <br/>**`Alphanumeric with Space`**- Ermöglicht Räumen in der Straße Adresse, um die Anforderungen der maximalen Länge des Trägers zu erfüllen. Während des Checkouts kann der Kunde eine beliebige Kombination aus Zahlen (0-9), alphabetischen Zeichen (a-z, A-Z) und Leerzeichen in die Straße des Empfängers und des Absenders eingeben. Zusätzliche Leerzeichen werden beim Speichern der Adresse entfernt.<br/>**`Numeric Only`** - Akzeptiert bei der Dateneingabe nur Zahlen (0-9). <br/>**`Alpha Only`**- Akzeptiert bei der Dateneingabe nur alphabetische Zeichen (a-z, A-Z).<br/>**`URL`** - Akzeptiert bei der Dateneingabe nur eine URL. <br/>**`Email`**- Akzeptiert bei der Dateneingabe nur eine E-Mail-Adresse.<br/>**`Length Only`**: Überprüft die Eingabe anhand der Länge der in das Feld eingegebenen Daten. |
| [!UICONTROL Input/Output Filter] | Wendet einen Vorverarbeitungsfilter auf Werte an, die in ein Textfeld, einen Textbereich oder einen mehrzeiligen Eingabetyp eingegeben wurden, bevor der Datensatz gespeichert wird. Optionen: <br/>**`None`**- Wendet keinen Filter auf Text an, der in das Feld eingegeben wird.<br/>**`Strip HTML Tags`** - Entfernt HTML-Tags aus dem Text. Dieser Filter kann dabei helfen, Daten zu bereinigen, die in ein Feld aus einer anderen Quelle eingefügt werden, die HTML-Tags enthält. <br/>**`Escape HTML Entities`**- Konvertiert Sonderzeichen aus dem Text in eine gültige HTML-Escapesequenz, z. B. `amp;`. Escape-Sequenzen sind zwischen einem kaufmännischen Und-Zeichen und einem Semikolon eingeschlossen und werden häufig für typografische Anführungszeichen, Urheberrechtssymbole und Markensymbole verwendet. Escape-Sequenzen werden auch verwendet, um Zeichen wie die Zeichen kleiner als (`<`) und größer als (`>`) sowie das kaufmännische Und-Zeichen zu identifizieren, die auch im Code verwendet werden. Dieser Filter kann dazu beitragen, Sonderzeichen zu bereinigen, die manchmal von Textverarbeitungsprogrammen in Datenbankfelder eingefügt werden. |
| [!UICONTROL Add to Column Options] | Gibt an, ob das Attribut als Spalte im Raster [Kunden](customers-all.md) enthalten ist. Optionen: `Yes` / `No` |
| [!UICONTROL Use in Filter Options] | Gibt an, ob das Attribut als Filter für Suchvorgänge über das Raster verwendet werden kann. Optionen: `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | Gibt die Filterzuordnungsbedingungen für Attribute für Suchvorgänge im Raster an. Das Feld _Nach Keyword suchen_ für das Raster ist davon nicht betroffen. Optionen: `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | Gibt an, ob der Attributwert bei Suchvorgängen als Keyword verwendet werden kann. Optionen: `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | Bestimmt, ob das Attribut in Bedingungen [Kundensegment](customer-segments.md) enthalten ist. Optionen: `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Show on Storefront] | Bestimmt, ob das Attribut als Feld in den Kundeninformationen in der Storefront angezeigt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Sort Order] | Gibt die Sortierreihenfolge dieses Attributs in Bezug auf andere Kundenattribute an. Die Sortierreihenfolge bestimmt die Reihenfolge, in der Felder bei der Dateneingabe unter Verwendung der Tastaturnavigation den Fokus erhalten. |
| [!UICONTROL Forms to Use in] | Bestimmt die Seiten mit Dateneingabeformularen, auf denen das Attribut angezeigt wird. Optionen: <br/>[`Customer Registration`](account-dashboard-account-information.md) <br/>[`Customer Account Edit`](account-create.md) <br/>[`Admin Checkout`](../stores-purchase/checkout-process.md) |

## Standard-Kundenattribute

| Attributcode | Beschreibung |
| --------------- | ------------------ |
| `created_at` | Das Datum der Erstellung des Kundenkontos. |
| `updated_at` | Das Datum der letzten Aktualisierung des Kundenkontos. |
| `website_id` | Die Website-ID der Site, auf der das Kundenkonto erstellt wurde. |
| `store_id` | Die Store-ID der Site, auf der das Kundenkonto erstellt wurde. |
| `created_in` | Die Store-Ansicht, in der das Konto erstellt wurde. |
| `group_id` | Die ID der Kundengruppe, der der Kunde zugewiesen ist. |
| `disable_auto_group_change` | Legt fest, ob Kundengruppen bei der Validierung der [-ID dynamisch zugewiesen ](../stores-purchase/vat.md#configure-vat-id-validation) können. |
| `prefix` | Jedes Präfix, das mit dem Kundennamen verwendet wird (z. B. Herr, Frau oder Dr.). |
| `firstname` | Der Vorname des Kunden. |
| `middlename` | Der zweite Vorname oder zweite Vorname des Kunden. |
| `lastname` | Der Nachname des Kunden. |
| `suffix` | Jedes Suffix, das mit dem Kundennamen verwendet wird. (wie Jr., Sr. oder Esquire) |
| `email` | Die E-Mail-Adresse des Kunden. |
| `dob` | Das Geburtsdatum des Kunden.  <br><br>**_Wichtig:_**Halten Sie sich im Einklang mit den aktuellen Best Practices für Sicherheit und Datenschutz vor potenziellen Rechts- und Sicherheitsrisiken, die mit der Speicherung des vollständigen Geburtsdatums der Kundinnen und Kunden (Monat, Tag, Jahr) mit anderen persönlichen Kennungen verbunden sind. Es wird empfohlen, die Speicherung der vollständigen Geburtsdaten von Kundinnen und Kunden zu begrenzen und alternativ ein Kundenjahr zu verwenden. |
| `taxvat` | Die Umsatzsteuer-ID (MwSt.), die dem Kunden zugewiesen wird. Die Standardbeschriftung dieses Attributs ist `VAT Number`. Das Feld MwSt.-Nummer ist immer in allen Versand- und Rechnungskundenadressen vorhanden, wenn es von der Administratorseite aus angezeigt wird, es ist jedoch kein Pflichtfeld. |
| `gender` | Das Geschlecht des Kunden. |

## Demo der Kundenattribute

Sehen Sie sich dieses Video an, um zu demonstrieren, wie Sie Kundenattribute erstellen:

>[!VIDEO](https://video.tv.adobe.com/v/343661?quality=12&learn=on)
