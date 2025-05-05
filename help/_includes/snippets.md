---
title: Snippets
description: Reused notes and visual elements to note a feature or page applying to a specific edition
source-git-commit: e82b979ee2c5f51caba6a2aa416c5f20dbce110a
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---

# Snippets

## EE only feature {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce-Funktion" src="../assets/adobe-logo.svg" width="20" height="20" /> Exklusive Funktion nur in Adobe Systems Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=de#product-editions">Weitere Informationen</a>)</td></tr>
</table>

## B2B only feature {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce B2B feature" src="../assets/b2b.svg" width="20" height="20" /> Exclusive feature available only with <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=de">Adobe Commerce B2B</a></td></tr>
</table>

## Nur CE-Funktion {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Funktion Magento Open Source" src="../assets/open-source.svg" width="20" height="20" /> Für Magento Open Source ist eine alternative Methode erforderlich (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=de#product-editions">Weitere Informationen</a>)</td></tr>
</table>

## Hinweis zur IMS-Administratorauthentifizierung {#ims-admin-note}

>[!NOTE]
>
>Adobe Systems Commerce-Händler, die über eine Adobe ID verfügen und eine optimierte Log-in für die Adobe Systems Commerce und Adobe Systems Unternehmen Produkten wünschen, können die Commerce-Admin-Authentifizierung in die Adobe Systems IMS-Authentifizierungs-arbeitsablauf integrieren. Nachdem diese Integration für Ihre Commerce-Geschäft aktiviert wurde, muss jeder Admin-User seine Adobe Systems-Anmeldeinformationen – nicht seine Commerce Konto-Anmeldeinformationen – für die Anmeldung verwenden. Weitere Informationen finden Sie unter [Integrieren von Adobe Systems Commerce mit Adobe Systems IMS –](/help/getting-started/adobe-ims-integration-overview.md) Übersicht.

## Hinweis zu GTag-APIs {#gtag-api-note}

>[!NOTE]
>
>Ab Version 2.4.5 wird die Integration der Google-Dienste aktualisiert, um die Verwendung der GTag-APIs zu unterstützen. GTag ist ein einheitlicher Mechanismus für die Integration mit Google Funktionen für Webseiten und unterstützt die neuesten Funktionen und Möglichkeiten für die Tracking und Verwaltung von Inhalte über Google Services. Weitere Informationen finden Sie in der [Google Analytics Entwicklerdokumentation](https://developers.google.com/analytics/devguides/collection/gtagjs).

## URL automatische Notiz zum Überspringen neu schreiben {#url-rewrite-skip}

>[!NOTE]
>
>When automatic redirects are enabled and you save a category, all product and category rewrites are generated in real time and stored in rewrite tables by default. This process could result in significant performance issues for categories with many assigned products. The solution is to change this default and skip the generation of category/products URL rewrites of products for category save. In diesem Fall werden Produktneuschreibungen nur für die kanonische Produkt-URL generiert. Weitere Informationen finden [ unter ](/help/merchandising-promotions/url-redirect-product-automatic.md) Produktweiterleitungen .

## Hinweis zu URL-Neuschreibungsparametern {#url-rewrite-params}

>[!IMPORTANT]
>
>Im Zuge der Weiterleitung werden alle in der URL angegebenen GET-Parameter aus Sicherheitsgründen entfernt.

## Neue Preisregel {#new-price-rule}

>[!NOTE]
>
>Preisregeln werden automatisch mit anderen Systemregeln verarbeitet. Processing frequency depends on the [cron configuration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=de). When you create a price rule, allow enough time for it to get into the system. WHen you are sure it is in the system, test the rule.

## Configuration settings {#config}

To access the store configuration settings, choose **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;from the_ Admin _sidebar.

## UPS API deprecation {#ups-api}

>[!IMPORTANT]
>
>Ab Juni 2024 können Adobe Systems Commerce-Händler keine Transaktionen mehr mit der aktuellen UPS-Integration durchführen. Dies liegt daran, dass die United Parcel Dienst (UPS)-APIs, die von der nativ Adobe Systems Commerce-Integration verwendet werden, das erforderliche OAuth 2.0-Sicherheitsmodell derzeit nicht unterstützen. Um die Integration zu aktivieren, erstellen Sie eine Applikation auf der UPS Entwicklerplattform[&#128279;](https://developer.ups.com/get-started), um die für OAuth 2.0 erforderlichen Anmeldeinformationen abzurufen. Verwenden Sie die neuen Anmeldeinformationen als `username` und `password` in der Commerce UPS Versandkonfiguration. Weitere Informationen zur Änderung des Sicherheitsmodells finden Sie unter [Guide_](https://developer.ups.com/oauth-developer-guide) zur Migration von Zugriffsschlüsseln im Entwicklerportal. <br/>
>
>Händler sollten [ein Qualitäts-Patch-Update](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html?lang=de) auf ihre Geschäft anwenden, um von der SOAP-API zur RESTful-API zu migrieren, die OAuth 2.0-Authentifizierungsprotokolle unterstützt.


## Verfügbare Dokumentation {#docs-links}

| Ressource Dokumentation | Beschreibung |
|----------------------- | ----------- |
| [Adobe Commerce 2.4 Admin User Guides](../landing/home.md) | Documentation and resources for merchants working in the Admin. |
| [Services for Adobe Commerce Documentation](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html?lang=de) | Dokumentation zur Unterstützung einer Sammlung von Merchandising-Services, die Händlern die Integration wichtiger Komponenten ihres Geschäfts in ihren Store erleichtern. |
| [Handbuch für Commerce in der Cloud-Infrastruktur](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html?lang=de) | Step-by-step procedures for deploying Adobe Commerce on a managed, automated hosting cloud platform. |
| [Adobe Commerce 2.4 Operational Guides](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html?lang=de) | Systems documentation about the concepts, processes, tools, and best practices to develop, deploy, and maintain Adobe Commerce on Cloud and on-premises projects. |
| [Adobe Commerce 2.4 Developer Documentation](https://developer.adobe.com/commerce/docs) | Developer-focused documentation used to customize Adobe Commerce and integrate with third-party systems. |

{style="table-layout:auto"}

## Kompatibilität B2B {#b2b-compatibility}

>[!IMPORTANT]
>
>Adobe Systems Commerce B2B Version 1.4.2+ ist kompatibel mit PHP 8.2. Wenn Sie die Commerce-Instanz auf Version 2.4.7+ aktualisieren, stellen Sie sicher, dass die Instanz die PHP-Version 8.2 verwendet, um die Kompatibilität mit der Adobe Systems Commerce-Version B2B zu gewährleisten. Darüber hinaus unterstützt die Version B2B 1.4.2+ die [GraphQL-Anwendung nicht Server](https://experienceleague.adobe.com/de/docs/commerce-operations/performance-best-practices/concepts/application-server).
