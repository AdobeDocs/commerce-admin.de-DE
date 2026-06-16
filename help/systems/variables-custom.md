---
title: Hinzufügen benutzerdefinierter Variablen
description: Erfahren Sie, wie Sie benutzerdefinierte Variablen erstellen und in Seiten, Blöcke und Produktinhalte einfügen.
exl-id: 8233518a-abcf-4889-b75b-4aa503c7cebb
role: Admin, User
feature: System, Variables, Page Content, Communications
TQID: https://experienceleague.adobe.com/zhgemfdr2g5sanaFuiF9l20figj9ZD-3codE97WWWg8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 344
ht-degree: 1%

---

# Hinzufügen benutzerdefinierter Variablen

Um die spezifischen Anforderungen Ihres Unternehmens zu erfüllen, können Sie benutzerdefinierte Variablen erstellen und sie in [Seiten](../content-design/pages.md), [Blöcke](../content-design/blocks.md) und [E-Mail-Vorlagen](email-templates.md) einfügen. Die Liste der zulässigen Variablen, die angezeigt wird, wenn Sie auf die Schaltfläche _Variable einfügen_ klicken, enthält sowohl [vordefinierte](variables-predefined.md) als auch benutzerdefinierte Variablen. Die Liste der verfügbaren Variablen für eine bestimmte E-Mail-Vorlage wird durch die Daten bestimmt, die mit der Vorlage verknüpft sind. Unter [Variablenreferenz](variables-reference.md) finden Sie eine Liste der häufig verwendeten E-Mail-Vorlagen und der zugehörigen Variablen.

![Benutzerdefinierte Variablen](./assets/variables-custom.png){width="600" zoomable="yes"}

>[!NOTE]
>
>In E-Mail- und Newsletter-Vorlagen können nur zulässige vordefinierte oder benutzerdefinierte Variablen verwendet werden.

## Schritt 1: Benutzerdefinierte Variable erstellen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Custom Variables]**.

1. Klicken Sie auf **[!UICONTROL Add New Variable]**.

1. Geben Sie eine Kennung für **[!UICONTROL Variable Code]** ein, wobei nur Kleinbuchstaben ohne Leerzeichen verwendet werden.

   Bei Bedarf können Sie zur Darstellung von Leerzeichen Unterstriche oder Bindestriche verwenden. Beispiel: `my_custom_variable`

1. Geben Sie eine **[!UICONTROL Variable Name]** ein, die als interne Referenz verwendet wird. Beispiel: `My Custom Variable`

1. Um den Wert einzugeben, der mit der Variablen verknüpft ist, führen Sie einen der folgenden Schritte aus:

   - Geben Sie **[!UICONTROL Variable HTML Value]** den Variablenwert ein, der mit einfachen HTML-Tags formatiert ist. Beispiel:

     `<b>This formatted content appears in place of the variable.</b>`

   - Geben Sie **[!UICONTROL Variable Plain Value]** den Variablenwert als unformatierten Text ein. Beispiel:

     `This unformatted content appears in place of the variable.`

   >[!TIP]
   >
   >Wenn Sie mehr Platz benötigen, ziehen Sie die untere rechte Ecke des Textfelds.

   ![Neue benutzerdefinierte Variable](./assets/variable-custom-add.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

## Schritt 2: Benutzerdefinierte Variable in Ihren Inhalt einfügen

Verwenden Sie [!DNL Page Builder], um eine benutzerdefinierte Variable einzufügen.

1. Öffnen Sie die Seite, den Block, die Kategorie oder das Produkt, zu der bzw. dem Sie die Variable zum Inhalt hinzufügen möchten.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Content]** .

1. Klicken Sie auf **[!UICONTROL Edit with Page Builder]**.

1. Klicken Sie im linken Bedienfeld auf **[!UICONTROL Elements]** und führen Sie einen der folgenden Schritte aus:

   - Klicken Sie in einen vorhandenen Textbereich, in den Sie die Variable einfügen möchten.

   - Ziehen Sie ein neues **[!UICONTROL Text]** auf die Bühne.

1. Klicken Sie ganz rechts in der Editor-Symbolleiste auf ( ![Variable einfügen](./assets/editor-btn-insert-variable.png) ), um eine Variable einzufügen.

   ![[!DNL Page Builder] und Bedienfeld](./assets/variable-custom-pagebuilder-stage.png){width="600" zoomable="yes"}

1. Wählen Sie in der Liste die benutzerdefinierte Variable aus, die Sie einfügen möchten, und klicken Sie auf **[!UICONTROL Insert Variable]**.

   ![Neue benutzerdefinierte Variable](./assets/variable-custom-insert-select.png){width="600" zoomable="yes"}

   Die Variablenkennung wird als Platzhalter im Editor angezeigt.

   ![[!DNL Page Builder] - Variablenplatzhalter](./assets/pagebuilder-variable-inserted.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.
