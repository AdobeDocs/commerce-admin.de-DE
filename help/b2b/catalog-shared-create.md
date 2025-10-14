---
title: Erstellen eines freigegebenen Katalogs
description: Erfahren Sie mehr über das Erstellen von freigegebenen Katalogen und das Duplizieren vorhandener freigegebener Kataloge.
exl-id: 969c352c-ff88-4902-8347-334ee8b79afb
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# Erstellen eines freigegebenen Katalogs

Wenn ein [freigegebener Katalog](catalog-shared.md) erstellt wird, erstellt das System automatisch eine [Kundengruppe](account-company-customer-group.md) mit demselben Namen. Wenn Sie beispielsweise einen freigegebenen Katalog mit dem Namen _ABC Catalog_ erstellen, erstellt das System auch eine entsprechende Kundengruppe _ABC Catalog_. Das Zuweisen einer Firma zum freigegebenen benutzerdefinierten Katalog entspricht im Wesentlichen dem Zuweisen einer Firma zu einer Kundengruppe.

Ein neuer freigegebener Katalog umfasst keine Produkte, benutzerdefinierten Preise oder Unternehmensverknüpfungen. Ein öffentlicher Katalog (der Standardkatalog, der bei Aktivierung freigegebener Kataloge erstellt wird) wird automatisch Gästen und Kunden zugewiesen, die keinem Unternehmen zugeordnet sind.

![freigegebene Kataloge](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

Die folgenden Aspekte eines freigegebenen Katalogs müssen eingerichtet werden, bevor er verwendet werden kann:

- Katalogbereich
- Produktauswahl
- Benutzerdefinierte Preise
- Unternehmenszuweisungen

## Preisspanne

Wenn Sie eine Multisite-Installation haben, stellen Sie sicher, dass Sie den Preisbereich konfigurieren, bevor Sie Ihre freigegebenen Kataloge erstellen. Der [Preisbereich](../catalog/catalog-price-scope.md) kann auf `Global` oder `Website` festgelegt werden. Sie kann jedoch erst zu Beginn des Einrichtungsprozesses festgelegt werden. Die Website-Auswahl wird in Schritt 2 der [freigegebenen Katalogeinrichtung“ &#x200B;](catalog-shared-pricing-structure.md).

![Website-Auswahl](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **Katalog** und wählen Sie darunter **Katalog** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **Preis** .

1. Legen Sie **Katalogpreisbereich** auf `Website` fest.

   ![Katalogpreis-Umfang](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Schritt 1: Freigegebenen Katalog erstellen

Es gibt zwei Möglichkeiten, einen freigegebenen Katalog zu erstellen. Sie können einen freigegebenen Katalog eines beliebigen Typs erstellen oder einen vorhandenen freigegebenen Katalog duplizieren. Ein neuer freigegebener Katalog enthält keine Produkte und wurde noch keiner Firma zugewiesen.

### Methode 1: Neuen freigegebenen Katalog hinzufügen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Shared Catalog]** und führen Sie folgende Schritte aus:

   - Geben Sie einen **[!UICONTROL Name]** für den freigegebenen Katalog ein.

     Der zugewiesene Name wird im Admin- und Kunden-Dashboard verwendet, um ggf. auf den freigegebenen Katalog zu verweisen. Er wird auch zum Namen der entsprechenden Kundengruppe.

   - Wählen Sie **[!UICONTROL Type]** : `Custom` oder `Public` aus.

   - Wählen Sie die entsprechende **[!UICONTROL Customer Tax Class]** aus, die für Käufe aus dem freigegebenen Katalog gilt.

     Weitere Informationen zur Einrichtung und Definition der Steuerklasse finden Sie unter [Steuerklassen](../stores-purchase/tax-class.md).

     Das folgende Beispiel zeigt einen neuen benutzerdefinierten Katalog für einen bestimmten Großhandelskunden.

     ![Neuer freigegebener Katalog](./assets/shared-catalog-new.png){width="600" zoomable="yes"}

   - **[!UICONTROL Description]** eingeben

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

   Der neue Katalog wird im _[!UICONTROL Shared Catalogs]_&#x200B;angezeigt.

### Methode 2: Duplizieren eines vorhandenen freigegebenen Katalogs

Ein doppelter benutzerdefinierter Katalog behält das Preismodell und die Struktur des Originals bei, jedoch nicht die Unternehmensverknüpfungen. Eine entsprechende Kundengruppe wird ebenfalls mit demselben Namen wie der doppelte Katalog erstellt. Standardmäßig erhält ein doppelter Katalog den Namen _Duplikat_ des ursprünglichen Katalogs.

Wenn ein öffentlicher freigegebener Katalog dupliziert wird, ändert sich der Typ des doppelten Katalogs in `custom`.

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Wechseln Sie für den freigegebenen Katalog im Raster, den Sie duplizieren möchten, zur Spalte **[!UICONTROL Action]** und wählen Sie **[!UICONTROL General Settings]** aus.

1. Klicken Sie in den Optionen oben auf der Seite auf **[!UICONTROL Duplicate]**.

   ![Doppelter freigegebener Katalog](./assets/shared-catalog-duplicate.png){width="600" zoomable="yes"}

1. Aktualisieren Sie die folgenden Felder für den neuen Katalog:

   - **[!UICONTROL Name]**
   - **[!UICONTROL Type]**
   - **[!UICONTROL Customer Tax Class]**
   - **[!UICONTROL Description]**

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

   Das Duplikat wird im _[!UICONTROL Shared Catalogs]_&#x200B;mit einer eindeutigen ID angezeigt.

## Schritt 2: Abschließen der Einrichtung

Nachdem Sie einen neuen freigegebenen Katalog erstellt haben, müssen Sie ihn mit der entsprechenden Produktauswahl, [Unternehmenszuweisungen](catalog-shared-assign-companies.md) und [Kategorieberechtigungen“ &#x200B;](../catalog/category-permissions.md). Weitere Informationen finden Sie unter [Festlegen von Preisen und Strukturen](catalog-shared-pricing-structure.md).

>[!NOTE]
>
>**[B2B-Version 1.3.](release-notes.md#b2b-v130) und höher** - Wenn Sie einen freigegebenen Katalog erstellen, wird jede [Kategorieberechtigung](../catalog/category-permissions.md) für den Katalog auf _[!UICONTROL Allow for the Display Product Prices]_&#x200B;und&#x200B;_[!UICONTROL Add to Cart]_ für Kundengruppen festgelegt, denen dieser Zugriff in den Katalogberechtigungseinstellungen zugewiesen ist. Zuvor wurden diese Einstellungen automatisch auf `Deny` gesetzt, auch wenn die Katalogberechtigungen auf `Allow` gesetzt waren.

## Demo zum freigegebenen Katalog

Sehen Sie sich dieses Video an, um eine Demonstration der freigegebenen Katalogverwaltung anzuzeigen:

>[!VIDEO](https://video.tv.adobe.com/v/3411351?quality=12&learn=on&captions=ger)

## Seitenverweis für freigegebenen Katalog

### Schaltflächenleiste

| Schaltfläche | Beschreibung |
|--- |--- |
| [!UICONTROL Back] | Kehrt zur Seite Freigegebene Kataloge zurück, ohne den neuen freigegebenen Katalog zu speichern. |
| [!UICONTROL Reset] | Löscht das Formular von nicht gespeicherten Änderungen und stellt die ursprünglichen Katalogdetailinformationen wieder her. |
| [!UICONTROL Save and Continue Edit] | Speichert alle Änderungen und lässt das Formular im Bearbeitungsmodus geöffnet. |
| [!UICONTROL Save] | Speichert Änderungen, schließt das Formular und kehrt zur Seite Freigegebene Kataloge zurück. |

{style="table-layout:auto"}

### Katalogdetails

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Name] | Identifiziert den freigegebenen Katalog innerhalb des Admin-Bereichs und in den Kundenkonten, in denen er verfügbar ist. Der Katalogname sollte beschreibend sein und nicht mehr als 32 Zeichen lang sein. Sie können nicht zwei freigegebene Kataloge mit demselben Namen haben. Maximal Zeichen: 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Gibt einen Katalog mit benutzerdefinierter Preisgestaltung an, der nur für die spezifischen Unternehmen verfügbar ist, denen er zugewiesen ist.<br/>**[!UICONTROL Public]**- Identifiziert den freigegebenen Katalog, der für alle Gastbesucher und für angemeldete Kunden verfügbar ist, die keiner Firma zugeordnet sind. Bei der Installation von [!DNL Adobe Commerce B2B] wird ein standardmäßiger öffentlicher freigegebener Katalog erstellt, der jedoch von einem Store-Administrator konfiguriert werden muss. Es kann immer nur ein öffentlicher freigegebener Katalog vorhanden sein. |
| [!UICONTROL Customer Tax Class] | Bestimmt die Steuerklasse, die für Käufe aus dem Katalog verwendet wird. Die Optionen umfassen alle verfügbaren Steuerklassen. |
| [!UICONTROL Description] | Eine kurze Erläuterung der Verwendung des Katalogs. |

{style="table-layout:auto"}

### Rasterspalten

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Eine eindeutige numerische Kennung, die einer freigegebenen Katalogentität zugewiesen ist. |
| [!UICONTROL Name] | Der Name des freigegebenen Katalogs. |
| [!UICONTROL Type] | Gibt den Typ des freigegebenen Katalogs an. Kann `Public` oder `Custom` sein. |
| [!UICONTROL Created At] | Das Datum, an dem der freigegebene Katalog im System erstellt wurde. |
| [!UICONTROL Created By] | Der Name des Admin-Benutzers, der einen freigegebenen Katalog erstellt hat. |
| [!UICONTROL Action] | Die Liste der Aktionen. Optionen: `Set Pricing and Structure`, `Assign Companies`, `General Settings`, `Delete`. |

{style="table-layout:auto"}
