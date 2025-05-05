---
title: Übersicht über freigegebene Kataloge
description: Erfahren Sie mehr über die von Adobe Commerce B2B bereitgestellten freigegebenen Kataloge und darüber, wie Sie sie zur Pflege von Gated-Katalogen mit benutzerdefinierter Preisgestaltung für verschiedene Unternehmenskonten verwenden können.
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# Übersicht über freigegebene Kataloge

Adobe Commerce B2B bietet Ihnen die Möglichkeit, _Kataloge mit_ Preisen für verschiedene Unternehmen zu verwalten. Zusätzlich zum standardmäßigen Produktkatalog (_) bietet_ Kunden Zugriff auf zwei Arten von freigegebenen Katalogen mit unterschiedlichen Preisstrukturen.

Wenn die Funktion [Freigegebener Katalog](enable-basic-features.md) in der Konfiguration aktiviert ist, bleibt der ursprüngliche primäre Katalog im Admin-Bereich sichtbar, aber nur der standardmäßige (allgemeine) öffentliche freigegebene Katalog ist in der Storefront sichtbar. Darüber hinaus können benutzerdefinierte Kataloge erstellt werden, die nur für Mitglieder bestimmter (Unternehmens[-](account-companies.md) sichtbar sind.

Für den `Default (General)` freigegebenen Katalog müssen Sie Produkte zuweisen, um den Katalog in der Storefront anzuzeigen. Standardmäßig ist es leer und enthält keine Produkte.

>[!NOTE]
>
>**[B2B-Version 1.3.](release-notes.md#b2b-v130) und höher** - Wenn Sie einen freigegebenen Katalog erstellen, wird jede [Kategorieberechtigung](../catalog/category-permissions.md) für den Katalog auf _[!UICONTROL Allow for the Display Product Prices]_&#x200B;und&#x200B;_[!UICONTROL Add to Cart]_ für Kundengruppen festgelegt, denen dieser Zugriff in den Katalogberechtigungseinstellungen zugewiesen ist. Zuvor wurden diese Einstellungen automatisch auf `Deny` gesetzt, auch wenn die Katalogberechtigungen auf `Allow` gesetzt waren.

>[!IMPORTANT]
>
>Alle vorhandenen [Gruppenberechtigungseinstellungen](../configuration-reference/catalog/catalog.md#category-permissions) werden von **_allen_** Kategorien im Katalog ignoriert, wenn die **_[!UICONTROL Shared Catalog]_** aktiviert ist. [!UICONTROL Shared Catalog] steuert alle Kategorieberechtigungen im Katalog vollständig, wenn er aktiviert ist.

Die Seite _[!UICONTROL Shared Catalogs]_&#x200B;bietet Zugriff auf die Tools, die zum Verwalten Ihrer freigegebenen Kataloge verwendet werden. Die Seite ähnelt dem standardmäßigen [Admin Workspace](../getting-started/admin-workspace.md) mit Filtern und Aktionssteuerelementen. Im Raster werden alle freigegebenen Kataloge aufgelistet, einschließlich des standardmäßigen öffentlichen freigegebenen Katalogs und aller benutzerdefinierten Kataloge, die Sie eingerichtet haben.

![freigegebene Kataloge](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## Zugriff auf die [!UICONTROL Shared Catalogs]

Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

## Aktionssteuerelemente

Die [Aktionssteuerelemente](../getting-started/admin-actions-control.md) in der oberen linken Ecke können mit dem Massenaktionssteuerelement verwendet werden, um ausgewählte freigegebene Kataloge zu löschen, die nicht mehr benötigt werden. Im Raster enthält die Spalte _[!UICONTROL Actions]_&#x200B;die vollständige Auswahl an Tools zur Verwaltung Ihrer freigegebenen Kataloge.

![Aktionen für freigegebene Kataloge](./assets/shared-catalog-grid-action-column-controls.png){width="350"}

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
| [!UICONTROL Select] | Wählt freigegebene Katalogdatensätze zum Anwenden einer Aktion aus. Mit dem Steuerelement in der Kopfzeile können Sie alle freigegebenen Katalogdatensätze im Raster auswählen oder die Auswahl aufheben. Aktivieren Sie das Kontrollkästchen, um einen einzelnen freigegebenen Katalog auszuwählen. |
| [!UICONTROL ID] | Eine eindeutige numerische Kennung, die beim Erstellen des Katalogs nacheinander zugewiesen wird. |
| [!UICONTROL Name] | Der Name des freigegebenen Katalogs. Standardmäßig ist der standardmäßige (allgemeine) freigegebene Katalog verfügbar. |
| [!UICONTROL Type] | Gibt den Typ des freigegebenen Katalogs an als: <br/>**[!UICONTROL Public]**- Der standardmäßige öffentliche freigegebene Katalog wird automatisch bei der Installation von Adobe Commerce B2B erstellt. Sie ist zunächst den `General` und `Not Logged In` Kundengruppen zugewiesen und für Gäste und einzelne angemeldete Kunden sichtbar, die nicht mit einem Unternehmen verknüpft sind. Das System unterstützt jeweils nur einen öffentlichen freigegebenen Katalog.<br/>**[!UICONTROL Custom]** - Ein benutzerdefinierter freigegebener Katalog enthält Preise, die nur für angemeldete Mitarbeiter der zugewiesenen Unternehmenskonten sichtbar sind. Sie können beliebig viele benutzerdefinierte freigegebene Kataloge erstellen. |
| [!UICONTROL Customer Tax Class] | Die Steuerklasse, die der entsprechenden Debitorengruppe zugeordnet ist. Diese Spalte wird nicht im Standardraster angezeigt, kann jedoch hinzugefügt werden, indem das Spalten-Layout geändert wird. |
| [!UICONTROL Created At] | Datum und Uhrzeit der Erstellung des freigegebenen Katalogs. |
| [!UICONTROL Created By] | Der Vor- und Nachname des Store-Administrators, der den freigegebenen Katalog erstellt hat. |
| [!UICONTROL Action] | Listet Aktionen auf, die auf ausgewählte Kataloge angewendet werden können. Optionen: `Set Pricing and Structure` / `Assign Companies` / `General Settings` / `Delete` |

{style="table-layout:auto"}
