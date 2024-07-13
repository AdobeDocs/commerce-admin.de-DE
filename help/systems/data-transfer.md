---
title: Datenübertragung
description: Erfahren Sie mehr über die Unterstützung für die Datenübertragung, einschließlich der Datenvalidierung.
exl-id: 5057e398-c458-42e9-8ec0-bf116a667a3c
feature: System, Data Import/Export
source-git-commit: b89d6b08d0559dc769a8c51570696f033f23c7f3
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Datenübertragungen

Verwenden Sie die Import- und Export-Tools, um mehrere Datensätze in einem Vorgang zu verwalten. Sie können neue Elemente importieren sowie vorhandene Produktsätze aktualisieren, ersetzen und löschen.

Sie können beispielsweise Ihrem Inventar neue Produkte hinzufügen, Produktdaten und erweiterte Preisdaten aktualisieren und eine Reihe vorhandener Produkte durch neue Produkte ersetzen. Mit den Import- und Exportwerkzeugen können Sie große Produktkataloge effizienter verwalten, da Sie die Daten exportieren, in einer Tabelle bearbeiten und wieder in Ihren Speicher importieren können, anstatt mehrere Vorgänge in der Admin-Konsole auszuführen.


>[!NOTE]
>
>Adobe Commerce unterstützt auch den SAAS-Datenexport, um Produktdaten vom Commerce-Server an SaaS-Dienste zu übertragen. Der SAAS-Datenexport ist in Commerce SaaS-Dienste integriert, einschließlich [Produkt Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/overview.html), [Live Search](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview) und [Katalogdienst](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/guide-overview). Weitere Informationen finden Sie im [SAAS-Datenexport-Handbuch](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

## Datenvalidierung

Alle Daten müssen validiert werden, um die Qualität, Genauigkeit und Integrität der Werte sicherzustellen, bevor sie in den Speicher importiert werden. Die Validierung beginnt, wenn Sie auf **[!UICONTROL Check Data]** klicken. Während des Vorgangs werden alle Entitäten in der Importdatei für Folgendes überprüft:

- **Attribute** - Spaltenkopfzeilennamen werden überprüft, um sicherzustellen, dass sie mit den entsprechenden Attributen in der Systemdatenbank übereinstimmen. Der Wert jedes Attributs wird überprüft, um sicherzustellen, dass die Anforderungen des Datentyps (Dezimalzahl, Ganzzahl, Varchar, Text und Datum/Uhrzeit) erfüllt sind.
- **Komplexe Daten** - Werte, die aus einem definierten Satz stammen, z. B. eine Dropdown-Liste oder ein Mehrfachauswahleingabetyp, werden überprüft, um sicherzustellen, dass die Werte im definierten Satz vorhanden sind.
- **Dienstdaten** - Die Werte in den Dienstdatenspalten werden überprüft, um sicherzustellen, dass die Eigenschaften oder komplexen Datenwerte mit den bereits in der Systemdatenbank definierten übereinstimmen.
- **Erforderliche Werte** - Für neue Entitäten ist das Vorhandensein erforderlicher Attributwerte in der Datei markiert. Für vorhandene Entitäten müssen Sie nicht erneut überprüfen, ob die erforderlichen Attributwerte vorhanden sind.
- **Trennzeichen** - Obwohl die Trennzeichen bei der Anzeige in einem Arbeitsblatt nicht sichtbar sind, werden Datenwerte in einer CSV-Datei durch Kommas getrennt und Textwerte werden in doppelte Anführungszeichen gesetzt. Während des Validierungsprozesses wird die Formatierung für die Trennzeichen und die einzelnen Anführungszeichen, die Zeichenfolgen enthalten, überprüft.

Die Ergebnisse der Validierung werden im Abschnitt Validierungsergebnisse angezeigt und enthalten die folgenden Informationen:

- Die Anzahl der geprüften Entitäten
- Die Anzahl ungültiger Zeilen
- Die Anzahl der gefundenen Fehler

Wenn die Daten gültig sind, wird die Meldung _Erfolg importieren_ angezeigt.

![Systemmeldung - Datei ist gültig](./assets/data-import-validation-message.png){width="500" zoomable="yes"}

Wenn die Validierung fehlschlägt, lesen Sie die Beschreibung der einzelnen Fehler und korrigieren Sie das Problem in der CSV-Datei. Wenn beispielsweise eine Zeile eine ungültige SKU enthält, wird der Importvorgang gestoppt, diese Zeile und alle nachfolgenden Zeilen werden nicht importiert. Importieren Sie die Daten nach der korrekten Problembehebung erneut. Wenn viele Fehler auftreten, kann es mehrere Versuche dauern, die Validierung zu bestehen.

### Datenvalidierungsmeldungen

#### Validierung

- `Product with specified SKU not found in rows: 1`
- `URL key for specified store already exists`
- `'7z' file extension is not supported`
- `TXT file extension is not supported`

#### Fehler

- `Wrong field type. Type in the imported file %decimal%, expected type is %text%.`
- `Value is not allowed. Attribute value does not exist in the system.`
- `Field %column name% is required.Wrong value separator is used.`
- `Wrong encoding used. Supported character encoding is UTF-8 and Windows-1252.`
- `Imported file does not contain SKU field.`
- `SKU does not exist in the system.`
- `Column name %column name% is invalid. Should start with a letter. Alphanumeric.`
- `Imported file does not contain a header.`
- `%website name% website does not exist in the system.`
- `%storeview name% storeview does not exist in the system.`
- `Imported attribute %attribute name% does not exist in the system.`
- `Imported resource (image) could not be downloaded from external resource due to timeout or access permissions.`
- `Imported resource (image) does not exist in the local media storage.`
- `Product creation error displayed to the user equal to the one seen during manual product save.`
- `Advanced Price creation error displayed to the user equal to the one seen during the manual product save.`
- `Customer creation error displayed to the user equal to the one seen during the manual customer save.`
