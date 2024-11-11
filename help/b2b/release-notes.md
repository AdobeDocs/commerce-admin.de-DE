---
title: '[!DNL Adobe Commerce B2B] Versionshinweise'
description: Informationen zu Änderungen in [!DNL Adobe Commerce B2B] Versionen finden Sie in den Versionshinweisen .
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: ad2acb61acc3e7ace3421f51987939394f5d8cbe
workflow-type: tm+mt
source-wordcount: '7801'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B] Versionshinweise

Diese Versionshinweise für die B2B-Erweiterung erfassen Ergänzungen und Fehlerbehebungen, die Adobe während eines Versionszyklus hinzugefügt hat, einschließlich:

![Neu](../assets/new.svg) Neue Funktionen
![Korrektur des Problems](../assets/fix.svg) Fehlerbehebungen und Verbesserungen
![Bekanntes Problem](../assets/bug.svg) Bekannte Probleme

>[!NOTE]
>
>Informationen zu den für verfügbare Adobe Commerce-Versionen unterstützten Versionen der B2B Commerce-Erweiterung finden Sie unter [Produktverfügbarkeit](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) .


## B2B 1.5.0

*30. Oktober 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}
Kompatibel mit den Adobe Commerce-Versionen 2.4.8-Beta1, 2.4.7 bis 2.4.7-p2, 2.4.6 bis 2.4.6-p7

Version 1.5.0 von B2B umfasst neue Funktionen, Qualitätsverbesserungen und Fehlerbehebungen.

>[!NOTE]
>
> Erfahren Sie mehr über abwärtskompatible Änderungen (BICs), die in der Version B2B 1.5.0 eingeführt wurden, indem Sie die Highlights und Referenzinformationen im Thema [Abwärtsinkompatible Änderungen](backward-incompatible-changes.md) überprüfen.

### Unternehmensverwaltung

![Neu](../assets/new.svg) **Unternehmensverwaltung**<!--B2B-2901-->: Händler können Adobe Commerce-Unternehmen jetzt als hierarchische Organisationen anzeigen und verwalten, indem sie bestimmte Mutterunternehmen zuweisen. Nachdem ein Unternehmen einer Muttergesellschaft zugewiesen wurde, kann der Administrator des Mutterunternehmens das Unternehmenskonto verwalten. Nur autorisierte Admin-Benutzer können Unternehmenszuweisungen hinzufügen und verwalten. Weitere Informationen finden Sie unter [Verwalten der Unternehmenshierarchie](manage-company-hierarchy.md).

- Fügen Sie Unternehmenszuweisungen aus dem neuen Abschnitt &quot;*[!UICONTROL Company Hierarchy]*&quot;auf der Seite &quot;*[!UICONTROL Company Account]*&quot;im Admin hinzu und verwalten Sie sie.

- Sortieren und filtern Sie Unternehmen nach der neuen Einstellung *[!UICONTROL Company Type]* . Im Unternehmensraster gibt die Spalte *[!UICONTROL Company Type]* an, ob ein Unternehmen ein einzelnes Unternehmen oder Teil einer hierarchischen Struktur ist (über- oder untergeordnet).

![Neu](../assets/new.svg) **Verwalten der Unternehmenskonfiguration im Maßstab**<!--B2B-2849--> - Ändern Sie schnell die Konfigurationseinstellungen des Unternehmens für ausgewählte Unternehmen mithilfe der Massenaktion *[!UICONTROL Change company setting]* , die jetzt bei der Verwaltung von Unternehmen über das Raster *[!UICONTROL Companies]* oder *[!UICONTROL Company Hierarchy]* verfügbar ist. Wenn Sie beispielsweise einen neuen freigegebenen Katalog für eine Unternehmensgruppe erstellen, können Sie die freigegebene Katalogkonfiguration in einer einzigen Aktion ändern, anstatt jedes Unternehmen einzeln zu bearbeiten.

![Neu](../assets/new.svg) API-Entwickler können den neuen REST-API-Endpunkt &quot;Unternehmen Relations&quot;`/V1/company/{parentId}/relations` verwenden, um Unternehmenszuweisungen zu erstellen, anzuzeigen und zu entfernen. Siehe [Verwalten von Unternehmensobjekten](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) im *Web API Developer Guide*.

### Unternehmenskonten

![Neu](../assets/new.svg)<!--B2B-2828--> **Zuweisung mehrerer Unternehmen**: Vereinfachen Sie den Zugriff auf Unternehmenskonten für Unternehmensbenutzer, indem Sie einen Benutzer mehreren Unternehmen zuweisen. Wenn Sie beispielsweise einen Käufer haben, der von mehreren Firmen-Sites bestellt wird, erstellen Sie ein einziges Konto und weisen Sie alle Unternehmen, mit denen der Käufer arbeitet, diesem Konto zu. Dann kann sich der Käufer einmalig anmelden und zwischen den Unternehmenskonten wechseln, indem er das Unternehmen aus der Storefront auswählt.

>[!NOTE]
>
>Ein Unternehmensbenutzer kann mehreren Unternehmen zugewiesen werden, kann jedoch nur für ein Unternehmen als Unternehmensadministrator fungieren.

![New](../assets/new.svg) <!--B2B-2747--> **Auswahl des Unternehmensbereichs**: Bietet Benutzern des Unternehmens, die mehreren Unternehmen zugewiesen sind, die Möglichkeit, Unternehmen im Storefront zu wechseln. Wenn der Umfang geändert wird, werden die Daten aktualisiert, um die Informationen basierend auf dem neuen Unternehmenskontext anzuzeigen. Wenn das neue Unternehmen beispielsweise einen anderen freigegebenen Katalog verwendet, werden dem Benutzer des Unternehmens Produkte, Preise und andere Informationen basierend auf dem neuen freigegebenen Katalog angezeigt. Inhalte im Zusammenhang mit Bestellungen, Anführungszeichen, Angebotsvorlagen werden ebenfalls entsprechend dem Kontext des ausgewählten Unternehmens aktualisiert.

>[!NOTE]
>
>Wenn der Benutzer des Unternehmens Unternehmen mit Artikeln im Warenkorb wechselt, aktualisieren Sie den Warenkorb, um das Produktangebot, die Preise und Werberabatte basierend auf dem neuen Unternehmenskontext widerzuspiegeln.

![Problem behoben](../assets/fix.svg)<!--ACP2E-1933--> Unternehmensadministratoren können nun Unternehmensbenutzer aus dem Storefront hinzufügen. Zuvor hat Commerce einen Fehler protokolliert, wenn ein Admin-Benutzer versucht hat, einen neuen Benutzer hinzuzufügen: `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

### Anführungszeichenvorlagen

Verbesserungen der Anführungsfunktionen helfen Käufern und Verkäufern bei der effektiveren Verwaltung von Angeboten und Offering-Verhandlungen.

![Neu](../assets/new.svg) **Anführungsvorlagen**—<!--B2B-3367-->Käufer und Verkäufer können jetzt den Angebotsprozess optimieren, indem sie wiederverwendbare und anpassbare Anführungsvorlagen erstellen. Mithilfe von Angebotsvorlagen kann der Prozess der Angebotsverhandlung einmal abgeschlossen werden und Käufer können vorab genehmigte verknüpfte Angebote für wiederkehrende Bestellungen generieren, anstatt den Prozess der Angebotsverhandlung für jede Bestellung zu durchlaufen. Anführungsvorlagen erweitern die vorhandene Anführungsfunktion durch die folgenden erweiterten Funktionen:

- **Bestellschwellen** ermöglichen es den Verkäufern, Mindest- und Höchstbestellungsverpflichtungen festzulegen, um sicherzustellen, dass der Käufer vereinbarte Kaufmengen einhält.
- **Die Festlegung von Mindest- und Höchstmengen für die Artikelbestellung** gibt dem Käufer die Möglichkeit, die Bestellmengen für das verknüpfte Angebot anzupassen, ohne dass eine neue Vorlage oder weitere Verhandlungen erforderlich sind.
- **Verfolgen Sie die Anzahl der verknüpften Angebote, die generiert und erfolgreich abgeschlossen wurden**, um Einblicke in die Erfüllung ausgehandelter Vereinbarungen zu erhalten.
- **Verknüpfte Anführungszeichen** sind vorab genehmigte Anführungszeichen, die der Käufer aus einer aktiven Anführungsvorlage generiert, um wiederkehrende Bestellungen basierend auf den in der Anführungsvorlage ausgehandelten Bedingungen zu senden.

![Neu](../assets/new.svg) **Verbesserungen der vorhandenen Anführungsfunktionen**

- **Aktualisierte Regeln der Commerce Access Control List (ACL)** ermöglichen es B2B-Managern und -Aufsichtsbehörden, Anführungszeichen und Anführungszeichenvorlagen untergeordneter Benutzer zu verwalten. Separate Regeln unterstützen eine detaillierte Konfiguration für den Zugriff auf Ansicht, Bearbeitung und Löschung.

- **Zitat als Entwurf speichern**<!--B2B-2566-->: Beim Erstellen einer [Preisanfrage](quote-request.md) aus dem Warenkorb können Käufer das Angebot jetzt als Entwurf speichern, damit sie es überprüfen und aktualisieren können, bevor sie den Prozess der Preisverhandlungen mit dem Verkäufer starten. Das Ablaufdatum des Zitats im Entwurf ist nicht angegeben. Käufer können Entwurfsangebote im Abschnitt [!UICONTROL My Quotes] ihres Konto-Dashboards überprüfen und aktualisieren.

- **Zitat umbenennen**<!--B2B-2596-->: Käufer können jetzt einen Anführungsnamen auf der Seite [Anführungszeichen Detail](account-dashboard-my-quotes.md#quote-actions) ändern, indem sie die Option **[!UICONTROL Rename]** auswählen. Diese Option steht autorisierten Käufern zur Verfügung, wenn sie das Angebot bearbeiten. Namensänderungsereignisse werden im Anführungsverlauf-Protokoll aufgezeichnet.

- **Zitat duplizieren**<!--B2B-2701-->: Käufer und Verkäufer können jetzt ein neues Angebot erstellen, indem sie ein vorhandenes Angebot kopieren. Eine Kopie wird aus der Detailansicht des Zitats erstellt, indem Sie in der Detailansicht des Anführungszeichens [Anführungszeichen ](quote-price-negotiation.md#button-bar) in der Admin- oder Storefront [4} die Option **[!UICONTROL Create Copy]** auswählen.](account-dashboard-my-quotes.md#quote-actions)

- **Verschieben Sie das Anführungszeichen in die Anforderungsliste**<!--B2B-2755-->: Käufer haben jetzt die Möglichkeit, Produkte aus einem Angebot zu entfernen und in einer Anforderungsliste zu speichern, wenn sie sich entscheiden, sie nicht in den Anführungszeichenverhandlungsvorgang aufzunehmen.

- **Entfernen Sie mehrere Produkte aus einem Anführungszeichen**<!--B2B-2881-->: In Anführungszeichen mit einer großen Anzahl von Produkten können Käufer jetzt mehrere Produkte aus dem Anführungszeichen entfernen, indem sie sie auswählen und die Option *[!UICONTROL Remove]* aus dem Steuerelement *[!UICONTROL Actions]* auf der Anführungsdetailseite verwenden. In früheren Versionen musste ein Käufer Produkte einzeln löschen.

- **Sperren des Zeilendiskonts**<!--B2B-2597-->: Während der Preisverhandlungen können Verkäufer die Diskontsperre für Zeileneinträge verwenden, um beim Anwenden von Rabatten während des Anführungszeichenverhandelungsprozesses mehr Flexibilität zu erzielen. Beispielsweise kann ein Verkäufer einen Sonderrabatt für Zeileneinträge auf einen Artikel anwenden und den Artikel sperren, um weitere Rabatte zu vermeiden. Wenn ein Artikel gesperrt ist, kann der Artikelpreis nicht aktualisiert werden, wenn ein Rabatt auf Anführungszeichen angewendet wird. Siehe [Angebot für einen Käufer initiieren](sales-rep-initiates-quote.md).

![Korrektur des Fehlers](../assets/fix.svg) **Korrekturen für vorhandene Anführungsfunktionen**

- Händler, die in der Detailansicht des Zitats in der Admin-Ansicht auf die Schaltfläche *[!UICONTROL Print]* klicken, werden jetzt aufgefordert, das Angebot als PDF zu speichern. Zuvor wurden Händler zu einer Seite umgeleitet, die Anführungszeichendetails enthielt. <!--ACP2E-1984-->

- Beim Versand eines Kundenangebots mit dem Prozentsatz `0` und einer Mengenänderung löst der Administrator zuvor eine Ausnahme aus, speichert aber die Menge. Nachdem diese Korrektur angewendet wurde, wird für die ordnungsgemäße Ausnahme `0 percentage` mit einer Meldung ausgelöst. <!--ACP2E-1742-->

- Während der Preisverhandlungen kann ein Verkäufer nun im Feld Rabatt für verhandelte Angebote einen `0%` Rabatt angeben und das Angebot an den Käufer zurücksenden. Wenn der Verkäufer zuvor einen Rabatt von 0 % eingegeben und das Angebot an den Käufer zurückgesendet hat, hat der Administrator eine Fehlermeldung vom Typ `Exception occurred during quote sending` zurückgegeben. <!--ACP2E-1742-->

- Die ReCaptcha-Validierung funktioniert jetzt beim Checkout-Prozess für ein B2B-Angebot ordnungsgemäß, wenn ReCaptcha V3 für den Storefront-Checkout konfiguriert ist. Zuvor schlug die Validierung mit der Fehlermeldung `recaptcha validation failed, please try again` fehl.  <!--ACP2E-2097-->

### Bestellungen

![Korrektur des Problems](../assets/fix.svg) <!--ACP2E-1825-->Bestellungen können nicht mehr von einem mit dem Unternehmen verknüpften Benutzer aufgegeben werden, nachdem das Unternehmen blockiert wurde. Zuvor konnte ein mit dem Unternehmen verbundener Benutzer Bestellungen aufgeben, wenn das Unternehmen blockiert wurde.

## B2B v1.4.2-p3

*8. Oktober 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) Kompatibilität mit den Sicherheits-Patch-Versionen Adobe Commerce 2.4.7-p3+ und 2.4.6-p8+ hinzugefügt.

![Problem behoben](../assets/fix.svg) Umfasst die im [Sicherheitsbulletin APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html) dokumentierten Sicherheitskorrekturen.

>[!IMPORTANT]
>
>Adobe Commerce B2B Version 1.4.2+ ist kompatibel mit PHP 8.2. Wenn Sie die Commerce-Instanz auf Version 2.4.7+ aktualisieren, stellen Sie sicher, dass die Instanz PHP 8.2 verwendet, um die Kompatibilität mit der Adobe Commerce B2B-Version zu gewährleisten. Darüber hinaus unterstützt die Version B2B 1.4.2+ nicht den [GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

## B2B v1.4.2-p2

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) Kompatibilität mit den Sicherheits-Patch-Versionen Adobe Commerce 2.4.7-p2+ und 2.4.6-p7+ hinzugefügt.

![Problem behoben](../assets/fix.svg) Enthält die im Sicherheitsbulletin xxxx dokumentierten Sicherheitskorrekturen.

>[!IMPORTANT]
>
>Adobe Commerce B2B Version 1.4.2+ ist kompatibel mit PHP 8.2. Wenn Sie die Commerce-Instanz auf Version 2.4.7+ aktualisieren, stellen Sie sicher, dass die Instanz PHP 8.2 verwendet, um die Kompatibilität mit der Adobe Commerce B2B-Version zu gewährleisten. Darüber hinaus unterstützt die Version B2B 1.4.2+ nicht den [GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

## B2B v1.4.2-p1

*9. August 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) Kompatibilität mit den Sicherheits-Patch-Versionen Adobe Commerce 2.4.7-p1+ und 2.4.6-p6+ hinzugefügt.

>[!IMPORTANT]
>
>Adobe Commerce B2B Version 1.4.2+ ist kompatibel mit PHP 8.2. Wenn Sie die Commerce-Instanz auf Version 2.4.7+ aktualisieren, stellen Sie sicher, dass die Instanz PHP 8.2 verwendet, um die Kompatibilität mit der Adobe Commerce B2B-Version zu gewährleisten. Darüber hinaus unterstützt B2B 1.4.2+ derzeit nicht den [GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

## B2B v1.4.2

*10. Oktober 2023*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

Die Version B2B v1.4.2 enthält Qualitätsverbesserungen und Fehlerbehebungen.

![Korrektur des Problems](../assets/fix.svg) <!--B2B-2897-->Wenn ein Verkäufer ein Käuferangebot erstellt, das eine Produkt-SKU enthält, die nicht im freigegebenen Katalog verfügbar ist, der mit dem Käuferunternehmen verknüpft ist, zeigt das System die Fehlermeldung `The SKU you entered is not available in the shared catalog. Please check the SKU and try again` an.  Der Verkäufer kann das Angebot erst dann speichern, wenn er das nicht verfügbare Produkt entfernt. Zuvor wurde das Anführungszeichen mit der nicht verfügbaren SKU gespeichert und das Anführungszeichen konnte nicht in die Storefront geladen werden.

>[!IMPORTANT]
>
>Adobe Commerce B2B Version 1.4.2+ ist kompatibel mit PHP 8.2. Wenn Sie die Commerce-Instanz auf Version 2.4.7+ aktualisieren, stellen Sie sicher, dass die Instanz PHP 8.2 verwendet, um die Kompatibilität mit der Adobe Commerce B2B-Version zu gewährleisten. Darüber hinaus unterstützt B2B 1.4.2+ derzeit nicht den [GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

## B2B v1.4.1

*7. August 2023*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}[Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Kompatibel mit Adobe Commerce 2.4.7-beta1.

Die Version B2B v1.4.1 enthält Qualitätsverbesserungen und Fehlerbehebungen.

![Korrektur des Problems](../assets/fix.svg) <!--ACP2E-1825-->Bestellungen können nicht mehr von einem mit dem Unternehmen verknüpften Benutzer aufgegeben werden, nachdem das Unternehmen blockiert wurde. Zuvor konnte ein mit dem Unternehmen verbundener Benutzer Bestellungen aufgeben, wenn das Unternehmen blockiert wurde.

![Korrektur des Problems](../assets/fix.svg) <!--ACP2E-1943-->Der rücksortierte Status des Produkts wird jetzt korrekt auf der Storefront angezeigt. Zuvor wurden Produkte, die für den Versand verfügbar waren, fälschlicherweise als zurückbestellt identifiziert.

![Korrektur des Fehlers](../assets/fix.svg) <!--ACP2E-1862-->Wenn das Registrierungsformular für das Unternehmen ein Kundendateiattribut enthält, ist die beim Registrierungsprozess hochgeladene Datei nun nach der Erstellung des Unternehmens in den Kontoinformationen für den Unternehmensadministrator enthalten. Zuvor fehlte der Anhang.

![Korrektur des Fehlers](../assets/fix.svg) <!--ACP2E-1793-->Die Musterauswahl für ein konfigurierbares Produkt wird jetzt wie erwartet auf der Konfigurationsseite für das Anforderungslistenelement angezeigt. Zuvor wurde die Musterauswahl als Dropdown-Feld auf der Konfigurationsseite für das Anforderungslistenelement angezeigt.

![Korrektur des Problems](../assets/fix.svg) <!--ACP2E-1968-->Wenn die [Firmen-GraphQL-Abfrage](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) verwendet wird, um Unternehmensdetails zurückzugeben, werden die Ergebnisse jetzt erfolgreich ohne Fehler zurückgegeben.

## B2B v1.4.0

*13. Juni 2023*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}[Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Kompatibel mit Adobe Commerce 2.4.7-beta1

Diese Version enthält neue Funktionen und Verbesserungen für verhandelbare Anführungszeichen für B2B und mehrere Fehlerbehebungen.

![Neu](../assets/new.svg) Kompatibilität mit Adobe Commerce 2.4.7-beta1 hinzugefügt.

![Neu](../assets/new.svg) **Verkäufer initiierte Anführungszeichen**: Verkäufer können jetzt direkt über das Anführungszeichen und das Kundenraster im Admin ein Angebot für einen Käufer einleiten. Diese Funktion optimiert den Angebotsprozess und reduziert die Komplexität für Kunden. Wenn ein Kunde keine Bestellung initiiert hat, kann ein Verkäufer schnell im Namen des Kunden ein Angebot erstellen und den Verhandlungsprozess starten. Zuvor konnten Angebote nur vom Käufer oder von einem als Kunde angemeldeten Verkäufer aus dem Geschäft erstellt werden.

![Neu](../assets/new.svg) **Zeileneinkaufsrabatte und -verhandlungen**—<!--B2B-2440--> Mit einem Angebot können B2B-Käufer und -Verkäufer jetzt auf Zeileneintragsebene verhandeln, indem sie Rabatte anwenden und Notizen austauschen, bis eine Vereinbarung erreicht ist. Die Erstellung und Aktualisierung von Notizen sind im Zeileneintrag- und Anführungsverlauf enthalten, um die Kommunikation zu verfolgen. Bisher konnten Käufer und Verkäufer nur Notizen austauschen und Rabatte auf Angebotsebene anwenden.

![Korrektur des Fehlers](../assets/fix.svg) Adobe Commerce zeigt jetzt bei der Zahlung die richtigen Details an, wenn die Option &quot;Bestellungen kaufen&quot;aktiviert ist und ein virtuelles Angebot, das mit der PayPal-Zahlungsoption erstellt wurde, ausgewählt wurde. Zuvor wurden Summen unter diesen Bedingungen als null angezeigt.

![Korrektur des Problems](../assets/fix.svg) <!--ACP2E-1504--> Validierungsfehler treten nicht mehr auf, wenn Sie versuchen, ein Unternehmen mit einer Kreditbeschränkung von mehr als 999 zu speichern. Zuvor wurde für Unternehmenskreditlimits über 999 ein Kommatrennzeichen eingefügt, was zu einem Validierungsfehler führte, der die Speicherung von Updates verhinderte.

![Korrektur des Fehlers](../assets/fix.svg) <!--ACP2E-1474--> Die ausgewählte Lieferadresse bleibt jetzt unverändert, wenn Sie eine Bestellung mit einem verhandelbaren Angebot aufgeben. Zuvor wurde bei der Bestellung die ausgewählte Lieferadresse in die standardmäßige Lieferadresse geändert.

![Korrektur des Fehlers](../assets/fix.svg) <!--ACP2E-1429--> In den Speicherkonfigurationseinstellungen für B2B-Funktionen ist das Feld **[!UICONTROL Enable Shared Catalog direct products price assigning]** jetzt automatisch deaktiviert. Auf der Storefront ist sie ausgeblendet, wenn die Einstellung **[!UICONTROL Enable Company]** oder **[!UICONTROL Enable Shared Catalog]** auf **[!UICONTROL No]** gesetzt ist.

![Korrektur des Fehlers](../assets/fix.svg) <!--ACP2E-1683--> Beim Erstellen eines Unternehmenskontos aus der Storefront validiert Commerce jetzt die E-Mail-Adresse, bevor die Unternehmensregistrierung verarbeitet wird. Wenn die E-Mail-Adresse ungültig ist, schlägt der Vorgang fehl und es werden keine Kontoaktualisierungen verarbeitet. Zuvor wurde ein Kundenkonto erstellt, selbst wenn die Anfrage zur Erstellung eines Unternehmenskontos aufgrund einer ungültigen E-Mail-Adresse fehlschlug.

![Korrektur des Problems](../assets/fix.svg) <!--ACP2E-1664--> Produkt-SKUs, die doppelte Anführungszeichen im freigegebenen Katalog enthalten, und die Preisstruktur verursachen keine Fehler mehr im Admin.

![Korrektur des Fehlers](../assets/fix.svg) <!--ACP2E-1498--> Die Konfiguration für den Absturz der Commerce-Anwendung wurde aktualisiert, um zu verhindern, dass Gastbenutzer Daten aus anderen Kundengruppen sehen.

### Bekanntes Problem

Wenn Sie B2B 1.4.0 auf [Adobe Commerce-Version 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html) installieren oder aktualisieren, tritt der folgende Fehler auf:

```
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

Sie können dieses Problem beheben, indem Sie manuelle Abhängigkeiten für das B2B-Sicherheitspaket hinzufügen, indem Sie manuelle Abhängigkeiten für das B2B-Sicherheitspaket mit einem [Stabilitäts-Tag](https://getcomposer.org/doc/04-schema.md#package-links) hinzufügen. Anweisungen finden Sie in der [Adobe Commerce Knowledge Base](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html).

## B2B v1.3.5-p8

*8. Oktober 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) Kompatibilität mit den Sicherheits-Patch-Versionen Adobe Commerce 2.4.6-p8 hinzugefügt.

![Problem behoben](../assets/fix.svg) Umfasst die im [Sicherheitsbulletin APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html) dokumentierten Sicherheitskorrekturen.

## B2B v1.3.5-p7

*9. August 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) Kompatibilität mit den Sicherheits-Patch-Versionen von Adobe Commerce 2.4.6-p7 hinzugefügt.

## B2B v1.3.5

*14. März 2023*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) B2B-Version 1.3.5-p2 wurde veröffentlicht, um die Kompatibilität mit Adobe Commerce 2.4.6-p2 zu unterstützen.

![Neu](../assets/new.svg) B2B-Version 1.3.5-p1 wurde veröffentlicht, um die Kompatibilität mit Adobe Commerce 2.4.6-p1 zu unterstützen.

>[!NOTE]
>
>Nachdem Sie Commerce von 2.4.6 auf die [neueste Version](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6) aktualisiert haben, stellen Sie sicher, dass Sie auf die unterstützte B2B 1.3.5 Patch-Version aktualisieren. Oder aktualisieren Sie die B2B-Erweiterung von Version 1.3.5 auf Version 1.4.0 oder höher, um die neuesten Funktionen zu erhalten.

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.6 hinzugefügt.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-689--> Adobe Commerce zeigt jetzt bei der Zahlung die richtigen Details an, wenn die Option &quot;Bestellungen kaufen&quot;aktiviert ist und ein virtuelles Angebot, das mit der PayPal-Zahlungsoption erstellt wurde, ausgewählt wurde. Zuvor wurden Summen unter diesen Bedingungen als null angezeigt.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-609--> Die Liste der Kundengruppen für die Einstellung **Browsing Category zulassen** enthält keine Kundengruppen mehr, die mit freigegebenen Katalogen zusammenhängen.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-1244--> Das Kundenattribut &quot;Tax/VAT Number&quot;funktioniert jetzt wie erwartet mit Unternehmensadministratorkonten sowohl auf der Admin- als auch auf der Storefront. Zum Erstellen eines Unternehmenskontos sind keine benutzerdefinierten Steuer-/MwSt-Attribute mehr erforderlich. Zuvor hatte ein Händler, der ein Unternehmenskonto mit einem benutzerdefinierten Steuer-/MwSt-Attribut erstellte, sowohl auf der Storefront als auch in Admin einen Validierungsfehler ausgegeben.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-1236--> Die Deaktivierung der Funktion des freigegebenen Katalogs für einen bestimmten Bereich funktioniert jetzt ordnungsgemäß. Zuvor legte Adobe Commerce einen ungültigen Bereich fest, wenn ein Händler die Konfiguration eines freigegebenen Katalogs speicherte.

![Korrektur des Problems](../assets/fix.svg) <!--- ACP2E-1203--> Administratoren können jetzt benutzerdefinierte Kundenattributwerte für Unternehmensbenutzer speichern. Zuvor konnten benutzerdefinierte Attribute für Unternehmensbenutzer nicht gespeichert werden.

![Korrektur des Problems](../assets/fix.svg) <!--- ACP2E-1221--> Leistungsprobleme werden durch die Validierung von Unternehmensberechtigungen behoben, die über GraphQL bereitgestellt werden, wenn bereits viele Unternehmensberechtigungen zugewiesen sind.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-1242--> Adobe Commerce gibt keinen Fehler mehr auf der Warenkorbseite aus, wenn die Schnellbestellung zum Hinzufügen eines Produkts in einer Menge verwendet wird, die den verfügbaren Bestand überschreitet.

![Korrektur des Problems](../assets/fix.svg) <!--- ACP2E-1090--> Die Leistung von `SELECT` Vorgängen für Unternehmensberechtigungen wurde verbessert.

![Korrektur des Problems](../assets/fix.svg) <!--- ACP2E-2456--> Kategorieabfragen geben jetzt Produktpreise gemäß den Store-Konfigurationseinstellungen zurück, wenn keine expliziten Kategorieberechtigungen für die zu abgefragende Kategorie festgelegt wurden.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-6829--> Die Schaltfläche **[!UICONTROL Place Order]** funktioniert jetzt erwartungsgemäß, wenn ein Kauf mit einer genehmigten Anführungsanforderung abgeschlossen wird. Probleme mit dem verhandelbaren Anführungszeichen `negotiableQuoteCheckoutSessionPlugin` -Plug-in wurden behoben.

## B2B v1.3.4-p10

*9. Oktober 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.5-p10 hinzugefügt.

![Problem behoben](../assets/fix.svg) Umfasst die im [Sicherheitsbulletin APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html) dokumentierten Sicherheitskorrekturen.

## B2B v1.3.4

*9. August 2022*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.5 hinzugefügt.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce sendet keine E-Mail-Benachrichtigungen mehr, wenn ein bestehendes Unternehmen durch einen API-Aufruf aktualisiert wird. E-Mails werden jetzt nur noch bei der Erstellung eines Unternehmens gesendet.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-406-->Adobe Commerce berechnet jetzt korrekt die Gesamtsumme eines verhandelbaren Kurses, wenn die Steuerberechnungseinstellung **[!UICONTROL Enable Cross Border Trade]** aktiviert ist.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-322-->Konfigurierbare Produkte werden jetzt an die letzte Position in der Produktliste verschoben, nachdem der Lagerbestand aktualisiert wurde, wenn die Einstellung **[!UICONTROL Move out of stock to the bottom]** aktiviert ist. Eine neue benutzerdefinierte Datenbankabfrage wird implementiert, um sicherzustellen, dass die Sortierreihenfolge des Elasticsearch-Index jetzt der Admin-aktivierten Sortierreihenfolge entspricht. Zuvor wurden konfigurierbare Produkte und ihre untergeordneten Produkte nicht an den unteren Rand der Liste verschoben, wenn diese Einstellung aktiviert war.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-308-->Die E-Mail zum Bestellvorgang berücksichtigt jetzt die E-Mail-Sendeeinstellung jeder Website in einer Bereitstellung für mehrere Sites. Eine Prüfung für die Einstellung **[!UICONTROL Disable Email Communications]** wird der benutzerdefinierten Logik für E-Mail-Warteschlangen hinzugefügt. Zuvor hat Adobe Commerce die E-Mail-Sendeeinstellung für die sekundäre Website nicht berücksichtigt.

![Korrektur des Problems](../assets/fix.svg) <!--- ACP2E-302-->Der Titel des SKU-Felds auf der Seite &quot;Schnellbestellung&quot;wurde für mehr Klarheit geändert.

![Korrektur des Problems](../assets/fix.svg) <!--- ACP2E-543-->Adobe Commerce zeigt jetzt eine informativere Fehlermeldung an, wenn ein Käufer eine ungültige SKU in das Feld **SKU eingeben oder Produktname eingeben** eingibt.

![Korrektur des Problems](../assets/fix.svg) <!--- ACP2E-1753-->Das Feld **[!UICONTROL Account Created in]** für einen Unternehmensadministrator behält jetzt den erwarteten Wert nach dem Speichern des Unternehmens bei.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-722 -->Die `customer`-Abfrage gibt keine leeren Ergebnisse mehr zurück, wenn sie Anforderungslisten abruft, die durch `uid` gefiltert werden.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-210 -->Es wurde ein Plug-in vor dem `collectQuoteTotals` -Aufruf hinzugefügt, um sicherzustellen, dass Store-Gutschriften nur einmal angewendet werden.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-665 -->Kunden werden jetzt zur Anmeldeseite weitergeleitet, wenn ihr Konto von einem Administrator aus dem Admin gelöscht wird. Zuvor hatte Adobe Commerce einen Fehler ausgegeben. Der Plug-in-Codeblock (`SessionPlugin`) befindet sich jetzt im Block `try…catch` . Zuvor war dieser Code nicht in den generischen Block zur Ausnahmebehandlung eingeschlossen.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-661 --> Auf der Seite &quot;Quick Order&quot;im Mobile-Modus. Wenn Sie nach Eingabe eines gültigen Produktnamen oder einer gültigen SKU die Taste **Enter** drücken, wird der Käufer nun erwartungsgemäß zum nächsten Feld geleitet.

![Korrektur des Problems](../assets/fix.svg) <!--- ACP2E-607 -->Der Firmenname ist jetzt wie erwartet in den Abschnitten Rechnungsadresse und Lieferadresse des Checkout-Workflows sichtbar.

![Korrektur des Problems](../assets/fix.svg) <!--- ACP2E-375 -->Die Gutschrift für den Store ist jetzt nicht mehr verfügbar, wenn die **[!UICONTROL Zero Subtotal Checkout]** -Zahlungsmethode deaktiviert ist. Zuvor war das Kontrollkästchen Gutschrift speichern während der Bestellplatzierung durch den Administrator nicht funktionstüchtig. Die Anwendung hat die Bestellung nicht mit der Speichergutschrift platziert und diesen Fehler angezeigt: `The requested Payment Method is not available`.

## B2B v1.3.3

*9. August 2022*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.4 hinzugefügt.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-41985--> Die Zeit, die für die Aktualisierung von Adobe Commerce 2.3.x auf Adobe Commerce 2.4.x bei Implementierungen mit mehr als 100.000 Unternehmensrollen erforderlich ist, wurde erheblich verkürzt.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-42153--> Die POST `V1/order/:orderId/invoice` -Anfrage unterstützt jetzt die Erstellung von Teilrechnungen, wenn die **[!UICONTROL Payment on Account]** -Zahlungsmethode aktiviert ist. Zuvor hatte Adobe Commerce den folgenden Fehler ausgegeben: `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-41975--> PayPal Payflow Pro funktioniert jetzt wie erwartet mit einem B2B-verhandelbaren Angebot, wenn der Warenkorb des Kunden andere Produkte enthält. Adobe Commerce verarbeitet die Bestellung nun erfolgreich und sendet wie erwartet eine E-Mail an den Kunden. Zuvor hatte Adobe Commerce einen schwerwiegenden Fehler ausgegeben und eine Bestätigungs-E-Mail an den Kunden gesendet, in der Nullwerte enthalten waren.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-41819--> Die Paginierung wird jetzt auf der Ergebnisseite der Katalogsuche korrekt angezeigt, nachdem einige Produkte im freigegebenen Katalog ausgeschlossen wurden.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-42886--> Benutzerdefinierte Kundenattribute werden jetzt erwartungsgemäß gespeichert, wenn ein Unternehmensbenutzer in Admin erstellt oder gespeichert wird.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-42927--> Die Schaltfläche **[!UICONTROL Submit]** im Formular &quot;Neues Unternehmen erstellen&quot;ist jetzt nach einem Klick deaktiviert, um mehrere Formularübermittlungen zu verhindern. Bisher konnten Sie dieses Formular mehrmals senden, indem Sie wiederholt auf diese Schaltfläche klickten, wodurch ein Fehler aufgetreten war.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-42787--> Adobe Commerce zeigt den Link zur Neuanordnung nicht mehr auf der Storefront an, wenn sich ein Käufer in einem Store anmeldet, für den die Neuanordnung deaktiviert wurde.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-43115--> Bei der Schnellbestellsuche nach SKU wird jetzt nicht mehr zwischen Groß- und Kleinschreibung unterschieden, wenn der freigegebene Katalog aktiviert ist.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-42203--> Sie können jetzt eine Datei für ein Kundenattribut aktualisieren, wenn Sie ein Unternehmen erstellen. Zuvor, als Sie versuchten, ein Unternehmen mit einem Anhang vom Typ `File` zu erstellen, erstellte Adobe Commerce das Unternehmen nicht und protokollierte diesen Fehler im Ausnahmeprotokoll: `Something went wrong while saving file`.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-42242--> Sie können jetzt ein Unternehmen mit einem Kundenkonto erstellen, das über ein benutzerdefiniertes Attribut mit dem Typ (`File`) oder (`Image`) verfügt. Wenn das Konto zuvor über eine dieser anpassbaren Optionen verfügte, wurde das Ladeprogramm für die Firmenbearbeitungsseite nicht aufgelöst, was die Bearbeitung von Firmendetails verhinderte.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-42268--> Die `products`-Abfrage gibt jetzt ein genaues `total_count` -Feld zurück, wenn der freigegebene Katalog aktiviert ist.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-42203--> Sie können jetzt eine Datei für ein Kundenattribut aktualisieren, wenn Sie ein Unternehmen erstellen. Zuvor, als Sie versuchten, ein Unternehmen mit einem Anhang vom Typ `File` zu erstellen, erstellte Adobe Commerce das Unternehmen nicht und protokollierte diesen Fehler im Ausnahmeprotokoll: `Something went wrong while saving file`.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-43178--> Die Seiten _Unternehmenkonfiguration_ und _Unternehmen erstellen_ funktionieren jetzt erwartungsgemäß, nachdem Sie eine Online-Versandmethode deaktiviert haben. Es wurde eine Überprüfung hinzugefügt, um die versuchte Verarbeitung deaktivierter Versandmodule zu verhindern. Zuvor wurde in Adobe Commerce folgender Fehler angezeigt: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-42214--> Die Seite _Kategorie_ zeigt jetzt konsistente Produktdaten an, während Berechtigungen während der partiellen Indizierung generiert werden. Diesem Prozess wurde ein neuer partieller Indexer für Ordnerberechtigungen hinzugefügt. Zuvor waren die Daten, die angezeigt wurden, während der Indexer ausgeführt wurde, falsch.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-42567--> Die `categoryList`-Abfrage gibt jetzt die richtige Anzahl von Produkten zurück, wenn Katalogberechtigungen verwendet und Produkte einem freigegebenen Katalog zugewiesen werden.

![Problem behoben](../assets/fix.svg) <!--- MC-42528--> Die `categoryList`-Abfrage berücksichtigt jetzt Kategorieberechtigungen und gibt nur zulässige Kategorien zurück. Zuvor wurden alle zugewiesenen und nicht zugewiesenen Kategorien zurückgegeben.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-42399--> Die `rest/V1/company/{id}` -Anfrage gibt jetzt die `is_purchase_order_enabled` -Attributwerte wie erwartet zurück.

![Korrektur des Problems](../assets/fix.svg) <!--- ACP2E-128--> Benutzerdefinierte Kundenattribute werden jetzt wie erwartet auf der Registerkarte _Unternehmensadministrator_ angezeigt.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-130--> Der Baustein Meine Wunschliste auf der Seite Mein Konto wird jetzt für Unternehmensadministratoren und Firmenbenutzer erwartungsgemäß angezeigt.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-133--> Quick Order-Fehler werden nicht mehr im Warenkorb angezeigt. Zuvor wurde dieser Fehler in Adobe Commerce im Warenkorb angezeigt, wenn die SKU nicht im Katalog gefunden wurde: `The SKU was not found in the catalog`.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-194--> Die Speichervorgänge für freigegebene Kataloge wurden so optimiert, dass sie schneller ausgeführt werden. Bisher konnte das Speichern eines freigegebenen Katalogs mit vielen Kundengruppen mehrere Minuten dauern.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-42240--> Adobe Commerce löscht jetzt alle Berechtigungen für Unterkategorien aus der Tabelle `sharedcatalog_category_permissions`, wenn die übergeordnete Kategorie gelöscht wird. Zuvor wurden nur die übergeordneten Kategoriedaten entfernt.

## B2B v1.3.2

*29. August 2022*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.3 hinzugefügt.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce sendet jetzt erfolgreich aktualisierte E-Mails zu abgelaufenen verhandelbaren Anführungszeichen. Bisher hat Adobe Commerce keine Update-E-Mails gesendet, wenn ein übertragbares Angebot abgelaufen ist.

![Problem behoben](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce sendet jetzt erfolgreich aktualisierte E-Mails über bald ablaufende E-Mails und abgelaufene verhandelbare Anführungszeichen, wenn ein `cron` -Auftrag fehlt.

### Firma

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-41542--> Das Dropdown-Feld zum Erstellen eines neuen Unternehmenskontos für die Seite &quot;Land&quot;listet keine leeren Optionswerte mehr auf. Zuvor waren die ersten beiden Optionswerte und der Ländercode `AN` leer.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-41260--> Beim Klicken auf die Schaltfläche **[!UICONTROL Return]** für eine Bestellung, die von einem Unternehmensbenutzer erstellt wurde, wird nun ein Verwaltungsbenutzer wie erwartet zur Seite &quot;Rückkehr erstellen&quot;weitergeleitet. Zuvor wurde der Administrator zur Seite Auftragsverlauf umgeleitet.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-40798--> Adobe Commerce schlägt beim Ausführen der `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply`-Methode während `bin/magento setup:upgrade` nicht mehr mit einem Speicherfehler fehl. Zuvor verwendete Adobe Commerce bei der Initialisierung von Berechtigungen nicht die Batch-Größe für die Erfassung, sondern lud stattdessen eine Sammlung aller Unternehmensrollen ein.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-40551--> Unternehmensbenutzer können jetzt benutzerdefinierte Kundenattributwerte bearbeiten und aktualisieren. Zuvor waren diese Attribute nicht ordnungsgemäß an das Formular zum Erstellen und Bearbeiten von Benutzern gebunden. Ein Unternehmensbenutzer konnte andere Attributwerte eingeben, aber Adobe Commerce hat diese Werte nicht korrekt gespeichert.

![Problem behoben](../assets/fix.svg) <!--- MC-32653--> Die Ressourcenstruktur für Berechtigungen für Unternehmensrollen kann jetzt erwartungsgemäß übersetzt werden. Zuvor wurde die Berechtigungsstruktur nicht übersetzt, obwohl gültige Übersetzungsdateien vorhanden waren.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce speichert jetzt benutzerdefinierte Kundenattributwerte für B2B-Benutzer erwartungsgemäß. Zuvor führte das Erstellen eines Unternehmenskontos mit benutzerdefinierten Kundenattributen zu einem Vorlagenfehler, und Adobe Commerce konnte das Formular nicht erfolgreich laden. Durch Hinzufügen eines Arguments zum Layout von `company_create_account` wurde dieses Problem behoben.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-41721--> Unternehmensbenutzerfilter wie &quot;Alle Benutzer anzeigen&quot;, &quot;Aktive Benutzer anzeigen&quot;und &quot;Inaktive Benutzer anzeigen&quot;funktionieren jetzt erwartungsgemäß. Zuvor führte das Filtern von Aktionen auf der Firmenbenutzerseite zu einem JavaScript-Fehler.

### Firmenguthaben

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-41551--> Administratoren mit eingeschränkten Konten, die nur Berechtigungen auf Website-Ebene enthalten, können jetzt ein Unternehmen erstellen, das eine andere Währung als die Website verwendet.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce sendet nun Unternehmens-E-Mails von der richtigen `from` E-Mail-Adresse und dem korrekten Umfang. Zuvor hat Adobe Commerce den Umfang der Website beim Versand einer Firmenkreditzuweisung oder bei der Aktualisierung einer E-Mail nicht berücksichtigt.

### Schnellbestellung

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-42104--> Das Erstellen einer Bestellung mithilfe der Schnellbestellung aus einer CSV-Datei funktioniert jetzt wie erwartet mit nicht vorhandenen SKUs.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-40268--> Die Verwendung der Schnellreihenfolge zur Suche nach mehreren SKUs funktioniert jetzt erwartungsgemäß. Zuvor enthielten die Ergebnisse doppelte Einträge.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-40261--> Die Anzeige der hinzugefügten Produktliste behandelt jetzt in Kleinbuchstaben und Großbuchstaben eingegebene SKUs auf die gleiche Weise, wenn Sie SKUs verwenden, um während der Schnellbestellung mehrere Produkte auszuwählen.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-40225--> Bei der Verwendung der Schnellbestellung werden jetzt Produkte in der vom Käufer angegebenen Menge hinzugefügt. Zuvor hat Adobe Commerce nur ein Produkt hinzugefügt, selbst wenn die vom Käufer angegebenen Mengen ein Produkt übersteigen.

![Problem behoben](../assets/fix.svg) <!--- MC-41283--> Die Funktion zum automatischen Vervollständigen von Schnellbestellungen funktioniert jetzt mit teilweisen SKUs.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce zeigt jetzt Produkte an, die in der automatischen Liste mit Vorschlägen und Suchergebnissen der Schnellbestellseite als **Nicht einzeln sichtbar** konfiguriert wurden.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-42402--> Käufer können jetzt das Schnellbestellformular verwenden, um mehrere Produkte von SKUs hinzuzufügen, die Großbuchstaben enthalten. Zuvor wurde nur das erste Produkt hinzugefügt.

### Negotiatives Zitat

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-41232--> Käufer werden jetzt zur bearbeitbaren Anführungsseite weitergeleitet, nachdem sie den Link in ein umlauffähiges Anführungszeichen im URL-Feld eingefügt und sich erfolgreich angemeldet haben. Zuvor wurden Käufer zur Seite Mein Konto weitergeleitet.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-39317--> Die Neuanordnung funktioniert jetzt erwartungsgemäß bei Bestellungen, die ein Produkt mit einer anpassbaren Datumsoption für ein Kundenkonto enthalten, das beim Checkout erstellt wurde. Zuvor hat Adobe Commerce die Neuanordnung nicht verarbeitet und diesen Fehler angezeigt: `The product has required options. Enter the options and try again`.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-39063--> Die Lieferadresse für ein umlauffähiges Angebot kann beim Checkout nicht mehr bearbeitet werden, wenn das Modul &quot;Bestellung&quot;deaktiviert ist. Dieses Verhalten resultierte aus einer vorherigen Korrektur, bei der `isQuoteAddressLocked` aus dem umlauffähigen Anführungszeichen-Checkout-Renderer entfernt wurde.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-38967--> Händler können jetzt Produkte zu einem verhandelbaren Angebot vom Admin hinzufügen.

### Bestellungen

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-39983--> Adobe Commerce zeigt jetzt eine informative Fehlermeldung wie erwartet an, wenn Sie eine Bestellung mit PayPal Express Checkout aufgeben, wenn das Attribut **[!UICONTROL Name Prefix]** auf `required` gesetzt ist. Zuvor hat Adobe Commerce die Bestellung nicht platziert oder eine Fehlermeldung angezeigt.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-39620--> Die UI-Komponente für die Abrechnungsadresse im Bestellmodul verwendet jetzt die Anführungsadresse richtig, wenn Google Tag Manager aktiviert ist. Zuvor trat auf der Zahlungsseite ein JavaScript-Fehler auf.

### Anforderungslisten

![Korrektur des Problems](../assets/fix.svg) <!--- MC-40426--> Händler können jetzt den Endpunkt POST `rest/all/V1/requisition_lists` verwenden, um eine Anforderungsliste für einen Kunden zu erstellen. Zuvor hatte Adobe Commerce diesen 400-Fehler ausgegeben, als Sie versuchten, eine Anforderungsliste zu erstellen: `Could not save Requisition List`.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-41123--> Die Schaltfläche **[!UICONTROL Add to Requisition List]** wird jetzt für die Artikel in einem Warenkorb angezeigt, wenn der Warenkorb auch nicht vorrätige Produkte enthält. Wenn ein Warenkorb zuvor zwei Produkte enthielt, von denen eines nicht vorrätig war, wurde für keines der beiden Produkte die Schaltfläche _[!UICONTROL Add to Requisition List]_angezeigt.

![Problem behoben](../assets/fix.svg) <!--- MC-40877--> Sie können jetzt die REST-API verwenden, um ein Produkt zu einer Anforderungsliste hinzuzufügen.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-40155--> Die Werte der Anforderungsliste **[!UICONTROL Latest Activity Date]** entsprechen jetzt dem Gebietsschema-Format.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-39580--> Adobe Commerce gibt keinen schwerwiegenden Fehler mehr aus, wenn Sie ein Bundle-Produkt aus einer Anforderungsliste bearbeiten.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-40454--> Adobe Commerce zeigt jetzt den richtigen Produktpreis an, wenn Sie ein Produkt mit einer anpassbaren Option `(File)` zu einer Wunschliste aus einer Anforderungsliste hinzufügen. Der Link zur hochgeladenen Datei ist ebenfalls erwartungsgemäß sichtbar. Zuvor wurden in Adobe Commerce falsche Produktpreise angezeigt und der Link zur Datei nicht angezeigt.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-36383--> Produkte mit einer anpassbaren Option `(File)` können jetzt aus einer Anforderungsliste zum Warenkorb hinzugefügt werden.

### Freigegebener Katalog

![Problem behoben](../assets/fix.svg) <!--- MC-40497--> Ein Administrator mit einer auf eine bestimmte Website beschränkten Rolle kann jetzt einen freigegebenen Katalog erstellen, anzeigen und bearbeiten. Zuvor hatte Adobe Commerce einen schwerwiegenden Fehler ausgegeben, wenn ein Administrator mit einer eingeschränkten Rolle versuchte, einen freigegebenen Katalog zu erstellen.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-41337--> Die Navigationsergebnisse mit Ebenen enthalten jetzt eine genaue Anzahl von Produkten mit gefilterten Attributen, und Käufer können jetzt mehrere Filter anwenden. Zuvor konnte nur ein Filter angewendet werden, und in Adobe Commerce wurde in der Navigation mit Ebenen eine ungenaue Produktanzahl angezeigt.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-40779--> Adobe Commerce zeigt jetzt Produktzahlen in Navigationsfiltern mit Ebenen in Suchergebnissen korrekt an. Zuvor verwendete ein Plug-in für die Seite &quot;Suchergebnisse&quot;kein Elasticsearch, stellte aber eine neue Abfrage an die Datenbank bereit.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-39978--> Adobe Commerce löscht keine Stufenpreise mehr, wenn ein Händler alle Produkte aus einem standardmäßigen freigegebenen Katalog löscht.

![Korrektur des Fehlers](../assets/fix.svg) <!--- MC-39802--> Filter werden jetzt nach der aktuellen Kategorie gefiltert und auf allen Seiten korrekt angezeigt, wenn freigegebene Kataloge aktiviert sind. Zuvor wurden Filter nur für die aktuelle Seite fälschlicherweise berechnet und nicht nach der aktuellen Kategorie gefiltert.

![Korrektur des Problems](../assets/fix.svg) <!--- MC-39522--> Die GraphQL `products`-Abfrage gibt nicht mehr den Preisbereich und die Kategorie eines Produkts für Produkte zurück, die keinem freigegebenen Katalog zugewiesen sind, wenn der freigegebene Katalog aktiviert ist. Zuvor gab die Abfrage die Aggregationen des Produkts zurück, obwohl das Produkt selbst nicht im Array `items` zurückgegeben wurde.

## B2B v1.3.1

*9. Februar 2021*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.2 hinzugefügt.

![Neu](../assets/new.svg) Online-Zahlungsmethoden werden jetzt für Bestellungen unterstützt.

![Korrektur eines Problems](../assets/fix.svg) Beim Hinzufügen eines konfigurierbaren Produkts zum Warenkorb direkt aus einer Anforderungsliste, wenn dieses Produkt in einer vorherigen Bestellung verwendet wurde, wird kein Systemfehler mehr zurückgegeben.

![Korrektur des Fehlers](../assets/fix.svg) Adobe Commerce zeigt jetzt die Registerkarte &quot;Meine Genehmigung erforderlich&quot;für Bestellungen korrekt an, wenn eine geteilte Datenbankkonfiguration bereitgestellt wird.

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt jetzt Details zu Bundle-Produkten und Geschenkkarten an, wenn Sie Bestellungen anzeigen.

![Korrektur des Fehlers](../assets/fix.svg) Käufer werden jetzt erwartungsgemäß umgeleitet, nachdem sie sich beim Browsen in einem Store, in dem **[!UICONTROL Website Restriction]** aktiviert ist und **[!UICONTROL Restriction Mode]** auf `Private Sales: Login Only` eingestellt ist, bei ihrem Konto angemeldet haben. Zuvor wurden Käufer zur Homepage des Stores weitergeleitet. <!--- MC-38934-->

![Korrektur des Fehlers](../assets/fix.svg) Der Auftragsverlauf wird jetzt wie erwartet in Implementierungen mit einer B2B-Unternehmenshierarchie geladen, die viele Kunden (über 13000) enthält. Zuvor wurde der Auftragsverlauf langsam oder gar nicht geladen, und in Adobe Commerce trat ein 503-Fehler auf. <!--- MC-38830-->

![Korrektur des Problems](../assets/fix.svg) Adobe Commerce zeigt nicht mehr mehrere identische Warnmeldungen an, wenn Sie ein nicht konfiguriertes Produkt mit anpassbaren Optionen über eine Kategorieseite zu einer Anforderungsliste hinzufügen. <!--- MC-38342-->

![Problem behoben](../assets/fix.svg) Neue und duplizierte Produkte sind jetzt wie erwartet auf der Kategorieseite sichtbar, wenn freigegebene B2B-Kataloge aktiviert sind. <!--- MC-38307-->

![Korrektur des Fehlers](../assets/fix.svg) Adobe Commerce behält jetzt den korrekten `store_id` bei, der einem Unternehmensadministrator zugeordnet ist, wenn die Kundengruppe für ein Unternehmen aktualisiert wird. Zuvor wurde `store_id` zum Standardspeicher geändert, wenn die Gruppe aktualisiert wurde. <!--- MC-38196-->

![Problem behoben](../assets/fix.svg) Adobe Commerce speichert jetzt ein gruppiertes Produkt als Liste einfacher Produkte in einer Anforderungsliste, und zwar auf die gleiche Weise wie ein gruppiertes Produkt zum Warenkorb. Zuvor wurde die Verknüpfung für ein gruppiertes Produkt aus der Anforderungsliste immer zu einfachen Produkten und nicht zum gruppierten Produkt umgeleitet, da Adobe Commerce gruppierte Produkte speicherte. <!--- MC-38049-->

![Korrektur des Fehlers](../assets/fix.svg) Beim Export von Bestellinformationen im CSV-Format können Sie jetzt Bestellungen nach dem Feld **[!UICONTROL Company Name]** filtern. Zuvor hat Adobe Commerce einen Fehler in `var/export/{file-id}` <!--- MC-37785--> protokolliert.

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt jetzt das Popup &quot;Anforderungsliste erstellen&quot;wie erwartet an, wenn Sie die Registerkarte &quot;Neue Anforderungsliste erstellen&quot;im Storefront auswählen. <!--- MC-37915-->

![Problem behoben](../assets/fix.svg) Anforderungslisten enthalten jetzt alle gruppierten Produkte und Mengen, die der Liste hinzugefügt wurden. Zuvor, als ein Händler nach dem Hinzufügen von Produkten von einer Produktdetailseite zu einer Anforderungsliste navigierte, zeigte Adobe Commerce diesen Fehler: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![Problem behoben](../assets/fix.svg) Die richtige Store-Ansicht ist jetzt mit der entsprechenden Website verknüpft, wenn Sie ein Unternehmen in einer Bereitstellung mit mehreren Sites erstellen. Zuvor war es nicht möglich, ein Unternehmen zu erstellen, und in Adobe Commerce wurde der folgende Fehler angezeigt: `The store view is not in the associated website`. <!--- MC-37488-->

![Korrektur des Fehlers](../assets/fix.svg) Beim Bestellen von Produkten nach SKU mithilfe der Schnellbestellung werden in der CSV-Datei keine doppelten Produktmengen mehr erzeugt. <!--- MC-37427-->

![Korrektur des Fehlers](../assets/fix.svg) Die Schaltfläche **[!UICONTROL Add to Cart]** wird nicht mehr blockiert, wenn der Abschnitt _[!UICONTROL Enter Multiple SKUs]_der Seite &quot;Quick Order&quot;einen leeren Wert enthält. Stattdessen zeigt Adobe Commerce jetzt eine Meldung an, in der Sie zur Eingabe gültiger SKUs aufgefordert werden. <!--- MC-37387-->

![Korrektur des Problems](../assets/fix.svg) Adobe Commerce zeigt diese Meldung jetzt auf der Produktseite an, wenn Sie eine Produktüberprüfung von einer Anforderungsliste aus senden: `You submitted your review for moderation`. Die Überprüfung wird auch auf der Seite &quot;Ausstehende Prüfungen&quot;angezeigt (Admin **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**). Zuvor hatte Adobe Commerce zwar die Überprüfung zur Liste der ausstehenden Überprüfungen hinzugefügt, aber auf der Produktseite einen 404-Fehler ausgegeben. <!--- MC-37119-->

![Problem behoben](../assets/fix.svg) Die Leistung des `sharedCatalogUpdateCategoryPermissions` -Verbrauchers wurde verbessert. Nach der Erstellung eines freigegebenen Katalogs verwendet der Indexer für Katalogberechtigungen jetzt nur die Kundengruppen-ID aus dem freigegebenen Katalog, nicht alle Kundengruppen. <!--- MC-36770-->

![Korrektur des Fehlers](../assets/fix.svg) Benutzerdefinierte Kundenadressattributfelder, die mit der nicht standardmäßigen Adresse eines Käufers verknüpft sind, werden jetzt wie erwartet im Store-Kasse-Workflow gespeichert. <!--- MC-36630-->

![Problem behoben](../assets/fix.svg) Bestellungen für Produkte, die zum standardmäßigen freigegebenen Katalog eines Stores gehören, können jetzt über die Admin REST API (`rest/V1/carts/{<CART_ID>/items`) wie erwartet für Käufer platziert werden. Adobe Commerce prüft jetzt, ob das Produkt einem öffentlichen Katalog zugewiesen wurde, bevor die Katalogberechtigungen in `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave` validiert wurden. Zuvor hat Adobe Commerce das Produkt nicht zum Warenkorb des Kunden hinzugefügt und diesen Fehler ausgegeben: `No such shared catalog entity`. <!--- MC-36535-->

![Problem behoben](../assets/fix.svg) Adobe Commerce sendet jetzt E-Mails zur Registrierung neuer Unternehmensbenutzer von der Adresse des Adobe Commerce-Stores. Zuvor wurde diese E-Mail von der Adresse des Unternehmens-Administrators gesendet. <!--- MC-36480-->

![Problem behoben](../assets/fix.svg) Adobe Commerce überprüft jetzt benutzerdefinierte Attribute auf die Duplizierung reservierter Firmenattributnamen, bevor es einem Händler gestattet wird, ein neues Attribut zu speichern. <!--- MC-36282-->

![Korrektur des Fehlers](../assets/fix.svg) Die `credit_history` -Abfrage gibt jetzt den Kreditverlauf des angegebenen Unternehmens sowohl für den ursprünglich zugewiesenen Betrag als auch für den gekauften Betrag zurück. Zuvor gab diese Abfrage einen Fehler zurück.

![Korrektur des Fehlers](../assets/fix.svg) Die Felder **[!UICONTROL Company]** und **[!UICONTROL Job Title]** auf der Seite &quot;Kontoinformationen bearbeiten&quot;sind nicht mehr bearbeitbar.

### Bekannte Probleme

- B2B-Käufer können Online-Zahlungsmethoden verwenden, um den üblichen Bestellfluss zu umgehen. Dieses Szenario kann eintreten, wenn der Käufer seinen gesamten Checkout-Gesamtbetrag auf 0 reduzieren kann - z. B. durch einen Promo-Code oder eine Geschenkkarte - und dann den Code oder die Geschenkkarte entfernen kann. Auch unter diesen Bedingungen stellt Adobe Commerce die Bestellung für den korrekten Betrag auf der Grundlage der Preise der Artikel in ihrem zugewiesenen Katalog auf. **_Problemumgehung_**: Deaktivieren Sie Geschenkkarten und Couponcodes, wenn die Online-Zahlungsmethoden für die Bestellvalidierung aktiviert sind. <!--- B2B-1603-->

- Käufer werden zum Warenkorb weitergeleitet, wenn sie versuchen, eine Bestellung aus einer Bestellung mit PayPal Express Checkout aufzugeben, wenn **[!UICONTROL In-Context Mode]** deaktiviert ist. <!--- B2B-1604-->

- Adobe Commerce zeigt manchmal den Fehler 404 an, wenn ein Käufer eine Bestellung erstellt und dann zur Checkout-Seite navigiert. Dieser Fehler tritt auf, wenn ein Käufer zuvor eine andere Bestellung mit einer Online-Zahlungsmethode erstellt hat, bevor er zur Checkout-Seite navigiert, ohne den vorherigen Kauf abzuschließen. Der Käufer kann die Bestellung weiterhin aufgeben. **_Arbeite um_**: Keine. <!--- B2B-1605-->

- Rabatte für eine bestimmte Zahlungsmethode bleiben auch dann bestehen, wenn der Käufer beim letzten Kassengang seine Zahlungsmethode ändert. Daher können Kunden einen Rabatt erhalten, auf den sie keinen Anspruch haben. Dieses Problem tritt auf, weil trotz der Änderung der Zahlungsmethode weiterhin eine Warenkorbregel für die ursprüngliche Zahlungsmethode angewendet wird. **_Arbeite um_**: Keine. Siehe bekanntes Problem [Adobe Commerce 2.4.2 B2B: Rabatt bleibt für Online-Kaufaufträge erhalten, nachdem die Zahlungsmethode geändert wurde](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _Knowledge Base_ . <!-- B2B-1012 -->

- Die `deleteRequisitionListOutput` -Abfrage gibt Details zur gelöschten Anforderungsliste anstelle der verbleibenden Anforderungslisten zurück. <!--- MC-39894-->

## B2B v1.3.0

*15. Oktober 2020*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

Diese Version enthält Verbesserungen bei der Bestellvalidierung, Versandmethoden, Warenkorb und Protokollierung von Admin-Aktionen.

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.1 hinzugefügt.

![Neu](../assets/new.svg) Die Genehmigungen für B2B-Bestellungen wurden verbessert, um die Benutzerfreundlichkeit zu verbessern und Massenaktionen bei Bestellungen zu ermöglichen.

![Neu](../assets/new.svg) B2B-Händler können jetzt die Versandmethoden steuern, die jedem Unternehmen angeboten werden.<!--- BUNDLE-160 161 162 -->

![Neu](../assets/new.svg) Händler können Benutzern nun erlauben, den Inhalt ihres Warenkorbs in einer einzigen Aktion zu löschen, und diese Funktion auf jeder Website unabhängig konfigurieren <!--- BUNDLE-108 -->

![Neu](../assets/new.svg) B2B-Käufer können jetzt einzelne Artikel oder den gesamten Inhalt ihres Warenkorbs direkt zu einer Anforderungsliste hinzufügen. <!--- BUNDLE-145 144-->

![Neu](../assets/new.svg) B2B-Händler können Bestellungen vom Administrator im Namen von Kunden erstellen, die &quot;Zahlung auf Konto&quot;als Zahlungsmethode verwenden. <!--- BUNDLE-166 178-->

![Neu](../assets/new.svg) Händler können jetzt alle mit einem Benutzer verknüpften Anführungszeichen direkt auf der Detailseite des Kunden anzeigen. <!--- BUNDLE-139 -->

![Neu](../assets/new.svg) Händler können jetzt das Raster Kunden jetzt online nach Unternehmen filtern. <!--- BUNDLE-137 -->

![Neu](../assets/new.svg) Administratoren können jetzt Kunden im Admin nach Vertriebsmitarbeiter filtern. <!--- BUNDLE-110 -->

![Neu](../assets/new.svg) Um die Erstellung betrügerischer oder Spam-Konten zu reduzieren, können Händler jetzt Google reCAPTCHA im Formular &quot;Neue Unternehmensanfrage&quot;im Storefront aktivieren. <!--- BUNDLE-154 -->

![Neu](../assets/new.svg) In den Unternehmensmodulen durchgeführte Admin-Aktionen werden jetzt im Admin-Aktionsprotokoll protokolliert. Aktionen werden von allen relevanten Unternehmensmodulen protokolliert: `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`. <!--- BUNDLE-180 181 182 183 -->

![Korrektur des Fehlers](../assets/fix.svg) Adobe Commerce zeigt die Schaltfläche **[!UICONTROL Delete customer]** nicht mehr auf der Seite **Kunden** an, wenn der angemeldete Administrator nicht berechtigt ist, Kunden in Bereitstellungen zu löschen, in denen B2B installiert ist. <!--- MC-35655-->

![Korrektur des Problems](../assets/fix.svg) Die Kundengruppe wird nicht mehr automatisch für einen Kunden geändert, der einem Unternehmen zugewiesen ist, wenn Sie den Kunden im Kundenraster bearbeiten. <!--- MC-35254-->

![Korrektur des Fehlers](../assets/fix.svg) Wenn ein Händler einen freigegebenen Katalog erstellt, werden die Berechtigungen jetzt automatisch auf `Allow` für die Funktionen **[!UICONTROL Display Product Prices]** und **[!UICONTROL Add to Cart]** in Kategorien gesetzt, wenn der Kundengruppe dieser Zugriff in den Einstellungen für Katalogberechtigungen zugewiesen wird. Zuvor wurden diese Einstellungen automatisch auf `Deny` gesetzt, selbst wenn die Katalogberechtigungen auf `Allow` festgelegt waren.<!--- MC-34792-->

![Problem behoben](../assets/fix.svg) Berechtigungen für freigegebene Katalogkategorien werden nicht mehr überschrieben, wenn ein Produkt auf der Seite zur Produktbearbeitung bearbeitet wird.<!--- MC-34777-->

![Problem behoben](../assets/fix.svg) Adobe Commerce sendet jetzt eine E-Mail-Benachrichtigung, in der bestätigt wird, dass ein Kunde berechtigt ist, die festgelegte Kreditgrenze zu überschreiten, wenn ein Händler die Einstellung **[!UICONTROL Allow To Exceed Credit Limit]** aktiviert. Zuvor wurde in der von Adobe Commerce gesendeten Benachrichtigungs-E-Mail angegeben, dass der Kunde nicht berechtigt war, die Beschränkung zu überschreiten. <!--- MC-34584-->

![Problem behoben](../assets/fix.svg) Der HTML-Container, der den Produktpreis auf Anforderungslisten umgibt, wird jetzt für die untergeordneten Elemente von gebündelten Produkten korrekt wiedergegeben. <!--- MC-36331-->

![Problem behoben](../assets/fix.svg) Händler können jetzt die Sprache festlegen, in der die Benutzer-E-Mail des Unternehmens gesendet wird, wenn ein Unternehmen in mehrsprachigen Bereitstellungen erstellt wird. Bisher konnten Händler über das Dropdown-Menü die entsprechende Store-Ansicht und Sprache nicht auswählen.  <!--- MC-35777-->

![Korrektur des Problems](../assets/fix.svg) Benutzerdefinierte Felder für Kundenadressen-Attribute werden jetzt wie erwartet im Store-Front-Checkout-Workflow angezeigt. <!--- MC-35607-->

![Problem behoben](../assets/fix.svg) Die Registerkarte &quot;Konfiguration der B2B-Funktionen&quot;wird jetzt korrekt geöffnet. <!--- MC-35458-->Kunden können jetzt QuickOrder verwenden, um Produkte zum Warenkorb hinzuzufügen und dann erfolgreich Artikel zu entfernen. Zuvor wurde das Produkt nicht entfernt, wenn ein Käufer mit QuickOrder mehrere Produkte zum Warenkorb hinzufügte und dann ein Produkt entfernte. <!--- MC-35327-->

![Problem behoben](../assets/fix.svg) Ein Unternehmen kann jetzt mit der REST API-PUT `/V1/company/:companyId` -Anfrage aktualisiert werden, ohne dass die `region_id` angegeben wird, wenn der Status als **nicht erforderlich** konfiguriert ist. Zuvor gab Adobe Commerce einen Fehler aus, obwohl `region_id` nicht erforderlich war. <!--- MC-35304-->

![Korrektur eines Problems](../assets/fix.svg) Wenn Sie ein B2B-Unternehmen mithilfe der REST-API (`http://magento.local/rest/V1/company/2`) erstellen oder aktualisieren, bei dem `2` die Unternehmens-ID darstellt, enthält die Antwort jetzt die Einstellungen für `applicable_payment_method` oder `available_payment_methods` wie erwartet. <!--- MC-35248-->

![Korrektur des Fehlers](../assets/fix.svg) Adobe Commerce zeigt keine 404-Seite mehr an, wenn ein Händler beim Erstellen einer Anforderungsliste auf der Storefront die Schaltfläche **Enter** verwendet, anstatt auf die Schaltfläche **[!UICONTROL Save]** zu klicken.<!--- MC-35094-->

![Problem behoben](../assets/fix.svg) Kategorieberechtigungen ändern sich nicht mehr, wenn ein neues Produkt einem öffentlich freigegebenen Katalog zugewiesen wird. Zuvor wurden Kategorieberechtigungen dupliziert. <!--- MC-34386-->

![Korrektur des Fehlers](../assets/fix.svg) Beim REST-API-Endpunkt PUT `rest/default/V1/company/{id}`, der zum Aktualisieren der E-Mail-Adresse des Unternehmens verwendet wird, wird nicht mehr zwischen Groß- und Kleinschreibung unterschieden. <!--- MC-34308-->

![Korrektur des Fehlers](../assets/fix.svg) Die Deaktivierung von Belohnungsmodulen wirkt sich nicht mehr auf B2B-Funktionen in Kundenkonten aus. Bisher wurden bei deaktivierten Belohnungsmodulen die folgenden Registerkarten für B2B-Fragen nicht angezeigt: Firmenprofil, Unternehmensbenutzer sowie Rollen und Berechtigungen.<!--- MC-34191-->

![Problem behoben](../assets/fix.svg) Adobe Commerce verwendet jetzt den richtigen Absendernamen in E-Mail-Benachrichtigungen, wenn Änderungen an Unternehmenskonten vorgenommen werden. Zuvor verwendete Adobe Commerce den allgemeinen Absendernamen des Kontakts, der im Standardbereich für alle E-Mails definiert war. <!--- MC-33917-->

![Korrektur des Fehlers](../assets/fix.svg) Sie können jetzt erfolgreich den Multishipping für Bestellungen implementieren, die sowohl physische als auch virtuelle Produkte enthalten. <!--- MC-33818-->

![Korrektur des Problems](../assets/fix.svg) Händler können jetzt Unternehmensbenutzer aus dem Abschnitt _[!UICONTROL Company Users]_auf den Seiten Mein Konto und meine Unternehmensstruktur erstellen, wenn **[!UICONTROL Access Restriction]**aktiviert und **[!UICONTROL Restriction Mode]**auf `Sales: Login Only` eingestellt ist. Zuvor hatte Adobe Commerce diesen Fehler ausgegeben, als ein Händler versuchte, einen Benutzer zu erstellen: `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![Problem behoben](../assets/fix.svg) Adobe Commerce setzt die Kundengruppe eines Kunden nicht mehr auf den Standardwert zurück, wenn ein Kunde seine Kontoinformationen speichert. <!--- MC-33554-->

![Korrektur des Fehlers](../assets/fix.svg) Adobe Commerce gibt keinen schwerwiegenden Fehler mehr aus, wenn ein Administrator einem Kunden, der einen aktiven Warenkorb hat, einen Kundenkreis zuordnet. <!--- MC-33313-->

![Problem behoben](../assets/fix.svg) Adobe Commerce stellt jetzt ein `addToCart` DataLayer -Ereignis für die Seiten &quot;Schnellreihenfolge&quot;und &quot;Anforderung&quot;bereit.  <!--- MC-33295-->

![Korrektur des Fehlers](../assets/fix.svg) Benachrichtigungs-E-Mails, die an Vertriebsmitarbeiter gesendet werden, die einem Unternehmen zugewiesen sind, enthalten jetzt das zugewiesene Firmenlogo. Zuvor enthielt die Benachrichtigungs-E-Mail das standardmäßige LUMA-Logo und nicht das hochgeladene Firmenlogo. <!--- MC-33232-->

![Problem behoben](../assets/fix.svg) Eine Anforderungsliste enthält jetzt alle gruppierten Produkte und Mengen, die der Liste hinzugefügt wurden. Zuvor, als ein Händler nach dem Hinzufügen von Produkten von einer Produktdetailseite zu einer Anforderungsliste navigierte, zeigte Adobe Commerce diesen Fehler: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![Korrektur des Fehlers](../assets/fix.svg) Die `products` -Abfrage gibt jetzt ein genaues `total_count` -Feld zurück, wenn der freigegebene Katalog aktiviert ist. <!--- MC-42268-->

![Problem behoben](../assets/fix.svg) Die Seiten &quot;Unternehmenkonfiguration&quot;und &quot;Unternehmen erstellen&quot;funktionieren jetzt erwartungsgemäß, nachdem Sie eine Methode für den Online-Versand deaktiviert haben. Es wurde eine Überprüfung hinzugefügt, um die versuchte Verarbeitung deaktivierter Versandmodule zu verhindern. Zuvor wurde in Adobe Commerce folgender Fehler angezeigt: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![Korrektur des Fehlers](../assets/fix.svg) Der Speicherverbrauch für Integrationstests wurde reduziert, was die Testleistung verbessert und die für die Testabwicklung erforderliche Zeit verkürzt. <!--- AC-266-->

## B2B v1.2.0

*28. Juli 2020*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.0 hinzugefügt.

![Neu](../assets/new.svg) Storefront-Bestellsuche, mit einem zusätzlichen Dank für die Beiträge von Marek Mularczyk von [Divante](https://www.divante.com/) und Community-Mitgliedern.

![Neu](../assets/new.svg) Bestellungen werden verbessert und neu geschrieben. Sie sind jetzt standardmäßig in Adobe Commerce enthalten.

![Neu](../assets/new.svg) Die Validierungsregeln für Bestellungen wurden implementiert. Mit diesen Regeln können Benutzer den Workflow &quot;Bestellung&quot;steuern, indem sie Regeln für den Kauf von Bestellungen erstellen.

![Neu](../assets/new.svg) Anmeldung als Kunde ist jetzt standardmäßig in Adobe Commerce enthalten. Diese Funktion ermöglicht es Site-Mitarbeitern, Kunden zu unterstützen, indem sie sich als Kunde anmelden und sehen, was sie sehen.

![Problem behoben](../assets/fix.svg) Attribut-Aggregate funktionieren jetzt ordnungsgemäß für die mehrteilige Navigation mit Elasticsearch

![Korrektur des Fehlers](../assets/fix.svg) Suchaufträge nach Sonderzeichen funktionieren jetzt ordnungsgemäß.

![Korrektur des Fehlers](../assets/fix.svg) Beim Klicken auf die Schaltfläche **[!UICONTROL Clear All]** werden jetzt alle Filter erweitert, anstatt sie zu reduzieren.

![Problem behoben](../assets/fix.svg) Produkt-SKU/Name ist jetzt in der Suchfilterzusammenfassung für Auftragsverlauf enthalten.

![Korrektur eines Problems](../assets/fix.svg) Die Sortierungsanzeige wird jetzt korrekt im Raster &quot;Meine Bestellung&quot;angezeigt.

![Problem behoben](../assets/fix.svg) Jetzt können Sie nur einmal auf die Schaltflächen Genehmigen, Abbrechen, Ablehnen und Bestellung klicken. Zuvor konnten Sie mehrmals auf die Schaltfläche klicken.

![Korrektur des Fehlers](../assets/fix.svg) Die Schaltflächen &quot;Bestellung bestätigen&quot;, &quot;Ablehnen&quot;, &quot;Abbrechen&quot;und &quot;Validieren&quot;werden jetzt auf Mobilgeräten korrekt dargestellt.

![Korrektur des Fehlers](../assets/fix.svg) Zuvor wurde bei der Genehmigung einer Bestellung mit einem Rabatt, der abgelaufen ist, die Bestellung zum vollen Betrag platziert und die Bestellsumme nicht aktualisiert. Jetzt wird die Bestellsumme aktualisiert, um die korrekte Gesamtsumme anzuzeigen.

![Problem behoben](../assets/fix.svg) Ein Problem wurde in 2.3.4 behoben, bei dem benutzerdefinierte Erweiterungsattribute nicht aus der Kundenadresse in die Anführungsadresse kopiert wurden. Dieses Problem wurde behoben.

![Es wurde ein Problem behoben](../assets/fix.svg) Bei installiertem B2B wurde ein SQL-Fehler angezeigt, wenn Kategorien freigegebenen Katalogen zugewiesen wurden. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Aufgrund eines falschen Variablentypwerts konnten Administratoren einer Bestellung keine konfigurierbaren Produkte hinzufügen. Die Option-Dropdown-Listen werden nicht aufgefüllt. Diese Funktion funktioniert jetzt ordnungsgemäß.

![Korrektur des Fehlers](../assets/fix.svg) Zuvor trat beim Bearbeiten von Kategorieberechtigungen für die Gruppe &quot;Nicht angemeldet&quot;beim Speichern der Änderungen ein Fehler auf. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Es wurde ein Problem behoben, durch das Store-Administratoren Produkte zu einer Bestellung hinzufügen können, die nicht im freigegebenen Katalog enthalten ist. Zuvor wurde beim Hinzufügen eines Elements, das nicht im Katalog enthalten war, eine Fehlermeldung angezeigt.

![Korrektur des Fehlers](../assets/fix.svg) Zuvor trat ein Fehler auf, nachdem der Befehl `php bin/magento indexer:set-dimensions-mode catalog_product_price website` ausgeführt und dann versucht wurde, einen freigegebenen Katalog zu erstellen. Dieses Problem wurde behoben.

![Korrektur des Problems](../assets/fix.svg) Beim Hinzufügen eines Unternehmens und Zuweisen des Unternehmens-Administrators zu einer nicht standardmäßigen Website wurde die falsche Site-ID gesendet, was zu einem Fehler führte. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Zuvor schlug das Hinzufügen eines Produkts zu einer Bestellung mit _Quick Order_ fehl, nachdem ein Kunde in eine andere Kundengruppe verschoben wurde. Dieses Problem wurde behoben.

![Korrektur des Fehlers](../assets/fix.svg) Zuvor wurde beim Versuch, mit der WebAPI mit einem B2B-Anführungszeichen auszuchecken, ein falscher Wert an die API gesendet, was zu einem Fehler führte. Dieses Problem wurde behoben.

![Korrektur eines Problems](../assets/fix.svg): Zuvor trat ein Fehler auf, wenn ein Unternehmen über die API auf &quot;Aktiv&quot;gesetzt wurde. Dieses Problem wurde nun behoben.

![Korrektur des Fehlers](../assets/fix.svg) Aufgrund eines nicht benötigten `form` -Tags wurde die Bestellseite automatisch aktualisiert, wenn Sie die Eingabetaste gedrückt haben, nachdem Sie eine geplante Versandgebühr geändert haben. Dieses Problem wurde behoben.

![Korrektur des Fehlers](../assets/fix.svg) Zuvor trat ein Fehler auf, wenn ein Anzeigelimit für Produkte auf einer Katalogseite festgelegt wurde, das kleiner war als die Anzahl der Produkte insgesamt. Diese Funktion funktioniert jetzt wie erwartet.

![Problem behoben](../assets/fix.svg) Zuvor wurde beim Ändern des Administrators eines Unternehmens die ursprüngliche Admin-Adresse in den neuen Administrator kopiert und erhielte zwei Adressen. Jetzt wird nur die richtige Adresse hinzugefügt.

![Korrektur des Fehlers](../assets/fix.svg) Zuvor schlug die Verwendung der API zum Speichern eines Anführungselements fehl, wenn Git auf &quot;Zulässiger und Kunde benachrichtigen&quot;gesetzt war. Dieser API-Aufruf funktioniert jetzt erwartungsgemäß.

![Problem behoben](../assets/fix.svg) Die behobene Produktsteuer wird jetzt auf der Detailseite &quot;Anführungszeichen&quot;angezeigt.

![Korrektur des Fehlers](../assets/fix.svg) Zuvor konnte die Datei nicht heruntergeladen werden, wenn auf der Registerkarte &quot;Kommentare&quot;der Seite &quot;Meine Anführungszeichen&quot;auf einen Anhang geklickt wurde. Dieses Verhalten funktioniert nun erwartungsgemäß.

### Bekannte Probleme

- Adobe Commerce gibt während der Aktualisierung auf B2B 1.2.0 in einer Bereitstellung auf mehreren Websites eine Ausnahme aus. Wenn `setup:upgrade` ausgeführt wird, tritt dieser Fehler beim `PurchaseOrder`-Modul auf: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **Problemumgehung**: Installieren Sie die `B2B-716 Add NonTransactionableInterface` -Schnittstelle für den `InitPurchaseOrderSalesSequence`-DatenPatch-Hotfix, der jetzt im Abschnitt **Mein Konto** > **Downloads** von `magento.com` verfügbar ist.
- Wenn ein Rabattcode abläuft, bevor eine Bestellung (Bestellformular) genehmigt wurde, zeigt die Bestellstelle den diskontierten Betrag weiterhin an, aber sobald die Bestellung validiert wurde, wird der nicht abgezinste Gesamtbetrag angezeigt. **Problemumgehung**: Installieren Sie den Hotfix `B2B-709 Purchase Order Discount patch` für dieses Problem, der jetzt im Abschnitt **Mein Konto** > **Downloads** von `magento.com` verfügbar ist.
- Wenn Artikel in einer Bestellung nicht vorrätig sind oder wenn die Menge beim Konvertieren der Bestellung in eine tatsächliche Bestellung unzureichend ist, tritt ein Fehler auf. Wenn Rückstände aktiviert sind, wird die Bestellung normal verarbeitet.
