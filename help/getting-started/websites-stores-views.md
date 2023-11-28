---
title: Site-, Store- und Ansichtsbereich
description: Erfahren Sie mehr über die Hierarchie von Websites, Geschäften und Store-Ansichten, mit denen Sie Einkaufserlebnisse für Ihre Kunden bereitstellen können.
exl-id: 80fc1b73-c869-4f1c-b1a1-d61823b91d83
feature: System, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Site-, Store- und Ansichtsbereich

Jede Installation von Adobe Commerce und Magento Open Source verfügt über eine [hierarchy](../stores-purchase/stores.md) von Websites, Geschäften und Store-Ansichten. Der Begriff _Umfang_ bestimmt, wo in der Hierarchie eine Datenbankentität (z. B. ein Produkt, ein Attribut oder eine Kategorie) für ein Inhaltselement oder eine Konfigurationseinstellung gilt. Websites, Stores und Store-Ansichten verfügen über eine 1:n-Beziehung zwischen über- und untergeordneten Seiten. Eine einzelne Installation kann über mehrere Websites verfügen und jede Website kann über mehrere Stores und Store-Ansichten verfügen.

>[!NOTE]
>
>Weitere Informationen finden Sie unter [Mehrere Websites oder Stores](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) im [!DNL Commerce] Entwicklerdokumentation.

## Websites

Installationen beginnen mit einer einzigen [website](../stores-purchase/stores.md#add-websites), die _Hauptwebsite_ Standardmäßig. Sie können auch mehrere Websites für eine Installation einrichten, von denen jede über eine eigene IP-Adresse und Domäne verfügt.

## Stores

Eine einzelne Website kann mehrere [Stores](../stores-purchase/stores.md#add-stores), jeweils mit einem eigenen Hauptmenü. Die Geschäfte teilen sich den Produktkatalog, können jedoch eine andere Auswahl an Produkten und Designs haben. Alle Geschäfte auf derselben Website teilen sich den Admin und Checkout.

## Store-Ansichten

Jeder für Kunden verfügbare Store wird entsprechend einem bestimmten _[Ansicht](../stores-purchase/store-views.md)_. Zunächst verfügt ein Store über eine einzige Standardansicht. Zusätzliche Store-Ansichten können hinzugefügt werden, um verschiedene Sprachen oder für andere Zwecke zu unterstützen. Kunden können die Sprachauswahl in der Kopfzeile verwenden, um die Store-Ansicht zu ändern.

Beachten Sie beim Arbeiten mit Websites, Geschäften und Store-Ansichten Folgendes:

- Commerce-Instanzen verfügen über ein kaskadierendes Modell: global → website → store → store view.
- Jede Website verfügt über mindestens eine standardmäßige Store- und Store-Ansicht.
- Jede Store-Ansicht kann über eine andere Basis-URL verfügen.
- Die Hauptfunktion einer Website ist die Konfiguration von Funktionen auf oberster Ebene.
- Die primäre Funktion eines Stores ist die Konfiguration der Stammkategorie.
- Die Hauptfunktion einer Store-Ansicht sind Übersetzungsinformationen und die Konfiguration von Währungssymbolen.

## Perimeter

Wenn Ihre Adobe Commerce- oder Magento Open Source-Installation eine Hierarchie von Websites, Geschäften oder Ansichten aufweist, können Sie den Kontext festlegen oder _Umfang_ einer Konfigurationseinstellung. Dem Kontext vieler Datenbankentitäten kann auch ein bestimmter Bereich zugewiesen werden, um zu bestimmen, wie er in der Store-Hierarchie verwendet wird. Weitere Informationen finden Sie unter [Produktbereich](../catalog/introduction.md#product-scope) und [Preissegment](../catalog/catalog-price-scope.md).

Einige Konfigurationseinstellungen wie die Postleitzahl haben einen globalen Gültigkeitsbereich, da im gesamten System derselbe Wert verwendet wird. Die [website](../stores-purchase/stores.md#add-websites) Der Perimeter gilt für alle Geschäfte, die unterhalb dieser Ebene in der Hierarchie liegen, einschließlich aller Geschäfte und deren Ansichten. Jedes Element mit dem Umfang von [Store-Ansicht](../stores-purchase/store-views.md) kann für jede Store-Ansicht anders festgelegt werden, was normalerweise zur Unterstützung mehrerer Sprachen verwendet wird. Informationen zum Außerkraftsetzen der Standardwerte der Konfigurationseinstellungen finden Sie unter [Festlegen des Umfangs](../configuration-reference/scope-change.md#set-the-scope).

Sofern der Store nicht ausgeführt wird [Einzelspeichermodus](#single-store-mode), wird der Umfang jeder Konfigurationseinstellung in geringem Text unter der Feldbeschriftung angezeigt. Wenn Ihre Installation mehrere Websites, Stores oder Ansichten umfasst, wählen Sie die [Store-Ansicht](../stores-purchase/store-views.md) wobei die Einstellungen vor der Durchführung von Änderungen gelten.

![Hierarchie von Websites, Stores und Store-Ansichten](./assets/scope-multisite.svg){width="550"}

| Anwendungsbereich | Beschreibung |
|--- |--- |
| [!UICONTROL Global] | Systemweite Einstellungen und Ressourcen, die während der Installation verfügbar sind. |
| [!UICONTROL Website] | Einstellungen und Ressourcen, die auf die aktuelle Website beschränkt sind. Jede Website verfügt über einen Standardspeicher. |
| [!UICONTROL Store] | Einstellungen und Ressourcen, die auf den aktuellen Store beschränkt sind. Jeder Store verfügt über eine standardmäßige Stammkategorie (Hauptmenü) und eine standardmäßige Store-Ansicht. |
| [!UICONTROL Store View] | Einstellung und Ressourcen, die auf die aktuelle Store-Ansicht beschränkt sind. |

{style="table-layout:auto"}

## Einzelspeichermodus

Wenn Ihre Commerce-Installation nur über eine einzige Store- und Store-Ansicht verfügt, können Sie die Anzeige vereinfachen, indem Sie alle Store-Ansichtsoptionen und Scope-Indikatoren deaktivieren. Der Einzelspeichermodus wird überschrieben, wenn Sie [Hinzufügen weiterer Store-Ansichten](../stores-purchase/store-views.md) später.

![Umfang - Einzelansicht](./assets/scope-single-view.svg){width="550"}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. under **[!UICONTROL General]**, scrollen Sie nach unten zum unteren Seitenrand und erweitern Sie die **[!UICONTROL Single-Store Mode]** Abschnitt.

1. Satz **[!UICONTROL Enable Single-Store Mode]** nach `Yes`.

   ![Allgemeine Konfiguration - Einzelspeichermodus aktivieren](./assets/general-single-store-mode.png){width="400"}

1. Klicken **[!UICONTROL Save Config]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, gehen Sie wie folgt vor:

   - Klicken Sie auf **[!UICONTROL Cache Management]** in der Systemmeldung am oberen Rand der Seite.

     ![Systemmeldung - Cache-Verwaltung](../catalog/assets/msg-cache-management.png){width="600" zoomable="yes"}

   - Wählen Sie die **[!UICONTROL Page Cache]** aktivieren.

   - Mit **[!UICONTROL Actions]** auf `Refresh`klicken **[!UICONTROL Submit]**
