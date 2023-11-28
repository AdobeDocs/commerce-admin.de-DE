---
title: '[!DNL Business Intelligence] tools'
description: Erfahren Sie, wie Adobe Commerce- und Magento Open Source-Händler mithilfe von Business Intelligence-Tools Einblicke gewinnen können, mit denen sie fundierte Geschäftsentscheidungen treffen.
exl-id: 687d04e4-841b-44f7-94ca-bbb20fbe2d8b
feature: Commerce Intelligence, Reporting
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# [!DNL Business Intelligence] tools

Verwenden Sie Business Intelligence-Tools, um Einblicke zu gewinnen, die für fundierte Geschäftsentscheidungen verwendet werden.

## [!DNL Business Intelligence] account

Wenn Sie eine [!DNL Business Intelligence] -Konto über Adobe nutzen, erhalten Sie Zugriff auf fünf Dashboards mit ca. 70 Berichten. Diese Berichte sollen Einblicke in Ihre Daten bieten und Fragen wie &quot;Wie wachsen meine Bestellungen monatlich?&quot;, &quot;Wer sind meine treusten Kunden?&quot;und &quot;Funktioniert meine Couponstrategie?&quot;beantworten. Detaillierte Informationen zu diesem Tool-Set finden Sie im Abschnitt [MBI-Benutzerhandbuch][1].

## [!DNL Advanced Reporting]

[!DNL Advanced Reporting] ist in Adobe Commerce und Magento Open Source enthalten. Mit dieser Funktion erhalten Sie Zugriff auf eine Suite dynamischer Berichte, die auf Ihren Produkt-, Bestell- und Kundendaten basieren, mit einem personalisierten Dashboard, das auf Ihre geschäftlichen Anforderungen zugeschnitten ist. while [!DNL Advanced Reporting] uses [!DNL Business Intelligence] für die Analyse benötigen Sie kein Business Intelligence-Konto, um [!DNL Advanced Reporting].

Technische Informationen finden Sie im Abschnitt [[!DNL Advanced Reporting]][2]{:target=&quot;_blank&quot;} Thema in der Entwicklerdokumentation.

>[!NOTE]
>
>[!DNL Business Intelligence] -Konten verwenden integrierte Berichte anstelle der [!DNL Advanced Reporting] Funktion.

![Erweitertes Berichterstellungs-Dashboard](./assets/reporting-advanced.png){width="700"}

### Voraussetzungen

* Die Website muss auf einem öffentlichen Webserver ausgeführt werden.

* Die Domäne muss über ein gültiges SSL-Zertifikat (Security) verfügen.

* [!DNL Commerce] muss ohne Fehler erfolgreich installiert oder aktualisiert worden sein.

* Im [!DNL Commerce] Konfiguration für [Store-URLs](../stores-purchase/store-urls.md), die **[!UICONTROL Base URL (Secure)]** -Einstellung für die Store-Ansicht muss auf die sichere URL verweisen. Beispiel: `https://yourdomain.com`.

* Im [!DNL Commerce] Konfiguration für Store-URLs, **[!UICONTROL Use Secure URLs on Storefront]** und **[!UICONTROL Use Secure URLs in Admin]** muss auf `Yes`.

* [[!DNL Commerce] crontab][3] erstellt und auf dem installierten Server werden Cron-Aufträge ausgeführt.

>[!NOTE]
>
>[!DNL Advanced Reporting] kann nur mit [!DNL Commerce] Installationen, die kontinuierlich eine [Basiswährung](../stores-purchase/currency-configuration.md).


### Schritt 1: Aktivieren [!DNL Advanced Reporting]

Im [!DNL Commerce] Konfiguration, [[!DNL Advanced Reporting]](../configuration-reference/general/advanced-reporting.md) ist standardmäßig aktiviert und wird automatisch gestartet, wenn cron [konfiguriert](../configuration-reference/advanced/system.md) und laufen. Der Versuch, das Abonnement einzurichten, wird zu Beginn jeder Stunde über die nächsten 24 Stunden bis zum Erfolg gestartet. Der Abonnementstatus lautet &quot;Ausstehend&quot;, bis das Abonnement erfolgreich eingerichtet wurde.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In der linken Navigationsleiste, in der **[!UICONTROL General]** erweitert ist, wählen Sie **[!UICONTROL Advanced Reporting]** und gehen Sie wie folgt vor:

   * Stellen Sie sicher, dass **[!UICONTROL Advanced Reporting Service]** auf `Enable` (Standardeinstellung).

   * Legen Sie die **[!UICONTROL Time of day to send data]** auf die Stunde, Minute und Sekunde, nach einer 24-Stunden-Zeit, die Sie möchten, dass der Dienst aktualisierte Daten von Ihrem Store erhält. Standardmäßig werden die Daten um 2:00 Uhr gesendet.

   * under **[!UICONTROL Industry Data]**, wählen Sie die **[!UICONTROL Industry]** die Ihr Geschäft am besten beschreibt.

   ![Erweiterte Berichtkonfiguration](./assets/advanced-reporting-config.png){width="400"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

1. Klicken Sie bei Aufforderung auf **[[!UICONTROL Cache Management]](../systems/cache-management.md)** in der Nachricht am oberen Seitenrand ein und aktualisieren Sie alle ungültigen Caches.

1. Warten Sie über Nacht oder bis nach dem Zeitpunkt des nächsten geplanten Updates. Überprüfen Sie dann den Status Ihres Abonnements. Wenn der Status weiterhin ist _pending_, stellen Sie sicher, dass Ihre Installation alle Anforderungen erfüllt.

### Schritt 2: Zugriff [!DNL Advanced Reporting]

1. Führen Sie einen der folgenden Schritte aus:

   * Im _Admin_ Seitenleiste, wählen **[!UICONTROL Dashboard]**. Klicken Sie anschließend auf **[!UICONTROL Go to Advanced Reporting]**.
   * Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Reports]** > _[!UICONTROL Business Intelligence]_>**[!UICONTROL Advanced Reporting]**.

   Die [!DNL Advanced Reporting] Dashboard bietet eine schnelle Zusammenfassung Ihrer Bestellungen, Kunden und Produkte. Scrollen Sie nach unten, um das vollständige Dashboard anzuzeigen.

1. Um eine bessere Ansicht der Daten zu erhalten, legen Sie die **[!UICONTROL Filters]** in der oberen rechten Ecke des Zeitraums und der Speicheransicht, die Sie in den Bericht aufnehmen möchten. Führen Sie dann die folgenden Schritte aus:

   * Bewegen Sie den Mauszeiger über einen Datenpunkt, um weitere Informationen zu erhalten.
   * Um alle Dashboard-Berichte anzuzeigen, klicken Sie auf jede Registerkarte.

   ![Datenpunkt](./assets/reporting-advanced-data-point.png){width="600" zoomable="yes"}

## Zugriff [!DNL Advanced Reporting] Datenressourcen

Klicken Sie oben rechts im Dashboard für erweiterte Berichte auf **[!UICONTROL Additional Resources]**.

![Erweiterte Berichtsdatenressourcen](./assets/advanced-reporting-your-data-resources.png){width="600" zoomable="yes"}

## Fehlerbehebung

Wenn Sie die Meldung &quot;Seite nicht gefunden&quot;mit dem Code 404 erhalten, überprüfen Sie, ob Ihr Store die Anforderungen für [!DNL Advanced Reporting]. Folgen Sie dann den Anweisungen, um zu überprüfen, ob die Integration installiert ist.

### Überprüfen, ob die Integration aktiv ist

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integration]**.

1. Stellen Sie sicher, dass **[!UICONTROL Magento Analytics user]** wird in der Liste angezeigt und die **[!UICONTROL Status]** is `Active`.

1. Um den Benutzer wiederherzustellen, klicken Sie auf **[!UICONTROL Reauthorize]** und gehen Sie wie folgt vor:

   ![Neu autorisieren](./assets/advanced-reporting-integration-reauthorize.png){width="600"}

   * Klicken Sie bei Aufforderung auf **[!UICONTROL Reauthorize]** um den Zugriff auf die API-Ressourcen zu genehmigen.

     ![Zugriff auf API-Ressourcen erneut autorisieren](./assets/advanced-reporting-integration-api.png){width="600"}

   * Überprüfen Sie, ob die Liste der Integrationstoken für Erweiterungen abgeschlossen ist. Klicken Sie anschließend auf **Fertig**.

     ![Integrationstoken](./assets/advanced-reporting-integration-tokens-for-extensions.png){width="600"}

1. Suchen Sie nach der Meldung, die die Integration anzeigt. `Magento Analytics user` erneut autorisiert wird.

1. Warten Sie über Nacht oder bis nach dem Zeitpunkt des nächsten geplanten Updates.

### Einheitliche Basiswährung überprüfen

[!DNL Advanced Reporting] kann nur mit [!DNL Commerce] -Installationen, die nur eine [Basiswährung](../stores-purchase/currency-configuration.md) seit dem Zeitpunkt der Installation. Das Ergebnis ist, dass im Verlauf alle Bestellungen dieselbe Basiswährung verwenden. [!DNL Advanced Reporting] funktioniert nicht, wenn Sie Ihre Basiswährung jederzeit geändert haben und Bestellungen in Ihrer Geschichte haben, die mit verschiedenen Basiswährungen verarbeitet wurden.

Um festzustellen, ob Ihr Store mehrere Basiswährungen hat, können Sie Ihre [!DNL Commerce] -Datenbank über die Befehlszeile unter Verwendung des folgenden MySQL-Beispiels. Möglicherweise müssen Sie die Tabellennamen entsprechend Ihrer Datenstruktur ändern:

```sql
select distinct base_currency_code from sales_order;
```

### Datendiskrepanz

Wenn Sie feststellen, dass die Variable `Data last updated...` -Beschriftung das gestrige Datum und nicht das heutige Datum anzeigt. Möglicherweise kann es zu einer Verzögerung von bis zu einem Tag in den Aktualisierungen der erweiterten Berichterstellung kommen. Diese Verzögerung ist auf eine größer als erwartete Warteschlangengröße zurückzuführen.

## Dashboard-Berichte

**[!UICONTROL Orders]**

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Revenue] | Zeigt den gesamten Umsatz an, den die Store-Ansicht während des definierten Zeitraums erhalten hat. |
| [!UICONTROL Orders] | Zeigt alle Bestellungen an, die während des definierten Zeitraums über die Store-Ansicht aufgegeben wurden. |
| [!UICONTROL AOV] | Zeigt den durchschnittlichen Bestellwert an, der während des definierten Zeitraums über die Store-Ansicht platziert wurde. |
| [!UICONTROL Refunds] | Zeigt alle Erstattungen an, die während des definierten Zeitraums über die Store-Ansicht verarbeitet wurden. |
| [!UICONTROL Tax Collected] | Zeigt alle Steuern an, die über die Store-Ansicht während des definierten Zeitraums erfasst wurden. |
| [!UICONTROL Shipping Collected] | Zeigt alle Versandgebühren an, die während des definierten Zeitraums über die Store-Ansicht gesammelt wurden. |
| [!UICONTROL Orders by Status] | Zeigt die Anzahl der Bestellungen nach Status für die Store-Ansicht während des definierten Zeitraums an. |
| [!UICONTROL Orders by Status] | Listet eine Zusammenfassung der Anzahl der Bestellungen nach Status auf. |
| [!UICONTROL Coupon Usage] | Listet alle Gutscheincodes und die Anzahl der Benutzer für jeden Gutschein auf, die über die Store-Ansicht während des definierten Zeitraums eingelöst wurden. |
| [!UICONTROL Orders and Revenue by Billing Region] | Führt die Anzahl der Bestellungen und Umsätze nach Region für die Store-Ansicht im definierten Zeitraum auf. |
| [!UICONTROL Tax Collected by Billing Region] | Führt den Steuerbetrag auf, der für die Store-Ansicht während des definierten Zeitraums nach Region erhoben wurde. |
| [!UICONTROL Shipping Fees Collected by Shipping Region] | Listet die Versandgebühren auf, die für die Store-Ansicht während des definierten Zeitraums nach Region erhoben wurden. |

{style="table-layout:auto"}

**[!UICONTROL Customers]**

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Unique Customers] | Zeigt die Anzahl der Unique Customer-Konten an, die während des definierten Zeitraums mit der Store-Ansicht verknüpft sind. |
| [!UICONTROL New Registered Accounts] | Zeigt die Anzahl neuer Kundenkonten an, die während des definierten Zeitraums bei der Store-Ansicht registriert wurden. |
| [!UICONTROL Top Coupon Users] | Listet die Top-Gutscheinbenutzer nach Kunden-ID und die Anzahl der Bestellungen mit Gutscheinen für die Store-Ansicht während des definierten Zeitraums auf. |
| [!UICONTROL Customer KPI Table] | Listet die Anzahl der Bestellungen, den Umsatz und den durchschnittlichen Bestellwert nach Kunden-ID für die Store-Ansicht im definierten Zeitraum auf. |

{style="table-layout:auto"}

**[!UICONTROL Products]**

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Quantity of Products Sold] | Zeigt die Anzahl der Produkte an, die während des definierten Zeitraums über die Store-Ansicht verkauft wurden. |
| [!UICONTROL Products Added to Wishlists] | Listet alle Produkte auf, die während des definierten Zeitraums über die Store-Ansicht zu Wunschlisten hinzugefügt wurden. |
| [!UICONTROL Best Selling Products by Quantity] | Listet die am besten verkauften Produkte und Mengen auf, die während des definierten Zeitraums über die Store-Ansicht verkauft wurden. |
| [!UICONTROL Best Selling Products by Revenue] | Listet die am besten verkauften Produkte und den Umsatz auf, die durch den Verkauf des Produkts über die Store-Ansicht während des definierten Zeitraums generiert wurden. |

{style="table-layout:auto"}


[1]: https://experienceleague.adobe.com/docs/commerce-business-intelligence/mbi/guide-overview.html
[2]: https://developer.adobe.com/commerce/php/development/advanced-reporting/
[3]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
