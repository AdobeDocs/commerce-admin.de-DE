---
title: Site-, Store- und Ansichtsbereich
description: Erfahren Sie mehr über die Hierarchie von Websites, Geschäften und Store-Ansichten, mit denen Sie Einkaufserlebnisse für Ihre Kunden bereitstellen können.
exl-id: 80fc1b73-c869-4f1c-b1a1-d61823b91d83
feature: System, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Site-, Store- und Ansichtsbereich

Jede Adobe Commerce- und Magento Open Source-Installation verfügt über eine [Hierarchie](../stores-purchase/stores.md) von Websites, Stores und Store-Ansichten. Der Begriff _scope_ bestimmt, wo in der Hierarchie eine Datenbankentität (z. B. ein Produkt, ein Attribut oder eine Kategorie), ein Inhaltselement oder eine Konfigurationseinstellung gilt. Websites, Stores und Store-Ansichten verfügen über eine 1:n-Beziehung zwischen über- und untergeordneten Seiten. Eine einzelne Installation kann über mehrere Websites verfügen und jede Website kann über mehrere Stores und Store-Ansichten verfügen.

>[!NOTE]
>
>Weitere Informationen finden Sie unter [Mehrere Websites oder Stores](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) in der Entwicklerdokumentation von [!DNL Commerce].

## Websites

Installationen beginnen mit einer einzelnen [Website](../stores-purchase/stores.md#add-websites), die standardmäßig als _Hauptwebsite_ bezeichnet wird. Sie können auch mehrere Websites für eine Installation einrichten, von denen jede über eine eigene IP-Adresse und Domäne verfügt.

## Stores

Eine einzelne Website kann über mehrere [Stores](../stores-purchase/stores.md#add-stores) verfügen, von denen jede über ein eigenes Hauptmenü verfügt. Die Geschäfte teilen sich den Produktkatalog, können jedoch eine andere Auswahl an Produkten und Designs haben. Alle Geschäfte auf derselben Website teilen sich den Admin und Checkout.

## Store-Ansichten

Jeder Store, der für Kunden verfügbar ist, wird entsprechend einer bestimmten _[Ansicht](../stores-purchase/store-views.md)_ dargestellt. Zunächst verfügt ein Store über eine einzige Standardansicht. Zusätzliche Store-Ansichten können hinzugefügt werden, um verschiedene Sprachen oder für andere Zwecke zu unterstützen. Kunden können die Sprachauswahl in der Kopfzeile verwenden, um die Store-Ansicht zu ändern.

Beachten Sie beim Arbeiten mit Websites, Geschäften und Store-Ansichten Folgendes:

- Commerce-Instanzen verfügen über ein kaskadierendes Modell: global → website → store → store view.
- Jede Website verfügt über mindestens eine standardmäßige Store- und Store-Ansicht.
- Jede Store-Ansicht kann über eine andere Basis-URL verfügen.
- Die Hauptfunktion einer Website ist die Konfiguration von Funktionen auf oberster Ebene.
- Die primäre Funktion eines Stores ist die Konfiguration der Stammkategorie.
- Die Hauptfunktion einer Store-Ansicht sind Übersetzungsinformationen und die Konfiguration von Währungssymbolen.

## Perimeter

Wenn Ihre Adobe Commerce- oder Magento Open Source-Installation eine Hierarchie von Websites, Stores oder Ansichten aufweist, können Sie den Kontext oder den _Perimeter_ einer Konfigurationseinstellung festlegen. Dem Kontext vieler Datenbankentitäten kann auch ein bestimmter Bereich zugewiesen werden, um zu bestimmen, wie er in der Store-Hierarchie verwendet wird. Weitere Informationen finden Sie unter [Produktumfang](../catalog/introduction.md#product-scope) und [Preisbereich](../catalog/catalog-price-scope.md).

Einige Konfigurationseinstellungen wie die Postleitzahl haben einen globalen Gültigkeitsbereich, da im gesamten System derselbe Wert verwendet wird. Der Gültigkeitsbereich [Website](../stores-purchase/stores.md#add-websites) gilt für alle Geschäfte unterhalb dieser Ebene in der Hierarchie, einschließlich aller Geschäfte und deren Ansichten. Jedes Element mit dem Umfang [store view](../stores-purchase/store-views.md) kann für jede Store-Ansicht unterschiedlich festgelegt werden, was normalerweise zur Unterstützung mehrerer Sprachen verwendet wird. Informationen zum Überschreiben der Standardwerte von Konfigurationseinstellungen finden Sie unter [Festlegen des Umfangs](../configuration-reference/scope-change.md#set-the-scope).

Sofern der Store nicht im [Einzelspeichermodus](#single-store-mode) ausgeführt wird, wird der Umfang jeder Konfigurationseinstellung in geringem Text unter der Feldbeschriftung angezeigt. Wenn Ihre Installation mehrere Websites, Stores oder Ansichten umfasst, wählen Sie die [Store-Ansicht](../stores-purchase/store-views.md), in der die Einstellungen gelten, bevor Sie Änderungen vornehmen.

![Hierarchie der Websites, Stores und Store-Ansichten](./assets/scope-multisite.svg){width="550"}

| Anwendungsbereich | Beschreibung |
|--- |--- |
| [!UICONTROL Global] | Systemweite Einstellungen und Ressourcen, die während der Installation verfügbar sind. |
| [!UICONTROL Website] | Einstellungen und Ressourcen, die auf die aktuelle Website beschränkt sind. Jede Website verfügt über einen Standardspeicher. |
| [!UICONTROL Store] | Einstellungen und Ressourcen, die auf den aktuellen Store beschränkt sind. Jeder Store verfügt über eine standardmäßige Stammkategorie (Hauptmenü) und eine standardmäßige Store-Ansicht. |
| [!UICONTROL Store View] | Einstellung und Ressourcen, die auf die aktuelle Store-Ansicht beschränkt sind. |

{style="table-layout:auto"}

## Einzelspeichermodus

Wenn Ihre Commerce-Installation nur über eine einzige Store- und Store-Ansicht verfügt, können Sie die Anzeige vereinfachen, indem Sie alle Store-Ansichtsoptionen und Scope-Indikatoren deaktivieren. Der Einzelspeichermodus wird überschrieben, wenn Sie [später weitere Store-Ansichten hinzufügen](../stores-purchase/store-views.md).

![Umfang - Einzelansicht](./assets/scope-single-view.svg){width="550"}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Scrollen Sie unter &quot;**[!UICONTROL General]**&quot; nach unten zum unteren Rand der Seite und erweitern Sie den Abschnitt &quot;**[!UICONTROL Single-Store Mode]**&quot;.

1. Setzen Sie **[!UICONTROL Enable Single-Store Mode]** auf `Yes`.

   ![Allgemeine Konfiguration - Einzelspeichermodus aktivieren](./assets/general-single-store-mode.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, gehen Sie wie folgt vor:

   - Klicken Sie oben auf der Seite in der Systemmeldung auf den Link **[!UICONTROL Cache Management]** .

     ![Systemmeldung - Cache-Verwaltung](../catalog/assets/msg-cache-management.png){width="600" zoomable="yes"}

   - Aktivieren Sie das Kontrollkästchen **[!UICONTROL Page Cache]** .

   - Wenn **[!UICONTROL Actions]** auf `Refresh` gesetzt ist, klicken Sie auf **[!UICONTROL Submit]**
