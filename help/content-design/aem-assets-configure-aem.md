---
title: Installieren des AEM Assets-Pakets für Commerce
description: Fügen Sie die Asset-Metadaten hinzu, die erforderlich sind, um die AEM Assets-Integration für Commerce zum Synchronisieren von Assets zwischen Adobe Commerce- und Experience Manager Assets-Projekten zu aktivieren.
feature: CMS, Media, Integration
exl-id: deb7c12c-5951-4491-a2bc-542e993f1f84
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# Installieren des AEM Assets-Pakets

Adobe stellt `commerce-assets` eine Projektvorlage zum Hinzufügen von Commerce-Namespace- und Metadatenschema-Ressourcen zur Experience Manager Assets as a Cloud Service-Umgebungskonfiguration bereit. Stellen Sie diese Vorlage als Maven-Paket in Ihrer Umgebung bereit. Konfigurieren Sie dann die Commerce-Metadaten in der AEM Assets-Authoring-Umgebung, um die Einrichtung abzuschließen.

Die Vorlage fügt die folgenden Ressourcen zur Authoring-Umgebung von AEM Assets hinzu.

- Ein [benutzerdefinierter Namespace](https://github.com/ankumalh/assets-commerce/blob/main/ui.config/jcr_root/apps/commerce/config/org.apache.sling.jcr.repoinit.RepositoryInitializer~commerce-namespaces.cfg.json), der zur Identifizierung von Commerce-bezogenen Eigenschaften `Commerce`.

- Ein benutzerdefinierter Metadatentyp `commerce:isCommerce` mit der Bezeichnung `Eligible for Commerce`, um mit einem Adobe Commerce-Projekt verknüpfte Commerce-Assets zu taggen.

- Ein benutzerdefinierter Metadatentyp `commerce:productmetadata` und eine entsprechende UI-Komponente, um eine *[!UICONTROL Product Data]* Eigenschaft hinzuzufügen. Produktdaten enthalten die Metadateneigenschaften, um ein Commerce-Asset mit Produkt-SKUs zu verknüpfen und `role`- und `position` für das Asset anzugeben.

  ![Benutzerdefiniertes Produktdaten-Benutzeroberflächen-Steuerelement](./assets/aem-commerce-sku-metadata-fields-from-template.png){width="600" zoomable="yes"}

- Ein Metadatenschema-Formular mit einer Registerkarte &quot;Commerce&quot;, das die `Eligible for Commerce?`- und `Product Data` für das Tagging von Commerce-Assets enthält. Das Formular bietet außerdem Optionen zum Ein- oder Ausblenden der Felder `roles` und `order` (Position) in der AEM Assets-Benutzeroberfläche.

  Registerkarte ![Commerce für das Metadatenschema-Formular von AEM Assets](./assets/assets-configure-metadata-schema-form-editor.png){width="600" zoomable="yes"}

- Ein [Beispiel für getaggte und genehmigte Commerce](https://github.com/ankumalh/assets-commerce/blob/main/ui.content/src/main/content/jcr_root/content/dam/wknd/en/activities/hiking/equipment_6.jpg/.content.xml)Assets`equipment_6.jpg` zur Unterstützung der anfänglichen Asset-Synchronisierung. Nur genehmigte Commerce-Assets können von AEM Assets mit Adobe Commerce synchronisiert werden.

>[!NOTE]
>Weitere Informationen zur `commerce-assets` AEM-Projektvorlage finden Sie in der [Readme](https://github.com/ankumalh/assets-commerce).

Sie benötigen die folgenden Ressourcen und Berechtigungen, um dieses AEM-Projekt zum Aktualisieren der Umgebungskonfiguration verwenden zu können:

- [Zugriff auf das AEM Assets Cloud Manager-Programm und Umgebungen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/cloud-manager#access-sysadmin-bo) mit den Rollen „Programm“ und „Bereitstellungs-Manager“

- eine [lokale AEM-Entwicklungsumgebung](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview) und die Vertrautheit mit dem lokalen AEM-Entwicklungsprozess.

- Machen Sie sich mit der [AEM](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure)Projektstruktur und der Bereitstellung benutzerdefinierter Inhaltspakete mit Cloud Manager vertraut.

## Installieren des `commerce-assets`

1. Erstellen Sie aus der Cloud Manager bei Bedarf Produktions- und Staging-Umgebungen für Ihr AEM Assets-Projekt.

1. Konfigurieren Sie bei Bedarf eine Bereitstellungs-Pipeline.

1. Laden Sie von GitHub den Textbausteincode aus dem [Commerce-Assets AEM-Projekt](https://github.com/ankumalh/assets-commerce) herunter.

1. Installieren Sie [lokalen AEM-](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview)) den benutzerdefinierten Code als Maven-Paket in Ihrer AEM Assets-Umgebungskonfiguration oder durch manuelles Kopieren des Codes in die vorhandene Projektkonfiguration.

1. Übertragen Sie die Änderungen und pushen Sie Ihre lokale Entwicklungsverzweigung in das Cloud Manager-Git-Repository.

1. Stellen Sie in Cloud Manager [Code bereit, um die AEM-Umgebung zu aktualisieren](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deploying-code-with-cloud-manager).

## Konfigurieren eines Metadatenprofils

Legen Sie in der AEM Assets-Autorenumgebung Standardwerte für Commerce-Asset-Metadaten fest, indem Sie ein Metadatenprofil erstellen. Wenden Sie dann das neue Profil auf AEM Asset-Ordner an, um diese Standardwerte automatisch zu verwenden. Diese Konfiguration optimiert die Asset-Verarbeitung durch Reduzierung manueller Schritte.

Beim Konfigurieren des Metadatenprofils müssen Sie nur die folgenden Komponenten konfigurieren:

- Fügen Sie eine Registerkarte Commerce hinzu. Diese Registerkarte ermöglicht Commerce-spezifische Konfigurationseinstellungen, die von der Vorlage hinzugefügt werden
- Fügen Sie das Feld `Eligible for Commerce` zur Registerkarte Commerce hinzu.

Die Komponente Produktdaten-Benutzeroberfläche wird automatisch auf Grundlage der Vorlage hinzugefügt.

### Metadatenprofil einrichten

1. Melden Sie sich bei der Adobe Experience Manager-Autorenumgebung an.

1. Navigieren Sie im Adobe Experience Manager-Arbeitsbereich zum Arbeitsbereich für die Inhaltsverwaltung in AEM Assets durch Klicken auf das Adobe Experience Manager-Symbol.

   ![AEM Assets-Authoring](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. Öffnen Sie die Administrator-Tools, indem Sie auf das Hammersymbol klicken.

   ![AEM-Autoren-Admin zur Verwaltung von Metadatenprofilen](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. Öffnen Sie die Seite Profilkonfiguration , indem Sie auf **[!UICONTROL Metadata Profiles]** klicken.

1. **[!UICONTROL Create]** eines Metadatenprofils für die Commerce-Integration.

   ![AEM-Autoren-Admin fügt Metadatenprofile hinzu ](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. Fügen Sie eine Registerkarte für Commerce-Metadaten hinzu.

   1. Klicken Sie links auf **[!UICONTROL Settings]**.

   1. Klicken Sie im Abschnitt Registerkarte auf **[!UICONTROL +]** und geben Sie dann die **[!UICONTROL Tab Name]** an, `Commerce`.

1. Fügen Sie das Feld `Eligible for Commerce` zum Formular hinzu.

   ![AEM-Autoren-Admin fügt Metadatenfelder zum Profil hinzu](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

   - Klicken Sie auf **[!UICONTROL Build form]**.

   - Ziehen Sie das `Single Line text` Feld in das Formular.

   - Fügen Sie den `Eligible for Commerce` Text für die Bezeichnung hinzu, indem Sie auf **[!UICONTROL Field Label]** klicken.

   - Fügen Sie auf der Registerkarte Einstellungen den Titeltext zu **Feldbezeichnung“**.

   - Setzen Sie den Platzhaltertext auf `yes`.

   - Kopieren Sie den folgenden Wert in das Feld **[!UICONTROL Map to Property]** und fügen Sie ihn ein

     ```terminal
     ./jcr:content/metadata/commerce:isCommerce
     ```

1. Optional. Um genehmigte Commerce-Assets beim Hochladen in die AEM Assets-Umgebung automatisch zu synchronisieren, setzen Sie den Standardwert für das _[!UICONTROL Review Status]_auf der Registerkarte `Basic` auf `approved`.

1. Speichern Sie die Aktualisierung.

#### Anwenden des Metadatenprofils auf den Commerce Assets-Quellordner

1. Wählen Sie auf [!UICONTROL  Metadata Profiles] Seite das Integrationsprofil Commerce aus.

1. Wählen Sie im Menü Aktion die Option **[!UICONTROL Apply Metadata Profiles to Folders]** aus.

1. Wählen Sie den Ordner aus, der Commerce-Assets enthält.

   Erstellen Sie einen Commerce-Ordner, wenn er noch nicht vorhanden ist.

1. Klicken Sie auf **[!UICONTROL Apply]**.

## Nächster Schritt

[Installieren von Adobe Commerce-Paketen](aem-assets-configure-commerce.md)
