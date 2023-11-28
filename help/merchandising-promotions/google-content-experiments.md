---
title: '[!DNL Google Content Experiments]'
description: Verwendung von [!DNL Google Content Experiments] , um einen A/B-Test für Commerce-Produkte, -Kategorien oder Inhaltsseiten einzurichten.
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

Das folgende Beispiel zeigt, wie Sie einen A/B-Test für Produkte, Kategorien oder Inhaltsseiten mit Google Analytics Content Experiments einrichten. Es wird empfohlen, zwei Browser-Registerkarten offen zu halten, während Sie die Anweisungen durchlaufen, da Sie zwischen dem Commerce-Administrator und Ihrem [!DNL Google Analytics] -Konto.

>[!NOTE]
>
>[!DNL Google Content Experiments] ist veraltet und wird für den Austausch durch [Google Optimize](https://support.google.com/optimize/answer/7084762?hl=en).

## Schritt 1. Aktivieren von Inhaltsexperimenten (Commerce)

1. Melden Sie sich beim Administrator Ihrer Commerce-Installation an.

1. Befolgen Sie die Anweisungen zum Aktivieren von [Google Analytics](google-analytics.md) mit Inhaltstests in der Commerce-Konfiguration.

   ![Vertriebskonfiguration - Google-API - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## Schritt 2. Einrichten der Varianten (Commerce)

Erstellen Sie mehrere Varianten desselben Produkts, derselben Kategorie oder derselben Seite.

- Jede Variante muss eine eindeutige [URL-Schlüssel](../catalog/catalog-urls.md).
- Jede Variante muss denselben [Store-Ansicht](../getting-started/websites-stores-views.md#scope-settings) ausgewählt ist.

Sie können bis zu zehn Varianten jeder Entität erstellen, die Sie testen möchten. Für Produkte verwenden Sie [Speichern und duplizieren](../catalog/product-workspace.md) um Zeit zu sparen.

## Schritt 3. Einrichten des Experiments (Google)

>[!NOTE]
>
>Sie müssen über die entsprechenden Berechtigungen für das Google-Konto verfügen, um ein Experiment zu erstellen.

1. Öffnen Sie eine andere Browser-Registerkarte und melden Sie sich bei Ihrem [Google Analytics][2] -Konto.

   Navigieren Sie bei Bedarf zum **[!UICONTROL Account]** und **[!UICONTROL Property]**.

1. Wählen Sie in der Seitenleiste auf der linken Seite **[!UICONTROL Admin]** und eine der folgenden Methoden verwenden:

   **Methode 1:** Vorhandene Ansicht auswählen

   In der Kopfzeile der _[!UICONTROL View]_klicken Sie auf den Abwärtspfeil und wählen Sie die Ansicht aus, die die Daten für das Experiment bereitstellen soll.

   **Methode 2:** Neue Berichtsansicht erstellen

   - In der Kopfzeile der _Ansicht_ Spalte, klicken **[!UICONTROL Create View]** und gehen Sie wie folgt vor:

      - Identifizieren Sie den Experimentort als `Website` oder `Mobile app`.

      - Beschreibende Eingabe **[!UICONTROL Reporting View Name]**.

      - Geben Sie die **[!UICONTROL Reporting Time Zone]**.

   - Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Create View]** und klicken Sie dann auf den Pfeil nach hinten , um zur vorherigen Seite zurückzukehren.

1. Im linken Bereich unter _[!UICONTROL Reports]_auswählen **[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**.

1. Klicks **[!UICONTROL Create experiment]** und gehen Sie wie folgt vor:

   - Geben Sie den Prozentsatz des zu umgeleiteten Traffics an.

   - Geben Sie die **[!UICONTROL Original Page URL]** und die URLs jedes **[!UICONTROL page variation]** die Sie testen möchten.

   - Füllen Sie die anderen Optionen aus.

1. Klicken Sie nach der Einrichtung des Experiments auf **[!UICONTROL Manually Insert the Code]** und kopieren Sie das Codefragment.

## Schritt 4. Codefragment einfügen (Commerce)

1. Kehren Sie zum Administrator Ihrer Commerce-Installation zurück und öffnen Sie die Originalversion des Produkts, der Kategorie oder der Seite im Bearbeitungsmodus.

1. Erweitern Sie die **[!UICONTROL View Optimization]** für das Produkt, die Kategorie oder die Seite.

1. Fügen Sie das Codefragment, das Sie aus Google Analytics kopiert haben, in die **[!UICONTROL Experiment Code]** Textfeld.

   >[!NOTE]
   >
   >Fügen Sie das Codefragment nicht in eine der Varianten ein.

   ![Optimierung der Produktansicht](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

## Schritt 5: Experiment überprüfen und starten (Google)

1. Kehren Sie zu Ihrem [Google Analytics][2] -Konto.

1. Überprüfen Sie die Experimenteinstellungen.

1. Wenn Sie bereit zum Starten sind, klicken Sie auf **[!UICONTROL Start Experiment]**.

   Klicken Sie andernfalls auf **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
