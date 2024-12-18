---
title: Warenkorb-Persistenz
description: Erfahren Sie, wie ein persistenter Warenkorb nicht gekaufte Artikel im Warenkorb nachverfolgt und die Informationen für den nächsten Besuch des Kunden speichert.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: 2bddf979333bdafbfb6b445140515942b1115eea
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 0%

---

# Warenkorb-Persistenz

Ein persistenter Warenkorb speichert einen Verweis auf das Kundenkonto auf dem aktuellen Gerät und stellt sicher, dass der Inhalt des Warenkorbs verfügbar bleibt, wenn die angemeldete Sitzung abläuft.

Wenn ein Kunde _erinnert_ bleibt der Inhalt seines Warenkorbs auf dem aktuellen Gerät verfügbar, wenn die angemeldete Sitzung abläuft. Nach Ablauf der Sitzung wird der Warenkorb des Kunden über die persistente Warenkorbsitzung aufgerufen. Wenn sich derselbe Kunde auf einem anderen Gerät oder Browser anmeldet und etwas zu seinem Warenkorb hinzufügt und dann mit einer aktiven persistenten Sitzung zum Gerät zurückkehrt, wird sein Warenkorb mit den hinzugefügten Artikeln aktualisiert.

Die Verwendung eines beständigen Warenkorbs kann die Anzahl der abgebrochenen Warenkörbe reduzieren und den Umsatz steigern. Der persistente Warenkorb (**)** zu keinem Zeitpunkt vertrauliche Kontoinformationen offen.

Um die Verwendung der Warenkorbpersistenz für Ihre Site oder in bestimmten Store-Ansichten zu verwalten, können Sie [Einstellungen für den persistenten Warenkorb konfigurieren](#configure-a-persistent-cart). Weitere Informationen darüber, wie sich diese Einstellungen auf das Kundenerlebnis in Ihrer Storefront auswirken, finden Sie unter [Workflow für persistente Warenkörbe](#persistent-cart-workflow).

>[!NOTE]
>
>Die Funktion „Dauerhafter Warenkorb“ ist nur für Kunden verfügbar, die registriert und angemeldet sind. Gäste-Shopper können die persistente Warenkorbfunktion nicht verwenden.

## Workflow für persistenten Warenkorb

Wenn der persistente Warenkorb [aktiviert](#configure-a-persistent-cart) ist, hängt der Workflow von Folgendem ab:

- Die Werte der _[!UICONTROL Enable Remember Me]_- und_[!UICONTROL Clear Persistence on Log Out]_
- Die Entscheidung des Kunden, das Kontrollkästchen _[!UICONTROL Remember Me]_zu aktivieren oder zu deaktivieren
- Wenn das persistente Cookie gelöscht wird

Wenn die Kundensitzung abläuft, wird unter folgenden Bedingungen ein `Not Jane Smith?` Link in der Kopfzeile der Seite angezeigt:
- Der angemeldete Kunde hat die Option _[!UICONTROL Remember Me]_ausgewählt und ein persistentes Cookie wird angewendet
- Der Kunde meldet sich ab, wenn das System mit _[!UICONTROL Clear Persistence on Sign Out]_auf `No` konfiguriert ist.

Das System speichert die Warenkorbinhalte auf dem aktuellen Gerät, auch wenn die angemeldete Sitzung abläuft. Über den `Not Jane Smith?` Link kann der Kunde die persistente Sitzung beenden und als Gast arbeiten bzw. sich als anderer oder derselbe Kunde anmelden.

Wenn der Kunde beim Anmelden das Kontrollkästchen _[!UICONTROL Remember Me]_aktiviert hat, erstellt und verwaltet Ihr Store ein separates persistentes Cookie. Dieses Cookie hilft, den Warenkorb des Kunden auch dann zugänglich zu halten, wenn er den Browser schließt oder zu einer anderen Site navigiert und seine angemeldete Sitzung abläuft.

Wenn derselbe Kunde Ihren Shop über mehrere Browser besucht, während er angemeldet ist, oder eine persistente Sitzung aktiv ist, werden die Änderungen, die der Kunde in einem Browser am Warenkorbinhalt vornimmt, in anderen Browsern angezeigt, wenn die Seite aktualisiert wird.

>[!NOTE]
>
>Um eine Warenkorbsynchronisierung über mehrere Geräte oder Browser hinweg sicherzustellen, müssen sich Kunden auf jedem neuen Gerät anmelden, das sie für den Einkauf verwenden. Für angemeldete Kunden wird der Inhalt des Warenkorbs auf mehreren Geräten und Browsern synchronisiert, solange sie unter demselben Konto angemeldet sind. Die Konfiguration des persistenten Warenkorbs spielt dabei keine Rolle.

### Verhalten des Kontrollkästchens „Angaben speichern“

Kunden können das Kontrollkästchen _[!UICONTROL Remember Me]_auf der Anmeldeseite oder bei der Erstellung eines neuen Kontos aktivieren, um den Inhalt des Warenkorbs auf dem aktuellen Gerät verfügbar zu halten, wenn die angemeldete Sitzung abläuft.

| Mich erinnern? | Ergebnis |
| ------------ |  ------ |
| Ausgewählt | Erstellt ein persistentes Cookie und speichert den Inhalt des Warenkorbs auf dem aktuellen Gerät, wenn die Kundenanmeldesitzung abläuft. |
| Nicht ausgewählt | Erstellt kein persistentes Cookie und bewahrt den Inhalt des Warenkorbs nicht auf dem aktuellen Gerät auf, wenn die Anmeldesitzung abläuft. Beachten Sie, dass der Warenkorbinhalt weiterhin im Konto des Kunden gespeichert und bei der nächsten Anmeldung des Kunden neu geladen wird. |

{style="table-layout:auto"}

### Persistenz für Abmeldeverhalten löschen

Wenn sich der Kunde anmeldet oder sich mit der ausgewählten Option _Angaben speichern_ registriert, bestimmt die Konfiguration der Option _Persistenz beim Abmelden löschen_ das Verhalten des persistenten Warenkorbs.

|  | Löschen der Persistenz beim Abmelden mit der Einstellung „Ja“ | Persistenz bei auf „Nein“ festgelegter Abmeldung löschen |
| ------ | ------ | ------ |
| _Erinnert_ Kunde meldet sich ab | Löscht sowohl Sitzungs- als auch persistente Cookies, sodass der Warenkorbinhalt auf dem aktuellen Gerät ausgeblendet wird, bis sich derselbe Kunde wieder anmeldet. | Löscht das Sitzungs-Cookie, aber das persistente Cookie bleibt in Kraft. Der Warenkorbinhalt bleibt auf dem aktuellen Gerät verfügbar. |
| _Erinnert_ Kunde meldet sich nicht ab, aber das Sitzungs-Cookie läuft ab | Das persistente Cookie bleibt in Kraft und der Warenkorbinhalt ist vom aktuellen Gerät aus zugänglich. | Das persistente Cookie bleibt in Kraft und der Warenkorbinhalt ist vom aktuellen Gerät aus zugänglich. |

### Beispiel für eine offene Sitzung auf einem freigegebenen Computer

Jane beendet ihren Urlaubseinkauf als _erinnerte_ angemeldete Kundin. Sie fügt ein Geschenk für John in ihren Warenkorb und etwas für ihre Mutter. Anschließend geht sie für einen Snack in die Küche und ihre Anmeldesitzung läuft ab.

John setzt sich an den Computer, um schnell einzukaufen, während Jane in der Küche ist. Ohne den `Not Jane Smith?`-Link oben auf der Seite zu bemerken, findet John ein schönes Geschenk für Jane und fügt es zum Warenkorb hinzu. Wenn er auscheckt, bemerkt er, dass die Versand- und Rechnungsadressen vorausgefüllt sind und denkt, dass er angemeldet ist. John ist so in Eile, dass er die zusätzlichen Artikel bei der _nicht bemerkt_ und die Bestellung abgibt. Janes Warenkorb ist jetzt leer, und John kaufte alle Geschenke.

## Konfigurieren eines persistenten Warenkorbs

Bei der Einrichtung eines persistenten Warenkorbs können Sie die Lebensdauer der Cookies und die Optionen angeben, die Sie für verschiedene Kundenaktivitäten zur Verfügung stellen möchten.

Um den persistenten Warenkorb zu verwenden, muss der Browser des Kunden so eingestellt sein, dass Cookies erlaubt sind. Es gibt zwei Arten von Cookies, die für Warenkorboperationen verwendet werden:

- **Sitzungs-**: Ein kurzfristiges Sitzungs-Cookie ist während eines einzelnen Besuchs Ihrer Site vorhanden. Dieses Cookie läuft ab, wenn sich der Kunde abmeldet, oder wenn die Sitzung abläuft.

- **Persistentes Cookie** - Ein langfristiges, persistentes Cookie ist auch nach dem Ende der angemeldeten Sitzung weiterhin vorhanden. Dieses Cookie stellt sicher, dass der Inhalt des Warenkorbs eines Kunden verfügbar bleibt, wenn sich der Kunde abmeldet oder die Sitzung abläuft.

Weitere Informationen darüber, wie sich diese Konfigurationseinstellungen auf den Kunden-Workflow auswirken, finden Sie unter [Workflow für den Warenkorb](#persistent-cart-workflow).

{{$include /help/_includes/persistent-cart-configuration.md}}
