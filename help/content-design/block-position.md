---
title: Positionieren von Inhaltsblöcken
description: Positionieren Sie einen Block an einer bestimmten Position auf der Seite und sogar für ein bestimmtes Produkt oder eine bestimmte Kategorie, ohne Code zu schreiben
exl-id: cfc9eb2c-19c8-43f1-937d-4162b5011b8a
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/BgZJJ9DGr8KD2-6XNf3yPTjo3ulGVdp0yyrJMXHWX-4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 0%

---

# Positionieren von Inhaltsblöcken

Der Code, der das Seitenlayout und die Platzierung von Blöcken steuert, wird in XML ([) &#x200B;](widgets.md). Diese Widgets erleichtern die Positionierung eines Blocks an einer bestimmten Stelle auf der Seite und sogar für ein bestimmtes Produkt oder eine bestimmte Kategorie, ohne Code zu schreiben. Sie können jede Option aus einer Liste auswählen, anstatt sich alle möglichen Kombinationen zu merken.

In der folgenden Liste werden die Speicherorte nach Seitentyp beschrieben, an denen Blöcke normalerweise platziert werden. Weitere Informationen zur Definition von Bereichen auf der Seite finden Sie unter [Standard-Seiten-Layouts](page-layout.md#standard-page-layouts).

## Kategorieseiten und CMS-Seiten

| Blockreferenz | Position |
|----------|-------- |
| [!UICONTROL Breadcrumbs] | Die Navigationshilfe oben auf vielen Seiten, die Ihre aktuelle Position als Link anzeigt. Jeder zusätzliche Inhalt, der in der Breadcrumbs-Referenz platziert wird, schwebt rechts von den Breadcrumbs, falls angezeigt. |
| [!UICONTROL Left Column] | Der Inhalt wird der linken Spalte hinzugefügt. |
| [!UICONTROL Main Content Area] | Der Inhalt wird zum Hauptinhaltsbereich hinzugefügt. |
| [!UICONTROL My Cart Extra Actions] | Der Inhalt wird unter _Warenkorbzwischensumme_ angezeigt, wenn der Kunde oben auf der Seite auf das Warenkorbsymbol klickt. |
| [!UICONTROL Navigation Bar] | Inhalte werden unter der Hauptnavigationsleiste angezeigt. |
| [!UICONTROL Page Bottom] | Der Inhalt wird unten auf der Seite angezeigt. |
| [!UICONTROL Page Footer] | Der Inhalt wird über der Fußzeile der Seite angezeigt. |
| [!UICONTROL Page Header] | Der Inhalt wird unter der Kopfzeile der Seite angezeigt. |
| [!UICONTROL Page Top] | Der Inhalt wird oben auf der Seite angezeigt. |
| [!UICONTROL Right Column] | Inhalte werden in der rechten Spalte angezeigt. |
| [!UICONTROL Store Language] | Der Inhalt wird in der oberen linken Ecke der Kopfzeile angezeigt. |

{style="table-layout:auto"}

## Produktseite

| Blockreferenz | Position |
|----------|-------- |
| [!UICONTROL Alert URLs] | Der Inhalt wird unter dem Titel des Produkts auf der Produktdetailseite angezeigt. |
| [!UICONTROL Bottom Block Options Wrapper] | Wenn benutzerdefinierte Optionen hinzugefügt werden, wird der Inhalt unter der Schaltfläche _Zum Warenkorb hinzufügen_ angezeigt. |
| [!UICONTROL Breadcrumbs] | Inhalte werden rechts neben Breadcrumbs angezeigt - die Navigationshilfe, die Links als Pfad bereitstellt, der unter der Navigationsleiste angezeigt wird. |
| [!UICONTROL Info Column Options Wrapper] | Wenn benutzerdefinierte Optionen hinzugefügt werden, werden Inhalte rechts angezeigt. Derselbe Speicherort gilt für konfigurierbare Optionen. |
| [!UICONTROL Left Column] | Inhalte werden unter den linken Spaltenblöcken angezeigt. |
| [!UICONTROL Main Content Area] | Der Inhalt wird unter dem Hauptinhaltsbereich angezeigt. |
| [!UICONTROL My Cart Extra Actions] | Der Inhalt wird unter _Warenkorbzwischensumme_ angezeigt, wenn der Kunde oben auf der Seite auf das Warenkorbsymbol klickt. |
| [!UICONTROL Navigation Bar] | Inhalte werden unter der Hauptnavigationsleiste angezeigt. |
| [!UICONTROL Page Bottom] | Der Inhalt wird unten auf der Seite angezeigt. |
| [!UICONTROL Page Footer] | Der Inhalt wird über der Fußzeile der Seite angezeigt. |
| [!UICONTROL Page Header] | Der Inhalt wird unter der Kopfzeile der Seite angezeigt. |
| [!UICONTROL Page Top] | Der Inhalt wird oben auf der Seite angezeigt. |
| [!UICONTROL PayPal Express Checkout (Payflow Edition) Shortcut Wrapper] | Wenn die PayPal-Zahlungsmethode aktiviert ist, wird der Inhalt unter der Schaltfläche _PayPal kaufen_ angezeigt. |
| [!UICONTROL PayPal Express Checkout Shortcut Wrapper] | Wenn die PayPal-Zahlungsmethode aktiviert ist, wird der Inhalt unter der Schaltfläche _PayPal kaufen_ angezeigt. |
| [!UICONTROL Product Tags List] | Der Inhalt wird unter der Tag-Leiste „Produkte“ angezeigt. |
| [!UICONTROL Product View Extra Hint] | Der Inhalt wird unter dem höchsten Hauptpreis des Produkts angezeigt. |
| [!UICONTROL Right Column] | Inhalte werden unterhalb der rechten Spaltenblöcke angezeigt. |
| [!UICONTROL Store Language] | Inhalte werden rechts neben der Sprachauswahl angezeigt. |
| [!UICONTROL Tags List Before] | Der Inhalt wird über dem Feld _[!UICONTROL Add Your Tags]_&#x200B;angezeigt. |

{style="table-layout:auto"}
