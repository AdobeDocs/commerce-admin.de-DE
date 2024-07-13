---
title: Anmeldedaten und URLs
description: Erfahren Sie mehr über die Commerce-URLs und Kontoanmeldeinformationen, mit denen Sie Zugriff auf Ihren Administrator und Ihre Storefront erhalten.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Anmeldedaten und URLs

Bevor Sie mit der Einrichtung und Konfiguration fortfahren, stellen Sie sicher, dass Sie über die erforderlichen Informationen verfügen, um auf den Administrator Ihres Stores und Ihr Commerce-Konto zuzugreifen.

## Storefront-URL

Die Adresse für Ihre [Storefront](storefront.md) ist normalerweise die Domäne, die Ihrer IP-Adresse zugewiesen ist. Einige Stores werden im Stammverzeichnis oder am obersten Speicherort installiert. Andere werden in einem Ordner unter dem Stammverzeichnis installiert. Der Speicher befindet sich möglicherweise in einer Subdomäne, die mit einer primären Domäne verknüpft ist. Die URL für Ihren Store könnte wie eine der folgenden aussehen:

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`s

Wenn Sie noch keine Domäne haben, enthält Ihre Store-URL eine Reihe von vier Zahlen, die jeweils durch einen Punkt in der _gepunkteten quad_ -Notation getrennt sind.

## Admin-URL

Die Adresse für Ihren Store [Admin](admin.md) wird während der Installation eingerichtet. Die Standardadresse entspricht der Ihres Stores, am Ende jedoch mit `/admin` . Obwohl die Beispiele in diesem Handbuch das Standardverzeichnis verwenden, empfiehlt es sich, Ihren Administrator von einem Speicherort aus auszuführen, der für Ihren Store eindeutig ist.

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce] account

Ihr [Commerce-Konto](commerce-account-create.md) bietet Zugriff auf Informationen zu Ihren Produkten und Diensten, Kontoeinstellungen, Abrechnungsverlauf und Support-Ressourcen. Um auf Ihr Konto zuzugreifen, navigieren Sie zur Commerce-Haupt-Site und klicken Sie oben rechts auf **[!UICONTROL My Account]** .

## Kundenkonto

Während Sie sich in der Umgebung des Stores zurechtfinden, stellen Sie sicher, dass Sie ein Test [Kundenkonto](../customers/account-dashboard.md) einrichten, damit Sie den Speicher- und Checkout-Prozess aus der Sicht des Kunden erleben können.

## Beispieldaten

Adobe bietet einen Beispieldatensatz mit einem Beispielspeicher mit mehr als 250 Produkten (davon sind rund 200 konfigurierbare Produkte), Kategorien, Preisregeln für Werbeaktionen, CMS-Seiten, Banner usw. Beispieldaten verwenden das Design _Luma_ auf der Storefront. [Die Installation dieser Beispieldaten](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html) ist optional, kann aber beim Testen und Entwickeln von Anpassungen für Ihr E-Commerce-Geschäft hilfreich sein.
