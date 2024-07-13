---
title: Store-Ansichten
description: Erfahren Sie, wie Sie eine Store-Ansicht hinzufügen und bearbeiten.
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# Store-Ansichten

Store-Ansichten werden normalerweise verwendet, um den Store in verschiedenen Gebietsschemata verfügbar zu machen. Käufer können die Sprachauswahl in der Kopfzeile des Stores verwenden, um die Store-Ansicht zu ändern.

![Umfang - Mehrere Store-Ansichten](./assets/scope-multiview.svg){width="550"}

## Hinzufügen einer Store-Ansicht

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

   ![Alle Stores](./assets/stores-all.png){width="700" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Create Store View]**.

   ![ Store-Ansicht erstellen](./assets/create-store-view.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Store]** auf den übergeordneten Store dieser Ansicht.

1. Geben Sie für diese Store-Ansicht den Wert &quot;**[!UICONTROL Name]**&quot;ein.

   Der Name wird in der Sprachauswahl in der Store-Kopfzeile angezeigt. Beispiel: `Spanish`.

1. Geben Sie für **[!UICONTROL Code]** den Code ein, der die Ansicht identifiziert (in Kleinbuchstaben).

   Beispiel: `spanish`.

1. Um die Ansicht zu aktivieren, setzen Sie **[!UICONTROL Status]** auf `Enabled`.

1. (Optional) Geben Sie eine **[!UICONTROL Sort Order]** -Zahl ein, um die Sequenz zu bestimmen, in der diese Ansicht mit anderen Ansichten aufgeführt wird.

1. Klicken Sie auf **[!UICONTROL Save Store View]**.

## Bearbeiten einer Store-Ansicht

Da der Ansichtsname in der Sprachauswahl angezeigt wird, sollten Sie den Namen der Standardansicht eventuell in eine aussagekräftigere Bezeichnung ändern. Das Feld _Name_ ist einfach eine Bezeichnung und kann einfach geändert werden.

Wenn für Ihre Adobe Commerce- oder Magento Open Source-Installation eine Multisite- oder Multi-Store-Einrichtung eingerichtet ist, ändern Sie das Feld &quot;Code speichern&quot;nicht, ohne sicherzustellen, dass der Wert nicht in der Datei `index.php` referenziert wird. Wenn Sie keinen Zugriff auf den Server haben, um die Datei zu untersuchen, bitten Sie einen Entwickler um Hilfe.

| Feld | Ausgangswert | Aktualisierter Wert |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Klicken Sie in der Spalte _[!UICONTROL Store View]_des Rasters auf den Namen der Ansicht, die Sie bearbeiten möchten.

   Beim Bearbeiten der Standardansicht sind die Felder _[!UICONTROL Store]_und_[!UICONTROL Status]_ nicht verfügbar.

   ![Store-Ansicht - bearbeitete Standardansicht](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. Aktualisieren Sie die folgenden Felder nach Bedarf:

   - **[!UICONTROL Store]** (nur nicht standardmäßige Ansichten)
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** (nur wenn nicht in `index.php` verwendet)
   - **[!UICONTROL Status]** (nur nicht standardmäßige Ansichten)
   - **[!UICONTROL Sort Order]**

1. Klicken Sie auf **[!UICONTROL Save Store View]**.
