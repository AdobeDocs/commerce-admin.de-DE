---
title: Kategorieberechtigungen
description: Erfahren Sie, wie Sie mithilfe von Kategorien die Anzeige von Produktpreisen steuern, bestimmen können, welche Kundengruppen Produkte zum Warenkorb hinzufügen können, und die Landingpage angeben.
exl-id: d80a0545-918e-4c08-9f37-4aa3cd7771f4
feature: Catalog Management, Categories, Customers, Configuration
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 0%

---

# Kategorieberechtigungen

{{ee-feature}}

Der Kategoriezugriff kann auf bestimmte Kundengruppen beschränkt oder vollständig eingeschränkt sein. Sie können die Anzeige von Produktpreisen steuern, festlegen, welche Kundengruppen Produkte zum Warenkorb hinzufügen können, und die Landingpage festlegen.

>[!NOTE]
>
>Kategorieberechtigungen haben einen globalen Umfang. Wenn diese Option aktiviert ist, wird der Zugriff auf jede Kategorie anhand der individuellen Berechtigungen eingeschränkt. Standardmäßig sind Kategorieberechtigungen nicht aktiviert.

Wenn Sie beispielsweise nur an Großhandelskunden verkaufen, können Sie jedem erlauben, den Katalog zu durchsuchen, aber Preise anzuzeigen und Käufe nur für Käufer in der Kundengruppe _Großhandel_ zuzulassen. Im folgenden Beispiel haben nur angemeldete Benutzer Zugriff auf die Kategorie „Sammlungen“. Für Gäste erscheint die Option „Sammlungen“ nicht im Hauptmenü.

![Angemeldete Benutzer sehen die Kategorie „Sammlungen“](./assets/storefront-category-permissions-logged-in.png){width="600" zoomable="yes"}

Wenn diese Option aktiviert ist, wird auf der Kategorieseite ein neuer _[!UICONTROL Category Permissions]_-Abschnitt angezeigt, in dem Sie den erforderlichen Zugriff auf jede Kategorie anwenden können. Sie können jeder Kategorie mehrere Berechtigungsregeln für verschiedene Websites und Kundengruppen hinzufügen.

## Schritt 1: Kategorieberechtigungen konfigurieren

>[!IMPORTANT]
>
>Alle vorhandenen [Gruppenberechtigungseinstellungen](../configuration-reference/catalog/catalog.md#category-permissions) werden von **_allen_** Kategorien im Katalog ignoriert, wenn die **_[!UICONTROL Shared Catalog]_** aktiviert ist. [!UICONTROL Shared Catalog] steuert alle Kategorieberechtigungen im Katalog vollständig, wenn er aktiviert ist.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie darunter **[!UICONTROL Catalog]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Category Permissions]** .

   ![Kategorieberechtigungen](../configuration-reference/catalog/assets/catalog-category-permissions.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Optionen finden Sie unter [Kategorieberechtigungen](../configuration-reference/catalog/catalog.md#category-permissions) in _Konfigurationsreferenz_.

1. Legen Sie **[!UICONTROL Enable]** auf `Yes` fest.

1. Füllen Sie die anderen Optionen entsprechend dem aus, was Sie für Ihren Store zulassen oder einschränken möchten (siehe folgende Abschnitte).

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link **[!UICONTROL Cache Management]** in der Systemmeldung und befolgen Sie die Anweisungen zum Aktualisieren des Caches.

### [!UICONTROL Allow Browsing Category]

Diese Option gilt für alle Kategorien auf der [Website](../getting-started/websites-stores-views.md).

Gehen Sie wie folgt vor, um Mitgliedern **_bestimmten Kundengruppe_** das Durchsuchen von Kategorieprodukten zu ermöglichen:

1. Legen Sie **[!UICONTROL Allow Browsing Category]** auf `Specified Customer Groups` fest.

1. Wählen Sie im Feld **[!UICONTROL Customer Groups]** jede Gruppe aus, die Produkte in der Kategorie durchsuchen darf.

   Halten Sie zum Auswählen mehrerer Gruppen die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt, während Sie auf die einzelnen Gruppen klicken.

   ![Erlauben Sie das Browsen nach Großhandels-Kundengruppe](./assets/category-permissions-allow-browsing-customer-groups.png){width="600" zoomable="yes"}

Gehen **_wie folgt vor, um den Zugriff auf eine_** einzuschränken und zu ihr umzuleiten:

1. Legen Sie **[!UICONTROL Allow Browsing Category]** auf `No, Redirect to Landing Page` fest.

1. Wählen Sie die **[!UICONTROL Landing Page]** aus, zu der Besucher umgeleitet werden.

   ![Zur Startseite umleiten](./assets/category-permissions-browse-category-landing-page.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Obwohl die _[!UICONTROL Allow Browsing Category]_&#x200B;Einstellung für alle Kategorien auf der Website gilt, können Sie für jede Shop-Ansicht eine andere Landingpage konfigurieren.

### [!UICONTROL Display Product Prices]

Diese Option gilt für alle Kategorien auf der [Website](../getting-started/websites-stores-views.md).

Gehen Sie wie folgt vor **_um den Preis von Produkten in der Kategorie nur Mitgliedern_** bestimmter Kundengruppen“ anzuzeigen:

1. Legen Sie **[!UICONTROL Display Product Prices]** auf `Yes, for Specified Customer Groups` fest.

1. Wählen Sie im Feld **[!UICONTROL Customer Groups]** jede Gruppe aus, für die der Preis der Produkte in der Kategorie angezeigt werden darf.

   Halten Sie zum Auswählen mehrerer Gruppen die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt, während Sie auf die einzelnen Gruppen klicken.)

   ![Nur die Großhandelskunden-Gruppe kann Preise sehen](./assets/category-permissions-price-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Allow Adding to Cart]

Diese Option gilt für alle Kategorien auf der [Website](../getting-started/websites-stores-views.md).

Gehen Sie wie folgt vor, um **_Mitgliedern_** bestimmter Kundengruppen“ zu ermöglichen, Kategorieprodukte in den Warenkorb zu legen:

1. Legen Sie **[!UICONTROL Allow Adding to Cart]** auf `Yes, for Specified Customer Groups` fest.

1. Wählen Sie im Feld **[!UICONTROL Customer Groups]** jede Gruppe aus, die Produkte aus der Kategorie zum Warenkorb hinzufügen darf.

   Halten Sie zum Auswählen mehrerer Gruppen die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt, während Sie auf die einzelnen Gruppen klicken.

   ![Nur die Großhandelskunden-Gruppe kann ein Produkt in den Warenkorb legen](./assets/category-permissions-cart-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Disallow Catalog Search]

Legen Sie diese Option fest, um zu verhindern, dass Mitglieder einer bestimmten Kundengruppe die Katalogsuche verwenden. Sie gilt für alle Kategorien auf der [Website](../getting-started/websites-stores-views.md).

- Um **_nur angemeldete Kunden) die_** Katalogsuche zuzulassen, wählen Sie `NOT LOGGED IN` aus.

- Um zu ermöglichen **_dass (nur bestimmte Kundengruppen_** die Katalogsuche verwenden können, wählen Sie jede Gruppe aus, die von der Verwendung der Kategoriesuche ausgeschlossen werden soll.

  Halten Sie zum Auswählen mehrerer Gruppen die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt, während Sie auf die einzelnen Gruppen klicken.

  ![Katalogsuche nicht zulässig für allgemeine Kundengruppe](./assets/category-permissions-disallow-category-search.png){width="600" zoomable="yes"}

## Schritt 2: Kategorieberechtigungen anwenden

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie in der Kategoriebaum die Zielkategorie aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Category Permissions]** auf der Seite und führen Sie folgende Schritte aus:

   - Um eine Berechtigungsregel zu erstellen, klicken Sie auf **[!UICONTROL New Permission]**.

     ![Abschnitt „Kategorieberechtigungen“](./assets/category-permissions-section-admin.png){width="600" zoomable="yes"}

   - Wählen Sie die entsprechenden **[!UICONTROL Website]** und **[!UICONTROL Customer Group]** aus.

   - Legen Sie die individuellen Berechtigungen nach Bedarf fest.

   >[!NOTE]
   >
   >Wenn für eine übergeordnete Kategorie die Berechtigung `Browsing Category` = `Deny` festgelegt ist, wird sie nicht im Breadcrumb[Protokoll &#x200B;](navigation-breadcrumb-trail.md) untergeordneten Kategorieseite angezeigt.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

>[!NOTE]
>
>Wenn **_Zulassen_**-Berechtigungen für die `Root Category` festgelegt sind, werden diese Berechtigungen automatisch auf alle Unterkategorien und alle Produkte innerhalb der `Catalog` angewendet. Wenn ein Produkt mehreren Kategorien zugewiesen ist und über **_Zulassen_**-Berechtigungen für mindestens eine Kategorie verfügt, verfügt es automatisch über dieselben **_Zulassen_**-Berechtigungen für alle zugewiesenen Kategorien.
