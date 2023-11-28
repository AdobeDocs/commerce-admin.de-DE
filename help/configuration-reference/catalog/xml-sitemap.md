---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap] Seite des Commerce-Administrators.
exl-id: 319c34e9-bd5f-46f8-810f-bc4d5228f9c9
feature: Configuration, Site Navigation
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---

# [!UICONTROL Catalog] > [!UICONTROL XML Sitemap]

{{config}}

## [!UICONTROL Categories Options]

![Kategorieoptionen](./assets/xml-sitemap-categories-options.png)<!-- zoom -->

<!-- [Categories Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Frequency] | Store-Ansicht | Bestimmt, wie oft Sitemap-Kategorien aktualisiert werden. Optionen: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Store-Ansicht | Ein Wert zwischen `0.0` und `1.0` , das die Priorität von Kategorie-Sitemap-Aktualisierungen im Verhältnis zu anderen Inhalten bestimmt. Null (`0.0`) hat die niedrigste Priorität. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Products Options]

![Produktoptionen](./assets/xml-sitemap-products-options.png)<!-- zoom -->

<!-- [Products Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Frequency] | Store-Ansicht | Bestimmt, wie oft Sitemap-Produkte aktualisiert werden. Optionen: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Store-Ansicht | Ein Wert zwischen `0.0` und `1.0` , das die Priorität von Produkt-Sitemap-Aktualisierungen im Verhältnis zu anderen Inhalten bestimmt. Null (`0.0`) hat die niedrigste Priorität. |
| [!UICONTROL Add Images into Sitemap] | Store-Ansicht | Bestimmt, in welchem Umfang Bilder in die Sitemap aufgenommen werden. Optionen: `None` / `Base Only` / `All` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL CMS Pages Options]

![CMS-Seitenoptionen](./assets/xml-sitemap-cms-pages-options.png)<!-- zoom -->

<!-- [CMS Pages Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Frequency] | Store-Ansicht | Bestimmt, wie oft CMS-Seiten von Sitemap aktualisiert werden. Optionen: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Store-Ansicht | Ein Wert zwischen `0.0` und `1.0` , das die Priorität von CMS-Seiten-Sitemap-Aktualisierungen im Verhältnis zu anderen Inhalten festlegt. Null (`0.0`) hat die niedrigste Priorität. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Store Url Options]

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Frequency] | Store-Ansicht | Bestimmt, wie oft URLs gespeichert werden, die aktualisiert werden. Optionen: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Store-Ansicht | Ein Wert zwischen `0.0` und `1.0` bestimmt die Priorität von Store-URL-Aktualisierungen im Verhältnis zu anderen Inhalten. Null (`0.0`) hat die niedrigste Priorität. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Generation Settings]

![Generierungseinstellungen](./assets/xml-sitemap-generation-settings.png)<!-- zoom -->

<!-- [Generation Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Bestimmt, ob eine XML-Sitemap für den Store verfügbar ist. Optionen: `Yes` / `No` |
| [!UICONTROL Start Time] | Store-Ansicht | Gibt die Stunde, Minute und Sekunde des Tages an, in der die Sitemap aktualisiert wird. |
| [!UICONTROL Frequency] | Store-Ansicht | Bestimmt, wie oft die Sitemap aktualisiert wird. Optionen: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Store-Ansicht | Die E-Mail-Adresse der Person, die während des Sitemap-Aktualisierungsprozesses benachrichtigt wird, wenn ein Fehler auftritt. Trennen Sie bei mehreren Adressen jede durch ein Komma. |
| [!UICONTROL Error Email Sender] | Webseite | Identifiziert den Store-Kontakt, der als Absender der Fehlerbenachrichtigung angezeigt wird. Optionen: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Error Email Template] | Webseite | Identifiziert die für die Fehlerbenachrichtigung verwendete E-Mail-Vorlage. Standardvorlage: `Sitemap generate Warnings` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Sitemap File Limits]

![Dateibeschränkungen für Sitemap](./assets/xml-sitemap-sitemap-file-limits.png)<!-- zoom -->

<!-- [Sitemap File Limits](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Maximum No of URLs Per File] | Store-Ansicht | Bestimmt die maximale Anzahl von URLs, die in eine Sitemap aufgenommen werden können. |
| [!UICONTROL Maximum File Size] | Store-Ansicht | Bestimmt die maximale Größe der generierten Sitemap in Byte. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Search Engine Submission Settings]

![Suchmaschinen-Sendeeinstellungen](./assets/xml-sitemap-search-engine-submission-settings.png)<!-- zoom -->

<!-- [Search Engine Submission Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Submission to Robots.txt] | Store-Ansicht | Ermöglicht die Übermittlung von Anweisungen für die Datei robots.txt . Optionen: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
