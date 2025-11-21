---
title: HIPAA-Bereitschaft auf Adobe Commerce
description: Erfahren Sie, wie Sie in Adobe Commerce die Erweiterung für HIPAA-Konformität hinzufügen und zusätzliche Funktionen für die Einhaltung der HIPAA-Vorschriften nutzen können.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: afb6b4ca31675f6e549282749ef032ef1cd2f9f9
workflow-type: tm+mt
source-wordcount: '2391'
ht-degree: 1%

---

# HIPAA-Bereitschaft auf Adobe Commerce

{{ee-feature}}

>[!IMPORTANT]
>
>**Haftungsausschluss**<br/>
>Diese Informationen sollen Adobe-Kunden bei der Beantwortung ihrer Fragen zu Adobe HIPAA-fähigen Services helfen. Sie stellt keine Rechtsberatung dar. Händler sollten sich mit ihrem eigenen Rechtsbeistand beraten, um sich über ihre Verpflichtungen aus dem HIPAA und die angemessene Verwendung und Konfiguration der Produkte von Adobe zu informieren.

>[!BEGINSHADEBOX]

**Health Insurance Portability and Accountability Act (HIPAA)**

Der Health Insurance Portability and Accountability Act (HIPAA) ist das wichtigste US-amerikanische Gesetz zum Schutz der Privatsphäre im Gesundheitswesen und wird vom US-amerikanischen Gesundheitsministerium (US Department of Health and Human Services, HHS) durchgesetzt. HIPAA gilt für _abgedeckte Rechtssubjekte_ (wie Gesundheitsdienstleister, Versicherer und Clearinghäuser) und _Geschäftspartner_ (wie solche Rechtssubjekte, die Dienstleistungen für abgedeckte Rechtssubjekte erbringen). HIPAA-Anforderungen sind in drei separaten Regeln festgelegt: Datenschutzregel, Sicherheitsregel und Regel für Verletzungsbenachrichtigungen. Adobe fungiert als Business Associate für bestimmte Produkte, die Adobe als „HIPAA-fähige Services“ einstuft. Daten, die unter HIPAA geregelt sind, werden als _Protected Health Information_ oder PHI bezeichnet. PHI ist eine Untergruppe von Gesundheitsinformationen, die (1) von einem Gesundheitsdienstleister, einem Gesundheitsplan oder einer Clearingstelle für Gesundheitsdienstleistungen erstellt oder empfangen werden, (2) sich auf die vergangene, gegenwärtige oder zukünftige physische oder psychische Gesundheit oder den Zustand einer Person, die Gesundheitsversorgung einer Person oder die vergangene, gegenwärtige oder zukünftige Zahlung für die Gesundheitsversorgung einer Person beziehen und (3) die Person oder in Bezug auf die eine vernünftige Grundlage für die Annahme besteht, dass die Informationen zur Identifizierung der Person verwendet werden können. Die HIPAA-Datenschutz- und Sicherheitsregeln verlangen, dass eine abgedeckte Organisation schriftliche Zusicherungen von einem Geschäftspartner in Form einer Business Associate Agreement (BAA) erhält, die den Geschäftspartner verpflichten, die Privatsphäre und Sicherheit der PHI der abgedeckten Organisation zu schützen. Weitere Informationen finden Sie unter [HIPAA und Adobe-Produkte und -Services](https://www.adobe.com/trust/compliance/hipaa-hds/hipaa-ready.html) im Adobe Trust Center.

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA-fähig

Die Adobe Commerce HIPAA-fähige Erweiterung fügt Adobe Commerce-Installationen zusätzliche Funktionen und Merkmale hinzu, die es Händlern ermöglichen, ihre jeweiligen HIPAA-Verpflichtungen zu erfüllen.

Die Erweiterung &quot;Adobe Commerce HIPAA-Ready“, `magento/hipaa-ee` für Adobe Commerce in Cloud-Infrastrukturen oder Adobe Managed Services-Projekten verfügbar ist. Der HIPAA-fähige Installationsprozess von Adobe Commerce deaktiviert einige native Services und Funktionen, um HIPAA-Anforderungen zu erfüllen. Siehe [Deaktivierte Services und Funktionen](#disabled-services-and-features).

>[!NOTE]
>
>Der Zugriff auf HIPAA-fähige Funktionen ist nur für Händler verfügbar, die das Add-on für das Gesundheitswesen für Adobe Commerce erworben haben.

*Diese Materialien dienen nur zu Informationszwecken. Die Bereitstellung dieser Informationen berechtigt den Empfänger nicht zu vertraglichen oder sonstigen Rechten. Es wurden zwar Anstrengungen unternommen, um die Richtigkeit der Informationen zum Zeitpunkt ihrer Bereitstellung sicherzustellen, es wird jedoch keine Gewähr für die Richtigkeit und Vollständigkeit dieser Informationen gegeben. Adobe ist nicht verpflichtet, diese Informationen zu aktualisieren, wenn sich die Gesetze oder die Produkte von Adobe ändern. Außerdem darf dieses Dokument ohne schriftliche Zustimmung von Adobe nicht an andere Personen als die vorgesehene Empfängerin oder den Empfänger verteilt werden.*

## Systemanforderungen

Die folgende Tabelle zeigt die Kompatibilität zwischen Adobe Commerce-Versionen und der HIPAA-fähigen Erweiterung:

| Adobe Commerce | Unterstützt | Notizen |
|----------------|-----------|-------|
| 2.4.7-P4 und höher | 1,2,0 | Unterstützung für 2.4.7-P4 erfordert einen [Hotfix](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-27147) |
| 2.4.6-p9 - 2.4.6-p10 | 1,2,0 | |
| 2.4.6-p8 | 1,1,0 | Die Unterstützung für [Datendienste](#adobe-commerce-services) wurde mit Version 1.1.0 eingeführt |
| 2.4.6-p3 - 2.4.6-p7 | 1,0,0 | |

>[!IMPORTANT]
>
>- Die HIPAA-fähige Erweiterung ist nur für Adobe Commerce in Cloud- oder Adobe Commerce Managed Services-Projekten verfügbar.
>- Die Erweiterung ist als Composer-Metapaket von `repo.magento.com` verfügbar.
>- Für den Zugriff auf HIPAA-fähige Funktionen ist das Add-on für das Gesundheitswesen für Adobe Commerce erforderlich.
>- Adobe Commerce Beta-Versionen werden nicht unterstützt.

## Installation

**Voraussetzung**

>[!BEGINSHADEBOX]

- Adobe hat Ihr Adobe Commerce-Konto für den Zugriff auf die HIPAA-fähige Erweiterung bereitgestellt.
- Zugriff auf [repo.magento.com](https://repo.magento.com) zur Installation der Erweiterung. Informationen zum Generieren von Schlüsseln und zum Abrufen der erforderlichen Berechtigungen finden Sie unter [Abrufen Ihrer Authentifizierungsschlüssel](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

>[!ENDSHADEBOX]

Installieren Sie die neueste Version der HIPAA-fähigen Services-Erweiterung (`magento/hipaa-ee`) von Adobe auf einer Instanz, auf der die Adobe Commerce-Versionen 2.4.7-p5 oder 2.4.6-p3 bis 2.4.6-p8 ausgeführt werden. Die Erweiterung wird als Composer-Metapaket aus dem Repository [repo.magento.com](https://repo.magento.com) bereitgestellt. Das Metapaket enthält die Sammlung von Modulen, die die HIPAA-Funktionen für eine Adobe Commerce-Instanz aktivieren.

>[!NOTE]
>
>Um sicherzustellen, dass Backoffice-Ereignisdaten, die an Experience Platform gesendet werden, HIPAA-fähig sind, lesen Sie das [Handbuch zur Datenverbindungserweiterung](https://experienceleague.adobe.com/en/docs/commerce/data-connection/fundamentals/install#install-the-data-services-hipaa-extension).

1. Wechseln Sie auf Ihrer lokalen Workstation in das Projektverzeichnis für Ihr Adobe Commerce on Cloud-Infrastrukturprojekt.

   >[!NOTE]
   >
   >Informationen zur lokalen Verwaltung von Commerce-Projektumgebungen finden Sie unter [Verwalten von Verzweigungen mit der CLI](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/cli-branches) im _Benutzerhandbuch für Adobe Commerce auf Cloud-Infrastruktur_.

1. Checken Sie die Umgebungsverzweigung aus, um sie mithilfe der Adobe Commerce Cloud-CLI zu aktualisieren.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Fügen Sie das Metapaket-`magento/hipaa-ee` mithilfe der Composer-CLI zur Composer-Konfiguration hinzu.

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. Paketabhängigkeiten aktualisieren.

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. Fügen Sie den aktualisierten Code hinzu, übertragen Sie ihn und übertragen Sie ihn in die Cloud-Umgebung.

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   Durch das Pushen der Aktualisierungen wird der [Commerce-Cloud-Bereitstellungsprozess](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/deploy/process) zum Anwenden der Änderungen initiiert. Überprüfen Sie den Bereitstellungsstatus im [Bereitstellungsprotokoll](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/test/log-locations).

### Installation überprüfen

Nachdem die Aktualisierungen bereitgestellt wurden, stellen Sie sicher, dass die `Hipaa*`-Erweiterung installiert ist

1. Verwenden Sie SSH, um sich bei der Remote-Cloud-Umgebung anzumelden.

   ```shell
   magento-cloud ssh
   ```

1. Verwenden Sie in der Befehlszeile die Adobe Commerce-CLI, um den Modulstatus zu überprüfen.

   ```shell
   bin/magento module:status
   ```

1. Überprüfen Sie, ob die HIPAA-Module in der Liste der aktivierten Module enthalten sind:

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
   Magento_HipaaSales
   Magento_HipaaCustomer
   <truncated for brevity>
   ```

   Alle Module mit dem Präfix `Magento_Hipaa` müssen im Abschnitt Aktivierte Module aufgeführt werden.

## Funktionsverbesserungen für HIPAA-Bereitschaft

Die `magento/hipaa-ee`-Erweiterung führt einige Änderungen und Verbesserungen am Commerce-Basisprodukt ein. Die folgenden Abschnitte enthalten Details zu diesen Änderungen und dazu, wie sie das Basisprodukt ändern.

### Aktionsprotokolle

Audit-Protokollierung ist eine HIPAA-Anforderung. In Adobe Commerce zeichnet die Funktion [Aktionsprotokolle](../../systems/action-log.md) jede Änderung auf, die von einem Administrator bzw. einer Administratorin vorgenommen wurde, der bzw. die in Ihrem Geschäft arbeitet. Um HIPAA-Anforderungen für das Administratorprotokoll zu erfüllen, wurde die Funktion aktualisiert und erfasst alle Benutzer- und Kundenaktionen, die über die Admin-Benutzeroberfläche und durch API-Aufrufe ausgeführt werden.

Aktionsprotokolle erfassen auch Ereignisse, wenn Adobe-Services auf Ihre Speicherdaten zugreifen. Sie können diese Ereignisse identifizieren, indem Sie im Bericht „Aktionsprotokolle“ nach der Aktion „Daten außerhalb gesendet“ filtern.

#### Bericht zu Aktionslogs

Das _Aktionslogs_ Berichtsraster (**[!UICONTROL System]** > Aktionsprotokolle > Bericht) wurde geändert, um Kundenaktionen aufzunehmen, die über die Admin-Benutzeroberfläche und -API ausgeführt werden.

1. Es wurden zwei Spalten hinzugefügt:
   - ***Source***: Zeigt an, wo die Aktion ausgeführt wurde.
Werte: `Admin UI` | `Customer UI` | `REST API` | `SOAP API` | `GraphQL API`
   - ***Client-***: Zeigt den Client-Typ an.
Werte: customer | Administrator | Integration

2. Die Spalte ***Benutzername*** wurde in &quot;***&quot;***
   - ***Client-Kennung***: Zeigt die Anmelde-ID des Benutzers an, der die Aktion ausgeführt hat.
Werte:
      - eine E-Mail, wenn Client-Typ Kunde ist
      - Benutzername, wenn Client-Typ „Admin“ ist
      - ein Name, wenn Client-Typ „Integration“ ist

3. Die Spalte ***Vollständiger Aktionsname*** wurde in &quot;***&quot;***
   - ***Target***: Zeigt den Aktionsnamen an.
Werte:
      - Ein Endpunkt, wenn Source eine REST-API oder SOAP-API ist
      - Abfrage- oder Mutationsname einer GraphQL-API
      - Ein Aktionsname in einer Admin-Benutzeroberfläche oder Kunden-Benutzeroberfläche.

#### Konfigurieren von Admin-Aktionen für die Protokollierung

Diese Funktion ist nicht verfügbar, da alle Aktionen standardmäßig aufgezeichnet werden müssen.

### Einschränkung der HIPAA-Kundensuchergebnisse

Die HIPAA-Funktion zur Einschränkung von Suchergebnissen für Kunden in Adobe Commerce stellt die Einhaltung der HIPAA-Vorschriften sicher, indem der Zugriff auf geschützte Gesundheitsinformationen (PHI) und personenbezogene Daten (PII) eingeschränkt wird. Diese Funktion schränkt die Möglichkeit ein, Kundendatensätze basierend auf Benutzerrollen zu suchen und anzuzeigen, sodass nur autorisierte Benutzer auf diese Informationen zugreifen können.

#### Wichtigste Funktionen

- **Sucheinschränkungen**: Benutzende ohne die erforderlichen Rollen können nicht nach Kundendatensätzen suchen oder diese anzeigen.
- **Obligatorische Suche nach Zugriff**: Im Gegensatz zum standardmäßigen Adobe Commerce-Verhalten sind Kundeninformationen nicht ohne Suchen sichtbar. Dadurch wird sichergestellt, dass Benutzende spezifische Details zu einem Kunden kennen müssen, um seine Informationen zu finden.
- **Eingeschränkte Suchergebnisse**: Suchergebnisse, die den Kriterien entsprechen, sind auf 10 Datensätze beschränkt, sodass nur eine überschaubare Anzahl von Datensätzen gleichzeitig angezeigt wird.
- **Mindestanzahl von Filtern**: Benutzer müssen mindestens drei Filter anwenden (z. B. E-Mail, Nachname und Status), um eine Suche durchzuführen und sicherzustellen, dass die Suchen spezifisch und zielgerichtet sind.
- **Filterbenachrichtigungen**: Wenn Sucheinschränkungen aktiviert sind, werden Benutzende benachrichtigt, Filter anzuwenden, um ihre Suchergebnisse zu verfeinern.

#### Konfiguration

Die Konfiguration zur Begrenzung der Anzahl der Kunden in den Suchergebnissen befindet sich im Admin-Bereich unter **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Advanced]** > **[!UICONTROL Admin]** > **[!UICONTROL Admin Grids]**. Diese Konfiguration ist standardmäßig aktiviert, wenn die `hipaa-ee`-Erweiterung installiert ist.

- **Begrenzung der Anzahl der Kunden im Raster**: Mit dieser Einstellung können Sie die Begrenzung der Anzahl der Kunden, die in den Rastersuchergebnissen angezeigt werden, aktivieren oder deaktivieren.
- **Suchergebnis-Limit für Kundenraster**: Diese Einstellung gibt die maximale Anzahl von Kundendatensätzen an, die in den Rastersuchergebnissen angezeigt werden können.

#### Betroffene Funktionsbereiche

Die Suchergebniseinschränkungsfunktion gilt für Kundenraster auf der Seite Admin-Bestellung erstellen (**[!UICONTROL Sales]** > **[!UICONTROL Orders]** > **[!UICONTROL Create New Order]**) und der Seite Kunden (**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**).

- Filter werden standardmäßig geöffnet.
- Benutzer müssen mindestens drei Filter anwenden, um eine Suche durchzuführen.
- Suchergebnisse sind standardmäßig auf 10 Datensätze beschränkt.
- Wenn mehr Datensätze den Suchkriterien entsprechen, informieren Benachrichtigungen die Benutzer über die Ergebnisbegrenzung und die Notwendigkeit, ihre Suche zu verfeinern.
- Raster-Paginierung ist nicht verfügbar.
- Frühere Suchergebnisse und angewendete Filter werden beim Verlassen der Seite nicht gespeichert.

Die Suchergebniseinschränkungsfunktion gilt auch für die REST-API für die Kundensuche (`/V1/customers/search`).

- Ohne angewendete Filter oder mit unzureichenden Filtern gibt die API eine Fehlermeldung zurück, die angibt, dass die erforderliche Anzahl von Filtern zum Ausführen einer Suche erforderlich ist.
- Autorisierte Benutzer, die ausreichende Filter anwenden, erhalten API-Ergebnisse innerhalb des angegebenen Limits.
- Wenn die Ergebnisse begrenzt sind, wird der Antwort eine Meldung hinzugefügt, die die Gesamtzahl der gefundenen Datensätze und das aktuell angewendete Limit angibt.

### Funktionen importieren und exportieren

Die Verbesserungen der Import- und Exportfunktionen konzentrieren sich auf die Verbesserung des administrativen Erlebnisses und die Bereitstellung einer besseren Sichtbarkeit der Benutzeraktionen.

>[!NOTE]
>
>Diese ***Verbesserungen ändern nicht die Kernlogik zum Importieren und Exportieren*** sondern erweitern die Funktionalität, um eine umfassendere Protokollierung und eine verbesserte Datenzuordnung zu ermöglichen. Die grundlegende Funktionalität von Import und Export bleibt unverändert. Benutzer können die vorhandenen Funktionen und Workflows weiterhin unterbrechungsfrei verwenden.

#### Protokollierung administrativer Aktionen

Eine der wichtigsten Verbesserungen bei den Import- und Exportfunktionen ist die verbesserte Protokollierung von Verwaltungsaktionen. Diese Verbesserung bietet die Möglichkeit, tiefere Einblicke in Aktivitäten im Zusammenhang mit dem Datenimport und -export zu erhalten, was zu einer verbesserten Nachverfolgung und Auditierbarkeit beiträgt. Die folgenden Aktionen werden jetzt protokolliert und im Raster **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**&#x200B;angezeigt:

| Typ | Aktionen |
| ---- | ------- |
| importieren | <ul><li>Ein Administrator führt einen Import aus<li>Ein Administrator lädt eine importierte Datei herunter<li>Ein Administrator lädt eine Fehlerdatei herunter<ul/> |
| Export | <ul><li>Ein Administrator fordert an<li>Ein Administrator lädt eine exportierte Datei herunter<ul/> |
| Geplante Importe/Exporte | <ul><li>Ein Administrator plant den Export<li>Ein Administrator bearbeitet einen geplanten Export<li>Ein Administrator führt einen geplanten Export aus<li>Ein Administrator löscht einen geplanten Export<li>Ein Administrator plant einen Import<li>Ein Administrator bearbeitet einen geplanten Import<li>Ein Administrator führt einen geplanten Import aus<li>Ein Administrator löscht einen geplanten Import<li>Ein Administrator führt eine Massenlöschung von Import-/Exportvorgängen aus<ul/> |

### Verbesserungen bei der Anzeige und verbesserte Filterung und Sortierung

Um Admin-Benutzern die Möglichkeit zu geben, informativere Raster anzuzeigen, bietet der HIPAA-fähige Service mehrere Verbesserungen zum Anzeigen, Filtern und Sortieren von Daten.

#### Importverlauf ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Filterung für alle Spalten außer **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]** und **[!UICONTROL Summary]** aktiviert.

#### Export ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- **[!UICONTROL ID]** Spalte hinzugefügt.
- **[!UICONTROL Requested At]** Spalte hinzugefügt (_Datum und Uhrzeit der Exportanfrage_).
- Eine **[!UICONTROL User]** Spalte wurde hinzugefügt _Benutzername eines Administrators, der die Anfrage durchgeführt hat_).
- **[!UICONTROL Action]** Spalte entfernt.
- Der **[!UICONTROL Download]** Link wurde in eine **[!UICONTROL File name]** Spalte verschoben _z. B. das Raster Importverlauf_.
- Die Aktion zum Löschen einer exportierten Datei wurde deaktiviert _zur Verbesserung des Trackings_.
- Sortierung für alle Spalten außer **[!UICONTROL File name]** aktiviert.
- Filterung für alle Spalten aktiviert.

#### Geplante Importe und Exporte ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- **[!UICONTROL ID]** Spalte hinzugefügt.
- Eine **[!UICONTROL Scheduled At]** Spalte wurde hinzugefügt (_Datum und Uhrzeit der Planung des Imports oder Exports_).
- Eine **[!UICONTROL User]** Spalte wurde hinzugefügt (der _Benutzername eines Admin-Benutzers, der den Import oder Export geplant hat_).

## HIPAA-fähige Services und Tools

In diesem Abschnitt werden HIPAA-fähige Adobe-Services beschrieben, die für die Verwendung mit dem HIPAA-Angebot für Adobe Commerce verfügbar sind. Außerdem werden Tools beschrieben, mit denen Sie wichtige Sicherheits- und Compliance-Kontrollen für Ihren Store überwachen können.

| Service | Produktion | Staging | staging_for_support | Entwicklung |
|---------------------------------------|------------|---------|---------------------|-------------|
| Adobe Commerce mit Add-on für das Gesundheitswesen | Ja | Ja | Ja | Nein |
| SendGrid | Nein | Nein | Nein | Nein |
| AWS Simple Email Service | Ja | Ja | Ja | Nein |

### Adobe Commerce Services

In der folgenden Tabelle sind die Adobe Commerce-Services aufgeführt, die für das Angebot „HIPAA-Bereitschaft“ verfügbar sind. Zu diesen Services gehören unter anderem:

| Service | produktionsfremd | Produktion |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|------------|
| [Adobe Developer App Builder](https://developer.adobe.com/app-builder/docs/intro_and_overview/) | Ja | Ja |
| [API Mesh für Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/) | Ja | Ja |
| [SaaS-Datenexport](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview) | Ja | Ja |
| [Live-Suche](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview) | Nein | Nein |
| [Produktempfehlungen](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/overview) | Nein | Nein |
| [Zahlungsdienste](https://experienceleague.adobe.com/en/docs/commerce/payment-services/guide-overview) | Nein | Nein |
| [Back-Office-Ereignisse der Datenverbindung](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice) | Ja | Ja |
| [Datenverbindungs-Storefront-Ereignisse](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#storefront-events) | Nein | Nein |
| [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) | Nein | Nein |

### Tools

Mit dem [Security Scan Tool](../../systems/security-scan.md) für Adobe Commerce können Sie Ihren Store überwachen, um sicherzustellen, dass alle erforderlichen Sicherheitskontrollen aktiviert sind und betriebsbereit sind. Zusätzlich zu den standardmäßigen Sicherheitsprüfungen hat Adobe das Tool erweitert, um HIPAA-spezifische Prüfungen für Kundinnen und Kunden anzuzeigen, die das HIPAA-Angebot für Adobe Commerce verwenden. Die HIPAA-Prüfungen im Security Scan Tool sollen sicherstellen, dass:

- Auditing-Module sind nicht deaktiviert
- Die Zwei-Faktor-Authentifizierung (2FA) ist nicht deaktiviert
- Marketing-Funktionen sind deaktiviert
- Alle installierten Erweiterungen entsprechen einer vordefinierten Zulassungsliste
- Es sind keine nicht unterstützten Adobe-Services installiert

Sie können [das Tool konfigurieren](../../systems/security-scan.md#run-a-security-scan) um Ihnen E-Mail-Benachrichtigungen mit Details aus geplanten Scans zu senden oder [Berichte manuell anzuzeigen](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/launch/overview).

## Deaktivierte Funktionen

Um HIPAA-Anforderungen zu erfüllen, sind einige von Adobe Commerce unterstützte Funktionen standardmäßig entweder nicht verfügbar oder deaktiviert. Händler haben die Möglichkeit, diese Funktionen auf eigenes Risiko wieder zu aktivieren oder zu verwenden.

Die folgenden Funktionen sind im Modul HIPAA-Bereitschaft standardmäßig deaktiviert. Händler können diese Funktionen auf eigenes Risiko aktivieren.

- **[Transaktions-E-](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/project/sendgrid)**: SendGrid ist standardmäßig deaktiviert, da der Service nicht HIPAA-fähig ist. Adobe Commerce bietet eine Integrationsoption, die Sie mit Ihrem eigenen [AWS Simple Email Service](https://docs.aws.amazon.com/ses/)-Konto verwenden können. Weitere Konfigurationsdetails erhalten Sie von Ihrem Customer Technical Account Manager oder dem Adobe Commerce Support.

- **[Gast-Checkout](../../stores-purchase/checkout-guest.md)** - Diese Funktion stellt ein potenzielles Risiko für verschiedene Aspekte von HIPAA dar, einschließlich Protokollierung, Zugriffskontrolle, PHI-Hygiene und Herkunft und möglicherweise mehr.

- **[Newsletter-Funktion](../../merchandising-promotions/newsletters.md)** - Diese Funktion ist deaktiviert, um die Verwendung von PHI in einem Marketing-Kontext zu verhindern.

- **[Einstellung des erweiterten Reporting-](../../getting-started/business-intelligence.md)**: Diese Konfigurationseinstellung ist deaktiviert, um zu verhindern, dass PHI für die Analyse und das Reporting verwendet wird.
