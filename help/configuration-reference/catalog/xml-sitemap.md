---
title: '[!UICONTROL Catalog] > [!UICONTROL XML Sitemap]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Catalog] > [!UICONTROL XML Sitemap] des Commerce Admin.
exl-id: 319c34e9-bd5f-46f8-810f-bc4d5228f9c9
feature: Configuration, Site Navigation
TQID: https://experienceleague.adobe.com/1oTTRT977C3zcifhCRFBuXf7ny-6rqGSC--enriyj-Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 381
ht-degree: 2%

---

# [!UICONTROL Catalog] > [!UICONTROL XML Sitemap]

{{config}}

## [!UICONTROL Categories Options]

![Kategorieoptionen](./assets/xml-sitemap-categories-options.png)<!-- zoom -->

<!-- [Categories Options](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Frequency] | Shop-Ansicht | Legt fest, wie oft Sitemap-Kategorien aktualisiert werden. Optionen: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Shop-Ansicht | Ein Wert zwischen `0.0` und `1.0`, der die Priorität von Kategorie-Sitemap-Aktualisierungen im Verhältnis zu anderen Inhalten bestimmt. Null (`0.0`) hat die niedrigste Priorität. |

{style="table-layout:auto"}

## [!UICONTROL Products Options]

![Produktoptionen](./assets/xml-sitemap-products-options.png)<!-- zoom -->

<!-- [Products Options](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Frequency] | Shop-Ansicht | Legt fest, wie oft Sitemap-Produkte aktualisiert werden. Optionen: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Shop-Ansicht | Ein Wert zwischen `0.0` und `1.0`, der die Priorität von Produkt-Sitemap-Aktualisierungen im Verhältnis zu anderen Inhalten bestimmt. Null (`0.0`) hat die niedrigste Priorität. |
| [!UICONTROL Add Images into Sitemap] | Shop-Ansicht | Bestimmt das Ausmaß, in dem Bilder in die Sitemap aufgenommen werden. Optionen: `None` / `Base Only` / `All` |

{style="table-layout:auto"}

## [!UICONTROL CMS Pages Options]

![Optionen für CMS-Seiten](./assets/xml-sitemap-cms-pages-options.png)<!-- zoom -->

<!-- [CMS Pages Options](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Frequency] | Shop-Ansicht | Legt fest, wie oft Sitemap-CMS-Seiten aktualisiert werden. Optionen: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Shop-Ansicht | Ein Wert zwischen `0.0` und `1.0`, der die Priorität von Sitemap-Aktualisierungen der CMS-Seite in Bezug auf andere Inhalte bestimmt. Null (`0.0`) hat die niedrigste Priorität. |

{style="table-layout:auto"}

## [!UICONTROL Store Url Options]

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Frequency] | Shop-Ansicht | Bestimmt, wie oft die Speicher-URLs aktualisiert werden. Optionen: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Shop-Ansicht | Ein Wert zwischen `0.0` und `1.0`, der die Priorität von Aktualisierungen der Store-URL im Verhältnis zu anderen Inhalten bestimmt. Null (`0.0`) hat die niedrigste Priorität. |

{style="table-layout:auto"}

## [!UICONTROL Generation Settings]

![Erzeugungseinstellungen](./assets/xml-sitemap-generation-settings.png)<!-- zoom -->

<!-- [Generation Settings](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Shop-Ansicht | Legt fest, ob eine XML-Sitemap für den Store verfügbar ist. Optionen: `Yes` / `No` |
| [!UICONTROL Generation Method] | Shop-Ansicht | Bestimmt, wie die XML-Sitemap generiert wird. `Standard` verwendet den herkömmlichen synchronen Generierungsprozess und verarbeitet alle Daten im Speicher, während `Batch` einen asynchronen, speicheroptimierten Batch-Modus für mehr Flexibilität und Skalierbarkeit verwendet. Diese Option ist ab Version 2.4.9 verfügbar. Optionen: `Standard` / `Batch` |
| [!UICONTROL Start Time] | Shop-Ansicht | Gibt die Stunde, Minute und Sekunde des Tages an, an dem die Sitemap aktualisiert wird. |
| [!UICONTROL Frequency] | Shop-Ansicht | Bestimmt, wie oft die Sitemap aktualisiert wird. Optionen: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Shop-Ansicht | Die E-Mail-Adresse der Person, die eine Benachrichtigung erhält, wenn während des Sitemap-Aktualisierungsprozesses ein Fehler auftritt. Trennen Sie die einzelnen Adressen bei mehreren Adressen durch ein Komma. |
| [!UICONTROL Error Email Sender] | Website | Identifiziert den Store-Kontakt, der als Absender der Fehlerbenachrichtigung angezeigt wird. Optionen: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Error Email Template] | Website | Identifiziert die E-Mail-Vorlage, die für die Fehlerbenachrichtigung verwendet wird. Standardvorlage: `Sitemap generate Warnings` |

{style="table-layout:auto"}

## [!UICONTROL Sitemap File Limits]

![Sitemap-Dateibeschränkungen](./assets/xml-sitemap-sitemap-file-limits.png)<!-- zoom -->

<!-- [Sitemap File Limits](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Maximum No of URLs Per File] | Shop-Ansicht | Bestimmt die maximale Anzahl von URLs, die in eine einzelne Sitemap aufgenommen werden können. |
| [!UICONTROL Maximum File Size] | Shop-Ansicht | Bestimmt die maximale Größe der generierten Sitemap in Byte. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Submission Settings]

![Einstellungen für die Suchmaschinenübermittlung](./assets/xml-sitemap-search-engine-submission-settings.png)<!-- zoom -->

<!-- [Search Engine Submission Settings](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Submission to Robots.txt] | Shop-Ansicht | Ermöglicht die Übermittlung von Anweisungen für die Datei robots.txt. Optionen: `Yes` / `No` |

{style="table-layout:auto"}
