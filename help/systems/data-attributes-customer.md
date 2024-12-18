---
title: Referenz zu Kundendatenattributen
description: Verwenden Sie diese Referenz von Kundendatenattributen bei der Arbeit mit Kundendatenimporten und -exporten.
exl-id: d22ebfed-f439-4a3f-b39e-e957b65c8c21
feature: Customers, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Referenz zu Kundendatenattributen

In den folgenden Tabellen sind die Attribute aus einem typischen Export der Hauptdatei und Kundenadressen des Kunden aufgeführt. Die Installation, die zum Exportieren dieser Daten verwendet wurde, verfügt über zwei Websites und mehrere Store-Ansichten mit installierten Beispieldaten.

Jedes Attribut oder Feld wird in der CSV-Datei als Spalte dargestellt, und Kundendatensätze werden durch Zeilen dargestellt. Spalten, die mit einem Unterstrich beginnen, sind Service-Entitäten, die Eigenschaften oder komplexe Daten enthalten.

## Hauptdatei des Kunden

| Attribut | Beschreibung |
|--- |--- |
| `email` | Die E-Mail-Adresse des Kunden. |
| `_website` |  |
| `_store` |  |
| `confirmation` | Bestätigungs-Flag. |
| `created_at` | Das Datum der Erstellung des Kundenkontos. |
| `created_in` | Die Store-Ansicht, in der das Konto erstellt wurde. |
| `disable_auto_group_change` | Legt fest, ob Kundengruppen bei der Validierung der MwSt.-ID dynamisch zugewiesen werden können. |
| `dob` | Das Geburtsdatum des Kunden. <br><br>**_Wichtig:_**Überprüfen Sie entsprechend den aktuellen Best Practices für Sicherheit und Datenschutz die Speicherung und Verarbeitung des vollständigen Geburtsdatums der Kundinnen und Kunden (Monat, Tag, Jahr). Wenn er mit anderen persönlichen Kennungen (wie_vollständiger Name _) erfasst wird, stellt er ein potenzielles Rechts- und Sicherheitsrisiko dar. Wir empfehlen, die Speicherung der vollständigen Geburtsdaten von Kunden zu begrenzen und stattdessen vorzuschlagen, als Alternative das Kundenjahr zu verwenden. |
| `firstname` | Der Vorname des Kunden. |
| `gender` | Das Geschlecht des Kunden. |
| `group_id` | Die ID der Kundengruppe, der der Kunde zugewiesen ist. |
| `lastname` | Der Nachname des Kunden. |
| `middlename` | Der zweite Vorname oder zweite Vorname des Kunden. |
| `password_hash` | Passwort-Hash |
| `prefix` | Jedes Präfix, das mit dem Kundennamen verwendet wird (z. B. `Mr.`, `Ms.`, `Mrs.` und `Dr.`). |
| `rp_token` | Passwort-Token zurücksetzen. |
| `rp_token_created_at` | Datum, an dem das Kennwort zurückgesetzt wurde. |
| `store_id` | Store-ID |
| `suffix` | Jedes Suffix, das mit dem Kundennamen verwendet wird (z. B. `Jr.`, `Sr.` und `Esquire`). |
| `taxvat` |  |
| `website_id` | Die Website-ID der Site, auf der das Kundenkonto erstellt wurde. |
| `password` | Das Kundenkennwort. |

{style="table-layout:auto"}

## Kundenadressen

| Attribut | Beschreibung |
|--- |--- |
| `_website` |  |
| `_email` |  |
| `_entity_id` |  |
| `city` | Die Stadt, in der sich die Kundenadresse befindet. |
| `company` | Der Firmenname, falls für diese Adresse zutreffend. |
| `country_id` | Die Länder-ID, in denen sich die Kundenadresse befindet. |
| `fax` | Die Faxnummer des Kunden, falls zutreffend. |
| `firstname` | Der Vorname des Kunden. |
| `lastname` | Der Nachname des Kunden. |
| `middlename` | Der zweite Vorname oder zweite Vorname des Kunden. |
| `postcode` | Die Postleitzahl, an der sich die Kundenadresse befindet. |
| `prefix` | Jedes Präfix, das mit dem Kundennamen verwendet wird (z. B. `Mr.`, `Ms.`, `Mrs.` und `Dr.`). |
| `region` | Die Region, in der sich die Kundenadresse befindet. |
| `region_id` | Regions-ID |
| `street` | Die Straße des Kunden. Eine zweite Zeile der Straßenadresse ist verfügbar, wenn in der Konfiguration angegeben. |
| `suffix` | Falls verwendet, das Suffix, das mit dem Namen des Kunden verknüpft ist (z. B. `Jr.`, `Sr.` oder `III`). |
| `telephone` | Die Telefonnummer des Kunden, die mit der Adresse verknüpft ist. |
| `vat_id` | Die MwSt.-ID ist eine interne Kennung für die MwSt.-Nummer des Kunden bei Verwendung in der MwSt.-Validierung. |
| `vat_is_valid` |  |
| `vat_request_date` |  |
| `vat_request_id` |  |
| `vat_request_success` |  |
| `_address_default_billing_` | Gibt die Standard-Rechnungsadresse an. Der Wert `1` gibt an, dass die Adresse die standardmäßige Rechnungsadresse des Kunden ist. Werte: 1 / 0 |
| `_address_default_shipping_` | Gibt die Standard-Versandadresse an. Der Wert `1` gibt an, dass die Adresse die standardmäßige Versandadresse des Kunden ist. Werte: `1` / `0` |

{style="table-layout:auto"}
