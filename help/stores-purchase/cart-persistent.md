---
title: Warenkorbpersistenz
description: Erfahren Sie, wie ein beständiger Warenkorb nicht gekaufte Artikel verfolgt und die Informationen für den nächsten Besuch des Kunden speichert.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: ea3aae3fce7f5e18155138b2bb9e7df0b3831fdd
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---

# Warenkorbpersistenz

Ein beständiger Warenkorb verfolgt nicht gekaufte Artikel im Warenkorb und speichert die Informationen. Dadurch wird sichergestellt, dass der Inhalt des Warenkorbs auch nach Ablauf der angemeldeten Sitzung verfügbar bleibt.

Wenn ein Kunde _an_ erinnert wird, bleibt der Inhalt seines Warenkorbs auf dem aktuellen Gerät verfügbar, wenn die angemeldete Sitzung abläuft. Nach Ablauf der Sitzung wird der Warenkorb des Kunden über die persistente Warenkorbsitzung aufgerufen. Wenn sich derselbe Kunde auf einem anderen Gerät oder Browser anmeldet und etwas zum Warenkorb hinzufügt und dann mit einer aktiven, beständigen Sitzung zum Gerät zurückkehrt, wird sein Warenkorb mit den hinzugefügten Artikeln aktualisiert.

Die Verwendung eines beständigen Warenkorbs kann die Anzahl der abgebrochenen Warenkörbe reduzieren und den Umsatz steigern. Der beständige Warenkorb **zeigt keine vertraulichen Kontoinformationen an.**

Um die Verwendung der Warenkorbpersistenz für Ihre Site oder in bestimmten Store-Ansichten zu verwalten, können Sie [persistente Warenkorbeinstellungen konfigurieren](#configure-a-persistent-cart). Weitere Informationen dazu, wie sich diese Einstellungen auf das Kundenerlebnis in Ihrer Storefront auswirken, finden Sie unter [Workflow für beständigen Warenkorb](#persistent-cart-workflow).

>[!NOTE]
>
>Die beständige Warenkorbfunktion ist nur für Kunden verfügbar, die registriert und angemeldet sind. Gastkäufer können die persistente Warenkorbfunktion nicht verwenden.

## Workflow für beständigen Warenkorb

Wenn der beständige Warenkorb [aktiviert](#configure-a-persistent-cart) ist, hängt der Workflow von Folgendem ab:

- Die Werte der Einstellungen _[!UICONTROL Enable Remember Me]_und_[!UICONTROL Clear Persistence on Log Out]_
- Die Entscheidung des Kunden, das Kontrollkästchen _[!UICONTROL Remember Me]_auszuwählen oder zu deaktivieren
- Wenn das persistente Cookie gelöscht wird

Wenn die Kundensitzung abläuft, wird in der Kopfzeile der Seite unter den folgenden Bedingungen ein `Not Jane Smith?` -Link angezeigt:
- der angemeldete Kunde die Option _[!UICONTROL Remember Me]_ausgewählt hat und ein beständiges Cookie angewendet wird
- Der Kunde meldet sich ab, wenn das System mit _[!UICONTROL Clear Persistence on Sign Out]_als `No` konfiguriert ist.

Das System speichert den Inhalt des Warenkorbs auf dem aktuellen Gerät, auch wenn die angemeldete Sitzung abläuft. Der Link `Not Jane Smith?` ermöglicht es dem Kunden, die persistente Sitzung zu beenden und zu beginnen, als Gast zu arbeiten, oder sich als ein anderer oder derselbe Kunde anzumelden.

Wenn der Kunde beim Anmelden das Kontrollkästchen _[!UICONTROL Remember Me]_aktiviert hat, erstellt und verwaltet Ihr Store ein separates persistentes Cookie. Dieses Cookie hilft, den Warenkorb des Kunden auch dann zugänglich zu machen, wenn er den Browser schließt oder zu einer anderen Site navigiert und die angemeldete Sitzung abläuft.

Wenn derselbe Kunde Ihren Store mit mehreren Browsern besucht, während er angemeldet ist oder eine persistente Sitzung aktiv ist, spiegeln sich die vom Kunden vorgenommenen Änderungen am Warenkorbinhalt in einem Browser in anderen Browsern wider, wenn die Seite aktualisiert wird.

>[!NOTE]
>
>Um die Synchronisierung des Warenkorbs über mehrere Geräte oder Browser hinweg sicherzustellen, müssen sich Kunden auf jedem neuen Gerät, das sie zum Einkaufen verwenden, anmelden. Für angemeldete Kunden werden die Inhalte des Warenkorbs über mehrere Geräte und Browser hinweg synchronisiert, solange sie unter demselben Konto angemeldet sind, unabhängig von der Konfiguration des beständigen Warenkorbs.

### Verhalten des Kontrollkästchens &quot;Angaben speichern&quot;

Kunden können das Kontrollkästchen _[!UICONTROL Remember Me]_auf der Anmeldeseite oder beim Erstellen eines neuen Kontos aktivieren, um den Inhalt des Warenkorbs beim Ablauf der angemeldeten Sitzung auf dem aktuellen Gerät zugänglich zu machen.

| Erinnern Sie sich an mich? | Ergebnis |
| ------------ |  ------ |
| Ausgewählt | Erstellt ein beständiges Cookie und behält den Inhalt des Warenkorbs auf dem aktuellen Gerät bei, wenn die Kundenanmeldesitzung abläuft. |
| Nicht ausgewählt | Erstellt kein beständiges Cookie und behält den Inhalt des Warenkorbs beim Ablauf der Anmeldesitzung auf dem aktuellen Gerät nicht bei. Beachten Sie, dass der Warenkorbinhalt weiterhin im Kundenkonto gespeichert und neu geladen wird, wenn sich der Kunde das nächste Mal anmeldet. |

{style="table-layout:auto"}

### Löschen der Persistenz beim Abmelden

Wenn sich der Kunde anmeldet oder sich bei der ausgewählten Option _Angaben speichern_ registriert, bestimmt die Konfiguration der Option _Persistenz beim Abmelden löschen_ das Verhalten des Warenkorbs.

|  | &quot;Persistenz beim Abmelden&quot;auf &quot;Ja&quot;festlegen | &quot;Persistenz beim Abmelden&quot;auf &quot;Nein&quot;setzen |
| ------ | ------ | ------ |
| _Erinnert_ Kunden meldet sich ab | Löscht sowohl Sitzungs- als auch persistente Cookies, sodass der Warenkorbinhalt auf dem aktuellen Gerät ausgeblendet wird, bis sich derselbe Kunde wieder anmeldet. | Löscht das Sitzungs-Cookie, aber das beständige Cookie bleibt in Kraft. Der Warenkorbinhalt bleibt auf dem aktuellen Gerät verfügbar. |
| _Erinnerter_ Kunde meldet sich nicht ab, doch das Sitzungs-Cookie läuft ab | Das persistente Cookie bleibt in Kraft, und der Warenkorbinhalt kann vom aktuellen Gerät aus aufgerufen werden. | Das persistente Cookie bleibt in Kraft, und der Warenkorbinhalt kann vom aktuellen Gerät aus aufgerufen werden. |

### Beispiel einer offenen Sitzung auf einem freigegebenen Computer

Jane beendet ihren Weihnachtseinkauf als angemeldeter Kunde _Erinnert_. Sie fügt John ein Geschenk zum Warenkorb und etwas für ihre Mutter hinzu. Dann geht sie zum Snack in die Küche und ihre Anmeldesitzung läuft ab.

John sitzt am Computer, um schnell einkaufen zu können, während Jane in der Küche ist. Ohne den `Not Jane Smith?` -Link oben auf der Seite zu sehen, findet John ein schönes Geschenk für Jane und fügt es zum Warenkorb hinzu. Wenn er auscheckt, merkt er, dass die Versand- und Rechnungsadresse vorausgefüllt sind und glaubt, dass er angemeldet ist. John hat es so eilig, dass er die zusätzlichen Elemente während der _Bestellprüfung_ nicht bemerkt und die Bestellung sendet. Janes Warenkorb ist jetzt leer, und John kaufte alle Geschenke.

## Persistenten Warenkorb konfigurieren

Bei der Einrichtung eines beständigen Warenkorbs können Sie die Lebensdauer der Cookies und die Optionen festlegen, die Sie für verschiedene Kundenaktivitäten verfügbar machen möchten.

Um den beständigen Warenkorb zu verwenden, muss der Browser des Kunden so eingestellt sein, dass Cookies zugelassen werden. Es gibt zwei Arten von Cookies, die für Warenkorbvorgänge verwendet werden:

- **Sitzungs-Cookie** - Ein kurzfristiges Sitzungs-Cookie ist während eines einzelnen Besuchs Ihrer Site vorhanden. Dieses Cookie läuft ab, wenn sich der Kunde abmeldet oder die Sitzung abläuft.

- **Persistentes Cookie** - Ein langfristiges, beständiges Cookie existiert nach dem Ende der angemeldeten Sitzung weiterhin. Dieses Cookie stellt sicher, dass der Inhalt des Warenkorbs eines Kunden weiterhin verfügbar ist, wenn sich der Kunde abmeldet oder die Sitzung abläuft.

Weitere Informationen dazu, wie sich diese Konfigurationseinstellungen auf den Kunden-Workflow auswirken, finden Sie unter [Workflow für beständigen Warenkorb](#persistent-cart-workflow).

{{$include /help/_includes/persistent-cart-configuration.md}}
