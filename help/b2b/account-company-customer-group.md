---
title: Zuweisen einer Kundengruppe zu einer Firma
description: Erfahren Sie, wie Sie einem Unternehmenskonto in Ihrem Adobe Commerce-Store eine Kundengruppe zuweisen.
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
source-git-commit: 581d2cf82880552432471171b69a1a597da54c30
workflow-type: tm+mt
source-wordcount: '236'
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
