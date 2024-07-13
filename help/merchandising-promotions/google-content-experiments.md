---
title: '[!DNL Google Content Experiments]'
description: Erfahren Sie, wie Sie mit [!DNL Google Content Experiments] einen A/B-Test für Commerce-Produkte, -Kategorien oder -Inhaltsseiten einrichten.
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

Das folgende Beispiel zeigt, wie Sie einen A/B-Test für Produkte, Kategorien oder Inhaltsseiten mit Google Analytics Content Experiments einrichten. Es wird empfohlen, bei der Bearbeitung der Anweisungen zwei Browser-Registerkarten offen zu halten, da Sie zwischen dem Commerce-Administrator und Ihrem [!DNL Google Analytics]-Konto hin- und herspringen müssen.

>[!NOTE]
>
>[!DNL Google Content Experiments] ist veraltet und wird für die Ersetzung durch [Google Optimize](https://support.google.com/optimize/answer/7084762?hl=en) geplant.

## Schritt 1. Aktivieren von Inhaltsexperimenten (Commerce)

1. Melden Sie sich beim Administrator Ihrer Commerce-Installation an.

1. Befolgen Sie die Anweisungen zum Aktivieren von [Google Analytics](google-analytics.md) mit Inhaltsexperimenten in der Commerce-Konfiguration.

   ![Vertriebskonfiguration - Google-API - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## Schritt 2. Einrichten der Varianten (Commerce)

Erstellen Sie mehrere Varianten desselben Produkts, derselben Kategorie oder derselben Seite.

- Jede Variante muss über einen eindeutigen [URL-Schlüssel](../catalog/catalog-urls.md) verfügen.
- Für jede Variante muss dieselbe [Store-Ansicht](../getting-started/websites-stores-views.md#scope-settings) ausgewählt sein.

Sie können bis zu zehn Varianten jeder Entität erstellen, die Sie testen möchten. Verwenden Sie für Produkte [Speichern und Duplizieren](../catalog/product-workspace.md) , um Zeit zu sparen.

## Schritt 3. Einrichten des Experiments (Google)

>[!NOTE]
>
>Sie müssen über die entsprechenden Berechtigungen für das Google-Konto verfügen, um ein Experiment zu erstellen.

1. Öffnen Sie eine andere Browser-Registerkarte und melden Sie sich bei Ihrem [Google Analytics][2] -Konto an.

   Navigieren Sie nötigenfalls zu den **[!UICONTROL Account]** und **[!UICONTROL Property]**.

1. Wählen Sie links in der Seitenleiste **[!UICONTROL Admin]** aus und verwenden Sie eine der folgenden Methoden:

   **Methode 1:** Vorhandene Ansicht auswählen

   Klicken Sie in der Kopfzeile der Spalte _[!UICONTROL View]_auf den Pfeil nach unten und wählen Sie die Ansicht aus, die die Daten für das Experiment bereitstellen soll.

   **Methode 2:** Neue Berichtsansicht erstellen

   - Klicken Sie in der Kopfzeile der Spalte _Ansicht_ auf **[!UICONTROL Create View]** und führen Sie die folgenden Schritte aus:

      - Identifizieren Sie den Experimentspeicherort entweder als `Website` oder als `Mobile app`.

      - Geben Sie eine beschreibende **[!UICONTROL Reporting View Name]** ein.

      - Geben Sie den Wert **[!UICONTROL Reporting Time Zone]** an.

   - Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Create View]** und dann auf den Pfeil nach hinten , um zur vorherigen Seite zurückzukehren.

1. Wählen Sie im linken Bereich unter _[!UICONTROL Reports]_**[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**aus.

1. Klicken Sie auf **[!UICONTROL Create experiment]** und führen Sie die folgenden Schritte aus:

   - Geben Sie den Prozentsatz des zu umgeleiteten Traffics an.

   - Geben Sie die **[!UICONTROL Original Page URL]** und die URLs jeder **[!UICONTROL page variation]** an, die Sie testen möchten.

   - Füllen Sie die anderen Optionen aus.

1. Wenn das Experiment eingerichtet ist, klicken Sie auf **[!UICONTROL Manually Insert the Code]** und kopieren Sie das Codefragment.

## Schritt 4. Codefragment einfügen (Commerce)

1. Kehren Sie zum Administrator Ihrer Commerce-Installation zurück und öffnen Sie die Originalversion des Produkts, der Kategorie oder der Seite im Bearbeitungsmodus.

1. Erweitern Sie den Abschnitt **[!UICONTROL View Optimization]** für das Produkt, die Kategorie oder die Seite.

1. Fügen Sie das Codefragment, das Sie aus Google Analytics kopiert haben, in das Textfeld **[!UICONTROL Experiment Code]** ein.

   >[!NOTE]
   >
   >Fügen Sie das Codefragment nicht in eine der Varianten ein.

   ![Optimierung der Produktansicht](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

## Schritt 5: Experiment überprüfen und starten (Google)

1. Kehren Sie zu Ihrem [Google Analytics][2] -Konto zurück.

1. Überprüfen Sie die Experimenteinstellungen.

1. Wenn Sie bereit sind zu beginnen, klicken Sie auf **[!UICONTROL Start Experiment]**.

   Klicken Sie andernfalls auf **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
