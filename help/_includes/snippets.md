---
title: Snippets
description: Wiederverwendete Notizen und visuelle Elemente zur Notiz eines Features oder einer Seite, die auf eine bestimmte Bearbeitung angewendet wird
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Snippets

## Funktion nur anzeigen {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce-Funktion" src="../assets/adobe-logo.svg" width="20" height="20" /> Exklusive Funktion nur in Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Weitere Informationen</a>)</td></tr>
</table>

## Funktion nur B2B {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="B2B für Adobe Commerce-Funktion" src="../assets/b2b.svg" width="20" height="20" /> Exklusive Funktion nur verfügbar mit <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">B2B für Adobe Commerce</a></td></tr>
</table>

## Nur CE-Funktion {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Source" src="../assets/open-source.svg" width="20" height="20" /> Alternative Methode ist für die Magento Open Source erforderlich (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Weitere Informationen</a>)</td></tr>
</table>

## IMS-Admin-Authentifizierungshinweis {#ims-admin-note}

>[!NOTE]
>
>Adobe Commerce-Händler, die über eine Adobe ID verfügen und eine optimierte Anmeldung bei Adobe Commerce- und Adobe Business-Produkten wünschen, können die Commerce-Admin-Authentifizierung mit dem Adobe IMS-Authentifizierungs-Workflow integrieren. Nachdem diese Integration für Ihren Commerce-Store aktiviert wurde, muss sich jeder Admin-Benutzer mit seinen Adobe-Anmeldeinformationen, nicht mit seinen Commerce-Kontoanmeldeinformationen, anmelden. Siehe [Übersicht über die Integration von Adobe Commerce mit Adobe IMS](/help/getting-started/adobe-ims-integration-overview.md).

## Hinweis zu GTag-APIs {#gtag-api-note}

>[!NOTE]
>
>Ab Version 2.4.5 wird die Google Services-Integration aktualisiert, um die Verwendung der GTag-APIs zu unterstützen. GTag ist ein einheitlicher Integrationsmechanismus mit Google-Funktionen für Web-Seiten und unterstützt die neuesten Funktionen und Möglichkeiten zum Tracking und Verwalten von Inhalten über Google Services. Weitere Informationen finden Sie in der [Entwicklerdokumentation für Google Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

## URL-Neuschreibungs-automatische Notiz überspringen {#url-rewrite-skip}

>[!NOTE]
>
>Wenn automatische Weiterleitungen aktiviert sind und Sie eine Kategorie speichern, werden alle Produkt- und Kategorieumschreibungen in Echtzeit generiert und standardmäßig in Umschreibungstabellen gespeichert. Dieser Prozess kann bei Kategorien mit vielen zugewiesenen Produkten zu erheblichen Leistungsproblemen führen. Die Lösung besteht darin, diese Standardeinstellung zu ändern und die Erstellung von Kategorie-/Produkt-URL-Neuschreibungen von Produkten für die Kategoriespeicherung zu überspringen. In diesem Fall werden Produktneuschreibungen nur für die kanonische Produkt-URL generiert. Siehe [Automatische Produktumleitungen](/help/merchandising-promotions/url-redirect-product-automatic.md) für weitere Informationen.

## Hinweis zu URL-Neuschreibungsparametern {#url-rewrite-params}

>[!IMPORTANT]
>
>Bei der Weiterleitung werden alle in der URL angegebenen GET-Parameter aus Sicherheitsgründen entfernt.

## Neue Preisregel {#new-price-rule}

>[!NOTE]
>
>Preisregeln werden automatisch mit anderen Systemregeln verarbeitet. Die Verarbeitungsfrequenz hängt von den [Cron-Konfiguration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html). Wenn Sie eine Preisregel erstellen, warten Sie, bis sie in das System aufgenommen wurde. Testen Sie die Regel, wenn Sie sicher sind, dass sie sich im System befindet.

## Konfigurationseinstellungen {#config}

Um auf die Store-Konfigurationseinstellungen zuzugreifen, wählen Sie **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**vom_ Admin _Seitenleiste.

## Einstellung der UPS-API {#ups-api}

>[!IMPORTANT]
>
>Ab Juni 2024 können Adobe Commerce-Händler keine Transaktionen mehr mit der aktuellen UPS-Integration ausführen. Dies liegt daran, dass die von der nativen Adobe Commerce-Integration verwendeten United Parcel Service (UPS)-APIs derzeit das erforderliche OAuth 2.0-Sicherheitsmodell nicht unterstützen. Weitere Informationen zu dieser Änderung finden Sie unter [_Migrationshandbuch für den Zugriffsschlüssel des Entwicklerportals_](https://developer.ups.com/oauth-developer-guide). <br/>
>
>Händler sollten [Anwenden eines Quality Patch-Updates](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html) zu ihrem Speicher hinzufügen, um von der SOAP-API zur RESTful-API zu migrieren, die OAuth 2.0-Authentifizierungsprotokolle unterstützt.


## Verfügbare Dokumentation {#docs-links}

| Dokumentationsressource | Beschreibung |
|----------------------- | ----------- |
| [Adobe Commerce 2.4-Händlerdokumentation](../landing/home.md) | Händlerorientierte Dokumentation für Adobe Commerce und Magento Open Source |
| [Dokumentation zu Services für Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) | Dokumentation zur Unterstützung einer Reihe von Services, die Händlern die Integration wichtiger Komponenten ihres Unternehmens in ihren Shop erleichtern. |
| [Handbuch zu Commerce in Cloud-Infrastrukturen](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | Schrittweise Anleitungen für die Bereitstellung von Adobe Commerce auf einer verwalteten, automatisierten Hosting-Cloud-Plattform. |
| [Adobe Commerce 2.4 - Betriebshandbücher](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Systemdokumentation zu den Konzepten, Prozessen, Tools und Best Practices für die Entwicklung, Bereitstellung und Wartung von Projekten, die auf Adobe Commerce- und Magento Open Source-Plattformen bereitgestellt werden. |
| [Entwicklerdokumentation zu Adobe Commerce 2.4](https://developer.adobe.com/commerce/docs) | Entwicklerorientierte Dokumentation zum Erstellen und Anpassen von Adobe Commerce oder Magento Open Source |

{style="table-layout:auto"}
