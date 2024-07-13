---
title: Adobe Experience Cloud-Integration für Commerce Admin
description: Erfahren Sie mehr über die Admin Unified Experience-Erweiterung, die Commerce mit Experience Cloud integriert, sodass Kunden von der Experience Cloud-Startseite aus auf Commerce-Projekte zugreifen können.
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: 61874f3dac4f574ad393e8ae258f3d6c56c8f37e
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Adobe Experience Cloud-Integration für Commerce

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce-Funktion" src="../assets/adobe-logo.svg" width="20" height="20" /> Ausschließliche Funktion nur in Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Mehr erfahren</a>)</td></tr>
</table>

Integrieren Sie Adobe Commerce-Projekte in Experience Cloud, indem Sie die Admin Unified Experience-Erweiterung aktivieren. Wenn die Integration aktiv ist, können Administratoren von Adobe Experience Cloud aus auf Commerce-Projekte zugreifen.

![Zugriff auf Commerce über die Experience Cloud-Startseite](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Verfügbare Commerce-Projekte anzeigen

Administratoren können Commerce-Projekte, auf die sie Zugriff haben, anzeigen, indem sie auf der Experience Cloud-Startseite die Option **[!UICONTROL Commerce]** auswählen.

![Arbeitsbereich &quot;Commerce-Projekte&quot;auf Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

Administratoren können den Admin und die Storefront für jedes Projekt über den Arbeitsbereich [!DNL Commerce Projects] öffnen und zusätzliche Informationen anzeigen.

- **Schnappschuss der Commerce Storefront-Startseite** - Momentaufnahme der Storefront-Startseite. Wenn ein Projekt mehrere Websites hat, zeigt der Schnappschuss die Startseite für die Standardsite an.

- **[Projektname](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)** - Identifiziert die Cloud-Projekungsumgebung für die Instanz. Der Projektname verwendet standardmäßig den Verzweigungsnamen [Git](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) im Cloud-Projekt. Ändern oder aktualisieren Sie den Projektnamen in den [Konfigurationseinstellungen für den einheitlichen Experience Store ](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[Storefront-URL](../stores-purchase/store-urls.md)** - Zeigt die Basis-URL für die Standardwebsite an.

- **[Umgebungstyp](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**: In einer Entwicklungs- oder Staging-Umgebung bereitgestellte Commerce-Instanzen werden mit der Beschriftung [!UICONTROL Development] oder [!UICONTROL Staging] gekennzeichnet. Instanzen ohne Beschriftung werden in einer Produktionsumgebung bereitgestellt.

- **Commerce-Administratorzugriff**: Öffnen Sie den Administrator durch Klicken auf **[!UICONTROL Open]**.

- **Storefront access**: Öffnen Sie die Storefront, indem Sie im Optionsmenü die Option **[!UICONTROL Open storefront]** auswählen.

- **Schnellzugriff zur Auswahl von Projekten** - Wählen Sie **[!UICONTROL Add to Favorites]** aus dem Optionsmenü aus, um ein Projekt zur Registerkarte [!UICONTROL Favorites] hinzuzufügen.

## Authentifizierungsfluss

Wenn die Experience Cloud-Integration aktiviert ist, verwenden Administratoren den folgenden Workflow zum Authentifizieren und Aufrufen von Commerce-Projekten.

1. Melden Sie sich über die Experience Cloud-Anmeldeseite an.

   ![Experience Cloud Anmeldeseite](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   Administratoren müssen sich mit dem Adobe-Geschäftsprofil für die mit der Commerce-Instanz verknüpfte Organisation bei Experience Cloud anmelden. Siehe [Verwalten von Adobe-Profilen](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

1. Öffnen Sie auf der Experience Cloud-Startseite die [!UICONTROL Commerce Projects workspace] durch Auswahl von **[!UICONTROL Open]**.

1. Rufen Sie den Administrator für ein Projekt auf, indem Sie **[!UICONTROL Open]** auswählen.

1. Wählen Sie auf der Adobe Commerce-Anmeldeseite **[!UICONTROL Sign in with Adobe ID]** aus, um die Authentifizierung abzuschließen und den Admin zu öffnen.

   ![Adobe Commerce-Anmeldeseite](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Weitere Informationen dazu, wie sich der Authentifizierungs-Workflow bei Aktivierung oder Deaktivierung der Experience Cloud-Integration auf den Experience Cloud-Integrations-Workflow auswirkt, finden Sie unter [Verwalten der-Integration](admin-unified-experience-integration-manage.md) .

## Voraussetzungen

- Adobe Commerce 2.4.5 oder höher
- Adobe Commerce auf Cloud-Infrastruktur
- Adobe Commerce-Erweiterungen

   - Commerce Admin Unified Experience-Erweiterung (`magento/module-unified-experience`)

     Wenn das Modul nicht in der Commerce-Instanz verfügbar ist, kann es mithilfe von Composer installiert werden.

   - [Adobe I/O-Ereignisdienst](https://developer.adobe.com/commerce/extensibility/events/): Erforderlich, um Ereignisdaten zu senden, mit denen der Administratorzugriff auf Commerce-Projekte über Experience Cloud verwaltet werden kann.

     Die Adobe I/O Events-Integration mit Commerce wird durch die Commerce Event-Erweiterung (`magento/commerce-eventing`) aktiviert, die für Adobe Commerce 2.4.4 und neuere Versionen verfügbar ist.

## Integration aktivieren

Aktivieren Sie die Integration, indem Sie die Anweisungen unter [Experience Cloud-Integration mit Commerce Admin konfigurieren](admin-unified-experience-integration-configure.md) befolgen.

>[!TIP]
>
>Wenn die Experience Cloud-Integration bereits in der Commerce-Instanz aktiviert ist, finden Sie unter [Verwalten der Experience Cloud-Integration](admin-unified-experience-integration-manage.md) weitere Informationen zum Ändern oder Aktualisieren der Konfiguration, zum Verwalten des Administratorzugriffs und zur Fehlerbehebung.
