---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart] des Commerce-Administrators.
exl-id: d6c5ae46-32ed-4fcd-bcd6-ee3a07d7db5f
feature: Configuration, Shopping Cart
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Persistent Shopping Cart]

{{config}}

>[!NOTE]
>
>Ein [beständiger Warenkorb](../../stores-purchase/cart-persistent.md) ermöglicht die Beibehaltung nicht gekaufter Artikel, die im Warenkorb belassen werden, und speichert sie für einen Zeitraum, der in _Persistenz-Lebensdauer_ konfiguriert ist. Cookies sollten im Kundenbrowser zur Verwendung persistenter Warenkorb zugelassen werden.

## [!UICONTROL General Options]

![Allgemeine Optionen](./assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Persistence] | Webseite | Bestimmt, ob die Persistenz aktiviert ist. |
| [!UICONTROL Persistence Lifetime (seconds)] | Webseite | Definiert die Lebensdauer des beständigen Cookies in Sekunden. Der maximal zulässige Wert beträgt 3153600000 Sekunden (100 Jahre). |
| [!UICONTROL Enable "Remember Me"] | Webseite | Definiert, ob das Kontrollkästchen _Angaben speichern_ auf den Anmelde- und Registrierungsseiten des Stores angezeigt wird. Optionen: <br/>**`Yes`**- Zeigt das Kontrollkästchen _Angaben speichern_ an.<br/>**`No`** - Das Kontrollkästchen _Angaben speichern_ wird nicht angezeigt und das beständige Cookie wird nur für Kunden verwendet, die es bereits haben. |
| [!UICONTROL "Remember Me" Default Value] | Webseite | Definiert den Standardstatus für das Kontrollkästchen _Angaben speichern_ . |
| [!UICONTROL Clear Persistence on Log Out] | Webseite | Definiert, ob das persistente Cookie gelöscht wird, wenn sich ein Store-Kunde abmeldet. Unabhängig von der Konfiguration wird das persistente Cookie weiterhin verwendet, wenn sich ein Kunde nicht abmeldet, das Sitzungs-Cookie jedoch abläuft. |
| [!UICONTROL Persist Shopping Cart] | Webseite | Definiert, ob die Verwendung des beständigen Cookies Zugriff auf die Warenkorbdaten des entsprechenden Kontos gewährt. Optionen: <br/>**`Yes`**- Der Warenkorbinhalt wird nach dem Ende der Sitzung gespeichert.<br/>**`No`** - Der Warenkorbinhalt wird nach Ende der Sitzung nicht mehr gespeichert. |
| [!UICONTROL Persist Wish List] | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob der Status der Kundenwunschlisten beim Ende der Sitzung beibehalten wird. Optionen: <br/>**`Yes`**- Der Inhalt der Wunschliste wird gespeichert, wenn die Sitzung beendet wird.<br/>**`No`** - Die Wunschliste wird nicht gespeichert, wenn die Sitzung beendet wird. |
| [!UICONTROL Persist Recently Ordered Items] | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob der Status der kürzlich sortierten Elemente beibehalten wird, wenn die Sitzung beendet wird. Optionen: <br/>**`Yes`**- Der Status der zuletzt sortierten Elemente wird gespeichert, wenn die Sitzung beendet wird.<br/>**`No`** - Der Status der zuletzt sortierten Elemente wird nicht gespeichert, wenn die Sitzung beendet wird. |
| [!UICONTROL Persist Currently Compared Products] | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob der Status der derzeit verglichenen Produkte beibehalten wird, wenn die Sitzung beendet wird. Optionen: <br/>**`Yes`**- Der Status der derzeit verglichenen Produkte wird gespeichert, wenn die Sitzung beendet wird.<br/>**`No`** - Der Status der derzeit verglichenen Produkte wird nicht gespeichert, wenn die Sitzung beendet wird. |
| [!UICONTROL Persist Comparison History] | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob der Vergleichsverlauf beibehalten wird, wenn die Sitzung beendet wird. Optionen: <br/>**`Yes`**- Der Status des Vergleichsverlaufs wird gespeichert, wenn die Sitzung beendet wird.<br/>**`No`** - Der Status des Vergleichsverlaufs wird nicht gespeichert, wenn die Sitzung beendet wird. |
| [!UICONTROL Persist Recently Viewed Products] | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob der Status der zuletzt angezeigten Produkte beibehalten wird, wenn die Sitzung beendet wird. Optionen: <br/>**`Yes`**- Der Status der zuletzt angezeigten Produkte wird gespeichert, wenn die Sitzung beendet wird.<br/>**`No`** - Der Status der zuletzt angezeigten Produkte wird nicht gespeichert, wenn die Sitzung beendet wird. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob der Status der Gruppenmitgliedschaft und Segmentierungskriterien von Kunden beibehalten wird, wenn die Sitzung beendet wird. Optionen: <br/>**`Yes`**- Der Status der Gruppenmitgliedschaft und Segmentierungsdaten des Kunden wird gespeichert, wenn die Sitzung beendet wird.<br/>**`No`** - Der Status der Gruppenmitgliedschaft und Segmentierungsdaten des Kunden werden nicht gespeichert, wenn die Sitzung beendet wird. |

{style="table-layout:auto"}
