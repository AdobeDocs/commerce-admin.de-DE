---
title: Wunschlisten
description: Erfahren Sie mehr über Wunschlisten und wie sie das Einkaufserlebnis verbessern und mehr Verkäufe fördern können.
exl-id: 42c73566-0e32-4639-9fa2-d504fa161ebc
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/neTWJnIbZcaAAMQiX-SV82fTyvOGEeNLhBfxDUh4Ulk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 395
ht-degree: 0%

---

# Wunschlisten

Eine Wunschliste ist eine Liste von Produkten, die ein registrierter Kunde mit Freunden teilen oder speichern kann, um sie später in den Warenkorb zu legen. Wenn Wunschlisten aktiviert sind, wird der Link Zur Wunschliste hinzufügen auf den Kategorie- und Produktseiten jedes Produkts im Store angezeigt. Je nach Design kann es sich um einen Text-Link oder ein Grafikbild handeln.

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce unterstützt die Verwendung mehrerer Wunschlisten pro Kundenkonto.

![Magento Open Source](../assets/open-source.svg) Magento Open Source unterstützt die Verwendung einer einzigen Wunschliste pro Kundenkonto.

Freigegebene Wunschlisten werden von einer Store-E-Mail-Adresse gesendet, aber der Textkörper der Nachricht enthält eine personalisierte Anmerkung des Kunden. Sie können die E-Mail-Vorlage anpassen, die bei der Freigabe von Wunschlisten verwendet wird, und den Store-Kontakt auswählen, der als Absender angezeigt wird.

Wunschlisten können über das Dashboard des [Kundenkontos“ aktualisiert ](../customers/account-dashboard.md). Artikel können vom Kunden oder vom Store-Administrator zwischen der Wunschliste und dem Warenkorb hinzugefügt oder übertragen werden.

![Beispiel-Storefront - Meine Wunschliste](./assets/storefront-my-wishlist.png){width="700" zoomable="yes"}

Wenn ein Produkt mit mehreren Optionen zu einer Wunschliste hinzugefügt wird, werden alle Optionen, die vom Kunden ausgewählt wurden, in die Beschreibung des Wunschlistenelements aufgenommen. Wenn der Kunde beispielsweise dasselbe Paar Schuhe in drei verschiedenen Farben hinzufügt, wird jedes Paar als separater Wunschlistenpunkt angezeigt. Wenn der Kunde dasselbe Produkt jedoch mehrmals zur Wunschliste hinzufügt, wird das Produkt nur einmal angezeigt, jedoch mit der auf der Produktseite ausgewählten Menge.

## Wunschliste Unterstützung in der Admin

Kunden können [Wunschlisten verwalten](wishlist-storefront.md) indem sie sich bei ihren Konten in der Storefront anmelden. Als Store-Administrator können Sie auch Kundenwunschlisten über den Administrator verwalten.

**_So aktualisieren Sie Wunschlistenelemente vom Administrator:_**

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden in der Liste und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Wählen Sie im linken Bereich die Option **[!UICONTROL Wish List]** und suchen Sie das Element, das in der Liste bearbeitet werden soll.

   Alle für das Produkt ausgewählten Optionen werden unter dem Produktnamen angezeigt.

   ![Commerce Admin - Kunden-Wunschliste](./assets/customer-wishlist-edit-admin.png){width="600" zoomable="yes"}

1. Gehen Sie wie folgt vor, um die Produktoptionen zu bearbeiten:

   - Klicken Sie in der Spalte **[!UICONTROL Action]** auf **[!UICONTROL Configure]**.

   - Aktualisieren Sie auf der Produktseite die Optionen und **[!UICONTROL Quantity]** nach Bedarf.

   - Klicken Sie auf **[!UICONTROL OK]**.

1. Klicken Sie abschließend auf **[!UICONTROL Save Customer]** oder **[!UICONTROL Save and Continue Edit]**.
