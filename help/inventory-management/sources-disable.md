---
title: Deaktivieren von Inventarquellen
description: Erfahren Sie, wie Sie Quellen deaktivieren und Informationen ändern, einschließlich Standort und Kontaktpunkt.
exl-id: 3fcbfa3c-8bb7-4e08-a395-9760bbd69f04
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Quellen deaktivieren

Um sicherzustellen, dass alle Bestelldaten in [!DNL Commerce] bleiben, können Quellen nicht gelöscht werden. Quellen, Bestellungen und Lieferungen sind direkt miteinander verbunden. Sie können Quellen deaktivieren und Informationen, einschließlich Standort und Kontaktpunkt, ändern.

Je nach Status Ihrer Standorte können Sie eine Quelle deaktivieren. Eine deaktivierte Quelle behält alle Zuweisungen pro Lager und Produkt, kann aber nicht für Inventar und Bestellungen aufgerufen werden.

Wenn eine Quelle deaktiviert ist:

- [!DNL Inventory Management] ignoriert die Quelle für die Versand- oder Auftragsverarbeitung und listet sie nicht auf.
- Die Lagerbestände haben keinen Zugriff auf die Lagerbestände aus der Quelle für aggregierte Lagerbestände.
- Bestellsendungen können nicht deaktivierten Standorten zugewiesen werden.

Sie können die Standard-Source nicht deaktivieren. [!DNL Commerce] verwendet diese Quelle für alle neuen importierten Produkte, für Bundle-Produkte und für die Systemunterstützung von Drittanbietern. Sie können benutzerdefinierte Quellen jederzeit aktivieren oder deaktivieren.

In den folgenden Situationen ist es hilfreich, eine Quelle auf `disabled` festzulegen:

- Hinzufügen eines Stores oder Warehouse : Wenn Sie neue Storefronts öffnen oder neue Warehouses und Lieferorte online schalten, fügen Sie einen Quelleintrag hinzu, um das Produktinventar mithilfe des Imports einzurichten und eine Verbindung zu potenziellen Stores herzustellen.
- Saisonale Sendungen - Feiertage können eine geschäftige Zeit des Jahres sein. Möglicherweise möchten Sie den Versand nur von bestimmten Versandstandorten wie Lagern beschränken, um stationäre Standorte gut bestückt und auf lokale Käufer ausgerichtet zu halten. Oder Sie können für einen begrenzten Zeitraum neue Lieferorte hinzufügen, um höhere Verkaufs- und Auftragseingangsraten zu verarbeiten.
- Standort schließen - Wenn Sie einen Standort für die Verlagerung an neue Standorte schließen oder dauerhaft deaktivieren, um neue Lieferungen vom Standort aus zu stoppen.

## Deaktivieren einer oder mehrerer benutzerdefinierter Quellen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Aktivieren Sie das Kontrollkästchen für jede aktivierte benutzerdefinierte Quelle, die Sie deaktivieren möchten.

1. Klicken Sie auf _Aktionen_ oben links im Menü und wählen Sie **[!UICONTROL Disable]**.

   ![[!DNL Inventory Management] - Menü „Aktionen“](assets/inventory-source-disable.png){width="600" zoomable="yes"}

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL OK]**.

## Aktivieren oder Deaktivieren einer einzelnen benutzerdefinierten Quelle

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Suchen Sie eine benutzerdefinierte Quelle und klicken Sie auf **[!UICONTROL Edit]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt _Allgemein_ und ändern Sie **[!UICONTROL Is Enabled]**:

   | Option | Beschreibung |
   | ----- | ----- |
   | `Yes` | Source ist aktiviert. Die Menge addiert sich zur Verkaufsmenge. Die Quelle listet bei Versandaufträgen die aktuelle Menge auf. Der Source-Auswahlalgorithmus prüft, ob es sich um die Versandquelle handelt. |
   | `No` | Source ist deaktiviert. Mengen werden nicht zu den verkäuflichen Mengen hinzugefügt. Die Quelle wird beim Versand von Bestellungen nicht aufgelistet. Lieferoptionen überspringen diese Quelle. |

1. Klicken Sie auf **[!UICONTROL Save and Close]**.
