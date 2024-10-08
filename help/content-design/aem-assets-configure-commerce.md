---
title: Installieren und Konfigurieren der Experience Manager Assets-Integration
description: Erfahren Sie, wie Sie [!DNL AEM Assets Integration for Adobe Commerce] auf einer Adobe Commerce-Instanz installieren und konfigurieren.
feature: CMS, Media
exl-id: 2f8b3165-354d-4b7b-a46e-1ff46af553aa
source-git-commit: 5e3de8e9b99c864e5650c59998e518861ca106f5
workflow-type: tm+mt
source-wordcount: '1131'
ht-degree: 0%

---

# Installieren und Konfigurieren der AEM Assets-Integration für Commerce

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Bereiten Sie Ihre Commerce-Umgebung auf die Verwendung der AEM Assets-Integration für Commerce vor, indem Sie die PHP-Erweiterung `aem-assets-integration` installieren. Aktualisieren Sie dann die Admin-Konfiguration, um die Kommunikation und Workflows zwischen Adobe Commerce und AEM Assets zu aktivieren.

## Systemanforderungen

Für die AEM Assets-Integration für Commerce gelten die folgenden System- und Konfigurationsanforderungen.

**Softwareanforderungen**

- Adobe Commerce 2.4.5+
- PHP 8.1, 8.2, 8.3
- Verfasser: 2.x

**Konfigurationsanforderungen**

- Adobe Commerce muss für die Verwendung der [Adobe IMS-Authentifizierung](/help/getting-started/adobe-ims-config.md) konfiguriert sein.
- Kontobereitstellung und Berechtigungen
   - [Commerce-Cloud-Projekt-Administrator](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access) - Installieren Sie die erforderlichen Erweiterungen und konfigurieren Sie den Commerce-Anwendungsserver über den Admin oder die Befehlszeile
   - [Commerce Admin](https://experienceleague.adobe.com/en/docs/commerce-admin/start/guide-overview) - Aktualisieren der Speicherkonfiguration und Verwalten von Commerce-Benutzerkonten

## Konfigurationsübersicht

Aktivieren Sie die Integration, indem Sie die folgenden Aufgaben ausführen:

1. [Installieren Sie die AEM Assets Integration-Erweiterung (`aem-assets-integration`)](#install-the-aem-assets-integration-extension).
1. [Konfigurieren Sie den Commerce Services Connector](#configure-the-commerce-services-connector), um Ihre Adobe Commerce-Instanz mit den Diensten zu verbinden, die die Übertragung von Daten zwischen Adobe Commerce und AEM Assets ermöglichen.
1. [Adobe I/O-Ereignisse für Commerce konfigurieren](#configure-adobe-io-events-for-commerce)
1. [Abrufen von Authentifizierungsberechtigungen für den API-Zugriff](#get-authentication-credentials-for-api-access)

## Installieren der AEM Assets Integration-Erweiterung

>[!BEGINSHADEBOX]

**Voraussetzung**

- Rufen Sie [repo.magento.com](https://repo.magento.com/admin/dashboard) auf, um die Erweiterung zu installieren.

  Informationen zur Schlüsselgenerierung und zum Abrufen der erforderlichen Berechtigungen finden Sie unter [Abrufen Ihrer Authentifizierungsschlüssel](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). Informationen zu Cloud-Installationen finden Sie im [Commerce on Cloud Infrastructure Guide](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/authentication-keys)

- Zugriff auf die Befehlszeile des Adobe Commerce-Anwendungsservers.

>[!ENDSHADEBOX]

Installieren Sie die neueste Version der AEM Assets Integration-Erweiterung (`aem-assets-integration`) auf einer Adobe Commerce-Instanz mit der Version Adobe Commerce 2.4.5+. Die AEM Asset-Integration wird als Composer-Metapaket vom Repository [repo.magento.com](https://repo.magento.com/admin/dashboard) bereitgestellt.

>[!BEGINTABS]

>[!TAB Cloud-Infrastruktur]

Verwenden Sie diese Methode, um die [!DNL AEM Assets Integration] -Erweiterung für eine Commerce Cloud-Instanz zu installieren.

1. Wechseln Sie auf Ihrer lokalen Workstation zum Projektverzeichnis für Ihr Adobe Commerce-Projekt in der Cloud-Infrastruktur-Projekt.

   >[!NOTE]
   >
   >Informationen zum lokalen Verwalten von Commerce-Projektumgebungen finden Sie unter [Verwalten von Verzweigungen mit der CLI](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) im _Benutzerhandbuch zu Adobe Commerce on Cloud Infrastructure_.

1. Sehen Sie sich die Umgebungsverzweigung an, die mit der Adobe Commerce Cloud-CLI aktualisiert werden soll.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Fügen Sie die AEM Assets Integration for Commerce -Erweiterung hinzu.

   ```shell
   composer require "magento/aem-assets-integration" "<version-tbd>" --no-update
   ```

1. Aktualisieren Sie Package-Abhängigkeiten.

   ```shell
   composer update "magento/aem-assets-integration"
   ```

1. Übernehmen und pushen Sie Code-Änderungen für die Dateien `composer.json` und `composer.lock`.

1. Fügen Sie die Codeänderungen für die Dateien `composer.json` und `composer.lock` hinzu, übertragen Sie sie und übertragen Sie sie in die Cloud-Umgebung.

   ```shell
   git add -A
   git commit -m "Install AEM Assets Integration extension for Adobe Commerce"
   git push origin <branch-name>
   ```

   Durch das Übermitteln der Aktualisierungen wird der [Commerce-Cloud-Bereitstellungsprozess](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) initiiert, um die Änderungen anzuwenden. Überprüfen Sie den Bereitstellungsstatus im [Bereitstellungsprotokoll](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

>[!TAB On-premise]

Verwenden Sie diese Methode, um die Erweiterung [!DNL AEM Assets Integration] für eine lokale Instanz zu installieren.

1. Verwenden Sie Composer, um Ihrem Projekt die AEM Assets Integration für Commerce-Erweiterung hinzuzufügen:

   ```shell
   composer require "magento/aem-assets-integration" --no-update
   ```

1. Aktualisieren Sie die Abhängigkeiten und installieren Sie die Erweiterung:

   ```shell
   composer update  "magento/aem-assets-integration"
   ```

1. Upgrade von Adobe Commerce:

   ```shell
   bin/magento setup:upgrade
   ```

1. Löschen Sie den Cache:

   ```shell
   bin/magento cache:clean
   ```

>[!TIP]
>
>Bei der Bereitstellung in der Produktion sollten Sie den kompilierten Code nicht löschen, um Zeit zu sparen. Sichern Sie Ihr System immer, bevor Sie Änderungen vornehmen.

>[!ENDTABS]

## Konfigurieren von Commerce Services Connector

Der Commerce Services Connector ermöglicht die Datensynchronisation und Kommunikation zwischen der Commerce-Instanz, dem Asset Rule Engine-Dienst und anderen unterstützenden Diensten.

>[!NOTE]
>
>Die Einrichtung des Commerce Services Connector ist ein einmaliger Prozess, der für die Verwendung von [Adobe Commerce SaaS-Diensten](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#availableservices) erforderlich ist. Wenn Sie den Connector bereits für einen anderen Dienst konfiguriert haben, können Sie die vorhandene Konfiguration über den Commerce-Administrator anzeigen, indem Sie **[!UICONTROL Systems]** > [!UICONTROL Services] > **[!UICONTROL Commerce Services Connector]** auswählen.

Um Daten zwischen Ihrer Adobe Commerce-Instanz und den Diensten zu übertragen, die die AEM Assets-Integration aktivieren, konfigurieren Sie den Commerce Services Connector wie folgt:

- Produktions- und Sandbox-API-Schlüssel für die Authentifizierung.
- Richten Sie einen Datenraum (SaaS-Kennung) für sicheren Cloud-Speicher ein.
- Geben Sie die IMS-Organisations-ID an, in der Ihre Commerce- und AEM Assets-Umgebungen bereitgestellt sind.

Detaillierte Anweisungen finden Sie unter [Commerce Services Connector](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#organizationid).

Nachdem Sie den Commerce Services Connector konfiguriert haben, generiert das System die SaaS-Projekt- und Datenbank-IDs, die die sichere Cloud-Speicher-Umgebung für Ihre Commerce-Services identifizieren und die IDs in der Admin-Konfiguration anzeigen. Diese Werte sind erforderlich, um den Onboarding-Prozess für die Asset-Synchronisierung abzuschließen.

![Speichern von Projekt- und Datenspeicherungs-IDs für die AEM Assets-Integration](assets/aem-saas-project-config.png){width="600" zoomable="yes"}

## Adobe I/O-Ereignisse für Commerce konfigurieren

Die AEM Assets-Integration verwendet den Adobe I/O Events-Dienst, um benutzerdefinierte Ereignisdaten zwischen der Commerce-Instanz und der Experience Cloud zu senden. Die Ereignisdaten werden zur Koordinierung der Workflows für die AEM Assets-Integration verwendet.

>[!BEGINSHADEBOX]

**Voraussetzung**

- Stellen Sie sicher, dass RabbitMQ aktiviert ist und auf Ereignisse wartet.
   - [RabbitMQ-Einrichtung für Adobe Commerce in lokalen Betrieben](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)
   - [RabbitMQ-Einrichtung für Adobe Commerce in der Cloud-Infrastruktur](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)
   - Stellen Sie sicher, dass [cron-Aufträge aktiviert sind](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration). Cron-Aufträge sind für die Kommunikation und Workflows für die AEM Assets-Integration erforderlich.

>[!NOTE]
>
> Für Projekte mit Commerce-Version 2.4.5 müssen Sie [die Adobe I/O-Module installieren](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce). Ab Commerce-Version 2.4.6 werden diese Module automatisch geladen. Für die AEM Assets-Integration für Commerce müssen Sie nur die Module installieren. Die Einrichtung von App Builder ist nicht erforderlich.

>[!ENDSHADEBOX]

### Aktivieren des Commerce Eventframework

Aktivieren Sie das Eventing-Framework über den Commerce-Administrator.

1. Navigieren Sie vom Administrator zu **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Adobe I/O Events**.

1. Erweitern Sie **[!UICONTROL Commerce events]**.

1. Setzen Sie **[!UICONTROL Enabled]** auf `Yes`.

   ![Adobe I/O Events Commerce Admin-Konfiguration - Aktivieren von Commerce-Ereignissen](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"}

1. Geben Sie den Namen des Händlers in die Felder **[!UICONTROL Merchant ID]** und den Umgebungsnamen in **[!UICONTROL Environment ID]** ein. Verwenden Sie beim Festlegen dieser Werte nur alphanumerische Zeichen und Unterstriche.

## Abrufen von Authentifizierungsberechtigungen für den API-Zugriff

Für die AEM Assets-Integration für Commerce sind OAuth-Authentifizierungsberechtigungen erforderlich, um API-Zugriff auf die Commerce-Instanz zu ermöglichen. Diese Anmeldeinformationen sind erforderlich, um API-Anfragen bei der Verwaltung von Assets mithilfe der AEM Assets-Integration zu authentifizieren.

Sie generieren die Anmeldeinformationen, indem Sie die Integration zur Commerce-Instanz hinzufügen und sie aktivieren.

### Integration zur Commerce-Umgebung hinzufügen

1. Wechseln Sie vom Administrator zu **System** > Erweiterungen > **Integrationen** und klicken Sie dann auf **Neue Integration hinzufügen**.

1. Geben Sie Informationen zur Integration ein.

   Geben Sie im Abschnitt **Allgemein** nur die Integration **Name** und **E-Mail** an. Verwenden Sie die E-Mail für ein Adobe IMS-Konto mit Zugriff auf die Organisation, in der Commerce und Experience Manager Assets bereitgestellt werden.

   ![AEM Assets-Integration für die Commerce-Admin-Konfiguration](assets/aem-add-commerce-integration.png){width="600" zoomable="yes"}

1. Überprüfen Sie Ihre Identität, indem Sie auf **Identität bestätigen** klicken.

   Das System überprüft Ihre Identität, indem es sich bei der Experience Cloud mit Ihrer Adobe-ID authentifiziert.

1. API-Ressourcen konfigurieren

   1. Klicken Sie im linken Bereich auf **[!UICONTROL API]**.

   1. Wählen Sie die externe Medienressource **[!UICONTROL Catalog > Inventory > Products > External Media]** aus.

      ![Konfiguration der Admin-Integration für API-Ressourcen](assets/aem-commerce-integration-api-resources.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save]**.

### Anmeldeinformationen generieren

Generieren Sie auf der Seite Integrationen die OAuth-Authentifizierungsberechtigungen, indem Sie für die Assets-Integration auf **Aktivieren** klicken. Sie benötigen diese Anmeldeinformationen, um das Commerce-Projekt beim Assets Rule Engine-Dienst zu registrieren und API-Anfragen zum Verwalten von Assets zwischen Adobe Commerce und AEM Assets zu senden.

1. Generieren Sie auf der Seite Integrationen die Anmeldeinformationen durch Klicken auf **[!UICONTROL Activate]**.

   ![Aktivieren der Commerce-Konfiguration für die Assets-Integration](assets/aem-activate-commerce-integration.png){width="600" zoomable="yes"}

1. Wenn Sie die API verwenden möchten, speichern Sie die Anmeldeinformationen für den Consumer-Schlüssel und das Zugriffstoken, um die Authentifizierung in Ihrem API-Client zu konfigurieren.

   ![OAuth-Anmeldeinformationen zum Authentifizieren von API-Anfragen](./assets/aem-commerce-integration-credentials.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Done]**.

>[!NOTE]
>
>Sie können auch Authentifizierungsberechtigungen mithilfe der Adobe Commerce-APIs generieren. Weitere Informationen zu diesem Vorgang und weitere Informationen zur OAuth-basierten Authentifizierung für Adobe Commerce finden Sie unter [OAuth-basierte Authentifizierung](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) in der Adobe Developer-Dokumentation.
