---
title: Adobe Experience Cloud-Integration für Commerce Admin
description: Erfahren Sie mehr über die einheitliche Admin-Erlebniserweiterung , mit der Commerce mit Experience Cloud integriert wird, sodass Kundinnen und Kunden von der Experience Cloud-Startseite aus auf Commerce-Projekte zugreifen können.
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: 61874f3dac4f574ad393e8ae258f3d6c56c8f37e
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Adobe Experience Cloud-Integration für Commerce

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce-Funktion" src="../assets/adobe-logo.svg" width="20" height="20" /> Exklusive Funktion nur in Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=de#product-editions">Weitere Informationen</a>)</td></tr>
</table>

Integrieren Sie Adobe Commerce-Projekte mit Experience Cloud durch Aktivierung der einheitlichen Admin-Erlebniserweiterung. Wenn die Integration aktiv ist, können Admins über Adobe Experience Cloud auf Commerce-Projekte zugreifen.

![Zugriff auf Commerce über die Experience Cloud-Startseite](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Verfügbare Commerce-Projekte anzeigen

Admins können Commerce-Projekte, für die sie Zugriffsberechtigungen haben, anzeigen, indem sie auf der Experience Cloud-Startseite **[!UICONTROL Commerce]** auswählen.

![Arbeitsbereich Commerce-Projekte auf Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

Administratoren können die Admin und die Storefront für jedes Projekt im [!DNL Commerce Projects] Arbeitsbereich öffnen und zusätzliche Informationen anzeigen.

- **Momentaufnahme der Commerce-Storefront-**: Momentaufnahme der Storefront-Startseite. Wenn ein Projekt mehrere Websites hat, wird in der Momentaufnahme die Startseite der Standard-Website angezeigt.

- **[Projektname](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html?lang=de)**: Gibt die Cloud-Projektumgebung für die Instanz an. Der Projektname im Cloud[Projekt ist standardmäßig auf den ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html?lang=de)Git-Verzweigungsnamen“ festgelegt. Ändern oder aktualisieren Sie den Projektnamen in den [Konfigurationseinstellungen des einheitlichen Experience Store](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[Storefront URL](../stores-purchase/store-urls.md)** - Zeigt die Basis-URL für die Standard-Website an.

- **[Umgebungstyp](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html?lang=de)** - Commerce-Instanzen, die in einer Entwicklungs- oder Staging-Umgebung bereitgestellt werden, werden mit einer [!UICONTROL Development] oder [!UICONTROL Staging] Kennzeichnung gekennzeichnet. Instanzen ohne -Kennzeichnung werden in einer Produktionsumgebung bereitgestellt.

- **Commerce-Administratorzugriff**—Öffnen Sie den Administrator, indem Sie auf **[!UICONTROL Open]** klicken.

- **Storefront-Zugriff** - Öffnen Sie die Storefront, indem Sie **[!UICONTROL Open storefront]** aus dem Optionsmenü auswählen.

- **Schnellzugriff auf ausgewählte Projekte** - Wählen Sie **[!UICONTROL Add to Favorites]** aus dem Optionsmenü aus, um ein Projekt zur Registerkarte [!UICONTROL Favorites] hinzuzufügen.

## Authentifizierungsfluss

Wenn die Experience Cloud-Integration aktiviert ist, verwenden Admins den folgenden Workflow, um Commerce-Projekte zu authentifizieren und darauf zuzugreifen.

1. Melden Sie sich über die Experience Cloud-Anmeldeseite an.

   ![Experience Cloud-Anmeldeseite](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   Administratoren müssen sich mit dem Adobe-Geschäftsprofil für das Unternehmen, das mit der Commerce-Instanz verknüpft ist, bei Experience Cloud anmelden. Siehe [Verwalten von Adobe-](https://helpx.adobe.com/de/enterprise/using/manage-adobe-profiles.html).

1. Öffnen Sie auf der Experience Cloud-Startseite die [!UICONTROL Commerce Projects workspace], indem Sie **[!UICONTROL Open]** auswählen.

1. Greifen Sie auf den Administrator für ein Projekt zu, indem Sie **[!UICONTROL Open]** auswählen.

1. Wählen Sie auf der Anmeldeseite von Adobe Commerce die Option **[!UICONTROL Sign in with Adobe ID]** aus, um die Authentifizierung abzuschließen und den Administrator zu öffnen.

   ![Adobe Commerce-Anmeldeseite](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Siehe [Verwalten der Experience Cloud-Integration](admin-unified-experience-integration-manage.md) für Details dazu, wie sich der Authentifizierungs-Workflow auswirkt, wenn die Experience Cloud-Integration aktiviert oder deaktiviert wird.

## Anforderungen

- Adobe Commerce 2.4.5 oder höher
- Adobe Commerce auf Cloud-Infrastruktur
- Adobe Commerce-Erweiterungen

   - Commerce Admin Unified Experience-Erweiterung (`magento/module-unified-experience`)

     Wenn das Modul nicht in der Commerce-Instanz verfügbar ist, kann es mit dem Composer installiert werden.

   - [Adobe I/O-Ereignisdienst](https://developer.adobe.com/commerce/extensibility/events/) - Erforderlich zum Senden von Ereignisdaten, um den Administratorzugriff auf Commerce-Projekte von Experience Cloud aus zu verwalten.

     Die Integration von Adobe I/O-Ereignissen in Commerce wird durch die Commerce Event Extension (`magento/commerce-eventing`) aktiviert, die in Adobe Commerce 2.4.4 und höheren Versionen verfügbar ist.

## Integration aktivieren

Aktivieren Sie die Integration, indem Sie die Anweisungen unter [Konfigurieren der Experience Cloud-Integration mit Commerce Admin](admin-unified-experience-integration-configure.md) befolgen.

>[!TIP]
>
>Wenn die Experience Cloud-Integration bereits auf der Commerce-Instanz aktiviert ist, finden Sie unter [Verwalten der Experience Cloud-Integration](admin-unified-experience-integration-manage.md) weitere Informationen zum Ändern oder Aktualisieren der Konfiguration, Verwalten des Administratorzugriffs und zur Fehlerbehebung.
