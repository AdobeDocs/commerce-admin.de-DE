---
title: Anreicherung der Produktdetailseite
description: Verwenden Sie [!DNL Adobe Commerce] Anreicherung von Produktdetailseiten, um die von KI empfohlene Produktkopie zu überprüfen, Anreicherungsaufträge zu erstellen und genehmigte Aktualisierungen für LLM- und KI-Erkennung bereitzustellen.
role: Admin, User, Leader
recommendations: noCatalog
touch: true
badgePaas or on-premises: label="Cloud or on-premises only" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed Cloud or on-premises infrastructure) and on-premises projects only."
autotag-review: '2026-06-23T17:36:07.142Z'
TQID: 'https://experienceleague.adobe.com/cjHuva7PP7UzP-yVhe0rkDzHgAYjfSdYEx3g5gorxwk'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c32adafa-ed01-4b31-997e-2413013911b0
    internal-label: Integrations
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9e234eb68fe34171d9e5cf95e8cdab5c31825492
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 0%
---

# Anreicherung der Produktdetailseite

Anreicherung von Produktdetailseiten (PDP) Maximieren Sie das Crawlability für LLMs auf jeder PDP mit strukturierten Produktdaten, ohne dass Änderungen an Ihrem menschlichen Erlebnis vorgenommen werden müssen. Diese Funktion liest sich durch Ihren Produktkatalog, um eine strukturierte Daten-Payload für jede PDP zu erstellen, die von LLMs einfach lesbar und parsierbar ist.

## Funktionsweise {#how-it-works}

Ihr Adobe Commerce-Katalog enthält Produktinformationen wie Attribute, Varianten, Kategorien, Preise und Verfügbarkeit. In einem PDP-Anreicherungsauftrag wählen Sie die Produktseiten und Gruppen von Katalogfakten aus, um sie für KI-Agenten verfügbar zu machen. Die Informationen werden für Agenten organisiert, ohne dass das Storefront-Erlebnis geändert wird.

Mit der PDP-Anreicherung können Sie:

- Wählen Sie bestimmte aktivierte Produkte mit Live-Produktseiten aus.
- Überprüfen Sie eine Zusammenfassung der ausgewählten Seiten und Fakten, bevor Sie den Vorgang speichern oder ausführen.
- Vorschau der in der Anreicherung enthaltenen Produktinformationen.

| Richtung | Zweck |
| --- | --- |
| Commerce-Katalog -> Anreicherungsvorgang | Wählen Sie Live-Produktseiten und die einzuschließenden Katalogfakten aus. |
| Anreicherungsauftrag -> KI-Agenten | Stellen Sie die ausgewählten, vorhandenen Produktinformationen in strukturierter Form zur Verfügung. Die für Menschen sichtbare Schaufensterfront ändert sich nicht. |

## Zugriff auf PDP-Anreicherung

Bevor Sie beginnen, lesen Sie zunächst die bereitstellungsspezifischen [Voraussetzungen für die KI-Produkterkennung](prerequisites.md). Nachdem Sie die Einrichtung für Ihre Commerce-Plattform abgeschlossen haben, öffnen Sie **[!UICONTROL AI Product Discovery]** in der Admin-Liste und wählen Sie **[!UICONTROL Product Details Page Enrichment]** aus.

## Zwei Pfade von PDP-Anreicherungen

Es gibt zwei Pfade zum Empfang von PDP-Anreicherungen:

- **Agentenverkehr** - Diese Art der Anreicherung beginnt automatisch 24-48 Stunden nach der Konfiguration der Commerce-Instanz und zeigt die Ergebnisse auf der Registerkarte **Optimierungen** an.
- **Anreicherungsmanager**: Diese Anreicherungen werden vom Händler konfiguriert, wenn er auf die Schaltfläche &quot;**[!UICONTROL Create enrichment]**&quot; klickt und manuell die SKUs auswählt, die angereichert werden sollen. Weitere Informationen zum [Anreicherungsmanager](#create-an-enrichment-job).

## PDP-Anreicherungsaktivität überprüfen

Die Seite PDP-Anreicherung wird auf der Registerkarte **[!UICONTROL Optimizations]** geöffnet. Verwenden Sie das Dashboard, um die Anreicherungsabdeckung, die Vorgangsaktivität und die Vorgänge zu überprüfen, die Aufmerksamkeit erfordern. Verwenden Sie die Registerkarte **[!UICONTROL Settings]** , um [&#x200B; Commerce](settings.md)Instanz mit der KI-Produkterkennung zu verknüpfen.

### Suchen Sie nach Jobs, die Aufmerksamkeit erfordern

Im Abschnitt **[!UICONTROL Needs your attention]** werden Vorgänge hervorgehoben, für die Maßnahmen erforderlich sind. Auf einer Karte können der Auftragsname, die Auswahl von Produkten, die Anzahl der Produktseiten, der Auftragsstatus und der Fortschritt angezeigt werden. Verwenden Sie die auf einer Karte verfügbare Aktion, um mit dem Auftrag fortzufahren.

### Alle Aufträge durchsuchen

Verwenden Sie die Tabelle, um Aufträge zu suchen und zu verfolgen. Nach Auftragsdetails suchen oder nach Status filtern, einschließlich **[!UICONTROL Generating]**, **[!UICONTROL Ready to review]**, **[!UICONTROL Deployed]**, **[!UICONTROL Queued]** oder **[!UICONTROL Failed]**. Die Tabelle listet die ID, den Namen, die Herkunft, die Anzahl der Produktseiten, das Startdatum, den Status und die verfügbaren Aktionen jedes Vorgangs auf.

## Erstellen eines Anreicherungsauftrags

In diesem Abschnitt erfahren Sie, wie Sie eine Anreicherungsseite für Produktdetails erstellen.

![PDP-Anreicherung erstellen](./assets/create-cat-enrich.png)

1. Klicken Sie **[!UICONTROL Optimizations]** auf **[!UICONTROL Create enrichment]**.
1. Geben Sie einen **Anreicherungsnamen“ ein** z. B. „Black Friday 2026“.
1. Wählen Sie die **Kategorie** aus, z. B. „Kaffee“.
1. Wählen Sie den **Attributsatz** aus, z. B. „Zubehör“.
1. Wählen Sie den **Produkttyp** aus, z. B. „Einfaches Produkt“.
1. Wählen Sie die **Preisspanne**.
1. Klicken Sie auf **[!UICONTROL Apply filters]**.

   Sie können eine Vorschau der Produkte anzeigen, die Ihren Anreicherungskriterien entsprechen, und auf **Anpassen** klicken, um den Umfang der Produkte, die Sie anreichern möchten, zu erweitern.

1. Klicken Sie auf **[!DNL Next]** , um die spezifischen Produkte zu bestätigen, die Sie anreichern möchten.
1. Klicken Sie auf **[!DNL Run enrichment]**.

   Der Anreicherungsvorgang wird ausgeführt und in der Tabelle **Optimierungen** angezeigt. Nach Abschluss der Ausführung können Sie [&#x200B; Optimierungen &#x200B;](#review-and-deploy-an-enrichment-job) und bereitstellen.

### Überprüfen eines Anreicherungsauftrags {#review-and-deploy-an-enrichment-job}

Öffnen Sie einen Anreicherungsauftrag.

![Liste der PDP-Anreicherungs-URLs](./assets/pdp-enrich-urls.png)

Die Tabelle **URLs mit**&quot; listet alle Produkte mit Anreicherungsmöglichkeiten auf. Für jedes Produkt haben Sie folgende Möglichkeiten:

- **Erweitern Sie die Zeile** um die KI-Analyse und die vorgeschlagene Anreicherung anzuzeigen.
- **Bearbeiten** Sie den vorgeschlagenen Produktnamen oder die Beschreibung, bevor Sie sie anwenden, um sie an Ihre Markensprache und Ihre Merchandising-Richtlinien anzupassen.
- **Stellen Sie die** für die Produkte bereit, die Sie anreichern möchten, und veröffentlichen Sie sie direkt in Ihrer Adobe Commerce-Storefront.
- **Als behoben markieren** sobald die Anreicherung überprüft und angewendet wurde.
- **Ignorieren** Vorschläge, die für Ihre Katalogstrategie nicht relevant sind.

Die Vorschläge sind in drei Ansichten unterteilt: **Aktuelle Vorschläge**, **Feste** und **Ignorierte Vorschläge**. Sobald eine Anreicherung angewendet wird, wechselt sie zu **Feste**) mit dem Status **Angewendet**. Angewendete Anreicherungen können jederzeit zurückgesetzt werden.

### Optimieren bereitstellen

Nachdem Sie die Vorschläge geprüft und die zu optimierenden Produktseiten ausgewählt haben, klicken Sie auf **Optimierungen bereitstellen**, um die Anreicherung mit Optimieren bei Edge zu veröffentlichen. In **Bestätigungsdialogfeld „Für Edge bereitstellen** werden die ausgewählten Produkt-URLs, der Optimierungstyp und die angewendete Anreicherung angezeigt. Nach der Bereitstellung wird in einem Bestätigungsbildschirm bestätigt, welche Produktseiten erfolgreich optimiert wurden.

Die Optimierung wird ausschließlich an KI-Benutzeragenten über die [Optimieren bei Edge](https://experienceleague.adobe.com/de/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn) bereitgestellt. Besuchende sehen Ihr bestehendes Storefront-Erlebnis weiterhin genau wie zuvor, ohne dass sich Ihr PDP-Design, Ihre Seitenleistung oder Ihr Markenerlebnis ändern.

## Einschränkungen und Überlegungen {#limits}

- Es können nur aktivierte Produkte mit einer Live-Produktseite ausgewählt werden.
- In der Anreicherung werden bereits im Katalog vorhandene Fakten organisiert. Es werden keine neuen Produktinformationen hinzugefügt.
- Der Workflow für die PDP-Anreicherung ändert die Storefront nicht.
- PDP-Anreicherungsaufträge und Kataloganreicherungsaufträge haben unterschiedliche Zwecke und Workflows.
- Die PDP-Optimierung verwendet [Optimieren bei Edge](https://experienceleague.adobe.com/de/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn) .

## Best Practices {#best-practices}

- Verwenden Sie klare Auftragsnamen, die die Produktgruppe oder Kampagne identifizieren.
- Zeigen Sie eine Vorschau der im Auftrag enthaltenen Fakten an und bestätigen Sie, dass diese korrekt und für KI-Agenten geeignet sind.
- Überprüfen Sie, ob Produkte bereits angereichert wurden, bevor Sie sie überspringen oder überschreiben.
- Koordinieren Sie die Katalogsynchronisierung und Eigentümerschaft der Produktfakten mit den für diese Datensätze zuständigen Teams.

## Beispiel: Anreicherung eines Produkts mit Varianten und Spezifikationen

Eine Produktseite enthält oft mehr Kataloginformationen, als KI-Agenten lesen können. Zum Beispiel verkauft ein Händler einen wasserdichten Wanderschuh. Die Größen-, Breiten- und Farboptionen befinden sich in einem Variantenselektor, der mit JavaScript geladen wird. Materialien, Abdichtung und Pflegehinweise befinden sich auf einer reduzierten Registerkarte Details , und die Anleitung zur Anpassung wird in einem Popup-Fenster geöffnet. Ein Käufer kann alle diese Dateien öffnen, aber eine KI-Crawler, die die Seite beim ersten Laden liest, kann nur den Produktnamen, den Preis und eine kurze Beschreibung sehen.

Wenn der Anreicherungsvorgang für dieses Produkt ausgeführt wird, nimmt es alle Katalogdaten des Produkts, einschließlich seiner Attribute und aller Varianten, und packt sie in ein strukturiertes Format, das KI-Agenten lesen können. Ein KI-Assistent kann dann Fragen beantworten wie: „Ist dieser Stiefel in einer breiten Passform in Größe 11 verfügbar?“ oder „Ist es vollständig wasserdicht?“ aus den eigenen Katalogdaten des Händlers.

Der Anreicherungsauftrag verwendet nur Informationen, die bereits im Katalog vorhanden sind. Es werden keine neuen Produktfakten erstellt und die Produktseite, die Käuferinnen und Käufer sehen, wird nicht geändert.
