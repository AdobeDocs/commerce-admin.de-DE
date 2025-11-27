---
title: Überwachung des Synchronisierungsstatus von Daten-Feeds
description: Überwachen Sie die Synchronisierung von Datenexporten und identifizieren Sie Probleme oder Verzögerungen bei der Feed-Verarbeitung für [!DNL Catalog Service],  [!DNL Live Search] und  [!DNL Product Recommendations].
feature: Products, Customers, Data Import/Export
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 15118877bb8cc533b2323819db34da0513899e25
workflow-type: tm+mt
source-wordcount: '1458'
ht-degree: 0%

---


# Überwachung des Synchronisierungsstatus von Daten-Feeds

Adobe Commerce-Administratoren können den Synchronisierungsstatus von Daten, die von Adobe Commerce an verbundene Commerce-Services exportiert werden, über die Seite Daten-Feed-Synchronisierungsstatus in Commerce Admin überwachen.

![Detailseite „Daten-Feed-Synchronisierungsstatus“ mit Reporting zum Feed-Elementstatus](assets/data-feed-sync-status.png)

Diese Seite bietet Echtzeiteinblicke in den Zustand und die Leistung von Datenexport-Feeds, die Produkt- und Kategoriedaten von Commerce an externe Services wie [!DNL Product Recommendations], [!DNL Live Search] und [!DNL Catalog Service] übertragen.

Auf der Seite Synchronisierungsstatus wird nur der Exportstatus angezeigt. Ein Erfolgsstatus gibt an, dass die Daten erfolgreich exportiert wurden und letztendlich in Connected Commerce Services verfügbar sein werden. Verwenden Sie das [Daten-Management-Dashboard](data-dashboard.md), um den tatsächlichen Status der Entitätssynchronisierung anzuzeigen.

Die Überwachung des Feed-Status hilft, die Datenkonsistenz sicherzustellen, und ermöglicht die sofortige Lösung aller Probleme, die während des Exportvorgangs auftreten. Administratoren haben folgende Möglichkeiten:

* **Synchronisierungsstatus anzeigen** für alle Daten-Feeds
* **Identifizieren und Beheben von Fehlern** bei der Feed-Verarbeitung
* **Zugriff auf detaillierte Statusinformationen** für einzelne Feed-Elemente

Status wird für die folgenden Feeds verfolgt:

* Produkt-Feed
* Feed für Produktattribute
* Feed-Kategorien
* Feed für Produktüberschreibungen
* Produktpreise Futtermittel
* Produkt-Feed-Varianten

>[!TIP]
>
>Weitere Informationen zum Datensynchronisierungsprozess finden Sie unter [Synchronisieren von Daten mit dem SaaS](https://experienceleague.adobe.com/de/docs/commerce/saas-data-export/data-synchronization)Datenexport im *SaaS-Datenexport-Handbuch*.

## Installieren der Erweiterung

Die Seite Daten-Feed-Status steht allen Commerce-Händlern mit aktiven Lizenzen für die folgenden Commerce-Services zur Verfügung:

* [[!DNL Product Recommendations v6.0.0+]](https://experienceleague.adobe.com/de/docs/commerce/product-recommendations/guide-overview)
* [[!DNL Live Search v4.1.0+]](https://experienceleague.adobe.com/de/docs/commerce/live-search/guide-overview)
* [[!DNL Catalog Service v1.17+]](https://experienceleague.adobe.com/de/docs/commerce/catalog-service/guide-overview) mit einer aktiven Lizenz.

**Anforderungen**

* PHP 8.1, 8.2, 8.3 oder 8.4
* Adobe Commerce 2.4.4+
* [Adobe Commerce-Datenexporterweiterung](https://experienceleague.adobe.com/de/docs/commerce/saas-data-export/manage-extension), Version 103.4.15 oder höher
* Zugriff auf [repo.magento.com](https://repo.magento.com)

  Informationen zum Generieren von Schlüsseln und Abrufen der erforderlichen Berechtigungen finden Sie unter [Abrufen Ihrer Authentifizierungsschlüssel](https://experienceleague.adobe.com/de/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). Informationen zu Cloud-Installationen finden Sie im Handbuch zu [Commerce in Cloud-Infrastrukturen](https://experienceleague.adobe.com/de/docs/commerce-on-cloud/user-guide/develop/authentication-keys).

* Zugriff auf die Befehlszeile des Adobe Commerce-Anwendungsservers.

### Installationsschritte

Fügen Sie das Modul `magento/module-data-exporter-status` mit dem Composer hinzu:

```shell
composer require magento/module-data-exporter-status
```

Detaillierte Informationen zu den Installationsschritten finden Sie in den folgenden Handbüchern:

* [Installieren der Erweiterung auf Adobe Commerce in der Cloud-Infrastruktur](https://experienceleague.adobe.com/de/docs/commerce-on-cloud/user-guide/configure-store/extensions)

* [Installieren der Erweiterung Adobe Commerce On-Premise](https://experienceleague.adobe.com/de/docs/commerce-operations/installation-guide/tutorials/extensions)

## Aufrufen der Seite Daten-Feed-Status .

Rufen Sie von Commerce Admin aus über Commerce Admin die Seite Daten-Feed-Status unter **[!DNL System]** > Datenübertragung > **[!DNL Data Feed Sync Status]** auf.

![Seite „Status der Daten-Feed-Synchronisierung“ mit einer Zusammenfassung der Daten-Feed-Exportaktivität](assets/data-feed-sync-status.png)

Die Überwachung des Daten-Feed-Status bietet zwei Schnittstellen:

* Auf der [Zusammenfassungsseite für den Synchronisierungsstatus von Daten-Feeds](#data-feed-sync-status-summary) auf der die verfügbaren Feeds und der aktuelle Status aufgeführt sind
* Die [Daten-Feed-Synchronisierungsstatus - Detailseite](#data-feed-sync-status-details) die detaillierte Informationen zu einem ausgewählten Feed anzeigt.

## Zusammenfassung des Synchronisierungsstatus von Daten-Feeds

Die Zusammenfassungsseite für den Feed-Synchronisierungsstatus enthält Informationen zur Exportaktivität für Daten-Feeds, einschließlich der folgenden Informationen:

| Feld | Beschreibung |
|-------|-------------|
| **Feed-Name** | Der Name des Feed-Indexers, der für die Synchronisierung einer bestimmten Entität oder eines Teils davon verantwortlich ist, z. B. Produkt- oder Produktpreis. |
| **Source-Datensätze** | Anzahl der für den Export aus der Commerce-Datenbank verfügbaren Datensätze. Diese Zahl kann größer sein als die Anzahl der im Commerce Admin angezeigten Datensätze, da jedes Feed-Element zu einem bestimmten Bereich gehört, z. B. Code für die Store-Ansicht. |
| **Datensätze erfolgreich gesendet** | Anzahl der erfolgreich zur weiteren Verarbeitung an Commerce SaaS übermittelten Datensätze. Wenn während der Übertragung Fehler aufgetreten sind, die Anzahl der erfolgreich an externe Dienste übertragenen Datensätze. |
| **Fehlgeschlagene Datensätze** | Anzahl der Datensätze, die nicht exportiert werden konnten und bearbeitet werden mussten. |
| **Aktion** | Wählen Sie **[!UICONTROL Details]** aus, um die Synchronisierungsaktivität für einen Feed anzuzeigen. |

## Details zum Synchronisierungsstatus von Daten-Feeds

Klicken Sie auf der Zusammenfassungsseite des Daten-Feed-Status auf einen Feed-Namen oder verwenden Sie die [!DNL View Details]-Aktion, um auf detaillierte Informationen zu einzelnen Datensätzen in einem Feed zuzugreifen.

![[!UICONTROL Data Feed Sync Status - Details] Seite mit Reporting zum Feed-Elementstatus](assets/data-feed-sync-status-details.png)

Die Detailansicht enthält die folgenden Informationen zu jedem Feed-Element:

| Feld | Beschreibung |
|-------|-------------|
| **Feed-Element-ID** | Interne Kennung des Feed-Eintrags |
| **Entitäts-ID** | Die Quellenentitäts-ID (Produkt-ID, Kategorie-ID usw.) |
| **Exportstatus** | Der [Synchronisierungsstatus](#export-status-types) des Feed-Elements. Aktueller Status des Exportversuchs mit farbcodierten Indikatoren |
| **Letztes Synchronisationsdatum** | Zeitstempel, wann der Datensatz zuletzt an Commerce Services gesendet wurde |
| **Wird die Entität gelöscht?** | Gibt an, ob die Entität oder ihr Teil (z. B. Produkt- oder Produktpreis) in Adobe Commerce gelöscht wurde. Elemente werden nur angezeigt, wenn bei der Synchronisierung ein Fehler aufgetreten ist. |
| **Anfrage-ID** | Eine eindeutige Kennung für die Synchronisierungsanfrage. Geben Sie diese ID an den Support bei der Fehlerbehebung bei bestimmten Entitätsaktualisierungen. |
| **Fehler** | Detaillierte Fehlerinformationen, wenn das Feed-Element nicht synchronisiert werden konnte. |

Sie können die Ansicht mit den folgenden Steuerelementen verwalten:

* [!DNL Mass Action] für ausgewählte Feed-Elemente die Neusynchronisierung planen
* [!DNL Filters]
* [!DNL Default View] zum Erstellen und Speichern einer gefilterten Ansicht und zum Wechseln zwischen Ansichten
* [!DNL Columns] Spalten in der Tabelle ein- und ausblenden.

### Indikatoren für die Futtermittelgesundheit

Oben auf jeder Feed-Detailseite geben kritische Konsistenzindikatoren den Systemstatus für jeden Feed an:

#### Indexerstatus

* **Valid**: Daten werden synchronisiert; keine Neuindizierung erforderlich.
* **Ungültig**: Originaldaten wurden geändert; der Index sollte aktualisiert werden.
* **Verarbeitung**: Indizierung läuft.

>[!TIP]
>
>Weitere Informationen zur Indexverarbeitung finden Sie unter [Indexverwaltung](https://experienceleague.adobe.com/de/docs/commerce-admin/systems/tools/index-management).

#### Changelog-Rückstand

* **Alle synchronisiert**: Keine ausstehenden Änderungen zu verarbeiten
* **Elemente im Rückstand**: Anzahl der ausstehenden Änderungen, die darauf warten, verarbeitet zu werden

### Statusarten exportieren

Das System bietet Statusanzeigen, mit denen Sie Probleme schnell identifizieren können:

#### Statuskategorien

| **Status** | **Beschreibung** | **Aktion erforderlich** |
|--------|-----------|-------------|
| **An Service gesendet** | Feed-Element erfolgreich in Commerce-Service exportiert. | Keine |
| **Fehlgeschlagen, wird erneut versucht** | Vorübergehender Fehler. Das System versucht es automatisch erneut. | Monitor für Auflösung |
| **Fehlgeschlagen, erfordert Aufmerksamkeit** | Fehlgeschlagen aufgrund eines Anwendungs- oder Datenfehlers. | Untersuchen und Beheben des Problems in der Spalte [!DNL Error] |
| **Warten auf Übermittlung** | Zum Export in die Warteschlange gestellt, aber noch nicht verarbeitet. | Normaler Verarbeitungsstatus |

## Überwachen des Daten-Feed-Status

Wenn Sie produkt- und kategoriebezogene Entitäten in der Commerce-Datenbank aktualisieren, werden die Daten entsprechend Ihrer Feed-Konfiguration an Commerce-Services übertragen. Sie können diesen Prozess in Echtzeit über die Zusammenfassungsseite für den Status der Daten-Feed-Synchronisation überwachen.

>[!IMPORTANT]
>
>Die Dauer der Datensynchronisation hängt von der Größe des Katalogs, dem Volumen der aktualisierten Daten und der Leistung des externen Services ab.

Wenn die Anzahl der erfolgreich gesendeten Datensätze mit der Anzahl der Quelldatensätze übereinstimmt, bedeutet dies, dass die Synchronisierung abgeschlossen ist und alle Daten erfolgreich übertragen wurden.

>[!NOTE]
>
>Adobe bietet außerdem Befehlszeilenschnittstellen-Tools und Systemprotokolle, die Entwickler und Systemintegratoren verwenden können, um Synchronisierungsvorgänge zu verwalten und zu verfolgen. Weitere Informationen finden Sie im [SaaS-Datenexporthandbuch](https://experienceleague.adobe.com/de/docs/commerce-merchant-services/saas-data-export/overview).

### Fehlgeschlagene Exporte verwalten

So zeigen Sie die Details fehlgeschlagener Exporte an und ergreifen Korrekturmaßnahmen:

1. Suchen Sie auf der Seite Feed-Synchronisierungsstatus den Feed mit fehlgeschlagenen Datensätzen.
1. Klicken Sie auf **[!DNL Details]**.

1. Überprüfen Sie die Fehlermeldungen auf bestimmte Fehlerursachen.

1. Verwenden Sie Massenaktionen, um Neusynchronisierungsvorgänge für fehlgeschlagene Elemente zu planen.

### Fehlgeschlagene Daten neu synchronisieren

Über das Menü [!DNL Actions] auf der Seite [!DNL Data Feed Sync Status - Details] können Sie fehlgeschlagene oder problematische Daten-Feeds manuell neu synchronisieren.

Während das System automatisch bestimmte Arten von Fehlern wiederholt, kann in den folgenden Szenarien ein manueller Eingriff erforderlich sein:

* Sie bemerken Authentifizierungs- oder Berechtigungsfehler (401, 403 Status-Codes).
* Nach dem Beheben von Datenformatproblemen, die Payload-Fehler verursacht haben.
* Die folgenden Aktualisierungen gelten für externe Dienstkonfigurationen oder Endpunkte.
* Sie stellen Anpassungen bereit, die sich auf Datenexportprozesse auswirken.

Durch die proaktive Überwachung des Feed-Status und die umgehende Behebung von Fehlern können Sie die Datenkonsistenz und -zuverlässigkeit in Ihrem Commerce-Ökosystem gewährleisten.

#### Feed-Elemente manuell neu synchronisieren

Wenn Sie bestimmte Feed-Elemente neu synchronisieren müssen:

1. **Datensätze auswählen**: Aktivieren Sie Kontrollkästchen, um fehlgeschlagene Datensätze auszuwählen, die bearbeitet werden müssen.
2. **Aktion wählen**: Wählen Sie **[!DNL Schedule Resync]** aus dem Dropdown-Menü „Massenaktion“.
3. **Bestätigen**: Klicken Sie auf **[!DNL Submit]** und bestätigen Sie den Vorgang der Neusynchronisierung.
4. **Ergebnisse überwachen**: Überprüfen Sie die Erfolgsmeldung und überwachen Sie Statusänderungen.

## Best Practices

### Regelmäßige Überwachung

1. **Tägliche Prüfungen**: Überprüfen Sie die Übersichtsseite täglich auf Feeds mit hohen Fehlerquoten
1. **Weekly Deep Dive**: Untersuchen Sie den detaillierten Status für kritische Feeds (Produkte, Preise)
1. **Monatliche Analyse**: Verfolgen Sie Trends bei den Erfolgsraten und der Leistung beim Export

### Fehlerbehebung in Workflows

1. **Probleme identifizieren**: Suchen Sie nach Fehlern und hohen Fehlerzahlen
1. **Indexerzustand überprüfen**: Stellen Sie sicher, dass Indexer gültig sind und der Rückstand verwaltbar ist
1. **Fehlerdetails überprüfen**: Klicken Sie auf Fehlgeschlagene Datensätze, um bestimmte Fehlermeldungen anzuzeigen
1. **Neusynchronisierung planen**: Verwenden Sie Massenaktionen, um fehlgeschlagene Exporte erneut zu versuchen
1. **Bildschirmauflösung**: Stellen Sie sicher, dass resynchronisierte Elemente einen erfolgreichen Status aufweisen.

### Beheben häufiger Probleme

#### Hohe Ausfallraten

**Symptome**: Große Anzahl von Datensätzen mit dem Status „Fehlgeschlagen, Aufmerksamkeit erforderlich“

**Mögliche Ursachen**:

* Konfigurationsänderungen des externen Services
* Inkompatibilitäten des Datenformats
* Probleme mit Authentifizierung oder Berechtigungen

**Auflösungsschritte**:

1. Status und Konfiguration des externen Services überprüfen
1. Überprüfen von Fehlermeldungen auf Muster
1. Authentifizierungsdaten überprüfen
1. Wenden Sie sich bei Bedarf an den externen Support

#### Langsame Exportleistung

**Symptome**: Hoher Changelog-Rückstand, langsame Statusaktualisierungen

**Mögliche Ursachen**:

* Leistungsprobleme mit dem Indexer
* Hohes Datenvolumen
* Begrenzung der externen Serviceleistung

**Auflösungsschritte**:

1. Indexerstatus überprüfen und bei Ungültigkeit erneut ausführen
2. Überwachen der Reaktionszeiten externer Services
3. Planen von Exporten außerhalb der Spitzenzeiten
4. Überprüfen der Systemressourcen und -leistung

#### Authentifizierungsfehler

**Symptome**: Statuscodes 401 oder 403

**Auflösungsschritte**:

1. API-Anmeldeinformationen und Token überprüfen
1. Prüfen der Berechtigungen für externe Dienstkonten
1. Abgelaufene Authentifizierungstoken verlängern
1. Bei Zugriffsproblemen wenden Sie sich an Ihren Dienstleister

>[!MORELIKETHIS]
>
>* [Daten-Management-Dashboard](https://experienceleague.adobe.com/de/docs/commerce-admin/systems/data-transfer/data-sync/data-dashboard)
>* [SaaS-Datenexport-Handbuch](https://experienceleague.adobe.com/de/docs/commerce-merchant-services/saas-data-export/overview)
