---
title: Verschlüsselungsschlüssel
description: Erfahren Sie, wie Sie Ihren eigenen Verschlüsselungsschlüssel automatisch generieren oder hinzufügen, der regelmäßig geändert werden sollte, um die Sicherheit zu verbessern.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 2469b3853d074f7a7adfe822b645e41d1420259a
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Verschlüsselungsschlüssel

Adobe Commerce und Magento Open Source verwenden einen Verschlüsselungsschlüssel, um Kennwörter und andere vertrauliche Daten zu schützen. Ein branchenüblicher [!DNL ChaCha20-Poly1305]-Algorithmus wird mit einem 256-Bit-Schlüssel verwendet, um alle Daten zu verschlüsseln, die verschlüsselt werden müssen. Dazu gehören Kreditkartendaten und Integrationskennwörter (Zahlungs- und Versandmodul). Darüber hinaus wird ein starker sicherer Hash-Algorithmus (SHA-256) verwendet, um alle Daten zu hash, die nicht entschlüsselt werden müssen.

Während der ersten Installation werden Sie aufgefordert, entweder Commerce einen Verschlüsselungsschlüssel generieren zu lassen oder einen eigenen einzugeben. Mit dem Verschlüsselungsschlüssel-Tool können Sie den Schlüssel nach Bedarf ändern. Der Verschlüsselungsschlüssel sollte regelmäßig geändert werden, um die Sicherheit zu verbessern, und der ursprüngliche Schlüssel kann jederzeit beeinträchtigt werden. Bei jeder Änderung des Schlüssels werden alle Legacy-Daten mit dem neuen Schlüssel neu kodiert.

Technische Informationen finden Sie unter [Erweiterte lokale Installation](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) im _Installationshandbuch_.

>[!IMPORTANT]
>
>Bevor Sie diese Anweisungen zum Ändern des Verschlüsselungsschlüssels befolgen, stellen Sie sicher, dass die folgende Datei schreibbar ist: `[your store]/app/etc/env.php`

**So ändern Sie einen Verschlüsselungsschlüssel:**

Die folgenden Anweisungen erfordern den Zugriff auf ein Terminal.

1. Aktivieren Sie den [Wartungsmodus](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/setup/application-modes#maintenance-mode).

   ```bash
   bin/magento maintenance:enable
   ```

1. Deaktivieren Sie Cron-Aufträge.

   _Cloud-Infrastrukturprojekte:_

   ```bash
   ./vendor/bin/ece-tools cron:disable
   ```

   _Vor-Ort-Projekte_

   ```bash
   crontab -e
   ```

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

   ![Systemverschlüsselungsschlüssel](./assets/encryption-key.png){width="700" zoomable="yes"}

1. Führen Sie einen der folgenden Schritte aus:

   - Um einen neuen Schlüssel zu generieren, setzen Sie **[!UICONTROL Auto-generate Key]** auf `Yes`.
   - Um einen anderen Schlüssel zu verwenden, setzen Sie **[!UICONTROL Auto-generate Key]** auf `No`. Geben Sie dann im Feld **[!UICONTROL New Key]** den zu verwendenden Schlüssel ein oder fügen Sie ihn ein.

1. Klicken Sie auf **[!UICONTROL Change Encryption Key]**.

   >[!NOTE]
   >
   >Verwahren Sie den neuen Schlüssel an einem sicheren Speicherort auf. Es ist erforderlich, die Daten zu entschlüsseln, wenn Probleme mit Ihren Dateien auftreten.

1. Leeren Sie den Cache.

   _Cloud-Infrastrukturprojekte:_

   ```bash
   magento-cloud cc
   ```

   _Vor Ort durchgeführte Projekte:_

   ```bash
   bin/magento cache:flush
   ```

1. Aktivieren Sie Cron-Aufträge.

   _Cloud-Infrastrukturprojekte:_

   ```bash
   ./vendor/bin/ece-tools cron:enable
   ```

   _Vor Ort durchgeführte Projekte:_

   ```bash
   crontab -e
   ```

1. Wartungsmodus deaktivieren.

   ```bash
   bin/magento maintenance:disable
   ```
