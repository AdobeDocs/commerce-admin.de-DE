---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL General] &gt; [!UICONTROL Content Management] des Commerce Admin-Bereichs.
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 5929a2ff26dadda40ecfa9e435a73343caef3cde
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![WYSIWYG-Optionen](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://experienceleague.adobe.com/de/docs/commerce-admin/content-design/wysiwyg/editor) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | Shop-Ansicht | Legt fest, ob der Editor für den Store aktiviert ist. Optionen: Standardmäßig aktiviert/standardmäßig deaktiviert/vollständig deaktiviert |
| [!UICONTROL WYSIWYG Editor] | Website | Bestimmt die Version des TinyMCE-Editors, der für den WYSIWYG-Editor verwendet wird. Optionen: <br/>**`TinyMCE 5`**- (Standard) Verwendet TinyMCE Version 5 als standardmäßigen WYSIWYG-Editor.<br><br>_ **&#x200B; Hinweis:**&#x200B;_Ein Update der TinyMCE 5.10-Bibliothek in Adobe Commerce und Magento Open Source 2.4.5 behebt eine Sicherheitslücke, die die beliebige Ausführung von JavaScript beim Aktualisieren eines Bildes oder Links mit einigen URL-Typen ermöglicht hat. TinyMCE 3 ist seit Version 2.4.0 veraltet und wurde in Version 2.4.3 entfernt. TinyMCE 4 wurde in Version 2.4.4 entfernt. |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | Global | Bestimmt, ob [statische URLs](../../content-design/catalog-urls-dynamic-media.md) für Medieninhalte verwendet werden, auf die vom WYSIWYG-Editor verwiesen wird. Die Einstellung gilt für alle Stellen, an denen der WYSIWYG-Editor verfügbar ist, einschließlich Produkten, Kategorien, Seiten und Blöcken. Optionen: <br/>**`Yes`**- Verwendet statische URLs für Medieninhalte, die mit dem WYSIWYG-Editor eingefügt werden. Statische URLs sind absolut und werden ungültig, wenn sich die [Basis-URL](../../stores-purchase/store-urls.md) des Stores ändert.<br/>**`No`** (Standard) - Verwendet dynamische URLs für Medieninhalte, die mit dem WYSIWYG-Editor eingefügt werden, basierend auf der `{{media url="..."}}`. Dynamische URLs sind relativ und funktionieren nicht beschädigt, wenn sich die Basis-URL des Stores ändert. |

{style="table-layout:auto"}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![CMS-Seitenhierarchie](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://experienceleague.adobe.com/de/docs/commerce-admin/content-design/elements/pages/page-hierarchy) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | Global | Aktiviert die Verwendung der Seitenhierarchie für Ihre Inhaltsseiten. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | Global | Ermöglicht die Verknüpfung von Metadaten mit Seiten in der Hierarchie. Optionen: `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | Global | Bestimmt den Standardstil des Menüs. Optionen: `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Content Tools]

![Erweiterte Inhalts-Tools](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://experienceleague.adobe.com/de/docs/commerce-admin/page-builder/walkthrough/3-catalog-content) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | Global | Legt fest, ob die [!DNL Page Builder] erweiterten Inhalts-Tools verfügbar sind. Optionen: <br/>**`Yes`**- Der Arbeitsbereich [!DNL Page Builder] wird im Abschnitt Inhalt von Seiten, Blöcken, Produkten und Kategorien angezeigt.<br/>**`No`** - Die standardmäßigen CMS-Bearbeitungswerkzeuge werden im _[!UICONTROL Content]_&#x200B;Abschnitt der Seiten, Blöcke, Produkte und Kategorien angezeigt. |
| [!UICONTROL Enable Page Builder Content Preview] | Global | Legt fest, ob die [!DNL Page Builder] Inhaltsvorschauen für Produkte und Kategorien aktiviert sind. Optionen: `Yes` / `No` <br/>**_Hinweis:_** Standardmäßig ist dies auf `Yes` festgelegt, aber das Deaktivieren der Vorschau kann Leistungsprobleme verhindern, die sich aus dem Laden von Vorschauen innerhalb eines Produkt- oder Kategorieformulars ergeben. |
| [!UICONTROL Google Maps API Key] | Global | Der [!DNL Google Maps]-API-Schlüssel aus Ihrem Google-Konto. |
| [!UICONTROL Test Key] |  | Validiert den [!DNL Google Maps] API-Schlüssel. |
| [!UICONTROL Google Maps Style] | Global | Fügen Sie den JSON-Code im [!DNL Google Maps] hier ein, um das Erscheinungsbild des Inhaltstyps „Zuordnung“ zu ändern. |
| [!UICONTROL Default Column Grid Size] | Global | Bestimmt die Standardanzahl der Spalten im [!DNL Page Builder]. |
| [!UICONTROL Maximum Column Grid Size] | Global | Bestimmt die maximale Anzahl von Spalten im [!DNL Page Builder]. |

{style="table-layout:auto"}

>[!TIP]
>
>Mit Page Builder können Sie mühelos inhaltsreiche Seiten mit benutzerdefinierten Layouts erstellen, die Ihre visuelle storytelling verbessern und die Kundeninteraktion und -loyalität fördern. Diese Funktionen verbessern die Qualität und reduzieren den Zeit- und Kostenaufwand für die Erstellung benutzerdefinierter Seiten. Weitere Informationen zu diesen Funktionen und deren Verwendung zum Erstellen ansprechender Inhalte für Ihren Adobe Commerce- oder Magento Open Source-Store finden Sie im [_Page Builder-Benutzerhandbuch_](../../page-builder/guide-overview.md).
