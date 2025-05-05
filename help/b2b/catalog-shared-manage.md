---
title: Verwalten freigegebener Kataloge
description: Erfahren Sie mehr über die Informationen und Tools, die auf der Seite Freigegebene Kataloge verfügbar sind.
exl-id: a01ac292-240d-42e7-b4c9-2982f293c521
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# Verwalten freigegebener Kataloge

Die Seite _[!UICONTROL Shared Catalogs]_&#x200B;bietet Zugriff auf die Tools, die zum Verwalten Ihrer freigegebenen Kataloge erforderlich sind. Die Seite ähnelt dem standardmäßigen Admin Workspace mit Filtern und Aktionssteuerelementen. Im Raster werden alle freigegebenen Kataloge aufgelistet, einschließlich des standardmäßigen öffentlichen freigegebenen Katalogs und aller benutzerdefinierten Kataloge, die Sie eingerichtet haben.

## Aktualisieren der Produktauswahl

Die Auswahl von Produkten in einem freigegebenen Katalog kann einfach über die Spalte _[!UICONTROL Action]_&#x200B;des Rasters Freigegebene Kataloge aktualisiert werden. Die von Ihnen vorgenommenen Änderungen sind für Mitglieder aller zugehörigen Unternehmenskonten sichtbar. Der Prozess ist im Wesentlichen der gleiche wie die Auswahl von Produkten für eine neue [Katalogstruktur](catalog-shared-pricing-structure.md) mit der Ausnahme, dass der Umfang der Konfiguration nicht geändert werden kann.

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Wechseln Sie für den freigegebenen Katalog im Raster zur Spalte **[!UICONTROL Action]** und wählen Sie **[!UICONTROL Set Pricing and Structure]** aus.

   ![Freigegebenes Katalograster und Aktionsmenü](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. Befolgen Sie die Anweisungen in [Schritt 2: Wählen Sie Produkte](catalog-shared-pricing-structure.md#step-2-choose-the-products).

   Sie können das erste Element überspringen, da der Umfang eines freigegebenen Katalogs nach dem ersten Speichern nicht mehr geändert werden kann.

Wenn Sie mit einem bestimmten Produkt arbeiten, werden im Abschnitt _[!UICONTROL Products In Shared Catalog]_&#x200B;alle freigegebenen Kataloge aufgelistet, in denen das Produkt verfügbar ist. Weitere Informationen finden Sie unter [Hinzufügen von Produkten zu einem freigegebenen Katalog](catalog-shared-product-add.md).

![Produkt in freigegebenen Katalogen](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

## Benutzerdefinierte Preise aktualisieren

Die benutzerdefinierten Preise von Produkten in einem freigegebenen Katalog können einfach über die Spalte Aktion des Rasters Freigegebene Kataloge aktualisiert werden. Die von Ihnen vorgenommenen Änderungen sind für Mitglieder des zugehörigen Unternehmens oder der Kundengruppe in der Storefront sichtbar. Der Prozess ist im Wesentlichen der gleiche wie das Festlegen benutzerdefinierter Preise für einen neuen [freigegebenen Katalog](catalog-shared-pricing-structure.md) mit der Ausnahme, dass der Umfang der Konfiguration nicht geändert werden kann.

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Wechseln Sie für den freigegebenen Katalog im Raster, den Sie aktualisieren möchten, zur Spalte **[!UICONTROL Action]** und wählen Sie **[!UICONTROL Set Pricing and Structure]** aus.

1. Klicken Sie auf der Seite _[!UICONTROL Catalog Structure]_&#x200B;auf **[!UICONTROL Configure]**&#x200B;und führen Sie einen der folgenden Schritte aus:

   - Klicken Sie in der Fortschrittsanzeige oben auf der Seite auf **[!UICONTROL Pricing]**.
   - Klicken Sie oben rechts auf **[!UICONTROL Next]**.

1. Befolgen Sie die Anweisungen in [Schritt 3: Benutzerdefinierte Preise festlegen](catalog-shared-pricing-structure.md#step-3-set-custom-prices).

## Aktualisieren von Kategorieberechtigungen

[Kategorieberechtigungen](../catalog/category-permissions.md) werden für Produkte, die aus der Kategoriestruktur zu einem freigegebenen Katalog hinzugefügt werden, automatisch auf `Allow` festgelegt. Sie können die Berechtigungen später bei Bedarf anpassen oder zusätzliche Regeln erstellen.

>[!NOTE]
>
>**[B2B-Version 1.3.](release-notes.md#b2b-v130) und höher** - Wenn Sie einen freigegebenen Katalog erstellen, wird jede [Kategorieberechtigung](../catalog/category-permissions.md) für den Katalog auf `Allow` für die _[!UICONTROL Display Product Prices]_&#x200B;und&#x200B;_[!UICONTROL Add to Cart]_ für Kundengruppen festgelegt, denen dieser Zugriff in den Katalogberechtigungseinstellungen zugewiesen ist. Zuvor wurden diese Einstellungen automatisch auf `Deny` gesetzt, auch wenn die Katalogberechtigungen auf `Allow` gesetzt waren.

>[!IMPORTANT]
>
>Alle vorhandenen [Gruppenberechtigungseinstellungen](../configuration-reference/catalog/catalog.md#category-permissions) werden von **_allen_** Kategorien im Katalog ignoriert, wenn die **_[!UICONTROL Shared Catalog]_** aktiviert ist. [!UICONTROL Shared Catalog] steuert alle Kategorieberechtigungen im Katalog vollständig, wenn er aktiviert ist.

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie in der Kategoriestruktur die Kategorie der Produkte aus, die Sie aktualisieren möchten.

   Um alle Produkte einzubeziehen, wählen Sie die Kategorie der obersten Ebene in der Baumstruktur aus.

1. Scrollen Sie nach unten und erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Category Permissions]** .

1. Klicken Sie auf **[!UICONTROL New Permission]** und führen Sie folgende Schritte aus:

   ![Neue Berechtigung](./assets/category-permissions-new.png){width="600" zoomable="yes"}

   - Wählen Sie die **[!UICONTROL Customer Group]** aus, die dem freigegebenen Katalog entspricht, und ändern Sie die Berechtigungseinstellungen nach Bedarf.

     ![Kategorienberechtigungsregel](./assets/shared-catalog-category-permissions.png){width="600" zoomable="yes"}

   - Um eine Berechtigungsregel für eine andere Kundengruppe zu erstellen, klicken Sie auf **[!UICONTROL New Permissions]** und wiederholen Sie den Vorgang.

   - Um eine Berechtigungsregel zu löschen, klicken Sie auf das Symbol _Löschen_ ![Papierkorb](../assets/icon-delete-trashcan-solid.png).

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

## Aktualisieren der Katalogdetails

Die Detailinformationen eines freigegebenen Katalogs können einfach über die Spalte Aktion des Rasters Freigegebene Kataloge aktualisiert werden. Die von Ihnen vorgenommenen Änderungen werden in allen zugehörigen Unternehmenskonten übernommen.

![Allgemeine Einstellungen](./assets/shared-catalog-grid-general-settings.png){width="700" zoomable="yes"}

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Wechseln Sie für den freigegebenen Katalog, den Sie aktualisieren möchten, zur Spalte **[!UICONTROL Action]** und wählen Sie **[!UICONTROL General Settings]** aus.

   ![Katalogdetails](./assets/shared-catalog-update-details.png){width="600" zoomable="yes"}

1. Aktualisieren Sie die Katalogdetailinformationen nach Bedarf.

   - Wenn Sie den Namen eines freigegebenen Katalogs ändern, wird auch der Name der entsprechenden Kundengruppe geändert.
   - Durch Ändern des Katalogtyps von `Custom` in `Public` wird der vorhandene öffentliche Katalog in einen benutzerdefinierten Katalog konvertiert. Alle Unternehmen, die mit dem ursprünglichen öffentlichen Katalog verknüpft sind, werden dem Ersatz zugewiesen. Ein öffentlicher Katalog kann nicht in einen benutzerdefinierten Katalog konvertiert werden.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

## Seitenverweis für freigegebenen Katalog

### Schaltflächenleiste

| Schaltfläche | Beschreibung |
|--- |--- |
| [!UICONTROL Back] | Kehrt zur Seite Freigegebene Kataloge zurück, ohne den neuen freigegebenen Katalog zu speichern. |
| [!UICONTROL Delete] | Löscht den Katalog und weist alle zugehörigen Unternehmen und deren Mitglieder dem öffentlichen freigegebenen Katalog zu. |
| [!UICONTROL Reset] | Löscht das Formular von nicht gespeicherten Änderungen und stellt die ursprünglichen Katalogdetailinformationen wieder her. |
| [!UICONTROL Duplicate] | Erstellt eine [Duplikat des Katalogs](catalog-shared-create.md). Bei einem benutzerdefinierten Katalog das Preismodell und die Struktur des Originals, jedoch ohne die Unternehmensverknüpfungen. Wenn ein öffentlicher freigegebener Katalog dupliziert wird, ändert sich der Typ des doppelten Katalogs in `custom`. Eine entsprechende Kundengruppe wird ebenfalls mit demselben Namen wie der doppelte Katalog erstellt. Standardmäßig erhält ein doppelter Katalog den Namen _Duplikat_ des ursprünglichen Katalogs. |
| [!UICONTROL Save and Continue Edit] | Speichert alle Änderungen und lässt das Formular im Bearbeitungsmodus geöffnet. |
| [!UICONTROL Save] | Speichert Änderungen, schließt das Formular und kehrt zur Seite Freigegebene Kataloge zurück. |

{style="table-layout:auto"}

### Katalogdetails

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Name] | Identifiziert den freigegebenen Katalog innerhalb des Admin-Bereichs und in den Kundenkonten, in denen er verfügbar ist. Der Katalogname sollte beschreibend sein und nicht mehr als 32 Zeichen lang sein. Sie können nicht zwei freigegebene Kataloge mit demselben Namen haben. Maximal Zeichen: 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Gibt einen Katalog mit benutzerdefinierter Preisgestaltung an, der nur für die spezifischen Unternehmen verfügbar ist, denen er zugewiesen ist.<br/>**[!UICONTROL Public]**- Identifiziert den freigegebenen Katalog, der für alle Gastbesucher und für angemeldete Kunden verfügbar ist, die keiner Firma zugeordnet sind. Bei der Installation von Adobe Commerce B2B wird ein „standardmäßiger“ öffentlicher freigegebener Katalog erstellt, der jedoch vom Administrator konfiguriert werden muss. Es kann immer nur ein öffentlicher freigegebener Katalog vorhanden sein. |
| [!UICONTROL Customer Tax Class] | Bestimmt die Steuerklasse, die für Käufe aus dem Katalog verwendet wird. Die Optionen umfassen alle verfügbaren Steuerklassen. |
| [!UICONTROL Description] | Eine kurze Erläuterung der Verwendung des Katalogs. |

{style="table-layout:auto"}
