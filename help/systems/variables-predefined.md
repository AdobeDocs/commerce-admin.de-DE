---
title: Vordefinierte Variablen verwenden
description: Erfahren Sie mehr über die vordefinierten Variablen und wie sie in einer E-Mail-Vorlage hinzugefügt werden.
exl-id: 01e909c4-c932-4262-9f33-bd2740a6355f
role: Admin, User
feature: System, Variables, Page Content, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Vordefinierte Variablen verwenden

[Vordefinierte](variables-predefined.md) Variablen erleichtern die Personalisierung von Vorlagen für [E-Mail](email-templates.md) und [Newsletter](../merchandising-promotions/newsletters.md) sowie anderer Inhaltstypen. Die Liste der zulässigen [vordefinierten](variables-predefined.md) Variablen wird angezeigt, wenn Sie auf die Schaltfläche &quot;Variable einfügen&quot;klicken. Wie in der folgenden Abbildung dargestellt, wird die Liste der verfügbaren Variablen für eine bestimmte E-Mail-Vorlage durch die mit der Vorlage verknüpften Daten bestimmt. Eine Liste häufig verwendeter E-Mail-Vorlagen und der zugehörigen Variablen finden Sie in der [Variablenreferenz](variables-reference.md) .

![Vordefinierte Variablen für E-Mail-Vorlage](./assets/email-template-new-pickup-order-predefined-variables.png){width="700" zoomable="yes"}

## Variable zu einer E-Mail-Vorlage hinzufügen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Führen Sie einen der folgenden Schritte aus:

   - Um die Variable einer vorhandenen Vorlage hinzuzufügen, klicken Sie in der Liste auf die Vorlage, um sie im Bearbeitungsmodus zu öffnen.

   - Um die Variable in einer neuen Vorlage zu verwenden, klicken Sie auf **[!UICONTROL Add New Template]** und passen Sie den Standardvorlagencode an. Siehe [Nachrichtenvorlagen](email-template-custom.md#message-templates).

1. Wählen Sie unter _[!UICONTROL Load default template]_die **[!UICONTROL Template]**aus, die Sie anpassen möchten.

1. Um eine Vorlage anzuwenden, klicken Sie auf **[!UICONTROL Load Template]**.

   Das Feld _[!UICONTROL Currently used for]_zeigt den Konfigurationspfad für die Vorlage an. Die_[!UICONTROL Template Subject]_ und _[!UICONTROL Template Content]_werden automatisch relativ zur ausgewählten Vorlage generiert.

   - **[!UICONTROL Template Subject]** - Dieser Text wird in der Betreffzeile einer E-Mail angezeigt.

   - **[!UICONTROL Template Content]** - Dieser Text wird im vollständigen Inhalt der gesendeten E-Mail angezeigt.

   ![Inhalt der E-Mail-Vorlage](./assets/email-template-content.png){width="600" zoomable="yes"}

1. Geben Sie einen **[!UICONTROL Template Name]** ein.

1. Klicken Sie für eine Liste der [vordefinierten](variables-predefined.md) Variablen, die mit dieser E-Mail-Vorlage verwendet werden können, auf **[!UICONTROL Insert Variable]**.

   Bestimmen Sie, welche Variable in die Vorlage eingefügt werden soll. Klicken Sie dann oben rechts auf _Schließen_ (X). (Sie kehren später dazu zurück.)

1. Um eine Nachbildung der Vorlage anzuzeigen, klicken Sie in der Schaltflächenleiste auf **[!UICONTROL Preview Template]** .

   Wenn die Vorschau auf einer neuen Registerkarte geöffnet wird, legen Sie fest, wo die Variable im Verhältnis zum anderen Inhalt platziert werden soll. Kehren Sie dann zur ursprünglichen Registerkarte zurück, um fortzufahren.

   ![Vorschauvorlage anzeigen](./assets/email-template-new-pickup-order-preview.png){width="600" zoomable="yes"}

1. Positionieren Sie im Feld **[!UICONTROL Template Content]** die Einfügemarke an der Stelle, an der die Variable angezeigt werden soll, und klicken Sie auf **[!UICONTROL Insert Variable...]**.

1. Klicken Sie in der Liste der verfügbaren Variablen auf die Variable, die Sie in die Vorlage einfügen möchten.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Template]**.

## Konvertieren der Vorlage in Text

1. Öffnen einer Vorlage im Bearbeitungsmodus

1. Klicken Sie oben auf der Seite auf **[!UICONTROL Convert to Plain Text]**.

1. Wenn Sie aufgefordert werden, Tags zu entfernen, klicken Sie auf **[!UICONTROL OK]**.

1. Um die Textversion zu speichern, klicken Sie auf **[!UICONTROL Save Template]**.

## HTML-Version wiederherstellen

1. Klicken Sie oben auf der Seite auf **[!UICONTROL Return HTML Version]**.

1. Um die HTML-Version der Vorlage zu speichern, klicken Sie auf **[!UICONTROL Save Template]**.
