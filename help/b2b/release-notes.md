---
title: '[!DNL Adobe Commerce B2B] Versionshinweise'
description: prüfen im Versionshinweise nach Informationen zu Änderungen in [!DNL Adobe Commerce B2B] Versionen.
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: de145205e5fcdcb49ca7626b2666e82af102344f
workflow-type: tm+mt
source-wordcount: '8702'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B] Versionshinweise

Diese Versionshinweise für die B2B Erweiterung Erfassungsergänzungen und Korrekturen, die Adobe Systems während eines Versionszyklus hinzugefügt hat, darunter:

![Neu](../assets/new.svg) Neue Funktionen
![Problem behoben](../assets/fix.svg) Fehlerbehebungen und Verbesserungen
![Bekanntes Problem](../assets/bug.svg) Bekannte Probleme

>[!NOTE]
>
>Unter [Produktverfügbarkeit](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html?lang=de) finden Sie Informationen zu Versionen der B2B-Commerce-Erweiterung, die für verfügbare Adobe Commerce-Versionen unterstützt werden.

## B2B 1.5.2

*8. April 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Sicherheitspatches der Adobe Commerce-Versionen 2.4.8, 2.4.7-p5 und 2.4.6-p10.
Kompatibel mit Adobe Commerce 2.4.7 bis 2.4.7-p4, 2.4.6 bis 2.4.6-p9

Die B2B Version 1.5.2 umfasst Qualitätsverbesserungen und Fehlerbehebungen.

### Geschäftsleitung

![Neu](../assets/new.svg)<!-- B2B-4123 -->Administratoren können jetzt mithilfe des Storefront-Umschalters mehrere Unternehmen von einem einzigen Konto aus verwalten. Zu den wichtigsten Vorteilen gehören:

- **Vereinfachte Verwaltung mehrerer Unternehmen** Administratoren können jetzt mehrere Unternehmen von einem Benutzerkonto aus überwachen, sodass keine separaten Anmeldungen für jedes Unternehmen erstellt und verwaltet werden müssen.
- **Effizienter Unternehmenswechsel** Eine intuitive Benutzeroberfläche ermöglicht Administratoren den schnellen Wechsel zwischen Unternehmen und Aktualisierungen, wodurch die Produktivität bei der Verwaltung mehrerer Entitäten verbessert wird.
- **Optimierte Abläufe** - Regionale Manager und Geschäftsführer können alle ihre Unternehmen zentral verwalten, was eine schnellere Entscheidungsfindung und einen reibungsloseren Geschäftsbetrieb ermöglicht.

Diese Verbesserung baut auf der Multi-Company-Membership-Funktion von B2B 1.5.0 auf, die es Benutzern ermöglichte, mehreren Unternehmen anzugehören, aber keinen unternehmensübergreifenden Admin-Zugriff unterstützte. Durch den Umschalter für Unternehmen entfällt die Notwendigkeit separater Administratorkonten, während die ordnungsgemäße Zugriffssteuerung und unternehmensspezifische Ansichten beibehalten werden.

### Firma

![Problem behoben](../assets/fix.svg)<!-- B2B-4480 --> Es wurde ein Problem behoben, bei dem Gastkunden eine `No such entity with cartId = ?` Fehlermeldung angezeigt wurde, wenn sie sich als Firmenbenutzer mit Produkten in ihrem Warenkorb anmeldeten.

### Verhandelbares Angebot

![Problem behoben](../assets/fix.svg) Die B2B-Version 1.5.2 enthält die folgenden Fehlerbehebungen für verhandelbare Angebote:

- &#x200B;<!-- B2B-3252 -->Das Feld [!UICONTROL Line Item Discount Amount] validiert jetzt die Eingabe, um die Eingabe negativer Rabattwerte zu verhindern.
- &#x200B;<!-- B2B-3224 -->Es wurde ein Problem mit dem Benutzererlebnis behoben, bei dem lange Zeileneintragsnotizen abgeschnitten und für B2B-Kunden schwer lesbar waren.
- &#x200B;<!-- B2B-2865 -->B2B-Kunden können jetzt Produktmengen mithilfe von Dezimalwerten (z. B. 1.5 oder 2.75) angeben, wenn sie Angebote erstellen.

### Angebotsvorlage

![Neu](../assets/new.svg)<!-- B2B-4104 --> Neue Möglichkeit für B2B-Käufer und -Verkäufer, externe Dokument-Links an Angebotsvorlagen anzuhängen. Diese Funktion ermöglicht die direkte Verknüpfung mit Dokumenten, die in -Services wie DocuSign und Adobe Sign gehostet werden, aus Anführungszeichen und ergänzt so die vorhandene Funktion zum Anhängen von Dateien. Zu den wichtigsten Vorteilen gehören:

- Optimierte Zusammenarbeit durch direkten Zugriff auf wichtig Vereinbarungen und Verträge
- Erhöhte Transparenz durch sofortigen Zugriff auf die neueste Dokumentation
- Schnellere Angebotsverhandlungen, da Dateien nicht mehr heruntergeladen und hochgeladen werden müssen
- Flexibles Dokumentenmanagement mithilfe externer Dokumentenhosting-Services

## B2B 1.5.1

*11. Februar 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Sicherheitsaktualisierungen der Adobe Commerce-Versionen 2.4.7-p4+ und 2.4.6-p9+.
Kompatibel mit Adobe Commerce 2.4.8-beta1 bis 2.4.8-beta2, 2.4.7 bis 2.4.7-p3, 2.4.6 bis 2.4.9-p8

Die B2B-Version 1.5.1 enthält Qualitätsverbesserungen und Fehlerbehebungen.

### Firma

![Problem behoben](../assets/fix.svg)<!-- B2B-4422 --> Wenn ein Kunde versucht, auf der Seite „Angebotsdetails“ einen anderen Anbieter zu wählen, leitet das System den Kunden jetzt auf eine Seite *Zugriff verweigert* um sicherzustellen, dass ein für ein Unternehmen erstelltes Angebot nicht für die Bestellung mit den Preisen eines anderen Unternehmens verwendet werden kann. Zuvor konnte ein Benutzer ein Angebot mit dem Preis für ein Unternehmen erstellen und dann zu einem anderen Unternehmen wechseln, um eine Bestellung mit unterschiedlichen Preisen aufzugeben.

### Rabatte auf Einzelposten

![Problem behoben](../assets/fix.svg)<!-- B2B-2938 --> Verbesserte Systemeffizienz durch Behebung einer Leistungsbeeinträchtigung, die im Szenario zur Neuberechnung des Angebots beobachtet wurde. Zuvor wurden zu jedem Warenkorb-Zeileneintrag zwei neue Entitäten hinzugefügt, was zu einem merklichen Anstieg der Datenbankanfragen führte, was zu einer langsameren Leistung führte.

### Verhandelbares Angebot

![Es wurde ](../assets/fix.svg)<!-- B2B-3820 --> Problem behoben: Das System behält jetzt die Position von Benutzeroberflächenelementen bei, wenn die JavaScript-Validierung auf die *[!UICONTROL min/max qty]* Felder auf der Seite „Zitatvorlage“ der Luma-Storefront angewendet wird. Zuvor hat das Anwenden der JavaScript-Validierung auf diese Felder dazu geführt, dass sich andere Benutzeroberflächenelemente auf der Seite verschoben haben.

### Warenkorb

![Fest Problem](../assets/fix.svg)<!-- B2B-4222 --> Es wurde ein neues Warenkorb-Verwaltungssystem eingeführt, das die Shopping-Erlebnis für Benutzer, die mehrere Firma Konten verwalten, optimiert. Das neue System ordnet Warenkörbe Kontakt Unternehmen und nicht dem Kunden Konto zu, um die Shopping-Erlebnis zu rationalisieren und die arbeitsablauf zu verbessern, indem es die folgenden Funktionen unterstützt.

- **Unternehmensspezifische Warenkörbe:** Warenkörbe sind jetzt mit Kontakt Unternehmen verknüpft, um Firma-spezifische Preis- und Produktoptionen zu unterstützen.
- **Nahtloser** Wechsel – Benutzer können problemlos zwischen verschiedenen Firma Konten wechseln, ohne dass sich dies auf den Inhalt der Warenkorb der einzelnen Firma auswirkt.
- **Kontextbezogene Integrität**: Alle Warenkorb Details bleiben im Kontext der jeweiligen Firma und bieten eine konsistente und zuverlässige Shopping-Erlebnis.

## B2B 1.5.0

*30. Oktober 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Patch-Versionen für Adobe Commerce 2.4.7-p3+ und 2.4.6-p8+.
Kompatibel mit Adobe Commerce 2.4.8-beta1, 2.4.7 bis 2.4.7-p2, 2.4.6 bis 2.4.6-p7.

Adobe Commerce B2B Version 1.5.0 ist auch mit PHP 8.3 kompatibel und unterstützt den [GraphQL Application Server](https://experienceleague.adobe.com/de/docs/commerce-operations/performance-best-practices/concepts/application-server).

Die B2B-Version 1.5.0 enthält neue Funktionen, Qualitätsverbesserungen und Fehlerbehebungen.

>[!NOTE]
>
> Erfahren Sie mehr über abwärtsinkompatible Änderungen (BICs), die in der B2B-Version 1.5.0 eingeführt wurden, indem Sie die Highlights und Referenzinformationen im Thema [Abwärtsinkompatible Änderungen](backward-incompatible-changes.md) überprüfen.

### Unternehmensleitung

![Neu](../assets/new.svg) **Unternehmensverwaltung**<!--B2B-2901--> - Händler können jetzt Adobe Commerce-Unternehmen als hierarchische Organisationen anzeigen und verwalten, indem sie Unternehmen bestimmten Mutterunternehmen zuweisen. Nachdem eine Firma einer übergeordneten Firma zugewiesen wurde, kann der Administrator der übergeordneten Firma das Firmenkonto verwalten. Nur autorisierte Admin-Benutzerinnen und -Benutzer können Unternehmenszuweisungen hinzufügen und verwalten. Weitere Informationen finden Sie unter [Unternehmenshierarchie verwalten](manage-company-hierarchy.md).

- Fügen Sie Unternehmenszuweisungen über den neuen Abschnitt *[!UICONTROL Company Hierarchy]* auf der Seite *[!UICONTROL Company Account]* in der Admin Console hinzu und verwalten Sie diese.

- Sortieren und Filtern von Unternehmen nach der neuen *[!UICONTROL Company Type]*. Im Raster Firmen gibt die Spalte *[!UICONTROL Company Type]* an, ob eine Firma eine einzelne Firma oder Teil einer Organisationshierarchie (über- oder untergeordnet) ist.

![](../assets/new.svg) **Neu Verwalten Firma Konfiguration in großem Maßstab**<!--B2B-2849-->: Ändern Sie Firma Konfigurationseinstellungen für ausgewählte Unternehmen schnell mithilfe der Massenaktion, die jetzt bei der *[!UICONTROL Change company setting]* Verwaltung von Unternehmen aus dem *[!UICONTROL Companies]* ODER-Raster *[!UICONTROL Company Hierarchy]* verfügbar ist. Wenn Sie z. B. einen neuen freigegebenen Katalog für eine Gruppe von Unternehmen erstellen, können Sie die Konfiguration des freigegebenen Katalogs in einer einzigen Aktion ändern, anstatt jede Firma einzeln zu bearbeiten.

![](../assets/new.svg) Neu-API Entwickler können den neuen REST-API-Endpunkt `/V1/company/{parentId}/relations` für Unternehmensbeziehungen verwenden, um Firma Zuweisungen zu erstellen, zu Ansicht und zu entfernen. Siehe [&quot;Verwalten Firma-Objekte](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) &quot; im *Web-API-Entwicklerhandbuch*.

### Unternehmenskonten

![Neu](../assets/new.svg)<!--B2B-2828--> **Zuweisung mehrerer Unternehmen** - Vereinfachen Sie den Zugriff auf Firmenkonten für Firmenbenutzer, indem Sie einen Benutzer mehreren Unternehmen zuweisen. Wenn Sie beispielsweise einen Käufer haben, der Bestellungen von mehreren Firmen-Sites aufgibt, erstellen Sie ein einziges Konto und weisen Sie diesem Konto alle Firmen zu, mit denen der Käufer arbeitet. Dann kann sich der Käufer einmal anmelden und zwischen Unternehmenskonten wechseln, indem er das Unternehmen in der Storefront auswählt.

>[!NOTE]
>
>Eine Firma User kann mehreren Unternehmen zugewiesen werden, sie können jedoch nur für eine Firma der Firma Administrator sein.

![Neu](../assets/new.svg) <!--B2B-2747--> **Unternehmen Umfang Selektor**: Bietet Firma Benutzern, die mehreren Unternehmen zugewiesen sind, die Möglichkeit, Unternehmen in der Storefront zu ändern. Wenn das Umfang gewechselt wird, werden die Daten aktualisiert, um die Informationen basierend auf dem neuen Firma Kontext anzuzeigen. Wenn der neue Firma z. B. einen anderen freigegebenen Katalog verwendet, werden dem Firma User Produkte, Preise und andere Informationen angezeigt, die auf dem neuen freigegebenen Katalog basieren. Inhalte in Bezug auf Bestellungen, Angebote und Angebotsvorlagen werden ebenfalls auf der Grundlage des Kontexts des ausgewählten Unternehmens aktualisiert.

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

- **Angebot als Entwurf**<!--B2B-2566--> Speichern – Bei der Erstellung eines [Angebots Anfrage](quote-request.md) aus dem Warenkorb können Käufer das Angebot jetzt als Entwurf speichern, damit sie es überprüfen und aktualisieren können, bevor sie den Angebotsverhandlungsprozess mit dem Verkäufer einleiten. Der Angebotsentwurf hat kein Gültigkeit Datum. Einkäufer können Angebotsentwürfe im Abschnitt [!UICONTROL My Quotes] ihres Konto-Dashboards einsehen und aktualisieren.

- **Angebot umbenennen**<!--B2B-2596--> - Käufer können jetzt einen Angebotsnamen auf der Seite [Angebotsdetails“ ](account-dashboard-my-quotes.md#quote-actions), indem sie die Option **[!UICONTROL Rename]** auswählen. Diese Option steht autorisierten Käufern beim Bearbeiten des Angebots zur Verfügung. Namensänderungsereignisse werden im Angebotsprotokoll aufgezeichnet.

- **Doppeltes Angebot**<!--B2B-2701--> - Käufer und Verkäufer können jetzt ein neues Angebot durch Kopieren eines vorhandenen Angebots erstellen. Eine Kopie wird aus der Angebotsdetailansicht erstellt, indem **[!UICONTROL Create Copy]** in der [Angebotsdetailansicht) ](quote-price-negotiation.md#button-bar) Admin oder der [Storefront“ ](account-dashboard-my-quotes.md#quote-actions).

- **Angebotsartikel in Anforderungsliste verschieben**<!--B2B-2755--> - Einkäufer haben jetzt die Möglichkeit, Produkte aus einem Angebot zu entfernen und in einer Anforderungsliste zu speichern, wenn sie sie nicht in den Angebotsaushandlungsprozess einbeziehen möchten.

- **Mehrere Produkte aus einem Angebot entfernen**<!--B2B-2881--> - Bei Angeboten mit einer großen Anzahl von Produkten können Käufer jetzt mehrere Produkte aus dem Angebot entfernen, indem sie sie auswählen und die Option *[!UICONTROL Remove]* aus dem *[!UICONTROL Actions]* auf der Seite „Angebotsdetails“ verwenden. In früheren Versionen musste ein Käufer Produkte einzeln löschen.

- **Rabattsperre für Einzelposten**<!--B2B-2597--> - Bei der Angebotsaushandlung können Verkäufer die Rabattsperre für Einzelposten verwenden, um mehr Flexibilität bei der Anwendung von Rabatten während der Angebotsaushandlung zu erhalten. Beispielsweise kann ein Verkäufer einen speziellen Positionsrabatt auf einen Artikel anwenden und den Artikel sperren, um weitere Rabatte zu verhindern. Wenn ein Artikel gesperrt ist, kann der Artikelpreis nicht aktualisiert werden, wenn ein Rabatt auf Angebotsebene angewendet wird. Siehe [Angebot für einen Einkäufer starten](sales-rep-initiates-quote.md).

![Problem behoben](../assets/fix.svg) **Fehlerbehebungen für vorhandene Angebotsfunktionen**

- Händler, die auf die *[!UICONTROL Print]* Button in den Angebotsdetails Ansicht im Admin klicken, werden nun aufgefordert, das Angebot als PDF zu speichern. Zuvor wurden Händler zu einer Seite mit Angebotsdetails umgeleitet. <!--ACP2E-1984-->

- Zuvor hat der Administrator beim Versand eines Kundenangebots mit `0` Prozentsatz und der Änderung der Menge eine Ausnahme ausgelöst, die Menge jedoch gespeichert. Nachdem diese Fehlerbehebung angewendet wurde, wird für die `0 percentage` richtige Ausnahme mit einer Meldung ausgelöst. <!--ACP2E-1742-->

- Während der Angebotsaushandlung kann ein Verkäufer jetzt einen `0%` Rabatt im Feld Ausgehandelter Angebotsrabatt angeben und das Angebot an den Käufer zurücksenden. Wenn der Verkäufer zuvor einen Rabatt von 0 % eingegeben und das Angebot an den Käufer zurückgesendet hat, hat der Administrator eine `Exception occurred during quote sending` Fehlermeldung zurückgegeben. <!--ACP2E-1742-->

- Die reCAPTCHA-Validierung funktioniert jetzt beim Checkout für ein B2B-Angebot ordnungsgemäß, wenn reCAPTCHA V3 für den Storefront-Checkout konfiguriert ist. Zuvor schlug die Validierung mit einer `recaptcha validation failed, please try again` Fehlermeldung fehl.  <!--ACP2E-2097-->

### Bestellungen

![Problem behoben](../assets/fix.svg) <!--ACP2E-1825-->Bestellungen können von einem mit dem Unternehmen verbundenen Benutzer nicht mehr aufgegeben werden, nachdem das Unternehmen gesperrt wurde. Zuvor konnte ein mit der Firma verbundener Benutzer Bestellungen aufgeben, wenn die Firma blockiert wurde.

## B2B v1.4.2-p5

*8. April 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce-Sicherheits-Patch-Versionen 2.4.7-p5+ und 2.4.6-p10+.

![Neu](../assets/new.svg) Hinzugefügte Kompatibilität mit Adobe Commerce 2.4.7-p5+ und 2.4.6-p10+ Sicherheits-Patch-Versionen.

![Problem behoben](../assets/fix.svg) Umfasst die in [Security Bulletin APSB25-26](https://helpx.adobe.com/de/security/products/magento/apsb25-26.html) dokumentierten Sicherheitskorrekturen.

{{b2b-compatibility}}

## B2B v1.4.2-p4

*11. Februar 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Sicherheitsaktualisierungen für Adobe Commerce 2.4.7-p4+ und 2.4.6-p9+.

![Neu](../assets/new.svg) Hinzugefügte Kompatibilität mit Adobe Commerce 2.4.7-p4+ und 2.4.6-p9+ Sicherheits-Patch-Versionen.

![Fest Problem](../assets/fix.svg) Schließt die im [Security Bulletin APSB25-08](https://helpx.adobe.com/de/security/products/magento/apsb25-08.html) dokumentierten Fehlerbehebungen ein.

{{b2b-compatibility}}

## B2B v1.4.2-p3

*8. Oktober 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Sicherheitsaktualisierungen für Adobe Commerce 2.4.7-p3+ und 2.4.6-p8+.

![Neu](../assets/new.svg) Hinzugefügte Kompatibilität mit Adobe Commerce 2.4.7-p3+ und 2.4.6-p8+ Sicherheits-Patch-Versionen.

![Fest Problem](../assets/fix.svg) Schließt die im [Security Bulletin APSB24-73](https://helpx.adobe.com/de/security/products/magento/apsb24-73.html) dokumentierten Fehlerbehebungen ein.

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
>Adobe Commerce B2B ab Version 1.4.2 ist mit PHP 8.2 kompatibel. Wenn Sie die Commerce-Instanz auf Version 2.4.7 oder höher aktualisieren, stellen Sie sicher, dass die Instanz PHP Version 8.2 verwendet, um die Kompatibilität mit Adobe Commerce B2B-Version zu gewährleisten. Darüber hinaus unterstützt B2B 1.4.2+ derzeit nicht den [GraphQL-Anwendungsserver](https://experienceleague.adobe.com/de/docs/commerce-operations/performance-best-practices/concepts/application-server).

## B2B v1.4.1

*7. August 2023*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} [Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html?lang=de). Kompatibel mit Adobe Commerce 2.4.7-beta1.

Die B2B-Version 1.4.1 enthält Qualitätsverbesserungen und Fehlerbehebungen.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1825-->Bestellungen können von einem mit dem Unternehmen verbundenen Benutzer nicht mehr aufgegeben werden, nachdem das Unternehmen gesperrt wurde. Zuvor konnte ein mit der Firma verbundener Benutzer Bestellungen aufgeben, wenn die Firma blockiert wurde.

![Problem behoben](../assets/fix.svg) Der <!--ACP2E-1943--> „Produkt rückgestellt“ wird jetzt korrekt in der Storefront angezeigt. Zuvor wurden Produkte, die für den Versand verfügbar waren, fälschlicherweise als zurückbestellt identifiziert.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1862-->Wenn das Unternehmensregistrierungsformular ein Kundendateitypattribut enthält, wird die während des Registrierungsprozesses hochgeladene Datei jetzt nach der Erstellung des Unternehmens in die Kontoinformationen für den Unternehmensadministrator aufgenommen. Zuvor fehlte der Anhang.

![Fest Problem](../assets/fix.svg) <!--ACP2E-1793-->Der Farbfeld Selektor für ein konfigurierbares Produkt wird nun wie erwartet in der Seite &quot;Bestellanforderungs- Liste Artikelkonfiguration&quot; angezeigt. Zuvor wurde die Musterauswahl als Dropdown-Feld auf der Konfigurationsseite des Anforderungslistenelements angezeigt.

![Fest Problem](../assets/fix.svg) <!--ACP2E-1968-->Bei der Verwendung des [Company GraphQL-Abfrage](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) zur Rückgabe Firma Details werden die Ergebnisse nun erfolgreich und fehlerfrei zurückgegeben.

## B2B v1.4.0

*13. Juni 2023*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} [Adobe Systems Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html?lang=de). Kompatibel mit Adobe Systems Commerce 2.4.7-beta1

Diese Version enthält neue Funktionen und Verbesserungen für B2B verhandelbare Angebote und mehrere Fehlerbehebungen.

![](../assets/new.svg) Neu Kompatibilität mit Adobe Systems Commerce 2.4.7-beta1 hinzugefügt.

![](../assets/new.svg) **Neu vom Verkäufer initiierte** Angebote – Verkäufer können jetzt ein Angebot für eine Einkäufer direkt aus den Rastern &quot;Angebot&quot; und &quot;Kunde&quot; in der Verwaltung initiieren. Diese Funktion rationalisiert den Angebotsprozess und reduziert die Komplexität für Kunden. Wenn ein Kunde keine Bestellung initiiert hat, kann ein Verkäufer schnell ein Angebot im Namen des Kunden erstellen und den Verhandlungsprozess starten. Bisher konnten Angebote nur von der Einkäufer oder von einem Verkäufer, der als Kunde angemeldet war, aus der Storefront erstellt werden.

![](../assets/new.svg) **Neu Zeile Artikelrabatte und -verhandlung—<!--B2B-2440--> Innerhalb eines Angebots können B2B Käufer und Verkäufer jetzt auf der Zeileneintrag Ebene verhandeln, Rabatte anwenden und Schuldverschreibungen** austauschen, bis eine Einigung erzielt wird. Die Erstellung und Aktualisierung von Notizen ist im Zeileneintrag- und Angebotsverlauf enthalten, um die Kommunikation zu verfolgen. Zuvor konnten Käufer und Verkäufer nur auf Angebotsebene Notizen austauschen und Rabatte gewähren.

![Fest Problem](../assets/fix.svg) Adobe Systems Commerce zeigt jetzt während der Zahlung korrekte Details an, wenn die Option Bestellungen aktiviert ist und ein virtuelles Angebot ausgewählt wurde, das mit der Zahlungsoption PayPal erstellt wurde. Zuvor wurden Gesamtsummen unter diesen Bedingungen als Null angezeigt.

![Problem behoben](../assets/fix.svg) Beim Speichern eines Unternehmens mit einem Kreditlimit von über 999 treten <!--ACP2E-1504--> Validierungsfehler nicht mehr auf. Zuvor wurde für Unternehmenskreditlimits, die größer als 999 waren, in Adobe Commerce ein Kommatrennzeichen eingefügt, was einen Validierungsfehler verursachte, der das Speichern von Aktualisierungen verhinderte.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1474--> Die ausgewählte Lieferadresse bleibt jetzt unverändert, wenn Sie eine Bestellung mit einem verhandelbaren Angebot aufgeben. Zuvor wurde bei der Bestellung die ausgewählte Lieferadresse in die standardmäßige Lieferadresse geändert.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1429--> In den Store-Konfigurationseinstellungen für B2B-Funktionen ist das Feld **[!UICONTROL Enable Shared Catalog direct products price assigning]** jetzt automatisch deaktiviert. Auf der Storefront wird sie ausgeblendet, wenn die **[!UICONTROL Enable Company]**- oder **[!UICONTROL Enable Shared Catalog]** auf **[!UICONTROL No]** festgelegt ist.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1683--> Beim Erstellen eines Unternehmenskontos in der Storefront validiert Commerce jetzt die E-Mail-Adresse, bevor die Unternehmensregistrierung verarbeitet wird. Wenn die E-Mail-Adresse ungültig ist, schlägt der Vorgang fehl und es werden keine Kontoaktualisierungen verarbeitet. Zuvor wurde ein Kundenkonto erstellt, selbst wenn die Anforderung zum Erstellen eines Unternehmenskontos aufgrund einer ungültigen E-Mail-Adresse fehlgeschlagen ist.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1664--> Produkt-SKUs, die doppelte Anführungszeichen im freigegebenen Katalog und in der Preisstruktur enthalten, verursachen keine Fehler mehr in der Admin-Instanz.

![Problem behoben](../assets/fix.svg) <!--ACP2E-1498--> Die Varnish-Konfiguration für die Commerce-Anwendung wurde aktualisiert, um zu verhindern, dass Gastbenutzer Daten von anderen Kundengruppen sehen.

### Bekanntes Problem

Beim Installieren oder Aktualisieren von B2B 1.4.0 auf [Adobe Commerce Version 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html?lang=de) tritt der folgende Fehler auf:

```
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

Sie können dieses Problem beheben, indem Sie manuelle Abhängigkeiten für das B2B-Sicherheitspaket hinzufügen, indem Sie manuelle Abhängigkeiten für das B2B-Sicherheitspaket mit einem &quot;[&quot; ](https://getcomposer.org/doc/04-schema.md#package-links). Anweisungen finden Sie in der [Adobe Commerce Knowledge Base](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html?lang=de).

## B2B v1.3.5-p10

*8. April 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce-Sicherheits-Patch-Versionen 2.4.6-p10+.

![Neu](../assets/new.svg) Hinzugefügte Kompatibilität mit den Adobe Commerce 2.4.6-p10 Sicherheits-Patch-Versionen.

![Fest Problem](../assets/fix.svg) Schließt die im [Security Bulletin APSB25-26](https://helpx.adobe.com/de/security/products/magento/apsb25-26.html) dokumentierten Fehlerbehebungen ein.

## B2B v1.3.5-p9

*11. Februar 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce 2.4.6-p9+ Sicherheits-Patch-Versionen.

![Neu](../assets/new.svg) Hinzugefügte Kompatibilität mit den Adobe Commerce 2.4.6-p9 Sicherheits-Patch-Versionen.

![Fest Problem](../assets/fix.svg) Schließt die im [Security Bulletin APSB25-08](https://helpx.adobe.com/de/security/products/magento/apsb25-08.html) dokumentierten Fehlerbehebungen ein.

## B2B v1.3.5-p8

*8. Oktober 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce-Sicherheits-Patch-Versionen 2.4.6-p8+.

![Neu](../assets/new.svg) Hinzugefügte Kompatibilität mit den Adobe Commerce 2.4.6-p8 Sicherheits-Patch-Versionen.

![Problem behoben](../assets/fix.svg) Umfasst die in [Security Bulletin APSB24-73](https://helpx.adobe.com/de/security/products/magento/apsb24-73.html) dokumentierten Sicherheitskorrekturen.

## B2B v1.3.5-p7

*9. August 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce-Sicherheits-Patch-Versionen 2.4.6-p7+.

![](../assets/new.svg) Neu Kompatibilität mit den Adobe Systems Commerce 2.4.6-p7 Sicherheits-Patch Versionen hinzugefügt.

## B2B v1.3.5

*14. März 2023*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce 2.4.0 - 2.4.6 und neuere Versionen

![Neu](../assets/new.svg) Version B2B 1.3.5-p2 wurde veröffentlicht, um die Kompatibilität mit Adobe Commerce 2.4.6-p2 zu unterstützen.

![Neu](../assets/new.svg) Version B2B 1.3.5-p1 wurde veröffentlicht, um die Kompatibilität mit Adobe Commerce 2.4.6-p1 zu unterstützen.

>[!NOTE]
>
>Stellen Sie nach dem Upgrade von Commerce von 2.4.6 auf [neueste Version](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html?lang=de#2.4.6) sicher, dass Sie auf die unterstützte Patch-Version B2B 1.3.5 aktualisieren. Oder aktualisieren Sie die B2B-Erweiterung von Version 1.3.5 auf Version 1.4.0 oder höher, um die neuesten Funktionen zu erhalten.

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

![Fest Problem](../assets/fix.svg) <!--- ACP2E-6829--> Das **[!UICONTROL Place Order]** Button funktioniert jetzt wie erwartet, wenn ein Kauf mit einem genehmigten Angebot abgeschlossen wird Anfrage. Probleme mit dem verhandelbaren Angebot `negotiableQuoteCheckoutSessionPlugin` Plug-in wurden behoben.

## B2B v1.3.4-p12

*8. April 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Abgestützt"} Adobe Systems Commerce 2.4.0 und neuere Versionen

![](../assets/new.svg) Neu Unterstützung für Adobe Systems Commerce 2.4.5-p12 wurde hinzugefügt.

![Problem behoben](../assets/fix.svg) Umfasst die in [Security Bulletin APSB25-26](https://helpx.adobe.com/de/security/products/magento/apsb25-26.html) dokumentierten Sicherheitskorrekturen.

## B2B v1.3.4-p11

*11. Februar 2025*

[!BADGE Unterstützt]{type=Informative tooltip="Abgestützt"} Adobe Systems Commerce 2.4.0 und neuere Versionen

![](../assets/new.svg) Neu Unterstützung für Adobe Systems Commerce 2.4.5-p11 hinzugefügt.

![Problem behoben](../assets/fix.svg) Enthält die in [Security Bulletin APSB25-08](https://helpx.adobe.com/de/security/products/magento/apsb25-08.html) dokumentierten Sicherheitskorrekturen.

## B2B v1.3.4-p10

*9. Oktober 2024*

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Adobe Commerce 2.4.0 und neuere Versionen

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.5-p10 wurde hinzugefügt.

![Problem behoben](../assets/fix.svg) Umfasst die in [Security Bulletin APSB24-73](https://helpx.adobe.com/de/security/products/magento/apsb24-73.html) dokumentierten Sicherheitskorrekturen.

## B2B v1.3.4

*9. August 2022*

[!BADGE Unterstützt]{type=Informative tooltip="Abgestützt"} Adobe Commerce 2.4.0 und neuere Versionen

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

![Fest Problem](../assets/fix.svg) <!--- ACP2E-665 -->Kunden werden jetzt zur Log-in Seite weitergeleitet, wenn ihre Konto von einem Administrator vom Administrator gelöscht werden. Zuvor gab Adobe Systems Commerce einen Fehler aus. Der Codeblock Plug-in (`SessionPlugin`) befindet sich jetzt innerhalb des Blocks `try…catch` . Zuvor war dieser Code nicht im generischen Block für die Ausnahmebehandlung eingeschlossen.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-661 --> Wenn Sie auf der Seite „Schnellbestellung“ im mobilen Modus **Eingabetaste** nach Eingabe eines gültigen Produktnamens oder einer gültigen SKU drücken, gelangen Sie der Einkäufer erwartungsgemäß zum nächsten Feld.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-607 -->Firmenname ist jetzt wie erwartet in den Abschnitten Abrechnungs- und Versandadresse des Checkout-Workflows sichtbar.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-375 -->Store-Guthaben ist jetzt nicht verfügbar, wenn die **[!UICONTROL Zero Subtotal Checkout]** Zahlungsmethode deaktiviert ist. Zuvor war das Kontrollkästchen „Gutschrift speichern“ während der Auftragserteilung durch den Administrator nicht funktionsfähig. Die Anwendung hat die Bestellung mit dem Speicherguthaben nicht aufgegeben und den folgenden Fehler angezeigt: `The requested Payment Method is not available`.

## B2B v1.3.3

*9. August 2022*

[!BADGE Unterstützt]{type=Informative tooltip="Abgestützt"} Adobe Commerce 2.4.0 und neuere Versionen

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

![Fest Problem](../assets/fix.svg) <!--- MC-42214--> Das _Kategorie_ Seite zeigt nun konsistente Produktdaten an, während Berechtigungen während der partiellen Indizierung generiert werden. Diesem Prozess wurde ein neuer Teilindexer für Ordnerberechtigungen hinzugefügt. Zuvor waren die während der Indexerstellung angezeigten Daten falsch.

![Fest Problem](../assets/fix.svg) <!--- MC-42567--> Das `categoryList` Abfrage gibt jetzt die richtige Anzahl von Produkten zurück, wenn Katalogberechtigungen verwendet und Produkte einem freigegebenen Katalog zugewiesen werden.

![Fest Problem](../assets/fix.svg) <!--- MC-42528--> Das `categoryList` Abfrage respektiert nun Kategorie Berechtigungen und gibt nur erlaubte Kategorien zurück. Zuvor wurden alle zugewiesenen und nicht zugewiesenen Kategorien zurückgegeben.

![Problem behoben](../assets/fix.svg) <!--- MC-42399--> Die `rest/V1/company/{id}`-Anfrage gibt jetzt erwartungsgemäß `is_purchase_order_enabled` Attributwerte zurück.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-128--> Benutzerdefinierte Kundenattribute werden nun wie erwartet auf der Registerkarte _Unternehmensadministrator“_.

![Fest Problem](../assets/fix.svg) <!--- ACP2E-130--> Der Liste-Block &quot;Mein Wunsch&quot; auf der Mein Konto Seite wird nun wie erwartet für Unternehmensadministratoren und Unternehmensbenutzer angezeigt.

![Fest Problem](../assets/fix.svg) <!--- ACP2E-133--> Fehler der Schnellbestellung werden nicht mehr im Warenkorb angezeigt. Bisher zeigte Adobe Systems Commerce diesen Fehler im Warenkorb an, wenn die Produktnummer nicht im Katalog gefunden wurde:  `The SKU was not found in the catalog`.

![Fest Problem](../assets/fix.svg) <!--- ACP2E-194--> Speichervorgänge für freigegebene Kataloge wurden optimiert, um schneller ausgeführt zu werden. Zuvor konnte das Speichern eines freigegebenen Katalogs mit vielen Kundengruppen mehrere Minuten dauern.

![Problem behoben](../assets/fix.svg) <!--- MC-42240--> Adobe Commerce löscht jetzt alle Unterkategorieberechtigungen aus der `sharedcatalog_category_permissions`, wenn die übergeordnete Kategorie gelöscht wird. Zuvor wurden nur die Daten der übergeordneten Kategorie entfernt.

## B2B v1.3.2

*29. August 2022*

[!BADGE Unterstützt]{type=Informative tooltip="Abgestützt"} Adobe Commerce 2.4.0 und neuere Versionen

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.3 wurde hinzugefügt.

![Problem behoben](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce sendet jetzt erfolgreich Aktualisierungs-E-Mails zu abgelaufenen verhandelbaren Angeboten. Zuvor hat Adobe Commerce bei Ablauf eines verhandelbaren Angebots keine Aktualisierungs-E-Mails gesendet.

![Problem behoben](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce sendet jetzt erfolgreich Aktualisierungs-E-Mails, die demnächst ablaufen, und abgelaufene verhandelbare Anführungszeichen, wenn ein `cron` fehlt.

### Firma

![Problem behoben](../assets/fix.svg) <!--- MC-41542--> Im Dropdown-Feld Neue Firmenkonto-Seite erstellen werden keine leeren Optionswerte mehr aufgelistet. Zuvor waren die ersten beiden Optionswerte und der Ländercode `AN` leer.

![Problem behoben](../assets/fix.svg) <!--- MC-41260--> Wenn Sie auf die Schaltfläche **[!UICONTROL Return]** für eine Bestellung klicken, die von einem Unternehmensbenutzer erstellt wurde, wird ein Benutzer mit Administratorrechten wie erwartet zur Seite „Rücksendung erstellen“ weitergeleitet. Zuvor wurde der Administrator zur Seite Auftragsverlauf weitergeleitet.

![Problem behoben](../assets/fix.svg) <!--- MC-40798--> Adobe Commerce schlägt beim Ausführen der `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` während der `bin/magento setup:upgrade` nicht mehr mit einem Fehler wegen unzureichendem Arbeitsspeicher fehl. Zuvor hat Adobe Commerce bei der Initialisierung von Berechtigungen nicht die Batch-Größe für die Sammlung verwendet, sondern stattdessen eine Sammlung aller Unternehmensrollen geladen.

![Problem behoben](../assets/fix.svg) Benutzende von <!--- MC-40551--> können jetzt benutzerdefinierte Attributwerte von Kunden bearbeiten und aktualisieren. Zuvor waren diese Attribute nicht ordnungsgemäß an das Benutzerformular zum Erstellen und Bearbeiten gebunden. Ein Unternehmensbenutzer konnte verschiedene Attributwerte eingeben, aber Adobe Commerce hat diese Werte nicht korrekt gespeichert.

![Problem behoben](../assets/fix.svg) <!--- MC-32653--> Der Ressourcenbaum für Berechtigungen für Unternehmensrollen kann jetzt wie erwartet übersetzt werden. Zuvor wurde die Berechtigungsstruktur nicht übersetzt, obwohl gültige Übersetzungsdateien vorhanden waren.

![Problem behoben](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce speichert jetzt benutzerdefinierte Kundenattributwerte für B2B-Benutzer wie erwartet. Zuvor löste das Erstellen eines Unternehmenskontos, das benutzerdefinierte Kundenattribute enthielt, einen Vorlagenfehler aus, und Adobe Commerce konnte das Formular nicht erfolgreich laden. Durch Hinzufügen eines Arguments zum Layout von `company_create_account` wurde dieses Problem behoben.

![Fest Problem](../assets/fix.svg) <!--- MC-41721--> Unternehmens benutzerdefinierte Filter z. B. Alle anzeigen Benutzer, Anzeigen Aktiv Benutzer und Anzeigen inaktive Benutzer, funktionieren jetzt wie erwartet. Zuvor wurde beim Filtern von Aktionen auf der Firma User Seite ein JavaScript-Fehler ausgegeben.

### Firmenkredit

![Fest Problem](../assets/fix.svg) <!--- MC-41551--> Administratoren mit eingeschränkten Konten, die nur Berechtigungen auf Website-Ebene enthalten, können jetzt eine Firma erstellen, die eine andere Währung als die Website verwendet.

![Fest Problem](../assets/fix.svg) <!--- MC-41523--> Adobe Systems Commerce sendet jetzt Firma-E-Mails von der richtigen `from` E-Mail-Adresse und Umfang. Bisher hat Adobe Systems Commerce beim Versenden Firma Gutschriftszuweisungs- oder Aktualisierungs-E-Mails Website-Umfang nicht berücksichtigt.

### Schnellbestellung

![Fest Problem](../assets/fix.svg) <!--- MC-42104--> Das Erstellen einer bestellen mit der Schnellbestellung aus einer CSV Datei funktioniert jetzt wie erwartet mit nicht vorhandenen SKUs.

![Fest Problem](../assets/fix.svg) <!--- MC-40268--> Die Verwendung der Schnellbestellung zum suchen für mehrere SKUs funktioniert jetzt wie erwartet. Bisher wurden Duplikat Einträge zu den Ergebnissen geführt.

![Fest Problem](../assets/fix.svg) <!--- MC-40261--> In der Anzeige &quot;Hinzugefügtes Produkt&quot; Liste werden jetzt in Klein- und Großbuchstaben eingegebene SKUs gleich behandelt, wenn Sie SKUs verwenden, um mehrere Produkte während der Schnellbestellung auszuwählen.

![Fest Problem](../assets/fix.svg) <!--- MC-40225--> Bei Verwendung der Schnellbestellung werden jetzt Produkte in der Anzahl hinzugefügt, die von der Erstkäufer angegeben wird. Zuvor hat Adobe Commerce nur ein Produkt hinzugefügt, selbst wenn die vom Käufer angegebene Menge ein Produkt überschreitet.

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

![Problem behoben](../assets/fix.svg) <!--- MC-41123--> Die Schaltfläche **[!UICONTROL Add to Requisition List]** wird jetzt für die vorrätigen Produkte eines Warenkorbs angezeigt, wenn der Warenkorb auch nicht vorrätige Produkte enthält. Wenn ein Warenkorb zuvor zwei Produkte enthielt, von denen eines nicht vorrätig war, wurde bei keinem der Produkte die Schaltfläche _[!UICONTROL Add to Requisition List]_&#x200B;angezeigt.

![Problem behoben](../assets/fix.svg) <!--- MC-40877--> Sie können jetzt die REST-API verwenden, um ein Produkt zu einer Anforderungsliste hinzuzufügen.

![Fest Problem Die](../assets/fix.svg) <!--- MC-40155--> Werte der Anforderungs Liste **[!UICONTROL Latest Activity Date]** entsprechen jetzt dem Sprachenformat.

![Fest Problem](../assets/fix.svg) <!--- MC-39580--> Adobe Systems Commerce löst keinen schwerwiegenden Fehler mehr aus, wenn Sie ein Paket Produkt aus einer Anforderungs-Liste bearbeiten.

![Fest Ausgabe](../assets/fix.svg) <!--- MC-40454--> Adobe Systems Commerce zeigt jetzt den korrekten Produktpreis an, wenn Sie ein Produkt mit einer anpassbaren Option `(File)` zu einem Wunsch hinzufügen Liste aus einer Anforderungs Liste. Die verknüpfen zur hochgeladenen Datei sind wie erwartet ebenfalls sichtbar. Bisher wurden in Adobe Systems Commerce falsche Produktpreise angezeigt und die verknüpfen zur Datei nicht angezeigt.

![Fest Problem](../assets/fix.svg)<!--- MC-36383-->: Produkte mit einer anpassbaren Option `(File)` können nun aus einer Anforderungs-Liste zu einer Warenkorb hinzugefügt werden.

### Freigegebener Katalog

![Problem behoben](../assets/fix.svg) <!--- MC-40497--> Ein Administrator mit der Rolle , die auf eine bestimmte Website beschränkt ist, kann jetzt einen freigegebenen Katalog erstellen, anzeigen und bearbeiten. Zuvor gab es in Adobe Commerce einen schwerwiegenden Fehler, wenn ein Administrator mit einer eingeschränkten Rolle versuchte, einen freigegebenen Katalog zu erstellen.

![Fest Problem](../assets/fix.svg) <!--- MC-41337--> Ergebnisse von geschichteten Navigation enthalten jetzt eine genaue Zählung von Produkten mit gefilterten Attributen, und Käufer können jetzt mehrere Filter anwenden. Zuvor konnte nur ein Filter angewendet werden, und Adobe Systems Commerce zeigte eine ungenaue Produktanzahl in mehrschichtigen Navigation an.

![Fest Problem](../assets/fix.svg) <!--- MC-40779--> Adobe Systems Commerce zeigt die Produktanzahl nun in mehrschichtigen Navigation Filter in suchen Ergebnissen korrekt an. Bisher verwendete ein Plug-in für die Search Results Seite nicht ElasticSearch, sondern gab eine neue Abfrage für die Datenbank aus.

![Problem behoben](../assets/fix.svg) <!--- MC-39978--> Adobe Commerce löscht keine Stufenpreise mehr, wenn ein Händler alle Produkte aus einem freigegebenen Standardkatalog löscht.

![Problem behoben](../assets/fix.svg) <!--- MC-39802--> Filter werden jetzt nach der aktuellen Kategorie gefiltert und auf allen Seiten korrekt angezeigt, wenn freigegebene Kataloge aktiviert sind. Zuvor wurden Filter nur für die aktuelle Seite falsch berechnet und nicht nach der aktuellen Kategorie gefiltert.

![Problem behoben](../assets/fix.svg) <!--- MC-39522--> Die Abfrage &quot;GraphQL `products`&quot; gibt die Preisspanne und Kategorie eines Produkts für Produkte, die keinem freigegebenen Katalog zugewiesen sind, nicht mehr zurück, wenn der freigegebene Katalog aktiviert ist. Zuvor gab die Abfrage die Aggregationen des Produkts zurück, obwohl das Produkt selbst nicht im `items`-Array zurückgegeben wurde.

## B2B v1.3.1

*9. Februar 2021*

[!BADGE Unterstützt]{type=Informative tooltip="Abgestützt"} Adobe Commerce 2.4.0 und neuere Versionen

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.2 wurde hinzugefügt.

![Neu](../assets/new.svg) Für Bestellungen werden jetzt Online-Zahlungsmethoden unterstützt.

![Es wurde ](../assets/fix.svg), dass beim Hinzufügen eines konfigurierbaren Produkts zum Warenkorb direkt über eine Anforderungsliste, wenn dieses Produkt in einer früheren Bestellung verwendet wurde, kein Systemfehler mehr zurückgegeben wird.

![Fest Problem](../assets/fix.svg) Adobe Systems Commerce zeigt jetzt die Tab &quot;Meine Genehmigung erforderlich&quot; für Bestellungen korrekt an, wenn eine geteilte Datenbankkonfiguration bereitgestellt wird.

![Fest Ausgabe](../assets/fix.svg) Adobe Systems Commerce zeigt jetzt Details zu Paket Produkten und Geschenk-Karte an, wenn Sie Bestellungen Ansicht.

![Fest Problem](../assets/fix.svg) Käufer werden jetzt wie erwartet umgeleitet, nachdem sie beim Surfen in einem Geschäft, in **[!UICONTROL Website Restriction]** dem aktiviert und **[!UICONTROL Restriction Mode]** auf `Private Sales: Login Only`eingestellt ist, in ihre Konto Protokollierung. Zuvor wurden Käufer zum Geschäft Startseite umgeleitet. <!--- MC-38934-->

![Fest Problem](../assets/fix.svg) Der Auftragsverlauf wird jetzt wie erwartet in der Konto eines Firma-Administrators geladen, Dashboard Seite in Bereitstellungen mit einer B2B Firma Hierarchie mit vielen Kunden (größer als 13000). Zuvor wurde bestellen Verlauf langsam oder gar nicht geladen, und Adobe Systems Commerce zeigte den Fehler 503 an. <!--- MC-38830-->

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt nicht mehr mehrere identische Warnmeldungen an, wenn Sie ein nicht konfiguriertes Produkt mit anpassbaren Optionen über eine Kategorieseite zu einer Anforderungsliste hinzufügen. <!--- MC-38342-->

![Problem behoben](../assets/fix.svg) Wenn freigegebene B2B-Kataloge aktiviert sind, werden neue und duplizierte Produkte jetzt wie erwartet auf der Kategorieseite angezeigt. <!--- MC-38307-->

![Problem behoben](../assets/fix.svg) Adobe Commerce behält jetzt die richtige `store_id` bei, die einem Unternehmensadministrator zugeordnet ist, wenn die Kundengruppe für ein Unternehmen aktualisiert wird. Zuvor wurde der `store_id` beim Aktualisieren der Gruppe in den Standardspeicher geändert. <!--- MC-38196-->

![Problem behoben](../assets/fix.svg) Adobe Commerce speichert jetzt ein gruppiertes Produkt in einer Anforderungsliste als Liste einfacher Produkte auf die gleiche Weise, wie es ein gruppiertes Produkt zum Warenkorb hinzufügt. Aufgrund der Art und Weise, wie Adobe Commerce gruppierte Produkte gespeichert hat, wurde der Link für ein gruppiertes Produkt aus der Anforderungsliste bisher immer zu einfachen Produkten und nicht zu dem gruppierten Produkt umgeleitet. <!--- MC-38049-->

![Problem Fest Sie](../assets/fix.svg) können Bestellungen jetzt beim Export von bestellen-Informationen in CSV **[!UICONTROL Company Name]** Format nach Feld filtern. Zuvor protokollierte Adobe Systems Commerce einen Fehler in `var/export/{file-id}`. <!--- MC-37785-->

![Fest Problem](../assets/fix.svg) Adobe Systems Commerce zeigt jetzt wie erwartet das Popup-Fenster für die Erstellen Anforderungsanforderung Liste an, wenn Sie die Erstellen Neu Anforderung Liste Tab in der Storefront auswählen. <!--- MC-37915-->

![Fest Problem](../assets/fix.svg) Anforderungslisten enthalten jetzt alle gruppierten Produkte und Mengen, die der Liste hinzugefügt wurden. Wenn ein Händler zuvor zu einer Bestellanforderung navigierte Liste, nachdem er Produkte aus einer Produktdetail-Seite hinzugefügt hatte, zeigte Adobe Systems Commerce diesen Fehler an: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![Fest Problem](../assets/fix.svg) Die richtige Geschäft Ansicht wird jetzt mit der entsprechenden Website verknüpft, wenn Sie eine Firma in einer Implementierung mit mehreren Websites erstellen. Zuvor war es nicht möglich, eine Firma zu erstellen, und Adobe Systems Commerce zeigte folgenden Fehler an: `The store view is not in the associated website`. <!--- MC-37488-->

![Fest Problem](../assets/fix.svg) Die Bestellung von Produkten per Produktnummer per Schnellbestellung führt nicht mehr dazu, dass die Produktmengen in der CSV Datei Duplikat werden. <!--- MC-37427-->

![Fest Problem](../assets/fix.svg) Der **[!UICONTROL Add to Cart]** Button wird nicht mehr blockiert, wenn der _[!UICONTROL Enter Multiple SKUs]_&#x200B;Abschnitt der Schnellbestellung Seite einen leeren Wert enthält. Stattdessen zeigt Adobe Systems Commerce jetzt eine Meldung an, in der Sie zur Eingabe gültiger SKUs aufgefordert werden. <!--- MC-37387-->

![Fest Problem](../assets/fix.svg) Adobe Systems Commerce zeigt jetzt diese Meldung auf der Produktseite an, wenn Sie eine Produktbewertung über eine Anforderung abgeben Liste: `You submitted your review for moderation`. Die Bewertung wird auch auf der Ausstehend Bewertungen Seite (Admin **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**) angezeigt. Obwohl Adobe Systems Commerce die Überprüfung zu den Liste der ausstehenden Überprüfungen hinzugefügt hatte, wurde zuvor ein 404-Fehler auf der Produktseite angezeigt. <!--- MC-37119-->

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

- Rabatte für eine bestimmte Zahlungsmethode bleiben während des Checkouts für eine Bestellung bestehen, auch wenn der Käufer seine Zahlungsmethode während des endgültigen Checkouts ändert. Kunden können somit einen Rabatt erhalten, zu dem sie keinen Anspruch haben. Dieses Problem tritt auf, weil für die ursprüngliche Zahlungsmethode trotz der Änderung der Zahlungsmethode weiterhin eine Warenkorbregel angewendet wird. **_Problemumgehung_**: Keine. Siehe den bekannten Artikel [Adobe Commerce 2.4.2 B2B: Rabatt bleibt für Online-Bestellungen bestehen, nachdem die Zahlungsmethode geändert wurde](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html?lang=de) _Wissensdatenbank_. <!-- B2B-1012 -->

- Das `deleteRequisitionListOutput` Abfrage gibt anstelle der verbleibenden Anforderungslisten Details zum gelöschten Anforderungs Liste zurück. <!--- MC-39894-->

## B2B v1.3.0

*15. Oktober 2020*

[!BADGE Unterstützt]{type=Informative tooltip="Abgestützt"} Adobe Systems Commerce 2.4.0 und neuere Versionen

Diese Version enthält Verbesserungen in Bezug auf bestellen Genehmigungen, Versandmethoden, Warenkorb und Protokollierung von Administratoraktionen.

![](../assets/new.svg) Neu Unterstützung für Adobe Systems Commerce 2.4.1 wurde hinzugefügt.

![Neu](../assets/new.svg) Die B2B-Bestellgenehmigungen wurden verbessert, um die Benutzerfreundlichkeit zu verbessern und Massenaktionen auf Bestellungen zu ermöglichen.

![Neu](../assets/new.svg) B2B-Händler können jetzt Versandmethoden steuern, die jeder Firma angeboten werden.<!--- BUNDLE-160 161 162 -->

![](../assets/new.svg) Neu Händler können es den Nutzern nun ermöglichen, den Inhalt ihrer Warenkorb in einer einzigen Aktion zu löschen, und diese Möglichkeit unabhängig auf jeder Website konfigurieren<!--- BUNDLE-108 -->

![](../assets/new.svg) Neu B2B Einkäufer können nun Kontakt Artikel oder den gesamten Inhalt ihrer Warenkorb direkt zu einer Bestellanforderung Liste hinzufügen.<!--- BUNDLE-145 144-->

![](../assets/new.svg) Neu B2B Händler können Bestellungen aus dem Admin im Namen von Kunden erstellen, die die Zahlungsmethode Zahlung auf Rechnung verwenden.<!--- BUNDLE-166 178-->

![](../assets/new.svg) Neu Händler können nun alle Angebote, die mit einer User verbunden sind, direkt aus der Detail-Seite des Kunden Ansicht.<!--- BUNDLE-139 -->

![](../assets/new.svg) Neu Händler können das &quot;Kunden jetzt online&quot;-Raster nun nach Unternehmen filtern.<!--- BUNDLE-137 -->

![](../assets/new.svg) Neu Administratoren können Kunden nun im Admin nach Vertriebsmitarbeitern filtern.<!--- BUNDLE-110 -->

![](../assets/new.svg) Neu Um die Erstellung von betrügerischen oder Spam-Konten zu reduzieren, können Händler Google reCAPTCHA jetzt im Neu Unternehmensanforderungsformular in der Storefront aktivieren.<!--- BUNDLE-154 -->

![](../assets/new.svg) Neu Admin-Aktionen, die in den Unternehmensmodulen durchgeführt wurden, werden jetzt im Admin-Aktionen-Protokoll protokolliert. Aktionen werden von allen relevanten Firma Modulen protokolliert: `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`.  <!--- BUNDLE-180 181 182 183 -->

![Fest Problem](../assets/fix.svg) Adobe Systems Commerce zeigt die **[!UICONTROL Delete customer]** Button nicht mehr auf der Seite &quot; **Kunden** &quot; an, wenn der angemeldete Administrator nicht über die Rechte zum Löschen von Kunden in Bereitstellungen verfügt, in denen B2B installiert ist. <!--- MC-35655-->

![Fest Problem](../assets/fix.svg) Debitoren Gruppe wird nicht mehr automatisch für einen Debitor geändert, der einem Unternehmen zugewiesen ist, wenn Sie den Debitor im Debitorenraster bearbeiten. <!--- MC-35254-->

![Fest Problem](../assets/fix.svg) Wenn ein Händler einen freigegebenen Katalog erstellt, werden Berechtigungen jetzt automatisch auf `Allow` die **[!UICONTROL Display Product Prices]** und **[!UICONTROL Add to Cart]** Funktionen in Kategorien festgelegt, wenn dem Kunden Gruppe dieser Zugriff in den Katalogeinstellungen Berechtigung zugewiesen wird. Zuvor wurden diese Einstellungen automatisch auf `Deny` Linear gesetzt, wenn Katalogberechtigungen auf `Allow`festgelegt wurden.<!--- MC-34792-->

![Problem behoben](../assets/fix.svg) Berechtigungen für freigegebene Katalogkategorien werden nicht mehr überschrieben, wenn ein Produkt auf der Seite „Produktbearbeitung“ bearbeitet wird.<!--- MC-34777-->

![Fest Problem](../assets/fix.svg) Adobe Systems Commerce sendet jetzt eine E-Mail, Benachrichtigung bestätigt wird, dass ein Kunde das festgelegte Kreditlimit überschreiten Berechtigung, wenn ein Händler die **[!UICONTROL Allow To Exceed Credit Limit]** Einstellung aktiviert. Zuvor wurde in der Benachrichtigung E-Mail von Adobe Systems Commerce angegeben, dass der Kunde keine Berechtigung hatte, das Limit zu überschreiten. <!--- MC-34584-->

![Problem Fest Der](../assets/fix.svg) HTML Container, der den Produktpreis in Anforderungslisten umgibt, wird jetzt für die untergeordneten Elemente von gebündelten Produkten korrekt dargestellt. <!--- MC-36331-->

![Fest Problem](../assets/fix.svg) Händler können jetzt die Sprache festlegen, in der Firma User E-Mail gesendet wird, wenn sie eine Firma in mehrsprachigen Bereitstellungen erstellen. Bisher wurde das Dropdown-Menü, in dem Händler die entsprechende Geschäft Ansicht und Sprache auswählen konnten, nicht angezeigt.  <!--- MC-35777-->

![Problem behoben](../assets/fix.svg) Benutzerdefinierte Kundenadressenattribut-Felder werden jetzt wie erwartet im Checkout-Workflow der Storefront angezeigt. <!--- MC-35607-->

![Problem behoben](../assets/fix.svg) Die Registerkarte Konfiguration von B2B-Funktionen wird jetzt korrekt geöffnet. <!--- MC-35458-->Gäste können jetzt QuickOrder verwenden, um Produkte zu ihrem Warenkorb hinzuzufügen und dann erfolgreich Artikel zu entfernen. Wenn ein Käufer QuickOrder verwendet hat, um mehrere Produkte zum Warenkorb hinzuzufügen, und dann ein Produkt entfernt hat, wurde das Produkt nicht entfernt. <!--- MC-35327-->

![Problem behoben](../assets/fix.svg) Ein Unternehmen kann jetzt mit der REST-API PUT `/V1/company/:companyId`-Anfrage aktualisiert werden, ohne die `region_id` anzugeben, wenn der Status als &quot;**erforderlich“ konfiguriert**. Zuvor gab Adobe Commerce einen Fehler aus, wenn er nicht angegeben wurde, obwohl `region_id` nicht erforderlich war. <!--- MC-35304-->

![Problem behoben](../assets/fix.svg) Wenn Sie ein B2B-Unternehmen mithilfe der REST-API erstellen oder aktualisieren (`http://magento.local/rest/V1/company/2`, wobei `2` die Unternehmens-ID darstellt), enthält die Antwort jetzt die erwarteten Einstellungen für `applicable_payment_method` oder `available_payment_methods`. <!--- MC-35248-->

![Fest Problem](../assets/fix.svg) Adobe Systems Commerce zeigt keine 404-Seite mehr an, wenn ein Händler die **Eingabe** Button verwendet, anstatt auf die **[!UICONTROL Save]** Button zu klicken, wenn eine Anforderungsanforderung Liste in der Storefront erstellt wird.<!--- MC-35094-->

![Fest Problem](../assets/fix.svg) Kategorie ändern sich die Berechtigungen nicht mehr, wenn ein neues Produkt einem öffentlich freigegebenen Katalog zugewiesen wird. Zuvor wurden Kategorie-Berechtigungen dupliziert. <!--- MC-34386-->

![Fest Problem](../assets/fix.svg) Beim REST-API-Endpunkt PUT `rest/default/V1/company/{id}`, der zur Aktualisierung von Unternehmens-E-Mails verwendet wird, wird nicht mehr zwischen Groß- und Kleinschreibung unterschieden. <!--- MC-34308-->

![Fest Problem](../assets/fix.svg) Das Deaktivieren von Prämienmodulen wirkt sich nicht mehr auf B2B Funktionen von Kundenkonten aus. Wenn Prämienmodule zuvor deaktiviert waren, wurden die folgenden B2B-bezogenen Registerkarten nicht angezeigt: Unternehmensprofil, Unternehmensbenutzer sowie Rollen und Berechtigungen.<!--- MC-34191-->

![Fest Problem](../assets/fix.svg) Adobe Systems Commerce jetzt den korrekten Absendernamen für E-Mail-Benachrichtigungen verwendet, wenn Änderungen an Firma Konten vorgenommen werden. Zuvor verwendete Adobe Systems Commerce den allgemeinen Absendernamen, der in der Standard Umfang für alle E-Mails definiert ist. <!--- MC-33917-->

![Fest Problem](../assets/fix.svg) Sie können jetzt erfolgreich Multishipping für Bestellungen implementieren, die sowohl physische als auch virtuelle Produkte enthalten. <!--- MC-33818-->

![Fest Problem](../assets/fix.svg) : Händler können jetzt Firma Benutzer aus dem Bereich auf den _[!UICONTROL Company Users]_&#x200B;Seiten &quot;Mein Konto&quot; und &quot;Unternehmensstruktur&quot; erstellen, wenn **[!UICONTROL Access Restriction]**&#x200B;diese Option aktiviert ist und **[!UICONTROL Restriction Mode]**&#x200B;auf `Sales: Login Only`eingestellt ist. Bisher gab Adobe Systems Commerce diesen Fehler aus, wenn ein Händler versuchte, eine User zu erstellen: `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![Fest Problem](../assets/fix.svg) Adobe Systems Commerce setzt die Kunden Gruppe eines Kunden nicht mehr auf die Standardeinstellungen zurück, wenn ein Kunde seine Konto Informationen speichert. <!--- MC-33554-->

![Problem behoben](../assets/fix.svg) Adobe Commerce gibt keinen schwerwiegenden Fehler mehr aus, wenn ein Administrator eine Kundin oder einen Kunden, die bzw. der über einen aktiven Warenkorb verfügt, einer Kundengruppe zuweist. <!--- MC-33313-->

![Problem behoben](../assets/fix.svg) Adobe Commerce bietet jetzt ein `addToCart` Datenschichtereignis für Schnellauftrags- und Anforderungslistenseiten.  <!--- MC-33295-->

![Problem behoben](../assets/fix.svg) Benachrichtigungs-E-Mails, die an einem Unternehmen zugewiesene Vertriebsmitarbeiter gesendet werden, enthalten jetzt das zugewiesene Firmenlogo. Zuvor enthielt die Benachrichtigungs-E-Mail das standardmäßige LUMA-Logo, nicht das hochgeladene Firmenlogo. <!--- MC-33232-->

![Problem behoben](../assets/fix.svg) Eine Anforderungsliste enthält jetzt alle gruppierten Produkte und Mengen, die der Liste hinzugefügt wurden. Wenn ein Händler zu einer Anforderungsliste navigiert ist, nachdem ihm Produkte von einer Produktdetailseite hinzugefügt wurden, hat Adobe Commerce zuvor folgenden Fehler angezeigt: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![Problem behoben](../assets/fix.svg) Die `products`-Abfrage gibt jetzt ein genaues `total_count` zurück, wenn der freigegebene Katalog aktiviert ist. <!--- MC-42268-->

![Problem behoben](../assets/fix.svg) Die Seiten Unternehmenskonfiguration und Firma erstellen funktionieren jetzt wie erwartet, nachdem Sie eine Online-Versandmethode deaktiviert haben. Die Überprüfung wurde hinzugefügt, um die versuchte Verarbeitung deaktivierter Versandmodule zu verhindern. Zuvor hat Adobe Commerce folgenden Fehler angezeigt: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![Problem behoben](../assets/fix.svg) Der Speicherverbrauch für Integrationstests wurde reduziert, was die Testleistung verbessert und die Zeit für den Abschluss des Tests verkürzt. <!--- AC-266-->

## B2B v1.2.0

*28. Juli 2020*

[!BADGE Unterstützt]{type=Informative tooltip="Abgestützt"} Adobe Commerce 2.4.0 und neuere Versionen

![Neu](../assets/new.svg) Unterstützung für Adobe Commerce 2.4.0 wurde hinzugefügt.

![Neu](../assets/new.svg) Storefront Order Search, mit einem zusätzlichen Dank für den Beitrag von Marek Mularczyk von [Divante](https://www.divante.com/) und Community-Mitgliedern.

![Neu](../assets/new.svg) Bestellungen werden verbessert und neu geschrieben. Sie sind jetzt standardmäßig in Adobe Commerce enthalten.

![Neu](../assets/new.svg) Genehmigungsregeln für Bestellungen wurden implementiert. Diese Regeln ermöglichen es Benutzern, den Workflow „Bestellung“ zu steuern, indem sie Einkaufsregeln für Bestellungen erstellen.

![Neu](../assets/new.svg) Die Anmeldung als Kunde ist jetzt standardmäßig in Adobe Commerce enthalten. Mit dieser Funktion können Site-Mitarbeiter Kunden unterstützen, indem sie sich als Kunde anmelden, um zu sehen, was sie sehen.

![Problem behoben](../assets/fix.svg) Attributaggregationen funktionieren jetzt ordnungsgemäß für die mehrschichtige Navigation mit Elasticsearch

![Fest Problem](../assets/fix.svg) Die Suche nach Aufträgen nach Sonderzeichen funktioniert nun fehlerfrei.

![Problem behoben](../assets/fix.svg) Durch Klicken auf die Schaltfläche **[!UICONTROL Clear All]** werden nun alle Filter erweitert und nicht reduziert.

![Problem behoben](../assets/fix.svg) Produkt-SKU/Name ist jetzt in der Zusammenfassung des Suchfilters für den Auftragsverlauf enthalten.

![Problem behoben](../assets/fix.svg) Die Sortieranzeige wird jetzt korrekt im Raster Meine Bestellungen angezeigt.

![Problem behoben](../assets/fix.svg) Jetzt können Sie nur noch einmal auf die Schaltflächen Genehmigen, Abbrechen, Ablehnen und Bestellung klicken. Zuvor konnten Sie auf die Schaltfläche mehrmals klicken.

![Problem behoben](../assets/fix.svg) Die Schaltflächen „Bestellung genehmigen“, „Ablehnen“, „Abbrechen“ und „Validieren“ werden jetzt auf Mobilgeräten korrekt dargestellt.

![Problem behoben](../assets/fix.svg) Bei der vorherigen Genehmigung einer Bestellung mit einem Rabatt, der abgelaufen ist, wurde die Bestellung mit dem vollständigen Betrag platziert und die Bestellsumme nicht aktualisiert. Jetzt wird die Bestellsumme aktualisiert, um die richtige Summe anzuzeigen.

![Problem behoben](../assets/fix.svg) In Version 2.3.4 wurde ein Problem eingeführt, bei dem benutzerdefinierte Erweiterungsattribute nicht von der Kundenadresse zur Angebotsadresse kopiert wurden. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Wenn B2B installiert ist, wird beim Zuweisen von Kategorien zu freigegebenen Katalogen ein SQL-Fehler angezeigt. Dieses Problem wurde behoben.

![Fest Problem](../assets/fix.svg) Aufgrund eines falschen Variable Typ-Werts konnten Administratoren einer bestellen keine konfigurierbaren Produkte hinzufügen. Die Dropdown-Listen für Optionen werden nicht befüllt. Diese Funktion funktioniert jetzt ordnungsgemäß.

![Es wurde ](../assets/fix.svg) Problem behoben: Beim Bearbeiten von Kategorieberechtigungen für die Gruppe Nicht angemeldet trat beim Speichern der Änderungen zuvor ein Fehler auf. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Es wurde eine Korrektur hinzugefügt, mit der Store-Administratoren Produkte zu einer Bestellung hinzufügen können, die nicht im freigegebenen Katalog enthalten sind. Zuvor wurde eine Fehlermeldung angezeigt, wenn ein Element hinzugefügt wurde, das sich nicht im Katalog befindet.

![Es wurde ](../assets/fix.svg) Problem behoben. Nachdem der `php bin/magento indexer:set-dimensions-mode catalog_product_price website` ausgeführt und dann versucht wurde, einen freigegebenen Katalog zu erstellen, trat zuvor ein Fehler auf. Dieses Problem wurde behoben.

![Fest Problem](../assets/fix.svg) Beim Hinzufügen einer Firma und dem Zuweisen des Firma Administrators zu einer nicht standardmäßigen Website wurde die falsche Site-ID gesendet, was zu einem Fehler führte. Dieses Problem wurde behoben.

![Fest Problem](../assets/fix.svg) Bisher schlug das Hinzufügen eines Produkts zu einem bestellen mit _der Schnellbestellung_ fehl, nachdem ein Kunde zu einem anderen Kunden Gruppe verschoben wurde. Dieses Problem wurde behoben.

![Es wurde ](../assets/fix.svg) Problem behoben, dass beim Versuch, die Web-API mit einem B2B-Zitat zu verwenden, zuvor ein falscher Wert an die API gesendet wurde, was zu einem Fehler führte. Dieses Problem wurde behoben.

![Problem behoben](../assets/fix.svg) Zuvor trat ein Fehler auf, wenn ein Unternehmen über die API auf „Aktiv“ gesetzt wurde. Dieses Problem wurde nun behoben.

![Fest Problem](../assets/fix.svg) Aufgrund einer nicht benötigten `form` Tag Seite der bestellen automatisch aktualisiert, wenn Sie die Eingabetaste gedrückt haben, nachdem Sie eine vorgeschlagene Versandgebühr geändert haben. Dieses Problem wurde behoben.

![Problem Fest Zuvor](../assets/fix.svg) wurde ein Fehler angezeigt, wenn ein Produktanzeigelimit für eine Katalog-Seite festgelegt wurde und dieses Limit kleiner als die Anzahl der Gesamtprodukte war. Diese Funktion funktioniert jetzt wie erwartet.

![Fest Problem](../assets/fix.svg) Bisher wurde beim Ändern des Administrators einer Firma die ursprüngliche Administratoradresse an den neuen Administrator kopiert, sodass dieser zwei Adressen erhält. Jetzt wird nur noch die richtige Adresse hinzugefügt.

![Fest Problem](../assets/fix.svg) Bisher schlug die Verwendung der API zum Speichern eines Angebotselements fehl, wenn git auf &quot;Zugelassen und Kunde benachrichtigen&quot; festgelegt war. Dieser API-Aufruf funktioniert jetzt wie erwartet.

![Fest Problem](../assets/fix.svg) Die Fest Produktsteuer wird jetzt auf der Seite &quot;Angebote&quot; angezeigt.

![Fest Problem](../assets/fix.svg) Bisher konnte die Datei nicht herunterladen , wenn Sie in der Tab &quot;Kommentare&quot; der Seite &quot;Meine Zitate&quot; auf einen Anhang klickten. Dieses Verhalten funktioniert jetzt wie erwartet.

### Bekannte Probleme

- Adobe Systems Commerce löst während des Upgrades auf B2B 1.2.0 in einer Implementierung mit mehreren Websites eine Ausnahme aus. Bei `setup:upgrade` der Ausführung tritt dieser Fehler auf der `PurchaseOrder` Modul auf: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **Problemumgehung**: Installieren die `B2B-716 Add NonTransactionableInterface` Schnittstelle zu den `InitPurchaseOrderSalesSequence` Daten Patch Hotfix, der jetzt im **Abschnitt Mein Konto** > **Downloads** von verfügbar `magento.com`ist.
- Wenn ein Rabattcode abläuft, bevor eine Bestellung genehmigt wurde, zeigt die Bestellung weiterhin den rabattierten Betrag an, aber sobald die Bestellung genehmigt wurde, wird die bestellen auf die nicht rabattierte Gesamtsumme gesetzt. **Problemumgehung**: Installieren den `B2B-709 Purchase Order Discount patch` Hotfix für dieses Problem ein, der jetzt im **Abschnitt Mein Konto** > **Downloads** von verfügbar `magento.com`ist.
- Wenn Artikel in einem Einkaufs bestellen nicht vorrätig sind oder nicht genügend Anzahl, wenn der Einkaufs bestellen in einen tatsächlichen bestellen umgewandelt wird, tritt ein Fehler auf. Wenn Lieferrückstände aktiviert sind, wird die bestellen normal verarbeitet.
