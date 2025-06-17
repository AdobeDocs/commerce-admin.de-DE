---
title: '[!DNL Adobe Commerce B2B] Versionshinweise'
description: Informationen zu Änderungen in Versionen finden Sie in  [!DNL Adobe Commerce B2B]  Versionshinweisen .
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: 706b62170507da90934eeff1d894865b27713b55
workflow-type: tm+mt
source-wordcount: '8867'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B] Versionshinweise

In diesen Versionshinweisen für die B2B-Erweiterung werden Ergänzungen und Fehlerbehebungen erfasst, die Adobe während eines Veröffentlichungszyklus hinzugefügt hat, darunter:

![Neu](../assets/new.svg) Neue Funktionen
![Problem behoben](../assets/fix.svg) Fehlerbehebungen und Verbesserungen
![Bekanntes Problem](../assets/bug.svg) Bekannte Probleme

>[!NOTE]
>
>Unter [Produktverfügbarkeit](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) finden Sie Informationen zu Versionen der B2B-Commerce-Erweiterung, die für verfügbare Adobe Commerce-Versionen unterstützt werden.

## B2B v1.5.2-p1

*10. Juni 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Sicherheitspatches der Adobe Commerce-Versionen 2.4.8-p1, 2.4.7-p6 und 2.4.6-p11.
Kompatibel mit Adobe Commerce 2.4.7 bis 2.4.7-p5, 2.4.6 bis 2.4.6-p10

![Problem behoben](../assets/fix.svg) Umfasst die in [Security Bulletin APSB25-50](https://helpx.adobe.com/security/products/magento/apsb25-50.html) dokumentierten Sicherheitskorrekturen.

## B2B 1.5.2

*8. April 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Sicherheitspatches der Adobe Commerce-Versionen 2.4.8, 2.4.7-p5 und 2.4.6-p10.
Kompatibel mit Adobe Commerce 2.4.7 bis 2.4.7-p4, 2.4.6 bis 2.4.6-p9

Die B2B-Version 1.5.2 enthält Qualitätsverbesserungen und Fehlerbehebungen.

### Unternehmensleitung

![Neu](../assets/new.svg)<!-- B2B-4123 -->Administratoren können jetzt mithilfe des Storefront-Umschalters mehrere Unternehmen von einem einzigen Konto aus verwalten. Zu den wichtigsten Vorteilen gehören:

- **Vereinfachte Verwaltung mehrerer Unternehmen** Administratoren können jetzt mehrere Unternehmen von einem Benutzerkonto aus überwachen, sodass keine separaten Anmeldungen für jedes Unternehmen erstellt und verwaltet werden müssen.
- **Effizienter Unternehmenswechsel** Eine intuitive Benutzeroberfläche ermöglicht Administratoren den schnellen Wechsel zwischen Unternehmen und Aktualisierungen, wodurch die Produktivität bei der Verwaltung mehrerer Entitäten verbessert wird.
- **Optimierte Abläufe** - Regionale Manager und Geschäftsführer können alle ihre Unternehmen zentral verwalten, was eine schnellere Entscheidungsfindung und einen reibungsloseren Geschäftsbetrieb ermöglicht.

Diese Verbesserung baut auf der Multi-Company-Membership-Funktion von B2B 1.5.0 auf, die es Benutzern ermöglichte, mehreren Unternehmen anzugehören, aber keinen unternehmensübergreifenden Admin-Zugriff unterstützte. Durch den Umschalter für Unternehmen entfällt die Notwendigkeit separater Administratorkonten, während die ordnungsgemäße Zugriffssteuerung und unternehmensspezifische Ansichten beibehalten werden.

### Firma

![Problem behoben](../assets/fix.svg)<!-- B2B-4480 --> Es wurde ein Problem behoben, bei dem Gastkunden eine `No such entity with cartId = ?` Fehlermeldung angezeigt wurde, wenn sie sich als Firmenbenutzer mit Produkten in ihrem Warenkorb anmeldeten.

### Verhandelbares Angebot

![Problem behoben](../assets/fix.svg) Die B2B-Version 1.5.2 enthält die folgenden Fehlerbehebungen für verhandelbare Angebote:

- <!-- B2B-3252 -->Das Feld [!UICONTROL Line Item Discount Amount] validiert jetzt die Eingabe, um die Eingabe negativer Rabattwerte zu verhindern.
- <!-- B2B-3224 -->Es wurde ein Problem mit dem Benutzererlebnis behoben, bei dem lange Zeileneintragsnotizen abgeschnitten und für B2B-Kunden schwer lesbar waren.
- <!-- B2B-2865 -->B2B-Kunden können jetzt Produktmengen mithilfe von Dezimalwerten (z. B. 1.5 oder 2.75) angeben, wenn sie Angebote erstellen.

### Angebotsvorlage

![Neu](../assets/new.svg)<!-- B2B-4104 --> Neue Möglichkeit für B2B-Käufer und -Verkäufer, externe Dokument-Links an Angebotsvorlagen anzuhängen. Diese Funktion ermöglicht die direkte Verknüpfung mit Dokumenten, die in -Services wie DocuSign und Adobe Sign gehostet werden, aus Anführungszeichen und ergänzt so die vorhandene Funktion zum Anhängen von Dateien. Zu den wichtigsten Vorteilen gehören:

- Optimierte Zusammenarbeit durch direkten Zugriff auf wichtige Vereinbarungen und Verträge
- Erhöhte Transparenz durch sofortigen Zugriff auf die neueste Dokumentation
- Schnellere Angebotsverhandlungen, da Dateien nicht mehr heruntergeladen und hochgeladen werden müssen
- Flexibles Dokumentenmanagement mithilfe externer Dokumentenhosting-Services

## B2B 1.5.1

*11. Februar 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Sicherheitsaktualisierungen der Adobe Commerce-Versionen 2.4.7-p4+ und 2.4.6-p9+.
Kompatibel mit Adobe Commerce 2.4.8-beta1 bis 2.4.8-beta2, 2.4.7 bis 2.4.7-p3, 2.4.6 bis 2.4.6-p8

Die B2B-Version 1.5.1 enthält Qualitätsverbesserungen und Fehlerbehebungen.

### Firma

![Problem behoben](../assets/fix.svg)<!-- B2B-4422 --> Wenn ein Kunde versucht, auf der Seite „Angebotsdetails“ einen anderen Anbieter zu wählen, leitet das System den Kunden jetzt auf eine Seite *Zugriff verweigert* um sicherzustellen, dass ein für ein Unternehmen erstelltes Angebot nicht für die Bestellung mit den Preisen eines anderen Unternehmens verwendet werden kann. Zuvor konnte ein Benutzer ein Angebot mit dem Preis für ein Unternehmen erstellen und dann zu einem anderen Unternehmen wechseln, um eine Bestellung mit unterschiedlichen Preisen aufzugeben.

### Rabatte auf Einzelposten

![Problem behoben](../assets/fix.svg)<!-- B2B-2938 --> Verbesserte Systemeffizienz durch Behebung einer Leistungsbeeinträchtigung, die im Szenario zur Neuberechnung des Angebots beobachtet wurde. Zuvor wurden zu jedem Warenkorb-Zeileneintrag zwei neue Entitäten hinzugefügt, was zu einem merklichen Anstieg der Datenbankanfragen führte, was zu einer langsameren Leistung führte.

### Verhandelbares Angebot

![Es wurde ](../assets/fix.svg)<!-- B2B-3820 --> Problem behoben: Das System behält jetzt die Position von Benutzeroberflächenelementen bei, wenn die JavaScript-Validierung auf die *[!UICONTROL min/max qty]* Felder auf der Seite „Zitatvorlage“ der Luma-Storefront angewendet wird. Zuvor hat das Anwenden der JavaScript-Validierung auf diese Felder dazu geführt, dass sich andere Benutzeroberflächenelemente auf der Seite verschoben haben.

### Warenkorb

![Problem behoben](../assets/fix.svg)<!-- B2B-4222 --> Einführung eines neuen Warenkorb-Verwaltungssystems zur Optimierung des Einkaufserlebnisses für Benutzer, die mehrere Unternehmenskonten verwalten. Das neue System verknüpft Warenkörbe mit einzelnen Unternehmen und nicht mit dem Kundenkonto, um das Einkaufserlebnis zu optimieren und den Workflow zu verbessern, indem die folgenden Funktionen unterstützt werden.

- **Firmenspezifische Warenkörbe:** - Einkaufswagen sind jetzt mit einzelnen Unternehmen verknüpft, um unternehmensspezifische Preis- und Produktoptionen zu unterstützen.
- **Nahtloser Wechsel** - Benutzer können einfach zwischen verschiedenen Unternehmenskonten wechseln, ohne den Inhalt des Warenkorbs der einzelnen Unternehmen zu beeinflussen.
- **Kontextuelle Integrität** - Alle Warenkorbdetails bleiben im Kontext des jeweiligen Unternehmens, was ein konsistentes und zuverlässiges Einkaufserlebnis bietet.

## B2B 1.5.0

*30. Oktober 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Patch-Versionen für Adobe Commerce 2.4.7-p3+ und 2.4.6-p8+.
Kompatibel mit Adobe Commerce 2.4.8-beta1, 2.4.7 bis 2.4.7-p2, 2.4.6 bis 2.4.6-p7.

Adobe Commerce B2B Version 1.5.0 ist auch mit PHP 8.3 kompatibel und unterstützt den [GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

Die B2B-Version 1.5.0 enthält neue Funktionen, Qualitätsverbesserungen und Fehlerbehebungen.

>[!NOTE]
>
> Erfahren Sie mehr über abwärtsinkompatible Änderungen (BICs), die in der B2B-Version 1.5.0 eingeführt wurden, indem Sie die Highlights und Referenzinformationen im Thema [Abwärtsinkompatible Änderungen](backward-incompatible-changes.md) überprüfen.

### Unternehmensleitung

![Neu](../assets/new.svg) **Unternehmensverwaltung**<!--B2B-2901--> - Händler können jetzt Adobe Commerce-Unternehmen als hierarchische Organisationen anzeigen und verwalten, indem sie Unternehmen bestimmten Mutterunternehmen zuweisen. Nachdem eine Firma einer übergeordneten Firma zugewiesen wurde, kann der Administrator der übergeordneten Firma das Firmenkonto verwalten. Nur autorisierte Admin-Benutzerinnen und -Benutzer können Unternehmenszuweisungen hinzufügen und verwalten. Weitere Informationen finden Sie unter [Unternehmenshierarchie verwalten](manage-company-hierarchy.md).

- Fügen Sie Unternehmenszuweisungen über den neuen Abschnitt *[!UICONTROL Company Hierarchy]* auf der Seite *[!UICONTROL Company Account]* in der Admin Console hinzu und verwalten Sie diese.

- Sortieren und Filtern von Unternehmen nach der neuen *[!UICONTROL Company Type]*. Im Raster Firmen gibt die Spalte *[!UICONTROL Company Type]* an, ob eine Firma eine einzelne Firma oder Teil einer Organisationshierarchie (über- oder untergeordnet) ist.

![Neu](../assets/new.svg) **Unternehmenskonfiguration skaliert verwalten**<!--B2B-2849--> - Ändern Sie die Unternehmenskonfigurationseinstellungen für ausgewählte Unternehmen schnell mithilfe der *[!UICONTROL Change company setting]* Massenaktion, die jetzt beim Verwalten von Unternehmen über das *[!UICONTROL Companies]*- oder *[!UICONTROL Company Hierarchy]* verfügbar ist. Wenn Sie beispielsweise einen neuen freigegebenen Katalog für eine Gruppe von Unternehmen erstellen, können Sie die Konfiguration des freigegebenen Katalogs in einer einzigen Aktion ändern, anstatt jedes Unternehmen einzeln zu bearbeiten.

![Neu](../assets/new.svg) API-Entwicklerinnen und -Entwickler können die neue `/V1/company/{parentId}/relations` für die Company Relations REST-API verwenden, um Unternehmenszuweisungen zu erstellen, anzuzeigen und zu entfernen. Siehe [Verwalten von Unternehmensobjekten](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) im *Web API-Entwicklerhandbuch*.

### Unternehmenskonten

![Neu](../assets/new.svg)<!--B2B-2828--> **Zuweisung mehrerer Unternehmen** - Vereinfachen Sie den Zugriff auf Firmenkonten für Firmenbenutzer, indem Sie einen Benutzer mehreren Unternehmen zuweisen. Wenn Sie beispielsweise einen Käufer haben, der Bestellungen von mehreren Firmen-Sites aufgibt, erstellen Sie ein einziges Konto und weisen Sie diesem Konto alle Firmen zu, mit denen der Käufer arbeitet. Dann kann sich der Käufer einmal anmelden und zwischen Unternehmenskonten wechseln, indem er das Unternehmen in der Storefront auswählt.

>[!NOTE]
>
>Ein Unternehmensbenutzer kann mehreren Unternehmen zugewiesen werden, er kann jedoch der Unternehmensadministrator für nur ein Unternehmen sein.

![Neu](../assets/new.svg) <!--B2B-2747--> **Bereichsauswahl für Unternehmen** - Bietet die Möglichkeit für Unternehmensbenutzer, die mehreren Unternehmen zugewiesen sind, Unternehmen in der Storefront zu ändern. Wenn der Umfang gewechselt wird, werden die Daten aktualisiert, um die Informationen basierend auf dem neuen Unternehmenskontext anzuzeigen. Wenn die neue Firma beispielsweise einen anderen freigegebenen Katalog verwendet, sieht der Firmenbenutzer Produkte, Preise und andere Informationen, die auf dem neuen freigegebenen Katalog basieren. Inhalte in Bezug auf Bestellungen, Angebote und Angebotsvorlagen werden ebenfalls auf der Grundlage des Kontexts des ausgewählten Unternehmens aktualisiert.

>[!NOTE]
>Der Warenkorbinhalt spiegelt die vom aktuellen Kunden ausgewählten Artikel wider. Wenn der Kunde über einen aktiven Warenkorb verfügt und ein anderes Unternehmen auswählt, wird er aufgefordert, den Warenkorb zu aktualisieren, um das Produktsortiment, die Preise und Rabatte für Werbeaktionen auf der Grundlage des neuen Firmenkontexts widerzuspiegeln. Produkte, die im mit der neuen Firma verknüpften Katalog nicht verfügbar sind, werden aus dem Warenkorb entfernt. Wenn das Produkt einen anderen Preis oder eine andere Verfügbarkeit hat, wird der Warenkorb aktualisiert, um die im Kontext des ausgewählten Unternehmens verfügbaren Daten widerzuspiegeln.<!--B2B-4222-->

![Problem behoben](../assets/fix.svg)<!--ACP2E-1933--> Unternehmensadministratoren können jetzt Unternehmensbenutzer aus der Storefront hinzufügen. Zuvor hat Commerce einen Fehler protokolliert, wenn ein Administrator bzw. eine Administratorin versucht hat, einen neuen Benutzer hinzuzufügen: `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

### Angebote und Angebotsvorlagen

Verbesserungen der Angebotsfunktionen helfen Käufern und Verkäufern, Angebote und Angebotsverhandlungen effektiver zu verwalten.

![Neu](../assets/new.svg) **Angebotsvorlagen** - <!--B2B-3367-->Käufer und Verkäufer können jetzt den Angebotsprozess optimieren, indem sie wiederverwendbare und anpassbare Angebotsvorlagen erstellen. Mithilfe von Angebotsvorlagen kann der Prozess der Angebotsaushandlung einmal abgeschlossen werden, und Käufer können vorab genehmigte verknüpfte Angebote für wiederkehrende Bestellungen generieren, anstatt für jede Bestellung den Prozess der Angebotsaushandlung durchzuführen. Zitatvorlagen erweitern die vorhandene Zitatfunktion, indem sie die folgenden erweiterten Funktionen hinzufügen:

- **Bestellschwellen** ermöglichen es Verkäufern, Mindest- und Höchstbestellverpflichtungen festzulegen, um sicherzustellen, dass der Käufer vereinbarte Kaufmengen einhält.
- **Festlegen von Mindest- und Höchstbestellmengen für Artikel** bietet dem Käufer die Flexibilität, die Bestellmengen für das verknüpfte Angebot anzupassen, ohne dass eine neue Vorlage oder weitere Verhandlungen erforderlich sind.
- **Verfolgen Sie die Anzahl der verknüpften Angebote, die generiert und erfolgreich** wurden, um Einblicke in die Erfüllung ausgehandelter Vereinbarungen zu erhalten.
- **Verknüpfte Angebote** sind vorab genehmigte Angebote, die der Käufer aus einer aktiven Angebotsvorlage generiert, um wiederkehrende Bestellungen auf der Grundlage der in der Angebotsvorlage ausgehandelten Bedingungen einzureichen.

![Neu](../assets/new.svg) **Verbesserungen vorhandener Angebotsfunktionen**

- **Aktualisierte Regeln der Commerce-Zugriffssteuerungsliste (ACL) ermöglichen** B2B-Managern und -Supervisoren die Verwaltung von Angeboten und Angebotsvorlagen von untergeordneten Benutzern. Separate Regeln unterstützen eine granulare Konfiguration für die Anzeige, Bearbeitung und Löschberechtigung.

- **Angebot als Entwurf speichern**<!--B2B-2566--> - Beim Erstellen einer [Angebotsanfrage](quote-request.md) aus dem Warenkorb können Käufer das Angebot jetzt als Entwurf speichern, damit sie es überprüfen und aktualisieren können, bevor sie den Angebotsverhandlungsprozess mit dem Verkäufer starten. Der Angebotsentwurf hat kein Ablaufdatum. Einkäufer können Angebotsentwürfe im Abschnitt [!UICONTROL My Quotes] ihres Konto-Dashboards einsehen und aktualisieren.

- **Angebot umbenennen**<!--B2B-2596--> - Käufer können jetzt einen Angebotsnamen auf der Seite [Angebotsdetails“ ](account-dashboard-my-quotes.md#quote-actions), indem sie die Option **[!UICONTROL Rename]** auswählen. Diese Option steht autorisierten Käufern beim Bearbeiten des Angebots zur Verfügung. Namensänderungsereignisse werden im Angebotsprotokoll aufgezeichnet.

- **Doppeltes Angebot**<!--B2B-2701--> - Käufer und Verkäufer können jetzt ein neues Angebot durch Kopieren eines vorhandenen Angebots erstellen. Eine Kopie wird aus der Angebotsdetailansicht erstellt, indem **[!UICONTROL Create Copy]** in der [Angebotsdetailansicht) ](quote-price-negotiation.md#button-bar) Admin oder der [Storefront“ ](account-dashboard-my-quotes.md#quote-actions).

- **Angebotsartikel in Anforderungsliste verschieben**<!--B2B-2755--> - Einkäufer haben jetzt die Möglichkeit, Produkte aus einem Angebot zu entfernen und in einer Anforderungsliste zu speichern, wenn sie sie nicht in den Angebotsaushandlungsprozess einbeziehen möchten.

- **Mehrere Produkte aus einem Angebot entfernen**<!--B2B-2881--> - Bei Angeboten mit einer großen Anzahl von Produkten können Käufer jetzt mehrere Produkte aus dem Angebot entfernen, indem sie sie auswählen und die Option *[!UICONTROL Remove]* aus dem *[!UICONTROL Actions]* auf der Seite „Angebotsdetails“ verwenden. In früheren Versionen musste ein Käufer Produkte einzeln löschen.

- **Rabattsperre für Einzelposten**<!--B2B-2597--> - Bei der Angebotsaushandlung können Verkäufer die Rabattsperre für Einzelposten verwenden, um mehr Flexibilität bei der Anwendung von Rabatten während der Angebotsaushandlung zu erhalten. Beispielsweise kann ein Verkäufer einen speziellen Positionsrabatt auf einen Artikel anwenden und den Artikel sperren, um weitere Rabatte zu verhindern. Wenn ein Artikel gesperrt ist, kann der Artikelpreis nicht aktualisiert werden, wenn ein Rabatt auf Angebotsebene angewendet wird. Siehe [Angebot für einen Einkäufer starten](sales-rep-initiates-quote.md).

![Problem behoben](../assets/fix.svg) **Fehlerbehebungen für vorhandene Angebotsfunktionen**

- Händler, die in der Detailansicht des Angebots in der Admin-Liste auf die Schaltfläche *[!UICONTROL Print]* klicken, werden jetzt aufgefordert, das Angebot als PDF zu speichern. Zuvor wurden Händler zu einer Seite mit Angebotsdetails umgeleitet. <!--ACP2E-1984-->

- Zuvor hat der Administrator beim Versand eines Kundenangebots mit `0` Prozentsatz und der Änderung der Menge eine Ausnahme ausgelöst, die Menge jedoch gespeichert. Nachdem diese Fehlerbehebung angewendet wurde, wird für die `0 percentage` richtige Ausnahme mit einer Meldung ausgelöst. <!--ACP2E-1742-->

- Während der Angebotsaushandlung kann ein Verkäufer jetzt einen `0%` Rabatt im Feld Ausgehandelter Angebotsrabatt angeben und das Angebot an den Käufer zurücksenden. Wenn der Verkäufer zuvor einen Rabatt von 0 % eingegeben und das Angebot an den Käufer zurückgesendet hat, hat der Administrator eine `Exception occurred during quote sending` Fehlermeldung zurückgegeben. <!--ACP2E-1742-->

- Die reCAPTCHA-Validierung funktioniert jetzt beim Checkout für ein B2B-Angebot ordnungsgemäß, wenn reCAPTCHA V3 für den Storefront-Checkout konfiguriert ist. Zuvor schlug die Validierung mit einer `recaptcha validation failed, please try again` Fehlermeldung fehl.  <!--ACP2E-2097-->

### Bestellungen

![Problem behoben](../assets/fix.svg) <!--ACP2E-1825-->Bestellungen können von einem mit dem Unternehmen verbundenen Benutzer nicht mehr aufgegeben werden, nachdem das Unternehmen gesperrt wurde. Zuvor konnte ein mit der Firma verbundener Benutzer Bestellungen aufgeben, wenn die Firma blockiert wurde.

## B2B v1.4.2-p6

*10. Juni 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce-Sicherheits-Patch-Versionen 2.4.7-p6+ und 2.4.6-p11+.

![Problem behoben](../assets/fix.svg) Umfasst die in [Security Bulletin APSB25-50](https://helpx.adobe.com/security/products/magento/apsb25-50.html) dokumentierten Sicherheitskorrekturen.

{{b2b-compatibility}}

## B2B v1.4.2-p5

*8. April 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce-Sicherheits-Patch-Versionen 2.4.7-p5+ und 2.4.6-p10+.

![Neu](../assets/new.svg) Hinzugefügte Kompatibilität mit Adobe Commerce 2.4.7-p5+ und 2.4.6-p10+ Sicherheits-Patch-Versionen.

![Problem behoben](../assets/fix.svg) Umfasst die in [Security Bulletin APSB25-26](https://helpx.adobe.com/security/products/magento/apsb25-26.html) dokumentierten Sicherheitskorrekturen.

{{b2b-compatibility}}

## B2B v1.4.2-p4

*11. Februar 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Sicherheitsaktualisierungen für Adobe Commerce 2.4.7-p4+ und 2.4.6-p9+.

![Neu](../assets/new.svg) Hinzugefügte Kompatibilität mit Adobe Commerce 2.4.7-p4+ und 2.4.6-p9+ Sicherheits-Patch-Versionen.

![Problem behoben](../assets/fix.svg) Enthält die in [Security Bulletin APSB25-08](https://helpx.adobe.com/security/products/magento/apsb25-08.html) dokumentierten Sicherheitskorrekturen.

{{b2b-compatibility}}

## B2B v1.4.2-p3

*8. Oktober 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Sicherheitsaktualisierungen für Adobe Commerce 2.4.7-p3+ und 2.4.6-p8+.

![Neu](../assets/new.svg) Hinzugefügte Kompatibilität mit Adobe Commerce 2.4.7-p3+ und 2.4.6-p8+ Sicherheits-Patch-Versionen.

![Problem behoben](../assets/fix.svg) Umfasst die in [Security Bulletin APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html) dokumentierten Sicherheitskorrekturen.

{{b2b-compatibility}}

## B2B v1.4.2-p2

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce-Sicherheits-Patch-Versionen 2.4.7-p2+ und 2.4.6-p7+.

![Neu](../assets/new.svg) Hinzugefügte Kompatibilität mit Adobe Commerce 2.4.7-p2+ und 2.4.6-p7+ Sicherheits-Patch-Versionen.

![Problem behoben](../assets/fix.svg) Umfasst die im Sicherheitsbulletin xxxx dokumentierten Sicherheitskorrekturen.

{{b2b-compatibility}}

## B2B v1.4.2-p1

*9. August 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce-Sicherheits-Patch-Versionen 2.4.7-p1+ und 2.4.6-p6+.

![Neu](../assets/new.svg) Hinzugefügte Kompatibilität mit Adobe Commerce 2.4.7-p1+ und 2.4.6-p6+ Sicherheits-Patch-Versionen.

{{b2b-compatibility}}

## B2B v1.4.2

*10. Oktober 2023*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce Version 2.4.7 und Version von 2.4.6 bis 2.4.6-p5.

Die B2B-Version 1.4.2 enthält Qualitätsverbesserungen und Fehlerbehebungen.

![Problem behoben](../assets/fix.svg) <!--B2B-2897-->Wenn ein Verkäufer ein Einkäuferangebot erstellt, das eine Produkt-SKU enthält, die nicht im freigegebenen Katalog verfügbar ist, der mit der Einkäuferfirma verknüpft ist, zeigt das System die Fehlermeldung `The SKU you entered is not available in the shared catalog. Please check the SKU and try again` an.  Der Verkäufer kann das Angebot erst speichern, wenn er das nicht verfügbare Produkt entfernt hat. Zuvor wurde das Angebot mit der nicht verfügbaren SKU gespeichert und das Angebot konnte nicht in die Storefront geladen werden.

>[!IMPORTANT]
>
>Adobe Commerce B2B ab Version 1.4.2 ist mit PHP 8.2 kompatibel. Wenn Sie die Commerce-Instanz auf Version 2.4.7 oder höher aktualisieren, stellen Sie sicher, dass die Instanz PHP Version 8.2 verwendet, um die Kompatibilität mit Adobe Commerce B2B-Version zu gewährleisten. Darüber hinaus unterstützt B2B 1.4.2+ derzeit nicht den [GraphQL-Anwendungsserver](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

## B2B v1.4.1

*7. August 2023*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} [Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Kompatibel mit Adobe Commerce 2.4.7-beta1.

Die B2B-Version 1.4.1 enthält Qualitätsverbesserungen und Fehlerbehebungen.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1825-->Bestellungen können von einem mit dem Unternehmen verbundenen Benutzer nicht mehr aufgegeben werden, nachdem das Unternehmen gesperrt wurde. Zuvor konnte ein mit der Firma verbundener Benutzer Bestellungen aufgeben, wenn die Firma blockiert wurde.

![Problem behoben](../assets/fix.svg) Der <!--ACP2E-1943--> „Produkt rückgestellt“ wird jetzt korrekt in der Storefront angezeigt. Zuvor wurden Produkte, die für den Versand verfügbar waren, fälschlicherweise als zurückbestellt identifiziert.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1862-->Wenn das Unternehmensregistrierungsformular ein Kundendateitypattribut enthält, wird die während des Registrierungsprozesses hochgeladene Datei jetzt nach der Erstellung des Unternehmens in die Kontoinformationen für den Unternehmensadministrator aufgenommen. Zuvor fehlte der Anhang.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1793-->Der Musterselektor für ein konfigurierbares Produkt wird jetzt wie erwartet auf der Konfigurationsseite des Anforderungslistenelements angezeigt. Zuvor wurde die Musterauswahl als Dropdown-Feld auf der Konfigurationsseite des Anforderungslistenelements angezeigt.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1968-->Bei Verwendung der [Unternehmensabfrage von GraphQL](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) zum Zurückgeben von Unternehmensdetails werden Ergebnisse jetzt erfolgreich und fehlerfrei zurückgegeben.

## B2B v1.4.0

*13. Juni 2023*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} [Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Kompatibel mit Adobe Commerce 2.4.7-beta1

Diese Version enthält neue Funktionen und Verbesserungen für B2B-verhandelbare Angebote und mehrere Fehlerbehebungen.

![Neu](../assets/new.svg) Hinzugefügte Kompatibilität mit Adobe Commerce 2.4.7-beta1.

![Neu](../assets/new.svg) **Vom Verkäufer initiierte Angebote** - Verkäufer können jetzt ein Angebot für einen Käufer direkt über die Angebots- und Kundenraster in der Admin initiieren. Diese Funktion optimiert den Angebotsprozess und reduziert die Komplexität für Kunden. Wenn ein Kunde keine Bestellung initiiert hat, kann ein Verkäufer schnell ein Angebot im Namen des Kunden erstellen und den Verhandlungsprozess starten. Zuvor konnten Angebote nur vom Käufer oder von einem als Kunde angemeldeten Verkäufer in der Storefront erstellt werden.

![Neu](../assets/new.svg) **Einzelpostenrabatte und -verhandlung**-<!--B2B-2440--> Innerhalb eines Angebots können B2B-Käufer und -Verkäufer jetzt auf Zeilenpostenebene verhandeln, Rabatte anwenden und Notizen austauschen, bis eine Vereinbarung getroffen wird. Notizenerstellung und -aktualisierungen sind im Zeileneintrag und Angebotshistorie enthalten, um die Kommunikation zu verfolgen. Bisher konnten Käufer und Verkäufer nur Notizen umtauschen und Rabatte auf der Angebotsebene gewähren.

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt jetzt während der Zahlung die richtigen Details an, wenn die Option Bestellungen aktiviert ist und ein virtuelles Angebot ausgewählt wurde, das mit der Zahlungsoption PayPal erstellt wurde. Zuvor wurden die Gesamtwerte unter diesen Bedingungen als Null angezeigt.

![Problem behoben](../assets/fix.svg) Beim Speichern eines Unternehmens mit einem Kreditlimit von über 999 treten <!--ACP2E-1504--> Validierungsfehler nicht mehr auf. Zuvor wurde für Unternehmenskreditlimits, die größer als 999 waren, in Adobe Commerce ein Kommatrennzeichen eingefügt, was einen Validierungsfehler verursachte, der das Speichern von Aktualisierungen verhinderte.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1474--> Die ausgewählte Lieferadresse bleibt jetzt unverändert, wenn Sie eine Bestellung mit einem verhandelbaren Angebot aufgeben. Zuvor wurde bei der Bestellung die ausgewählte Lieferadresse in die standardmäßige Lieferadresse geändert.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1429--> In den Store-Konfigurationseinstellungen für B2B-Funktionen ist das Feld **[!UICONTROL Enable Shared Catalog direct products price assigning]** jetzt automatisch deaktiviert. Auf der Storefront wird sie ausgeblendet, wenn die **[!UICONTROL Enable Company]**- oder **[!UICONTROL Enable Shared Catalog]** auf **[!UICONTROL No]** festgelegt ist.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1683--> Beim Erstellen eines Unternehmenskontos in der Storefront validiert Commerce jetzt die E-Mail-Adresse, bevor die Unternehmensregistrierung verarbeitet wird. Wenn die E-Mail-Adresse ungültig ist, schlägt der Vorgang fehl und es werden keine Kontoaktualisierungen verarbeitet. Zuvor wurde ein Kundenkonto erstellt, selbst wenn die Anforderung zum Erstellen eines Unternehmenskontos aufgrund einer ungültigen E-Mail-Adresse fehlgeschlagen ist.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1664--> Produkt-SKUs, die doppelte Anführungszeichen im freigegebenen Katalog und in der Preisstruktur enthalten, verursachen keine Fehler mehr in der Admin-Instanz.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1498--> Die Varnish-Konfiguration für die Commerce-Anwendung wurde aktualisiert, um zu verhindern, dass Gastbenutzer Daten von anderen Kundengruppen sehen.

### Bekanntes Problem

Beim Installieren oder Aktualisieren von B2B 1.4.0 auf [Adobe Commerce Version 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html) tritt der folgende Fehler auf:

```
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

Sie können dieses Problem beheben, indem Sie manuelle Abhängigkeiten für das B2B-Sicherheitspaket hinzufügen, indem Sie manuelle Abhängigkeiten für das B2B-Sicherheitspaket mit einem &quot;[&quot; ](https://getcomposer.org/doc/04-schema.md#package-links). Anweisungen finden Sie in der [Adobe Commerce Knowledge Base](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html).

## B2B v1.3.5-p10

*8. April 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce-Sicherheits-Patch-Versionen 2.4.6-p10+.

![Neu](../assets/new.svg) Hinzugefügte Kompatibilität mit den Adobe Commerce 2.4.6-p10 Sicherheits-Patch-Versionen.

![Problem behoben](../assets/fix.svg) Umfasst die in [Security Bulletin APSB25-26](https://helpx.adobe.com/security/products/magento/apsb25-26.html) dokumentierten Sicherheitskorrekturen.

## B2B v1.3.5-p9

*11. Februar 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce 2.4.6-p9+ Sicherheits-Patch-Versionen.

![Neu](../assets/new.svg) Hinzugefügte Kompatibilität mit den Adobe Commerce 2.4.6-p9 Sicherheits-Patch-Versionen.

![Problem behoben](../assets/fix.svg) Enthält die in [Security Bulletin APSB25-08](https://helpx.adobe.com/security/products/magento/apsb25-08.html) dokumentierten Sicherheitskorrekturen.

## B2B v1.3.5-p8

*8. Oktober 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce-Sicherheits-Patch-Versionen 2.4.6-p8+.

![Neu](../assets/new.svg) Hinzugefügte Kompatibilität mit den Adobe Commerce 2.4.6-p8 Sicherheits-Patch-Versionen.

![Problem behoben](../assets/fix.svg) Umfasst die in [Security Bulletin APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html) dokumentierten Sicherheitskorrekturen.

## B2B v1.3.5-p7

*9. August 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce-Sicherheits-Patch-Versionen 2.4.6-p7+.

![Neu](../assets/new.svg) Hinzugefügte Kompatibilität mit den Adobe Commerce 2.4.6-p7 Sicherheits-Patch-Versionen.

## B2B v1.3.5

*14. März 2023*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce 2.4.0 - 2.4.6 und neuere Versionen

![Neu](../assets/new.svg) Version B2B 1.3.5-p2 wurde veröffentlicht, um die Kompatibilität mit Adobe Commerce 2.4.6-p2 zu unterstützen.

![Neu](../assets/new.svg) Version B2B 1.3.5-p1 wurde veröffentlicht, um die Kompatibilität mit Adobe Commerce 2.4.6-p1 zu unterstützen.

>[!NOTE]
>
>Stellen Sie nach dem Upgrade von Commerce von 2.4.6 auf [neueste Version](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6) sicher, dass Sie auf die unterstützte Patch-Version B2B 1.3.5 aktualisieren. Oder aktualisieren Sie die B2B-Erweiterung von Version 1.3.5 auf Version 1.4.0 oder höher, um die neuesten Funktionen zu erhalten.

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.6 wurde hinzugefügt.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-689--> Wenn die Option Bestellungen aktiviert ist und ein virtuelles Angebot ausgewählt wurde, das mit der Zahlungsoption PayPal erstellt wurde, zeigt Adobe Commerce jetzt während der Zahlung die richtigen Details an. Zuvor wurden die Gesamtwerte unter diesen Bedingungen als Null angezeigt.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-609--> Die Liste der Kundengruppen für die Einstellung **Browser-Kategorie zulassen** enthält keine Kundengruppen mehr, die mit freigegebenen Katalogen verbunden sind.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-1244--> Das Kundenattribut für Steuer-/MwSt.-Nummer funktioniert jetzt bei Unternehmensadministratorkonten sowohl in der Admin- als auch in der Storefront wie erwartet. Benutzerdefinierte Steuer-/Mehrwertsteuerattribute sind nicht mehr erforderlich, um ein Unternehmenskonto zu erstellen. Wenn ein Händler zuvor ein Unternehmenskonto mit einem benutzerdefinierten MwSt.-Attribut erstellt hat, hat Adobe Commerce sowohl in der Storefront als auch in der Admin einen Validierungsfehler ausgegeben.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-1236--> Die Deaktivierung der Funktion „Freigegebener Katalog“ in einem bestimmten Bereich funktioniert jetzt ordnungsgemäß. Zuvor hat Adobe Commerce einen ungültigen Bereich festgelegt, wenn ein Händler die Konfiguration des freigegebenen Katalogs gespeichert hat.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-1203--> Admin-Benutzer können jetzt benutzerdefinierte Attributwerte von Kunden für Firmenbenutzer speichern. Zuvor konnten benutzerdefinierte Kundenattribute für Unternehmensbenutzer nicht gespeichert werden.

![Es wurde ](../assets/fix.svg), <!--- ACP2E-1221--> Leistungsprobleme durch die Validierung von Unternehmensberechtigungen behoben werden, die über GraphQL bereitgestellt werden, wenn bereits viele Unternehmensberechtigungen zugewiesen sind.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-1242--> Adobe Commerce gibt keinen Fehler mehr auf der Warenkorbseite aus, wenn die Schnellbestellung zum Hinzufügen eines Produkts in einer Menge verwendet wird, die den verfügbaren Lagerbestand übersteigt.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-1090--> Die Leistung von Vorgängen `SELECT` Unternehmensberechtigungen wurde verbessert.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-2456--> Kategorieabfragen geben jetzt Produktpreise entsprechend den Einstellungen der Store-Konfiguration zurück, wenn für die abgefragte Kategorie keine expliziten Kategorieberechtigungen festgelegt sind.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-6829--> Die Schaltfläche **[!UICONTROL Place Order]** funktioniert jetzt wie erwartet, wenn ein Kauf mit einer genehmigten Angebotsanfrage abgeschlossen wird. Probleme mit dem `negotiableQuoteCheckoutSessionPlugin`-Plug-in für verhandelbare Angebote wurden behoben.

## B2B v1.3.4-p13

*10. Juni 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce 2.4.0 und neuere Versionen

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.5-p12 wurde hinzugefügt.

![Problem behoben](../assets/fix.svg) Umfasst die in [Security Bulletin APSB25-50](https://helpx.adobe.com/security/products/magento/apsb25-50.html) dokumentierten Sicherheitskorrekturen.

## B2B v1.3.4-p12

*8. April 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce 2.4.0 und neuere Versionen

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.5-p12 wurde hinzugefügt.

![Problem behoben](../assets/fix.svg) Umfasst die in [Security Bulletin APSB25-26](https://helpx.adobe.com/security/products/magento/apsb25-26.html) dokumentierten Sicherheitskorrekturen.

## B2B v1.3.4-p11

*11. Februar 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce 2.4.0 und neuere Versionen

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.5-p11 wurde hinzugefügt.

![Problem behoben](../assets/fix.svg) Enthält die in [Security Bulletin APSB25-08](https://helpx.adobe.com/security/products/magento/apsb25-08.html) dokumentierten Sicherheitskorrekturen.

## B2B v1.3.4-p10

*9. Oktober 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce 2.4.0 und neuere Versionen

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.5-p10 wurde hinzugefügt.

![Problem behoben](../assets/fix.svg) Umfasst die in [Security Bulletin APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html) dokumentierten Sicherheitskorrekturen.

## B2B v1.3.4

*9. August 2022*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce 2.4.0 und neuere Versionen

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.5 wurde hinzugefügt.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce sendet keine E-Mail-Benachrichtigungen mehr, wenn ein vorhandenes Unternehmen durch einen API-Aufruf aktualisiert wird. E-Mails werden jetzt nur noch bei der Erstellung einer Firma gesendet.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-406-->Adobe Commerce berechnet jetzt korrekt den Gesamtwert eines verhandelbaren Angebots, wenn die Einstellung für die **[!UICONTROL Enable Cross Border Trade]** aktiviert ist.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-322-->Konfigurierbare Produkte werden jetzt an die letzte Position in der Produktliste verschoben, nachdem der Lagerbestand aktualisiert wurde, wenn die **[!UICONTROL Move out of stock to the bottom]** aktiviert ist. Eine neue benutzerdefinierte Datenbankabfrage wird implementiert, um sicherzustellen, dass die Elasticsearch-Indexsortierreihenfolge jetzt die Admin-fähige Sortierreihenfolge berücksichtigt. Zuvor wurden konfigurierbare Produkte und ihre untergeordneten Produkte nicht an das Ende der Liste verschoben, wenn diese Einstellung aktiviert war.

![Problem behoben](../assets/fix.svg) Die E<!--- ACP2E-308-->Mail-Bestellung berücksichtigt jetzt in einer Bereitstellung mit mehreren Sites die E-Mail-Versandeinstellung jeder Website. Eine Prüfung auf die **[!UICONTROL Disable Email Communications]** wird der benutzerdefinierten Logik für E-Mail-Warteschlangen hinzugefügt. Zuvor berücksichtigte Adobe Commerce nicht die E-Mail-Sendeeinstellung für die sekundäre Website.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-302-->Der Titel des SKU-Felds der Schnellbestellungsseite wurde aus Gründen der Klarheit geändert.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-543-->Adobe Commerce zeigt jetzt eine informativere Fehlermeldung an, wenn ein Käufer eine ungültige SKU in das Feld **SKU oder Produktname eingeben** eingibt.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-1753-->Das Feld **[!UICONTROL Account Created in]** für einen Unternehmensadministrator behält jetzt seinen Wert wie erwartet bei, nachdem Sie das Unternehmen gespeichert haben.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-722 -->Die `customer` Abfrage gibt keine leeren Ergebnisse mehr zurück, wenn Anforderungslisten abgerufen werden, die nach `uid` gefiltert werden.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-210 --> Vor dem `collectQuoteTotals`-Aufruf wurde ein Plug-in hinzugefügt, um sicherzustellen, dass Speichergutschriften nur einmal angewendet werden.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-665 -->Kunden werden jetzt zur Anmeldeseite weitergeleitet, wenn ihr Konto von einem Administrator aus der Admin gelöscht wird. Zuvor gab Adobe Commerce einen Fehler aus. Der Plug-in-Code (`SessionPlugin`) befindet sich nun im `try…catch`. Zuvor war dieser Code nicht im generischen Block für die Ausnahmebehandlung eingeschlossen.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-661 --> Wenn Sie auf der Seite „Schnellbestellung“ im mobilen Modus **Eingabetaste** nach Eingabe eines gültigen Produktnamens oder einer gültigen SKU drücken, gelangen Sie der Einkäufer erwartungsgemäß zum nächsten Feld.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-607 -->Firmenname ist jetzt wie erwartet in den Abschnitten Abrechnungs- und Versandadresse des Checkout-Workflows sichtbar.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-375 -->Store-Guthaben ist jetzt nicht verfügbar, wenn die **[!UICONTROL Zero Subtotal Checkout]** Zahlungsmethode deaktiviert ist. Zuvor war das Kontrollkästchen „Gutschrift speichern“ während der Auftragserteilung durch den Administrator nicht funktionsfähig. Die Anwendung hat die Bestellung mit dem Speicherguthaben nicht aufgegeben und den folgenden Fehler angezeigt: `The requested Payment Method is not available`.

## B2B v1.3.3-p14

*10. Juni 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce 2.4.0 und neuere Versionen

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.5-p12 wurde hinzugefügt.

![Problem behoben](../assets/fix.svg) Umfasst die in [Security Bulletin APSB25-50](https://helpx.adobe.com/security/products/magento/apsb25-50.html) dokumentierten Sicherheitskorrekturen.

## B2B v1.3.3

*9. August 2022*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce 2.4.0 und neuere Versionen

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.4 wurde hinzugefügt.

![Problem behoben](../assets/fix.svg) <!--- MC-41985--> Der Zeitaufwand für die Aktualisierung von Adobe Commerce 2.3.x auf Adobe Commerce 2.4.x in Bereitstellungen mit mehr als 100.000 Unternehmensrollen wurde erheblich reduziert.

![Problem behoben](../assets/fix.svg) <!--- MC-42153--> Die POST-`V1/order/:orderId/invoice` unterstützt jetzt die Erstellung von Teilrechnungen, wenn die **[!UICONTROL Payment on Account]** Zahlungsmethode aktiviert ist. Zuvor gab Adobe Commerce diesen Fehler aus: `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![Problem behoben](../assets/fix.svg) <!--- MC-41975--> PayPal Payflow Pro funktioniert jetzt wie erwartet mit einem B2B-verhandelbaren Angebot, wenn der Warenkorb des Kunden andere Produkte enthält. Adobe Commerce verarbeitet die Bestellung jetzt erfolgreich und sendet wie erwartet eine E-Mail an den Kunden. Zuvor gab Adobe Commerce einen schwerwiegenden Fehler aus und sandte eine Bestätigungs-E-Mail an den Kunden, die null Werte enthielt.

![Problem behoben](../assets/fix.svg) Die <!--- MC-41819-->-Paginierung wird jetzt korrekt auf der Katalogsuchergebnisseite angezeigt, nachdem einige Produkte im freigegebenen Katalog ausgeschlossen wurden.

![Problem behoben](../assets/fix.svg) <!--- MC-42886--> Benutzerdefinierte Kundenattribute werden jetzt wie erwartet beim Erstellen oder Speichern eines Unternehmensbenutzers in der Admin Console gespeichert.

![Problem behoben](../assets/fix.svg) <!--- MC-42927--> Die Schaltfläche &quot;**[!UICONTROL Submit]**&quot; im Formular „Neues Unternehmen erstellen“ ist jetzt nach einem Klick deaktiviert, um mehrere Formularübermittlungen zu verhindern. Zuvor konnten Sie dieses Formular mehrmals senden, indem Sie wiederholt auf diese Schaltfläche klickten, was einen Fehler verursachte.

![Problem behoben](../assets/fix.svg) <!--- MC-42787--> Adobe Commerce zeigt den Link zur Neuanordnung nicht mehr in der Storefront an, wenn sich ein Käufer bei einem Store anmeldet, für den die Neuanordnung deaktiviert wurde.

![Problem behoben](../assets/fix.svg) <!--- MC-43115--> Bei der Schnellbestellungssuche nach SKU wird jetzt nicht mehr zwischen Groß- und Kleinschreibung unterschieden, wenn der freigegebene Katalog aktiviert ist.

![Problem behoben](../assets/fix.svg) <!--- MC-42203--> Sie können jetzt beim Erstellen einer Firma eine Datei für ein Kundenattribut aktualisieren. Wenn Sie bisher versucht haben, eine Firma mit einem Anhang vom Typ `File` zu erstellen, hat Adobe Commerce die Firma nicht erstellt und diesen Fehler im Ausnahmenprotokoll protokolliert: `Something went wrong while saving file`.

![Problem behoben](../assets/fix.svg) <!--- MC-42242--> Sie können jetzt eine Firma mit einem Kundenkonto erstellen, das über ein benutzerdefiniertes Attribut mit dem Typ (`File`) oder (`Image`) verfügt. Wenn das Konto zuvor eine dieser anpassbaren Optionen hatte, wurde der Seitenlader für die Unternehmensbearbeitung nicht aufgelöst, was die Bearbeitung von Unternehmensdetails verhinderte.

![Problem behoben](../assets/fix.svg) <!--- MC-42268--> Die `products`-Abfrage gibt jetzt ein genaues `total_count` zurück, wenn der freigegebene Katalog aktiviert ist.

![Problem behoben](../assets/fix.svg) <!--- MC-42203--> Sie können jetzt beim Erstellen einer Firma eine Datei für ein Kundenattribut aktualisieren. Wenn Sie bisher versucht haben, eine Firma mit einem Anhang vom Typ `File` zu erstellen, hat Adobe Commerce die Firma nicht erstellt und diesen Fehler im Ausnahmenprotokoll protokolliert: `Something went wrong while saving file`.

![Problem behoben](../assets/fix.svg) <!--- MC-43178--> Die Seiten _Unternehmenskonfiguration_ und _Unternehmen erstellen_ funktionieren jetzt wie erwartet, nachdem Sie eine Online-Versandmethode deaktiviert haben. Die Überprüfung wurde hinzugefügt, um die versuchte Verarbeitung deaktivierter Versandmodule zu verhindern. Zuvor hat Adobe Commerce diesen Fehler angezeigt: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![Problem behoben](../assets/fix.svg) <!--- MC-42214--> Auf der Seite _Kategorie_ werden jetzt konsistente Produktdaten angezeigt, während Berechtigungen während der partiellen Indizierung generiert werden. Diesem Prozess wurde ein neuer partieller Indexer für Verzeichnisberechtigungen hinzugefügt. Zuvor waren die Daten, die während der Indizierung angezeigt wurden, falsch.

![Problem behoben](../assets/fix.svg) <!--- MC-42567--> Die `categoryList`-Abfrage gibt jetzt die richtige Anzahl von Produkten zurück, wenn Katalogberechtigungen verwendet und Produkte einem freigegebenen Katalog zugewiesen werden.

![Problem behoben](../assets/fix.svg) <!--- MC-42528--> Die `categoryList` Abfrage berücksichtigt jetzt Kategorieberechtigungen und gibt nur zulässige Kategorien zurück. Zuvor wurden alle zugewiesenen und nicht zugewiesenen Kategorien zurückgegeben.

![Problem behoben](../assets/fix.svg) <!--- MC-42399--> Die `rest/V1/company/{id}`-Anfrage gibt jetzt erwartungsgemäß `is_purchase_order_enabled` Attributwerte zurück.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-128--> Benutzerdefinierte Kundenattribute werden nun wie erwartet auf der Registerkarte _Unternehmensadministrator“_.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-130--> Der Block Meine Wunschliste auf der Seite Mein Konto wird jetzt für Unternehmensadministratoren und Unternehmensbenutzer wie erwartet angezeigt.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-133--> Fehler bei der Schnellbestellung werden nicht mehr im Warenkorb angezeigt. Zuvor hat Adobe Commerce diesen Fehler im Warenkorb angezeigt, wenn die SKU nicht im Katalog gefunden wurde: `The SKU was not found in the catalog`.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-194--> Vorgänge zum Speichern freigegebener Kataloge wurden optimiert, um sie schneller auszuführen. Zuvor konnte das Speichern eines freigegebenen Katalogs mit vielen Kundengruppen mehrere Minuten dauern.

![Problem behoben](../assets/fix.svg) <!--- MC-42240--> Adobe Commerce löscht jetzt alle Unterkategorieberechtigungen aus der `sharedcatalog_category_permissions`, wenn die übergeordnete Kategorie gelöscht wird. Zuvor wurden nur die Daten der übergeordneten Kategorie entfernt.

## B2B v1.3.2

*29. August 2022*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce 2.4.0 und neuere Versionen

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.3 wurde hinzugefügt.

![Problem behoben](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce sendet jetzt erfolgreich Aktualisierungs-E-Mails zu abgelaufenen verhandelbaren Angeboten. Zuvor hat Adobe Commerce bei Ablauf eines verhandelbaren Angebots keine Aktualisierungs-E-Mails gesendet.

![Problem behoben](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce sendet jetzt erfolgreich Aktualisierungs-E-Mails, die demnächst ablaufen, und abgelaufene verhandelbare Anführungszeichen, wenn ein `cron` fehlt.

### Firma

![Problem behoben](../assets/fix.svg) <!--- MC-41542--> Im Dropdown-Feld Neue Firmenkonto-Seite erstellen werden keine leeren Optionswerte mehr aufgelistet. Zuvor waren die ersten beiden Optionswerte und der Ländercode `AN` leer.

![Problem behoben](../assets/fix.svg) <!--- MC-41260--> Wenn Sie auf die Schaltfläche **[!UICONTROL Return]** für eine Bestellung klicken, die von einem Unternehmensbenutzer erstellt wurde, wird ein Benutzer mit Administratorrechten wie erwartet zur Seite „Rücksendung erstellen“ weitergeleitet. Zuvor wurde der Administrator zur Seite Auftragsverlauf weitergeleitet.

![Problem behoben](../assets/fix.svg) Nur [!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."} schlägt <!--- MC-40798--> Adobe Commerce beim Ausführen der `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` während des `bin/magento setup:upgrade` nicht mehr mit einem Fehler wegen unzureichendem Arbeitsspeicher fehl. Zuvor hat Adobe Commerce bei der Initialisierung von Berechtigungen nicht die Batch-Größe für die Sammlung verwendet, sondern stattdessen eine Sammlung aller Unternehmensrollen geladen.

![Problem behoben](../assets/fix.svg) Benutzende von <!--- MC-40551--> können jetzt benutzerdefinierte Attributwerte von Kunden bearbeiten und aktualisieren. Zuvor waren diese Attribute nicht ordnungsgemäß an das Benutzerformular zum Erstellen und Bearbeiten gebunden. Ein Unternehmensbenutzer konnte verschiedene Attributwerte eingeben, aber Adobe Commerce hat diese Werte nicht korrekt gespeichert.

![Problem behoben](../assets/fix.svg) <!--- MC-32653--> Der Ressourcenbaum für Berechtigungen für Unternehmensrollen kann jetzt wie erwartet übersetzt werden. Zuvor wurde die Berechtigungsstruktur nicht übersetzt, obwohl gültige Übersetzungsdateien vorhanden waren.

![Problem behoben](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce speichert jetzt benutzerdefinierte Kundenattributwerte für B2B-Benutzer wie erwartet. Zuvor löste das Erstellen eines Unternehmenskontos, das benutzerdefinierte Kundenattribute enthielt, einen Vorlagenfehler aus, und Adobe Commerce konnte das Formular nicht erfolgreich laden. Durch Hinzufügen eines Arguments zum Layout von `company_create_account` wurde dieses Problem behoben.

![Problem behoben](../assets/fix.svg) <!--- MC-41721--> Filter für Firmenbenutzer wie Alle Benutzer anzeigen, Aktive Benutzer anzeigen und Inaktive Benutzer anzeigen funktionieren jetzt erwartungsgemäß. Zuvor hatten Filteraktionen auf der Seite „Firmenbenutzer“ einen JavaScript-Fehler verursacht.

### Unternehmenskredit

![Problem behoben](../assets/fix.svg) <!--- MC-41551--> Administratoren mit eingeschränkten Konten, die nur Berechtigungen auf Website-Ebene enthalten, können jetzt ein Unternehmen erstellen, das eine andere Währung als die Website verwendet.

![Problem behoben](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce sendet jetzt Unternehmens-E-Mails von der richtigen `from`-E-Mail-Adresse und dem richtigen Umfang. Zuvor berücksichtigte Adobe Commerce beim Senden der Kreditzuweisung eines Unternehmens oder bei der E-Mail-Aktualisierung den Umfang der Website nicht.

### Schnellauftrag

![Problem behoben](../assets/fix.svg) <!--- MC-42104--> Das Erstellen einer Bestellung mithilfe einer Schnellbestellung aus einer CSV-Datei funktioniert jetzt mit nicht vorhandenen SKUs wie erwartet.

![Problem behoben](../assets/fix.svg) <!--- MC-40268--> Die Verwendung der Schnellbestellung zur Suche nach mehreren SKUs funktioniert jetzt erwartungsgemäß. Zuvor enthielten die Ergebnisse doppelte Einträge.

![Problem behoben](../assets/fix.svg) <!--- MC-40261--> In der Anzeige der Liste Hinzugefügte Produkte werden SKUs, die in Klein- und Großbuchstaben eingegeben wurden, jetzt gleich behandelt, wenn Sie SKUs verwenden, um mehrere Produkte während der Schnellbestellung auszuwählen.

![Problem behoben](../assets/fix.svg) Durch <!--- MC-40225--> Verwendung von Schnellbestellungen werden jetzt Produkte in der vom Einkäufer angegebenen Menge hinzugefügt. Zuvor hat Adobe Commerce nur ein Produkt hinzugefügt, selbst wenn die vom Käufer angegebene Menge ein Produkt überschreitet.

![Problem behoben](../assets/fix.svg) <!--- MC-41283--> Die Funktion zur automatischen Vervollständigung von Schnellbestellungen funktioniert jetzt mit partiellen SKUs.

![Problem behoben](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce zeigt jetzt Produkte an, die in der Auto-Suggest-Liste und den Suchergebnissen **der Seite „Schnellbestellung“ als** Nicht einzeln sichtbar“ konfiguriert wurden.

![Problem behoben](../assets/fix.svg) Käuferinnen und <!--- MC-42402--> können jetzt das Schnellbestellungsformular verwenden, um mehrere Produkte nach SKUs hinzuzufügen, die Großbuchstaben enthalten. Zuvor wurde nur das erste Produkt hinzugefügt.

### Verhandelbares Angebot

![Problem behoben](../assets/fix.svg) <!--- MC-41232--> Käufer werden jetzt zur Seite mit verhandelbaren Angeboten weitergeleitet, nachdem sie den Link zu einem verhandelbaren Angebot in das URL-Feld eingefügt und sich erfolgreich angemeldet haben. Zuvor wurden Käufer zur Seite Mein Konto weitergeleitet.

![Problem behoben](../assets/fix.svg) Die Neuanordnung von <!--- MC-39317--> funktioniert jetzt wie erwartet für Bestellungen, die ein Produkt mit einer anpassbaren Datumsoption für ein Kundenkonto enthalten, das während des Checkouts erstellt wurde. Zuvor hat Adobe Commerce die Neuanordnung nicht verarbeitet und den folgenden Fehler angezeigt: `The product has required options. Enter the options and try again`.

![Problem behoben](../assets/fix.svg) <!--- MC-39063--> Die Lieferadresse für ein verhandelbares Angebot kann während des Checkouts nicht mehr bearbeitet werden, wenn das Bestellmodul deaktiviert ist. Dieses Verhalten resultierte aus einer vorherigen Fehlerbehebung, bei der `isQuoteAddressLocked` aus dem verhandelbaren Angebot-Checkout-Renderer entfernt wurde.

![Problem behoben](../assets/fix.svg) <!--- MC-38967--> Händler können jetzt Produkte zu einem verhandelbaren Angebot vom Administrator hinzufügen.

### Bestellungen

![Es wurde ](../assets/fix.svg), <!--- MC-39983--> Adobe Commerce jetzt eine informative Fehlermeldung wie erwartet anzeigt, wenn Sie eine Bestellung mit PayPal Express Checkout aufgeben, wenn das **[!UICONTROL Name Prefix]** auf `required` gesetzt ist. Zuvor hat Adobe Commerce keine Bestellung aufgegeben oder keine Fehlermeldung angezeigt.

![Problem behoben](../assets/fix.svg) <!--- MC-39620--> Die Benutzeroberflächenkomponente für die Rechnungsadresse im Bestellmodul verwendet jetzt die Angebotsadresse korrekt, wenn der Google Tag Manager aktiviert ist. Zuvor ist auf der Zahlungsseite ein JavaScript-Fehler aufgetreten.

### Anforderungslisten

![Problem behoben](../assets/fix.svg) <!--- MC-40426--> Händler können jetzt den Endpunkt POST-`rest/all/V1/requisition_lists` verwenden, um eine Anforderungsliste für einen Kunden zu erstellen. Zuvor gab Adobe Commerce diesen 400-Fehler, als Sie versuchten, eine Anforderungsliste zu erstellen: `Could not save Requisition List`.

![Problem behoben](../assets/fix.svg) <!--- MC-41123--> Die Schaltfläche **[!UICONTROL Add to Requisition List]** wird jetzt für die vorrätigen Produkte eines Warenkorbs angezeigt, wenn der Warenkorb auch nicht vorrätige Produkte enthält. Wenn ein Warenkorb zuvor zwei Produkte enthielt, von denen eines nicht vorrätig war, wurde bei keinem der Produkte die Schaltfläche _[!UICONTROL Add to Requisition List]_angezeigt.

![Problem behoben](../assets/fix.svg) <!--- MC-40877--> Sie können jetzt die REST-API verwenden, um ein Produkt zu einer Anforderungsliste hinzuzufügen.

![Problem behoben](../assets/fix.svg) <!--- MC-40155--> Werte **[!UICONTROL Latest Activity Date]** Anforderungsliste entsprechen nun dem Gebietsschemaformat.

![Problem behoben](../assets/fix.svg) Wenn Sie ein Produktpaket aus einer Anforderungsliste bearbeiten, gibt <!--- MC-39580--> Adobe Commerce keinen schwerwiegenden Fehler mehr aus.

![Problem behoben](../assets/fix.svg) <!--- MC-40454--> Adobe Commerce zeigt jetzt den richtigen Produktpreis an, wenn Sie ein Produkt mit einer anpassbaren Option `(File)` einer Wunschliste aus einer Anforderungsliste hinzufügen. Der Link zur hochgeladenen Datei ist ebenfalls erwartungsgemäß sichtbar. Zuvor zeigte Adobe Commerce falsche Produktpreise an und zeigte den Link zur Datei nicht an.

![Problem behoben](../assets/fix.svg) <!--- MC-36383--> Produkte mit einer anpassbaren Option `(File)` können jetzt über eine Anforderungsliste zum Warenkorb hinzugefügt werden.

### Freigegebener Katalog

![Problem behoben](../assets/fix.svg) <!--- MC-40497--> Ein Administrator mit der Rolle , die auf eine bestimmte Website beschränkt ist, kann jetzt einen freigegebenen Katalog erstellen, anzeigen und bearbeiten. Zuvor gab es in Adobe Commerce einen schwerwiegenden Fehler, wenn ein Administrator mit einer eingeschränkten Rolle versuchte, einen freigegebenen Katalog zu erstellen.

![Problem behoben](../assets/fix.svg) <!--- MC-41337--> Ergebnisse der mehrschichtigen Navigation enthalten jetzt eine genaue Anzahl von Produkten mit gefilterten Attributen, und Käufer können jetzt mehrere Filter anwenden. Zuvor konnte nur ein Filter angewendet werden, und in Adobe Commerce wurde in der mehrschichtigen Navigation eine ungenaue Produktzahl angezeigt.

![Problem behoben](../assets/fix.svg) <!--- MC-40779--> Adobe Commerce zeigt jetzt die Produktzahlen in mehrschichtigen Navigationsfiltern in den Suchergebnissen korrekt an. Zuvor hat ein Plug-in für die Suchergebnisseite Elasticsearch nicht verwendet, sondern eine neue Abfrage an die Datenbank gesendet.

![Problem behoben](../assets/fix.svg) <!--- MC-39978--> Adobe Commerce löscht keine Stufenpreise mehr, wenn ein Händler alle Produkte aus einem freigegebenen Standardkatalog löscht.

![Problem behoben](../assets/fix.svg) <!--- MC-39802--> Filter werden jetzt nach der aktuellen Kategorie gefiltert und auf allen Seiten korrekt angezeigt, wenn freigegebene Kataloge aktiviert sind. Zuvor wurden Filter nur für die aktuelle Seite falsch berechnet und nicht nach der aktuellen Kategorie gefiltert.

![Problem behoben](../assets/fix.svg) <!--- MC-39522--> Die Abfrage &quot;GraphQL `products`&quot; gibt die Preisspanne und Kategorie eines Produkts für Produkte, die keinem freigegebenen Katalog zugewiesen sind, nicht mehr zurück, wenn der freigegebene Katalog aktiviert ist. Zuvor gab die Abfrage die Aggregationen des Produkts zurück, obwohl das Produkt selbst nicht im `items`-Array zurückgegeben wurde.

## B2B v1.3.1

*9. Februar 2021*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce 2.4.0 und neuere Versionen

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.2 wurde hinzugefügt.

![Neu](../assets/new.svg) Für Bestellungen werden jetzt Online-Zahlungsmethoden unterstützt.

![Es wurde ](../assets/fix.svg), dass beim Hinzufügen eines konfigurierbaren Produkts zum Warenkorb direkt über eine Anforderungsliste, wenn dieses Produkt in einer früheren Bestellung verwendet wurde, kein Systemfehler mehr zurückgegeben wird.

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt jetzt bei Bestellungen, wenn eine Aufspaltungs-Datenbankkonfiguration bereitgestellt wird, die Registerkarte Meine Genehmigung erforderlich korrekt an.

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt jetzt Details zu Bundle-Produkten und Geschenkgutscheinen an, wenn Sie Bestellungen anzeigen.

![Problem behoben](../assets/fix.svg) Käufer werden jetzt wie erwartet umgeleitet, nachdem sie sich bei ihrem Konto angemeldet haben, während sie in einem Store suchten, in dem **[!UICONTROL Website Restriction]** aktiviert ist und **[!UICONTROL Restriction Mode]** auf `Private Sales: Login Only` gesetzt ist. Zuvor wurden die Käufer zur Startseite des Shops weitergeleitet. <!--- MC-38934-->

![Problem behoben](../assets/fix.svg) Der Bestellverlauf wird jetzt wie erwartet auf der Dashboard-Seite eines Unternehmensadministrators in Bereitstellungen mit einer B2B-Unternehmenshierarchie geladen, die viele Kunden enthält (mehr als 13000). Zuvor wurde der Auftragsverlauf langsam oder überhaupt nicht geladen, und in Adobe Commerce wurde ein 503-Fehler angezeigt. <!--- MC-38830-->

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt nicht mehr mehrere identische Warnmeldungen an, wenn Sie ein nicht konfiguriertes Produkt mit anpassbaren Optionen über eine Kategorieseite zu einer Anforderungsliste hinzufügen. <!--- MC-38342-->

![Problem behoben](../assets/fix.svg) Wenn freigegebene B2B-Kataloge aktiviert sind, werden neue und duplizierte Produkte jetzt wie erwartet auf der Kategorieseite angezeigt. <!--- MC-38307-->

![Problem behoben](../assets/fix.svg) Adobe Commerce behält jetzt die richtige `store_id` bei, die einem Unternehmensadministrator zugeordnet ist, wenn die Kundengruppe für ein Unternehmen aktualisiert wird. Zuvor wurde der `store_id` beim Aktualisieren der Gruppe in den Standardspeicher geändert. <!--- MC-38196-->

![Problem behoben](../assets/fix.svg) Adobe Commerce speichert jetzt ein gruppiertes Produkt in einer Anforderungsliste als Liste einfacher Produkte auf die gleiche Weise, wie es ein gruppiertes Produkt zum Warenkorb hinzufügt. Aufgrund der Art und Weise, wie Adobe Commerce gruppierte Produkte gespeichert hat, wurde der Link für ein gruppiertes Produkt aus der Anforderungsliste bisher immer zu einfachen Produkten und nicht zu dem gruppierten Produkt umgeleitet. <!--- MC-38049-->

![Es wurde ein Problem ](../assets/fix.svg). Beim Exportieren von Bestellinformationen im CSV-Format können Bestellungen jetzt nach dem Feld &quot;**[!UICONTROL Company Name]**&quot; gefiltert werden. Zuvor hat Adobe Commerce einen Fehler in `var/export/{file-id}` protokolliert. <!--- MC-37785-->

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt jetzt das Popup Anforderungsliste erstellen wie erwartet an, wenn Sie in der Storefront die Registerkarte Neue Anforderungsliste erstellen auswählen. <!--- MC-37915-->

![Problem behoben](../assets/fix.svg) Anforderungslisten enthalten nun alle gruppierten Produkte und Mengen, die der Liste hinzugefügt wurden. Wenn ein Händler zu einer Anforderungsliste navigiert ist, nachdem ihm Produkte von einer Produktdetailseite hinzugefügt wurden, hat Adobe Commerce zuvor folgenden Fehler angezeigt: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![Problem behoben](../assets/fix.svg) Wenn Sie ein Unternehmen in einer Bereitstellung mit mehreren Sites erstellen, ist die richtige Store-Ansicht jetzt mit der relevanten Website verknüpft. Zuvor war es nicht möglich, eine Firma zu erstellen, und Adobe Commerce hat folgenden Fehler angezeigt: `The store view is not in the associated website`. <!--- MC-37488-->

![Problem behoben](../assets/fix.svg) Die Bestellung von Produkten nach SKU mithilfe von Schnellbestellungen führt nicht mehr zu doppelten Produktmengen in der CSV-Datei. <!--- MC-37427-->

![Problem behoben](../assets/fix.svg) Die Schaltfläche &quot;**[!UICONTROL Add to Cart]**&quot; ist nicht mehr blockiert, wenn der Abschnitt &quot;_[!UICONTROL Enter Multiple SKUs]_&quot; auf der Seite „Schnellbestellung“ einen leeren Wert enthält. Stattdessen zeigt Adobe Commerce jetzt eine Meldung an, in der Sie aufgefordert werden, gültige SKUs einzugeben. <!--- MC-37387-->

![Es wurde ein Problem ](../assets/fix.svg): Adobe Commerce zeigt diese Meldung jetzt auf der Produktseite an, wenn Sie eine Produktüberprüfung über eine Anforderungsliste senden: `You submitted your review for moderation`. Die Überprüfung wird auch auf der Seite Ausstehende Überprüfungen angezeigt (Admin **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**). Obwohl Adobe Commerce die Überprüfung zur Liste der ausstehenden Überprüfungen hinzugefügt hat, wurde zuvor ein 404-Fehler auf der Produktseite angezeigt. <!--- MC-37119-->

![Problem behoben](../assets/fix.svg) Die Leistung des `sharedCatalogUpdateCategoryPermissions` Verbrauchers wurde verbessert. Nach dem Erstellen eines freigegebenen Katalogs verwendet der Indexer für Katalogberechtigungen jetzt nur noch die Kundengruppen-ID aus dem freigegebenen Katalog, nicht aber alle Kundengruppen. <!--- MC-36770-->

![Problem behoben](../assets/fix.svg) Benutzerdefinierte Kundenadressen-Attributfelder, die mit der nicht standardmäßigen Adresse eines Käufers verknüpft sind, werden jetzt wie erwartet im Checkout-Workflow der Storefront gespeichert. <!--- MC-36630-->

![Problem behoben](../assets/fix.svg) Bestellungen für Produkte, die zum standardmäßigen freigegebenen Katalog eines Shops gehören, können jetzt wie erwartet über die Admin REST API (`rest/V1/carts/{<CART_ID>/items`) für Einkäufer aufgegeben werden. Adobe Commerce prüft jetzt, ob das Produkt vor der Validierung freigegebener Katalogberechtigungen in `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave` einem öffentlichen Katalog zugewiesen wurde. Zuvor hat Adobe Commerce das Produkt nicht zum Warenkorb des Käufers hinzugefügt und folgenden Fehler ausgegeben: `No such shared catalog entity`. <!--- MC-36535-->

![Problem behoben](../assets/fix.svg) Adobe Commerce sendet jetzt E-Mails zur Registrierung von Unternehmensbenutzern über die Adresse des Adobe Commerce-Stores. Zuvor wurde diese E-Mail von der Adresse des Unternehmensadministrators gesendet. <!--- MC-36480-->

![Problem behoben](../assets/fix.svg) Adobe Commerce prüft jetzt benutzerdefinierte Attribute auf Duplizierung reservierter Firmenattributnamen, bevor es einem Händler erlaubt wird, ein neues Attribut zu speichern. <!--- MC-36282-->

![Problem behoben](../assets/fix.svg) Die `credit_history` Abfrage gibt jetzt die Kredithistorie des angegebenen Unternehmens für den ursprünglich zugewiesenen Betrag und den gekauften Betrag zurück. Zuvor hat diese Abfrage einen Fehler zurückgegeben.

![Problem behoben](../assets/fix.svg) Die Felder **[!UICONTROL Company]** und **[!UICONTROL Job Title]** auf der Seite Kontoinformationen bearbeiten können nicht mehr bearbeitet werden.

### Bekannte Probleme

- B2B-Käufer können Online-Zahlungsmethoden verwenden, um den üblichen Bestellfluss zu umgehen. Dieses Szenario kann eintreten, wenn der Käufer seine gesamte Checkout-Summe auf 0 reduzieren kann - z. B. durch einen Promo-Code oder eine Geschenkkarte - und dann den Code oder die Geschenkkarte entfernen kann. Selbst unter diesen Bedingungen gibt Adobe Commerce immer noch die Bestellung für den richtigen Betrag auf der Grundlage der Preise der Artikel in ihrem zugewiesenen Katalog auf. **_Problemumgehung_**: Deaktivieren Sie Geschenkkarten und Gutscheincodes, wenn Online-Zahlungsmethoden für die Bestellgenehmigung aktiviert sind. <!--- B2B-1603-->

- Käufer werden zum Warenkorb weitergeleitet, wenn sie versuchen, eine Bestellung über eine Bestellung mit PayPal Express Checkout aufzugeben, wenn **[!UICONTROL In-Context Mode]** deaktiviert ist. <!--- B2B-1604-->

- Adobe Commerce zeigt manchmal einen 404-Fehler an, wenn ein Käufer eine Bestellung erstellt und dann zur Kasse navigiert. Dieser Fehler tritt auf, wenn ein Käufer zuvor eine andere Bestellung mit einer Online-Zahlungsmethode erstellt hat, bevor er zur Kasse navigiert, ohne den vorherigen Kauf abzuschließen. Der Käufer kann die Bestellung dennoch aufgeben. **_Problemumgehung_**: Keine. <!--- B2B-1605-->

- Rabatte für eine bestimmte Zahlungsmethode bleiben während des Checkouts für eine Bestellung bestehen, auch wenn der Käufer seine Zahlungsmethode während des endgültigen Checkouts ändert. Kunden können somit einen Rabatt erhalten, zu dem sie keinen Anspruch haben. Dieses Problem tritt auf, weil für die ursprüngliche Zahlungsmethode trotz der Änderung der Zahlungsmethode weiterhin eine Warenkorbregel angewendet wird. **_Problemumgehung_**: Keine. Siehe den bekannten Artikel [Adobe Commerce 2.4.2 B2B: Rabatt bleibt für Online-Bestellungen bestehen, nachdem die Zahlungsmethode geändert wurde](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _Wissensdatenbank_. <!-- B2B-1012 -->

- Die `deleteRequisitionListOutput` Abfrage gibt Details zur gelöschten Anforderungsliste anstelle der übrigen Anforderungslisten zurück. <!--- MC-39894-->

## B2B v1.3.0

*15. Oktober 2020*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce 2.4.0 und neuere Versionen

Diese Version umfasst Verbesserungen bei Auftragsgenehmigungen, Versandmethoden, Warenkorb und der Protokollierung von Admin-Aktionen.

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.1 wurde hinzugefügt.

![Neu](../assets/new.svg) Die B2B-Bestellgenehmigungen wurden verbessert, um die Benutzerfreundlichkeit zu verbessern und Massenaktionen auf Bestellungen zu ermöglichen.

![Neu](../assets/new.svg) B2B-Händler können jetzt Versandmethoden steuern, die jeder Firma angeboten werden.<!--- BUNDLE-160 161 162 -->

![Neu](../assets/new.svg) Händler können es Benutzern jetzt ermöglichen, den Inhalt ihres Warenkorbs in einer einzigen Aktion zu löschen und diese Funktion unabhängig auf jeder Website zu konfigurieren <!--- BUNDLE-108 -->

![Neu](../assets/new.svg) B2B-Käufer können jetzt einzelne Artikel oder den gesamten Inhalt ihres Warenkorbs direkt einer Anforderungsliste hinzufügen. <!--- BUNDLE-145 144-->

![Neu](../assets/new.svg) B2B-Händler können Bestellungen vom Administrator im Namen von Kunden erstellen, indem sie „Zahlung auf Konto“ als Zahlungsmethode verwenden. <!--- BUNDLE-166 178-->

![Neu](../assets/new.svg) Händler können jetzt alle mit einem Benutzer verknüpften Angebote direkt auf der Detailseite des Kunden einsehen. <!--- BUNDLE-139 -->

![Neu](../assets/new.svg) Händler können jetzt das Raster „Kunden jetzt online“ nach Unternehmen filtern. <!--- BUNDLE-137 -->

![Neu](../assets/new.svg) Administratoren können jetzt Kunden im Administrator nach Vertriebsmitarbeiter filtern<!--- BUNDLE-110 -->

![Neu](../assets/new.svg) Um die Erstellung von betrügerischen Konten oder Spam-Konten zu reduzieren, können Händler jetzt Google reCAPTCHA auf dem neuen Unternehmensanfrageformular in der Storefront aktivieren. <!--- BUNDLE-154 -->

![Neu](../assets/new.svg) In den Unternehmensmodulen durchgeführte Admin-Aktionen werden jetzt im Admin-Aktionsprotokoll protokolliert. Aktionen werden aus allen relevanten Unternehmensmodulen protokolliert: `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`. <!--- BUNDLE-180 181 182 183 -->

![Es wurde ein Problem ](../assets/fix.svg): Adobe Commerce zeigt die Schaltfläche **[!UICONTROL Delete customer]** auf der Seite **Kunden** nicht mehr an, wenn der angemeldete Administrator nicht über die Berechtigungen zum Löschen von Kunden in Bereitstellungen verfügt, in denen B2B installiert ist. <!--- MC-35655-->

![Problem behoben](../assets/fix.svg) Die Kundengruppe wird für einen Kunden, der einer Firma zugewiesen ist, nicht mehr automatisch geändert, wenn Sie den Kunden im Kundenraster bearbeiten. <!--- MC-35254-->

![Problem behoben](../assets/fix.svg) Wenn ein Händler einen freigegebenen Katalog erstellt, werden die Berechtigungen jetzt automatisch auf `Allow` für die **[!UICONTROL Display Product Prices]**- und **[!UICONTROL Add to Cart]**-Funktionen in Kategorien festgelegt, wenn der Kundengruppe dieser Zugriff in den Katalogberechtigungseinstellungen zugewiesen wird. Zuvor wurden diese Einstellungen automatisch auf `Deny` gesetzt, auch wenn die Katalogberechtigungen auf `Allow` gesetzt waren.<!--- MC-34792-->

![Problem behoben](../assets/fix.svg) Berechtigungen für freigegebene Katalogkategorien werden nicht mehr überschrieben, wenn ein Produkt auf der Seite „Produktbearbeitung“ bearbeitet wird.<!--- MC-34777-->

![Problem behoben](../assets/fix.svg) Adobe Commerce sendet jetzt eine E-Mail-Benachrichtigung, die bestätigt, dass ein Kunde berechtigt ist, das festgelegte Kreditlimit zu überschreiten, wenn ein Händler die **[!UICONTROL Allow To Exceed Credit Limit]** aktiviert. Zuvor wurde in der von Adobe Commerce gesendeten Benachrichtigungs-E-Mail angegeben, dass der Kunde nicht berechtigt war, das Limit zu überschreiten. <!--- MC-34584-->

![Problem behoben](../assets/fix.svg) Der HTML-Container, der den Produktpreis auf Anforderungslisten umgibt, wird jetzt für die untergeordneten Elemente von gebündelten Produkten korrekt gerendert. <!--- MC-36331-->

![Problem behoben](../assets/fix.svg) Händler können jetzt die Sprache festlegen, in der die E-Mail-Adresse des Firmenbenutzers gesendet wird, wenn ein Unternehmen in mehrsprachigen Bereitstellungen erstellt wird. Zuvor ermöglicht das Dropdown-Menü den Händlern, die entsprechende Shop-Ansicht auszuwählen, und die Sprache wurde nicht angezeigt.  <!--- MC-35777-->

![Problem behoben](../assets/fix.svg) Benutzerdefinierte Kundenadressenattribut-Felder werden jetzt wie erwartet im Checkout-Workflow der Storefront angezeigt. <!--- MC-35607-->

![Problem behoben](../assets/fix.svg) Die Registerkarte Konfiguration von B2B-Funktionen wird jetzt korrekt geöffnet. <!--- MC-35458-->Gäste können jetzt QuickOrder verwenden, um Produkte zu ihrem Warenkorb hinzuzufügen und dann erfolgreich Artikel zu entfernen. Wenn ein Käufer QuickOrder verwendet hat, um mehrere Produkte zum Warenkorb hinzuzufügen, und dann ein Produkt entfernt hat, wurde das Produkt nicht entfernt. <!--- MC-35327-->

![Problem behoben](../assets/fix.svg) Ein Unternehmen kann jetzt mit der REST-API PUT `/V1/company/:companyId`-Anfrage aktualisiert werden, ohne die `region_id` anzugeben, wenn der Status als &quot;**erforderlich“ konfiguriert**. Zuvor gab Adobe Commerce einen Fehler aus, wenn er nicht angegeben wurde, obwohl `region_id` nicht erforderlich war. <!--- MC-35304-->

![Problem behoben](../assets/fix.svg) Wenn Sie ein B2B-Unternehmen mithilfe der REST-API erstellen oder aktualisieren (`http://magento.local/rest/V1/company/2`, wobei `2` die Unternehmens-ID darstellt), enthält die Antwort jetzt die erwarteten Einstellungen für `applicable_payment_method` oder `available_payment_methods`. <!--- MC-35248-->

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt keine 404-Seite mehr an, wenn ein Händler beim Erstellen einer Anforderungsliste in der Storefront die Schaltfläche **Eingabe** verwendet, anstatt auf die Schaltfläche **[!UICONTROL Save]** zu klicken.<!--- MC-35094-->

![Problem behoben](../assets/fix.svg) Kategorieberechtigungen ändern sich nicht mehr, wenn ein neues Produkt einem öffentlichen freigegebenen Katalog zugewiesen wird. Zuvor wurden Kategorieberechtigungen dupliziert. <!--- MC-34386-->

![Problem behoben](../assets/fix.svg) Beim REST-API-Endpunkt PUT `rest/default/V1/company/{id}`, mit dem die Unternehmens-E-Mail aktualisiert wird, wird nicht mehr zwischen Groß- und Kleinschreibung unterschieden. <!--- MC-34308-->

![Problem behoben](../assets/fix.svg) Die Deaktivierung von Belohnungsmodulen wirkt sich nicht mehr auf B2B-Funktionen in Kundenkonten aus. Wenn die Belohnungsmodule zuvor deaktiviert waren, wurden die folgenden B2B-bezogenen Registerkarten nicht angezeigt: Firmenprofil, Firmenbenutzer sowie Rollen und Berechtigungen.<!--- MC-34191-->

![Es wurde ein Problem ](../assets/fix.svg): Adobe Commerce verwendet jetzt den richtigen Absendernamen in E-Mail-Benachrichtigungen, wenn Änderungen an Unternehmenskonten vorgenommen werden. Zuvor verwendete Adobe Commerce für alle E-Mails den allgemeinen Absendernamen des Kontakts, der im Standardbereich definiert ist. <!--- MC-33917-->

![Problem behoben](../assets/fix.svg) Sie können jetzt erfolgreich Multishipping für Bestellungen implementieren, die sowohl physische als auch virtuelle Produkte enthalten. <!--- MC-33818-->

![Problem behoben](../assets/fix.svg) Händler können jetzt Firmenbenutzer aus dem Abschnitt _[!UICONTROL Company Users]_auf den Seiten Mein Konto und Unternehmensstruktur erstellen, wenn **[!UICONTROL Access Restriction]**aktiviert und **[!UICONTROL Restriction Mode]**auf `Sales: Login Only` gesetzt ist. Zuvor gab Adobe Commerce diesen Fehler aus, als ein Händler versuchte, einen Benutzer zu erstellen: `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![Problem behoben](../assets/fix.svg) Adobe Commerce setzt die Kundengruppe eines Kunden nicht mehr auf den Standardwert zurück, wenn ein Kunde seine Kontoinformationen speichert. <!--- MC-33554-->

![Problem behoben](../assets/fix.svg) Adobe Commerce gibt keinen schwerwiegenden Fehler mehr aus, wenn ein Administrator eine Kundin oder einen Kunden, die bzw. der über einen aktiven Warenkorb verfügt, einer Kundengruppe zuweist. <!--- MC-33313-->

![Problem behoben](../assets/fix.svg) Adobe Commerce bietet jetzt ein `addToCart` Datenschichtereignis für Schnellauftrags- und Anforderungslistenseiten.  <!--- MC-33295-->

![Problem behoben](../assets/fix.svg) Benachrichtigungs-E-Mails, die an einem Unternehmen zugewiesene Vertriebsmitarbeiter gesendet werden, enthalten jetzt das zugewiesene Firmenlogo. Zuvor enthielt die Benachrichtigungs-E-Mail das standardmäßige LUMA-Logo, nicht das hochgeladene Firmenlogo. <!--- MC-33232-->

![Problem behoben](../assets/fix.svg) Eine Anforderungsliste enthält jetzt alle gruppierten Produkte und Mengen, die der Liste hinzugefügt wurden. Wenn ein Händler zu einer Anforderungsliste navigiert ist, nachdem ihm Produkte von einer Produktdetailseite hinzugefügt wurden, hat Adobe Commerce zuvor folgenden Fehler angezeigt: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![Problem behoben](../assets/fix.svg) Die `products`-Abfrage gibt jetzt ein genaues `total_count` zurück, wenn der freigegebene Katalog aktiviert ist. <!--- MC-42268-->

![Problem behoben](../assets/fix.svg) Die Seiten Unternehmenskonfiguration und Firma erstellen funktionieren jetzt wie erwartet, nachdem Sie eine Online-Versandmethode deaktiviert haben. Die Überprüfung wurde hinzugefügt, um die versuchte Verarbeitung deaktivierter Versandmodule zu verhindern. Zuvor hat Adobe Commerce folgenden Fehler angezeigt: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![Problem behoben](../assets/fix.svg) Der Speicherverbrauch für Integrationstests wurde reduziert, was die Testleistung verbessert und die Zeit für den Abschluss des Tests verkürzt. <!--- AC-266-->

## B2B v1.2.0

*28. Juli 2020*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce 2.4.0 und neuere Versionen

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.0 wurde hinzugefügt.

![Neu](../assets/new.svg) Storefront Order Search, mit einem zusätzlichen Dank für den Beitrag von Marek Mularczyk von [Divante](https://www.divante.com/) und Community-Mitgliedern.

![Neu](../assets/new.svg) Bestellungen werden verbessert und neu geschrieben. Sie sind jetzt standardmäßig in Adobe Commerce enthalten.

![Neu](../assets/new.svg) Genehmigungsregeln für Bestellungen wurden implementiert. Diese Regeln ermöglichen es Benutzern, den Workflow „Bestellung“ zu steuern, indem sie Einkaufsregeln für Bestellungen erstellen.

![Neu](../assets/new.svg) Die Anmeldung als Kunde ist jetzt standardmäßig in Adobe Commerce enthalten. Mit dieser Funktion können Site-Mitarbeiter Kunden unterstützen, indem sie sich als Kunde anmelden, um zu sehen, was sie sehen.

![Problem behoben](../assets/fix.svg) Attributaggregationen funktionieren jetzt ordnungsgemäß für die mehrschichtige Navigation mit Elasticsearch

![Problem behoben](../assets/fix.svg) Die Suche nach Bestellungen anhand von Sonderzeichen funktioniert jetzt ordnungsgemäß.

![Problem behoben](../assets/fix.svg) Durch Klicken auf die Schaltfläche **[!UICONTROL Clear All]** werden nun alle Filter erweitert und nicht reduziert.

![Problem behoben](../assets/fix.svg) Produkt-SKU/Name ist jetzt in der Zusammenfassung des Suchfilters für den Auftragsverlauf enthalten.

![Problem behoben](../assets/fix.svg) Die Sortieranzeige wird jetzt korrekt im Raster Meine Bestellungen angezeigt.

![Problem behoben](../assets/fix.svg) Jetzt können Sie nur noch einmal auf die Schaltflächen Genehmigen, Abbrechen, Ablehnen und Bestellung klicken. Zuvor konnten Sie auf die Schaltfläche mehrmals klicken.

![Problem behoben](../assets/fix.svg) Die Schaltflächen „Bestellung genehmigen“, „Ablehnen“, „Abbrechen“ und „Validieren“ werden jetzt auf Mobilgeräten korrekt dargestellt.

![Problem behoben](../assets/fix.svg) Bei der vorherigen Genehmigung einer Bestellung mit einem Rabatt, der abgelaufen ist, wurde die Bestellung mit dem vollständigen Betrag platziert und die Bestellsumme nicht aktualisiert. Jetzt wird die Bestellsumme aktualisiert, um die richtige Summe anzuzeigen.

![Problem behoben](../assets/fix.svg) In Version 2.3.4 wurde ein Problem eingeführt, bei dem benutzerdefinierte Erweiterungsattribute nicht von der Kundenadresse zur Angebotsadresse kopiert wurden. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Wenn B2B installiert ist, wird beim Zuweisen von Kategorien zu freigegebenen Katalogen ein SQL-Fehler angezeigt. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Aufgrund eines falschen Variablentypwerts konnten Admins keine konfigurierbaren Produkte zu einer Bestellung hinzufügen. Die Dropdown-Listen für Optionen werden nicht befüllt. Diese Funktion funktioniert jetzt ordnungsgemäß.

![Es wurde ](../assets/fix.svg) Problem behoben: Beim Bearbeiten von Kategorieberechtigungen für die Gruppe Nicht angemeldet trat beim Speichern der Änderungen zuvor ein Fehler auf. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Es wurde eine Korrektur hinzugefügt, mit der Store-Administratoren Produkte zu einer Bestellung hinzufügen können, die nicht im freigegebenen Katalog enthalten sind. Zuvor wurde eine Fehlermeldung angezeigt, wenn ein Element hinzugefügt wurde, das sich nicht im Katalog befindet.

![Problem behoben](../assets/fix.svg) [!BADGE nur PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."} Zuvor trat nach dem Ausführen des `php bin/magento indexer:set-dimensions-mode catalog_product_price website` und dem anschließenden Versuch, einen freigegebenen Katalog zu erstellen, ein Fehler auf. Dieses Problem wurde behoben.

![Es wurde ](../assets/fix.svg) Problem behoben, dass beim Hinzufügen eines Unternehmens und Zuweisen des Unternehmensadministrators zu einer nicht standardmäßigen Website die falsche Site-ID gesendet wurde, was einen Fehler verursachte. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Nachdem ein Kunde in eine andere Kundengruppe verschoben wurde, schlug das Hinzufügen eines Produkts zu einer Bestellung mit _Schnellbestellung_ mit einem Fehler fehl. Dieses Problem wurde behoben.

![Es wurde ](../assets/fix.svg) Problem behoben, dass beim Versuch, die Web-API mit einem B2B-Zitat zu verwenden, zuvor ein falscher Wert an die API gesendet wurde, was zu einem Fehler führte. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Zuvor trat ein Fehler auf, wenn ein Unternehmen über die API auf „Aktiv“ gesetzt wurde. Dieses Problem wurde jetzt behoben.

![Fehlerkorrektur](../assets/fix.svg) Aufgrund eines nicht benötigten `form`-Tags wird die Bestellseite automatisch aktualisiert, wenn Sie die Eingabetaste drücken, nachdem Sie eine vorgeschlagene Versandgebühr geändert haben. Dieses Problem wurde behoben.

![Es wurde ](../assets/fix.svg) Problem behoben: Beim Festlegen eines Produktanzeigebeschränkens auf einer Katalogseite, wobei dieser Grenzwert kleiner als die Anzahl der Gesamtprodukte war, ist zuvor ein Fehler aufgetreten. Diese Funktion funktioniert jetzt erwartungsgemäß.

![Problem behoben](../assets/fix.svg) Zuvor wurde beim Ändern des Administrators eines Unternehmens die ursprüngliche Admin-Adresse zum neuen Administrator kopiert, sodass er zwei Adressen erhielt. Jetzt wird nur noch die richtige Adresse hinzugefügt.

![Es wurde ein Problem ](../assets/fix.svg). Zuvor schlug die Verwendung der -API zum Speichern eines Angebotselements, wenn Git auf „Zulässig“ eingestellt war, und „Kunde benachrichtigen“ fehl. Dieser API-Aufruf funktioniert jetzt erwartungsgemäß.

![Problem behoben](../assets/fix.svg) Die feste Produktsteuer wird jetzt auf der Seite mit den Angebotsdetails angezeigt.

![Es wurde ](../assets/fix.svg) Problem behoben: Zuvor konnte die Datei nicht heruntergeladen werden, wenn auf der Seite Meine Anführungszeichen auf der Registerkarte Kommentare auf eine Anlage geklickt wurde. Dieses Verhalten funktioniert jetzt erwartungsgemäß.

### Bekannte Probleme

- Adobe Commerce löst während des Upgrades auf B2B 1.2.0 in einer Bereitstellung für mehrere Websites eine Ausnahme aus. Beim Ausführen von `setup:upgrade` tritt dieser Fehler im `PurchaseOrder` Modul auf: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **Problemumgehung**: Installieren Sie die `B2B-716 Add NonTransactionableInterface`-Schnittstelle zum `InitPurchaseOrderSalesSequence`-Daten-Patch-Hotfix, der jetzt im Abschnitt **Mein Konto** > **Downloads** des `magento.com` verfügbar ist.
- Wenn ein Rabattcode abläuft, bevor eine Bestellung genehmigt wurde, zeigt die Bestellung weiterhin den reduzierten Betrag an. Nach der Genehmigung der Bestellung wird die Bestellung jedoch zum nicht reduzierten Gesamtbetrag aufgegeben. **Problemumgehung**: Installieren Sie den `B2B-709 Purchase Order Discount patch` Hotfix für dieses Problem, der jetzt im Abschnitt **Mein Konto** > **Downloads** von `magento.com` verfügbar ist.
- Wenn Artikel in einer Bestellung nicht vorrätig sind oder die Menge nicht ausreicht, wenn die Bestellung in eine tatsächliche Bestellung umgewandelt wird, tritt ein Fehler auf. Wenn Nachbestellungen aktiviert sind, wird die Bestellung normal verarbeitet.
