---
title: Snippets
description: Wiederverwendete Hinweise und visuelle Elemente zum Notizen einer Funktion oder Seite, die auf eine bestimmte Bearbeitung angewendet wird
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# Snippets

## Nur Funktion {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce-Funktion" src="../assets/adobe-logo.svg" width="20" height="20" /> Ausschließliche Funktion nur in Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Mehr erfahren</a>)</td></tr>
</table>

## Nur B2B-Funktion {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce B2B-Funktion" src="../assets/b2b.svg" width="20" height="20" /> Ausschließliche Funktion nur bei <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">Adobe Commerce B2B</a> verfügbar</td></tr>
</table>

## Nur CE-Funktion {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Source" src="../assets/open-source.svg" width="20" height="20" /> Für die Magento Open Source ist eine alternative Methode erforderlich (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Mehr erfahren</a>).</td></tr>
</table>

## IMS-Administratorauthentifizierungshinweis {#ims-admin-note}

>[!NOTE]
>
>Adobe Commerce-Händler, die über eine Adobe ID verfügen und sich bei Adobe Commerce anmelden möchten, und Adobe Business-Produkte können die Commerce-Administratorauthentifizierung mit dem Adobe IMS-Authentifizierungsarbeitsablauf integrieren. Nachdem diese Integration für Ihren Commerce-Store aktiviert wurde, muss sich jeder Admin-Benutzer mit seinen Adobe-Anmeldeinformationen (nicht mit seinen Commerce-Kontoanmeldeinformationen) anmelden. Siehe [Überblick über die Integration von Adobe Commerce in Adobe IMS](/help/getting-started/adobe-ims-integration-overview.md).

## Hinweise zu GTag-APIs {#gtag-api-note}

>[!NOTE]
>
>Ab Version 2.4.5 wird die Google-Dienstintegration aktualisiert, um die Verwendung der GTag-APIs zu unterstützen. GTag ist ein einheitlicher Mechanismus für die Integration mit Google-Funktionen für Webseiten und unterstützt die neuesten Funktionen und Möglichkeiten zum Tracking und Verwalten von Inhalten über Google Services. Weitere Informationen finden Sie in der [Google Analytics-Entwicklerdokumentation](https://developers.google.com/analytics/devguides/collection/gtagjs).

## Automatische URL-Neuschreibungsnotiz zum Überspringen {#url-rewrite-skip}

>[!NOTE]
>
>Wenn automatische Umleitungen aktiviert sind und Sie eine Kategorie speichern, werden alle Produkt- und Kategorieumschreibungen in Echtzeit generiert und standardmäßig in Umschreibungstabellen gespeichert. Dieser Prozess könnte zu erheblichen Leistungsproblemen bei Kategorien mit vielen zugewiesenen Produkten führen. Die Lösung besteht darin, diesen Standard zu ändern und die Generierung von Kategorie-/Produkt-URL-Neuschreibungen von Produkten für Kategoriespeicherung zu überspringen. In diesem Fall werden Produktneuschreibungen nur für die kanonische Produkt-URL generiert. Weitere Informationen finden Sie unter [Automatische Produktumleitungen](/help/merchandising-promotions/url-redirect-product-automatic.md) .

## Hinweis zu URL-Neuschreibungsparametern {#url-rewrite-params}

>[!IMPORTANT]
>
>Bei der Weiterleitung werden alle in der URL angegebenen GET aus Sicherheitsgründen entfernt.

## Neue Preisregel {#new-price-rule}

>[!NOTE]
>
>Preisregeln werden automatisch mit anderen Systemregeln verarbeitet. Die Verarbeitungsfrequenz hängt von der [cron-Konfiguration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html) ab. Wenn Sie eine Preisregel erstellen, lassen Sie genügend Zeit, um in das System zu gelangen. Wenn Sie sicher sind, dass es sich im System befindet, testen Sie die Regel.

## Konfigurationseinstellungen {#config}

Um auf die Speicherkonfigurationseinstellungen zuzugreifen, wählen Sie **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**in der Seitenleiste_ Admin _aus.

## Einstellung der UPS-API {#ups-api}

>[!IMPORTANT]
>
>Ab Juni 2024 können Adobe Commerce-Händler nicht mehr mit der aktuellen UPS-Integration arbeiten. Dies liegt daran, dass die von der nativen Adobe Commerce-Integration verwendeten United Parcel Service-APIs (UPS) derzeit das erforderliche OAuth 2.0-Sicherheitsmodell nicht unterstützen. Weitere Informationen zu dieser Änderung finden Sie unter [_Migrationshandbuch für den Zugriffsschlüssel für Entwicklerportal_](https://developer.ups.com/oauth-developer-guide) <br/>.
>
>Händler sollten [ein Qualitäts-Patch-Update](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html) auf ihren Speicher anwenden, um von der SOAP-API zur RESTful-API zu migrieren, die OAuth 2.0-Authentifizierungsprotokolle unterstützt.


## Verfügbare Dokumentation {#docs-links}

| Dokumentationsressource | Beschreibung |
|----------------------- | ----------- |
| [Dokumentation zum Adobe Commerce 2.4-Händler](../landing/home.md) | Merchandising-fokussierte Dokumentation für Adobe Commerce |
| [Dienste für die Dokumentation zu Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) | Dokumentation zur Unterstützung einer Reihe von Diensten, die Händlern bei der Integration wichtiger Komponenten ihres Geschäfts in ihren Speicher helfen. |
| [Handbuch zu Commerce on Cloud Infrastructure](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | Schrittweise Anleitungen zur Bereitstellung von Adobe Commerce auf einer verwalteten, automatisierten Hosting-Cloud-Plattform. |
| [Adobe Commerce 2.4-Operationshandbücher](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Systemdokumentation zu Konzepten, Prozessen, Tools und Best Practices zur Entwicklung, Bereitstellung und Wartung von Adobe Commerce-Projekten. |
| [Adobe Commerce 2.4-Entwicklerdokumentation](https://developer.adobe.com/commerce/docs) | Entwicklerorientierte Dokumentation zur Anpassung von Adobe Commerce und Integration in Drittanbietersysteme |

{style="table-layout:auto"}
