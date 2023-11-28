---
title: Einrichtung der Geschenkregistrierung
description: Erfahren Sie, wie Sie Geschenkregistertypen für Ihre Store-Kunden einrichten.
exl-id: d618c769-10be-4881-a799-42484d35c57b
feature: Gift, Storefront
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 0%

---

# Einrichtung der Geschenkregistrierung

{{ee-feature}}

Für jede Art von Veranstaltung, wie z.B. Hochzeit, Geburtstag, Jubiläum, neues Baby oder jede andere besondere Veranstaltung, kann eine Geschenkregistrierung erstellt werden. Adobe Commerce umfasst standardmäßig die folgenden Spezialereignisse:

- Baby
- Geburtstag
- Hochzeit

Wenn Sie eine Registrierung erstellen, wird sie zu einer Option in der Liste der Geschenkregistertypen im Konto des Kunden.

Sie können eine der drei vorbereiteten Geschenkregister verwenden oder eine eigene benutzerdefinierte Registrierung erstellen. Jeder Geschenkregistertyp enthält mehrere Attribute, d. h. die Dateneingabefelder, die ein Kunde zum Erstellen einer Geschenkregistrierung ausfüllt. Die Attribute bieten zusätzliche Informationen zum Ereignis, zur Zeit und zum Standort oder zu weiteren benötigten Informationen. Je nach Eingabetyp haben einige Attribute mehrere Optionen. Beispiel: die `Wedding` Der Typ der Geschenkregistrierung weist das Attribut auf `Role`mit dem `Bride`, `Groom`, und `Partner` Optionen. Weitere Informationen zu Attributen und Eingabetypen finden Sie unter [Attribute](../customers/attribute-properties.md).

![Gift-Registrierungstypen](./assets/gift-registry-types.png){width="700" zoomable="yes"}

## Verwenden Sie eine vorbereitete Geschenkregistrierung.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**.

   Die Geburtstags-, Hochzeit- und Babyregistrierung ist für Kunden bereit, diese von ihren Konten aus zu nutzen.

1. Vergewissern Sie sich, dass die [E-Mail-Vorlagenkonfiguration](../systems/email-templates.md#configure-email-templates), damit sie Ihre Marke widerspiegeln.

## Erstellen einer benutzerdefinierten Geschenkregistrierung

1. Navigieren Sie in der Admin-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Gift Registry Type]**.

1. under **[!UICONTROL General Information]**, führen Sie Folgendes aus:

   - Eindeutige Eingabe **[!UICONTROL Code]** zur internen Identifizierung der Geschenkregistrierung.

     Der Code muss mit einem Kleinbuchstaben beginnen. Der Rest des Codes kann aus einer beliebigen Kombination aus Kleinbuchstaben (a-z), Zahlen (0-9) und Unterstrichen (`_`).

   - Für **[!UICONTROL Label]** Geben Sie einen Namen für die Geschenkregistrierung ein, wie er im Speicher angezeigt werden soll.

     Dieser Titel ist eine Option in der Liste der Geschenkregistertypen, die dem Kunden zur Verfügung stehen.

   - Für **[!UICONTROL Sort Order]** Geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der diese Geschenkregistrierung erscheint, wenn sie mit anderen Typen aufgeführt wird.

   - Um die Geschenkregistrierung zu aktivieren, legen Sie **[!UICONTROL Is Listed]** nach `Yes`.

     ![Gift-Registry - Allgemeine Informationen](./assets/gift-registry-new-general-information.png){width="600" zoomable="yes"}

1. Untersuchen Sie jeden Abschnitt der Geschenkregistrierung, um die Art der Informationen zu ermitteln, die Sie einbeziehen möchten.

1. Wählen Sie im linken Bereich die Option **[!UICONTROL Attributes]** und klicken **[!UICONTROL Add Attribute]**.

   ![Gift Registry - neues Attribut](./assets/gift-registry-type-new-attribute.png){width="600" zoomable="yes"}

1. Gehen Sie für jedes Attribut wie folgt vor:

   - Zuweisen einer eindeutigen **[!UICONTROL Code]** , um das Attribut intern zu identifizieren. Der Code kann bis zu 15 Zeichen lang sein und muss mit einem Kleinbuchstaben beginnen. Der Rest des Codes kann Kleinbuchstaben (`a`-`z`), Zahlen (`0`-`9`) und dem Unterstrich (`_`), um Wörter zu trennen.

   - Wählen Sie die **[!UICONTROL Input Type]** für die Dateneingabe verwendet werden. Sie können einen der benutzerdefinierten oder statischen Typen verwenden.

   - Wenn der Eingabetyp mehrere Optionen aufweist, klicken Sie auf **[!UICONTROL Add New Option]** und füllen Sie die Informationen für jede Option aus.

     Einige Eingabetypen verfügen über zusätzliche Eigenschaften. Beispielsweise verfügt der Ereignisort über zusätzliche Eigenschaften, um das Ereignis durchsuchbar zu machen, und ist in der öffentlichen Liste der Geschenkregister Ihres Stores enthalten.

      - Satz **[!UICONTROL Attribute Group]** in den Bereich der Geschenkregistrierung, in dem das Attribut angezeigt werden soll.

      - Für **[!UICONTROL Label]** Geben Sie einen Namen ein, um das Dateneingabefeld in der Registrierung zu identifizieren.

      - Wenn der Kunde eine Auswahl treffen oder einen Wert in das Feld eingeben muss, legen Sie **[!UICONTROL Is Required]** nach `Yes`.

      - Für **[!UICONTROL Sort Order]** Geben Sie eine Nummer ein, um die Reihenfolge zu bestimmen, in der diese Geschenkregistrierung erscheint, wenn sie mit anderen Geschenkregistern aufgelistet ist, die möglicherweise im Speicher verfügbar sind.

1. Um eine weitere Option hinzuzufügen, klicken Sie auf **Neue Option hinzufügen**.

   Jede neue hinzugefügte Option wird in einem neuen Abschnitt oben angezeigt. Wiederholen Sie diesen Vorgang für das neue Attribut.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

## Feldbeschreibungen

### [!UICONTROL General Information]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Code] | Ein eindeutiger Name zur internen Identifizierung des Geschenkregistertyps. Das erste Zeichen des Codes muss ein Kleinbuchstabe sein. Der restliche Code kann aus einer beliebigen Kombination aus Kleinbuchstaben (a-z), Zahlen (0-9) und Unterstrichen (`_`). |
| [!UICONTROL Label] | Der Name des Geschenkregistertyps, der im Speicher angezeigt wird. |
| [!UICONTROL Sort Order] | Bestimmt die Reihenfolge, in der dieser Geschenkregistertyp angezeigt wird, wenn er mit anderen Typen aufgeführt wird. |
| [!UICONTROL Is Listed] | Stellt fest, ob der Geschenkregistertyp für Kunden im Laden verfügbar ist. Optionen: `Yes` / `No`. |

{style="table-layout:auto"}

### [!UICONTROL Attributes]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Code] | Ein eindeutiger Name zur internen Identifizierung des Attributs. Der Code kann eine beliebige Kombination aus Kleinbuchstaben (a-z), Zahlen (0-9) und dem Unterstrich (`_`). |
| [!UICONTROL Input Type] | Bestimmt den Datentyp und die Eingabesteuerung, die dem Attribut zugeordnet sind, nach Typ. |
| [!UICONTROL Attribute Group] | Wählen Sie die Gruppe aus, in der das Attribut in der Geschenkregistrierung aufgeführt ist. |
| [!UICONTROL Label] | Der Name, der das Attribut im Konto-Dashboard des Kunden angibt. |
| [!UICONTROL Is Required] | Gibt an, ob das Attribut ein erforderlicher Eintrag ist. Die Geschenkregistrierung kann erst gespeichert werden, wenn alle erforderlichen Attribute abgeschlossen sind. Optionen: `Yes` / `No`. |
| [!UICONTROL Sort Order] | Bestimmt die Reihenfolge, in der das Attribut angezeigt wird, wenn es mit anderen Attributen aufgeführt wird. |

{style="table-layout:auto"}

#### [!UICONTROL Input Type Options]

Wählen Sie den Datentyp und die Eingabesteuerung aus, die mit dem Attribut verknüpft sind.

**_[!UICONTROL Custom Types]_**

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Text] | Zeigt das Attribut als Textfeld an. |
| [!UICONTROL Select] | Zeigt das Attribut als Dropdownliste an. Klicks **[!UICONTROL Add New Option]** , um der Dropdown-Liste weitere Bedingungen hinzuzufügen:<br/>**[!UICONTROL Code]**- Ein eindeutiger Name zur internen Identifizierung des Attributs.<br/>**[!UICONTROL Label]** - Der Name, der das Attribut im Konto-Dashboard des Kunden identifiziert.<br/>**[!UICONTROL Is Default]**- Setzen Sie diesen Schalter, um die Standardbedingung auszuwählen.<br/>**[!UICONTROL Delete Option]** - Klicken Sie auf , um die Option zu löschen. |
| [!UICONTROL Date] | Zeigt das Attribut als Datumsfeld an. Optionen: `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Country] | Zeigt das Attribut als Dropdownliste mit Ländern an. Satz **[!UICONTROL Show Region]** an: `Yes` / `No`. |

{style="table-layout:auto"}

**_[!UICONTROL Static Types]_**

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Event Date] | Bestimmt, wie das Datumsattribut im Store verwendet wird. Optionen: <br/>**[!UICONTROL Searchable]**- Bestimmt, ob das Attribut für die erweiterte Suche verfügbar ist. Optionen: `Yes` / `No`.<br/>**[!UICONTROL Is Listed]** - Bestimmt, ob das Ereignis in der Liste der im Store verfügbaren Ereignisse enthalten ist. Optionen: `Yes` / `No`. <br/>**[!UICONTROL Date Format]**- Bestimmt das Format des Ereignisdatums. Optionen: `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Event Country] | Zeigt das Attribut als Liste von Ländern an. Optionen: <br/>**[!UICONTROL Searchable]**- Bestimmt, ob das Attribut für die erweiterte Suche verfügbar ist. Optionen: `Yes` / `No`.<br/>**[!UICONTROL Is Listed]** - Bestimmt, ob das Ereignis in der Liste der im Store verfügbaren Ereignisse enthalten ist. Optionen: `Yes` / `No`. <br/>**[!UICONTROL Show Region]**- Bestimmt den Bereich des Ereignisses. |
| [!UICONTROL Event Location] | Der Speicherort des Ereignisses, das mit der Geschenkregistrierung in Verbindung steht. <br/>Satz **[!UICONTROL Is Searcheable]** an: `Yes` / `No` <br/>Satz **[!UICONTROL Is Listed]** an: `Yes` / `No` |
| [!UICONTROL Role] | Die Rolle, die den Empfänger des Geschenks identifiziert. Beispiel: `Bride`, `Groom`oder `Partner`.<br/>**[!UICONTROL Is Searcheable]**- Legen Sie `Yes`/ `No`<br/>** ist aufgeführt **- Legen Sie `Yes` / `No`<br/>**[!UICONTROL Add New Option]** - Klicken Sie auf , um weitere Bedingungen zum Dropdown-Menü hinzuzufügen:<br/>**Code** - Ein eindeutiger Name zur internen Identifizierung des Attributs.<br/>**[!UICONTROL Label]**- Der Name, der das Attribut im Konto-Dashboard des Kunden identifiziert.<br/>**[!UICONTROL Is Default]** - Setzen Sie diesen Schalter, um die Standardbedingung auszuwählen.<br/>**[!UICONTROL Delete Option]**- Klicken Sie auf , um die Option zu löschen. |

{style="table-layout:auto"}

#### [!UICONTROL Attribute Group Options]

Wählen Sie die Gruppe aus, in der das Attribut in der Geschenkregistrierung aufgeführt ist.

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Event Information] | Gruppiert alle Attribute der Geschenkregistrierung, die die Informationen zum Geschenkregisterereignis, zur Zeit, zum Ort usw. hinzufügen. |
| [!UICONTROL Gift Registry Properties] | Kombiniert alle Attribute, die Informationen direkt zur Geschenkregistrierung hinzufügen. |
| [!UICONTROL Privacy Settings] | Listet die Attribute auf, die Informationen zum Datenschutz für Geschenkregistrierung hinzufügen. |
| [!UICONTROL Recipients Information] | Gruppiert die Attribute, die Informationen über die Person bereitstellen, die eine Geschenkregistrierung erstellt. |
| [!UICONTROL Shipping Address] | Kombiniert die Attribute, die Informationen zur Versandadresse des Geschenkregisterereignisses hinzufügen. |

{style="table-layout:auto"}
