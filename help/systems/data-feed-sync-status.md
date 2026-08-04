---
title: Überwachen des Synchronisierungsstatus von Daten-Feeds in Commerce
description: Exporte verfolgen. Diagnose von Synchronisationsproblemen für [!DNL Catalog Service],  [!DNL Live Search],  [!DNL Product Recommendations] und [!DNL Adobe Commerce Optimizer Connector].
feature: Products, Customers, Data Import/Export
role: Admin
level: Beginner
exl-id: 4e1b9da0-450c-4488-8693-1938a948e792
TQID: https://experienceleague.adobe.com/Y8vYxKS-8iX-bCLSJpAiJOItWlJk348bSMWfk1Cgpbg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11id: e1e0219c-f879-479f-8427-888ed2a6e9c2id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 424b379815ffbf818c2490d0195bf0bf7dd51ab7
workflow-type: tm+mt
source-wordcount: 1664
ht-degree: 0%

---


# Überwachung des Synchronisierungsstatus von Daten-Feeds

Auf der [!UICONTROL Data Feed Sync Status] Seite können Commerce-Admins den Exportzustand für Produkt- und Kategoriedaten-Feeds im Admin-Bereich überwachen.

## Zielgruppe und Verfügbarkeit {#audience}

Die Seite Status der Daten-Feed-Synchronisierung steht Commerce-Händlern mit einer aktiven Lizenz für einen der folgenden Services ohne zusätzliche Kosten zur Verfügung:

- [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)
- [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview)
- [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview)
- [[!DNL Adobe Commerce Optimizer Connector]](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/overview)

Die Seite Status der Daten-Feed-Synchronisierung ist in unterstützten Commerce-Service-Konfigurationen automatisch verfügbar. Wenn auf Adobe Commerce in Cloud-Infrastrukturen und On-Premise-Bereitstellungen die Seite fehlt, nachdem ein entsprechender Service oder Connector aktiviert wurde, befolgen Sie die folgenden manuellen Installationsanweisungen. Verwenden Sie nicht das Installationsverfahren von Composer für produktverwaltete SaaS-Erlebnisse.

## Aufrufen der Synchronisierungsstatus-Seite {#access-data-feed-sync-status-page}

Navigieren Sie im Admin-Bereich zu **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]**.

![Seite „Status der Daten-Feed-Synchronisierung“ mit einer Zusammenfassung der Daten-Feed-Exportaktivität](assets/data-feed-sync-status.png){width="600" zoomable="yes"}

>[!NOTE]
>
> Auf dieser Seite wird nur der Exportstatus angezeigt. Ein Erfolgsstatus bedeutet, dass Daten erfolgreich exportiert wurden - es wird nicht bestätigt, dass Daten in Connected Services verfügbar sind. Detaillierte [ finden Sie unter „Bestätigen von Daten ](#confirm-data-in-connected-services) verbundenen Services“.

## Verfügbare Export-Feeds

Die Liste der verfügbaren Export-Feeds, die Sie auf der Seite Datensynchronisierungsstatus verwalten können, hängt davon ab, welche Commerce-Services verbunden sind.

- **Für [!DNL Adobe Commerce on Cloud, On Premises, and Commerce as a Cloud Service] mit konfigurierten Commerce-Services:** Siehe [Unterstützte Feeds](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/reference/feed-table-reference#supported-feeds) im _SaaS-Datenexporthandbuch_.

- **Für Cloud- oder On-Premise-Bereitstellungen von Adobe Commerce, die mit dem konfiguriert sind[!DNL Adobe Commerce Optimizer Connector]:** Siehe [Unterstützte Feeds](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/reference/connector-reference#supported-feeds) im _Adobe Commerce Optimizer Connector-Handbuch_.


## Zusammenfassung des Synchronisierungsstatus von Daten-Feeds {#data-feed-sync-status-summary}

Das Zusammenfassungsraster listet jeden Feed und seine Exportanzahl auf.

| Feld | Beschreibung |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Feed-Name** | Feed-Indexer für ein Unternehmen oder einen Teil eines Unternehmens (Produkt, Produktpreis). |
| **Source-Datensätze** | Anzahl der Commerce-Datensätze, die synchronisiert werden müssen. Kann die Anzahl der Admin-Raster überschreiten, da Feed-Elemente im Umfang enthalten sind (z. B. Code für Store-Ansicht). |
| **Datensätze erfolgreich gesendet** | Anzahl der Feed-Elemente, die erfolgreich von Commerce an den konfigurierten Service-Endpunkt gesendet wurden. Dies bestätigt nicht die Verfügbarkeit der nachgelagerten Aufnahme oder des Katalogs. Wenn Synchronisierungsfehler aufgetreten sind, kann diese Anzahl kleiner sein als die Anzahl der Quelldatensätze. |
| **Fehlgeschlagene Datensätze** | Anzahl der Datensätze, die nicht an verbundene Commerce-Services gesendet werden konnten. |
| **Aktion** | Wählen Sie **[!UICONTROL Details]** aus, um die Synchronisierungsaktivität für einen Feed anzuzeigen. |

## Details zum Synchronisierungsstatus von Daten-Feeds {#data-feed-sync-status-details}

Wählen Sie auf der Zusammenfassungsseite einen Feed-Namen aus oder wählen Sie **[!UICONTROL Details]** aus, um den Exportstatus für jedes Feed-Element anzuzeigen:

![Seite mit Details zum Daten-Feed-Synchronisierungsstatus mit Berichten zum Feed-Elementstatus](assets/data-feed-sync-status-details.png){width="600" zoomable="yes"}

| Feld | Beschreibung |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Feed-Element-ID** | Automatisch generierte Kennung für Systemzwecke |
| **Entitäts-ID** | Die eindeutige Kennung der Quellentität (Produkt-ID, Kategorie-ID usw.) |
| **Feed-Kennungen** | Eindeutige Kennungen für das Feed-Element. Beispiel: SKU und Store-Ansicht-Code für den Produkt-Feed. Die Werte variieren je nach Feed. |
| **Exportstatus** | Der [Synchronisationsstatus](#export-status-types) des Feed-Elements mit farbcodierten Indikatoren |
| **Letztes Synchronisationsdatum** | Datum und Uhrzeit des letzten Exportversuchs oder der letzten Übermittlung durch Commerce. Dieser Zeitstempel bestätigt nicht die nachgelagerte Verfügbarkeit. |
| **Wird die Entität gelöscht?** | Gibt an, ob die Entität in Adobe Commerce gelöscht wurde. Gelöschte Elemente werden nur angezeigt, wenn die Synchronisierung fehlgeschlagen ist. |
| **Anfrage-ID** | Eindeutige ID für die Synchronisierungsanfrage. Bereitstellen an den Support bei der Fehlerbehebung bei Entitätsaktualisierungen. |
| **Fehler** | Detaillierte Fehlerinformationen zu Synchronisierungsfehlern |

Sie können die Ansicht mit den folgenden Steuerelementen verwalten:

- [!UICONTROL Mass Action] für ausgewählte Feed-Elemente die Neusynchronisierung planen
- [!UICONTROL Filters] und [!UICONTROL Columns]
- [!UICONTROL Default View] zum Erstellen und Speichern einer gefilterten Ansicht und zum Wechseln zwischen Ansichten

### Indikatoren für die Futtermittelgesundheit {#feed-health-indicators}

| **Indikator** | **Beschreibung** |
| ------------- | --------------- |
| Indexerstatus | <ul><li>**Bereit**: Der Indexer ist auf dem neuesten Stand. Keine Neuindizierung erforderlich.</li><li>**Neuindizierung erforderlich**: Source-Daten geändert. Führen Sie eine Neuindizierung aus, um die letzten Änderungen zu erfassen.</li><li>**Verarbeitung**: Indizierung läuft.</li></ul> |
| Changelog-Rückstand | <ul><li>**Alle synchronisiert**: Keine ausstehenden Änderungen zu verarbeiten.</li><li>**Elemente im**: Anzahl der ausstehenden Änderungen, die darauf warten, verarbeitet zu werden. Ein Auftragsbestand von mehr als 1.000 Elementen kann auf Leistungsprobleme hinweisen.</li></ul> |
| Indexermodus | <ul><li>**Zeitplanmodus** (empfohlen): Der Indexer wird planmäßig ausgeführt, was das Risiko von Datenverlust reduziert.</li><li>**Aktualisierung beim Speichern** (in Echtzeit): Wird auf der Seite als Warnung angezeigt. Der Echtzeitmodus wird nicht erwartet und erhöht das Risiko von Datenverlust unter Last.</li></ul> |

>[!TIP]
>
> Weitere Informationen zur Indexverarbeitung finden Sie unter [Indexverwaltung](index-management.md).

### Statusarten exportieren {#export-status-types}

| **Status** | **Beschreibung** | **Aktion erforderlich** |
| ----------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------------ |
| **An Service gesendet** | Das Feed-Element wurde erfolgreich von Commerce zur nachgelagerten Verarbeitung übermittelt. | Keine |
| **Fehlgeschlagen, wird erneut versucht** | Senden fehlgeschlagen, das System versucht jedoch, erneut zu senden. | Monitor für Auflösung |
| **Fehlgeschlagen, erfordert Aufmerksamkeit** | Fehlgeschlagen aufgrund eines Anwendungs- oder Datenfehlers. | Untersuchen und Beheben des Problems in der Spalte [!UICONTROL Error] |
| **Warten auf Übermittlung** | Änderungen im Änderungsprotokoll erkannt, aber noch nicht verarbeitet. | Normaler Verarbeitungsstatus |

## Überwachen des Daten-Feed-Status

Wenn Sie produkt- und kategoriebezogene Entitäten in der Commerce-Datenbank aktualisieren, werden die Daten entsprechend Ihrer Feed-Konfiguration an Commerce-Services übertragen. Sie können die Exportaktivität und ihren aktuellen Status über die Seite [!UICONTROL Data Feed Sync Status] überwachen.

>[!IMPORTANT]
>
> Die Dauer der Datensynchronisation hängt von der Größe des Katalogs, dem Volumen der aktualisierten Daten und der Leistung des externen Services ab.

Wenn die Anzahl der erfolgreich gesendeten Nachrichten mit der Quellanzahl für einen Feed übereinstimmt und keine Elemente mehr auf die Übermittlung warten oder fehlgeschlagen sind, hat Commerce den Export für diesen Feed abgeschlossen. Verwenden Sie das entsprechende Dashboard, um [nachgelagerte Verfügbarkeit zu ](#confirm-data-in-connected-services).

>[!NOTE]
>
> Adobe bietet außerdem Befehlszeilenschnittstellen-Tools und Systemprotokolle, die Entwickler und Systemintegratoren verwenden können, um Synchronisierungsvorgänge zu verwalten und zu verfolgen. Weitere Informationen finden Sie im [SaaS-Datenexporthandbuch](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview).

### Fehlgeschlagene Exporte verwalten {#manage-failed-exports}

So überprüfen Sie fehlgeschlagene Exporte und planen eine Neusynchronisierung:

1. Suchen Sie auf der Zusammenfassungsseite den Feed mit fehlgeschlagenen Datensätzen.
1. Wählen Sie **[!UICONTROL Details]** aus.
1. Überprüfen Sie die Fehlermeldungen in der Spalte [!UICONTROL Error] .
1. Aktivieren Sie die Kontrollkästchen der Datensätze, die neu synchronisiert werden sollen.
1. Wählen Sie im Menü [!UICONTROL Mass Action] die Option **[!UICONTROL Schedule Resync]** aus, wählen Sie **[!UICONTROL Submit]** aus und bestätigen Sie den Vorgang.
1. Statusänderungen auf der Detailseite überwachen.

Das System versucht automatisch, bestimmte Fehler erneut auszuführen.

#### Zeitpunkt der manuellen Neusynchronisierung {#resync-feed-items}

Führen Sie in folgenden Fällen eine manuelle Neusynchronisierung durch:

- Authentifizierungs- oder Berechtigungsfehler (401- oder 403-Status-Codes) bestehen fort
- Es wurden Datenformatprobleme behoben, die zu Payload-Fehlern führten
- Konfiguration externer Services oder Endpunkte wurden geändert
- Es wurden Anpassungen bereitgestellt, die sich auf den Datenexport auswirken

### Bestätigen von Daten in Connected Services {#confirm-data-in-connected-services}

Um die End-to-End-Synchronisierung nach Abschluss der Exporte zu überprüfen, verwenden Sie eine der folgenden Methoden. Die Beschränkungen des Exportstatus auf dieser Seite finden Sie unter [Hinweis oben](#export-status-scope).

- **[!DNL Adobe Commerce as a Cloud Service]mit Commerce-Services:** Überprüfen Sie das entsprechende [Data Management Dashboard](data-dashboard.md), um die nachgelagerte Verfügbarkeit zu bestätigen.
- **Adobe Commerce on Cloud oder On-Premise mit Adobe Commerce Optimizer Connector**: Überprüfen Sie zuerst den Exportstatus für Commerce Admin und dann die Seite [Datensynchronisierung](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/data-sync) in [!DNL Commerce Optimizer Studio]
- **[!DNL Adobe Commerce Optimizer](eigenständig):** Daten werden nicht aus dem Commerce-Backend exportiert. Verwenden Sie die [Datensynchronisierungsseite](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/data-sync) in [!DNL Commerce Optimizer Studio], um die Verfügbarkeit der Daten zu bestätigen.

>[!TIP]
>
> Weitere Informationen zum Datensynchronisierungsprozess finden Sie unter [Synchronisieren von Daten mit dem SaaS](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/data-synchronization/data-sync-manage#view-and-manage-the-synchronization-process)Datenexport im *SaaS-Datenexporthandbuch*.

## Best Practices {#best-practices}

- Die Zusammenfassungsseite für Feeds mit hohen Fehlerquoten wird täglich überprüft.
- Untersuchen Sie wöchentlich Details zu kritischen Feeds wie Produkten und Preisen.
- Verfolgen Sie monatlich die Trends des Exporterfolgs, um wiederkehrende Probleme zu identifizieren.

## Beheben häufiger Probleme {#troubleshoot-common-issues}

| Problem | Symptome | Vorgehensweise |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Hohe Ausfallraten | Viele Datensätze zeigen den Status *Fehlgeschlagen, Aufmerksamkeit erforderlich* an | <ul><li>Status und Konfiguration des externen Services überprüfen</li><li>Prüfen Sie die Fehlermeldungen auf Muster in der Spalte [!UICONTROL Error] .</li><li>Nachdem Sie das zugrunde liegende Problem behoben haben, lesen Sie [Verwalten und Resynchronisieren fehlgeschlagener Exporte](#manage-failed-exports)</li><li>Wenden Sie sich bei Bedarf an den externen Support</li></ul> |
| Langsame Exportleistung | Hoher Änderungsrückstand oder langsame Statusaktualisierungen | <ul><li>Prüfen Sie [feed health indicators](#feed-health-indicators) auf Indexer und Rückstandsstatus</li><li>Indizierung erneut ausführen, wenn **Reindex required** angezeigt wird</li><li>Überwachen der Reaktionszeiten externer Services</li><li>Planen Sie Exporte nach Möglichkeit außerhalb der Spitzenzeiten</li><li>Überprüfen der Systemressourcen und -leistung</li></ul> |
| Authentifizierungsfehler | 401- oder 403-Status-Codes in der Spalte [!UICONTROL Error] | <ul><li>API-Anmeldeinformationen und Token überprüfen</li><li>Prüfen der Berechtigungen für externe Dienstkonten</li><li>Verlängern Sie abgelaufene Token oder wenden Sie sich an Ihren Dienstleister</li><li>Nachdem die Anmeldeinformationen wiederhergestellt wurden, [betroffenen Datensätze neu synchronisiert](#manage-failed-exports)</li></ul> |
| Fehlende Seite „Synchronisierungsstatus für Daten-Feed“ | **[!UICONTROL Data Feed Sync Status]** wird nach der Aktivierung eines Connected Services nicht unter **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** aufgeführt | <ul><li>Bestätigen Sie für Commerce as a Cloud Service, dass ein berechtigter Service aktiviert ist (siehe [Zielgruppe und Verfügbarkeit](#audience))</li><li>Nur für Commerce in der Cloud oder On-Premise ([ Sie die Erweiterung manuell](#install-the-extension)</li></ul> |

Adobe Commerce in der Cloud-Infrastruktur oder lokal: Vergewissern Sie sich, dass ein berechtigter Service oder der Adobe Commerce Optimizer-Connector aktiviert ist. Wenn die Seite noch fehlt, befolgen Sie die manuellen Installationsanweisungen.
ACCS oder Adobe Commerce Optimizer: Installieren Sie das Modul nicht manuell. Verwenden Sie die produktverwaltete Synchronisierung oder wenden Sie sich an das entsprechende Service-Supportteam.

## Installieren der Erweiterung {#install-the-extension}

Eine manuelle Installation ist für Adobe Commerce in Cloud- oder On-Premise-Bereitstellungen nur erforderlich, wenn die [!UICONTROL Data Feed Sync Status] im Admin-Bereich fehlt, nachdem Sie einen geeigneten Service aktiviert haben. Siehe [Zielgruppe und Verfügbarkeit](#audience).

### Voraussetzungen

- Adobe Commerce 2.4.4+. Detaillierte Anforderungen finden Sie unter [Systemanforderungen](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/system-requirements).
- [Adobe Commerce-Datenexporterweiterung](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/reference/manage-extension), Version 103.4.15 oder höher
- Authentifizierungsschlüssel mit der Berechtigung zum Herunterladen des erforderlichen Pakets aus dem Adobe Commerce-Repository. Informationen zum Erstellen von Authentifizierungsschlüsseln und zum Abrufen des erforderlichen Paketzugriffs finden Sie unter [Abrufen Ihrer Authentifizierungsschlüssel](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). Informationen zu Cloud-Installationen finden Sie im Handbuch zu [Commerce in Cloud-Infrastrukturen](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/authentication-keys).
- Zugriff auf die Befehlszeile des Adobe Commerce-Anwendungsservers.

### Installationsschritte

Fügen Sie das Modul `magento/module-data-exporter-status` mit dem Composer hinzu:

```shell
composer require magento/module-data-exporter-status
```

Detaillierte Informationen zu den Installationsschritten finden Sie in den folgenden Handbüchern:

- [Installieren der Erweiterung für Adobe Commerce in der Cloud-Infrastruktur](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure-store/extensions)
- [Installieren der Erweiterung auf Adobe Commerce On-Premise](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/tutorials/extensions)

>[!MORELIKETHIS]
>
> - [Daten-Management-Dashboard](data-dashboard.md)
> - [SaaS-Datenexport-Handbuch](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview)
