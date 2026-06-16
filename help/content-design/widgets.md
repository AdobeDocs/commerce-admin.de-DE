---
title: Widgets
description: Erfahren Sie mehr über Widgets, die ein Code-Fragment bereitstellen, mit dem Sie eine breite Palette von Inhalten anzeigen und bei bestimmten Blockreferenzen in Ihrem Store platzieren können.
exl-id: 993ba2ca-a8de-4f7e-8cab-7ba7d16eebe7
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/ov5Wt8dIf--1UoXqFtv-NiAaEVL97UaQodxU4bGe8zo
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 671
ht-degree: 0%

---

# Widgets

Ein Widget ist ein Code-Fragment, mit dem eine breite Palette von Inhalten angezeigt und an bestimmten Blockreferenzen in Ihrem Store platziert werden kann. Viele Widgets zeigen dynamische Echtzeitdaten an und bieten Ihren Kunden Möglichkeiten zur Interaktion mit Ihrem Geschäft. Das Widget-Tool erleichtert das Platzieren eines Widgets innerhalb vorhandener Inhalte, z. B. Blöcke mit Bildern und Text, und interaktive Elemente an den meisten Stellen in Ihrem Store.

Sie können Widgets verwenden, um Landingpages für Marketing-Kampagnen zu erstellen und an bestimmten Stellen im gesamten Store Werbeinhalte anzuzeigen. Widgets können auch verwendet werden, um interaktive Elemente und Aktionsblöcke für externe Überprüfungssysteme, Videochats, Abstimmungs- und Abonnementformulare hinzuzufügen oder Navigationselemente für Tag-Clouds und Bild-Regler bereitzustellen.

{{$include /help/_includes/directives-caution.md}}

![Widget „Neue Produktliste“](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## Widget-Typen

Beim [Erstellen eines Widgets](widget-create.md) müssen Sie den Typ festlegen. Dieser Typ bestimmt, wie das Widget funktioniert.

| Typ | Beschreibung |
|--- |--- |
| [!UICONTROL CMS Hierarchy Node Link] | Verwenden Sie diese Option, um einen Link zu einem bestimmten Knoten in der Seitenhierarchie anzuzeigen, der in andere Inhalte integriert werden kann. |
| [!UICONTROL CMS Page Link] | Verwenden Sie diese Option, um benutzerdefinierten Text und einen Titel anzugeben, der auf eine bestimmte CMS-Seite verweist. Wenn der Link vollständig ist, kann er auf Inhaltsseiten und -blöcken verwendet werden. |
| [!UICONTROL CMS Static Block] | Verwenden Sie diese Option, um einen Inhaltsblock an einer bestimmten Position auf einer Seite anzuzeigen. |
| [!UICONTROL Catalog Category Link] | Verwenden Sie diese Option, um entweder einen Inline- oder einen Block-Stil-Link zu einer ausgewählten Katalogkategorie anzuzeigen. Wenn der Link vollständig ist, kann er auf Inhaltsseiten und -blöcken verwendet werden. |
| [!UICONTROL Catalog Events Carousel] | Verwenden Sie diese Option, um eine Liste bevorstehender Katalogereignisse anzuzeigen. |
| [!UICONTROL Catalog New Products List] | Verwenden Sie diese Option, um einen Block von Produkten anzuzeigen, die während der im Produktdatensatz angegebenen Zeit als neu gekennzeichnet wurden. |
| [!UICONTROL Catalog Product Link] | Verwenden Sie diese Option, um entweder einen Inline- oder einen Block-Stil-Link zu einem ausgewählten Katalogprodukt anzuzeigen. Wenn der Link vollständig ist, kann er auf Inhaltsseiten und -blöcken verwendet werden. |
| [!UICONTROL Catalog Products List] | Verwenden Sie diese Option, um eine Liste der Produkte aus dem Katalog anzuzeigen. |
| [!UICONTROL Dynamic Blocks Rotator] | Verwenden Sie diese Option, um einen einzelnen dynamischen Block oder eine Reihe dynamischer Blöcke in einer Reihe, zufälligen Reihenfolge oder gemischt anzuzeigen. Der dynamische Block kann durch eine Preisregel ausgelöst und auf einer bestimmten Seite und Position platziert oder so konfiguriert werden, dass er auf allen Seiten angezeigt wird. |
| [!UICONTROL Gift Registry Search] | Verwenden Sie diese Option, um Käufern die Möglichkeit zu geben, nach öffentlichen Geschenkregistern anhand des Namens oder der Registrierungs-ID zu suchen. |
| [!UICONTROL Order by SKU] | Bestellung nach SKU kann im Shop angezeigt werden, um es allen Käufern zu erleichtern, oder nur bestimmten Kundengruppen zur Verfügung gestellt werden. Käufer können entweder die SKU- und Mengeninformationen direkt in den Block „Bestellung nach SKU“ eingeben oder eine CSV-Datei von ihrem Kundenkonto hochladen. |
| [!UICONTROL Orders and Returns] | Verwenden Sie diese Option, um Gästen die Möglichkeit zu geben, den Status ihrer Bestellungen zu überprüfen und Anfragen zur Rücksendung von Waren einzureichen. Das Widget wird nur für Gäste und Kunden angezeigt, die nicht bei ihren Konten angemeldet sind. |
| [!UICONTROL Recently Compared Products] | Zeigt den Block der kürzlich verglichenen Produkte an. Sie können die Anzahl der eingeschlossenen Produkte angeben und sie als Liste oder Produktraster formatieren. |
| [!UICONTROL Recently Viewed Products] | Verwenden Sie diese Option, um den Block der zuletzt angezeigten Produkte anzuzeigen. Sie können die Anzahl der eingeschlossenen Produkte angeben und sie als Liste oder Produktraster formatieren. Das Widget zeigt möglicherweise keine Preisaktualisierungen in Echtzeit an. Der Käufer muss auf ein Produkt klicken, um die aktuellen Preise auf seiner Produktseite anzuzeigen. |
| [!UICONTROL Wish List Search] | Verwenden Sie diese Option, um einem Kunden die Möglichkeit zu geben, anhand des Namens oder der E-Mail-Adresse des Besitzers der Wunschliste nach öffentlich verfügbaren Wunschlisten zu suchen. Store-Kunden können Wunschlisten finden, die zu anderen Kunden gehören, sie anzeigen und Produkte von ihnen bestellen oder die Produkte zu ihren eigenen Wunschlisten hinzufügen. |

{style="table-layout:auto"}

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
