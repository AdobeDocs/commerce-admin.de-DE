---
title: Entwicklertools
description: Erfahren Sie mehr über die erweiterten Entwickler-Tools, die zur Unterstützung von Entwicklern verfügbar sind, die an Anpassungsprojekten arbeiten.
exl-id: 34529aa9-201f-4817-b53b-a15b6a78a923
role: Admin, Developer
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1711'
ht-degree: 0%

---

# Entwicklertools

Verwenden Sie die erweiterten Entwicklertools, um den Kompilierungsmodus während der Frontend-Entwicklung zu bestimmen, eine Zulassungsliste von IP-Adressen zu erstellen und Vorlagenpfadhinweise anzuzeigen. Es gibt auch Tools, mit denen Sie problemlos Textänderungen an Textstellen in der Benutzeroberfläche der Storefront und des Administrators vornehmen können.

- [Aktionsprotokolle](action-log.md) ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce)
- [Frontend-Entwicklungs-Workflow](#frontend-development-workflow)
- [Verwenden statischer Dateisignaturen](#static-file-signatures)
- [Optimierung der Ressourcendatei](#optimizing-resource-files)
- [Entwicklerclientbeschränkungen](#client-restrictions)
- [Hinweise zum Vorlagenpfad](#template-path-hints)
- [Inline übersetzen](#translate-inline)

## Vorgangsmodi

Ihre Adobe Commerce- oder Magento Open Source-Instanz kann bereitgestellt werden, um in einer der beiden _production_ oder _Entwicklermodus_. Auf die Tools und Konfigurationseinstellungen, die speziell für Entwickler entwickelt wurden, kann nur zugegriffen werden, während der Store in ausgeführt wird _Entwicklermodus_.

Der Betriebsmodus kann nur von einem Benutzer mit entsprechenden Berechtigungen über die Befehlszeile des Servers geändert werden. Siehe [Betriebsmodus festlegen](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/set-mode.html) im _Konfigurationshandbuch_ für weitere Informationen.

Die meisten Themen in der Händlerdokumentation gelten für eine Commerce-Instanz, die im Produktionsmodus ausgeführt wird. Die folgenden Konfigurationseinstellungen und Tools können jedoch nur verwendet werden, wenn die Installation im Entwicklermodus ausgeführt wird.

## Frontend-Entwicklungs-Workflow

Der Frontend-Entwicklungs-Workflow-Typ bestimmt, ob während der Entwicklung eine geringere Kompilierung auf Client- oder Server-Seite erfolgt. Less ist eine Erweiterung von CSS mit zusätzlichen Funktionen und Konventionen, die optimierten Code erzeugt. Clientseitige Weniger Kompilierung wird für die Designentwicklung empfohlen. Die serverseitige Kompilierung ist der Standardmodus. Die Optionen des Entwicklungs-Workflows stehen nicht für Stores im Produktionsmodus zur Verfügung.
Siehe [Clientseitige LESS-Kompilierung im Vergleich zur serverseitigen](https://developer.adobe.com/commerce/frontend-core/guide/css/quickstart/compilation-mode/){:target=&quot;_blank&quot;} in der Commerce-Entwicklerdokumentation.

>[!NOTE]
>
>Die Konfiguration des Frontend-Entwicklungs-Workflows ist verfügbar unter [Entwicklermodus](../systems/developer-tools.md#operation-modes) nur.

![Erweiterte Konfiguration - Frontend-Entwicklungs-Workflow](../configuration-reference/advanced/assets/developer-frontend-development-workflow.png){width="600" zoomable="yes"}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL Developer]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Front-end Development Workflow]** Abschnitt.

1. Satz **[!UICONTROL Workflow Type]** auf einen der folgenden Werte zu:

   - `Client side less compilation` - Die Kompilierung erfolgt im Browser mithilfe des nativen `less.js` -Bibliothek.
   - `Server side less compilation` - Die Kompilierung erfolgt auf dem Server mithilfe der Bibliothek Less PHP. Dies ist der Standardmodus für die Produktion.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Statische Dateisignaturen

Durch Hinzufügen einer digitalen Signatur zur URL statischer Dateien können Browser erkennen, wann eine neuere Version der Datei verfügbar ist. Statische Dateien, die mit digitalen Signaturen verfolgt werden können, umfassen JavaScript, CSS, Bilder und Schriftarten. Die Signatur wird direkt nach der Basis-URL an den Pfad angehängt. Wenn sich die Signatur einer Datei von der im Cache des Browsers gespeicherten Signatur unterscheidet, wird die neuere Version der Datei verwendet.

Siehe [Statische Inhaltssignatur](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/static-content-signing.html){:target=&quot;_blank&quot;} in der Commerce-Entwicklerdokumentation.

>[!NOTE]
>
>Die Konfiguration der statischen Dateieinstellungen ist nur verfügbar, wenn Sie in [Entwicklermodus](../systems/developer-tools.md#operation-modes).

![Erweiterte Konfiguration - Einstellungen für statische Dateien](../configuration-reference/advanced/assets/developer-static-files-settings.png){width="600" zoomable="yes"}

Eine detaillierte Liste der Konfigurationseinstellungen finden Sie unter [_Statische Dateieinstellungen_](../configuration-reference/advanced/developer.md) im _Konfigurationsreferenz_.

**_So aktivieren Sie signierte statische Dateien:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL Developer]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Static Files Settings]** Abschnitt.

1. Satz **[!UICONTROL Sign Static Files]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Optimierung der Ressourcendatei

Die zum Laden von Ressourcendateien benötigte Zeit kann durch Zusammenführen und Bündeln von Dateien und Minimieren von Code verringert werden.

- Beim Zusammenführen werden separate Dateien desselben Typs in einer einzigen Datei zusammengefasst.
- Bundling ist eine Technik, die separate Dateien gruppiert, um die Anzahl der HTTP-Anfragen zu reduzieren, die zum Laden einer Seite erforderlich sind.
- Die Minimierung entfernt Leerzeichen, Zeilenumbrüche und Kommentare, wirkt sich jedoch nicht auf die Funktionalität des Codes aus. Da minimierte Dateien nicht bearbeitet werden können, sollte der Prozess nur angewendet werden, wenn Sie bereit sind, in die Produktion zu wechseln.

Standardmäßig führen Adobe Commerce und Magento Open Source keine Dateien zusammen, bündeln sie nicht oder minimieren sie. Der Projektentwickler sollte festlegen, welche Dateioptimierungsmethoden verwendet werden sollen.

Siehe [Best Practices bei der Leistung](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/overview.html) für weitere Informationen.

>[!NOTE]
>
>CSS- und JavaScript-Dateien können in [Entwicklermodus](../systems/developer-tools.md#operation-modes) nur.

| Dateityp | Unterstützte Vorgänge |
| --------------- | -------------------- |
| CSS-Dateien | `MergeMinify` |
| JavaScript-Dateien | `MergeBundleMinify` |
| Vorlagendateien | `Minify` |

{style="table-layout:auto"}

**_Optimierung der Ressourcendateien:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL Developer]**.

1. Um CSS-Dateien zu optimieren, erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL CSS Settings]** und führen Sie folgende Schritte aus:

   - Satz **[!UICONTROL Merge CSS Files]** nach `Yes`.
   - Satz **[!UICONTROL Minify CSS Files]** nach `Yes`.

   ![Erweiterte Konfiguration - CSS-Einstellungen](../configuration-reference/advanced/assets/developer-css-settings.png){width="600" zoomable="yes"}

[_CSS Settings_](../configuration-reference/advanced/developer.md)

1. Um JavaScript-Dateien zu optimieren, erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL JavaScript Settings]** und führen Sie folgende Schritte aus:

   - Satz **[!UICONTROL Merge JavaScript Files]** nach `Yes`.
   - Satz **[!UICONTROL Minify JavaScript Files]** nach `Yes`.

   ![Erweiterte Konfiguration - JavaScript-Einstellungen](../configuration-reference/advanced/assets/developer-javascript-settings.png){width="600" zoomable="yes"}

1. Erweitern Sie zum Minimieren von PHTML-Vorlagendateien ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Template Settings]** Abschnitt und Satz **[!UICONTROL Minify Html]** nach `Yes`.

   ![Erweiterte Konfiguration - Vorlageneinstellungen](../configuration-reference/advanced/assets/developer-template-settings.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Kundenbeschränkungen

Vor der Verwendung eines Tools wie [Vorlagenpfadhinweise](#template-path-hints), stellen Sie sicher, dass Sie Ihre IP-Adresse zur Zulassungsliste &quot;Developer Client Restrictions&quot;hinzufügen, um zu verhindern, dass das Einkaufserlebnis von Kunden im Store gestört wird. Wenn Sie Ihre IP-Adresse nicht kennen, können Sie online danach suchen.

>[!NOTE]
>
>Entwickler-Client-Einschränkungen können in [Entwicklermodus](../systems/developer-tools.md#operation-modes) nur.

Technische Informationen finden Sie unter [Benutzerdefinierte VCL für das Zulassen von Anforderungen](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/custom-vcl-snippets/fastly-vcl-allowlist.html) im _Benutzerhandbuch zu Commerce on Cloud Infrastructure_.

**_So fügen Sie Ihre IP-Adresse zur Zulassungsliste hinzu:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL Developer]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Developer Client Restrictions]** Abschnitt.

   ![Erweiterte Konfiguration - Client-Beschränkungen für Entwickler](../configuration-reference/advanced/assets/developer-developer-client-restrictions.png){width="600" zoomable="yes"}

1. Für **[!UICONTROL Allow IPs]**, geben Sie Ihre IP-Adresse ein.

   Wenn der Zugriff über mehrere IP-Adressen erforderlich ist, trennen Sie jede durch ein Komma.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

1. Aktualisieren Sie bei Aufforderung alle ungültigen Caches.

## Hinweise zum Vorlagenpfad

Vorlagenpfadhinweise sind ein Diagnosetool, das Notation mit dem Pfad zu jeder Vorlage hinzufügt, die auf der Seite verwendet wird. Vorlagenpfadhinweise können entweder für die Storefront oder für den Administrator aktiviert werden.

>[!NOTE]
>
>Vorlagenpfadhinweise können in [Entwicklermodus](../systems/developer-tools.md#operation-modes) nur.

Siehe [Suchen nach Vorlagen, Layouts und Stilen](https://developer.adobe.com/commerce/frontend-core/guide/themes/debug/){:target=&quot;_blank&quot;} in der Commerce-Entwicklerdokumentation.

![Beispiel-Storefront - Hinweise zum Vorlagenpfad](./assets/storefront-template-path-hints.png){width="700" zoomable="yes"}

### Schritt 1: Hinzufügen Ihrer IP-Adresse zur Zulassungsliste &quot;&quot;

Bevor Sie Vorlagenpfadhinweise verwenden, fügen Sie Ihre IP-Adresse zum [Zulassungsliste](#client-restrictions) um Störungen mit Kunden zu vermeiden, die im Geschäft einkaufen. Wenn Sie fertig sind, müssen Sie den Commerce-Cache löschen, um alle Hinweise aus dem Store zu entfernen.

![Erweiterte Konfiguration - Client-Beschränkungen für Entwickler](../configuration-reference/advanced/assets/developer-developer-client-restrictions.png){width="600" zoomable="yes"}

### Schritt 2: Vorlagenpfadhinweise aktivieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL Developer]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Debug]** und führen Sie folgende Schritte aus:

   ![Erweiterte Konfiguration - debug](../configuration-reference/advanced/assets/developer-debug.png){width="600" zoomable="yes"}

   - Um Vorlagenpfadhinweise für den Store zu aktivieren, legen Sie **[!UICONTROL Enabled Template Path Hints for Storefront]** nach `Yes`.

   - So aktivieren Sie Vorlagenpfadhinweise nur für den Store, wenn die URL die `templatehints` Parameter, festlegen **Hinweise für Storefront mit URL-Parameter aktivieren** nach `Yes`. Legen Sie dann bei Bedarf einen Wert für den Parameter fest. Der Standardwert ist `magento`, Sie können jedoch einen benutzerdefinierten Wert verwenden. Wenn Sie beispielsweise den Wert in `lorem`, verwenden Sie `mymagento.com?templatehints=lorem` , um Vorlagenhinweise anzuzeigen.

   - Um Vorlagenpfadhinweise für den Administrator zu aktivieren, legen Sie **[!UICONTROL Enabled Template Path Hints for Admin]** nach `Yes`.

   - Um die Namen der Blöcke einzuschließen, legen Sie **[!UICONTROL Add Block Class Type to Hints]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### Schritt 3: Cache löschen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Flush Magento Cache]**.

## Inline übersetzen

Sie können das Tool Inline übersetzen in [Entwicklermodus](../systems/developer-tools.md#operation-modes) um Text in der Benutzeroberfläche zu berühren, um Ihre Stimme und Marke widerzuspiegeln. Wenn der Modus Inline übersetzen aktiviert ist, wird jeder Text auf der Seite, der bearbeitet werden kann, rot dargestellt. Sie können Feldbezeichnungen, Nachrichten und anderen Text, der in der Storefront und im Admin-Bereich angezeigt wird, einfach bearbeiten. Viele Designs verwenden beispielsweise Terminologie wie _Mein Konto_, _Meine Wunschliste_, und _Mein Dashboard_, um Kunden bei der Umgehung zu unterstützen. Sie können jedoch die Wörter lieber einfach verwenden _Konto_, _Wunschliste_, und _Dashboard_.

>[!NOTE]
>
>Das Tool Inline übersetzen ist nur verfügbar, wenn Sie in [Entwicklermodus](../systems/developer-tools.md#operation-modes).

Siehe [Übersetzungen - Übersicht](https://developer.adobe.com/commerce/frontend-core/guide/translations/) in der Commerce-Entwicklerdokumentation.

![Beispiel-Storefront - übersetzbarer Text](./assets/storefront-translate-inline.png){width="700" zoomable="yes"}

Wenn Ihr Store in mehreren Sprachen verfügbar ist, können Sie feine Anpassungen am übersetzten Text für das Gebietsschema vornehmen. Auf dem Server wird der Schnittstellentext in einer separaten CSV-Datei für jeden Ausgabeblock verwaltet und nach Gebietsschema geordnet. als alternativen Ansatz, anstatt die _Inline übersetzen_ können Sie die CSV-Dateien auch direkt auf dem Server bearbeiten. Übersetzungsdateien werden in `app/code/Magento/<module_name>/i18n/<language_locale>.csv`.

>[!NOTE]
>
>Um das Tool Inline übersetzen verwenden zu können, muss Ihr Browser Popup-Fenster zulassen.

### Schritt 1: Ausgabecache deaktivieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. Aktivieren Sie die folgenden Kontrollkästchen:

   - `Blocks HTML output`
   - `Page Cache`
   - `Translations`

1. Legen Sie die **[!UICONTROL Actions]** Kontrolle an `Disable` und klicken **[!UICONTROL Submit]**.

### Schritt 2: Aktivieren des Tools &quot;Inline übersetzen&quot;

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Um mit einer bestimmten Store-Ansicht zu arbeiten, legen Sie die **[!UICONTROL Store View]** aktualisiert werden.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL Developer]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Translate Inline]** Abschnitt.

   Löschen Sie die **[!UICONTROL Use Website]** nach Bedarf, um diese Einstellungen zu ändern.

   Die _[!UICONTROL Enabled for Admin]_ist beim Bearbeiten einer bestimmten Store-Ansicht nicht verfügbar.

   ![Erweiterte Konfiguration - Inline-Übersetzung](../configuration-reference/advanced/assets/developer-translate-inline.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Enabled for Storefront]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

1. Aktualisieren Sie bei entsprechender Aufforderung die ungültigen Caches, aber lassen Sie die deaktivierten Caches unverändert.

### Schritt 3: Text aktualisieren

1. Öffnen Sie Ihre Storefront in einem Browser und rufen Sie die Seite auf, die Sie bearbeiten möchten.

   Verwenden Sie bei Bedarf die Sprachauswahl, um die Store-Ansicht zu ändern. Jede Textzeichenfolge, die übersetzt werden kann, ist rot dargestellt. Wenn Sie den Mauszeiger über ein Textfeld bewegen, wird ein Buchsymbol ( ![Symbol &quot;Buch&quot;](../assets/icon-book.png) ) angezeigt.

1. Klicken Sie auf das Buchsymbol, um die _Übersetzen_ und gehen Sie wie folgt vor:

   - Wenn die Änderung für die spezifische Store-Ansicht gilt, wählen Sie die **[!UICONTROL Store View Specific]** aktivieren.

   - Geben Sie den neuen **[!UICONTROL Custom]** Text.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Submit]**.

   ![Benutzerdefinierten Text eingeben](./assets/storefront-translate-inline-detail.png){width="700" zoomable="yes"}

1. Um Ihre Änderungen im Store anzuzeigen, aktualisieren Sie den Browser.

1. Wiederholen Sie diesen Vorgang für alle Elemente im Store, die geändert werden sollen.

### Schritt 4: Wiederherstellen der ursprünglichen Einstellungen

1. Kehren Sie zum Administrator Ihres Stores zurück.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Satz **[!UICONTROL Store View]** in die jeweilige Ansicht, die bearbeitet wurde.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL Developer]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Translate Inline]** Abschnitt.

1. Satz **[!UICONTROL Enabled for Frontend]** nach `No`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. Aktivieren Sie das Kontrollkästchen der folgenden ausgehenden Zwischenspeicher, die zuvor deaktiviert waren:

   - `Blocks HTML output`
   - `Page Cache`
   - `Translations`

1. Legen Sie die **[!UICONTROL Actions]** Kontrolle an `Enable` und klicken **[!UICONTROL Submit]**.

1. Aktualisieren Sie bei Aufforderung alle ungültigen Caches.

### Schritt 5: Überprüfen der Änderungen in Ihrem Store

Gehen Sie zu Ihrer Storefront und überprüfen Sie jede Seite, die aktualisiert wurde, um sicherzustellen, dass die Änderungen korrekt sind. In diesem Beispiel `Customer Login` wurde geändert in `Customer Sign In`. Wenn Änderungen an einer bestimmten Ansicht vorgenommen wurden, verwenden Sie die Sprachauswahl, um zur richtigen Ansicht zu wechseln.

![Beispiel-Storefront - Anmeldung eines übersetzten Kunden](./assets/storefront-translate-inline-customer-sign-in.png){width="700" zoomable="yes"}
