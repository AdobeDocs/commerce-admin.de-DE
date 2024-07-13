---
title: '[!DNL Commerce Intelligence] tools'
description: Erfahren Sie, wie Adobe Commerce- und Magento Open Source-Händler Commerce Intelligence-Tools verwenden können, um Einblicke zu erhalten, die für fundierte Geschäftsentscheidungen verwendet werden.
exl-id: 687d04e4-841b-44f7-94ca-bbb20fbe2d8b
feature: Commerce Intelligence, Reporting
source-git-commit: 78bcac16713f9ec87faf7029732972db73216e79
workflow-type: tm+mt
source-wordcount: '1163'
ht-degree: 0%

---

# [!DNL Commerce Intelligence] tools

Verwenden Sie Commerce Intelligence-Tools, um Einblicke zu erhalten, die für fundierte Geschäftsentscheidungen verwendet werden.

## [!DNL Commerce Intelligence] account

Wenn Sie ein [!DNL Commerce Intelligence] -Konto über Adobe aktivieren, erhalten Sie Zugriff auf fünf Dashboards mit etwa 70 Berichten. Diese Berichte sollen Einblicke in Ihre Daten bieten und Fragen wie &quot;Wie wachsen meine Bestellungen monatlich?&quot;, &quot;Wer sind meine treusten Kunden?&quot;und &quot;Funktioniert meine Couponstrategie?&quot;beantworten. Ausführliche Informationen zu diesem Tool-Set finden Sie im [Commerce Intelligence-Benutzerhandbuch][1].

## [!DNL Advanced Reporting]

[!DNL Advanced Reporting] ist in Adobe Commerce und Magento Open Source enthalten. Mit dieser Funktion erhalten Sie Zugriff auf eine Suite dynamischer Berichte, die auf Ihren Produkt-, Bestell- und Kundendaten basieren, mit einem personalisierten Dashboard, das auf Ihre geschäftlichen Anforderungen zugeschnitten ist. Während [!DNL Advanced Reporting] [!DNL Commerce Intelligence] für Analysen verwendet, benötigen Sie kein Commerce Intelligence-Konto, um [!DNL Advanced Reporting] zu verwenden.

Technische Informationen finden Sie im Thema [[!DNL Advanced Reporting]][2]{:target=&quot;_blank&quot;} in der Entwicklerdokumentation.

>[!NOTE]
>
>Aufgrund von Kompatibilitätsproblemen mit [!DNL Adobe Commerce Intelligence] kann Commerce die erweiterte Berichterstellung vorübergehend nicht mit AWS S3 Bucket als Medium für Quelldatendateien in [!DNL Commerce Intelligence] unterstützen.

![Erweitertes Berichterstellungs-Dashboard](./assets/reporting-advanced.png){width="700"}

### Voraussetzungen

* Die Website muss auf einem öffentlichen Webserver ausgeführt werden.

* Die Domäne muss über ein gültiges SSL-Zertifikat (Security) verfügen.

* [!DNL Commerce] muss ohne Fehler erfolgreich installiert oder aktualisiert worden sein.

* In der [!DNL Commerce] -Konfiguration für [Store-URLs](../stores-purchase/store-urls.md) muss die Einstellung **[!UICONTROL Base URL (Secure)]** für die Store-Ansicht auf die sichere URL verweisen. Beispiel: `https://yourdomain.com`.

* In der [!DNL Commerce] -Konfiguration für Store-URLs müssen **[!UICONTROL Use Secure URLs on Storefront]** und **[!UICONTROL Use Secure URLs in Admin]** auf `Yes` gesetzt werden.

* [[!DNL Commerce] crontab][3] wird erstellt und Cron-Aufträge werden auf dem installierten Server ausgeführt.

>[!NOTE]
>
>[!DNL Advanced Reporting] kann nur mit [!DNL Commerce] -Installationen verwendet werden, die kontinuierlich eine einzelne [Basiswährung](../stores-purchase/currency-configuration.md) verwendet haben.


### Schritt 1: Aktivieren Sie [!DNL Advanced Reporting]

In der [!DNL Commerce] -Konfiguration ist [[!DNL Advanced Reporting]](../configuration-reference/general/advanced-reporting.md) standardmäßig aktiviert und startet automatisch, wenn der Cron [konfiguriert](../configuration-reference/advanced/system.md) ist und ausgeführt wird. Der Versuch, das Abonnement einzurichten, wird zu Beginn jeder Stunde über die nächsten 24 Stunden bis zum Erfolg gestartet. Der Abonnementstatus lautet &quot;Ausstehend&quot;, bis das Abonnement erfolgreich eingerichtet wurde.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Navigationsbereich, in dem **[!UICONTROL General]** erweitert ist, **[!UICONTROL Advanced Reporting]** und gehen Sie wie folgt vor:

   * Stellen Sie sicher, dass **[!UICONTROL Advanced Reporting Service]** auf `Enable` gesetzt ist (die Standardeinstellung).

   * Stellen Sie den Wert &quot;**[!UICONTROL Time of day to send data]**&quot;auf die Stunde, Minute und Sekunde (gemäß einer 24-Stunden-Uhr-Zeit) ein, die der Dienst für den Empfang aktualisierter Daten aus Ihrem Store benötigen soll. Standardmäßig werden die Daten um 2:00 Uhr gesendet.

   * Wählen Sie unter **[!UICONTROL Industry Data]** die **[!UICONTROL Industry]** aus, die Ihr Geschäft am besten beschreibt.

   ![Erweiterte Berichtkonfiguration](./assets/advanced-reporting-config.png){width="400"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

1. Wenn Sie dazu aufgefordert werden, klicken Sie in der Meldung oben auf der Seite auf **[[!UICONTROL Cache Management]](../systems/cache-management.md)** und aktualisieren Sie alle ungültigen Caches.

1. Warten Sie über Nacht oder bis nach dem Zeitpunkt des nächsten geplanten Updates. Überprüfen Sie dann den Status Ihres Abonnements. Wenn der Status immer noch _ausstehend_ lautet, stellen Sie sicher, dass Ihre Installation alle Anforderungen erfüllt.

### Schritt 2: Zugriff auf [!DNL Advanced Reporting]

1. Führen Sie einen der folgenden Schritte aus:

   * Wählen Sie in der Seitenleiste _Admin_ die Option **[!UICONTROL Dashboard]** aus. Klicken Sie dann auf **[!UICONTROL Go to Advanced Reporting]**.
   * Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Reports]** > _[!UICONTROL Business Intelligence]_>**[!UICONTROL Advanced Reporting]**.

   Das Dashboard [!DNL Advanced Reporting] bietet eine schnelle Zusammenfassung Ihrer Bestellungen, Kunden und Produkte. Scrollen Sie nach unten, um das vollständige Dashboard anzuzeigen.

1. Um eine bessere Ansicht der Daten zu erhalten, setzen Sie &quot;**[!UICONTROL Filters]**&quot;in der oberen rechten Ecke auf den Zeitraum und die Store-Ansicht, die Sie in den Bericht aufnehmen möchten. Führen Sie dann die folgenden Schritte aus:

   * Bewegen Sie den Mauszeiger über einen Datenpunkt, um weitere Informationen zu erhalten.
   * Um alle Dashboard-Berichte anzuzeigen, klicken Sie auf jede Registerkarte.

   ![Datenpunkt](./assets/reporting-advanced-data-point.png){width="600" zoomable="yes"}

## Zugriff auf [!DNL Advanced Reporting] Datenressourcen

Klicken Sie in der oberen rechten Ecke des Dashboards Erweiterte Berichterstellung auf **[!UICONTROL Additional Resources]**.

![Erweiterte Berichterstellungsdatenressourcen](./assets/advanced-reporting-your-data-resources.png){width="600" zoomable="yes"}

## Fehlerbehebung

Wenn Sie die Meldung &quot;Seite nicht gefunden&quot;mit dem Code 404 erhalten, überprüfen Sie, ob Ihr Store die Anforderungen für [!DNL Advanced Reporting] erfüllt. Folgen Sie dann den Anweisungen, um zu überprüfen, ob die Integration installiert ist.

### Überprüfen, ob die Integration aktiv ist

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integration]**.

1. Stellen Sie sicher, dass die **[!UICONTROL Magento Analytics user]** -Integration in der Liste angezeigt wird und die **[!UICONTROL Status]** den Wert `Active` aufweist.

1. Um den Benutzer wiederherzustellen, klicken Sie auf **[!UICONTROL Reauthorize]** und führen Sie die folgenden Schritte aus:

   ![Neu autorisieren](./assets/advanced-reporting-integration-reauthorize.png){width="600"}

   * Klicken Sie bei Aufforderung auf **[!UICONTROL Reauthorize]** , um den Zugriff auf die API-Ressourcen zu genehmigen.

     ![Erneutes Autorisieren des Zugriffs auf API-Ressourcen](./assets/advanced-reporting-integration-api.png){width="600"}

   * Überprüfen Sie, ob die Liste der Integrationstoken für Erweiterungen abgeschlossen ist. Klicken Sie dann auf **Fertig**.

     ![Integrationstoken](./assets/advanced-reporting-integration-tokens-for-extensions.png){width="600"}

1. Suchen Sie nach der Meldung, die angibt, dass die Integration `Magento Analytics user` erneut autorisiert ist.

1. Warten Sie über Nacht oder bis nach dem Zeitpunkt des nächsten geplanten Updates.

### Einheitliche Basiswährung überprüfen

[!DNL Advanced Reporting] kann nur mit [!DNL Commerce] -Installationen verwendet werden, die seit dem Zeitpunkt der Installation nur eine einzige [Basiswährung](../stores-purchase/currency-configuration.md) verwendet haben. Das Ergebnis ist, dass im Verlauf alle Bestellungen dieselbe Basiswährung verwenden. [!DNL Advanced Reporting] funktioniert nicht, wenn Sie zu irgendeinem Zeitpunkt Ihre Basiswährung geändert haben und Bestellungen in Ihrem Verlauf haben, die mit verschiedenen Basiswährungen verarbeitet wurden.

Um festzustellen, ob Ihr Store mehrere Basiswährungen hat, können Sie Ihre [!DNL Commerce] -Datenbank über die Befehlszeile mit dem folgenden MySQL-Beispiel abfragen. Möglicherweise müssen Sie die Tabellennamen entsprechend Ihrer Datenstruktur ändern:

```sql
select distinct base_currency_code from sales_order;
```

### Datendiskrepanz

Wenn Sie feststellen, dass die Beschriftung `Data last updated...` das gestrige Datum und nicht das heutige anzeigt, kann es in den Aktualisierungen der erweiterten Berichterstellung zu einer Verzögerung von bis zu einem Tag kommen. Diese Verzögerung ist auf eine größer als erwartete Warteschlangengröße zurückzuführen.

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
