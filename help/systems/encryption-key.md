---
title: Verschlüsselungsschlüssel
description: Erfahren Sie, wie Sie Ihren eigenen Verschlüsselungsschlüssel ändern. Dies sollte regelmäßig erfolgen, um die Sicherheit zu verbessern.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 4968c40cd6f8a47ea595db20ed5d77c11e134db6
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# Verschlüsselungsschlüssel

>[!NOTE]
>
>Wenn Sie versucht haben, diese Schritte auszuführen und Probleme haben, lesen Sie den Artikel [Fehlerbehebung bei der Rotation von Verschlüsselungsschlüsseln: CVE-2024-34102](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/troubleshooting-encryption-key-rotation-cve-2024-34102) Knowledge Base“.

Adobe Commerce und Magento Open Source verwenden zum Schutz von Passwörtern und anderen sensiblen Daten einen Verschlüsselungsschlüssel. Ein [!DNL ChaCha20-Poly1305]-Algorithmus nach Industriestandard wird mit einem 256-Bit-Schlüssel verwendet, um alle Daten zu verschlüsseln, die verschlüsselt werden müssen. Dazu gehören Kreditkartendaten und Passwörter für die Integration (Zahlungs- und Versandmodul). Darüber hinaus wird ein starker sicherer Hash-Algorithmus (SHA-256) verwendet, um alle Daten zu hashen, für die keine Entschlüsselung erforderlich ist.

Während der Erstinstallation werden Sie aufgefordert, Commerce entweder einen eigenen Verschlüsselungsschlüssel generieren zu lassen oder einen eigenen einzugeben. Mit dem Verschlüsselungsschlüssel-Tool können Sie den Schlüssel nach Bedarf ändern. Der Verschlüsselungsschlüssel sollte regelmäßig geändert werden, um die Sicherheit zu verbessern, und der ursprüngliche Schlüssel kann jederzeit gefährdet sein.

Technische Informationen finden Sie unter [Erweiterte lokale Installation](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) im _Installationshandbuch_ und [Datenwiederverschlüsselung](https://developer.adobe.com/commerce/php/development/security/data-encryption/) im _PHP-Entwicklerhandbuch_.

>[!IMPORTANT]
>
>- Bevor Sie diese Anweisungen zum Ändern des Verschlüsselungsschlüssels befolgen, stellen Sie sicher, dass auf die folgende Datei geschrieben werden kann: `[your store]/app/etc/env.php`
>- Die Funktion zum Ändern des Verschlüsselungsschlüssels in den Admin-Einstellungen ist veraltet und wurde in 2.4.8 entfernt. Sie müssen den auf dieser Seite beschriebenen CLI-Befehl verwenden, um den Verschlüsselungsschlüssel nach der Aktualisierung auf 2.4.8 zu ändern.
>- Durch Drehen des Verschlüsselungsschlüssels werden sofort alle Kunden- und Admin-Sitzungen ungültig (mit Ausnahme der Integrationsbenutzer) und sie müssen sich erneut anmelden.

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

1. Ändern Sie den Verschlüsselungsschlüssel mit einer der folgenden Methoden.

   +++CLI-Befehl

   Bestätigen Sie, dass der neue Befehl vorhanden ist:

   ```bash
   bin/magento list | grep encryption:key:change
   ```

   Es sollte folgende Ausgabe angezeigt werden:

   ```bash
   encryption:key:change Change the encryption key inside the env.php file.
   ```

   Wenn Sie diese Ausgabe sehen, führen Sie den folgenden CLI-Befehl aus und stellen Sie sicher, dass er fehlerfrei abgeschlossen wird. Wenn Sie bestimmte Systemkonfigurationswerte oder Zahlungsfelder erneut verschlüsseln müssen, lesen Sie das detaillierte [Handbuch zur erneuten Verschlüsselung](https://developer.adobe.com/commerce/php/development/security/data-encryption/) im _PHP-Entwicklerhandbuch_.

   ```bash
   bin/magento encryption:key:change
   ```

   +++

   +++Admin-Einstellungen

   >[!IMPORTANT]
   >
   >Diese Funktion ist veraltet und wurde in 2.4.8 entfernt. Adobe empfiehlt, die Verschlüsselungsschlüssel über die CLI zu ändern.

   1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

      ![Systemverschlüsselungsschlüssel](./assets/encryption-key.png){width="700" zoomable="yes"}

   1. Führen Sie einen der folgenden Schritte aus:

      - Um einen neuen Schlüssel zu generieren, setzen Sie **[!UICONTROL Auto-generate Key]** auf `Yes`.
      - Um einen anderen Schlüssel zu verwenden, setzen Sie **[!UICONTROL Auto-generate Key]** auf `No`. Geben Sie dann im Feld **[!UICONTROL New Key]** den zu verwendenden Schlüssel ein.

   1. Klicken Sie auf **[!UICONTROL Change Encryption Key]**.

      >[!NOTE]
      >
      >Verwahren Sie den neuen Schlüssel an einem sicheren Ort auf. Es ist erforderlich, die Daten zu entschlüsseln, wenn Probleme mit Ihren Dateien auftreten.

   +++

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
