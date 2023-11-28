---
title: Adobe Experience Cloud-Integration für Commerce Admin
description: Erfahren Sie mehr über die Admin Unified Experience-Erweiterung, die Commerce mit Experience Cloud integriert, sodass Kunden von der Experience Cloud-Startseite aus auf Commerce-Projekte zugreifen können.
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Adobe Experience Cloud-Integration für Commerce

{{ee-feature}}

{{$include /help/_includes/admin-unified-experience-beta-note.md}}

Integrieren Sie Adobe Commerce-Projekte in Experience Cloud, indem Sie die Admin Unified Experience-Erweiterung aktivieren. Wenn die Integration aktiv ist, können Administratoren von Adobe Experience Cloud aus auf Commerce-Projekte zugreifen.

![Zugriff auf Commerce über die Experience Cloud-Startseite](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Verfügbare Commerce-Projekte anzeigen

Administratoren können Commerce-Projekte, auf die sie Zugriff haben, anzeigen, indem sie **[!UICONTROL Commerce]** von der Experience Cloud-Homepage aus.

![Arbeitsbereich &quot;Commerce-Projekte&quot;auf Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

Administratoren können den Admin und die Storefront für jedes Projekt über die [!DNL Commerce Projects] Arbeitsbereich und weitere Informationen anzeigen.

- **Snapshot der Commerce-Storefront-Startseite**—Schnappschuss der Storefront-Homepage. Wenn ein Projekt mehrere Websites hat, zeigt der Schnappschuss die Startseite für die Standardsite an.

- **[Projektname](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**—Identifiziert die Cloud-Projektumgebung für die Instanz. Der Projektname wird standardmäßig auf die [Git-Zweigname](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) im Cloud-Projekt. Ändern oder aktualisieren Sie den Projektnamen im [Einheitliche Experience Store-Konfigurationseinstellungen](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[Storefront-URL](../stores-purchase/store-urls.md)**—Zeigt die Basis-URL für die Standardwebsite an.

- **[Umgebungstyp](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**—In einer Entwicklungs- oder Staging-Umgebung bereitgestellte Commerce-Instanzen werden mit einer [!UICONTROL Development] oder [!UICONTROL Staging] Beschriftung. Instanzen ohne Beschriftung werden in einer Produktionsumgebung bereitgestellt.

- **Commerce Admin-Zugriff**- Öffnen Sie den Administrator, indem Sie auf **[!UICONTROL Open]**.

- **Storefront-Zugriff**—Öffnen Sie die Storefront durch Auswahl von **[!UICONTROL Open storefront]** aus dem Menü &quot;Optionen&quot;aus.

- **Schnellzugriff auf ausgewählte Projekte**—select **[!UICONTROL Add to Favorites]** über das Menü &quot;Optionen&quot;, um ein Projekt zum [!UICONTROL Favorites] Registerkarte.

## Authentifizierungsfluss

Wenn die Experience Cloud-Integration aktiviert ist, verwenden Administratoren den folgenden Workflow, um sich zu authentifizieren und auf Commerce-Projekte zuzugreifen.

1. Melden Sie sich über die Experience Cloud-Anmeldeseite an.

   ![Anmeldeseite von Experience Cloud](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   Administratoren müssen sich mit dem Adobe-Geschäftsprofil für die mit der Commerce-Instanz verknüpfte Organisation bei der Experience Cloud anmelden. Siehe [Adobe-Profile verwalten](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

1. Öffnen Sie auf der Experience Cloud-Startseite die [!UICONTROL Commerce Projects workspace] durch Auswahl **[!UICONTROL Open]**.

1. Rufen Sie den Administrator für ein Projekt auf, indem Sie **[!UICONTROL Open]**.

1. Wählen Sie auf der Adobe Commerce-Anmeldeseite die Option **[!UICONTROL Sign in with Adobe ID]** , um die Authentifizierung abzuschließen und den Admin zu öffnen.

   ![Adobe Commerce-Anmeldeseite](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Siehe [Verwalten der Experience Cloud-Integration](admin-unified-experience-integration-manage.md) für Informationen darüber, wie sich der Authentifizierungs-Workflow bei aktivierter oder deaktivierter Experience Cloud-Integration auswirkt.

## Voraussetzungen

- Adobe Commerce 2.4.5 oder höher
- Adobe Commerce auf Cloud-Infrastruktur
- Adobe Commerce-Erweiterungen

   - Commerce Admin Unified Experience-Erweiterung (`magento/module-unified-experience`)

     Wenn das Modul nicht in der Commerce-Instanz verfügbar ist, kann es mithilfe von Composer installiert werden.

   - [Adobe I/O-Ereignisdienst](https://developer.adobe.com/commerce/extensibility/events/)—Erforderlich zum Senden von Ereignisdaten, um den Administratorzugriff auf Commerce-Projekte über Experience Cloud zu verwalten.

     Die Adobe I/O Events-Integration mit Commerce wird durch die Commerce Event-Erweiterung (`magento/commerce-eventing`), die mit Adobe Commerce 2.4.4 und höheren Versionen verfügbar ist.

## Integration aktivieren

Aktivieren Sie die Integration, indem Sie die Anweisungen zum [Konfigurieren der Experience Cloud-Integration mit dem Commerce Admin](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>Wenn die Experience Cloud-Integration bereits in der Commerce-Instanz aktiviert ist, lesen Sie [Verwalten der Experience Cloud-Integration](admin-unified-experience-integration-manage.md) für Details zum Ändern oder Aktualisieren der Konfiguration, zum Verwalten des Administratorzugriffs und zur Fehlerbehebung.
