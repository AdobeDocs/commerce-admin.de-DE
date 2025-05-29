---
title: Anmeldedaten und URLs
description: Erfahren Sie mehr über die Commerce-URLs und Kontoanmeldeinformationen, mit denen Sie Zugriff auf Ihren Admin und Ihre Storefront erhalten.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Anmeldedaten und URLs

Bevor Sie mit der Einrichtung und Konfiguration fortfahren, stellen Sie sicher, dass Sie über die Informationen verfügen, die für den Zugriff auf die Admin Ihres Stores und Ihr Commerce-Konto erforderlich sind.

## Storefront-URL

Die Adresse für Ihre [Storefront](storefront.md) ist normalerweise die Domain, die Ihrer IP-Adresse zugewiesen ist. Einige Stores werden im Stammverzeichnis oder im obersten Verzeichnis installiert. Andere werden in einem Verzeichnis unterhalb des Stammverzeichnisses installiert. Der Store befindet sich möglicherweise in einer Subdomain, die mit einer primären Domain verknüpft ist. Die URL für Ihren Store könnte wie folgt aussehen:

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`s

Wenn Sie noch keine Domain haben, enthält Ihre Store-URL eine Reihe von vier Zahlen, die jeweils durch einen Punkt in _gepunkteten Quad“-_ getrennt sind.

## Admin-URL

Die Adresse für Ihren [ (](admin.md)) wird während der Installation eingerichtet. Die Standardadresse entspricht der Ihres Geschäfts, am Ende steht jedoch `/admin`. Obwohl in den Beispielen in diesem Handbuch das Standardverzeichnis verwendet wird, empfiehlt es sich, Ihre Admin von einem für Ihren Store eindeutigen Speicherort aus auszuführen.

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce]

Ihr [Commerce-Konto](commerce-account-create.md) bietet Zugriff auf Informationen über Ihre Produkte und Services, Kontoeinstellungen, den Rechnungsverlauf und Support-Ressourcen. Um auf Ihr -Konto zuzugreifen, gehen Sie zur Commerce-Haupt-Site und klicken Sie oben rechts auf **[!UICONTROL My Account]** .

## Kundenkonto

Richten Sie während Ihrer Lernphase im Laden unbedingt einen Test ([-Konto) ein](../customers/account-dashboard.md) damit Sie den Shop- und Kaufvorgang aus Kundensicht erleben können.

## Beispieldaten

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."}

Adobe bietet einen Beispieldatensatz mit einem Beispielspeicher mit mehr als 250 Produkten (etwa 200 davon sind konfigurierbare Produkte), Kategorien, Preisregeln für Werbeaktionen, CMS-Seiten, Bannern usw. Beispieldaten verwenden das _Luma_-Design in der Storefront. [Die Installation dieser Beispieldaten](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html?lang=de) ist optional, kann aber beim Testen und Entwickeln von Anpassungen für Ihr E-Commerce-Unternehmen hilfreich sein.
