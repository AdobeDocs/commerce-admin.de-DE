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

Ein _Breadcrumb-Pfad_ ist ein Satz von Links, die dem Kunden zeigen, wo er sich im Verhältnis zu anderen Seiten im Store befindet. Sie können auf einen beliebigen Link im Breadcrumb-Pfad klicken, um zur vorherigen Seite zurückzukehren.

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

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich unter _[!UICONTROL General]_die Option **[!UICONTROL Web]**.

   ![Breadcrumbs für CMS-Seiten anzeigen](../configuration-reference/general/assets/web-default-pages.png){width="600" zoomable="yes"}

1. Erweitern Sie den Abschnitt _[!UICONTROL Default Pages]_.

1. Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** .

1. Setzen Sie **[!UICONTROL Show Breadcrumbs for CMS Pages]** auf `No` oder `Yes`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Die übergeordnete Kategorie wird auf der untergeordneten Kategorieseite nicht im Breadcrumb-Pfad angezeigt, wenn sie über die Einstellungen `Browsing Category`= `Deny` [Kategorieberechtigung](category-permissions.md) verfügt.
