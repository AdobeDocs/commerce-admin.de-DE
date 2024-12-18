---
title: Katalogpreisregeln
description: Erfahren Sie mehr über Katalogpreisregeln, mit denen Käufern Produkte zu einem ermäßigten Preis basierend auf einer Reihe definierter Bedingungen angeboten werden können.
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Katalogpreisregeln

Katalogpreisregeln können verwendet werden, um Käufern Produkte zu einem reduzierten Preis anzubieten, basierend auf einer Reihe definierter Bedingungen. Katalogpreisregeln verwenden keine [Couponcodes](price-rules-cart-coupon.md), da sie ausgelöst werden, bevor ein Produkt in den Warenkorb gelegt wird.

Sie können beispielsweise die Bedingungen für eine Preisregel definieren und festlegen, die, wenn sie erfüllt ist, automatisch Produkte mit einem Sonderpreis oder einem Sonderpreis anzeigt. Definierte Regeleigenschaften können Kundengruppen, Produktkategorien, einen Rabattbetrag oder -prozentsatz, die Produktfarbe, die Produktgröße oder fast jedes Produktattribut umfassen, das in Ihrem Geschäft eingerichtet wurde. Sie können Start- und Enddaten für eine Preisregel festlegen, die automatisch an den in der Regel definierten Daten eine Promotion startet und stoppt. Die Eigenschaften einer gespeicherten Regel können bei Bedarf aktualisiert oder geändert werden.

- ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Sie können eine definierte Regel auch mit einem [dynamischen Block) verknüpfen](../content-design/dynamic-blocks.md) um das Ereignis oder Produkt in Ihrem Store zu bewerben.

- ![Magento Open Source ](../assets/open-source.svg) (nur Magento Open Source) Für wiederkehrende Promotions können Sie eine gespeicherte Regel jedes Mal manuell auf den Status _Aktiv_ oder _Inaktiv_ setzen, wenn Sie die Promotion ausführen möchten.

## Zugriff auf Katalogpreisregeln

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

   ![Katalogpreisregeln](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. Aktualisieren von Eigenschaften für eine Regel:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Klicken Sie auf **[!UICONTROL Edit]** , um die Seite _Regelinformationen_ anzuzeigen.

   - ![Magento Open Source ](../assets/open-source.svg) (nur Magento Open Source) Klicken Sie auf die Regel in der Liste, um die Seite mit den Regelinformationen anzuzeigen.

   Dort können Sie die Einstellungen für die Regel ändern (ähnlich wie [Erstellen einer Regel](price-rules-catalog-create.md)).

## Filteroptionen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Geben Sie einen Text ein, um die Liste nach einer bestimmten Regel-ID-Nummer zu filtern. |
| [!UICONTROL Rule] | Geben Sie einen Text ein, um die Liste nach dem Regelnamen zu filtern, der bei der Erstellung der Regel definiert wurde. |
| [!UICONTROL Priority] | ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Geben Sie Text in dieses Feld ein, um die Liste nach der für eine Regel definierten Priorität zu filtern. |
| [!UICONTROL Web Site] | ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Verwenden Sie diese Option, um die Liste nach für eine Regel definierten Websites zu filtern. |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Klicken Sie auf **[!UICONTROL Edit]**, um die Regelinformationen anzuzeigen und die Regeleinstellungen zu aktualisieren (ähnlich wie beim Erstellen einer Regel). |
| [!UICONTROL Start] | ![Magento Open Source ](../assets/open-source.svg) (nur Magento Open Source) Verwenden Sie die dynamischen Kalenderfelder (An: und Von:), um die Liste nach dem Startdatum für die Regel zu filtern, wie es bei der Erstellung der Regel definiert wurde. |
| [!UICONTROL End] | ![Magento Open Source ](../assets/open-source.svg) (nur Magento Open Source) Verwenden Sie die dynamischen Kalenderfelder (An: und Von:), um die Liste nach dem Enddatum für die Regel zu filtern, wie es bei der Erstellung der Regel definiert wurde. |
| [!UICONTROL Status] | ![Magento Open Source ](../assets/open-source.svg) (nur Magento Open Source) Verwenden Sie diese Option, um die Liste nach Regelstatus (`Active` oder `Inactive`) zu filtern. |

{style="table-layout:auto"}
