---
title: Verwalten von Newsletter-Abonnenten
description: Erfahren Sie, wie Sie Ihre Newsletter-Abonnenten mithilfe einer einfachen Liste aktiver Abonnements verwalten können.
exl-id: c7e8e642-e3fd-4979-9ea3-2d96839730b2
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Verwalten von Newsletter-Abonnenten

Als Best Practice sollten Sie Ihre Abonnement-Liste regelmäßig verwalten und sicherstellen, dass Sie alle Anfragen zur Abmeldung bearbeiten. In einigen Ländern ist es gesetzlich vorgeschrieben, dass Abmeldeanfragen innerhalb eines bestimmten Zeitraums bearbeitet werden.

Sie können Ihre Abonnentinnen und Abonnenten einfach über eine einfache Liste aktiver Abonnements verwalten. Wenn ein Kunde eine Abmeldeanfrage sendet, können Sie einfach eine Aktion _Abmelden_ auf ein oder mehrere ausgewählte Abonnements anwenden.

Bei Einzelstandort-Setups mit mehreren Store-Ansichten kann ein Kundenkonto-Abonnement mit einer bestimmten Store-Ansicht verknüpft werden.

Bei Multi-Store- und Multi-Site-Setups mit einem globalen [Kundenkontobereich](../customers/customer-account-scope.md) kann ein Kundenkonto für mehrere Sites/Stores Newsletter abonniert werden. In diesem Fall können Sie das Kundenkonto bearbeiten, um eine Gruppe von Abonnements zu verwalten, oder ein Abonnement für eine bestimmte Site/einen bestimmten Store kündigen, um einer Anfrage nachzukommen.

Wenn Sie Newsletter über einen Drittanbieterdienst versenden möchten, können Sie Ihre Abonnement-Liste als CSV- oder XML-Datei exportieren.

## Abonnements für einen Kunden verwalten

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden im Raster und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Klicken Sie im linken Bedienfeld auf **[!UICONTROL Newsletter]** .

1. Ändern Sie die Abonnements für den Kunden entsprechend Ihrer Site-/Store-Einrichtung.

   Bei einem Setup mit nur einer Site bzw. nur einem Store können Sie einfach das Kontrollkästchen **[!UICONTROL Subscribed to Newsletter]** aktivieren oder deaktivieren.

   ![Kontrollkästchen für das Abonnement eines einzelnen Kunden-Newsletters](./assets/newsletter-customer-single-store.png){width="500" zoomable="yes"}

   Bei einem Setup mit einer einzelnen Site bzw. mehreren Stores können Sie das Kontrollkästchen **[!UICONTROL Subscribed to Newsletter]** aktivieren oder deaktivieren und **[!UICONTROL Subscribed on Store View]** auf die richtige Store-Ansicht für das Abonnement festlegen.

   ![Kontrollkästchen für das Abonnement von Multi-Store-Kunden-Newslettern und die Auswahl für die Store-Ansicht](./assets/newsletter-customer-multi-store.png){width="500" zoomable="yes"}

   Bei einer Einrichtung mit mehreren Sites/mehreren Shops mit einem globalen Kundenkontobereich zeigt die Seite den Abonnementstatus für alle Sites an. Sie können das Kontrollkästchen **[!UICONTROL Subscribed]** aktivieren oder deaktivieren und/oder die **[!UICONTROL Store View]** für das Abonnement ändern.

   ![Kontrollkästchen für das Abonnement von Multi-Site-Kunden-Newslettern und Store-Selektoren](./assets/newsletter-customer-multi-site.png){width="500" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Customer]**.

## Abo über die Abonnentenliste stornieren

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

   Bei einem Multi-Site-Setup, bei dem einige Kunden Abonnements für mehr als eine Site haben, wird jedes Abonnement als Zeilenelement im Raster angezeigt.

1. Suchen Sie den Abonnenten im Raster und aktivieren Sie das Kontrollkästchen in der ersten Spalte.

   >[!NOTE]
   >
   >Für eine Massenabmeldung aktivieren Sie das Kontrollkästchen jedes Abonnenten, den Sie abbrechen möchten.

1. Legen Sie das _[!UICONTROL Action]_auf **[!UICONTROL Unsubscribe]**fest und klicken Sie auf **[!UICONTROL Submit]**.

   ![Newsletter abbestellen](./assets/newsletter-unsubscribe.png){width="600" zoomable="yes"}

   Der Status des Datensatzes ändert sich in `Unsubscribed`.

## Abonnentenliste exportieren

1. Verwenden Sie in der Liste &quot;_[!UICONTROL Newsletter Subscribers]_&quot; die Filtersteuerelemente, um nur Datensätze mit einem_ Status _von `Subscribed` und für die entsprechende Website-, Store- oder Store-Ansicht einzuschließen.

1. Legen Sie das **[!UICONTROL Export to]**-Steuerelement auf eine der folgenden Einstellungen fest:

   - `CSV`
   - `XML`

1. Klicken Sie auf **[!UICONTROL Export]**, suchen Sie im unteren Bildschirmbereich nach der Eingabeaufforderung und speichern Sie die Datei.

   ![Newsletter-Abonnenten exportieren](./assets/newsletter-subscribers-export.png){width="600" zoomable="yes"}

## Löschen eines Abonnenten aus der Abonnentenliste

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

1. Suchen Sie den Abonnenten im Raster und aktivieren Sie das Kontrollkästchen in der ersten Spalte.

1. Legen Sie das _[!UICONTROL Action]_auf **[!UICONTROL Delete]**fest und klicken Sie auf **[!UICONTROL Submit]**.

1. Wenn Sie zum Bestätigen aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.
