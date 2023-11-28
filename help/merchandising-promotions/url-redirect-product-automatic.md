---
title: Automatische Umleitungen
description: Erfahren Sie, wie Sie automatische Weiterleitungen konfigurieren, die generiert werden, wenn sich der URL-Schlüssel eines Produkts oder einer Kategorie in Ihrem Commerce-Store ändert.
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Automatische Umleitungen

Ihr Store kann so konfiguriert werden, dass automatisch eine dauerhafte Umleitung generiert wird, sobald sich der URL-Schlüssel eines Produkts oder einer Kategorie ändert. Im Abschnitt Suchmaschinenoptimierung zeigt das Kontrollkästchen unter dem URL-Schlüssel an, ob dauerhafte Umleitungen aktiviert sind. Wenn Ihr Store bereits für die automatische Umleitung von Katalog-URLs konfiguriert ist, ist eine Umleitung eine einfache Aktualisierung des URL-Schlüssels. Der Prozess zum Erstellen einer automatischen Umleitung ist für Produkte und Kategorien identisch.

>[!NOTE]
>
>Wenn automatische Umleitungen aktiviert sind und Sie eine Kategorie speichern, werden alle Produkt- und Kategorienumschreibungen in Echtzeit generiert und standardmäßig in Datenbanktabellen gespeichert. Dies könnte zu erheblichen Leistungsproblemen bei Kategorien mit vielen zugewiesenen Produkten führen. Die Lösung besteht darin, diesen Standard zu ändern und die Generierung von Kategorie-/Produkt-URL-Neuschreibungen für Produkte beim Speichern von Kategorien zu überspringen. In diesem Fall werden Produktneuschreibungen nur für die kanonische Produkt-URL generiert.

## Automatische Umleitungen einrichten

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Search Engine Optimization]** Abschnitt.

   ![Katalogkonfiguration - Suchmaschinenoptimierung](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Produkt-URLs automatisch umleiten

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Suchen Sie das Produkt in der Liste und klicken Sie auf , um den Datensatz zu öffnen.

1. Erweitern ![Erweiterungsauswahl ](../assets/icon-display-expand.png) die **[!UICONTROL Search Engine Optimization]** Abschnitt.

   ![Optimierung der Produktsuchmaschine - dauerhafte Umleitung](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. Für **[!UICONTROL URL Key]** führen Sie folgende Schritte aus:

   - Stellen Sie sicher, dass die Variable **[!UICONTROL Create Permanent Redirect for old URL]** aktiviert ist. Falls nicht, befolgen Sie die Anweisungen unter [automatische Umleitungen aktivieren](url-rewrite.md#configure-url-rewrites).

   - Aktualisieren Sie die **[!UICONTROL URL Key]** bei Bedarf alle Kleinbuchstaben und nicht nachgestellten Bindestriche zwischen diesen Zeichen anstelle von Leerzeichen verwenden.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, folgen Sie den Links in der Meldung oben im Arbeitsbereich.

   Die permanente Umleitung ist jetzt für das Produkt und alle zugehörigen Kategorie-URLs in Kraft.

## Automatische Umleitung von Kategorie-URLs

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Suchen Sie die Kategorie im Baum und klicken Sie auf , um den Datensatz zu öffnen.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Search Engine Optimization]** Abschnitt.

1. Für **[!UICONTROL URL Key]** führen Sie folgende Schritte aus:

   - Stellen Sie sicher, dass die Variable **[!UICONTROL Create Permanent Redirect for old URL]** aktiviert ist. Falls nicht, befolgen Sie die Anweisungen unter [automatische Umleitungen aktivieren](url-rewrite.md#configure-url-rewrites).

   - Aktualisieren Sie die **[!UICONTROL URL Key]** bei Bedarf alle Kleinbuchstaben und nicht nachgestellten Bindestriche zwischen diesen Zeichen anstelle von Leerzeichen verwenden.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, folgen Sie den Links in der Meldung oben im Arbeitsbereich.

   Die permanente Umleitung ist jetzt für die Kategorie und alle zugehörigen Produkt-URLs in Kraft.

## Generierung von Produkt-URL-Neuschreibungen für Kategoriespeicherung überspringen {#skip-rewrite}

>[!WARNING]
>
>Wenn Sie die automatische Generierung der URL-Adresse für Kategorie/Produkte deaktivieren, werden alle vorhandenen URL-Neuschreibungen für Kategorie/Produkttyp dauerhaft entfernt, was nicht wiederhergestellt werden kann. Dies kann möglicherweise zu ungelösten Kategorie-/Produkttyp-URL-Konflikten führen, bei denen der URL-Schlüssel manuell aktualisiert werden muss.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Search Engine Optimization]** Abschnitt.

1. Satz **[!UICONTROL Generate "category/product" URL Rewrites]** nach `No`.

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL OK]** um die Änderung und das Entfernen bestehender URL-Neuschreibungen zu bestätigen.

   ![Kategorie-/Produkt-URL-Neuschreibungen deaktivieren - Bestätigen](./assets/seo-rewrite-off.png){width="350"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
