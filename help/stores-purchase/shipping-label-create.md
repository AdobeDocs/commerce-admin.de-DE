---
title: Erstellen von Versandkennzeichnungen und -paketen
description: Erfahren Sie, wie Sie Artikel in einer Bestellung verpacken und Versandkennzeichnungen erstellen.
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: be8a4e9d7cbcf34452724f8055980007794f525f
workflow-type: tm+mt
source-wordcount: '1944'
ht-degree: 0%

---

# Erstellen von Versandkennzeichnungen

Um Versandkennzeichnungen zu erstellen, müssen Sie zunächst Ihr Versandunternehmen-Konto einrichten, um Kennzeichnungen zu unterstützen. Folgen Sie dann den Anweisungen, um eine Beschreibung des Pakets und seines Inhalts einzugeben.

Nachdem Sie die Informationen zur Versandkennzeichnung konfiguriert und eine Bestellung gesendet haben, stellt Commerce eine Verbindung zum System der Versandunternehmen her, sendet eine Bestellung und erhält eine Versandkennzeichnung sowie eine Tracking-Nummer. Wenn im System ein Versandaufkleber für diese Sendung vorhanden ist, wird dieser durch einen neuen ersetzt. Vorhandene Tracking-Nummern werden jedoch nicht ersetzt. Jede neue Tracking-Nummer wird der bestehenden hinzugefügt.

## Schritt 1: Spediteure kontaktieren

Bevor Sie beginnen, stellen Sie sicher, dass Ihre Versandkonten für die Verarbeitung von Beschriftungen eingerichtet sind. Einige Spediteure berechnen möglicherweise eine zusätzliche Gebühr, um Ihrem Konto Versandaufkleber hinzuzufügen.

Kontaktieren Sie jeden Spediteur, den Sie verwenden, um die Versandkennzeichnungen für Ihren Shop zu aktivieren.

Befolgen Sie die Anweisungen der einzelnen Spediteure, um Ihrem Konto Support für Versandtitel hinzuzufügen.

- **FedEx** - Wenden Sie sich an [FedEx Web Integration Services][1], um mehr über die Anforderungen für den Etikettendruck für Ihr Konto zu erfahren.
- **USPS** - Im [Web-Tools-API-Portal][4] unter Shipper Support Center erfahren Sie, wie Sie Ihre Anmeldedaten für den Etikettendruck einrichten.
- **UPS**- Kontaktieren Sie [UPS][2], um zu bestätigen, dass Ihr Konto Versandaufkleber unterstützt. Um Versandkennzeichnungen zu generieren, müssen Sie die UPS XML-Option verwenden.
- **DHL** - Wenden Sie sich an [DHL eCommerce Solutions][3], um mehr über die Anforderungen an den Etikettendruck für Ihr Konto zu erfahren.

## Schritt 2: Konfiguration für jeden Provider aktualisieren

1. Vergewissern Sie sich, dass Ihre [Store-Informationen](../getting-started/store-details.md#store-information) vollständig sind.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Shipping Settings]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Origin]** und konfigurieren Sie die **[!UICONTROL Shipping Origin Address]**.

1. Befolgen Sie die nachstehenden Anweisungen für jedes Provider-Konto, das für den Etikettendruck aktiviert ist.

### USV-Konfiguration

United Parcel Service versendet sowohl im In- als auch im Ausland. Versandaufkleber können jedoch nur für Sendungen generiert werden, die ihren Ursprung in den USA haben.

1. Wählen Sie im Abschnitt _[!UICONTROL Sales]_&#x200B;im linken Bereich **[!UICONTROL Delivery Methods]**&#x200B;aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL UPS]** .

1. Überprüfen Sie, ob Ihr USV-**[!UICONTROL Shipper Number]** korrekt ist.

   Ihre Lieferantennummer wird nur angezeigt, wenn [!DNL United Parcel Service XML] aktiviert ist.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

### USPS-Konfiguration

Die [!DNL United States Postal Service] versendet sowohl im In- als auch im Ausland.

{{$include /help/_includes/usps-api-type-configuration-note.md}}

1. Erweitern Sie **[!UICONTROL Delivery Methods]** -Konfiguration ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL USPS]** .

1. Wählen Sie **[!UICONTROL USPS Type]** als `USPS Rest APIs` oder `USPS Web Tools API` aus.

1. Überprüfen Sie, ob die **[!UICONTROL Secure Gateway URL]** korrekt ist.

1. Geben Sie die **[!UICONTROL Password]** ein, die Sie von USPS erhalten haben.

1. Stellen Sie sicher, dass die folgende Konfiguration basierend auf der ausgewählten **[!UICONTROL USPS Type]** abgeschlossen ist:

   Wenn Sie die USPS Web Tools-API verwenden:
   - Benutzer-ID
   - Kennwort

   Wenn Sie die USPS-REST-APIs verwenden:
   - Consumer Key
   - Verbrauchergeheimnis
   - Preisoptionen
   - Kontotyp
   - Kontonummer
   - Kunden-Registrierungs-ID (CRID)
   - Mailer-Kennung (MID)
   - Manifest-MID
   - AES/ITN

1. Legen Sie **[!UICONTROL Size]** auf `Large` fest und geben Sie Werte für die folgenden Dimensionen ein:

   - length
   - Breite
   - Höhe
   - Umfang

1. Klicken Sie auf **[!UICONTROL Save Config]**.

### FedEx-Konfiguration

FedEx versendet national und international. Geschäfte außerhalb der USA können FedEx-Labels nur für internationale Sendungen erstellen.

1. Erweitern Sie **[!UICONTROL Delivery Methods]** -Konfiguration ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL FedEx]** .

1. Überprüfen Sie, ob die folgenden FedEx-Anmeldeinformationen korrekt sind:

   - Zählernummer
   - Schlüssel
   - Kennwort

1. Klicken Sie auf **[!UICONTROL Save Config]**.

### DHL-Konfiguration

DHL erbringt internationale Versanddienstleistungen.

1. Erweitern Sie **[!UICONTROL Delivery Methods]** -Konfiguration ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL DHL]** .

1. Überprüfen Sie, ob die **[!UICONTROL Gateway URL]** korrekt ist.

1. Vergewissern Sie sich, dass die folgenden Anmeldeinformationen vollständig sind:

   - Zugriffs-ID
   - Kennwort
   - Kontonummer

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Schritt 3: Erstellen Sie Versandaufkleber

### Methode 1: Kennzeichnung für neue Sendung erstellen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie die Reihenfolge im Raster und öffnen Sie den Datensatz.

   Der Status der Bestellung muss entweder `Pending` oder `Processing` sein.

1. Klicken Sie oben rechts auf **[!UICONTROL Ship]**.

1. Bestätigen Sie die Versandinformationen entsprechend den Anforderungen des Spediteurs.

1. Aktivieren Sie in der rechten unteren Ecke das Kontrollkästchen **[!UICONTROL Create Shipping Label]** .

1. Klicken Sie auf **[!UICONTROL Submit Shipment]**.

1. Hinzufügen oder Aktualisieren von Produkten im Paket:

   - Um Produkte aus der Bestellung zum Paket hinzuzufügen, klicken Sie auf **[!UICONTROL Add Products]**. Die Spalte _[!UICONTROL Quantity]_&#x200B;zeigt die maximale Anzahl von Produkten an, die für das Paket verfügbar sind.

   - Aktivieren Sie das Kontrollkästchen jedes Produkts, das dem Paket hinzugefügt werden soll, und geben Sie die **[!UICONTROL Quantity]** jedes Produkts ein. Klicken Sie dann auf **[!UICONTROL Add Selected Product(s) to Package]**.

   - Um ein Paket hinzuzufügen, klicken Sie auf **[!UICONTROL Add Package]**.

   - Um ein Paket zu löschen, klicken Sie auf **[!UICONTROL Delete Package]**.

   - Um eine Bestellung zu stornieren, klicken Sie auf **[!UICONTROL Cancel]**. Es wird kein Versandaufkleber erstellt und das Kontrollkästchen &quot;_[!UICONTROL Create Shipping Label]_&quot; wird deaktiviert.

   >[!NOTE]
   >
   >Wenn Sie einen anderen Pakettyp als den Standardpakettyp verwenden oder eine Signatur benötigen, können die Versandkosten von denen abweichen, die Sie dem Kunden in Rechnung gestellt haben. Unterschiede bei den Versandkosten werden in Ihrem Geschäft nicht berücksichtigt.

1. Klicken Sie auf **[!UICONTROL OK]**.

   Commerce verbindet sich mit dem Spediteursystem, reicht die Bestellung ein und erhält für jedes Paket ein Versandlabel und eine Tracking-Nummer.

### Methode 2: Kennzeichnung für bestehende Sendung erstellen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Suchen Sie die Bestellung im Raster und öffnen Sie das Versandformular.

1. Klicken Sie im Abschnitt _[!UICONTROL Shipping and Tracking Information]_&#x200B;auf **[!UICONTROL Create Shipping Label]**.

1. Verteilen Sie die bestellten Produkte an die entsprechenden Pakete und klicken Sie auf **[!UICONTROL OK]**.

1. Um die Paketinformationen zu überprüfen, klicken Sie auf **[!UICONTROL Show Packages]**.

## Schritt 4: Beschriftungen drucken

Versandaufkleber werden im PDF-Format generiert und können vom Administrator ausgedruckt werden. Jedes Etikett enthält die Bestellnummer und die Paketnummer.

>[!NOTE]
>
>Da für jedes Paket eine individuelle Versandbestellung erstellt wird, können mehrere Versandkennzeichnungen für eine einzelne Sendung empfangen werden.

### Methode 1: Aufkleber aus Lieferformular drucken

1. Navigieren Sie in der _Admin_-Seitenleiste zu einer der folgenden Seiten und suchen Sie nach dem Versanddatensatz:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Suchen Sie die Reihenfolge im Raster und öffnen Sie den Datensatz. Wählen Sie im linken Bedienfeld **[!UICONTROL Shipments]** aus. Öffnen Sie dann den Lieferdatensatz.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Sendung im Raster suchen und Datensatz öffnen.

1. Um die PDF-Datei herunterzuladen, gehen Sie zum Abschnitt _[!UICONTROL Shipping and Tracking]_&#x200B;des Formulars und klicken Sie auf **[!UICONTROL Print Shipping Label]**.

   Je nach Browsereinstellungen können die Versandkennzeichnungen direkt aus der PDF-Datei angezeigt und ausgedruckt werden.

   Die Schaltfläche _[!UICONTROL Print Shipping Label]_&#x200B;wird erst angezeigt, nachdem der Spediteur Beschriftungen für die Sendung generiert hat. Wenn die Schaltfläche fehlt, klicken Sie auf **[!UICONTROL Create Shipping Label]**. Die Schaltfläche wird angezeigt, nachdem Commerce die Kennzeichnung vom Provider erhalten hat.

### Methode 2: Etiketten für mehrere Bestellungen drucken

1. Navigieren Sie in _Admin_-Seitenleiste zu einer der folgenden Seiten und wählen Sie die zu druckenden Bestellungen oder Sendungen aus:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Aktivieren Sie im Raster das Kontrollkästchen jeder zu druckenden Bestellung mit Versandaufklebern.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Aktivieren Sie im Raster das Kontrollkästchen jeder Sendung mit zu druckenden Etiketten.

1. Setzen Sie das **[!UICONTROL Actions]** auf `Print Shipping Labels`.

1. Klicken Sie auf **[!UICONTROL Submit]**.

Für jede Sendung, die mit den ausgewählten Bestellungen verbunden ist, wird ein kompletter Satz von Versandaufklebern gedruckt.

## Erforderliche Provider-Einstellungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Type] | Die Pakettypen unterscheiden sich je nach Träger und Methode. Zunächst wird der Standardpakettyp für jeden Provider ausgewählt. USPS benötigt den Pakettyp nicht für Inlandslieferungen. |
| [!UICONTROL Customs Value] | (Nur internationale Sendungen) Der deklarierte Wert oder Verkaufspreis des Inhalts einer internationalen Sendung. |
| [!UICONTROL Total Weight] | Das Gesamtgewicht aller zum Paket hinzugefügten Produkte wird automatisch berechnet. Der Wert kann auch manuell geändert und als Pfund oder Kilogramm eingegeben werden. |
| [!UICONTROL Length, Width, Height] | (Optional) Die Paketdimensionen werden nur für benutzerdefinierte Pakete verwendet. Sie können die Maßeinheiten als Zoll oder Zentimeter angeben.<br/><br/>**[!UICONTROL Not Required]**: Vom Spediteur wird keine Lieferbestätigung an das Geschäft gesendet.<br/><br/>**[!UICONTROL No Signature]**: Eine Lieferbestätigung ohne Unterschrift des Empfängers wird vom Spediteur an das Geschäft gesendet.<br/><br/>**[!UICONTROL Signature Required]**: Der Spediteur erhält die Unterschrift des Empfängers und stellt dem Geschäft ein gedrucktes Exemplar zur Verfügung.<br/><br/>**[!UICONTROL Direct]**: (Nur FedEx) FedEx erhält eine Signatur von einer Person an der Lieferadresse. Wenn niemand für die Unterzeichnung des Pakets zur Verfügung steht, versucht der Provider, das Paket zu einem anderen Zeitpunkt zuzustellen.<br/><br/>**[!UICONTROL Indirect]**: (Nur FedEx-Hauslieferungen) FedEx erhält die Unterschrift einer Person (möglicherweise eines Nachbarn oder Gebäudemanagers) an der Lieferadresse. Der Empfänger kann ein signiertes FedEx-Tür-Tag hinterlassen, um zu autorisieren, das Paket zu hinterlassen, ohne dass jemand anwesend ist, um es zu signieren.<br/><br/>**[!UICONTROL Contents]**: (Nur USPS) Wählen Sie eine der folgenden Beschreibungen des Pakets aus:<br/>- Geschenk<br/>- Dokumente<br/>- Handelsmuster<br/>- Zurückgegebene Waren<br/>- Waren<br/>- Andere <br/><br/>**[!UICONTROL Explanation]**: (Nur USPS) Eine detaillierte Beschreibung des Paketinhalts.<br/><br/>**[!UICONTROL Adult Required]**: Der Spediteur erhält die Unterschrift eines erwachsenen Empfängers und stellt dem Geschäft ein gedrucktes Exemplar zur Verfügung. |

{style="table-layout:auto"}

## Erstellen von Paketen

Das Fenster _[!UICONTROL Create Packages]_&#x200B;wird angezeigt, wenn Sie einen Versandtitel erstellen. Sie können sofort mit der Konfiguration des ersten Pakets beginnen.

### Konfigurieren eines Pakets

>[!NOTE]
>
>Wenn Sie den nicht standardmäßigen Wert für die [!UICONTROL Type] auswählen oder eine Unterschriftsbestätigung verlangen, kann der Preis einer Sendung von dem Preis abweichen, den Sie dem Kunden in Rechnung gestellt haben.

1. Um eine Liste der ausgelieferten Produkte anzuzeigen und sie zum Paket hinzuzufügen, klicken Sie auf **[!UICONTROL Add Products]**.

   - Geben Sie die Produkte und Mengen an.

     In der Spalte _[!UICONTROL Qty]_&#x200B;wird die maximale Menge angezeigt, die hinzugefügt werden kann. Bei der ersten Verpackung entspricht die Zahl der Gesamtmenge des zu versendenden Produkts.

   - Um die Produkte zum Paket hinzuzufügen, klicken Sie auf **[!UICONTROL Add Selected Product(s) to Package]**.

1. Um ein Paket hinzuzufügen, klicken Sie auf **[!UICONTROL Add Package]**.

   Sie können mehrere Pakete hinzufügen und sie gleichzeitig bearbeiten.

1. Um ein Paket zu löschen, klicken Sie auf **[!UICONTROL Delete Package]**.

Nachdem Produkte zum Paket hinzugefügt wurden, kann die Menge nicht direkt bearbeitet werden.

### Menge erhöhen

1. Klicken Sie auf **[!UICONTROL Add Selection]**.

1. Geben Sie die zusätzliche Menge ein.

   Die Nummer wird zur vorherigen Menge des Produkts in der Verpackung hinzugefügt.

### Menge verringern

1. Löschen Sie das Produkt aus dem Paket.

1. Klicken Sie auf **[!UICONTROL Add Selection]**.

1. Geben Sie den neuen, kleineren Wert ein.

### Versandkennzeichnungen generieren

Nachdem Sie alle Produkte verteilt haben, entspricht die Gesamtzahl der Pakete, die Sie verwenden werden, der Anzahl des letzten Pakets in der Liste. Die _OK_-Schaltfläche ist deaktiviert, bis alle gelieferten Artikel an Pakete verteilt werden und alle erforderlichen Informationen vollständig sind.

Um die Kennzeichnungen zu generieren, klicken Sie auf **[!UICONTROL OK]**.

Sie können bei Bedarf auf **[!UICONTROL Cancel]** klicken, um den Prozess anzuhalten. Die Pakete werden nicht gespeichert, und der Versand-Label-Prozess wird abgebrochen.

### Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Type] | Gibt den Typ eines Pakets an. Wählen Sie einen der vordefinierten Werte aus. Die verfügbaren Pakettypen sind für jeden Versanddienstleister unterschiedlich. Wenn das Popup-Fenster Pakete erstellen geöffnet wird, wird das Standardpaket für den Spediteur im Feld Typ angezeigt. Wenn Sie ein Paket auswählen, das nicht von einem Spediteur entworfen wurde, müssen Sie die Abmessungen des Pakets eingeben. Für Versandbeschriftungen, die für DHL-, FedEx- und UPS-Lieferungen erstellt wurden, ist das Feld Warentyp auf `Merchandise` gesetzt. Bei USPS spiegelt das Feld den Wert aus dem Feld _Inhalt_ im _[!UICONTROL Create Packages]_&#x200B;wider. |
| [!UICONTROL Total Weight] | Das Gesamtgewicht eines Pakets. Das Feld wird vorab mit dem Gesamtgewicht der Produkte in einer Verpackung ausgefüllt. Die Maßeinheit kann entweder auf Pfund oder Kilogramm eingestellt werden. |
| [!UICONTROL Length] | Die Länge eines Packages, Ganzzahlen und Gleitkommazahlen. Das Feld ist aktiviert, wenn der benutzerdefinierte Pakettyp verwendet wird. Die Maßeinheit kann auf Zoll oder Zentimeter festgelegt werden. |
| [!UICONTROL Width] | Die Breite eines Packages, Ganzzahlen und Gleitkommazahlen. Das Feld ist aktiviert, wenn der benutzerdefinierte Pakettyp verwendet wird. Die Maßeinheiten können über das Dropdown-Menü neben dem Feld Höhe angegeben werden. Wählen Sie zwischen Zoll und Zentimeter. |
| [!UICONTROL Height] | Die Höhe eines Packages, Ganzzahlen und Gleitkommazahlen. Das Feld ist aktiviert, wenn der benutzerdefinierte Pakettyp verwendet wird. Die Maßeinheiten können über das Dropdown-Menü neben dem Feld Höhe angegeben werden. Wählen Sie zwischen Zoll und Zentimeter. |
| [!UICONTROL Signature] | Definiert die Versandbestätigung. Optionen: <br/><br/>**[!UICONTROL Not Required]**: Es wird kein Lieferbestätigungsschreiben an Sie gesendet.<br/><br/>**[!UICONTROL No Signature]**: Sie erhalten ein Versandbestätigungsschreiben ohne Unterschrift eines Empfängers.<br/><br/>**[!UICONTROL Signature Required]**: Der Spediteur erhält die Unterschrift des Empfängers und stellt Ihnen sein gedrucktes Exemplar zur Verfügung.<br/><br/>**[!UICONTROL Adult Required]**: Der Spediteur erhält die Unterschrift des erwachsenen Empfängers und stellt Ihnen sein gedrucktes Exemplar zur Verfügung.<br/><br/>**[!UICONTROL Direct (FedEx only)]**: FedEx erhält eine Signatur von jemandem an der Versandadresse und versucht erneut, den Versand durchzuführen, wenn niemand für die Unterzeichnung des Pakets zur Verfügung steht.<br/><br/>**[!UICONTROL Indirect (FedEx only)]**: FedEx erhält eine Signatur auf eine von drei Arten: <br/>(1) von einer Person an der Lieferadresse; <br/>(2) von einem Nachbarn, einem Gebäudemanager oder einer anderen Person an der Adresse; oder <br/>(3) der Empfänger kann ein signiertes FedEx-Tür-Tag hinterlassen, das die Freigabe des Pakets autorisiert, ohne dass jemand anwesend ist. Nur für Sendungen zu Wohnzwecken verfügbar. Die Optionen können je nach Versandmethode leicht variieren. Die neuesten Informationen finden Sie in den Ressourcen des Spediteurs. |
| [!UICONTROL Contents] | (Nur für USPS-Sendungen verfügbar) Beschreibung des Paketinhalts. Optionen: `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | (Nur USPS-Sendungen) Detaillierte Beschreibung des Paketinhalts. |

{style="table-layout:auto"}

[1]: https://www.fedex.com/en-us/api/get-support.html
[2]: https://www.ups.com/us/en/support/contact-us.page
[3]: https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html
[4]: https://www.usps.com/business/web-tools-apis/#ssc

<!-- Last updated from includes: 2025-10-29 05:34:15 -->
