---
title: Versionshinweise zur KI-Produktsuche
description: Lesen Sie die Versionshinweise zur KI-Produkterkennung für Funktionen zur Katalog- und PDP-Anreicherung, Fehlerbehebungen, Upgrade-Anleitungen, unterstützte Commerce-Versionen und bekannte Probleme.
feature: Release Notes
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%
---
# Versionshinweise zur KI-Produkterkennung

In diesen Versionshinweisen werden Aktualisierungen der Kataloganreicherung und der PDP-Anreicherung beschrieben, einschließlich neuer Funktionen, Fehlerbehebungen, Upgrade-Anforderungen und bekannter Probleme. Jeder Versionseintrag identifiziert die betroffene Erweiterung oder den betroffenen Workflow.

![Neu](../assets/new.svg) Neue Funktionen
![Problem behoben](../assets/fix.svg) Fehlerbehebungen und Verbesserungen
![Bekanntes Problem](../assets/bug.svg) Bekannte Probleme

## Version 2.1.3 {#release-2-1-3}

*30. November 2026*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} [!DNL Adobe Commerce] 2.4.9, 2.4.8 und 2.4.7 in PHP 8.3 bis 8.5. [!DNL Adobe Commerce as a Cloud Service]

In Version 2.1.3 wird die Anreicherung von Produktdetailseiten mit der Kataloganreicherung zu einem neuen Admin-Menüelement namens **KI-Produkterkennung** kombiniert. Darüber hinaus umfasst die Unterstützung [!DNL Adobe Commerce as a Cloud Service].

## Version 2.1.2 {#release-2-1-2}

*22. Oktober 2026*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} [!DNL Adobe Commerce] 2.4.9, 2.4.8 und 2.4.7 in PHP 8.3 bis 8.5.

Version 2.1.2 macht die Kataloganreicherung zu einer eigenständigen Erweiterung. Sie enthält jetzt alles, was zuvor von der separaten [!DNL Adobe Brand Visibility]-Erweiterung (`magento/llm-optimizer`) bereitgestellt wurde: Anwenden genehmigter Vorschläge auf den Katalog, Zurücksetzen dieser Vorschläge und Schützen der eigenen Bearbeitungen vor Überschreibungen.

### Upgrade von früheren Versionen {#upgrade-from-earlier-versions}

>[!IMPORTANT]
>
>Version 2.1.2 kann nicht zusammen mit der [!DNL Adobe Brand Visibility]-Erweiterung installiert werden. Wenn Sie es installiert haben, entfernen Sie es als Teil des Upgrades.

1. Entfernen Sie die [!DNL Adobe Brand Visibility] Erweiterung, falls sie installiert ist:

   ```bash
   composer remove magento/llm-optimizer
   ```

   Wenn die Erweiterung durch Kopieren oder Symlinking von `Magento/LlmoCatalog` nach `app/code` installiert wurde, löschen Sie dieses Verzeichnis. Deaktivieren Sie nicht nur das Modul . Ein deaktiviertes Modul, das sich noch auf der Festplatte befindet, kann dazu führen, dass `setup:upgrade` die Tabelle verwerfen, in der die Originalwerte von angereicherten Produkten gespeichert sind.

1. Aktualisieren Sie die Kataloganreicherung und wenden Sie die Änderungen an:

   ```bash
   composer require magento/module-catalog-enrichment:^2.1
   bin/magento setup:upgrade
   bin/magento cache:flush
   ```

   Leeren Sie den Cache nach dem Upgrade. Bei einem Upgrade werden bestehende Zugriffsberechtigungen auf neue Berechtigungsressourcen verschoben, und diese Berechtigungen werden erst wirksam, wenn der Cache gelöscht wird.

### Anforderungen

![Neu](../assets/new.svg) **PHP 8.3 und [!DNL Adobe Commerce] 2.4.7 oder höher**—PHP 8.1 ist das Ende des Lebenszyklus und PHP 8.2 erreicht am 31. Dezember 2026 das Ende des Lebenszyklus, sodass keines von beiden unterstützt wird. [!DNL Adobe Commerce] 2.4.6 und früher werden nicht unterstützt.

### Neue Funktionen

![Neu](../assets/new.svg) Menü **[!UICONTROL AI Product Discovery]** - Die Seiten zur Kataloganreicherung haben jetzt einen eigenen Abschnitt in der Admin-Seitenleiste. Navigieren Sie zu **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**. Zuvor war die Seite unter **[!UICONTROL Catalog]**.

![Neu](../assets/new.svg) [!BADGE Beta]{type=Informative tooltip="Noch nicht allgemein verfügbar"} **[!UICONTROL Product Details Page Enrichment (Beta)]** - Eine neue Seite unter **[!UICONTROL AI Product Discovery]**, auf der Anreicherungsvorschläge für Produktdetailseiten überprüft werden können. Die Anreicherung der Produktdetailseite befindet sich in der Beta-Phase und ist noch nicht allgemein verfügbar.

![Neu](../assets/new.svg) **Genehmigte Vorschläge anwenden und zurücksetzen** - Genehmigte Name- und Beschreibungsaktualisierungen werden von dieser Erweiterung in den Katalog geschrieben. Commerce zeichnet den ursprünglichen Wert jedes angereicherten Attributs auf, wenn es sich zum ersten Mal ändert. Daher wird bei einem Rollback immer der Wert wiederhergestellt, den Sie vor der Anreicherung hatten, auch nachdem mehrere Vorschläge auf dasselbe Attribut angewendet wurden.

![Neu](../assets/new.svg) **Ihre Bearbeitungen werden berücksichtigt** - Wenn Sie einen angereicherten Namen oder eine Beschreibung im Admin-Produktformular ändern, mit **[!UICONTROL Update Attributes]** oder durch einen Import, wird Ihr Wert beibehalten und der zugehörige Vorschlag wird *Veraltet*. Eine Änderung am Standardbereich betrifft nur Store-Ansichten, die den Wert erben.

![Neu](../assets/new.svg) **Schreibgeschützter Katalogzugriff für Vorschläge** - [!DNL Commerce Catalog Agent] können Produkt-, Kategorie-, Attributsatz- und Produkttypdaten lesen, um Produkte für die Analyse auszuwählen. Der Lesevorgang gibt nur Attribute zurück, die mit **[!UICONTROL Used in Product Listing]** gekennzeichnet sind, sowie die Attribute, die angereichert werden können. Katalogdaten können nicht geändert werden.

### Fehlerbehebungen und Verbesserungen

![Problem behoben](../assets/fix.svg) **Erfolge beim Anwenden von Berichten** - Wenn eine Anfrage zum Anwenden nach bereits abgeschlossenem Vorgang erneut versucht wird, werden die Änderungen jetzt als angewendet gemeldet, anstatt keine Änderungen zu melden. Nichts wird zweimal geschrieben.

![Problem behoben](../assets/fix.svg) **Nur genehmigte Services können den Katalog ändern**—Apply und Rollback akzeptieren nur Anfragen von [!DNL Commerce Catalog Agent]. Zuvor wurde jedes gültige Adobe IMS-Token akzeptiert. Dieselbe Prüfung gilt jetzt auch für SOAP-Anfragen.

![Problem behoben](../assets/fix.svg) **deutlichere Fehler** - Ein Adobe IMS-Ausfall gibt jetzt `401` anstelle von `500` zurück, sodass die Anfrage nicht erneut für den Katalog versucht wird und eine nicht erkannte Adobe IMS-Umgebung abgelehnt wird, anstatt als Staging behandelt zu werden.

![Problem behoben](../assets/fix.svg) **Adobe IMS-Umgebung** - Die Kataloganreicherung meldet sich jetzt standardmäßig bei der Adobe IMS-Produktionsumgebung an, einschließlich der Instanzen, die mit einem [!DNL Commerce Services]-Datenbereich verbunden sind. Zuvor wurden diese Instanzen an die Staging-Umgebung gesendet.

![Problem behoben](../assets/fix.svg) **Anmelden nach der [!DNL Adobe Brand Visibility] Domain-Änderung** - Die Seite Kataloganreicherung wird jetzt von `abv.adobe.com` geladen, was eine Anmeldungsschleife behebt, nachdem die vorherige Domain weitergeleitet wurde.

### Bekannte Probleme

![Bekanntes Problem](../assets/bug.svg) **Rollen mit [!UICONTROL Catalog] Zugriff** - Eine Benutzerrolle, die vor dieser Version gespeichert wurde und der **[!UICONTROL Catalog]** Zugriff gewährt wurde, behält den Zugriff auf die **[!UICONTROL Catalog Enrichment Service API]** Ressource. Überprüfen Sie diese Rollen in **[!UICONTROL System]** > **[!UICONTROL Permissions]** > **[!UICONTROL User Roles]** und löschen Sie die Ressource, in der sie nicht benötigt wird.

## Version 1.0.2 {#release-1-0-2}

Erste Version der Admin-Seite für die Kataloganreicherung. Erfordert, dass die [!DNL Adobe Brand Visibility] Erweiterung Vorschläge auf den Katalog anwendet.
