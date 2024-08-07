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

Die Seite &quot;_[!UICONTROL Shared Catalogs]_&quot; bietet Zugriff auf die Tools, die zur Verwaltung Ihrer freigegebenen Kataloge erforderlich sind. Die Seite ähnelt dem standardmäßigen Admin-Arbeitsbereich mit Filtern und Aktionssteuerelementen. Das Raster listet alle freigegebenen Kataloge auf, einschließlich des standardmäßigen öffentlichen freigegebenen Katalogs und aller benutzerdefinierten Kataloge, die Sie eingerichtet haben.

## Aktualisieren der Produktauswahl

Die Auswahl der Produkte in einem freigegebenen Katalog kann einfach über die Spalte &quot;_[!UICONTROL Action]_&quot;des freigegebenen Katalograds aktualisiert werden. Die Änderungen, die Sie vornehmen, sind für Mitglieder aller zugehörigen Unternehmenskonten sichtbar. Der Prozess entspricht im Wesentlichen der Auswahl von Produkten für eine neue [Katalogstruktur](catalog-shared-pricing-structure.md), allerdings kann der Umfang der Konfiguration nicht geändert werden.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Markieren Sie für den freigegebenen Katalog im Raster die Spalte **[!UICONTROL Action]** und wählen Sie **[!UICONTROL Set Pricing and Structure]** aus.

   ![Freigegebenes Katalograster und Aktionsmenü](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. Befolgen Sie die Anweisungen unter [Schritt 2: Produkte auswählen](catalog-shared-pricing-structure.md#step-2-choose-the-products).

   Sie können das erste Element überspringen, da der Umfang eines freigegebenen Katalogs nach dem ersten Speichern nicht mehr geändert werden kann.

Wenn Sie mit einem bestimmten Produkt arbeiten, werden im Abschnitt &quot;_[!UICONTROL Products In Shared Catalog]_&quot;alle freigegebenen Kataloge aufgelistet, in denen das Produkt verfügbar ist. Weitere Informationen finden Sie unter [Produkte zu einem freigegebenen Katalog hinzufügen](catalog-shared-product-add.md).

![Produkt in freigegebenen Katalogen](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

## Aktualisierung benutzerdefinierter Preise

Die benutzerdefinierten Preise für Produkte in einem beliebigen freigegebenen Katalog können einfach über die Spalte Aktion im Raster Gemeinsame Kataloge aktualisiert werden. Die Änderungen, die Sie vornehmen, sind für Mitglieder des zugehörigen Unternehmens oder der zugehörigen Kundengruppe in der Storefront sichtbar. Der Prozess entspricht im Wesentlichen dem Festlegen der benutzerdefinierten Preise für einen neuen [freigegebenen Katalog](catalog-shared-pricing-structure.md), allerdings kann der Umfang der Konfiguration nicht geändert werden.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Markieren Sie für den freigegebenen Katalog im Raster, den Sie aktualisieren möchten, die Spalte **[!UICONTROL Action]** und wählen Sie **[!UICONTROL Set Pricing and Structure]** aus.

1. Klicken Sie auf der Seite _[!UICONTROL Catalog Structure]_auf **[!UICONTROL Configure]**und führen Sie einen der folgenden Schritte aus:

   - Klicken Sie in der Fortschrittsanzeige oben auf der Seite auf **[!UICONTROL Pricing]**.
   - Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Next]**.

1. Befolgen Sie die Anweisungen in [Schritt 3: Festlegen benutzerdefinierter Preise](catalog-shared-pricing-structure.md#step-3-set-custom-prices).

## Aktualisieren von Kategorienberechtigungen

[Kategorieberechtigungen](../catalog/category-permissions.md) werden für Produkte, die aus dem Kategoriebaum zu einem freigegebenen Katalog hinzugefügt werden, automatisch auf `Allow` gesetzt. Sie können später die Berechtigungen anpassen oder bei Bedarf zusätzliche Regeln erstellen.

>[!NOTE]
>
>**[B2B-Version 1.3.0](release-notes.md#b2b-v130) und höher** - Wenn Sie einen freigegebenen Katalog erstellen, wird jede [Kategorieberechtigung](../catalog/category-permissions.md) für den Katalog auf `Allow` für die _[!UICONTROL Display Product Prices]_und auf_[!UICONTROL Add to Cart]_ für Kundengruppen festgelegt, denen dieser Zugriff in den Einstellungen für Katalogberechtigungen zugewiesen ist. Zuvor wurden diese Einstellungen automatisch auf `Deny` gesetzt, selbst wenn die Katalogberechtigungen auf `Allow` festgelegt waren.

>[!IMPORTANT]
>
>Alle vorhandenen [Gruppenberechtigungseinstellungen](../configuration-reference/catalog/catalog.md#category-permissions) werden von den Kategorien **_Alle_** im Katalog ignoriert, wenn die Funktion **_[!UICONTROL Shared Catalog]_** aktiviert ist. [!UICONTROL Shared Catalog] steuert alle Kategorieberechtigungen im Katalog vollständig, wenn sie aktiviert sind.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie im Kategoriebaum die Kategorie der Produkte aus, die Sie aktualisieren möchten.

   Um alle Produkte einzubeziehen, wählen Sie die Kategorie der obersten Ebene im Baum aus.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Category Permissions]** um den ![Erweiterungsselektor](../assets/icon-display-expand.png).

1. Klicken Sie auf **[!UICONTROL New Permission]** und führen Sie die folgenden Schritte aus:

   ![Neue Berechtigung](./assets/category-permissions-new.png){width="600" zoomable="yes"}

   - Wählen Sie die **[!UICONTROL Customer Group]** aus, die dem freigegebenen Katalog entspricht, und ändern Sie die Berechtigungseinstellungen nach Bedarf.

     ![Kategorieberechtigungsregel](./assets/shared-catalog-category-permissions.png){width="600" zoomable="yes"}

   - Um eine Berechtigungsregel für eine andere Kundengruppe zu erstellen, klicken Sie auf **[!UICONTROL New Permissions]** und wiederholen Sie den Vorgang.

   - Um eine Berechtigungsregel zu löschen, klicken Sie auf das Symbol _Löschen_ ![Papierkorb kann](../assets/icon-delete-trashcan-solid.png) .

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

## Aktualisieren der Katalogdetails

Die Detailinformationen eines freigegebenen Katalogs können einfach über die Spalte Aktion des Rasters Gemeinsame Kataloge aktualisiert werden. Die Änderungen, die Sie vornehmen, werden in allen zugehörigen Unternehmenskonten übernommen.

![Allgemeine Einstellungen](./assets/shared-catalog-grid-general-settings.png){width="700" zoomable="yes"}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Markieren Sie für den freigegebenen Katalog, den Sie aktualisieren möchten, die Spalte **[!UICONTROL Action]** und wählen Sie **[!UICONTROL General Settings]** aus.

   ![Katalogdetails](./assets/shared-catalog-update-details.png){width="600" zoomable="yes"}

1. Aktualisieren Sie die Katalogdetailinformationen nach Bedarf.

   - Durch Änderung des Namens eines freigegebenen Katalogs wird auch der Name der entsprechenden Kundengruppe geändert.
   - Wenn Sie den Katalogtyp von `Custom` in `Public` ändern, wird der vorhandene öffentliche Katalog in einen benutzerdefinierten Katalog konvertiert. Alle Unternehmen, die mit dem ursprünglichen öffentlichen Katalog verbunden sind, werden der Ersetzung zugewiesen. Ein öffentlicher Katalog kann nicht in einen benutzerdefinierten Katalog konvertiert werden.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

## Gemeinsame Katalogseitenreferenz

### Schaltflächenleiste

| Schaltfläche | Beschreibung |
|--- |--- |
| [!UICONTROL Back] | Kehrt zur Seite &quot;Freigegebene Kataloge&quot;zurück, ohne den neuen freigegebenen Katalog zu speichern. |
| [!UICONTROL Delete] | Löscht den Katalog und weist alle verbundenen Unternehmen und deren Mitglieder dem öffentlich freigegebenen Katalog zu. |
| [!UICONTROL Reset] | Löscht das Formular nicht gespeicherter Änderungen und stellt die ursprünglichen Katalogdetailinformationen wieder her. |
| [!UICONTROL Duplicate] | Erstellt eine [doppelte Kopie des Katalogs](catalog-shared-create.md). Für einen benutzerdefinierten Katalog, das Preismodell und die Struktur des Originals, aber ohne die Unternehmensverbände. Wenn ein öffentlicher freigegebener Katalog dupliziert wird, ändert sich der Typ des doppelten Katalogs in `custom`. Eine entsprechende Kundengruppe wird auch mit demselben Namen wie der duplizierte Katalog erstellt. Standardmäßig erhält ein duplizierter Katalog den Namen _Duplizieren des_ Originalkatalogs. |
| [!UICONTROL Save and Continue Edit] | Speichert alle Änderungen und behält das Formular im Bearbeitungsmodus bei. |
| [!UICONTROL Save] | Speichert Änderungen, schließt das Formular und kehrt zur Seite Gemeinsame Kataloge zurück. |

{style="table-layout:auto"}

### Katalogdetails

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Name] | Identifiziert den freigegebenen Katalog im gesamten Admin und in den Kundenkonten, in denen er verfügbar ist. Der Katalogname sollte beschreibend sein und nicht länger als 32 Zeichen sein. Sie können nicht zwei freigegebene Kataloge mit demselben Namen haben. Maximale Zeichen: 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Identifiziert einen Katalog mit benutzerdefinierten Preisen, die nur für die spezifischen Unternehmen verfügbar sind, denen er zugewiesen ist.<br/>**[!UICONTROL Public]**- Identifiziert den freigegebenen Katalog, der für alle Gastbesucher und angemeldete Kunden, die nicht mit einem Unternehmen verbunden sind, verfügbar ist. Ein &quot;standardmäßiger&quot;freigegebener Katalog wird erstellt, wenn Adobe Commerce B2B installiert ist, muss jedoch vom Administrator konfiguriert werden. Es kann jeweils nur ein öffentlicher freigegebener Katalog vorhanden sein. |
| [!UICONTROL Customer Tax Class] | Bestimmt die Steuerklasse, die für Käufe verwendet wird, die aus dem Katalog getätigt werden. Die Optionen umfassen alle verfügbaren Steuerklassen. |
| [!UICONTROL Description] | Kurze Erläuterung der Verwendung des Katalogs. |

{style="table-layout:auto"}
