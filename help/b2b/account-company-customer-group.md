---
title: Zuweisen einer Kundengruppe zu einer Firma
description: Erfahren Sie, wie Sie einem Unternehmenskonto in Ihrem Adobe Commerce-Store eine Kundengruppe zuweisen.
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
TQID: https://experienceleague.adobe.com/O03eRkYyE78HIHjmwYRXqfOR2A7k1KFL11AspJGCi-U
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 236
ht-degree: 0%

---

# Zuweisen einer Kundengruppe zu einer Firma

Das Zuweisen einer Kundengruppe zu einem Unternehmen entspricht im Wesentlichen dem Zuweisen eines freigegebenen Katalogs. Wenn der freigegebene Katalog nicht [in der Konfiguration aktiviert](enable-basic-features.md) wird einem Unternehmen eine Kundengruppe - und kein freigegebener Katalog - zugewiesen.

- Einem Unternehmen kann jeweils nur eine Kundengruppe oder ein freigegebener Katalog zugewiesen werden. Eine Kundengruppe, die einem freigegebenen Katalog zugeordnet ist, kann nicht gelöscht werden.
- Wenn Sie die der Firma zugewiesene Kundengruppe ändern, werden die Profile aller Firmenmitglieder aktualisiert.
- Wenn die Kundengruppenzuweisung von einem freigegebenen Katalog in eine reguläre Kundengruppe geändert wird, verlieren die Firmenmitglieder den Zugriff auf den freigegebenen Katalog, und der primäre Katalog wird für sie in der Storefront verfügbar.
- Nach dem Ändern der Unternehmensgruppe muss sich ein Firmenbenutzer abmelden und in der Storefront anmelden, um neue Preise im Katalog zu sehen.

## Ändern der Kundengruppe

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Suchen Sie das Unternehmen im Raster und klicken Sie in der Spalte _[!UICONTROL Action]_&#x200B;auf **[!UICONTROL Edit]**.

   ![Firma bearbeiten](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. Scrollen Sie auf der Unternehmensseite nach unten und erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Advanced Settings]** .

1. Legen Sie die entsprechende **[!UICONTROL Customer Group]** fest.

   Die [!UICONTROL Customer Group] enthält alle vorhandenen freigegebenen Kataloge, auch wenn diese in der Konfiguration deaktiviert sind.

   ![Kundengruppe oder freigegebenen Katalog ändern](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

1. Wenn Sie zum Bestätigen aufgefordert werden, klicken Sie auf **[!UICONTROL Proceed]**.

1. Klicken Sie auf **[!UICONTROL Save]**.
