---
title: KI-Produkterkennung
description: Erfahren Sie, wie [!DNL Adobe Commerce] Kataloganreicherung und PDP-Anreicherung Lücken in strukturierten Produktdaten und kundenorientierten Kopien für die KI-Produkterkennung beheben.
role: Admin, User, Leader
source-git-commit: f2cf82dad7ec3c86a3b9a0a5635556ac2e77dd05
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%
---
# KI-Produkterkennung

Mithilfe der Produktsuche können Kunden Produkte finden und bewerten, die ihren Anforderungen entsprechen. In KI-Tools für Gespräche wie [!DNL ChatGPT] und [!DNL Gemini] können Käufer beschreiben, was sie in ihrer Alltagssprache wollen, und KI-generierte Antworten verwenden, um Produkte zu erkunden und zu vergleichen. Die Nützlichkeit dieser Antworten hängt zum Teil davon ab, ob KI-Agenten auf relevante Produktdaten zugreifen und diese interpretieren können.

## Für wen ist dieses Handbuch? {#who-this-guide-is-for}

- Digitale Marketer und Merchandiser, die möchten, dass Produktdaten präzise und nützlich für die KI-gestützte Produktsuche sind.
- Merchandiser, die eine kontrollierte Möglichkeit benötigen, ausgewählte Produkte anzureichern oder eine Kopie für eine Kampagne vorzubereiten.
- [!DNL Adobe Commerce] Administratoren, die für Katalogdaten, Services und Administratorzugriff verantwortlich sind.

## Warum die Produkterkennung wichtig ist

Käufer beschreiben oft einen Bedarf, eine Verwendung oder eine Präferenz, anstatt nach einem genauen Produktnamen oder technischen Attribut zu suchen. Um diese Anfragen mit relevanten Produkten abzugleichen, benötigen KI-Agenten Produktinformationen, die für Kunden strukturiert und sinnvoll sind.

Wenn Produktaufzeichnungen unvollständig, inkonsistent oder nur auf technische Spezifikationen ausgerichtet sind, können Support-Mitarbeiter Schwierigkeiten haben, zu verstehen, welche Produkte zur Absicht eines Käufers passen. Käufer können relevante Produkte verpassen, und Händler müssen möglicherweise Zeit damit verbringen, Kataloginhalte manuell zu korrigieren und anzureichern.

Darüber hinaus eröffnen markenlose Kundenabfragen neue Möglichkeiten zur Produkterkennung. Wenn Käufer ihre Bedürfnisse beschreiben, ohne eine Marke anzugeben, zeigen KI-Oberflächen relevante Produkte konkurrierender Marken an, basierend darauf, wie gut diese Produkte mit den Absichten der Käufer übereinstimmen. Für Händler ist dies eine Möglichkeit, neue Kunden zu erreichen, die mit ihrer Marke nicht vertraut sind, und die Sichtbarkeit ihrer Produkte über die bestehende Markenbekanntheit hinaus zu erhöhen.

Es gibt jedoch einige Herausforderungen bei der Produkterkennung auf KI-Oberflächen, z. B. Lücken in Ihrem Katalog, die die KI-gestützte Produkterkennung einschränken können.

[!DNL Adobe Commerce] löst diese Kataloglückenprobleme, indem es zwei komplementäre Anreicherungs-Workflows bereitstellt: Anreicherung von Produktdetailseiten und Kataloganreicherung. Diese beiden Anreicherungen verbessern, wie KI-Agenten auf Produkte zugreifen, sie verstehen und mit der Absicht der Käufer abstimmen. Sie sind im Menü _Admin_ > **KI-Produkterkennung** verfügbar.

## Produktfakten sind schwer zugänglich und schwer zu interpretieren

Produktinformationen sind häufig über Attribute, Varianten, Optionen, Kategorien und andere Katalogfelder verteilt. Obwohl diese Informationen für Käufer in der Storefront möglicherweise verfügbar sind, sind sie von KI-Crawler nicht immer zugänglich oder leicht zu interpretieren. Produktdetails, die durch dynamisch gerenderte Inhalte, JavaScript-abhängige Komponenten, interaktive Shopping-Assistenten, Popups oder verknüpfte Seiten präsentiert werden, sind für Crawler möglicherweise nur schwer abzurufen.

Selbst wenn diese Informationen zugänglich sind, sind sie möglicherweise nicht so strukturiert, dass KI-Agenten sie zuverlässig interpretieren können. Infolgedessen verfügen KI-Agenten möglicherweise nicht über ein vollständiges Verständnis der Funktionen, verfügbaren Optionen und Möglichkeiten eines Produkts, sodass sie ihre Fähigkeit, Produkte genau an die Kundenanforderungen anzupassen, einschränken.

### Verfügbar machen strukturierter Fakten mit Anreicherung von Produktdetailseiten

Die PDP-Anreicherung erstellt eine strukturierte Daten-Payload mit relevanten Produktinformationen, einschließlich Attributen, Varianten, Optionen, Feature Bullets, Kategorienbeziehungen, Preisen und Verfügbarkeit. Dadurch erhalten KI-Agenten ein vollständigeres und strukturierteres Verständnis der Funktionen, Möglichkeiten und verfügbaren Konfigurationen eines Produkts.

Mit [ Technologie von „Optimize at Edge](#prerequisites) werden die angereicherten Produktinformationen den KI-Crawler direkt zugänglich gemacht, ohne dass Änderungen an der für Menschen sichtbaren Storefront erforderlich sind. Händler können die Art und Weise verbessern, wie Produktinformationen KI-Agenten präsentiert werden, ohne das Layout von Storefronts zu ändern, neue Komponenten mit Käufersicht einzuführen oder benutzerdefinierte Storefronts zu entwickeln.

Siehe [Anreicherung der Produktdetailseite](pdp-enrichment.md).

## Produktkatalog spiegelt nicht die Absicht des Erstkäufers wider

Käufer beschreiben ihre Bedürfnisse, Probleme und vorgesehenen Anwendungsfälle zunehmend in natürlicher Sprache, anstatt nach bestimmten Produktnamen oder technischen Spezifikationen zu suchen. Produktnamen und -beschreibungen konzentrieren sich jedoch häufig auf technische Attribute, ohne die Vorteile, Anwendungsfälle oder realen Probleme, die ein Produkt löst, klar zu kommunizieren.

Dies schafft eine Lücke zwischen der Art und Weise, wie Käufer ihre Bedürfnisse ausdrücken, und wie Produkte im Katalog beschrieben werden. Ohne klare, kundenorientierte Produktinhalte können KI-Agenten Schwierigkeiten haben, den Wert und die Relevanz eines Produkts für die Absicht eines Käufers zu interpretieren, wobei sie möglicherweise geeignete Produkte zugunsten von Alternativen übersehen, deren Beschreibungen klarer auf die Bedürfnisse des Käufers abgestimmt sind.

### Optimieren des Produktkataloginhalts mit dem Kundenwunsch mithilfe der Kataloganreicherung

Durch die Kataloganreicherung werden technische Produktattribute und vorhandene Kataloginformationen in kundenorientierte Produktnamen und Beschreibungen umgewandelt, die die Vorteile, Funktionen und realen Anwendungsfälle eines Produkts klar kommunizieren. Produktnamen und -beschreibungen gehören zu den einflussreichsten Informationsquellen, die KI-Oberflächen verwenden, um Produktfunktionen zu verstehen und ihre Relevanz für die Kaufabsicht zu bestimmen.

Durch die Verbindung technischer Produktspezifikationen mit den Bedürfnissen und Problemen, die Käuferinnen und Käufer in natürlicher Sprache beschreiben, hilft die Kataloganreicherung KI-Agenten, den Wert eines Produkts besser zu verstehen, die Unklarheit bei der Interpretation seiner Funktionen zu reduzieren und relevante Produkte genauer an die Kundenabsichten anzupassen.

Händler können die vorgeschlagenen Verbesserungen überprüfen und genehmigen, bevor sie sie direkt auf ihren Adobe Commerce-Produktkatalog anwenden. Dadurch wird sichergestellt, dass Storefronts und Vertriebskanäle, die auf dem Katalog basieren, den Käufern über Touchpoints hinweg konsistent dieselben angereicherten, wertorientierten Produktinformationen übermitteln können.

Siehe [Kataloganreicherung](catalog-enrichment.md).

#### Brand Governance-Regeln

Mit Brand Governance-Regeln können Sie die Anforderungen für Produktkopien definieren, die für die Kataloganreicherung gelten, einschließlich Länge, Phrasen, Ton und Groß-/Kleinschreibung. Diese Regeln gelten nur für die Kataloganreicherung, nicht für die PDP-Anreicherung.

Siehe [Erstellen von Regeln für Kataloganreicherungen](brand-governance.md).
