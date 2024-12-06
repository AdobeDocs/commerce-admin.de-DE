---
title: HIPAA-Bereitschaft für Adobe Commerce
description: Erfahren Sie, wie Sie in Adobe Commerce die Erweiterung für HIPAA-Konformität hinzufügen und zusätzliche Funktionen für die Einhaltung der HIPAA-Vorschriften nutzen können.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: cbcdaf8f5c531ba10a95e9455a5ebc28bd61c3b5
workflow-type: tm+mt
source-wordcount: '1597'
ht-degree: 1%

---

# HIPAA-Bereitschaft für Adobe Commerce

>[!IMPORTANT]
>
>**Haftungsausschluss**<br/>
>Diese Informationen sollen Adobe-Kunden bei der Beantwortung ihrer Fragen zu Adobe HIPAA-Ready Services helfen. Es handelt sich nicht um Rechtsberatung. Die Händler sollten sich mit ihrem Rechtsbeistand beraten, um ihre Verpflichtungen im Rahmen der HIPAA und die angemessene Verwendung und Konfiguration von Adobe-Produkten zu verstehen.

>[!BEGINSHADEBOX]

**Health Insurance Portability and Accounability Act (HIPAA)**

Der Health Insurance Portability and Accounability Act (HIPAA) ist das wichtigste Bundesdatenschutzgesetz in den USA und wird vom US-amerikanischen Gesundheitsministerium für Gesundheit und menschliche Dienstleistungen (HHS) durchgesetzt. Die HIPAA gilt für _abgedeckte Entitäten_ (z. B. Gesundheitsdienstleister, Versicherer und Clearinghäuser) und _Geschäftspartner_ (z. B. Unternehmen, die Dienstleistungen für abgedeckte Stellen erbringen). Die HIPAA-Anforderungen gelten für drei separate Regeln: Datenschutzregel, Sicherheitsregel und Regel für die Verletzung von Benachrichtigungen. Adobe fungiert als Business Associate für bestimmte Produkte, die von Adobe als &quot;HIPAA-Ready Services&quot;klassifiziert werden. Unter HIPAA regulierte Daten werden als _geschützte Gesundheitsinformationen_ oder PHI bezeichnet. PHI ist eine Untergruppe von Gesundheitsinformationen, die (1) von einem Gesundheitsdienstleister, einem Gesundheitsplan oder einem Clearinghaus für die Gesundheitsversorgung erstellt oder empfangen wird, (2) sich auf die frühere, aktuelle oder künftige physische oder psychische Gesundheit oder den Gesundheitszustand einer Person, die Gesundheitsversorgung einer Person oder die frühere, gegenwärtige oder künftige Zahlung für die Bereitstellung von Gesundheitsdienstleistungen an eine Person beziehen und (3) die Person oder die Grundlage für die Annahme gibt. die Informationen können zur Identifizierung der Person verwendet werden. Nach den HIPAA-Datenschutz- und -Sicherheitsregeln muss ein abgedecktes Unternehmen schriftliche Zusicherungen von einem Business Associate in Form eines Business Associate Agreement (BPA) erhalten, in denen es vom Business Associate (BAT) verlangt, die Privatsphäre und Sicherheit des PHI des abgedeckten Unternehmens zu schützen. Weitere Informationen finden Sie unter [HIPAA und Adobe Products and Services](https://www.adobe.com/trust/compliance/hipaa-ready.html) im Adobe Trust Center.

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA-bereit

Die Adobe Commerce HIPAA-Ready-Erweiterung fügt Adobe Commerce-Installationen zusätzliche Funktionen hinzu, mit denen Händler ihren jeweiligen HIPAA-Verpflichtungen nachkommen können.

Die Adobe Commerce HIPAA-Ready-Erweiterung `magento/hipaa-ee` ist für Adobe Commerce in Cloud-Infrastruktur- oder Adobe Managed Services-Projekten verfügbar. Der HIPAA-bereite Installationsprozess von Adobe Commerce deaktiviert einige native Dienste und Funktionen, um die HIPAA-Anforderungen zu erfüllen. Siehe [Deaktivierte Dienste und Funktionen](#disabled-services-and-features).

>[!NOTE]
>
>Der Zugriff auf die HIPAA-fähigen Funktionen ist nur für Händler verfügbar, die das Health Care Add-On für Adobe Commerce erworben haben.

*Diese Materialien dienen nur zu Informationszwecken. Die Bereitstellung dieser Informationen berechtigt den Empfänger nicht zu vertraglichen oder sonstigen Rechten. Es wurden zwar Anstrengungen unternommen, um die Richtigkeit der Informationen ab dem Zeitpunkt ihrer Bereitstellung sicherzustellen, es wird jedoch keine Darstellung dafür vorgenommen, dass diese Informationen korrekt und vollständig sind. Adobe verpflichtet sich nicht, diese Informationen zu aktualisieren, wenn sich das Recht oder die Adobe ändern. Außerdem darf dieses Dokument nur mit schriftlicher Zustimmung von Adobe an den vorgesehenen Empfänger weitergegeben werden.*

## Systemanforderungen

Adobe Commerce muss entweder auf Adobe Commerce in der Cloud-Infrastruktur oder auf Adobe Commerce Managed Services mit den Versionen 2.4.6-p3 - 2.4.6-p8 bereitgestellt werden (keine Beta-Versionen).

## Installation

**Voraussetzung**

>[!BEGINSHADEBOX]

- Adobe hat Ihr Adobe Commerce-Konto für den Zugriff auf die HIPAA Ready-Erweiterung bereitgestellt.
- Zugriff auf [repo.magento.com](https://repo.magento.com) , um die Erweiterung zu installieren. Informationen zur Schlüsselgenerierung und zum Abrufen der erforderlichen Berechtigungen finden Sie unter [Abrufen Ihrer Authentifizierungsschlüssel](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

>[!ENDSHADEBOX]

Installieren Sie die neueste Version der Adobe HIPAA-Ready Services-Erweiterung (`magento/hipaa-ee`) auf einer Instanz, auf der die Adobe Commerce-Version 2.4.6-p3 - 2.4.6-p8 ausgeführt wird. Die Erweiterung wird als Composer-Metapaket vom Repository [repo.magento.com](https://repo.magento.com) bereitgestellt. Das Metapaket umfasst die Sammlung von Modulen, die die HIPAA-Funktionen für eine Adobe Commerce-Instanz aktivieren.

1. Wechseln Sie auf Ihrer lokalen Workstation zum Projektverzeichnis für Ihr Adobe Commerce-Projekt in der Cloud-Infrastruktur-Projekt.

   >[!NOTE]
   >
   >Informationen zum lokalen Verwalten von Commerce-Projektumgebungen finden Sie unter [Verwalten von Verzweigungen mit der CLI](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) im _Benutzerhandbuch zu Adobe Commerce on Cloud Infrastructure_.

1. Checken Sie die Umgebungsverzweigung aus, die mit der Adobe Commerce Cloud-CLI aktualisiert werden soll.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Fügen Sie das Metapaket `magento/hipaa-ee` mithilfe der Composer-CLI zur Komponentenkonfiguration hinzu.

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. Aktualisieren Sie Package-Abhängigkeiten.

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. Fügen Sie den aktualisierten Code hinzu, übertragen Sie ihn und pushen Sie ihn in die Cloud-Umgebung.

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   Durch das Übermitteln der Aktualisierungen wird der [Commerce-Cloud-Bereitstellungsprozess](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) initiiert, um die Änderungen anzuwenden. Überprüfen Sie den Bereitstellungsstatus im [Bereitstellungsprotokoll](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

### Installation überprüfen

Nachdem die Aktualisierungen bereitgestellt wurden, überprüfen Sie, ob die `Hipaa*`-Erweiterung installiert ist.

1. Verwenden Sie SSH, um sich bei der Remote-Cloud-Umgebung anzumelden.

   ```shell
   magento-cloud ssh
   ```

1. Verwenden Sie in der Befehlszeile die Adobe Commerce-CLI, um den Modulstatus zu überprüfen.

   ```shell
   bin/magento module:status
   ```

1. Stellen Sie sicher, dass die HIPAA-Module in der Liste der aktivierten Module enthalten sind:

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

   Alle Module mit dem Präfix `Magento_Hipaa` müssen sich im Abschnitt &quot;Aktivierte Module&quot;befinden.

## Funktionsverbesserungen für HIPAA-Bereitschaft

Die `magento/hipaa-ee` -Erweiterung führt einige Änderungen und Verbesserungen am grundlegenden Commerce-Produkt ein. Die folgenden Abschnitte enthalten Details zu diesen Änderungen und wie sie das Basisprodukt ändern.

### Aktionsprotokolle

Die Prüfprotokollierung ist eine HIPAA-Anforderung. In Adobe Commerce erfasst die Funktion [Aktionsprotokolle](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) jede Änderung, die von einem in Ihrem Store tätigen Admin-Benutzer vorgenommen wurde. Um die HIPAA-Anforderungen für das Auditprotokoll zu erfüllen, wurde die Funktion aktualisiert und enthält nun alle Admin-Benutzer- und Kundenaktionen, die über die Admin-Benutzeroberfläche und über API-Aufrufe ausgeführt werden.

#### Bericht &quot;Action Logs&quot;

Das Berichtsraster _Aktionsprotokolle_ (**[!UICONTROL System]** > Aktionsprotokolle > Bericht) wurde geändert, um Kundenaktionen aufzunehmen, die über die Admin-Benutzeroberfläche und -API ausgeführt werden.

1. Es wurden zwei Spalten hinzugefügt:
   - ***Source***: Zeigt an, wo die Aktion ausgeführt wurde.
Werte: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Client-Typ***: Zeigt den Client-Typ an.
Werte: Kunde | Admin | Integration

2. Die Spalte ***Benutzername*** wurde in ***Client-Kennung*** umbenannt.
   - ***Client-Kennung***: Zeigt die Anmelde-ID des Benutzers an, der die Aktion ausgeführt hat.
Werte:
      - eine E-Mail, wenn der Client-Typ Kunde ist
      - einen Benutzernamen, wenn der Client-Typ Admin ist
      - einen Namen, wenn der Client-Typ Integration ist

3. Die Spalte ***Full Action Name*** wurde in ***Target*** umbenannt.
   - ***Ziel***: Zeigt den Aktionsnamen an.
Werte:
      - einen Endpunkt, wenn Source eine REST-API oder SOAP-API ist
      - einen Abfrage- oder Mutationsnamen, wenn eine GraphQL-API
      - einen Aktionsnamen, wenn es sich um eine Administrator-Benutzeroberfläche oder eine Kundenbenutzeroberfläche handelt.

#### Konfigurieren von Admin-Aktionen für die Protokollierung

Diese Funktion ist nicht verfügbar, da alle Aktionen standardmäßig aufgezeichnet werden müssen.

### Import- und Exportfunktionen

Die Verbesserungen bei Import- und Exportfunktionen konzentrieren sich auf die Verbesserung des administrativen Erlebnisses und die bessere Sichtbarkeit von Benutzeraktionen.

>[!NOTE]
>
>Diese ***Verbesserungen ändern nicht die Import- und Export-Kernlogik***, sondern erweitern die Funktionalität, um eine umfassendere Protokollierung und verbesserte Datenzuordnung zu bieten. Die grundlegende Funktionalität von Import und Export bleibt unverändert. Benutzer können die vorhandenen Funktionen und Workflows ohne Unterbrechung weiterhin verwenden.

#### Protokollierung administrativer Aktionen

Eine der wichtigsten Verbesserungen der Import- und Exportfunktionen ist die verbesserte Protokollierung von Verwaltungsaktionen. Diese Verbesserung bietet die Möglichkeit, Aktivitäten im Zusammenhang mit dem Datenimport und -export genauer zu untersuchen und so zu einer verbesserten Nachverfolgung und Auditbarkeit beizutragen. Die folgenden Aktionen werden nun protokolliert und im Raster **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**angezeigt:

| Typ | Aktionen |
| ---- | ------- |
| Import | <ul><li>Ein Administrator führt einen Import aus<li>Ein Administrator lädt eine importierte Datei herunter<li>Ein Administrator lädt eine Fehlerdatei herunter<ul/> |
| Export | <ul><li>Admin-Benutzeranforderungen<li>Ein Administrator lädt eine exportierte Datei herunter<ul/> |
| Geplante Importe/Exporte | <ul><li>Ein Administrator plant den Export von Zeitplänen<li>Ein Administrator bearbeitet einen geplanten Export<li>Ein Admin-Benutzer führt einen geplanten Export durch<li>Ein Admin-Benutzer löscht einen geplanten Export<li>Ein Admin-Benutzer plant den Import<li>Ein Administrator bearbeitet einen geplanten Import<li>Ein Admin-Benutzer führt einen geplanten Import durch<li>Ein Admin-Benutzer löscht einen geplanten Import<li>Ein Admin-Benutzer führt einen Massenlöschvorgang von Import-/Exportvorgängen aus<ul/> |

### Verbesserungen bei der Anzeige und verbesserte Filterung und Sortierung

Um Admin-Benutzern informativere Raster bereitzustellen, bietet der HIPAA-Ready-Dienst verschiedene Verbesserungen beim Anzeigen, Filtern und Sortieren von Daten.

#### Importverlauf ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Das Filtern aller Spalten mit Ausnahme von **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]** und **[!UICONTROL Summary]** wurde aktiviert.

#### Export ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- Es wurde eine **[!UICONTROL ID]** -Spalte hinzugefügt.
- Es wurde eine **[!UICONTROL Requested At]** -Spalte hinzugefügt (_Datum und Uhrzeit, zu der der Export angefordert wurde_).
- Eine Spalte **[!UICONTROL User]** wurde hinzugefügt (_Benutzername eines Administrators, der die Anfrage ausgeführt hat_).
- Eine **[!UICONTROL Action]** -Spalte wurde entfernt.
- Der Link **[!UICONTROL Download]** wurde in eine Spalte **[!UICONTROL File name]** verschoben (_wie das Raster &quot;Importverlauf&quot;_).
- Die Aktion, die für das Löschen einer exportierten Datei verantwortlich ist (_zur Verbesserung des Trackings_), wurde deaktiviert.
- Die Sortierung wurde für alle Spalten mit Ausnahme von **[!UICONTROL File name]** aktiviert.
- Die Filterung aller Spalten wurde aktiviert.

#### Geplante Importe und Exporte ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Es wurde eine **[!UICONTROL ID]** -Spalte hinzugefügt.
- Eine Spalte **[!UICONTROL Scheduled At]** wurde hinzugefügt (Datum und Uhrzeit, zu der der Import oder Export geplant wurde _)._
- Eine Spalte **[!UICONTROL User]** wurde hinzugefügt (der Benutzername _eines Admin-Benutzers, der den Import oder Export geplant hat_).

## Behinderte Dienste und Funktionen

Um HIPAA-Anforderungen zu entsprechen, sind einige von Adobe Commerce unterstützte Dienste und Funktionen entweder nicht verfügbar oder standardmäßig deaktiviert. Händler können diese Dienste und Funktionen auf eigene Gefahr erneut aktivieren oder verwenden.

### Dienste

- **Adobe Commerce-Dienste**: Keine der Adobe Commerce-Dienste oder Erweiterbarkeitsdienste sind unter dem HIPAA-Bereitstellungsangebot verfügbar. Zu diesen Diensten gehören unter anderem:

   - Live Search
   - API-Mesh
   - App Builder

- **Transaktions-E-Mail**—[SendGrid](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html) ist standardmäßig deaktiviert, da der Dienst nicht HIPAA-bereit ist. Adobe Commerce bietet eine Integrationsoption, die Sie mit Ihrem eigenen [AWS Simple Email Service](https://docs.aws.amazon.com/ses/) -Konto verwenden können. Konfigurationsdetails erhalten Sie von Ihrem technischen Kundenbetreuer oder vom Adobe Commerce-Support.

### Funktionen, die standardmäßig deaktiviert sind

Die folgenden Funktionen sind im HIPAA-Readiness-Modul standardmäßig deaktiviert. Händler können diese Funktionen auf eigene Gefahr aktivieren.

- **[Gast-Checkout](../stores-purchase/checkout-guest.md)** - Diese Funktion stellt ein potenzielles Risiko für verschiedene Aspekte von HIPAA dar, darunter Protokollierung, Zugriffskontrolle, PHI-Hygiene und -Herkunft sowie möglicherweise mehr.

- **[Newsletter-Funktion](../merchandising-promotions/newsletters.md)**: Diese Funktion ist deaktiviert, um zu verhindern, dass PHI in einem Marketingkontext verwendet wird.

- **[Erweiterte Einstellung des Reporting-Dienstes](../getting-started/business-intelligence.md)** - Diese Konfigurationseinstellung ist deaktiviert, um zu verhindern, dass PHI für die Analyse und Berichterstellung verwendet wird.
