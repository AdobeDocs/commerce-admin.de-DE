---
title: Integrationen
description: Erfahren Sie, wie Sie OAuth-Anmeldeinformationen konfigurieren und die Umleitungs-URL für Drittanbieter-Integrationen konfigurieren.
exl-id: b7632994-b07b-4cdb-b62c-79bc7a3a01c8
role: Admin, Developer
feature: System, Integration, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Integrationen

Durch die Definition einer Integration in Commerce Admin werden der Speicherort der OAuth-Anmeldeinformationen und die Umleitungs-URL für Drittanbieter-Integrationen festgelegt und die verfügbaren API-Ressourcen identifiziert, die für die Integration benötigt werden. Weitere Informationen zum Integrationsregistrierungsprozess finden Sie unter [OAuth-basierte Authentifizierung](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) in der Entwicklerdokumentation von Commerce.

![Integrationen](./assets/integrations.png){width="700" zoomable="yes"}

## Onboarding-Workflow

1. **Integration autorisieren** - Gehen Sie zur Seite **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**, suchen Sie die entsprechende Integration und autorisieren Sie sie.
1. **Anmeldung überprüfen und einrichten** - Wenn Sie dazu aufgefordert werden, akzeptieren Sie den angeforderten Zugriff. Wenn Sie zu einem Drittanbieter weitergeleitet werden, melden Sie sich beim System an oder erstellen Sie ein Konto. Nach erfolgreicher Anmeldung kehren Sie zur Integrationsseite zurück.
1. **Bestätigung der autorisierten Integration erhalten** - Das System sendet eine Benachrichtigung, dass die Integration erfolgreich autorisiert wurde. Nach dem Einrichten einer Integration und Empfangen der Anmeldeinformationen ist es nicht mehr erforderlich, Aufrufe für Zugriffs- oder Anfragetoken durchzuführen.

## Integration hinzufügen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

   ![Neue Integration](./assets/integration-new.png){width="600" zoomable="yes"}

1. Geben Sie die folgenden Integrationsinformationen ein:

   - Geben Sie die **[!UICONTROL Name]** der Integration und die Kontaktadresse **[!UICONTROL Email]** ein.

   - Geben Sie den Wert **[!UICONTROL Callback URL]** ein, an den OAuth-Anmeldeinformationen gesendet werden können, wenn OAuth für den Token-Austausch verwendet wird. Die Verwendung von `https://` wird dringend empfohlen.

   - Geben Sie den Wert **[!UICONTROL Identity Link URL]** ein, um die Benutzer mit diesen Anmeldedaten für die Adobe Commerce- oder Magento Open Source-Integration an ein Drittanbieterkonto weiterzuleiten.

   >[!NOTE]
   >
   > Die Warnung `Integration not secure` wird in der Nähe jedes Integrationsnamens im Raster [!UICONTROL Integrations] als Erinnerung angezeigt, bis HTTPS-URLs in den Feldern [!UICONTROL Callback URL] und [!UICONTROL Identity Link URL] gespeichert werden.

   - Geben Sie bei Aufforderung Ihr Kennwort zur Bestätigung Ihrer Identität ein.

1. Wählen Sie im linken Bereich **[!UICONTROL API]** aus und gehen Sie wie folgt vor:

   - Setzen Sie **[!UICONTROL Resource Access]** auf einen der folgenden Werte:

      - `All`
      - `Custom`

   - Aktivieren Sie für den benutzerdefinierten Zugriff das Kontrollkästchen der jeweiligen Ressource, die benötigt wird.

     ![Integrationen - verfügbare API](./assets/integrations-available-api.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

## Aktivieren einer Integration

Standardmäßig wird eine gespeicherte Integration im Raster mit dem Status `Inactive` angezeigt. Führen Sie die folgenden Schritte aus, um sie zu aktivieren:

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Suchen Sie die neu erstellte Integration und klicken Sie auf den Link **[!UICONTROL Activate]** .

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Allow]**.

   Diese Aktion zeigt die Integrationstoken für Erweiterungen an. Kopieren Sie diese Informationen in einen sicheren, verschlüsselten Speicherort, der für die Verwendung mit Ihrer Integration verwendet werden kann.

   ![Integrationstoken für Erweiterungen](./assets/integration-tokens-for-extensions.png){width="600" zoomable="yes"}

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Done]**.

## Eine Integration erneut autorisieren

Um ein neues Integrationszugriffstoken und ein Zugriffstoken-Geheimnis zu generieren, autorisierte die Integration vom Administrator erneut:

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Suchen Sie die Integration mit dem Status **[!UICONTROL Active]** .

1. Klicken Sie in der Spalte _[!UICONTROL Activate]_auf den Wert **[!UICONTROL Reauthorize]**.

1. Klicken Sie auf **[!UICONTROL Reauthorize]** , um den Zugriff auf die API-Ressourcen zu genehmigen.

1. Speichern Sie die neuen Integrations-Token für Erweiterungen und klicken Sie auf **[!UICONTROL Done]**.

## Ändern der Sicherheitseinstellung für den API-Gastzugriff

Standardmäßig gestattet das System keinen anonymen Gastzugriff auf CMS-, Katalog- und andere Store-Ressourcen. Wenn Sie die Einstellung ändern müssen, gehen Sie wie folgt vor:

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Services]** und wählen Sie **[!UICONTROL Magento Web API]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Web API Security Setting]** .

   ![Dienstkonfiguration - Web-API-Sicherheitseinstellungen](../configuration-reference/services/assets/web-api-security.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Allow Anonymous Guest Access]** auf `Yes`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

Weitere Informationen finden Sie unter [Beschränkung des Zugriffs auf anonyme Web-APIs](https://developer.adobe.com/commerce/webapi/rest/use-rest/anonymous-api-security/) in der Commerce-Entwicklerdokumentation.

## Integration löschen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Suchen Sie die vorhandene Integration und klicken Sie in der Spalte **[!UICONTROL Delete]** auf das Symbol ( ![Papierkorbsymbol](../assets/icon-delete-trashcan-solid.png) ).

1. Klicken Sie zur Bestätigung Ihrer Aktion auf **[!UICONTROL OK]**.
