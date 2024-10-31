---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap] des Commerce-Administrators.
exl-id: 319c34e9-bd5f-46f8-810f-bc4d5228f9c9
feature: Configuration, Site Navigation
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 2%

---

# [!UICONTROL Catalog] > [!UICONTROL XML Sitemap]

{{config}}

## [!UICONTROL Categories Options]

![Optionen für Kategorien](./assets/xml-sitemap-categories-options.png)<!-- zoom -->

<!-- [Categories Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Frequency] | Store-Ansicht | Bestimmt, wie oft Sitemap-Kategorien aktualisiert werden. Optionen: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Store-Ansicht | Ein Wert zwischen `0.0` und `1.0` , der die Priorität von Kategorie-Sitemap-Aktualisierungen in Bezug auf anderen Inhalt bestimmt. Null (`0.0`) hat die niedrigste Priorität. |

{style="table-layout:auto"}

## [!UICONTROL Products Options]

![Produktoptionen](./assets/xml-sitemap-products-options.png)<!-- zoom -->

<!-- [Products Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Frequency] | Store-Ansicht | Bestimmt, wie oft Sitemap-Produkte aktualisiert werden. Optionen: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Store-Ansicht | Ein Wert zwischen `0.0` und `1.0` , der die Priorität von Produkt-Sitemap-Aktualisierungen im Verhältnis zu anderen Inhalten bestimmt. Null (`0.0`) hat die niedrigste Priorität. |
| [!UICONTROL Add Images into Sitemap] | Store-Ansicht | Bestimmt, in welchem Umfang Bilder in die Sitemap aufgenommen werden. Optionen: `None` / `Base Only` / `All` |

{style="table-layout:auto"}

## [!UICONTROL CMS Pages Options]

![CMS-Seitenoptionen](./assets/xml-sitemap-cms-pages-options.png)<!-- zoom -->

<!-- [CMS Pages Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Frequency] | Store-Ansicht | Bestimmt, wie oft Sitemap-CMS-Seiten aktualisiert werden. Optionen: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Store-Ansicht | Ein Wert zwischen `0.0` und `1.0` , der die Priorität von CMS-Seitensitemap-Aktualisierungen in Bezug auf andere Inhalte festlegt. Null (`0.0`) hat die niedrigste Priorität. |

{style="table-layout:auto"}

## [!UICONTROL Store Url Options]

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Frequency] | Store-Ansicht | Bestimmt, wie oft URLs gespeichert werden, die aktualisiert werden. Optionen: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Store-Ansicht | Ein Wert zwischen `0.0` und `1.0` , der die Priorität von Store-URL-Aktualisierungen im Vergleich zu anderen Inhalten bestimmt. Null (`0.0`) hat die niedrigste Priorität. |

{style="table-layout:auto"}

## [!UICONTROL Generation Settings]

![Generierungseinstellungen](./assets/xml-sitemap-generation-settings.png)<!-- zoom -->

<!-- [Generation Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Bestimmt, ob eine XML-Sitemap für den Store verfügbar ist. Optionen: `Yes` / `No` |
| [!UICONTROL Start Time] | Store-Ansicht | Gibt die Stunde, Minute und Sekunde des Tages an, in der die Sitemap aktualisiert wird. |
| [!UICONTROL Frequency] | Store-Ansicht | Bestimmt, wie oft die Sitemap aktualisiert wird. Optionen: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Store-Ansicht | Die E-Mail-Adresse der Person, die während des Sitemap-Aktualisierungsprozesses benachrichtigt wird, wenn ein Fehler auftritt. Trennen Sie bei mehreren Adressen jede durch ein Komma. |
| [!UICONTROL Error Email Sender] | Webseite | Identifiziert den Store-Kontakt, der als Absender der Fehlerbenachrichtigung angezeigt wird. Optionen: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Error Email Template] | Webseite | Identifiziert die für die Fehlerbenachrichtigung verwendete E-Mail-Vorlage. Standardvorlage: `Sitemap generate Warnings` |

{style="table-layout:auto"}

## [!UICONTROL Sitemap File Limits]

![Dateibeschränkungen der Sitemap](./assets/xml-sitemap-sitemap-file-limits.png)<!-- zoom -->

<!-- [Sitemap File Limits](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Maximum No of URLs Per File] | Store-Ansicht | Bestimmt die maximale Anzahl von URLs, die in eine Sitemap aufgenommen werden können. |
| [!UICONTROL Maximum File Size] | Store-Ansicht | Bestimmt die maximale Größe der generierten Sitemap in Byte. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Submission Settings]

![Suchmaschinen-Sendeeinstellungen](./assets/xml-sitemap-search-engine-submission-settings.png)<!-- zoom -->

<!-- [Search Engine Submission Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Submission to Robots.txt] | Store-Ansicht | Ermöglicht die Übermittlung von Anweisungen für die Datei robots.txt . Optionen: `Yes` / `No` |

{style="table-layout:auto"}
