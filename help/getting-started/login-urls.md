---
title: Anmeldedaten und URLs
description: Erfahren Sie mehr über die Commerce-URLs und Kontoanmeldeinformationen, mit denen Sie Zugriff auf Ihren Admin und Ihre Storefront erhalten.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---

# Anmeldedaten und URLs

Bevor Sie mit der Einrichtung und Konfiguration fortfahren, stellen Sie sicher, dass Sie über die Informationen verfügen, die für den Zugriff auf den Administrator Ihres Stores und Ihr Commerce-Konto erforderlich sind.

## Storefront-URL

Die Adresse für Ihre [storefront](storefront.md) ist normalerweise die Domäne, die Ihrer IP-Adresse zugewiesen ist. Einige Stores werden im Stammverzeichnis oder am obersten Speicherort installiert. Andere werden in einem Ordner unter dem Stammverzeichnis installiert. Der Speicher befindet sich möglicherweise in einer Subdomäne, die mit einer primären Domäne verknüpft ist. Die URL für Ihren Store könnte wie eine der folgenden aussehen:

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`s

Wenn Sie noch keine Domäne haben, enthält Ihre Store-URL eine Reihe von vier Zahlen, die jeweils durch einen Punkt in _gepunkteter Quad_ -Notation.

## Admin-URL

Die Adresse Ihres Stores [Admin](admin.md) während der Installation eingerichtet wird. Die Standardadresse entspricht der Ihres Stores, jedoch mit `/admin` am Ende. Obwohl die Beispiele in diesem Handbuch das Standardverzeichnis verwenden, empfiehlt es sich, Ihren Administrator von einem Speicherort aus auszuführen, der für Ihren Store eindeutig ist.

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce] account

Ihre [Commerce-Konto](commerce-account-create.md) bietet Zugriff auf Informationen zu Ihren Produkten und Diensten, Kontoeinstellungen, Abrechnungsverlauf und Support-Ressourcen. Um auf Ihr Konto zuzugreifen, rufen Sie die Haupt-Commerce-Site auf und klicken Sie auf **[!UICONTROL My Account]** in der oberen rechten Ecke.

## Kundenkonto

Während Sie sich in der Umgebung des Stores fortbewegen, stellen Sie sicher, dass Sie einen Test einrichten [Kundenkonto](../customers/account-dashboard.md), damit Sie den Store- und Checkout-Prozess aus der Sicht des Kunden erleben können.

## Beispieldaten

Adobe bietet einen Beispieldatensatz mit einem Beispielspeicher mit mehr als 250 Produkten (davon sind rund 200 konfigurierbare Produkte), Kategorien, Preisregeln für Werbeaktionen, CMS-Seiten, Banner usw. Beispieldaten verwenden die _Luma_ Thema auf der Storefront. [Installieren dieser Beispieldaten](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html) ist optional, kann aber beim Testen und Entwickeln von Anpassungen für Ihr E-Commerce-Geschäft hilfreich sein.
