---
title: Geplante Änderungen für Katalogpreisregeln
description: Erfahren Sie, wie Sie Katalogpreisregeln im Rahmen einer Kampagne planmäßig anwenden und mit anderen Inhaltsänderungen gruppieren können.
exl-id: ec4b915f-0a27-438d-b1b0-f1bcd297af6d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 0%

---

# Geplante Änderungen für Katalogpreisregeln

{{ee-feature}}

Das Feld Geplante Änderungen wird oben auf der Seite angezeigt, wenn eine neue Preisregel gespeichert oder aktualisiert wird. Katalogpreisregeln können planmäßig im Rahmen einer Kampagne angewendet und mit anderen Inhaltsänderungen gruppiert werden. Sie können eine Kampagne auf der Grundlage geplanter Änderungen an einer Preisregel erstellen oder die Änderungen auf eine bestehende Kampagne anwenden.

>[!NOTE]
>
>Alle geplanten Aktualisierungen werden nacheinander angewendet. Das bedeutet, dass jeder Entität nur eine geplante Aktualisierung zu einem bestimmten Zeitpunkt zugewiesen werden kann. Jede geplante Aktualisierung wird auf alle Store-Ansichten innerhalb des Zeitrahmens angewendet. Daher kann eine Entität nicht mehrere geplante Aktualisierungen für verschiedene Store-Ansichten gleichzeitig aufweisen. Alle Entitätsattributwerte in allen Store-Ansichten, die von der aktuellen geplanten Aktualisierung nicht betroffen sind, werden von den Standardwerten übernommen und nicht von der vorherigen geplanten Aktualisierung.

Wenn in derselben Kampagne mehrere Preisregeln ausgeführt werden, bestimmt die Prioritätseinstellung der Preisregel, welche Regel Vorrang hat. Weitere Informationen finden Sie unter [Inhaltstaging](../content-design/content-staging.md).

>[!IMPORTANT]
>
>Wenn eine Kampagne, die eine Preisregel enthält, zunächst ohne Enddatum erstellt wird, kann die Kampagne später nicht so bearbeitet werden, dass ein Enddatum enthalten ist. Es wird empfohlen, entweder beim Erstellen der Kampagne ein Enddatum hinzuzufügen oder eine duplizierte Version der vorhandenen Kampagne zu erstellen und das Enddatum nach Bedarf dem Duplikat hinzuzufügen.

![Katalogpreisregel - Geplante Änderungen](./assets/price-rule-catalog-scheduled.png){width="600" zoomable="yes"}

## Aktualisierung einer Katalogpreisregel planen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**Katalogpreisregel**.

1. Öffnen Sie die Regel im Bearbeitungsmodus.

1. Im **[!UICONTROL Scheduled Changes]** Klicken Sie oben auf der Seite auf **[!UICONTROL Schedule New Update]**.

1. Mit dem **[!UICONTROL Save as a New Update]** die Option aktiviert ist, gehen Sie wie folgt vor:

   - Für **[!UICONTROL Update Name]** Geben Sie einen Namen für die Aktualisierung der Regel ein.

   - Kurzbeschreibung eingeben **[!UICONTROL Description]** der Aktualisierung, einschließlich der Art und Weise und der Gründe ihrer Anwendung.

   - Verwenden Sie die _Kalender_ (![Kalendersymbol](../assets/icon-calendar.png)), um die **[!DNL Start Date]** und **[!UICONTROL End Date]** , damit die geplante Änderung in Kraft tritt. Lassen Sie das Enddatum leer, um eine offene Änderung zu erstellen.

   ![Katalogpreisregeln - Neue geplante Änderungen](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Das Start- und Enddatum/die Endzeit wird durch das Standarddatum/die Standardzeit und die Zeitzone des Admin-Bedienfelds und nicht durch die Zeitzone einer bestimmten Website bestimmt. Beachten Sie die Zeitzone der Website, um die Start- und Endzeiten richtig zu bestimmen. Erstellen Sie separate Regeln für Websites in verschiedenen Zeitzonen, die zu bestimmten lokalen Zeiten beginnen und/oder anhalten müssen.

1. Scrollen Sie nach unten zum **[!UICONTROL Rule Information]** und ändern Sie die Regel nach Bedarf.

   Sie können Änderungen für jeden Regelparameter planen, einschließlich der Websites (Bereich)/Kundengruppen für die Regel, der Bedingungen der Regel und der von der Regel angewendeten Aktionen. Weitere Informationen finden Sie unter [Erstellen einer Katalogpreisregel](price-rules-catalog-create.md).

   >[!NOTE]
   >
   >Wenn Sie zu einem der Regelinformationsparameter wechseln, stellen Sie sicher, dass die Variable _[!UICONTROL Status]_korrekt eingestellt ist. Wenn die Änderung zu einer aktiv angewendeten Regel führen soll, sollte der Status`Active`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

   Die geplante Änderung wird oben auf der Seite mit dem Start- und Enddatum der Kampagne angezeigt.

## Geplante Regeländerung bearbeiten

1. Im **[!UICONTROL Scheduled Changes]** Klicken Sie oben auf der Seite auf **[!UICONTROL View/Edit]**.

1. Nehmen Sie die erforderlichen Änderungen an der geplanten Aktualisierung vor.

1. Klicken **[!UICONTROL Save]**.

## Vorschau der geplanten Regeländerung

1. Im **[!UICONTROL Scheduled Changes]** Klicken Sie oben auf der Seite auf **[!UICONTROL Preview]**.

   Die Vorschau öffnet eine neue Browser-Registerkarte, die Ihre Storefront mit der angewendeten geplanten Änderung lädt. Navigieren Sie zu einem Produkt, das von der Änderung betroffen ist.

   ![Geplante Änderung in der Vorschau anzeigen](./assets/price-rule-catalog-scheduled-update-preview.png){width="600" zoomable="yes"}

1. Klicken Sie in der linken oberen Ecke des Vorschaufensters auf **[!UICONTROL Calendar]**.

   Die Kalenderdetails zeigen andere Kampagnen an, die für denselben Tag geplant sind. Jeder Datensatz in der Liste ist eine separate Regelaktualisierung.

   ![Liste der geplanten Aktualisierungen für ein bestimmtes Datum](./assets/price-rule-catalog-scheduled-preview-calendar.png){width="600" zoomable="yes"}

1. Um eine Vorschau eines anderen Tages oder einer anderen Uhrzeit anzuzeigen, klicken Sie auf das **[!UICONTROL Date & Time]** calendar ![Kalendersymbol](../assets/icon-calendar.png) und gehen Sie wie folgt vor:

   - Wählen Sie ein anderes Datum und/oder eine andere Uhrzeit aus.

   - Klicken **[!UICONTROL Preview]**.

1. Um zum Kalender zurückzukehren, klicken Sie auf **[!UICONTROL Calendar]** in der Kopfzeile der Vorschauseite.

   Von hier aus können Sie Folgendes tun:

   **Link zur Vorschau freigeben**

   Um einen Link zur Store-Vorschau für Ihre Kollegen freizugeben, klicken Sie auf **[!UICONTROL Share]**. Kopieren Sie den Link in die Zwischenablage und fügen Sie ihn in den Nachrichten-Textkörper ein.

   >[!NOTE]
   >
   >Für die Anzeige einer freigegebenen Vorschau ist ein Administratorkonto erforderlich. Wenn [Rolle hat Zugriff](../systems/permissions-user-roles.md) um ein Admin-Benutzerkonto zu erstellen, müssen Sie vor der Freigabe das Konto für einen neuen Benutzer erstellen.

   **Ändern des Umfangs der Vorschau**

   Um geplante Änderungen für verschiedene Store-Ansichten anzuzeigen, klicken Sie auf **[!UICONTROL Scope]** in der Kopfzeile der Vorschauseite. Wählen Sie die Website-, Store- oder Store-Ansicht aus, die Sie in der Vorschau anzeigen möchten.

1. Kehren Sie bei Bedarf zum Kalender zurück und klicken Sie auf **[!UICONTROL View/Edit]** im _[!UICONTROL Action]_um eine weitere geplante Aktualisierung zu öffnen.
