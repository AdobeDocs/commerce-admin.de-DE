---
title: Vordefinierte Variablen verwenden
description: Erfahren Sie mehr über die vordefinierten Variablen und wie Sie sie einer E-Mail-Vorlage hinzufügen.
exl-id: 01e909c4-c932-4262-9f33-bd2740a6355f
role: Admin, User
feature: System, Variables, Page Content, Communications
TQID: 'https://experienceleague.adobe.com/TKhaNVRFLc3VK0iDkCpqoWSnvFRJmDWAIw1uBPzlh00'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 8d0b446f-5b16-5a10-b272-01143504a11c
    internal-label: System
  - id: 17d326fa-534a-55a5-b46f-8ae1de1e2f75
    internal-label: Page Content
  - id: bb03f6c4-cab9-560e-9d02-5816e1808d17
    internal-label: Communications
subfeature_v2:
  - id: 2191e157-828a-5358-ad69-ebcaa8402915
    internal-label: Variables
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%
---
# Vordefinierte Variablen verwenden

[Vordefinierte](variables-predefined.md) Variablen erleichtern die Personalisierung von [E-Mail](email-templates.md)- und [Newsletter](../merchandising-promotions/newsletters.md)-Vorlagen und anderen Inhaltstypen. Die Liste der zulässigen [vordefinierten](variables-predefined.md) Variablen wird angezeigt, wenn Sie auf die Schaltfläche Variable einfügen klicken. Wie in der folgenden Abbildung dargestellt, wird die Liste der verfügbaren Variablen für eine bestimmte E-Mail-Vorlage durch die Daten bestimmt, die mit der Vorlage verknüpft sind. Unter [Variablenreferenz](variables-reference.md) finden Sie eine Liste der häufig verwendeten E-Mail-Vorlagen und der zugehörigen Variablen.

![Vordefinierte Variablen für E-Mail-Vorlage](./assets/email-template-new-pickup-order-predefined-variables.png){width="700" zoomable="yes"}

## Hinzufügen einer Variablen zu einer E-Mail-Vorlage

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Führen Sie einen der folgenden Schritte aus:

   - Um die Variable zu einer vorhandenen Vorlage hinzuzufügen, klicken Sie auf die Vorlage in der Liste, um sie im Bearbeitungsmodus zu öffnen.

   - Um die Variable in einer neuen Vorlage zu verwenden, klicken Sie auf **[!UICONTROL Add New Template]** und passen Sie den Code der Standardvorlage an. Siehe [Nachrichtenvorlagen](email-template-custom.md#message-templates).

1. Wählen Sie unter _[!UICONTROL Load default template]_&#x200B;die **[!UICONTROL Template]**&#x200B;aus, die Sie anpassen möchten.

1. Um eine Vorlage anzuwenden, klicken Sie auf **[!UICONTROL Load Template]**.

   Das Feld _[!UICONTROL Currently used for]_&#x200B;zeigt den Konfigurationspfad für die Vorlage an. Die&#x200B;_[!UICONTROL Template Subject]_ und _[!UICONTROL Template Content]_&#x200B;werden automatisch relativ zur ausgewählten Vorlage generiert.

   - **[!UICONTROL Template Subject]** - Dieser Text wird in der Betreffzeile einer E-Mail angezeigt.

   - **[!UICONTROL Template Content]** - Dieser Text wird im vollständigen Inhalt der gesendeten E-Mail angezeigt.

   ![E-Mail-Vorlageninhalt](./assets/email-template-content.png){width="600" zoomable="yes"}

1. Geben Sie einen **[!UICONTROL Template Name]** ein.

1. Eine Liste der [vordefinierten](variables-predefined.md) Variablen, die mit dieser E-Mail-Vorlage verwendet werden können, finden Sie **[!UICONTROL Insert Variable]**.

   Bestimmen Sie, welche Variable Sie in die Vorlage einfügen möchten. Klicken Sie dann _Schließen_ (X) in der oberen rechten Ecke. (Sie kehren später hierauf zurück.)

1. Um ein Modell der Vorlage anzuzeigen, klicken Sie in der Schaltflächenleiste auf **[!UICONTROL Preview Template]** .

   Wenn die Vorschau auf einer neuen Registerkarte geöffnet wird, legen Sie fest, wo die Variable in Bezug auf den anderen Inhalt platziert werden soll. Kehren Sie dann zur ursprünglichen Registerkarte zurück, um fortzufahren.

   ![Vorlage in Vorschau anzeigen](./assets/email-template-new-pickup-order-preview.png){width="600" zoomable="yes"}

1. Positionieren Sie im **[!UICONTROL Template Content]** die Einfügemarke an der Stelle, an der die Variable angezeigt werden soll, und klicken Sie auf **[!UICONTROL Insert Variable...]**.

1. Klicken Sie in der Liste der verfügbaren Variablen auf die Variable, die Sie in die Vorlage einfügen möchten.

1. Klicken Sie abschließend auf **[!UICONTROL Save Template]**.

## Konvertieren der Vorlage in einfachen Text

1. Öffnen Sie eine Vorlage im Bearbeitungsmodus.

1. Klicken Sie oben auf der Seite auf **[!UICONTROL Convert to Plain Text]**.

1. Wenn Sie zum Entfernen von Tags aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.

1. Um die Nur-Text-Version zu speichern, klicken Sie auf **[!UICONTROL Save Template]**.

## HTML-Version wiederherstellen

1. Klicken Sie oben auf der Seite auf **[!UICONTROL Return HTML Version]**.

1. Um die HTML-Version der Vorlage zu speichern, klicken Sie auf **[!UICONTROL Save Template]**.
