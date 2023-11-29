---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL General] &gt; [!UICONTROL Content Management] Seite des Commerce-Administrators.
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
source-git-commit: 5eef49c10680a47574afe3d3ecfa430dca7ad9ff
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![WYSIWYG-Optionen](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://docs.magento.com/user-guide/cms/editor.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | Store-Ansicht | Bestimmt, ob der Editor für den Store aktiviert ist. Optionen: standardmäßig aktiviert/standardmäßig deaktiviert/vollständig deaktiviert |
| [!UICONTROL WYSIWYG Editor] | Webseite | Bestimmt die Version des TinyMCE-Editors, der für den WYSIWYG-Editor verwendet wird. Optionen: <br/>**`TinyMCE 5`**- (Standard) Verwendet die TinyMCE-Version 5 als standardmäßigen WYSIWYG-Editor.<br><br>_** Hinweis:**_Durch ein Update der TinyMCE 5.10-Bibliothek in Adobe Commerce und Magento Open Source 2.4.5 wurde eine Sicherheitslücke behoben, die eine beliebige JavaScript-Ausführung ermöglichte, wenn ein Bild oder ein Link mit einigen URL-Typen aktualisiert wurde. TinyMCE 3 wurde in Version 2.4.0 eingestellt und in Version 2.4.3 entfernt. TinyMCE 4 wurde in Version 2.4.4 entfernt. |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | Global | Bestimmt, ob [statische URLs](../../content-design/catalog-urls-dynamic-media.md) werden für Medieninhalte verwendet, auf die im WYSIWYG-Editor verwiesen wird. Die Einstellung gilt für alle Stellen, an denen der WYSIWYG-Editor verfügbar ist, einschließlich Produkten, Kategorien, Seiten und Blöcken. Optionen: <br/>**`Yes`**- Verwendet statische URLs für Medieninhalte, die mit dem WYSIWYG-Editor eingefügt werden. Statische URLs sind absolut und umbrechen, wenn die [Basis-URL](../../stores-purchase/store-urls.md) der Store-Änderungen.<br/>**`No`** (Standard) - Verwendet dynamische URLs für Medieninhalte, die mit dem WYSIWYG-Editor basierend auf dem  `{{media url="..."}}` Richtlinie. Dynamische URLs sind relativ und beschädigen nicht, wenn sich die Basis-URL des Stores ändert. |

{style="table-layout:auto"}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![CMS-Seitenhierarchie](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://docs.magento.com/user-guide/cms/page-hierarchy.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | Global | Aktiviert die Verwendung der Seitenhierarchie für Ihre Inhaltsseiten. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | Global | Ermöglicht die Zuordnung von Metadaten zu Seiten in der Hierarchie. Optionen: `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | Global | Legt den Standardmenüstil fest. Optionen: `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Content Tools]

![Erweiterte Inhaltswerkzeuge](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://docs.magento.com/user-guide/cms/page-builder-workspace.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | Global | Bestimmt, ob die [!DNL Page Builder] erweiterte Inhaltstools verfügbar sind. Optionen: <br/>**`Yes`**- die [!DNL Page Builder] Der Arbeitsbereich wird im Abschnitt Inhalt von Seiten, Bausteinen, Produkten und Kategorien angezeigt.<br/>**`No`** - Die standardmäßigen CMS-Bearbeitungswerkzeuge werden im _[!UICONTROL Content]_-Abschnitt von Seiten, Bausteinen, Produkten und Kategorien. |
| [!UICONTROL Enable Page Builder Content Preview] | Global | Bestimmt, ob die [!DNL Page Builder] Inhaltsvorschauen sind für Produkte und Kategorien aktiviert. Optionen: `Yes` / `No` <br/>**_Hinweis:_**Dies ist auf `Yes` Standardmäßig verhindert das Deaktivieren der Vorschau jedoch alle Leistungsprobleme, die durch das Laden der Vorschau in einem Produkt- oder Kategorieformular verursacht werden. |
| [!UICONTROL Google Maps API Key] | Global | Die [!DNL Google Maps] API-Schlüssel aus Ihrem Google-Konto. |
| [!UICONTROL Test Key] |  | Validiert die [!DNL Google Maps] API-Schlüssel. |
| [!UICONTROL Google Maps Style] | Global | Fügen Sie die [!DNL Google Maps] Stil-JSON-Code hier , um das Erscheinungsbild des Inhaltstyps &quot;Map&quot;zu ändern. |
| [!UICONTROL Default Column Grid Size] | Global | Legt die Standardanzahl von Spalten im [!DNL Page Builder] Gitter. |
| [!UICONTROL Maximum Column Grid Size] | Global | Bestimmt die maximale Anzahl von Spalten im [!DNL Page Builder] Gitter. |

{style="table-layout:auto"}

>[!TIP]
>
>Mit Page Builder können Sie inhaltsreiche Seiten mit benutzerdefinierten Layouts erstellen, die Ihr visuelles Geschichtenerzählen verbessern und die Kundeninteraktion und -loyalität fördern. Diese Funktionen sollen die Qualität verbessern und die Zeit und Kosten für die Erstellung benutzerdefinierter Seiten reduzieren. Weitere Informationen zu diesen Funktionen und wie Sie sie verwenden können, um ansprechende Inhalte für Ihren Adobe Commerce- oder Magento Open Source-Store zu erstellen, finden Sie im Abschnitt [_Benutzerhandbuch für Page Builder_](../../page-builder/guide-overview.md).
