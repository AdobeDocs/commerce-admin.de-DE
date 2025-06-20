---
title: Snippets
description: Wiederverwendete Notizen und visuelle Elemente zur Notiz eines Features oder einer Seite, die auf eine bestimmte Bearbeitung angewendet wird
source-git-commit: 0ffeaa42e0207322da1b55a9fd6b6b2cf24ff4ba
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---

# Snippets

## Funktion nur anzeigen {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce-Funktion" src="../assets/adobe-logo.svg" width="20" height="20" /> Exklusive Funktion nur in Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Weitere Informationen</a>)</td></tr>
</table>

## Funktion nur B2B {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce B2B-Funktion" src="../assets/b2b.svg" width="20" height="20" /> Exklusive Funktion nur bei <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">Adobe Commerce B2B verfügbar</a></td></tr>
</table>

## Nur CE-Funktion {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Source-Funktion" src="../assets/open-source.svg" width="20" height="20" /> Für Magento Open Source ist eine alternative Methode erforderlich (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Weitere Informationen</a>)</td></tr>
</table>

## IMS-Administratorauthentifizierungshinweis {#ims-admin-note}

>[!NOTE]
>
>Adobe Commerce-Händler, die über eine Adobe ID verfügen und eine optimierte Anmeldung bei Adobe Commerce- und Adobe Business-Produkten wünschen, können die Commerce Admin-Authentifizierung mit dem Adobe IMS-Authentifizierungs-Workflow integrieren. Nachdem diese Integration für Ihren Commerce Store aktiviert wurde, muss sich jeder Admin-Benutzer mit seinen Adobe-Anmeldeinformationen, nicht mit seinen Commerce-Kontoanmeldeinformationen, anmelden. Siehe [Integrieren von Adobe Commerce mit Adobe IMS - Übersicht](/help/getting-started/adobe-ims-integration-overview.md).

## Hinweis zu GTag-APIs {#gtag-api-note}

>[!NOTE]
>
>Ab Version 2.4.5 wird die Google Services-Integration aktualisiert, um die Verwendung der GTag-APIs zu unterstützen. GTag ist ein einheitlicher Integrationsmechanismus mit Google-Funktionen für Web-Seiten und unterstützt die neuesten Funktionen und Möglichkeiten für das Tracking und die Verwaltung von Inhalten mit Google Services.

## URL-Neuschreibungs-automatische Notiz überspringen {#url-rewrite-skip}

>[!NOTE]
>
>Wenn automatische Weiterleitungen aktiviert sind und Sie eine Kategorie speichern, werden alle Produkt- und Kategorieumschreibungen in Echtzeit generiert und standardmäßig in Umschreibungstabellen gespeichert. Dieser Prozess kann bei Kategorien mit vielen zugewiesenen Produkten zu erheblichen Leistungsproblemen führen. Die Lösung besteht darin, diesen Standardwert zu ändern und die Neuschreibungen der Kategorie-/Produkt-URLs von Produkten zum Speichern der Kategorie zu überspringen. In diesem Fall werden Produktneuschreibungen nur für die kanonische Produkt-URL generiert. Weitere Informationen finden [ unter ](/help/merchandising-promotions/url-redirect-product-automatic.md) Produktweiterleitungen .

## Hinweis zu URL-Neuschreibungsparametern {#url-rewrite-params}

>[!IMPORTANT]
>
>Im Zuge der Weiterleitung werden alle in der URL angegebenen GET-Parameter aus Sicherheitsgründen entfernt.

## Neue Preisregel {#new-price-rule}

>[!NOTE]
>
>Preisregeln werden automatisch mit anderen Systemregeln verarbeitet. Die Verarbeitungsfrequenz hängt von der [cron-Konfiguration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html) ab. Wenn Sie eine Preisregel erstellen, warten Sie, bis sie in das System aufgenommen wurde. Testen Sie die Regel, wenn Sie sicher sind, dass sie sich im System befindet.

## Konfigurationseinstellungen {#config}

Um auf die Store-Konfigurationseinstellungen zuzugreifen, wählen Sie **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**in der Seitenleiste_ Admin _aus.

## Einstellung der UPS-API {#ups-api}

>[!IMPORTANT]
>
>Ab Juni 2024 können Adobe Commerce-Händler keine Transaktionen mehr mit der aktuellen UPS-Integration durchführen. Dies liegt daran, dass die von der nativen Adobe Commerce-Integration verwendeten United Parcel Service (UPS)-APIs derzeit das erforderliche OAuth 2.0-Sicherheitsmodell nicht unterstützen. Um die Integration zu aktivieren[ erstellen Sie eine Anwendung auf der UPS Entwicklerplattform, ](https://developer.ups.com/get-started) die für OAuth 2.0 erforderlichen Anmeldeinformationen abzurufen. Verwenden Sie die neuen Anmeldeinformationen als `username` und `password` in der Commerce UPS Versandkonfiguration. Weitere Informationen zur Änderung des Sicherheitsmodells finden Sie unter [Handbuch zur Migration des Zugriffsschlüssels für das Entwicklerportal_](https://developer.ups.com/oauth-developer-guide). <br/>
>
>Händler sollten [ein Qualitäts-Patch](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html)Update auf ihren Store anwenden, um von der SOAP-API zur RESTful-API zu migrieren, die OAuth 2.0-Authentifizierungsprotokolle unterstützt.


## Verfügbare Dokumentation {#docs-links}

| Dokumentationsressource | Beschreibung |
|----------------------- | ----------- |
| [Adobe Commerce 2.4 Admin-Benutzerhandbücher](../landing/home.md) | Dokumentation und Ressourcen für Händler, die in der Verwaltung arbeiten. |
| [Dokumentation zu Services für Adobe Commerce](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html) | Dokumentation zur Unterstützung einer Sammlung von Merchandising-Services, die Händlern die Integration wichtiger Komponenten ihres Geschäfts in ihren Store erleichtern. |
| [Handbuch zu Commerce in der Cloud-Infrastruktur](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | Schrittweise Anleitungen für die Bereitstellung von Adobe Commerce auf einer verwalteten, automatisierten Hosting-Cloud-Plattform. |
| [Adobe Commerce 2.4-Betriebshandbücher](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Systemdokumentation zu den Konzepten, Prozessen, Tools und Best Practices für die Entwicklung, Bereitstellung und Wartung von Adobe Commerce in Cloud- und lokalen Projekten. |
| [Entwicklerdokumentation zu Adobe Commerce 2.4](https://developer.adobe.com/commerce/docs) | Entwicklerorientierte Dokumentation zur Anpassung von Adobe Commerce und Integration mit Drittanbietersystemen. |

{style="table-layout:auto"}

## B2B-Kompatibilität {#b2b-compatibility}

>[!IMPORTANT]
>
>Adobe Commerce B2B ab Version 1.4.2 ist mit PHP 8.2 kompatibel. Wenn Sie die Commerce-Instanz auf Version 2.4.7 oder höher aktualisieren, stellen Sie sicher, dass die Instanz PHP Version 8.2 verwendet, um die Kompatibilität mit der Adobe Commerce B2B-Version zu gewährleisten. Darüber hinaus unterstützt die B2B-Version 1.4.2+ nicht den [GraphQL-Anwendungsserver](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).
