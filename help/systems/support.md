---
title: Support-Tools
description: Erfahren Sie mehr über die bereitgestellten Support-Tools, mit denen Sie Probleme in Ihrem System identifizieren können.
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/bS1CIJI9ZXybrYA-EgekVKjXQhywA6jdpWOM-bvw4Mc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: cc250cf1-34eb-4863-80d0-d170d45ea067
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 566
ht-degree: 0%

---

# Support-Tools

{{ee-feature}}

Die Support-Tools dienen zur Identifizierung bekannter Probleme in Ihrem System. Sie können während der Entwicklungs- und Optimierungsprozesse als Ressource und als Diagnosewerkzeug verwendet werden, um unser Supportteam bei der Identifizierung und Lösung von Problemen zu unterstützen.

## Systemberichte

Mit dem Tool für die Systemberichterstellung können Sie regelmäßig vollständige oder teilweise Momentaufnahmen des Systems erstellen und diese zur späteren Verwendung speichern. Sie können Leistungseinstellungen vor und nach Code-Entwicklungszyklen oder Änderungen an den Server-Einstellungen vergleichen. Das System-Reporting-Tool kann den Zeitaufwand für die Vorbereitung und Übermittlung der vom Support benötigten Informationen für den Beginn einer Untersuchung erheblich reduzieren.

Über das Raster Systemberichte können Sie vorhandene Berichte anzeigen und herunterladen, Berichte löschen und Berichte erstellen.

### Zugriff auf Systemberichte

Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![Admin - System Reports](./assets/reports.png){width="600" zoomable="yes"}

### Erstellen eines Berichts

1. Klicken Sie auf **[!UICONTROL New Report]**.

1. Wählen Sie in der Liste **[!UICONTROL Groups]** alle Informationen aus, die Sie in den Bericht aufnehmen möchten. Standardmäßig sind alle Gruppen ausgewählt.

   ![Systembericht - Gruppen auswählen](./assets/report-create.png){width="600" zoomable="yes"}

1. Klicken Sie oben rechts auf **[!UICONTROL Create]**.

   Je nach der Anzahl der ausgewählten Berichtstypen kann es einige Minuten dauern, bis der Bericht generiert wird. Wenn der Bericht fertig ist, wird er am oberen Rand des Rasters mit dem generierten Datum und der generierten Uhrzeit angezeigt.

### Modulinformationen anzeigen

Nützliche Informationen zu installierten Modulen finden Sie hier.

**_So zeigen Sie Berichtsinformationen für jedes installierte Modul an:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Klicken Sie auf **[!UICONTROL New Report]**.
1. Wählen Sie `Modules` aus der Liste **[!UICONTROL Groups]** aus.
1. Klicken Sie auf **[!UICONTROL Create]**.
1. Nachdem der Bericht generiert wurde, klicken Sie auf **[!UICONTROL Select]** und dann auf **[!UICONTROL View]** , um alle Modulversionen anzuzeigen.
1. Klicken Sie auf **[!UICONTROL Download]** , um den Bericht herunterzuladen.

### Systemberichte verwalten

Wählen Sie in der Spalte **[!UICONTROL Action]** des Rasters eine der folgenden Optionen aus:

- `View` - Verwenden Sie diese Funktion, um die Details des Berichts anzuzeigen.
- `Delete` - Mit dieser Funktion können Sie den generierten Bericht aus der Liste löschen.
- `Download` : Verwenden Sie diese Funktion, um den Bericht als HTML-Datei zu speichern.

### Anzeigen von Systemberichtsdetails

1. Wählen Sie für den benötigten Bericht **[!UICONTROL View]** in der Spalte _[!UICONTROL Actions]_&#x200B;aus.

1. Erweitern Sie im linken Bereich ![Erweiterungsauswahl](../assets/icon-display-expand.png) jeden Abschnitt des Berichts, um die Details anzuzeigen.

   ![Allgemeine Informationen zu Systemberichten](./assets/report-information.png){width="600" zoomable="yes"}

### Verfügbare Systemberichte

| Berichtsgruppe | Enthaltene Informationen |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerce version<br>data count<br>cache status<br>index status |
| [!UICONTROL Environment] | Umgebungsinformationen/<br>-Status |
| [!UICONTROL Data] | Kategorien nach URL-Schlüssel duplizieren<br> Produkte nach URL-Schlüssel duplizieren<br> Produkte nach SKU duplizieren<br> Bestellungen nach Inkrement-ID <br>Duplizieren von Benutzern nach E-Mail<br>beschädigte Kategoriedaten |
| [!UICONTROL Modules] | Benutzerdefinierte Module Liste<br>Deaktivierte Module Liste<br>Alle Module Liste |
| [!UICONTROL Configuration] | Konfiguration<br>Daten aus der Funktionsmatrix `app/etc/env.php`<br>Versandmethoden<br>Zahlungsmethoden<br>Zahlungen |
| [!UICONTROL Logs] | Protokolldateien<br>Top-Systemmeldungen<br>Aktuelle Top-Systemmeldungen<br>Top-Debugmeldungen<br>Aktuelle Top-Debugmeldungen<br>Top-Ausnahmemeldungen<br>Aktuelle Top-Ausnahmemeldungen |
| [!UICONTROL Attributes] | Benutzerdefinierte EAV-Attribute<br>neue EAV-Attribute<br>Entitätstypen<br>Alle EAV-Attribute<br>Kategorie-EAV-Attribute<br>Produkt-EAV-Attribute<br>Kunden-EAV-Attribute<br>Kundenadresse EAV-Attribut<br>RMA-Element EAV-Attribute |
| [!UICONTROL Events] | Benutzerdefinierte globale Ereignisse<br>Benutzerdefinierte Admin-Ereignisse<br>Benutzerdefinierte Frontend-Ereignisse<br>Benutzerdefinierte Dokumentereignisse<br>Benutzerdefinierte Crontab-Ereignisse<br>benutzerdefinierte REST-Ereignisse<br>Benutzerdefinierte SOAP-Ereignisse<br>Core-globale Ereignisse<br>Core-Admin-Ereignisse<br><br> Core-Frontend-Ereignisse<br>Core-Crontab-Ereignisse<br><br> Core-REST-Ereignisse<br>Alle globalen Ereignisse<br>Alle Admin-Ereignisse<br><br> Alle Doc-Ereignisse<br>Alle REST-Ereignisse<br>Alle SOAP-Ereignisse<br>Alle Crontab-Ereignisse |
| [!UICONTROL Cron] | Cron-Zeitpläne nach Status-Code<br>Cron-Zeitpläne nach Auftrags-Code<br>Fehler in Cron-Zeitplänen Warteschlange<br>Cron-Zeitplanliste<br>Benutzerdefinierte globale Cron-Aufträge<br>Benutzerdefinierte konfigurierbare Cron-Aufträge<br>Core-globale Cron-Aufträge<br>Core konfigurierbare Cron-Aufträge<br>Alle globalen Cron-Aufträge<br>Alle konfigurierbaren Cron-Aufträge |
| [!UICONTROL Design] | AdminHTML-Designliste<br>Frontend-Designliste |
| [!UICONTROL Stores] | Website-Baumstruktur<br>Websites-Liste<br>Stores-Liste<br>Store-Ansichten-Liste |
| OMS-Connector <br>_(sichtbar mit OMS-Integration)_ | Ergebnisse <br> Connector-<br>-Connector-Überwachung |

{style="table-layout:auto"}
