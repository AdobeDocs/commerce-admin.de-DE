---
title: PayPal-Abrechnungsbericht
description: Erfahren Sie mehr über den PayPal-Abrechnungsbericht als Tool zur Verwaltung von PayPal-Transaktionen.
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/c7v5oSsVPmD6r6obfGEoxPiGkMI4KMWAmfJAW0-CCJk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 233
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
