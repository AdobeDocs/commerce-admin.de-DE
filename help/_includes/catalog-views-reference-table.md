---
title: Referenztabelle für Katalogansichten
description: Wiederverwendete Referenztabelle für das Katalogansichtsraster
source-git-commit: bc4baccc4b40fb7ecdc7f489bfaf3c797881db88
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%
---
# Referenztabelle für Katalogansichten

Das Raster listet eine Zeile für jede Katalogansicht auf, die erstellt wird, wenn ein freigegebener Katalog mit [!DNL Adobe Commerce Optimizer] synchronisiert wird. Das Raster ist abgesehen von der Schlüsselzuweisungsaktion schreibgeschützt. Katalogsichten werden automatisch erstellt und entfernt, wenn der Connector freigegebene Kataloge synchronisiert, die in Adobe Commerce konfiguriert sind. Wenn ein Katalog entfernt wird, gibt es eine [Übergangsphase](/help/systems/catalog-view-sync-status.md#configure-the-deletion-grace-period) bevor die entsprechende Katalogansicht und die Daten gelöscht werden.

Informationen zum Zuweisen oder Aufheben der Zuweisung von eingeschränkten Zugriffsschlüsseln finden Sie [Zuweisen von Schlüsseln zu einer Katalogansicht](/help/systems/restricted-access-keys.md#assign-keys-to-a-catalog-view).

| Feld | Beschreibung |
| --- | --- |
| [!UICONTROL ACO Catalog View ID] | Die Kennung der entsprechenden Katalogansicht in [!DNL Adobe Commerce Optimizer]. Siehe [Zusammenfassung des Synchronisierungsstatus der Katalogansicht](/help/systems/catalog-view-sync-status.md#catalog-view-sync-status-summary), um den Synchronisierungsstatus zu überprüfen. |
| [!UICONTROL Store View] | Die Store-Ansicht, die die Katalogansicht darstellt. Siehe [Store-Ansichten](/help/stores-purchase/store-views.md). |
| [!UICONTROL Access Keys] | Die Titel der eingeschränkten Zugriffsschlüssel, die derzeit der Katalogansicht zugewiesen sind. Siehe [Verwaltung von Zugriffsschlüsseln](/help/systems/restricted-access-keys.md). |
| [!UICONTROL Actions] | Wählen Sie **[!UICONTROL Edit Restricted Access Keys]** aus, um Schlüssel für die Katalogansicht zuzuweisen oder deren Zuweisung aufzuheben. Siehe [Zuweisen von Schlüsseln zu einer Katalogansicht](/help/systems/restricted-access-keys.md#assign-keys-to-a-catalog-view). |

{style="table-layout:auto"}
