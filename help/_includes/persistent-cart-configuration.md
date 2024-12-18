---
title: Konfigurationsreferenz des beständigen Warenkorbs
description: Wiederverwendbarer Inhalt für die Konfigurationsreferenz des beständigen Warenkorbs.
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# [!UICONTROL General Options]

![Allgemeine Optionen](/help/configuration-reference/customers/assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-persistent#configure-a-persistent-cart) -->

| Feld | [Umfang](/help/getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |------------------------------------------------------------------------|--- |
| [!UICONTROL Enable Persistence] | Website | Legt fest, ob die Persistenzfunktion aktiviert ist. |
| [!UICONTROL Persistence Lifetime (seconds)] | Website | Definiert die Lebensdauer des persistenten Cookies in Sekunden. Der maximal zulässige Wert ist 34560000 Sekunden (400 Tage). Dies ist eine Begrenzung der maximal empfohlenen Cookie-Lebensdauer. |
| [!UICONTROL Enable "Remember Me"] | Website | Definiert, ob _Kontrollkästchen_ Angaben speichern“ auf den Anmelde- und Registrierungsseiten des Stores angezeigt wird. Optionen: <br/>**`Yes`**- Zeigt das Kontrollkästchen _Angaben_.<br/>**`No`** - Zeigt das Kontrollkästchen _Angaben speichern_ nicht an und das persistente Cookie wird nur für Kunden verwendet, die es bereits haben. |
| [!UICONTROL "Remember Me" Default Value] | Website | Definiert den Standardstatus für das Kontrollkästchen _Angaben speichern_. |
| [!UICONTROL Clear Persistence on Log Out] | Website | Definiert, ob das persistente Cookie gelöscht wird, wenn sich ein Store-Kunde abmeldet. Unabhängig davon, wie diese Option konfiguriert ist, wird das persistente Cookie weiterhin verwendet, wenn sich ein Kunde nicht abmeldet, das Sitzungs-Cookie jedoch abläuft. |
| [!UICONTROL Persist Shopping Cart] | Website | Definiert, ob die Verwendung des persistenten Cookies Zugriff auf die Warenkorbdaten des entsprechenden Kontos bietet. Optionen: <br/>**`Yes`**oder **`No`**. |
| [!UICONTROL Persist Wish List] | Website | ![Adobe Commerce](/help/assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob der Status der Kundenwunschlisten beim Ende der Sitzung beibehalten wird. Optionen: <br/>**`Yes`**- Der Inhalt der Wunschliste wird am Ende der Sitzung gespeichert.<br/>**`No`** - Die Wunschliste wird am Ende der Sitzung nicht gespeichert. |
| [!UICONTROL Persist Recently Ordered Items] | Website | ![Adobe Commerce](/help/assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob der Status der zuletzt bestellten Artikel beim Sitzungsende gespeichert wird. Optionen: <br/>**`Yes`**oder **`No`**. |
| [!UICONTROL Persist Currently Compared Products] | Website | ![Adobe Commerce](/help/assets/adobe-logo.svg) (nur Adobe Commerce) Legt fest, ob der Status der aktuell verglichenen Produkte beibehalten wird, wenn die Sitzung beendet wird. Optionen: <br/>**`Yes`**oder **`No`**. |
| [!UICONTROL Persist Comparison History] | Website | ![Adobe Commerce](/help/assets/adobe-logo.svg) (nur Adobe Commerce) Legt fest, ob der Status des Vergleichsverlaufs beim Ende der Sitzung beibehalten wird. Optionen: <br/>**`Yes`**oder **`No`**. |
| [!UICONTROL Persist Recently Viewed Products] | Website | ![Adobe Commerce](/help/assets/adobe-logo.svg) (nur Adobe Commerce) Legt fest, ob der Status der zuletzt angezeigten Produkte beim Beenden der Sitzung beibehalten wird. Optionen: <br/>**`Yes`**oder **`No`**. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Website | ![Adobe Commerce](/help/assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob der Status der Gruppenmitgliedschaft und die Segmentierungskriterien der Kundinnen und Kunden beim Ende der Sitzung beibehalten werden. Optionen: <br/>**`Yes`**- Der Status der Gruppenmitgliedschaft und der Segmentierungsdaten des Kunden werden gespeichert, wenn die Sitzung beendet wird.<br/>**`No`** - Der Status der Gruppenmitgliedschaft und der Segmentierungsdaten des Kunden werden zum Ende der Sitzung nicht gespeichert. |

{style="table-layout:auto"}
