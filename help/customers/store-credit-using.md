---
title: Store-Guthaben anwenden
description: Store-Administratoren können eine Store-Gutschrift auf einen Kauf anwenden.
exl-id: 97b6b206-71db-435c-8736-a781437bb0b4
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/O2EJMZscownPnhjPeFROdwikhYmHuDYdCx4N7NpXlho
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 321
ht-degree: 0%

---

# Store-Guthaben anwenden

{{ee-feature}}

Shop-Administratoren können den Guthabensaldo und die Historie aus dem Kundenkonto einsehen und auch eine Shop-Gutschrift auf einen Kauf anwenden.

![Kundenkredit- und -historie](assets/store-credit-balance-history.png){width="600" zoomable="yes"}

## Kreditsaldo anzeigen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden im Raster.

1. Klicken Sie in _Spalte_ Aktion **[!UICONTROL Edit]** auf.

1. Scrollen Sie _[!UICONTROL Customer View]_&#x200B;Seite und zeigen Sie die **[!UICONTROL Store Credit Balance]**&#x200B;unten an.

![Kontostand speichern](assets/store-credit-balance.png){width="600" zoomable="yes"}

## Aktualisieren des Speicherkreditsaldos

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > _Vorgänge_ > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden im Raster.

1. Klicken Sie in _Spalte_ Aktion **[!UICONTROL Edit]** auf.

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Store Credit]** aus.

1. Wählen Sie die Website (Storefront) aus, die Sie mit dem Saldo verknüpfen möchten.

1. Geben Sie **[!UICONTROL Update Balance]** den neuen Wert ein.

1. Um den Kunden über die Saldoaktualisierung zu informieren, aktivieren Sie das Kontrollkästchen **[!UICONTROL Notify Customer by Email]** und wählen Sie die Shop-Ansicht aus **[!UICONTROL Send Email Notification From the Following Store View]**.

1. Geben Sie eine **[!UICONTROL Comment]** über die Änderung ein.

1. Wenn die Aktualisierungen abgeschlossen sind, klicken Sie auf **[!UICONTROL Save and Continue Edit]** oder **[!UICONTROL Save Customer]**.

Der aktualisierte Saldo sollte in **[!UICONTROL Balance History]** angezeigt werden.

## Anwenden eines Guthabens auf eine Bestellung als Store-Administrator

Als Store-Administrator können Sie verschiedene Dinge im Namen eines Kunden tun, einschließlich der Abgabe von Bestellungen. Wenn Sie [eine Bestellung erstellen](../stores-purchase/customer-account-create-order.md) können Sie ein dem Kunden geschuldetes Filialguthaben zuordnen. Der verfügbare Saldo wird im Abschnitt _Zahlungs- und Versandinformationen_ angezeigt. Aktivieren Sie das Kontrollkästchen &quot;**[!UICONTROL Use Store Credit]**&quot;, um den Saldo anzuwenden, oder einen Teil des Saldos, wenn die Bestellsumme kleiner ist.

![Den Kontostand für den Shop auf die Bestellung anwenden](assets/store-credit-apply.png){width="500" zoomable="yes"}

## Warenkorb-Guthaben während des Checkouts anwenden

Wenn ein Guthaben für die Website vorhanden ist, kann der Kunde eine Gutschrift auf den Bestellsaldo anwenden, bevor er die Bestellung in der Storefront aufgibt.

1. Der Kunde zeigt den Betrag des verfügbaren Speicherguthabens an.

   Während des Schritts _Überprüfen und_&quot; wird der verfügbare Betrag unter &quot;_[!UICONTROL Store Credit]_&quot; angezeigt.

1. Um den Betrag auf die Bestellung anzuwenden, klicken Sie auf **[!UICONTROL Use Store Credit]**.

   >[!INFO]
   >
   >Die Bestellsumme wird neu berechnet, und der Betrag der angewendeten Speichergutschrift wird im _[!UICONTROL Order Summary]_&#x200B;angezeigt.

   ![Auf die Bestellung angewendetes Guthaben speichern](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. Wenn Sie bereit sind, klicken Sie auf **[!UICONTROL Place Order]**.
