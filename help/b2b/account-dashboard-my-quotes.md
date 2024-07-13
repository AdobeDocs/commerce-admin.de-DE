---
title: '[!UICONTROL My Quotes]'
description: Erfahren Sie mehr über das Kundenerlebnis bei Angeboten, die in ihrem Konto-Dashboard verfügbar sind.
exl-id: 137f0a99-8f24-4838-b54b-b0ef2c39a32a
feature: B2B, Companies, Quotes
source-git-commit: 27b0c43f72faa2c2e8717fd5929f36d12f9e1b08
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---


# [!UICONTROL My Quotes]

Wenn Anführungszeichen aktiviert sind, werden im Abschnitt &quot;_[!UICONTROL My Quotes]_&quot;des Dashboards für Kundenkonten alle vom Kunden gesendeten Anführungszeichen aufgelistet. Je nach Berechtigung können nur Käufer, die im Namen eines Unternehmens Einkäufe tätigen, Anfragen zur Aushandlung des Kaufpreises einreichen.

![Meine Anführungszeichen](./assets/account-dashboard-my-quotes.png){width="700" zoomable="yes"}

Der Käufer startet den Prozess durch [Einreichen einer Anfrage](quote-request.md) für ein Angebot aus dem Warenkorb. E-Mail wird während des [Verhandlungsprozesses](quote-price-negotiation.md) zwischen Käufer und Verkäufer ausgetauscht. Für den Käufer ist die Seite &quot;[!UICONTROL My Quotes]&quot; die zentrale Stelle für die Kommunikation zwischen Käufer und Verkäufer während des Verhandlungsprozesses. Ein Käufer, der den vom Verkäufer angebotenen ausgehandelten Preis akzeptiert, kann direkt von der Angebotsseite zur Kasse gehen. Dem ausgehandelten Angebot können keine zusätzlichen Rabatte hinzugefügt werden.

Ein Käufer kann bei der Aushandlung eines Angebots die folgenden Schritte ausführen:

* Überprüfen der Artikelpreise und -aktualisierungen
* Verfolgen Sie den Verhandlungsprozess über die Abschnitte [!UICONTROL Comments] und [!UICONTROL History].
* Anführungszeichen ändern, um Elemente zu entfernen
* Kommunizieren und verhandeln Sie mit dem Verkäufer, indem Sie Notizen auf der Posten- und Anführungsebene hinzufügen.
* Angebot an Verkäufer zur Überprüfung senden
* Konvertieren des Anführungszeichens in eine Bestellung, wenn die Bedingungen akzeptabel sind
* Anführungszeichen schließen
* Anführungszeichen löschen
* [!BADGE 1.5.0-Beta-Funktionen]{type=Informative url="/help/b2b/release-notes.md" tooltip="Nur für Beta-Programmteilnehmer verfügbar"}

Das folgende Beispiel zeigt ein Angebot, das vom Käufer aktualisiert und zur Überprüfung an den Verkäufer zurückgesendet wurde.


![Ansicht des Käufers von Angebot](./assets/account-dashboard-my-quote-detail.png){width="700" zoomable="yes"}

Anführungszeichen mit dem Status `Updated` werden gesperrt, bis der Verkäufer das Anführungszeichen zurückgibt.

## Anführungszeichen anzeigen

Mit den erforderlichen [Berechtigungen für ihre Rolle](account-company-roles-permissions.md) können Kunden, die mit einem Unternehmenskonto verknüpft sind, Anführungszeichen sehen, die von [untergeordneten Benutzern angefordert werden](account-company-structure.md). Unternehmensadministratoren können alle Anführungszeichen für das Unternehmenskonto anzeigen.

1. Der Kunde meldet sich bei seinem Konto in der Storefront an.

1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL My Quotes]** .

1. Um alle von ihnen erstellten Anführungszeichen anzuzeigen, klicken Sie auf den Link **[!UICONTROL Show My Quotes]** (nur für den Unternehmensadministrator oder das Konto mit untergeordneten Benutzern angezeigt).

1. Um alle Anführungszeichen aller Unternehmensbenutzer anzuzeigen, klicken Sie auf **[!UICONTROL Show All Quotes]**.

## Ansehen eines Angebots

1. Der Kunde meldet sich bei seinem Konto an.

1. Wählen Sie im linken Bereich **[!UICONTROL My Quotes]** aus.

1. Sucht das Anführungszeichen in der Liste und klickt in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL View]**.

## Anführungszeichen drucken

1. In dem offenen Angebot rechts neben dem Abschnitt _[!UICONTROL Items Quoted]_klickt der Kunde auf **[!UICONTROL Print]**.

1. Überprüft die **[!UICONTROL Destination]** entweder als Drucker oder PDF.

1. Klicks **[!UICONTROL Print]**.

## Anführungsanforderung abbrechen

1. Klicken Sie im offenen Anführungszeichen direkt über dem Abschnitt &quot;Artikel zitiert&quot;auf **[!UICONTROL Close quote]**.

   Die Anfrage wird abgebrochen und der Anführungszeichenstatus wird in `Closed` geändert. Das geschlossene Anführungszeichen bleibt in Ihrer Anführungszeichenliste und wird weiterhin im Raster _[!UICONTROL Quotes]_des Administrators aufgeführt.

1. Klicken Sie auf **[!UICONTROL Delete]**, um das stornierte Anführungszeichen aus der Anführungszeichenliste zu entfernen.

1. Wenn Sie zur Bestätigung aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.

   Das geschlossene Anführungszeichen wird aus der Anführungszeichenliste entfernt. Er bleibt jedoch im Raster _[!UICONTROL Quotes]_im Admin mit dem Status `Closed` aufgeführt.

## Anführungsaktionen

| Aktion | Beschreibung |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Umbenennen | [!BADGE 1.5.0-beta-Funktionen]{type=Informative url=&quot;/help/b2b/release-notes.md&quot; tooltip=&quot;Nur für Beta-Programmteilnehmer verfügbar&quot;} Ändern Sie den Namen des Zitats |
| Erstellen einer Kopie | [!BADGE 1.5.0-beta-Funktionen]{type=Informative url=&quot;/help/b2b/release-notes.md&quot; tooltip=&quot;Nur für Beta-Programmteilnehmer verfügbar&quot;} Ein Käufer kann ein neues Zitat aus dem aktuellen Zitat erstellen, indem er es kopiert und umbenennt. |
| Anführungszeichen | Ein Käufer schließt ein Angebot und kann es nicht erneut öffnen. Bei Bedarf kann der Käufer sie mithilfe der Aktion [!UICONTROL Create Copy] neu erstellen. Diese Option ist nicht verfügbar, wenn der Anführungszeichenstatus `Draft` ist. |
| Anführungszeichen löschen | Wenn ein Käufer ein Angebot löscht, wird es aus dem System entfernt und ist nicht mehr verfügbar. |
| Drucken | Öffnet ein Druckformular zum Speichern des Anführungszeichens als PDF, Datei oder Drucken auf einem konfigurierten Drucker. |

## Spaltenbeschreibungen

| Spalte | Beschreibung |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Quote Name] | Der Name, der dem Angebot vom Käufer zugewiesen wurde. |
| [!UICONTROL Created] | Das Datum, an dem die Angebotsanforderung zum ersten Mal eingereicht wurde. |
| [!UICONTROL Created By] | Vor- und Nachname des Käufers, der die Angebotsanforderung eingereicht hat. |
| [!UICONTROL Status] | Gibt den Status des Zitats an. Der Status eines Angebots kann nur durch Handlung des Käufers oder Verkäufers geändert werden. <br/>**[!UICONTROL Submitted]**- Die Angebotsanforderung des Käufers wurde vom Verkäufer noch nicht eröffnet. In diesem Zustand kann der Käufer die Angebotsanforderung noch ändern. Verfügbare Aktionen: `View` / `Close` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Pending]** - Der Verkäufer hat die Anfrage geöffnet und ist dabei, sie zu überprüfen und eine Antwort vorzubereiten. Verfügbare Aktionen: `View` / `Close` <br/>**[!UICONTROL Updated]**- Der Verkäufer hat eine Antwort an den Käufer gesendet und die Schaltfläche _[!UICONTROL Proceed to Checkout]_ist aktiviert. In diesem Zustand kann der Käufer das Angebot weiterhin ändern. Verfügbare Aktionen: `View` / `Send for Review` / `Proceed to Checkout` / `Delete Quote` / `Close` / `Edit Quantity` / `Delete SKU` / `Add comments` / `Edit Shipping Address`<br/>**[!UICONTROL Open]**- Der Käufer aktualisiert das Angebot noch, und die Schaltfläche_[!UICONTROL Proceed to Checkout]_ ist deaktiviert. Verfügbare Aktionen: `View` / `Send for Review` / `Delete Quote` / `Edit quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` <br/>**[!UICONTROL Ordered]**- Der Käufer hat eine Bestellung basierend auf dem ausgehandelten Angebot eingereicht. Das Anführungszeichen ist gesperrt und kann nicht bearbeitet werden. Verfügbare Aktion: Anzeigen<br/>**[!UICONTROL Closed]** - Der Käufer hat die Verhandlung beendet und das Angebot abgebrochen. Das Angebot ist gesperrt und kann weder vom Käufer noch vom Verkäufer bearbeitet werden. Verfügbare Aktionen: `View` / `Delete` <br/>**[!UICONTROL Declined]**- Der Verkäufer hat die Anforderung eines Angebots abgelehnt oder während des Verhandlungsprozesses eine Änderung vorgeschlagen. Ein Angebot kann in jeder Workflow-Phase abgelehnt werden. Alle benutzerdefinierten Preise werden aus dem Angebot entfernt. Der Käufer kann das Angebot weiter bearbeiten und erneut einreichen oder den Kauf mit den üblichen Katalogpreisen tätigen. Verfügbare Aktionen: `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Expired]** - Die Lebensdauer des Zitats ist abgelaufen. Alle vorgeschlagenen Preise werden zurückgesetzt. Der Käufer kann entweder den Kauf auf der Grundlage von Standardkatalogpreisen abschließen oder eine weitere Verhandlungsrunde einleiten. Verfügbare Aktionen: `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` |

{style="table-layout:auto"}
