---
title: '[!DNL Google Analytics]'
description: Erfahren Sie, wie Sie mit [!DNL Google Analytics] nützliche Metriken für Ihre Commerce-Sites erfassen können.
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics] bietet Ihnen die Möglichkeit, zusätzliche benutzerdefinierte Dimensionen und Metriken für das Tracking zu definieren, mit Unterstützung für Offline- und mobile App-Interaktionen und Zugriff auf laufende Aktualisierungen. [!DNL Google Analytics] 4 ist die Messlösung der nächsten Generation von Google und ersetzt [!DNL Universal Analytics]. Ab dem 1. Juli 2023 werden keine neuen Treffer mehr von den standardmäßigen universellen Analytics-Eigenschaften verarbeitet.

>[!NOTE]
>
>Wenn Ihr Unternehmen Datenschutzbestimmungen wie die [Datenschutz-Grundverordnung](../getting-started/compliance-gdpr.md) und/oder den [California Consumer Privacy Act](../getting-started/compliance-ccpa.md) unterliegt, finden Sie weitere Informationen unter [Google-Datenschutzeinstellungen](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>Wenn Sie den [Cookie-Beschränkungsmodus](../getting-started/compliance-cookie-law.md) aktivieren, erfasst [!DNL Google Analytics] keine Daten zu Besuchern, es sei denn, sie haben Cookies akzeptiert.

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### Schritt 1: Einrichten von [!UICONTROL Google Analytics] 4

Wenn Sie noch nicht über ein [!DNL Google Analytics] 4-Setup für Ihre Site verfügen, führen Sie eine der folgenden Methoden aus:

- [Einrichten der Analytics-Datenerfassung zum ersten Mal](https://support.google.com/analytics/answer/9304153)
- [Google Analytics 4 zu einer Site mit  [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165) hinzufügen

### Schritt 2: Commerce-Konfiguration abschließen

1. Melden Sie sich bei Admin für Ihren Commerce Store an.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Google API]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Google GTag]** .

1. Erweitern Sie den Unterabschnitt **[!UICONTROL Google Analytics4]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und gehen Sie wie folgt vor:

   - Setzen Sie **[!UICONTROL Enable]** auf `Yes`.

   - Belassen Sie die **[!UICONTROL Account type]** als `Google Analytics4`.

   - Geben Sie Ihren **[!UICONTROL Measurement ID]** ein. Weitere Informationen finden Sie in der [Google Analytics-Hilfe](https://support.google.com/analytics/answer/9539598).

   - Wenn Sie A/B-Tests und andere Leistungstests für Ihren Inhalt durchführen möchten, setzen Sie **Inhaltsexperimente** auf `Yes`.

   ![Vertriebskonfiguration - Google-API für Google Analytics 4](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Google Universal Analytics

>[!IMPORTANT]
>
>Ab dem 1. Juli 2023 werden in den standardmäßigen universellen Analytics-Eigenschaften keine Daten mehr verarbeitet. Wenn Sie weiterhin auf [!DNL Universal Analytics] angewiesen sind, wird empfohlen, dass Sie [sich in Zukunft auf die Verwendung von Google Analytics 4](https://support.google.com/analytics/answer/10759417) vorbereiten.

### Schritt 1: Einrichten von Google Universal Analytics

Besuchen Sie die Google-Website und melden Sie sich für ein [Google Universal Analytics][1] -Konto an.

### Schritt 2: Commerce-Konfiguration abschließen

1. Melden Sie sich bei Admin für Ihren Commerce Store an.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Google API]** aus.

1. Erweitern Sie den Abschnitt **[!UICONTROL Google Analytics]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   - Setzen Sie **[!UICONTROL Enable]** auf `Yes`.

   - Geben Sie Ihren [!DNL Google Analytics] **[!UICONTROL Account Number]** ein.

   - Wenn Sie A/B-Tests und andere Leistungstests für Ihren Inhalt durchführen möchten, setzen Sie **[!UICONTROL Content Experiments]** auf `Yes`.

   ![Vertriebskonfiguration - Google-API - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Verbesserter E-Commerce

Enhanced E-Commerce ist ein Plug-in für [!DNL Google Universal Analytics], das Ihnen Einblicke in das Einkaufs- und Kaufverhalten Ihrer Kunden bietet. Mit Enhanced E-Commerce können Sie Berichte zu wichtigen Kundenaktivitäten erstellen, z. B. wenn Kunden Artikel zum Warenkorb hinzufügen, den Kassenprozess starten oder einen Kauf abschließen. Sie können auch Muster von Käufern identifizieren und analysieren, die ihren Warenkorb verlassen, ohne einen Kauf tätigen zu müssen.

Die folgenden Anweisungen zeigen, wie Sie [!DNL Google Tag Manager] mit [!DNL Universal Analytics] konfigurieren, um Enhanced E-Commerce-Daten und -Berichte zu erstellen.

### Schritt 1. Für Google-Konten anmelden

1. Registrieren Sie sich für ein [Google Tag Manager](google-tag-manager.md) -Konto und schließen Sie die Commerce-Konfiguration ab.

1. Registrieren Sie sich für ein neues [Google Universal Analytics][1] -Konto.

### Schritt 2. Konfigurieren des erweiterten E-Commerce

1. Melden Sie sich bei Ihrem Google Universal Analytics-Konto an.

1. Erstellen Sie eine Eigenschaft für die erweiterte E-Commerce-Analyse mit den folgenden Einstellungen:

   - Status: EIN
   - Verwandte Produkte: ON
   - Erweiterte E-Commerce-Berichterstellung aktivieren: ON
   - Checkout-Beschriftung: (nicht erforderlich)

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Submit]**.

### Schritt 3. Erstellen von Tags und Triggern

1. Melden Sie sich bei Ihrem [!DNL Google Tag Manager] -Konto an und erstellen Sie die folgenden Trigger:

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
   >Das [!UICONTROL Checkout] -Ereignis wird nur für die integrierten Commerce-Basiszahlungsmethoden (wie `Check / Money Order` und `Cash On Delivery Payment`) ausgelöst. Dieses Ereignis wird nicht für `PayPal checkout` und andere externe Zahlungsmethoden ausgeführt, die eine Umleitung zum Checkout aus externen Ressourcen verwenden.

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

   - Geben Sie die folgenden **[!UICONTROL Add to Cart]**-Tracking-Einstellungen ein:

     | Einstellung | Wert |
     |--- |--- |
     | [!UICONTROL Track Type] | Ereignis |
     | [!UICONTROL Category] | E-Commerce |
     | [!UICONTROL Action] | Zum Warenkorb hinzufügen |
     | [!UICONTROL Trigger] | addToCart |

   - Geben Sie die folgenden **[!UICONTROL Checkout option]**-Tracking-Einstellungen ein:

     | Einstellung | Wert |
     |--- |--- |
     | [!UICONTROL Track Type] | Ereignis |
     | [!UICONTROL Category] | E-Commerce |
     | [!UICONTROL Action] | Checkout-Option |
     | [!UICONTROL Trigger] | checkoutOption |

   - Geben Sie die folgenden **[!UICONTROL PageView]**-Tracking-Einstellungen ein:

     | Einstellung | Wert |
     |--- |--- |
     | [!UICONTROL Track Type] | PageView |
     | [!UICONTROL Trigger] | gtm.dom |

   - Führen Sie die folgende **[!UICONTROL Product Click]** -Tracking-Konfiguration aus:

     | Einstellung | Wert |
     |--- |--- |
     | [!UICONTROL Track Type] | Ereignis |
     | [!UICONTROL Category] | E-Commerce |
     | [!UICONTROL Action] | Produktklick |
     | [!UICONTROL Trigger] | productClick |

   - Führen Sie die folgende **[!UICONTROL Promotion Click]** -Tracking-Konfiguration aus:

     | Einstellung | Wert |
     |--- |--- |
     | [!UICONTROL Track Type] | Ereignis |
     | [!UICONTROL Category] | E-Commerce |
     | [!UICONTROL Action] | Promotion Click |
     | [!UICONTROL Trigger] | promotionClick |

   - Führen Sie die folgende **[!UICONTROL Remove from Cart]** -Tracking-Konfiguration aus:

     | Einstellung | Wert |
     |--- |--- |
     | [!UICONTROL Track Type] | Ereignis |
     | [!UICONTROL Category] | E-Commerce |
     | [!UICONTROL Action] | Aus Warenkorb entfernen |
     | [!UICONTROL Trigger] | removeFromCart |

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Preview]** und vergewissern Sie sich, dass die Tags ordnungsgemäß funktionieren.

1. Klicken Sie nach der Überprüfung der Einstellungen auf **[!UICONTROL Publish]**.


[1]: https://support.google.com/analytics/answer/2817075?hl=en
