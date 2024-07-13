---
title: '[!DNL Page Builder] Benutzerhandbuch'
description: Umfassende Informationen zu [!DNL Page Builder] für Adobe Commerce- und Magento Open Source-Administratoren.
seo-title: Adobe Commerce [!DNL Page Builder] User Guide
seo-description: Describes how to use the [!DNL Page Builder] module in Adobe Commerce or Magento Open Source.
exl-id: 983ef3a8-b803-40ff-a9f5-07eb895df31c
source-git-commit: fa4030d391fc9a3b21cf8fb6f681df9e9165157d
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# [!DNL Page Builder] Benutzerhandbuch

Dieses Handbuch richtet sich an Administratoren von Adobe Commerce und Magento Open Source. Es enthält detaillierte Informationen zu [!DNL Page Builder]-Funktionen, einschließlich einer dreiteiligen exemplarischen Vorgehensweise zum Erstellen grundlegender Inhaltskomponenten. Es wird von einem grundlegenden Verständnis der Core-Konfiguration und -Funktionalität von [!DNL Commerce] ausgegangen.

[!DNL Page Builder] hat zwei Bereiche für Store-Administratoren:

- Admin: Verwenden Sie diesen Bereich, um auf die Konfigurationsoberfläche zuzugreifen und mit den Seitenaufbau-Tools zu arbeiten.
- Befehlszeilenschnittstelle: Verwenden Sie dieses Tool, um Installations- und Backend-Konfigurationsaufgaben auszuführen.

Dieses Handbuch behandelt:

| Betreff | Beschreibung |
| ------- | ----------- |
| [Einführung](introduction.md) | Was ist [!DNL Page Builder]? Und wie verbessert sie die Inhaltserstellung für Adobe Commerce- und Magento Open Source-Sites? |
| [Versionshinweise](release-notes.md) | Überprüfen Sie die in jeder Version des [!DNL Page Builder]-Moduls bereitgestellten Aktualisierungen. |
| [Setup](setup.md) | Um die Standardeinstellungen zu aktualisieren, können Sie das standardmäßige Seitenlayout ändern und erweiterte Funktionen für [!DNL Page Builder] aktivieren. Sie können auch [!DNL Google Maps] integrieren, um Ortsinhalte in Ihre Seiten zu integrieren. |
| [Workspace](workspace.md) | Überprüfen Sie die Komponenten des Arbeitsbereichs [!DNL Page Builder] und wie Sie damit ansprechende Inhalte für Ihre Geschäfte erstellen können. |
| Exemplarische Vorgehensweise | Wenn Sie gerade erst mit [!DNL Page Builder] beginnen, können Sie sich schnell vertraut machen, indem Sie die exemplarischen Vorgehensweisen abschließen:<br>[1 - Beispielseite](1-simple-page.md)<br>[2 - wiederverwendbarer Inhaltsbaustein](2-blocks.md)<br>[3 - Katalogseite für Produktlisten](3-catalog-content.md) |
| [Workspace](workspace.md) | Lernen Sie die im Arbeitsbereich &quot;[!DNL Page Builder]&quot;verfügbaren Tools kennen, wenn Sie einfache Seiten, Produkt- und Katalogseiten, Bausteine und dynamische Bausteine erstellen. |
| Layout | Durchsuchen Sie den Abschnitt _Layout_ des Bedienfelds [!DNL Page Builder] und erfahren Sie, wie Sie mit diesen Tools Layoutkomponenten zur [!DNL Page Builder]-Bühne hinzufügen: <br>[Zeilen](row.md)<br>[Spalten](column.md)<br>[Registerkarten](tabs.md) |
| Elemente | Erkunden Sie den Abschnitt _Elemente_ des Bedienfelds [!DNL Page Builder] und wie Sie mit diesen Tools grundlegende Elemente zu jedem Layout-Container auf der [!DNL Page Builder]-Bühne hinzufügen können: <br>[Text](text.md)<br>[Überschriften](heading.md)<br>[Schaltflächen](buttons.md)<br>[Divider](divider.md)<br>[HTML-Code](html-code.md) |
| Medien | Durchsuchen Sie den Abschnitt _Medien_ des Bedienfelds [!DNL Page Builder] und erfahren Sie, wie Sie mit diesen Tools Medienelemente zu einem Layout-Container auf der [!DNL Page Builder]-Bühne hinzufügen: <br>[Bilder](image.md)<br>[Video](video.md)<br>[Banner](banner.md)<br>[Regler](slider.md)<br>[[!DNL Google Maps]](map.md) |
| Inhalt hinzufügen | Erkunden Sie den Abschnitt _Inhalt hinzufügen_ des Bedienfelds [!DNL Page Builder] und wie Sie Inhaltskomponenten zur Phase [!DNL Page Builder] hinzufügen: <br>[Baustein](block.md)<br>[Dynamischer Baustein](dynamic-block.md)<br>[Produkte](products.md)<br>[Produkt-Recommendations](recommendations.md) (nur Adobe Commerce) |
| [Vorlagen](templates.md) | Speichern Sie Ihren vorhandenen [!DNL Page Builder] -Inhalt als Vorlage und wenden Sie diese Vorlage dann auf einen anderen Bereich an, um schnell und konsistent Inhalte zu erstellen. |

{style="table-layout:auto"}

Die Kernfunktionen von Adobe Commerce und Magento Open Source werden nicht abgedeckt.

## Zusätzliche Dokumentation

{{docs-links}}

## [!DNL Page Builder] Entwicklerinformationen

[!DNL Page Builder] wird mit Adobe Commerce 2.4.x und Magento Open Source 2.4.3 und höher installiert, wobei alle Funktionen standardmäßig aktiviert sind. Informationen zu den in Modulversionen enthaltenen Änderungen finden Sie in den [[!DNL Page Builder] Versionshinweisen](release-notes.md). Das [[!DNL Page Builder] Entwicklerhandbuch](https://developer.adobe.com/commerce/frontend-core/page-builder/) enthält Details zur Modularchitektur und -anpassung.

## Fehlerbehebung bei Ressourcen

Hilfe zur Fehlerbehebung bei [!DNL Page Builder] -Problemen finden Sie in den folgenden Artikeln der Support Knowledge Base:[!DNL Commerce]

- [Leere Seite, wenn DotDigital [!DNL Page Builder] Formular gespeichert wurde](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/magento-2.4.1-empty-page-when-dotdigital-page-builder-form-saved.html)
- [[!DNL Page Builder] lädt keine Mediensalerie](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-12/mdva-32133-magento-patch-page-builder-doesn-t-load-media-gallery.html)
- [[!DNL Page Builder] Vorschau bricht den Produktpreis je nach Site ab](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-16/mdva-33453-page-builder-preview-breaks-product-price-differs-across-sites.html)
- [Kann die Seite &quot;Begriffe&quot;nicht speichern](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-19/mdva-33614-magento-patch-can-t-save-terms-page.html)
