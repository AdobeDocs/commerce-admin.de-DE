---
title: Migrate media files to AEM
description: Migrate the media files from Adobe Commerce or an external source into the AEM Assets DAM.
feature: CMS, Media, Integration
source-git-commit: 094c585b335e5751a1387989d5ba33332c351c57
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# Migrate media files to the AEM Assets DAM

Sowohl Adobe Commerce als auch Adobe Experience Manager (AEM) bieten integrierte Funktionen zur Optimierung der Migration von Mediendateien von Commerce zum Digital Asset Management System (DAM) von AEM Assets. Sie können auch Mediendateien aus anderen Quellen migrieren.

## Voraussetzungen

| Kategorie | Anforderung |
|----------|-------------|
| **Systemanforderungen** | <ul><li>AEM as a Cloud Service-Umgebung mit AEM Assets bereitgestellt</li><li>Ausreichende Speicherkapazität</li><li>Netzwerkbandbreite für große Dateiübertragungen</li></ul> |
| **Erforderlicher Zugriff und Berechtigungen** | <ul><li>Administratorzugriff auf AEM Assets as a Cloud Service</li><li>Zugriff auf das Quellsystem, in dem Mediendateien gespeichert werden (Adobe Commerce oder externes System)</li><li>Appropriate permissions to access cloud storage services</li></ul> |
| **Cloud-Speicherkonto** | <ul><li>AWS S3- oder Azure Blob Storage-Konto</li><li>Konfiguration von privaten Containern/Buckets</li><li>Authentifizierungsdaten</li></ul> |
| **Source Content** | <ul><li>Organized media files ready for migration</li><li>Image and video files in <a href="https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/file-format-support#image-formats">formats supported by AEM Assets</a>.</li><li>Clean, deduplicated assets</li></li> |
| **Metadata Preparation** | <ul><li><a href="https://experienceleague.adobe.com/de/docs/commerce-admin/content-design/aem-asset-management/getting-started/aem-assets-configure-aem">AEM Assets-Metadatenprofil für Commerce-Assets konfiguriert</a></li><li>Zugeordnete Metadatenwerte für jedes Asset</li><li>CSV-Datei-Editor (z. B. Microsoft Excel)</li></ul> |

## Best Practices für die Migration

1. Kuratieren Sie Assets vor der Migration, indem Sie nicht verwendete und doppelte Inhalte entfernen.
1. Organisieren Sie Assets logisch nach Größe, Format oder Anwendungsfall.
1. Erwägen Sie, große Migrationen in kleinere Batches aufzuteilen.
1. Planung ressourcenintensiver Importe außerhalb der Spitzenzeiten
1. Validieren der Metadatenzuordnung vor dem vollständigen Import

## Migrations-Workflow

Follow the migration workflow to export media files from Adobe Commerce or another external system and import them into the AEM Assets DAM.

### Schritt 1: Exportieren von Inhalten aus der vorhandenen Datenquelle

Für Adobe Commerce-Händler bietet das Remote-Speichermodul eine optimierte Möglichkeit, Mediendateien aus Commerce zu exportieren und in AEM Assets zu importieren. Dieses Modul ermöglicht die Speicherung und Verwaltung von Mediendateien auf Remote-Speicher-Services wie AWS S3, wodurch der Migrationsprozess effizienter wird. Informationen zum Einrichten des Remote-Speichers für Ihre Commerce-Instanz finden Sie unter [Konfigurieren des Remote](https://experienceleague.adobe.com/de/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage-aws-s3) im *Commerce-Konfigurationshandbuch*.

Wenn Sie Mediendateien haben, die außerhalb von Adobe Commerce gespeichert sind, laden Sie sie direkt in eine der [Datenquellen](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/assets-view/bulk-import-assets-view#prerequisites) hoch, die von AEM as a Cloud Service unterstützt werden.

### Step 2: Build a CSV file for metadata mapping

Erstellen Sie eine Metadatenzuordnungsdatei im CSV-Format und laden Sie sie in den Quellordner hoch, der Ihre Mediendateien enthält. Diese Datei ordnet jedem Asset wesentliche Metadaten zu:

- Organisieren und Kategorisieren von Assets im DAM zur einfachen Erkennung
- Richtige Synchronisierung zwischen Adobe Commerce und AEM Assets aktivieren
- Pflegen von Beziehungen zwischen Assets und Produkten nach der Migration

Geben Sie für jede Mediendatei, die Sie migrieren möchten, Werte für die Metadatenfelder im [AEM Assets-Metadatenprofil für Commerce-Assets &#x200B;](aem-assets-configure-aem.md), wie in der folgenden Tabelle beschrieben.

| Metadaten | Beschreibung | Wert |
|-------|-------------|--------|
| assetPath | Der vollständige Pfad, in dem das Asset im AEM Assets-Repository gespeichert wird.<br><br>Use the path to create sub-folders to organize Commerce assets, for example `content/dam/commerce/<brand>/<type>`. | `/content/dam/commerce/<sub-folder>/..<filename>` |
| dc:title | Der Anzeigetitel des Assets in AEM Assets | Zeichenfolgenwert (z. B. `Sample 1`) |
| dam:status | Der Genehmigungsstatus des Assets in AEM Assets | `approved` |
| commerce:positions | The position/order of the asset in product galleries | Numeric value (e.g., &quot;1&quot;) |
| commerce:isCommerce | Flag indicating if the asset is used in commerce | `Yes` |
| commerce:skus | Mit diesem Asset verknüpfte Produkt-SKUs | Zeichenfolgenwert (z. B. `sample1`) |
| commerce:roles | Die Rollen oder Typen von Bildern für das Asset (z. B. `thumbnail`, `main image`, `swatch`) | Mehrere Werte, durch Semikolons getrennt (z. B. „Miniaturansicht; Bild; Farbfeld_Bild; SMALL_IMAGE„) |

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

1. [Log in to your AEM Assets as a Cloud Service author environment](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/onboarding/journey/aem-users#login-aem).

1. Wählen Sie in der Ansicht Experience Manager-Tools die Option **[!UICONTROL Assets]** > **[!UICONTROL Bulk Import]** aus.

   ![AEM Assets-Authoring](./assets/aem-assets-bulk-import-selection.png){width="600" zoomable="yes"}

1. Wählen Sie aus den Massenimportkonfigurationen die Option **[!UICONTROL Create]** aus, um das Konfigurationsformular zu öffnen.

   ![AEM Assets-Authoring](./assets/aem-assets-bulk-import-configuration.png){width="600" zoomable="yes"}

1. Richten Sie die Konfiguration ein und speichern Sie sie.

   You&#39;ll need:

   - Authentication credentials for your data source
   - The target folder in AEM Assets where imported files will be stored
   - Information about the MIME types, file size, and other parameters to customize the import configuration (optional)
   - The path to the metadata mapping CSV file you uploaded to the Cloud storage instance.

   Ausführliche Anweisungen finden Sie unter [Konfigurieren des Tools für den Massenimport](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/manage/add-assets#configure-bulk-ingestor-tool) im *AEM Assets as a Cloud Service-Benutzerhandbuch*.

1. Verwenden Sie nach dem Speichern der Konfiguration die Tools für den Massenimport, um den Importvorgang zu testen und auszuführen.

>[!MORELIKETHIS]
>
>[Video-Demo zum Tool für den Massenimport](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/manage/add-assets#asset-bulk-ingestor)
>[Tipps, Best Practices und Einschränkungen](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/manage/add-assets#tips-limitations)
>[Hochladen oder Aufnehmen von Assets mithilfe von APIs](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/admin/developer-reference-material-apis#asset-upload)

