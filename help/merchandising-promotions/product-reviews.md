---
title: Produktbewertungen
description: Erfahren Sie, wie Produktbewertungen Ihren Shop verbessern und Ihren Produkten mehr Glaubwürdigkeit verleihen können.
exl-id: 82f96b24-626f-4b2d-be42-3d655d08dfda
feature: Merchandising, Products
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Produktbewertungen

Produktbewertungen tragen dazu bei, ein Gemeinschaftsgefühl aufzubauen, und werden als glaubwürdiger angesehen, als jedes Werbegeld kaufen kann. Tatsächlich geben einige Suchmaschinen Sites mit Produktbewertungen ein höheres Ranking als die ohne. Für diejenigen, die Ihre Site durch die Suche nach einem bestimmten Produkt finden, ist eine Produktbewertung im Wesentlichen die Landingpage Ihres Stores. Produktbewertungen helfen Kunden, Ihren Laden zu finden, sie bei der Stange zu halten und führen oft zum Verkauf.

Commerce enthält eine native Funktion zur Produktüberprüfung, die Sie über den Administrator verwalten können. Sie können auch eine Erweiterung aus der [Commerce Marketplace](../getting-started/commerce-marketplace.md) verwenden, um ein gehostetes Überprüfungsverwaltungssystem zu verwenden.

>[!NOTE]
>
>Die Versionen 2.4.0 bis 2.4.3 von Adobe Commerce und Magento Open Source enthielten die vom Yotpo-Anbieter entwickelte Erweiterung. Ab Version 2.4.4 ist diese Erweiterung nicht mehr im Bundle der Hauptversion enthalten und muss von der Commerce Marketplace installiert und aktualisiert werden. Der Marketplace bietet außerdem Zugriff auf die aktuelle Dokumentation, die vom Erweiterungsentwickler bereitgestellt wird.
>><br><br>
>>Wenn Sie die gebündelte Erweiterung aktiviert und konfiguriert haben, müssen Sie Ihre Datei „composer.json“ im Rahmen des Upgrade-Prozesses auf 2.4.4 aktualisieren, um zukünftige Erweiterungs-Updates zu verwalten. Siehe [Upgrade-Module](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) im _Upgrade-Handbuch_ für weitere Informationen.

## Produktbewertungen in der Storefront

Wenn die native Funktion für Produktbewertungen aktiviert ist, können Kunden für jedes Produkt in Ihrem Katalog Bewertungen schreiben. Bewertungen können über die Produktseite geschrieben werden, indem Sie auf Folgendes klicken:

- **Fügen Sie Ihre Bewertung** für Produkte mit vorhandenen Bewertungen hinzu.

- **Seien Sie der erste, der dieses Produkt bewertet** für Produkte ohne bestehende Bewertungen.

Auf der Registerkarte [!UICONTROL Reviews] werden alle aktuellen Überprüfungen und das Formular aufgelistet, das zum Senden einer Überprüfung verwendet wurde.

Ihre Konfiguration bestimmt, ob Kundinnen und Kunden ein Konto bei Ihrem Store eröffnen müssen, bevor sie Produktbewertungen schreiben, oder ob sie Bewertungen als Gäste senden können. Die Anforderung, dass Überprüfende ein Konto eröffnen müssen, verhindert anonyme Übermittlungen und verbessert die Qualität der Überprüfungen.

![Beispiel-Storefront - Fügen Sie Ihre Bewertung hinzu](./assets/storefront-review-this-product.png){width="700" zoomable="yes"}

Die Anzahl der Sterne gibt die Zufriedenheitsbewertung des Produkts an. Besucher können auf den Link klicken, um die Rezensionen zu lesen und ihre eigenen zu schreiben. Als Anreiz können Kunden Prämienpunkte für die Einreichung einer Bewertung erhalten. Wenn eine Überprüfung eingereicht wird, wird sie zur Moderation an den Administrator gesendet. Nach der Genehmigung wird die Überprüfung in Ihrem Store veröffentlicht.

![Beispiel-Storefront - Registerkarte „Überprüfungen“](./assets/storefront-reviews-tab.png){width="700" zoomable="yes"}

### [!UICONTROL My Product Reviews]

Im Abschnitt _[!UICONTROL My Product Reviews]_des Kundenkonto-Dashboards werden alle vom Kunden eingereichten und zur Veröffentlichung genehmigten Bewertungen aufgelistet. Jede Überprüfungszusammenfassung enthält das Datum, an dem die Überprüfung eingereicht wurde, Links zur Produktseite und Details zur Überprüfung.

![Meine Produktbewertungen](./assets/account-dashboard-my-product-reviews.png){width="700" zoomable="yes"}

1. In der Seitenleiste seines Kontos wählt der Kunde **[!UICONTROL My Product Reviews]** aus.

1. Um die vollständige Überprüfung anzuzeigen, klicken Sie auf **[!UICONTROL See Details]**.

   ![Details überprüfen](./assets/account-dashboard-my-product-reviews-details.png){width="700" zoomable="yes"}

## Produktüberprüfungsfunktionen aktivieren

Die Commerce-Produktüberprüfungsfunktion ist standardmäßig aktiviert.

>[!NOTE]
>
>Um diese Felder zum `No` und Deaktivieren von Commerce-Produktüberprüfungen festzulegen, müssen Sie die Kontrollkästchen **Systemwert verwenden** deaktivieren.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie darunter **[!UICONTROL Catalog]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Product Reviews]** .

   ![Katalogkonfiguration - Commerce-Produktbewertungen](../configuration-reference/catalog/assets/catalog-product-reviews.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Enabled]** auf `Yes` fest.

   Dies ist die Standardeinstellung, die Produktüberprüfungen ermöglicht.

1. Legen Sie **[!UICONTROL Allow Guests to Write Reviews]** auf `Yes` fest.

   Dies ist die Standardeinstellung, die bestimmt, ob Kunden ein Konto bei Ihrem Geschäft eröffnen müssen, um Produktbewertungen schreiben zu können.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Erstellen benutzerdefinierter Bewertungen

Mit den Commerce-Produktbewertungen können Kunden Bewertungen zuweisen, wenn sie eine Produktbewertung senden. Die Standardbewertungen sind Qualität, Preis und Wert. Darüber hinaus können Sie Ihre eigenen benutzerdefinierten Bewertungen hinzufügen. Die fünf Sterne, die auf Katalogseiten angezeigt werden, werden für jedes Produkt gemittelt.

![Beispiel-Storefront - Benutzerdefinierte Bewertungen](./assets/attribute-custom-ratings-review.png){width="700" zoomable="yes"}

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Rating]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add New Rating]**.

   ![Admin - Ratings](./assets/product-reviews-rating.png){width="700" zoomable="yes"}

1. Geben Sie im Abschnitt _[!UICONTROL Rating Title]_die **[!UICONTROL Default Value]**für die neue Bewertung ein.

   Geben Sie gegebenenfalls auch die Übersetzung für jede Shop-Ansicht ein.

   ![Einstellungen für Bewertungstitel](./assets/product-rating-title.png){width="600" zoomable="yes"}

1. Legen _im Abschnitt „Rating_ Sichtbarkeit“ **[!UICONTROL Visibility In]** auf die Store-Ansicht fest, in der die Bewertung verwendet werden soll.

   Um mehrere Store-Ansichten auszuwählen, halten Sie die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken Sie auf die einzelnen Elemente.

   >[!NOTE]
   >
   >Bewertungen sind nur sichtbar, wenn sie einer Store-Ansicht zugewiesen sind.

1. Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge dieser Bewertung zu bestimmen, wenn sie mit anderen aufgelistet wird.

1. Wenn Sie Ihre Bewertung auf der Storefront anzeigen möchten, aktivieren Sie das Kontrollkästchen **[!UICONTROL Is Active]** .

   ![Einstellungen für die Bewertungssichtbarkeit](./assets/product-rating-visibility.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Rating]**.

   Die durchschnittliche Bewertung für alle Bewertungen wird für jedes Produkt auf der Seite Katalogproduktraster angezeigt.

   ![Katalogseite](./assets/catalog-rating-page.png){width="700" zoomable="yes"}
