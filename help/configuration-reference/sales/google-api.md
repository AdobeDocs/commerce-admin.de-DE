---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Google API]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL Google API] des Commerce-Administrators.
exl-id: 5031ad3d-1c9a-4bc6-9bfa-683414dca979
feature: Configuration, Marketing Tools
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Google API]

{{config}}

## [!UICONTROL Google Analytics]

![Google Analytics](./assets/google-api-analytics-ee.png)<!-- zoom -->

<!-- [Google Analytics](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Store-Ansicht | Aktiviert [!DNL Google Analytics] für Ihren Store. Optionen: `Yes` / `No` |
| [!UICONTROL Account Type] | Store-Ansicht | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt die Konfigurationsoptionen entsprechend Ihrem Google Analytics-Kontotyp. Optionen: Universal Analytics (Standard)/Google Tag Manager |
| [!UICONTROL Account Number] | Store-Ansicht | Die Kontonummer bzw. der Trackingcode, die bzw. der beim Erstellen Ihres [!DNL Google Analytics] -Kontos zugewiesen wurde. |
| [!UICONTROL Anonymize IP] | Store-Ansicht | Bestimmt, ob Identifizierungsinformationen aus IP-Adressen entfernt werden, die in [!DNL Google Analytics] Ergebnissen angezeigt werden. |
| [!UICONTROL Enable Content Experiments] | Store-Ansicht | Aktiviert [Google Content Experiments](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207), mit denen bis zu zehn verschiedene Versionen derselben Seite getestet werden können. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Google Analytics - Google Tag Manager]

{{ee-feature}}

![Google Analytics - Google Tag Manager-Kontotyp](./assets/google-api-analytics-tag-manager.png)<!-- zoom -->

Wenn **[!UICONTROL Account Type]** auf `Google Tag Manager` gesetzt ist, werden zusätzliche Felder angezeigt.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container ID] | Store-Ansicht | Die eindeutige ID für den [!DNL Google Tag Manager] -Container. Dieser Wert beginnt normalerweise mit `GTM-`. Diese ID befindet sich in Ihrem [!DNL Google Tag Manager] -Konto. Wenn [!DNL Google Tag Manager] bereits für Ihren Store installiert und konfiguriert ist, wird die Container-ID in diesem Feld automatisch angezeigt. |
| [!UICONTROL List property for the catalog page] | Store-Ansicht | Gibt die [!DNL Google Tag Manager] -Eigenschaft an, die mit der Katalogseite verknüpft ist. Standardwert: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Store-Ansicht | Identifiziert die [!DNL Google Tag Manager] -Eigenschaft, die mit dem Querverkaufsblock verknüpft ist. Standardwert: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Store-Ansicht | Identifiziert die [!DNL Google Tag Manager] -Eigenschaft, die mit dem Upsell-Block verknüpft ist. Standardwert: `Up-sell` |
| [!UICONTROL List property for the related products block] | Store-Ansicht | Identifiziert die [!DNL Google Tag Manager] -Eigenschaft, die mit dem zugehörigen Produktblock verknüpft ist. Standardwert: `Related Products` |
| [!UICONTROL List property for the search results page] | Store-Ansicht | Identifiziert die [!DNL Google Tag Manager] -Eigenschaft, die mit der Suchergebnisseite verknüpft ist. Standardwert: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Store-Ansicht | Identifiziert die [!DNL Google Tag Manager] -Eigenschaft, die mit den Bezeichnungen für interne Promotions verknüpft ist. Standardwert: `Label` |

{style="table-layout:auto"}

## [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-google-adwords.png)<!-- zoom -->

<!-- [Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Store-Ansicht | Aktiviert Google AdWords für den Store. Optionen: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Store-Ansicht | Die ID aus Ihrem Google AdWords-Konto. |
| [!UICONTROL Conversion Language] | Store-Ansicht | Die Sprache, die für AdWords-Konvertierungen verwendet wird. Optionen: `All available languages` |
| [!UICONTROL Conversion Format] | Store-Ansicht | Bestimmt das Format der [!DNL Google Site Stats] -Benachrichtigung, die auf der Konvertierungsseite angezeigt wird. Die Benachrichtigung verlinkt zu einer Seite, die Besucher über die Cookies informiert, die zur Verfolgung ihrer Besuche verwendet werden. Dieser numerische Wert wird der Variable `google_conversion_format` in Ihrem AdWords-Skript zugewiesen. Weitere Informationen finden Sie unter [Über das Konversions-Tracking](https://support.google.com/google-ads/answer/1722022?hl=en) auf der Google-Website. Optionen: <br/>**`1`**- Zeigt eine einzeilige Benachrichtigung an.<br/>**`2`** - (Standard) Zeigt eine zweizeilige Benachrichtigung an. <br/>**`3`**- Zeigt keine Kundenbenachrichtigung an. |
| [!UICONTROL Conversion Color] | Store-Ansicht | Bestimmt die Farbe der Konversionsbeschriftung. Verwenden Sie einen [Farbwähler](https://www.w3schools.com/colors/colors_picker.asp), um den Hexadezimalwert auszuwählen. Dieser hexadezimale Wert wird der Variable `google_conversion_color` in Ihrem AdWords-Skript zugewiesen. Beispiel: ffffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Store-Ansicht | Eine Textbeschriftung, die mit der Benachrichtigung [!DNL Google Site Stats] angezeigt wird. Diese Textzeichenfolge wird der Variable `~` in Ihrem AdWords-Skript zugewiesen. Beispiel: &quot;Vielen Dank für Ihr Einkaufen!&quot; |
| [!UICONTROL Conversion Value Type] | Store-Ansicht | Gibt den Typ des Werts an, mit dem bestimmt wird, wann eine Konvertierung stattfindet. Optionen: <br/>**`Dynamic`**- Bestimmt anhand des dynamischen Bestellbetrags, ob eine Konversion stattgefunden hat.<br/>**`Constant`** - Stellt fest, dass eine Konversion anhand des eingegebenen Werts stattgefunden hat. |
| [!UICONTROL Conversion Value] | Store-Ansicht | Gibt den Wert an, der für den Konversionswerttyp _[!UICONTROL Constant]_verwendet wird. |
| [!UICONTROL Send Order Currency] | Store-Ansicht | Aktiviert transaktionsspezifische Währungskonversionswerte in AdWords (für Websites mit unterschiedlichen Basiswährungen). |

{style="table-layout:auto"}

## [!UICONTROL Google GTag]

{{gtag-api-note}}

### [!UICONTROL Google Analytics4]

![Google Analytics4](./assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

<!-- [Google Analytics4](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Store-Ansicht | Aktiviert Google Analytics 4 für Ihren Store. Optionen: `Yes` / `No` |
| [!UICONTROL Account Type] | Store-Ansicht | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt die Konfigurationsoptionen entsprechend Ihrem Google Analytics-Kontotyp. Optionen: `Google Analytics4` (Standard) / `Google Tag Manager` |
| [!UICONTROL Measurement ID] | Store-Ansicht | Die Kontonummer bzw. der Trackingcode, die bzw. der beim Erstellen Ihres Google Analytics-Kontos zugewiesen wurde. |
| [!UICONTROL Anonymize IP] | Store-Ansicht | Bestimmt, ob Identifizierungsinformationen aus IP-Adressen entfernt werden, die in Google Analytics-Ergebnissen angezeigt werden. |
| [!UICONTROL Enable Content Experiments] | Store-Ansicht | Aktiviert [Google Content Experiments](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207), mit denen bis zu zehn verschiedene Versionen derselben Seite getestet werden können. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Google Analytics4 - Google Tag Manager]

{{ee-feature}}

![Google Analytics4 - Google Tag Manager-Kontotyp](./assets/google-api-gtag-google-analytics4-gtm.png)<!-- zoom -->

Wenn **[!UICONTROL Account Type]** auf `Google Tag Manager` gesetzt ist, werden zusätzliche Felder angezeigt.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container Id] | Store-Ansicht | Die eindeutige ID für den [!DNL Google Tag Manager] -Container. Dieser Wert beginnt normalerweise mit `GTM-`. Diese ID befindet sich in Ihrem Google Tab Manager-Konto. Wenn [!DNL Google Tag Manager] bereits für Ihren Store installiert und konfiguriert ist, wird die Container-ID in diesem Feld automatisch angezeigt. |
| [!UICONTROL List property for the catalog page] | Store-Ansicht | Gibt die [!DNL Google Tag Manager] -Eigenschaft an, die mit der Katalogseite verknüpft ist. Standardwert: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Store-Ansicht | Identifiziert die [!DNL Google Tag Manager] -Eigenschaft, die mit dem Querverkaufsblock verknüpft ist. Standardwert: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Store-Ansicht | Identifiziert die [!DNL Google Tag Manager] -Eigenschaft, die mit dem Upsell-Block verknüpft ist. Standardwert: `Up-sell` |
| [!UICONTROL List property for the related products block] | Store-Ansicht | Identifiziert die [!DNL Google Tag Manager] -Eigenschaft, die mit dem zugehörigen Produktblock verknüpft ist. Standardwert: `Related Products` |
| [!UICONTROL List property for the search results page] | Store-Ansicht | Identifiziert die [!DNL Google Tag Manager] -Eigenschaft, die mit der Suchergebnisseite verknüpft ist. Standardwert: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Store-Ansicht | Identifiziert die [!DNL Google Tag Manager] -Eigenschaft, die mit den Bezeichnungen für interne Promotions verknüpft ist. Standardwert: `Label` |

{style="table-layout:auto"}

### [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-gtag-google-adwords.png)<!-- zoom -->

<!-- -- Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Store-Ansicht | Aktiviert Google AdWords für den Store. Optionen: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Store-Ansicht | Die ID aus Ihrem Google AdWords-Konto. |
| [!UICONTROL Conversion Language] | Store-Ansicht | Die Sprache, die für AdWords-Konvertierungen verwendet wird. Optionen: Alle verfügbaren Sprachen |
| [!UICONTROL Conversion Format] | Store-Ansicht | Legt das Format der Google Site Stats-Benachrichtigung fest, die auf der Konvertierungsseite angezeigt wird. Die Benachrichtigung verlinkt zu einer Seite, die Besucher über die Cookies informiert, die zur Verfolgung ihrer Besuche verwendet werden. Dieser numerische Wert wird der Variable `google_conversion_format` in Ihrem AdWords-Skript zugewiesen. Weitere Informationen finden Sie unter [Über das Konversions-Tracking](https://support.google.com/google-ads/answer/1722022?hl=en) auf der Google-Website. Optionen: <br/>**`1`**- Zeigt eine einzeilige Benachrichtigung an.<br/>**`2`** - (Standard) Zeigt eine zweizeilige Benachrichtigung an. <br/>**`3`**- Zeigt keine Kundenbenachrichtigung an. |
| [!UICONTROL Conversion Color] | Store-Ansicht | Bestimmt die Farbe der Konversionsbeschriftung. Verwenden Sie einen [Farbwähler](https://www.w3schools.com/colors/colors_picker.asp), um den Hexadezimalwert auszuwählen. Dieser hexadezimale Wert wird der Variable `google_conversion_color` in Ihrem AdWords-Skript zugewiesen. Beispiel: ffffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Store-Ansicht | Eine Textbeschriftung, die mit der Google Site Stats-Benachrichtigung angezeigt wird. Diese Textzeichenfolge wird der Variable `~` in Ihrem AdWords-Skript zugewiesen. Beispiel: &quot;Vielen Dank für Ihr Einkaufen!&quot; |
| [!UICONTROL Conversion Value Type] | Store-Ansicht | Gibt den Typ des Werts an, mit dem bestimmt wird, wann eine Konvertierung stattfindet. Optionen: <br/>**`Dynamic`**- Bestimmt anhand des dynamischen Bestellbetrags, ob eine Konversion stattgefunden hat.<br/>**`Constant`** - Stellt fest, dass eine Konversion anhand des eingegebenen Werts stattgefunden hat. |
| [!UICONTROL Conversion Value] | Store-Ansicht | Gibt den Wert an, der für den Konversionswerttyp _[!UICONTROL Constant]_verwendet wird. |
| [!UICONTROL Send Order Currency] | Store-Ansicht | Aktiviert transaktionsspezifische Währungskonversionswerte in AdWords (für Websites mit unterschiedlichen Basiswährungen). |

{style="table-layout:auto"}
