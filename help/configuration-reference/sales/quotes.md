---
title: '[!UICONTROL Sales] > [!UICONTROL Quotes]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] > [!UICONTROL Quotes] des Commerce Admin.
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
TQID: https://experienceleague.adobe.com/puZjB2YCCyZXT0U6AdDBd-YjxopU637-yxgOaB6hkvM
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
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>Mit der Installation und Aktivierung von Adobe Commerce B2B kann das Kauferlebnis mit unternehmensspezifischen Funktionen personalisiert werden. Adobe Commerce B2B ist eine integrierte Lösung, die sowohl B2B- als auch B2C-Modelle unterstützt. Weitere Informationen zu den B2B-Funktionen finden Sie im [Adobe Commerce B2B-Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=de).

{{config}}

<!-- [Quotes](https://experienceleague.adobe.com/de/docs/commerce-admin/b2b/quotes/quotes) -->

## [!UICONTROL General]

![Allgemein](./assets/quotes-general.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | Website | Der Mindestbetrag der Zwischensumme des Warenkorbs nach allen Rabatten, der erforderlich ist, bevor ein Kunde eine Angebotsanfrage einreichen kann. Standardwert: `0` |
| [!UICONTROL Minimum Amount Message] | Shop-Ansicht | Die Nachricht, die im Warenkorb angezeigt wird, wenn ein Kunde versucht, eine Angebotsanfrage einzureichen, aber der erforderliche Mindestbetrag nicht erreicht wurde. |
| [!UICONTROL Default Expiration Period] | Website | Bestimmt die standardmäßige Lebensdauer eines [Angebots](../../b2b/quote-price-negotiation.md) als Zeitraum ab dem Datum, an dem die Angebotsanfrage gesendet wird. Optionen: `Days` / `Weeks` / `Months` |

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![angehängte Dateien](./assets/quotes-attached-files.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | Global | Legt die Dateiformate fest, die an ein Angebot angehängt werden können. Unterstützte Standardwerte: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` und `jpeg` |
| [!UICONTROL Maximum file size] | Global | Bestimmt die maximale Größe für eine Datei, die an ein Angebot angehängt ist. Diese Einstellung kann von der Server-Konfiguration überschrieben werden. |

{style="table-layout:auto"}
