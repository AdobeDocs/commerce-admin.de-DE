---
title: Währungskonfiguration
description: Erfahren Sie, wie Sie den Umfang der Basiswährung festlegen und die Währungen angeben, die Sie akzeptieren, sowie die Währung, die Sie für die Preisanzeige verwenden möchten.
exl-id: ba78095f-36eb-4e38-a6e8-72d85e0cf980
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# Währungskonfiguration

Bevor Sie individuelle Währungskurse einrichten, müssen Sie zunächst den Umfang der [Basiswährung“ &#x200B;](../configuration-reference/general/currency-setup.md). Sie ist standardmäßig als global festgelegt, wodurch die Einstellung der Basiswährung auf die gesamte [Store-Hierarchie“ angewendet &#x200B;](../getting-started/websites-stores-views.md). Wenn Sie eine Adobe Commerce- oder Magento Open Source-Installation für mehrere Sites haben, können Sie mehrere Basiswährungen verwalten, indem Sie den Umfang auf die Website-Ebene festlegen.

Außerdem geben Sie die Währungen an, die Sie akzeptieren, und welche Währung Sie für die Anzeige von [Preisen](../catalog/catalog-price-scope.md) in Ihrem Geschäft verwenden möchten. Im folgenden Diagramm wird der Umfang der Basiswährung auf Website-Ebene festgelegt, sodass jede Website eine andere Basiswährung haben kann.

![Diagramm zum Währungsumfang](./assets/scope-currency-config.svg){width="600" zoomable="yes"}

## Schritt 1: Akzeptierte Währungen auswählen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Setzen Sie **[!UICONTROL Scope]** in der oberen linken Ecke auf die Store-Ansicht, für die die Konfiguration gilt.

1. Wählen Sie im linken Bedienfeld unter _Allgemein_ die Option **[!UICONTROL Currency Setup]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Currency Options]** und legen Sie die folgenden Optionen fest:

   - **[!UICONTROL Base Currency]** - Legen Sie die primäre Währung fest, die Sie für Online-Transaktionen verwenden.

   - **[!UICONTROL Default Display Currency]** - Legen Sie dies auf die Währung fest, mit der Sie die Preise in der Store-Ansicht anzeigen.

   - **[!UICONTROL Allowed Currencies]** - Wählen Sie in der Store-Ansicht alle Währungen aus, die Sie als Zahlung akzeptieren. Stellen Sie sicher, dass Sie auch Ihre primäre Währung auswählen.

     Halten Sie bei mehreren Währungen die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

   ![Allgemeine Konfiguration - Währungsoptionen](../configuration-reference/general/assets/currency-setup-currency-options.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung jeder dieser Konfigurationseinstellungen finden Sie unter [Währungsoptionen](../configuration-reference/general/currency-setup.md) im _Konfigurationsreferenzhandbuch_.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren _klicken Sie auf_ Schließen![&#x200B; ( Feld schließen](../assets/icon-close-x.png) ) in der rechten oberen Ecke der Systemmeldung.

   Sie können [den Cache aktualisieren](../systems/cache-management.md) später.

1. Definieren Sie den Umfang der Basiswährung:

   - Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie darunter **[!UICONTROL Catalog]**.

   - Scrollen Sie nach unten und erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Price]** . (Dieser Abschnitt wird nur angezeigt, wenn der Bereich als **[!UICONTROL Store View:]** (_)_ ist.

   - Legen Sie **[!UICONTROL Catalog Price Scope]** entweder auf `Global` oder auf `Website` fest.

   ![Katalogkonfiguration - Preisoptionen](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

## Schritt 2: Konfigurieren der Importverbindung

1. Scrollen Sie nach oben auf der Seite.

1. Erweitern Sie im linken Bereich **[!UICONTROL General]** und wählen Sie **[!UICONTROL Currency Setup]**.

1. Konfigurieren Sie Ihre Währungs-Service-Verbindung:

   Es gibt drei Service-Optionen: _[!UICONTROL Fixer.io (legacy)]_,_[!UICONTROL Fixer Api (APILayer)]_ und _[!UICONTROL Currency Converter API]_

   >[!IMPORTANT]
   >
   >Ab Version 2.4.6 wird der [[!DNL Fixer.io]](https://fixer.io/)-Service nicht mehr unterstützt und durch den Service [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) ersetzt. Es wird dringend empfohlen, ein APILayer-Konto anstelle eines veralteten [!DNL Fixer.io]-Kontos zu verwenden.

   - _So stellen Sie eine Verbindung zum Service [fixer.io her](https://fixer.io/):_

      - Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Fixer.io]** .

      - Geben Sie Ihre fixer.io-**[!UICONTROL API key]** ein.

      - Geben Sie **[!UICONTROL Connection Timeout in Seconds]** die Anzahl Sekunden der Inaktivität ein, die erlaubt sein sollen, bevor die Verbindung unterbrochen wird.

     ![Allgemeine Konfiguration - Währungseinrichtung - Fixer.io-Optionen](../configuration-reference/general/assets/currency-setup-fixer.png){width="600" zoomable="yes"}

   - _Verbindung mit dem [[!DNL Fixer Api (APILayer)] Dienst](https://apilayer.com/):_

      - Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Fixer Api (APILayer)]** .

      - Geben Sie Ihre [!DNL APILayer] **[!UICONTROL API key]** ein.

      - Geben Sie **[!UICONTROL Connection Timeout in Seconds]** die Anzahl Sekunden der Inaktivität ein, die erlaubt sein sollen, bevor die Verbindung unterbrochen wird.

     ![Allgemeine Konfiguration - Währungseinrichtung - Optionen der Fixer-API (APILayer)](../configuration-reference/general/assets/currency-setup-fixer-api.png){width="600" zoomable="yes"}

   - _Verbindung mit dem [[!DNL Currency Convertor API] Dienst](https://free.currencyconverterapi.com/):_

      - Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Currency Convertor API]** .

      - Geben Sie die **[!UICONTROL API key]** Ihres Währungsumrechners ein.

      - Geben Sie **[!UICONTROL Connection Timeout in Seconds]** die Anzahl Sekunden der Inaktivität ein, die erlaubt sein sollen, bevor die Verbindung unterbrochen wird.

     ![Allgemeine Konfiguration - Währungseinrichtung - Währungsumrechner-API-Optionen](../configuration-reference/general/assets/currency-setup-converter.png){width="600" zoomable="yes"}

## Schritt 3: Konfigurieren der Einstellungen für den geplanten Import

1. Erweitern Sie unter „Währungseinstellungen“ den ![&#x200B; „Erweiterungsauswahl](../assets/icon-display-expand.png) auf den Abschnitt **[!UICONTROL Scheduled Import Settings]**.

   ![Allgemeine Konfiguration - Einstellungen für den geplanten Import der Währung](../configuration-reference/general/assets/currency-setup-scheduled-import-settings.png){width="600" zoomable="yes"}

1. Um Währungskurse automatisch zu aktualisieren, setzen Sie **[!UICONTROL Enabled]** auf `Yes`.

1. Legen Sie die Aktualisierungsoptionen fest:

   - **[!UICONTROL Service]** - Auf den Tarifanbieter festlegen. Der Standardwert ist `Fixer.io (legacy)`.

   - **[!UICONTROL Start Time]** - Festgelegt auf die Stunde, Minute und Sekunde, in der die Tarife gemäß dem Zeitplan aktualisiert werden.

   - **[!UICONTROL Frequency]** - Legen Sie eine der folgenden Einstellungen fest, um zu bestimmen, wie oft die Raten aktualisiert werden:

      - `Daily`
      - `Weekly`
      - `Monthly`

   - **[!UICONTROL Error Email Recipient]** - Geben Sie die E-Mail-Adresse der Person ein, die eine E-Mail-Benachrichtigung erhalten soll, wenn während des Importvorgangs ein Fehler auftritt.

     Um mehrere E-Mail-Adressen einzugeben, trennen Sie sie durch ein Komma.

   - **[!UICONTROL Error Email Sender]** - Auf den [Store-Kontakt](../getting-started/store-details.md#store-email-addresses) festlegen, der als Absender der Fehlerbenachrichtigung angezeigt wird.

   - **[!UICONTROL Error Email Template]** - Auf die für die Fehlerbenachrichtigung verwendete E-Mail-Vorlage festlegen.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link **[!UICONTROL Cache Management]** und aktualisieren Sie den ungültigen Cache.

   ![Systemmeldung - Aktualisieren Sie den ungültigen Cache](./assets/msg-cache-management.png){width="600" zoomable="yes"}

## Schritt 4: Währungskurse aktualisieren

Die Währungskurse müssen mit den aktuellen Werten aktualisiert werden, bevor sie in Kraft treten. [Aktualisieren Sie die Sätze](currency-update.md) manuell oder um die Sätze automatisch zu importieren.

## Schritt 5: Währungssymbole anpassen (optional)

Die Verwaltung von Währungssymbolen bietet Ihnen die Möglichkeit, das Symbol anzupassen, das mit jeder Währung verbunden ist, die in Ihrem Geschäft als Zahlung akzeptiert wird.

![Währungssymbole](./assets/stores-currency-symbols.png){width="600" zoomable="yes"}

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Symbols]**.

   Jede Währung, die für Ihren Store aktiviert ist, wird in der _[!UICONTROL Currency]_&#x200B;angezeigt.

1. Ändern Sie die Einstellungen in der Liste nach Bedarf:

   - Geben Sie für jede Währung, die Sie verwenden möchten, ein benutzerdefiniertes Symbol ein, oder aktivieren Sie das Kontrollkästchen &quot;**[!UICONTROL Use Standard]**&quot; für jede Währung.

   - Um das Standardsymbol zu überschreiben, deaktivieren Sie das Kontrollkästchen _[!UICONTROL Use Standard]_&#x200B;und geben Sie das gewünschte Symbol ein.

   >[!NOTE]
   >
   >Es ist nicht möglich, die Ausrichtung des Währungssymbols von links nach rechts zu ändern.

1. Klicken Sie abschließend auf **[!UICONTROL Save Currency Symbols]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link **[!UICONTROL Cache Management]** und aktualisieren Sie alle ungültigen Caches.
