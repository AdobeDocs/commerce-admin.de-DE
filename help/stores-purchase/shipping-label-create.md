---
title: Erstellen von Versandbeschriftungen und Packages
description: Erfahren Sie, wie Sie Artikel in einer Bestellung verpacken und Versandbeschriftungen erstellen.
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '1889'
ht-degree: 0%

---

# Versandtitel erstellen

Um Versandbezeichnungen zu erstellen, müssen Sie zunächst Ihr Versandbetreiberkonto einrichten, um die Etiketten zu unterstützen. Folgen Sie dann den Anweisungen, um eine Beschreibung des Pakets und seiner Inhalte einzugeben.

Nachdem Sie die Versandbeschriftungen konfiguriert und eine Bestellung eingereicht haben, stellt Commerce eine Verbindung zum Versandunternehmen her, sendet eine Bestellung und erhält einen Versandtitel und eine Trackingnummer. Wenn im System ein Versandetikett für diese Sendung vorhanden ist, wird dieses durch ein neues ersetzt. Vorhandene Tracking-Zahlen werden jedoch nicht ersetzt. Jede neue Trackingnummer wird der vorhandenen hinzugefügt.

## Schritt 1: Kontaktieren Sie Ihre Versandunternehmen.

Bevor Sie beginnen, stellen Sie sicher, dass Ihre Versandkonten so eingerichtet sind, dass die Beschriftungen verarbeitet werden. Einige Fluggesellschaften berechnen möglicherweise eine zusätzliche Gebühr, um Ihrem Konto Versandtitel hinzuzufügen.

Wenden Sie sich an jeden Anbieter, den Sie zum Aktivieren von Versandbeschriftungen für Ihren Shop verwenden.

Befolgen Sie die Anweisungen der einzelnen Anbieter, um Ihrem Konto Unterstützung für Versandtitel hinzuzufügen.

- **FedEx** - Wenden Sie sich an [FedEx Web Integration Services][1] , um mehr über die Druckanforderungen für Ihr Konto zu erfahren.
- **USPS** - Im [Web Tools API Portal][4] des Shipper Support Center erfahren Sie, wie Sie Ihre Beschriftungsdruckberechtigungen einrichten.
- **UPS** - Wenden Sie sich an [UPS][2], um zu bestätigen, dass Ihr Konto Versandbeschriftungen unterstützt. Um Versandbezeichnungen zu erstellen, müssen Sie die UPS XML-Option verwenden.
- **DHL** - Kontaktieren Sie [DHL eCommerce Solutions][3] , um mehr über die Druckanforderungen für Ihr Konto zu erfahren.

## Schritt 2: Konfiguration für jeden Netzbetreiber aktualisieren

1. Stellen Sie sicher, dass Ihre [Store-Informationen](../getting-started/store-details.md#store-information) abgeschlossen sind.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Eintrag **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Shipping Settings]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Origin]** und konfigurieren Sie die **[!UICONTROL Shipping Origin Address]**.

1. Befolgen Sie die unten stehenden Anweisungen für jedes Betreiberkonto, das für den Beschriftungsdruck aktiviert ist.

### UPS-Konfiguration

United Parcel Service wird sowohl im Inland als auch international vertrieben. Die Erstellung von Versandbeschriftungen ist jedoch nur für Sendungen mit Ursprung in den USA möglich.

1. Wählen Sie im Abschnitt _[!UICONTROL Sales]_im linken Bereich die Option **[!UICONTROL Delivery Methods]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL UPS]** .

1. Überprüfen Sie, ob Ihr UPS **[!UICONTROL Shipper Number]** korrekt ist.

   Ihre Sendungsnummer wird nur angezeigt, wenn [!DNL United Parcel Service XML] aktiviert ist.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

### USPS-Konfiguration

Der [!DNL United States Postal Service] wird sowohl im Inland als auch international ausgeliefert.

1. Erweitern Sie in der **[!UICONTROL Delivery Methods]** -Konfiguration den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) für den Abschnitt **[!UICONTROL USPS]**.

1. Überprüfen Sie, ob die **[!UICONTROL Secure Gateway URL]** richtig ist.

1. Geben Sie die **[!UICONTROL Password]** ein, die Sie von USPS erhalten haben.

1. Setzen Sie **[!UICONTROL Size]** auf `Large` und geben Sie Werte für die folgenden Dimensionen ein:

   - Länge
   - Breite
   - Höhe
   - Mädchen

1. Klicken Sie auf **[!UICONTROL Save Config]**.

### FedEx-Konfiguration

FedEx ist international und national tätig. Geschäfte außerhalb der USA können FedEx-Etiketten nur für internationale Sendungen erstellen.

1. Erweitern Sie in der **[!UICONTROL Delivery Methods]** -Konfiguration den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) für den Abschnitt **[!UICONTROL FedEx]**.

1. Überprüfen Sie, ob die folgenden FedEx-Anmeldeinformationen korrekt sind:

   - Zähleranzahl
   - Schlüssel
   - Kennwort

1. Klicken Sie auf **[!UICONTROL Save Config]**.

### DHL-Konfiguration

DHL erbringt internationale Seeverkehrsdienstleistungen.

1. Erweitern Sie in der **[!UICONTROL Delivery Methods]** -Konfiguration den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) für den Abschnitt **[!UICONTROL DHL]**.

1. Überprüfen Sie, ob die **[!UICONTROL Gateway URL]** richtig ist.

1. Stellen Sie sicher, dass die folgenden Anmeldedaten abgeschlossen sind:

   - Zugriffs-ID
   - Kennwort
   - Kontonummer

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Schritt 3: Erstellen von Versandbeschriftungen

### Methode 1: Erstellen eines Etiketts für eine neue Sendung

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie die Reihenfolge im Raster und öffnen Sie den Datensatz.

   Der Status der Reihenfolge muss entweder `Pending` oder `Processing` lauten.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Ship]**.

1. Validieren Sie die Versandinformationen entsprechend den Beförderungsanforderungen.

1. Aktivieren Sie in der rechten unteren Ecke das Kontrollkästchen **[!UICONTROL Create Shipping Label]** .

1. Klicken Sie auf **[!UICONTROL Submit Shipment]**.

1. Hinzufügen oder Aktualisieren von Produkten im Paket:

   - Um Produkte aus der Bestellung zum Paket hinzuzufügen, klicken Sie auf **[!UICONTROL Add Products]**. Die Spalte &quot;_[!UICONTROL Quantity]_&quot; zeigt die maximale Anzahl von Produkten an, die für das Paket verfügbar sind.

   - Aktivieren Sie das Kontrollkästchen der einzelnen Produkte, die dem Paket hinzugefügt werden sollen, und geben Sie jeweils den Wert **[!UICONTROL Quantity]** ein. Klicken Sie dann auf **[!UICONTROL Add Selected Product(s) to Package]**.

   - Um ein Paket hinzuzufügen, klicken Sie auf **[!UICONTROL Add Package]**.

   - Um ein Paket zu löschen, klicken Sie auf **[!UICONTROL Delete Package]**.

   - Um eine Bestellung abzubrechen, klicken Sie auf **[!UICONTROL Cancel]**. Es wird kein Versandtitel erstellt und das Kontrollkästchen _[!UICONTROL Create Shipping Label]_wird deaktiviert.

   >[!NOTE]
   >
   >Wenn Sie einen anderen Pakettyp als den Standard verwenden oder eine Unterschrift benötigen, können die Versandkosten von dem abweichen, was Sie dem Kunden berechnet haben. Jegliche Unterschiede bei den Versandkosten spiegeln sich nicht in Ihrem Geschäft wider.

1. Klicken Sie auf **[!UICONTROL OK]**.

   Commerce stellt eine Verbindung zum Versandunternehmen her, sendet die Bestellung und erhält für jedes Paket einen Versandtitel und eine Trackingnummer.

### Methode 2: Erstellung eines Etiketts für eine bestehende Verbringung

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Suchen Sie die Bestellung im Raster und öffnen Sie das Versandformular.

1. Klicken Sie im Abschnitt _[!UICONTROL Shipping and Tracking Information]_auf **[!UICONTROL Create Shipping Label]**.

1. Verteilen Sie die bestellten Produkte in die entsprechenden Packages und klicken Sie auf **[!UICONTROL OK]**.

1. Um die Paketinformationen zu überprüfen, klicken Sie auf **[!UICONTROL Show Packages]**.

## Schritt 4: Drucken der Beschriftungen

Versandtitel werden im PDF-Format generiert und können vom Administrator gedruckt werden. Jeder Titel enthält die Bestellnummer und die Paketnummer.

>[!NOTE]
>
>Da für jedes Paket ein individueller Versandauftrag erstellt wird, können mehrere Versandtitel für eine einzelne Sendung empfangen werden.

### Methode 1: Drucketikett aus dem Versandformular

1. Wechseln Sie auf der _Admin-Seitenleiste_ zu einer der folgenden Seiten und suchen Sie dann den Versanddatensatz:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Suchen Sie die Reihenfolge im Raster und öffnen Sie den Datensatz. Wählen Sie im linken Bereich **[!UICONTROL Shipments]** aus. Öffnen Sie dann den Versanddatensatz.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Suchen Sie die Sendung im Raster und öffnen Sie den Datensatz.

1. Um die PDF-Datei herunterzuladen, gehen Sie zum Abschnitt _[!UICONTROL Shipping and Tracking]_des Formulars und klicken Sie auf **[!UICONTROL Print Shipping Label]**.

   Je nach Browsereinstellungen können die Versandtitel direkt über die PDF-Datei angezeigt und gedruckt werden.

   Die Schaltfläche _[!UICONTROL Print Shipping Label]_erscheint erst, nachdem der Träger Beschriftungen für die Sendung generiert hat. Wenn die Schaltfläche fehlt, klicken Sie auf **[!UICONTROL Create Shipping Label]**. Die Schaltfläche wird angezeigt, nachdem Commerce die Beschriftung vom Netzbetreiber erhalten hat.

### Methode 2: Druckbeschriftungen für mehrere Bestellungen

1. Wechseln Sie auf der _Admin-Seitenleiste_ zu einer der folgenden Seiten und wählen Sie dann die zu druckenden Bestellungen oder Sendungen aus:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Aktivieren Sie im Raster das Kontrollkästchen der einzelnen Bestellungen, deren Versandbezeichnungen gedruckt werden sollen.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Aktivieren Sie im Raster das Kontrollkästchen jeder Sendung mit den zu druckenden Bezeichnungen.

1. Setzen Sie das Steuerelement **[!UICONTROL Actions]** auf `Print Shipping Labels`.

1. Klicken Sie auf **[!UICONTROL Submit]**.

Für jede Sendung, die sich auf die ausgewählten Bestellungen bezieht, wird ein kompletter Satz von Versandetiketten gedruckt.

## Erforderliche Trägereinstellungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Type] | Pakettypen unterscheiden sich je nach Träger und Methode. Der Standard-Pakettyp für jeden Netzbetreiber wird zunächst ausgewählt. USPS benötigt den Pakettyp nicht für inländische Sendungen. |
| [!UICONTROL Customs Value] | (Nur internationale Sendungen) Der angegebene Wert oder Verkaufspreis des Inhalts einer internationalen Lieferung. |
| [!UICONTROL Total Weight] | Die Gesamtgewichtung aller Produkte, die der Verpackung hinzugefügt werden, wird automatisch berechnet. Der Wert kann auch manuell geändert und als Pfund oder Kilogramm angegeben werden. |
| [!UICONTROL Length, Width, Height] | (Optional) Die Paketdimensionen werden nur für benutzerdefinierte Pakete verwendet. Sie können die Maßeinheiten als Zoll oder Zentimeter angeben.<br/><br/>**[!UICONTROL Not Required]**: Der Versandverantwortliche bestätigt nicht, dass der Versand an den Laden erfolgt.<br/><br/>**[!UICONTROL No Signature]**: Eine Versandbestätigung ohne Unterschrift des Empfängers wird vom Versandunternehmen an den Speicher gesendet.<br/><br/>**[!UICONTROL Signature Required]**: Das Versandunternehmen erhält die Unterschrift des Empfängers und stellt dem Geschäft eine gedruckte Kopie zur Verfügung.<br/><br/>**[!UICONTROL Direct]**: (Nur FedEx) FedEx erhält eine Signatur von einer Person an der Lieferadresse. Wenn niemand für das Paket signiert werden kann, versucht der Netzbetreiber, das Paket zu einem anderen Zeitpunkt bereitzustellen.<br/><br/>**[!UICONTROL Indirect]**: (Nur FedEx-Wohnungslieferungen) Der FedEx erhält die Unterschrift einer Person (möglicherweise eines Nachbarn oder Gebäudemanagers) an der Lieferadresse. Der Empfänger kann ein signiertes FedEx-Türtag hinterlassen, um zu erlauben, dass das Paket verlassen bleibt, ohne dass jemand anwesend ist, um es zu unterschreiben.<br/><br/>**[!UICONTROL Contents]**: (Nur USPS) Wählen Sie eine der folgenden Beschreibungen des Pakets aus:<br/>- Gift<br/>- Documents<br/>- Commercial Sample<br/>- Returned Goods<br/>- Merchandise<br/>- Other <br/><br/>**[!UICONTROL Explanation]**: (Nur USPS) Eine detaillierte Beschreibung des Paketinhalts.<br/><br/>**[!UICONTROL Adult Required]**: Das Versandunternehmen erhält die Unterschrift eines erwachsenen Empfängers und stellt dem Geschäft eine gedruckte Kopie zur Verfügung. |

{style="table-layout:auto"}

## Pakete erstellen

Das Fenster _[!UICONTROL Create Packages]_wird angezeigt, wenn Sie eine Versandbeschriftung erstellen. Sie können sofort mit der Konfiguration des ersten Pakets beginnen.

### Package konfigurieren

>[!NOTE]
>
>Wenn Sie den nicht standardmäßigen Wert für die [!UICONTROL Type] auswählen oder eine Signaturbestätigung verlangen, kann der Preis einer Sendung von dem Preis abweichen, den Sie dem Kunden in Rechnung gestellt haben.

1. Um eine Liste der gelieferten Produkte anzuzeigen und sie zum Paket hinzuzufügen, klicken Sie auf **[!UICONTROL Add Products]**.

   - Geben Sie die Erzeugnisse und Mengen an.

     In der Spalte _[!UICONTROL Qty]_wird die maximal hinzuzufügende Menge angezeigt. Bei der ersten Verpackung entspricht die Zahl der Gesamtmenge des zu versendenden Erzeugnisses.

   - Um die Produkte zum Paket hinzuzufügen, klicken Sie auf **[!UICONTROL Add Selected Product(s) to Package]**.

1. Um ein Paket hinzuzufügen, klicken Sie auf **[!UICONTROL Add Package]**.

   Sie können mehrere Pakete hinzufügen und sie gleichzeitig bearbeiten.

1. Um ein Paket zu löschen, klicken Sie auf **[!UICONTROL Delete Package]**.

Nachdem Produkte zum Package hinzugefügt wurden, kann die Menge nicht direkt bearbeitet werden.

### Menge erhöhen

1. Klicken Sie auf **[!UICONTROL Add Selection]**.

1. Geben Sie die zusätzliche Menge ein.

   Die Nummer wird der vorherigen Menge des Erzeugnisses in der Verpackung hinzugefügt.

### Menge verringern

1. Löschen Sie das Produkt aus dem Paket.

1. Klicken Sie auf **[!UICONTROL Add Selection]**.

1. Geben Sie den neuen, kleineren Wert ein.

### Versandtitel generieren

Nachdem Sie alle Produkte verteilt haben, entspricht die Gesamtzahl der Pakete, die Sie verwenden werden, der Anzahl des letzten Pakets in der Liste. Die Schaltfläche _OK_ ist deaktiviert, bis alle ausgelieferten Elemente in Packages verteilt sind und alle erforderlichen Informationen vollständig sind.

Um die Beschriftungen zu generieren, klicken Sie auf **[!UICONTROL OK]**.

Sie können bei Bedarf auf **[!UICONTROL Cancel]** klicken, um den Prozess zu stoppen. Die Pakete werden nicht gespeichert und der Versandbeschriftungsprozess wird abgebrochen.

### Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Type] | Gibt den Pakettyp an. Wählen Sie einen der vordefinierten Werte aus. Die verfügbaren Pakettypen unterscheiden sich je nach Versandunternehmen. Wenn das Popup-Fenster Pakete erstellen geöffnet wird, wird im Feld Typ das Standardpaket für den Versandunternehmen angezeigt. Wenn Sie ein Package auswählen, das nicht von einem Versandunternehmen entwickelt wurde, müssen Sie die Abmessungen des Pakets angeben. Für Versandbeschriftungen, die für DHL-, FedEx- und UPS-Sendungen erstellt wurden, ist das Feld &quot;Warentyp&quot;auf `Merchandise` eingestellt. Bei USPS spiegelt das Feld den Wert aus dem Feld _Inhalt_ im Fenster _[!UICONTROL Create Packages]_wider. |
| [!UICONTROL Total Weight] | Die Gesamtgewichtung eines Packages. Das Feld wird vorab mit der Gesamtgewichtung der Produkte in einem Package ausgefüllt. Die Maßeinheit kann entweder auf Pfund oder Kilogramm eingestellt werden. |
| [!UICONTROL Length] | Die Länge eines Pakets, einer Ganzzahl und von Gleitkommazahlen. Das Feld wird aktiviert, wenn der benutzerdefinierte Pakettyp verwendet wird. Die Maßeinheit kann entweder auf Zoll oder Zentimeter eingestellt werden. |
| [!UICONTROL Width] | Die Breite von Paketen, Ganzzahlen und Gleitkommazahlen. Das Feld wird aktiviert, wenn der benutzerdefinierte Pakettyp verwendet wird. Die Maßeinheiten können über das Dropdown-Menü neben dem Feld Höhe angegeben werden. Wählen Sie zwischen Zoll und Zentimetern aus. |
| [!UICONTROL Height] | Die Höhe von Paket-, Integer- und Gleitkommazahlen. Das Feld wird aktiviert, wenn der benutzerdefinierte Pakettyp verwendet wird. Die Maßeinheiten können über das Dropdown-Menü neben dem Feld Höhe angegeben werden. Wählen Sie zwischen Zoll und Zentimetern aus. |
| [!UICONTROL Signature] | Definiert die Versandbestätigung. Optionen:<br/><br/>**[!UICONTROL Not Required]**: Sie erhalten keinen Zustellbestätigungsbrief.<br/><br/>**[!UICONTROL No Signature]**: Ein Versand-Bestätigungsbrief ohne Unterschrift eines Empfängers wird an Sie gesendet.<br/><br/>**[!UICONTROL Signature Required]**: Das Versandunternehmen erhält die Unterschrift des Empfängers und stellt Ihnen die gedruckte Kopie zur Verfügung.<br/><br/>**[!UICONTROL Adult Required]**: Der Versandunternehmen erhält die Unterschrift des Erwachsenenempfängers und stellt Ihnen die gedruckte Kopie zur Verfügung.<br/><br/>**[!UICONTROL Direct (FedEx only)]**: FedEx erhält eine Signatur von einer Person an der Lieferadresse und versucht erneut, die Bereitstellung durchzuführen, wenn niemand für das Paket unterschrieben werden kann.<br/><br/>**[!UICONTROL Indirect (FedEx only)]**: FedEx erhält eine Unterschrift auf eine von drei Arten: <br/>(1) von einer Person an der Lieferadresse; <br/>(2) von einem Nachbarn, Gebäudemanager oder einer anderen Person an der Adresse; oder <br/>(3) der Empfänger kann einen signierten FedEx-Türtag verlassen, der die Freigabe des Pakets genehmigt, ohne dass jemand anwesend ist. Nur für den Versand von Wohngebäuden verfügbar. Die Optionen können bei verschiedenen Versandmethoden leicht variieren. Aktuelle Informationen finden Sie in den Ressourcen des Versandunternehmens. |
| [!UICONTROL Contents] | (Nur für USPS-Sendungen verfügbar) Beschreibung des Paketinhalts. Optionen: `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | (Nur USPS-Sendungen) Detaillierte Beschreibung des Paketinhalts. |

{style="table-layout:auto"}

[1]: https://www.fedex.com/en-us/api/get-support.html
[2]: https://www.ups.com/us/en/support/contact-us.page
[3]: https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html
[4]: https://www.usps.com/business/web-tools-apis/#ssc
