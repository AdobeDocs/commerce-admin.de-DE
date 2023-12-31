---
title: Verschlüsselungsschlüssel
description: Erfahren Sie, wie Sie Ihren eigenen Verschlüsselungsschlüssel automatisch generieren oder hinzufügen, der regelmäßig geändert werden sollte, um die Sicherheit zu verbessern.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 21be3c7a56cb72d685b2b3605bc27266e8e55f37
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Verschlüsselungsschlüssel

Adobe Commerce und Magento Open Source verwenden einen Verschlüsselungsschlüssel, um Kennwörter und andere vertrauliche Daten zu schützen. Branchenüblich [!DNL ChaCha20-Poly1305] -Algorithmus wird mit einem 256-Bit-Schlüssel verwendet, um alle Daten zu verschlüsseln, die verschlüsselt werden müssen. Dazu gehören Kreditkartendaten und Integrationskennwörter (Zahlungs- und Versandmodul). Darüber hinaus wird ein starker sicherer Hash-Algorithmus (SHA-256) verwendet, um alle Daten zu hash, die nicht entschlüsselt werden müssen.

Während der ersten Installation werden Sie aufgefordert, entweder Commerce einen Verschlüsselungsschlüssel generieren zu lassen oder einen eigenen einzugeben. Mit dem Verschlüsselungsschlüssel-Tool können Sie den Schlüssel nach Bedarf ändern. Der Verschlüsselungsschlüssel sollte regelmäßig geändert werden, um die Sicherheit zu verbessern, und der ursprüngliche Schlüssel kann jederzeit beeinträchtigt werden. Bei jeder Änderung des Schlüssels werden alle Legacy-Daten mit dem neuen Schlüssel neu kodiert.

Technische Informationen finden Sie unter [Fortgeschrittene Installation vor Ort](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) im _Installationsanleitung_.

## Schritt 1: Datei schreiben

Um den Verschlüsselungsschlüssel zu ändern, stellen Sie sicher, dass die folgende Datei schreibbar ist: `[your store]/app/etc/env.php`

## Schritt 2: Verschlüsselungsschlüssel ändern

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

   ![Schlüssel zur Systemverschlüsselung](./assets/encryption-key.png){width="700" zoomable="yes"}

1. Führen Sie einen der folgenden Schritte aus:

   - Um einen neuen Schlüssel zu generieren, legen Sie **[!UICONTROL Auto-generate Key]** nach `Yes`.
   - Um einen anderen Schlüssel zu verwenden, legen Sie **[!UICONTROL Auto-generate Key]** nach `No`. Dann in der **[!UICONTROL New Key]** eingeben oder den Schlüssel einfügen, den Sie verwenden möchten.

1. Klicken **[!UICONTROL Change Encryption Key]**.

1. Verwahren Sie den neuen Schlüssel an einem sicheren Speicherort auf.

   Es ist erforderlich, die Daten zu entschlüsseln, wenn Probleme mit Ihren Dateien auftreten.
