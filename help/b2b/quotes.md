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

Angebote können von einem autorisierten Firmenkäufer oder einem Vertriebsmitarbeiter initiiert werden. Nach Erstellung des Angebots beginnt der Verhandlungsprozess, sobald der Käufer oder Verkäufer das Angebot zur Überprüfung einreicht. Die _Anführungszeichen_ Raster, das jedes erhaltene Angebot auflistet und einen Verlauf der Kommunikation zwischen Käufer und Verkäufer führt. Verwenden Sie den Standard [Arbeitsablaufkontrollen](../getting-started/admin-workspace.md) um die Liste zu filtern, ändern Sie das Spaltenlayout, speichern Sie Ansichten und exportieren Sie Daten.

- In der Storefront übermitteln Käufer das Angebot als [Verhandlungsantrag](quote-price-negotiation.md) den Preis aus dem Warenkorb. Bei der Erstellung des Angebots kann ein Käufer das Angebot als Entwurf speichern oder direkt an den Verkäufer übermitteln.

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

**Schritt 1: Erstellung von Anführungszeichen**

- **Anfrageangebot des Käufers** - Der Käufer [ein Anführungszeichen anfordern](quote-request.md) aus dem Warenkorb. Die Anforderung wird im _Meine Angebote_ Liste im Konto-Dashboard des Käufers und E-Mail-Benachrichtigung wird an den Vertriebsmitarbeiter gesendet, der dem Unternehmenskonto zugewiesen ist. Im Admin wird die Anforderung im _Anführungszeichen_ Raster mit dem Status `New`. Ein Angebot kann vom Käufer bis zur Eröffnung durch den Verkäufer geändert werden.

  ![Anführungszeichen](./assets/quote-request-from-shopping-cart.png){width="700" zoomable="yes"}


- **Vertriebsmitarbeiter** - Ein Vertriebsmitarbeiter kann [Erstellen eines Zitats](sales-rep-initiates-quote.md) vom Administrator im Namen eines bestimmten Firmenkäufers. Der Kundenbetreuer muss das Angebot aktualisieren, um dem Käufer Produkte und andere Informationen wie Rabatte und Hinweise hinzuzufügen. Die Verkaufsdarstellung kann das Angebot als `draft` oder senden Sie es an den Käufer, um die Verhandlungen zu beginnen. Im Entwurfszustand ist das Angebot nur für den Verkäufer sichtbar. Sobald das Anführungszeichen gesendet wurde, lautet der Status `Submitted`. Er kann vom Verkäufer erst geändert werden, wenn der Käufer ihn zurücksendet.

  ![Verkäufer, die ein Käuferangebot aus dem Quotes-Raster im Admin initiieren](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}


**Schritt 2: Anführungszeichenprüfung und Verhandlungen**

**Anforderung von Kundenansichten und Antwort** - Im Admin sieht der Verkäufer die Anfrage nach einem Angebot. Der Status des Anführungszeichens ändert sich in `Pending`und der Käufer kann keine Änderungen vornehmen. Die [Antwort des Verkäufers](quote-price-negotiation.md) durch Angebot von ermäßigten Preisen für die Produkte in der Preisliste, gibt einen Kommentar ein und sendet das Angebot an den Käufer zurück. Der Käufer und der Vertriebsmitarbeiter werden per E-Mail darüber informiert, dass der Verkäufer geantwortet hat.

**Anfrageangebote des Verkäufers und Antworten** - Der Käufer klickt auf den Link in der E-Mail-Benachrichtigung, um das Angebot zu öffnen, oder öffnet das Angebot aus dem _Meine Angebote_ Seite des Konto-Dashboards. Der Käufer kann dem Verkäufer Notizen auf der Posten- oder Angebotsebene hinterlassen und Artikel entfernen.

Der Käufer und der Verkäufer können den Verhandlungsprozess fortsetzen, bis eine Vereinbarung getroffen wird, oder der Verkäufer lehnt das Angebot ab. Wenn der Käufer Änderungen am Angebot vornimmt, d. h. Produkte hinzufügt, entfernt oder die Produktmengen ändert, muss das Angebot zur Überprüfung an den Verkäufer zurückgegeben werden.

**4. Schritt: Annahme des Angebots durch den Käufer** - Der Käufer nimmt den vorgeschlagenen Preis an und erstattet weiter. Dem ausgehandelten Angebot können keine zusätzlichen Rabatte hinzugefügt werden.

## B2B-Rollenressourcen für Store-Anführungszeichen

Die Konfigurationsoptionen für Anführungszeichen werden mithilfe des [Rollenressourcen](../systems/permissions-user-roles.md#role-resources). Diese Rollenressourcen müssen für die Administratorrolle festgelegt sein, die dem Store-Administrator zugewiesen ist.

Um Zugriff auf Anführungsfunktionen im Admin zu gewähren, gehen Sie zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, wählen Sie die Rolle aus und navigieren Sie zu [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] im_ Rollenressourcen _Baum.

## Anwenden einer Aktion

In der Admin-Konsole können B2B-Administratoren und -Verkäufer Anführungszeichen aus dem Anführungszeichen-Raster mithilfe der [!UICONTROL Actions] Menü.

![Anführungszeichen](./assets/quotes-grid.png){width="700" zoomable="yes"}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > **[!UICONTROL Quotes]**.

1. Aktivieren Sie in der ersten Spalte des Rasters das Kontrollkästchen für jeden Datensatz, auf den Sie die Aktion anwenden möchten.

1. Im **[!UICONTROL Actions]** die anzuwendende Aktion auswählen.

### Ansehen eines Angebots

1. Im **[!UICONTROL Actions]** Spalte für einen Datensatz, klicken Sie auf **[!UICONTROL View]**.

1. Befolgen Sie die Anweisungen und beginnen Sie mit dem [Preisverhandlungen](quote-price-negotiation.md) -Prozess.

### Anführungsaktivität

Zeigen Sie den Verhandlungs-Timeline, die Kommunikation und andere Anführungsaktivitäten über die [!UICONTROL Comments] und [!UICONTROL History Log]—Informationen umfassen Statusänderungen, Aktualisierungen von Kunden- und Versandinformationen, Artikel- und Preisaktualisierungen sowie andere wichtige Informationen.

1. Öffnen Sie ein Zitat.

1. Anzeigen von Kommentaren und Verlaufsverlauf zu Anführungszeichen durch Scrollen zu **[!UICONTROL Negotiation]** und wählen Sie **[!UICONTROL Comments]** und **[!UICONTROL History Log]**.

   ![Verlauf anzeigen](./assets/quote-view-history.png){width="400"}

1. Der Verlauf wird auch auf Zeileneintrag-Ebene verfolgt.

   ![Anzeigen des Zeilenelementverlaufs](./assets/quote-view-line-item-history.png){width="400"}


### Anforderung eines Anführungszeichens ablehnen

Nur Angebotsanfragen mit `Open` -Status abgelehnt werden.

1. Wählen Sie jede offene Anführungsanforderung aus, die Sie ablehnen möchten.

1. Legen Sie die _[!UICONTROL Actions]_Kontrolle an `Declined`.

1. Geben Sie bei Aufforderung den Grund für die Ablehnung des Angebots ein und klicken Sie auf **[!UICONTROL Confirm]**.

   ![Zitat ablehnen?](./assets/quote-decline-confirm.png){width="400"}


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
| [!UICONTROL Status] | Gibt den aktuellen Status einer Anführungsanforderung an. Der Status eines Angebots kann nur durch Handlung des Käufers oder Verkäufers geändert werden. Siehe auch die Statuseinstellungen unter [Konto des Käufers](account-dashboard-my-quotes.md).<ul><li>**[!UICONTROL New]** - Der Käufer hat einen Antrag auf ein Angebot gestellt, wurde aber vom Verkäufer nicht eingesehen. Der Antrag kann vom Käufer bis zur Eröffnung durch den Verkäufer aktualisiert werden.</li><li>**[!UICONTROL Draft]** - Der Verkäufer erstellt einen Kostenvoranschlag für einen Käufer. Das Angebot ist für den Käufer erst sichtbar, wenn der Verkäufer die Angebotsdetails (Artikel, Menge, Rabatt usw.) hinzufügt und dem Käufer das Angebot übermittelt.</li> <li>**[!UICONTROL Open]** - Der Verkäufer hat die Anfrage geöffnet und ist dabei, sie zu überprüfen und eine Antwort vorzubereiten. </li><li>**[!UICONTROL Submitted]** - Der Verkäufer hat dem Käufer eine Antwort geschickt. Der Zitat-Datensatz kann während des Verhandlungsprozesses nicht bearbeitet werden.</li><li>**[!UICONTROL Client Reviewed]** - Der Käufer hat die Antwort des Verkäufers angesehen und bereitet derzeit eine Antwort vor.</li><li>**[!UICONTROL Updated]** - Der Käufer übermittelte eine Antwort, die jedoch vom Verkäufer nicht eingesehen wurde.</li><li>**[!UICONTROL Ordered]** - Der Käufer hat den Auftrag auf der Grundlage des ausgehandelten Preises eingereicht.</li><li>**[!UICONTROL Closed]** - Der Käufer hat die Preisanfrage storniert.</li><li>**[!UICONTROL Declined]** - Der Verkäufer lehnte die Angebotsanforderung ab. Alle benutzerdefinierten Preise werden aus dem Anführungszeichen entfernt und der Datensatz wird von weiteren Bearbeitungen gesperrt.</li><li>**[!UICONTROL Expired]** - Der Käufer hat nicht innerhalb der vorgesehenen Frist auf die Antwort des Verkäufers geantwortet, und das Angebot ist nicht mehr gültig.</li></ul> |
| [!UICONTROL Actions] | **[!UICONTROL View]** - Öffnet die Angebotsanfrage und führt einen Bericht über die Verhandlungen zwischen Käufer und Verkäufer. |

{style="table-layout:auto"}

## Schaltflächenleiste

| Schaltfläche | Beschreibung |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Send] | Übermittelt das aktualisierte Angebot als Antwort auf die Anfrage des Käufers. Diese Schaltfläche ist deaktiviert, wenn der Verkäufer auf eine Antwort des Käufers wartet. |
| [!UICONTROL Back] | Gibt Folgendes zurück _Anführungszeichen_ Seite ohne Speichern von Änderungen. |
| [!UICONTROL Create Copy] | [!BADGE 1.5.0-Beta-Funktionen]{type=Informative url=&quot;/help/b2b/release-notes.md&quot; tooltip=&quot;Nur für Beta-Programmteilnehmer verfügbar&quot;} Erstellen Sie ein neues Zitat aus dem aktuellen Zitat, indem Sie es kopieren und umbenennen. Wenn das neue Anführungszeichen geöffnet wird, lautet der Standardname `<original quote name> (copy)`. Ändern Sie den Namen, indem Sie den Wert im [!UICONTROL Name] und das Anführungszeichen als Entwurf speichern. |
| [!UICONTROL Print] | Sendet das Anführungszeichen an einen Drucker oder speichert es als PDF-Datei. |
| [!UICONTROL Create a copy] | Erstellt eine Kopie des Anführungszeichens mit dem Namen `<original quote name> (copy)` und öffnet es. Benennen Sie das neue Angebot nach Bedarf um und aktualisieren Sie es, bevor Sie es als Entwurf speichern oder an den Käufer senden. |
| [!UICONTROL Save as Draft] | Speichert alle Änderungen an dem Angebot, sendet es jedoch nicht an den Käufer zurück. |
| [!UICONTROL Decline] | Der Vorschlag, die Preise zu verhandeln, wird entweder im Rahmen der ersten Untersuchung oder während der laufenden Verhandlungen abgelehnt. Wenn ein Angebot abgelehnt wird, sollte der Verkäufer einen Kommentar hinzufügen, um die Entscheidung zu erläutern. Wenn ein Angebot abgelehnt wird, werden alle ausgehandelten Preise auf die ursprünglichen Werte zurückgesetzt. Diese Schaltfläche ist deaktiviert, während der Verkäufer auf eine Antwort vom Käufer wartet. |

{style="table-layout:auto"}

## Beispielangebot

Die folgende Abbildung zeigt ein Beispiel der Zitat-Detailansicht im Admin mit einigen konfigurierten Einstellungen.

![Beispielangebot](./assets/quote-full.png){width="700" zoomable="yes"}


>[!NOTE]
>
>[!BADGE 1.5.0-Beta-Funktionen]{type=Informative url="/help/b2b/release-notes.md" tooltip="Nur für Beta-Programmteilnehmer verfügbar"}
