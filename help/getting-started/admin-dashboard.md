---
title: Admin-Dashboard
description: Erfahren Sie mehr über das Admin-Dashboard, bei dem es sich normalerweise um die erste Seite handelt, die bei der Anmeldung angezeigt wird.
exl-id: 56957c0a-1618-444b-a37a-ecf0d7b27eae
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Admin-Dashboard

Das Dashboard ist normalerweise die erste Seite, die bei der Anmeldung bei _Admin_ angezeigt wird und einen Echtzeitüberblick über Vertrieb und Kundenaktivität bieten kann. Dashboard-Daten liefern eine Momentaufnahme der Lebensdauerverkäufe, der durchschnittlichen Bestellmenge, der letzten Bestellungen und Suchbegriffe. Das Diagramm zeigt abgeschlossene Bestellungen und Beträge für den ausgewählten Datumsbereich an und kann entweder aus dynamischen, Echtzeit- oder historischen aggregierten Daten generiert werden. Die Registerkarten am unteren Rand bieten schnelle Berichte zu Ihren am besten verkauften Produkten, den am häufigsten angezeigten Produkten, neuen Kunden und Kunden, die am häufigsten gekauft haben.

Wenn Sie eine erhebliche Menge an zu verarbeitenden Daten haben, kann das Diagramm zur Leistungsverbesserung deaktiviert werden. Das Dashboard im folgenden Beispiel ist so konfiguriert, dass Echtzeitdaten verwendet werden. Es zeigt abgeschlossene Bestellungen nach Stunde für die letzten 24 Stunden an. Das Diagramm wird für jede abgeschlossene Bestellung aktualisiert.

![Dashboard](./assets/dashboard-full.png){zoomable="yes"}

[Erweiterte Berichterstellung](business-intelligence.md#advanced-reporting) zeigt ein personalisiertes Dashboard an, das auf Ihren Produkt-, Bestell- und Kundendaten basiert.

![Erweiterte Berichterstellung](./assets/dashboard-advanced-reporting.png){zoomable="yes"}

## Dashboard konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**und nehmen Sie die folgenden Einstellungen vor.

1. Klicken Sie nach Abschluss der Konfiguration auf **[!UICONTROL Save Config]**.

1. Klicken Sie nach dem Speichern der Änderungen auf **[!UICONTROL Cache Management]** und aktualisieren Sie jeden ungültigen Cache.

### Grafiken aktivieren

Wenn Sie eine große Datenmenge verarbeiten müssen, können Sie die Anzeige der Grafik deaktivieren, um die Leistung zu verbessern. Wenn die Option nicht aktiviert ist, wird anstelle der Grafik die Meldung &quot;Keine Daten gefunden&quot;angezeigt, obwohl die Summen der Zusammenfassung unten noch generiert werden.

1. Wählen Sie im linken Navigationsbereich unter **[!UICONTROL Advanced]** die Option **[!UICONTROL Admin]**.

1. Erweitern Sie ggf. den Abschnitt **[!UICONTROL Dashboard]** .

   ![Erweiterte Konfiguration - Grafiken aktivieren](./assets/admin-dashboard-config.png){width="600"}

1. Um den Standardwert zu ändern, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** .

1. Setzen Sie **Grafiken aktivieren** auf `Yes`.

Weitere Informationen zu den Admin-Konfigurationsoptionen finden Sie im [Konfigurationshandbuch](../configuration-reference/advanced/admin.md).

### Startseite ändern

Das Dashboard ist die standardmäßige [Startseite](../configuration-reference/advanced/admin.md) für den Admin. Sie können jedoch eine andere Startseite konfigurieren.

1. Wenn Sie die Admin-Konfigurationsoptionen noch nicht geöffnet haben, wählen Sie im linken Navigationsbereich unter _[!UICONTROL Advanced]_die Option **[!UICONTROL Admin]**aus.

1. Klicken Sie auf , um den Abschnitt **Startseite** zu erweitern.

   ![Admin-Dashboard - Einstellung der Startseite](./assets/admin-startup-page.png){width="600"}

1. Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** und wählen Sie die **Startseite** aus, die bei der Anmeldung beim Administrator angezeigt werden soll.

### Startdatum auswählen

1. Wählen Sie im linken Navigationsbereich unter **[!UICONTROL General]** die Option **Berichte**.

1. Erweitern Sie auf der Seite den Abschnitt **[!UICONTROL Dashboard]** .

1. Deaktivieren Sie die Kontrollkästchen **[!UICONTROL Use system value]** für die Datumseinstellungen und gehen Sie wie folgt vor:

   - Setzen Sie **Jahr-zu-Datum-Starts** auf **Monat** und **Tag**.

   - Setzen Sie **Aktuelle Monatsstarts** auf den **Tag**.

   ![Admin-Dashboard - Datumseinstellungen](./assets/reports-dashboard.png){width="600"}

Weitere Informationen zu den [!UICONTROL Reports] -Konfigurationsoptionen finden Sie im [_Konfigurationshandbuch_](../configuration-reference/general/reports.md).

### Konfigurieren der Datenquelle

Das Dashboard-Diagramm kann in Echtzeit oder mithilfe von historischen, aggregierten Daten erstellt werden. Wenn die Leistung ein Problem darstellt, können Sie die Dinge durch die Verwendung aggregierter Daten beschleunigen.

1. Klicken Sie im linken Navigationsbereich auf **Verkauf** erweitern und unter dem Punkt **Verkauf** auswählen.

1. Erweitern Sie auf der Seite den Abschnitt **[!UICONTROL Dashboard]** .

   ![Admin-Dashboard - Datenquelleneinstellung](./assets/config-sales-dashboard.png){width="600"}

1. Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** und legen Sie **[!UICONTROL Use Aggregated Data]** auf einen der folgenden Werte fest:

   - Wählen Sie für historische aggregierte Daten `Yes` aus.
   - Wählen Sie für Echtzeitdaten &quot;`No`&quot;.

## Diagrammabschnitte

| Abschnitt | Beschreibung |
|--- |--- |
| [!UICONTROL Orders] | Auf dieser Registerkarte wird ein Echtzeit-Diagramm aller abgeschlossenen Bestellungen für die aktuelle Store-Ansicht und den angegebenen Zeitraum angezeigt. |
| [!UICONTROL Amounts] | Auf dieser Registerkarte wird ein Echtzeit-Diagramm mit allen abgeschlossenen Bestellmengen für die aktuelle Store-Ansicht und den angegebenen Zeitraum angezeigt. |
| [!UICONTROL Time Range] | Bestimmt die Daten, die in den unten stehenden Summen der Grafik und Zusammenfassung dargestellt werden. Optionen: `Last 7 Days` / `Current Month` / `YTD` / `2YTD` |
| [!UICONTROL Summary Totals] | Die Gesamtsummen für Umsatz, Steuern, Versand und Menge unter dem Diagramm basieren auf den Diagrammdaten und der aktuellen Zeitbereichseinstellung. |

{style="table-layout:auto"}

## Momentaufnahmen-Daten

| Abschnitt | Beschreibung |
|--- |--- |
| [!UICONTROL Lifetime Sales] | Die aggregierten Gesamtverkäufe während der Lebensdauer des Stores. |
| [!UICONTROL Average Order] | Die durchschnittliche Bestellmenge während der Lebensdauer des Stores. |
| [!UICONTROL Last Orders] | Eine Zusammenfassung der letzten fünf aufgegebenen Bestellungen. |
| [!UICONTROL Last Search Terms] | Die letzten fünf Suchbegriffe. |
| [!UICONTROL Top Search Terms] | Die fünf häufigsten Suchbegriffe. |

{style="table-layout:auto"}

## Berichtregisterkarten

| Abschnitt | Beschreibung |
|--- |--- |
| [!UICONTROL Bestsellers] | Die fünf am besten verkauften Produkte im angegebenen Zeitraum. |
| [!UICONTROL Most Viewed Products] | Die fünf Produkte wurden im angegebenen Zeitraum am häufigsten angezeigt. |
| [!UICONTROL New Customers] | Die letzten fünf Kunden, die sich im angegebenen Zeitraum für ein Konto angemeldet haben. |
| [!UICONTROL Customers] | Die letzten fünf Kunden mit einer Bestellung, die die Verarbeitung im angegebenen Zeitraum abgeschlossen hat. |

{style="table-layout:auto"}

## Dashboard-Schaltfläche

| Schaltfläche | Beschreibung |
|--- |--- |
| [!UICONTROL Reload Data] | Aktualisiert Dashboard-Daten. |
| [!UICONTROL Go to Advanced Reporting] | Zeigt ein personalisiertes Dashboard mit dynamischen Diagrammen und Berichten an, die auf Ihren Produkt-, Bestell- und Kundendaten basieren. Weitere Informationen finden Sie unter [Erweiterte Berichterstellung](business-intelligence.md#advanced-reporting). |

{style="table-layout:auto"}
