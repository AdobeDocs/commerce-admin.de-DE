---
title: Suchmaschinenoptimierung
description: Erfahren Sie mehr über Tools zur Suchmaschinenoptimierung (SEO) für Commerce-Sites und Best Practices für eine optimale SEO.
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
TQID: https://experienceleague.adobe.com/cEXR2743G7ZzRSKqb9r344Osipo-R-GlqxNZwC-u-Nk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: b5520579-b31f-4df7-9281-f0d9f91e2edcid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 551
ht-degree: 0%

---

# SEO-Übersicht

_Suchmaschinenoptimierung_ (SEO) ist die Praxis der Feinabstimmung des Inhalts und der Präsentation einer Site, um die Art und Weise zu verbessern, wie die Seiten von Suchmaschinen indiziert werden. Commerce bietet verschiedene Funktionen zur Unterstützung Ihrer fortlaufenden SEO-Bemühungen.

>[!TIP]
>
>Informationen zu Adobe Commerce as a Cloud Service finden Sie in den [SEO-Richtlinien](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/) in der Dokumentation zu Commerce Storefront

## Metadaten

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."}

Erfahren Sie mehr über das Hinzufügen und Verbessern von [ (Metadaten](meta-data.md) für Ihre Site und Ihren Store.

## Verwenden einer Sitemap

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."}

Eine [Sitemap](sitemap-xml.md) verbessert die Art und Weise, wie Ihr Store von Suchmaschinen indiziert wird, und wurde entwickelt, um Seiten zu finden, die von Web-Crawler übersehen werden könnten. Eine Sitemap kann so konfiguriert werden, dass alle Seiten und Bilder indiziert werden.

## URL-Neuschreibungen

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."}

Mit dem [URL Rewrite](url-rewrite.md)-Tool können Sie jede URL ändern, die mit einem Produkt, einer Kategorie oder einer CMS-Seite verknüpft ist.

## Suchmaschinenroboter

Die Commerce-Konfiguration enthält Einstellungen zum Generieren und Verwalten von Anweisungen für Web-Crawler und Bots, die Ihre Site indizieren. Wenn die Anfrage für `robots.txt` Commerce erreicht (und keine physische Datei), wird sie dynamisch an den Robots-Controller weitergeleitet. Die Anweisungen sind Anweisungen, die von den meisten Suchmaschinen erkannt und befolgt werden.

Standardmäßig enthält die von Commerce generierte Datei „robots.txt“ Anweisungen für das Web-Crawler. Damit lassen sich bestimmte Teile der Site, die Dateien enthalten, die intern vom System verwendet werden, nicht indizieren. Sie können die Standardeinstellungen verwenden oder eigene benutzerdefinierte Anweisungen für alle oder für bestimmte Suchmaschinen definieren. Es gibt viele Online-Artikel, die sich ausführlich mit dem Thema befassen.

### Beispiel für benutzerdefinierte Anweisungen

**Ermöglicht vollständigen Zugriff**

    user-agent:*
    disallow:

**Deaktiviert den Zugriff auf alle Ordner**

    user-agent:*
    disallow: /

**Standardanweisungen**

    User-agent: *
    Disallow: /index.php/
    Disallow: /*?
    Disallow: /checkout/
    Disallow: /app/
    Disallow: /lib/
    Disallow: /*.php$
    Disallow: /pkginfo/
    Disallow: /report/
    Disallow: /var/
    Disallow: /catalog/
    Disallow: /customer/
    Disallow: /sendfriend/
    Disallow: /review/
    Disallow: /*SID=

### Konfigurieren von `robots.txt`

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die **[!UICONTROL Global]** Konfiguration in der ersten Zeile des Rasters und klicken Sie auf **[!UICONTROL Edit]**.

   ![Globale Design-Konfiguration](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. Scrollen Sie nach unten und erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Search Engine Robots]** und führen Sie die folgenden Schritte aus:

   ![Design-Konfiguration - Suchmaschinenroboter](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - Legen Sie **[!UICONTROL Default Robots]** auf eine der folgenden Einstellungen fest:

     | Option | Beschreibung |
     |------|------------|
     | `INDEX, FOLLOW` | Weist Web-Crawler an, die Site zu indizieren und später erneut auf Änderungen zu prüfen. |
     | `NOINDEX, FOLLOW` | Weist Web-Crawler an, die Indizierung der Site zu vermeiden, sich jedoch zu einem späteren Zeitpunkt erneut um Änderungen zu kümmern. |
     | `INDEX, NOFOLLOW` | Weist Web-Crawler an, die Website nur einmal zu indizieren, aber nicht den Links auf der Seite zu folgen. |
     | `NOINDEX, NOFOLLOW` | Weist Web-Crawler an, die Indizierung der Website zu vermeiden und keinem Link auf der Seite zu folgen. |

     {style="table-layout:auto"}

   - Geben Sie bei Bedarf benutzerdefinierte Anweisungen in das **[!UICONTROL Edit Custom instruction of robots.txt file]** ein. Beispielsweise können Sie während der Entwicklung einer Site den Zugriff auf alle Ordner verbieten.

   - Um die Standardanweisungen wiederherzustellen, klicken Sie auf **[!UICONTROL Reset to Default]**.

1. Klicken Sie abschließend auf **[!UICONTROL Save Configuration]**.
