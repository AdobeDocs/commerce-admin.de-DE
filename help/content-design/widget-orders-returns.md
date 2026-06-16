---
title: Widget „Bestellungen und Rückgaben“
description: Erfahren Sie, wie Sie mit dem Widget Bestellungen und Rücksendungen Kunden die Möglichkeit geben, den Status ihrer Bestellungen zu überprüfen, Rechnungen zu drucken und Sendungen zu verfolgen.
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/jWpFWPBwvKr5EnMXdV5-3zAqagGuzPrvOL6-gMiEw-M
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 382
ht-degree: 0%

---

# Widget „Bestellungen und Rückgaben“

Das Widget _Bestellungen und Rücksendungen_ bietet Gästen die Möglichkeit, den Status ihrer Bestellungen zu überprüfen, Rechnungen zu drucken und Sendungen zu verfolgen. Wenn das Widget zur Storefront hinzugefügt wird, ist es nur für Gäste und für Kunden sichtbar, die nicht bei ihren Konten angemeldet sind. Sie können Bestellungen finden, indem Sie die Bestell-ID, den Nachnamen der Rechnungsstellung und entweder die E-Mail-Adresse oder die Postleitzahl angeben.

![Widget „Bestellungen und Rückgaben“ in der Seitenleiste der Storefront](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## Das Widget „Bestellungen und Rückgaben“ in der Storefront

1. Der Kunde kann die Option **[!UICONTROL Find Order By]** verwenden, um einen der folgenden Parameter für die Suche der Bestellung auszuwählen:

   - E-Mail-Adresse
   - Postleitzahl

1. Der Kunde gibt den **[!UICONTROL Order ID]** und die **[!UICONTROL Billing Last Name]** ein.

1. Gibt entweder die **[!UICONTROL Email Address]** oder die **[!UICONTROL ZIP Code]** ein, die mit der Bestellung verknüpft sind.

1. Klicks **[!UICONTROL Search]**, um die Bestellung abzurufen.

   ![Bestellinformationen werden in der Storefront angezeigt](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## Einrichten des Widgets „Bestellungen und Rückgaben“

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Widget]**.

1. Gehen Sie im Abschnitt _[!UICONTROL Settings]_wie folgt vor:

   - Legen Sie **[!UICONTROL Type]** auf `Orders and Returns` fest.

   - Wählen Sie die **[!UICONTROL Design Theme]** aus, die vom Store verwendet wird.

1. Klicken Sie auf **[!UICONTROL Continue]**.

1. Gehen Sie im Abschnitt _[!UICONTROL Storefront Properties]_wie folgt vor:

   - Geben Sie **[!UICONTROL Widget Title]** einen beschreibenden Titel für das Widget ein.

     Dieser Titel ist nur von der Administratorin bzw. dem Administrator sichtbar.

   - Wählen Sie **[!UICONTROL Assign to Store Views]** die Store-Ansichten aus, in denen das Widget sichtbar ist.

     Sie können eine bestimmte Shop-Ansicht oder `All Store Views` auswählen. Halten Sie zum Auswählen mehrerer Ansichten die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken Sie auf die einzelnen Optionen.

   - (Optional) Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der dieses Element zusammen mit anderen im selben Teil der Seite angezeigt wird. (`0` = First, `1` = Second, `3` = Third usw.)

1. Klicken Sie im Abschnitt _[!UICONTROL Layout Updates]_auf **[!UICONTROL Add Layout Update]**und führen Sie folgende Schritte aus:

   - Legen Sie **[!UICONTROL Display On]** auf den Seitentyp fest, auf dem das Widget angezeigt werden soll.

   - Um zu bestimmen, wo das Widget auf der Seite angezeigt wird, füllen Sie die restlichen Informationen zur Layout-Aktualisierung aus.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link in der Nachricht oben auf der Seite und folgen Sie den Anweisungen.
