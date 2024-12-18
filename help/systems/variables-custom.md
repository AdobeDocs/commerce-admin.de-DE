---
title: Hinzufügen benutzerdefinierter Variablen
description: Erfahren Sie, wie Sie benutzerdefinierte Variablen erstellen und in Seiten, Blöcke und Produktinhalte einfügen.
exl-id: 8233518a-abcf-4889-b75b-4aa503c7cebb
role: Admin, User
feature: System, Variables, Page Content, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '343'
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
