---
title: Zuweisen einer Kundengruppe zu einem Unternehmen
description: Erfahren Sie, wie Sie in Ihrem Adobe Commerce-Store einem Unternehmenskonto eine Kundengruppe zuweisen.
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
source-git-commit: a5a8da076d6cd91eb6c3e573fec5b3fb9d2d3341
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Zuweisen einer Kundengruppe zu einem Unternehmen

Die Zuweisung einer Kundengruppe zu einem Unternehmen entspricht im Wesentlichen der Zuweisung eines freigegebenen Katalogs. Wenn &quot;Freigegebener Katalog&quot;in der Konfiguration nicht ](enable-basic-features.md) aktiviert ist, wird einer Firma eine Kundengruppe (und nicht ein freigegebener Katalog) zugewiesen.[

>[!NOTE]
>
> Einem Unternehmen kann jeweils nur eine Kundengruppe oder ein freigegebener Katalog zugewiesen werden. Eine Kundengruppe, die mit einem freigegebenen Katalog verknüpft ist, kann nicht gelöscht werden.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Suchen Sie das Unternehmen im Raster und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

   ![Unternehmen bearbeiten](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. Scrollen Sie auf der Unternehmensseite nach unten und erweitern Sie den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Advanced Settings]** .

1. Legen Sie die entsprechende **[!UICONTROL Customer Group]** fest.

   >[!NOTE]
   >
   >Die Liste &quot;[!UICONTROL Customer Group]&quot;enthält alle vorhandenen freigegebenen Kataloge, auch wenn die Option &quot;Freigegebene Kataloge&quot;in der Konfiguration deaktiviert ist.

   Wenn Sie die dem Unternehmen zugewiesene Kundengruppe ändern, werden die Profile aller Unternehmensmitglieder aktualisiert.

   >[!NOTE]
   >
   >Nachdem ein Benutzer die Unternehmensgruppe geändert hat, muss er sich bei der Storefront abmelden und sich dort anmelden, um neue Preise im Katalog zu sehen.

   ![Ändern der Kundengruppe oder des freigegebenen Katalogs](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   >[!NOTE]
   >
   >Wenn die Kundengruppenzuweisung von einem freigegebenen Katalog in eine reguläre Kundengruppe geändert wird, verlieren Unternehmensmitglieder den Zugriff auf den freigegebenen Katalog und der Hauptkatalog steht ihnen über das Storefront zur Verfügung.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL Proceed]**.

1. Klicken Sie auf **[!UICONTROL Save]**.
