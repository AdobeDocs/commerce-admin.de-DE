---
title: Kartenkauf und -einlösung
description: Informieren Sie sich über den Lebenszyklus von Geschenkgutscheinen, die Sie in Ihrem Shop-Katalog einkaufen oder einlösen können.
exl-id: ecaa39aa-f504-4bfd-874b-12b44093c2a9
feature: Products, Gift
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 0%

---

# Kartenkauf und -einlösung

{{ee-feature}}

Geschenkgutscheine werden im Warenkorb ähnlich wie Gutscheine auf eine Bestellung angewendet. Während des Kassengangs gibt der Käufer den Gutscheincode ein, um einen Betrag von der Geschenkkarte auf den Kauf anzuwenden. Karteninhaber mit Kundenkonten können den Status und den Restbetrag im Konto-Dashboard überprüfen. Einzel- und Mehrfachgutscheine können verwendet werden, um eine Bestellung ganz oder teilweise zu bezahlen.

Der angewendete Geschenkkarten-Code kann angezeigt werden, indem Sie die Bestellung in _Admin_ öffnen. Dadurch können Sie den Code abrufen, um ihn bei Bedarf auf einer physischen Geschenkkarte zu platzieren. Bei Stornierung oder Rückerstattung eines Geschenkkartenauftrags müssen Sie das entsprechende Geschenkkartenkonto manuell kündigen. Sie können das Konto entweder vollständig löschen oder deaktivieren.

![Detail der Geschenkkarte im Warenkorb](./assets/storefront-gift-card-order-customer-account.png){width="700" zoomable="yes"}

Beispielsweise kann ein Kunde, der im Demo-Luma-Laden einkauft, entweder eine virtuelle oder eine physische Geschenkkarte erwerben.

**Virtuelle Geschenkkarte** - Eine virtuelle Geschenkkarte von Luma wird dem Empfänger per E-Mail mit einer optionalen Nachricht zugeschickt. Sie kann auf jeder der Luma-Websites eingelöst werden und läuft nie ab.

**Physikalische Geschenkkarte** - Eine Geschenkkarte von Luma wird in einem benutzerdefinierten Kunst-Mailer verpackt und kostenlos an den Empfänger gesendet. Es kann im Voraus produziert, mit eindeutigen Codes gekennzeichnet und im Geschäft, per Telefon oder auf einer der Websites der Familie Luma eingelöst werden. Es läuft nie ab.

**Kombinierte Geschenkkarte** - Eine kombinierte Geschenkkarte hat sowohl die Eigenschaften einer virtuellen als auch einer physischen Geschenkkarte. Eine kombinierte Geschenkkarte von Luma wird versandt und per E-Mail an den Empfänger verschickt. Die E-Mail und die Lieferadresse sind während des Kaufs der Geschenkkarte erforderlich. Es läuft nie ab.

## Lebenszyklus von Gift-Karten

1. **Der Kunde bestimmt den Geschenkkartenwert**.

   Der Kunde bestimmt den Wert der Geschenkkarte auf der Produktseite. Abhängig von der Konfiguration gibt es entweder ein Feld für feste Preise, eine Liste von Preisoptionen oder beides. Alle Beträge werden in der Währung angezeigt, die im Store verwendet wird.

1. **Der Kunde vervollständigt die Geschenkkarteninformationen**.

   Bei einer physischen Geschenkkarte gibt der Kunde den **Absendernamen** und den **Empfängernamen** ein. Bei virtuellen oder kombinierten Geschenkkarten gibt der Kunde auch die **Sender Email** und die **Empfänger-E-Mail** ein. Wenn der Kunde angemeldet ist, werden der Absendername (und gegebenenfalls die Absender-E-Mail-Adresse) automatisch in seinem Konto angegeben. Je nach Konfiguration kann der Kunde auch eine Nachricht an den Empfänger eingeben.

1. **Kunde schließt Checkout ab**.

   Die Geschenkkarte wird als Zeileneintrag im Warenkorb mit Details angezeigt, die den Namen des Absenders, Empfängers und der Nachricht (falls zutreffend) enthalten. Der mit der Geschenkkarte verbundene Betrag wird beim Hinzufügen zum Warenkorb in die Basiswährung des Stores konvertiert.

1. **Der Kunde erhält die Bestätigung der Bestellung**.

   Der Käufer der Geschenkkarte kann auf den Link in der Bestätigung klicken, um die Bestellung über sein Konto-Dashboard zu verfolgen.

1. **Empfänger erhält die Geschenkkarte**.

   Bei virtuellen oder kombinierten Geschenkkarten erhält der Empfänger eine E-Mail mit dem Code der Geschenkkarte, dem Namen des Absenders und gegebenenfalls der Nachricht. Wenn mehrere Geschenkkarten in einer Bestellung erworben werden und der Typ entweder virtuell oder kombiniert ist, werden alle entsprechenden Geschenkkarten-Codes in einer E-Mail an den Empfänger gesendet. Geschenkgutscheine können direkt an den Empfänger oder den Kunden versandt werden, der die Geschenkkarte dann persönlich an den Empfänger übergeben kann.

1. **Der Empfänger wendet eine Geschenkkarte auf den Kauf an**.

   Der Empfänger kauft einen Artikel in Ihrem Geschäft und wendet den Geschenkkartencode während des Kassengangs an. Jedes Mal, wenn eine Geschenkkarte beim Checkout angewendet wird, wird der Betrag in der Gesamtbestelleinheit angezeigt und von der Gesamtsumme abgezogen. Der volle Restbetrag jeder Geschenkkarte wird von der Gesamtsumme des Warenkorbs abgezogen. Wenn mehrere Geschenkkarten für einen Kauf verwendet werden, werden sie in aufsteigender Reihenfolge angewendet, beginnend mit der Karte mit dem kleinsten Restbetrag, bis alle angewendet werden oder die Gesamtsumme null ist. Erreicht die Gesamtsumme den Nullwert, erhält das letzte auf den Warenkorb angewendete Geschenkkartenkonto einen teilweisen Abzug. Alle Karten, die nicht in den Warenkorb gelegt wurden, erhalten keinen Saldoabzug. Die Beträge werden erst nach der Bestellung von den Geschenkgutscheinen abgezogen.

## Storefront-Erlebnis

Funktionsweise von Geschenkgutscheinen auf der Storefront:

- Der Gutscheincode kann im Warenkorb oder beim Checkout angewendet werden, um den Gesamtbetrag der Bestellung abzudecken.

- Im Katalog wird eine Geschenkkarte als eigenständiger Produkttyp präsentiert.

- Der Geschenkkartencode wird aktiviert, nachdem die Bestellung fakturiert wurde. Wenn die Bestellung nicht bezahlt wird, kann der empfangende Kunde die Geschenkkarte nicht benutzen.

- Konten für Geschenkcodes werden erstellt, um den Saldo eines bestimmten Gutscheins zu verfolgen. Ein Store-Administrator kann den Saldo manuell anpassen.

Der empfangende Kunde kann den Abschnitt _[!UICONTROL Gift Card]_seines Konto-Dashboards verwenden, um den Saldo seines [Geschenkkartekontos](product-gift-card-accounts.md) zu überprüfen und Geschenkkarten für [Kredit speichern](../customers/store-credit-using.md) einzulösen.

![Geschenkkarte](./assets/account-dashboard-gift-card.png){width="700" zoomable="yes"}

### Status und Saldo der Geschenkkarte prüfen

1. Über die Storefront meldet sich der Kunde an und öffnet die Seite seines Kundenkontos.

1. Der Kunde öffnet die Seite &quot;**[!UICONTROL Gift Card]**&quot; und gibt den Code der Geschenkkarte ein.

1. Der Kunde klickt auf **[!UICONTROL Check status and balance]**.

![Gift Card Balance](./assets/gift-balance.png){width="700" zoomable="yes"}

Der Restbetrag der Geschenkkarte wird angezeigt.

### Aktivierung der Giftkarte

1. Auf der Seite _[!UICONTROL Gift Card]_gibt der Kunde den Code der Geschenkkarte ein.

1. Der Kunde klickt auf **[!UICONTROL Redeem Gift Card]**.

![Meldung über die erfolgreiche Aktivierung der Geschenkkarte](./assets/gift-redeemed-balance.png){width="700" zoomable="yes"}

Der Betrag der Geschenkkarte wird aktiviert und zum Gesamtkonto des Geschäfts hinzugefügt.

![Guthabenkonto speichern](./assets/store-credit.png){width="700" zoomable="yes"}

Alle Vorgänge für den Restbetrag der Geschenkkarte sind auf der Seite _[!UICONTROL Store Credit]_verfügbar.

### Anwenden einer Geschenkkarte beim Auschecken

Wenn die Geschenkkarte nicht eingelöst werden kann, kann ein Kunde den Geschenkgutschein-Code während des Auscheckens anwenden.

1. Während des Schritts _Überprüfung und Zahlungen_ klickt der Kunde auf **[!UICONTROL Apply Gift Card]**.

1. Fügt den Code der Geschenkkarte ein und klickt dann auf **[!UICONTROL Apply]**.

   Der Rabatt sollte in den _[!UICONTROL Order Summary]_widergespiegelt werden.

1. Klicken Sie auf **[!UICONTROL Place Order]** , um die Bestellung abzuschließen.
