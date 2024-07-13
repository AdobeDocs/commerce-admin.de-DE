---
title: Konfigurationsbereich
description: Erfahren Sie mehr über das Festlegen des Umfangs für Konfigurationseinstellungen in der Commerce-Admin-Konsole.
exl-id: b7b87ac5-dc7d-472f-af24-52b4d12e46c5
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 0%

---

# Konfigurationsbereich

Die Option &quot;Store-Ansicht&quot;in der oberen linken Ecke vieler Konfigurationsseiten filtert die Seitenansicht für einen bestimmten Bereich und legt den Wert einiger Entitäten fest, die von Commerce verwendet werden. Er listet alle Ebenen in der Hierarchie nach Namen auf und wird verwendet, um den Bereich in eine andere Ebene zu ändern. Alle Einstellungen, die den aktuellen Umfang darstellen, sind grau dargestellt, sodass nur die Einstellungen verfügbar sind, die den aktuellen Umfang darstellen. Der Gültigkeitsbereich ist zunächst auf _Standardkonfiguration_ eingestellt. Für Admin-Benutzer mit eingeschränktem Zugriff enthält die Liste der verfügbaren Store-Ansichten nur die Ansichten, auf die der Benutzer [Berechtigung](../systems/permissions.md) hat.

| Ebene | Beschreibung |
|--- |--- |
| [!UICONTROL Default Config] | Die standardmäßige Systemkonfiguration. |
| [!UICONTROL Main Website] | Der Name der Website oben in der Hierarchie. |
| [!UICONTROL Main Website Store] | Der Name des Standardspeichers, der mit der übergeordneten Website verknüpft ist. |
| [!UICONTROL Default Store View] | Der Name der standardmäßigen Store-Ansicht, die mit dem übergeordneten Store verknüpft ist. |
| [!UICONTROL Stores Configuration] | Wechselt zum Raster &quot;Stores&quot;und entspricht der Auswahl von [!UICONTROL Stores] > [!UICONTROL All Stores] in der Admin-Seitenleiste. |

{style="table-layout:auto"}

![Aktivieren Sie die aktivierten Kontrollkästchen &quot;Systemwert&quot;](./assets/store-view-control.png){width="700" zoomable="yes"}

## [!UICONTROL Use system value]

Das Kontrollkästchen _[!UICONTROL Use System Value]_rechts von vielen Konfigurationseinstellungen wird verwendet, um den Standardwert für das Feld innerhalb des aktuellen Konfigurationsbereichs anzuwenden oder zu überschreiben. Der Standardwert für das Feld kann nicht geändert werden, wenn das Kontrollkästchen aktiviert wird. Um den Wert zu ändern, deaktivieren Sie das Kontrollkästchen und geben Sie den neuen Wert ein. Sie werden beim Ändern des Systemwerts zur Bestätigung aufgefordert.

Die Beschriftung des Kontrollkästchens ändert sich entsprechend dem aktuellen Umfang und bezieht sich immer auf die übergeordnete Ebene, die in der Bereichshierarchie einen Schritt nach oben ist. Da die übergeordnete Ebene ein Container für alle Elemente unterhalb dieser Ebene ist, wird die Scope-Einstellung von der übergeordneten Ebene übernommen, es sei denn, sie wird überschrieben.

## Optionen für Standardwerte

| Kontrollkästchen | Beschreibung |
|--- |--- |
| [!UICONTROL Use system value] | Dieses Kontrollkästchen wird angezeigt, wenn der Konfigurationsbereich auf `Default Config` festgelegt ist. |
| [!UICONTROL Use Default] | Dieses Kontrollkästchen wird angezeigt, wenn der Konfigurationsbereich auf &quot;Main `Website`&quot;festgelegt ist, und bezieht sich auf den Standardspeicher, der der Website zugewiesen ist. |
| [!UICONTROL Use Website] | Dieses Kontrollkästchen wird angezeigt, wenn der Konfigurationsbereich auf eine bestimmte Store-Ansicht festgelegt ist. Wenn diese Option aktiviert ist, wird die Einstellung der übergeordneten Website verwendet, die mit der Store-Ansicht verknüpft ist. In diesem Fall wird die Store-Ebene übersprungen, da sie für den Standardspeicher gilt, der mit der Website verknüpft ist. |

{style="table-layout:auto"}

## Festlegen des Umfangs

Bevor Sie eine Konfigurationseinstellung vornehmen, die nur für eine bestimmte Website-, Store- oder Store-Ansicht gilt, gehen Sie wie folgt vor:

1. Führen Sie auf der Seitenleiste _Admin_ einen der folgenden Schritte aus:

   - Die meisten Konfigurationseinstellungen finden Sie unter **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - Gehen Sie für [designbezogene Einstellungen](../content-design/configuration.md) zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**. Wählen Sie dann im Raster die entsprechende Store-Ansicht aus.

1. Navigieren Sie zur Konfigurationseinstellung, die geändert werden soll, und führen Sie die folgenden Schritte aus:

   - Setzen Sie oben links **[!UICONTROL Store View]** auf die spezifische Ansicht, für die die Konfiguration gilt. Wenn Sie aufgefordert werden, den Perimeterwechsel zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

     Nach jedem Feld wird ein Kontrollkästchen angezeigt und es können zusätzliche Felder verfügbar werden.

   - Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** nach jedem Feld, das Sie bearbeiten möchten. Aktualisieren Sie dann den Wert für die Ansicht.

   - Wiederholen Sie diesen Vorgang für jedes Feld, das auf der Seite aktualisiert werden muss.

   ![Festlegen der Länderoptionen der französischen Store-Ansicht](./assets/store-view-french.png){width="700" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Schnellverweis zum Umfang

| Anwendungsbereich | Beschreibung |
|--- |--- |
| **[!UICONTROL Global]** |  |
| Admin | Alle Websites, Stores und Store-Ansichten in der Installation werden von demselben Administrator verwaltet. |
| Standardkonfiguration | Die globalen [Standardkonfigurationseinstellungen](../getting-started/websites-stores-views.md#scope-settings) werden in der Store-Hierarchie verwendet, es sei denn, sie werden auf einer niedrigeren Ebene überschrieben. |
| Katalog | Der Begriff _Katalog_ bezieht sich auf die Produktdatenbank als Ganzes und ist während der gesamten Installation verfügbar. |
| Produktpreise | Die Produktpreise können entweder global oder auf Website-Ebene für die Anwendung konfiguriert werden. |
| Produktkonfigurationen | Attribute, die als [konfigurierbare Produktoptionen](../catalog/product-create-configurable.md) verwendet werden, müssen einen globalen Gültigkeitsbereich haben. |
| Kunden | Kundenkonten können für Anwendungen auf globaler oder Website-Ebene konfiguriert werden. Jede Website kann über einen separaten Satz von [Kundenkonten](../customers/customer-account-scope.md) verfügen oder Kundenkonten für andere Websites in der Installation freigeben. |
| **[!UICONTROL Website]** |  |
| Domäne | Zusätzliche [Websites](../stores-purchase/introduction.md#store-structure) können als Subdomänen der primären Domäne eingerichtet werden oder über separate IP-Adressen und dedizierte Domänen verfügen. |
| Kunden | Kundenkonten können für Anwendungen auf globaler oder Website-Ebene konfiguriert werden. Jede Website kann über einen separaten Satz von [Kundenkonten](../customers/customer-account-scope.md) verfügen oder Kundenkonten für andere Websites in der Installation freigeben. |
| Währung | Jeder Website kann eine andere [Basiswährung](../stores-purchase/currency-configuration.md) zugewiesen werden. Die Basiswährung wird zur Verarbeitung aller Transaktionen verwendet, obwohl dem Kunden je nach Gebietsschema der Store-Ansicht möglicherweise eine andere Anzeigewährung angezeigt wird. |
| Produkte | Einzelne Produkte werden der Hierarchie auf Website-Ebene zugewiesen. Im Raster Produkte werden alle Produkte des Katalogs und die Websites aufgelistet, auf denen sie verfügbar sind. Mit der Einstellung &quot;[Produkt in Websites](../catalog/settings-basic-websites.md)&quot;werden die einzelnen Websites identifiziert, auf denen das Produkt verfügbar ist. |
| Produktpreise | [Produktpreise](../catalog/catalog-price-scope.md) können für Anwendungen entweder auf globaler oder auf Website-Ebene konfiguriert werden. |
| Zahlungsmethoden | [Zahlungsmethoden](../stores-purchase/payments.md) werden auf Website-Ebene konfiguriert, obwohl der Titel und die Anweisungen für jede Store-Ansicht konfiguriert werden können. |
| Checkout | Der [Checkout-Prozess](../stores-purchase/checkout-process.md) findet auf Website-Ebene statt, obwohl einige Anzeigeoptionen für jede Store-Ansicht konfiguriert werden können. Alle Stores, die mit einer Website verknüpft sind, haben dieselbe [Checkout-Konfiguration](../stores-purchase/checkout-process.md#checkout-options). |
| Zugelassene Länder | Zulässige Länder können auf Website-Ebene konfiguriert werden. Die Einstellungen für [zulässige Länder](../getting-started/store-details.md#country-options) werden beim Checkout verwendet, um zu begrenzen, woher ein Kunde kommen kann. |
| **[!UICONTROL Store]** |  |
| Domäne | Bei mehreren Stores kann jeder Store über dieselbe Domäne, eine Subdomäne oder unterschiedliche Domänen verfügen. Weitere Informationen finden Sie unter [Hinzufügen von Stores](../stores-purchase/stores.md#add-stores). |
| Stammkategorie | Jeder Store kann einen separaten Satz von Produkten und Hauptmenü haben, der auf einer &quot;Stamm&quot;-Kategorie und Unterkategorien basiert. Jeder Katalog verfügt über eine [Stammkategorie](../catalog/category-root.md) , die auf Store-Ebene zugewiesen wird. |
| **[!UICONTROL Store View]** |  |
| Unterkategorien | Die [Unterkategorien](../catalog/category-create.md#category-structure), aus denen das Hauptmenü besteht (unter der Wurzel), werden auf der Ebene der Store-Ansicht zugewiesen. |
| Gebietsschema | Jeder Store-Ansicht kann ein anderes [Gebietsschema](../getting-started/store-details.md#locale-options) zugewiesen werden. Die Anzeigewährung, Maßeinheiten und die Admin-Oberfläche sind für das Gebietsschema spezifisch. |
| Sprachen | Um mehrere Sprachen zu unterstützen, müssen alle Inhalte, einschließlich Produktbeschreibungen, für jede Store-Ansicht [übersetzt](../stores-purchase/store-localize.md#localize-products) sein. |
| Anzeigenwährung | Für jede Store-Ansicht kann eine andere [Anzeigewährung](../stores-purchase/currency-configuration.md) verwendet werden, obwohl die Transaktionen auf Website-Ebene mit der Basiswährung verarbeitet werden. |

{style="table-layout:auto"}
