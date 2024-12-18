---
title: CCPA-Konformität
description: Erfahren Sie mehr über den California Consumer Privacy Act (CCPA), mit dem die Rechte von Verbrauchern in Kalifornien erweitert werden, um zu bestimmen, wie ihre personenbezogenen Daten erfasst, gespeichert und verwendet werden.
exl-id: 165c8b78-683e-4015-b3c4-d3211750799e
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '2252'
ht-degree: 0%

---

# CCPA-Konformität

>[!NOTE]
>
>Diese Informationen sind nur ein Teil der Beiträge, die Adobe Commerce-Händlern und -Entwicklern helfen sollen, die Auswirkungen des California Consumer Privacy Act zu verstehen. Die Informationen basieren auf dem Text des Statuts. Um zu bestätigen, ob CCPA für Ihr Unternehmen gilt, wenden Sie sich an Ihren Anwalt.

Der [California Consumer Privacy Act][5] (CCPA) erweitert die Rechte von Verbrauchern in Kalifornien, um zu bestimmen, wie ihre personenbezogenen Daten erfasst, gespeichert und verwendet werden. Der Schwerpunkt liegt auf dem Schutz der Verbraucher vor dem unbefugten Verkauf oder Austausch ihrer personenbezogenen Daten. Der CCPA wurde 2018 erlassen und trat am 1. Januar 2020 in Kraft.

Der CCPA räumt den Verbrauchern die folgenden neuen Rechte ein:

- **Recht auf**: die Kategorien personenbezogener Daten über sie, die in den letzten 12 Monaten erfasst, verwendet, weitergegeben oder verkauft wurden.
- **Recht auf Löschung** bestimmter Arten personenbezogener Daten, die sich im Besitz eines Unternehmens und/oder seiner Dienstleister befinden.
- **Recht auf Abmeldung** vom Verkauf ihrer personenbezogenen Daten.
- **Recht auf Nichtdiskriminierung** in Bezug auf Preis oder Dienstleistung für die Ausübung eines Datenschutzrechts nach CCPA.

Für CCPA-Zwecke werden personenbezogene Daten in diesem Zusammenhang wie folgt definiert:

>Informationen, die einen bestimmten Verbraucher oder Haushalt identifizieren, sich darauf beziehen, beschreiben, mit ihm in Verbindung gebracht werden können oder vernünftigerweise direkt oder indirekt mit ihm in Verbindung gebracht werden könnten. (Abschnitt 1798.140)

In dieser Hinsicht deckt er bestimmte Datenelemente ab, die im Rahmen anderer Gesetze oder Vorschriften nicht als personenbezogene Daten betrachtet werden können. Händler sollten dies bei der Entscheidung, ob und wie sie das Gesetz einhalten sollten, beachten.

Der CCPA verpflichtet Unternehmen zudem, _angemessene Sicherheit_ zu gewährleisten, und enthält erweiterte Datenschutzbestimmungen für Verbraucher, einschließlich des Rechts, im Falle einer Verletzung des Datenschutzes rechtliche Schritte einzuleiten.

Besprechen Sie mit Ihrem Rechtsbeistand, ob und wie Sie die für Sie und Ihr Unternehmen geltenden CCPA-Anforderungen erfüllen sollten. Dazu gehören die neuen Bestimmungen über Mitteilung, Opt-out und Aufbewahrung von Aufzeichnungen, die Unternehmen in Übereinstimmung mit dem Gesetz umsetzen müssen.

## Geschäftsanforderungen

Der CCPA gilt für gewinnorientierte Unternehmen, die in Kalifornien Geschäfte tätigen und eine der folgenden Bedingungen erfüllen:

- Über einen Bruttojahresumsatz von über 25 Millionen US-Dollar verfügen
- Kaufen, empfangen oder verkaufen Sie die personenbezogenen Daten von 100.000 oder mehr Einwohnern, Haushalten oder Geräten in Kalifornien
- Erwirtschaften Sie 50 % oder mehr ihres Jahresumsatzes aus dem Verkauf der personenbezogenen Daten von Einwohnern Kaliforniens.

## CCPA-Konformitätshandbuch

In diesem Abschnitt finden Sie eine allgemeine Übersicht über die Schritte, die Händler unternehmen müssen, um Datenschutzbestimmungen wie den California Consumer Privacy Act (CCPA) einzuhalten.

### DSGVO und CCPA

Wenn Ihr Unternehmen sowohl die [Datenschutz-Grundverordnung (DSGVO](compliance-gdpr.md) als auch den CCPA einhalten muss, können Sie einen Teil der Arbeit aus Ihrem DSGVO-Compliance-Programm für den CCPA nutzen. Obwohl die Verordnungen einige Ähnlichkeiten aufweisen, gibt es einige Unterschiede:

- Die Definition der personenbezogenen Daten ist für jede Verordnung unterschiedlich.
- Die DSGVO verlangt von Verbrauchern, sich anzumelden, bevor ihre personenbezogenen Daten für bestimmte Zwecke verwendet werden können. Der CCPA bietet Verbrauchern das Recht, sich abzumelden.
- Der CCPA hat zusätzliche Anforderungen für die Dateninventarisierung und -zuordnung.
- Die Verordnungen haben unterschiedliche Datenschutzrichtlinien.

Unternehmen, die die DSGVO einhalten, können zusätzliche Verpflichtungen im Rahmen des CCPA haben. Weitere Informationen finden Sie im [CCPA Fact Sheet][3]{:target="_blank"}.

### Compliance-Roadmap

Für die Entwicklung und Umsetzung eines Plans zur Einhaltung der Vorschriften sind koordinierte Anstrengungen erforderlich. Verwenden Sie diese Roadmap als Leitfaden, um Ressourcen zu mobilisieren und Aufgaben zu priorisieren, damit Sie an mehreren Fronten vorankommen können. Der Vorgang ist für alle [!DNL Commerce] Anlagen im Wesentlichen gleich, mit folgender Ausnahme:

- **Adobe Commerce auf Cloud-Infrastruktur**: Händler mit auf Adobe gehosteten Stores [Cloud-Infrastruktur][4]{:target="_blank"} können bei der Beantwortung von Verbraucheranfragen den technischen Adobe Commerce-Kundenbetreuer oder den Support um Hilfe bitten.

- **On-Premise**: Händler mit On-Premise-Installationen von Adobe Commerce oder Magento Open Source müssen ihre eigenen Prozesse und Tools entwickeln, um auf Verbraucheranfragen im Zusammenhang mit Datenschutzbestimmungen zu reagieren und diese zu verwalten.

#### Schritt 1: Zusammenstellen eines funktionsübergreifenden Teams, um die Einhaltung der Vorschriften zu gewährleisten

Stellen Sie ein Team zusammen, das die folgenden funktionalen Rollen in Ihrem Unternehmen repräsentiert, und planen Sie eine Schulungssitzung, um sie mit den Rechtsvorschriften vertraut zu machen. Weisen Sie dann die erforderlichen Aufgaben den Stakeholdern nach Rolle zu.

- Geschäftsstrategie und Betrieb
- Rechtliches
- Informationstechnologie
- Benutzererlebnis
- Kundendienst
- Administrative Unterstützung

Aus geschäftlicher Sicht müssen Sie festlegen, ob Ihr Unternehmen diese Datenschutzmaßnahmen nur auf Verbraucher in Kalifornien ausweitet oder sie allen Verbrauchern unabhängig vom Standort zur Verfügung stellt.

#### Schritt 2: Bestandsaufnahme Ihrer digitalen Eigenschaften

**Stakeholder:** Informationstechnologie, rechtliche, administrative Unterstützung

Erfassen Sie eine Bestandsaufnahme Ihrer digitalen Objekte, einschließlich aller Integrationen, und wissen Sie, wer Zugriff auf Ihre Verbraucherdaten hat.

1. Legen Sie fest, welche öffentlichen und privaten personenbezogenen Daten über Ihre Websites und Mobile Apps erfasst werden. Eine standardmäßige Commerce-Datenbank speichert beispielsweise die folgenden Arten von öffentlichen und privaten personenbezogenen Daten:

   - **Public**: Wunschlisten, Produktbewertungen

   - **Privat**: Kundeninformationen, Bestellinformationen, Prämienpunkte, Geschenkregistrierung, Adressbuch, Warenkredit, Zahlungsmethoden, Abrechnungsvereinbarungen, Newsletter-Abonnements, Einladungen.

     Wenn Ihre [!DNL Commerce]-Installation angepasst wurde, werden möglicherweise zusätzliche persönliche Informationen erfasst. Persönliche Informationen können auch in [Cookies](./compliance-cookie-law.md), Tags und anderen Technologien gespeichert sein, die Informationen erfassen.

1. Identifizieren Sie die Parteien, mit denen Sie Daten teilen. Die Liste sollte Dienstleister und Dritte umfassen. Zu den Dritten gehören Werbenetzwerke, Internetdienstanbieter, Datenanalyseanbieter, Regierungsstellen, Betriebssysteme und Plattformen, soziale Netzwerke und Wiederverkäufer von Verbraucherdaten, die nicht direkt personenbezogene Daten von Ihren Verbrauchern erfassen.

   - **Dienstleister**: Entitäten, die für Geschäftszwecke Zugriff auf Ihre Verbraucherdaten haben und Services in Ihrem Namen bereitstellen. Beispielsweise ist Adobe ein Dienstleister, ebenso wie einige Entwickler von Anpassungen, Erweiterungen und Services.

     Überprüfen Sie die Standardeinstellungen von Google Universal Analytics, Google Tag Manager - und alle anderen von Ihnen verwendeten Datendienste - und nehmen Sie die erforderlichen Änderungen vor, um die Verordnung einzuhalten. Weitere Informationen finden Sie unter [Datenschutzeinstellungen für Google](../merchandising-promotions/google-tools.md#google-privacy-settings).

   - **Andere Dritte**: Entitäten, mit denen Sie Verbraucherdaten teilen oder verkaufen. Beispielsweise könnten Sie Verbraucherdaten im Austausch für Werbung an ein Werbenetzwerk weitergeben.

#### Schritt 3: Kunden-Journey und Datenerfassungsprozess in Ihren Stores zuordnen

**Stakeholder:** Benutzererlebnis, Informationstechnologie, administrative Unterstützung

1. Identifizieren Sie jeden Punkt auf der [Kunden-Journey], an dem personenbezogene Daten erfasst werden, sowie die Art der Informationen, die bei jedem Schritt erfasst werden.

   Besucher Ihrer Site müssen im Voraus oder zum Zeitpunkt der Datenerfassung benachrichtigt werden. Beispielsweise erfasst ein Store ohne benutzerdefinierte Integrationen persönliche Informationen, wenn ein Kundenkonto erstellt wird und während des Checkouts. Wenn Ihr Store über benutzerdefinierte Integrationen verfügt, können zusätzliche Datenelemente und Attribute identifiziert werden.

1. In den folgenden Themen finden Sie die entsprechenden Datenflussdiagramme und Datenbankentitätszuordnungen für jede Version:

   - [Referenz zu personenbezogenen Daten (2.x)][1]
   - [Referenz zu personenbezogenen Daten (1.x)][2]

   ![Diagramm](./assets/privacy-frontend-diagram.svg)

#### Schritt 4: Einrichten von Verfahren und Mechanismen für die Beantwortung von Kundenanfragen

**Stakeholder:** Kundendienst, Informationstechnologie, Anwendererlebnis, administrative Unterstützung

Aus Sicht des Daten-Managements bezieht jede Anfrage nach personenbezogenen Daten die folgenden Parteien ein:

- **Betroffene Personen** (Verbraucher): Im Rahmen des CCPA kann jede Person in Kalifornien, die personenbezogene Daten bereitstellt, um einen Kauf zu tätigen und/oder ein Kundenkonto zu unterhalten, einen Antrag auf Zugriff auf oder Löschung ihrer personenbezogenen Daten stellen.

- **Unternehmen, die als Unternehmen im Rahmen von CCPA** (Marken) handeln: [!DNL Commerce] Händler erfassen und speichern personenbezogene Daten von ihren Kunden und Gästen, die in ihren Geschäften Einkäufe tätigen.

- **Datenverarbeiter** (Technologieanbieter): Adobe Commerce und Magento Open Source handeln als Auftragsverarbeiter für personenbezogene Daten, die als Teil der für Händler bereitgestellten Services gespeichert werden. Als Auftragsverarbeiter verarbeitet Adobe personenbezogene Daten gemäß der Einwilligung und Weisungen des Händlers gemäß der Lizenzvereinbarung.

Händler sind für Folgendes verantwortlich:

1. Identifizieren Sie die an der Anfrage zum Zugriff auf die betroffene Person (Data Subject Access Request, DSAR) beteiligten Parteien und überprüfen Sie die Identität jeder Person, die darum bittet, sie zu kennen, abzumelden oder zu löschen. Dies gilt für eine Person, die über ein passwortgeschütztes Kundenkonto verfügt, oder für eine Person, die in Ihrem Geschäft als Gast einkauft.

1. auf Anfrage eines Verbrauchers innerhalb von 45 Tagen nach Eingang einer nachprüfbaren Verbraucheranfrage Informationen an den Verbraucher weitergeben und übermitteln, es sei denn, dies ist nicht möglich. (Das Gesetz enthält bestimmte andere Anforderungen an ein Unternehmen, die Einhaltung bei Verspätungen von bis zu 45 Tagen aufrechtzuerhalten.)

   Händler müssen jede DSAR innerhalb von 45 Tagen ab dem Tag des Eingangs der Anfrage beantworten. Bei Bedarf kann es bis zu 45 Tage dauern, bis der Händler reagiert, insgesamt also maximal 90 Tage ab dem Tag, an dem die Anfrage eingeht. Dies setzt voraus, dass der Händler den Kunden über den Grund der Verzögerung informiert.

1. Entwickeln Sie einen Mechanismus für die Darstellung der erforderlichen Benachrichtigungen in Ihrem Geschäft und die Erfassung von Verbraucherantworten.

1. Legen Sie Antwortverfahren fest und dokumentieren Sie jede der folgenden Anfragen:

   - **Anfragen an Know** - Besucher Ihres Geschäfts müssen über alle Vereinbarungen informiert werden, die Sie zum Verkauf oder zur Weitergabe ihrer personenbezogenen Daten an Dritte treffen müssen, und es muss ihnen erlaubt werden, sich abzumelden. Die Details über Ihre Verwendung personenbezogener Daten und die Parteien, mit denen Sie Daten teilen oder verkaufen, können in Ihrer Datenschutzerklärung gepflegt werden.

   - **Opt-out-Anfragen** - Wenn personenbezogene Daten gegen eine wertvolle Gegenleistung an Dritte verkauft oder übertragen werden, erfordert der CCPA an jedem Punkt, an dem sie erfasst werden, einen _Do Not Sell My_&quot;-Link. Zusätzliche benutzeraktivierte Eingabesteuerelemente wie Kontrollkästchen und Schaltflächen können in E-Mail-Nachrichten, Einstellungen für Website-Voreinstellungen oder in Website-Formularen am Punkt der Datenerfassung verwendet werden, damit Einzelpersonen eine gültige Opt-out-Anfrage senden können.

   - **Löschanfragen**

      - Händler, deren Stores auf Adobe Commerce Cloud gehostet werden, sollten sich an den Adobe-Support wenden, um Unterstützung beim Löschen personenbezogener Daten zu erhalten. Wenden Sie sich an Ihren technischen Kundenbetreuer für Adobe oder an den Support, um weitere Informationen zu erhalten.
      - Händler, die Installationen von Adobe Commerce oder Magento Open Source On-Premise ausführen, müssen ihren eigenen Prozess und ihr eigenes Skript implementieren, um personenbezogene Daten auf Anfrage zu löschen.

#### Schritt 5: Inhalt für die erforderlichen Kundenbenachrichtigungen schreiben

**Stakeholder:** Recht, Kundendienst, Anwendererlebnis, Informationstechnologie, administrative Unterstützung

1. Bestimmen Sie in Zusammenarbeit mit Ihrem Rechtsbeistand die Arten von Hinweisen, die Ihrer Website hinzugefügt werden sollten, um die CCPA-Verpflichtungen zu erfüllen.

   - **Benachrichtigung über die Erhebung**: Eine Benachrichtigung, die zu oder vor dem Zeitpunkt erfolgt, zu dem personenbezogene Daten vom Verbraucher erfasst werden. Der Hinweis sollte in einfacher Sprache verfasst sein und für die durchschnittliche Person leicht verständlich sein. Der Hinweis sollte auffällig sein und in einer oder mehreren Sprachen bereitgestellt werden, die auch für den Inhalt Ihrer Website gelten.

   - **Mitteilung über das Recht auf Opt-out**: Eine Mitteilung, die Verbraucher über ihr Recht informiert, den Verkauf ihrer personenbezogenen Daten abzubestellen.

   - **Hinweis zu finanziellen Anreizen** Ein Hinweis, in dem alle finanziellen Anreize, Preise oder Service-Unterschiede erläutert werden, die Ihr Unternehmen im Austausch für persönliche Informationen erhält.

   - **So senden Sie eine Anfrage zur Erfassung und Verwendung personenbezogener Daten**: Anweisungen für Einzelpersonen zur Einreichung einer Anfrage, dass Sie die personenbezogenen Daten, die Sie über die Person erfasst haben, offenlegen, einschließlich:

      - Spezifische persönliche Informationen, die Sie über den Verbraucher gesammelt haben
      - Kategorien personenbezogener Daten, die Sie über den Verbraucher gesammelt haben
      - Kategorien von Quellen, aus denen die personenbezogenen Daten erfasst werden
      - Kategorien von personenbezogenen Daten über den Verbraucher, die Sie zu Geschäftszwecken verkauft oder offen gelegt haben
      - Kategorien von Dritten, an die die personenbezogenen Daten zu Geschäftszwecken verkauft oder weitergegeben wurden
      - Die Gründe, warum Ihr Unternehmen personenbezogene Daten erfasst und/oder verkauft

1. Senden Sie den Inhalt an das Team und, wenn möglich, Ihren Rechtsbeistand zur Überprüfung.

1. Legen Sie fest, wo die Benachrichtigungen angezeigt werden, wie sie funktionieren (für jeden Besuch, bei der Authentifizierung oder beim Klicken) und ihre Position und ihr Format in Bezug auf andere Inhalte.

1. Übergeben Sie die genehmigten Inhalte an Ihr Entwicklungs-Team.

#### Schritt 6: Prüfen Sie Ihre Vereinbarungen mit Dienstleistern.

**Stakeholder:** rechtliche, administrative Unterstützung

Überprüfen und aktualisieren Sie bei Bedarf alle Dienstleisterverträge entsprechend den CCPA-Anforderungen.

#### Schritt 7: Aktualisieren Ihrer Datenschutzrichtlinie

**Stakeholder:** rechtliche, administrative Unterstützung

Überprüfen Sie Ihre aktuelle Datenschutzrichtlinie und überlegen Sie, welche zusätzlichen Offenlegungen erforderlich sind.

- **Verwendung personenbezogener Daten**: Sie müssen offenlegen, welche personenbezogenen Daten erfasst werden und welche finanziellen Anreize Sie im Austausch mit dem Verkauf personenbezogener Daten erhalten. Es ist auch erforderlich, dass Sie erklären, wie der Anreiz gemäß CCPA zulässig ist und wie der Wert der personenbezogenen Daten berechnet wird.

- **Alter der Einwilligung**: Wenn Sie personenbezogene Daten über Minderjährige erfassen oder verwenden, können Sie den folgenden Anforderungen unterliegen:

   - **Minderjährige &lt; 13**: Minderjährige unter 13 Jahren benötigen eine elterliche Genehmigung, um sich für den Verkauf ihrer personenbezogenen Daten zu entscheiden.

   - **Minderjährige 13 bis &lt; 16**: Minderjährige im Alter von mindestens 13 Jahren und unter 16 Jahren können sich für den Verkauf ihrer personenbezogenen Daten entscheiden, sofern das Unternehmen ein angemessenes Verfahren zur Dokumentation der Aktion einführt. Der Prozess muss in der „Datenschutzrichtlinie“ des [ beschrieben ](privacy-policy.md). Wenn ein Unternehmen Anfragen von Minderjährigen in dieser Altersgruppe erhält, muss es sie über ihr Recht informieren, diese später auszuschließen, und erklären, wie dies zu tun ist.

  >[!IMPORTANT]
  >
  >Es ist den Händlern untersagt, personenbezogene Daten von Kindern auf [!DNL Commerce] Plattform oder Systemen zu speichern. Wenn Grund zu der Annahme besteht, dass erfasste Daten einem Minderjährigen gehören, müssen sie sofort von einer [!DNL Commerce] entfernt werden, um einen Verstoß gegen die Adobe-Lizenzbedingungen zu vermeiden.

#### Schritt 8: Dokumentieren Sie alle damit verbundenen Verfahren und führen Sie Aufzeichnungen

**Stakeholder:** Kundendienst, administrative Unterstützung

Führen Sie über einen Zeitraum von 24 Monaten nach Erhalt jeder einzelnen Rechteanforderung ein Protokoll über die Anforderung und die Antwort Ihres Unternehmens.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m2.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m1.html
[3]: https://oag.ca.gov/system/files/attachments/press_releases/CCPA%20Fact%20Sheet%20%2800000002%29.pdf
[4]: https://www.adobe.com/commerce/magento.html
[5]: https://oag.ca.gov/privacy/ccpa
