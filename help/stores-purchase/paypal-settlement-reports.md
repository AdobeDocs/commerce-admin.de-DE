---
title: PayPal-Abrechnungsbericht
description: Erfahren Sie mehr über den PayPal-Abrechnungsbericht als Tool zur Verwaltung von PayPal-Transaktionen.
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# PayPal-Abrechnungsbericht

Der PayPal-Abrechnungsbericht stellt Händlern die Informationen zu jeder Transaktion zur Verfügung, die die Abrechnung von Geldern beeinflusst.

>[!NOTE]
>
>Vor der Erstellung von Abrechnungsberichten muss der Store-Administrator PayPal Merchant Technical Services auffordern, ein SFTP-Benutzerkonto zu erstellen, die Erstellung von Abrechnungsberichten zu aktivieren und SFTP in seinem PayPal-Geschäftskonto zu aktivieren.

Nach der Konfiguration und Aktivierung von Abrechnungsberichten im PayPal-Händlerkonto beginnen Adobe Commerce und Magento Open Source in den folgenden 24 Stunden mit der Erstellung von Berichten. Die Liste der verfügbaren Abwicklungsberichte kann vom Administrator eingesehen werden.

**_So zeigen Sie Abwicklungsberichte an:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**.

   ![PayPal-Abrechnungsberichte](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. Klicken Sie oben rechts auf **[!UICONTROL Fetch Updates]**, um die neuesten Aktualisierungen anzuzeigen.

   Das System stellt eine Verbindung zum PayPal-SFTP-Server her, um die Berichte abzurufen. Nach Abschluss des Vorgangs wird eine Meldung mit der Anzahl der abgerufenen Berichte angezeigt. Der Bericht enthält für jede Transaktion folgende Informationen:

   | Berichtsspalte | Beschreibung |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | Einer der folgenden Referenz-Codes:<br/>- Order IDT<br/>- Transaction ID<br/>- Subscription ID |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]** - Der Text, den der Händler auf der Transaktion bei PayPal eingegeben hat.<br/>**[!UICONTROL Transaction Debit or Credit]**- Die Richtung der Geldbewegung des Bruttobetrags.<br/>**[!UICONTROL Fee Debit or Credit]** - Die Richtung der Geldbewegung gegen Gebühr. |

   {style="table-layout:auto"}
