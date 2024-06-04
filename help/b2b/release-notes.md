---
title: '''[!DNL Adobe Commerce B2B] Versionshinweise'
description: Informationen zu Änderungen in [!DNL Adobe Commerce B2B] veröffentlicht.
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: e837dded8569cf917be8c36277362f5df77fb708
workflow-type: tm+mt
source-wordcount: '6851'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B] Versionshinweise

Diese Versionshinweise für die B2B-Erweiterung erfassen Ergänzungen und Fehlerbehebungen, die Adobe während eines Versionszyklus hinzugefügt hat, einschließlich:

![Neu](../assets/new.svg) Neue Funktionen
![Problem behoben](../assets/fix.svg) Fehlerbehebungen und Verbesserungen
![Bekanntes Problem](../assets/bug.svg) Bekannte Probleme

>[!NOTE]
>
>Siehe [Produktverfügbarkeit](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) Informationen zu den Versionen der für verfügbare Adobe Commerce-Versionen unterstützten B2B Commerce-Erweiterung.

## B2B 1.5.0-beta

{{$include /help/_includes/b2b-beta-note.md}}

*13. November 2023*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

Die Version B2B v1.5.0 Beta enthält neue Funktionen, Qualitätsverbesserungen und Fehlerbehebungen.

![Neu](../assets/new.svg) Verbesserungen der Anführungsfunktionen helfen Käufern und Verkäufern bei der effektiveren Verwaltung von Angeboten und Offering-Verhandlungen.

- **Zitat als Entwurf speichern**<!--B2B-2566-->—Beim Erstellen einer [Angebotsanforderung](quote-request.md) Im Warenkorb können Käufer das Angebot jetzt als Entwurf speichern, indem sie **[!UICONTROL Save as Draft]** auf [!UICONTROL Request a Quote] Formular.

  Das Ablaufdatum des Zitats im Entwurf ist nicht angegeben. Käufer können Entwürfe von Angeboten aus der [!UICONTROL My Quotes] im Konto-Dashboard.

- **Anführungszeichen umbenennen**<!--B2B-2596-->—Käufer können jetzt einen Anführungsnamen aus dem [Anführungsdetails](account-dashboard-my-quotes.md#quote-actions) Seite durch Auswahl der **[!UICONTROL Rename]** -Option. Diese Option steht autorisierten Käufern zur Verfügung, wenn sie das Angebot bearbeiten. Namensänderungsereignisse werden im Anführungsverlauf-Protokoll aufgezeichnet.

- **Anführungszeichen duplizieren**<!--B2B-2701-->—Käufer und Verkäufer können jetzt ein neues Angebot erstellen, indem sie ein vorhandenes Angebot kopieren. Eine Kopie wird über die Detailansicht des Zitats erstellt, indem Sie  **[!UICONTROL Create Copy]** auf [Anführungsdetailansicht](quote-price-negotiation.md#button-bar) im Admin oder [Storefront](account-dashboard-my-quotes.md#quote-actions).

- **Zeileneintrag - Sperren**<!--B2B-2597-->—Während der Preisverhandlungen können Verkäufer die Diskontsperre für Zeileneinträge für mehr Flexibilität bei der Anwendung von Rabatten verwenden. Beispielsweise kann ein Verkäufer einen Sonderrabatt für Zeileneinträge auf einen Artikel anwenden und den Artikel sperren, um weitere Rabatte zu vermeiden. Wenn ein Artikel gesperrt ist, kann der Artikelpreis nicht aktualisiert werden, wenn ein Rabatt auf Anführungszeichen angewendet wird. Siehe [Ankündigung eines Angebots für einen Käufer](sales-rep-initiates-quote.md).

![Neu ](../assets/new.svg)**Unternehmensverwaltung**<!--B2B-2901-->—Händler können Adobe Commerce-Unternehmen nun als hierarchische Organisationen anzeigen und verwalten, indem sie bestimmte Mutterunternehmen zuweisen. Nachdem ein Unternehmen einer Muttergesellschaft zugewiesen wurde, kann der Administrator des Mutterunternehmens das Unternehmenskonto verwalten. Nur autorisierte Admin-Benutzer können Unternehmenszuweisungen hinzufügen und verwalten. Weitere Informationen finden Sie unter [Verwalten der Unternehmenshierarchie](assign-companies.md).

- Auf der Seite &quot;Unternehmen&quot;wird eine neue **[!UICONTROL Company Type]** -Feld gibt Mutter- und untergeordnete Unternehmen an. Händler können die Unternehmensansicht nach Unternehmenstyp filtern und Unternehmen mithilfe von Zeileneinträgen oder Massenaktionen verwalten.

- Merchants können Unternehmenszuweisungen aus dem neuen **[!UICONTROL Company Hierarchy]** im Abschnitt [!UICONTROL Company Account] Seite.

- API-Entwickler können den neuen REST-API-Endpunkt für Unternehmensbeziehungen verwenden `/V1/company/{parentId}/relations` , um Unternehmenszuweisungen zu erstellen, anzuzeigen und zu entfernen. Siehe [Verwalten von Unternehmensobjekten](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) im *Entwicklerhandbuch für Web-API*.

![Problem behoben](../assets/fix.svg)<!--ACP2E-1984-->Merchandising durch Klicken auf **[!UICONTROL Print]** -Schaltfläche in der Detailansicht des Zitats in der Admin-Konsole werden jetzt aufgefordert, das Angebot als PDF zu speichern. Zuvor wurden Händler zu einer Seite umgeleitet, die Anführungszeichendetails enthielt.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1742-->Beim Versand eines Kundenangebots mit 0 Prozent und einer Mengenänderung löst der Administrator zuvor eine Ausnahme aus, speichert aber die Menge. Wenn diese Korrektur angewendet wurde, gilt für die Variable `0 percentage` eine ordnungsgemäße Ausnahme mit einer Meldung ausgelöst wird.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1742-->Bei der Angebotsverhandlung kann ein Verkäufer jetzt eine `0%` Rabatt im Feld Preisrabatt für verhandelte Angebote und Rücksendung des Angebots an den Käufer. Wenn der Verkäufer zuvor einen Rabatt von 0 % eingab und das Angebot an den Käufer zurückschickte, gab der Administrator eine `Exception occurred during quote sending` Fehlermeldung.

![Problem behoben](../assets/fix.svg) <!--ACP2E-2097-->Die ReCaptcha-Validierung funktioniert jetzt beim Checkout-Prozess für ein B2B-Angebot ordnungsgemäß, wenn ReCaptcha V3 für den Storefront-Checkout konfiguriert ist. Zuvor schlug die Validierung mit einem `recaptcha validation failed, please try again` Fehlermeldung.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1825-->Kaufaufträge können von einem mit dem Unternehmen verbundenen Benutzer nicht mehr erteilt werden, nachdem das Unternehmen blockiert wurde. Zuvor konnte ein mit dem Unternehmen verbundener Benutzer Bestellungen aufgeben, wenn das Unternehmen blockiert wurde.

![Problem behoben](../assets/fix.svg)<!--ACP2E-1933-->Unternehmensadministratoren können nun Unternehmensbenutzer aus der Storefront hinzufügen. Zuvor hat Commerce einen Fehler protokolliert, wenn ein Admin-Benutzer versucht hat, einen neuen Benutzer hinzuzufügen: `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

## B2B v1.4.2

*10. Oktober 2023*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

Die Version B2B v1.4.2 enthält Qualitätsverbesserungen und Fehlerbehebungen

![Problem behoben](../assets/fix.svg) <!--B2B-2897-->Wenn ein Verkäufer ein Käuferangebot erstellt, das eine Produkt-SKU enthält, die nicht im freigegebenen Katalog mit dem Käuferunternehmen verfügbar ist, zeigt das System die Fehlermeldung an `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`.  Der Verkäufer kann das Angebot erst dann speichern, wenn er das nicht verfügbare Produkt entfernt. Zuvor wurde das Anführungszeichen mit der nicht verfügbaren SKU gespeichert und das Anführungszeichen konnte nicht in die Storefront geladen werden.

## B2B v1.4.1

*7. August 2023*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}[Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Kompatibel mit Adobe Commerce 2.4.7-beta1.

Die Version B2B v1.4.1 enthält Qualitätsverbesserungen und Fehlerbehebungen.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1825-->Kaufaufträge können von einem mit dem Unternehmen verbundenen Benutzer nicht mehr erteilt werden, nachdem das Unternehmen blockiert wurde. Zuvor konnte ein mit dem Unternehmen verbundener Benutzer Bestellungen aufgeben, wenn das Unternehmen blockiert wurde.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1943-->Der rücksortierte Status des Produkts wird jetzt korrekt auf der Storefront angezeigt. Zuvor wurden Produkte, die für den Versand verfügbar waren, fälschlicherweise als zurückbestellt identifiziert.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1862-->Wenn das Registrierungsformular für das Unternehmen ein Attribut vom Typ Kundendatei enthält, wird die bei der Registrierung hochgeladene Datei jetzt nach der Erstellung des Unternehmens in die Kontoinformationen für den Unternehmensadministrator eingefügt. Zuvor fehlte der Anhang.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1793-->Die Musterauswahl für ein konfigurierbares Produkt wird jetzt wie erwartet auf der Konfigurationsseite für das Anforderungslistenelement angezeigt. Zuvor wurde die Musterauswahl als Dropdown-Feld auf der Konfigurationsseite für das Anforderungslistenelement angezeigt.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1968-->Bei Verwendung von [Firmen-GraphQL-Abfrage](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) , um Unternehmensdetails zurückzugeben, werden die Ergebnisse jetzt erfolgreich ohne Fehler zurückgegeben.

## B2B v1.4.0

*13. Juni 2023*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}[Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Kompatibel mit Adobe Commerce 2.4.7-beta1

Diese Version enthält neue Funktionen und Verbesserungen für verhandelbare Anführungszeichen für B2B und mehrere Fehlerbehebungen.

![Neu](../assets/new.svg) Kompatibilität mit Adobe Commerce 2.4.7-Beta1 hinzugefügt.

![Neu](../assets/new.svg) **Vom Verkäufer initiierte Angebote**—Verkäufer können jetzt direkt über das Anführungszeichen und das Kundenraster in der Admin-Konsole ein Angebot für einen Käufer erstellen. Diese Funktion optimiert den Angebotsprozess und reduziert die Komplexität für Kunden. Wenn ein Kunde keine Bestellung initiiert hat, kann ein Verkäufer schnell im Namen des Kunden ein Angebot erstellen und den Verhandlungsprozess starten. Zuvor konnten Angebote nur vom Käufer oder von einem als Kunde angemeldeten Verkäufer aus dem Geschäft erstellt werden.

![Neu](../assets/new.svg) **Rabatte und Verhandlungen für Zeileneinträge**—<!--B2B-2440--> B2B-Käufer und -Verkäufer können nun innerhalb eines Angebots auf der Ebene des Zeileneintrags verhandeln, Rabatte anwenden und Notizen austauschen, bis eine Vereinbarung getroffen wurde. Die Erstellung und Aktualisierung von Notizen sind im Zeileneintrag- und Anführungsverlauf enthalten, um die Kommunikation zu verfolgen. Bisher konnten Käufer und Verkäufer nur Notizen austauschen und Rabatte auf Angebotsebene anwenden.

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt jetzt bei der Zahlung die korrekten Details an, wenn die Option Bestellungen kaufen aktiviert ist und ein virtuelles Angebot, das mit der PayPal-Zahlungsoption erstellt wurde, ausgewählt wurde. Zuvor wurden Summen unter diesen Bedingungen als null angezeigt.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1504--> Überprüfungsfehler treten nicht mehr auf, wenn Sie versuchen, ein Unternehmen mit einer Kreditbeschränkung von mehr als 999 zu speichern. Zuvor wurde für Unternehmenskreditlimits über 999 ein Kommatrennzeichen eingefügt, was zu einem Validierungsfehler führte, der die Speicherung von Updates verhinderte.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1474-->  Die ausgewählte Lieferadresse bleibt bei Bestellung mit einem verhandelbaren Angebot unverändert. Zuvor wurde bei der Bestellung die ausgewählte Lieferadresse in die standardmäßige Lieferadresse geändert.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1429--> In den Speicherkonfigurationseinstellungen für B2B-Funktionen muss die Variable **[!UICONTROL Enable Shared Catalog direct products price assigning]** -Feld ist jetzt automatisch deaktiviert. Auf der Storefront wird sie ausgeblendet, wenn die **[!UICONTROL Enable Company]** Einstellung oder **[!UICONTROL Enable Shared Catalog]** festgelegt ist auf **[!UICONTROL No]**.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1683--> Beim Erstellen eines Unternehmenskontos aus dem Storefront validiert Commerce jetzt die E-Mail-Adresse, bevor die Registrierung des Unternehmens verarbeitet wird. Wenn die E-Mail-Adresse ungültig ist, schlägt der Vorgang fehl und es werden keine Kontoaktualisierungen verarbeitet. Zuvor wurde ein Kundenkonto erstellt, selbst wenn die Anfrage zur Erstellung eines Unternehmenskontos aufgrund einer ungültigen E-Mail-Adresse fehlschlug.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1664--> Produkt-SKUs, die doppelte Anführungszeichen im freigegebenen Katalog und die Preisstruktur enthalten, verursachen keine Fehler mehr im Admin.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1498--> Die Konfiguration für die Anwendung Commerce wurde aktualisiert, um zu verhindern, dass Gastbenutzer Daten aus anderen Kundengruppen sehen.

### Bekanntes Problem

Wenn Sie B2B 1.4.0 installieren oder aktualisieren [Adobe Commerce-Version 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html), tritt der folgende Fehler auf:

```terminal
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

Sie können dieses Problem beheben, indem Sie manuelle Abhängigkeiten für das B2B-Sicherheitspaket hinzufügen, indem Sie manuelle Abhängigkeiten für das B2B-Sicherheitspaket mit einer [Stabilitäts-Tag](https://getcomposer.org/doc/04-schema.md#package-links). Anweisungen finden Sie in der [Adobe Commerce-Wissensdatenbank](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html).

## B2B v1.3.5

*14. März 2023*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) B2B-Version 1.3.5-p2 wurde veröffentlicht, um die Kompatibilität mit Adobe Commerce 2.4.6-p2 zu unterstützen.

![Neu](../assets/new.svg) B2B-Version 1.3.5-p1 wurde veröffentlicht, um die Kompatibilität mit Adobe Commerce 2.4.6-p1 zu unterstützen.

>[!NOTE]
>
>Nach dem Upgrade von Commerce von 2.4.6 auf [neueste Version](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6), stellen Sie sicher, dass Sie auf die unterstützte B2B 1.3.5 Patch-Version aktualisieren. Oder aktualisieren Sie die B2B-Erweiterung von Version 1.3.5 auf Version 1.4.0 oder höher, um die neuesten Funktionen zu erhalten.

![Neu](../assets/new.svg) Adobe Commerce 2.4.6 wird nun unterstützt.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-689--> Adobe Commerce zeigt jetzt bei der Zahlung die korrekten Details an, wenn die Option Bestellungen kaufen aktiviert ist und ein virtuelles Angebot, das mit der PayPal-Zahlungsoption erstellt wurde, ausgewählt wurde. Zuvor wurden Summen unter diesen Bedingungen als null angezeigt.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-609--> Die Liste der Kundengruppen für die **Browserkategorie zulassen** -Einstellung enthält keine Kundengruppen mehr, die sich auf freigegebene Kataloge beziehen.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-1244--> Das Kundenattribut &quot;Tax/VAT Number&quot;funktioniert jetzt wie erwartet mit Unternehmensadministratorkonten sowohl auf Admin- als auch auf Storefront. Zum Erstellen eines Unternehmenskontos sind keine benutzerdefinierten Steuer-/MwSt-Attribute mehr erforderlich. Zuvor hatte ein Händler, der ein Unternehmenskonto mit einem benutzerdefinierten Steuer-/MwSt-Attribut erstellte, sowohl auf der Storefront als auch in Admin einen Validierungsfehler ausgegeben.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-1236--> Die Deaktivierung der Funktion &quot;Freigegebener Katalog&quot;für einen bestimmten Bereich funktioniert jetzt ordnungsgemäß. Zuvor legte Adobe Commerce einen ungültigen Bereich fest, wenn ein Händler die Konfiguration eines freigegebenen Katalogs speicherte.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-1203--> Administratoren können jetzt benutzerdefinierte Attributwerte für Unternehmensbenutzer speichern. Zuvor konnten benutzerdefinierte Attribute für Unternehmensbenutzer nicht gespeichert werden.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-1221--> Leistungsprobleme werden durch die Validierung von Unternehmensberechtigungen behoben, die über GraphQL bereitgestellt werden, wenn bereits viele Unternehmensberechtigungen zugewiesen sind.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-1242--> Adobe Commerce gibt keinen Fehler mehr auf der Warenkorbseite aus, wenn die Schnellbestellung verwendet wird, um ein Produkt in einer Menge hinzuzufügen, die den verfügbaren Bestand überschreitet.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-1090--> Die Leistung von `SELECT` Die Vorgänge für Unternehmensberechtigungen wurden verbessert.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-2456--> Kategorieabfragen geben jetzt Produktpreise entsprechend den Store-Konfigurationseinstellungen zurück, wenn für die abgerufene Kategorie keine expliziten Kategorieberechtigungen festgelegt wurden.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-6829--> Die **[!UICONTROL Place Order]** -Schaltfläche funktioniert jetzt wie erwartet, wenn Sie einen Kauf mit einer genehmigten Angebotserstellung abschließen. Probleme mit dem verhandelbaren Kurs `negotiableQuoteCheckoutSessionPlugin` -Plug-in aufgelöst.

## B2B v1.3.4

*9. August 2022*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) Adobe Commerce 2.4.5 wird nun unterstützt.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce sendet keine E-Mail-Benachrichtigungen mehr, wenn ein vorhandenes Unternehmen durch einen API-Aufruf aktualisiert wird. E-Mails werden jetzt nur noch bei der Erstellung eines Unternehmens gesendet.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-406-->Adobe Commerce berechnet nun die Gesamtsumme eines verhandelbaren Kurses korrekt, wenn die Variable **[!UICONTROL Enable Cross Border Trade]** Die Einstellung für die Steuerberechnung ist aktiviert.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-322-->Konfigurierbare Produkte werden jetzt an die letzte Position in der Produktliste verschoben, nachdem der Lagerbestand aktualisiert wurde. **[!UICONTROL Move out of stock to the bottom]** -Einstellung aktiviert ist. Eine neue benutzerdefinierte Datenbankabfrage wird implementiert, um sicherzustellen, dass die Sortierreihenfolge des Elasticsearch-Index jetzt der Admin-aktivierten Sortierreihenfolge entspricht. Zuvor wurden konfigurierbare Produkte und ihre untergeordneten Produkte nicht an den unteren Rand der Liste verschoben, wenn diese Einstellung aktiviert war.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-308-->Die E-Mail zum Bestellvorgang berücksichtigt jetzt die E-Mail-Sendeeinstellung jeder Website in einer Bereitstellung für mehrere Sites. Eine Prüfung für die **[!UICONTROL Disable Email Communications]** wird der benutzerdefinierten Logik für E-Mail-Warteschlangen hinzugefügt. Zuvor hat Adobe Commerce die E-Mail-Sendeeinstellung für die sekundäre Website nicht berücksichtigt.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-302-->Der Titel des SKU-Felds auf der Seite &quot;Schnellbestellung&quot;wird für mehr Klarheit geändert.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-543-->Adobe Commerce zeigt jetzt eine informativere Fehlermeldung an, wenn ein Käufer eine ungültige SKU in die **SKU oder Produktname eingeben** -Feld.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-1753-->Die **[!UICONTROL Account Created in]** -Feld für einen Unternehmensadministrator behält jetzt den erwarteten Wert nach dem Speichern des Unternehmens bei.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-722 -->Die `customer` Die Abfrage gibt keine leeren Ergebnisse mehr zurück, wenn sie Anforderungslisten abruft, die nach `uid`.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-210 -->Es wurde ein Plug-in vor dem `collectQuoteTotals` -Aufforderung, sicherzustellen, dass die Gutschriften aus dem Geschäft nur einmal angewendet werden.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-665 -->Kunden werden jetzt zur Anmeldeseite weitergeleitet, wenn ihr Konto von einem Administrator aus dem Admin gelöscht wird. Zuvor hatte Adobe Commerce einen Fehler ausgegeben. Das Plug-in (`SessionPlugin`) Der Codeblock befindet sich jetzt in der `try…catch` blockieren. Zuvor war dieser Code nicht in den generischen Block zur Ausnahmebehandlung eingeschlossen.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-661 --> Drücken Sie auf der Seite &quot;Quick Order&quot;im Mobile-Modus auf **Eingabe** nach Eingabe eines gültigen Produktnamen oder einer gültigen SKU wechselt der Käufer nun wie erwartet zum nächsten Feld.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-607 -->Der Firmenname ist nun wie erwartet in den Abschnitten Rechnungsadresse und Lieferadresse des Checkout-Workflows sichtbar.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-375 -->Store-Gutschriften sind jetzt nicht verfügbar, wenn die Variable **[!UICONTROL Zero Subtotal Checkout]** Die Zahlungsmethode ist deaktiviert. Zuvor war das Kontrollkästchen Gutschrift speichern während der Bestellplatzierung durch den Administrator nicht funktionstüchtig. Die Anwendung hat die Bestellung nicht mit der Store-Gutschrift platziert und diesen Fehler angezeigt: `The requested Payment Method is not available`.

## B2B v1.3.3

*9. August 2022*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) Adobe Commerce 2.4.4 wird nun unterstützt.

![Problem behoben](../assets/fix.svg) <!--- MC-41985--> Die Zeit, die für die Aktualisierung von Adobe Commerce 2.3.x auf Adobe Commerce 2.4.x bei Implementierungen mit mehr als 100.000 Unternehmensrollen erforderlich ist, wurde erheblich verkürzt.

![Problem behoben](../assets/fix.svg) <!--- MC-42153--> Die POST `V1/order/:orderId/invoice` -Anfrage unterstützt jetzt die Erstellung von Teilrechnungen, wenn die **[!UICONTROL Payment on Account]** Zahlungsmethode aktiviert ist. Zuvor gab Adobe Commerce diesen Fehler aus: `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![Problem behoben](../assets/fix.svg) <!--- MC-41975--> PayPal Payflow Pro funktioniert jetzt wie erwartet mit B2B-verhandelbaren Kursofferten, wenn der Warenkorb des Kunden andere Produkte enthält. Adobe Commerce verarbeitet die Bestellung nun erfolgreich und sendet wie erwartet eine E-Mail an den Kunden. Zuvor hatte Adobe Commerce einen schwerwiegenden Fehler ausgegeben und eine Bestätigungs-E-Mail an den Kunden gesendet, in der Nullwerte enthalten waren.

![Problem behoben](../assets/fix.svg) <!--- MC-41819--> Die Paginierung wird jetzt korrekt auf der Ergebnisseite der Katalogsuche angezeigt, nachdem einige Produkte im freigegebenen Katalog ausgeschlossen wurden.

![Problem behoben](../assets/fix.svg) <!--- MC-42886--> Benutzerdefinierte Kundenattribute werden jetzt erwartungsgemäß gespeichert, wenn ein Unternehmensbenutzer in der Admin-Konsole erstellt oder gespeichert wird.

![Problem behoben](../assets/fix.svg) <!--- MC-42927--> Die **[!UICONTROL Submit]** -Schaltfläche im Formular Neues Unternehmen erstellen ist jetzt nach einem Klick deaktiviert, um mehrere Formularübermittlungen zu verhindern. Bisher konnten Sie dieses Formular mehrmals senden, indem Sie wiederholt auf diese Schaltfläche klickten, wodurch ein Fehler aufgetreten war.

![Problem behoben](../assets/fix.svg) <!--- MC-42787--> Adobe Commerce zeigt den Link zur Neuanordnung nicht mehr im Storefront an, wenn sich ein Käufer in einem Speicher anmeldet, für den die Neuanordnung deaktiviert wurde.

![Problem behoben](../assets/fix.svg) <!--- MC-43115--> Bei der Suche nach Schnellbestellungen nach SKU wird jetzt nicht mehr zwischen Groß- und Kleinschreibung unterschieden, wenn der freigegebene Katalog aktiviert ist.

![Problem behoben](../assets/fix.svg) <!--- MC-42203--> Sie können jetzt beim Erstellen eines Unternehmens eine Datei für ein Kundenattribut aktualisieren. Zuvor, als Sie versucht haben, ein Unternehmen mit einem Anhang vom Typ `File`, hat Adobe Commerce das Unternehmen nicht erstellt und diesen Fehler im Ausnahmeprotokoll protokolliert: `Something went wrong while saving file`.

![Problem behoben](../assets/fix.svg) <!--- MC-42242--> Sie können jetzt ein Unternehmen mit einem Kundenkonto erstellen, das über ein benutzerdefiniertes Attribut mit einer`File`) oder (`Image`). Wenn das Konto zuvor über eine dieser anpassbaren Optionen verfügte, wurde das Ladeprogramm für die Firmenbearbeitungsseite nicht aufgelöst, was die Bearbeitung von Firmendetails verhinderte.

![Problem behoben](../assets/fix.svg) <!--- MC-42268--> Die `products` -Abfrage gibt nun eine genaue `total_count` Feld, wenn der freigegebene Katalog aktiviert ist.

![Problem behoben](../assets/fix.svg) <!--- MC-42203-->  Sie können jetzt beim Erstellen eines Unternehmens eine Datei für ein Kundenattribut aktualisieren. Zuvor, als Sie versucht haben, ein Unternehmen mit einem Anhang vom Typ `File`, hat Adobe Commerce das Unternehmen nicht erstellt und diesen Fehler im Ausnahmeprotokoll protokolliert: `Something went wrong while saving file`.

![Problem behoben](../assets/fix.svg) <!--- MC-43178--> Die _Unternehmenskonfiguration_ und _Unternehmen erstellen_ Seiten funktionieren nun erwartungsgemäß, nachdem Sie eine Online-Versandmethode deaktiviert haben. Es wurde eine Überprüfung hinzugefügt, um die versuchte Verarbeitung deaktivierter Versandmodule zu verhindern. Zuvor wurde in Adobe Commerce dieser Fehler angezeigt: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![Problem behoben](../assets/fix.svg) <!--- MC-42214--> Die _Kategorie_ -Seite zeigt nun konsistente Produktdaten an, während Berechtigungen während der partiellen Indizierung generiert werden. Diesem Prozess wurde ein neuer partieller Indexer für Ordnerberechtigungen hinzugefügt. Zuvor waren die Daten, die angezeigt wurden, während der Indexer ausgeführt wurde, falsch.

![Problem behoben](../assets/fix.svg) <!--- MC-42567--> Die `categoryList` -Abfrage gibt jetzt die richtige Anzahl von Produkten zurück, wenn Katalogberechtigungen verwendet und Produkte einem freigegebenen Katalog zugewiesen werden.

![Problem behoben](../assets/fix.svg) <!--- MC-42528--> Die `categoryList` -Abfrage berücksichtigt jetzt Kategorieberechtigungen und gibt nur zulässige Kategorien zurück. Zuvor wurden alle zugewiesenen und nicht zugewiesenen Kategorien zurückgegeben.

![Problem behoben](../assets/fix.svg) <!--- MC-42399--> Die `rest/V1/company/{id}` Anfrage gibt jetzt zurück `is_purchase_order_enabled` -Attributwerten erwartungsgemäß.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-128--> Benutzerdefinierte Kundenattribute werden jetzt wie erwartet in der _Unternehmensadministrator_ Registerkarte.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-130--> Der Baustein Meine Wunschliste auf der Seite Mein Konto wird jetzt für Unternehmensadministratoren und Firmenbenutzer erwartungsgemäß angezeigt.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-133--> Quick Order-Fehler werden nicht mehr im Warenkorb angezeigt. Zuvor wurde dieser Fehler in Adobe Commerce im Warenkorb angezeigt, wenn die SKU nicht im Katalog gefunden wurde:  `The SKU was not found in the catalog`.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-194--> Der Speichervorgang für freigegebene Kataloge wurde optimiert, um eine schnellere Ausführung zu ermöglichen. Bisher konnte das Speichern eines freigegebenen Katalogs mit vielen Kundengruppen mehrere Minuten dauern.

![Problem behoben](../assets/fix.svg) <!--- MC-42240--> Adobe Commerce löscht jetzt alle Berechtigungen für Unterkategorien aus dem `sharedcatalog_category_permissions` -Tabelle, wenn die übergeordnete Kategorie gelöscht wird. Zuvor wurden nur die übergeordneten Kategoriedaten entfernt.

## B2B v1.3.2

*29. August 2022*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) Adobe Commerce 2.4.3 wird nun unterstützt.

![Problem behoben](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce sendet nun erfolgreich aktualisierte E-Mails zu abgelaufenen verhandelbaren Anführungszeichen. Bisher hat Adobe Commerce keine Update-E-Mails gesendet, wenn ein übertragbares Angebot abgelaufen ist.

![Problem behoben](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce sendet jetzt erfolgreich aktualisierte E-Mails über bald ablaufende und abgelaufene verhandelbare Anführungszeichen, wenn ein `cron` Auftrag fehlt.

### Firma

![Problem behoben](../assets/fix.svg) <!--- MC-41542--> Im Dropdown-Feld Neues Unternehmenskonto erstellen werden keine leeren Optionswerte mehr aufgeführt. Zuvor wurden die ersten beiden Optionswerte und der Ländercode `AN` leer waren.

![Problem behoben](../assets/fix.svg) <!--- MC-41260--> Klicken Sie auf **[!UICONTROL Return]** -Schaltfläche für eine Bestellung, die von einem Unternehmensbenutzer erstellt wurde, leitet einen Administrator jetzt wie erwartet zur Seite &quot;Rückkehr erstellen&quot;um. Zuvor wurde der Administrator zur Seite Auftragsverlauf umgeleitet.

![Problem behoben](../assets/fix.svg) <!--- MC-40798--> Adobe Commerce schlägt beim Ausführen der `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` Methode während `bin/magento setup:upgrade`. Zuvor verwendete Adobe Commerce bei der Initialisierung von Berechtigungen nicht die Batch-Größe für die Erfassung, sondern lud stattdessen eine Sammlung aller Unternehmensrollen ein.

![Problem behoben](../assets/fix.svg) <!--- MC-40551--> Unternehmensbenutzer können jetzt benutzerdefinierte Attributwerte von Kunden bearbeiten und aktualisieren. Zuvor waren diese Attribute nicht ordnungsgemäß an das Formular zum Erstellen und Bearbeiten von Benutzern gebunden. Ein Unternehmensbenutzer konnte andere Attributwerte eingeben, aber Adobe Commerce hat diese Werte nicht korrekt gespeichert.

![Problem behoben](../assets/fix.svg) <!--- MC-32653--> Die Ressourcenstruktur für Berechtigungen für Unternehmensrollen kann jetzt erwartungsgemäß übersetzt werden. Zuvor wurde die Berechtigungsstruktur nicht übersetzt, obwohl gültige Übersetzungsdateien vorhanden waren.

![Problem behoben](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce speichert jetzt benutzerdefinierte Kundenattributwerte für B2B-Benutzer erwartungsgemäß. Zuvor führte das Erstellen eines Unternehmenskontos mit benutzerdefinierten Kundenattributen zu einem Vorlagenfehler, und Adobe Commerce konnte das Formular nicht erfolgreich laden. Hinzufügen eines Arguments zum Layout von `company_create_account` Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) <!--- MC-41721--> Unternehmensbenutzerfilter wie &quot;Alle Benutzer anzeigen&quot;, &quot;Aktive Benutzer anzeigen&quot;und &quot;Inaktive Benutzer anzeigen&quot;funktionieren jetzt erwartungsgemäß. Zuvor führte das Filtern von Aktionen auf der Firmenbenutzerseite zu einem JavaScript-Fehler.

### Firmenguthaben

![Problem behoben](../assets/fix.svg) <!--- MC-41551--> Administratoren mit eingeschränkten Konten, die nur Berechtigungen auf Website-Ebene enthalten, können jetzt ein Unternehmen erstellen, das eine andere Währung als die Website verwendet.

![Problem behoben](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce sendet nun Unternehmens-E-Mails von der richtigen `from` E-Mail-Adresse und Umfang. Zuvor hat Adobe Commerce den Umfang der Website beim Versand einer Firmenkreditzuweisung oder bei der Aktualisierung einer E-Mail nicht berücksichtigt.

### Schnellbestellung

![Problem behoben](../assets/fix.svg) <!--- MC-42104--> Das Erstellen einer Bestellung mit der Schnellbestellung aus einer CSV-Datei funktioniert jetzt mit nicht vorhandenen SKUs erwartungsgemäß.

![Problem behoben](../assets/fix.svg) <!--- MC-40268--> Die Verwendung der Schnellreihenfolge für die Suche nach mehreren SKUs funktioniert jetzt erwartungsgemäß. Zuvor enthielten die Ergebnisse doppelte Einträge.

![Problem behoben](../assets/fix.svg) <!--- MC-40261--> Die Anzeige der hinzugefügten Produktliste behandelt jetzt in Kleinbuchstaben und Großbuchstaben eingegebene SKUs auf die gleiche Weise, wenn Sie SKUs verwenden, um während der Schnellbestellung mehrere Produkte auszuwählen.

![Problem behoben](../assets/fix.svg) <!--- MC-40225--> Durch die Verwendung von Quick Order werden jetzt Produkte in der vom Käufer angegebenen Menge hinzugefügt. Zuvor hat Adobe Commerce nur ein Produkt hinzugefügt, selbst wenn die vom Käufer angegebenen Mengen ein Produkt übersteigen.

![Problem behoben](../assets/fix.svg) <!--- MC-41283--> Die Funktion zum automatischen Vervollständigen von Schnellbestellungen funktioniert jetzt mit teilweisen SKUs.

![Problem behoben](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce zeigt jetzt Produkte an, die als **Nicht sichtbar** in der Liste mit automatischen Vorschlägen und Suchergebnissen der Schnellbestellseite.

![Problem behoben](../assets/fix.svg) <!--- MC-42402--> Käufer können jetzt das Schnellbestellformular verwenden, um mehrere Produkte von SKUs hinzuzufügen, die Großbuchstaben enthalten. Zuvor wurde nur das erste Produkt hinzugefügt.

### Negotiatives Zitat

![Problem behoben](../assets/fix.svg) <!--- MC-41232--> Käufer werden jetzt zur verhandelbaren Anführungsseite weitergeleitet, nachdem sie den Link in ein verhandelbares Anführungszeichen im URL-Feld eingefügt und sich erfolgreich angemeldet haben. Zuvor wurden Käufer zur Seite Mein Konto weitergeleitet.

![Problem behoben](../assets/fix.svg) <!--- MC-39317--> Die Neuanordnung funktioniert jetzt wie erwartet bei Bestellungen, die ein Produkt mit einer anpassbaren Datumsoption für ein Kundenkonto enthalten, das beim Checkout erstellt wurde. Zuvor hat Adobe Commerce die Neuanordnung nicht verarbeitet und diesen Fehler angezeigt: `The product has required options. Enter the options and try again`.

![Problem behoben](../assets/fix.svg) <!--- MC-39063--> Die Lieferadresse für ein übertragbares Angebot kann während des Auscheckens nicht mehr bearbeitet werden, wenn das Bestellmodul deaktiviert ist. Dieses Verhalten resultierte aus einer vorherigen Korrektur, bei der `isQuoteAddressLocked` wurde aus dem übertragbaren Anführungszeichen-Checkout-Renderer entfernt.

![Problem behoben](../assets/fix.svg) <!--- MC-38967--> Händler können jetzt Produkte von einem Admin zu einem verhandelbaren Angebot hinzufügen.

### Bestellungen

![Problem behoben](../assets/fix.svg) <!--- MC-39983--> Adobe Commerce zeigt jetzt eine informative Fehlermeldung wie erwartet an, wenn Sie eine Bestellung mit PayPal Express Checkout aufgeben, wenn das **[!UICONTROL Name Prefix]** -Attribut auf `required`. Zuvor hat Adobe Commerce die Bestellung nicht platziert oder eine Fehlermeldung angezeigt.

![Problem behoben](../assets/fix.svg) <!--- MC-39620--> Die UI-Komponente für die Abrechnungsadresse im Modul &quot;Bestellung&quot;verwendet jetzt die Anführungsadresse richtig, wenn Google Tag Manager aktiviert ist. Zuvor trat auf der Zahlungsseite ein JavaScript-Fehler auf.

### Anforderungslisten

![Problem behoben](../assets/fix.svg) <!--- MC-40426--> Händler können jetzt die POST verwenden `rest/all/V1/requisition_lists` -Endpunkt, um eine Anforderungsliste für einen Kunden zu erstellen. Zuvor hatte Adobe Commerce diesen 400-Fehler ausgegeben, als Sie versuchten, eine Anforderungsliste zu erstellen: `Could not save Requisition List`.

![Problem behoben](../assets/fix.svg) <!--- MC-41123--> Die **[!UICONTROL Add to Requisition List]** -Schaltfläche wird nun für die in einem Warenkorb befindlichen Produkte angezeigt, wenn der Warenkorb auch nicht vorrätige Produkte enthält. Wenn ein Warenkorb zuvor zwei Produkte enthielt, von denen eines nicht vorrätig war, wurde die _[!UICONTROL Add to Requisition List]_für keines der Produkte angezeigt.

![Problem behoben](../assets/fix.svg) <!--- MC-40877--> Sie können jetzt die REST-API verwenden, um ein Produkt zu einer Anforderungsliste hinzuzufügen.

![Problem behoben](../assets/fix.svg) <!--- MC-40155--> Anforderungsliste **[!UICONTROL Latest Activity Date]** -Werte entsprechen jetzt dem Gebietsschema-Format.

![Problem behoben](../assets/fix.svg) <!--- MC-39580--> Adobe Commerce gibt keinen schwerwiegenden Fehler mehr aus, wenn Sie ein Bundle-Produkt aus einer Anforderungsliste bearbeiten.

![Problem behoben](../assets/fix.svg) <!--- MC-40454--> Adobe Commerce zeigt jetzt den richtigen Produktpreis an, wenn Sie ein Produkt mit einer anpassbaren Option hinzufügen `(File)` auf eine Wunschliste aus einer Anforderungsliste. Der Link zur hochgeladenen Datei ist ebenfalls erwartungsgemäß sichtbar. Zuvor wurden in Adobe Commerce falsche Produktpreise angezeigt und der Link zur Datei nicht angezeigt.

![Problem behoben](../assets/fix.svg) <!--- MC-36383--> Produkte mit anpassbarer Option `(File)` kann nun aus einer Liste von Anforderungen in einen Warenkorb aufgenommen werden.

### Freigegebener Katalog

![Problem behoben](../assets/fix.svg) <!--- MC-40497--> Ein Administrator mit einer auf eine bestimmte Website beschränkten Rolle kann jetzt einen freigegebenen Katalog erstellen, anzeigen und bearbeiten. Zuvor hatte Adobe Commerce einen schwerwiegenden Fehler ausgegeben, wenn ein Administrator mit einer eingeschränkten Rolle versuchte, einen freigegebenen Katalog zu erstellen.

![Problem behoben](../assets/fix.svg) <!--- MC-41337--> Die Navigationsergebnisse mit Ebenen enthalten jetzt eine genaue Anzahl von Produkten mit gefilterten Attributen, und Käufer können jetzt mehrere Filter anwenden. Zuvor konnte nur ein Filter angewendet werden, und in Adobe Commerce wurde in der Navigation mit Ebenen eine ungenaue Produktanzahl angezeigt.

![Problem behoben](../assets/fix.svg) <!--- MC-40779--> Adobe Commerce zeigt in den Suchergebnissen nun Produktzahlen in Navigationsfiltern mit Ebenen korrekt an. Zuvor verwendete ein Plug-in für die Seite &quot;Suchergebnisse&quot;kein Elasticsearch, stellte aber eine neue Abfrage an die Datenbank bereit.

![Problem behoben](../assets/fix.svg) <!--- MC-39978--> Adobe Commerce löscht keine Stufenpreise mehr, wenn ein Händler alle Produkte aus einem standardmäßigen freigegebenen Katalog löscht.

![Problem behoben](../assets/fix.svg) <!--- MC-39802--> Filter werden jetzt nach der aktuellen Kategorie gefiltert und auf allen Seiten korrekt angezeigt, wenn freigegebene Kataloge aktiviert sind. Zuvor wurden Filter nur für die aktuelle Seite fälschlicherweise berechnet und nicht nach der aktuellen Kategorie gefiltert.

![Problem behoben](../assets/fix.svg) <!--- MC-39522--> Die GraphQL `products` -Abfrage gibt nicht mehr den Preisbereich und die Kategorie eines Produkts für Produkte zurück, die keinem freigegebenen Katalog zugewiesen sind, wenn der freigegebene Katalog aktiviert ist. Zuvor wurden durch die Abfrage die Aggregationen des Produkts zurückgegeben, obwohl das Produkt selbst nicht im `items` Array.

## B2B v1.3.1

*9. Februar 2021*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) Adobe Commerce 2.4.2 wird nun unterstützt.

![Neu](../assets/new.svg) Online-Zahlungsmethoden werden jetzt für Bestellungen unterstützt.

![Problem behoben](../assets/fix.svg) Beim Hinzufügen eines konfigurierbaren Produkts zum Warenkorb direkt aus einer Anforderungsliste, wenn dieses Produkt in einer vorherigen Bestellung verwendet wurde, wird kein Systemfehler mehr zurückgegeben.

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt jetzt die Registerkarte &quot;Meine Genehmigung erforderlich&quot;für Bestellungen korrekt an, wenn eine geteilte Datenbankkonfiguration bereitgestellt wird.

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt jetzt Details zu Bundle-Produkten und Geschenkkarten an, wenn Sie Bestellungen anzeigen.

![Problem behoben](../assets/fix.svg) Käufer werden jetzt wie erwartet umgeleitet, nachdem sie sich beim Browsen in einem Geschäft mit **[!UICONTROL Website Restriction]** aktiviert ist und **[!UICONTROL Restriction Mode]** auf `Private Sales: Login Only`. Zuvor wurden Käufer zur Homepage des Stores weitergeleitet. <!--- MC-38934-->

![Problem behoben](../assets/fix.svg) Der Auftragsverlauf wird jetzt wie erwartet in Implementierungen mit einer B2B-Unternehmenshierarchie geladen, die viele Kunden enthält (mehr als 13000). Zuvor wurde der Auftragsverlauf langsam oder gar nicht geladen, und in Adobe Commerce trat ein 503-Fehler auf. <!--- MC-38830-->

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt nicht mehr mehrere identische Warnmeldungen an, wenn Sie ein nicht konfiguriertes Produkt mit anpassbaren Optionen auf einer Kategorieseite zu einer Anforderungsliste hinzufügen. <!--- MC-38342-->

![Problem behoben](../assets/fix.svg) Neue und duplizierte Produkte sind nun wie erwartet auf der Kategorieseite sichtbar, wenn freigegebene B2B-Kataloge aktiviert sind. <!--- MC-38307-->

![Problem behoben](../assets/fix.svg) Adobe Commerce behält jetzt die korrekten `store_id` , der bei der Aktualisierung der Kundengruppe für ein Unternehmen mit einem Unternehmensadministrator verknüpft ist. Zuvor wurde die Variable `store_id` zum Standardspeicher geändert, wenn die Gruppe aktualisiert wurde. <!--- MC-38196-->

![Problem behoben](../assets/fix.svg) Adobe Commerce speichert nun ein gruppiertes Produkt als Liste einfacher Produkte in einer Anforderungsliste, und zwar auf die gleiche Weise wie ein gruppiertes Produkt zum Warenkorb. Zuvor wurde die Verknüpfung für ein gruppiertes Produkt aus der Anforderungsliste immer zu einfachen Produkten und nicht zum gruppierten Produkt umgeleitet, da Adobe Commerce gruppierte Produkte speicherte. <!--- MC-38049-->

![Problem behoben](../assets/fix.svg) Sie können jetzt Bestellungen nach der **[!UICONTROL Company Name]** beim Exportieren von Bestellinformationen im CSV-Format. Zuvor hat Adobe Commerce einen Fehler in `var/export/{file-id}`. <!--- MC-37785-->

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt jetzt das Popup &quot;Anforderungsliste erstellen&quot;wie erwartet an, wenn Sie auf der Storefront die Registerkarte &quot;Neue Anforderungsliste erstellen&quot;auswählen. <!--- MC-37915-->

![Problem behoben](../assets/fix.svg) In Anforderungslisten sind nun alle gruppierten Produkte und Mengen enthalten, die der Liste hinzugefügt wurden. Wenn zuvor ein Händler nach dem Hinzufügen von Produkten von einer Produktdetailseite zu einer Anforderungsliste navigierte, wurde dieser Fehler in Adobe Commerce angezeigt: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![Problem behoben](../assets/fix.svg) Die richtige Store-Ansicht ist jetzt mit der entsprechenden Website verknüpft, wenn Sie ein Unternehmen in einer Bereitstellung für mehrere Sites erstellen. Zuvor war es nicht möglich, ein Unternehmen zu erstellen, und in Adobe Commerce wurde dieser Fehler angezeigt: `The store view is not in the associated website`. <!--- MC-37488-->

![Problem behoben](../assets/fix.svg) Die Bestellung von Produkten nach SKU mithilfe von Quick Order führt nicht mehr zu doppelten Produktmengen in der CSV-Datei. <!--- MC-37427-->

![Problem behoben](../assets/fix.svg) Die **[!UICONTROL Add to Cart]** -Schaltfläche wird nicht mehr blockiert, wenn die _[!UICONTROL Enter Multiple SKUs]_auf der Seite &quot;Quick Order&quot;einen leeren Wert enthält. Stattdessen zeigt Adobe Commerce jetzt eine Meldung an, in der Sie zur Eingabe gültiger SKUs aufgefordert werden. <!--- MC-37387-->

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt diese Meldung jetzt auf der Produktseite an, wenn Sie eine Produktüberprüfung von einer Anforderungsliste aus senden: `You submitted your review for moderation`. Die Überprüfung wird auch auf der Seite &quot;Ausstehende Überprüfungen&quot;(Admin) angezeigt. **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**). Zuvor hatte Adobe Commerce zwar die Überprüfung zur Liste der ausstehenden Überprüfungen hinzugefügt, aber auf der Produktseite einen 404-Fehler ausgegeben. <!--- MC-37119-->

![Problem behoben](../assets/fix.svg) Die Leistung der `sharedCatalogUpdateCategoryPermissions` Die Verbraucher wurden verbessert. Nach der Erstellung eines freigegebenen Katalogs verwendet der Indexer für Katalogberechtigungen jetzt nur die Kundengruppen-ID aus dem freigegebenen Katalog, nicht alle Kundengruppen. <!--- MC-36770-->

![Problem behoben](../assets/fix.svg) Benutzerdefinierte Kundenadressattributfelder, die mit der nicht standardmäßigen Adresse eines Käufers verknüpft sind, werden jetzt wie erwartet im Workflow zur Kasse des Storefront-Checkouts gespeichert. <!--- MC-36630-->

![Problem behoben](../assets/fix.svg) Bestellungen für Produkte, die zum standardmäßigen freigegebenen Katalog eines Stores gehören, können jetzt für Käufer über die Admin REST API (`rest/V1/carts/{<CART_ID>/items`). Adobe Commerce prüft jetzt, ob das Produkt einem öffentlichen Katalog zugewiesen wurde, bevor die Berechtigungen für freigegebene Kataloge in `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`. Zuvor hat Adobe Commerce das Produkt nicht zum Warenkorb des Käufers hinzugefügt und diesen Fehler ausgegeben: `No such shared catalog entity`. <!--- MC-36535-->

![Problem behoben](../assets/fix.svg) Adobe Commerce sendet jetzt E-Mails zur Registrierung neuer Unternehmensbenutzer von der Adresse des Adobe Commerce-Stores. Zuvor wurde diese E-Mail von der Adresse des Unternehmens-Administrators gesendet. <!--- MC-36480-->

![Problem behoben](../assets/fix.svg) Adobe Commerce überprüft jetzt benutzerdefinierte Attribute auf die Duplizierung reservierter Unternehmensattributnamen, bevor es einem Händler gestattet wird, ein neues Attribut zu speichern. <!--- MC-36282-->

![Problem behoben](../assets/fix.svg) Die `credit_history` -Abfrage gibt nun den Kreditverlauf des angegebenen Unternehmens sowohl für den ursprünglich zugewiesenen als auch für den gekauften Betrag zurück. Zuvor gab diese Abfrage einen Fehler zurück.

![Problem behoben](../assets/fix.svg) Die **[!UICONTROL Company]** und  **[!UICONTROL Job Title]** -Felder auf der Seite Kontoinformationen bearbeiten sind nicht mehr bearbeitbar.

### Bekannte Probleme

- B2B-Käufer können Online-Zahlungsmethoden verwenden, um den üblichen Bestellfluss zu umgehen. Dieses Szenario kann eintreten, wenn der Käufer seinen gesamten Checkout-Gesamtbetrag auf 0 reduzieren kann - z. B. durch einen Promo-Code oder eine Geschenkkarte - und dann den Code oder die Geschenkkarte entfernen kann. Auch unter diesen Bedingungen stellt Adobe Commerce die Bestellung für den korrekten Betrag auf der Grundlage der Preise der Artikel in ihrem zugewiesenen Katalog auf. **_Workaround_**: Deaktivieren Sie Geschenkgutscheine und Couponcodes, wenn die Online-Zahlungsmethoden für die Bestellvalidierung aktiviert sind. <!--- B2B-1603-->

- Käufer werden zum Warenkorb umgeleitet, wenn sie versuchen, eine Bestellung aus einer Bestellung über PayPal Express Checkout aufzugeben, wenn sie **[!UICONTROL In-Context Mode]** deaktiviert ist. <!--- B2B-1604-->

- Adobe Commerce zeigt manchmal den Fehler 404 an, wenn ein Käufer eine Bestellung erstellt und dann zur Checkout-Seite navigiert. Dieser Fehler tritt auf, wenn ein Käufer zuvor eine andere Bestellung mit einer Online-Zahlungsmethode erstellt hat, bevor er zur Checkout-Seite navigiert, ohne den vorherigen Kauf abzuschließen. Der Käufer kann die Bestellung weiterhin aufgeben. **_Arbeiten um_**: Keine. <!--- B2B-1605-->

- Rabatte für eine bestimmte Zahlungsmethode bleiben auch dann bestehen, wenn der Käufer beim letzten Kassengang seine Zahlungsmethode ändert. Daher können Kunden einen Rabatt erhalten, auf den sie keinen Anspruch haben. Dieses Problem tritt auf, weil trotz der Änderung der Zahlungsmethode weiterhin eine Warenkorbregel für die ursprüngliche Zahlungsmethode angewendet wird. **_Arbeiten um_**: Keine. Siehe [Bekanntes Problem bei Adobe Commerce 2.4.2 B2B: Rabatt bleibt für Online-Kaufaufträge erhalten, nachdem die Zahlungsmethode geändert wurde](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _Wissensdatenbank_ Artikel. <!-- B2B-1012 -->

- Die `deleteRequisitionListOutput` -Abfrage gibt Details zur gelöschten Anforderungsliste anstelle der verbleibenden Anforderungslisten zurück. <!--- MC-39894-->

## B2B v1.3.0

*15. Oktober 2020*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

Diese Version enthält Verbesserungen bei der Bestellvalidierung, Versandmethoden, Warenkorb und Protokollierung von Admin-Aktionen.

![Neu](../assets/new.svg) Adobe Commerce 2.4.1 wird nun unterstützt.

![Neu](../assets/new.svg) Die Genehmigungen für B2B-Bestellungen wurden verbessert, um die Benutzerfreundlichkeit zu verbessern und Massenaktionen bei Bestellungen zu ermöglichen.

![Neu](../assets/new.svg) B2B-Händler können jetzt die Versandmethoden steuern, die jedem Unternehmen angeboten werden.<!--- BUNDLE-160 161 162 -->

![Neu](../assets/new.svg) Merchants können es Benutzern nun ermöglichen, den Inhalt ihres Warenkorbs in einer einzigen Aktion zu löschen, und diese Funktion unabhängig auf jeder Website konfigurieren <!--- BUNDLE-108 -->

![Neu](../assets/new.svg) B2B-Käufer können jetzt einzelne Artikel oder den gesamten Inhalt ihres Warenkorbs direkt auf eine Anforderungsliste setzen. <!--- BUNDLE-145 144-->

![Neu](../assets/new.svg) B2B-Händler können Bestellungen vom Administrator im Namen von Kunden erstellen, die Zahlung auf Konto als Zahlungsmethode verwenden. <!--- BUNDLE-166 178-->

![Neu](../assets/new.svg) Händler können jetzt alle mit einem Benutzer verknüpften Angebote direkt auf der Detailseite des Kunden anzeigen. <!--- BUNDLE-139 -->

![Neu](../assets/new.svg) Händler können jetzt das Raster Kunden jetzt online nach Unternehmen filtern. <!--- BUNDLE-137 -->

![Neu](../assets/new.svg) Administratoren können jetzt Kunden im Admin nach Vertriebsmitarbeiter filtern. <!--- BUNDLE-110 -->

![Neu](../assets/new.svg) Um die Erstellung betrügerischer oder Spam-Konten zu reduzieren, können Händler Google reCAPTCHA jetzt im Formular &quot;Neue Unternehmensanfrage&quot;im Storefront aktivieren. <!--- BUNDLE-154 -->

![Neu](../assets/new.svg) In den Unternehmensmodulen durchgeführte Admin-Aktionen werden jetzt im Admin-Aktionsprotokoll protokolliert. Die Aktionen werden von allen relevanten Unternehmensmodulen protokolliert: `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`.  <!--- BUNDLE-180 181 182 183 -->

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt die **[!UICONTROL Delete customer]** Schaltfläche auf der **Kunden** Seite, wenn der angemeldete Administrator nicht berechtigt ist, Kunden in Bereitstellungen zu löschen, in denen B2B installiert ist. <!--- MC-35655-->

![Problem behoben](../assets/fix.svg) Die Kundengruppe wird nicht mehr automatisch für einen Kunden geändert, der einem Unternehmen zugewiesen wird, wenn Sie den Kunden im Kundenraster bearbeiten. <!--- MC-35254-->

![Problem behoben](../assets/fix.svg) Wenn ein Händler einen freigegebenen Katalog erstellt, werden die Berechtigungen jetzt automatisch auf `Allow` für die **[!UICONTROL Display Product Prices]** und **[!UICONTROL Add to Cart]** Funktionen in Kategorien, wenn der Kundengruppe dieser Zugriff in den Einstellungen für Katalogberechtigungen zugewiesen wird. Zuvor wurden diese Einstellungen automatisch auf `Deny` auch wenn die Katalogberechtigungen auf `Allow`.<!--- MC-34792-->

![Problem behoben](../assets/fix.svg) Berechtigungen für freigegebene Katalogkategorien werden nicht mehr überschrieben, wenn ein Produkt auf der Seite zur Produktbearbeitung bearbeitet wird.<!--- MC-34777-->

![Problem behoben](../assets/fix.svg) Adobe Commerce sendet jetzt eine E-Mail-Benachrichtigung, in der bestätigt wird, dass ein Kunde berechtigt ist, das festgelegte Kreditlimit zu überschreiten, wenn ein Händler die **[!UICONTROL Allow To Exceed Credit Limit]** -Einstellung. Zuvor wurde in der von Adobe Commerce gesendeten Benachrichtigungs-E-Mail angegeben, dass der Kunde nicht berechtigt war, die Beschränkung zu überschreiten. <!--- MC-34584-->

![Problem behoben](../assets/fix.svg) Der HTML-Container, der den Produktpreis auf Anforderungslisten umgibt, wird nun für die untergeordneten Elemente von gebündelten Produkten korrekt wiedergegeben. <!--- MC-36331-->

![Problem behoben](../assets/fix.svg) Händler können jetzt die Sprache festlegen, in der die Benutzer-E-Mail des Unternehmens gesendet wird, wenn ein Unternehmen in mehrsprachigen Bereitstellungen erstellt wird. Bisher konnten Händler über das Dropdown-Menü die entsprechende Store-Ansicht und Sprache nicht auswählen.  <!--- MC-35777-->

![Problem behoben](../assets/fix.svg) Benutzerdefinierte Felder für Kundenadressen-Attribute werden jetzt wie erwartet im Store-Front-Checkout-Workflow angezeigt. <!--- MC-35607-->

![Problem behoben](../assets/fix.svg) Die Registerkarte Konfiguration der B2B-Funktionen wird jetzt korrekt geöffnet. <!--- MC-35458-->Kunden können jetzt QuickOrder verwenden, um Produkte zum Warenkorb hinzuzufügen und dann erfolgreich Artikel zu entfernen. Zuvor wurde das Produkt nicht entfernt, wenn ein Käufer mit QuickOrder mehrere Produkte zum Warenkorb hinzufügte und dann ein Produkt entfernte. <!--- MC-35327-->

![Problem behoben](../assets/fix.svg) Ein Unternehmen kann jetzt mit der REST-API-PUT aktualisiert werden `/V1/company/:companyId` -Anfrage ohne Angabe der `region_id` wann der Status als konfiguriert ist **nicht erforderlich**. Zuvor wurde `region_id` nicht erforderlich war, gab Adobe Commerce einen Fehler aus, wenn er nicht angegeben wurde. <!--- MC-35304-->

![Problem behoben](../assets/fix.svg) Wenn Sie ein B2B-Unternehmen mithilfe der REST-API erstellen oder aktualisieren (`http://magento.local/rest/V1/company/2`, wobei `2` die Unternehmens-ID darstellt), enthält die Antwort jetzt die Einstellungen für `applicable_payment_method` oder `available_payment_methods` wie erwartet. <!--- MC-35248-->

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt keine 404-Seite mehr an, wenn ein Händler die Variable **Eingabe** -Schaltfläche anstatt auf **[!UICONTROL Save]** Schaltfläche beim Erstellen einer Anforderungsliste auf der Storefront.<!--- MC-35094-->

![Problem behoben](../assets/fix.svg) Kategorieberechtigungen ändern sich nicht mehr, wenn ein neues Produkt einem öffentlich freigegebenen Katalog zugewiesen wird. Zuvor wurden Kategorieberechtigungen dupliziert. <!--- MC-34386-->

![Problem behoben](../assets/fix.svg) PUT des REST-API-Endpunkts `rest/default/V1/company/{id}`nicht mehr zwischen Groß- und Kleinschreibung unterscheiden. <!--- MC-34308-->

![Problem behoben](../assets/fix.svg) Die Deaktivierung von Belohnungsmodulen wirkt sich nicht mehr auf B2B-Funktionen in Kundenkonten aus. Bisher wurden bei deaktivierten Belohnungsmodulen die folgenden Registerkarten für B2B-Fragen nicht angezeigt: Firmenprofil, Unternehmensbenutzer sowie Rollen und Berechtigungen.<!--- MC-34191-->

![Problem behoben](../assets/fix.svg) Adobe Commerce verwendet jetzt den richtigen Absendernamen in E-Mail-Benachrichtigungen, wenn Änderungen an Unternehmenskonten vorgenommen werden. Zuvor verwendete Adobe Commerce den allgemeinen Absendernamen des Kontakts, der im Standardbereich für alle E-Mails definiert war. <!--- MC-33917-->

![Problem behoben](../assets/fix.svg) Sie können jetzt erfolgreich Multishipping für Bestellungen implementieren, die sowohl physische als auch virtuelle Produkte enthalten. <!--- MC-33818-->

![Problem behoben](../assets/fix.svg) Händler können nun Unternehmensbenutzer über die _[!UICONTROL Company Users]_auf den Seiten &quot;Mein Konto&quot;und &quot;Unternehmensstruktur&quot;angezeigt, wenn **[!UICONTROL Access Restriction]**aktiviert ist und **[!UICONTROL Restriction Mode]**auf `Sales: Login Only`. Zuvor hatte Adobe Commerce diesen Fehler ausgegeben, wenn ein Händler versuchte, einen Benutzer zu erstellen: `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![Problem behoben](../assets/fix.svg) Adobe Commerce setzt die Kundengruppe eines Kunden nicht mehr auf den Standardwert zurück, wenn ein Kunde seine Kontoinformationen speichert. <!--- MC-33554-->

![Problem behoben](../assets/fix.svg) Adobe Commerce gibt keinen schwerwiegenden Fehler mehr aus, wenn ein Administrator einen Kunden, der einen aktiven Warenkorb hat, einer Kundengruppe zuweist. <!--- MC-33313-->

![Problem behoben](../assets/fix.svg) Adobe Commerce bietet jetzt eine `addToCart` Das DataLayer-Ereignis für die Schnellreihenfolge und Anforderung listet Seiten auf.  <!--- MC-33295-->

![Problem behoben](../assets/fix.svg) Benachrichtigungs-E-Mails, die an Vertriebsmitarbeiter gesendet werden, die einem Unternehmen zugewiesen sind, enthalten jetzt das zugewiesene Firmenlogo. Zuvor enthielt die Benachrichtigungs-E-Mail das standardmäßige LUMA-Logo und nicht das hochgeladene Firmenlogo. <!--- MC-33232-->

![Problem behoben](../assets/fix.svg) Eine Anforderungsliste enthält nun alle gruppierten Erzeugnisse und Mengen, die der Liste hinzugefügt wurden. Wenn zuvor ein Händler nach dem Hinzufügen von Produkten von einer Produktdetailseite zu einer Anforderungsliste navigierte, wurde dieser Fehler in Adobe Commerce angezeigt: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![Problem behoben](../assets/fix.svg) Die `products` -Abfrage gibt nun eine genaue `total_count` Feld, wenn der freigegebene Katalog aktiviert ist. <!--- MC-42268-->

![Problem behoben](../assets/fix.svg) Die Seiten &quot;Unternehmenkonfiguration&quot;und &quot;Unternehmen erstellen&quot;funktionieren jetzt erwartungsgemäß, nachdem Sie eine Online-Versandmethode deaktiviert haben. Es wurde eine Überprüfung hinzugefügt, um die versuchte Verarbeitung deaktivierter Versandmodule zu verhindern. Zuvor wurde in Adobe Commerce dieser Fehler angezeigt: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![Problem behoben](../assets/fix.svg) Der Speicherverbrauch für Integrationstests wurde reduziert, was die Testleistung verbessert und die für den Testabschluss erforderliche Zeit verkürzt. <!--- AC-266-->

## B2B v1.2.0

*28. Juli 2020*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) Adobe Commerce 2.4.0 wird nun unterstützt.

![Neu](../assets/new.svg) Storefront-Bestellsuche mit zusätzlichem Dank für Beiträge von Marek Mularczyk aus [Divante](https://www.divante.com/) und Community-Mitgliedern.

![Neu](../assets/new.svg) Bestellungen werden verbessert und neu geschrieben. Sie sind jetzt standardmäßig in Adobe Commerce enthalten.

![Neu](../assets/new.svg) Die Validierungsregeln für Bestellungen wurden implementiert. Mit diesen Regeln können Benutzer den Workflow &quot;Bestellung&quot;steuern, indem sie Regeln für den Kauf von Bestellungen erstellen.

![Neu](../assets/new.svg) Als Kunde anmelden ist jetzt standardmäßig in Adobe Commerce enthalten. Diese Funktion ermöglicht es Site-Mitarbeitern, Kunden zu unterstützen, indem sie sich als Kunde anmelden und sehen, was sie sehen.

![Problem behoben](../assets/fix.svg) Attributzusammenfassungen funktionieren jetzt für die mehrteilige Navigation mit Elasticsearch ordnungsgemäß

![Problem behoben](../assets/fix.svg) Die Suche nach Bestellungen nach Sonderzeichen funktioniert jetzt ordnungsgemäß.

![Problem behoben](../assets/fix.svg) Klicken Sie auf **[!UICONTROL Clear All]** Mit der Schaltfläche werden jetzt alle Filter erweitert, anstatt sie zu reduzieren.

![Problem behoben](../assets/fix.svg) Produkt-SKU/Name ist jetzt in der Suchfilterzusammenfassung für Auftragsverlauf enthalten.

![Problem behoben](../assets/fix.svg) Der Sortierindikator wird jetzt korrekt im Raster &quot;Meine Bestellung&quot;angezeigt.

![Problem behoben](../assets/fix.svg) Jetzt können Sie nur einmal auf die Schaltflächen Genehmigen, Abbrechen, Ablehnen und Bestellung klicken. Zuvor konnten Sie mehrmals auf die Schaltfläche klicken.

![Problem behoben](../assets/fix.svg) Die Schaltflächen &quot;Bestellung validieren&quot;, &quot;Ablehnen&quot;, &quot;Abbrechen&quot;und &quot;Validieren&quot;werden jetzt auf Mobilgeräten korrekt dargestellt.

![Problem behoben](../assets/fix.svg) Zuvor wurde bei der Genehmigung eines Kaufauftrags mit einem Rabatt, der abgelaufen ist, die Bestellung zum vollen Betrag platziert und die Bestellsumme nicht aktualisiert. Jetzt wird die Bestellsumme aktualisiert, um die korrekte Gesamtsumme anzuzeigen.

![Problem behoben](../assets/fix.svg) In Version 2.3.4 wurde ein Problem eingeführt, bei dem benutzerdefinierte Erweiterungsattribute nicht aus der Kundenadresse in die Anführungsadresse kopiert wurden. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Wenn B2B installiert ist, wird beim Zuweisen von Kategorien zu freigegebenen Katalogen ein SQL-Fehler angezeigt. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Aufgrund eines falschen Variablentypwerts konnten Administratoren einer Bestellung keine konfigurierbaren Produkte hinzufügen. Die Option-Dropdown-Listen werden nicht aufgefüllt. Diese Funktion funktioniert jetzt ordnungsgemäß.

![Problem behoben](../assets/fix.svg) Beim Bearbeiten von Kategorieberechtigungen für die Gruppe &quot;Nicht angemeldet&quot;trat bisher beim Speichern der Änderungen ein Fehler auf. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Es wurde eine Korrektur hinzugefügt, die es Store-Administratoren ermöglicht, Produkte zu einer Bestellung hinzuzufügen, die sich nicht im freigegebenen Katalog befindet. Zuvor wurde beim Hinzufügen eines Elements, das nicht im Katalog enthalten war, eine Fehlermeldung angezeigt.

![Problem behoben](../assets/fix.svg) Zuvor nach Ausführung des Befehls `php bin/magento indexer:set-dimensions-mode catalog_product_price website` und dann beim Versuch, einen freigegebenen Katalog zu erstellen, würde ein Fehler auftreten. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Beim Hinzufügen eines Unternehmens und Zuweisen des Unternehmens-Administrators zu einer nicht standardmäßigen Website wurde die falsche Site-ID gesendet, was zu einem Fehler führte. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Zuvor wurde, nachdem ein Kunde in eine andere Kundengruppe verschoben wurde, ein Produkt zu einer Bestellung hinzugefügt, indem _Schnellbestellung_ mit einem Fehler fehlschlagen. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Bisher wurde beim Versuch, mit der WebAPI mit einem B2B-Anführungszeichen auszuchecken, ein falscher Wert an die API gesendet, was zu einem Fehler führte. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Bislang trat bei der Einstellung eines Unternehmens über die API auf &quot;Aktiv&quot;ein Fehler auf. Dieses Problem wurde nun behoben.

![Problem behoben](../assets/fix.svg) Aufgrund einer nicht erforderlichen `form` -Tag, wird die Bestellseite automatisch aktualisiert, wenn Sie die Eingabetaste drücken, nachdem Sie eine geplante Versandgebühr geändert haben. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Bisher trat beim Festlegen einer Anzeigebegrenzung für ein Produkt auf einer Katalogseite, die kleiner war als die Anzahl der Produkte insgesamt, ein Fehler auf. Diese Funktion funktioniert jetzt wie erwartet.

![Problem behoben](../assets/fix.svg) Bisher wurde beim Ändern des Administrators eines Unternehmens die ursprüngliche Admin-Adresse in den neuen Administrator kopiert und gab ihnen zwei Adressen. Jetzt wird nur die richtige Adresse hinzugefügt.

![Problem behoben](../assets/fix.svg) Zuvor schlug die Verwendung der API zum Speichern eines Anführungselements fehl, wenn Git auf &quot;Zulässiger und Kunde benachrichtigen&quot;gesetzt war. Dieser API-Aufruf funktioniert jetzt erwartungsgemäß.

![Problem behoben](../assets/fix.svg) Die feste Produktsteuer wird jetzt auf der Detailseite Anführungszeichen angezeigt.

![Problem behoben](../assets/fix.svg) Bisher konnte die Datei nicht heruntergeladen werden, wenn Sie auf der Registerkarte &quot;Kommentare&quot;der Seite &quot;Meine Anführungszeichen&quot;auf einen Anhang geklickt haben. Dieses Verhalten funktioniert nun erwartungsgemäß.

### Bekannte Probleme

- Adobe Commerce gibt während der Aktualisierung auf B2B 1.2.0 in einer Bereitstellung auf mehreren Websites eine Ausnahme aus. Wann `setup:upgrade` ausgeführt wird, tritt dieser Fehler auf der `PurchaseOrder` -Modul: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **Workaround**: Installieren Sie die `B2B-716 Add NonTransactionableInterface` -Schnittstelle zu `InitPurchaseOrderSalesSequence` Datenpatch-Hotfix, der jetzt über das **Mein Konto** > **Downloads** Abschnitt `magento.com`.
- Wenn ein Rabattcode abläuft, bevor eine Bestellung (Bestellformular) genehmigt wurde, zeigt die Bestellstelle den diskontierten Betrag weiterhin an, aber sobald die Bestellung validiert wurde, wird der nicht abgezinste Gesamtbetrag angezeigt. **Workaround**: Installieren Sie die `B2B-709 Purchase Order Discount patch` Hotfix für dieses Problem, das jetzt im **Mein Konto** > **Downloads** Abschnitt `magento.com`.
- Wenn Artikel in einer Bestellung nicht vorrätig sind oder wenn die Menge beim Konvertieren der Bestellung in eine tatsächliche Bestellung unzureichend ist, tritt ein Fehler auf. Wenn Rückstände aktiviert sind, wird die Bestellung normal verarbeitet.
