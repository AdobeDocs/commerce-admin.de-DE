---
title: Anwendungsfälle und Workflows für Angebotsvorlagen
description: Erstellen Sie eine Angebotsvorlage aus einem vorhandenen Angebot, um die Angebotsaushandlung für wiederkehrende Bestellungen zu optimieren.
feature: B2B, Quotes
exl-id: 7d1e7a3d-6c50-416a-b490-0a083e1c06b4
source-git-commit: 71b9326aa5a8c3d7656b3c0f166cf25291b2abba
workflow-type: tm+mt
source-wordcount: '1167'
ht-degree: 0%

---

# Anwendungsfall und Workflows für Angebotsvorlagen

Mit der Funktion „Angebotsvorlage“ können Käufer und Verkäufer den Angebotsprozess optimieren, indem sie wiederverwendbare und anpassbare Angebotsvorlagen erstellen.

- **Anpassbare Angebote** - Käufer können verknüpfte Angebote aus einer vorab genehmigten Vorlage generieren, sodass sie innerhalb bestimmter Parameter wie Positionsmengen und -auswahlen angepasst werden können.
- **Auftragsschwellen** - Verkäufer können Mindest- und Höchstauftragsverpflichtungen festlegen, um sicherzustellen, dass Käufer vereinbarte Kaufmengen einhalten. Nachdem der Käufer die Angebotsvorlage akzeptiert hat, erhöht sich die Anzahl des Bestellschwellenwerts jedes Mal, wenn ein verknüpftes Angebot generiert wird. Wenn das verknüpfte Angebot geschlossen wird, ohne in eine Bestellung umgewandelt zu werden, wird die Bestellung von der Schwellenwertanzahl abgezogen. Wenn der maximale Bestellschwellenwert erreicht ist, läuft die Angebotsvorlage ab.
- **Ablaufdaten** - Vorlagen können Gültigkeitszeiträume (*[!UICONTROL Valid Until]*) haben, sodass die Bedingungen nur innerhalb eines bestimmten Zeitraums angewendet werden können. Bei Ablauf wird die Vorlage geschlossen und alle zugehörigen verknüpften Anführungszeichen werden geschlossen.
- **Rabatte und Preise** - Verkäufer können dieselben Rabattfunktionen für Positionen, Angebotsebenen und Versandkosten verwenden, die auch für Angebote verfügbar sind, um Rabatte für wiederkehrende Bestellungen festzulegen und so den Verhandlungsprozess zu vereinfachen.
- **Tracking und Reporting** - Das System verfolgt die Anzahl der verknüpften Angebote, die aus der Vorlage generiert wurden, und erfolgreich abgeschlossene Bestellungen, um Einblicke in die Erfüllung der vereinbarten Bestellquoten zu erhalten.

## Anwendungsfall

Ein Unternehmenskäufer kann mithilfe einer Angebotsvorlage einen bestimmten Satz von Produkten über einen bestimmten Zeitraum bestellen. Der Käufer konfiguriert die folgenden Angebotsvorlagenoptionen, um den Angebotsprozess effizienter und konsistenter zu gestalten und mit strategischen Kaufvereinbarungen abzustimmen.

- Auftrags-Schwellenwert zur Angabe der Mindest- und Höchstanzahl der Aufträge, die für ausgehandelte Preise infrage kommen. Dies kann verwendet werden, um in Vertragsvereinbarungen angegebene Auftragskontingente anzuwenden und zu verfolgen.

- Mengenschwellen (Mindest-/Höchstmengen) Die Vorlage legt eine Mengenschwelle fest, um die Mindest- und Höchstmenge festzulegen, die für jede Bestellung gekauft werden kann, um sicherzustellen, dass der Verkäufer die Lagerbestände effektiv verwalten kann, während der Käufer die Flexibilität hat, die Mengen nach Bedarf anzupassen.

## Angebotsvorlagen-Workflow

Angebotsvorlagen können vom Käufer oder Verkäufer initiiert werden.

**Schritt 1: Erstellung einer Angebotsvorlage (neu)**

- **Käufer erstellt die Angebotsvorlage**

  Bei der Überprüfung eines bestehenden Angebots entscheidet der Käufer, dass das Unternehmen im Laufe des nächsten Jahres mehrere Bestellungen einreichen muss und zusätzliche Rabatte auf der Grundlage des Wiederholungsgeschäfts anfordern möchte. Sie erstellen eine Angebotsvorlage mithilfe der *[!UICONTROL Create quote template]* für das Angebot. Anschließend leiten sie die Verhandlung ein, indem sie die Angebotsvorlage zur Überprüfung an den Verkäufer senden.

  Käufer können auch eine Angebotsvorlage anfordern, indem sie Produkte, die sie regelmäßig kaufen möchten, zum Warenkorb hinzufügen. Fordern Sie dann ein Angebot an und geben Sie in den Kommentaren an, wie oft sie den Kauf wiederholen möchten.

- **Vertriebsmitarbeiter** - Ein Vertriebsmitarbeiter kann eine Angebotsvorlage vom Administrator im Namen eines bestimmten Einkäufers im Unternehmen erstellen. Der Vertriebsmitarbeiter kann die Angebotsvorlage im Administrator aus einem vorhandenen Angebot oder aus dem [!UICONTROL Quote Templates] erstellen und als `draft` speichern oder an den Käufer senden, um die Verhandlung zu starten. Im Entwurfsstatus ist das Angebot nur für den Verkäufer sichtbar. Sobald das Angebot gesendet wurde, ist der Status `Submitted`. Sie kann vom Verkäufer erst geändert werden, wenn der Käufer sie zurücksendet.

  ![Verkäufer, der ein Käuferangebot über das Angebotsraster im Admin initiiert](./assets/quote-template-create-from-grid.png){width="700" zoomable="yes"}

  Wenn der Verkäufer die Angebotsvorlage erstellt, beträgt das Ablaufdatum ([!UICONTROL Valid until]) standardmäßig 180 Tage. Wenn der Käufer die Vorlage erstellt hat, ist das Ablaufdatum leer.  Der Käufer muss das Ablaufdatum festlegen, bevor er die Vorlage zur Überprüfung an den Käufer zurücksendet.

  Wenn der Verkäufer die Angebotsvorlage erstellt, beträgt das Ablaufdatum (*[!UICONTROL Valid until]*) standardmäßig 180 Tage. Wenn der Käufer die Vorlage erstellt hat, ist das Ablaufdatum leer.  Der Käufer muss das Ablaufdatum festlegen, bevor er die Vorlage zur Überprüfung an den Käufer zurücksendet.

**Schritt 2: Angebotsüberprüfung und -verhandlung (Überprüfung)**

Das Überprüfen oder Verhandeln einer Angebotsvorlage kann das Ändern von Mengen, das Entfernen von Artikeln, das Hinzufügen von Positionskommentaren, das Anwenden von Positionsrabatten oder Angebotsrabatten (Verkäufer) und das Hinzufügen einer Lieferadresse (Käufer) umfassen.

- **Verkäufer zeigt Anfrage an und sendet Antwort** - Im Administrator zeigt der Verkäufer die Angebotsvorlage aus dem *[!UICONTROL Quote Templates]** Raster an oder öffnet sie über den Link in der E-Mail-Benachrichtigung. In der Storefront ändert sich der Status des Angebots in `Pending`, und der Käufer kann keine Änderungen vornehmen. Nach demselben Prozess für [Angebotsaushandlung](quote-price-negotiation.md) antwortet der Verkäufer, indem er Preisnachlässe anbietet und Mengen und Artikel nach Bedarf anpasst, gibt einen Kommentar ein und sendet die Angebotsvorlage an den Käufer zurück. Der Käufer und der Vertriebsmitarbeiter werden per E-Mail benachrichtigt, dass der Verkäufer geantwortet hat.

- **Der Käufer zeigt die Angebotsvorlage vom Verkäufer an und sendet eine Antwort** - Er klickt auf den Link in der E-Mail-Benachrichtigung, um die Angebotsvorlage zu öffnen, oder öffnet sie auf der Seite _Meine Angebotsvorlagen_ des Konto-Dashboards. Der Einkäufer kann dem Verkäufer Notizen auf der Positionsartikel- oder Angebotsebene hinterlassen, Mengen ändern und Artikel entfernen.

Der Käufer und der Verkäufer setzen den Verhandlungsprozess fort, bis eine Vereinbarung getroffen wird, oder der Verkäufer lehnt die Angebotsvorlage ab. Wenn der Käufer Änderungen an der Angebotsvorlage vornimmt - durch Hinzufügen oder Entfernen von Produkten oder Ändern von Produktmengen -, muss er zur Überprüfung an den Verkäufer zurückgeschickt werden.

- **Käufer fügt eine Lieferadresse hinzu** - Der Käufer muss der Angebotsvorlage eine Lieferadresse hinzufügen, wenn sie keine hat. Nachdem der Käufer die Adresse hinzugefügt hat, kann der Verkäufer Versand- und Lieferoptionen bereitstellen. Die angezeigten Versandmethoden hängen von der Storefront-Konfiguration ab.

Wenn der Käufer eine Lieferadresse hinzufügt, muss die Verhandlungsvereinbarung überprüft werden, und der Verkäufer kann den Verhandlungsprozess fortsetzen, bis eine Vereinbarung erzielt wird, oder der Verkäufer lehnt die Angebotsvorlage ab.

**Schritt 3: Käufer akzeptiert Angebotsvorlage**

Der Käufer akzeptiert die ausgehandelten Bedingungen in der Vorlage. Nachdem die Angebotsvorlage akzeptiert wurde, kann der Käufer sie verwenden, um [vorab genehmigte, verknüpfte Angebote zu generieren](account-dashboard-my-quote-templates.md#generate-a-linked-quote) die ohne weitere Verhandlung verwendet werden können, um Bestellungen einzureichen.

Versandoptionen sind beim Checkout gesperrt.

Angebotsvorlagen bleiben aktiv, bis sie ablaufen, storniert oder geschlossen werden oder der Käufer die maximale Bestellschwelle nicht mehr erreicht hat.

### Angebotsvorlage anzeigen

1. Klicken Sie in der Spalte **[!UICONTROL Actions]** für einen Datensatz auf **[!UICONTROL View]**.

1. Um auf die Kundenanfrage zu reagieren, befolgen Sie die Anweisungen und beginnen Sie denselben [Preisaushandlungsprozess](quote-price-negotiation.md) der für die Verhandlung von Angeboten verwendet wird.

### Angebotsvorlagenaktivität anzeigen

Zeigen Sie die Aktivität Verhandlungs-Zeitleiste, Kommunikation und andere Angebotsvorlagen aus der [!UICONTROL Comments] und [!UICONTROL History Log] an. Zu den Informationen gehören Statusänderungen, Aktualisierungen von Kunden- und Versandinformationen, Artikel- und Preisaktualisierungen und andere wichtige Informationen.

1. Öffnen Sie eine Angebotsvorlage.

1. Zeigen Sie Kommentare und den Verlauf von Angebotsverhandlungen an, indem Sie zu **[!UICONTROL Negotiation]** scrollen und **[!UICONTROL Comments]** und **[!UICONTROL History Log]** auswählen.

   ![Verlauf anzeigen](./assets/quote-view-history.png){width="400" zoomable="yes"}

1. Der Verlauf wird auch auf Zeileneingangsebene verfolgt.

   ![Positionsverlauf anzeigen](./assets/quote-view-line-item-history.png){width="400" zoomable="yes"}

### Angebotsvorlage ablehnen

Nur Angebotsvorlagen mit einem `In Review` können abgelehnt werden.

1. Öffnen Sie im *[!UICONTROL Quote Templates]* die Angebotsvorlage, die Sie ablehnen möchten.

1. Klicken Sie in der Angebotsvorlage auf **[!UICONTROL Decline]**.

1. Geben Sie bei Aufforderung den Grund für die Ablehnung des Angebots ein und klicken Sie auf **[!UICONTROL Confirm]**.
