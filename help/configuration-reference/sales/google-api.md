---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Google API]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL Google API] des Commerce Admin-Bereichs.
exl-id: 5031ad3d-1c9a-4bc6-9bfa-683414dca979
feature: Configuration, Marketing Tools
source-git-commit: 5ee52e8d4f2ebb8fc28f13cca53e87c3529f76d3
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Google API]

{{config}}

## [!UICONTROL Google Analytics]

![Google Analytics](./assets/google-api-analytics-ee.png)<!-- zoom -->

<!-- [Google Analytics](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/google-tools/google-analytics) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Shop-Ansicht | Aktiviert die [!DNL Google Analytics] für Ihren Store. Optionen: `Yes` / `No` |
| [!UICONTROL Account Type] | Shop-Ansicht | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Legt die Konfigurationsoptionen entsprechend Ihrem Google Analytics-Kontotyp fest. Optionen: Universal Analytics (Standard) / Google Tag Manager |
| [!UICONTROL Account Number] | Shop-Ansicht | Die Kontonummer oder der Trackingcode, die bzw. der beim Erstellen Ihres [!DNL Google Analytics] Kontos zugewiesen wurde. |
| [!UICONTROL Anonymize IP] | Shop-Ansicht | Bestimmt, ob identifizierende Informationen aus IP-Adressen entfernt werden, die in [!DNL Google Analytics] Ergebnissen angezeigt werden. |

{style="table-layout:auto"}

## [!UICONTROL Google Analytics - Google Tag Manager]

{{ee-feature}}

![Google Analytics - Google Tag Manager-Kontotyp](./assets/google-api-analytics-tag-manager.png)<!-- zoom -->

Wenn **[!UICONTROL Account Type]** auf `Google Tag Manager` gesetzt ist, werden zusätzliche Felder angezeigt.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container ID] | Shop-Ansicht | Die eindeutige ID für den [!DNL Google Tag Manager]. Dieser Wert beginnt normalerweise mit `GTM-`. Diese ID befindet sich in Ihrem [!DNL Google Tag Manager]. Wenn [!DNL Google Tag Manager] bereits für Ihren Store installiert und konfiguriert ist, wird die Container-ID automatisch in diesem Feld angezeigt. |
| [!UICONTROL List property for the catalog page] | Shop-Ansicht | Identifiziert die [!DNL Google Tag Manager] Eigenschaft, die mit der Katalogseite verknüpft ist. Standardwert: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Shop-Ansicht | Identifiziert die [!DNL Google Tag Manager] Eigenschaft, die mit dem Crosssell-Block verknüpft ist. Standardwert: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Shop-Ansicht | Gibt die [!DNL Google Tag Manager] Eigenschaft an, die mit dem Upsell-Block verknüpft ist. Standardwert: `Up-sell` |
| [!UICONTROL List property for the related products block] | Shop-Ansicht | Identifiziert die [!DNL Google Tag Manager] Eigenschaft, die mit dem zugehörigen Produktblock verknüpft ist. Standardwert: `Related Products` |
| [!UICONTROL List property for the search results page] | Shop-Ansicht | Gibt die [!DNL Google Tag Manager] an, die mit der Suchergebnisseite verknüpft ist. Standardwert: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Shop-Ansicht | Identifiziert die [!DNL Google Tag Manager] Eigenschaft, die mit den Kennzeichnungen für interne Promotions verknüpft ist. Standardwert: `Label` |

{style="table-layout:auto"}

## [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-google-adwords.png)<!-- zoom -->

<!-- [Google AdWords](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/google-tools/google-adwords) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Shop-Ansicht | Aktiviert Google AdWords für den Store. Optionen: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Shop-Ansicht | Die ID aus Ihrem Google AdWords-Konto. |
| [!UICONTROL Conversion Language] | Shop-Ansicht | Die Sprache, die für AdWords-Konvertierungen verwendet wird. Optionen: `All available languages` |
| [!UICONTROL Conversion Format] | Shop-Ansicht | Legt das Format der [!DNL Google Site Stats] fest, die auf der Konvertierungsseite angezeigt wird. Die Benachrichtigung verweist auf eine Seite, die Besuchende über die Cookies informiert, die zum Nachverfolgen ihrer Besuche verwendet werden. Dieser numerische Wert wird der Variablen `google_conversion_format` in Ihrem AdWords-Skript zugewiesen. Weitere Informationen finden Sie unter [Über das Konversions](https://support.google.com/google-ads/answer/1722022?hl=en)Tracking auf der Google-Website. Optionen: <br/>**`1`**- Zeigt eine einzeilige Benachrichtigung an.<br/>**`2`** - (Standard) Zeigt eine zweizeilige Benachrichtigung an. <br/>**`3`**- Zeigt keine Kundenbenachrichtigung an. |
| [!UICONTROL Conversion Color] | Shop-Ansicht | Bestimmt die Farbe der Konvertierungsbeschriftung. Verwenden Sie einen [Farbwähler](https://www.w3schools.com/colors/colors_picker.asp), um den Hexadezimalwert auszuwählen. Dieser Hexadezimalwert wird der Variablen `google_conversion_color` in Ihrem AdWords-Skript zugewiesen. Beispiel: ffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Shop-Ansicht | Eine Textbeschriftung, die mit der [!DNL Google Site Stats] Benachrichtigung angezeigt wird. Diese Textzeichenfolge wird der Variablen `~` in Ihrem AdWords-Skript zugewiesen. Beispiel: „Vielen Dank für Ihren Einkauf!“ |
| [!UICONTROL Conversion Value Type] | Shop-Ansicht | Gibt den Typ des Werts an, mit dem bestimmt wird, wann eine Konvertierung stattfindet. Optionen: <br/>**`Dynamic`**- Bestimmt anhand des dynamischen Bestellbetrags, ob eine Konversion stattgefunden hat.<br/>**`Constant`** - Bestimmt anhand des eingegebenen Werts, dass eine Konvertierung stattgefunden hat. |
| [!UICONTROL Conversion Value] | Shop-Ansicht | Gibt den Wert an, der für einen _[!UICONTROL Constant]_&#x200B;Konversionswerttyp verwendet wird. |
| [!UICONTROL Send Order Currency] | Shop-Ansicht | Ermöglicht transaktionsspezifische Währungsumrechnungswerte in AdWords (für Websites mit unterschiedlichen Basiswährungen). |

{style="table-layout:auto"}

## [!UICONTROL Google GTag]

{{gtag-api-note}}

### [!UICONTROL Google Analytics4]

![Google Analytics4](./assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

<!-- [Google Analytics4](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/google-tools/google-analytics) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Shop-Ansicht | Aktiviert Google Analytics 4 für Ihren Store. Optionen: `Yes` / `No` |
| [!UICONTROL Account Type] | Shop-Ansicht | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Legt die Konfigurationsoptionen entsprechend Ihrem Google Analytics-Kontotyp fest. Optionen: `Google Analytics4` (Standard) / `Google Tag Manager` |
| [!UICONTROL Measurement ID] | Shop-Ansicht | Die Kontonummer oder der Trackingcode, die bzw. der beim Erstellen Ihres Google Analytics-Kontos zugewiesen wurde. |
| [!UICONTROL Anonymize IP] | Shop-Ansicht | Bestimmt, ob identifizierende Informationen aus IP-Adressen entfernt werden, die in den Google Analytics-Ergebnissen angezeigt werden. |

{style="table-layout:auto"}

### [!UICONTROL Google Analytics4 - Google Tag Manager]

{{ee-feature}}

![Google Analytics4 - Google Tag Manager-Kontotyp](./assets/google-api-gtag-google-analytics4-gtm.png)<!-- zoom -->

Wenn **[!UICONTROL Account Type]** auf `Google Tag Manager` gesetzt ist, werden zusätzliche Felder angezeigt.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container Id] | Shop-Ansicht | Die eindeutige ID für den [!DNL Google Tag Manager]. Dieser Wert beginnt normalerweise mit `GTM-`. Diese ID befindet sich in Ihrem Google Tab Manager-Konto. Wenn [!DNL Google Tag Manager] bereits für Ihren Store installiert und konfiguriert ist, wird die Container-ID automatisch in diesem Feld angezeigt. |
| [!UICONTROL List property for the catalog page] | Shop-Ansicht | Identifiziert die [!DNL Google Tag Manager] Eigenschaft, die mit der Katalogseite verknüpft ist. Standardwert: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Shop-Ansicht | Identifiziert die [!DNL Google Tag Manager] Eigenschaft, die mit dem Crosssell-Block verknüpft ist. Standardwert: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Shop-Ansicht | Gibt die [!DNL Google Tag Manager] Eigenschaft an, die mit dem Upsell-Block verknüpft ist. Standardwert: `Up-sell` |
| [!UICONTROL List property for the related products block] | Shop-Ansicht | Identifiziert die [!DNL Google Tag Manager] Eigenschaft, die mit dem zugehörigen Produktblock verknüpft ist. Standardwert: `Related Products` |
| [!UICONTROL List property for the search results page] | Shop-Ansicht | Gibt die [!DNL Google Tag Manager] an, die mit der Suchergebnisseite verknüpft ist. Standardwert: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Shop-Ansicht | Identifiziert die [!DNL Google Tag Manager] Eigenschaft, die mit den Kennzeichnungen für interne Promotions verknüpft ist. Standardwert: `Label` |

{style="table-layout:auto"}

### [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-gtag-google-adwords.png)<!-- zoom -->

<!-- -- Google AdWords](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/google-tools/google-adwords) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Shop-Ansicht | Aktiviert Google AdWords für den Store. Optionen: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Shop-Ansicht | Die ID aus Ihrem Google AdWords-Konto. |
| [!UICONTROL Conversion Language] | Shop-Ansicht | Die Sprache, die für AdWords-Konvertierungen verwendet wird. Optionen: Alle verfügbaren Sprachen |
| [!UICONTROL Conversion Format] | Shop-Ansicht | Legt das Format der Google-Site-Statusbenachrichtigung fest, die auf der Konvertierungsseite angezeigt wird. Die Benachrichtigung verweist auf eine Seite, die Besuchende über die Cookies informiert, die zum Nachverfolgen ihrer Besuche verwendet werden. Dieser numerische Wert wird der Variablen `google_conversion_format` in Ihrem AdWords-Skript zugewiesen. Weitere Informationen finden Sie unter [Über das Konversions](https://support.google.com/google-ads/answer/1722022?hl=en)Tracking auf der Google-Website. Optionen: <br/>**`1`**- Zeigt eine einzeilige Benachrichtigung an.<br/>**`2`** - (Standard) Zeigt eine zweizeilige Benachrichtigung an. <br/>**`3`**- Zeigt keine Kundenbenachrichtigung an. |
| [!UICONTROL Conversion Color] | Shop-Ansicht | Bestimmt die Farbe der Konvertierungsbeschriftung. Verwenden Sie einen [Farbwähler](https://www.w3schools.com/colors/colors_picker.asp), um den Hexadezimalwert auszuwählen. Dieser Hexadezimalwert wird der Variablen `google_conversion_color` in Ihrem AdWords-Skript zugewiesen. Beispiel: ffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Shop-Ansicht | Eine Textbeschriftung, die mit der Google-Site-Statusbenachrichtigung angezeigt wird. Diese Textzeichenfolge wird der Variablen `~` in Ihrem AdWords-Skript zugewiesen. Beispiel: „Vielen Dank für Ihren Einkauf!“ |
| [!UICONTROL Conversion Value Type] | Shop-Ansicht | Gibt den Typ des Werts an, mit dem bestimmt wird, wann eine Konvertierung stattfindet. Optionen: <br/>**`Dynamic`**- Bestimmt anhand des dynamischen Bestellbetrags, ob eine Konversion stattgefunden hat.<br/>**`Constant`** - Bestimmt anhand des eingegebenen Werts, dass eine Konvertierung stattgefunden hat. |
| [!UICONTROL Conversion Value] | Shop-Ansicht | Gibt den Wert an, der für einen _[!UICONTROL Constant]_&#x200B;Konversionswerttyp verwendet wird. |
| [!UICONTROL Send Order Currency] | Shop-Ansicht | Ermöglicht transaktionsspezifische Währungsumrechnungswerte in AdWords (für Websites mit unterschiedlichen Basiswährungen). |

{style="table-layout:auto"}
