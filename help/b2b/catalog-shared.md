---
title: Übersicht über freigegebenen Katalog
description: Erfahren Sie mehr über die von Adobe Commerce B2B bereitgestellten freigegebenen Kataloge und wie Sie sie verwenden können, um geordnete Kataloge mit benutzerdefinierten Preisen für verschiedene Unternehmenskonten zu verwalten.
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# Übersicht über freigegebenen Katalog

Adobe Commerce B2B bietet Ihnen die Möglichkeit, geordnete _shared_-Kataloge mit benutzerdefinierten Preisen für verschiedene Unternehmen zu verwalten. Neben dem standardmäßigen Produktkatalog _primary_ bietet er dem Kunden Zugriff auf zwei Arten freigegebener Kataloge mit unterschiedlichen Preisstrukturen.

Wenn die Funktion &quot;[Freigegebener Katalog&quot;](enable-basic-features.md) in der Konfiguration aktiviert ist, bleibt der ursprüngliche Primärkatalog vom Administrator sichtbar, aber nur der öffentliche Standardkatalog (Allgemein) ist in der Storefront sichtbar. Darüber hinaus können benutzerdefinierte Kataloge erstellt werden, die nur für Mitglieder bestimmter [Unternehmenskonten](account-companies.md) sichtbar sind.

Für den öffentlichen freigegebenen Katalog `Default (General)` müssen Sie Produkte zuweisen, damit der Katalog im Storefront angezeigt wird. Standardmäßig ist er leer und enthält keine Produkte.

>[!NOTE]
>
>**[B2B-Version 1.3.0](release-notes.md#b2b-v130) und höher** - Wenn Sie einen freigegebenen Katalog erstellen, wird jede [Kategorieberechtigung](../catalog/category-permissions.md) für den Katalog auf _[!UICONTROL Allow for the Display Product Prices]_und_[!UICONTROL Add to Cart]_ für Kundengruppen festgelegt, denen dieser Zugriff in den Einstellungen für Katalogberechtigungen zugewiesen ist. Zuvor wurden diese Einstellungen automatisch auf `Deny` gesetzt, selbst wenn die Katalogberechtigungen auf `Allow` festgelegt waren.

>[!IMPORTANT]
>
>Alle vorhandenen [Gruppenberechtigungseinstellungen](../configuration-reference/catalog/catalog.md#category-permissions) werden von den Kategorien **_Alle_** im Katalog ignoriert, wenn die Funktion **_[!UICONTROL Shared Catalog]_** aktiviert ist. [!UICONTROL Shared Catalog] steuert alle Kategorieberechtigungen im Katalog vollständig, wenn sie aktiviert sind.

Die Seite &quot;_[!UICONTROL Shared Catalogs]_&quot; bietet Zugriff auf die Tools zur Verwaltung Ihrer freigegebenen Kataloge. Die Seite ähnelt dem standardmäßigen [Admin-Arbeitsbereich](../getting-started/admin-workspace.md) mit Filtern und Aktionssteuerelementen. Das Raster listet alle freigegebenen Kataloge auf, einschließlich des standardmäßigen öffentlichen freigegebenen Katalogs und aller benutzerdefinierten Kataloge, die Sie eingerichtet haben.

![Freigegebene Kataloge](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## Zugriff auf die Seite [!UICONTROL Shared Catalogs]

Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

## Aktionssteuerelemente

Die Steuerelemente [actions](../getting-started/admin-actions-control.md) in der oberen linken Ecke können mit dem Steuerelement für Massenaktionen verwendet werden, um ausgewählte freigegebene Kataloge zu löschen, die nicht mehr benötigt werden. Im Raster enthält die Spalte _[!UICONTROL Actions]_die vollständige Auswahl an Tools zur Verwaltung Ihrer freigegebenen Kataloge.

![Freigegebene Katalogaktionen](./assets/shared-catalog-grid-action-column-controls.png){width="350"}

| Kontrolle | Beschreibung |
|------|-----------|
| [[!UICONTROL Set Pricing and Structure]](catalog-shared-pricing-structure.md) | Bestimmt die Produktauswahl und die benutzerdefinierten Preise, die im freigegebenen Katalog verfügbar sind. |
| [[!UICONTROL Assign Companies]](catalog-shared-assign-companies.md) | Legt fest, welche Unternehmen auf einen freigegebenen Katalog zugreifen können. |
| [[!UICONTROL General Settings]](catalog-shared-manage.md) | Bestimmt die Katalogdetailinformationen, einschließlich Name, Katalogtyp, Kundensteuerklasse und Beschreibung. |
| [!UICONTROL Delete] | Löscht die ausgewählten freigegebenen Kataloge. |

{style="table-layout:auto"}

## Spaltenbeschreibungen

| Überschrift | Beschreibung |
|--- |--- |
| [!UICONTROL Select] | Wählt freigegebene Katalogdatensätze für die Anwendung einer Aktion aus. Mit dem Steuerelement in der Kopfzeile können Sie alle freigegebenen Katalogdatensätze im Raster auswählen oder die Auswahl aufheben. Um einen einzelnen freigegebenen Katalog auszuwählen, aktivieren Sie das Kontrollkästchen. |
| [!UICONTROL ID] | Eine eindeutige numerische Kennung, die bei der Erstellung des Katalogs der Sequenz zugeordnet wird. |
| [!UICONTROL Name] | Der Name des freigegebenen Katalogs. Standardmäßig ist der standardmäßige freigegebene Katalog (Allgemein) verfügbar. |
| [!UICONTROL Type] | Identifiziert den Typ des freigegebenen Katalogs als: <br/>**[!UICONTROL Public]**- Der standardmäßige öffentliche freigegebene Katalog wird automatisch erstellt, wenn Adobe Commerce B2B installiert ist. Er wird zunächst den Kundengruppen `General` und `Not Logged In` zugewiesen und ist für Gäste und einzelne angemeldete Kunden sichtbar, die nicht mit einem Unternehmen verbunden sind. Das System unterstützt jeweils nur einen öffentlichen freigegebenen Katalog.<br/>**[!UICONTROL Custom]** - Ein benutzerdefinierter freigegebener Katalog enthält Preise, die nur für angemeldete Mitarbeiter der zugewiesenen Unternehmenskonten sichtbar sind. Sie können beliebig viele benutzerdefinierte freigegebene Kataloge erstellen. |
| [!UICONTROL Customer Tax Class] | Die der entsprechenden Kundengruppe zugewiesene Steuerklasse. Diese Spalte wird nicht im Standardraster angezeigt, kann jedoch durch Änderung des Spaltenlayouts hinzugefügt werden. |
| [!UICONTROL Created At] | Datum und Uhrzeit der Erstellung des freigegebenen Katalogs. |
| [!UICONTROL Created By] | Der Vor- und Nachname des Store-Administrators, der den freigegebenen Katalog erstellt hat. |
| [!UICONTROL Action] | Führt Aktionen auf, die auf ausgewählte Kataloge angewendet werden. Optionen: `Set Pricing and Structure` / `Assign Companies` / `General Settings` / `Delete` |

{style="table-layout:auto"}
