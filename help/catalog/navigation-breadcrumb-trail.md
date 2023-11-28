---
title: Breadcrumb-Pfad
description: Erfahren Sie mehr über die verschiedenen Breadcrumb-Pfad-Muster und wie Sie sie so konfigurieren, dass sie auf Inhalts- und Katalogseiten angezeigt werden.
exl-id: 2f60d48e-960f-437c-8f8f-a3d06cc0840a
feature: Catalog Management, Categories, Site Navigation, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Breadcrumb-Pfad

A _Breadcrumb-Pfad_ ist ein Satz von Links, der dem Kunden zeigt, wo er sich im Verhältnis zu anderen Seiten im Store befindet. Sie können auf einen beliebigen Link im Breadcrumb-Pfad klicken, um zur vorherigen Seite zurückzukehren.

Die Breadcrumb-Leiste kann so konfiguriert werden, dass sie auf Inhaltsseiten und auf Katalogseiten angezeigt wird. Das Format und die Position des Breadcrumb-Pfads variieren nach Thema, befinden sich jedoch normalerweise direkt unter der Kopfzeile. Standardmäßig wird die Breadcrumb-Leiste auf CMS-Seiten angezeigt.

![In der Storefront angezeigte Breadcrumb-Leiste](./assets/storefront-breadcrumb-trail.png){width="700" zoomable="yes"}

## Allgemeine Brotkrümel

Breadcrumbs können in drei Haupttypen unterteilt werden, die je nach Zweck unterschiedlich sind. Im Folgenden werden der Kern und die wichtigsten Grundsätze der Implementierung der einzelnen Brotkrümel beschrieben.

### Hierarchiebasierte Breadcrumbs

Dieser Breadcrumb-Typ basiert auf der auf der Site eingerichteten Kategoriehierarchie. Die angezeigten Ketten teilen dem Benutzer mit, wo er sich in der Struktur befindet. In diesem Fall ist jeder Text-Link für eine Seite vorgesehen, die eine Ebene höher ist als die vorherige.

Beispiel: `Men > Tops > Hoodies & Sweatshirts`

Der Vorteil dieses Typs besteht darin, dass Benutzer leicht erkennen können, in welcher Kategoriestufe sie sich befinden, und einfachen Zugriff auf die Navigation zwischen Katalogseiten haben.

### Historische Breadcrumbs

Die auf Verlauf (oder Pfad) basierende Navigation ähnelt der Schaltfläche &quot;Zurück&quot;in einem Browser. Mit dieser Art der Navigation können Benutzer schnell zu den vorherigen Seiten zurückkehren, die sie ohne Änderungen besucht haben.

Der Vorteil dieses Typs besteht darin, dass es am hilfreichsten ist, wenn Kunden nach Auswahl mehrerer Filter auf einer Kategorieseite zu einer vorherigen Seite zurückkehren möchten.

Beispiel: `Home > What's New > Gear > Bags`

### Attributbasierte Breadcrumbs

Dieser Breadcrumb-Typ zeigt die auf der Kategorieseite ausgewählten Attribute an. Der Hauptunterschied zu den anderen Typen besteht darin, dass die attributbasierten Breadcrumbs die Filter und Optionen darstellen, die der Kunde in der Navigationsschicht für bestimmte Produkte ausgewählt hat (z. B. Preis, Qualität und Farbe).

Beispiel: `Home > Suits > All Suits > Refined by > Slim Fit`

## Hinzufügen/Entfernen von Breadcrumbs aus CMS-Seiten

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Bereich unter _[!UICONTROL General]_auswählen **[!UICONTROL Web]**.

   ![Breadcrumbs für CMS-Seiten anzeigen](../configuration-reference/general/assets/web-default-pages.png){width="600" zoomable="yes"}

1. Erweitern Sie die _[!UICONTROL Default Pages]_Abschnitt.

1. Deaktivieren Sie die **[!UICONTROL Use system value]** aktivieren.

1. Satz **[!UICONTROL Show Breadcrumbs for CMS Pages]** nach `No` oder `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Die übergeordnete Kategorie wird auf der untergeordneten Kategorieseite nicht auf der Breadcrumb-Leiste angezeigt, wenn sie `Browsing Category`= `Deny` [Kategorienberechtigung](category-permissions.md) -Einstellungen.
