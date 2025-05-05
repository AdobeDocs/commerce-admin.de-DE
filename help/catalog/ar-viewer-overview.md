---
title: '[!DNL AR Viewer] für Adobe Commerce'
description: Erfahren Sie, wie  [!DNL AR Viewer]  Ihre Adobe Commerce-Instanz unterstützen kann und wie Sie die Erweiterung erfolgreich integrieren und einrichten können.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# [!DNL AR Viewer] für Adobe Commerce

Augmented Reality (AR) beschreibt Anwendererlebnisse, die der Live-Ansicht von der Kamera eines Geräts 2D- oder 3D-Elemente hinzufügen, sodass diese Elemente in der realen Welt zu leben scheinen.

Die [!DNL AR Viewer] für Adobe Commerce-Erweiterung bietet ein nahtloses Erlebnis, das darauf ausgelegt ist, gerenderte 3D-Grafiken für den Benutzer anzuzeigen.

Die Informationen in diesem Handbuch bieten einen Überblick über das Onboarding-Erlebnis für die [!DNL AR Viewer] in Adobe Commerce und darüber, wie die [!DNL AR Viewer] den Benutzenden nützt, sowie Best Practices, die auf dieser Journey befolgt werden sollten.

Die von Pixar entwickelte [Universal Scene Description (USD)](https://openusd.org/release/index.html){target=_blank} ist die erste Open-Source-Software, die robuste und skalierbare 3D-Szenen, die aus vielen verschiedenen Assets, Quellen und Animationen bestehen können, austauschen und dabei hochgradig kollaborative Workflows fördern kann. Dieses USD wird in `.USDZ` Dateien verwendet. Diese `.USDZ`-Datei stellt AR- und 3D-Inhalte für die Geräte der Benutzenden bereit.

>[!NOTE]
>
> Der [!DNL AR Viewer] unterstützt nur `.USDZ`.

## [!DNL AR Viewer]

Die [!DNL AR Viewer] ist sowohl mit [!DNL Magento Open Source] als auch mit Adobe Commerce kompatibel. Weitere [ zu unterstützten Versionen finden ](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html?lang=de){target=_blank} unter „Lebenszyklusrichtlinie.

Weitere Informationen finden [ unter  [!DNL AR Viewer] Installieren der ](../catalog/ar-viewer-setup.md)-Erweiterung).

Um [!DNL AR Viewer] verwenden zu können, müssen Sie über Folgendes für Ihre Instanz verfügen:

* PHP 8.1.0
* Adobe Commerce Version 2.4.4 und neuer
* Magento Open Source (CE) Version 2.4.x

## Einschränkungen bei der Kompatibilität

[!DNL AR Viewer] Kompatibilitätseinschränkungen:

* Nur `.USDZ`: Diese Funktion unterstützt nur `.USDZ`.
* `qr-code`: Erfordert `endroid/qr-code` Version 4.5.
* `Catalog module`: Erfordert `magento/module-catalog` Version 104.0.0.
