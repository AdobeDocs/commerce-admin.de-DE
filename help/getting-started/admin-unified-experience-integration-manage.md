---
title: Verwalten der Experience Cloud-Integration
description: Erfahren Sie, wie Sie die Experience Cloud-Integration verwalten und Probleme beheben können.
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 0%

---

# Verwalten der Experience Cloud-Integration

{{$include /help/_includes/admin-unified-experience-beta-note.md}}

Nach der ersten Aktivierung können Sie den Status der Experience Cloud-Integration verwalten, indem Sie die Commerce Admin Unified Experience-Erweiterung aktivieren oder deaktivieren.

- Wenn die Erweiterung &quot;Commerce Admin Unified Experience&quot;aktiviert ist und Administratorkonten [richtig bereitgestellt](#manage-admin-user-accounts), können Commerce-Administratoren verfügbare Commerce-Projekte aus Adobe Experience Cloud anzeigen und aufrufen. Administratoren können weiterhin über die Admin-URL für die Commerce-Projektumgebung auf einzelne Projekte zugreifen.

- Wenn die Erweiterung &quot;Commerce Admin Unified Experience&quot;deaktiviert ist, ist der Zugriff über Experience Cloud deaktiviert. Administratoren müssen sich mit der Admin-URL für die Commerce-Projektumgebung bei einzelnen Projekten anmelden.

>[!WARNING]
>
>Wenn die Integration des Adobe Identity Management Service (IMS) deaktiviert ist, wird die Experience Cloud-Integration automatisch deaktiviert.

## Integration über den Administrator verwalten

1. Öffnen Sie über den Commerce Admin das Menü Speicherkonfiguration , indem Sie **[!UICONTROL Stores]** Wählen Sie im linken Navigationsmenü die Option **[!UICONTROL Configuration]**.

1. Wählen Sie im Menü Konfiguration die Option **[!UICONTROL Advanced > Admin]** und erweitern Sie dann die **[!UICONTROL Unified Experience option]**.

   ![Admin Store-Konfiguration für Experience Cloud-Integration](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. Aktivieren oder deaktivieren Sie die Integration, indem Sie die **[!UICONTROL Enable]** -Wert.

1. Ändern Sie den Projektnamen, der im Arbeitsbereich &quot;Commerce-Projekte&quot;angezeigt wird, indem Sie die **[!UICONTROL Project Name]** -Wert.

1. Speichern Sie die Konfiguration.

1. Löschen Sie den Cache.

## Integration mithilfe der Adobe Commerce-CLI verwalten

Commerce-Systemadministratoren mit Administratorzugriff auf das Commerce-Cloud-Projekt können Adobe Commerce-CLI-Befehle verwenden, um die Experience Cloud-Integration zu verwalten.

1. Melden Sie sich in Ihrer lokalen Entwicklungsumgebung beim Cloud-Projekt an.

   ```bash
   magento-cloud login
   ```

1. Stellen Sie im Stammverzeichnis Ihrer Cloud-Projektumgebung eine Verbindung zum Commerce-Anwendungsserver her.

   ```bash
   ssh magento-cloud
   ```

1. Überprüfen Sie den Status der Admin Unified Experience-Erweiterung:

   ```bash
   bin/magento admin:uex:status
   ```

1. Ändern Sie den Status der Erweiterung, um die Integration zu deaktivieren

   - **Aktivieren**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **Deaktivieren**—`bin/magento config:set admin/unified_experience/enabled 0`

## Verwalten von Admin-Benutzerkonten

Alle Commerce Admin-Benutzer müssen sowohl über ein Admin-Konto in der Commerce-Instanz als auch über ein Adobe-Benutzerkonto (Adobe ID) verfügen, um auf Adobe-Produkte und -Dienste zugreifen zu können. Beide Konten müssen derselben E-Mail-Adresse zugeordnet sein.

- **Commerce-Admin-Konto**—[Verwalten von Commerce-Admin-Benutzern](../systems/permissions-users-all.md) aus dem Admin für die Commerce-Instanz. Den Benutzerkonten für Commerce-Administratoren muss die Administratorrolle zugewiesen werden.

  Systemadministratoren im Commerce-Projekt können [SSH zur Verbindung mit der Remote-Umgebung](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment)und die Commerce-CLI verwenden `admin:user:create` und `admin:user:unlock` Befehle zum Hinzufügen oder Entsperren von Admin-Benutzerkonten.

- **Adobe-Benutzerkonto**—Ein Administrator der mit der Commerce-Instanz verknüpften Adobe-Organisation muss sich bei der Adobe Admin Console anmelden und die Adobe ID für jeden Commerce-Administrator der Organisation hinzufügen. Anschließend müssen sie Produktberechtigungen und Berechtigungen für den Zugriff auf die Commerce-Anwendung zuweisen. Siehe [Konfigurieren von Adobe Commerce-Benutzern in Adobe Admin Console](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console).

Administratoren, die die Konfiguration für die Experience Cloud-Integration über die Adobe Developer Console verwalten, müssen über ein Adobe-Benutzerkonto mit Systemadministrator- oder Entwicklerzugriff verfügen.

>[!NOTE]
>
>Ein Adobe ID ist ein über Adobe erstelltes Konto, das für den Zugriff auf Produkte und Dienste über Experience Cloud erforderlich ist. Commerce-Administratoren ohne Adobe ID können [ein kostenloses Konto erstellen](https://helpx.adobe.com/manage-account/using/create-update-adobe-id.html) verwenden dieselbe E-Mail-Adresse, die sie für die Anmeldung beim Commerce Admin verwenden.
