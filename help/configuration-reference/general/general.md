---
title: '[!UICONTROL General] &gt; [!UICONTROL General]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL General] &gt; [!UICONTROL General] Seite des Commerce-Administrators.
exl-id: 67760d24-ad12-4c49-9649-0607c57f5cf0
feature: Configuration, System
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL General]

{{config}}

## [!UICONTROL Country Options]

Siehe [Länderoptionen](../../getting-started/store-details.md#country-options) für weitere Informationen zu diesen Konfigurationsfeldern und Optionen.

![Allgemein > Länderoptionen](./assets/general-country-options.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Default Country] | Store-Ansicht | Das Land, in dem sich Ihr Geschäft befindet. |
| [!UICONTROL Allow Countries] | Webseite | Die Länder, in denen Sie Bestellungen annehmen. |
| [!UICONTROL Zip/Postal Code is Optional for] | Global | Länder, die keine Postleitzahl in der Lieferadresse benötigen. |
| [!UICONTROL European Union Countries] | Global | Länder, die Mitglieder der Europäischen Union sind. |
| [!UICONTROL Top Destinations] | Store-Ansicht | Die wichtigsten Länder, die Sie für den Verkauf auswählen. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL State Options]

Siehe [Statusoptionen](../../getting-started/store-details.md#state-options) für weitere Informationen zu diesen Konfigurationsfeldern und Optionen.

![Allgemein > Statusoptionen](./assets/general-state-options.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL State is required for] | Global | Die Länder (in denen Sie geschäftlich tätig sind), in denen eine Region oder ein Staat in die Postanschrift aufgenommen werden muss. |
| [!UICONTROL Allow to Choose State if It is Optional for Country] | Global | Stellt für Länder, in denen dies nicht erforderlich ist, fest, ob die Variable _Region/Bundesland_ -Feld ist in der Postanschrift des Kunden enthalten.<br /> <br />**`Yes`**- Enthält die _Region/Bundesland_ -Feld in die Kundenadresse ein, auch wenn dies vom Land nicht benötigt wird.<br />**`No`** - Lässt das Feld Region/Bundesland von der Kundenadresse aus zu, wenn dies vom Land nicht benötigt wird. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Locale Options]

Siehe [Gebietsschemaoptionen](../../getting-started/store-details.md#locale-options) für weitere Informationen zu diesen Konfigurationsfeldern und Optionen.

![Allgemein > Gebietsschemaoptionen](./assets/general-locale-options.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Timezone] | Webseite | Die Zeitzone des Primärmarkts, der von der Website bereitgestellt wird. Normalerweise entspricht die Zeitzone der am physischen Standort Ihres Unternehmens verwendeten. |
| [!UICONTROL Locale] | Store-Ansicht | Die Sprache, Währung und das Messsystem, die auf dem Markt verwendet wird, der von der Store-Ansicht bereitgestellt wird. |
| [!UICONTROL Weight Unit] | Store-Ansicht | Die Maßeinheit, die normalerweise für Sendungen vom Gebietsschema verwendet wird. Optionen: `lbs` / `kgs` |
| [!UICONTROL First Day of Week] | Store-Ansicht | Der Tag, der als erster Tag der Woche auf dem Markt gilt, der von der Store-Ansicht bereitgestellt wird. |
| [!UICONTROL Weekend Days] | Store-Ansicht | Die Tage, die auf das Wochenende fallen auf dem Markt serviert von der Store-Ansicht. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Website Restrictions]

{{ee-feature}}

![Allgemein > Website-Einschränkungen](./assets/general-website-restrictions.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Zugriffsbeschränkungen](../../merchandising-promotions/event-configure.md#access-restrictions) im _Handbuch zu Merchandising und Promotions_.

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Access Restriction] | Webseite | Bestimmt, ob die Website im eingeschränkten Modus ausgeführt wird.<br /> <br />**`Yes`**- Der Website-Zugriff ist wie in den unten stehenden Feldern festgelegt eingeschränkt.<br />**`No`** - Einschränkungen sind deaktiviert und die folgenden Einstellungen haben keine Auswirkungen. |
| [!UICONTROL Restriction Mode] | Webseite | Bestimmt die Art der Zugriffsbeschränkung, die für die Website gilt.<br /> <br />**`Website Closed`**- Der Zugriff auf die Storefront ist eingeschränkt und Storefront-URLs werden vorübergehend zur Landingpage weitergeleitet. Diese Einstellung kann während der Site-Wartung oder vor dem Start nützlich sein.<br />**`Private Sales: Login Only`** - Nur registrierte Kunden können sich anmelden, um auf die Storefront zuzugreifen. Alle Storefront-URLs werden vorübergehend zur angegebenen Landingpage oder zum Anmeldeformular umgeleitet. Benutzer können in diesem Modus kein Konto erstellen.<br />**`Private Sales: Login and Register`**- Benutzer müssen sich anmelden, um auf die Storefront zuzugreifen. Alle Storefront-URLs werden vorübergehend zum Anmeldeformular weitergeleitet, bis sich der Benutzer anmeldet. Benutzer können sich für ein Konto registrieren, während sich die Site in diesem Modus befindet. |
| [!UICONTROL Startup Page] | Store-Ansicht | Wenn sich die Website im privaten Verkaufsmodus befindet, bestimmt diese Einstellung die Seite, die angezeigt wird, bis sich der Kunde anmeldet.<br />  <br />**`To login form`**- Benutzer werden bis zur Anmeldung zum Anmeldeformular weitergeleitet.<br />**`To landing page`** - Benutzer werden bis zur Anmeldung zu der unten angegebenen statischen Seite weitergeleitet.<br /> <br />**_Wichtig!_**Stellen Sie sicher, dass Sie von der angegebenen Landingpage einen Link zur Anmeldeseite hinzufügen, damit sich Kunden anmelden können, um auf die vollständige Site zuzugreifen. |
| [!UICONTROL Landing Page] | Store-Ansicht | Legt die erste Seite fest, die angezeigt wird, wenn sich die Website im privaten Verkaufsmodus befindet. |
| [!UICONTROL HTTP Response] | Webseite | Bestimmt die HTTP-Antwort, die gesendet wird, wenn die Website geschlossen wird und eine Verbindung von einem Bot, Crawler oder Spider hergestellt wird.<br /> <br />**`503 Service unavailable`**- Die Seite ist nicht verfügbar, aber der Spider sollte den Index nicht aktualisieren.<br />**`200 OK`** - Die Landingpage ist korrekt und sollte vom Spider als einzige Seite auf der Site behandelt werden. |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | Webseite | Bestimmt, ob die Felder auf der _Anmelden_ und _Kennwort vergessen_ Formulare werden automatisch aus früheren Einträgen ausgefüllt. Optionen: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Store Information]

![Allgemein > Store-Informationen](./assets/general-store-information.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Store-Informationen](../../getting-started/store-details.md) im _Handbuch &quot;Erste Schritte&quot;_.

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Store Name] | Store-Ansicht | Der Name des Stores, der mit der Store-Ansicht verknüpft ist. |
| [!UICONTROL Store Phone Number] | Store-Ansicht | Die primäre Telefonnummer des Stores (die mit der Store-Ansicht verknüpft ist) ist für Unternehmen zugänglich. Beispiel: Mo. - Fr., 9-5, Sat. 9.00 Uhr PST |
| Land | Webseite | Das Land des Unternehmens, das die Website betreibt. |
| [!UICONTROL Region/State] | Webseite | Die Region oder der Bundesstaat des Unternehmens, das die Website betreibt. |
| [!UICONTROL ZIP/Postal Code] | Webseite | Die Postleitzahl des Unternehmens, das die Website betreibt. |
| [!UICONTROL City] | Webseite | Der Ort des Unternehmens, das die Website betreibt. |
| [!UICONTROL Street Address] | Webseite | Die Straße oder Postanschrift des Unternehmens, das die Website betreibt. |
| [!UICONTROL Street Address Line 2|]Webseite | Die zweite Zeile der Geschäftsstraßen-Adresse, falls erforderlich. |
| [!UICONTROL VAT Number] | Webseite | Die Mehrwertsteuernummer des Unternehmens, dem die Commerce-Installation gehört, falls zutreffend. |
| [!UICONTROL Validate VAT Number] |  | Überprüft die Umsatzsteuer-Identifikationsnummer. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Single-Store Mode]

![Allgemein > Einzelspeichermodus](./assets/general-single-store-mode.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Einzelspeichermodus](../../getting-started/websites-stores-views.md#single-store-mode) im _Handbuch &quot;Erste Schritte&quot;_.

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Single-Store Mode] | Global | Wenn dies für Einzelspeicherinstallationen aktiviert ist, blendet das Konfigurationsfeld Umfang und zugehörige Feldbezeichnungen Optionen aus: `Yes` / `No` <br/>**_Hinweis:_**Der Einzelspeichermodus wird bei Geschäften mit mehr als einer Ansicht ignoriert. |

{:style=&quot;table-layout:auto&quot;}
