---
title: Verwalten von Newsletter-Abonnenten
description: Hier erfahren Sie, wie Sie Ihre Newsletter-Abonnenten mithilfe einer einfachen Liste aktiver Abonnements verwalten.
exl-id: c7e8e642-e3fd-4979-9ea3-2d96839730b2
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Verwalten von Newsletter-Abonnenten

Als Best Practice sollten Sie Ihre Abonnementliste regelmäßig verwalten und alle Abmeldeanfragen verarbeiten. In einigen Rechtsordnungen ist es gesetzlich vorgeschrieben, dass Abmeldeanfragen innerhalb eines bestimmten Zeitraums bearbeitet werden.

Sie können Ihre Abonnenten einfach über eine einfache Liste aktiver Abonnements verwalten. Wenn ein Kunde eine Abmeldeanforderung sendet, können Sie einfach eine _Abmelden_ Aktion auf ein oder mehrere ausgewählte Abonnements.

Bei Einzelsite-Setups mit mehreren Store-Ansichten kann ein Kundenkontoabonnement einer bestimmten Store-Ansicht zugeordnet werden.

In Multi-Store- und Multi-Site-Setups mit einer globalen [Kundenkontobereich](../customers/customer-account-scope.md), kann ein Kundenkonto für Newsletter für mehrere Sites/Geschäfte abonniert werden. In diesem Fall können Sie das Kundenkonto bearbeiten, um eine Gruppe von Abonnements zu verwalten oder ein Abonnement für eine bestimmte Site/einen bestimmten Store abzubrechen, um eine Anfrage zu berücksichtigen.

Wenn Sie Newsletter mit einem Drittanbieterdienst versenden möchten, können Sie Ihre Abonnementliste als CSV- oder XML-Datei exportieren.

## Verwalten von Abonnements für Kunden

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden im Raster und klicken Sie auf **[!UICONTROL Edit]** im _[!UICONTROL Action]_Spalte.

1. Klicks **[!UICONTROL Newsletter]** im linken Bereich.

1. Ändern Sie die Abonnements für den Kunden entsprechend Ihrer Site-/Store-Einrichtung.

   Bei einer einzelnen Site-/Einzelspeichereinrichtung können Sie einfach die **[!UICONTROL Subscribed to Newsletter]** aktivieren.

   ![Kästchen für die Abonnement eines Einzelstore-Kunden-Newsletters](./assets/newsletter-customer-single-store.png){width="500" zoomable="yes"}

   Bei einer einzelnen Site-/Multi-Store-Einrichtung können Sie die **[!UICONTROL Subscribed to Newsletter]** Kontrollkästchen und festlegen **[!UICONTROL Subscribed on Store View]** zur richtigen Store-Ansicht für das Abonnement.

   ![Kontrollkästchen für Abonnements für Newsletter von mehreren Stores und Auswahl der Store-Ansicht](./assets/newsletter-customer-multi-store.png){width="500" zoomable="yes"}

   Bei einer Einrichtung mit mehreren Sites/mehreren Stores mit einem globalen Kundenkontobereich zeigt die Seite den Abonnementstatus für alle Sites an. Sie können die **[!UICONTROL Subscribed]** und/oder ändern Sie **[!UICONTROL Store View]** für das Abonnement.

   ![Abonnement-Checkboxes für Newsletter von mehreren Sites und Store-Ansichtsauswahl](./assets/newsletter-customer-multi-site.png){width="500" zoomable="yes"}

1. Klicken **[!UICONTROL Save Customer]**.

## Abbrechen von Abonnements über die Abonnentenliste

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

   Bei einer Einrichtung mit mehreren Sites, bei der einige Kunden Abonnements für mehr als eine Site haben, wird jedes Abonnement als Zeileneintrag in der Tabelle angezeigt.

1. Suchen Sie den Abonnenten im Raster und aktivieren Sie das Kontrollkästchen in der ersten Spalte.

   >[!NOTE]
   >
   >Aktivieren Sie für eine Massenabmeldung das Kontrollkästchen jedes Abonnenten, den Sie abbrechen möchten.

1. Legen Sie die _[!UICONTROL Action]_Kontrolle an **[!UICONTROL Unsubscribe]**und klicken **[!UICONTROL Submit]**.

   ![Newsletter abmelden](./assets/newsletter-unsubscribe.png){width="600" zoomable="yes"}

   Der Status des Datensatzes ändert sich in `Unsubscribed`.

## Liste der Abonnenten exportieren

1. Aus dem _[!UICONTROL Newsletter Subscribers]_Liste verwenden Sie die Filtersteuerelemente, um nur Datensätze mit einer_ Status _von `Subscribed` und für die entsprechende Website-, Store- oder Store-Ansicht.

1. Legen Sie die **[!UICONTROL Export to]** ein Steuerelement zu einem der folgenden Elemente hinzufügen:

   - `CSV`
   - `XML`

1. Klicks **[!UICONTROL Export]** und suchen Sie nach der Eingabeaufforderung am unteren Bildschirmrand und speichern Sie die Datei.

   ![Newsletter-Abonnenten exportieren](./assets/newsletter-subscribers-export.png){width="600" zoomable="yes"}

## Abonnenten aus der Abonnentenliste löschen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

1. Suchen Sie den Abonnenten im Raster und aktivieren Sie das Kontrollkästchen in der ersten Spalte.

1. Legen Sie die _[!UICONTROL Action]_Kontrolle an **[!UICONTROL Delete]**und klicken **[!UICONTROL Submit]**.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.
