---
title: Cron (geplante Aufgaben)
description: Erfahren Sie, wie Sie die Ausführung und Planung von Commerce Cron-Aufträgen über den Administrator steuern können.
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/6zjak78aoXbzoHzdnOL4tvXgq4KAAjwMNLlLPax4ovE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: cc250cf1-34eb-4863-80d0-d170d45ea067
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 458
ht-degree: 0%

---

# Cron (geplante Aufgaben)

Adobe Commerce und Magento Open Source führen einige Vorgänge planmäßig durch, indem sie regelmäßig ein Skript ausführen. Sie können die Ausführung und Planung von Commerce-Cron-Aufträgen über den Administrator steuern. Speichervorgänge, die nach einem Cron-Zeitplan ausgeführt werden, umfassen unter anderem:

- [E-Mail](email-communications.md)
- [Katalogpreisregeln](../merchandising-promotions/price-rules-catalog.md)
- [Newsletter](../merchandising-promotions/newsletters.md)
- [Generieren einer XML-Sitemap](../merchandising-promotions/sitemap-xml.md)
- [Währungskursaktualisierungen](../stores-purchase/currency-update.md)
- [Inventory management](../inventory-management/introduction.md)

>[!IMPORTANT]
>
>Commerce-Services müssen in Crontab installiert werden, um sicherzustellen, dass Kernkomponenten und einige Erweiterungen von Drittanbietern erwartungsgemäß funktionieren. Siehe die [Anweisungen im _Installationshandbuch_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html?lang=de) für detaillierte Informationen über die Installation von Services auf crontab.

Darüber hinaus können Sie Folgendes so konfigurieren, dass es gemäß einem Cron-Zeitplan ausgeführt wird:

- Systemrasteraktualisierungen und -neuindizierung bestellen
- Ausstehende Zahlungsdauer

Stellen Sie sicher, dass [Basis-URLs](../stores-purchase/store-urls.md) für den Store korrekt festgelegt sind, damit die URLs, die während Cron-Vorgängen generiert werden, korrekt sind. Informationen zu Adobe Commerce in Cloud-Infrastrukturen finden Sie unter [Einrichten von Cron](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html?lang=de) im _Handbuch zu Commerce in Cloud-Infrastrukturen_. Für On-Premise siehe [Konfigurieren und Ausführen &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=de)) im _Konfigurationshandbuch_.

## Cron konfigurieren

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Cron]** .

   ![Erweiterte Konfiguration - Cron-Aufgaben](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. Füllen Sie die folgenden Einstellungen für die Gruppen **[!UICONTROL Index]** und **[!UICONTROL Default]** aus.

   Die Einstellungen sind in jedem Abschnitt gleich.

   - **[!UICONTROL Generate Schedules Every]** - Definiert, wie oft der Zeitplan generiert wird (in Minuten). Zeitpläne werden in der Datenbank gespeichert.
   - **[!UICONTROL Schedule Ahead for]** - Definiert, wie weit im Voraus Cron-Aufträge geplant werden (in Minuten). Wenn diese Einstellung beispielsweise auf `10` festgelegt ist und das Cron ausgeführt wird, werden Cron-Aufträge für die nächsten 10 Minuten geplant.
   - **[!UICONTROL Missed if not Run Within]** - Definiert die Zeit (in Minuten), die zum Ermitteln eines verpassten Auftrags verwendet wird. Wenn der Cron-Auftrag nicht zur geplanten Zeit ausgeführt wird und die angegebene Zeit verstrichen ist, kann er nicht ausgeführt werden und sein Status ist auf `Missed` festgelegt.
   - **[!UICONTROL History Cleanup Every]** - Definiert die Zeit (in Minuten), zu der der Verlauf beendeter Aufgaben aus der Datenbank gelöscht wird.
   - **[!UICONTROL Success History Lifetime]** - Definiert die Zeitdauer (in Minuten), die der Verlauf von Cron-Aufträgen mit dem Status `Successful` in der Datenbank verbleibt.
   - **[!UICONTROL Failure History Lifetime]** - Definiert die Zeitdauer (in Minuten), die der Verlauf von Cron-Aufträgen mit dem Status `Error` in der Datenbank verbleibt.
   - **[!UICONTROL Use Separate Process]** - Definiert, ob alle Cron-Aufträge aus der Gruppe in einem separaten Systemprozess ausgeführt werden. Optionen: `Yes` / `No`

   ![Erweiterte Konfiguration - Cron-Gruppenindex](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
