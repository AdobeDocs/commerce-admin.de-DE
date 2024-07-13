---
title: Lebensdauer der Kundensitzung
description: Die Lebensdauer der Kundensitzung bestimmt die Lebensdauer einer Customer Shopping-Sitzung.
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Lebensdauer der Kundensitzung

Die Lebensdauer einer Customer Shopping-Sitzung wird durch verschiedene Faktoren bestimmt, darunter die Länge der Server-Sitzung, die Verwendung eines [beständigen Warenkorbs](../stores-purchase/cart-persistent.md) und die Lebensdauer der im Browser gespeicherten Informationen. Diese beziehen sich zwar auf dasselbe Kundenerlebnis, sind jedoch separate Prozesse mit unterschiedlichen Ablaufereignissen und Lebenszeiten.

| Prozess | Beschreibung |
| --- | --- |
| Sitzung | Informationen, die auf dem Server gespeichert werden, wie der Inhalt des Warenkorbs. Wenn die Serversitzung abläuft, bevor das Cookie abläuft, verlieren Kunden möglicherweise den Inhalt des Warenkorbs und verringern das Sicherheitsrisiko. |
| Sitzungs-Cookie | Informationen, die im Browser als Anzahl oder Zeichenfolge gespeichert werden. Wenn das Sitzungs-Cookie vor der Serversitzung abläuft, wird der Kunde abgemeldet. Das Sitzungs-Cookie wird gelöscht, wenn der Kunde das Browserfenster schließt. Standardmäßig ist die Cookie-Lebensdauer auf 3600 Sekunden oder eine Stunde festgelegt. Wenn während dieser Zeit keine Tastaturaktivität ausgeführt wird, endet die aktuelle Sitzung und Kunden müssen sich wieder bei ihren Konten anmelden, um den Einkauf fortzusetzen. |

{style="table-layout:auto"}

Wenn [Persistenter Warenkorb](../stores-purchase/cart-persistent.md) aktiviert ist, werden die Inhalte des Warenkorbs zum nächsten Mal gespeichert, wenn sich Kunden in ihren Konten anmelden. Bei Verwendung eines persistenten Warenkorbs wird empfohlen, die Lebensdauer der Serversitzung und des Sitzungs-Cookies auf einen langen Zeitraum festzulegen.

Auf dem Server wird die Sitzungslänge durch die Datei `php.ini` und mehrere Variablen gesteuert. Derzeit verfügt Adobe Commerce nicht über eine Admin-Konfigurationseinstellung, die die Dauer der Serversitzung steuert.

## Cookie-Lebensdauer konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu [!UICONTROL **Stores**] > _[!UICONTROL Settings]_>[!UICONTROL **Konfiguration**].

1. Wenn mehrere Stores vorhanden sind, setzen Sie die Auswahl **[!UICONTROL Store View]** in der oberen rechten Ecke auf den Store, für den die Konfiguration gilt.

1. Wählen Sie im linken Bereich unter **[!UICONTROL General]** die Option **[!UICONTROL Web]**.

1. Erweitern Sie den Abschnitt **[!UICONTROL Default Cookie Settings]** .

   ![Standard-Cookie-Einstellungen](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. Um den Standardwert zu ändern, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** und geben Sie den neuen Wert in Sekunden ein.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Konfigurieren der Funktion _Angaben speichern_

Um die Anmeldung zu vereinfachen, ermöglicht es die Funktion **[!UICONTROL Remember Me]** Benutzerkontoinhabern, die Eingabe ihrer Anmeldedaten bei jedem Eintritt in die Storefront zu vermeiden. Aus Sicherheitsgründen ist die Persistenzfunktion standardmäßig deaktiviert.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Persistent Shopping Cart]** aus.

1. Erweitern Sie den Abschnitt **[!UICONTROL General Options]** .

1. Setzen Sie für **[!UICONTROL Enable Persistence]** den Wert auf `Yes`. (Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** , um die Änderung der Standardeinstellung zu ermöglichen.)

1. Setzen Sie für **[!UICONTROL Enable "Remember Me"]** entsprechend Ihren Anforderungen auf `Yes` oder `No`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
