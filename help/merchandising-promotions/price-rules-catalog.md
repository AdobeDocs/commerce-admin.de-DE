---
title: Katalogpreisregeln
description: Erfahren Sie mehr über Katalogpreisregeln, die verwendet werden können, um Käufern Produkte zu einem ermäßigten Preis anzubieten, der auf einer Reihe definierter Bedingungen basiert.
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Katalogpreisregeln

Katalogpreisregeln können verwendet werden, um Käufern Produkte zu einem ermäßigten Preis anzubieten, der auf einer Reihe von definierten Bedingungen basiert. Katalogpreisregeln verwenden keine [Coupon-Codes](price-rules-cart-coupon.md), da sie ausgelöst werden, bevor ein Produkt in den Warenkorb gelegt wird.

Sie können beispielsweise die Bedingungen für eine Preisregel definieren und festlegen, dass, wenn sie erfüllt ist, automatisch Produkte mit einem Sonderpreis oder einem Sonderpreis angezeigt werden. Definierte Regeleigenschaften können Kundengruppen, Produktkategorien, einen Rabattbetrag oder Prozentsatz, die Produktfarbe, die Produktgröße oder nahezu jedes in Ihrem Store eingerichtete Produktattribut umfassen. Sie können Start- und Enddaten für eine Preisregel festlegen, die eine Promotion automatisch an den in der Regel definierten Daten startet und stoppt. Die Eigenschaften einer gespeicherten Regel können bei Bedarf aktualisiert oder geändert werden.

- ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Sie können eine definierte Regel auch mit einem [dynamischen Block](../content-design/dynamic-blocks.md) verknüpfen, um das Ereignis oder das Produkt in Ihrem Store zu bewerben.

- ![Magento Open Source](../assets/open-source.svg) (nur Magento Open Source) Bei wiederkehrenden Promotions können Sie eine gespeicherte Regel bei jedem Ausführen der Promotion manuell auf den Status _Aktiv_ oder _Inaktiv_ festlegen.

## Auf Katalogpreisregeln zugreifen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

   ![Katalogpreisregeln](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. Eigenschaften für eine Regel aktualisieren:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Klicken Sie auf **[!UICONTROL Edit]** , um die Seite _Regelinformationen_ anzuzeigen.

   - ![Magento Open Source](../assets/open-source.svg) (nur Magento Open Source) Klicken Sie auf die Regel in der Liste, um die Seite Regelinformationen anzuzeigen.

   Dort können Sie die Einstellungen für die Regel ändern (ähnlich wie beim [Erstellen einer Regel](price-rules-catalog-create.md)).

## Filteroptionen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Geben Sie Text ein, um die Liste nach einer bestimmten Regel-ID-Nummer zu filtern. |
| [!UICONTROL Rule] | Geben Sie Text ein, um die Liste anhand des bei der Regelerstellung definierten Regelnamens zu filtern. |
| [!UICONTROL Priority] | ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Geben Sie Text in dieses Feld ein, um die Liste anhand der für eine Regel definierten Priorität zu filtern. |
| [!UICONTROL Web Site] | ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Mit dieser Option können Sie die Liste auf der Grundlage der für eine Regel definierten Websites filtern. |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Klicken Sie auf **[!UICONTROL Edit]** , um die Regelinformationen anzuzeigen und die Regeleinstellungen zu aktualisieren (ähnlich wie beim Erstellen einer Regel). |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Verwenden Sie die dynamischen Kalenderfelder (An: und Von:), um die Liste nach dem Startdatum für die Regel zu filtern, das bei der Regelerstellung definiert wurde. |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Verwenden Sie die dynamischen Kalenderfelder (An: und Von:), um die Liste nach dem Enddatum der Regel zu filtern, das bei der Regelerstellung definiert wurde. |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (nur Magento Open Source) Mit dieser Option können Sie die Liste nach Regelstatus (`Active` oder `Inactive`) filtern. |

{style="table-layout:auto"}
