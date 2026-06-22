---
title: '[!DNL AR Viewer] für Adobe Commerce'
description: Erfahren Sie, wie  [!DNL AR Viewer]  Ihre Adobe Commerce-Instanz unterstützen kann und wie Sie die Erweiterung erfolgreich integrieren und einrichten können.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
TQID: https://experienceleague.adobe.com/ofebqdDS0exPDKJMLB-mpE0eVjRKT5ck91Fm2-7CVjA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a09a5a04-e30b-4d55-b031-38e6f5ec86db
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 247
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

Die [!DNL AR Viewer] ist sowohl mit [!DNL Magento Open Source] als auch mit Adobe Commerce kompatibel. Weitere [&#x200B; zu unterstützten Versionen finden &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html?lang=de){target=_blank} unter „Lebenszyklusrichtlinie.

Weitere Informationen finden [&#x200B; unter  [!DNL AR Viewer] Installieren der &#x200B;](../catalog/ar-viewer-setup.md)-Erweiterung).

Um [!DNL AR Viewer] verwenden zu können, müssen Sie über Folgendes für Ihre Instanz verfügen:

* PHP 8.1.0
* Adobe Commerce Version 2.4.4 und neuer
* Magento Open Source (CE) Version 2.4.x

## Einschränkungen bei der Kompatibilität

[!DNL AR Viewer] Kompatibilitätseinschränkungen:

* Nur `.USDZ`: Diese Funktion unterstützt nur `.USDZ`.
* `qr-code`: Erfordert `endroid/qr-code` Version 4.5.
* `Catalog module`: Erfordert `magento/module-catalog` Version 104.0.0.

