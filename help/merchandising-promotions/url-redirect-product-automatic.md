---
title: Automatische Weiterleitungen
description: Erfahren Sie, wie Sie automatische Weiterleitungen konfigurieren, die generiert werden, wenn sich der URL-Schlüssel eines Produkts oder einer Kategorie in Ihrem Commerce Store ändert.
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
source-git-commit: d088d5833b9c61e7b1c90a0839fdf38527929ce5
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Automatische Weiterleitungen

Ihr Store kann so konfiguriert werden, dass er automatisch eine permanente Weiterleitung generiert, wenn sich der URL-Schlüssel eines Produkts oder einer Kategorie ändert. Im Abschnitt Suchmaschinenoptimierung zeigt das Kontrollkästchen unter dem URL-Schlüssel an, ob dauerhafte Weiterleitungen aktiviert sind. Wenn Ihr Geschäft bereits so konfiguriert ist, dass Katalog-URLs automatisch Redirect werden, ist eine Redirect eine einfache Aktualisierung des URL Schlüssels. Der Prozess zum Erstellen einer automatischen Umleitung ist für Produkte und Kategorien identisch.

>[!NOTE]
>
>Wenn automatische Weiterleitungen aktiviert sind und Sie eine Kategorie speichern, werden alle Produkt- und Kategorieumschreibungen in Echtzeit generiert und standardmäßig in Datenbanktabellen gespeichert. Dies kann bei Kategorien mit vielen zugewiesenen Produkten zu erheblichen Leistungsproblemen führen. Die Lösung besteht darin, diese Standardeinstellung zu ändern und die Generierung von Kategorie-/Produkt-URL-Neuschreibungen für Produkte beim Speichern der Kategorie zu überspringen. In diesem Fall werden Produktneuschreibungen nur für die kanonische Produkt-URL generiert.

## Einrichten automatischer Weiterleitungen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich und **[!UICONTROL Catalog]** wählen Sie darunter aus **[!UICONTROL Catalog]** .

1. ![Erweitern Erweiterung Selektor](../assets/icon-display-expand.png) den **[!UICONTROL Search Engine Optimization]** Abschnitt.

   ![Katalogkonfiguration – Search Engine Optimization](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** Festlegen bis `Yes`.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.


>[!NOTE]
>
> URL-Neuschreibungen können für die Store-Ansicht oder den Website-Umfang generiert werden. Festlegen die URL Umfang vom Administrator unter **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Catalog]****[!UICONTROL Configuration]**> >**[!UICONTROL Search Engine Optimization]****[!UICONTROL Catalog]**neu schreiben. Wählen Sie die Umfang im_[!UICONTROL Product URL Rewrite Scope]_ Feld aus.

## Produkt-URLs automatisch Redirect

1. Gehen Sie in der _Admin-Seitenleiste_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Suchen Sie das Produkt im Liste und klicken Sie, um den Datensatz zu öffnen.

1. ![Erweitern Expansion Selektor ](../assets/icon-display-expand.png) den **[!UICONTROL Search Engine Optimization]** Abschnitt.

   ![Optimierung der Produktsuchmaschine - permanente Weiterleitung](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. Gehen Sie **[!UICONTROL URL Key]** wie folgt vor:

   - Stellen Sie sicher, dass das Kontrollkästchen **[!UICONTROL Create Permanent Redirect for old URL]** aktiviert ist. Falls nicht, befolgen Sie die Anweisungen zum [Aktivieren automatischer Weiterleitungen](url-rewrite.md#configure-url-rewrites).

   - Aktualisieren Sie die Datei **[!UICONTROL URL Key]** nach Bedarf, indem Sie anstelle von Leerzeichen nur Kleinbuchstaben und nicht nachfolgende Bindestriche zwischen diesen Zeichen verwenden.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, folgen Sie den Links in der Nachricht oben im Arbeitsbereich.

   Die permanente Umleitung ist jetzt für das Produkt und alle zugehörigen Kategorie-URLs aktiv.

## Kategorie-URLs automatisch umleiten

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Suchen Sie die Kategorie im Baum und klicken Sie, um den Datensatz zu öffnen.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Search Engine Optimization]** .

1. Führen **[!UICONTROL URL Key]** Sie für folgende Schritte durch:

   - Stellen Sie sicher, dass das Kontrollkästchen **[!UICONTROL Create Permanent Redirect for old URL]** markiert ist. Ist dies nicht der Fall, folgen Sie die Anweisungen](url-rewrite.md#configure-url-rewrites), um automatische Weiterleitungen zu [aktivieren.

   - Aktualisieren Sie die Datei **[!UICONTROL URL Key]** nach Bedarf, indem Sie anstelle von Leerzeichen nur Kleinbuchstaben und nicht nachfolgende Bindestriche zwischen diesen Zeichen verwenden.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, folgen Sie den Links in der Nachricht oben im Arbeitsbereich.

   Die permanente Redirect gilt nun für die Kategorie und alle zugehörigen Produkt-URLs.

## Überspringen Produktgenerierung URL schreibt für Kategorie zurück {#skip-rewrite}

>[!WARNING]
>
>Das Deaktivieren der automatischen Generierung von Kategorie/Produkten URL Umschreibungen führt dazu, dass alle vorhandenen Kategorie-/Produkttypen URL Umschreibungen dauerhaft entfernt werden, die nicht wiederhergestellt werden können. Dies kann potenziell zu ungelösten Kategorie-/Produkttypkonflikten URL führen, die eine manuelle Aktualisierung des URL Schlüssels erfordern, um sie zu lösen.

1. Wechseln Sie in der _Admin-Seitenleiste_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich und **[!UICONTROL Catalog]** wählen Sie darunter aus **[!UICONTROL Catalog]** .

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Search Engine Optimization]** .

1. Legen Sie **[!UICONTROL Generate "category/product" URL Rewrites]** auf `No` fest.

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL OK]** , um die Änderung und das Entfernen vorhandener URL-Neuschreibungen zu bestätigen.

   ![Kategorie-/Produkt-URL Umschreibungen deaktivieren – bestätigen](./assets/seo-rewrite-off.png){width="350"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
