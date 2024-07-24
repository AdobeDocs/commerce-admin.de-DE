---
title: Konfigurationsreferenz für beständigen Warenkorb
description: Wiederverwendbarer Inhalt für die Konfigurationsreferenz des beständigen Warenkorbs.
source-git-commit: d23cb0d63409e533cf950d8d14514d9f9157fd05
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# [!UICONTROL General Options]

![Allgemeine Optionen](/help/configuration-reference/customers/assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| Feld | [Umfang](/help/getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |------------------------------------------------------------------------|--- |
| [!UICONTROL Enable Persistence] | Webseite | Bestimmt, ob die Persistenzfunktion aktiviert ist. |
| [!UICONTROL Persistence Lifetime (seconds)] | Webseite | Definiert die Lebensdauer des beständigen Cookies in Sekunden. Der maximal zulässige Wert beträgt 34560000 Sekunden (400 Tage). Dies ist eine Beschränkung der maximal empfohlenen Cookie-Lebensdauer. |
| [!UICONTROL Enable "Remember Me"] | Webseite | Definiert, ob das Kontrollkästchen _Angaben speichern_ auf den Anmelde- und Registrierungsseiten des Stores angezeigt wird. Optionen: <br/>**`Yes`**- Zeigt das Kontrollkästchen _Angaben speichern_ an.<br/>**`No`** - Das Kontrollkästchen _Angaben speichern_ wird nicht angezeigt und das beständige Cookie wird nur für Kunden verwendet, die es bereits haben. |
| [!UICONTROL "Remember Me" Default Value] | Webseite | Definiert den Standardstatus für das Kontrollkästchen _Angaben speichern_ . |
| [!UICONTROL Clear Persistence on Log Out] | Webseite | Definiert, ob das persistente Cookie gelöscht wird, wenn sich ein Store-Kunde abmeldet. Unabhängig von der Konfiguration dieser Option wird das persistente Cookie weiterhin verwendet, wenn sich ein Kunde nicht abmeldet, das Sitzungs-Cookie jedoch abläuft. |
| [!UICONTROL Persist Shopping Cart] | Webseite | Definiert, ob die Verwendung des beständigen Cookies den Zugriff auf die Warenkorbdaten des entsprechenden Kontos ermöglicht. Optionen: <br/>**`Yes`**oder **`No`**. |
| [!UICONTROL Persist Wish List] | Webseite | ![Adobe Commerce](/help/assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob der Status der Kundenwunschlisten beim Ende der Sitzung beibehalten wird. Optionen: <br/>**`Yes`**- Der Inhalt der Wunschliste wird gespeichert, wenn die Sitzung beendet wird.<br/>**`No`** - Die Wunschliste wird nicht gespeichert, wenn die Sitzung beendet wird. |
| [!UICONTROL Persist Recently Ordered Items] | Webseite | ![Adobe Commerce](/help/assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob der Status der kürzlich sortierten Elemente gespeichert wird, wenn die Sitzung beendet wird. Optionen: <br/>**`Yes`**oder **`No`**. |
| [!UICONTROL Persist Currently Compared Products] | Webseite | ![Adobe Commerce](/help/assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob der Status der derzeit verglichenen Produkte beibehalten wird, wenn die Sitzung beendet wird. Optionen: <br/>**`Yes`**oder **`No`**. |
| [!UICONTROL Persist Comparison History] | Webseite | ![Adobe Commerce](/help/assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob der Vergleichsverlauf beibehalten wird, wenn die Sitzung beendet wird. Optionen: <br/>**`Yes`**oder **`No`**. |
| [!UICONTROL Persist Recently Viewed Products] | Webseite | ![Adobe Commerce](/help/assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob der Status der zuletzt angezeigten Produkte beibehalten wird, wenn die Sitzung beendet wird. Optionen: <br/>**`Yes`**oder **`No`**. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Webseite | ![Adobe Commerce](/help/assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob der Status der Gruppenmitgliedschaft und Segmentierungskriterien von Kunden beibehalten wird, wenn die Sitzung beendet wird. Optionen: <br/>**`Yes`**- Der Status der Gruppenmitgliedschaft und Segmentierungsdaten des Kunden wird gespeichert, wenn die Sitzung beendet wird.<br/>**`No`** - Der Status der Gruppenmitgliedschaft und Segmentierungsdaten des Kunden werden nicht gespeichert, wenn die Sitzung beendet wird. |

{style="table-layout:auto"}
