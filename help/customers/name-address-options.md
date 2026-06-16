---
title: Optionen für Kundennamen und Adressen
description: Die Optionen Kundenname und Adresse bestimmen, welche Felder in den Namen- und Adressformularen enthalten sind.
exl-id: 28949cfc-2c96-4d0a-a35b-b37b3aa2d1e9
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/qMXVcVWZJCrCNywOJF3psuO5vLWkNt9LoNtgFfFBzT8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 809
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

## Konfigurieren von Name- und Adressoptionen für Magento Open Source

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

1. So fügen Sie ein Präfix ein (z. B. Herr oder Frau) Legen Sie als Teil des Namens **Präfix anzeigen** auf `Yes` fest.

   ![Präfix im Formular für die Kundenanmeldung](assets/storefront-customer-account-prefix.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >Unter **Dropdown-Optionen für Präfixe** geben Sie jedes Präfix ein, das in der Liste angezeigt werden soll, getrennt durch ein Semikolon. Sie können ein Semikolon vor dem ersten Wert platzieren, um einen leeren Wert oben in der Liste anzuzeigen.

1. Um ein optionales Feld für den zweiten oder ersten Vornamen des Kunden einzuschließen, setzen Sie **[!UICONTROL Show Middle Name (initial)]** auf `Yes`.

1. Um ein Suffix einzuschließen (z. B. Jr. oder Sr.) Legen Sie **[!UICONTROL Show Suffix]** nach dem Kundennamen auf einen der folgenden Werte fest:

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
