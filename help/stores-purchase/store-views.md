---
title: Store-Ansichten
description: Erfahren Sie, wie Sie eine Store-Ansicht hinzufügen und bearbeiten.
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 2%

---

# Store-Ansichten

Store-Ansichten werden normalerweise verwendet, um den Store in verschiedenen Gebietsschemata verfügbar zu machen. Käufer können die Sprachauswahl in der Kopfzeile des Stores verwenden, um die Store-Ansicht zu ändern.

![Umfang - mehrere Store-Ansichten](./assets/scope-multiview.svg){width="550"}

## Hinzufügen einer Store-Ansicht

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

   ![Alle Stores](./assets/stores-all.png){width="700" zoomable="yes"}

1. Klicken **[!UICONTROL Create Store View]**.

   ![Store-Ansicht erstellen](./assets/create-store-view.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Store]** zum übergeordneten Speicher dieser Ansicht.

1. Geben Sie einen **[!UICONTROL Name]** für diese Store-Ansicht.

   Der Name wird in der Sprachauswahl in der Store-Kopfzeile angezeigt. Beispiel: `Spanish`.

1. Für **[!UICONTROL Code]** eingeben, geben Sie den Code ein, der die Ansicht identifiziert (in Kleinbuchstaben).

   Beispiel: `spanish`.

1. Um die Ansicht zu aktivieren, legen Sie **[!UICONTROL Status]** nach `Enabled`.

1. (Optional) Geben Sie einen **[!UICONTROL Sort Order]** -Zahl, um die Sequenz zu bestimmen, in der diese Ansicht mit anderen Ansichten aufgeführt wird.

1. Klicken **[!UICONTROL Save Store View]**.

## Bearbeiten einer Store-Ansicht

Da der Ansichtsname in der Sprachauswahl angezeigt wird, sollten Sie den Namen der Standardansicht eventuell in eine aussagekräftigere Bezeichnung ändern. Die _Name_ -Feld ist einfach eine Bezeichnung und kann leicht geändert werden.

Wenn Ihre Adobe Commerce- oder Magento Open Source-Installation über eine Multisite- oder Multi-Store-Einrichtung verfügt, ändern Sie das Feld &quot;Code speichern&quot;nicht, ohne zu überprüfen, ob der Wert nicht im `index.php` -Datei. Wenn Sie keinen Zugriff auf den Server haben, um die Datei zu untersuchen, bitten Sie einen Entwickler um Hilfe.

| Feld | Ausgangswert | Aktualisierter Wert |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** >  _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Im _[!UICONTROL Store View]_auf den Namen der Ansicht klicken, die Sie bearbeiten möchten.

   Wenn Sie die Standardansicht bearbeiten, wird die _[!UICONTROL Store]_und_[!UICONTROL Status]_ -Felder sind nicht verfügbar.

   ![Store-Ansicht - Standardansicht bearbeiten](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. Aktualisieren Sie die folgenden Felder nach Bedarf:

   - **[!UICONTROL Store]** (nur nicht standardmäßige Ansichten)
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** (nur bei Verwendung in `index.php`)
   - **[!UICONTROL Status]** (nur nicht standardmäßige Ansichten)
   - **[!UICONTROL Sort Order]**

1. Klicken **[!UICONTROL Save Store View]**.
