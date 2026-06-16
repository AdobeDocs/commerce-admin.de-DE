---
title: Ansichten speichern
description: Erfahren Sie, wie Sie eine Store-Ansicht hinzufügen und bearbeiten.
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
TQID: https://experienceleague.adobe.com/2VMBTnzG3lqsNEyx-e46rqDs1wHofaDeHL3j3SuqxOE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
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
source-wordcount: 284
ht-degree: 0%

---

# Ansichten speichern

Store-Ansichten werden normalerweise verwendet, um den Store in verschiedenen Gebietsschemata verfügbar zu machen. Käufer können die Sprachauswahl in der Kopfzeile des Stores verwenden, um die Store-Ansicht zu ändern.

![Umfang - mehrere Store-Ansichten](./assets/scope-multiview.svg){width="550"}

## Shop-Ansicht hinzufügen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

   ![Alle Stores](./assets/stores-all.png){width="700" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Create Store View]**.

   ![Store-Ansicht erstellen](./assets/create-store-view.png){width="600" zoomable="yes"}

1. **[!UICONTROL Store]** auf den übergeordneten Speicher dieser Ansicht festlegen.

1. Geben Sie einen **[!UICONTROL Name]** für diese Store-Ansicht ein.

   Der Name wird in der Sprachauswahl in der Store-Kopfzeile angezeigt. Beispiel: `Spanish`.

1. Geben Sie **[!UICONTROL Code]** den Code ein, der die Ansicht identifiziert (in Kleinbuchstaben).

   Beispiel: `spanish`.

1. Um die Ansicht zu aktivieren, setzen Sie **[!UICONTROL Status]** auf `Enabled`.

1. (Optional) Geben Sie eine **[!UICONTROL Sort Order]** ein, um die Reihenfolge zu bestimmen, in der diese Ansicht in anderen Ansichten aufgeführt wird.

1. Klicken Sie auf **[!UICONTROL Save Store View]**.

## Shop-Ansicht bearbeiten

Da der Ansichtsname in der Sprachauswahl angezeigt wird, empfiehlt es sich, den Namen der Standardansicht zu ändern, damit diese anschaulicher wird. Das Feld _Name_ ist einfach eine Bezeichnung und kann einfach geändert werden.

Wenn Ihre Adobe Commerce- oder Magento Open Source-Installation über eine Multi-Site- oder Multi-Store-Einrichtung verfügt, ändern Sie das Feld „Store-Code“ nicht, ohne sicherzustellen, dass der Wert in der `index.php`-Datei nicht referenziert wird. Wenn Sie keinen Zugriff auf den Server haben, um die Datei zu untersuchen, bitten Sie einen Entwickler um Hilfe.

| Feld | Ausgangswert | Aktualisierter Wert |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Klicken Sie in der Spalte _[!UICONTROL Store View]_&#x200B;des Rasters auf den Namen der Ansicht, die Sie bearbeiten möchten.

   Beim Bearbeiten der Standardansicht sind die Felder _[!UICONTROL Store]_&#x200B;und&#x200B;_[!UICONTROL Status]_ nicht verfügbar.

   ![Store-Ansicht - Standardansicht bearbeiten](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. Aktualisieren Sie die folgenden Felder nach Bedarf:

   - **[!UICONTROL Store]** (nur nicht standardmäßige Ansichten)
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** (nur wenn nicht in `index.php` verwendet)
   - **[!UICONTROL Status]** (nur nicht standardmäßige Ansichten)
   - **[!UICONTROL Sort Order]**

1. Klicken Sie auf **[!UICONTROL Save Store View]**.
