---
title: Katalogsuche - Übersicht
description: Erfahren Sie mehr über die Schnellsuche- und erweiterten Suchwerkzeuge, mit denen Kunden Produkte in der Storefront finden können.
exl-id: a796fa48-212a-47c7-ab6e-98edd4d040f4
feature: Catalog Management, Search
source-git-commit: 65d295694e13be2e0a0de29b8b396faa9f2c9cd4
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# Katalogsuche - Übersicht

>[!TIP]
>
>[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) bietet ein schnelles, superrelevantes und intuitives Sucherlebnis und ist für Adobe Commerce kostenlos verfügbar. In diesem Abschnitt wird die Standardsuchfunktion beschrieben, die von [!DNL Live Search] abweichen kann.

Untersuchungen zeigen, dass Personen, die die Suche verwenden, mit höherer Wahrscheinlichkeit einen Kauf tätigen als Kunden, die sich allein auf die Navigation verlassen. Tatsächlich ist es nach einigen Studien fast doppelt so wahrscheinlich, dass Menschen, die die Suche verwenden, einen Kauf tätigen.

In den folgenden Abschnitten werden die grundlegenden Katalogsuchfunktionen beschrieben. Informationen dazu, wie Sie die nativen Katalogsuchfunktionen konfigurieren und anpassen können, finden Sie unter:

- [Katalogsuche konfigurieren](search-configuration.md)
- [Suchergebnisse](search-results.md)
- [Suchbegriffe verwalten](search-terms.md)

>[!NOTE]
>
>Die native Suchfunktion in Commerce bietet exakte Suchergebnisse. Während [!DNL Live Search], ein optionales Modul, das in Adobe Commerce installiert und aktiviert werden kann, unterschiedlich implementiert ist und das Ergebnis nicht auf die exakte Suchzeichenfolge beschränkt ist. Wenn Sie beispielsweise zehn Produkte numerisch für _Omega_ beschriftet haben: Eine Suche nach `Omega 1` führt zu einer einzelnen Übereinstimmung für _Omega 1_ mit der nativen Suchfunktion. Dieselbe Suchzeichenfolge, die von der Live-Suche unterstützt wird, führt jedoch zu einer Übereinstimmung für mehrere Elemente, _Omega 1_ und _Omega 10_.

## Schnellsuche

>[!NOTE]
>
>Wenn [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview) installiert ist und das Widget [[!DNL Storefront Popover]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/storefront-popover) aktiviert ist, gibt das Suchfeld &quot;Suche beim Eingeben&quot;zurück, was zu einem Popup-Fenster führt.

Das Suchfeld in der Kopfzeile des Stores hilft Besuchern, Produkte in Ihrem Katalog zu finden. Der Suchtext kann der vollständige oder teilweise Produktname oder ein beliebiges anderes Wort oder eine Wortgruppe sein, das bzw. die das Produkt beschreibt. Die Suchbegriffe, die Personen zum Suchen von Produkten verwenden, können vom Administrator verwaltet werden.

1. Für **[!UICONTROL Search]** gibt der Kunde die ersten Buchstaben des gesuchten Inhalts ein.

   Alle Übereinstimmungen im Katalog werden unten mit der Anzahl der gefundenen Ergebnisse angezeigt.

1. Der Kunde drückt die Eingabetaste oder klickt in der Liste der entsprechenden Produkte auf ein Ergebnis.

   ![Suche](./assets/storefront-search-box.png){width="700" zoomable="yes"}

## Erweiterte Suche

>[!NOTE]
>
>Die hier beschriebene erweiterte Formularsuchfunktion gilt nicht für [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

Mit der erweiterten Suche können Käufer den Katalog anhand der in einem Formular eingegebenen Werte durchsuchen. Da das Formular mehrere Felder enthält, kann eine einzelne Suche mehrere Parameter enthalten. Das Ergebnis ist eine Liste aller Produkte im Katalog, die den Kriterien entsprechen. Ein Link zur erweiterten Suche befindet sich in der Fußzeile Ihres Stores.

![Erweiterte Suche](./assets/storefront-search-advanced.png){width="700" zoomable="yes"}

Jedes Feld im Formular entspricht einem Attribut aus Ihrem Produktkatalog. Um ein Feld hinzuzufügen, setzen Sie die Frontend-Eigenschaften des Attributs auf `Include in Advanced Search`. Als Best Practice empfiehlt es sich, nur die Felder einzuschließen, die Kunden am ehesten verwenden, um ein Produkt zu finden, da zu viele die Suche verlangsamen.

1. In der Fußzeile des Stores klickt der Kunde auf **[!UICONTROL Advanced Search]**.

1. Fügt im Formular _Erweiterte Suche_ vollständige oder teilweise Werte in so vielen Feldern wie nötig hinzu.

1. Klicken Sie auf **[!UICONTROL Search]** , um die Ergebnisse anzuzeigen.

   ![Suchergebnisse](./assets/storefront-search-advanced-results-modify.png){width="700" zoomable="yes"}

1. Wenn der Kunde nicht sieht, wonach er in den Suchergebnissen sucht, klickt er auf **[!UICONTROL Modify your search]** und versucht eine andere Kombination von Kriterien.
