---
title: '[!DNL AR Viewer] für Adobe Commerce'
description: Erfahren Sie, wie die [!DNL AR Viewer] Ihrer Adobe Commerce-Instanz zugute kommen könnte und wie Sie die Erweiterung erfolgreich integrieren und einrichten können.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# [!DNL AR Viewer] für Adobe Commerce

Die erweiterte Realität (AR) beschreibt Benutzererlebnisse, die 2D- oder 3D-Elemente zur Live-Ansicht einer Gerätekamera hinzufügen, sodass diese Elemente in der realen Welt zu leben scheinen.

Die Erweiterung [!DNL AR Viewer] für Adobe Commerce bietet ein nahtloses Erlebnis, das für die Anzeige gerenderter 3D-Grafiken für den Benutzer entwickelt wurde.

Die Informationen in diesem Handbuch geben einen Überblick über das Onboarding-Erlebnis für die [!DNL AR Viewer] in Adobe Commerce und darüber, wie die [!DNL AR Viewer] für den Benutzer von Vorteil ist, sowie über Best Practices, die für diese Journey gelten.

[Universal Scene Description (USD)](https://openusd.org/release/index.html){target=_blank} wurde von Pixar entwickelt und ist die erste Open-Source-Software, mit der 3D-Szenen, die aus vielen verschiedenen Assets, Quellen und Animationen bestehen können, robust und skalierbar ausgetauscht werden können. Gleichzeitig werden sehr kollaborative Workflows gefördert. Dieser USD wird in `.USDZ` -Dateien verwendet. Diese `.USDZ`-Datei stellt AR- und 3D-Inhalte für die Geräte des Benutzers bereit.

>[!NOTE]
>
> Die [!DNL AR Viewer] unterstützt nur `.USDZ` -Dateien.

## [!DNL AR Viewer] Anforderungen

Die [!DNL AR Viewer] ist sowohl mit [!DNL Magento Open Source] als auch mit Adobe Commerce kompatibel. Weitere Informationen zu unterstützten Versionen finden Sie unter [Lebenszyklusrichtlinie](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} .

Weitere Informationen finden Sie unter [Installieren der  [!DNL AR Viewer] Erweiterung](../catalog/ar-viewer-setup.md) .

Um [!DNL AR Viewer] verwenden zu können, müssen Sie über Folgendes für Ihre Instanz verfügen:

* PHP 8.1.0
* Adobe Commerce-Version 2.4.4 und neuer
* Magento Open Source (CE) Version 2.4.x

## Kompatibilitätsbeschränkungen

[!DNL AR Viewer] vorhandene Kompatibilitätsbeschränkungen:

* Nur `.USDZ`: Diese Funktion unterstützt nur `.USDZ` -Dateien.
* `qr-code`: Erfordert `endroid/qr-code` Version 4.5.
* `Catalog module`: Erfordert `magento/module-catalog` Version 104.0.0.
