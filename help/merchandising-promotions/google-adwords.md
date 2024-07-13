---
title: Google AdWords
description: Erfahren Sie, wie Sie Ihren Commerce Store für das Google AdWords-Konversions-Tracking konfigurieren, um die Anzeigenklicks zu messen, die zu einem Kauf oder einer anderen wertvollen Aktion führen.
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Google AdWords

[Google AdWords][1] ist ein Dienst, mit dem Sie Anzeigen in Google-Suchergebnissen und auf den Seiten von Unternehmen im Google Display Network platzieren können. Das AdWords-Dashboard enthält Tools zum Verwalten Ihrer Kampagnen, zum Verfolgen der Antwort und zum Messen der Ergebnisse.

Das Konversions-Tracking zeigt die Anzahl der Anzeigenklicks an, die zu einem Verkauf oder einer anderen wertvollen Aktion führen. Die Seite _Erfolg_ , die Ihrem Kunden angezeigt wird, nachdem eine Bestellung gesendet wurde, wird zum Verfolgen von Konversionen verwendet, da sie erst nach einem Kauf angezeigt wird. Nachdem Sie die Google AdWords-Konfiguration für Ihren Store abgeschlossen haben, müssen Sie das Konversions-Tracking-Skript nicht auf die Erfolgsseite kopieren, da Commerce bereits über die erforderlichen Informationen verfügt. Weitere Informationen finden Sie unter [Hilfe zu Google AdWords][2].

![Adobe Ad in Google Search Results](./assets/google-adwords-adobe-ad.png){width="500"}

## Schritt 1. Erstellen einer Google AdWords-Kampagne

1. Besuchen Sie [Google AdWords][3] und melden Sie sich für ein Konto an.

1. Befolgen Sie die Anweisungen zum Erstellen einer Kampagne.

1. Gehen Sie wie folgt vor, um das Konversions-Tracking für Ihre Kampagne einzurichten:

   - Wählen Sie auf der Registerkarte **[!UICONTROL Tools]** Ihres AdWords-Dashboards **[!UICONTROL Conversions]** und klicken Sie auf **[!UICONTROL Conversion]**.

   - Wenn Sie nach der Konversionsquelle gefragt werden, wählen Sie **[!UICONTROL Website]**.

   - Geben Sie einen Namen für die Konversionsaktion ein, die Sie verfolgen möchten, und klicken Sie auf **[!UICONTROL Done]**.

   - Klicken Sie auf **[!UICONTROL Value]** und weisen Sie der Konversion ggf. einen Wert zu. Beispiel:

      - Wenn Sie bei jedem Kauf 5 USD verdienen, wählen Sie &quot;`Each time it happens`&quot;und weisen Sie den Wert &quot;`$5`&quot;zu.
      - Wenn der Wert jedes Verkaufs variiert, lassen Sie den Wert leer.

     Klicken Sie abschließend auf **[!UICONTROL Done]**.

   - Klicken Sie auf &quot;**[!UICONTROL Conversion windows]**&quot;und nehmen Sie die Einstellungen vor, um zu bestimmen, wie lange die Konversionen verfolgt werden sollen, sowie die Berichtskategorie und das Attributionsmodell.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save and Continue]**.

## Schritt 2. Konversions-Tag abrufen

1. Wählen Sie unter **[!UICONTROL Install your tag]** aus, die Konversionen auf **[!UICONTROL Page load]** zu zählen.

1. Als Option können Sie die Benachrichtigung **[!UICONTROL Google Site Stats]** zur Konvertierungsseite hinzufügen.

   Die Benachrichtigung wird in der unteren Ecke mit einem Link zu den Sicherheitsstandards und der Cookie-Nutzung von Google angezeigt.

1. Führen Sie einen der folgenden Schritte aus, um festzulegen, wie Sie Ihr AdWords-Tag verwalten möchten:

   - Wenn Sie das Skript Ihrem Store selbst hinzufügen möchten, wählen Sie **[!UICONTROL Save instructions and tag]**.
   - Wenn Sie planen, dass jemand anderes das Skript zu Ihrem Store hinzufügt, wählen Sie **[!UICONTROL Email instructions and tag]**.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Done]**.

## Schritt 3. Konfigurieren des Stores

{{gtag-api-note}}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wenn Sie Google AdWords für eine bestimmte Store-Ansicht konfigurieren, gehen Sie wie folgt vor:

   - Wählen Sie in der linken oberen Ecke die zu konfigurierenden **[!UICONTROL Store View]** aus.

   - Wenn Sie aufgefordert werden, den Perimeterwechsel zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Google API]** aus.

1. Erweitern Sie den Abschnitt **[!UICONTROL Google AdWords]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   - Setzen Sie **[!UICONTROL Enable]** auf `Yes`.

   - Geben Sie den Wert **[!UICONTROL Conversion ID]** aus Ihrem Google AdWords-Skript ein.

   ![Vertriebskonfiguration - Google Ads-API](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. Gehen Sie wie folgt vor, um die Google Sites-Statusbenachrichtigung zu formatieren:

   - Setzen Sie **[!UICONTROL Conversion Language]** auf die Sprache, die im Google AdWords-Skript angegeben ist.

   - Geben Sie die **[!UICONTROL Conversion Format]** ein, die für die Google Sites-Statusbenachrichtigung auf der Konversionsseite verwendet werden soll.

      - `1` - Zeigt eine einzeilige Benachrichtigung mit einem Link zu weiteren Informationen zum Google-Tracking an.
      - `2` - Zeigt eine zweizeilige Benachrichtigung mit einem Link zu weiteren Informationen zum Google-Tracking an.
      - `3` - Zeigt keine Kundenbenachrichtigung an.

   - Geben Sie den [hexadezimalen Code][4]{:target=&quot;_blank&quot;} für den **[!UICONTROL Conversion Color]** ein, den Sie für die Benachrichtigungsbeschriftung zu Google Site Stats verwenden möchten.

   - Geben Sie den verschlüsselten Text für die **[!UICONTROL Conversion Label]** ein, die in der Google Sites-Statusbenachrichtigung angezeigt wird.

     Beispiel: `MlEYCOKBnGoQz6CZoAM`

     **Beispiel für Google AdWords-Tag-Code**

     ```html
     <!-- Google Code for Back to School Sale Conversion Page -->
     <script type="text/javascript">
     /* <![CDATA[ */
     var google_conversion_id = 999999999;
     var google_conversion_language = "en";
     var google_conversion_format = "3";
     var google_conversion_color = "ffffff";
     var google_conversion_label = "MlEYCOKBnGoQz6CZoAM";
     var google_remarketing_only = false;
     /* ]]> */
     </script>
     
     <script type="text/javascript" src="//www.googleadservices.com/pagead/conversion.js">
     </script>
     <noscript>
     <div style="display:inline;">
     <img height="1" width="1" style="border-style:none;" alt="" src="//www.googleadservices.com/pagead/conversion/872829007/?label=MlEYCOKBnGoQz6CZoAM&amp;guid=ON&amp;script=0"/>
     
     </noscript>
     ```

1. Setzen Sie **[!UICONTROL Conversion Value Type]** auf einen der folgenden Werte:

   - `Dynamic` - Stellt fest, dass eine Konversion basierend auf dem dynamischen Wert des Bestellbetrags stattgefunden hat.
   - `Constant` - Stellt fest, dass eine Konversion anhand eines angegebenen Werts stattgefunden hat.

   Geben Sie für den Konversionswerttyp _Konstante_ einen bestimmten **[!UICONTROL Value]** für den Wert _[!UICONTROL Order Amount]_ein, der als Konversion qualifiziert werden soll.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Schritt 4. Überprüfen der Konfiguration

Innerhalb weniger Stunden ändert sich der Tracking-Status in Ihrem Google AdWords-Dashboard von `Unverified` in `No recent conversions` oder `Recording conversions`. Wenn jemand auf Ihre Anzeige klickt und einen Kauf tätigt, wird die Konversion auf der Seite Konversionsaktionen Ihres Dashboards und Kampagnenberichts angezeigt.

[1]: https://www.google.com/adwords/
[2]: https://support.google.com/adwords/answer/6095821
[3]: https://ads.google.com/
[4]: https://www.w3schools.com/colors/colors_picker.asp
