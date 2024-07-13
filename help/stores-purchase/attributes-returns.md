---
title: Gibt das Attribut zurück
description: Erfahren Sie mehr über die Rückgabeattribute und wie Sie die Attribute erstellen, die für die Verarbeitung von Rückgaben in Ihrem Store erforderlich sind.
exl-id: 639c1e94-1211-4a4e-8599-e54ed99b2355
feature: Attributes, Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Gibt das Attribut zurück

{{ee-feature}}

Die Rückgabeattribute werden verwendet, um Informationen zu speichern, die während des Rückgabevorgangs des Produkts benötigt werden. Zu den Standardattributen gehören die Bedingung des zurückgegebenen Produkts, der Grund für die Rückgabe und ein Feld, das angibt, wie die Rückgabe aufgelöst wurde. Der Prozess zum Erstellen eines Rückgabeattributs ähnelt dem Erstellen eines [Kundenattributs](../customers/attribute-properties.md).

![Admin - Gibt Attribute zurück](./assets/attribute-returns.png){width="700" zoomable="yes"}

## Rückgabeattribut erstellen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add New Attribute]**.

   ![Neue Rückgabe - Attributeigenschaften](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### Eigenschaften definieren

1. Um das Attribut während der Dateneingabe zu identifizieren, legen Sie den Wert **[!UICONTROL Default Label]** fest.

1. Geben Sie für &quot;**[!UICONTROL Attribute Code]**&quot;einen Code ein, der das Attribut im System angibt.

1. Um den Typ des Eingabeditors zu bestimmen, der für die Dateneingabe verwendet wird, setzen Sie **[!UICONTROL Input Type]** auf einen der folgenden Werte:

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. Um das Feld zu einem erforderlichen Element zu machen, setzen Sie **[!UICONTROL Values Required]** auf `Yes`.

1. Um dem Feld einen Anfangswert zuzuweisen, geben Sie einen **[!UICONTROL Default Value]** ein.

1. Um die in das Feld eingegebenen Daten auf ihre Genauigkeit zu überprüfen, bevor der Datensatz gespeichert wird, setzen Sie **[!UICONTROL Input Validation]** auf einen der folgenden Werte:

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. Geben Sie für die Eingabetypen `Text Field` und `Text Area` die Werte **[!UICONTROL Minimum Text Length]** und **[!UICONTROL Maximum Text Length]** ein.

1. Um einen Vorverarbeitungsfilter anzuwenden, legen Sie **[!UICONTROL Input/Output Filter]** auf einen der folgenden Werte fest:

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. Um das Attribut für Kunden sichtbar zu machen, setzen Sie im Abschnitt _[!UICONTROL Storefront Properties]_den Wert **[!UICONTROL Show on Storefront]**auf `Yes`.

1. (Optional) Geben Sie für &quot;**[!UICONTROL Sort Order]**&quot;eine Zahl ein, um zu bestimmen, wo dieses Attribut relativ zu den anderen im selben Teil der Seite angezeigt wird. (`0` = first, `1` = second, `2` = third usw.)

### Verwalten der Bezeichnungen/Optionen

1. Wählen Sie im linken Bereich **[!UICONTROL Manage Labels/Options]** aus.

1. Geben Sie im Abschnitt **[!UICONTROL Manage Titles (Size, Color, etc.)]** den Titel für jede Store-Ansicht ein.

   ![Bezeichnungen verwalten](./assets/return-attributes.png){width="600" zoomable="yes"}

1. Wenn die **[!UICONTROL Input Type]** für das Attribut `Dropdown` ist, verwalten Sie die Optionen im Abschnitt **[!UICONTROL Manage Options (Values of Your Attribute)]** .

   - Um eine Option hinzuzufügen, klicken Sie auf **[!UICONTROL Add Option]** und geben Sie den Titel für &quot;Admin&quot;und jede Store-Ansicht ein.
   - Um eine Option zum ausgewählten Standard zu machen, wählen Sie &quot;**[!UICONTROL Is Default]**&quot;.
   - Um eine Option zu entfernen, klicken Sie auf **[!UICONTROL Delete]**.

1. Klicken Sie zum Speichern der Änderungen auf **[!UICONTROL Save Attribute]**.
