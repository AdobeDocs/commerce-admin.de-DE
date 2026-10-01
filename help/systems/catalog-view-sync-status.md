---
title: Überwachung des Synchronisationsstatus der Katalogansicht
description: Überwachen Sie den Zustand der freigegebenen B2B-Katalogprojektion und stimmen Sie Katalogansichten, Richtlinien, Preislisten und Zugriffsschlüssel für den Adobe Commerce Optimizer-Connector ab.
feature: Products, Customers, Data Import/Export
role: Admin
level: Intermediate
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: b974b164-8a4e-43b8-a9e2-8e67ec131677
    internal-label: Commerce on Prem
  - id: cdf0c6dd-1717-4e20-9530-a24eee57088b
    internal-label: Commerce on Cloud
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '1332'
ht-degree: 0%
---

# Überwachung des Synchronisierungsstatus der Katalogansicht

Verwenden Sie die Seite „Synchronisierungsstatus von Katalogansicht“, um die Synchronisierung zu überwachen und Katalogansichten zu beheben, die für Adobe Commerce Optimizer projiziert wurden. Für jeden benutzerdefinierten freigegebenen Katalog erstellt der [!DNL Adobe Commerce Optimizer Connector for B2B] eine Katalogansicht für jede Shop-Ansicht innerhalb des Website-Bereichs des freigegebenen Katalogs. Jede Katalogansicht ist mit einer Sortimentrichtlinie, dem verknüpften Preisbuch und dem öffentlichen Schlüssel konfiguriert, der zum Überprüfen von Token mit eingeschränktem Zugriff verwendet wird. Adobe Commerce behält die entsprechenden Katalogansichtsmetadaten bei, einschließlich des privaten Schlüssels und der standardmäßigen Preisbuch-ID.

>[!NOTE]
>
>Um den Synchronisierungsstatus für Katalogdaten-Feeds zu verfolgen, verwenden Sie die Seite [[!UICONTROL Data Feed Sync Status]](data-feed-sync-status.md) .

## Zielgruppe und Verfügbarkeit {#audience}

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce auf Cloud-Infrastruktur- und lokale Projekte."}

Die [!UICONTROL Catalog View Sync Status]-Seite ist für Adobe Commerce in Cloud-Infrastruktur und lokale Händler verfügbar, die freigegebene B2B-Kataloge mit der [!DNL Adobe Commerce Optimizer Connector for B2B]-Integration verwenden. Die Seite wird automatisch installiert und aktiviert, wenn die Connector-Erweiterung installiert wird.

## Rufen Sie die Seite Katalogansicht - Synchronisierungsstatus auf {#access-catalog-view-sync-status-page}

Navigieren Sie im Admin-Bereich zu **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Catalog View Sync Status]**.

![Die Seite „Katalogansicht - Synchronisationsstatus“ enthält Katalogansichten mit ihrem Synchronisationsstatus](assets/catalog-view-sync-status.png){width="600" zoomable="yes"}

Die Seite weist drei Registerkarten auf:

- **[!UICONTROL Catalog Views]** - Vom Connector erstellte Katalogansichten mit jeweiligem Synchronisierungsstatus. Siehe [Zusammenfassung des Synchronisierungsstatus der Katalogansicht](#catalog-view-sync-status-summary).
- **[!UICONTROL Orphaned in ACO]** - Entitäten, die in [!DNL Adobe Commerce Optimizer] ohne entsprechende [!DNL Adobe Commerce] vorhanden sind. Siehe [Verwaist in ACO-Registerkarte](#orphaned-in-aco-tab).
- **[!UICONTROL Deleted]** - Ein Datensatz mit Projektionen der Katalogansicht, die entfernt wurden, weil ihr freigegebener Katalog gelöscht wurde. Siehe [Registerkarte „Gelöscht](#deleted-tab).

## Zusammenfassung des Synchronisationsstatus der Katalogansicht {#catalog-view-sync-status-summary}

Zusammenfassungskarten oben auf der Seite zeigen die Anzahl der Katalogansichten in jedem Zustand sowie die Anzahl der eingeschränkten Zugriffsschlüssel, die innerhalb von 30 Tagen ablaufen:

| Karte | Beschreibung |
| --- | --- |
| **Gesund** | Katalogansichten ohne erkennbare Abweichung. |
| **Degraded** | Katalogansichten mit reparierbarer Drift. |
| **fehlgeschlagen** | Katalogansichten, die nie erstellt oder direkt in [!DNL Adobe Commerce Optimizer] gelöscht wurden. |
| **Tasten ≤ 30d** | Eingeschränkte Zugriffsschlüssel, die innerhalb von 30 Tagen ablaufen. |

Das Raster listet eine Zeile pro Katalogansicht auf:

| Feld | Beschreibung |
| --- | --- |
| **Katalogansicht** | Die Kennung der in [!DNL Adobe Commerce Optimizer] projizierten Katalogansicht. |
| **Source** | Der freigegebene Katalog, von dem aus die Katalogansicht projiziert wurde. Klicken Sie auf den Link, um den freigegebenen Katalog im Admin-Bereich zu öffnen. |
| **Store-Ansicht** | Die Store-Ansicht, die die Katalogansicht darstellt. |
| **Firmen** | Die Anzahl der Firmen, die derzeit mit dieser Katalogansicht verknüpft sind. |
| **Status** | Der allgemeine Synchronisierungsstatus der Katalogansicht. Siehe [Statuswerte synchronisieren](#sync-status-values). |
| **Richtlinie** | Gibt an, ob die dieser Katalogansicht zugewiesene Sortimentrichtlinie mit Ihrer [!DNL Adobe Commerce] übereinstimmt. |
| **Preisbuch** | Gibt an, ob das dieser Katalogansicht zugewiesene Preisbuch Ihrer [!DNL Adobe Commerce] entspricht. |
| **Zugriffsschlüssel** | Ob dieser Katalogansicht ein eingeschränkter Zugriffsschlüssel zugeordnet ist. |
| **Schlüssel läuft ab** | Das Ablaufdatum des eingeschränkten Zugriffsschlüssels der Katalogansicht und die Anzahl der verbleibenden Tage. |
| **Drift** | Die Art der festgestellten Drift, falls vorhanden. |
| **Zuletzt abgestimmt** | Wann diese Katalogansicht zuletzt im Abstimmungsprozess überprüft wurde. |
| **Aktion** | **[!UICONTROL View details]** öffnet die Detailseite für den Synchronisationsstatus des Katalogs, um den aktuellen Status, die Drift, Zugriffsschlüssel und aktuelle Ereignisse anzuzeigen. **[!UICONTROL Open in ACO admin]** öffnet die Detailseite für die Katalogansicht in [!DNL Adobe Commerce Optimizer] Studio. **[!UICONTROL Copy ID]** kopiert die Katalogansichts-ID als Referenz. Siehe [Abgleich und Reparieren von Drift](#reconcile-and-repair-drift). |

## Statuswerte synchronisieren {#sync-status-values}

| Status | Bedeutung |
| --- | --- |
| **Gesund** | Keine Drift erkannt. Katalogansicht, Richtlinie, Preiskatalog und Schlüssel stimmen mit Ihrer [!DNL Adobe Commerce]-Konfiguration überein. |
| **Degraded** | Drift wurde erkannt und ist reparierbar - zum Beispiel wurde ein Policy- oder Preisbuch direkt in [!DNL Adobe Commerce Optimizer] geändert. |
| **fehlgeschlagen** | Die Katalogansicht wurde nie erstellt oder direkt in [!DNL Adobe Commerce Optimizer] gelöscht. |
| **Ausstehend** | Die Katalogansicht wurde noch nicht abgestimmt oder wartet auf ihre erste Projektion. |
| **Einstellung** | Der freigegebene Katalog wurde in [!DNL Adobe Commerce] gelöscht und die Katalogansicht befindet sich innerhalb der Übergangsphase für die Löschung. |
| **Gelöscht** | Die Projektion für die Katalogansicht wurde nach Ablauf der Übergangsphase entfernt. Er wird 90 Tage lang als Datensatz auf der Registerkarte &quot;[!UICONTROL Deleted]&quot; gespeichert. |
| **Verwaist** | Die Katalogansicht oder der Schlüssel ist in [!DNL Adobe Commerce Optimizer] vorhanden, hat jedoch keine entsprechende [!DNL Adobe Commerce]. Siehe [Verwaist in ACO-Registerkarte](#orphaned-in-aco-tab). |

### Konfigurieren der Übergangsphase für Löschungen {#configure-the-deletion-grace-period}

Die Übergangsphase für die Löschung gibt das Datenaufbewahrungsfenster für Katalogansichten und zugehörige Daten an, nachdem der zugehörige freigegebene Katalog gelöscht wurde. Der Standardwert ist 7 Tage.
Nach Ablauf des Fensters werden alle Daten entfernt.

#### Ändern der Datenspeicherungseinstellung

1. Öffnen Sie die [!DNL Adobe Commerce] Admin.

1. Wählen Sie im **[!UICONTROL Stores]** Menü **[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Catalog View Sync]** > **[!UICONTROL Deletion]** > **[!UICONTROL Deletion Grace Period (days)]** aus.

1. Aktualisieren Sie den **[!UICONTROL Deletion Grace Period (days)]** nach Bedarf.

   Um eine ACO-Projektion einer Katalogansicht sofort nach dem Löschen eines freigegebenen Katalogs zu entfernen, setzen Sie diesen Wert auf `0`.

1. Wählen Sie **[!UICONTROL Save Config]** aus.

Weitere Informationen finden Sie unter [Services > ACO Catalog View Sync](../configuration-reference/services/aco-catalog-view-sync.md) für alle verfügbaren Sync- und Drift-Abstimmungseinstellungen.

## Anpassen und Reparieren von Konfigurationsunterschieden {#reconcile-and-repair-drift}

[!DNL Adobe Commerce] ist die maßgebliche Quelle für die Projektion des B2B-Shared-Katalogs. Bei der Abstimmung wird die [!DNL Adobe Commerce] mit der [!DNL Adobe Commerce Optimizer] verglichen und etwaige Unterschiede werden berichtet bzw. behoben.

>[!IMPORTANT]
>
>Änderungen, die direkt [!DNL Adobe Commerce Optimizer] einer vom Connector verwalteten Katalogansicht, Richtlinie, Preisliste oder Schlüssel vorgenommen werden, sind nicht die primäre Quelle der Wahrheit. Bei der Abstimmung werden diese Konfigurationsunterschiede als Konfigurationsunterschiede ausgewertet. Nach der Reparatur werden sie auf die [!DNL Adobe Commerce] zurückgesetzt. Nehmen Sie Konfigurationsänderungen in [!DNL Adobe Commerce] vor, nicht in [!DNL Adobe Commerce Optimizer]. Die Reparatur entfernt keine Richtlinien, die Sie manuell neben der vom Connector verwalteten Richtlinie hinzugefügt haben.

Verwenden Sie die Schaltflächen auf Seitenebene, um Folgendes abzustimmen:

- **[!UICONTROL Reconcile]** - Überprüft auf Konfigurationsunterschiede und aktualisiert den Synchronisierungsstatus, ohne Änderungen an [!DNL Adobe Commerce Optimizer] vorzunehmen.

- **[!UICONTROL Reconcile & Repair]** - Prüft auf Konfigurationsunterschiede und stellt die erwartete Konfiguration für alle reparierbaren Unterschiede automatisch wieder her.

  Bei Auswahl von **[!UICONTROL Reconcile & Repair]** wird eine asynchrone Abstimmanforderung gesendet, die vor Ausführung der Reparatur zurückgegeben wird. Eine Bestätigungsmeldung besagt, dass der Status in Kürze aktualisiert wird, die Seite jedoch nicht automatisch neu geladen wird. Warten Sie, bis die Verarbeitung abgeschlossen ist, und aktualisieren Sie dann das Raster, um das Ergebnis zu überprüfen.

Verwenden Sie das **[!UICONTROL Action]** Menü in einer Zeile, um:

- **[!UICONTROL View details]** - Öffnet die Detailseite für den Synchronisationsstatus des Katalogs, um den aktuellen Status, die Drift, die Zugriffsschlüssel und die letzten Ereignisse anzuzeigen.
- **[!UICONTROL Open in ACO admin]** - Öffnen Sie die Detailseite für die Katalogansicht in [!DNL Adobe Commerce Optimizer] Studio.
- **[!UICONTROL Copy ID]** - Kopieren Sie die Katalogansichts-ID als Referenz.

## Verwaist auf der Registerkarte ACO {#orphaned-in-aco-tab}

Auf der Registerkarte **[!UICONTROL Orphaned in ACO]** werden Katalogansichten und Schlüssel mit eingeschränktem Zugriff aufgelistet, die in [!DNL Adobe Commerce Optimizer] vorhanden sind, aber keine entsprechende [!DNL Adobe Commerce] haben - beispielsweise Entitäten, die manuell in [!DNL Adobe Commerce Optimizer] Studio und nicht vom Connector erstellt wurden. Diese Entitäten können nicht im Hauptraster angezeigt werden, da kein [!DNL Adobe Commerce] vorhanden ist, mit dem sie abgeglichen werden können.

![Verwaist in der ACO-Registerkarte, auf der Entitäten ohne Adobe Commerce-Quelle aufgelistet sind](assets/catalog-view-sync-orphan.png){width="600" zoomable="yes"}

| Feld | Beschreibung |
| --- | --- |
| **Typ** | Die Kategorie der verwaisten Entität: [!UICONTROL Catalog View] oder [!UICONTROL Access Key]. |
| **ACO-ID** | Die Kennung der Entität in [!DNL Adobe Commerce Optimizer]. |
| **Detail** | Zusätzlicher Kontext zur Entität, z. B. ihre Richtlinie. |
| **Zuerst gesehen** | Bei der ersten Erkennung der Abstimmung wurde diese Entität erkannt. |
| **Aktion** | Wählen Sie **[!UICONTROL Copy ID]** aus, um die Entitätskennung zu kopieren. Verwenden Sie die kopierte ID, um die Entität in [!DNL Adobe Commerce Optimizer] Studio-Katalogansichten zu finden und zu entfernen. |

>[!NOTE]
>
>Diese Registerkarte ist nur für Berichte verfügbar. Bei der Abstimmung werden verwaiste Entitäten nie gelöscht. Entfernen Sie sie direkt in [!DNL Adobe Commerce Optimizer] Studio, wenn sie nicht mehr benötigt werden.

## Registerkarte „Gelöscht“ {#deleted-tab}

Auf der Registerkarte **[!UICONTROL Deleted]** werden Katalogansichtsprojektionen aufgelistet, die entfernt wurden, weil ihr freigegebener Katalog in [!DNL Adobe Commerce] gelöscht wurde. Da der freigegebene Katalog und seine Katalogansicht nicht mehr vorhanden sind, werden diese Zeilen nirgends verknüpft. Sie werden nur aufbewahrt, um zu dokumentieren, was entfernt wurde.

![Registerkarte „Gelöscht“ mit Katalogansichtsprojektionen, die entfernt wurden, nachdem ihr freigegebener Katalog gelöscht wurde](assets/catalog-view-sync-deleted.png){width="600" zoomable="yes"}

| Feld | Beschreibung |
| --- | --- |
| **Katalogansicht** | Die Kennung der entfernten Katalogansicht. |
| **Source** | Der gelöschte freigegebene Katalog. |
| **Store-Ansicht** | Die Store-Ansicht, die die Katalogansicht darstellt. |
| **gelöscht um** | Beim Entfernen der Projektion. |

Zeilen auf dieser Registerkarte werden nach 90 Tagen automatisch gelöscht.

## Bekannte Einschränkungen

- In [!DNL Adobe Commerce Optimizer] Studio gibt es keinen visuellen Indikator, der Connector-verwaltete Katalogansichten von manuell erstellten unterscheidet. Verwenden Sie diese Seite, nicht die [!DNL Adobe Commerce Optimizer] Studio-Benutzeroberfläche, um zu bestimmen, was der Connector verwaltet.
- Die Spalte **[!UICONTROL ACO ID]** der Registerkarte **[!UICONTROL Orphaned in ACO]** identifiziert eine Katalogansicht, eine Richtlinie oder einen Zugriffsschlüssel und keine eindeutige Kennung. Die Spaltenbenennung kann sich ändern.

>[!MORELIKETHIS]
>
> - [Konfiguration der Katalogansicht verwalten](/help/b2b/catalog-views-manage.md) - Überprüfen Sie Katalogansichten aus dem freigegebenen Katalog oder dem Unternehmenskonto
> - [Synchronisierungsstatus des Daten-Feeds](data-feed-sync-status.md)
> - [Services > ACO Catalog View Sync](../configuration-reference/services/aco-catalog-view-sync.md) — Konfigurieren der Übergangsperioden für das Löschen und die Erstellung sowie des Drift-Abstimmers
> - [Verwaltung von eingeschränkten Zugriffsschlüsseln](restricted-access-keys.md) - Verwalten Sie die Schlüssel, deren Gültigkeit auf dieser Seite angezeigt wird
> - [Überwachen der Synchronisierung der Katalogansicht für freigegebene B2B](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/catalog-view-sync-status)Kataloge im *Adobe Commerce Optimizer Connector-Handbuch*
> - [Private Katalogansichten](https://experienceleague.adobe.com/de/docs/commerce/optimizer/setup/private-catalog-view)
> - [Schlüssel mit eingeschränktem Zugriff](https://experienceleague.adobe.com/de/docs/commerce/optimizer/setup/restricted-access-keys)
