---
title: Übersicht über freigegebenen Katalog
description: Erfahren Sie mehr über die freigegebenen Kataloge, die von B2B für Adobe Commerce bereitgestellt werden, und wie Sie sie verwenden können, um geordnete Kataloge mit benutzerdefinierten Preisen für verschiedene Unternehmenskonten zu verwalten.
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 0%

---

# Übersicht über freigegebenen Katalog

B2B für Adobe Commerce bietet Ihnen die Möglichkeit, die Erfassung von Daten beizubehalten _shared_ Kataloge mit benutzerdefinierten Preisen für verschiedene Unternehmen. Zusätzlich zur Norm _primary_, Produktkatalog, bietet er Kunden Zugriff auf zwei Arten freigegebener Kataloge mit unterschiedlichen Preisstrukturen.

Wenn die Variable [Freigegebene Katalogfunktion](enable-basic-features.md) in der Konfiguration aktiviert ist, bleibt der ursprüngliche primäre Katalog vom Administrator sichtbar, aber nur der öffentliche Standardkatalog (Allgemein) ist im Storefront sichtbar. Darüber hinaus können benutzerdefinierte Kataloge erstellt werden, die nur für Mitglieder bestimmter [Firma](account-companies.md) Konten.

Für `Default (General)` öffentlichen freigegebenen Katalog, müssen Sie Produkte zuweisen, um den Katalog in der Storefront anzuzeigen. Standardmäßig ist er leer und enthält keine Produkte.

>[!NOTE]
>
>**[B2B-Version 1.3.0](release-notes.md#b2b-v130) und höher** — Wenn Sie einen freigegebenen Katalog erstellen, wird jede [Kategorienberechtigung](../catalog/category-permissions.md) für den Katalog auf _[!UICONTROL Allow for the Display Product Prices]_und_[!UICONTROL Add to Cart]_ für Kundengruppen, denen dieser Zugriff in den Katalogberechtigungseinstellungen zugewiesen wurde. Zuvor wurden diese Einstellungen automatisch auf `Deny` auch wenn die Katalogberechtigungen auf `Allow`.

>[!IMPORTANT]
>
>Alle vorhandenen [Gruppenberechtigungseinstellungen](../configuration-reference/catalog/catalog.md#category-permissions) werden von **_all_** Kategorien im Katalog, wenn die **_[!UICONTROL Shared Catalog]_** aktiviert ist. [!UICONTROL Shared Catalog] steuert alle Kategorieberechtigungen im Katalog vollständig, wenn sie aktiviert sind.

Die _[!UICONTROL Shared Catalogs]_-Seite bietet Zugriff auf die Tools zur Verwaltung Ihrer freigegebenen Kataloge. Die Seite ähnelt der standardmäßigen [Admin Workspace](../getting-started/admin-workspace.md), mit Filtern und Aktionssteuerelementen. Das Raster listet alle freigegebenen Kataloge auf, einschließlich des standardmäßigen öffentlichen freigegebenen Katalogs und aller benutzerdefinierten Kataloge, die Sie eingerichtet haben.

![Freigegebene Kataloge](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## Zugriff auf [!UICONTROL Shared Catalogs] page

Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

## Aktionssteuerelemente

Die [Aktionssteuerelemente](../getting-started/admin-actions-control.md) in der linken oberen Ecke kann mit dem Steuerelement für Massenaktionen verwendet werden, um ausgewählte freigegebene Kataloge zu löschen, die nicht mehr benötigt werden. Im Raster wird die _[!UICONTROL Actions]_enthält die vollständige Auswahl der Tools zur Verwaltung Ihrer freigegebenen Kataloge.

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
| [!UICONTROL Type] | Identifiziert den Typ des freigegebenen Katalogs wie folgt: <br/>**[!UICONTROL Public]**- Der standardmäßige öffentliche freigegebene Katalog wird automatisch erstellt, wenn B2B für Adobe Commerce installiert ist. Sie wird zunächst dem `General` und `Not Logged In` Kundengruppen und ist für Gäste und einzelne angemeldete Kunden sichtbar, die nicht mit einem Unternehmen verbunden sind. Das System unterstützt jeweils nur einen öffentlichen freigegebenen Katalog.<br/>**[!UICONTROL Custom]** - Ein benutzerdefinierter freigegebener Katalog enthält Preise, die nur für angemeldete Mitarbeiter der zugewiesenen Unternehmenskonten sichtbar sind. Sie können beliebig viele benutzerdefinierte freigegebene Kataloge erstellen. |
| [!UICONTROL Customer Tax Class] | Die der entsprechenden Kundengruppe zugewiesene Steuerklasse. Diese Spalte wird nicht im Standardraster angezeigt, kann jedoch durch Änderung des Spaltenlayouts hinzugefügt werden. |
| [!UICONTROL Created At] | Datum und Uhrzeit der Erstellung des freigegebenen Katalogs. |
| [!UICONTROL Created By] | Der Vor- und Nachname des Store-Administrators, der den freigegebenen Katalog erstellt hat. |
| [!UICONTROL Action] | Führt Aktionen auf, die auf ausgewählte Kataloge angewendet werden. Optionen: `Set Pricing and Structure` / `Assign Companies` / `General Settings` / `Delete` |

{style="table-layout:auto"}
