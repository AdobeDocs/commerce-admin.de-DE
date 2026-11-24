---
title: Kataloganreicherung
description: Verwenden Sie [!DNL Adobe Commerce] Kataloganreicherung, um die von KI empfohlene Produktkopie zu überprüfen, Anreicherungsaufträge zu erstellen und genehmigte Aktualisierungen für LLM- und KI-Erkennung bereitzustellen.
role: Admin, User, Leader
recommendations: noCatalog
touch: true
badgePaas or on-premises: label="Cloud or on-premises only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed Cloud or on-premises infrastructure) and on-premises projects only."
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
source-git-commit: b2a1abb72839717a7249e9a34b13266b8e384189
workflow-type: tm+mt
source-wordcount: '1976'
ht-degree: 0%
---
# Kataloganreicherung

Die Kataloganreicherung ist eine native [!DNL Adobe Commerce]-Funktion, mit der Sie Produktnamen und lange Beschreibungen verbessern können, sodass Ihr Katalog präziser dargestellt wird, wenn Käufer LLMs und KI-Assistenten für die Produktforschung und -erkennung verwenden.

## Funktionsweise {#how-it-works}

Ihr [!DNL Adobe Commerce] Produktkatalog ist das „System of Record“ für Produktdaten: Namen, Beschreibungen, Attribute, Preise und Inventar. [!DNL Adobe Commerce] verbindet Live-Katalogdaten mit Adobe AI-Erlebnissen. Von dort aus kann der Katalogagent Lücken in Produktnamen und langen Beschreibungen identifizieren, Verbesserungen vorschlagen und genehmigte Änderungen zurück an Commerce schreiben, damit Sie sie in der Commerce-Admin überprüfen können.

Mit der Anreicherung von Katalogen haben Sie folgende Möglichkeiten:

- Identifizieren Sie Lücken und Inkonsistenzen in Produktnamen und langen Beschreibungen, die sich auf die Interpretation Ihrer Produkte durch LLMs auswirken.
- Überprüfen Sie Verbesserungsvorschläge mit unterstützendem Kontext, einschließlich Rechtfertigungen und Vergleiche vor und nach dem Kauf.
- Wenden Sie genehmigte Aktualisierungen direkt auf den Commerce-Katalog an, damit der Admin, die Storefront und andere Kanäle, die diese Felder lesen, weiterhin ausgerichtet sind.

Da Produktnamen und lange Beschreibungen in Commerce live sind, kann die einmalige Verbesserung der Kopie für jeden Kanal, der diese Produktdaten verwendet, von Vorteil sein. Der Nutzen hängt davon ab, wie und wann Ihre Systeme aktualisiert werden.

| Richtung | Zweck |
| --- | --- |
| Commerce-Katalog -> Analyse | Katalog- und Agentenverkehrssignale decken Anreicherungsvorschläge und -möglichkeiten auf. |
| Anreicherung -> Commerce-Katalog | Nachdem Sie eine Aktualisierung genehmigt haben, werden Änderungen am Produktnamen und an der Beschreibung im Commerce-Katalog gespeichert, sodass Admin und Storefront die optimierten Werte widerspiegeln. |

### Zugriff auf die Kataloganreicherung

Bevor Sie beginnen, lesen Sie zunächst die bereitstellungsspezifischen [Voraussetzungen für die KI-Produkterkennung](prerequisites.md). Nachdem Sie die Einrichtung für Ihre Commerce-Plattform abgeschlossen haben, navigieren Sie zu **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]** in der Admin Console.

![Dashboard für Kataloganreicherung](assets/catalog-enrich-dashboard.png){zoomable="yes"}

Der Arbeitsbereich Kataloganreicherung enthält die Registerkarten **[!UICONTROL Optimizations]**, **[!UICONTROL Brand governance]** und **[!UICONTROL Settings]** .

- Verwenden Sie die Registerkarte **[!UICONTROL Optimizations]** , um den auf dem Agent-Traffic basierenden Erkennungssignalen zu überprüfen und Anreicherungsaufträge zu verwalten.
- Verwenden Sie die Registerkarte **[!UICONTROL Brand Governance]** , um [Anforderungen](brand-governance.md) für die von [!DNL Commerce Catalog Agent] generierten Produktnamen und Beschreibungen zu definieren.
- Verwenden Sie die Registerkarte **[!UICONTROL Settings]** , um [Ihre Commerce-Instanz ](settings.md) KI-Produkterkennung zu verbinden.

Die gemeinsame Erweiterung ermöglicht auch die PDP-Anreicherung, die über einen separaten Workflow zur Bereitstellung strukturierter Produktfakten für KI-Agenten verfügt. Siehe [Anreicherung der Produktdetailseite](pdp-enrichment.md).

## Zwei Pfade von Kataloganreicherungen

Es gibt zwei Pfade zum Empfang von Kataloganreicherungen:

- **Agentenverkehr** - Diese Art der Anreicherung beginnt automatisch 24-48 Stunden nach der Konfiguration der Commerce-Instanz und zeigt die Ergebnisse auf der Registerkarte **Optimierungen** an.
- **Anreicherungsmanager** - Händler konfigurieren diese Anreicherungen, wenn sie auf die Schaltfläche &quot;**[!UICONTROL Create enrichment]**&quot; klicken und die zu anreichernden SKUs manuell auswählen. Weitere Informationen zum [Anreicherungsmanager](#create-an-enrichment-job).

### Überprüfen und Anwenden der Kataloganreicherung {#review-and-apply}

Nachdem die Kataloganreicherung aktiviert und konfiguriert wurde, verwenden Sie die Registerkarte **[!UICONTROL Optimizations]** , um Einblicke in die Suche und den agenten Traffic zu überprüfen und Anreicherungsaufträge zu verwalten.

### Überprüfen des monatlichen Agent-Traffics

Bei jeder monatlichen Traffic-Prüfung werden SKUs mit hohem Traffic identifiziert und ein empfohlener Batch bereitgestellt. Für die SKUs mit hohem Agent-Traffic werden automatisch Optimierungen für die Überprüfung generiert. Diese Optimierungen werden basierend auf Ihrer „Standard“-Governance-Regel automatisch generiert. Monatliche Karten zeigen die Produktanzahl, Besuche des KI-Agenten und den Auftragsstatus an. Batches mit agentem Traffic und selbstgewählter Batches verwenden denselben Regelauswahl-, Bestätigungs-, Ausführungs-, Überprüfungs- und Bereitstellungs-Workflow.

### Überprüfen von Aufträgen, die Aufmerksamkeit erfordern

Im **[!UICONTROL Needs your attention]** Abschnitt werden Aufträge hervorgehoben, für die Handlungsbedarf besteht, einschließlich abgeschlossener Aufträge, die bereit zur Überprüfung sind. Öffnen Sie einen abgeschlossenen Auftrag, um die vorgeschlagenen Produktänderungen vor der Bereitstellung zu überprüfen.

### Jobs suchen

In der **[!UICONTROL All jobs]** Tabelle werden die einzelnen Vorgangs-IDs, der Name, die Herkunft, die SKU-Anzahl, die verwendete Regel, die Startzeit und der Status aufgelistet. Die Herkunft gibt an, ob ein Batch aus dem Agentendatenverkehr selbst ausgewählt oder empfohlen wurde. Verarbeitungsstatus als **[!UICONTROL Queued]**, **[!UICONTROL Running]**, **[!UICONTROL Completed]** oder **[!UICONTROL Failed]** verfolgen. Im Arbeitsbereich Optimierungen können diese Aufträge auch während ihrer Ausführung als **[!UICONTROL Generating]** angezeigt werden, **[!UICONTROL Ready to review]** nach Abschluss der Generierung und nach der Bereitstellung genehmigter Änderungen als **[!UICONTROL Deployed]**. Sie können mehrere Aufträge gleichzeitig ausführen. Wiederholen Sie einen fehlgeschlagenen Auftrag mit **[!UICONTROL Retry]**.

### Erstellen eines Anreicherungsauftrags

**So erstellen Sie eine Kataloganreicherung:**

![Kataloganreicherung erstellen](./assets/create-cat-enrich.png){zoomable="yes"}

1. Klicken Sie **[!UICONTROL Optimizations]** auf **[!UICONTROL Create enrichment]**.
1. Geben Sie einen **Anreicherungsnamen“ ein** z. B. „Black Friday 2026“.
1. Wählen Sie die **Kategorie** aus, z. B. „Kaffee“.
1. Wählen Sie den **Attributsatz** aus, z. B. „Zubehör“.
1. Wählen Sie den **Produkttyp** aus, z. B. „Einfaches Produkt“.
1. Wählen Sie die **Preisspanne**.
1. Klicken Sie auf **[!UICONTROL Apply filters]**.

   Sie können eine Vorschau der Produkte anzeigen, die Ihren Anreicherungskriterien entsprechen, und auf **Anpassen** klicken, um den Umfang der Produkte, die Sie anreichern möchten, zu erweitern.

1. Klicken Sie auf **[!DNL Next]** und zeigen Sie eine Vorschau der [Governance](brand-governance.md)Regel) an, die auf Ihre Anreicherung angewendet wird.
1. Klicken Sie auf **[!DNL Next]** , um die spezifischen Produkte zu bestätigen, die Sie anreichern möchten.
1. Klicken Sie auf **[!DNL Run enrichment]**.

   Der Anreicherungsvorgang wird ausgeführt und in der Tabelle Optimierungen angezeigt. Nach Abschluss der Ausführung können Sie [ Optimierungen ](#review-deploy-catalog) und bereitstellen.

### Überprüfen und Bereitstellen eines Anreicherungsauftrags {#review-deploy-catalog}

Öffnen Sie einen Anreicherungsauftrag.

![Liste der URLs zur Kataloganreicherung](./assets/catalog-enrich-urls.png){zoomable="yes"}

Die Tabelle **URLs mit**&quot; listet alle Produkte mit Anreicherungsmöglichkeiten auf. Für jedes Produkt haben Sie folgende Möglichkeiten:

- **Erweitern Sie die Zeile** um die KI-Analyse und die vorgeschlagene Anreicherung anzuzeigen.
- **Bearbeiten** Sie den vorgeschlagenen Produktnamen oder die Beschreibung, bevor Sie sie anwenden, um sie an Ihre Markensprache und Ihre Merchandising-Richtlinien anzupassen.
- **Stellen Sie die** für die Produkte bereit, die Sie anreichern möchten, und veröffentlichen Sie sie direkt in Ihrem Adobe Commerce-Katalog.
- **Als behoben markieren** sobald die Anreicherung überprüft und angewendet wurde.
- **Ignorieren** Vorschläge, die für Ihre Katalogstrategie nicht relevant sind.

Die Vorschläge sind in drei Ansichten unterteilt: **Aktuelle Vorschläge**, **Feste** und **Ignorierte Vorschläge**. Sobald eine Anreicherung angewendet wird, wechselt sie zu Feste Vorschläge mit dem Status **Angewendet** und zu einer **Im Katalog anzeigen** Aktion, um die Aktualisierung in Adobe Commerce zu überprüfen. Angewendete Anreicherungen können jederzeit zurückgesetzt werden, wodurch der ursprüngliche Produktname und die ursprüngliche Beschreibung wiederhergestellt werden.

## Überprüfen der Anreicherung im Administrator {#verify-in-admin}

**So überprüfen Sie die angewendete Kataloganreicherung:**

1. Navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]** in der Commerce Admin Console.
1. Verwenden Sie Filter und den **[!UICONTROL Store View]** nach Bedarf (z. B. **[!UICONTROL Default Store View]**).
1. Suchen Sie nach der SKU.
1. Öffnen Sie das Produkt im Bearbeitungsmodus.

   Das Produktformular zeigt den angereicherten Produktnamen und/oder die Beschreibung an.

   ![Angereicherter Produktname](./assets/enriched-product-name.png){zoomable="yes"}

1. Optional: Wählen Sie **[!UICONTROL Override Catalog Agent provided Product Name]** aus, wenn Sie stattdessen einen manuell eingegebenen Namen beibehalten möchten.

   Manuelle Überschreibungen beeinflussen, wie Vorschläge mit dem Katalog synchronisiert werden. Weitere Informationen finden Sie unter [Manuelles Überschreiben in der Admin](#manual-override-in-the-admin).

1. Erweitern Sie den Abschnitt **[!UICONTROL Content]** und suchen Sie das Feld Beschreibung .

   Die angereicherte Beschreibung wird angezeigt, wenn Sie Änderungen der Beschreibung anwenden.

   ![Produktbeschreibung anreichern](./assets/enrich-product-description.png){zoomable="yes"}

1. Optional: Wählen Sie **[!UICONTROL Override Catalog Agent provided Description]** aus, wenn Sie stattdessen eine manuell eingegebene Beschreibung beibehalten möchten.

Manuelle Überschreibungen beeinflussen, wie Vorschläge mit dem Katalog synchronisiert werden. Weitere Informationen finden Sie unter [Manuelles Überschreiben in der Admin](#manual-override-in-the-admin).

## Überprüfen der Anreicherung in der Storefront {#verify-storefront}

**So überprüfen Sie die Anreicherung in der Storefront:**

1. Suchen Sie die SKU in Ihrer Storefront.
1. Öffnen Sie die Produktseite.
1. Bestätigen Sie, dass der Produktname und die Beschreibung mit dem übereinstimmen, was Sie genehmigt haben.

   Es kann einige Zeit dauern, bis die Anreicherungen in Ihrer Storefront angezeigt werden.

1. Bestätigen Sie, dass die Regionen mit der langen Beschreibung mit den genehmigten Werten übereinstimmen.
1. Optional: Bestätigen Sie nachgelagerte Kanäle, die dieselben Katalogattribute verwenden, sofern für Ihren Rollout relevant.

## Überschreibungen, Aufnahme und veraltete Vorschläge {#overrides-ingestion}

Nachdem die Kataloganreicherung den Namen oder die Beschreibung eines Produkts aktualisiert hat, können andere Aufnahmesysteme dieselben Felder ändern. Beispiele sind REST-API-Aufrufe, CSV-Importe und PIM-Feeds.

### Ausgangswert erneut aufgenommen {#original-value-reingested}

Wenn ein externer Prozess den ursprünglichen Namen oder die ursprüngliche Beschreibung schreibt (den Wert, der vor der Anwendung der Anreicherung existierte), berücksichtigt Commerce weiterhin den angereicherten Wert für dieses Feld gemäß den Regeln der Kataloganreicherung. Der Vorschlag wird möglicherweise nicht automatisch basierend auf dieser Aufnahme zurückgesetzt.

### Neuer Wert erneut aufgenommen {#new-value-reingested}

Wenn der externe Prozess einen neuen Wert sendet, bei dem es sich nicht um eine Wiederholung des Textes vor der Anreicherung handelt, berücksichtigt Commerce den neuen Katalogwert. Wenn Sie beispielsweise von „Rote Schuhe“ in „Ikonische rote Schuhe“ umbenennen, wird der angereicherte Wert ersetzt. Der zugehörige Anreicherungsvorschlag wird in der Regel als *veraltet“*, da der Live-Katalog nicht mehr mit dem Vorschlagskontext übereinstimmt.

### Manuelle Überschreibung in der Admin {#manual-override-in-the-admin}

Wenn Sie den Produktnamen oder die Beschreibung im [!DNL Adobe Commerce] Admin manuell bearbeiten:

- Der Admin-Wert gewinnt als Aufzeichnungssystem für diese manuelle Änderung.
- Der Anreicherungsvorschlag ist mit *Veraltet* gekennzeichnet.
- Der Vorschlag -Workflow kehrt zum ursprünglichen Status für dieses Element zurück, sodass Sie einen neuen Vorschlag erneut planen oder akzeptieren können, wenn die Analyse erneut ausgeführt wird.

Diese Regeln helfen Ihnen zu ermitteln, ob Kataloganreicherung, Aufnahme-Feeds oder Admin-Bearbeitungen relevant sind, wenn mehrere Kanäle dieselbe SKU berühren.

## Einschränkungen und Überlegungen {#limits}

- Die Anreicherung gilt nur für Produktnamen und lange Beschreibungen. Das Seitenlayout, die Widgets oder andere Storefront-Inhalte auf Seitenebene werden nicht geändert.
- Große Kataloge und eine hohe URL-Anzahl können sich darauf auswirken, wie schnell die Analyse abgeschlossen wird und wie viele Vorschläge gleichzeitig angezeigt werden.
- Aussagekräftige Vorschläge gehen davon aus, dass LLM-relevante Bots auf die von Ihnen gewünschten Produkt-URLs zugreifen können. Roboterregeln, Authentifizierung, Geoblocking und umfassende Personalisierung können die Abdeckung verringern.

## Best Practices {#best-practices}

- Dokumentieren Sie die Systemeignerschaft für Produktname und Beschreibung, damit PIM- oder Feed-Vorgänge nicht unbeabsichtigt mit der Kataloganreicherung kollidieren.
- Koordinieren Sie sich mit SEO- und Marken-Teams, bevor Sie Titel oder Beschreibungen in großen Mengen anwenden.
- Führen Sie nach wichtigen Katalogimporten eine Synchronisierung bzw. Neuanalyse durch, damit die Vorschläge den aktuellen Katalogstatus widerspiegeln.

## Beispiele

Die folgenden Beispiele zeigen, wie die Kataloganreicherung technische Rohattribute in kundenorientierte, erzählerische Produktkopien umwandelt, die LLMs zur Beantwortung von Fragen zum Einkauf verwenden können.

### Beispiel: Kaffeeprodukt mit technischen Attributen

Ein Coffee retailer-Katalog speichert nur die technischen Daten für ein Kaffeebohnen-Produkt mit mittlerer Röstung: Bohnensorte, Ursprungsregion, Verarbeitungsmethode, Röstniveau und Höhenbereich. Diese Felder beschreiben das Produkt, vermitteln dem Käufer jedoch nicht seinen Wert, sodass ein KI-Assistent wenig zu tun hat, wenn er eine Frage wie „Welcher Kaffee hat einen glatten, säurearmen Geschmack?“ beantwortet.

Die Kataloganreicherung liest die technischen Attribute und Gründe durch ihre Interaktion, um daraus käuferrelevante Merkmale abzuleiten:

| Technisches Attribut | Abgeleitetes Merkmal | Überlegung |
| --- | --- | --- |
| Honigverfahren, Medium Roast | Niedriger Säuregehalt | Obstschleim, der während der Honigverarbeitung auf der Bohne verbleibt, unterdrückt den Säuregehalt, und der mittlere Braten zersetzt die restlichen sauren Verbindungen. |
| Honigverfahren, Arabica, Medium Roast | Haselnussaroma | Fruchtzucker aus dem Schleim verbinden sich mit Arabicas natürlichen Nussnoten, verstärkt bei mittlerem Rösten. |
| Honigverfahren, Arabica | Reichhaltiges, cremiges Mundgefühl | Öle, die während der Trocknung aus dem Schleim absorbiert werden, erhöhen die Viskosität und den Körper. |
| Honigverfahren, Höhe 900-1200m | Karamelll-Untertöne | Die dichteren, hoch gelegenen Bohnen entwickeln komplexere Zucker, die durch die Honigverarbeitung vertieft werden. |

Die Kataloganreicherung wendet diese abgeleiteten Merkmale auf die Produktkopie an:

- **Vorher**: &quot;Medium Röstkaffeebohnen - Arabica, Brasilien Minas Gerais, Honigverfahren, 900-1200m“
- **Nachher**: „Arabica-Bohnen, die in 900-1200m im brasilianischen Minas Gerais angebaut werden, Honig verarbeitet und mittelgeröstet, entwickeln ein natürlich süßes, cremiges Mundgefühl mit ausgeprägtem Haselnuss-Charakter, Karamelll-Untertönen und geringer Säure. Ein konsistenter, zugänglicher Spezialkaffee, den man am besten durch Umgießen erleben kann.“

Der aktualisierte Name und die aktualisierte Beschreibung werden direkt im Commerce-Katalog gespeichert, sodass die Storefront, die LLM-Feeds und andere Kanäle, die diese Felder lesen, alle dieselbe angereicherte Kopie widerspiegeln.

### Beispiel: Modulare Möbelkonfiguration

Ein Möbel-retailer verkauft eine modulare Sektionalcouch, bei der die Produktbeschreibung nur die Konfigurationscodes und Stoffnamen auflistet, z. B. `6 Standard Seats + 6 Standard Sides in Sapphire Navy Corded Velvet`. Diese Kurzschreibweise ist für einen wiederkehrenden Kunden verständlich, gibt einem KI-Assistenten jedoch wenig Kontext darüber, wie das Produkt funktioniert oder was es langlebig oder komfortabel macht.

Die Kataloganreicherung erweitert die Konfigurations- und Fabric-Attribute zu einer erzählenden Beschreibung, die erklärt, was jede Komponente tut und warum sie für einen Käufer wichtig ist:

- **Vorher**: „6 Standardsitze + 6 Standardseiten in Sapphire Navy Corded Velvet“
- **Nachher**: „Diese Konfiguration umfasst 6 Standard-Sitzeinsätze und 6 Standard-Seiteneinsätze, die austauschbar als Arme oder Rücken fungieren und die modularen Bausteine Ihres Layouts bilden. Jeder Sitz verfügt über Standardschaum mit drei hochdichten Schichten, die entwickelt wurden, um den Auftrieb zu erhalten und dem Durchhängen zu widerstehen. Die Sapphire Navy Corded Velvet Hülle ist genauso haltbar wie luxuriös, mit strukturierten Kordeln, die einen subtilen Glanz und ein weiches, weiches Gefühl erzeugen. Die Abdeckungen werden von Hand genäht, um einen präzisen, maßgeschneiderten Look zu erzielen, und sind maschinenwaschbar und veränderbar, sodass sich Ihr Schnitt mit Ihrem Raum entwickeln kann.“

Da die angereicherte Beschreibung in den Commerce-Katalog zurückgeschrieben wird, ist sie für KI-Bots verfügbar, die die Produktdetailseite crawlen haben, sowie für jeden nachgelagerten Kanal oder Feed, der die Katalogdaten des Produkts verwendet, ohne das Layout oder Design zu ändern, das Kundinnen und Kunden auf der Seite sehen.
