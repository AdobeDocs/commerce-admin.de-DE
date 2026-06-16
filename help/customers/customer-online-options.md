---
title: Lebensdauer der Kundensitzung
description: Die Lebensdauer einer Kundensitzung bestimmt die Lebensdauer einer Kundeneinkaufssitzung.
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
TQID: https://experienceleague.adobe.com/cJ8Rv5zMkTvZMfrl-nj-3xy3guSPDlxa7HZ-ZG7kLFw
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 403
ht-degree: 0%

---

# Lebensdauer der Kundensitzung

Die Lebensdauer einer Kunden-Shopping-Sitzung wird durch mehrere Faktoren bestimmt, darunter die Länge der Server-Sitzung, die Verwendung eines [persistenten Warenkorbs](../stores-purchase/cart-persistent.md) und die Lebensdauer der im Browser gespeicherten Informationen. Obwohl diese sich auf dasselbe Kundenerlebnis beziehen, handelt es sich um separate Prozesse mit unterschiedlichen Ablaufereignissen und Lebensdauern.

| Prozess | Beschreibung |
| --- | --- |
| Sitzung | Auf dem Server gespeicherte Informationen, z. B. der Inhalt des Warenkorbs. Wenn die Serversitzung abläuft, bevor das Cookie abläuft, verlieren Kunden möglicherweise den Inhalt des Warenkorbs und verringern das Sicherheitsrisiko. |
| Sitzungs-Cookie | Informationen, die im Browser als eine Anzahl oder Zeichenfolge gespeichert werden. Wenn das Sitzungs-Cookie vor der Serversitzung abläuft, wird der Kunde abgemeldet. Das Sitzungs-Cookie wird gelöscht, sobald der Kunde das Browser-Fenster schließt. Standardmäßig ist die Cookie-Lebensdauer auf 3.600 Sekunden oder eine Stunde festgelegt. Wenn in diesem Zeitraum keine Tastaturaktivität vorhanden ist, wird die aktuelle Sitzung beendet, und die Kunden müssen sich wieder bei ihren Konten anmelden, um den Einkauf fortsetzen zu können. |

{style="table-layout:auto"}

Wenn [Warenkorb](../stores-purchase/cart-persistent.md) aktiviert ist, werden die Inhalte des Warenkorbs gespeichert, wenn sich Kunden das nächste Mal bei ihren Konten anmelden. Bei der Verwendung eines persistenten Warenkorbs wird empfohlen, die Lebensdauer der Serversitzung und des Sitzungs-Cookies auf einen langen Zeitraum festzulegen.

Auf dem Server wird die Länge der Sitzung durch die `php.ini` Datei und mehrere Variablen gesteuert. Derzeit verfügt Adobe Commerce über keine Admin-Konfigurationseinstellung, die die Länge der Serversitzung steuert.

## Konfigurieren der Cookie-Lebensdauer

1. Navigieren Sie in _Admin_-Seitenleiste zu [!UICONTROL **Stores**] > _[!UICONTROL Settings]_>[!UICONTROL **Configuration**].

1. Wenn Sie mehrere Stores haben, stellen Sie die **[!UICONTROL Store View]** in der oberen rechten Ecke auf den Store ein, für den die Konfiguration gilt.

1. Wählen Sie im linken Bedienfeld unter **[!UICONTROL General]** die Option **[!UICONTROL Web]** aus.

1. Erweitern Sie den Abschnitt **[!UICONTROL Default Cookie Settings]** .

   ![Standard-Cookie-Einstellungen](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. Um den Standardwert zu ändern, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** und geben Sie den neuen Wert in Sekunden ein.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Konfigurieren der _Angaben speichern_ Funktion

Um die Anmeldung zu vereinfachen, ermöglicht die **[!UICONTROL Remember Me]** den Inhabern von Benutzerkonten, die Eingabe ihrer Anmeldeinformationen bei jedem Betreten der Storefront zu vermeiden. Aus Sicherheitsgründen ist die Persistenzfunktion standardmäßig deaktiviert.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Persistent Shopping Cart]**.

1. Erweitern Sie den Abschnitt **[!UICONTROL General Options]** .

1. Legen Sie **[!UICONTROL Enable Persistence]** auf `Yes` fest. (Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** , um die Änderung der Standardeinstellung zu ermöglichen.)

1. Wählen Sie **[!UICONTROL Enable "Remember Me"]** je nach Ihren Anforderungen `Yes` oder `No` aus.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
