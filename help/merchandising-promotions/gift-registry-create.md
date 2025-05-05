---
title: Einrichtung der Geschenkregistrierung
description: Erfahren Sie, wie Sie Geschenkregistrierungstypen für Ihre Store-Kunden einrichten.
exl-id: d618c769-10be-4881-a799-42484d35c57b
feature: Gift, Storefront
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 0%

---

# Einrichtung der Geschenkregistrierung

{{ee-feature}}

Ein Geschenkgutschein kann für jede Art von Ereignis erstellt werden, wie z. B. Hochzeit, Geburtstag, Jahrestag, neues Baby oder jeden anderen besonderen Anlass. Standardmäßig umfasst Adobe Commerce die folgenden Sonderereignisse:

- Baby
- Geburtstag
- Hochzeit

Wenn Sie eine Registrierung erstellen, wird sie zu einer Option in der Liste der Geschenkregistrierungstypen im Konto des Kunden.

Sie können eine der drei vorbereiteten Geschenkregistrierungen verwenden oder Ihre eigene benutzerdefinierte Registrierung erstellen. Jeder Geschenkregistrierungstyp enthält mehrere Attribute. Dies sind die Dateneingabefelder, die ein Kunde ausfüllt, um eine Geschenkregistrierung zu erstellen. Die Attribute liefern zusätzliche Informationen über das Ereignis, die Uhrzeit und den Ort oder andere erforderliche Informationen. Je nach Eingabetyp stehen für einige Attribute mehrere Optionen zur Verfügung. Beispielsweise verfügt der Registrierungstyp &quot;`Wedding` Geschenk“ über das Attribut &quot;`Role`&quot; mit den Optionen &quot;`Bride`&quot;, &quot;`Groom`&quot; und &quot;`Partner`&quot;. Weitere Informationen zu Attributen und Eingabetypen finden Sie unter [Attribute](../customers/attribute-properties.md).

![Geschenkregistrierungstypen](./assets/gift-registry-types.png){width="700" zoomable="yes"}

## Verwenden einer vorbereiteten Geschenkregistrierung

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**.

   Die Geburtstags-, Hochzeits- und Babyregistrierungen können von den Kunden über ihre Konten verwendet werden.

1. Stellen Sie sicher, dass Sie die [E-Mail-Vorlagenkonfiguration](../systems/email-templates.md#configure-email-templates) abgeschlossen haben, damit sie Ihre Marke widerspiegeln.

## Erstellen einer benutzerdefinierten Geschenkregistrierung

1. Navigieren Sie in der Seitenleiste Admin zu **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Gift Registry Type]**.

1. Füllen Sie unter **[!UICONTROL General Information]** Folgendes aus:

   - Geben Sie einen eindeutigen **[!UICONTROL Code]** ein, um die Geschenkregistrierung intern zu identifizieren.

     Der Code muss mit einem Kleinbuchstaben beginnen. Der Rest des Codes kann eine beliebige Kombination aus Kleinbuchstaben (a-z), Zahlen (0-9) und Unterstrichen (`_`) sein.

   - Geben Sie **[!UICONTROL Label]** einen Namen für die Geschenkregistrierung ein, so wie er im Store angezeigt werden soll.

     Diese Beschriftung ist eine Option in der Liste der Geschenkregistrierungstypen, die dem Kunden zur Verfügung stehen.

   - Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der diese Geschenkregistrierung angezeigt wird, wenn sie mit anderen Typen aufgelistet wird.

   - Um die Geschenkregistrierung zu aktivieren, setzen Sie **[!UICONTROL Is Listed]** auf `Yes`.

     ![Geschenkregistrierung - allgemeine Informationen](./assets/gift-registry-new-general-information.png){width="600" zoomable="yes"}

1. Untersuchen Sie jeden Abschnitt der Geschenkregistrierung, um festzustellen, welche Art von Informationen Sie einschließen möchten.

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Attributes]** und klicken Sie auf **[!UICONTROL Add Attribute]**.

   ![Geschenkregistrierung - neues Attribut](./assets/gift-registry-type-new-attribute.png){width="600" zoomable="yes"}

1. Gehen Sie für jedes Attribut wie folgt vor:

   - Weisen Sie eine eindeutige **[!UICONTROL Code]** zu, um das Attribut intern zu identifizieren. Der Code kann bis zu 15 Zeichen lang sein und muss mit einem Kleinbuchstaben beginnen. Der Rest des Codes kann Kleinbuchstaben (`a`-`z`), Zahlen (`0`-`9`) und den Unterstrich (`_`) enthalten, um Wörter zu trennen.

   - Wählen Sie die **[!UICONTROL Input Type]**, die für die Dateneingabe verwendet werden soll. Sie können einen der benutzerdefinierten oder statischen Typen verwenden.

   - Wenn der Eingabetyp über mehrere Optionen verfügt, klicken Sie auf **[!UICONTROL Add New Option]** und füllen Sie die Informationen für jede Option aus.

     Einige Eingabetypen verfügen über zusätzliche Eigenschaften. Beispielsweise verfügt der Veranstaltungsort über zusätzliche Eigenschaften, um das Ereignis durchsuchbar zu machen, und ist in der öffentlichen Liste der Geschenkregistrierungen Ihres Stores enthalten.

      - Legen Sie **[!UICONTROL Attribute Group]** auf den Abschnitt in der Geschenkregistrierung fest, in dem das Attribut angezeigt werden soll.

      - Geben Sie **[!UICONTROL Label]** einen Namen ein, um das Dateneingabefeld in der Registrierung zu identifizieren.

      - Wenn der Kunde eine Auswahl treffen oder einen Wert in das Feld eingeben muss, setzen Sie **[!UICONTROL Is Required]** auf `Yes`.

      - Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der diese Geschenkregistrierung angezeigt wird, wenn sie mit anderen Geschenkregistern aufgelistet wird, die möglicherweise im Store verfügbar sind.

1. Um eine weitere Option hinzuzufügen, klicken Sie auf **Neue Option hinzufügen**.

   Jede neu hinzugefügte Option wird in einem neuen Abschnitt oben angezeigt. Wiederholen Sie diesen Vorgang für das neue Attribut.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

## Feldbeschreibungen

### [!UICONTROL General Information]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Code] | Ein eindeutiger Name zur internen Identifizierung des Geschenkregistrierungstyps. Das erste Zeichen des Codes muss aus einem Kleinbuchstaben bestehen. Der Rest des Codes kann eine beliebige Kombination aus Kleinbuchstaben (a-z), Zahlen (0-9) und dem Unterstrichzeichen (`_`) sein. |
| [!UICONTROL Label] | Der Name des Geschenkregistrierungstyps, der im Store angezeigt wird. |
| [!UICONTROL Sort Order] | Bestimmt die Reihenfolge, in der dieser Geschenkregistrierungstyp angezeigt wird, wenn er mit anderen Typen aufgelistet wird. |
| [!UICONTROL Is Listed] | Legt fest, ob der Geschenkregistrierungstyp für Kunden im Store verfügbar ist. Optionen: `Yes` / `No`. |

{style="table-layout:auto"}

### [!UICONTROL Attributes]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Code] | Ein eindeutiger Name zur internen Identifizierung des Attributs. Der Code kann eine beliebige Kombination aus Kleinbuchstaben (a-z), Zahlen (0-9) und dem Unterstrichzeichen (`_`) enthalten. |
| [!UICONTROL Input Type] | Bestimmt den Typ der Daten und Eingabedialog, die dem Attribut zugeordnet sind, je nach Typ. |
| [!UICONTROL Attribute Group] | Wählen Sie die Gruppe aus, in der das Attribut in der Geschenkregistrierung aufgeführt ist. |
| [!UICONTROL Label] | Der Name, der das Attribut im Konto-Dashboard des Kunden identifiziert. |
| [!UICONTROL Is Required] | Gibt an, ob das Attribut ein erforderlicher Eintrag ist. Die Geschenkregistrierung kann erst gespeichert werden, wenn alle erforderlichen Attribute abgeschlossen sind. Optionen: `Yes` / `No`. |
| [!UICONTROL Sort Order] | Bestimmt die Reihenfolge, in der das Attribut angezeigt wird, wenn es mit anderen Attributen aufgelistet wird. |

{style="table-layout:auto"}

#### [!UICONTROL Input Type Options]

Wählen Sie den Typ der Daten- und Eingabesteuerung aus, die mit dem Attribut verknüpft ist.

**_[!UICONTROL Custom Types]_**

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Text] | Zeigt das Attribut als Textfeld an. |
| [!UICONTROL Select] | Zeigt das Attribut als Dropdown-Liste an. Klicken Sie auf **[!UICONTROL Add New Option]** , um der Dropdown-Liste weitere Bedingungen hinzuzufügen:<br/>**[!UICONTROL Code]**- Ein eindeutiger Name, der das Attribut intern identifiziert.<br/>**[!UICONTROL Label]** - Der Name, der das Attribut im Konto-Dashboard des Kunden identifiziert.<br/>**[!UICONTROL Is Default]**- Stellen Sie diesen Schalter ein, um die Standardbedingung auszuwählen.<br/>**[!UICONTROL Delete Option]** - Klicken, um die Option zu löschen. |
| [!UICONTROL Date] | Zeigt das Attribut als Datumsfeld an. Optionen: `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Country] | Zeigt das Attribut als Dropdown-Liste von Ländern an. **[!UICONTROL Show Region]** festlegen auf: `Yes` / `No`. |

{style="table-layout:auto"}

**_[!UICONTROL Static Types]_**

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Event Date] | Bestimmt, wie das Datumsattribut im Store verwendet wird. Optionen: <br/>**[!UICONTROL Searchable]**- Bestimmt, ob das Attribut für die erweiterte Suche verfügbar ist. Optionen: `Yes` / `No`.<br/>**[!UICONTROL Is Listed]** - Bestimmt, ob das Ereignis in der Liste der Ereignisse enthalten ist, die im Store verfügbar ist. Optionen: `Yes` / `No`. <br/>**[!UICONTROL Date Format]**- Bestimmt das Format des Ereignisdatums. Optionen: `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Event Country] | Zeigt das Attribut als Liste von Ländern an. Optionen: <br/>**[!UICONTROL Searchable]**- Bestimmt, ob das Attribut für die erweiterte Suche verfügbar ist. Optionen: `Yes` / `No`.<br/>**[!UICONTROL Is Listed]** - Bestimmt, ob das Ereignis in der Liste der Ereignisse enthalten ist, die im Store verfügbar ist. Optionen: `Yes` / `No`. <br/>**[!UICONTROL Show Region]**- Bestimmt die Region des Ereignisses. |
| [!UICONTROL Event Location] | Der Ort des Ereignisses, das mit der Geschenkregistrierung in Verbindung steht. <br/>**[!UICONTROL Is Searcheable]** festlegen auf: `Yes` / `No` <br/>**[!UICONTROL Is Listed]** festlegen auf: `Yes` / `No` |
| [!UICONTROL Role] | Die Rolle, die den Geschenkempfänger identifiziert. Beispiel: `Bride`, `Groom` oder `Partner`.<br/>**[!UICONTROL Is Searcheable]**- Auf `Yes`/`No` setzen<br/>**&#x200B; Ist aufgeführt &#x200B;**- Auf `Yes`/`No` setzen<br/>**[!UICONTROL Add New Option]** - Klicken Sie, um dem Dropdown-Menü weitere Bedingungen hinzuzufügen:<br/>**Code** - Ein eindeutiger Name, der das Attribut intern identifiziert.<br/>**[!UICONTROL Label]**- Der Name, der das Attribut im Konto-Dashboard des Kunden identifiziert.<br/>**[!UICONTROL Is Default]** - Stellen Sie diesen Schalter ein, um die Standardbedingung auszuwählen.<br/>**[!UICONTROL Delete Option]**- Klicken, um die Option zu löschen. |

{style="table-layout:auto"}

#### [!UICONTROL Attribute Group Options]

Wählen Sie die Gruppe aus, in der das Attribut in der Geschenkregistrierung aufgeführt ist.

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Event Information] | Gruppiert alle Geschenkregistrierungsattribute, die Informationen zum Geschenkregistrierungsereignis, dessen Zeit, Ort usw. hinzufügen. |
| [!UICONTROL Gift Registry Properties] | Kombiniert alle Attribute, die Informationen direkt zur Geschenkregistrierung hinzufügen. |
| [!UICONTROL Privacy Settings] | Listet die Attribute auf, die Informationen zum Datenschutz bei Geschenkregistrierungsereignissen hinzufügen. |
| [!UICONTROL Recipients Information] | Gruppiert die Attribute, die Informationen zu der Person bereitstellen, die eine Geschenkregistrierung erstellt. |
| [!UICONTROL Shipping Address] | Kombiniert die Attribute, die Informationen zur Versandadresse des Geschenkregistrierungsereignisses hinzufügen. |

{style="table-layout:auto"}
