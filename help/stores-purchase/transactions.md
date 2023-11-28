---
title: Transaktionen
description: Erfahren Sie mehr über die Seite Transaktionen und wie Sie damit die Aktivität zwischen Ihrem Store und einem Zahlungssystem verfolgen können.
exl-id: 5970db88-146d-4caf-aab4-d9315357a4fe
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Transaktionen

Die _Transaktionen_ auf der Seite werden alle Zahlungsaktivitäten aufgelistet, die zwischen Ihrem Geschäft und einem Zahlungssystem stattgefunden haben, und erhalten Zugriff auf detailliertere Informationen.

## Transaktionen anzeigen

Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Transactions]**.

![Transaktionsraster](./assets/transactions.png){width="600" zoomable="yes"}

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Eine eindeutige numerische Kennung, die jeder Transaktion zugewiesen wird. |
| [!UICONTROL Order ID] | Eine eindeutige Kennung, die zugewiesen wird, wenn ein Kunde eine Bestellung aufgibt. |
| [!UICONTROL Transaction ID] | Eine eindeutige numerische Kennung, die zugewiesen wird, wenn eine Transaktion stattfindet, nachdem ein Kunde eine Bestellung aufgegeben hat. |
| [!UICONTROL Parent Transaction ID] | Die ID-Nummer der übergeordneten Transaktion |
| [!UICONTROL Payment Method] | Die mit einer Transaktion verknüpfte Zahlungsmethode. |
| [!UICONTROL Transaction Type] | Art der Transaktion, bei der es sich um Bestellung, Autorisierung, Erfassung, Nichterfüllung oder Erstattung handeln kann. |
| [!UICONTROL Closed] | Ob eine Transaktion geschlossen wird oder nicht. |
| [!UICONTROL Created] | Zeitpunkt und Datum der Erstellung der Transaktion. |

{style="table-layout:auto"}

## Anzeigen von Transaktionsdetails

Klicken Sie auf den Eintrag, den Sie anzeigen möchten.

Auf der Seite mit den Transaktionsdetails können Sie das Raster mit den Transaktionsdetails und untergeordneten Transaktionen anzeigen.

### Transaktionsdaten

Dieser Abschnitt enthält Informationen zur Transaktion und stellt einen Link zur Bestellseite im **Auftrags-ID** Spalte.

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Transaction ID] | Die Transaktions-ID-Nummer |
| [!UICONTROL Parent Transaction ID] | Eine entsprechende ID-Nummer der übergeordneten Transaktion, falls zutreffend. |
| [!UICONTROL Transaction Type] | Art der Transaktion, bei der es sich um Bestellung, Autorisierung, Erfassung, Nichterfüllung oder Erstattung handeln kann. |
| [!UICONTROL Is Closed] | Ob eine Transaktion geschlossen wird oder nicht. |
| [!UICONTROL Created At] | Zeitpunkt und Datum der Erstellung der Transaktion. |

{style="table-layout:auto"}

### Kindergeschäfte

Untergeordnete Transaktionen werden nach der Erstellung von Rechnungen für [Bestellungen](orders.md). In diesem Format können Sie den Transaktionsverlauf anhand einer Transaktionshierarchie verfolgen.

### [!UICONTROL Transaction Details]

Dieser Abschnitt enthält die zusätzlichen Informationen zu einer Transaktion. Informationen werden in Form von Schlüsseln und Werten angezeigt. Die verfügbaren Schlüssel sind:

- authAmount
- authCode
- aVSResponse
- billTo
- cardCodeResponse
- customer
- customerIP
- lineItems
- marketType
- bestellen
- payment
- product
- recurringBilling
- responseCode
- responseReasonCode
- responseReasonDescription
- settleAmount
- Lösung
- submitTimeLocal
- submitTimeUTC
- taxExempt
- transactionStatus

>[!NOTE]
>
>Wenn die Transaktionsdetails nicht verfügbar sind oder veraltet sind, klicken Sie auf **[!UICONTROL Fetch]** in der Schaltflächenleiste, um sie zu aktualisieren.
