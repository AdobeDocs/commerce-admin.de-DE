---
title: '[!DNL Google Content Experiments]'
description: Erfahren Sie, wie Sie  [!DNL Google Content Experiments]  A/B-Test von Commerce-Produkten, -Kategorien oder -Inhaltsseiten einrichten können.
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

Das folgende Beispiel zeigt, wie Sie mithilfe von Google Analytics-Inhaltsexperimenten einen A/B-Test für Produkte, Kategorien oder Inhaltsseiten einrichten. Es wird empfohlen, zwei Browser-Registerkarten offen zu lassen, während Sie die Anweisungen durcharbeiten, da Sie zwischen dem Commerce-Admin- und Ihrem [!DNL Google Analytics]-Konto hin- und herspringen müssen.

>[!NOTE]
>
>[!DNL Google Content Experiments] ist veraltet und soll durch [Google Optimize&rbrace; ersetzt ](https://support.google.com/optimize/answer/7084762?hl=en).

## Schritt 1. Aktivieren von Inhaltsexperimenten (Commerce)

1. Melden Sie sich beim Administrator Ihrer Commerce-Installation an.

1. Befolgen Sie die Anweisungen zum Aktivieren von [Google Analytics](google-analytics.md) mit Inhaltsexperimenten in der Commerce-Konfiguration.

   ![Verkaufskonfiguration - Google-API - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## Schritt 2. Einrichten der Varianten (Commerce)

Erstellen Sie mehrere Varianten desselben Produkts, derselben Kategorie oder derselben Seite.

- Jede Variante muss über einen eindeutigen [URL-Schlüssel](../catalog/catalog-urls.md) verfügen.
- Für jede Variante muss dieselbe [Store-Ansicht](../getting-started/websites-stores-views.md#scope-settings) ausgewählt sein.

Sie können bis zu zehn Varianten jeder Entität erstellen, die Sie testen möchten. Verwenden Sie für Produkte [Speichern und ](../catalog/product-workspace.md)), um Zeit zu sparen.

## Schritt 3. Einrichten des Experiments (Google)

>[!NOTE]
>
>Sie müssen über die entsprechenden Berechtigungen für das Google-Konto verfügen, um ein Experiment erstellen zu können.

1. Öffnen Sie eine andere Browser-Registerkarte und melden Sie sich bei Ihrem [Google Analytics][2]Konto an.

   Navigieren Sie bei Bedarf zum **[!UICONTROL Account]** und **[!UICONTROL Property]**.

1. Wählen Sie links in der Seitenleiste **[!UICONTROL Admin]** aus und verwenden Sie eine der folgenden Methoden:

   **Methode 1:** Vorhandene Ansicht auswählen

   Klicken Sie in der Kopfzeile der Spalte _[!UICONTROL View]_&#x200B;auf den Abwärtspfeil und wählen Sie die Ansicht aus, die die Daten für das Experiment liefern soll.

   **Methode 2:** Erstellen einer neuen Berichtsansicht

   - Klicken Sie in der Kopfzeile der Spalte _Ansicht_ auf **[!UICONTROL Create View]** und führen Sie folgende Schritte aus:

      - Geben Sie den Experimentspeicherort entweder als `Website` oder `Mobile app` an.

      - Geben Sie einen beschreibenden **[!UICONTROL Reporting View Name]** ein.

      - Geben Sie die **[!UICONTROL Reporting Time Zone]** an.

   - Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Create View]** und dann auf den Rückwärtspfeil, um zur vorherigen Seite zurückzukehren.

1. Wählen Sie im linken Bedienfeld unter _[!UICONTROL Reports]_&#x200B;die Option **[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**&#x200B;aus.

1. Klicken Sie auf **[!UICONTROL Create experiment]** und führen Sie folgende Schritte aus:

   - Geben Sie den Prozentsatz des umzuleitenden Traffics an.

   - Geben Sie die **[!UICONTROL Original Page URL]** und URLs jedes **[!UICONTROL page variation]** an, den Sie testen möchten.

   - Füllen Sie die anderen Optionen aus.

1. Wenn das Experiment eingerichtet ist, klicken Sie auf **[!UICONTROL Manually Insert the Code]** und kopieren Sie das Code-Fragment.

## Schritt 4. Einfügen eines Codeausschnitts (Commerce)

1. Kehren Sie zum Administrator Ihrer Commerce-Installation zurück und öffnen Sie die Originalversion des Produkts, der Kategorie oder der Seite im Bearbeitungsmodus.

1. Erweitern Sie den Abschnitt **[!UICONTROL View Optimization]** für das Produkt, die Kategorie oder die Seite.

1. Fügen Sie den von Google Analytics kopierten Codeausschnitt in das Textfeld **[!UICONTROL Experiment Code]** ein.

   >[!NOTE]
   >
   >Fügen Sie den Code-Ausschnitt in keine der Varianten ein.

   ![Optimierung der Produktansicht](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

## Schritt 5: Experiment überprüfen und starten (Google)

1. Kehren Sie zu Ihrem [Google Analytics][2]Konto zurück.

1. Überprüfen Sie die Experimenteinstellungen.

1. Wenn Sie bereit sind, klicken Sie auf **[!UICONTROL Start Experiment]**.

   Klicken Sie andernfalls auf **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
