---
title: Negotiable Anführungszeichen
description: Erfahren Sie mehr über Zitat-Workflows und wie Sie diesen Dienst für Ihre Unternehmenskonten bereitstellen können.
exl-id: c278818b-fa5a-4e7a-8ca2-c4b757da4f05
feature: B2B, Quotes
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 0%

---

# Negotiable Anführungszeichen

Käufer und Verkäufer verwenden Anführungszeichen, um den Verhandlungsprozess für bestellbare Artikel zu verwalten, die Mengen zu aktualisieren, Rabatte anzufordern und anzuwenden usw., bis sie eine Einigung erzielen. Der Prozess der Preisverhandlungen kann von einem autorisierten Firmenkäufer oder von einem Vertriebsmitarbeiter eingeleitet werden.

Angebote können von einem autorisierten Firmenkäufer oder einem Vertriebsmitarbeiter initiiert werden. Nach Erstellung des Angebots beginnt der Verhandlungsprozess, sobald der Käufer oder Verkäufer das Angebot zur Überprüfung einreicht. Das Raster _Angebote_ , das jedes erhaltene Angebot auflistet und einen Verlauf der Kommunikation zwischen Käufer und Verkäufer pflegt. Verwenden Sie die standardmäßigen [Arbeitsplatzsteuerelemente](../getting-started/admin-workspace.md), um die Liste zu filtern, das Spaltenlayout zu ändern, Ansichten zu speichern und Daten zu exportieren.

- In der Storefront reichen Käufer das Angebot als [Anfrage ein, den Preis aus dem Warenkorb zu verhandeln](quote-price-negotiation.md). Bei der Erstellung des Angebots kann ein Käufer das Angebot als Entwurf speichern oder direkt an den Verkäufer übermitteln.

- Im Admin können Vertriebsmitarbeiter Angebote im Namen des Firmenkäufers erstellen. Bei der Erstellung des Angebots kann ein Verkäufer das Angebot als Entwurf speichern oder es direkt an den Käufer senden, um den Verhandlungsprozess einzuleiten.

Während des Verhandlungsprozesses kann das Zitat nur von der Person aktualisiert werden, die Bedingungen für weitere Verhandlungen überprüft und vorschlägt.

## Voraussetzungen

Negative Anführungszeichen sind nur verfügbar, wenn Adobe Commerce die folgenden Konfigurationseinstellungen aufweist:

- [Die Adobe Commerce B2B-Erweiterung ist installiert.](install.md)
- [Konfigurierte B2B-Funktionen](enable-basic-features.md)
   - Unternehmenskonten aktivieren
   - B2B-Anführungszeichen aktivieren

## Anführungsarbeitsablauf

Angebote können vom Käufer oder vom Verkäufer initiiert werden.

**Schritt 1: Erstellung von Zitaten**

- **Käufer fordert Angebot** an - Der Käufer [fordert ein Angebot](quote-request.md) vom Warenkorb an. Die Anfrage wird in der Liste _Meine Angebote_ im Konto-Dashboard des Käufers angezeigt und die E-Mail-Benachrichtigung wird an den Vertriebsmitarbeiter gesendet, der dem Unternehmenskonto zugewiesen ist. Im Admin wird die Anforderung im Raster _Anführungszeichen_ mit dem Status `New` angezeigt. Ein Angebot kann vom Käufer bis zur Eröffnung durch den Verkäufer geändert werden.

  ![Anführungszeichen](./assets/quote-request-from-shopping-cart.png){width="700" zoomable="yes"}


- **Vertriebsmitarbeiter** - Ein Vertriebsmitarbeiter kann [vom Administrator ein Angebot](sales-rep-initiates-quote.md) für einen bestimmten Firmenkäufer erstellen. Der Kundenbetreuer muss das Angebot aktualisieren, um dem Käufer Produkte und andere Informationen wie Rabatte und Hinweise hinzuzufügen. Die Vertriebsdarstellung kann das Angebot als `draft` speichern oder an den Käufer senden, um die Verhandlungen zu beginnen. Im Entwurfszustand ist das Angebot nur für den Verkäufer sichtbar. Sobald das Anführungszeichen gesendet wurde, lautet der Status `Submitted`. Er kann vom Verkäufer erst geändert werden, wenn der Käufer ihn zurücksendet.

  ![Verkäufer, die ein Käuferangebot aus dem Quotes-Raster in Admin initiieren](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}


**Schritt 2: Überprüfung und Verhandlung eines Zitats**

**Der Verkäufer zeigt die Anfrage an und sendet die Antwort** - In der Admin-Ansicht zeigt der Verkäufer die Anfrage nach einem Angebot an. Der Status des Kurses ändert sich in `Pending`, und der Käufer kann keine Änderungen vornehmen. Der [Verkäufer antwortet](quote-price-negotiation.md), indem er den Rabatt für die Produkte im Angebot anbietet, einen Kommentar eingibt und das Angebot an den Käufer zurücksendet. Der Käufer und der Vertriebsmitarbeiter werden per E-Mail darüber informiert, dass der Verkäufer geantwortet hat.

**Der Käufer sieht das Angebot vom Verkäufer an und sendet die Antwort** - Der Käufer klickt auf den Link in der E-Mail-Benachrichtigung, um das Angebot zu öffnen, oder er öffnet das Angebot auf der Seite _Meine Angebote_ des Konto-Dashboards. Der Käufer kann dem Verkäufer Notizen auf der Posten- oder Angebotsebene hinterlassen und Artikel entfernen.

Der Käufer und der Verkäufer können den Verhandlungsprozess fortsetzen, bis eine Vereinbarung getroffen wird, oder der Verkäufer lehnt das Angebot ab. Wenn der Käufer Änderungen am Angebot vornimmt, d. h. Produkte hinzufügt, entfernt oder die Produktmengen ändert, muss das Angebot zur Überprüfung an den Verkäufer zurückgegeben werden.

**Schritt 4: Der Käufer akzeptiert das Angebot** - Der Käufer nimmt den vorgeschlagenen Preis an und checkt weiter aus. Dem ausgehandelten Angebot können keine zusätzlichen Rabatte hinzugefügt werden.

## B2B-Rollenressourcen für Store-Anführungszeichen

Konfigurationsoptionen für Anführungszeichen werden mit den [Rollenressourcen](../systems/permissions-user-roles.md#role-resources) gesteuert. Diese Rollenressourcen müssen für die Administratorrolle festgelegt sein, die dem Store-Administrator zugewiesen ist.

Um Zugriff auf Anführungszeichenfunktionen im Admin zu gewähren, gehen Sie zu &quot;**[!UICONTROL System]**&quot;> &quot;_[!UICONTROL Permissions]_&quot;> &quot;**[!UICONTROL User Roles]**&quot;, wählen Sie die Rolle aus und navigieren Sie zu &quot;[!UICONTROL Sales]&quot;> &quot;[!UICONTROL Operations]&quot;> &quot;[!UICONTROL Quotes]&quot;im Baum &quot;_ Rollenressourcen _&quot;.

## Anwenden einer Aktion

In der Admin-Konsole können B2B-Administratoren und -Verkäufer Anführungszeichen aus dem Anführungszeichenraster über das Menü [!UICONTROL Actions] verwalten.

![Anführungszeichen](./assets/quotes-grid.png){width="700" zoomable="yes"}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > **[!UICONTROL Quotes]**.

1. Aktivieren Sie in der ersten Spalte des Rasters das Kontrollkästchen für jeden Datensatz, auf den Sie die Aktion anwenden möchten.

1. Wählen Sie im Feld **[!UICONTROL Actions]** die anzuwendende Aktion aus.

### Ansehen eines Angebots

1. Klicken Sie in der Spalte **[!UICONTROL Actions]** für einen Datensatz auf **[!UICONTROL View]**.

1. Um auf die Kundenanfrage zu reagieren, befolgen Sie die Anweisungen und beginnen Sie mit dem Prozess [Preisverhandlungen](quote-price-negotiation.md) .

### Anführungsaktivität

Zeigen Sie die Verhandlungs-Timeline, die Kommunikation und andere Kursaktivitäten aus den [!UICONTROL Comments] und [!UICONTROL History Log] an - Informationen umfassen Statusänderungen, Aktualisierungen von Kunden- und Versandinformationen, Artikel- und Preisaktualisierungen sowie andere wichtige Informationen.

1. Öffnen Sie ein Zitat.

1. Sehen Sie sich Kommentare und den Verlauf von Zitat-Verhandlungen an, indem Sie zu **[!UICONTROL Negotiation]** scrollen und **[!UICONTROL Comments]** und **[!UICONTROL History Log]** auswählen.

   ![Ansichtsverlauf](./assets/quote-view-history.png){width="400"}

1. Der Verlauf wird auch auf Zeileneintrag-Ebene verfolgt.

   ![Anzeigen des Zeilenelementverlaufs](./assets/quote-view-line-item-history.png){width="400"}


### Anforderung eines Anführungszeichens ablehnen

Es können nur Zitat-Anfragen mit dem Status `Open` abgelehnt werden.

1. Wählen Sie jede offene Anführungsanforderung aus, die Sie ablehnen möchten.

1. Setzen Sie das Steuerelement _[!UICONTROL Actions]_auf `Declined`.

1. Geben Sie bei Aufforderung den Grund für die Ablehnung des Anführungszeichens ein und klicken Sie auf **[!UICONTROL Confirm]**.

   ![Zitat streichen?](./assets/quote-decline-confirm.png){width="400"}


## Spaltenbeschreibungen

| Spalte | Beschreibung |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Select] | Um die Anführungszeichen für eine Aktion auszuwählen, aktivieren Sie das Kontrollkästchen oder verwenden Sie das Auswahlsteuerelement in der Spaltenüberschrift. Optionen: Alle auswählen/Auswahl aufheben |
| [!UICONTROL ID] | Eine eindeutige numerische Kennung, die zugewiesen wird, wenn eine Angebotsanforderung aus dem Warenkorb eines Käufers eingereicht wird. Bei Ansicht des Anführungszeichens wird die ID anstelle des Anführungszeichens oben auf der Seite angezeigt. |
| [!UICONTROL Name] | Der Name, der einer Preisanfrage des Käufers zugewiesen wurde. |
| [!UICONTROL Created Date] | Datum und Uhrzeit der ersten Einreichung des Angebotsantrags durch den Käufer. |
| [!UICONTROL Company] | Name der Gesellschaft, für die ein Käufer ein Angebot beantragt. |
| [!UICONTROL Submitted By] | Der Vor- und Nachname des Firmenkäufers, der eine Angebotsanforderung einreicht. |
| [!UICONTROL Last Updated] | Datum und Uhrzeit der letzten Mitteilung zwischen Käufer und Verkäufer bezüglich des Preises. |
| [!UICONTROL Sales Rep] | Vor- und Nachname des Vertreters, der das Konto des Käufers verwaltet. |
| [!UICONTROL Quote Total (Base)] | Der Gesamtpreis der zu kaufenden Produkte basierend auf dem ursprünglichen Angebot. Der Gesamtbetrag wird in der Basiswährung der Website und in der Währung der Storefront angezeigt. |
| [!UICONTROL Quote Total (Negotiated)] | Der Gesamtpreis der zu kaufenden Produkte basierend auf dem ausgehandelten Angebot. Dieser Gesamtwert wird automatisch vom System berechnet und umfasst alle vom Verkäufer angewendeten Rabatte auf Zeileneintrag- oder Anführungsebene. Der Gesamtbetrag wird in der Basiswährung der Website und in der Währung der Storefront angezeigt. |
| [!UICONTROL Status] | Gibt den aktuellen Status einer Anführungsanforderung an. Der Status eines Angebots kann nur durch Handlung des Käufers oder Verkäufers geändert werden. Siehe auch die Statuseinstellungen des [Käuferkontos](account-dashboard-my-quotes.md).<ul><li>**[!UICONTROL New]** - Der Käufer hat einen Antrag auf ein Angebot gestellt, wurde aber vom Verkäufer nicht eingesehen. Der Antrag kann vom Käufer bis zur Eröffnung durch den Verkäufer aktualisiert werden.</li><li>**[!UICONTROL Draft]** - Der Verkäufer erstellt einen Kostenvoranschlag für einen Käufer. Das Angebot ist für den Käufer erst sichtbar, wenn der Verkäufer die Angebotsdetails (Artikel, Menge, Rabatt usw.) hinzufügt und dem Käufer das Angebot übermittelt.</li> <li>**[!UICONTROL Open]** - Der Verkäufer hat die Anfrage geöffnet und ist dabei, sie zu überprüfen und eine Antwort vorzubereiten. </li><li>**[!UICONTROL Submitted]** - Der Verkäufer hat dem Käufer eine Antwort geschickt. Der Zitat-Datensatz kann während des Verhandlungsprozesses nicht bearbeitet werden.</li><li>**[!UICONTROL Client Reviewed]** - Der Käufer hat die Antwort des Verkäufers angesehen und bereitet derzeit eine Antwort vor.</li><li>**[!UICONTROL Updated]** - Der Käufer hat eine Antwort übermittelt, aber sie wurde vom Verkäufer nicht eingesehen.</li><li>**[!UICONTROL Ordered]** - Der Käufer hat den Auftrag auf der Grundlage des ausgehandelten Preises eingereicht.</li><li>**[!UICONTROL Closed]** - Der Käufer hat die Preisanfrage abgebrochen.</li><li>**[!UICONTROL Declined]** - Der Verkäufer lehnte die Anforderung eines Angebots ab. Alle benutzerdefinierten Preise werden aus dem Anführungszeichen entfernt und der Datensatz wird von weiteren Bearbeitungen gesperrt.</li><li>**[!UICONTROL Expired]** - Der Käufer hat nicht innerhalb der festgelegten Frist auf die Antwort des Verkäufers geantwortet und das Angebot ist nicht mehr gültig.</li></ul> |
| [!UICONTROL Actions] | **[!UICONTROL View]** - Öffnet die Angebotsanforderung und führt einen Datensatz über die Verhandlungen zwischen Käufer und Verkäufer. |

{style="table-layout:auto"}

## Schaltflächenleiste

| Schaltfläche | Beschreibung |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Send] | Übermittelt das aktualisierte Angebot als Antwort auf die Anfrage des Käufers. Diese Schaltfläche ist deaktiviert, wenn der Verkäufer auf eine Antwort des Käufers wartet. |
| [!UICONTROL Back] | Gibt zur Seite _Anführungszeichen_ zurück, ohne Änderungen zu speichern. |
| [!UICONTROL Create Copy] | [!BADGE 1.5.0-beta-Funktionen]{type=Informative url=&quot;/help/b2b/release-notes.md&quot; tooltip=&quot;Nur für Beta-Programmteilnehmer verfügbar&quot;} Erstellen Sie ein neues Zitat aus dem aktuellen Zitat, indem Sie es kopieren und umbenennen. Wenn das neue Anführungszeichen geöffnet wird, lautet der Standardname `<original quote name> (copy)`. Ändern Sie den Namen, indem Sie den Wert im Feld [!UICONTROL Name] bearbeiten und das Anführungszeichen als Entwurf speichern. |
| [!UICONTROL Print] | Sendet das Anführungszeichen an einen Drucker oder speichert es als PDF-Datei. |
| [!UICONTROL Create a copy] | Erstellt eine Kopie des Anführungszeichens mit dem Namen `<original quote name> (copy)` und öffnet es. Benennen Sie das neue Angebot nach Bedarf um und aktualisieren Sie es, bevor Sie es als Entwurf speichern oder an den Käufer senden. |
| [!UICONTROL Save as Draft] | Speichert alle Änderungen an dem Angebot, sendet es jedoch nicht an den Käufer zurück. |
| [!UICONTROL Decline] | Der Vorschlag, die Preise zu verhandeln, wird entweder im Rahmen der ersten Untersuchung oder während der laufenden Verhandlungen abgelehnt. Wenn ein Angebot abgelehnt wird, sollte der Verkäufer einen Kommentar hinzufügen, um die Entscheidung zu erläutern. Wenn ein Angebot abgelehnt wird, werden alle ausgehandelten Preise auf die ursprünglichen Werte zurückgesetzt. Diese Schaltfläche ist deaktiviert, während der Verkäufer auf eine Antwort vom Käufer wartet. |

{style="table-layout:auto"}

## Beispielangebot

Die folgende Abbildung zeigt ein Beispiel der Zitat-Detailansicht im Admin mit einigen konfigurierten Einstellungen.

![Beispiel-Anführungszeichen](./assets/quote-full.png){width="700" zoomable="yes"}


>[!NOTE]
>
>[!BADGE 1.5.0-Beta-Funktionen]{type=Informative url="/help/b2b/release-notes.md" tooltip="Nur für Beta-Programmteilnehmer verfügbar"}
