---
title: Kataloganreicherung
description: Verwenden Sie die native Kataloganreicherungsfunktion in Adobe Commerce, um die von KI vorgeschlagenen Verbesserungen der Produktnamen und langen Beschreibungen für LLM und die KI-unterstützte Erkennung zu überprüfen und anzuwenden.
role: Admin, User, Leader
recommendations: noCatalog
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
autotag-review: '2026-06-23T17:36:07.142Z'
TQID: 'https://experienceleague.adobe.com/cjHuva7PP7UzP-yVhe0rkDzHgAYjfSdYEx3g5gorxwk'
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c32adafa-ed01-4b31-997e-2413013911b0id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094id: e1e0219c-f879-479f-8427-888ed2a6e9c2id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: a5d9ef32b56d3f422e7af6352002ed5827fc185c
workflow-type: tm+mt
source-wordcount: 2182
ht-degree: 0%

---

# Kataloganreicherung

Die Kataloganreicherung ist eine native [!DNL Adobe Commerce]-Funktion, mit der Sie Produktnamen und lange Beschreibungen verbessern können, sodass Ihr Katalog präziser dargestellt wird, wenn Käufer LLMs und KI-Assistenten für die Produktforschung und -erkennung verwenden.

>[!NOTE]
>
>Die Anreicherung von Katalogen basiert auf [!DNL Commerce Catalog Agent] und [!DNL Adobe LLM Optimizer] hinter den Kulissen. Sie verwenden die Anreicherung im Rahmen Ihres Commerce-Katalog-Workflows. Sie verwalten keine separate LLM Optimizer-Integration, um genehmigte Name- und Beschreibungsaktualisierungen anzuwenden. Eine umfassendere LLM-Überwachung und -Optimierung außerhalb von Commerce finden Sie in der [LLM Optimizer-Produktdokumentation](https://experienceleague.adobe.com/en/docs/llm-optimizer/using/home).

## Funktionsweise {#how-it-works}

Ihr [!DNL Adobe Commerce] Produktkatalog ist das „System of Record“ für Produktdaten: Namen, Beschreibungen, Attribute, Preise und Inventar. [!DNL Adobe Commerce] Storefront MCP (Model Context Protocol) verbindet Live-Katalogdaten mit Adobe AI-Erlebnissen. Von dort aus kann der Katalogagent Lücken in Produktnamen und langen Beschreibungen identifizieren, Verbesserungen vorschlagen und genehmigte Änderungen zurück an Commerce schreiben, damit Sie sie in der Commerce-Admin überprüfen können.

Mit der Anreicherung von Katalogen haben Sie folgende Möglichkeiten:

- Identifizieren Sie Lücken und Inkonsistenzen in Produktnamen und langen Beschreibungen, die sich auf die Interpretation Ihrer Produkte durch LLMs auswirken.
- Überprüfen Sie Verbesserungsvorschläge mit unterstützendem Kontext, einschließlich Rechtfertigungen und Vergleiche vor und nach dem Kauf.
- Wenden Sie genehmigte Aktualisierungen direkt auf den Commerce-Katalog an, damit der Admin, die Storefront und andere Kanäle, die diese Felder lesen, weiterhin ausgerichtet sind.

Da Produktnamen und lange Beschreibungen in Commerce live sind, kann die einmalige Verbesserung der Kopie für jeden Kanal, der diese Produktdaten verwendet, von Vorteil sein. Der Nutzen hängt davon ab, wie und wann Ihre Systeme aktualisiert werden.

| Richtung | Zweck |
| --- | --- |
| Commerce-Katalog -> Analyse | Katalog- und URL-Signale speisen Anreicherungsvorschläge ein. |
| Anreicherung -> Commerce-Katalog | Nachdem Sie eine Aktualisierung genehmigt haben, werden Änderungen am Produktnamen und an der Beschreibung im Commerce-Katalog gespeichert, sodass Admin und Storefront die optimierten Werte widerspiegeln. |

## Für wen ist das? {#who-this-is-for}

- Digitale Marketer und Merchandiser, die möchten, dass Produktdaten in LLM-basierten Antworten korrekt und konsistent sind.
- Digitale Marketer und Merchandiser, die eine kontrollierte Möglichkeit benötigen, die Katalogkopie skaliert zu verbessern.
- Commerce-Administratoren, die für die Katalogintegrität, Admin-Prozesse und Integrationen (API, CSV, PIM) verantwortlich sind, die Produktattribute befüllen.

## Voraussetzungen {#prerequisites}

Die folgenden Voraussetzungen gelten, wenn Sie Zugriff auf die Kataloganreicherung haben.

- Ihre Storefront kann durch LLM-orientierte und agentische Bots crawlen werden, bei denen eine crawlen Abdeckung für katalogorientierte Vorschläge erforderlich ist.
- Die erforderlichen Commerce-Services und die Katalogkonnektivität sind aktiviert und funktionieren ordnungsgemäß. Weitere Informationen [ Sie unter ](#enable-catalog-enrichment) der Kataloganreicherung aktivieren .
- [IMS ist konfiguriert](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations).
- Sie haben Zugriff auf die [Adobe Admin Console](https://helpx.adobe.com/business/enterprise/plan-your-deployment/basic-concepts/admin-console.html).
- Ihre Organisation hat den GenAI-Fahrer für die zugrunde liegenden KI-Services unterzeichnet oder sich ausdrücklich dagegen entschieden.

>[!NOTE]
>
>Im Rahmen der Einrichtung überprüft Commerce, ob Ihr Unternehmen den GenAI-Treiber unterzeichnet hat, der die KI-Services hinter der Kataloganreicherung abdeckt. Wenn Sie den Fahrer noch nicht angemeldet oder sich abgemeldet haben, werden Sie aufgefordert, den Fahrer zu signieren oder zu aktualisieren, bevor Sie die Kataloganreicherung verwenden können.

## Kataloganreicherung aktivieren {#enable-catalog-enrichment}

Arbeiten Sie mit Ihrem Commerce-Administrator oder Implementierungspartner zusammen, um Folgendes sicherzustellen, bevor Sie Vorschläge überprüfen oder anwenden:

### Installieren von Erweiterungen für Kataloganreicherung und Katalog-Services

1. Installieren Sie die Kataloganreicherungserweiterung in Ihrer Commerce-Instanz, indem Sie den folgenden Befehl ausführen:

   ```bash
   composer require magento/module-catalog-enrichment --no-update
   composer update magento/module-catalog-enrichment
   ```

1. Wenn Sie noch keine Katalog-Services installiert haben, [ Sie (](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/installation#install-the-catalog-service-extension)).

   **[!UICONTROL Catalog enrichment]** ist jetzt in Ihrer Commerce-Instanz verfügbar.

### Zugriff auf die Kataloganreicherung

Nach der Installation der Erweiterungen Catalog Enrichment und Catalog Services ist die Funktion Catalog Enrichment in Admin unter **[!UICONTROL Catalog]** > **[!UICONTROL Catalog Enrichment]** verfügbar.

![Kataloganreicherung](./assets/catalog-enrichment-menu.png)

### Konfigurieren der Kataloganreicherung

Konfigurieren Sie die Kataloganreicherung auf der Registerkarte **[!UICONTROL Settings]** , damit [!DNL Commerce Catalog Agent] eine Verbindung zu Ihrer [!DNL Adobe Commerce]-Umgebung herstellen und Vorschläge in Commerce Admin einblenden können.

1. Navigieren Sie in der Admin-Liste zu **[!UICONTROL Catalog]** > **[!UICONTROL Catalog Enrichment]**.
1. Wählen Sie in der **[!UICONTROL Scope]** oben auf der Seite die Store-Ansicht aus, die Sie konfigurieren möchten, oder lassen Sie **[!UICONTROL All Store Views]**, um die Einstellungen in allen Store-Ansichten zu verwalten.
1. Öffnen Sie die Registerkarte **[!UICONTROL Settings]** .
1. Erweitern Sie in **[!UICONTROL Commerce Configuration]** das Ansichtsfeld Store mit der Bezeichnung und der URL.

   Geben Sie Details zur [!DNL Adobe Commerce] an, um den Katalog-LLM Optimizer-Service und Audit-Workflows zu aktivieren.

   ![Commerce-Konfiguration auf der Registerkarte „Kataloganreicherungseinstellungen“](./assets/catalog-enrichment-commerce-config.png)

1. Geben Sie die erforderlichen Verbindungsdetails für die Store-Ansicht ein.

   - **[!UICONTROL Store View URL]**: URL, die der Store-Ansicht entspricht (z. B. `https://brand.example.com/fr/`).
   - **[!UICONTROL Environment ID]**: Eindeutige Kennung für die [!DNL Adobe Commerce] Umgebung, auf die die Verbindung zugreift.
   - **[!UICONTROL Website Code]**, **[!UICONTROL Store Code]** und **[!UICONTROL Store View Code]**: Website-, Store- und Store-Ansichtscodes für die Commerce-Website. Diese Werte müssen mit den Codes in Ihrem Commerce-Admin übereinstimmen.
   - **[!UICONTROL Host Name]**: Host-Name Ihrer [!DNL Adobe Commerce].

1. Klicken Sie auf **[!UICONTROL Save]**.

Warten Sie nach dem Speichern, bis ein erster Synchronisierungs- oder Validierungsauftrag abgeschlossen ist, bevor Sie sich auf die Katalog- oder Auditergebnisse für diese Store-Ansicht verlassen. Es kann bis zu 24 Stunden dauern, bis Produktvorschläge auf der **[!UICONTROL Catalog Enrichment]** angezeigt werden.

Um eine Store-Ansichtskonfiguration zu entfernen, erweitern Sie diesen Eintrag und klicken Sie auf **[!UICONTROL Delete]**.

#### Feldbeschreibungen {#commerce-connection-fields}

Erforderliche Felder sind im **[!UICONTROL Commerce Configuration]** Formular mit einem Sternchen (*) gekennzeichnet.

| Feld | Erforderlich | Beschreibung |
| --- | --- | --- |
| URL für Store-Ansicht | Ja | URL, die der Store-Ansicht entspricht (z. B. `https://brand.example.com/fr/`) |
| Umgebungs-ID | Ja | Eindeutige Kennung für die [!DNL Adobe Commerce] Umgebung, auf die die Verbindung zugreift. |
| Website-Code | Ja | Website-Code der Commerce-Website. |
| Speichercode | Ja | Store-Code der Commerce-Website. |
| Code für Shop-Ansicht | Ja | Store-Ansicht der Commerce-Website. |
| Host-Name | Ja | Hostname der [!DNL Adobe Commerce]. |

### Überprüfen und Anwenden der Kataloganreicherung {#review-and-apply}

Nachdem die Kataloganreicherung aktiviert und konfiguriert wurde, werden auf der Registerkarte **[!UICONTROL Agentic Opportunities]** Produktvorschläge angezeigt. Von hier aus können Sie Vorschläge überprüfen und genehmigte Aktualisierungen auf Produktnamen und lange Beschreibungen in Ihrem Commerce-Katalog anwenden.

Die Kataloganreicherung verwendet die folgenden Workflow-Ansichten:

- **[!UICONTROL Current Suggestions]**: Neue oder aktive Elemente zur Überprüfung.
- **[!UICONTROL Fixed Suggestions]**: Elemente, die Sie bereits angewendet oder aufgelöst haben.
- **[!UICONTROL Ignored Suggestions]**: Elemente, die Sie absichtlich von der Aktion ausgeschlossen haben.

![Kataloganreicherung](./assets/agentic-opportunities.png)

### Genehmigte Vorschläge bereitstellen {#review-deploy-catalog}

So stellen Sie genehmigte Vorschläge bereit:

1. Wählen Sie **[!UICONTROL Current Suggestions]** aus.
1. Klicken Sie auf das Erweiterungssteuerelement für die URL- oder SKU-Zeile, um die vorgeschlagenen Aktualisierungen des Produktnamens und der Produktbeschreibung anzuzeigen.
1. Überprüfen Sie den Vorschlag und bestätigen Sie, dass er mit Ihrer Merchandising- und SEO-Strategie übereinstimmt.

Sie können einen Vorschlag bearbeiten, bevor Sie ihn bereitstellen, oder ihn in **[!UICONTROL Ignored Suggestions]** verschieben, wenn er nicht Ihrer Strategie entspricht.

1. Wählen Sie die Zeile aus, in der die URL oder SKU aktualisiert werden soll.
1. Klicken Sie auf **[!UICONTROL Deploy optimizations]** und bestätigen Sie.

Genehmigte Name- und Beschreibungsänderungen werden wie andere Produktaktualisierungen im [!DNL Adobe Commerce] gespeichert.

>[!IMPORTANT]
>
>Behandeln Sie jede angewendete Aktualisierung als Änderung des Produktionskatalogs. Verwenden Sie Ihre üblichen Verfahren für Änderungskontrolle, Staging und Qualitätssicherung. Wenden Sie Aktualisierungen erst an, nachdem sich Merchandising- und SEO-Stakeholder auf die endgültige Kopie geeinigt haben.

Nachdem Sie eine Aktualisierung angewendet haben, wechseln die Vorschläge zu **[!UICONTROL Fixed Suggestions]** mit dem Status **Als behoben markiert**.

## Überprüfen der Anreicherung im Administrator {#verify-in-admin}

**So überprüfen Sie die angewendete Kataloganreicherung:**

1. Navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]** in der Commerce Admin Console.
1. Verwenden Sie Filter und den **[!UICONTROL Store View]** nach Bedarf (z. B. **[!UICONTROL Default Store View]**).
1. Suchen Sie nach der SKU.
1. Öffnen Sie das Produkt im Bearbeitungsmodus.

   Das Produktformular zeigt den angereicherten Produktnamen und/oder die Beschreibung an.

   ![Angereicherter Produktname](./assets/enriched-product-name.png)

1. Optional: Wählen Sie **[!UICONTROL Override Catalog Agent provided Product Name]** aus, wenn Sie stattdessen einen manuell eingegebenen Namen beibehalten möchten.

   Manuelle Überschreibungen beeinflussen, wie Vorschläge mit dem Katalog synchronisiert werden. Weitere Informationen finden Sie unter [Manuelles Überschreiben in der Admin](#manual-override-in-the-admin).

1. Erweitern Sie den Abschnitt **[!UICONTROL Content]** und suchen Sie das Feld Beschreibung .

   Die angereicherte Beschreibung wird angezeigt, wenn Sie Änderungen der Beschreibung angewendet haben.

   ![Produktbeschreibung anreichern](./assets/enrich-product-description.png)

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

- Die Anreicherung gilt nur für Produktnamen und lange Beschreibungen. Das PDP-Layout, Widgets oder andere Storefront-Inhalte auf Seitenebene werden nicht geändert.
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
