---
title: Erstellen von Versandkennzeichnungen und -paketen
description: Erfahren Sie, wie Sie Artikel in einer Bestellung verpacken und Versandkennzeichnungen erstellen.
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '1889'
ht-degree: 0%

---

# Erstellen von Versandkennzeichnungen

Um Versandkennzeichnungen zu erstellen, müssen Sie zunächst Ihr Spediteurkonto für die Unterstützung von Kennzeichnungen einrichten. Folgen Sie dann den Anweisungen, um eine Beschreibung des Pakets und seines Inhalts einzugeben.

Nachdem Sie die Informationen zur Versandkennzeichnung konfiguriert und eine Bestellung gesendet haben, stellt Commerce eine Verbindung mit dem System der Versanddienstleister her, sendet eine Bestellung und erhält eine Versandkennzeichnung und eine Tracking-Nummer. Wenn im System ein Versandaufkleber für diese Sendung vorhanden ist, wird dieses durch ein neues ersetzt. Vorhandene Tracking-Nummern werden jedoch nicht ersetzt. Jede neue Tracking-Nummer wird der bestehenden Nummer hinzugefügt.

## Schritt 1: Spediteure kontaktieren

Bevor Sie beginnen, stellen Sie sicher, dass Ihre Versandkonten für die Verarbeitung von Beschriftungen eingerichtet sind. Einige Spediteure berechnen möglicherweise eine zusätzliche Gebühr, um Ihrem Konto Versandaufkleber hinzuzufügen.

Kontaktieren Sie jeden Spediteur, den Sie verwenden, um Versandkennzeichnungen für Ihren Shop zu aktivieren.

Befolgen Sie die Anweisungen der einzelnen Spediteure, um Ihrem Konto Support für Versandkennzeichnungen hinzuzufügen.

- **FedEx** - Kontakt [FedEx Web Integration Services][1] Erfahren Sie mehr über die Anforderungen für den Etikettendruck für Ihr Konto.
- **USPS** - Siehe [Web-Tools-API-Portal][4] im Shipper Support Center erfahren Sie, wie Sie Ihre Anmeldedaten für den Etikettendruck einrichten.
- **USV**- Kontakt [USV][2] um zu bestätigen, dass Ihr Konto Versandkennzeichnungen unterstützt. Um Versandkennzeichnungen zu generieren, müssen Sie die UPS XML-Option verwenden.
- **DHL** - Kontakt [DHL eCommerce-Lösungen][3] Erfahren Sie mehr über die Anforderungen für den Etikettendruck für Ihr Konto.

## Schritt 2: Konfiguration für jeden Provider aktualisieren

1. Stellen Sie sicher, dass Ihre [Informationen speichern](../getting-started/store-details.md#store-information) ist abgeschlossen.

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich . **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Shipping Settings]**.

1. Expand ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL Origin]** -Abschnitt erstellen und konfigurieren **[!UICONTROL Shipping Origin Address]**.

1. Befolgen Sie die nachstehenden Anweisungen für jedes Provider-Konto, das für den Etikettendruck aktiviert ist.

### USV-Konfiguration

United Parcel Service versendet sowohl im In- als auch im Ausland. Versandetiketten können jedoch nur für Sendungen generiert werden, die ihren Ursprung in den USA haben.

1. In der _[!UICONTROL Sales]_im linken Bereich auswählen **[!UICONTROL Delivery Methods]**.

1. Expand ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL UPS]** -Abschnitt.

1. Überprüfen Sie, ob Ihre USV **[!UICONTROL Shipper Number]** ist richtig.

   Ihre Absendernummer wird nur angezeigt, wenn [!DNL United Parcel Service XML] ist aktiviert.

1. Klick **[!UICONTROL Save Config]**.

### USPS-Konfiguration

Die [!DNL United States Postal Service] Schiffe sowohl im Inland als auch international.

1. Weiter in der **[!UICONTROL Delivery Methods]** Konfiguration, erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL USPS]** -Abschnitt.

1. Überprüfen Sie, ob die **[!UICONTROL Secure Gateway URL]** ist richtig.

1. Geben Sie die **[!UICONTROL Password]** von USPS für Sie bereitgestellt.

1. set **[!UICONTROL Size]** bis `Large` und geben Sie Werte für die folgenden Dimensionen ein:

   - Länge
   - Breite
   - Höhe
   - Umfang

1. Klick **[!UICONTROL Save Config]**.

### FedEx-Konfiguration

FedEx versendet national und international. Geschäfte außerhalb der USA können nur FedEx-Labels für internationale Sendungen erstellen.

1. Weiter in der **[!UICONTROL Delivery Methods]** Konfiguration, erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL FedEx]** -Abschnitt.

1. Überprüfen Sie, ob die folgenden FedEx-Anmeldeinformationen korrekt sind:

   - Zählernummer
   - Schlüssel
   - Kennwort

1. Klick **[!UICONTROL Save Config]**.

### DHL-Konfiguration

DHL erbringt internationale Versanddienstleistungen.

1. Weiter in der **[!UICONTROL Delivery Methods]** Konfiguration, erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL DHL]** -Abschnitt.

1. Überprüfen Sie, ob die **[!UICONTROL Gateway URL]** ist richtig.

1. Vergewissern Sie sich, dass die folgenden Anmeldeinformationen vollständig sind:

   - Zugriffs-ID
   - Kennwort
   - Kontonummer

1. Klick **[!UICONTROL Save Config]**.

## Schritt 3: Erstellen Sie Versandkennzeichnungen

### Methode 1: Kennzeichnung für neue Sendung erstellen

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie die Reihenfolge im Raster und öffnen Sie den Datensatz.

   Der Status der Bestellung muss entweder `Pending` oder `Processing`.

1. Klicken Sie oben rechts auf **[!UICONTROL Ship]**.

1. Bestätigen Sie die Versandinformationen entsprechend den Anforderungen des Spediteurs.

1. Wählen Sie in der rechten unteren Ecke **[!UICONTROL Create Shipping Label]** Kontrollkästchen.

1. Klick **[!UICONTROL Submit Shipment]**.

1. Hinzufügen oder Aktualisieren von Produkten im Paket:

   - Um Produkte aus der Bestellung zum Paket hinzuzufügen, klicken Sie auf **[!UICONTROL Add Products]**. Die _[!UICONTROL Quantity]_Spalte zeigt die maximale Anzahl von Produkten an, die für das Paket verfügbar sind.

   - Aktivieren Sie das Kontrollkästchen jedes Produkts, das dem Paket hinzugefügt werden soll, und geben Sie Folgendes ein **[!UICONTROL Quantity]** von jedem. Klicken Sie anschließend auf **[!UICONTROL Add Selected Product(s) to Package]**.

   - Um ein Paket hinzuzufügen, klicken Sie auf **[!UICONTROL Add Package]**.

   - Um ein Paket zu löschen, klicken Sie auf **[!UICONTROL Delete Package]**.

   - Um eine Bestellung abzubrechen, klicken Sie auf **[!UICONTROL Cancel]**. Es wird kein Versandlabel erstellt und die _[!UICONTROL Create Shipping Label]_Das Kontrollkästchen ist deaktiviert.

   >[!NOTE]
   >
   >Wenn Sie einen anderen Pakettyp als den Standardpakettyp verwenden oder eine Signatur benötigen, können die Versandkosten von denen abweichen, die Sie dem Kunden in Rechnung gestellt haben. Unterschiede bei den Versandkosten spiegeln sich nicht in Ihrem Geschäft wider.

1. Klick **[!UICONTROL OK]**.

   Commerce verbindet sich mit dem Spediteursystem, reicht die Bestellung ein und erhält für jedes Paket ein Versandetikett und eine Tracking-Nummer.

### Methode 2: Erstellen eines Titels für eine bestehende Sendung

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Suchen Sie die Bestellung im Raster und öffnen Sie das Versandformular.

1. In der _[!UICONTROL Shipping and Tracking Information]_klicken Sie auf **[!UICONTROL Create Shipping Label]**.

1. Die bestellten Produkte an die entsprechenden Pakete verteilen und auf **[!UICONTROL OK]**.

1. Um die Paketinformationen anzuzeigen, klicken Sie auf **[!UICONTROL Show Packages]**.

## Schritt 4: Beschriftungen drucken

Versandetiketten werden im PDF-Format generiert und können vom Administrator ausgedruckt werden. Jedes Etikett enthält die Bestellnummer und die Paketnummer.

>[!NOTE]
>
>Da für jedes Paket eine individuelle Versandbestellung erstellt wird, können für eine einzelne Sendung mehrere Versandkennzeichnungen empfangen werden.

### Methode 1: Aufkleber aus dem Lieferformular drucken

1. Auf der _Admin-Seitenleiste_, navigieren Sie zu einer der folgenden Seiten und suchen Sie dann den Versanddatensatz:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Finden Sie die Reihenfolge im Raster und öffnen Sie den Datensatz. Wählen Sie im linken Bedienfeld **[!UICONTROL Shipments]**. Öffnen Sie dann den Lieferdatensatz.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Die Sendung im Raster finden und den Datensatz öffnen.

1. Um die PDF-Datei herunterzuladen, gehen Sie zu _[!UICONTROL Shipping and Tracking]_-Abschnitt des Formulars und klicken Sie auf **[!UICONTROL Print Shipping Label]**.

   Je nach Browsereinstellungen können die Versandaufkleber direkt aus der PDF-Datei eingesehen und ausgedruckt werden.

   Die _[!UICONTROL Print Shipping Label]_Die Schaltfläche wird erst angezeigt, nachdem der Spediteur Beschriftungen für die Sendung generiert hat. Wenn die Schaltfläche fehlt, klicken Sie auf **[!UICONTROL Create Shipping Label]**. Die Schaltfläche wird angezeigt, nachdem Commerce die Kennzeichnung vom Provider erhalten hat.

### Methode 2: Etiketten für mehrere Bestellungen drucken

1. Auf der _Admin-Seitenleiste_ Navigieren Sie dann zu einer der folgenden Seiten und wählen Sie die zu druckenden Bestellungen oder Sendungen aus:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Aktivieren Sie im Raster das Kontrollkästchen jeder zu druckenden Bestellung mit Versandaufklebern.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Aktivieren Sie im Raster das Kontrollkästchen jeder Sendung mit den zu druckenden Etiketten.

1. Legen Sie die **[!UICONTROL Actions]** steuern auf `Print Shipping Labels`.

1. Klick **[!UICONTROL Submit]**.

Für jede Sendung, die mit den ausgewählten Bestellungen verbunden ist, wird ein kompletter Satz von Versandaufklebern gedruckt.

## Erforderliche Provider-Einstellungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Type] | Die Pakettypen unterscheiden sich je nach Träger und Methode. Zunächst wird der Standardpakettyp für jeden Provider ausgewählt. USPS benötigt den Pakettyp nicht für Inlandslieferungen. |
| [!UICONTROL Customs Value] | (Nur internationale Sendungen) Der deklarierte Wert oder Verkaufspreis des Inhalts einer internationalen Sendung. |
| [!UICONTROL Total Weight] | Das Gesamtgewicht aller zum Paket hinzugefügten Produkte wird automatisch berechnet. Der Wert kann auch manuell geändert und als Pfund oder Kilogramm eingegeben werden. |
| [!UICONTROL Length, Width, Height] | (Optional) Die Paketdimensionen werden nur für benutzerdefinierte Pakete verwendet. Sie können die Maßeinheiten als Zoll oder Zentimeter angeben.<br/><br/>**[!UICONTROL Not Required]**: Der Spediteur sendet keine Lieferbestätigung an das Geschäft.<br/><br/>**[!UICONTROL No Signature]**: Eine Lieferbestätigung ohne Unterschrift des Empfängers wird vom Spediteur an das Geschäft gesendet.<br/><br/>**[!UICONTROL Signature Required]**: Der Spediteur erhält die Unterschrift des Empfängers und stellt dem Geschäft ein gedrucktes Exemplar zur Verfügung.<br/><br/>**[!UICONTROL Direct]**: (Nur FedEx) FedEx erhält eine Signatur von einer Person an der Versandadresse. Wenn niemand für die Unterzeichnung des Pakets zur Verfügung steht, versucht der Provider, das Paket zu einem anderen Zeitpunkt zuzustellen.<br/><br/>**[!UICONTROL Indirect]**: (Nur FedEx-Sendungen in Wohngebieten) FedEx erhält die Unterschrift einer Person (möglicherweise eines Nachbarn oder Gebäudemanagers) an der Lieferadresse. Der Empfänger kann ein signiertes FedEx-Tür-Tag hinterlassen, um zu autorisieren, das Paket zu belassen, ohne dass jemand anwesend ist, um es zu signieren.<br/><br/>**[!UICONTROL Contents]**: (Nur USPS) Wählen Sie eine der folgenden Beschreibungen des Pakets aus:<br/>- Geschenk<br/>- Dokumente<br/>- Warenmuster<br/>- Rückwaren<br/>- Waren<br/>- andere <br/><br/>**[!UICONTROL Explanation]**: (Nur USPS) Eine detaillierte Beschreibung des Paketinhalts.<br/><br/>**[!UICONTROL Adult Required]**: Der Spediteur erhält die Unterschrift eines erwachsenen Empfängers und stellt dem Geschäft ein gedrucktes Exemplar zur Verfügung. |

{style="table-layout:auto"}

## Erstellen von Paketen

Die _[!UICONTROL Create Packages]_Das Fenster wird angezeigt, wenn Sie einen Versandtitel erstellen möchten. Sie können sofort mit der Konfiguration des ersten Pakets beginnen.

### Konfigurieren eines Pakets

>[!NOTE]
>
>Wenn Sie den nicht standardmäßigen Wert für das [!UICONTROL Type] Oder Sie verlangen eine Unterschriftsbestätigung. Der Preis einer Sendung kann von dem Preis abweichen, den Sie dem Kunden in Rechnung gestellt haben.

1. Um eine Liste der ausgelieferten Produkte anzuzeigen und sie zum Paket hinzuzufügen, klicken Sie auf **[!UICONTROL Add Products]**.

   - Angabe der Produkte und Mengen.

     Die _[!UICONTROL Qty]_Spalte zeigt die maximale Menge an, die hinzugefügt werden kann. Bei der ersten Verpackung entspricht die Zahl der Gesamtmenge des zu versendenden Produkts.

   - Um die Produkte zum Paket hinzuzufügen, klicken Sie auf **[!UICONTROL Add Selected Product(s) to Package]**.

1. Um ein Paket hinzuzufügen, klicken Sie auf **[!UICONTROL Add Package]**.

   Sie können mehrere Pakete hinzufügen und sie gleichzeitig bearbeiten.

1. Um ein Paket zu löschen, klicken Sie auf **[!UICONTROL Delete Package]**.

Nachdem Produkte zum Paket hinzugefügt wurden, kann die Menge nicht direkt bearbeitet werden.

### Menge erhöhen

1. Klick **[!UICONTROL Add Selection]**.

1. Geben Sie die zusätzliche Menge ein.

   Die Nummer wird zur vorherigen Menge des Produkts in der Verpackung hinzugefügt.

### Menge verringern

1. Löschen Sie das Produkt aus dem Paket.

1. Klick **[!UICONTROL Add Selection]**.

1. Geben Sie den neuen, kleineren Wert ein.

### Versandkennzeichnungen generieren

Nachdem Sie alle Produkte verteilt haben, entspricht die Gesamtzahl der Pakete, die Sie verwenden werden, der Anzahl des letzten Pakets in der Liste. Die _OK_ Die Schaltfläche ist deaktiviert, bis alle versendeten Artikel an die Pakete verteilt werden und alle erforderlichen Informationen vollständig sind.

Um die Kennzeichnungen zu generieren, klicken Sie auf **[!UICONTROL OK]**.

Sie können auf Folgendes klicken **[!UICONTROL Cancel]** , um den Prozess bei Bedarf anzuhalten. Die Pakete werden nicht gespeichert, und der Versand-Label-Prozess wird abgebrochen.

### Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Type] | Gibt den Typ eines Pakets an. Wählen Sie einen der vordefinierten Werte aus. Die verfügbaren Pakettypen unterscheiden sich von Versandunternehmen zu Versandunternehmen. Wenn das Popup-Fenster Pakete erstellen geöffnet wird, wird das Standardpaket für den Spediteur im Feld Typ angezeigt. Wenn Sie ein Paket auswählen, das nicht von einem Spediteur entworfen wurde, müssen Sie die Abmessungen des Pakets eingeben. Für Versandaufkleber, die für DHL-, FedEx- und UPS-Lieferungen erstellt wurden, ist das Feld Warentyp auf Folgendes festgelegt `Merchandise`. Bei USPS spiegelt das Feld den Wert aus dem _Inhalt_ Feld in der _[!UICONTROL Create Packages]_Fenster. |
| [!UICONTROL Total Weight] | Das Gesamtgewicht eines Pakets. Das Feld wird vorab mit dem Gesamtgewicht der Produkte in einem Paket ausgefüllt. Die Maßeinheit kann entweder auf Pfund oder Kilogramm eingestellt werden. |
| [!UICONTROL Length] | Die Länge eines Pakets, Ganzzahlen und Gleitkommazahlen. Das Feld ist aktiviert, wenn der benutzerdefinierte Pakettyp verwendet wird. Die Maßeinheit kann auf Zoll oder Zentimeter festgelegt werden. |
| [!UICONTROL Width] | Die Breite eines Pakets, Ganzzahlen und Gleitkommazahlen. Das Feld ist aktiviert, wenn der benutzerdefinierte Pakettyp verwendet wird. Die Maßeinheiten können über das Dropdown-Menü neben dem Feld Höhe angegeben werden. Wählen Sie zwischen Zoll und Zentimeter. |
| [!UICONTROL Height] | Die Höhe eines Pakets, Ganzzahlen und Gleitkommazahlen. Das Feld ist aktiviert, wenn der benutzerdefinierte Pakettyp verwendet wird. Die Maßeinheiten können über das Dropdown-Menü neben dem Feld Höhe angegeben werden. Wählen Sie zwischen Zoll und Zentimeter. |
| [!UICONTROL Signature] | Definiert die Versandbestätigung. Optionen:<br/><br/>**[!UICONTROL Not Required]**: Es wird kein Lieferbestätigungsschreiben an Sie gesendet.<br/><br/>**[!UICONTROL No Signature]**: Sie erhalten ein Empfangsbestätigungsschreiben ohne Unterschrift eines Empfängers.<br/><br/>**[!UICONTROL Signature Required]**: Der Spediteur erhält die Unterschrift des Empfängers und stellt Ihnen sein gedrucktes Exemplar zur Verfügung.<br/><br/>**[!UICONTROL Adult Required]**: Der Spediteur erhält die Unterschrift des erwachsenen Empfängers und stellt Ihnen sein gedrucktes Exemplar zur Verfügung.<br/><br/>**[!UICONTROL Direct (FedEx only)]**: FedEx erhält eine Signatur von jemandem an der Versandadresse und versucht erneut, den Versand durchzuführen, wenn niemand für die Unterzeichnung des Pakets zur Verfügung steht.<br/><br/>**[!UICONTROL Indirect (FedEx only)]**: FedEx erhält eine Signatur auf eine von drei Arten:<br/>(1) von jemandem an der Lieferadresse; <br/>(2) von einem Nachbarn, Gebäudemanager oder einer anderen Person an der Anschrift oder <br/>(3) Der Empfänger kann ein signiertes FedEx Door Tag hinterlassen, das die Freigabe des Pakets autorisiert, ohne dass jemand anwesend ist. Nur für Sendungen im Wohnbereich verfügbar. Die Optionen können je nach Versandmethode leicht variieren. Die neuesten Informationen finden Sie in den Ressourcen des Spediteurs. |
| [!UICONTROL Contents] | (Nur für USPS-Sendungen verfügbar) Beschreibung des Paketinhalts. Optionen: `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | (Nur USPS-Sendungen) Detaillierte Beschreibung des Paketinhalts. |

{style="table-layout:auto"}

[1]: https://www.fedex.com/en-us/api/get-support.html
[2]: https://www.ups.com/us/en/support/contact-us.page
[3]: https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html
[4]: https://www.usps.com/business/web-tools-apis/#ssc
