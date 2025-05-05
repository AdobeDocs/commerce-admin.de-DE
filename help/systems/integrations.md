---
title: Integrationen
description: Erfahren Sie, wie Sie OAuth-Anmeldeinformationen konfigurieren und die Umleitungs-URL für Drittanbieterintegrationen verwenden.
exl-id: b7632994-b07b-4cdb-b62c-79bc7a3a01c8
role: Admin, Developer
feature: System, Integration, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Integrationen

Durch die Definition einer Integration in Commerce Admin wird der Speicherort der OAuth-Anmeldeinformationen und der Umleitungs-URL für Drittanbieterintegrationen festgelegt sowie die verfügbaren API-Ressourcen identifiziert, die für die Integration erforderlich sind. Weitere Informationen zum Integrationsregistrierungsprozess finden Sie unter [OAuth-basierte Authentifizierung](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) in der Entwicklerdokumentation von Commerce.

![Integrationen](./assets/integrations.png){width="700" zoomable="yes"}

## Onboarding-Workflow

1. **Integration autorisieren** - Gehen Sie zur Seite **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**, suchen Sie die entsprechende Integration und autorisieren Sie sie.
1. **Anmeldung überprüfen und einrichten** - Wenn Sie dazu aufgefordert werden, akzeptieren Sie den angeforderten Zugriff. Wenn er zu einem Drittanbieter umgeleitet wird, melden Sie sich beim System an oder erstellen Sie ein Konto. Nach erfolgreicher Anmeldung kehren Sie zur Seite Integration zurück.
1. **Bestätigung der autorisierten Integration erhalten** - Das System sendet eine Benachrichtigung, dass die Integration erfolgreich autorisiert wurde. Nachdem Sie eine Integration eingerichtet und die Anmeldeinformationen erhalten haben, müssen Sie keine Aufrufe mehr ausführen, um auf Token zuzugreifen oder sie anzufordern.

## Hinzufügen einer Integration

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

   ![Neue Integration](./assets/integration-new.png){width="600" zoomable="yes"}

1. Geben Sie die folgenden Integrationsinformationen ein:

   - Geben Sie den **[!UICONTROL Name]** der Integration und die **[!UICONTROL Email]** des Kontakts ein.

   - Geben Sie den **[!UICONTROL Callback URL]** ein, an den OAuth-Anmeldeinformationen gesendet werden können, wenn OAuth für den Token-Austausch verwendet wird. Die Verwendung von `https://` wird dringend empfohlen.

   - Geben Sie den **[!UICONTROL Identity Link URL]** ein, um die Benutzer zu einem Drittanbieterkonto mit diesen Anmeldedaten für die Adobe Commerce- oder Magento Open Source-Integration umzuleiten.

   >[!NOTE]
   >
   > Die `Integration not secure` Warnbeschriftung wird in der Nähe jedes Integrationsnamens im [!UICONTROL Integrations] als Erinnerung angezeigt, bis HTTPS-URLs in [!UICONTROL Callback URL]- und [!UICONTROL Identity Link URL] gespeichert werden.

   - Geben Sie bei Aufforderung Ihr Kennwort ein, um Ihre Identität zu bestätigen.

1. Wählen Sie im linken Bedienfeld **[!UICONTROL API]** aus und führen Sie folgende Schritte aus:

   - Legen Sie **[!UICONTROL Resource Access]** auf eine der folgenden Einstellungen fest:

      - `All`
      - `Custom`

   - Aktivieren Sie für den benutzerdefinierten Zugriff das Kontrollkästchen jeder benötigten Ressource.

     ![Integrationen - verfügbare API](./assets/integrations-available-api.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

## Aktivieren einer Integration

Standardmäßig wird eine gespeicherte Integration im Raster mit dem Status `Inactive` angezeigt. Um sie zu aktivieren, führen Sie die folgenden Schritte aus:

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Suchen Sie die neu erstellte Integration und klicken Sie auf den Link **[!UICONTROL Activate]** .

1. Klicken Sie oben rechts auf **[!UICONTROL Allow]**.

   Diese Aktion zeigt die Integrations-Token für Erweiterungen an. Kopieren Sie diese Informationen an einen sicheren, verschlüsselten Speicherort für Ihre Integration.

   ![Integrations-Token für Erweiterungen](./assets/integration-tokens-for-extensions.png){width="600" zoomable="yes"}

1. Klicken Sie oben rechts auf **[!UICONTROL Done]**.

## Integration erneut autorisieren

Um ein neues Integrations-Zugriffstoken und ein neues Zugriffstoken-Geheimnis zu generieren, haben Sie die Integration über den Administrator erneut autorisiert:

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Suchen Sie die Integration mit dem **[!UICONTROL Active]**.

1. Klicken Sie in _[!UICONTROL Activate]_&#x200B;Spalte auf die **[!UICONTROL Reauthorize]**.

1. Klicken Sie auf **[!UICONTROL Reauthorize]** , um den Zugriff auf die API-Ressourcen zu genehmigen.

1. Speichern Sie die neuen Integrations-Token für Erweiterungen und klicken Sie auf **[!UICONTROL Done]**.

## Ändern der Sicherheitseinstellung für den API-Gastzugriff

Standardmäßig lässt das System keinen anonymen Gastzugriff auf CMS, den Katalog und andere Store-Ressourcen zu. Wenn Sie die Einstellung ändern müssen, gehen Sie wie folgt vor:

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Services]** und wählen Sie **[!UICONTROL Magento Web API]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Web API Security Setting]** .

   ![Services-Konfiguration - Web-API-Sicherheitseinstellungen](../configuration-reference/services/assets/web-api-security.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Allow Anonymous Guest Access]** auf `Yes` fest.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

Weitere Informationen finden Sie unter [Einschränken des Zugriffs auf anonyme Web-APIs](https://developer.adobe.com/commerce/webapi/rest/use-rest/anonymous-api-security/) in der Entwicklerdokumentation zu Commerce.

## Löschen einer Integration

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Suchen Sie die vorhandene Integration und klicken Sie auf das Symbol ( ![Papierkorb-](../assets/icon-delete-trashcan-solid.png)) in der Spalte **[!UICONTROL Delete]** .

1. Um Ihre Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.
