---
title: Konfigurationsumfang
description: Erfahren Sie mehr über das Festlegen des Bereichs für Konfigurationseinstellungen in Commerce Admin.
exl-id: b7b87ac5-dc7d-472f-af24-52b4d12e46c5
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 0%

---

# Konfigurationsumfang

Die Store-Ansichtsauswahl in der linken oberen Ecke vieler Konfigurationsseiten filtert die Seitenansicht für einen bestimmten Bereich und legt den Wert einiger von Commerce verwendeter Entitäten fest. Sie listet jede Ebene in der Hierarchie nach Namen auf und wird verwendet, um den Bereich in eine andere Ebene zu ändern. Alle Einstellungen, die den aktuellen Bereich darstellen, sind ausgegraut, sodass nur die verfügbar sind, die die aktuelle Bereichseinstellung darstellen. Der Bereich ist zunächst auf _Standardkonfiguration“_. Für Admin-Benutzer mit eingeschränktem Zugriff enthält die Liste der verfügbaren Store-Ansichten nur die Ansichten, für die der Benutzer [Zugriffsberechtigung](../systems/permissions.md) hat.

| Ebene | Beschreibung |
|--- |--- |
| [!UICONTROL Default Config] | Die standardmäßige Systemkonfiguration. |
| [!UICONTROL Main Website] | Der Name der Website am Anfang der Hierarchie. |
| [!UICONTROL Main Website Store] | Der Name des Standardspeichers, der der übergeordneten Website zugeordnet ist. |
| [!UICONTROL Default Store View] | Der Name der standardmäßigen Store-Ansicht, die dem übergeordneten Store zugeordnet ist. |
| [!UICONTROL Stores Configuration] | Springt zum Stores-Raster. Dies entspricht der Auswahl von [!UICONTROL Stores] > [!UICONTROL All Stores] in der Admin -Seitenleiste. |

{style="table-layout:auto"}

![Kontrollkästchen „Systemwert verwenden“ aktiviert](./assets/store-view-control.png){width="700" zoomable="yes"}

## [!UICONTROL Use system value]

Das Kontrollkästchen _[!UICONTROL Use System Value]_&#x200B;rechts neben vielen Konfigurationseinstellungen wird verwendet, um den Standardwert im aktuellen Konfigurationsbereich entweder anzuwenden oder zu überschreiben. Der Wert des Standardfelds kann nicht geändert werden, wenn das Kontrollkästchen aktiviert wird. Um den Wert zu ändern, deaktivieren Sie das Kontrollkästchen und geben Sie den neuen Wert ein. Sobald Sie den Systemwert ändern, werden Sie zur Bestätigung aufgefordert.

Die Beschriftung des Kontrollkästchens ändert sich entsprechend dem aktuellen Umfang und bezieht sich immer auf die übergeordnete Ebene, die in der Bereichshierarchie eine Stufe höher liegt. Da die übergeordnete Ebene ein Container für alle Elemente unterhalb dieser Ebene ist, wird die Bereichseinstellung von der übergeordneten Ebene übernommen, es sei denn, sie wird überschrieben.

## Optionen für Standardwert

| Checkbox | Beschreibung |
|--- |--- |
| [!UICONTROL Use system value] | Dieses Kontrollkästchen wird angezeigt, wenn der Konfigurationsbereich auf `Default Config` festgelegt ist. |
| [!UICONTROL Use Default] | Dieses Kontrollkästchen wird angezeigt, wenn der Konfigurationsumfang auf `Website` festgelegt ist, und bezieht sich auf den Standardspeicher, der der Website zugewiesen ist. |
| [!UICONTROL Use Website] | Dieses Kontrollkästchen wird angezeigt, wenn der Konfigurationsbereich auf eine bestimmte Store-Ansicht festgelegt ist. Wenn diese Option aktiviert ist, wird die Einstellung aus der übergeordneten Website verwendet, die mit der Store-Ansicht verknüpft ist. In diesem Fall wird die Store-Ebene übersprungen, da sie auf den Standard-Store angewendet wird, der mit der Website verknüpft ist. |

{style="table-layout:auto"}

## Festlegen des Umfangs

Bevor Sie eine Konfigurationseinstellung vornehmen, die nur für eine bestimmte Website-, Store- oder Store-Ansicht gilt, gehen Sie wie folgt vor:

1. Führen Sie in _Seitenleiste_ Admin“ einen der folgenden Schritte aus:

   - Für die meisten Konfigurationseinstellungen navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - [Designbezogene Einstellungen](../content-design/configuration.md) finden Sie unter **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**. Wählen Sie dann im Raster die entsprechende Store-Ansicht aus.

1. Navigieren Sie zur zu ändernden Konfigurationseinstellung und gehen Sie wie folgt vor:

   - Legen Sie in der oberen linken Ecke **[!UICONTROL Store View]** auf die spezifische Ansicht fest, für die die Konfiguration gilt. Wenn Sie zum Bestätigen des Bereichswechsels aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.

     Nach jedem Feld wird ein Kontrollkästchen angezeigt, und möglicherweise werden zusätzliche Felder verfügbar.

   - Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** nach jedem Feld, das Sie bearbeiten möchten. Aktualisieren Sie dann den Wert für die Ansicht.

   - Wiederholen Sie diesen Vorgang für jedes Feld, das auf der Seite aktualisiert werden muss.

   ![Festlegen der Länderoptionen für die französische Store-Ansicht](./assets/store-view-french.png){width="700" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Kurzreferenz zum Umfang

| Umfang | Beschreibung |
|--- |--- |
| **[!UICONTROL Global]** |  |
| Administrator | Alle Websites, Stores und Store-Ansichten in der Installation werden von demselben Administrator verwaltet. |
| Standardkonfiguration | Die globalen [Standardkonfiguration](../getting-started/websites-stores-views.md#scope-settings)-Einstellungen werden über die Store-Hierarchie verwendet, es sei denn, sie werden auf einer niedrigeren Ebene überschrieben. |
| Katalog | Der Begriff _Katalog_ bezieht sich auf die Produktdatenbank als Ganzes und ist während der gesamten Installation verfügbar. |
| Produktpreise | Die Produktpreise können für die Anwendung entweder auf globaler oder auf Website-Ebene konfiguriert werden. |
| Produktkonfigurationen | Attribute, die als [konfigurierbare Produkt](../catalog/product-create-configurable.md)-Optionen verwendet werden, müssen einen globalen Gültigkeitsbereich haben. |
| Kunden | Kundenkonten können für die Anwendung auf globaler oder Website-Ebene konfiguriert werden. Jede Website kann über einen separaten Satz von [Kundenkonten](../customers/customer-account-scope.md) verfügen oder Kundenkonten für andere Websites in der Installation freigeben. |
| **[!UICONTROL Website]** |  |
| Domain | Zusätzliche [Websites](../stores-purchase/introduction.md#store-structure) können als Subdomains der primären Domain eingerichtet werden oder separate IP-Adressen und dedizierte Domains haben. |
| Kunden | Kundenkonten können für die Anwendung auf globaler oder Website-Ebene konfiguriert werden. Jede Website kann über einen separaten Satz von [Kundenkonten](../customers/customer-account-scope.md) verfügen oder Kundenkonten für andere Websites in der Installation freigeben. |
| Währung | Jeder Website kann eine andere [Basiswährung“ zugewiesen &#x200B;](../stores-purchase/currency-configuration.md). Die Basiswährung wird für die Verarbeitung aller Transaktionen verwendet, obwohl dem Kunden je nach Gebietsschema der Store-Ansicht eine andere Anzeigewährung angezeigt werden kann. |
| PRODUCT | Einzelne Produkte werden der Hierarchie auf Website-Ebene zugewiesen. Das Produktraster listet alle Produkte im Katalog sowie die Websites auf, auf denen sie verfügbar sind. Die Einstellung [Produkt auf Websites](../catalog/settings-basic-websites.md) gibt jede Website an, auf der das Produkt verfügbar ist. |
| Produktpreise | [Produktpreise](../catalog/catalog-price-scope.md) können für die Anwendung entweder auf globaler oder auf Website-Ebene konfiguriert werden. |
| Zahlungsmethoden | [Zahlungsmethoden](../stores-purchase/payments.md) werden auf Website-Ebene konfiguriert, obwohl der Titel und die Anweisungen für jede Shop-Ansicht konfiguriert werden können. |
| Checkout | Der [Checkout](../stores-purchase/checkout-process.md)Prozess findet auf Website-Ebene statt, obwohl einige Anzeigeoptionen für jede Shop-Ansicht konfiguriert werden können. Alle mit einer Website verknüpften Stores haben dieselbe [Checkout-Konfiguration](../stores-purchase/checkout-process.md#checkout-options). |
| Zugelassene Länder | Zugelassene Länder können auf Website-Ebene konfiguriert werden. Die Einstellungen [Zugelassene Länder](../getting-started/store-details.md#country-options) werden beim Checkout verwendet, um zu begrenzen, woher ein Kunde kommen kann. |
| **[!UICONTROL Store]** |  |
| Domain | Bei mehreren Stores kann jeder Store dieselbe Domain, eine Subdomain oder deutlich unterschiedliche Domains haben. Weitere Informationen finden Sie unter [&#x200B; von Stores](../stores-purchase/stores.md#add-stores). |
| Root Category | Jeder Store kann über einen separaten Satz von Produkten und ein Hauptmenü verfügen, das auf einer „Stamm“-Kategorie und Unterkategorien basiert. Jeder Katalog verfügt über eine [Stammkategorie](../catalog/category-root.md) die auf Store-Ebene zugewiesen wird. |
| **[!UICONTROL Store View]** |  |
| Unterkategorien | Die [Unterkategorien](../catalog/category-create.md#category-structure) aus denen das Hauptmenü (unter dem Stamm) besteht, werden auf Store-Ansichtsebene zugewiesen. |
| Gebietsschema | Jeder Shop-Ansicht kann ein anderes [Gebietsschema“ &#x200B;](../getting-started/store-details.md#locale-options) werden. Die Anzeigewährung, die Maßeinheiten und die Admin-Benutzeroberfläche sind spezifisch für das Gebietsschema. |
| Languages | Um mehrere Sprachen zu unterstützen, müssen alle Inhalte, einschließlich Produktbeschreibungen[&#x200B; für &#x200B;](../stores-purchase/store-localize.md#localize-products) Store-Ansicht übersetzt werden. |
| Währung anzeigen | Für jede Store[Ansicht kann eine andere &#x200B;](../stores-purchase/currency-configuration.md)Anzeigewährung“ verwendet werden, obwohl die Transaktionen auf Website-Ebene unter Verwendung der Basiswährung verarbeitet werden. |

{style="table-layout:auto"}
