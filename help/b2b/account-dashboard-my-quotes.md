---
title: '[!UICONTROL My Quotes]'
description: Erfahren Sie mehr über das Kundenerlebnis bei Angeboten, die in ihrem Konto-Dashboard verfügbar sind.
exl-id: 137f0a99-8f24-4838-b54b-b0ef2c39a32a
feature: B2B, Companies, Quotes
source-git-commit: 27b0c43f72faa2c2e8717fd5929f36d12f9e1b08
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---


# [!UICONTROL My Quotes]

Wenn Anführungszeichen aktiviert sind, wird die _[!UICONTROL My Quotes]_im Dashboard des Kundenkontos werden alle vom Kunden eingereichten Angebote aufgelistet. Je nach Berechtigung können nur Käufer, die im Namen eines Unternehmens Einkäufe tätigen, Anfragen zur Aushandlung des Kaufpreises einreichen.

![Meine Angebote](./assets/account-dashboard-my-quotes.png){width="700" zoomable="yes"}

Der Käufer beginnt mit dem Prozess durch [Senden einer Anfrage](quote-request.md) für ein Angebot aus dem Warenkorb. E-Mail wird zwischen Käufer und Verkäufer während der [Verhandlungsprozess](quote-price-negotiation.md). Für den Käufer [!UICONTROL My Quotes] page ist die zentrale Stelle für die Kommunikation zwischen Käufer und Verkäufer während des Verhandlungsprozesses. Ein Käufer, der den vom Verkäufer angebotenen ausgehandelten Preis akzeptiert, kann direkt von der Angebotsseite zur Kasse gehen. Dem ausgehandelten Angebot können keine zusätzlichen Rabatte hinzugefügt werden.

Ein Käufer kann bei der Aushandlung eines Angebots die folgenden Schritte ausführen:

* Überprüfen der Artikelpreise und -aktualisierungen
* Verfolgen des Verhandlungsprozesses von [!UICONTROL Comments] und [!UICONTROL History] Abschnitte
* Anführungszeichen ändern, um Elemente zu entfernen
* Kommunizieren und verhandeln Sie mit dem Verkäufer, indem Sie Notizen auf der Posten- und Anführungsebene hinzufügen.
* Angebot an Verkäufer zur Überprüfung senden
* Konvertieren des Anführungszeichens in eine Bestellung, wenn die Bedingungen akzeptabel sind
* Anführungszeichen schließen
* Anführungszeichen löschen
* [!BADGE 1.5.0-Beta-Funktionen]{type=Informative url="/help/b2b/release-notes.md" tooltip="Nur für Beta-Programmteilnehmer verfügbar"}

Das folgende Beispiel zeigt ein Angebot, das vom Käufer aktualisiert und zur Überprüfung an den Verkäufer zurückgesendet wurde.


![Käuferansicht des Angebots](./assets/account-dashboard-my-quote-detail.png){width="700" zoomable="yes"}

Anführungszeichen mit der `Updated` -Status gesperrt werden, bis der Verkäufer das Angebot zurückgibt.

## Anführungszeichen anzeigen

Mit den erforderlichen [Berechtigungen für ihre Rolle](account-company-roles-permissions.md), können Kunden, die mit einem Unternehmenskonto verknüpft sind, die von angeforderten Angebote sehen. [untergeordnete Benutzer](account-company-structure.md). Unternehmensadministratoren können alle Anführungszeichen für das Unternehmenskonto anzeigen.

1. Der Kunde meldet sich bei seinem Konto in der Storefront an.

1. Klicks **[!UICONTROL My Quotes]** in der linken Navigation.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Show My Quotes]** -Link (nur für den Unternehmensadministrator oder das Konto mit untergeordneten Benutzern angezeigt).

1. Um alle Anführungszeichen aller Unternehmensbenutzer anzuzeigen, klicken Sie auf **[!UICONTROL Show All Quotes]**.

## Ansehen eines Angebots

1. Der Kunde meldet sich bei seinem Konto an.

1. Wählen Sie im linken Bereich **[!UICONTROL My Quotes]**.

1. Findet das Anführungszeichen in der Liste und klickt auf **[!UICONTROL View]** im _[!UICONTROL Action]_Spalte.

## Anführungszeichen drucken

1. Im offenen Anführungszeichen rechts neben dem _[!UICONTROL Items Quoted]_-Abschnitt, auf den der Kunde klickt **[!UICONTROL Print]**.

1. Überprüft die **[!UICONTROL Destination]** als Drucker oder PDF.

1. Klicks **[!UICONTROL Print]**.

## Anführungsanforderung abbrechen

1. Klicken Sie im offenen Anführungszeichen direkt über dem Abschnitt &quot;Artikel zitiert&quot;auf **[!UICONTROL Close quote]**.

   Die Anfrage wird abgebrochen und der Anführungszeichenstatus ändert sich in `Closed`. Das geschlossene Anführungszeichen bleibt in Ihrer Anführungszeichenliste und wird weiterhin im _[!UICONTROL Quotes]_aus dem Admin.

1. Klicken Sie auf , um das stornierte Anführungszeichen aus der Anführungszeichenliste zu entfernen **[!UICONTROL Delete]**.

1. Wenn Sie zur Bestätigung aufgefordert werden, klickt **[!UICONTROL OK]**.

   Das geschlossene Anführungszeichen wird aus der Anführungszeichenliste entfernt. Sie wird jedoch weiterhin im _[!UICONTROL Quotes]_im Admin-Raster mit dem `Closed` -Status.

## Anführungsaktionen

| Aktion | Beschreibung |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Umbenennen | [!BADGE 1.5.0-Beta-Funktionen]{type=Informative url="/help/b2b/release-notes.md" tooltip="Nur für Beta-Programmteilnehmer verfügbar"} |
| Erstellen einer Kopie | [!BADGE 1.5.0-Beta-Funktionen]{type=Informative url="/help/b2b/release-notes.md" tooltip="Nur für Beta-Programmteilnehmer verfügbar"} |
| Anführungszeichen | Ein Käufer schließt ein Angebot und kann es nicht erneut öffnen. Bei Bedarf kann der Käufer sie mithilfe des [!UICONTROL Create Copy] Aktion. Diese Option ist nicht verfügbar, wenn der Anführungszeichenstatus `Draft`. |
| Anführungszeichen löschen | Wenn ein Käufer ein Angebot löscht, wird es aus dem System entfernt und ist nicht mehr verfügbar. |
| Drucken | Öffnet ein Druckformular zum Speichern des Anführungszeichens als PDF, Datei oder Drucken auf einem konfigurierten Drucker. |

## Spaltenbeschreibungen

| Spalte | Beschreibung |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Quote Name] | Der Name, der dem Angebot vom Käufer zugewiesen wurde. |
| [!UICONTROL Created] | Das Datum, an dem die Angebotsanforderung zum ersten Mal eingereicht wurde. |
| [!UICONTROL Created By] | Vor- und Nachname des Käufers, der die Angebotsanforderung eingereicht hat. |
| [!UICONTROL Status] | Gibt den Status des Zitats an. Der Status eines Angebots kann nur durch Handlung des Käufers oder Verkäufers geändert werden. <br/>**[!UICONTROL Submitted]**- Die Angebotsanfrage des Käufers wurde vom Verkäufer noch nicht eröffnet. In diesem Zustand kann der Käufer die Angebotsanforderung noch ändern. Verfügbare Aktionen: `View` / `Close` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Pending]** - Der Verkäufer hat die Anfrage eröffnet und ist dabei, sie zu überprüfen und eine Antwort vorzubereiten. Verfügbare Aktionen: `View` / `Close` <br/>**[!UICONTROL Updated]**- der Verkäufer dem Käufer eine Antwort übermittelt hat und _[!UICONTROL Proceed to Checkout]_-Schaltfläche aktiviert ist. In diesem Zustand kann der Käufer das Angebot weiterhin ändern. Verfügbare Aktionen: `View` / `Send for Review` / `Proceed to Checkout` / `Delete Quote` / `Close` / `Edit Quantity` / `Delete SKU` / `Add comments` / `Edit Shipping Address`<br/>**[!UICONTROL Open]**- Der Käufer aktualisiert das Angebot noch, und_[!UICONTROL Proceed to Checkout]_ -Schaltfläche deaktiviert ist. Verfügbare Aktionen: `View` / `Send for Review` / `Delete Quote` / `Edit quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` <br/>**[!UICONTROL Ordered]**- Der Käufer hat einen Auftrag auf der Grundlage des ausgehandelten Preises eingereicht. Das Anführungszeichen ist gesperrt und kann nicht bearbeitet werden. Verfügbare Aktion: Ansicht<br/>**[!UICONTROL Closed]** - Der Käufer hat die Verhandlung beendet und storniert das Angebot. Das Angebot ist gesperrt und kann weder vom Käufer noch vom Verkäufer bearbeitet werden. Verfügbare Aktionen: `View` / `Delete` <br/>**[!UICONTROL Declined]**- Der Verkäufer hat den Antrag auf ein Angebot abgelehnt oder während des Verhandlungsprozesses eine Änderung vorgeschlagen. Ein Angebot kann in jeder Workflow-Phase abgelehnt werden. Alle benutzerdefinierten Preise werden aus dem Angebot entfernt. Der Käufer kann das Angebot weiter bearbeiten und erneut einreichen oder den Kauf mit den üblichen Katalogpreisen tätigen. Verfügbare Aktionen: `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Expired]** - Die Lebensdauer des Zitats ist abgelaufen. Alle vorgeschlagenen Preise werden zurückgesetzt. Der Käufer kann entweder den Kauf auf der Grundlage von Standardkatalogpreisen abschließen oder eine weitere Verhandlungsrunde einleiten. Verfügbare Aktionen: `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` |

{style="table-layout:auto"}
