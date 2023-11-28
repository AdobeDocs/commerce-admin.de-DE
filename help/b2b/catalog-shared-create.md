---
title: Freigegebenen Katalog erstellen
description: Erfahren Sie mehr über das Erstellen freigegebener Kataloge und das Duplizieren vorhandener freigegebener Kataloge.
exl-id: 969c352c-ff88-4902-8347-334ee8b79afb
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Freigegebenen Katalog erstellen

Wenn eine [freigegebener Katalog](catalog-shared.md) erstellt wird, erstellt das System automatisch eine [Kundengruppe](account-company-customer-group.md) durch denselben Namen. Wenn Sie beispielsweise einen freigegebenen Katalog mit dem Namen _ABC-Katalog_, erstellt das System auch eine _ABC-Katalog_ Kundengruppe. Die Zuweisung eines Unternehmens zum freigegebenen benutzerdefinierten Katalog entspricht im Wesentlichen der Zuweisung eines Unternehmens zu einer Kundengruppe.

Ein neuer freigegebener Katalog enthält keine Produkte, benutzerdefinierten Preise oder Unternehmensverbände. Ein öffentlicher Katalog, der standardmäßig als freigegebener Katalog dient, der bei Aktivierung freigegebener Kataloge erstellt wird, wird automatisch Gästen und Kunden zugewiesen, die keiner Firma zugeordnet sind.

![Freigegebene Kataloge](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

Die folgenden Aspekte eines freigegebenen Katalogs müssen eingerichtet werden, bevor er verwendet werden kann:

- Katalogbereich
- Produktauswahl
- Benutzerspezifische Preise
- Unternehmenszuweisungen

## Preissegment

Wenn Sie über eine Multisite-Installation verfügen, konfigurieren Sie den Preisbereich, bevor Sie Ihre freigegebenen Kataloge erstellen. Die [Preissegment](../catalog/catalog-price-scope.md) kann auf `Global` oder `Website`. Sie kann jedoch nur zu Beginn des Einrichtungsprozesses festgelegt werden. Die Website-Auswahl wird in Schritt 2 der [freigegebene Katalogeinrichtung](catalog-shared-pricing-structure.md).

![Website-Auswahl](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **Katalog** und wählen **Katalog** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **Preis** Abschnitt.

1. Satz **Katalogpreisumfang** nach `Website`.

   ![Katalogpreisumfang](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

1. Klicken **[!UICONTROL Save Config]**.

## Schritt 1: Freigegebenen Katalog erstellen

Es gibt zwei Möglichkeiten, einen freigegebenen Katalog zu erstellen. Sie können einen freigegebenen Katalog des Typs erstellen oder einen vorhandenen freigegebenen Katalog duplizieren. Ein neuer freigegebener Katalog enthält keine Produkte und wird noch keinem Unternehmen zugewiesen.

### Methode 1: Hinzufügen eines neuen freigegebenen Katalogs

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Shared Catalog]** und gehen Sie wie folgt vor:

   - Geben Sie einen **[!UICONTROL Name]** für den freigegebenen Katalog.

     Der von Ihnen zugewiesene Name wird im gesamten Admin- und Kunden-Dashboard verwendet, falls zutreffend, um auf den freigegebenen Katalog zu verweisen. Es wird auch zum Namen der entsprechenden Kundengruppe.

   - Auswählen **[!UICONTROL Type]** : `Custom` oder `Public`.

   - Wählen Sie die geeignete **[!UICONTROL Customer Tax Class]** die für Käufe aus dem freigegebenen Katalog gilt.

     Weitere Informationen zur Einrichtung und Definition von Steuerklassen finden Sie unter [Steuerklassen](../stores-purchase/tax-class.md).

     Das folgende Beispiel zeigt einen neuen benutzerdefinierten Katalog für einen bestimmten Großkunden.

     ![Neuer freigegebener Katalog](./assets/shared-catalog-new.png){width="600" zoomable="yes"}

   - Eingabe **[!UICONTROL Description]**

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

   Der neue Katalog wird im _[!UICONTROL Shared Catalogs]_Gitter.

### Methode 2: Duplizieren eines vorhandenen freigegebenen Katalogs

Ein doppelter benutzerdefinierter Katalog behält das Preismodell und die Struktur des Originals bei, nicht jedoch die Unternehmensverbände. Eine entsprechende Kundengruppe wird auch mit demselben Namen wie der duplizierte Katalog erstellt. Standardmäßig wird ein duplizierter Katalog _Duplizieren von_ den Originalkatalog.

Wenn ein öffentlicher freigegebener Katalog dupliziert wird, ändert sich der Typ des doppelten Katalogs in `custom`.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Gehen Sie für den freigegebenen Katalog im Raster, den Sie duplizieren möchten, zum **[!UICONTROL Action]** und wählen Sie **[!UICONTROL General Settings]**.

1. Klicken Sie in den Optionen oben auf der Seite auf **[!UICONTROL Duplicate]**.

   ![Gemeinsamer Katalog duplizieren](./assets/shared-catalog-duplicate.png){width="600" zoomable="yes"}

1. Aktualisieren Sie die folgenden Felder für den neuen Katalog:

   - **[!UICONTROL Name]**
   - **[!UICONTROL Type]**
   - **[!UICONTROL Customer Tax Class]**
   - **[!UICONTROL Description]**

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

   Das Duplikat wird im _[!UICONTROL Shared Catalogs]_raster mit einer eindeutigen ID.

## Schritt 2: Einrichten abschließen

Nachdem Sie einen neuen freigegebenen Katalog erstellt haben, muss er mit der entsprechenden Produktauswahl konfiguriert werden. [Unternehmenszuweisungen](catalog-shared-assign-companies.md), und [Kategorienberechtigungen](../catalog/category-permissions.md). Um fortzufahren, siehe [Festlegen von Preisen und Struktur](catalog-shared-pricing-structure.md).

>[!NOTE]
>
>**[B2B-Version 1.3.0](release-notes.md#b2b-v130) und höher** — Wenn Sie einen freigegebenen Katalog erstellen, wird jede [Kategorienberechtigung](../catalog/category-permissions.md) für den Katalog auf _[!UICONTROL Allow for the Display Product Prices]_und_[!UICONTROL Add to Cart]_ für Kundengruppen, denen dieser Zugriff in den Katalogberechtigungseinstellungen zugewiesen wurde. Zuvor wurden diese Einstellungen automatisch auf `Deny` auch wenn die Katalogberechtigungen auf `Allow`.

## Freigegebene Katalogdemo

Sehen Sie sich dieses Video an, um eine Demonstration der gemeinsamen Katalogverwaltung zu sehen:

>[!VIDEO](https://video.tv.adobe.com/v/344446?quality=12&learn=on)

## Gemeinsame Katalogseitenreferenz

### Schaltflächenleiste

| Schaltfläche | Beschreibung |
|--- |--- |
| [!UICONTROL Back] | Kehrt zur Seite &quot;Freigegebene Kataloge&quot;zurück, ohne den neuen freigegebenen Katalog zu speichern. |
| [!UICONTROL Reset] | Löscht das Formular nicht gespeicherter Änderungen und stellt die ursprünglichen Katalogdetailinformationen wieder her. |
| [!UICONTROL Save and Continue Edit] | Speichert alle Änderungen und behält das Formular im Bearbeitungsmodus bei. |
| [!UICONTROL Save] | Speichert Änderungen, schließt das Formular und kehrt zur Seite Gemeinsame Kataloge zurück. |

{style="table-layout:auto"}

### Katalogdetails

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Name] | Identifiziert den freigegebenen Katalog im gesamten Admin und in den Kundenkonten, in denen er verfügbar ist. Der Katalogname sollte beschreibend sein und nicht länger als 32 Zeichen sein. Sie können nicht zwei freigegebene Kataloge mit demselben Namen haben. Maximale Zeichen: 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Identifiziert einen Katalog mit benutzerdefinierten Preisen, die nur für die spezifischen Unternehmen verfügbar sind, denen er zugewiesen ist.<br/>**[!UICONTROL Public]**- Identifiziert den freigegebenen Katalog, der für alle Gastbesucher und angemeldete Kunden verfügbar ist, die nicht mit einem Unternehmen verbunden sind. Ein standardmäßiger öffentlicher freigegebener Katalog wird erstellt, wenn [!DNL B2B for Adobe Commerce] installiert ist, aber von einem Store-Administrator konfiguriert werden muss. Es kann jeweils nur ein öffentlicher freigegebener Katalog vorhanden sein. |
| [!UICONTROL Customer Tax Class] | Bestimmt die Steuerklasse, die für Käufe verwendet wird, die aus dem Katalog getätigt werden. Die Optionen umfassen alle verfügbaren Steuerklassen. |
| [!UICONTROL Description] | Kurze Erläuterung der Verwendung des Katalogs. |

{style="table-layout:auto"}

### Rasterspalten

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Eine eindeutige numerische Kennung, die einer freigegebenen Katalogentität zugewiesen wird. |
| [!UICONTROL Name] | Der Name des freigegebenen Katalogs. |
| [!UICONTROL Type] | Gibt den Typ des freigegebenen Katalogs an. Kann `Public` oder `Custom`. |
| [!UICONTROL Created At] | Das Datum, an dem der freigegebene Katalog im System erstellt wurde. |
| [!UICONTROL Created By] | Der Name des Admin-Benutzers, der einen freigegebenen Katalog erstellt hat. |
| [!UICONTROL Action] | Die Liste der Aktionen. Optionen: `Set Pricing and Structure`, `Assign Companies`, `General Settings`, `Delete`. |

{style="table-layout:auto"}
