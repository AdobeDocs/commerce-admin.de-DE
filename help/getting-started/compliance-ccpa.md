---
title: CCPA-Konformität
description: Erfahren Sie mehr über den California Consumer Privacy Act (CCPA), der die Rechte von Verbrauchern in Kalifornien erweitert, um zu bestimmen, wie ihre personenbezogenen Daten erfasst, gespeichert und verwendet werden.
exl-id: 165c8b78-683e-4015-b3c4-d3211750799e
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '2260'
ht-degree: 0%

---

# CCPA-Konformität

>[!NOTE]
>
>Diese Informationen sind eine von mehreren Themen, die Adobe Commerce-Händlern und -Entwicklern dabei helfen, die Auswirkungen des California Consumer Privacy Act zu verstehen. Die Informationen basieren auf dem Statut. Wenden Sie sich an Ihren Anwalt, um zu bestätigen, ob der CCPA für Ihr Unternehmen gilt.

Die [California Consumer Privacy Act][5] (CCPA) erweitert die Rechte der Verbraucher in Kalifornien, um zu bestimmen, wie ihre personenbezogenen Daten erfasst, gespeichert und verwendet werden. Der Schwerpunkt liegt auf dem Schutz der Verbraucher vor unbefugtem Verkauf, Austausch oder personenbezogenen Daten. Der CCPA wurde 2018 erlassen und trat am 1. Januar 2020 in Kraft.

Der CCPA verleiht den Verbrauchern die folgenden neuen Rechte:

- **Recht auf Information** die Kategorien personenbezogener Daten, die in den letzten 12 Monaten erfasst, verwendet, weitergegeben oder verkauft wurden.
- **Recht auf Löschung** bestimmte Arten von personenbezogenen Daten, die im Besitz eines Unternehmens und/oder seiner Dienstleister sind.
- **Recht auf Abmeldung** des Verkaufs ihrer personenbezogenen Daten.
- **Recht auf Nichtdiskriminierung** in Bezug auf den Preis oder die Dienstleistung, die für die Ausübung eines Datenschutzrechts im Rahmen des CCPA gewährt wurde.

Für CCPA-Zwecke werden personenbezogene Daten in diesem Kontext definiert als:

>Informationen, die einen bestimmten Verbraucher oder Haushalt identifizieren, sich darauf beziehen, beschreiben, mit ihm in Verbindung gebracht werden können oder die vernünftigerweise direkt oder indirekt mit ihm verknüpft werden könnten. (Abschnitt 1798.140)

In diesem Zusammenhang werden bestimmte Datenelemente behandelt, die im Rahmen anderer Gesetze oder Vorschriften nicht als personenbezogene Daten betrachtet werden können. Händler sollten dies bei der Entscheidung berücksichtigen, ob und wie sie das Gesetz einhalten sollten.

Der CCPA verpflichtet Unternehmen auch zur Bereitstellung von _angemessene Sicherheit_ und enthält erweiterte Datenschutzbestimmungen für Verbraucher, einschließlich des Rechts, rechtliche Schritte einzuleiten, wenn ein Datenverstoß vorliegt.

Wenden Sie sich an Ihren Rechtsbeistand, um festzustellen, ob und wie Sie alle CCPA-Anforderungen erfüllen sollten, die für Sie und Ihr Unternehmen gelten können. Dazu gehören die neuen Anforderungen an die Benachrichtigung, das Opt-out und die Aufzeichnung, die Unternehmen gemäß den gesetzlichen Bestimmungen umsetzen müssen.

## Geschäftsanforderungen

Der CCPA gilt für gewinnorientierte Unternehmen, die in Kalifornien Geschäfte tätigen und eine der folgenden Voraussetzungen erfüllen:

- einen Jahresumsatz von mehr als 25 Millionen Dollar haben
- Kaufen, empfangen oder verkaufen Sie die personenbezogenen Daten von 100.000 oder mehr kalifornischen Einwohnern, Haushalten oder Geräten.
- Ableiten von 50 % oder mehr des Jahresumsatzes aus dem Verkauf von personenbezogenen Daten kalifornischer Einwohner.

## CCPA-Compliance-Handbuch

In diesem Abschnitt werden die Schritte erläutert, die Händler zur Einhaltung von Datenschutzbestimmungen wie dem California Consumer Privacy Act (CCPA) unternehmen müssen.

### DSGVO und CCPA

Wenn Ihr Unternehmen sowohl die [Die Datenschutz-Grundverordnung](compliance-gdpr.md) (DSGVO) und dem CCPA können Sie einen Teil der Arbeit aus Ihrem DSGVO-Compliance-Programm für den CCPA verwenden. Obwohl die Verordnungen einige Ähnlichkeiten aufweisen, gibt es einige Unterschiede:

- Die Definition der personenbezogenen Daten ist für jede Verordnung unterschiedlich.
- Die DSGVO schreibt vor, dass Verbraucher sich anmelden müssen, bevor ihre personenbezogenen Daten für bestimmte Zwecke verwendet werden dürfen. Der CCPA bietet Verbrauchern das Recht, sich abzumelden.
- Der CCPA verfügt über zusätzliche Anforderungen an das Dateninventar und die Zuordnung.
- Die Vorschriften enthalten unterschiedliche Anforderungen an die Datenschutzrichtlinien.

Unternehmen, die die DSGVO einhalten, haben möglicherweise zusätzliche Verpflichtungen im Rahmen des CCPA. Weitere Informationen finden Sie unter [CCPA-Datenblatt][3]{:target=&quot;_blank&quot;}.

### Compliance-Roadmap

Es bedarf koordinierter Anstrengungen, um einen Plan zur Einhaltung der Vorschriften zu entwickeln und umzusetzen. Verwenden Sie diesen Fahrplan als Leitfaden, um Ressourcen zu mobilisieren und Aufgaben zu priorisieren, damit Sie an mehreren Fronten vorankommen können. Der Prozess ist im Wesentlichen für alle gleich [!DNL Commerce] Installationen, mit der folgenden Ausnahme:

- **Adobe Commerce auf Cloud-Infrastruktur**: Händler mit auf Adobe gehosteten Stores [Cloud-Infrastruktur][4]{:target=&quot;_blank&quot;} kann den technischen Kundenbetreuer von Adobe Commerce oder den Kundensupport um Hilfe bei der Beantwortung von Kundenanfragen bitten.

- **On-Premise**: Händler mit On-Premise-Installationen von Adobe Commerce oder Magento Open Source müssen eigene Prozesse und Tools entwickeln, um auf Anfragen von Verbrauchern im Zusammenhang mit Datenschutzbestimmungen zu reagieren und diese zu verwalten.

#### Schritt 1: Zusammenstellen eines funktionsübergreifenden Teams zur Einhaltung von Vorschriften

Stellen Sie ein Team zusammen, das die folgenden funktionalen Rollen in Ihrem Unternehmen repräsentiert, und planen Sie eine Schulungssitzung, um sie auf den neuesten Stand der Gesetzgebung zu bringen. Weisen Sie dann die erforderlichen Aufgaben den Interessengruppen nach Rolle zu.

- Geschäftsstrategie und Betrieb
- Legal
- Informationstechnologie
- Anwendererlebnis
- Kundendienst
- Administrative Unterstützung

Aus geschäftlicher Sicht müssen Sie feststellen, ob Ihr Unternehmen diese Datenschutzmaßnahmen nur auf Verbraucher in Kalifornien ausdehnt oder sie allen Verbrauchern unabhängig vom Standort zur Verfügung stellt.

#### Schritt 2: Bestandsaufnahme Ihrer digitalen Eigenschaften

**Interessenträger:** Informationstechnologie, Rechtliche und administrative Unterstützung

Nehmen Sie eine Bestandsaufnahme Ihrer digitalen Eigenschaften vor, einschließlich aller Integrationen und Personen, die Zugriff auf Ihre Verbraucherdaten haben.

1. Bestimmen Sie, welche öffentlichen und privaten personenbezogenen Daten über Ihre Websites und mobilen Anwendungen erfasst werden. Eine Standard-Commerce-Datenbank speichert beispielsweise die folgenden Arten von öffentlichen und privaten personenbezogenen Daten:

   - **Öffentlich**: Wunschlisten, Produktbewertungen

   - **Privat**: Kundeninformationen, Bestellinformationen, Treuepunkte, Gift Registry, Adressbuch, Store-Guthaben, Zahlungsmethoden, Abrechnungsabkommen, Newsletter-Abonnements, Einladungen.

     Wenn [!DNL Commerce] -Installation angepasst wurde, können zusätzliche persönliche Daten erfasst werden. Personenbezogene Daten können sich auch in [Cookies](./compliance-cookie-law.md), Tags und andere Technologien, die Informationen erfassen.

1. Identifizieren Sie die Parteien, für die Sie Daten freigeben. Die Liste sollte Dienstleister und Dritte umfassen. Zu Dritten gehören Werbenetzwerke, Internetdienstanbieter, Datenanalyseanbieter, Regierungsstellen, Betriebssysteme und Plattformen, soziale Netzwerke und Wiederverkäufer von Verbraucherdaten, die keine direkten personenbezogenen Daten von Ihren Verbrauchern erfassen.

   - **Dienstleister**: Entitäten, die Zugriff auf Ihre Verbraucherdaten für einen geschäftlichen Zweck haben und in Ihrem Namen Dienste anbieten. Beispielsweise ist Adobe Dienstleister, ebenso wie einige Entwickler von Anpassungen, Erweiterungen und Diensten.

     Überprüfen Sie die Standardeinstellungen von Google Universal Analytics, Google Tag Manager und allen anderen von Ihnen verwendeten Datendiensten und nehmen Sie alle erforderlichen Änderungen vor, um der Verordnung zu entsprechen. Weitere Informationen finden Sie unter [Google-Datenschutzeinstellungen](../merchandising-promotions/google-tools.md#google-privacy-settings).

   - **Andere Dritte**: Entitäten, für die Sie Verbraucherdaten freigeben oder verkaufen. Beispielsweise können Sie Verbraucherdaten für ein Werbenetzwerk im Austausch gegen Werbung freigeben.

#### Schritt 3: Zuordnen des Journey- und Datenerfassungsprozesses für Kunden in Ihren Geschäften

**Interessenträger:** Benutzererfahrung, Informationstechnologie, administrative Unterstützung

1. Identifizieren Sie jeden Punkt im [Journey] wo personenbezogene Daten erfasst werden und welche Art von Informationen bei jedem Schritt erfasst werden.

   Besucher Ihrer Site müssen im Voraus oder an der Stelle der Datenerfassung benachrichtigt werden. Beispiel: Ein Store ohne benutzerdefinierte Integrationen erfasst personenbezogene Daten, wenn ein Kundenkonto erstellt wird und während der Kasse. Wenn Ihr Store über benutzerdefinierte Integrationen verfügt, kann es zusätzliche Datenelemente und Attribute zur Identifizierung geben.

1. In den folgenden Themen finden Sie relevante Datenflussdiagramme und Zuordnungen von Datenbankentitäten für jede Version:

   - [Referenz zu personenbezogenen Daten (2.x)][1]
   - [Referenz zu personenbezogenen Daten (1.x)][2]

   ![Diagramm](./assets/privacy-frontend-diagram.svg)

#### Schritt 4: Einrichten von Verfahren und Mechanismen zur Beantwortung von Kundenanfragen

**Interessenträger:** Kundendienst, Informationstechnologie, Benutzererlebnis, administrativer Support

Im Hinblick auf das Datenmanagement bezieht sich jede Anfrage nach personenbezogenen Daten auf die folgenden Personen:

- **Datensubjekte** (Verbraucher): Im Rahmen des CCPA kann jede Person in Kalifornien, die personenbezogene Daten für einen Kauf und/oder die Führung eines Kundenkontos bereitstellt, eine Anfrage zum Zugriff auf oder zur Löschung ihrer personenbezogenen Daten einreichen.

- **Unternehmen, die als Unternehmen im Rahmen des CCPA tätig sind** (Marken): [!DNL Commerce] Händler sammeln und speichern personenbezogene Daten von ihren Kunden und Gästen, die in ihren Geschäften Einkäufe tätigen.

- **Datenverarbeiter** (Technologieanbieter): Adobe Commerce und Magento Open Source fungieren als Verarbeiter der personenbezogenen Daten, die als Teil der Dienstleistungen für Händler gespeichert werden. Als Auftragsverarbeiter verarbeitet Adobe personenbezogene Daten gemäß der Lizenzvereinbarung gemäß den Berechtigungen und Anweisungen des Händlers.

Händler sind dafür verantwortlich, Folgendes zu tun:

1. Identifizieren Sie die an der Data Subject Access Request (DSAR) beteiligten Parteien und überprüfen Sie die Identität aller Personen, die Informationen benötigen, sich abmelden oder löschen möchten. Dies gilt für eine Person, die über ein kennwortgeschütztes Kundenkonto verfügt oder die in Ihrem Geschäft als Gast einkauft.

1. Offenlegen und Übermitteln von Informationen an einen Verbraucher, wenn er eine Rechteanforderung erhält, innerhalb von 45 Tagen nach Erhalt einer überprüfbaren Verbraucheranfrage durch den Verbraucher, sofern dies nicht möglich ist. (Das Gesetz enthält bestimmte weitere Anforderungen an ein Unternehmen, damit es bei Verspätungen von bis zu 45 Tagen die Vorschriften einhalten kann.)

   Händler müssen innerhalb von 45 Tagen ab dem Tag des Eingangs der Anfrage auf jede SAR antworten. Bei Bedarf können Händler bis zu 45 weitere Tage benötigen, um auf die Anfrage zu antworten. Dies dauert maximal 90 Tage ab dem Tag, an dem die Anfrage empfangen wird. Dies erfordert, dass der Händler den Kunden zur Erläuterung der Gründe für die Verzögerung auffordert.

1. Entwickeln Sie einen Mechanismus zur Präsentation der erforderlichen Benachrichtigungen in Ihrem Geschäft und zur Erfassung der Kundenreaktionen.

1. Richten Sie Reaktionsverfahren ein und dokumentieren Sie jede der folgenden Anforderungen:

   - **Anforderungen, die Sie kennen** - Besucher Ihres Geschäfts müssen über alle Vorkehrungen informiert werden, die Sie zum Verkauf oder zur Weitergabe Ihrer persönlichen Daten an Dritte treffen müssen, und sie müssen die Möglichkeit haben, sich abzumelden. Die Details Ihrer Nutzung personenbezogener Daten und die Parteien, mit denen Sie Daten teilen oder verkaufen, können in Ihrer Datenschutzerklärung beibehalten werden.

   - **Opt-out-Anfragen** - Werden personenbezogene Daten im Austausch gegen wertvolle Gegenleistung an Dritte verkauft oder weitergegeben, so erfordert der CCPA eine _Meine Informationen nicht verkaufen_ an jedem Ort, an dem sie erfasst wird. Zusätzliche benutzeraktivierte Eingabedialoge wie Checkboxes und Schaltflächen können in E-Mail-Kommunikation, Einstellungen für Website-Voreinstellungen oder in Website-Formularen zum Zeitpunkt der Datenerfassung verwendet werden, damit Einzelpersonen eine gültige Opt-out-Anfrage senden können.

   - **Löschanfragen**

      - Händler, deren Geschäfte auf Adobe Commerce Cloud gehostet werden, sollten sich an den Adobe-Support wenden, um Hilfe beim Löschen personenbezogener Daten zu erhalten. Wenden Sie sich für weitere Informationen an Ihren technischen Kundenbetreuer oder an den Kundensupport von Adobe.
      - Händler, die Installationen von Adobe Commerce oder Magento Open Source On-Premise ausführen, müssen einen eigenen Prozess und ein eigenes Skript implementieren, um personenbezogene Daten auf Anfrage zu löschen.

#### Schritt 5: Inhalt für die erforderlichen Kundenbenachrichtigungen schreiben

**Interessenträger:** Recht, Kundendienst, Benutzererfahrung, Informationstechnologie, Administrationsunterstützung

1. Legen Sie in Zusammenarbeit mit Ihrem Rechtsbeistand fest, welche Arten von Hinweisen zu Ihrer Website hinzugefügt werden sollen, um CCPA-Verpflichtungen zu erfüllen.

   - **Mitteilung über die Erhebung**: Ein Hinweis, der zum Zeitpunkt oder vor dem Zeitpunkt der Erfassung personenbezogener Daten beim Verbraucher abgegeben wird. Der Hinweis sollte in einfacher Sprache verfasst und für den Durchschnittsbürger leicht verständlich sein. Der Hinweis sollte auffällig sein und in mindestens einer Sprache wie dem Inhalt Ihrer Website bereitgestellt werden.

   - **Hinweis zum Opt-out**: Ein Hinweis, der Verbraucher über ihr Recht informiert, sich vom Verkauf ihrer personenbezogenen Daten abzumelden.

   - **Bekanntmachung finanzieller Anreize**: Ein Hinweis, der jeden finanziellen Anreiz, Preis oder Service-Unterschied erläutert, den Ihr Unternehmen im Austausch für personenbezogene Daten erhält.

   - **Senden einer Anfrage zur Erfassung und Verwendung personenbezogener Daten**: Anleitung für Einzelpersonen zur Einreichung einer Anfrage zur Offenlegung der von Ihnen erfassten personenbezogenen Daten, einschließlich:

      - Bestimmte persönliche Daten, die Sie über den Verbraucher gesammelt haben
      - Kategorien personenbezogener Daten, die Sie über den Verbraucher erfasst haben
      - Kategorien von Quellen, aus denen die personenbezogenen Daten erfasst werden
      - Kategorien personenbezogener Daten über den Verbraucher, die Sie für einen geschäftlichen Zweck verkauft oder offen gelegt haben
      - Kategorien von Dritten, an die die personenbezogenen Daten für einen geschäftlichen Zweck verkauft oder weitergegeben wurden
      - Die Gründe, aus denen Ihr Unternehmen personenbezogene Daten erfasst und/oder verkauft

1. Senden Sie den Inhalt an das Team und, wenn möglich, Ihren Rechtsbeistand zur Überprüfung.

1. Bestimmen Sie, wo die Hinweise erscheinen, wie sie funktionieren (für jeden Besuch, bei der Authentifizierung oder beim Clickthrough) und ihre Position und ihr Format in Bezug auf andere Inhalte.

1. Übergeben Sie den genehmigten Inhalt an Ihr Entwicklungsteam.

#### Schritt 6: Ihre Vereinbarungen mit Dienstleistern überprüfen

**Interessenträger:** Rechtliche und administrative Unterstützung

Überprüfen und aktualisieren Sie bei Bedarf alle Dienstleisterverträge entsprechend den CCPA-Anforderungen.

#### Schritt 7: Datenschutzrichtlinie aktualisieren

**Interessenträger:** Rechtliche und administrative Unterstützung

Überprüfen Sie Ihre aktuelle Datenschutzrichtlinie und überlegen Sie, welche zusätzlichen Offenlegungen erforderlich sind.

- **Verwendung personenbezogener Daten**: Sie müssen angeben, welche personenbezogenen Daten erhoben werden und welche finanziellen Anreize Sie im Austausch gegen den Verkauf personenbezogener Daten erhalten. Außerdem müssen Sie erläutern, wie der Anreiz im Rahmen des CCPA zulässig ist und wie der Wert der personenbezogenen Daten berechnet wird.

- **Alter der Zustimmung**: Wenn Sie personenbezogene Daten über Minderjährige sammeln oder verwenden, können die folgenden Voraussetzungen erfüllt sein:

   - **Minderjährige &lt; 13**: Für Minderjährige unter 13 Jahren ist eine elterliche Genehmigung erforderlich, um sich dem Verkauf ihrer personenbezogenen Daten anzuschließen.

   - **Minderjährige 13 bis &lt; 16**: Minderjährige, die mindestens 13 und weniger als 16 Jahre alt sind, können sich dem Verkauf ihrer personenbezogenen Daten anschließen, sofern das Unternehmen einen angemessenen Prozess zur Dokumentierung der Maßnahme einleitet. Der Prozess muss im [Datenschutzrichtlinie](privacy-policy.md). Wenn ein Unternehmen Anfragen von Minderjährigen in dieser Altersgruppe erhält, muss es sie über ihr Recht auf spätere Abmeldung informieren und erläutern, wie dies zu tun ist.

  >[!IMPORTANT]
  >
  >Kaufleute dürfen die personenbezogenen Daten von Kindern nicht in [!DNL Commerce] Plattform oder Systeme. Wenn Grund zu der Annahme besteht, dass die erfassten Daten zu einem Minderjährigen gehören, müssen sie aus einem [!DNL Commerce] -Plattform, um einen Verstoß gegen die Adobe-Lizenzbedingungen zu vermeiden.

#### Schritt 8: Dokumentieren Sie alle zugehörigen Verfahren und führen Sie Aufzeichnungen.

**Interessenträger:** Kundendienst, Verwaltungs-Support

Führen Sie 24 Monate lang nach Erhalt jeder einzelnen Rechteanforderung einen Datensatz mit der Anfrage und der Antwort Ihres Unternehmens auf diese Anfrage.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m2.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m1.html
[3]: https://oag.ca.gov/system/files/attachments/press_releases/CCPA%20Fact%20Sheet%20%2800000002%29.pdf
[4]: https://www.adobe.com/commerce/magento.html
[5]: https://oag.ca.gov/privacy/ccpa
