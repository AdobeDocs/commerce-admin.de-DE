---
title: Gibt das Attribut zurück
description: Erfahren Sie mehr über die Rückgabeattribute und wie Sie die Attribute erstellen, die für die Verarbeitung von Rückgaben in Ihrem Store erforderlich sind.
exl-id: 639c1e94-1211-4a4e-8599-e54ed99b2355
feature: Attributes, Returns
TQID: https://experienceleague.adobe.com/bKSZbmmyG9CWVIf0GzCgGImzHRIUV8HgD6asutC7lFo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 306
ht-degree: 0%

---

# Gibt das Attribut zurück

{{ee-feature}}

Die Rückgabeattribute werden verwendet, um Informationen zu speichern, die während des Rückgabevorgangs des Produkts benötigt werden. Zu den Standardattributen gehören die Bedingung des zurückgegebenen Produkts, der Grund für die Rückgabe und ein Feld, das angibt, wie die Rückgabe aufgelöst wurde. Der Prozess zum Erstellen eines Rückgabeattributs ähnelt dem Erstellen eines [Kundenattributs](../customers/attribute-properties.md).

![Admin - Gibt Attribute zurück](./assets/attribute-returns.png){width="700" zoomable="yes"}

## Erstellen eines Rückgabeattributs

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add New Attribute]**.

   ![Neue Rückgabe - Attributeigenschaften](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### Definieren der Eigenschaften

1. Um das Attribut während der Dateneingabe zu identifizieren, legen Sie die **[!UICONTROL Default Label]** fest.

1. Geben Sie **[!UICONTROL Attribute Code]** einen Code ein, der das Attribut innerhalb des Systems identifiziert.

1. Um den Typ des Eingabedialogs zu bestimmen, der für die Dateneingabe verwendet wird, legen Sie **[!UICONTROL Input Type]** auf einen der folgenden Werte fest:

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. Um das Feld zu einem erforderlichen Element zu machen, setzen Sie **[!UICONTROL Values Required]** auf `Yes`.

1. Um dem Feld einen Anfangswert zuzuweisen, geben Sie einen **[!UICONTROL Default Value]** ein.

1. Legen Sie **[!UICONTROL Input Validation]** auf eine der folgenden Einstellungen fest, um die Genauigkeit der in das Feld eingegebenen Daten vor dem Speichern des Datensatzes zu überprüfen:

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. Geben Sie für die Eingabetypen `Text Field` und `Text Area` den **[!UICONTROL Minimum Text Length]** und die **[!UICONTROL Maximum Text Length]** ein.

1. Um einen Vorverarbeitungsfilter anzuwenden, legen Sie **[!UICONTROL Input/Output Filter]** auf einen der folgenden Werte fest:

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. Um das Attribut für Kunden sichtbar zu machen, legen Sie im Abschnitt _[!UICONTROL Storefront Properties]_&#x200B;den Wert **[!UICONTROL Show on Storefront]**&#x200B;auf `Yes` fest.

1. (Optional) Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, um zu bestimmen, wo dieses Attribut relativ zu den anderen im selben Teil der Seite angezeigt wird. (`0` = First, `1` = Second, `2` = Third usw.)

### Titel/Optionen verwalten

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Manage Labels/Options]** aus.

1. Geben Sie im Abschnitt **[!UICONTROL Manage Titles (Size, Color, etc.)]** den Titel für jede Shop-Ansicht ein.

   ![Kennzeichnungen verwalten](./assets/return-attributes.png){width="600" zoomable="yes"}

1. Wenn der **[!UICONTROL Input Type]** für das Attribut `Dropdown` ist, verwalten Sie die Optionen im Abschnitt **[!UICONTROL Manage Options (Values of Your Attribute)]** .

   - Um eine Option hinzuzufügen, klicken Sie auf **[!UICONTROL Add Option]** und geben Sie den Titel für „Admin“ und jede Shop-Ansicht ein.
   - Um eine Option als Standard festzulegen, wählen Sie **[!UICONTROL Is Default]**.
   - Um eine Option zu entfernen, klicken Sie auf **[!UICONTROL Delete]**.

1. Um Änderungen zu speichern, klicken Sie auf **[!UICONTROL Save Attribute]**.
