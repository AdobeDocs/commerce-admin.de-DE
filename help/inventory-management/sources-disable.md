---
title: Lagerbestandsquellen deaktivieren
description: Erfahren Sie, wie Sie Quellen deaktivieren und Informationen ändern können, einschließlich Ort und Kontaktpunkt.
exl-id: 3fcbfa3c-8bb7-4e08-a395-9760bbd69f04
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Quellen deaktivieren

Um sicherzustellen, dass alle Bestelldaten in [!DNL Commerce] beibehalten werden, können Quellen nicht gelöscht werden. Quellen, Bestellungen und Sendungen sind direkt miteinander verbunden. Sie können Quellen deaktivieren und Informationen ändern, einschließlich Ort und Kontaktpunkt.

Abhängig vom Status Ihrer Standorte können Sie eine Quelle deaktivieren. Eine deaktivierte Quelle behält alle Zuweisungen nach Lagern und Produkten bei, ist jedoch nicht für Inventar und Bestellungen zugänglich.

Wenn eine Quelle deaktiviert ist:

- [!DNL Inventory Management] ignoriert und listet die Quelle für die Lieferung oder Auftragsverarbeitung nicht auf.
- Für die aggregierten Bestandssummen greifen die Bestände nicht auf die Lagerbestandsmengen aus der Quelle zu.
- Bestellsendungen können nicht behinderten Orten zugewiesen werden.

Sie können die standardmäßige Source nicht deaktivieren. [!DNL Commerce] verwendet diese Quelle für alle neuen importierten Produkte, für Bundle-Produkte und für die Systemunterstützung von Drittanbietern. Sie können benutzerdefinierte Quellen jederzeit aktivieren oder deaktivieren.

Das Festlegen einer Quelle auf `disabled` ist in folgenden Situationen hilfreich:

- Hinzufügen eines Stores oder Lagers - Wenn Sie neue Storefronts öffnen oder neue Lagerhäuser und Versandstandorte online bringen, fügen Sie einen Quelleintrag hinzu, um einen Produktbestand mithilfe von Import und Anschluss an potenzielle Lager einzurichten.
- Saisontransporte - Ferien können eine geschäftige Zeit des Jahres sein. Sie können den Versand nur von bestimmten Versandstandorten wie Lagerhäusern aus beschränken, um die Lagerstätten für Ziegelsteine und Mörtel gut zu halten und sich auf örtliche Käufer zu konzentrieren. Oder Sie können für eine begrenzte Zeit neue Versandstandorte hinzufügen, um höhere Verkaufs- und Auftragseingänge zu bewältigen.
- Schließung eines Standorts - Wenn Sie einen Standort schließen, um zu neuen Einrichtungen zu wechseln oder dauerhaft zu wechseln, deaktivieren Sie, um neue Sendungen vom Standort aus zu stoppen.

## Deaktivieren einer oder mehrerer benutzerdefinierter Quellen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Aktivieren Sie das Kontrollkästchen für jede aktivierte benutzerdefinierte Quelle, die Sie deaktivieren möchten.

1. Klicken Sie auf das Menü _Aktionen_ oben links und wählen Sie **[!UICONTROL Disable]** aus.

   ![[!DNL Inventory Management] Quellen - Aktionsmenü](assets/inventory-source-disable.png){width="600" zoomable="yes"}

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL OK]**.

## Aktivieren oder Deaktivieren einer einzelnen benutzerdefinierten Quelle

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Suchen Sie eine benutzerdefinierte Quelle und klicken Sie auf **[!UICONTROL Edit]**.

1. Erweitern Sie den Abschnitt _Allgemein_ um ![Erweiterungsselektor](../assets/icon-display-expand.png) und ändern Sie **[!UICONTROL Is Enabled]**:

   | Option | Beschreibung |
   | ----- | ----- |
   | `Yes` | Source ist aktiviert. Die Menge erhöht sich um die Verkaufsmenge. Die Quelle wird bei Versandbestellungen mit der aktuellen Menge aufgelistet. Der Source-Auswahlalgorithmus überprüft die Versandquelle. |
   | `No` | Source ist deaktiviert. Die Mengen werden nicht zu den Verkaufsmengen hinzugefügt. Die Quelle wird bei Versandbestellungen nicht aufgelistet. Die Versandoptionen überspringen diese Quelle. |

1. Klicken Sie auf **[!UICONTROL Save and Close]**.
