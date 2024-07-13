---
title: PayPal-Vergleichsbericht
description: Erfahren Sie mehr über den PayPal-Vergleichsbericht als Tool zur Verwaltung von PayPal-Transaktionen.
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# PayPal-Vergleichsbericht

Der PayPal-Abrechnungsbericht liefert den Händlern die Informationen zu jedem Geschäft, das sich auf die Abwicklung von Fonds auswirkt.

>[!NOTE]
>
>Vor der Generierung von Vergleichsberichten muss der Store-Administrator die technischen PayPal-Handelsdienste auffordern, ein SFTP-Benutzerkonto zu erstellen, die Generierung von Vergleichsberichten zu aktivieren und SFTP in seinem PayPal-Geschäftskonto zu aktivieren.

Nach der Konfiguration und Aktivierung der Vergleichsberichte im PayPal-Handelskonto werden Adobe Commerce und Magento Open Source in den darauf folgenden 24 Stunden mit der Erstellung von Berichten beginnen. Die Liste der verfügbaren Vergleichsberichte kann vom Administrator eingesehen werden.

**_Anzeigen von Vergleichsberichten:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**.

   ![PayPal-Vergleichsberichte](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. Klicken Sie für die neuesten Updates oben rechts auf &quot;**[!UICONTROL Fetch Updates]**&quot;.

   Das System stellt eine Verbindung zum PayPal SFTP-Server her, um die Berichte abzurufen. Wenn der Prozess abgeschlossen ist, wird eine Meldung mit der Anzahl der abgerufenen Berichte angezeigt. Der Bericht enthält für jede Transaktion die folgenden Informationen:

   | Berichtsspalte | Beschreibung |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | Einer der folgenden Referenzcodes:<br/>- Order IDT<br/>- Transaction ID<br/>- Subscription ID |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]** - Der vom Händler bei PayPal bei der Transaktion eingegebene Text.<br/>**[!UICONTROL Transaction Debit or Credit]**- Die Richtung der Geldbewegung des Bruttobetrags.<br/>**[!UICONTROL Fee Debit or Credit]** - Die Richtung der Geldbewegung gegen Gebühr. |

   {style="table-layout:auto"}
