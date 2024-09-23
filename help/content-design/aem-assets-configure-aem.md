---
title: Konfigurieren von Experience Manager Assets
description: Fügen Sie die Asset-Metadaten hinzu, die erforderlich sind, damit die AEM Assets-Integration für Commerce Assets zwischen Adobe Commerce- und Experience Manager Assets-Projekten synchronisieren kann.
feature: CMS, Media, Integration
exl-id: deb7c12c-5951-4491-a2bc-542e993f1f84
source-git-commit: 8a150c79c2e15ce5bd2cb2037f94c94f90b7a1df
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Konfigurieren von Experience Manager Assets

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Bereiten Sie die AEM as a Cloud Service-Umgebung auf die Verwaltung von Commerce-Assets vor, indem Sie die Umgebungskonfiguration aktualisieren und die Assets-Metadaten konfigurieren, um Commerce-Assets zu identifizieren und zu verwalten.

Für die Integration müssen ein benutzerdefinierter `Commerce`-Namespace und zusätzliche [Profilmetadaten](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-profiles) und [Schemadaten](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-schemas) hinzugefügt werden.

Adobe stellt eine AEM Projektvorlage bereit, um den Namespace und die Metadatenschema-Ressourcen zur as a Cloud Service-Umgebungskonfiguration von AEM Assets hinzuzufügen. Die Vorlage fügt hinzu:

- Ein [benutzerdefinierter Namespace](https://github.com/ankumalh/assets-commerce/blob/main/ui.config/jcr_root/apps/commerce/config/org.apache.sling.jcr.repoinit.RepositoryInitializer~commerce-namespaces.cfg.json), `Commerce` zur Identifizierung von Commerce-bezogenen Eigenschaften.

- Ein benutzerdefinierter Metadatentyp `commerce:isCommerce` mit der Bezeichnung `Does it exist in Commerce?` , um Commerce-Assets zu taggen, die mit einem Adobe Commerce-Projekt verknüpft sind.

- Ein benutzerdefinierter Metadatentyp `commerce:productmetadata` und eine entsprechende UI-Komponente, um eine *[!UICONTROL Product Data]* -Eigenschaft hinzuzufügen. Produktdaten enthalten die Metadateneigenschaften zum Verknüpfen eines Commerce-Assets mit Produkt-SKUs und zum Angeben der Bild-Attribute `role` und `position` für das Asset.

  ![Benutzerdefiniertes Benutzeroberflächensteuerelement für Produktdaten](./assets/aem-commerce-sku-metadata-fields-from-template.png){width="600" zoomable="yes"}

- Ein Metadatenschema-Formular mit einer Registerkarte &quot;Commerce&quot;, die die Felder `Does it exist in Adobe Commerce?` und `Product Data` zum Taggen von Commerce-Assets enthält. Das Formular bietet außerdem Optionen zum Anzeigen oder Ausblenden der Felder `roles` und `order` (Position) in der AEM Assets-Benutzeroberfläche.

  ![Registerkarte &quot;Commerce&quot;für AEM Assets-Metadatenschema-Formular](./assets/assets-configure-metadata-schema-form-editor.png){width="600" zoomable="yes"}

- Ein [Beispiel-Tag und ein genehmigtes Commerce-Asset](https://github.com/ankumalh/assets-commerce/blob/main/ui.content/src/main/content/jcr_root/content/dam/wknd/en/activities/hiking/equipment_6.jpg/.content.xml) `equipment_6.jpg`, um die anfängliche Asset-Synchronisierung zu unterstützen. Nur genehmigte Commerce-Assets können von AEM Assets mit Adobe Commerce synchronisiert werden.

Weitere Informationen zum Commerce-Assets-AEM-Projekt finden Sie unter [Bitte lesen](https://github.com/ankumalh/assets-commerce).

## Anpassen der Konfiguration der AEM Assets-Umgebung

>[!BEGINSHADEBOX]

**Voraussetzungen**

- [Zugriff auf das AEM Assets Cloud Manager-Programm und die Umgebungen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/cloud-manager#access-sysadmin-bo) mit den Rollen Programm und Bereitstellungs-Manager.

- Eine [lokale AEM Entwicklungsumgebung](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview) und Vertrautheit mit dem AEM lokalen Entwicklungsprozess.

- Verstehen Sie [AEM Projektstruktur](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) und wie Sie benutzerdefinierte Inhaltspakete mit Cloud Manager bereitstellen.

>[!ENDSHADEBOX]

### Bereitstellen des Commerce-Assets-AEM-Projekts in der AEM Assets-Authoring-Umgebung

1. Erstellen Sie bei Bedarf aus Cloud Manager Produktions- und Staging-Umgebungen für Ihr AEM Assets-Projekt.

1. Konfigurieren Sie bei Bedarf eine Bereitstellungs-Pipeline.

1. Laden Sie von GitHub den Textbausteincode aus dem [Commerce-Assets AEM Projekt](https://github.com/ankumalh/assets-commerce) herunter.

1. Installieren Sie den benutzerdefinierten Code aus Ihrer [lokalen AEM-Entwicklungsumgebung](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview) als Maven-Paket in Ihre AEM Assets-Umgebungskonfiguration oder kopieren Sie den Code manuell in die vorhandene Projektkonfiguration.

1. Übertragen Sie die Änderungen und übertragen Sie Ihre lokale Entwicklungsverzweigung in das Cloud Manager-Git-Repository.

1. Stellen Sie in Cloud Manager [Ihren Code bereit, um die AEM Umgebung zu aktualisieren](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deploying-code-with-cloud-manager).

## Konfigurieren eines Metadatenprofils

Legen Sie Standardwerte für Commerce-Asset-Metadaten fest, indem Sie ein Metadatenprofil erstellen. Wenden Sie nach der Einrichtung dieses Profil auf AEM Asset-Ordner an, um diese Standardeinstellungen automatisch zu verwenden. Diese optionale Einrichtung trägt durch die Reduzierung manueller Schritte zur Optimierung der Asset-Verarbeitung bei.

1. Wechseln Sie im Adobe Experience Manager-Arbeitsbereich zum Arbeitsbereich &quot;Inhaltsverwaltung für AEM Assets erstellen&quot;, indem Sie auf das Adobe Experience Manager-Symbol klicken.

   ![AEM Assets Authoring](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. Öffnen Sie die Administrator-Tools durch Auswahl des Hammersymbols.

   ![AEM Autorenadministrator verwaltet Metadatenprofile](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. Öffnen Sie die Profilkonfigurationsseite durch Klicken auf **[!UICONTROL Metadata Profiles]**.

1. **[!UICONTROL Create]** ein Metadatenprofil für die Commerce-Integration.

   ![AEM Autor-Admin fügt Metadatenprofile hinzu ](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. Hinzufügen einer Registerkarte für Commerce-Metadaten.

   1. Klicken Sie links auf **[!UICONTROL Settings]**.

   1. Klicken Sie im Registerkartenabschnitt auf **[!UICONTROL +]** und geben Sie dann die **[!UICONTROL Tab Name]**, `Commerce` an.

1. Fügen Sie das Feld `Does it exist in Commerce?` zum Formular hinzu und legen Sie den Standardwert auf `yes` fest.

   ![AEM Autor-Admin fügt dem Profil Metadatenfelder hinzu](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

1. Speichern Sie die Aktualisierung.

1. Wenden Sie das Metadatenprofil &quot;`Commerce integration`&quot;auf den Ordner an, in dem Commerce-Assets gespeichert sind.

   1. Wählen Sie auf der Seite [!UICONTROL  Metadata Profiles] das Commerce-Integrationsprofil aus.

   1. Wählen Sie im Aktionsmenü **[!UICONTROL Apply Metadata Profiles to Folder(s)]** aus.

   1. Wählen Sie den Ordner mit Commerce-Assets aus.

      Erstellen Sie einen Commerce-Ordner, falls er nicht vorhanden ist.

   1. Klicken Sie auf **[!UICONTROL Apply]**.

>[!TIP]
>
>Sie können Commerce-Assets beim Hochladen in die AEM Assets-Umgebung automatisch synchronisieren, indem Sie das Metadatenprofil aktualisieren und den Standardwert für das Feld _[!UICONTROL Review Status]_auf `Approved` festlegen. Der Eigenschaftstyp für das Feld `Review Status` ist `./jcr:content/metadata/dam:status`.


## Nächste Schritte

Richten Sie nach dem Aktualisieren der AEM-Umgebung Adobe Commerce ein:

1. [Installieren und Konfigurieren der AEM Assets-Integration für Commerce](aem-assets-configure-commerce.md)
2. [Aktivieren Sie die Asset-Synchronisierung, um Assets zwischen Ihrer Adobe Commerce-Projektumgebung und der AEM Assets-Projektumgebung zu übertragen.](aem-assets-setup-synchronization.md)
