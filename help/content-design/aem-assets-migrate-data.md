---
title: Migrieren von Mediendateien zu AEM
description: Migrieren Sie die Mediendateien aus Adobe Commerce oder einer externen Quelle in das AEM Assets-DAM.
feature: CMS, Media, Integration
exl-id: fead5732-b014-4cd3-a776-98a055a696ab
TQID: https://experienceleague.adobe.com/2eqYvVrxPO-yFYKtRPUExzxPPxXUy1v9KhR4LYjIBZY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: da3860b0-d637-47df-bef0-273751180266
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 892
ht-degree: 0%

---

# Migrieren von Mediendateien in das AEM Assets-DAM

Sowohl Adobe Commerce als auch Adobe Experience Manager (AEM) bieten integrierte Funktionen zur Optimierung der Migration von Mediendateien von Commerce zum Digital Asset Management System (DAM) von AEM Assets. Sie können auch Mediendateien aus anderen Quellen migrieren.

## Voraussetzungen

| Kategorie | Anforderung |
|----------|-------------|
| **Systemanforderungen** | <ul><li>AEM as a Cloud Service-Umgebung mit AEM Assets bereitgestellt</li><li>Ausreichende Speicherkapazität</li><li>Netzwerkbandbreite für große Dateiübertragungen</li></ul> |
| **Erforderlicher Zugriff und Berechtigungen** | <ul><li>Administratorzugriff auf AEM Assets as a Cloud Service</li><li>Zugriff auf das Quellsystem, in dem Mediendateien gespeichert werden (Adobe Commerce oder externes System)</li><li>Entsprechende Berechtigungen für den Zugriff auf Cloud-Speicher-Services</li></ul> |
| **Cloud-Speicherkonto** | <ul><li>AWS S3- oder Azure Blob Storage-Konto</li><li>Konfiguration von privaten Containern/Buckets</li><li>Authentifizierungsdaten</li></ul> |
| **Source-Inhalte** | <ul><li>Organisierte Mediendateien bereit für die Migration</li><li>Bild- und Videodateien in <a href="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/file-format-support#image-formats">von AEM Assets unterstützten Formaten</a>.</li><li>Bereinigen, deduplizierter Assets</li></li> |
| **Metadatenvorbereitung** | <ul><li><a href="https://experienceleague.adobe.com/de/docs/commerce-admin/content-design/aem-asset-management/getting-started/aem-assets-configure-aem">AEM Assets-Metadatenprofil für Commerce-Assets konfiguriert</a></li><li>Zugeordnete Metadatenwerte für jedes Asset</li><li>CSV-Datei-Editor (z. B. Microsoft Excel)</li></ul> |

## Best Practices für die Migration

1. Kuratieren Sie Assets vor der Migration, indem Sie nicht verwendete und doppelte Inhalte entfernen.
1. Organisieren Sie Assets logisch nach Größe, Format oder Anwendungsfall.
1. Erwägen Sie, große Migrationen in kleinere Batches aufzuteilen.
1. Planung ressourcenintensiver Importe außerhalb der Spitzenzeiten
1. Validieren der Metadatenzuordnung vor dem vollständigen Import

## Migrations-Workflow

Befolgen Sie den Migrations-Workflow, um Mediendateien aus Adobe Commerce oder einem anderen externen System zu exportieren und in das AEM Assets-DAM zu importieren.

### Schritt 1: Exportieren von Inhalten aus der vorhandenen Datenquelle

Für Adobe Commerce-Händler bietet das Remote-Speichermodul eine optimierte Möglichkeit, Mediendateien aus Commerce zu exportieren und in AEM Assets zu importieren. Dieses Modul ermöglicht die Speicherung und Verwaltung von Mediendateien auf Remote-Speicher-Services wie AWS S3, wodurch der Migrationsprozess effizienter wird. Informationen zum Einrichten des Remote-Speichers für Ihre Commerce-Instanz finden Sie unter [Konfigurieren des Remote](https://experienceleague.adobe.com/de/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage-aws-s3) im *Commerce-Konfigurationshandbuch*.

Wenn Sie Mediendateien haben, die außerhalb von Adobe Commerce gespeichert sind, laden Sie sie direkt in eine der [Datenquellen](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/assets-view/bulk-import-assets-view#prerequisites) hoch, die von AEM as a Cloud Service unterstützt werden.

### Schritt 2: Erstellen einer CSV-Datei für die Metadatenzuordnung

Erstellen Sie eine Metadatenzuordnungsdatei im CSV-Format und laden Sie sie in den Quellordner hoch, der Ihre Mediendateien enthält. Diese Datei ordnet jedem Asset wesentliche Metadaten zu:

- Organisieren und Kategorisieren von Assets im DAM zur einfachen Erkennung
- Richtige Synchronisierung zwischen Adobe Commerce und AEM Assets aktivieren
- Pflegen von Beziehungen zwischen Assets und Produkten nach der Migration

Geben Sie für jede Mediendatei, die Sie migrieren möchten, Werte für die Metadatenfelder im [AEM Assets-Metadatenprofil für Commerce-Assets &#x200B;](aem-assets-configure-aem.md), wie in der folgenden Tabelle beschrieben.

| Metadaten | Beschreibung | Wert |
|-------|-------------|--------|
| assetPath | Der vollständige Pfad, in dem das Asset im AEM Assets-Repository gespeichert wird.<br><br>Verwenden Sie den Pfad, um Unterordner zu erstellen und Commerce-Assets zu organisieren, z. B. `content/dam/commerce/<brand>/<type>`. | `/content/dam/commerce/<sub-folder>/..<filename>` |
| DC:title | Der Anzeigetitel des Assets in AEM Assets | Zeichenfolgenwert (z. B. `Sample 1`) |
| dam:status | Der Genehmigungsstatus des Assets in AEM Assets | `approved` |
| Handel:positions | Die Position/Reihenfolge des Assets in den Produktkatalogen | Numerischer Wert (z. B. „1„) |
| Handel:isCommerce | Markierung, die angibt, ob das Asset in Commerce verwendet wird | `Yes` |
| Handel:skus | Mit diesem Asset verknüpfte Produkt-SKUs | Zeichenfolgenwert (z. B. `sample1`) |
| Handel:roles | Die Rollen oder Typen von Bildern für das Asset (z. B. `thumbnail`, `main image`, `swatch`) | Mehrere Werte, durch Semikolons getrennt (z. B. „Miniaturansicht; Bild; Farbfeld_Bild; SMALL_IMAGE„) |

+++CSV-Code

Verwenden Sie diesen CSV-Beispielcode, um die Datei in einem Code-Editor oder einer Tabellenkalkulationsprogramm wie Microsoft Excel zu erstellen.

```csv
assetPath,dc:title{{String}},dam:status{{String}},commerce:positions{{String: multi}},commerce:isCommerce{{String}},commerce:skus{{String: multi}},commerce:roles{{String: multi}}
/content/dam/commerce/sample1.jpg,Sample 1,approved,1,Yes,sample1,thumbnail; image; swatch_image; small_image
/content/dam/commerce/sample2.jpg,Sample 2,approved,1,Yes,sample2,thumbnail; image; swatch_image; small_image
/content/dam/commerce/sample3.jpg,Sample 3,approved,1,Yes,sample3,thumbnail; image; swatch_image; small_image
```

+++

### Schritt 3: Massenimport von Assets in AEM Assets

Nachdem Sie die Metadatenzuordnungsdatei erstellt haben, verwenden Sie das Tool für den Massenimport von AEM Assets , um Ihre Assets zu importieren.

Im Folgenden finden Sie einen allgemeinen Überblick über die Verwendung des Tools.

1. [Melden Sie sich bei Ihrer AEM Assets as a Cloud Service-Autorenumgebung &#x200B;](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/onboarding/journey/aem-users#login-aem).

1. Wählen Sie in der Ansicht Experience Manager-Tools die Option **[!UICONTROL Assets]** > **[!UICONTROL Bulk Import]** aus.

   ![AEM Assets-Authoring](./assets/aem-assets-bulk-import-selection.png){width="600" zoomable="yes"}

1. Wählen Sie aus den Massenimportkonfigurationen die Option **[!UICONTROL Create]** aus, um das Konfigurationsformular zu öffnen.

   ![AEM Assets-Authoring](./assets/aem-assets-bulk-import-configuration.png){width="600" zoomable="yes"}

1. Richten Sie die Konfiguration ein und speichern Sie sie.

   Sie benötigen:

   - Authentifizierungsdaten für Ihre Datenquelle
   - Der Zielordner in AEM Assets, in dem importierte Dateien gespeichert werden
   - Informationen über die MIME-Typen, die Dateigröße und andere Parameter zum Anpassen der Importkonfiguration (optional)
   - Der Pfad zur CSV-Datei für die Metadatenzuordnung, die Sie in die Cloud-Speicherinstanz hochgeladen haben.

   Ausführliche Anweisungen finden Sie unter [Konfigurieren des Tools für den Massenimport](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/manage/add-assets#configure-bulk-ingestor-tool) im *AEM Assets as a Cloud Service-Benutzerhandbuch*.

1. Verwenden Sie nach dem Speichern der Konfiguration die Tools für den Massenimport, um den Importvorgang zu testen und auszuführen.

>[!MORELIKETHIS]
>
>[Video-Demo zum Tool für den Massenimport](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/manage/add-assets#asset-bulk-ingestor)
>[Tipps, Best Practices und Einschränkungen](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/manage/add-assets#tips-limitations)
>[Hochladen oder Aufnehmen von Assets mithilfe von APIs](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/admin/developer-reference-material-apis#asset-upload)
