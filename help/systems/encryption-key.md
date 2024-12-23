---
title: Verschlüsselungsschlüssel
description: Erfahren Sie, wie Sie automatisch einen eigenen Verschlüsselungsschlüssel generieren oder hinzufügen. Dieser sollte regelmäßig geändert werden, um die Sicherheit zu verbessern.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 65c15bb84b28088a6e8f06f3592600779ba033f5
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Verschlüsselungsschlüssel

>[!NOTE]
>
>Wenn Sie versucht haben, diese Schritte auszuführen und Probleme haben, lesen Sie den Artikel [Fehlerbehebung bei der Rotation von Verschlüsselungsschlüsseln: CVE-2024-34102](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/troubleshooting-encryption-key-rotation-cve-2024-34102) Knowledge Base“.

Adobe Commerce und Magento Open Source verwenden zum Schutz von Passwörtern und anderen sensiblen Daten einen Verschlüsselungsschlüssel. Ein [!DNL ChaCha20-Poly1305]-Algorithmus nach Industriestandard wird mit einem 256-Bit-Schlüssel verwendet, um alle Daten zu verschlüsseln, die verschlüsselt werden müssen. Dazu gehören Kreditkartendaten und Passwörter für die Integration (Zahlungs- und Versandmodul). Darüber hinaus wird ein starker sicherer Hash-Algorithmus (SHA-256) verwendet, um alle Daten zu hashen, für die keine Entschlüsselung erforderlich ist.

Während der Erstinstallation werden Sie aufgefordert, Commerce entweder einen eigenen Verschlüsselungsschlüssel generieren zu lassen oder einen eigenen einzugeben. Mit dem Verschlüsselungsschlüssel-Tool können Sie den Schlüssel nach Bedarf ändern. Der Verschlüsselungsschlüssel sollte regelmäßig geändert werden, um die Sicherheit zu verbessern, und der ursprüngliche Schlüssel kann jederzeit gefährdet sein.

Technische Informationen finden Sie unter [Erweiterte lokale Installation](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) im _Installationshandbuch_.

>[!IMPORTANT]
>
>Bevor Sie diese Anweisungen zum Ändern des Verschlüsselungsschlüssels befolgen, stellen Sie sicher, dass auf die folgende Datei geschrieben werden kann: `[your store]/app/etc/env.php`

**So ändern Sie einen Verschlüsselungsschlüssel:**

Für die folgenden Anweisungen ist der Zugriff auf ein Terminal erforderlich.

1. Aktivieren [Wartungsmodus](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/setup/application-modes#maintenance-mode).

   ```bash
   bin/magento maintenance:enable
   ```

1. Deaktivieren Sie Cron-Aufträge.

   _Cloud-Infrastrukturprojekte:_

   ```bash
   ./vendor/bin/ece-tools cron:disable
   ```

   _On-Premise-Projekte_

   ```bash
   crontab -e
   ```

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

   ![Systemverschlüsselungsschlüssel](./assets/encryption-key.png){width="700" zoomable="yes"}

1. Führen Sie einen der folgenden Schritte aus:

   - Um einen neuen Schlüssel zu generieren, setzen Sie **[!UICONTROL Auto-generate Key]** auf `Yes`.
   - Um einen anderen Schlüssel zu verwenden, setzen Sie **[!UICONTROL Auto-generate Key]** auf `No`. Geben Sie dann im Feld **[!UICONTROL New Key]** den zu verwendenden Schlüssel ein.

1. Klicken Sie auf **[!UICONTROL Change Encryption Key]**.

   >[!NOTE]
   >
   >Verwahren Sie den neuen Schlüssel an einem sicheren Ort auf. Es ist erforderlich, die Daten zu entschlüsseln, wenn Probleme mit Ihren Dateien auftreten.

1. Leeren Sie den Cache.

   _Cloud-Infrastrukturprojekte:_

   ```bash
   magento-cloud cc
   ```

   _On-Premise-Projekte:_

   ```bash
   bin/magento cache:flush
   ```

1. Aktivieren Sie Cron-Aufträge.

   _Cloud-Infrastrukturprojekte:_

   ```bash
   ./vendor/bin/ece-tools cron:enable
   ```

   _On-Premise-Projekte:_

   ```bash
   crontab -e
   ```

1. Deaktivieren Sie den Wartungsmodus.

   ```bash
   bin/magento maintenance:disable
   ```
