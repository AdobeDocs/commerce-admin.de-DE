---
title: '''[!DNL AR Viewer] für Adobe Commerce'
description: Erfahren Sie, wie Sie [!DNL AR Viewer] kann von Ihrer Adobe Commerce-Instanz und der erfolgreichen Integration und Einrichtung der Erweiterung profitieren.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# [!DNL AR Viewer] für Adobe Commerce

Die erweiterte Realität (AR) beschreibt Benutzererlebnisse, die 2D- oder 3D-Elemente zur Live-Ansicht einer Gerätekamera hinzufügen, sodass diese Elemente in der realen Welt zu leben scheinen.

Die [!DNL AR Viewer] für die Adobe Commerce-Erweiterung bietet ein nahtloses Erlebnis, das für die Anzeige gerenderter 3D-Grafiken für den Benutzer konzipiert ist.

Die Informationen in diesem Handbuch bieten einen Überblick über das Onboarding-Erlebnis für die [!DNL AR Viewer] in Adobe Commerce und wie die [!DNL AR Viewer] Vorteile für den Benutzer sowie Best Practices, die bei dieser Journey befolgt werden.

Entwickelt von Pixar, [Universal Scene Description (USD)](https://www.pixar.com/usd){target=_blank} ist die erste Open-Source-Software, die 3D-Szenen robuster und skalierbar vertauschen kann, die aus vielen verschiedenen Assets, Quellen und Animationen bestehen können, während gleichzeitig hochgradig kollaborative Workflows gefördert werden. Dieses USD wird in `.USDZ` -Dateien. Diese `.USDZ` -Datei stellt AR- und 3D-Inhalte für die Geräte des Benutzers bereit.

>[!NOTE]
>
> Die [!DNL AR Viewer] unterstützt nur `.USDZ` -Dateien.

## [!DNL AR Viewer] Anforderungen

Die [!DNL AR Viewer] ist mit beiden kompatibel [!DNL Magento Open Source] und Adobe Commerce. Siehe [Lebenszyklusrichtlinie](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} Weitere Informationen zu unterstützten Versionen.

Siehe [Installieren Sie die [!DNL AR Viewer] Erweiterung](../catalog/ar-viewer-setup.md) für weitere Informationen.

Zur Verwendung [!DNL AR Viewer]muss für Ihre Instanz Folgendes verfügbar sein:

* PHP 8.1.0
* Adobe Commerce-Version 2.4.4 und neuer
* Magento Open Source (CE) Version 2.4.x

## Kompatibilitätsbeschränkungen

[!DNL AR Viewer] vorhandene Kompatibilitätsbeschränkungen:

* `.USDZ` nur: Diese Funktion unterstützt nur `.USDZ` -Dateien.
* `qr-code`: Erfordert `endroid/qr-code` Version 4.5.
* `Catalog module`: Erfordert `magento/module-catalog` Version 104.0.0.
