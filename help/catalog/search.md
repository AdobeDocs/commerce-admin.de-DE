---
title: Übersicht über die Katalogsuche
description: Erfahren Sie mehr über die Tools für die Schnellsuche und die erweiterte Suche, die Kunden verwenden können, um Produkte in der Storefront zu finden.
exl-id: a796fa48-212a-47c7-ab6e-98edd4d040f4
feature: Catalog Management, Search
source-git-commit: 65d295694e13be2e0a0de29b8b396faa9f2c9cd4
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# Übersicht über die Katalogsuche

>[!TIP]
>
>[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) bietet ein schnelles, extrem relevantes und intuitives Sucherlebnis und ist für Adobe Commerce ohne zusätzliche Kosten verfügbar. In diesem Abschnitt wird die Standardsuchfunktion beschrieben, die sich von [!DNL Live Search] unterscheiden kann.

Untersuchungen zeigen, dass Personen, die die -Suche verwenden, mit größerer Wahrscheinlichkeit einen Kauf tätigen als Kunden, die nur auf die Navigation angewiesen sind. Tatsächlich tätigen Menschen, die die Suche nutzen, laut einigen Studien mit fast doppelt so hoher Wahrscheinlichkeit einen Kauf.

In den folgenden Abschnitten werden die grundlegenden Funktionen der Katalogsuche beschrieben. Informationen dazu, wie Sie die nativen Katalogsuchfunktionen konfigurieren und anpassen können, finden Sie unter:

- [Konfigurieren der Katalogsuche](search-configuration.md)
- [Suchergebnisse](search-results.md)
- [Verwalten von Suchbegriffen](search-terms.md)

>[!NOTE]
>
>Die native Suchfunktion in Commerce liefert Suchergebnisse mit exakter Übereinstimmung. [!DNL Live Search] wird ein optionales Modul, das in Adobe Commerce installiert und aktiviert werden kann, anders implementiert, und das Ergebnis ist nicht auf die exakte Suchzeichenfolge beschränkt. Beispiel: Bei zehn numerisch nach „Omega _gekennzeichneten Produkten_ eine Suche nach `Omega 1` Ergebnissen zu einer einzigen Übereinstimmung mit _Omega 1_ mit der nativen Suchfunktion. Dieselbe Suchzeichenfolge basiert jedoch auf Live-Suchergebnissen und führt zu einer Übereinstimmung für mehrere Elemente, _Omega 1_ und _Omega 10_.

## Schnellsuche

>[!NOTE]
>
>Wenn [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview) installiert und das [[!DNL Storefront Popover]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/storefront-popover)-Widget aktiviert ist, gibt das Suchfeld die Ergebnisse „Suche während der Eingabe“ in einem Popup zurück.

Das Suchfeld in der Kopfzeile des Stores hilft Besuchern, Produkte in Ihrem Katalog zu finden. Der Suchtext kann der vollständige oder teilweise Produktname oder ein anderes Wort oder eine Phrase sein, das bzw. die das Produkt beschreibt. Die Suchbegriffe, die Benutzer verwenden, um Produkte zu finden, können über den Administrator verwaltet werden.

1. **[!UICONTROL Search]** gibt der Kunde die ersten Buchstaben dessen ein, was er finden möchte.

   Alle Übereinstimmungen im Katalog werden unten mit der Anzahl der gefundenen Ergebnisse angezeigt.

1. Der Kunde drückt die Eingabetaste oder klickt auf ein Ergebnis in der Liste der passenden Produkte.

   ![Suche](./assets/storefront-search-box.png){width="700" zoomable="yes"}

## Erweiterte Suche

>[!NOTE]
>
>Die hier beschriebene Funktion der erweiterten Formularsuche gilt nicht für [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

Mit der erweiterten Suche können Käufer den Katalog anhand der in ein Formular eingegebenen Werte durchsuchen. Da das Formular mehrere Felder enthält, kann eine einzelne Suche mehrere Parameter enthalten. Das Ergebnis ist eine Liste aller Produkte im Katalog, die den Kriterien entsprechen. Ein Link zur erweiterten Suche befindet sich in der Fußzeile Ihres Stores.

![Erweiterte Suche](./assets/storefront-search-advanced.png){width="700" zoomable="yes"}

Jedes Feld im Formular entspricht einem Attribut aus Ihrem Produktkatalog. Um ein Feld hinzuzufügen, legen Sie die Frontend-Eigenschaften des -Attributs auf `Include in Advanced Search` fest. Es empfiehlt sich, nur die Felder einzubeziehen, die Kundinnen und Kunden am ehesten verwenden, um ein Produkt zu finden, da zu viele die Suche verlangsamen.

1. In der Fußzeile des Stores klickt der Kunde auf **[!UICONTROL Advanced Search]**.

1. Fügt im Formular _Erweiterte Suche_ vollständige oder teilweise Werte in so viele Felder wie nötig hinzu.

1. Klicken Sie auf **[!UICONTROL Search]** , um die Ergebnisse anzuzeigen.

   ![Suchergebnisse](./assets/storefront-search-advanced-results-modify.png){width="700" zoomable="yes"}

1. Wenn der Kunde in den Suchergebnissen nicht sieht, wonach er sucht, klickt er auf **[!UICONTROL Modify your search]** und versucht eine andere Kriterienkombination.
