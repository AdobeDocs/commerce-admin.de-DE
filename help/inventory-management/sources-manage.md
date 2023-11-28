---
title: Verwalten von Inventarquellen
description: Erfahren Sie mehr über Quellen und wie sie die physischen Orte definieren, an denen Produktbestand verwaltet und zur Erfüllung von Bestellungen versandt wird oder wo Dienste verfügbar sind.
exl-id: 1315a8c9-7791-4c4b-9463-3126b79793c2
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# Quellen verwalten

Quellen sind die physischen Orte, an denen das Produktinventar verwaltet und zur Erfüllung der Bestellung versandt wird oder an denen Dienstleistungen verfügbar sind. Zu diesen Standorten gehören Lagerhäuser, Bausteine- und Mörtelgeschäfte, Vertriebszentren, Abholstandorte und Ablageunternehmen. Sie weisen diesen Quellen Lagerbestandsmengen zu und [!DNL Commerce] aggregiert automatisch die gesamten verkaufbaren Produkte für Ihre Bestände. Fügen Sie für große Unternehmen mehrere Quellen für alle Ihre Standorte hinzu: an verschiedenen geografischen Standorten nach Land und Kontinent, Standorten in einer Stadt, basierend auf dem Inventartyp, auch basierend auf Dienstleistungen.

Es wird empfohlen, beim Erstellen einer Quelle bestimmte physische geografische Standorte anzugeben. Dadurch wird _Distance Priority Algorithm_ , um den Standort der Lieferanschrift mit den verfügbaren Quellen zu vergleichen, um die nächstgelegene Quelle zu ermitteln, aus der Sendungen durchgeführt werden können. Sie können Google-Maps oder Offline-Berechnungen verwenden, die Geocodes verwenden. Weitere Informationen hierzu finden Sie unter _Distance Priority Algorithm_, siehe [Konfigurieren des Distance Priority-Algorithmus](distance-priority-algorithm.md).

Beginnen Sie mit einer _Standardquelle_ , die Sie aktualisieren, aber nicht deaktivieren können. Diese Quelle wird von Einzelquell-Händlern und für die Produktmigration verwendet. Sie benötigen immer eine Standardquelle.

- **Standortinformationen** - Jede Quelle enthält den Namen, das Land, die physische Adresse des Standorts und einen Ansprechpartner.
- **Aktivieren von Ressourcen** - Sie können Quellen nach Bedarf aktivieren und deaktivieren. Aktivieren Sie eine Quelle nur, wenn sie Bestellungen und Aufstockungen akzeptiert und erfüllt.
- **Verfügbarer Bestand** - Ordnen Sie Inventarmengen für jede Quelle über die Produktseite zu und aktualisieren Sie sie. Die Lagerbestandsmengen werden über die Quell- und Bestandszuordnung berechnet, bereitgestellt und reserviert.

Das folgende Diagramm veranschaulicht die Quellen für einen Bicycle Shop Händler, der ein Mountainbike verkauft, die für Lager verfügbar sind und von der SSA für Sendungen zugänglich sind.

![Beispiel-Quellen-Diagramm](assets/diagram-sources.png){width="600" zoomable="yes"}

Alle Stores beginnen mit einer Standardquelle, die aktiviert bleiben muss:

- Alle neuen Produkte in [!DNL Commerce] Quelle und Lager erforderlich, die automatisch für den sofortigen Zugriff auf [!DNL Inventory Management].
- Einzelquell-Händler verwenden die Standardquelle als einzigen Bestandstandort und -lieferungen.

## Quellen bearbeiten

Sie können den Namen, die Adresse, den GPS-Standort und den Kontaktpunkt aktualisieren. Der Quellcode ist ein geschützter Wert, der als eindeutige Kennung fungiert, die die Quelle mit Ihren Produktmengen und Lagern verknüpft.

Beim Bearbeiten der Standardquelle können Sie alle Konfigurationen mit Ausnahme des Namens und des Codes bearbeiten. Es wird empfohlen, Einzelquell-Händler Informationen hinzuzufügen, die ihrem Standort entsprechen.

Die _[!UICONTROL Manage Sources]_Auf dieser Seite werden alle verfügbaren Lagerorte und Ausführungseinrichtungen aufgelistet. Sie können neue Inventarquellen hinzufügen und vorhandene Standorte bearbeiten.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Informationen zum Hinzufügen eines Lagerorts finden Sie unter [Hinzufügen einer neuen Quelle](sources-add.md).

1. Suchen Sie die Inventarquelle und öffnen Sie sie in _Bearbeiten_ -Modus.

1. Aktualisieren Sie die Informationen und speichern Sie die Änderungen.

   ![Quellen verwalten](assets/inventory-sources.png){width="600" zoomable="yes"}

## Schaltflächenleiste

| Schaltfläche | Beschreibung |
|--|--|
| [!UICONTROL Add New Source] | Öffnet das Formular Neue Quelle , mit dem eine neue Lagerbestandsquelle, eine neue Fülleinrichtung oder einen neuen Speicherort eingegeben wird. |

## Beschreibungen der Quellen-Spalte verwalten

| Spalte | Beschreibung |
|--|--|
| [!UICONTROL Code] | Ein eindeutiger alphanumerischer Code, der vom System zur Identifizierung der Inventarquelle verwendet wird. |
| [!UICONTROL Name] | Ein eindeutiger Name, der die Inventarquelle für Admin-Benutzer angibt. |
| [!UICONTROL Is Enabled] | Gibt an, ob die Inventarquelle aktiv und verfügbar ist. |
| [!UICONTROL Pickup Location] | Gibt an, ob die Quelle als Pickup-Speicherort für [Versand im Geschäft](../stores-purchase/shipping-in-store-delivery.md). |
| [!UICONTROL Action] | Klicken **[!UICONTROL Edit]** öffnet den Quelldatensatz des Bestands im Bearbeitungsmodus. |

## Sonstige Spalten

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Latitude] | Gibt die Breitenkoordinate der Inventarquelle für GPS an. Geben Sie den Wert als Zahl ein, dem je nach Bedarf ein Plus- oder Minuszeichen vorangestellt wird. Das Symbol und die Buchstaben des Abschlusses sind nicht zulässig. Beispiel: `32.7555` |
| [!UICONTROL State/Province] | Das Bundesland, in dem sich die Quelle befindet. |
| [!UICONTROL Postcode] | Postleitzahl der Quelle. |
| [!UICONTROL Email] | Die E-Mail des Hauptkontakts. |
| [!UICONTROL Longitude] | Gibt die Längenkoordinate der Inventarquelle für GPS an. Geben Sie den Wert als Zahl ein, dem je nach Bedarf ein Plus- oder Minuszeichen vorangestellt wird. Das Symbol und die Buchstaben des Abschlusses sind nicht zulässig. Beispiel: Longitude -97.3308 |
| [!UICONTROL City] | Die Stadt, in der sich die Quelle befindet. |
| [!UICONTROL Phone] | Die Telefonnummer des Hauptkontakts. |
| [!UICONTROL Country] | Das Land, in dem sich die Quelle befindet. |
| [!UICONTROL Street] | Die Straßenadresse der Quelle. |
| [!UICONTROL Fax] | Die Ortskennung und Faxnummer des Hauptkontakts. |
