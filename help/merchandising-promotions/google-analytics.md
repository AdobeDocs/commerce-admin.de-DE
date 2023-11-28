---
title: '[!DNL Google Analytics]'
description: Erfahren Sie, wie Sie [!DNL Google Analytics] , um nützliche Metriken für Ihre Commerce-Sites zu sammeln.
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics] bietet Ihnen die Möglichkeit, zusätzliche benutzerdefinierte Dimensionen und Metriken für das Tracking zu definieren, mit Unterstützung für Offline- und Mobile-App-Interaktionen und Zugriff auf laufende Aktualisierungen. [!DNL Google Analytics] 4 ist die Messlösung der nächsten Generation von Google und ersetzt [!DNL Universal Analytics]. Ab dem 1. Juli 2023 werden keine neuen Treffer mehr von den standardmäßigen universellen Analytics-Eigenschaften verarbeitet.

>[!NOTE]
>
>Wenn Ihr Unternehmen Datenschutzbestimmungen wie die [Die Datenschutz-Grundverordnung](../getting-started/compliance-gdpr.md) und/oder [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), siehe [Google-Datenschutzeinstellungen](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>Wenn Sie die [Cookie-Einschränkungsmodus](../getting-started/compliance-cookie-law.md), [!DNL Google Analytics] erfasst nur Daten zu Besuchern, wenn diese Cookies akzeptiert haben.

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### Schritt 1: Einrichten [!UICONTROL Google Analytics] 4

Wenn Sie noch keine [!DNL Google Analytics] 4-Setup für Ihre Site ausführen, führen Sie eine der folgenden Methoden aus:

- [Einrichten der Analytics-Datenerfassung](https://support.google.com/analytics/answer/9304153)
- [Google Analytics 4 zu einer Site mit [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### Schritt 2: Abschluss der Commerce-Konfiguration

1. Melden Sie sich bei Admin für Ihren Commerce-Store an.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Google API]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Google GTag]** Abschnitt.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Google Analytics4]** und gehen Sie wie folgt vor:

   - Satz **[!UICONTROL Enable]** nach `Yes`.

   - Lassen Sie die **[!UICONTROL Account type]** as `Google Analytics4`.

   - Geben Sie Ihre **[!UICONTROL Measurement ID]**. Weitere Informationen finden Sie unter [Hilfe für Google Analytics](https://support.google.com/analytics/answer/9539598).

   - Wenn Sie A/B-Tests und andere Leistungstests für Ihren Inhalt durchführen möchten, legen Sie **Inhaltstests** nach `Yes`.

   ![Vertriebskonfiguration - Google-API für Google Analytics 4](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Google Universal Analytics

>[!IMPORTANT]
>
>Ab dem 1. Juli 2023 werden in den standardmäßigen universellen Analytics-Eigenschaften keine Daten mehr verarbeitet. Wenn Sie sich weiterhin auf [!DNL Universal Analytics]wird empfohlen, [Vorbereitung auf die Verwendung der Google Analytics 4](https://support.google.com/analytics/answer/10759417) in Zukunft.

### Schritt 1: Einrichten von Google Universal Analytics

Besuchen Sie die Google-Website und melden Sie sich für eine [Google Universal Analytics][1] -Konto.

### Schritt 2: Abschluss der Commerce-Konfiguration

1. Melden Sie sich bei Admin für Ihren Commerce-Store an.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Google API]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Google Analytics]** und führen Sie folgende Schritte aus:

   - Satz **[!UICONTROL Enable]** nach `Yes`.

   - Geben Sie Ihre [!DNL Google Analytics] **[!UICONTROL Account Number]**.

   - Wenn Sie A/B-Tests und andere Leistungstests für Ihren Inhalt durchführen möchten, legen Sie **[!UICONTROL Content Experiments]** nach `Yes`.

   ![Vertriebskonfiguration - Google-API - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Verbesserter E-Commerce

Enhanced Ecommerce ist ein Plug-in für [!DNL Google Universal Analytics] gibt Ihnen einen Einblick in das Einkaufs- und Kaufverhalten Ihrer Kunden. Mit Enhanced E-Commerce können Sie Berichte zu wichtigen Kundenaktivitäten erstellen, z. B. wenn Kunden Artikel zum Warenkorb hinzufügen, den Kassenprozess starten oder einen Kauf abschließen. Sie können auch Muster von Käufern identifizieren und analysieren, die ihren Warenkorb verlassen, ohne einen Kauf tätigen zu müssen.

Die folgenden Anweisungen zeigen, wie Sie [!DNL Google Tag Manager] mit [!DNL Universal Analytics] um erweiterte E-Commerce-Daten und -Berichte zu erstellen.

### Schritt 1. Für Google-Konten anmelden

1. Registrieren Sie sich für eine [Google Tag Manager](google-tag-manager.md) und schließen Sie die Konfiguration Commerce ab.

1. Registrieren Sie sich für eine neue [Google Universal Analytics][1] -Konto.

### Schritt 2. Konfigurieren des erweiterten E-Commerce

1. Melden Sie sich bei Ihrem Google Universal Analytics-Konto an.

1. Erstellen Sie eine Eigenschaft für die erweiterte E-Commerce-Analyse mit den folgenden Einstellungen:

   - Status: EIN
   - Verwandte Produkte: ON
   - Erweiterte E-Commerce-Berichterstellung aktivieren: ON
   - Checkout-Beschriftung: (nicht erforderlich)

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Submit]**.

### Schritt 3. Erstellen von Tags und Triggern

1. Anmelden bei [!DNL Google Tag Manager] und erstellen Sie die folgenden Trigger:

   | Name | Ereignistyp | Filter |
   |--- |--- |--- |
   | `addToCart` | Benutzerspezifisches Ereignis |  |
   | `checkout` | Benutzerspezifisches Ereignis |  |
   | `checkout only` | Seitenansicht | Seiten-URL stimmt mit RegEx /checkout/ überein.* |
   | `checkoutOption` | Benutzerspezifisches Ereignis |  |
   | `gtm.dom` | Benutzerspezifisches Ereignis |  |
   | `productClick` | Benutzerspezifisches Ereignis |  |
   | `promotionClick` | Benutzerspezifisches Ereignis |  |
   | `removeFromCart` | Benutzerspezifisches Ereignis |  |

   >[!NOTE]
   >
   >Die [!UICONTROL Checkout] -Ereignis wird nur für die integrierten Commerce-grundlegenden Zahlungsmethoden ausgelöst (wie `Check / Money Order` und `Cash On Delivery Payment`). Dieses Ereignis wird nicht für `PayPal checkout` und anderen externen Zahlungsmethoden, die die Umleitung zum Checkout aus externen Ressourcen verwenden.

1. Erstellen Sie die folgenden universellen Analytics-Tags mit derselben grundlegenden Konfiguration.

   - Universal Analytics-Tags

     | Name | Typ | Auslösen von Triggern |
     |--- |--- |--- |
     | `Add to cart tracking` | Universal Analytics | addToCart |
     | `Checkout option tracking` | Universal Analytics | checkoutOption |
     | `Checkout tracking` | Universal Analytics | Kasse |
     | `Pageview tracking` | Universal Analytics | gtm.dom |
     | `Product click tracking` | Universal Analytics | productClick |
     | `Promo click tracking` | Universal Analytics | promotionClick |
     | `Remove from cart tracking` | Universal Analytics | removeFromCart |

   - Grundlegende Tag-Konfiguration

     | Einstellung | Wert |
     |--- |--- |
     | [!UICONTROL Product] | Google Analytics |
     | [!UICONTROL Tag Type] | Universal Analytics |
     | [!UICONTROL Tracking ID] | UA-XXX (die Tracking-ID aus Ihrem universellen Analytics-Konto) |
     | [!UICONTROL Enable Enhanced Ecommerce Features] | True |
     | [!UICONTROL Use data layer] | True |
     | [!UICONTROL Use Debug version] | True |

1. Führen Sie die einzelnen Tracking-Konfigurationen aus.

   - Geben Sie Folgendes ein: **[!UICONTROL Add to Cart]** Tracking-Einstellungen:

     | Einstellung | Wert |
     |--- |--- |
     | [!UICONTROL Track Type] | Ereignis |
     | [!UICONTROL Category] | E-Commerce |
     | [!UICONTROL Action] | Zum Warenkorb hinzufügen |
     | [!UICONTROL Trigger] | addToCart |

   - Geben Sie Folgendes ein: **[!UICONTROL Checkout option]** Tracking-Einstellungen:

     | Einstellung | Wert |
     |--- |--- |
     | [!UICONTROL Track Type] | Ereignis |
     | [!UICONTROL Category] | E-Commerce |
     | [!UICONTROL Action] | Checkout-Option |
     | [!UICONTROL Trigger] | checkoutOption |

   - Geben Sie Folgendes ein: **[!UICONTROL PageView]** Tracking-Einstellungen:

     | Einstellung | Wert |
     |--- |--- |
     | [!UICONTROL Track Type] | PageView |
     | [!UICONTROL Trigger] | gtm.dom |

   - Führen Sie Folgendes aus: **[!UICONTROL Product Click]** Tracking-Konfiguration:

     | Einstellung | Wert |
     |--- |--- |
     | [!UICONTROL Track Type] | Ereignis |
     | [!UICONTROL Category] | E-Commerce |
     | [!UICONTROL Action] | Produktklick |
     | [!UICONTROL Trigger] | productClick |

   - Führen Sie Folgendes aus: **[!UICONTROL Promotion Click]** Tracking-Konfiguration:

     | Einstellung | Wert |
     |--- |--- |
     | [!UICONTROL Track Type] | Ereignis |
     | [!UICONTROL Category] | E-Commerce |
     | [!UICONTROL Action] | Promotion Click |
     | [!UICONTROL Trigger] | promotionClick |

   - Führen Sie Folgendes aus: **[!UICONTROL Remove from Cart]** Tracking-Konfiguration:

     | Einstellung | Wert |
     |--- |--- |
     | [!UICONTROL Track Type] | Ereignis |
     | [!UICONTROL Category] | E-Commerce |
     | [!UICONTROL Action] | Aus Warenkorb entfernen |
     | [!UICONTROL Trigger] | removeFromCart |

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Preview]** und überprüfen Sie, ob die Tags ordnungsgemäß funktionieren.

1. Klicken Sie nach der Überprüfung der Einstellungen auf **[!UICONTROL Publish]**.


[1]: https://support.google.com/analytics/answer/2817075?hl=en
