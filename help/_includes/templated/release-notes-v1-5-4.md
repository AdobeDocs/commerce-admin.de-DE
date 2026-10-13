---
source-git-commit: bb5da9eea16601303b62ccc06327c6a832062c49
workflow-type: tm+mt
source-wordcount: '1471'
ht-degree: 0%
---
# Behobene Probleme in Adobe Commerce B2B (v1.5.4-alpha1)

## B2B v1.5.4-alpha1

*13. Oktober 2026*

Im Adobe Commerce B2B 1.5.4-alpha1-Code wurden 23 Probleme behoben. Nachfolgend werden einige der in dieser Version enthaltenen behobenen Probleme beschrieben.

### Admin-Benutzeroberfläche

#### [B2B] Bundle-Produktmengen werden nach der Aktualisierung der Preise in Backend-Angeboten nicht beibehalten

Es wurde ein Problem behoben, bei dem die Menge eines Bundle-Elements in einem verhandelbaren Admin-Angebot auf ihren vorherigen Wert zurückgesetzt wurde, nachdem die Menge im Raster nach einer Konfigurationsänderung über das Dialogfeld „Konfigurieren“ bearbeitet wurde.

_ACP2E-5005_

### B2B

#### [B2B] Die Seite mit Angebotsdetails (Storefront und Admin) verliert die Element-/Produktinformationen, wenn das zugehörige Produkt aus dem Katalog gelöscht wird

Es wurde ein Problem behoben, bei dem nicht verkäufliche Produkte aus abgeschlossenen verhandelbaren Angeboten verschwanden

_ACP2E-4680_

#### Die Produktpaketmenge wurde nach dem Versand des Angebots vom Backend nicht korrekt aktualisiert.

Es wurde ein Problem behoben, bei dem die Mengen der Bundle-Produktoptionen bei der Neukonfiguration eines verhandelbaren Angebots im Admin-Bedienfeld nicht aktualisiert wurden. Zuvor wurden Änderungen an den Mengen der Bundle-Optionen über die Schaltfläche Konfigurieren im Hintergrund verworfen.

_ACP2E-4801_

#### [CLOUD] [B2B] Admin Companies Grid verursacht hohe MySQL-CPU — korrelierte company_type/COUNT-Abfrage

Es wurde ein Problem behoben, bei dem das Admin Companies-Raster (Kunden → Unternehmen) eine hohe MySQL-CPU-Auslastung und langwierige Datenbanksitzungen verursachte. Zuvor war für die Bestimmung des Firmentyps (über-/untergeordnet/Firma) für jede Zeile eine korrelierte Unterabfrage für die Tabelle company_relation erforderlich, die einmal pro Unternehmenszeile ausgelöst wurde, wodurch sowohl die Auflistungs- als auch die Gesamtzahl der Abfragen O(N²) skaliert werden. Die Fehlerbehebung ersetzt dies durch einen einzelnen voraggregierten JOIN, der unabhängig von der Datensatzgröße einmal ausgeführt wird.

_ACP2E-4846_

#### Zahlung auf Konto (B2B) - Schaltfläche „Bestellung bearbeiten“ fehlt für ausstehende Bestellungen, wenn sie für COD sichtbar ist.

Die Schaltfläche „Bestellung bearbeiten“ ist jetzt für Bestellungen verfügbar, die mit Zahlung auf Rechnung aufgegeben werden. Zuvor war es nicht möglich, eine Bestellung mit Zahlung auf Rechnung zu bearbeiten, während die Bestellung noch aussteht

_ACP2E-4877_

#### PHP-Zeitüberschreitung beim Einsparen von B2B-Unternehmen mit Multi-Company-Super-User

Das Speichern eines B2B-Unternehmens oder das Laden der Super-User-Seite des Unternehmens in den Admin überschreitet nicht mehr die maximale PHP-Ausführungszeit, wenn der Super-User des Unternehmens einer sehr großen Anzahl von Unternehmen zugewiesen ist.

_ACP2E-4967_

#### [On-Premise] verhandelbare Anführungszeichen werden nicht erwartungsgemäß aktualisiert

Es wurde ein Problem behoben, bei dem verhandelbare Angebote nicht aktualisiert wurden, wenn ein Produkt, das in einem aktiven verhandelbaren Angebot vorhanden war, gelöscht wurde.

_ACP2E-5001_

#### Volatile „Zahlung auf Konto“ zusätzliche Prüfungen

Es wurde ein Problem behoben, bei dem Payment on Account, eine Zahlungsmethode, die ausschließlich für B2B-Firmenmitglieder bestimmt ist, von einzelnen (B2C)-Kunden während des Checkouts ausgewählt werden konnte. Bislang wurde diesen Kunden fälschlicherweise gestattet, mit der Zahlung auf Konto fortzufahren, anstatt den Fehler „Zahlungsmethode nicht verfügbar“ zu erhalten.

_ACP2E-5013_

#### Der Assistent zum Speichern freigegebener Kataloge löscht die Preisstruktur eines freigegebenen Katalogs

Fehlerkorrektur - Die Speicheraktion des Assistenten für freigegebene Kataloge löscht jetzt die Preisstruktur einer freigegebenen Katalogspeicherung

_ACP2E-5015_

#### GraphQL customer.role gibt für B2C-Kunden ohne Unternehmen „Interner Server-Fehler“ zurück

Es wurde ein Problem behoben, bei dem die Abfrage von Kunde { role {...} } über GraphQL einen „Internen Server-Fehler“ für B2C-Kunden zurückgibt, die keinem Unternehmen zugewiesen sind. Zuvor löste diese Abfrage einen PHP TypeError aus, da eine Null-Unternehmens-ID an eine Methode mit einem strikten Integer-Type-Hinweis übergeben wurde.

_ACP2E-5017_

#### [B2B] Der Artikelrabatt für Bundles wird nicht angewendet, wenn Optionsmengen in Backend-Angeboten aktualisiert werden

Fehlerkorrektur - Ein Rabatt auf Artikelebene, der auf ein Produkt des dynamischen Preispakets im Backend-Angebotsadministrator angewendet wurde, wird jetzt in der Zwischensumme oder der Zwischensumme (exkl. (Steuer) Spalten, wenn die Optionsmengen des Bundles über das Dialogfeld „Konfigurieren“ aktualisiert wurden. Zuvor war der Rabatt in der Rabattspalte aufgeführt, verringerte jedoch nicht die angegebene Zwischensumme.

_ACP2E-5034_

#### Anforderungsabschnitt wird bei jeder Seitennavigation neu geladen

Es wurde ein Problem behoben, bei dem der Anforderungsabschnitt bei jeder Produkt- und Kategorieseitennavigation einen unnötigen AJAX-Neuladen auslöste. Zuvor wurde der Abschnitt bei jedem Laden der Seite für Kunden mit nicht leeren Daten der Anforderungsliste neu geladen, selbst wenn keine Änderungen vorgenommen wurden.

_ACP2E-5037_

#### [B2B] Fehler bei fehlenden Regionsdaten an Firmenadresse

Es wurde ein Problem behoben, bei dem auf der Seite „Firmenprofil“ und auf der Seite „Admin-Kundenbearbeitung“ ein Fehler angezeigt wurde, wenn einer Firmenadresse eine Region zu ihrem Land hinzugefügt wurde, nachdem die Adresse ohne eine Region gespeichert wurde. Jetzt wird die Adresse korrekt auf den gespeicherten Regionstext zurückgesetzt, anstatt einen Fehler zu verursachen.

_ACP2E-5092_

#### Firmenaktualisierung für „admin“ mit nicht englischem Gebietsschema setzt das Kreditlimit zurück

Es wurde ein Problem behoben, bei dem die Bearbeitung der Details einer B2B-Firma das konfigurierte Kreditlimit versehentlich auf 0 zurücksetzen konnte, wenn das Gebietsschema des Administrators vom Standardgebietsschema abwich. Das Kreditlimit wird nun korrekt beibehalten, es sei denn, es wird explizit geändert.

_ACP2E-5127_

#### [CLOUD] Der Admin mit Websitebeschränkung kann Kundinnen und Kunden nicht löschen, wenn ihre user_id mit einer nicht zugänglichen customer_entity_id kollidiert

Wenn ein Admin mit Websitebeschränkung versucht hat, einen Kunden zu löschen, hat das Plug-in für die Berechtigungsprüfung des Systems zuvor die eigene Benutzer-ID des Administrators mit der ID verglichen
Kunden-Entitäts-IDs, um Einschränkungen für die Unternehmenshierarchie durchzusetzen, ohne zu überprüfen, ob der aktive Benutzer tatsächlich ein Kunde war; wenn die Benutzer-ID des Administrators eingetreten ist
Um die Entitäts-ID eines nicht verwandten Kunden auf einer Website zu berücksichtigen, auf die der Administrator nicht zugreifen konnte, versuchte das Plug-in, diesen nicht zugänglichen Kundendatensatz zu laden
und der Löschvorgang schlug mit dem Fehler „Weitere Berechtigungen sind erforderlich“ fehl, obwohl der Administrator über gültige Rechte für den zu löschenden Kunden verfügte. Dies wurde behoben
Durch das Hinzufügen einer Bedingung wird der Kunden-ID-Vergleich nur ausgeführt, wenn der handelnde Benutzer tatsächlich ein Kunde ist, d. h. vom Administrator initiierte Löschvorgänge umgehen diese Prüfung jetzt vollständig. Eingeschränkte Administratoren können wieder Kunden innerhalb ihrer zugewiesenen Websites löschen, ohne durch nicht verknüpfte, nicht zugängliche Kundendatensätze blockiert zu werden

_ACP2E-5146_

#### B2B-Bestellung zeigt falschen Firmennamen in Admin-Kundenaufträgen an

Fehlerkorrektur - In Admin-Kundenaufträgen wird für B2B-Bestellungen jetzt kein falscher Firmenname mehr angezeigt, wenn ein Benutzer mehreren Unternehmen zugewiesen wurde.
Der Firmenname wird nun basierend auf dem mit der Bestellung verbundenen Unternehmen korrekt angezeigt.

_B2B-4656_

### B2B, Warenkorb und Checkout

#### [ON PREM] [B2B] Der Quick Order Uploader friert ein, wenn versucht wird, eine Binärdatei mit der Erweiterung .CSV hochzuladen

Es wurde ein Problem behoben, bei dem der Uploader für Schnellbestellungsdateien alle Dateien akzeptierte, die mit einer CSV-Erweiterung umbenannt wurden, einschließlich Binärdateien. Zuvor wurde kein MIME-Typ oder keine Inhaltsvalidierung durchgeführt, sodass nicht-CSV-Dateien (z. B. ausführbare Dateien) hochgeladen und verarbeitet werden konnten, als ob sie gültige SKU-/MENGENLISTEN wären.

_ACP2E-5212_

### B2B, GraphQL

#### Ungenauigkeit der Gesamtanzahl der Anforderungsliste GQL

Fehlerkorrektur - Die GraphQL-Abfrage „Anforderungslisten“ gibt jetzt einen falschen Wert „total_count“ zurück, der nur die Anzahl der Artikel auf der aktuellen Seite und nicht die Gesamtzahl der Anforderungslistenentitäten widerspiegelt, die den Abfragekriterien entsprechen.

_ACP2E-4799_

### B2B, Bestellung

#### Hilfe beim Bereinigen von mehr als 59M Angebotstabellen (sales_clean_quotes kann nicht ausgeführt werden)

Es wurde ein Problem behoben, bei dem der `sales_clean_quotes` Cron-Auftrag bei Instanzen mit großen Anführungszeichen-Tabellen eine Zeitüberschreitung aufwies. Zuvor wählte die Bereinigungsabfrage alle Spalten aus der `negotiable_quote` unnötigerweise aus, was dazu führte, dass MySQL eine vollständige Dateisortierung für Millionen von Zeilen durchführte; und jedes Zitat wurde einzeln über die PHP-Modellschicht gelöscht, was die Leistungskosten erhöhte.

_ACP2E-4891 - [GitHub-Code-Beitrag](https://github.com/magento/magento2/commit/b63925d9)_

### B2B, Leistung

#### [CLOUD] Follow-up von ACSD-70033 : Stillstand bei der Tabelle magento_catalogpermissions_index_product. Fortsetzung

Zuvor konnte die Neuindizierung von Katalogberechtigungen mit aktiviertem freigegebenen Katalog zu einem Deadlock-Fehler führen, wodurch die Neuindizierung fehlschlug. Die Neuindizierung wird jetzt erfolgreich abgeschlossen, auch wenn mehrere Indexerprozesse gleichzeitig ausgeführt werden.

_ACP2E-4844_

### Inhalt

#### CMS-Seiten, die für verschiedene Websites erstellt wurden, zeigen falsche Seiten im Frontend an

In früheren Setups für mehrere Websites, in denen der Cache-Schlüssel für die Website-Einschränkung nicht pro Website enthalten war, wodurch die falsche CMS-Seite in der sekundären Website-Storefront bereitgestellt wurde. Der Cache-Schlüssel in WebsiteRestriction/Controller/Index/Stub.php enthält nun korrekt die aktuelle Website-ID, die über den Store-Manager aufgelöst wurde.

_ACP2E-4593_

### Framework

#### [B2B] Bestellungen werden nicht automatisch in Kundenaufträge mit ActiveMQ konvertiert

Es wurde ein Problem behoben, bei dem von Cron gestartete Verbraucher keine Nachrichten verarbeiteten, wenn ActiveMQ mit dem STOMP-Protokoll verwendet wurde. Daher wurden automatisch genehmigte Bestellungen nicht in Kundenaufträge umgewandelt. Die Nachrichtenverarbeitung für STOMP-Warteschlangen ist jetzt zuverlässiger und konsistenter mit der DB- und AMQP-Warteschlangenimplementierung.

_ACP2E-4349 - [GitHub-Code-](https://github.com/magento/magento2/commit/08b91f1a) - [GitHub-Code-Beitrag](https://github.com/magento/inventory/commit/239464da)_

### Installieren und Verwalten

#### [Cloud] Korrektur veralteter bestehender ISO-Unterteilungscodes

Die Regionscodes für 13 Länder wurden aktualisiert, damit sie der ISO-Norm 3166-2 entsprechen. Zuvor entsprachen einige Regionalcodes nicht dem Standard, was zu Problemen mit Drittanbieterintegrationen und der internationalen Compliance führen konnte. Für Belgien, Kolumbien, Spanien, Frankreich, Italien und Lettland wurden neue Regionen hinzugefügt. Regionscodes wurden für Deutschland, Estland, Finnland, Frankreich, Indien, Estland, Kolumbien, Lettland, Kolumbien und Costa Rica aktualisiert.

_ACP2E-4495 - [GitHub-Code-Beitrag](https://github.com/magento/magento2/commit/9b6a8bd9)_
