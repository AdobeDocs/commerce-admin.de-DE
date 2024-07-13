---
title: Cron (geplante Aufgaben)
description: Erfahren Sie, wie Sie die Ausführung und Planung von Commerce-Cron-Aufträgen über den Administrator steuern können.
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Cron (geplante Aufgaben)

Adobe Commerce und Magento Open Source führen einige Vorgänge planmäßig durch, indem sie regelmäßig ein Skript ausführen. Sie können die Ausführung und Planung von Commerce-Cron-Aufträgen über den Administrator steuern. Speichervorgänge, die gemäß einem Cron-Zeitplan ausgeführt werden, umfassen unter anderem:

- [E-Mail](email-communications.md)
- [Katalogpreisregeln](../merchandising-promotions/price-rules-catalog.md)
- [Newsletter](../merchandising-promotions/newsletters.md)
- [XML-Sitemap-Generierung](../merchandising-promotions/sitemap-xml.md)
- [Währungsratenaktualisierungen](../stores-purchase/currency-update.md)
- [Inventory management](../inventory-management/introduction.md)

>[!IMPORTANT]
>
>Commerce-Dienste müssen in Crontab installiert werden, um sicherzustellen, dass Kernkomponenten und einige Drittanbietererweiterungen erwartungsgemäß funktionieren. Detaillierte Informationen zum Installieren von Diensten auf der Registerkarte finden Sie in den [Anweisungen im _Installationshandbuch_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html) .

Darüber hinaus können Sie Folgendes so konfigurieren, dass es gemäß einem Cron-Zeitplan ausgeführt wird:

- Systemrasteraktualisierungen und Neuindizierung bestellen
- Ausstehende Zahlungslebensdauer

Vergewissern Sie sich, dass die [Basis-URLs](../stores-purchase/store-urls.md) für den Store korrekt festgelegt sind, damit die bei Cron-Vorgängen generierten URLs korrekt sind. Informationen zu Adobe Commerce in der Cloud-Infrastruktur finden Sie unter [Einrichten von Cron-Aufträgen](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html) im _Handbuch zu Commerce in Cloud Infrastructure_. Informationen zu On-Premise finden Sie unter [Konfigurieren und Ausführen von &quot;con](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html)&quot;im _Konfigurationshandbuch_.

## Cron konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Cron]** .

   ![Erweiterte Konfiguration - Cron-Aufgaben](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. Führen Sie die folgenden Einstellungen für die Gruppen **[!UICONTROL Index]** und **[!UICONTROL Default]** aus.

   Die Einstellungen sind in jedem Abschnitt identisch.

   - **[!UICONTROL Generate Schedules Every]** - Definiert, wie oft der Zeitplan generiert wird (in Minuten). Zeitpläne werden in der Datenbank gespeichert.
   - **[!UICONTROL Schedule Ahead for]** - Definiert, wie weit im Voraus geplante Cron-Aufträge geplant sind (in Minuten). Wenn diese Einstellung beispielsweise auf `10` festgelegt ist und der Cron ausgeführt wird, werden die Cron-Aufträge für die nächsten 10 Minuten geplant.
   - **[!UICONTROL Missed if not Run Within]** - Definiert die Zeit (in Minuten), die zum Ermitteln eines verpassten Auftrags verwendet wird. Wenn der Cron-Auftrag nicht zur geplanten Zeit ausgeführt wird und die angegebene Uhrzeit abgelaufen ist, kann er nicht ausgeführt werden und der Status ist auf `Missed` eingestellt.
   - **[!UICONTROL History Cleanup Every]** - Definiert die Zeit (in Minuten), zu der der Verlauf beendeter Aufgaben aus der Datenbank gelöscht wird.
   - **[!UICONTROL Success History Lifetime]** - Definiert die Zeitdauer (in Minuten), für die der Verlauf von Cron-Aufträgen mit dem Status `Successful` in der Datenbank verbleibt.
   - **[!UICONTROL Failure History Lifetime]** - Definiert die Zeitdauer (in Minuten), für die der Verlauf von Cron-Aufträgen mit dem Status `Error` in der Datenbank verbleibt.
   - **[!UICONTROL Use Separate Process]** - Definiert, ob alle Cron-Aufträge der Gruppe in einem separaten Systemprozess ausgeführt werden. Optionen: `Yes` / `No`

   ![Erweiterte Konfiguration - Cron-Gruppenindex](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
