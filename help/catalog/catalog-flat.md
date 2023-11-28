---
title: Flachkataloge
description: Erfahren Sie mehr über die Erstellung eines reduzierten Katalogs, in dem jede Zeile alle erforderlichen Daten zu einem Produkt oder einer Kategorie enthält.
exl-id: f67bd2e0-3902-41eb-b26f-c772a7692cef
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Flachkataloge

>[!IMPORTANT]
>
>Die Verwendung eines flachen Katalogs wird nicht mehr als Best Practice empfohlen. Die kontinuierliche Verwendung dieser Funktion führt bekanntermaßen zu Leistungsbeeinträchtigungen und anderen Indizierungsproblemen. Eine ausführliche Beschreibung und Lösung finden Sie im Abschnitt [Hilfe-Center](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/slow-performance-slow-and-long-running-crons.html).<br/><br/>Betroffene Versionen sind: <br/>- Adobe Commerce für Cloud-Infrastruktur, 2.3.x und höher<br/>- Adobe Commerce (On-Premise), 2.3.x und höher<br/>- Magento Open Source, 2.3.x und höher <br/><br/>Bei jeder Release-Version funktionieren einige Erweiterungen nur mit flachen Tabellen, wodurch ein Risiko entsteht, wenn flache Tabellen deaktiviert werden. Wenn Sie wissen, dass Sie einige Erweiterungen haben, die leere Katalogindizes verwenden, müssen Sie dieses Risiko beachten, wenn Sie diese Werte auf `No`.

Commerce speichert Katalogdaten normalerweise in mehreren Tabellen, basierend auf dem Entitäts-/Attribut-Wert-Modell (EAV). Da Produktattribute in vielen Tabellen gespeichert werden, sind SQL-Abfragen manchmal lang und komplex.

Dagegen erstellt ein flacher Katalog dynamisch Tabellen, wobei jede Zeile alle erforderlichen Daten über ein Produkt oder eine Kategorie enthält. Ein flacher Katalog wird automatisch aktualisiert - entweder jede Minute oder entsprechend Ihrem Cron-Auftrag. Eine einfache Katalogindizierung kann auch die Verarbeitung von Katalog- und Warenkorbpreisregeln beschleunigen. Ein Katalog mit bis zu 500.000 SKUs kann schnell als flacher Katalog indexiert werden.

>[!NOTE]
>
>Bevor Sie einen flachen Katalog für einen Live Store aktivieren, testen Sie die Konfiguration in einer Entwicklungsumgebung.

## Schritt 1: Einfache Kataloge aktivieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** darunter.

1. Erweitern Sie die _Storefront_ und führen Sie folgende Schritte aus:

   - Satz **[!UICONTROL Use Flat Catalog Category]** nach `Yes`. (Deaktivieren Sie bei Bedarf die **[!UICONTROL Use system value]** aktivieren.)

   - Satz **[!UICONTROL Use Flat Catalog Product]** nach `Yes`.

   ![Flachkatalogkonfiguration](./assets/use-flat-catalog.png){width="700" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf **[!UICONTROL Cache Management]** in der Systemmeldung und befolgen Sie die Anweisungen zum Aktualisieren des Caches.

## Schritt 2: Ergebnisse überprüfen

Es gibt zwei Methoden, mit denen Sie die Ergebnisse überprüfen können.

### Methode 1: Überprüfen der Ergebnisse für ein einzelnes Produkt

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Öffnen Sie ein Produkt im Bearbeitungsmodus.

1. Für **[!UICONTROL Name]**, Text hinzufügen `_TEST` an das Ende des Produktnamen.

1. Klicken **[!UICONTROL Save]**.

1. Navigieren Sie auf einer neuen Browser-Registerkarte zur Startseite Ihres Stores und führen Sie die folgenden Schritte aus:

   - Suchen Sie nach dem bearbeiteten Produkt.

   - Verwenden Sie die Navigation , um zum Produkt unter seiner zugewiesenen Kategorie zu navigieren.

     Aktualisieren Sie bei Bedarf die Seite, um die Ergebnisse anzuzeigen. Die Änderung wird innerhalb der Minute oder entsprechend Ihrer [Cron](../systems/cron.md) planen.

   ![Storefront mit reduziertem Katalog](./assets/storefront-flat-catalog-enabled.png){width="700" zoomable="yes"}

### Methode 2: Überprüfen der Ergebnisse für eine Kategorie

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Überprüfen Sie in der linken oberen Ecke, ob **[!UICONTROL Store View]** auf `All Store Views`.

   Klicken Sie bei entsprechender Aufforderung auf **[!UICONTROL OK]** zur Bestätigung.

1. Wählen Sie im Kategoriebaum eine vorhandene Kategorie aus und klicken Sie auf **[!UICONTROL Add Subcategory]** und führen Sie die folgenden Schritte aus:

   - Für **[!UICONTROL Category Name]**, eingeben `Test Category`.

   - Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

     ![Test-Unterkategorie](./assets/catalog-flat-test-category.png){width="600" zoomable="yes"}

   - Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Products in Category]** und klicken Sie auf **[!UICONTROL Reset Filter]** , um alle Produkte anzuzeigen.

   - Aktivieren Sie das Kontrollkästchen der verschiedenen Produkte, die der neuen Kategorie hinzugefügt werden sollen.

   - click **[!UICONTROL Save]**.

   ![Test-Kategorieprodukte](./assets/catalog-flat-test-category-products.png){width="600" zoomable="yes"}

1. Navigieren Sie auf einer neuen Browser-Registerkarte zur Startseite Ihres Stores und navigieren Sie mithilfe der Store-Navigation zu der von Ihnen erstellten Kategorie.

   Aktualisieren Sie bei Bedarf die Seite, um die Ergebnisse anzuzeigen. Die Änderung wird innerhalb der Minute oder entsprechend Ihrem Cron-Zeitplan angezeigt.

## Schritt 3: Testdaten entfernen

Führen Sie die folgenden Schritte aus, um die Testdaten zu entfernen und den ursprünglichen Produktnamen und die Katalogkonfiguration wiederherzustellen.

### Entfernen Sie die Testkategorie

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie in der Kategoriestruktur die von Ihnen erstellte Test-Unterkategorie aus.

1. Klicken Sie oben rechts auf **[!UICONTROL Delete]**.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.

   Bei dieser Kategorieentfernung werden die der Kategorie zugewiesenen Produkte nicht entfernt.

### Originalproduktnamen wiederherstellen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Öffnen Sie das Testprodukt im Bearbeitungsmodus.

1. Entfernen Sie die `_TEST` Text, den Sie zum **[!UICONTROL Product Name]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Save]**.

### Wiederherstellen der ursprünglichen Katalogkonfiguration

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** darunter.

1. Erweitern Sie die _Storefront_ und führen Sie folgende Schritte aus:

   - Satz **[!UICONTROL Use Flat Catalog Category]** nach `No`.

   - Satz **[!UICONTROL Use Flat Catalog Product]** nach `No`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

1. Wenn Sie dazu aufgefordert werden, aktualisieren Sie den Cache.
