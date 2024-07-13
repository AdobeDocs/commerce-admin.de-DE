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

Sie können Ihre Abonnenten einfach über eine einfache Liste aktiver Abonnements verwalten. Wenn ein Kunde eine Abmeldeanforderung sendet, können Sie einfach eine _Abmeldung_ -Aktion auf ein oder mehrere ausgewählte Abonnements anwenden.

Bei Einzelsite-Setups mit mehreren Store-Ansichten kann ein Kundenkontoabonnement einer bestimmten Store-Ansicht zugeordnet werden.

Bei Multi-Store- und Multi-Site-Setups mit einem globalen [Kundenkontobereich](../customers/customer-account-scope.md) kann ein Kundenkonto für Newsletter für mehrere Sites/Stores abonniert werden. In diesem Fall können Sie das Kundenkonto bearbeiten, um eine Gruppe von Abonnements zu verwalten oder ein Abonnement für eine bestimmte Site/einen bestimmten Store abzubrechen, um eine Anfrage zu berücksichtigen.

Wenn Sie Newsletter mit einem Drittanbieterdienst versenden möchten, können Sie Ihre Abonnementliste als CSV- oder XML-Datei exportieren.

## Verwalten von Abonnements für Kunden

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden im Raster und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Klicken Sie im linken Bereich auf **[!UICONTROL Newsletter]** .

1. Ändern Sie die Abonnements für den Kunden entsprechend Ihrer Site-/Store-Einrichtung.

   Bei einer einzelnen Site-/Einzelspeichereinrichtung können Sie einfach das Kontrollkästchen **[!UICONTROL Subscribed to Newsletter]** aktivieren oder deaktivieren.

   ![Kontrollkästchen für die Anmeldung eines Einzelspeicherkunden-Newsletters](./assets/newsletter-customer-single-store.png){width="500" zoomable="yes"}

   Bei einer einzelnen Site-/Multi-Store-Einrichtung können Sie das Kontrollkästchen **[!UICONTROL Subscribed to Newsletter]** aktivieren bzw. deaktivieren und **[!UICONTROL Subscribed on Store View]** auf die richtige Store-Ansicht für das Abonnement setzen.

   ![Kontrollkästchen für die Abonnementaktivität für Newsletter mehrerer Stores und Auswahl der Store-Ansicht](./assets/newsletter-customer-multi-store.png){width="500" zoomable="yes"}

   Bei einer Einrichtung mit mehreren Sites/mehreren Stores mit einem globalen Kundenkontobereich zeigt die Seite den Abonnementstatus für alle Sites an. Sie können das Kontrollkästchen **[!UICONTROL Subscribed]** aktivieren bzw. deaktivieren und/oder die **[!UICONTROL Store View]** für das Abonnement ändern.

   ![Abonnement-Checkboxes für mehrseitige Newsletter-Kunden und Store-Ansichtsauswahl](./assets/newsletter-customer-multi-site.png){width="500" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Customer]**.

## Abbrechen von Abonnements über die Abonnentenliste

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

   Bei einer Einrichtung mit mehreren Sites, bei der einige Kunden Abonnements für mehr als eine Site haben, wird jedes Abonnement als Zeileneintrag in der Tabelle angezeigt.

1. Suchen Sie den Abonnenten im Raster und aktivieren Sie das Kontrollkästchen in der ersten Spalte.

   >[!NOTE]
   >
   >Aktivieren Sie für eine Massenabmeldung das Kontrollkästchen jedes Abonnenten, den Sie abbrechen möchten.

1. Setzen Sie das Steuerelement _[!UICONTROL Action]_auf **[!UICONTROL Unsubscribe]**und klicken Sie auf **[!UICONTROL Submit]**.

   ![Newsletter abmelden](./assets/newsletter-unsubscribe.png){width="600" zoomable="yes"}

   Der Status des Datensatzes ändert sich in `Unsubscribed`.

## Liste der Abonnenten exportieren

1. Verwenden Sie in der Liste _[!UICONTROL Newsletter Subscribers]_die Filtersteuerelemente, um nur Datensätze mit dem Status_ Status _von `Subscribed` und für die entsprechende Website-, Store- oder Store-Ansicht einzuschließen.

1. Setzen Sie das Steuerelement **[!UICONTROL Export to]** auf einen der folgenden Werte:

   - `CSV`
   - `XML`

1. Klicken Sie auf &quot;**[!UICONTROL Export]**&quot;, suchen Sie nach der Eingabeaufforderung am unteren Bildschirmrand und speichern Sie die Datei.

   ![Newsletter-Abonnenten exportieren](./assets/newsletter-subscribers-export.png){width="600" zoomable="yes"}

## Abonnenten aus der Abonnentenliste löschen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

1. Suchen Sie den Abonnenten im Raster und aktivieren Sie das Kontrollkästchen in der ersten Spalte.

1. Setzen Sie das Steuerelement _[!UICONTROL Action]_auf **[!UICONTROL Delete]**und klicken Sie auf **[!UICONTROL Submit]**.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.
