---
title: Verwalten der Experience Cloud-Integration
description: Erfahren Sie, wie Sie die Experience Cloud-Integration verwalten und Probleme beheben
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
source-git-commit: 15569794c1e66ba5a93e46206244e2951522923e
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Verwalten der Experience Cloud-Integration

Verwalten Sie nach der erstmaligen Aktivierung den Status der Experience Cloud-Integration, indem Sie die Commerce Admin Unified Experience-Erweiterung aktivieren oder deaktivieren.

- Wenn die Commerce Admin Unified Experience-Erweiterung aktiviert ist und Administratorkonten [ordnungsgemäß bereitgestellt) ](#manage-admin-user-accounts), können Commerce-Administratoren verfügbare Commerce-Projekte in Adobe Experience Cloud anzeigen und darauf zugreifen. Administratoren können weiterhin über die Admin-URL für die Commerce-Projektumgebung auf einzelne Projekte zugreifen.

- Wenn die Commerce Admin Unified Experience-Erweiterung deaktiviert ist, ist der Zugriff über Experience Cloud deaktiviert. Administratoren müssen sich mit der Admin-URL für die Commerce-Projektumgebung bei den einzelnen Projekten anmelden.

>[!WARNING]
>
>Wenn die Adobe Identity Management Service (IMS)-Integration deaktiviert ist, wird die Experience Cloud-Integration automatisch deaktiviert.

## Verwalten der Integration über den Administrator

1. Öffnen Sie in Commerce Admin das Menü Store-Konfiguration , indem Sie im linken Navigationsmenü **[!UICONTROL Stores]** auswählen und dann **[!UICONTROL Configuration]** auswählen.

1. Wählen Sie im Menü Konfiguration die Option **[!UICONTROL Advanced > Admin]** aus und erweitern Sie dann die **[!UICONTROL Unified Experience option]**.

   ![Admin Store-Konfiguration für die Experience Cloud-Integration](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. Aktivieren oder deaktivieren Sie die Integration, indem Sie den **[!UICONTROL Enable]** Wert auswählen.

1. Ändern Sie den Projektnamen, der im Arbeitsbereich &quot;Commerce-Projekte“ angezeigt wird, indem Sie den **[!UICONTROL Project Name]** hinzufügen oder aktualisieren.

1. Speichern Sie die Konfiguration.

1. Löschen Sie den Cache.

## Verwalten der Integration mithilfe der Adobe Commerce-CLI

Commerce-Systemadministratoren mit Administratorzugriff auf das Commerce-Cloud-Projekt können Adobe Commerce-CLI-Befehle verwenden, um die Experience Cloud-Integration zu verwalten.

1. Melden Sie sich in Ihrer lokalen Entwicklungsumgebung beim Cloud-Projekt an.

   ```bash
   magento-cloud login
   ```

1. Stellen Sie im Stammverzeichnis Ihrer Cloud-Projektumgebung eine Verbindung zum Commerce-Anwendungsserver her.

   ```bash
   ssh magento-cloud
   ```

1. Überprüfen Sie den Status der einheitlichen Admin-Erlebniserweiterung:

   ```bash
   bin/magento admin:uex:status
   ```

1. Ändern Sie den Status der Erweiterung, um die Integration zu deaktivieren

   - **Aktivieren**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **deaktivieren**—`bin/magento config:set admin/unified_experience/enabled 0`

## Verwalten von Admin-Benutzerkonten

Alle Commerce-Admin-Benutzenden müssen sowohl über ein Admin-Konto in der Commerce-Instanz als auch über ein Adobe-Benutzerkonto (Adobe ID) verfügen, um auf Adobe-Produkte und -Services zugreifen zu können. Beide Konten müssen mit derselben E-Mail-Adresse verknüpft sein.

- **Commerce-Administratorkonto**—[Verwalten von Commerce-Administratorbenutzenden](../systems/permissions-users-all.md) vom Administrator für die Commerce-Instanz. Benutzerkonten für Commerce-Administratoren muss die Administratorrolle zugewiesen werden.

  Systemadministratoren im Commerce-Projekt können [SSH verwenden, um eine Verbindung zur Remote-Umgebung herzustellen](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html?lang=de#connect-to-a-remote-environment) und die Commerce-CLI-`admin:user:create` und `admin:user:unlock`-Befehle verwenden, um Admin-Benutzerkonten hinzuzufügen oder zu entsperren.

- **Adobe-Benutzerkonto** - Ein Administrator für das mit der Commerce-Instanz verknüpfte Adobe-Unternehmen muss sich bei der Adobe Admin Console anmelden und die Adobe ID für jeden Commerce-Administrator zum Unternehmen hinzufügen. Anschließend müssen sie Produktberechtigungen und -berechtigungen zuweisen, um auf die Commerce-Anwendung zugreifen zu können. Siehe [Konfigurieren von Adobe Commerce-Benutzern in der Adobe Admin Console](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console).

Administratoren, die die Konfiguration für die Experience Cloud-Integration über die Adobe Developer Console verwalten, müssen über ein Adobe-Benutzerkonto mit Systemadministrator- oder Entwicklerzugriff verfügen.

>[!NOTE]
>
>Ein Adobe ID ist ein über Adobe erstelltes Konto, das erforderlich ist, um über Experience Cloud auf Produkte und Services zuzugreifen. Commerce-Administratoren ohne Adobe ID können [kostenloses Konto erstellen](https://helpx.adobe.com/de/manage-account/using/create-update-adobe-id.html) indem sie dieselbe E-Mail-Adresse verwenden, mit der sie sich bei Commerce Admin anmelden.
