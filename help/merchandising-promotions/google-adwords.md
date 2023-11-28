---
title: Google AdWords
description: Erfahren Sie, wie Sie Ihren Commerce Store für das Google AdWords-Konversions-Tracking konfigurieren, um die Anzeigenklicks zu messen, die zu einem Verkauf oder einer anderen wertvollen Aktion führen.
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---

# Google AdWords

[Google AdWords][1] ist ein Dienst, mit dem Sie Anzeigen in Google-Suchergebnissen und auf den Seiten von Unternehmen im Google Display Network platzieren können. Das AdWords-Dashboard enthält Tools zum Verwalten Ihrer Kampagnen, zum Verfolgen der Antwort und zum Messen der Ergebnisse.

Das Konversions-Tracking zeigt die Anzahl der Anzeigenklicks an, die zu einem Verkauf oder einer anderen wertvollen Aktion führen. Die _Erfolg_ -Seite, die Ihrem Kunden angezeigt wird, nachdem eine Bestellung eingereicht wurde, wird verwendet, um Konversionen zu verfolgen, da sie erst nach einem Verkauf angezeigt wird. Nachdem Sie die Google AdWords-Konfiguration für Ihren Store abgeschlossen haben, müssen Sie das Konversions-Tracking-Skript nicht auf die Erfolgsseite kopieren, da Commerce bereits über die erforderlichen Informationen verfügt. Weitere Informationen finden Sie unter [Hilfe zu Google AdWords][2].

![Adobe Ad in Google Search Results](./assets/google-adwords-adobe-ad.png){width="500"}

## Schritt 1. Erstellen einer Google AdWords-Kampagne

1. Besuch [Google AdWords][3]und melden Sie sich für ein Konto an.

1. Befolgen Sie die Anweisungen zum Erstellen einer Kampagne.

1. Gehen Sie wie folgt vor, um das Konversions-Tracking für Ihre Kampagne einzurichten:

   - Im **[!UICONTROL Tools]** in Ihrem AdWords-Dashboard auswählen **[!UICONTROL Conversions]** und klicken **[!UICONTROL Conversion]**.

   - Wenn Sie nach der Konvertierungsquelle gefragt werden, wählen Sie **[!UICONTROL Website]**.

   - Geben Sie einen Namen für die Konvertierungsaktion ein, die Sie verfolgen möchten, und klicken Sie auf **[!UICONTROL Done]**.

   - Klicks **[!UICONTROL Value]** und, falls zutreffend, der Konversion einen Wert zuweisen. Beispiel:

      - Wenn Sie 5 USD für jeden Verkauf verdienen, wählen Sie `Each time it happens` und weisen Sie den Wert `$5`.
      - Wenn der Wert jedes Verkaufs variiert, lassen Sie den Wert leer.

     Klicken Sie zum Abschließen auf **[!UICONTROL Done]**.

   - Klicks **[!UICONTROL Conversion windows]** und die Einstellungen vervollständigen, um zu bestimmen, wie lange die Konversionen verfolgt werden sollen, die Berichtskategorie und das Attributionsmodell.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save and Continue]**.

## Schritt 2. Konversions-Tag abrufen

1. under **[!UICONTROL Install your tag]**, wählen Sie aus, Konversionen auf **[!UICONTROL Page load]**.

1. Als Option können Sie die **[!UICONTROL Google Site Stats]** Benachrichtigung zur Konversionsseite.

   Die Benachrichtigung wird in der unteren Ecke mit einem Link zu den Sicherheitsstandards und der Cookie-Nutzung von Google angezeigt.

1. Führen Sie einen der folgenden Schritte aus, um festzulegen, wie Sie Ihr AdWords-Tag verwalten möchten:

   - Wenn Sie das Skript Ihrem Store selbst hinzufügen möchten, wählen Sie **[!UICONTROL Save instructions and tag]**.
   - Wenn Sie möchten, dass jemand anderes das Skript zu Ihrem Store hinzufügt, wählen Sie **[!UICONTROL Email instructions and tag]**.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Done]**.

## Schritt 3. Konfigurieren des Stores

{{gtag-api-note}}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wenn Sie Google AdWords für eine bestimmte Store-Ansicht konfigurieren, gehen Sie wie folgt vor:

   - Wählen Sie links oben die **[!UICONTROL Store View]** zu konfigurieren ist.

   - Wenn Sie aufgefordert werden, den Perimeterwechsel zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Google API]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Google AdWords]** und führen Sie folgende Schritte aus:

   - Satz **[!UICONTROL Enable]** nach `Yes`.

   - Geben Sie die **[!UICONTROL Conversion ID]** aus Ihrem Google AdWords-Skript.

   ![Vertriebskonfiguration - Google Ads-API](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. Gehen Sie wie folgt vor, um die Google Sites-Statusbenachrichtigung zu formatieren:

   - Satz **[!UICONTROL Conversion Language]** in der Sprache, die im Google AdWords-Skript angegeben ist.

   - Geben Sie die **[!UICONTROL Conversion Format]** wird für die Google Sites-Statusbenachrichtigung auf der Konversionsseite verwendet.

      - `1`  - Zeigt eine einzeilige Benachrichtigung mit einem Link zu weiteren Informationen zum Google-Tracking an.
      - `2` - Zeigt eine zweizeilige Benachrichtigung mit einem Link zu weiteren Informationen zum Google-Tracking an.
      - `3` - Zeigt keine Kundenbenachrichtigung an.

   - Geben Sie die [Hexadezimalcode][4]{:target=&quot;_blank&quot;} für die **[!UICONTROL Conversion Color]** , die Sie für die Beschriftung der Google Site Stats-Benachrichtigung verwenden möchten.

   - Geben Sie den verschlüsselten Text für die **[!UICONTROL Conversion Label]** wird in der Google Sites-Statusbenachrichtigung angezeigt.

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

1. Satz **[!UICONTROL Conversion Value Type]** auf einen der folgenden Werte zu:

   - `Dynamic` - Stellt fest, dass eine Konversion basierend auf dem dynamischen Wert des Bestellbetrags stattgefunden hat.
   - `Constant` - Stellt fest, dass eine Konversion anhand eines angegebenen Werts stattgefunden hat.

   Für _Konstante_ Konversionswerttyp, geben Sie einen bestimmten **[!UICONTROL Value]** für die _[!UICONTROL Order Amount]_, um als Konversion zu qualifizieren.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Schritt 4. Überprüfen der Konfiguration

Innerhalb weniger Stunden ändert sich der Tracking-Status in Ihrem Google AdWords-Dashboard von `Unverified` nach `No recent conversions` oder `Recording conversions`. Wenn jemand auf Ihre Anzeige klickt und einen Kauf tätigt, wird die Konversion auf der Seite Konversionsaktionen Ihres Dashboards und Kampagnenberichts angezeigt.

[1]: https://www.google.com/adwords/
[2]: https://support.google.com/adwords/answer/6095821
[3]: https://ads.google.com/
[4]: https://www.w3schools.com/colors/colors_picker.asp
