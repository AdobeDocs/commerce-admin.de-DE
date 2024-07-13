---
title: Hinzufügen benutzerdefinierter Variablen
description: Erfahren Sie, wie Sie benutzerdefinierte Variablen erstellen und sie in Seiten, Blöcke und Produktinhalte einfügen.
exl-id: 8233518a-abcf-4889-b75b-4aa503c7cebb
role: Admin, User
feature: System, Variables, Page Content, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 1%

---

# Hinzufügen benutzerdefinierter Variablen

Um die spezifischen Anforderungen Ihres Unternehmens zu erfüllen, können Sie benutzerdefinierte Variablen erstellen und sie in [Seiten](../content-design/pages.md), [Blöcke](../content-design/blocks.md) und [E-Mail-Vorlagen](email-templates.md) einfügen. Die Liste der zulässigen Variablen, die angezeigt wird, wenn Sie auf die Schaltfläche _Variable einfügen_ klicken, enthält sowohl [vordefinierte](variables-predefined.md) als auch benutzerdefinierte Variablen. Die Liste der verfügbaren Variablen für eine bestimmte E-Mail-Vorlage wird durch die mit der Vorlage verknüpften Daten bestimmt. Eine Liste häufig verwendeter E-Mail-Vorlagen und der zugehörigen Variablen finden Sie in der [Variablenreferenz](variables-reference.md) .

![Benutzerdefinierte Variablen](./assets/variables-custom.png){width="600" zoomable="yes"}

>[!NOTE]
>
>In E-Mail- und Newsletter-Vorlagen können nur zulässige vordefinierte oder benutzerdefinierte Variablen verwendet werden.

## Schritt 1: Benutzerdefinierte Variable erstellen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Custom Variables]**.

1. Klicken Sie auf **[!UICONTROL Add New Variable]**.

1. Geben Sie eine Kennung für **[!UICONTROL Variable Code]** ein, wobei alle Kleinbuchstaben ohne Leerzeichen verwendet werden.

   Bei Bedarf können Sie einen Unterstrich oder einen Unterstrich verwenden, um ein Leerzeichen darzustellen. Beispiel: `my_custom_variable`

1. Geben Sie einen **[!UICONTROL Variable Name]** ein, der für interne Verweise verwendet wird. Beispiel: `My Custom Variable`

1. Führen Sie einen der folgenden Schritte aus, um den mit der Variablen verknüpften Wert einzugeben:

   - Geben Sie für **[!UICONTROL Variable HTML Value]** den Variablenwert ein, der mit einfachen HTML-Tags formatiert ist. Beispiel:

     `<b>This formatted content appears in place of the variable.</b>`

   - Geben Sie für &quot;**[!UICONTROL Variable Plain Value]**&quot;den Variablenwert als Nur-Text ohne Formatierung ein. Beispiel:

     `This unformatted content appears in place of the variable.`

   >[!TIP]
   >
   >Wenn Sie mehr Platz benötigen, ziehen Sie die untere rechte Ecke des Textfelds.

   ![Neue benutzerdefinierte Variable](./assets/variable-custom-add.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

## Schritt 2: Benutzerdefinierte Variable in den Inhalt einfügen

Verwenden Sie [!DNL Page Builder] , um eine benutzerdefinierte Variable einzufügen.

1. Öffnen Sie die Seite, den Block, die Kategorie oder das Produkt, der/dem Sie die Variable zum Inhalt hinzufügen möchten.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Content]** .

1. Klicken Sie auf **[!UICONTROL Edit with Page Builder]**.

1. Klicken Sie im linken Bereich auf **[!UICONTROL Elements]** und führen Sie einen der folgenden Schritte aus:

   - Klicken Sie in einen vorhandenen Textbereich, in den Sie die Variable einfügen möchten.

   - Ziehen Sie ein neues **[!UICONTROL Text]** -Objekt auf die Bühne.

1. Klicken Sie ganz rechts in der Editor-Symbolleiste auf ( ![Variable einfügen](./assets/editor-btn-insert-variable.png) ), um eine Variable einzufügen.

   ![[!DNL Page Builder] Bühne und Bedienfeld](./assets/variable-custom-pagebuilder-stage.png){width="600" zoomable="yes"}

1. Wählen Sie in der Liste die benutzerdefinierte Variable aus, die Sie einfügen möchten, und klicken Sie auf **[!UICONTROL Insert Variable]**.

   ![Neue benutzerdefinierte Variable](./assets/variable-custom-insert-select.png){width="600" zoomable="yes"}

   Die Variablenkennung wird als Platzhalter im Editor angezeigt.

   ![[!DNL Page Builder] stage - Variablenplatzhalter](./assets/pagebuilder-variable-inserted.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.
