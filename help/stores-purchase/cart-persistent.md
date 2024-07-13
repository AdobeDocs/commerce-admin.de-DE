---
title: Warenkorbpersistenz
description: Erfahren Sie, wie ein beständiger Warenkorb nicht gekaufte Artikel verfolgt und die Informationen für den nächsten Besuch des Kunden speichert.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: 26d4bb35c6e1878a8ea8c5f05a982559e5d6dc35
workflow-type: tm+mt
source-wordcount: '1475'
ht-degree: 0%

---

# Warenkorbpersistenz

Ein beständiger Warenkorb verfolgt nicht gekaufte Artikel, die noch im Warenkorb sind, und speichert die Informationen für den nächsten Besuch des Kunden. Kunden, die _an_ erinnern, können den Inhalt ihres Warenkorbs beim nächsten Besuch in Ihrem Geschäft wiederherstellen lassen.

Die Verwendung eines beständigen Warenkorbs kann dazu beitragen, die Anzahl der abgebrochenen Warenkörbe zu reduzieren und den Umsatz zu steigern. Es ist wichtig zu verstehen, dass der beständige Warenkorb zu keinem Zeitpunkt sensible Kontoinformationen anzeigt. Während der beständige Warenkorb verwendet wird, müssen sich sowohl registrierte Kunden als auch Gastkäufer entweder bei einem vorhandenen Konto anmelden oder ein Konto erstellen, bevor sie zum Checkout gehen. Für Gastkäufer ist ein beständiger Warenkorb die einzige Möglichkeit, Informationen aus einer vorherigen Sitzung abzurufen.

Um die Verwendung der Warenkorbpersistenz für Ihre Site oder in bestimmten Store-Ansichten zu verwalten, können Sie [persistente Warenkorbeinstellungen konfigurieren](#configure-a-persistent-cart). Weitere Informationen dazu, wie sich diese Einstellungen auf das Kundenerlebnis in Ihrer Storefront auswirken, finden Sie unter [Workflow für beständigen Warenkorb](#persistent-cart-workflow).

>[!NOTE]
>
>Bei Verwendung eines persistenten Warenkorbs wird empfohlen, die Lebensdauer der Serversitzung und des Sitzungs-Cookies auf einen langen Zeitraum festzulegen. Weitere Informationen finden Sie unter [Sitzungslebensdauer](../customers/customer-online-options.md) .

Um den beständigen Warenkorb zu verwenden, muss der Browser des Kunden so eingestellt sein, dass Cookies zugelassen werden. Es gibt zwei Arten von Cookies, die für Warenkorbvorgänge verwendet werden:

- **Sitzungs-Cookie** - Ein kurzfristiges Sitzungs-Cookie ist während eines einzelnen Besuchs auf Ihrer Site vorhanden und läuft ab, wenn der Kunde die Site verlässt oder nach einem bestimmten Zeitraum.

- **Persistentes Cookie** - Ein langfristiges, beständiges Cookie besteht nach Ende der Sitzung weiter und speichert einen Datensatz mit den Warenkorbinhalten des Kunden, um ihn später erneut darauf hinzuweisen.

## Workflow für beständigen Warenkorb

Wenn der beständige Warenkorb [aktiviert](#configure-a-persistent-cart) ist, hängt der Workflow von Folgendem ab:

- Die Werte der Einstellungen _Enable Merken Me_ und _Clear Persistence on Log Out_
- Die Entscheidung des Kunden, das Kontrollkästchen _Angaben speichern_ auszuwählen oder zu deaktivieren
- Wenn das persistente Cookie gelöscht wird

Wenn ein beständiges Cookie angewendet wird, wird im Seitenkopf ein `Not Jane Smith?` -Link angezeigt. Mit dieser Aufforderung kann der Kunde die persistente Sitzung beenden und als Gast arbeiten oder sich als anderer Kunde anmelden. Das System speichert einen Datensatz mit den Inhalten des Warenkorbs, auch wenn der Kunde später verschiedene Geräte verwendet, um in Ihrem Geschäft einzukaufen. Beispielsweise kann ein Kunde einen Artikel von einem Laptop zum Warenkorb hinzufügen, weitere Artikel von einem Mobilgerät hinzufügen und den Checkout-Prozess von einem Tablet abschließen.

Für jeden Browser gibt es ein separates unabhängiges beständiges Cookie. Wenn der Kunde während einer einzelnen persistenten Sitzung mehrere Browser verwendet, während er Ihren Store besucht, werden Änderungen, die in einem Browser vorgenommen wurden, bei einer Seitenaktualisierung in einem anderen Browser übernommen. Während der beständige Warenkorb aktiviert ist, erstellt und verwaltet Ihr Store ein separates beständiges Cookie für jeden Browser, der von einem Kunden zum Anmelden oder Erstellen eines Kontos verwendet wird.

### Beispiel: Eine offene Sitzung auf einem freigegebenen Computer

Jane schließt ihren Urlaubseinkauf mit einer anhaltenden Sitzung ab. Sie fügt John ein Geschenk zum Warenkorb und etwas für ihre Mutter hinzu. Dann geht sie zum Imbiss in die Küche.

John sitzt am Computer, um schnell einkaufen zu können, während Jane in der Küche ist. Ohne den `Not Jane Smith?` -Link oben auf der Seite zu sehen, findet er ein schönes Geschenk für Jane und fügt es zum Warenkorb hinzu. Wenn er zum Checkout geht und sich wie sich selbst anmeldet, werden beide Artikel im Warenkorb von Jane in seinen Warenkorb gelegt. John hat es so eilig, dass er die zusätzlichen Elemente während der _Bestellprüfung_ nicht bemerkt und die Bestellung sendet. Janes Warenkorb ist jetzt leer, und John kaufte alle Geschenke.

### Angaben speichern

Kunden können auf der Anmeldeseite das Kontrollkästchen _Angaben speichern_ aktivieren, um den Inhalt ihres Warenkorbs zu speichern.

| Erinnern Sie sich an mich? | Ergebnis |
| ------------ |  ------ |
| Ausgewählt | Erstellt ein beständiges Cookie und speichert den Inhalt des Warenkorbs für die nächste angemeldete Sitzung des Kunden. |
| Nicht ausgewählt | Erstellt kein beständiges Cookie und speichert die Warenkorbinformationen nicht für die nächste angemeldete Sitzung des Kunden. |

{style="table-layout:auto"}

### Beibehalten beim Abmelden - nein

| Aktion | Ergebnis |
| ------ | ------ |
| Kundenanmeldung | Ruft das persistente Cookie zusätzlich zum Sitzungs-Cookie auf, das bereits verwendet wird. |
| Kunden meldet sich ab | Löscht das Sitzungs-Cookie, aber das beständige Cookie bleibt in Kraft. Wenn sich der Kunde das nächste Mal anmeldet, werden die Warenkorbelemente wiederhergestellt oder zu neuen Artikeln hinzugefügt, die im Warenkorb platziert wurden. |
| Der Kunde meldet sich nicht ab und das Sitzungs-Cookie läuft ab | Das beständige Cookie bleibt in Kraft. |

{style="table-layout:auto"}

### Löschen der Persistenz beim Abmelden

| Aktion | Ergebnis |
| ------ | ------ |
| Kundenanmeldung | Ruft das persistente Cookie zusätzlich zum Sitzungs-Cookie auf, das bereits verwendet wird. |
| Kunden meldet sich ab | Löscht beide Cookies. |
| Der Kunde meldet sich nicht ab, aber das Sitzungs-Cookie läuft ab | Das beständige Cookie bleibt in Kraft. |

{style="table-layout:auto"}

## Persistente Warenkorbeinstellungen und -effekte

| Einstellungen | Effekt |
|----------|--------|
| **[!UICONTROL Enable Remember Me]** ist auf `No` gesetzt.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**hat einen beliebigen Wert.<br/><br/>Das Kontrollkästchen** Angaben speichern **ist auf der Anmelde- und Registrierungsseite nicht verfügbar. | Das persistente Cookie wird nicht verwendet. |
| **[!UICONTROL Enable Remember Me]** ist auf `Yes` gesetzt.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**hat einen beliebigen Wert.<br/><br/>** Angaben speichern **ist nicht ausgewählt. | Das Sitzungs-Cookie wird wie gewohnt angewendet. Das persistente Cookie wird nicht verwendet. |
| **[!UICONTROL Enable Remember Me]** ist auf `Yes` gesetzt.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**ist auf `Yes` gesetzt.<br/><br/>** Angaben speichern **ist auf `Yes` gesetzt. | Wenn sich ein Kunde anmeldet, werden beide Cookies angewendet. Wenn sich ein Kunde abmeldet, werden beide Cookies gelöscht. Wenn sich ein Kunde nicht anmeldet, das Sitzungs-Cookie jedoch abläuft, wird weiterhin das persistente Cookie verwendet. Abgesehen von der Abmeldung wird das persistente Cookie gelöscht, wenn seine Lebensdauer abgelaufen ist oder der Kunde auf den Link `Not Jane Smith` klickt. |
| **[!UICONTROL Enable Remember Me]** ist auf `Yes` gesetzt.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**ist auf `No` gesetzt.<br/><br/>** Angaben speichern **ist auf `Yes` gesetzt | Wenn sich ein Kunde anmeldet, werden beide Cookies angewendet. Wenn sich ein Kunde abmeldet, wird das Sitzungs-Cookie gelöscht, die persistente Sitzung wird fortgesetzt. Das persistente Cookie wird gelöscht, wenn seine Lebensdauer abgelaufen ist oder der Kunde auf den Link `Not Jane Smith` klickt. |

{style="table-layout:auto"}

## Persistenten Warenkorb konfigurieren

Bei der Einrichtung eines beständigen Warenkorbs können Sie die Lebensdauer der Cookies und die Optionen festlegen, die Sie für verschiedene Kundenaktivitäten verfügbar machen möchten.

Weitere Informationen dazu, wie der Kunden-Workflow durch diese Einstellungen bestimmt wird, finden Sie unter [Workflow für den beständigen Warenkorb](#persistent-cart-workflow).

>[!NOTE]
>
>Wenn das Sitzungs-Cookie abläuft, während der Kunde angemeldet ist, bleibt das persistente Cookie aktiv.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Persistent Shopping Cart]** aus.

1. Um den beständigen Warenkorb zu aktivieren und zusätzliche Optionen anzuzeigen, setzen Sie **[!UICONTROL Enable Persistence]** auf `Yes`.

   ![Aktivieren und Konfigurieren der Warenkorbspersistenz](../configuration-reference/customers/assets/persistent-shopping-cart-general.png){width="600" zoomable="yes"}

   Weitere Informationen zu den einzelnen Konfigurationseinstellungen finden Sie in der [_Konfigurationsreferenz_](../configuration-reference/customers/persistent-shopping-cart.md)

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Einstellungen zu ändern.

1. Geben Sie für &quot;**[!UICONTROL Persistence Lifetime (seconds)]**&quot;die Dauer in Sekunden ein, für die das persistente Cookie beibehalten werden soll.

   Der Standardwert von 31.536.000 Sekunden ist gleich einem Jahr. Die maximal zulässige Zeit beträgt 100 Jahre.

1. Setzen Sie **[!UICONTROL Enable "Remember Me"]** auf einen der folgenden Werte:

   - `Yes` - Zeigt das Kontrollkästchen _Angaben speichern_ auf der Anmeldeseite Ihres Stores an, damit Kunden ihre Warenkorbinformationen speichern können.

   - `No` - Die Persistenz kann weiterhin aktiviert werden, Kunden können jedoch nicht auswählen, ob sie ihre Informationen speichern möchten.

1. Um das Kontrollkästchen _Angaben speichern_ für den Kunden vorab zu aktivieren, setzen Sie **[!UICONTROL Remember Me Default Value]** auf `Yes`.

   Der Kunde kann diese Option bei Wahl löschen.

1. Setzen Sie **[!UICONTROL Clear Persistence on Log Out]** auf einen der folgenden Werte:

   - `Yes` - Der Warenkorb wird gelöscht, wenn sich ein registrierter Kunde abmeldet.

   - `No` - Der Warenkorb wird gespeichert, wenn sich ein registrierter Kunde abmeldet.

   >[!NOTE]
   >
   >Wenn das Sitzungs-Cookie abläuft, während der Kunde noch angemeldet ist, bleibt das persistente Cookie in Verwendung.

1. Setzen Sie **[!UICONTROL Persist Shopping Cart]** auf einen der folgenden Werte:

   - `Yes` - Wenn das Sitzungs-Cookie abläuft, wird das persistente Cookie beibehalten. Wenn sich ein Gastkäufer später anmeldet oder ein Konto erstellt, wird der Warenkorb wiederhergestellt.

   - `No` - Der Warenkorb wird für Gäste nach Ablauf des Sitzungs-Cookies nicht beibehalten.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Legen Sie **[!UICONTROL Persist Wish List]** fest, um zu bestimmen, ob der Status der Kundenwunschlisten beim Beenden der Sitzung beibehalten wird:

   - `Yes` - Der Inhalt der Wunschliste wird gespeichert, wenn die Sitzung beendet wird.

   - `No` - Die Wunschliste wird nicht gespeichert, wenn die Sitzung beendet wird.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Legen Sie **[!UICONTROL Persist Recently Ordered Items]** fest, um zu bestimmen, ob der Status der kürzlich sortierten Elemente beibehalten wird, wenn die Sitzung beendet wird:

   - `Yes` - Der Status der zuletzt sortierten Elemente wird gespeichert, wenn die Sitzung beendet wird.

   - `No` - Der Status der zuletzt sortierten Elemente wird nicht gespeichert, wenn die Sitzung beendet wird.

1. Setzen Sie **[!UICONTROL Persist Currently Compared Products]** auf `Yes` oder `No`.

1. Setzen Sie **[!UICONTROL Persist Comparison History]** auf `Yes` oder `No`.

1. Setzen Sie **[!UICONTROL Persist Recently Viewed Products]** auf `Yes` oder `No`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Legen Sie **[!UICONTROL Persist Customer Group Membership and Segmentation]** fest, um zu bestimmen, ob der Status der Gruppenmitgliedschaft und Segmentierungskriterien des Kunden beim Beenden der Sitzung beibehalten wird:

   - `Yes` - Der Status der Gruppenmitgliedschafts- und Segmentierungsdaten des Kunden wird gespeichert, wenn die Sitzung beendet wird.

   - `No` - Der Status der Gruppenmitgliedschaft und Segmentierungsdaten des Kunden werden nicht gespeichert, wenn die Sitzung beendet wird.

1. Klicken Sie auf **[!UICONTROL Save Config]**.
