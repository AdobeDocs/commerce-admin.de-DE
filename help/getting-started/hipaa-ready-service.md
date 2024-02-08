---
title: HIPAA-Bereitschaft für Adobe Commerce
description: Erfahren Sie, wie Sie das Adobe Commerce HIPAA-Ready-Modul hinzufügen und zusätzliche Funktionen erhalten können, mit denen Sie Ihre HIPAA-Verpflichtungen erfüllen können.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 3364a07b4c79a60ed813bf669a04711b69dae6f9
workflow-type: tm+mt
source-wordcount: '1443'
ht-degree: 0%

---

# HIPAA-Bereitschaft für Adobe Commerce

>[!IMPORTANT]
>
>**Haftungsausschluss**<br/>
>Diese Informationen sollen Adobe-Kunden bei der Beantwortung ihrer Fragen zu Adobe HIPAA-Ready Services helfen. Es handelt sich nicht um Rechtsberatung. Die Händler sollten sich mit ihrem Rechtsbeistand beraten, um ihre Verpflichtungen im Rahmen der HIPAA und die angemessene Verwendung und Konfiguration von Adobe-Produkten zu verstehen.

## Gesetz über die Portabilität und die Rechenschaftspflicht von Krankenversicherungen (HIPAA)

Der Health Insurance Portability and Accounability Act (HIPAA) ist das wichtigste Bundesdatenschutzgesetz in den USA und wird vom US-amerikanischen Gesundheitsministerium für Gesundheit und menschliche Dienstleistungen (HHS) durchgesetzt. HIPAA gilt für _Gedeckte Entitäten_ (wie Gesundheitsdienstleister, Versicherer und Clearinghäuser) und _Betriebsräte_ (z. B. die Stellen, die Dienste für abgedeckte Stellen erbringen). Die HIPAA-Anforderungen gelten für drei separate Regeln: Datenschutzregel, Sicherheitsregel und Regel für die Verletzung von Benachrichtigungen. Adobe fungiert als Business Associate für bestimmte Produkte, die von Adobe als &quot;HIPAA-Ready Services&quot;klassifiziert werden. Im Rahmen des HIPAA geregelte Daten werden als _Geschützte Gesundheitsinformationen_ oder PHI. PHI ist eine Untergruppe von Gesundheitsinformationen, die (1) von einem Gesundheitsdienstleister, einem Gesundheitsplan oder einem Clearinghaus für die Gesundheitsversorgung erstellt oder empfangen wird, (2) sich auf die frühere, aktuelle oder künftige physische oder psychische Gesundheit oder den Gesundheitszustand einer Person, die Gesundheitsversorgung einer Person oder die frühere, gegenwärtige oder künftige Zahlung für die Bereitstellung von Gesundheitsdienstleistungen an eine Person beziehen und (3) die Person oder die Grundlage für die Annahme gibt. die Informationen können zur Identifizierung der Person verwendet werden. Nach den HIPAA-Datenschutz- und -Sicherheitsregeln muss ein abgedecktes Unternehmen schriftliche Zusicherungen von einem Business Associate in Form eines Business Associate Agreement (BPA) erhalten, in denen es vom Business Associate (BAT) verlangt, die Privatsphäre und Sicherheit des PHI des abgedeckten Unternehmens zu schützen.

## Adobe Commerce HIPAA-bereit

Adobe Commerce HIPAA-Ready verfügt über zusätzliche Funktionen und Funktionen, die es Händlern ermöglichen, ihren jeweiligen HIPAA-Verpflichtungen nachzukommen. Sie können Adobe Commerce HIPAA-bereit installieren (`magento/hipaa-ee`) in Ihre Adobe Commerce in der Cloud-Infrastruktur. Es gibt auch einige Funktionen, die deaktiviert werden müssen, um mit HIPAA kompatibel zu sein.

*Diese Materialien dienen nur zu Informationszwecken. Die Bereitstellung dieser Informationen berechtigt den Empfänger nicht zu vertraglichen oder sonstigen Rechten. Es wurde zwar versucht, die Richtigkeit der Informationen zum Zeitpunkt ihrer Übermittlung sicherzustellen, doch wird keine Darstellung dafür vorgenommen, dass diese Informationen korrekt und vollständig sind, und Adobe verpflichtet sich nicht, diese Informationen zu aktualisieren, da sich das Gesetz oder die Adobe ändern. Dieses Dokument darf ohne schriftliche Zustimmung von Adobe an keine andere Partei als den vorgesehenen Empfänger weitergegeben werden.*

## Systemanforderungen

Die HIPAA-Bereitschaft für Adobe Commerce weist dieselben Systemanforderungen wie Adobe Commerce mit den zusätzlichen Anforderungen auf:

- Adobe Commerce-Version 2.4.6-p3 oder neuer (Nicht-Beta)
- Adobe Commerce auf Cloud-Infrastruktur oder Adobe Commerce auf Managed Services
- Neueste Version der `magento/hipaa-ee` Erweiterung

## Installation

Adobe HIPAA-Ready Services ist technisch ein Composer-Metapaket `magento/hipaa-ee` , die Links zu speziellen Modulen enthält. Dieses Metapaket befindet sich im Repository [repo.magento.com](https://repo.magento.com).

1. Installieren `magento/hipaa-ee` -Metapaket, müssen Sie Zugriff darauf haben. Informationen zur Schlüsselgenerierung und zum Erhalt der erforderlichen Berechtigungen finden Sie unter [Abrufen der Authentifizierungsschlüssel](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html?lang=en).

1. Überprüfen Sie die Umgebung, in der Sie das Paket installieren werden, und stellen Sie sicher, dass es den allgemeinen [Systemanforderungen](#system-requirements).

1. Metapaket hinzufügen `magento/hipaa-ee` zur Komponentenkonfiguration.

   Am einfachsten ist die Verwendung der Composer-CLI. Beispiel:

   ```shell
   composer require magento/hipaa-ee
   ```

1. Wenn Adobe Commerce noch nicht installiert ist, können Sie die Installation starten (folgen Sie dazu dem [Installationsanweisungen](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=en)).

   Wenn Adobe Commerce bereits installiert ist, führen Sie nach dem Herunterladen von Modulen `bin/magento setup:upgrade` und folgen Sie dann den Empfehlungen.

   ```shell
   bin/magento setup:upgrade
   ```

   Wenn dieser Befehl ausgeführt wird, werden die neu heruntergeladenen Module aktiviert und die Skripte zur Installation gestartet. Weitere Informationen zur Modulverwaltung finden Sie unter [Module aktivieren oder deaktivieren](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=en).

1. Nach Abschluss der Installation oder Aktualisierung sollten Sie überprüfen, ob die `Hipaa*` relevante Module wurden aufgenommen.

   Führen Sie den Befehl aus:

   ```shell
   bin/magento module:status
   ```

   Wenn das HIPAA Composer-Paket korrekt hinzugefügt wurde, sehen Sie die HIPAA-Module in der Ausgabe des Befehls. Beispiel:

   ```text
   List of enabled modules:
   <truncated for brevity>
   Magento_HipaaAnalytics
   Magento_HipaaCheckout
   Magento_HipaaLogging
   Magento_HipaaScheduledImportExport
   Magento_HipaaAdminLogging
   Magento_HipaaCustomerLogging
   Magento_HipaaNewsletter
   Magento_HipaaImportExport
   Magento_HipaaApiLogging
   <truncated for brevity>
   ```

   Alle Module mit dem Präfix `Magento_Hipaa` muss sich im Abschnitt Aktivierte Module befinden.

## Funktionsverbesserungen für HIPAA-Bereitschaft

Die `magento/hipaa-ee` -Paket enthält einige Änderungen und Verbesserungen am Commerce-Basisprodukt. Die folgenden Abschnitte enthalten Details zu diesen Änderungen und wie sie das Basisprodukt ändern.

### Aktionsprotokolle

Die Prüfprotokollierung ist eine HIPAA-Anforderung. In Adobe Commerce wird die [Aktionsprotokolle](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) erfasst alle Änderungen, die von einem Admin-Benutzer vorgenommen wurden, der in Ihrem Store arbeitet. Um die HIPAA-Anforderungen an das Auditprotokoll zu erfüllen, wurden Änderungen an der Funktion vorgenommen, um alle Admin-Benutzer- und Kundenaktionen aufzuzeichnen, die über die Admin-Benutzeroberfläche und über API-Aufrufe ausgeführt werden.

#### Bericht &quot;Action Logs&quot;

Die _Aktionsprotokolle_ Berichtsraster (**[!UICONTROL System]** > Aktionsprotokolle > Bericht) geändert, um Kundenaktionen aufzunehmen, die über die Admin-Benutzeroberfläche und -API ausgeführt werden.

1. Zwei zusätzliche Spalten:
   - ***Quelle***: Zeigt an, wo die Aktion ausgeführt wurde.\
     Werte: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Client-Typ***: Zeigt den Client-Typ an.\
     Werte: Kunde | Admin | Integration


2. Umbenennen ***Benutzername*** nach ***Client-Kennung***
   - ***Client-Kennung***: Zeigt die Anmelde-ID des Benutzers an, der die Aktion ausgeführt hat.\
     Werte:
      - eine E-Mail, wenn der Client-Typ Kunde ist
      - einen Benutzernamen, wenn der Client-Typ Admin ist
      - einen Namen, wenn der Client-Typ Integration ist

3. Umbenennen ***Vollständiger Aktionsname*** nach ***Target***
   - ***Target***: Zeigt den Aktionsnamen an\
     Werte:
      - einen Endpunkt, wenn die Quelle die REST-API oder die SOAP-API ist
      - einen Abfrage-/Mutationsnamen, wenn die GraphQL-API
      - einen Aktionsnamen, wenn die Administrator-Benutzeroberfläche oder die Kundenbenutzeroberfläche

#### Konfigurieren von Admin-Aktionen für die Protokollierung

Diese Funktion ist nicht verfügbar, da alle Aktionen standardmäßig aufgezeichnet werden müssen.

### Import-/Exportfunktionen

Die Verbesserungen bei Import-/Exportfunktionen konzentrieren sich auf die Verbesserung des administrativen Erlebnisses und die bessere Sichtbarkeit von Benutzeraktionen.

>[!NOTE]
>
>Diese ***Verbesserungen ändern die Import/Export-Core-Logik nicht.***; vielmehr erweitern sie die Funktionalität, um eine umfassendere Protokollierung und verbesserte Datenzuordnung zu bieten. Die grundlegende Funktionalität von Import/Export bleibt unverändert. Benutzer können die vorhandenen Funktionen und Workflows ohne Unterbrechung weiterhin verwenden.

#### Protokollierung administrativer Aktionen

Eine der wichtigsten Verbesserungen der Import-/Exportfunktionen ist die verbesserte Protokollierung von Verwaltungsaktionen. Dadurch wird die Fähigkeit eingeführt, Aktivitäten im Zusammenhang mit Datenimport/-export genauer zu untersuchen und so zu einer verbesserten Nachverfolgung und Auditbarkeit beizutragen. Die folgenden Aktionen werden jetzt protokolliert und in der **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**grid:

| Typ | Aktionen |
| ---- | ------- |
| Import | <ul><li>Ein Administrator führt einen Import aus<li>Ein Administrator lädt eine importierte Datei herunter<li>Ein Administrator lädt eine Fehlerdatei herunter<ul/> |
| Export | <ul><li>Admin-Benutzeranforderungen<li>Ein Administrator lädt eine exportierte Datei herunter<ul/> |
| Geplante Importe/Exporte | <ul><li>Ein Administrator plant den Export von Zeitplänen<li>Ein Administrator bearbeitet einen geplanten Export<li>Ein Admin-Benutzer führt einen geplanten Export durch<li>Ein Admin-Benutzer löscht einen geplanten Export<li>Ein Admin-Benutzer plant den Import<li>Ein Administrator bearbeitet einen geplanten Import<li>Ein Admin-Benutzer führt einen geplanten Import durch<li>Ein Admin-Benutzer löscht einen geplanten Import<li>Ein Admin-Benutzer führt einen Massenlöschvorgang von Import-/Exportvorgängen aus<ul/> |

### Verbesserungen bei der Anzeige und verbesserte Filterung/Sortierung

Um Admin-Benutzern informativere Raster zu ermöglichen, wurden die Anzeige von Daten sowie die Filter- und Sortierfunktionen um verschiedene Verbesserungen erweitert:

#### Importverlauf ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Filterung für alle Spalten mit Ausnahme von **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]**, und **[!UICONTROL Summary]**.

#### Export ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- Hinzufügung von **[!UICONTROL ID]** Spalte.
- Hinzufügung von **[!UICONTROL Requested At]** column (_Datum und Uhrzeit der Exportanforderung_).
- Hinzufügung von **[!UICONTROL User]** column (_Benutzername eines Administrators, der die Anfrage ausgeführt hat_).
- Entfernt ein **[!UICONTROL Action]** Spalte.
- Verschieben Sie die **[!UICONTROL Download]** Link zu einer **[!UICONTROL File name]** column (_zum Beispiel das Raster Importverlauf_).
- Die Aktion zum Löschen einer exportierten Datei (_zur Verbesserung des Trackings_).
- Sortierung für alle Spalten außer **[!UICONTROL File name]**.
- Die Filterung aller Spalten wurde aktiviert.

#### Geplante Importe/Exporte ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Hinzufügung von **[!UICONTROL ID]** Spalte.
- Hinzufügung von **[!UICONTROL Scheduled At]** column (_Datum und Uhrzeit der Planung des Imports oder Exports_).
- Hinzufügung von **[!UICONTROL User]** column (_Benutzername eines Admin-Benutzers, der den Import/Export geplant hat_).

## Funktionen für HIPAA-Bereitschaft deaktiviert

### SaaS-Dienste

Keiner der für Adobe Commerce angebotenen SaaS-Dienste ist im Rahmen des HIPAA-Bereitschaftsangebots verfügbar. Dazu gehören unter anderem:

- Live Search
- API-Mesh
- App Builder
- Catalog Service

### Standardmäßig deaktivierter Gastkasse

- Der Gast-Checkout birgt ein potenzielles Risiko für verschiedene Aspekte von HIPAA, darunter Protokollierung, Zugangssteuerung, PHI-Hygiene und -Herkunft sowie möglicherweise mehr.
- Gastauschecken ist standardmäßig im HIPAA-Readiness-Modul deaktiviert, kann aber für meine Händler auf eigene Gefahr aktiviert werden.

### Funktion &quot;Newsletter standardmäßig deaktiviert&quot;

- Die Newsletter-Funktion ist standardmäßig deaktiviert, um zu verhindern, dass PHI in einem Marketingkontext verwendet wird, kann aber vom Händler auf eigene Gefahr aktiviert werden.

### Die Einstellung des erweiterten Reporting-Dienstes wurde standardmäßig deaktiviert.

Die Einstellung des erweiterten Berichterstellungsdienstes ist standardmäßig deaktiviert, um zu verhindern, dass PHI für die Analyse und Berichterstellung verwendet wird. Sie kann jedoch vom Händler auf eigene Gefahr aktiviert werden.
