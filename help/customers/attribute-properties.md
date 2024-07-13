---
title: Kundenattributeigenschaften
description: Erfahren Sie, wie Sie Kundenattributeigenschaften konfigurieren.
exl-id: d464f846-6a1f-43bd-876a-6834605ef794
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1796'
ht-degree: 0%

---

# Kundenattributeigenschaften

{{ee-feature}}

Kundenattribute liefern die Informationen, die zur Unterstützung der Auftrags-, Erfüllungs- und Kundenverwaltungsprozesse erforderlich sind. Da Ihr Unternehmen einzigartig ist, benötigen Sie möglicherweise neben den vom System bereitgestellten Standardelementen auch Felder. Sie können den Abschnitten Kontoinformationen, Adressbuch und Rechnungsinformationen des Kundenkontos benutzerdefinierte Attribute hinzufügen. Kundenadressen-Attribute [ ](address-attributes.md) können auch während des Checkouts oder bei der Registrierung von Gästen für ein Konto im Abschnitt _Rechnungsinformationen_ verwendet werden.

![Kundenattribute](./assets/attributes-customer.png){width="700" zoomable="yes"}

## Schritt 1: Ausfüllen der Attributeigenschaften

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add New Attribute]**.

   ![Kundenattributeigenschaften](./assets/attribute-customer-new.png){width="600" zoomable="yes"}

1. Gehen Sie im Abschnitt **[!UICONTROL Attribute Properties]** wie folgt vor:

   - Geben Sie einen **[!UICONTROL Default Label]** -Wert ein, der das Attribut während der Dateneingabe angibt.

   - Geben Sie einen **[!UICONTROL Attribute Code]** -Wert ein, der das Attribut im System angibt.

   Der Attributcode muss mit einem Buchstaben beginnen und kann eine beliebige Kombination aus Kleinbuchstaben (a-z) und Zahlen (0-9) enthalten. Der Code muss weniger als 30 Zeichen lang sein und darf keine Sonderzeichen oder Leerzeichen enthalten. Das Unterstrichzeichen (`_`) kann verwendet werden, um ein Leerzeichen anzugeben.

   >[!TIP]
   >
   >**Tastaturbefehl:** Um nur die erforderlichen Felder auszufüllen, scrollen Sie nach unten zu _[!UICONTROL Storefront Properties]_, geben Sie den Wert_[!UICONTROL Sort Order]_ ein und speichern Sie.

1. Füllen Sie die Dateneintragseigenschaften aus:

   - Um den Typ des Eingabeditors zu bestimmen, der für die Dateneingabe verwendet wird, setzen Sie **[!UICONTROL Input Type]** auf einen der folgenden Werte:

     | Typ | Beschreibung |
     |----|-----------|
     | `Text Field` | Ein einzeiliges Textfeld. |
     | `Text Area` | Ein mehrzeiliges Eingabefeld für die Eingabe von Textabsätzen, z. B. eine Produktbeschreibung. Sie können den WYSIWYG-Editor verwenden, um den Text mit HTML-Tags zu formatieren, oder die Tags direkt in den Text eingeben. |
     | `Multiple Line` | Erstellt mehrere Textzeilen für das Attribut, ähnlich einer mehrzeiligen Straßenadresse. Die Anzahl der einzelnen Dateneintragszeilen kann zwischen zwei und 20 liegen. Verwenden Sie den Wert `Default Value` , um den Anfangswert des Felds anzugeben. |
     | `Date` | Zeigt einen Datumswert im bevorzugten Datumsformat und in der bevorzugten Zeitzone an. Datumswerte können aus einer Liste oder einem Kalender ausgewählt werden ( ![Kalendersymbol](../assets/icon-calendar.png) ). <br/><br/>**_Hinweis:_**Je nach Systemkonfiguration können Benutzer mit_Administrator _Daten direkt in ein Feld eingeben oder ein Datum aus dem Kalender oder der Liste auswählen. Informationen zum Festlegen von Datums- und Uhrzeitwerten finden Sie unter [Datums- und Uhrzeitoptionen](../catalog/attributes-input-types.md#date-and-time-options). |
     | `Yes/No` | Zeigt eine Dropdownliste mit den vordefinierten Optionen `Yes` und `No` an. |
     | `Dropdown` | Zeigt eine Dropdown-Liste mit Werten an, die nur eine Auswahl zulassen. Der Dropdown-Eingabetyp ist eine Schlüsselkomponente von [konfigurierbaren Produkten](../catalog/product-create-configurable.md). |
     | `Multiple Select` | Eine Dropdown-Liste, in der mehrere Werte ausgewählt werden können. |
     | `File (attachment)` | Ein Feld, in das eine Datei hochgeladen und dem Kundenattribut als Anlage zugeordnet werden kann. |
     | `Image File` | Ein Feld, in das ein Bild in die Galerie hochgeladen und dem Kundenattribut zugeordnet werden kann. |

   - Wenn der Kunde einen Wert in das Feld eingeben muss, setzen Sie **[!UICONTROL Values Required]** auf `Yes`.

   - Um dem Feld einen Anfangswert zuzuweisen, geben Sie einen **[!UICONTROL Default Value]** ein.

   - Um die Genauigkeit der im Feld eingegebenen Daten vor dem Speichern des Datensatzes zu überprüfen, setzen Sie **[!UICONTROL Input Validation]** auf den Datentyp, der im Feld zulässig sein soll. Die verfügbaren Werte hängen von dem angegebenen [!UICONTROL Input Type] ab.

     | Wert | Beschreibung |
     |-----|-----------|
     | `None` | Das Feld hat während der Dateneingabe keine Eingabevalidierung. |
     | `Alphanumeric` | Akzeptiert eine beliebige Kombination von Zahlen (0-9) und alphabetischen Zeichen (a-z, A-Z) während der Dateneingabe. Informationen zum Einschließen von Sonderzeichen finden Sie unter _Escape-HTML-Entitäten_. |
     | `Alphanumeric with Space` | Akzeptiert eine beliebige Kombination von Zahlen (0-9), alphabetischen Zeichen (a-z, A-Z) und Leerzeichen während der Dateneingabe. |
     | `Numeric Only` | Akzeptiert nur Zahlen (0-9) während der Dateneingabe. |
     | `Alpha Only` | Akzeptiert während der Dateneingabe nur alphabetische Zeichen (a-z, A-Z). |
     | `URL` | Akzeptiert nur eine URL während der Dateneingabe. |
     | `Email` | Akzeptiert nur eine E-Mail-Adresse während der Dateneingabe. |
     | `Length Only` | Validiert die Eingabe anhand der Länge der in das Feld eingegebenen Daten. |

   - Geben Sie die Eingabetypen **[!UICONTROL Minimum Text Length]** und **[!UICONTROL Maximum Text Length]** ein, um die Größe von Textfeldern und Textbereichen zu begrenzen.

   - Um einen Vorverarbeitungsfilter auf Werte anzuwenden, die in ein Textfeld, einen Textbereich oder einen mehrzeiligen Eingabetyp eingegeben wurden, legen Sie **[!UICONTROL Input/Output Filter]** auf einen der folgenden Werte fest:

     | Wert | Beschreibung |
     |-----|-----------|
     | `None` | Es wird kein Filter auf den in das Feld eingegebenen Text angewendet. |
     | `Strip HTML Tags` | Entfernt HTML-Tags aus dem Text. Dieser Filter kann beim Bereinigen von Daten helfen, die aus einer anderen Quelle, die HTML-Tags enthält, in ein Feld eingefügt werden. |
     | `Escape  HTML Entities` | Konvertiert Sonderzeichen im Text in eine gültige HTML-Escape-Sequenz, z. B. `&;`. Escape-Sequenzen sind zwischen einem kaufmännischen Und und einem Semikolon umschlossen und werden häufig für typografische Anführungszeichen, Copyright- und Markenzeichensymbole verwendet. Escape-Sequenzen werden auch verwendet, um Zeichen wie die Symbole &quot;kleiner als&quot;(`<`) und &quot;größer als&quot;(`>`) sowie das kaufmännische Und-Zeichen zu identifizieren, die auch im Code verwendet werden. Dieser Filter kann dazu beitragen, Sonderzeichen zu bereinigen, die manchmal aus Textverarbeitungen in Datenbankfelder eingefügt werden. |

1. Füllen Sie die Kundenraster- und Segmenteigenschaften aus:

   - Um die Spalte in das Kundenraster einbeziehen zu können, setzen Sie **[!UICONTROL Add to Column Options]** auf `Yes`.

   - Um das Kundenraster nach diesem Attribut zu filtern, setzen Sie **[!UICONTROL Use in Filter Options]** auf `Yes`.

   - Um das Kundenraster nach Textattribut mit unterschiedlichen Filterübereinstimmungsbedingungen zu filtern, setzen Sie **[!UICONTROL Grid Filter Condition Type]** auf `Partial Match`, `Prefix Match` oder `Full Match`. Das Feld _Suche nach Keyword_ für das Raster ist davon nicht betroffen.

   - Um das Kundenraster anhand dieses Attributs zu durchsuchen, setzen Sie **[!UICONTROL Use in Search Options]** auf `Yes`.

   - Um dieses Attribut [Kundensegmenten](customer-segments.md) zur Verfügung zu stellen, setzen Sie **[!UICONTROL Use in Customer Segment]** auf `Yes`.

## Schritt 2: Ausfüllen der Storefront-Eigenschaften

1. Scrollen Sie nach unten zum Abschnitt &quot;**[!UICONTROL Storefront Properties]**&quot;.

   ![Kundenattribute - Storefront-Eigenschaften](./assets/attribute-customer-storefront-properties.png){width="600" zoomable="yes"}

1. Um das Attribut für Kunden sichtbar zu machen, setzen Sie **[!UICONTROL Show on Storefront]** auf `Yes`.

1. Geben Sie eine Zahl in das Feld **[!UICONTROL Sort Order]** ein, die die Reihenfolge des Erscheinungsbilds bestimmt, wenn sie mit anderen Attributen aufgeführt wird.

1. Setzen Sie **[!UICONTROL Forms to Use]** auf jedes Formular, das das Attribut enthalten soll. Um mehrere Optionen auszuwählen, halten Sie die Strg-Taste gedrückt und klicken Sie auf jedes Formular.

   - [&quot;Kundenregistrierung&quot;](customer-sign-in.md)
   - [&quot;Bearbeiten von Kundenkonten&quot;](account-create.md)
   - [&quot;Admin Checkout&quot;](../stores-purchase/checkout-process.md)

## Schritt 3: Titel ausfüllen und speichern

1. Wählen Sie im linken Bereich **[!UICONTROL Manage Labels/Options]** aus.

1. Geben Sie unter &quot;**[!UICONTROL Manage Titles]**&quot;eine Beschriftung ein, um das Attribut für jede [Store-Ansicht](../getting-started/websites-stores-views.md) zu identifizieren.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Attribute]**.

   ![Kundenattribute - Beschriftungen/Optionen](./assets/attribute-customer-manage-label-options.png){width="600" zoomable="yes"}

## Feldbeschreibungen

### [!UICONTROL Attribute Properties]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Default Label] | Die Standardbeschriftung, mit der das Attribut in der Admin- und Storefront identifiziert wird. |
| [!UICONTROL Attribute Code] | Ein eindeutiger Code, der das Attribut im System identifiziert. Der Code kann bis zu 60 Zeichen lang sein und darf keine Leerzeichen oder Sonderzeichen enthalten. Anstelle eines Leerzeichens kann das Unterstrichsymbol verwendet werden. |
| [!UICONTROL Input Type] | Bestimmt das Eingabefeld, das für die Dateneingabe verwendet wird. Optionen: <br/>**`Text Field`**- Ein einzeiliges Textfeld.<br/>**`Text Area`** - Ein mehrzeiliger Textbereich. <br/>**`Multiple Line`**- Erstellt mehrere Textzeilen für das Attribut, ähnlich wie bei einer mehrzeiligen Straßenadresse. Die Anzahl der einzelnen Dateneintragszeilen kann zwischen 2 und 20 liegen.<br/>**`Date`** - Zeigt ein Datumsfeld mit einem Popup-Kalender an.<br/>**`Dropdown`**- Eine Dropdownliste, in der nur ein Wert ausgewählt werden kann.<br/>**`Multiple Select`** - Eine Dropdownliste, in der mehrere Werte ausgewählt werden können. <br/>**`Yes/No`**- Ein Feld, das nur eine Auswahl von `Yes` - oder `No` -Werten bietet.<br/>**`File (attachment)`** - Ein Feld, in das eine Datei hochgeladen und dem Kundenattribut als Anlage zugeordnet werden kann. <br/>**`Image File`**- Ein Feld, mit dem ein Bild in die Galerie hochgeladen und mit dem Kundenattribut verknüpft werden kann. |
| [!UICONTROL Values Required] | Bestimmt, ob ein Wert in das Feld eingegeben werden muss. Optionen: `Yes` / `No` |
| [!UICONTROL Default Value] | Gibt den Anfangswert des Attributs an. |
| [!UICONTROL Input Validation] | Die Auswahl der Optionen wird vom Eingabetyp bestimmt. Optionen: <br/>**`None`**- Das Feld hat während der Dateneingabe keine Eingabevalidierung.<br/>**`Alphanumeric`** - Akzeptiert während der Dateneingabe eine beliebige Kombination aus Zahlen (0-9) und alphabetischen Zeichen (a-z, A-Z). <br/>**`Alphanumeric with Space`**- Ermöglicht es, dass Leerzeichen in der Straßenadresse den maximalen Längenanforderungen des Frachtführers entsprechen. Beim Checkout kann der Kunde eine beliebige Kombination aus Zahlen (0-9), Buchstaben (a-z, A-Z) und Leerzeichen in die Straßenadresse des Empfängers und Absenders eingeben. Alle zusätzlichen Leerzeichen werden beim Speichern der Adresse abgeschnitten.<br/>**`Numeric Only`** - Akzeptiert während der Dateneingabe nur Zahlen (0-9). <br/>**`Alpha Only`**- Akzeptiert während der Dateneingabe nur alphabetische Zeichen (a-z, A-Z).<br/>**`URL`** - Akzeptiert nur eine URL während der Dateneingabe. <br/>**`Email`**- Akzeptiert nur eine E-Mail-Adresse während der Dateneingabe.<br/>**`Length Only`** - Validiert die Eingabe anhand der Länge der in das Feld eingegebenen Daten. |
| [!UICONTROL Input/Output Filter] | Wendet einen Vorverarbeitungsfilter auf Werte an, die in ein Textfeld, einen Textbereich oder einen mehrzeiligen Eingabetyp eingegeben wurden, bevor der Datensatz gespeichert wird. Optionen: <br/>**`None`**- Wendet keinen Filter auf den in das Feld eingegebenen Text an.<br/>**`Strip HTML Tags`** - Entfernt HTML-Tags aus dem Text. Dieser Filter kann beim Bereinigen von Daten helfen, die aus einer anderen Quelle, die HTML-Tags enthält, in ein Feld eingefügt werden. <br/>**`Escape HTML Entities`**- Konvertiert die im Text gefundenen Sonderzeichen in eine gültige HTML-Escape-Sequenz, z. B. `amp;`. Escape-Sequenzen sind zwischen einem kaufmännischen Und und einem Semikolon eingeschlossen und werden häufig für typografische Anführungszeichen, Copyright-Symbole und Markenzeichensymbole verwendet. Escape-Sequenzen werden auch verwendet, um Zeichen wie die Symbole &quot;kleiner als&quot;(`<`) und &quot;größer als&quot;(`>`) sowie das kaufmännische Und-Zeichen zu identifizieren, die auch im Code verwendet werden. Dieser Filter kann dazu beitragen, Sonderzeichen zu bereinigen, die manchmal aus Textverarbeitungen in Datenbankfelder eingefügt werden. |
| [!UICONTROL Add to Column Options] | Gibt an, ob das Attribut als Spalte im Raster [Kunden](customers-all.md) enthalten ist. Optionen: `Yes` / `No` |
| [!UICONTROL Use in Filter Options] | Gibt an, ob das Attribut als Filter für Suchvorgänge aus dem Raster verwendet werden kann. Optionen: `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | Gibt die Bedingungen für die Filterung von Attributen für Suchvorgänge aus dem Raster an. Das Feld _Suche nach Keyword_ für das Raster ist davon nicht betroffen. Optionen: `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | Gibt an, ob der Attributwert bei Suchvorgängen als Keyword verwendet werden kann. Optionen: `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | Bestimmt, ob das Attribut in den Bedingungen für [Kundensegment](customer-segments.md) enthalten ist. Optionen: `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Show on Storefront] | Bestimmt, ob das Attribut als Feld in den Kundeninformationen in der Storefront angezeigt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Sort Order] | Gibt die Sortierreihenfolge dieses Attributs in Bezug auf andere Kundenattribute an. Die Sortierreihenfolge bestimmt die Reihenfolge, in der Felder während der Dateneingabe bei Verwendung der Tastaturnavigation den Fokus erhalten. |
| [!UICONTROL Forms to Use in] | Bestimmt die Seiten mit Dateneingabeformularen, auf denen das Attribut angezeigt wird. Optionen: <br/>[`Customer Registration`](account-dashboard-account-information.md) <br/>[`Customer Account Edit`](account-create.md) <br/>[`Admin Checkout`](../stores-purchase/checkout-process.md) |

## Standardmäßige Kundenattribute

| Attributcode | Beschreibung |
| --------------- | ------------------ |
| `created_at` | Das Datum der Erstellung des Kundenkontos. |
| `updated_at` | Das Datum der letzten Aktualisierung des Kundenkontos. |
| `website_id` | Die Website-ID der Site, auf der das Kundenkonto erstellt wurde. |
| `store_id` | Die Store-ID der Site, auf der das Kundenkonto erstellt wurde. |
| `created_in` | Die Store-Ansicht, in der das Konto erstellt wurde. |
| `group_id` | Die ID der Kundengruppe, der der Kunde zugewiesen ist. |
| `disable_auto_group_change` | Bestimmt, ob Kundengruppen während der [MwSt.-ID-Validierung](../stores-purchase/vat.md#configure-vat-id-validation) dynamisch zugewiesen werden können. |
| `prefix` | Jedes Präfix, das mit dem Kundennamen verwendet wird (z. B. Herr, Frau oder Dr.). |
| `firstname` | Der Vorname des Kunden. |
| `middlename` | Der Vorname oder die mittlere Anfangsphase des Kunden. |
| `lastname` | Der Nachname des Kunden. |
| `suffix` | Jedes Suffix, das mit dem Kundennamen verwendet wird. (z. B. Jr., Sr. oder Esquire) |
| `email` | Die E-Mail-Adresse des Kunden. |
| `dob` | Das Geburtsdatum des Kunden.  <br><br>**_Wichtig:_**Beachten Sie im Einklang mit den aktuellen Best Practices für Sicherheit und Datenschutz alle möglichen rechtlichen und sicherheitstechnischen Risiken, die mit der Speicherung des vollständigen Geburtsdatums (Monat, Tag, Jahr) der Kunden mit anderen persönlichen Identifikatoren verbunden sind. Es wird empfohlen, die Speicherung der vollständigen Geburtsdaten der Kunden zu begrenzen und stattdessen das Geburtsjahr des Kunden zu verwenden. |
| `taxvat` | Die dem Kunden zugewiesene Mehrwertsteuernummer (MwSt). Die Standardbeschriftung dieses Attributs ist `VAT Number`. Das Feld MwSt.-Nummer ist immer in allen Versand- und Rechnungskunden-Adressen vorhanden, wenn sie vom Administrator angezeigt werden, es ist jedoch kein erforderliches Feld. |
| `gender` | Das Kundengeschlecht. |

## Demo für Kundenattribute

Eine Demonstration der Erstellung von Kundenattributen finden Sie in diesem Video:

>[!VIDEO](https://video.tv.adobe.com/v/343661?quality=12)
