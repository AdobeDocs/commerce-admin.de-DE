---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Quotes]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL Quotes] des Commerce-Administrators.
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>Mit der Installation und Aktivierung von Adobe Commerce B2B kann das Kauferlebnis mit unternehmensspezifischen Funktionen personalisiert werden. Adobe Commerce B2B ist eine integrierte Lösung, die sowohl B2B- als auch B2C-Modelle unterstützt. Weitere Informationen zu den B2B-Funktionen finden Sie im [Adobe Commerce B2B-Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

{{config}}

<!-- [Quotes](https://docs.magento.com/user-guide/sales/quotes.html) -->

## [!UICONTROL General]

![Allgemein](./assets/quotes-general.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | Webseite | Die Mindestsumme der Warenkorb-Zwischensumme nach etwaigen Rabatten, die erforderlich ist, damit ein Kunde ein Angebot anfordern kann. Standardwert: `0` |
| [!UICONTROL Minimum Amount Message] | Store-Ansicht | Die Meldung, die im Warenkorb angezeigt wird, wenn ein Kunde versucht, eine Preisanfrage zu stellen, aber der erforderliche Mindestbetrag nicht erreicht wird. |
| [!UICONTROL Default Expiration Period] | Webseite | Bestimmt die Standardlebensdauer eines [Anführungszeichens](../../b2b/quote-price-negotiation.md) als Zeitraum ab dem Datum, an dem die Anfrage für ein Anführungszeichen gesendet wird. Optionen: `Days` / `Weeks` / `Months` |

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![ Attached Files](./assets/quotes-attached-files.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | Global | Legt die Dateiformate fest, die an ein Anführungszeichen angehängt werden können. Unterstützte Standardwerte: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` und `jpeg` |
| [!UICONTROL Maximum file size] | Global | Bestimmt die maximale Größe einer Datei, die an ein Anführungszeichen angehängt ist. Diese Einstellung kann durch die Serverkonfiguration überschrieben werden. |

{style="table-layout:auto"}
