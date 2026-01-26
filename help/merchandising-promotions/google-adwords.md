---
title: Google AdWords
description: Erfahren Sie, wie Sie Ihren Commerce Store für das Google AdWords-Konversionstracking konfigurieren, um die Anzeigenklicks zu messen, die zu einem Verkauf oder einer anderen nützlichen Aktion führen.
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Google AdWords

[Google AdWords](https://www.google.com/adwords/) ist ein Service, mit dem Sie Anzeigen in Google-Suchergebnissen und auf den Seiten von Unternehmen im Google Display Network platzieren können. Das AdWords-Dashboard enthält Tools zur Verwaltung Ihrer Kampagnen, zur Nachverfolgung von Antworten und zur Messung von Ergebnissen.

Das Konversions-Tracking zeigt die Anzahl der Anzeigenklicks an, die zu einem Verkauf oder einer anderen wertvollen Aktion führen. Die _Erfolg_-Seite, die Ihrem Kunden nach der Übermittlung einer Bestellung angezeigt wird, wird verwendet, um Konversionen zu verfolgen, da sie nur nach einem Verkauf angezeigt wird. Nach Abschluss der Google AdWords-Konfiguration für Ihren Store müssen Sie das Konversionsverfolgungs-Skript nicht auf die Erfolgsseite kopieren, da Commerce bereits über die erforderlichen Informationen verfügt. Weitere Informationen finden Sie in der [Google AdWords-Hilfe](https://support.google.com/adwords/answer/6095821).

![Adobe-Anzeige in Google-Suchergebnissen](./assets/google-adwords-adobe-ad.png){width="500"}

## Schritt 1. Erstellen einer Google AdWords-Kampagne

1. Besuchen Sie [Google AdWords](https://ads.google.com/) und melden Sie sich für ein Konto an.

1. Befolgen Sie die Anweisungen zum Erstellen einer Kampagne.

1. Gehen Sie wie folgt vor, um das Konversionstracking für Ihre Kampagne einzurichten:

   - Wählen Sie auf der Registerkarte **[!UICONTROL Tools]** Ihres AdWords-Dashboards **[!UICONTROL Conversions]** aus und klicken Sie auf **[!UICONTROL Conversion]**.

   - Wenn Sie nach der Konvertierungsquelle gefragt werden, wählen Sie **[!UICONTROL Website]**.

   - Geben Sie einen Namen für die Konversionsaktion ein, die Sie verfolgen möchten, und klicken Sie auf **[!UICONTROL Done]**.

   - Klicken Sie auf **[!UICONTROL Value]** und weisen Sie der Konvertierung ggf. einen Wert zu. Beispiel:

      - Wenn Sie für jeden Verkauf 5 $ verdienen, wählen Sie `Each time it happens` und weisen Sie einen Wert von `$5` zu.
      - Wenn der Wert jedes Verkaufs variiert, lassen Sie den Wert leer.

     Klicken Sie zum Abschluss auf **[!UICONTROL Done]**.

   - Klicken Sie auf **[!UICONTROL Conversion windows]** und schließen Sie die Einstellungen ab, um zu bestimmen, wie lange die Konversionen verfolgt werden sollen, sowie die Berichtskategorie und das Attributionsmodell.

1. Klicken Sie abschließend auf **[!UICONTROL Save and Continue]**.

## Schritt 2. Konversions-Tag abrufen

1. Wählen Sie unter **[!UICONTROL Install your tag]** die Option zum Zählen von Konversionen auf **[!UICONTROL Page load]** aus.

1. Als Option können Sie die **[!UICONTROL Google Site Stats]**-Benachrichtigung zur Konversionsseite hinzufügen.

   Die Benachrichtigung wird in der unteren Ecke mit einem Link zu den Sicherheitsstandards von Google und zur Verwendung von Cookies angezeigt.

1. Um zu entscheiden, wie Sie Ihr AdWords-Tag verwalten möchten, führen Sie einen der folgenden Schritte aus:

   - Wenn Sie das Skript selbst zu Ihrem Store hinzufügen möchten, wählen Sie **[!UICONTROL Save instructions and tag]**.
   - Wenn Sie beabsichtigen, das Skript von einer anderen Person zu Ihrem Store hinzufügen zu lassen, wählen Sie **[!UICONTROL Email instructions and tag]** aus.

1. Klicken Sie abschließend auf **[!UICONTROL Done]**.

## Schritt 3. Konfigurieren des Stores

{{gtag-api-note}}

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Gehen Sie wie folgt vor, um Google AdWords für eine bestimmte Store-Ansicht zu konfigurieren:

   - Wählen Sie in der oberen linken Ecke die **[!UICONTROL Store View]** aus, die konfiguriert werden soll.

   - Wenn Sie zum Bestätigen des Bereichswechsels aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Google API]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Google AdWords]** und führen Sie folgende Schritte aus:

   - Legen Sie **[!UICONTROL Enable]** auf `Yes` fest.

   - Geben Sie die **[!UICONTROL Conversion ID]** aus Ihrem Google AdWords-Skript ein.

   ![Verkaufskonfiguration - Google Ads-API](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. Gehen Sie wie folgt vor, um die Google Sites-Startbenachrichtigung zu formatieren:

   - Legen Sie **[!UICONTROL Conversion Language]** auf die Sprache fest, die in Ihrem Google AdWords-Skript identifiziert ist.

   - Geben Sie die **[!UICONTROL Conversion Format]** ein, die für die Google Sites-Statusbenachrichtigung auf der Konversionsseite verwendet werden soll.

      - `1` - Zeigt eine einzeilige Benachrichtigung mit einem Link zu weiteren Informationen zum Google-Tracking an.
      - `2` - Zeigt eine zweizeilige Benachrichtigung mit einem Link zu weiteren Informationen zum Google-Tracking an.
      - `3` - Zeigt keine Kundenbenachrichtigung an.

   - Geben Sie den [Hexadezimalcode](https://www.w3schools.com/colors/colors_picker.asp){:target="_blank"} für die **[!UICONTROL Conversion Color]** ein, die Sie für die Google Site Stats Notification Label verwenden möchten.

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

1. Legen Sie **[!UICONTROL Conversion Value Type]** auf eine der folgenden Einstellungen fest:

   - `Dynamic` - Bestimmt anhand des dynamischen Bestellbetragswerts, ob eine Konversion stattgefunden hat.
   - `Constant` - Bestimmt anhand eines bestimmten eingegebenen Werts, dass eine Konversion stattgefunden hat.

   Geben _für den_ „Konstante“ einen bestimmten **[!UICONTROL Value]** ein, damit die _[!UICONTROL Order Amount]_&#x200B;als Konversion gilt.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Schritt 4. Konfiguration überprüfen

Innerhalb weniger Stunden ändert sich der Tracking-Status in Ihrem Google AdWords-Dashboard von `Unverified` zu `No recent conversions` oder `Recording conversions`. Wenn jemand auf Ihre Anzeige klickt und einen Kauf tätigt, wird die Konversion auf der Seite „Konversionsaktionen“ im Dashboard und Kampagnenbericht angezeigt.
