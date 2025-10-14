---
title: Optionen für Kundennamen und Adressen
description: Die Optionen Kundenname und Adresse bestimmen, welche Felder in den Namen- und Adressformularen enthalten sind.
exl-id: 28949cfc-2c96-4d0a-a35b-b37b3aa2d1e9
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# Optionen für Kundennamen und Adressen

Die _Name- und Adressoptionen_ bestimmen, welche Felder in den Namen- und Adressformularen enthalten sind, wenn Kundinnen und Kunden ein ([) &#x200B;](../customers/account-create.md) Ihrem Geschäft erstellen.

![Anmeldeformular für Kundenkonto](assets/storefront-customer-account-address-book.png){width="500" zoomable="yes"}

Die Schritte zum Konfigurieren der Optionen Name und Adresse sind für Adobe Commerce und Magento Open Source unterschiedlich.

## Konfigurieren von Name- und Adressoptionen für Adobe Commerce

Sie können die Namen- und Adressoptionen konfigurieren, die Kunden in der Storefront angezeigt werden, wenn sie ihr Konto erstellen.

### Schritt 1: Festlegen des Umfangs der Konfiguration

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Customer Configuration]**.

1. Erweitern Sie den Abschnitt **[!UICONTROL Name and Address Options]** .

   >[!INFO]
   >
   >Beachten Sie, dass der Umfang der Optionen Name und Adresse auf `website` Ebene gilt.

1. Scrollen Sie nach oben auf der Seite und legen Sie für den Bereich der Konfiguration einen der folgenden Werte fest:

   - `Default Config`
   - `Main Website` (oder bestimmter Standort für Installationen an mehreren Standorten)

   >[!INFO]
   >
   >Der Abschnitt _[!UICONTROL Name and Address Options]_&#x200B;wird nicht angezeigt, wenn der Bereich auf `Default Store View` festgelegt ist.

   ![Konfigurationsbereich](assets/customer-configuration-scope-ee.png){width="700" zoomable="yes"}

### Schritt 2: Konfigurieren der Optionen für Name und Adresse

1. Kehren Sie zum Abschnitt [!UICONTROL _Name und Adressoptionen_] der Seite Kundenkonfiguration zurück.

   >[!INFO]
   >
   > Wenn Sie die Einstellung für den `Default config` nicht verwenden, müssen Sie das Kontrollkästchen `Use Default` für jedes Feld deaktivieren, bevor Sie den Wert ändern.

   ![Optionen für Name und Adresse](../configuration-reference/customers/assets/customer-configuration-name-address-options-ee.png){width="600" zoomable="yes"}

1. Geben Sie **[!UICONTROL Prefix Dropdown Options]** jedes Präfix ein, das in der Liste angezeigt werden soll (durch ein Semikolon getrennt).

   >[!IMPORTANT]
   >
   >Setzen Sie ein Semikolon vor den ersten Wert, um einen leeren Wert oben in der Liste anzuzeigen.

1. Geben Sie **[!UICONTROL Suffix Dropdown Options]** jedes Suffix ein, das durch ein Semikolon getrennt in der Liste angezeigt werden soll.

1. Um die folgenden Felder in Kundenformulare einzuschließen, setzen Sie den Wert von „each“ auf `Optional` oder &quot;`Required`&quot;, sofern erforderlich.

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### Schritt 3: Speichern und aktualisieren

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

1. Klicken Sie in der Meldung oben auf der Seite auf **[!UICONTROL Cache Management]** und [aktualisieren](../systems/cache-management.md) auf jeden ungültigen Cache.

## Konfigurieren von Name- und Adressoptionen für die Magento Open Source

Konfigurieren Sie die Namen- und Adressoptionen, die Kundinnen und Kunden in der Storefront angezeigt werden, wenn sie ihr Konto erstellen.

![Anmeldeformular für Kundenkonto](assets/storefront-customer-account-signup.png){width="500" zoomable="yes"}

### Schritt 1: Festlegen des Umfangs der Konfiguration

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Customer Configuration]**.

1. Erweitern Sie den Abschnitt **[!UICONTROL Name and Address Options]** .

   >[!IMPORTANT]
   >
   > Beachten Sie, dass der Umfang der Optionen Name und Adresse auf `website` Ebene gilt.

   ![Optionen für Name und Adresse](../configuration-reference/customers/assets/customer-configuration-name-address-options-ce.png){width="600" zoomable="yes"}

1. Scrollen Sie zurück nach oben auf der Seite und legen Sie für den Bereich der Konfiguration einen der folgenden Werte fest:

   - `Default Config`
   - `Main Website` (oder bestimmter Standort für Installationen an mehreren Standorten)

   >[!NOTE]
   >
   >Der Abschnitt _Name und Adressoptionen_ wird nicht angezeigt, wenn der Umfang auf `Default Store View` festgelegt ist.

   ![Konfigurationsbereich](assets/configuration-scope.png){width="600" zoomable="yes"}

### Schritt 2: Konfigurieren der Optionen für Name und Adresse

1. Kehren Sie zum Abschnitt [!UICONTROL _Name und Adressoptionen_] der Seite Kundenkonfiguration zurück.

   >[!INFO]
   >
   >Wenn Sie die Einstellung für den `Default config` nicht verwenden, müssen Sie das Kontrollkästchen `Use Default` für jedes Feld deaktivieren, bevor Sie den Wert ändern.

1. Geben **für „Anzahl der Zeilen in einer**&quot; eine Zahl zwischen 1 und 4 ein.

   >[!WARNING]
   >
   >Standardmäßig umfasst die Straßenadresse drei Zeilen.

1. Um ein Präfix (z. B. Herr oder Frau) als Teil des Namens einzufügen, setzen Sie **Präfix anzeigen** auf `Yes`.

   ![Präfix im Formular für die Kundenanmeldung](assets/storefront-customer-account-prefix.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >Unter **Dropdown-Optionen für Präfixe** geben Sie jedes Präfix ein, das in der Liste angezeigt werden soll, getrennt durch ein Semikolon. Sie können ein Semikolon vor dem ersten Wert platzieren, um einen leeren Wert oben in der Liste anzuzeigen.

1. Um ein optionales Feld für den zweiten oder ersten Vornamen des Kunden einzuschließen, setzen Sie **[!UICONTROL Show Middle Name (initial)]** auf `Yes`.

1. Um ein Suffix einzuschließen (z. B. Jr. oder Sr.) nach dem Kundennamen setzen Sie **[!UICONTROL Show Suffix]** auf eine der folgenden Einstellungen:

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >Unter **Dropdown-Optionen für Suffixe** geben Sie jedes Suffix ein, das in der Liste angezeigt werden soll, getrennt durch ein Semikolon. Sie können ein Semikolon vor dem ersten Wert platzieren, um einen leeren Wert oben in der Liste anzuzeigen.

1. Um das Geburtsdatum einzuschließen, setzen Sie **[!UICONTROL Show Date of Birth]** auf einen der folgenden Werte:

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >Gemäß den aktuellen Best Practices für Sicherheit und Datenschutz sollten Sie sich über potenzielle rechtliche und Sicherheitsrisiken im Zusammenhang mit der Speicherung des vollständigen Geburtsdatums der Kunden (Monat, Tag, Jahr) mit anderen persönlichen Kennungen im Klaren sein. Es wird empfohlen, die Speicherung der vollständigen Geburtsdaten von Kundinnen und Kunden zu begrenzen und alternativ ein Kundenjahr zu verwenden.

   Kunden können das Kalendersymbol nach dem Feld verwenden, um das Geburtsdatum aus einem Popup-Kalender auszuwählen.

   ![Geburtsdatum im Formular für die Kundenanmeldung](assets/storefront-customer-account-date-of-birth.png){width="600" zoomable="yes"}

1. Um Kunden die Eingabe ihrer Steuer- oder [MwSt](../stores-purchase/vat.md)-Nummer zu ermöglichen, setzen Sie **[!UICONTROL Show Tax/VAT Number]** auf einen der folgenden Werte:

   - `Optional`
   - `Required`

1. Um ein Feld für das Geschlecht in das Kundenformular aufzunehmen, legen Sie **[!UICONTROL Show Gender]** auf eine der folgenden Einstellungen fest:

   - `Optional`
   - `Required`

   ![Geschlechteroptionen im Formular für die Kundenanmeldung](assets/storefront-customer-account-gender.png){width="600" zoomable="yes"}

1. Um die folgenden Felder in Kundenformulare einzuschließen, setzen Sie den Wert von „each“ auf `Optional` oder &quot;`Required`&quot;, sofern erforderlich.

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### Schritt 3: Speichern und aktualisieren

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

1. Klicken Sie in der Meldung oben auf der Seite auf **[!UICONTROL Cache Management]** und [aktualisieren](../systems/cache-management.md) auf jeden ungültigen Cache.
