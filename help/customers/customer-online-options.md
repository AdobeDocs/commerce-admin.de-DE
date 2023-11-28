---
title: Lebensdauer der Kundensitzung
description: Die Lebensdauer der Kundensitzung bestimmt die Lebensdauer einer Customer Shopping-Sitzung.
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Lebensdauer der Kundensitzung

Die Lebensdauer einer Customer Shopping-Sitzung wird durch verschiedene Faktoren bestimmt, darunter die Dauer der Server-Sitzung und die Verwendung einer [persistenter Warenkorb](../stores-purchase/cart-persistent.md)und die Lebensdauer der im Browser gespeicherten Informationen. Diese beziehen sich zwar auf dasselbe Kundenerlebnis, sind jedoch separate Prozesse mit unterschiedlichen Ablaufereignissen und Lebenszeiten.

| Prozess | Beschreibung |
| --- | --- |
| Sitzung | Informationen, die auf dem Server gespeichert werden, wie der Inhalt des Warenkorbs. Wenn die Serversitzung abläuft, bevor das Cookie abläuft, verlieren Kunden möglicherweise den Inhalt des Warenkorbs und verringern das Sicherheitsrisiko. |
| Sitzungs-Cookie | Informationen, die im Browser als Anzahl oder Zeichenfolge gespeichert werden. Wenn das Sitzungs-Cookie vor der Serversitzung abläuft, wird der Kunde abgemeldet. Das Sitzungs-Cookie wird gelöscht, wenn der Kunde das Browserfenster schließt. Standardmäßig ist die Cookie-Lebensdauer auf 3600 Sekunden oder eine Stunde festgelegt. Wenn während dieser Zeit keine Tastaturaktivität ausgeführt wird, endet die aktuelle Sitzung und Kunden müssen sich wieder bei ihren Konten anmelden, um den Einkauf fortzusetzen. |

{style="table-layout:auto"}

Wenn [Persistenter Warenkorb](../stores-purchase/cart-persistent.md) aktiviert ist, werden die Inhalte des Warenkorbs zum nächsten Mal gespeichert, wenn sich Kunden in ihren Konten anmelden. Bei Verwendung eines persistenten Warenkorbs wird empfohlen, die Lebensdauer der Serversitzung und des Sitzungs-Cookies auf einen langen Zeitraum festzulegen.

Auf dem Server wird die Sitzungslänge durch die `php.ini` und mehrere Variablen. Derzeit verfügt Adobe Commerce nicht über eine Admin-Konfigurationseinstellung, die die Dauer der Serversitzung steuert.

## Cookie-Lebensdauer konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu [!UICONTROL **Stores**] > _[!UICONTROL Settings]_>[!UICONTROL **Konfiguration**].

1. Wenn mehrere Stores vorhanden sind, legen Sie die **[!UICONTROL Store View]** Wählen Sie in der oberen rechten Ecke den Store aus, für den die Konfiguration gilt.

1. Im linken Bereich unter **[!UICONTROL General]** auswählen **[!UICONTROL Web]**.

1. Erweitern Sie die **[!UICONTROL Default Cookie Settings]** Abschnitt.

   ![Standard-Cookie-Einstellungen](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. Um den Standard zu ändern, löschen Sie die **[!UICONTROL Use system value]** und geben Sie den neuen Wert in Sekunden ein.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Konfigurieren _Angaben speichern_ Funktion

Um die Anmeldung zu vereinfachen, wird die **[!UICONTROL Remember Me]** -Funktion können Benutzer-Kontoinhaber die Eingabe ihrer Anmeldedaten bei jedem Eintritt in die Storefront vermeiden. Aus Sicherheitsgründen ist die Persistenzfunktion standardmäßig deaktiviert.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen **[!UICONTROL Persistent Shopping Cart]**.

1. Erweitern Sie die **[!UICONTROL General Options]** Abschnitt.

1. Für **[!UICONTROL Enable Persistence]**, auf `Yes`. (Löschen Sie die **[!UICONTROL Use system value]** aktivieren, damit die Standardeinstellung geändert werden kann.)

1. Für **[!UICONTROL Enable "Remember Me"]**, auf `Yes` oder `No` entsprechend Ihren Anforderungen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
