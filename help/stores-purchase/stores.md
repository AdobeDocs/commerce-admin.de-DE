---
title: Store- und Site-Struktur
description: Erfahren Sie mehr über die Hierarchie der Website-, Store- und Store-Ansicht.
exl-id: d745cbd0-151b-4f82-bb6c-fb6b9565a014
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# Store- und Site-Struktur

Wenn Adobe Commerce oder Magento Open Source installiert ist, wird eine Hierarchie mit einer Haupt-Website-, Store- und Store-Ansicht erstellt. Sie können bei Bedarf weitere Websites, Stores und Ansichten erstellen. Beispielsweise könnten Sie zusätzlich zu Ihrer Haupt-Website zusätzliche Websites mit einer anderen Domäne haben. Innerhalb jeder Website können Sie über mehrere Stores und innerhalb jedes Stores separate Store-Ansichten verfügen. Viele Installationen verfügen über eine Website und einen Store, jedoch mit mehreren Store-Ansichten, um verschiedene Sprachen zu unterstützen.

Bevor Sie beginnen, planen Sie die Hierarchie Ihres Store-Katalogs im Voraus, da sie in der gesamten Konfiguration referenziert wird. Jeder Store kann über eine separate [Stammkategorie](../catalog/category-root.md) verfügen, die es ermöglicht, für jeden Store einen völlig anderen Satz von Hauptmenüoptionen zu verwenden.

![Perimeterdiagramm](./assets/scope-multisite.svg){width="550"}

## Stores hinzufügen

Eine einzelne Installation von Adobe Commerce oder Magento Open Source kann über mehrere Stores verfügen, die einen Administrator gemeinsam nutzen. Stores, die sich unter derselben Website befinden, haben dieselbe IP-Adresse und Domäne, verwenden dasselbe Sicherheitszertifikat und geben einen einzigen Checkout-Prozess frei.

Wichtig ist, dass die Stores denselben Code verwenden und einen Administrator gemeinsam nutzen. Jeder Store kann über einen separaten Katalog verfügen oder die Stores können einen Katalog freigeben. Jeder Store kann über eine separate [Stammkategorie](../catalog/category-root.md) verfügen, die es ermöglicht, für jeden Store ein anderes Hauptmenü zu verwenden. Stores können auch unterschiedliche Marken, Präsentationen und Inhalte aufweisen. Nehmen Sie sich etwas Zeit, um Ihre Store-Hierarchie mit Blick auf zukünftiges Wachstum zu planen, bevor Sie beginnen, da sie während der gesamten Konfiguration verwendet wird.

![Umfang - mehrere Stores](./assets/scope-multistore.svg){width="550"}

Im Folgenden finden Sie einige Beispiele dafür, wie URLs für mehrere Stores konfiguriert werden können:

| URL | Beschreibung |
| --- | ----------- |
| `yourdomain.com/store1`<br>`yourdomain.com/store2` | Jeder Store hat einen anderen Pfad, gibt aber eine Domäne frei. |
| `store1.yourdomain.com`<br>`store2.yourdomain.com` | Jeder Store hat eine andere Subdomäne der primären Domäne. |

Multi-Store-Installationen von Adobe Commerce müssen über den Administrator und auch über die Befehlszeile des Servers konfiguriert werden. Das Adobe Commerce [Konfigurationshandbuch](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) enthält detaillierte Anweisungen zum Konfigurieren der Serverumgebung.

### Schritt 1: Auswählen der Store-Domäne

Der erste Schritt besteht darin, festzulegen, wie Sie den Store positionieren möchten. Sollten die Stores eine Domäne teilen, jede über eine Subdomäne verfügen oder unterschiedliche Domänen haben? Führen Sie für jeden Store einen der folgenden Schritte aus:

- Um den Store auf einer Ebene unterhalb der primären Domäne zu platzieren, müssen Sie nichts unternehmen.
- Richten Sie eine Subdomäne Ihrer primären Domäne ein.
- Richten Sie eine andere primäre Domäne ein.

### Schritt 2: Erstellen des Stores

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Klicken Sie auf **[!UICONTROL Create Store]** und legen Sie die Optionen für den neuen Store fest:

   - **[!UICONTROL Web Site]** - Wählen Sie eine Website aus, die dem neuen Store übergeordnet sein soll. Wenn die Installation nur eine Website enthält, akzeptieren Sie die Standardeinstellung (`Main Website`).

   - **[!UICONTROL Name]** - Geben Sie einen Namen für den neuen Store ein. Der Name dient nur als interne Referenz.

   - **[!UICONTROL Code]** - Geben Sie einen Code in Kleinbuchstaben ein, um den Store zu identifizieren. Beispiel: `mainstore`.

   - **[!UICONTROL Root Category]** - Wird auf die [Stammkategorie](../catalog/category-root.md) gesetzt, die die Kategoriestruktur für das Hauptmenü des neuen Stores definiert. Wenn Sie bereits eine bestimmte Stammkategorie für den Store erstellt haben, wählen Sie diese aus. Wählen Sie andernfalls `Default Category` aus. Sie können später zurückkehren und die Einstellung aktualisieren.

   ![Store erstellen - Speicheroptionen](./assets/stores-all-store-information.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Store]**.

### Schritt 3: Erstellen einer standardmäßigen Store-Ansicht

1. Klicken Sie auf **[!UICONTROL Create Store View]** und legen Sie die Optionen für die Store-Ansicht fest:

   - **[!UICONTROL Store]** - Stellen Sie auf den neuen Store ein, den Sie erstellt haben.

   - **[!UICONTROL Name]** - Geben Sie einen Namen für die Ansicht ein. Beispiel: `English`.

   - **[!UICONTROL Code]** - Geben Sie einen Code für die Ansicht in Kleinbuchstaben ein.

   - **[!UICONTROL Status]** - Auf `Enabled` setzen.

   - **[!UICONTROL Sort Order]** - Geben Sie eine Zahl ein, um die Position des Stores bei der Liste mit anderen Stores zu bestimmen.

1. Klicken Sie auf **[!UICONTROL Save Store View]**.

   Wenn Sie Ihren Store im Bearbeitungsmodus öffnen, können Sie sehen, dass er jetzt über eine Standardansicht verfügt.

   ![Neuer Speicher mit Standardansicht](./assets/new-store-default-view.png){width="600" zoomable="yes"}

### Schritt 4: Konfigurieren der Store-URL

1. Klicken Sie in der Seitenleiste _Admin_ auf **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich unter &quot;_[!UICONTROL General]_&quot;die Option &quot;**[!UICONTROL Web]**&quot;.

1. Setzen Sie oben links **[!UICONTROL Store View]** auf die Ansicht, die Sie für den neuen Store erstellt haben.

1. Wenn Sie aufgefordert werden, den Umschalter für [Gültigkeitsbereich](../getting-started/websites-stores-views.md#scope-settings) zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

   ![Auswählen der Store-Ansicht](./assets/create-store-config-view.png){width="600" zoomable="yes"}

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Base URLs]** und geben Sie die Basis-URL für den Store ein.

   Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** , um die Einstellung zu ändern.

   ![Allgemeine Konfiguration - Web-Basis-URLs](./assets/config-general-web-base-urls-clear-checkbox.png){width="600" zoomable="yes"}

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Secure Base URLs]** und wiederholen Sie den vorherigen Schritt, wenn Sie die sichere [URL](store-urls.md) für den Speicher konfigurieren möchten.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

### Schritt 5: Server konfigurieren

Informationen zum Konfigurieren des Servers für die Unterstützung mehrerer Websites finden Sie unter [Mehrere Websites oder Stores](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) im _Konfigurationshandbuch_.

Hilfe zur Konfiguration Ihres Webservers finden Sie in den folgenden Ressourcen:

- [Einrichten mehrerer Websites mit NGNX](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-nginx.html)
- [Einrichten mehrerer Websites mit Apache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-apache.html)

Informationen zu Adobe Commerce in der Cloud-Infrastruktur finden Sie unter [Einrichten mehrerer Websites oder Stores](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/multiple-sites.html).

## Websites hinzufügen

Mehrere Websites können in einer einzigen Adobe Commerce- oder Magento Open Source-Installation mit derselben Domäne oder unterschiedlichen Domänen eingerichtet werden. Standardmäßig haben Stores, die sich unter derselben Website befinden, dieselbe IP-Adresse und Domäne, verwenden dasselbe Sicherheitszertifikat und teilen einen einzigen Checkout-Prozess. Wenn Sie möchten, dass jeder Store über einen dedizierten Checkout-Prozess unter seiner eigenen Domäne verfügt, muss jeder Store über eine eigene IP-Adresse und ein separates Sicherheitszertifikat verfügen.

Multi-Site-Installationen von Adobe Commerce oder Magento Open Source müssen vom Administrator und auch über die Befehlszeile des Servers konfiguriert werden. Das Commerce [Konfigurationshandbuch](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) enthält detaillierte Anweisungen zum Konfigurieren der Serverumgebung.

![Umfang - Websites](./assets/scope-multisite.svg){width="550"}

### Schritt 1: Erstellen einer Website

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Create Website]**.

1. Legen Sie die **[!UICONTROL Web Site Information]** -Optionen fest:

   ![Website erstellen - options](./assets/create-website-info.png){width="600" zoomable="yes"}

   - **[!UICONTROL Name]** - Geben Sie die Domäne der neuen Website ein. Beispiel: `domain.com`.

   - **[!UICONTROL Code]** - Geben Sie einen Code ein, der auf dem Server verwendet wird, um auf die Domäne zu verweisen.

     Der Code muss mit einem Kleinbuchstaben (a-z) beginnen und kann eine beliebige Kombination aus Buchstaben (a-z), Zahlen (0-9) und dem Unterstrich (_) enthalten.

   - **[!UICONTROL Sort Order]** - _(Optional)_ Geben Sie eine Zahl ein, um die Sequenz zu bestimmen, in der diese Site mit anderen Sites aufgeführt ist. Damit diese Site oben in der Liste angezeigt wird, geben Sie eine Null (`0`) ein.

1. Klicken Sie auf **[!UICONTROL Save Web Site]**.

1. Richten Sie die einzelnen [store](#add-stores)- und [Store-Ansichten](store-views.md) ein, die für die neue Website erforderlich sind.

   Anschließend können Sie die Website im Bearbeitungsmodus öffnen, um den Standardspeicher festzulegen.

### Schritt 2: Konfigurieren der Store-URL

Befolgen Sie die Anweisungen, um die [Store-URLs](store-urls.md) zu konfigurieren.

### Schritt 3: Server konfigurieren

Informationen zum Konfigurieren des Servers für die Unterstützung mehrerer Websites finden Sie unter [Mehrere Websites oder Stores](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) im _Konfigurationshandbuch_.

Hilfe zur Konfiguration Ihres Webservers finden Sie in den folgenden Tutorials:

- [Einrichten mehrerer Websites mit NGNX](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-nginx.html)
- [Einrichten mehrerer Websites mit Apache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-apache.html)

Informationen zu Adobe Commerce in der Cloud-Infrastruktur finden Sie unter [Einrichten mehrerer Websites oder Stores](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/multiple-sites.html).
