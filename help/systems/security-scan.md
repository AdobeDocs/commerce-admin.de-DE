---
title: Sicherheitsüberprüfung
description: Erfahren Sie, wie Sie eine erweiterte Sicherheitsüberprüfung durchführen und jede Ihrer Adobe Commerce- und Magento Open Source-Sites überwachen.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: fa3931d4aaa5e7b903a17ec074703d2c8130c71d
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 0%

---


# Sicherheitsüberprüfung

Das Adobe Commerce Security Scan Tool bietet eine kostenlose Sicherheitsüberwachung für Ihre Adobe Commerce- und Magento Open Source-Sites. Das Tool funktioniert als webbasierter Service, auf den Sie über Ihr Adobe Commerce-Online-Konto unter [account.magento.com](https://account.magento.com/customer/account/login) zugreifen können.

![Sicherheits-Scan-Tool](./assets/magento-security-scan.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Adobe bietet diesen Service kostenlos an. Händler müssen jedoch Bedingungen akzeptieren, die die Haftung von Adobe auf der Grundlage von Suchergebnissen und der Website-Konfiguration einschränken.

## Abdeckung scannen

Das Security Scan Tool arbeitet sowohl über HTTP- als auch über HTTPS-Protokolle, um Malware zu erkennen, Sicherheitslücken zu erkennen und den Sicherheitszustand Ihres Stores zu erhalten. Das Tool steht allen Händlern, Entwicklern und dem für die Site-Sicherheit verantwortlichen Personal zur Verfügung.

Das Security Scan Tool bietet umfassende Sicherheitsüberwachungsfunktionen, mit denen Sie eine sichere Speicherumgebung aufrechterhalten können:

- Erhalten Sie mit insight einen Echtzeitsicherheitsstatus Ihres Stores.
- Erhalten Sie Vorschläge auf der Grundlage von Best Practices, die Sie bei der Lösung von Problemen unterstützen.
- Planen Sie die Ausführung einer Sicherheitsprüfung wöchentlich, täglich oder nach Bedarf.
- Führen Sie über 21.000 Sicherheitstests durch, um potenzielle Malware zu identifizieren.
- Zugriff auf historische Sicherheitsberichte, die den Fortschritt Ihrer Sites verfolgen und überwachen.
- Greifen Sie mit allen empfohlenen Aktionen auf den Scanbericht zu, der erfolgreiche und fehlgeschlagene Prüfungen anzeigt.

>[!NOTE]
>
>Bestimmte Sicherheitstests können bei der Suche des Security Scan Tools nach Adobe Commerce nicht ausgeschlossen werden. Sie können sich jedoch ggf. selbst [, indem Sie ](#manage-scan-failures) als falsch positiv kennzeichnen.

## Zugriff

Das Security Scan Tool schützt Ihre Website-Daten mit strengen Zugriffskontrollen. Nur Sie können Ihre Site scannen, da das Tool die Domain-Eigentümerschaft über Ihr Adobe Commerce-Konto verifizieren muss. Jede Site stellt über ein eindeutiges Token eine Verbindung zu Ihrem Konto her und verhindert so das unbefugte Scannen durch Dritte.

Das Tool konzentriert sich speziell auf Adobe Commerce-Domains und deren Sicherheitslücken. Ihr Webstore kann zwar Seiten von anderen Plattformen enthalten, das Security Scan Tool sollte jedoch nur Adobe Commerce-generierte Inhalte scannen, um zuverlässige Ergebnisse zu erzielen. Das Scannen von Nicht-Adobe Commerce-Seiten kann zu unzuverlässigen Schwachstellenbewertungen führen.

## Ausführen eines Scans

Der Scan-Prozess überprüft Ihre Site auf bekannte Sicherheitsprobleme und identifiziert fehlende Adobe Commerce-Patches und -Updates, die Ihren Store für Angriffe anfällig machen könnten.

>[!TIP]
>
>Informationen zu Commerce in Cloud-Infrastrukturprojekten finden Sie unter [Einrichten des Sicherheits-Scan-Tools](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/launch/overview#set-up-the-security-scan-tool).

So führen Sie eine Suche durch:

1. Melden Sie sich auf der Commerce-Startseite bei Ihrem [Commerce/Magento-Konto an](../getting-started/commerce-account-create.md).

1. Lesen und akzeptieren Sie die Bedingungen für die Verwendung des Security Scan Tools.

   1. Wählen Sie im linken Bedienfeld **[!UICONTROL Security Scan]** aus.
   1. Klicken Sie auf **[!UICONTROL Go to Security Scan]**.
   1. Lies die **[!UICONTROL Terms and Conditions]**.
   1. Zum Fortfahren auf **[!UICONTROL Agree]** klicken.

1. Klicken Sie auf der _[!UICONTROL Monitored Websites]_Seite auf **[!UICONTROL +Add Site]**.

   Wenn Sie mehrere Websites mit unterschiedlichen Domains haben, konfigurieren Sie für jede Domain einen separaten Scan.

   ![Überwachte Sites](./assets/monitored-website.png){width="600" zoomable="yes"}

1. Um zu überprüfen, ob Sie der Eigentümer der Website-Domain sind, indem Sie einen Bestätigungscode hinzufügen, führen Sie einen der folgenden Schritte aus:

   **Commerce-Storefront**:

   1. Geben Sie den **[!UICONTROL Site URL]** und die **[!UICONTROL Site Name]** ein.
   1. Klicken Sie auf **[!UICONTROL Generate Confirmation Code]**.
   1. Klicken Sie **Kopieren**, um Ihren Bestätigungs-Code in die Zwischenablage zu kopieren.

      ![Bestätigungs-Code generieren](./assets/scan-site1.png){width="400" zoomable="yes"}

   1. Melden Sie sich beim Administrator Ihres Stores als Benutzer mit vollständigen Administratorrechten an und führen Sie die folgenden Schritte aus:

      1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      1. Suchen Sie Ihre Site in der Liste und klicken Sie auf **[!UICONTROL Edit]**.
      1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL HTML Head]** .
      1. Scrollen Sie nach unten zu **[!UICONTROL Scripts and Style Sheets]** und klicken Sie in das Textfeld am Ende eines vorhandenen Codes. Fügen Sie den Bestätigungscode in das Textfeld ein.

         ![Skripte und Stylesheets](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      1. Klicken Sie abschließend auf **[!UICONTROL Save Configuration]**.

   **PWA-Storefront**:

   1. Geben Sie den **[!UICONTROL Site URL]** und die **[!UICONTROL Site Name]** ein.

   1. Wählen Sie **[!UICONTROL Confirmation Code]** die Option `META Tag` aus und klicken Sie dann auf **[!UICONTROL Generate Code]**.

   1. Klicken Sie auf **[!UICONTROL Copy]** , um das generierte Bestätigungs-Code-META-Tag in die Zwischenablage zu kopieren.

      ![Bestätigungs-Code generieren](./assets/scan-site2.png){width="400" zoomable="yes"}

   1. Gehen Sie zum Projektverzeichnis der PWA Studio-Storefront und gehen Sie folgendermaßen vor:

      1. Wechseln Sie im PWA Studio-Projektverzeichnis zu `packages > venia-concept > template.html`.
      1. Fügen Sie den kopierten Bestätigungs-Code (das generierte META-Tag) zum HTML-Head hinzu und speichern Sie die Änderungen.

         ![Bestätigungs-Code kopieren](./assets/code-pwa.png){width="600" zoomable="yes"}

      1. Kehren Sie zur PWA Studio-CLI zurück, installieren Sie mithilfe von „Garn“ die Projektabhängigkeiten und führen Sie den Projekterstellungsbefehl aus.

         ```sh
         yarn install &&
         yarn build
         ```

      1. *Erstellen Sie* Cloud-Projekt einen `pwa` Ordner und kopieren Sie den Inhalt in den `dist` Ordner Ihres Storefront-Projekts.

         ```sh
         mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
         ```

      1. Verwenden Sie das Git-CLI-Tool, um diese Änderungen zu testen, zu übertragen und in Ihr Cloud-Projekt zu übertragen.

         ```sh
         git add . &&
         git commit -m "Added storefront file bundles" &&
         git push origin
         ```

         Nach Abschluss des Build-Prozesses werden die Änderungen an Ihrer PWA-Storefront bereitgestellt.

1. Kehren Sie zur Seite _[!UICONTROL Security Scan]_in Ihrem Commerce-Konto zurück und klicken Sie auf **[!UICONTROL Verify Confirmation Code]**, um die Eigentümerschaft an der Domain herzustellen.

1. Konfigurieren Sie nach erfolgreicher Bestätigung die **[!UICONTROL Set Automatic Security Scan]** für einen der folgenden Typen:

   **Wöchentlicher Scan (empfohlen)**:

   Wählen Sie **[!UICONTROL Week Day]**, **[!UICONTROL Time]** und **[!UICONTROL Time Zone]** aus, dass der Scan jede Woche durchgeführt werden soll.

   Standardmäßig ist der Scan so geplant, dass er jede Woche um Mitternacht Samstag (UTC) beginnt und bis zum frühen Sonntag fortgesetzt wird.

   ![Wöchentlicher Scan](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **Tägliche Suche**:

   Wählen Sie die **[!UICONTROL Time]** aus und **[!UICONTROL Time Zone]** Sie, dass der Scan jeden Tag stattfinden soll.

   Standardmäßig ist der Beginn der Suche für jeden Tag um Mitternacht (UTC) geplant.

   ![Tägliche Suche](./assets/scan-daily.png){width="500" zoomable="yes"}

1. Geben Sie die **[!UICONTROL Email Address]** ein, in der Sie Benachrichtigungen über abgeschlossene Suchvorgänge und Sicherheits-Updates erhalten möchten.

   ![E-Mail-](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Submit]**.

   Nachdem das Eigentum an der Domain überprüft wurde, wird die Site in der Liste Überwachte Websites Ihres Commerce-Kontos angezeigt.

1. Wenn Sie mehrere Websites mit unterschiedlichen Domains haben, wiederholen Sie diesen Vorgang, um für jede Website eine Sicherheitsprüfung einzurichten.

## Suchfehler verwalten

Mit dem Security Scan Tool können Sie Suchfehler direkt in der Berichtsansicht verwalten. Sie können bestimmte Überprüfungsfehler als falsch positiv markieren und aus Ihrer Risikobewertung ausschließen.

### Vorteile bei der Verwaltung von Scanfehlern

Die Verwaltung von Suchfehlern hilft Ihnen, eine genauere Sicherheitsübersicht über Ihren Store zu erhalten, indem:

- Reduzierung von Fehlalarmen in Ihren Sicherheitsberichten.
- Konzentration auf relevante Sicherheitsprobleme, die Aufmerksamkeit erfordern.
- Pflegen einer klareren Übersicht über den tatsächlichen Sicherheitsstatus Ihres Stores.
- Die Notwendigkeit, den Support bei bekannten falsch positiven Ergebnissen zu kontaktieren, entfällt.
- Zeitersparnis durch die Selbstverwaltung von bereits untersuchten Scan-Fehlern.

Häufige Szenarien, in denen Sie einen Scan-Fehler als falsch positiv markieren können, sind:

- Wenn Sie bereits einen Sicherheits-Patch angewendet haben, den das Scan-Tool nicht erkannt hat.
- Wenn ein erkanntes Problem nicht auf Ihre spezifische Store-Konfiguration zutrifft.
- Wenn Sie eine alternative Sicherheitsmaßnahme implementiert haben, mit der das Problem behoben wird.
- Wenn der Überprüfungsfehler auf einer Konfiguration basiert, die Sie absichtlich für Ihre Geschäftsanforderungen festgelegt haben.

### Scan-Fehler ignorieren

Gehen Sie wie folgt vor, um Scanfehler zu verwalten, die als falsch positiv identifiziert wurden:

1. Klicken Sie auf der Seite _[!UICONTROL Monitored Websites]_auf **[!UICONTROL View Report]**für die Site, die Sie verwalten möchten.

1. Suchen Sie in der Berichtsansicht den fehlgeschlagenen Scan, den Sie als falsch positiv markieren möchten.

1. Klicken Sie auf **[!UICONTROL Ignore]**, um den jeweiligen Scan-Fehler anzuzeigen.

   ![Suchfehler ignorieren](assets/security-scan-ignore-failure.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Apply Changes]** , um Ihre Auswahl zu speichern.

Der ignorierte Überprüfungsfehler wird in den Abschnitt &quot;_[!UICONTROL Ignored Results]_&quot; verschoben und von der Risikobewertung ausgeschlossen.

### Suchfehler nicht mehr ignorieren

Führen Sie die folgenden Schritte aus, um einen zuvor ignorierten Überprüfungsfehler auf Ihrer aktiven Überwachung wiederherzustellen:

1. Scrollen Sie in der Berichtsansicht zum Abschnitt _[!UICONTROL Ignored Results]_.

1. Klicken Sie auf **[!UICONTROL Stop Ignoring]** für den Suchfehler, den Sie wiederherstellen möchten.

   ![Suchfehler ignorieren](assets/security-scan-stop-ignoring-failure.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Apply Changes]** , um Ihre Auswahl zu speichern.

Der Scan-Fehler wird wieder in den Abschnitt _[!UICONTROL Failed Scans]_verschoben und ist in Ihrer Risikobewertung enthalten.

### Ignorierte Scanfehler anzeigen

Ignorierte Ergebnisse werden in einem separaten Abschnitt des Berichts angezeigt. Die Risikobewertung wird automatisch aktualisiert, um nur aktive Scan-Fehler widerzuspiegeln. Sie können mehrere Überprüfungsfehler gleichzeitig verwalten, indem Sie mehrere Elemente auswählen, bevor Sie Änderungen anwenden.

![Ignorierte Suchfehler anzeigen](assets/security-scan-view-ignored-failures.png){width="600" zoomable="yes"}
