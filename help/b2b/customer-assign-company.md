---
title: Hinzufügen von Benutzern zu einem Unternehmenskonto
description: Erfahren Sie, wie Sie einen bestehenden Kunden zu einem Unternehmenskonto hinzufügen.
exl-id: ee2f9c27-37d6-4997-8285-1c4c84f8d04c
feature: B2B, Companies, Customers
role: Admin, User
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---

# Hinzufügen von Benutzern zu einem Unternehmenskonto

Wenn er in der Konfiguration aktiviert ist, fügt der Unternehmensadministrator Unternehmensbenutzer von der Storefront hinzu und verwaltet sie. Firmen-Benutzerkonten können jedoch auch über den Administrator hinzugefügt und verwaltet werden.

Bei Bedarf können Sie einen Benutzer mehreren Unternehmen zuweisen. Wenn B2B-Käufer beispielsweise mehrere Unternehmen unterstützen, können Sie deren Benutzerkonten zu allen Unternehmen hinzufügen, mit denen sie Geschäfte machen. In der Storefront können Käufer, die mehreren Unternehmen zugewiesen sind, zwischen Unternehmenskonten wechseln, indem sie aus den verfügbaren Unternehmen im *[!UICONTROL Company]* auswählen.

![Mit Firma verknüpfen](./assets/company-assign-multi-switcher.png){width="700"}

>[!NOTE]
>
>Wenn eine Person bereits ein persönliches Konto bei Ihrem Geschäft hat und später für eine Firma arbeiten geht, weisen Sie das persönliche Konto der Person nicht der Firma zu. Erstellen Sie stattdessen ein Firmen-Benutzerkonto für die Person mit einer Firmen-E-Mail-Adresse.

## Einen Firmenbenutzer hinzufügen

Wenn Sie einen Firmenbenutzer hinzufügen, ist das erste Unternehmen, das Sie mit dem Benutzerkonto verknüpfen, das Standardunternehmen.

1. Navigieren Sie in der Admin-Seitenleiste zu **[!UICONTROL Customers > All Customers]**.

1. Klicken Sie auf **[!UICONTROL Add new customer]**.

1. Konfigurieren Sie das neue Konto.

   1. Geben Sie den anfänglichen Kontostatus an, indem Sie den Umschalter **[!UICONTROL Customer Active]** festlegen.

      Aktivieren, um das Konto sofort zu aktivieren, oder deaktivieren, um ein inaktives Konto zu erstellen.

   1. Wählen Sie den Umfang der Website aus der Liste **[!UICONTROL Associate to Website]** aus.

   1. Klicken Sie auf **[!UICONTROL Associate to Company]** , um die verfügbaren Unternehmen anzuzeigen.

      ![Mit Firma verknüpfen](./assets/company-assign-customer-account.png){width="675"}

      Filtern Sie bei Bedarf die Liste, indem Sie die ersten Buchstaben des Firmennamens in das Eingabefeld eingeben.

   1. Wählen Sie in der Liste eine oder mehrere Firmen aus, denen Sie den Kunden zuweisen möchten, und klicken Sie auf **[!UICONTROL Done]**.

      Firmenbenutzer werden automatisch der Kundengruppe (oder dem [freigegebenen Katalog](catalog-shared.md) für jedes Unternehmen hinzugefügt, das mit ihrem Konto verknüpft ist.

   1. Geben Sie die erforderlichen Benutzerkontoinformationen ein: **[!UICONTROL First Name]**, **[!UICONTROL Last Name]** und **[!UICONTROL Email]**.

   1. Ermöglichen Sie Vertriebsmitarbeitern, sich im Namen des Kunden bei der Storefront anzumelden, indem Sie **[!UICONTROL Allow remote shopping assistance]** aktivieren.

   1. Wenden Sie die Änderungen an, indem Sie auf **[!UICONTROL Save Customer]** klicken.

      ![Kundenraster mit Unternehmenszuweisungen](./assets/company-assign-user-assignments.png){width="675"}

Das [!UICONTROL Customers grid] zeigt für jedes Unternehmen, dem der Benutzer zugewiesen ist, eine separate Zeile an. Die folgenden Spalten werden aktualisiert.

- Die Spalte _[!UICONTROL Customer Type]_wird aktualisiert und zeigt die dem Benutzer zugewiesene Rolle an.

  Wenn der Kunde zum ersten Mal einem Unternehmen zugewiesen wurde, wird die Spalte _[!UICONTROL Customer Type]_von_[!UICONTROL Individual user]_ auf _[!UICONTROL Company User]_aktualisiert.

- Die Spalte _[!UICONTROL Group]_ändert sich in den Namen der Kundengruppe (oder des freigegebenen Katalogs), die bzw. der dem Unternehmen zugewiesen ist.

- In der Spalte _[!UICONTROL Company]_wird der Name des Unternehmens angezeigt, mit dem das Kundenprofil jetzt verknüpft ist.

## Zuweisen eines Benutzers zu einem oder mehreren Unternehmenskonten

Wenn Sie einen neuen Benutzer zuweisen, ist das erste Unternehmen, das Sie mit dem Benutzerkonto verknüpfen, das Standardunternehmen.

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden im Raster und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Account Information]** aus.

1. Wählen Sie in der **[!UICONTROL Associate to Company]**-Liste eine oder mehrere Firmen aus, die Sie dem Firmenbenutzer zuweisen möchten, und klicken Sie auf **[!UICONTROL Done]**.

1. Wenden Sie die Änderungen an, indem Sie auf **[!UICONTROL Save Customer]** klicken.

## Unternehmenszuweisung aus einem Benutzerkonto entfernen

Wenn Sie eine Firma aus einem Benutzerprofil entfernen, wird der Benutzerzugriff auf diese Firma aufgehoben. Benutzerdaten bleiben in Admin verfügbar. Wenn Sie alle Unternehmenszuweisungen entfernen, ändert sich die _[!UICONTROL Customer Type]_in *[!UICONTROL Individual user]*Deaktivieren der B2B-Funktionen für das Konto.

1. Bearbeiten Sie im Kundenraster in der Admin das zu aktualisierende Kundenprofil.

1. Entfernen Sie im Abschnitt *[!UICONTROL Account Information] eine zugewiesene Firma aus dem Feld **[!UICONTROL Associate to Company]**, indem Sie auf die **[!UICONTROL X]** im Label Firmenname klicken.

1. Wenden Sie die Änderungen an, indem Sie auf **[!UICONTROL Save Customer]** klicken.

>[!NOTE]
>
>Wenn ein Firmenbenutzer als Unternehmensadministrator zugewiesen wird, können Sie die Unternehmensverknüpfung von diesem Benutzer erst aktualisieren, wenn Sie das Firmenkonto aktualisieren, um einen neuen Unternehmensadministrator zuzuweisen.
