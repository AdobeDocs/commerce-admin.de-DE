---
title: Katalogpreisregeln
description: Erfahren Sie mehr über Katalogpreisregeln, die verwendet werden können, um Käufern Produkte zu einem ermäßigten Preis anzubieten, der auf einer Reihe definierter Bedingungen basiert.
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Katalogpreisregeln

Katalogpreisregeln können verwendet werden, um Käufern Produkte zu einem ermäßigten Preis anzubieten, der auf einer Reihe von definierten Bedingungen basiert. Katalogpreisregeln verwenden nicht [Coupon-Codes](price-rules-cart-coupon.md), da sie ausgelöst werden, bevor ein Produkt in den Warenkorb gelegt wird.

Sie können beispielsweise die Bedingungen für eine Preisregel definieren und festlegen, dass, wenn sie erfüllt ist, automatisch Produkte mit einem Sonderpreis oder einem Sonderpreis angezeigt werden. Definierte Regeleigenschaften können Kundengruppen, Produktkategorien, einen Rabattbetrag oder Prozentsatz, die Produktfarbe, die Produktgröße oder nahezu jedes in Ihrem Store eingerichtete Produktattribut umfassen. Sie können Start- und Enddaten für eine Preisregel festlegen, die eine Promotion automatisch an den in der Regel definierten Daten startet und stoppt. Die Eigenschaften einer gespeicherten Regel können bei Bedarf aktualisiert oder geändert werden.

- ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Sie können eine definierte Regel auch mit einer [dynamischer Block](../content-design/dynamic-blocks.md) , um die Veranstaltung oder das Produkt in Ihrem Geschäft zu bewerben.

- ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Bei wiederkehrenden Promotions können Sie eine gespeicherte Regel manuell auf _Aktiv_ oder _Inaaktiv_ jedes Mal, wenn Sie die Promotion ausführen möchten.

## Auf Katalogpreisregeln zugreifen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

   ![Katalogpreisregeln](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. Eigenschaften für eine Regel aktualisieren:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Klicken Sie auf **[!UICONTROL Edit]** , um _Regelinformationen_ Seite.

   - ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Klicken Sie auf die Regel in der Liste, um die Seite Regelinformationen anzuzeigen.

   Dort können Sie die Einstellungen für die Regel ändern (ähnlich wie [Erstellen einer Regel](price-rules-catalog-create.md)).

## Filteroptionen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Geben Sie Text ein, um die Liste nach einer bestimmten Regel-ID-Nummer zu filtern. |
| [!UICONTROL Rule] | Geben Sie Text ein, um die Liste anhand des bei der Regelerstellung definierten Regelnamens zu filtern. |
| [!UICONTROL Priority] | ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Geben Sie Text in dieses Feld ein, um die Liste nach der für eine Regel definierten Priorität zu filtern. |
| [!UICONTROL Web Site] | ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Mit dieser Option können Sie die Liste auf der Grundlage der für eine Regel definierten Websites filtern. |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Klicken Sie auf **[!UICONTROL Edit]** , um die Regelinformationen anzuzeigen und die Regeleinstellungen zu aktualisieren (ähnlich wie beim Erstellen einer Regel). |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Filtern Sie die Liste mithilfe der dynamischen Kalenderfelder (An: und Von:) nach dem Startdatum der Regel, das bei der Regelerstellung definiert wurde. |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Filtern Sie die Liste mithilfe der dynamischen Kalenderfelder (An: und Von:) nach dem Enddatum der Regel, das bei der Regelerstellung definiert wurde. |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Mit dieser Option können Sie die Liste nach Regelstatus filtern (`Active` oder `Inactive`). |

{style="table-layout:auto"}

## Fehlerbehebung bei Ressourcen

Hilfe zur Behebung von Problemen mit Katalogpreisregeln finden Sie in den folgenden Artikeln der Knowledge Base für Commerce-Support:

- [404 Fehler auf der Storefront, sobald die Zeitpläne der Katalogpreisregeln aktualisiert wurden](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/404-error-on-store-front-once-catalog-price-rule-schedules-update-is-performed.html)
- [Verbesserte Leistung der Produktseite mit verwandten Produkten und Zielregeln](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31791-magento-patch-improvement-for-product-page-with-related-products-and-target-rules.html)
- [Katalogpreisregeln funktionieren nicht](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-24201-magento-patch-catalog-price-rules-don-t-work.html)
- [GraphQL-Preisberechnungen](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33975-magento-patch-graphql-price-calculations.html)
