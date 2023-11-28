---
title: Referenz zu Kundendatenattributen
description: Verwenden Sie diese Referenz zu Kundendatenattributen, wenn Sie mit Importen und Exporten von Kundendaten arbeiten.
exl-id: d22ebfed-f439-4a3f-b39e-e957b65c8c21
feature: Customers, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# Referenz zu Kundendatenattributen

In den folgenden Tabellen sind die Attribute aus einem typischen Export der Hauptdatei des Kunden und der Kundenadressen aufgeführt. Die zum Export dieser Daten verwendete Installation verfügt über zwei Websites und mehrere Store-Ansichten, wobei die Beispieldaten installiert sind.

Jedes Attribut oder Feld wird in der CSV-Datei als Spalte dargestellt, und Kundendatensätze werden durch Zeilen dargestellt. Spalten, die mit einem Unterstrich beginnen, sind Dienstentitäten, die Eigenschaften oder komplexe Daten enthalten.

## Hauptdatei des Kunden

| Attribut | Beschreibung |
|--- |--- |
| `email` | Die E-Mail-Adresse des Kunden. |
| `_website` |  |
| `_store` |  |
| `confirmation` | Bestätigungsmarkierung. |
| `created_at` | Das Datum der Erstellung des Kundenkontos. |
| `created_in` | Die Store-Ansicht, in der das Konto erstellt wurde. |
| `disable_auto_group_change` | Bestimmt, ob Kundengruppen während der MwSt-ID-Validierung dynamisch zugewiesen werden können. |
| `dob` | Das Geburtsdatum des Kunden. <br><br>**_Wichtig:_**Im Einklang mit den aktuellen Best Practices für Sicherheit und Datenschutz sollten Sie die Speicherung und Verarbeitung des vollständigen Geburtsdatums (Monat, Tag, Jahr) des Kunden überprüfen. Bei der Erfassung mit anderen persönlichen Identifikatoren (wie_vollständiger Name _), ist es ein potenzielles Rechts- und Sicherheitsrisiko. Es wird empfohlen, die Speicherung der vollständigen Geburtsdaten der Kunden zu begrenzen und stattdessen das Geburtsjahr des Kunden als Alternative zu verwenden. |
| `firstname` | Der Vorname des Kunden. |
| `gender` | Das Kundengeschlecht. |
| `group_id` | Die ID der Kundengruppe, der der Kunde zugewiesen ist. |
| `lastname` | Der Nachname des Kunden. |
| `middlename` | Der Vorname oder die mittlere Anfangsphase des Kunden. |
| `password_hash` | Kennwort-Hash |
| `prefix` | Jedes mit dem Kundennamen verwendete Präfix (z. B. `Mr.`, `Ms.`, `Mrs.`, und `Dr.`). |
| `rp_token` | Kennwort-Token zurücksetzen. |
| `rp_token_created_at` | Datum, an dem das Kennwort zurückgesetzt wurde. |
| `store_id` | Store ID |
| `suffix` | Jedes Suffix, das mit dem Kundennamen verwendet wird (z. B. `Jr.`, `Sr.`, und `Esquire`). |
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
| `company` | Der Name des Unternehmens, falls für diese Adresse zutreffend. |
| `country_id` | Die Land-ID, unter der sich die Kundenadresse befindet. |
| `fax` | Die Faxnummer des Kunden, falls zutreffend. |
| `firstname` | Der Vorname des Kunden. |
| `lastname` | Der Nachname des Kunden. |
| `middlename` | Der Vorname oder die mittlere Anfangsphase des Kunden. |
| `postcode` | Die Postleitzahl, unter der sich die Kundenadresse befindet. |
| `prefix` | Jedes mit dem Kundennamen verwendete Präfix (z. B. `Mr.`, `Ms.`, `Mrs.`, und `Dr.`). |
| `region` | Die Region, in der sich die Kundenadresse befindet. |
| `region_id` | Regions-ID |
| `street` | Die Straßenadresse des Kunden. Eine zweite Zeile der Straßenadresse ist verfügbar, sofern in der Konfiguration angegeben. |
| `suffix` | Bei Verwendung des Suffixes, der mit dem Kundennamen verknüpft ist (z. B. `Jr.`, `Sr.`oder `III`). |
| `telephone` | Die mit der Adresse verknüpfte Telefonnummer des Kunden. |
| `vat_id` | Die MwSt-ID ist eine interne Kennung für die MwSt-Nummer des Kunden bei der Verwendung bei der MwSt-Validierung. |
| `vat_is_valid` |  |
| `vat_request_date` |  |
| `vat_request_id` |  |
| `vat_request_success` |  |
| `_address_default_billing_` | Gibt die standardmäßige Rechnungsadresse an. Ein Wert von `1` gibt an, dass die Adresse die standardmäßige Rechnungsadresse des Kunden ist. Werte: 1 / 0 |
| `_address_default_shipping_` | Gibt die standardmäßige Versandadresse an. Ein Wert von `1` gibt an, dass die Adresse die standardmäßige Lieferadresse des Kunden ist. Werte: `1` / `0` |

{style="table-layout:auto"}
