---
title: Konfigurieren der Experience Cloud-Integration für Commerce Admin
description: Erfahren Sie, wie Sie ein Commerce-Projekt konfigurieren, um den Administratorzugriff über Experience Cloud zu ermöglichen.
hide: false
hidefromtoc: false
feature: Integration
role: Admin, Leader
exl-id: b2522d25-8255-4219-98b5-4b764430dea2
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '1130'
ht-degree: 0%

---

# Konfigurieren der Experience Cloud-Integration mit dem Commerce Admin

{{$include /help/_includes/admin-unified-experience-beta-note.md}}

Beginnen Sie mit der Experience Cloud-Integration mit Commerce Admin, indem Sie die Commerce-Anwendung so konfigurieren, dass die Erweiterungen Commerce Admin Unified Experience und Commerce Events verwendet werden.


## Voraussetzungen

- Adobe Commerce muss für die Verwendung von [Adobe IMS-Authentifizierung](../getting-started/adobe-ims-config.md)
- Kontobereitstellung und -berechtigungen - Administratoren müssen über eine [Adobe-Geschäftsprofil](https://helpx.adobe.com/enterprise/kb/introducing-adobe-profiles.html#:~:text=Adobe%20profiles%20help%20you%20manage,under%20the%20same%20email%20address) mit Zugriff auf die folgenden Ressourcen zur Konfiguration der Experience Cloud-Integration:
   - [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html)—Hinzufügen und Verwalten von Adobe-Benutzer- und Entwicklerkonten für das Unternehmen
   - [Adobe Developer-Konsole](https://developer.adobe.com/developer-console/docs/guides/getting-started/)—Entwickler- oder Systemadministratorzugriff zum Erstellen von App Builder-Projekten und Generieren der Verbindungsanmeldeinformationen und der Projektkonfiguration für die Verwendung des Adobe I/O Events-Dienstes
   - [Handel mit Cloud-Infrastrukturprojekten](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html#get-started-with-the-project-web-interface)—Installieren Sie die erforderlichen Module und konfigurieren Sie den Commerce-Anwendungsserver mithilfe der Adobe Commerce-CLI.
   - [Commerce Admin](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html)—Aktualisieren der Store-Konfiguration und Verwalten von Commerce-Benutzerkonten

## Konfigurationsübersicht

Aktivieren Sie die Integration, indem Sie die folgenden Aufgaben ausführen:

1. [Überprüfen der Commerce-Umgebung und der Anwendungskonfiguration](#check-the-commerce-environment-and-application-configuration).

1. [Aktivieren der Commerce Admin Unified Experience-Erweiterung](#enable-the-commerce-admin-unified-experience-extension).

1. [Einrichten von Adobe I/O-Ereignissen für Commerce](#set-up-adobe-io-events).

1. [Integration testen](#test-the-integration).

## Überprüfen der Commerce-Umgebung und der Anwendungskonfiguration

Bevor Sie die Experience Cloud-Integration konfigurieren, stellen Sie sicher, dass Ihr Projekt und Ihre Commerce-Anwendung die Anforderungen erfüllen.

1. Wechseln Sie auf Ihrer lokalen Workstation zum Projektverzeichnis für Ihr Commerce-Projekt.

1. Sehen Sie sich die Umgebungsverzweigung an, damit die Instanz mit Experience Cloud integriert werden kann.

1. Stellen Sie sicher, dass Adobe IMS aktiviert ist.

   - Verwenden Sie die [SSH-Zugriffs-URL](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html) für die Umgebung, um eine Verbindung zum Commerce-Anwendungsserver herzustellen.

   - Verwenden Sie in der Befehlszeile die Adobe Commerce-CLI, um den IMS-Modulstatus zu überprüfen.

     ```bash
     bin/magento admin:adobe-ims:status
     ```

   Wenn das Modul nicht aktiviert ist, [Aktivieren Sie sie mithilfe der Organisation und der Anmeldeinformationen für das IMS-Integrationsprojekt](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module). Wenn Sie nicht über die Anmeldeinformationen verfügen, [Senden eines Adobe Support-Tickets](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

1. Vergewissern Sie sich, dass sich der Admin-Benutzer mit seinem Adobe ID beim Commerce Admin anmelden kann.

   - Rufen Sie die Commerce-Admin-URL auf.

   - Wenn Sie angemeldet sind, melden Sie sich ab.

   - Stellen Sie sicher, dass der Admin-Benutzer zur Anmeldung mit seinem Adobe ID umgeleitet wird.

     ![Adobe Commerce-Anmeldung mit Adobe ID](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

1. Überprüfen Sie im Cloud-Projektverzeichnis auf Ihrer lokalen Workstation, ob die Erweiterung &quot;Commerce Admin Unified Experience&quot;installiert ist.

   ```bash
   composer show *unified-experience*
   ```

   Wenn die Erweiterung installiert ist, gibt der Composer den Namen und die Beschreibung der Erweiterung zurück.

   ```
   magento/module-unified-experience <version> Commerce module responsible for integration with Adobe Experience Cloud
   ```

   Wenn die Erweiterung nicht installiert ist, installieren Sie sie mit Composer. Übertragen Sie dann die Änderungen und stellen Sie die Cloud-Umgebung erneut bereit.

   ```
   composer require magento/module-unified-experience
   composer update
   ```

## Commerce Admin Unified Experience aktivieren

Aktivieren Sie die Commerce Admin Unified Experience-Erweiterung und melden Sie sich dann über Experience Cloud an.

>[!NOTE]
>
>Diese Anweisungen zeigen, wie ein Commerce Cloud-Projekt-Administrator die Erweiterung mithilfe der Adobe Commerce-CLI aktivieren kann. Commerce-Admin-Benutzer können die Erweiterung auch aktivieren, indem sie die [Konfigurationseinstellungen für Commerce Store](admin-unified-experience-integration-manage.md#from-the-commerce-admin).

1. Verwenden Sie im Stammverzeichnis Ihrer Cloud-Projektumgebung auf Ihrer lokalen Workstation die [Magento-Cloud-CLI-Tool](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli/cloud-cli-overview.html) , um sich beim Commerce-Anwendungsserver anzumelden.

   ```bash
   magento-cloud ssh
   ```

1. Aktivieren Sie die `magento/module-unified-experience` -Erweiterung mithilfe der Adobe Commerce-CLI:

   ```bash
   bin/magento config:set admin/unified_experience/enabled 1
   Admin Unified Experience integration is enabled
   ```

1. Löschen Sie den Cache.

   ```bash
   bin/magento cache:clean
   ```

## Einrichten von Adobe I/O-Ereignissen für Commerce

Wenn die Experience Cloud-Integration aktiviert ist, sendet der Adobe I/O Events-Dienst Commerce-Ereignisdaten an Experience Cloud, um den Administratorzugriff auf Commerce--Projekte zu verwalten. Für die Einrichtung des Dienstes muss die Adobe I/O Events for Commerce-Erweiterung aktiviert werden (`magento/commerce-eventing`) und konfigurieren Sie den Adobe I/O Events-Dienst in der Admin-Konsole.

### Commerce-Ereignisse aktivieren

Aktivieren Sie die Erweiterung Commerce Events (`magento/commerce-eventing`), um benutzerdefinierte Ereignisdaten von der Commerce-Anwendung an den Adobe I/O Events-Dienst zu senden.

>[!NOTE]
>
>Für Commerce 2.4.6 und höher ist die Commerce Events-Erweiterung standardmäßig installiert. Für Commerce-Projekte mit Commerce 2.4.5 verwenden Sie zunächst Composer zu [Installieren der Erweiterung](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce), und aktivieren Sie sie.

1. Fügen Sie in Ihrer lokalen Commerce-Projektentwicklungsumgebung die folgende Konfiguration zum `.magento.env.yaml` -Datei.

   ```yaml
   stage:
     global:
       ENABLE_EVENTING: true
     deploy:
       CRON_CONSUMERS_RUNNER:
         cron_run: true
         max_messages: 0
         consumers: []
   ```

1. Hinzufügen, Übertragen und Bereitstellen der aktualisierten `.magento.env.yaml file` in die Cloud-Umgebung.

>[!TIP]
>
>Weitere Informationen zum Konfigurieren und Verwalten von Umgebungsvariablen mit dem `.magento.env.yaml` -Datei, siehe [Umgebungsvariablen für die Bereitstellung konfigurieren](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/configure-env-yaml.html).

### Integration von Commerce-Ereignissen konfigurieren

Konfigurieren Sie die Integration von Commerce-Ereignissen, indem Sie die folgenden Aufgaben ausführen. Detaillierte Anweisungen finden Sie unter [Adobe I/O-Ereignisse für Commerce](https://developer.adobe.com/commerce/extensibility/events/project-setup/) Entwicklerdokumentation.

1. [App Builder-Projekt erstellen](https://developer.adobe.com/commerce/extensibility/events/project-setup/) um Ereignisdaten von der Commerce-Instanz zu erhalten.

   Sie benötigen Anmeldeinformationen und Konfigurationsdaten aus dem App Builder-Projekt, um die Integration in Commerce Admin zu konfigurieren.

1. Konfigurieren Sie Adobe Commerce für die Verwendung von Adobe I/O-Ereignissen.

   - [Aktualisieren der Speicherkonfigurationseinstellungen für den Adobe I/O Events-Dienst](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#begin-configuring-events-on-commerce).

   - [Ereignisanbieter zum Senden von Commerce-Ereignissen konfigurieren](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#create-an-event-provider-and-complete-the-commerce-configuration).

1. [Aktualisieren Sie das App Builder-Projekt, um Ereignisdaten von der Commerce-Instanz zu erhalten](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#subscribe-and-register-events).

   Registrieren Sie keine Ereignisse aus der Commerce-Instanz oder abonnieren Sie sie. Die Ereignisregistrierung wird an das App Builder-Projekt gesendet, wenn Sie den Ereignisanbieter für die Commerce-Anwendung konfigurieren.

   Nachdem Sie den Ereignisanbieter mit dem App Builder-Projekt verbunden haben, abonnieren Sie die `observer.uex_commerce_instance_update` -Ereignis und speichern Sie die Änderungen.

1. Um die Verbindung herzustellen, senden Sie ein Ereignis über den Ereignisanbieter an den Verbraucher.

   - Wählen Sie in der Befehlszeile des lokalen Cloud-Projektverzeichnisses Folgendes aus: [Verwenden Sie SSH, um eine Verbindung zum Commerce-Anwendungsserver herzustellen](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment).

     ```bash
     magento-cloud ssh
     ```

   - Senden Sie Ereignisdaten, indem Sie den Status der Admin Unified Experience-Erweiterung mit der Adobe Commerce-CLI überprüfen.

     ```bash
     bin/magento bin/magento admin:uex:status
     ```

### Integration testen

Vergewissern Sie sich, dass sich ein Commerce-Administrator bei Experience Cloud anmelden kann, um verfügbare Commerce-Projekte anzuzeigen und auf die Admin- und Storefront für jedes Projekt zuzugreifen.

1. [Anmelden bei Experience Cloud](https://experiencecloud.adobe.com/library) Verwendung der Adobe ID und der Organisation, die mit der Commerce-Instanz verknüpft sind.

   ![Zugriff auf Commerce-Projekte über die Experience Cloud-Startseite](./assets/admin-uex-home-page.png){width="600" zoomable="yes"}

1. Anzeigen der verfügbaren Commerce-Projekte durch Auswahl **[!UICONTROL Commerce]**.

   ![Arbeitsbereich &quot;Commerce-Projekte&quot;für Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="600" zoomable="yes"}

1. Öffnen Sie den Admin für eine Instanz, indem Sie **[!UICONTROL Open]**.

   ![Commerce-Admin-Ansicht mit aktivierter Experience Cloud-Integration](./assets/admin-dashboard.png){width="600" zoomable="yes"}

1. Stellen Sie sicher, dass Sie Admin-Aufgaben erwartungsgemäß ausführen können.

   Workflows im Commerce Admin sollten denselben Prozess verfolgen. Wenn Workflow-Änderungen oder Fehler nach der Aktivierung der Experience Cloud-Integration auftreten, wenden Sie sich an Ihren Commerce-Systemadministrator oder [Senden eines Adobe Support-Tickets](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

Nachdem Sie die Experience Cloud-Integration konfiguriert haben, stellen Sie sicher, dass die Administratorkonten ordnungsgemäß bereitgestellt wurden, um über Experience Cloud auf Commerce-Projekte zuzugreifen. Siehe [Verwalten von Admin-Benutzern](/help/getting-started/admin-unified-experience-integration-manage.md#manage-admin-user-accounts).
