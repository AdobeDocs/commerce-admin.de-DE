---
title: Sicherheitsüberprüfung
description: Erfahren Sie, wie Sie eine erweiterte Sicherheitsüberprüfung durchführen und jede Ihrer Adobe Commerce- und Magento Open Source-Sites überwachen.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 8e634311cd84a9e797a36218c29abb4699d72835
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Sicherheitsüberprüfung

Die erweiterte Sicherheitsüberprüfung ermöglicht es Ihnen, jede Ihrer Adobe Commerce- und Magento Open Source-Websites, einschließlich PWA, auf bekannte Sicherheitsrisiken und Malware zu überwachen und Patch-Updates und Sicherheitsbenachrichtigungen zu erhalten.

- Erhalten Sie mit insight einen Echtzeitsicherheitsstatus Ihres Stores.
- Erhalten Sie Vorschläge auf der Grundlage von Best Practices, die Sie bei der Lösung von Problemen unterstützen.
- Planen Sie die Ausführung der Sicherheitsüberprüfung auf wöchentliche, tägliche oder On-Demand-Basis.
- Führen Sie über 21.000 Sicherheitstests durch, um potenzielle Malware zu identifizieren.
- Zugriff auf historische Sicherheitsberichte, die den Fortschritt Ihrer Sites verfolgen und überwachen.
- Greifen Sie mit allen empfohlenen Aktionen auf den Scanbericht zu, der erfolgreiche und fehlgeschlagene Prüfungen anzeigt.

Das Tool zur Sicherheitsüberprüfung steht kostenlos im Dashboard Ihres [Commerce/Magento-Kontos zur ](../getting-started/commerce-account-create.md). Technische Informationen finden Sie unter [Einrichten des Sicherheits-Scan-Tools](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html?lang=de#set-up-the-security-scan-tool) im Handbuch zu _Commerce in Cloud-Infrastrukturen_.

![Sicherheits-Scan-Tool](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## Ausführen einer Sicherheitsprüfung

1. Melden Sie sich bei Ihrem [Commerce-/Magento-Konto an](../getting-started/commerce-account-create.md).

1. Klicken Sie im linken Bedienfeld auf die Registerkarte [!UICONTROL Security Scan] . (Überprüfen und akzeptieren Sie bei Bedarf alle aktualisierten Bedingungen für die Verwendung des Security Scan Tools.)

   - Wählen Sie im linken Bedienfeld **[!UICONTROL Security Scan]** aus.
   - Klicken Sie auf **[!UICONTROL Go to Security Scan]**.
   - Lies die **[!UICONTROL Terms and Conditions]**.
   - Zum Fortfahren auf **[!UICONTROL Agree]** klicken.

1. Klicken Sie auf der _[!UICONTROL Monitored Websites]_&#x200B;Seite auf **[!UICONTROL +Add Site]**.

   Wenn Sie mehrere Websites mit unterschiedlichen Domains haben, konfigurieren Sie für jede Domain einen separaten Scan.

   ![Überwachte Sites](./assets/monitored-website.png){width="600" zoomable="yes"}

1. Um zu überprüfen, ob Sie der Eigentümer der Website-Domain sind, indem Sie einen Bestätigungscode hinzufügen, führen Sie einen der folgenden Schritte aus:

   **Commerce-Storefront**:

   - Geben Sie den **[!UICONTROL Site URL]** und die **[!UICONTROL Site Name]** ein.
   - Klicken Sie auf **[!UICONTROL Generate Confirmation Code]**.
   - Klicken Sie **Kopieren**, um Ihren Bestätigungs-Code in die Zwischenablage zu kopieren.

     ![Bestätigungs-Code generieren](./assets/scan-site1.png){width="400" zoomable="yes"}

   - Melden Sie sich beim Administrator Ihres Stores als Benutzer mit vollständigen Administratorrechten an und führen Sie die folgenden Schritte aus:

      - Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - Suchen Sie Ihre Site in der Liste und klicken Sie auf **[!UICONTROL Edit]**.
      - Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL HTML Head]** .
      - Scrollen Sie nach unten zu **[!UICONTROL Scripts and Style Sheets]** und klicken Sie in das Textfeld am Ende eines vorhandenen Codes und fügen Sie den Bestätigungscode in das Textfeld ein.

        ![Skripte und Stylesheets](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - Klicken Sie abschließend auf **[!UICONTROL Save Configuration]**.

   **PWA-Storefront**:

   - Geben Sie den **[!UICONTROL Site URL]** und die **[!UICONTROL Site Name]** ein.

   - Wählen Sie **[!UICONTROL Confirmation Code]** die Option `META Tag` aus und klicken Sie dann auf **[!UICONTROL Generate Code]**.

   - Klicken Sie auf **[!UICONTROL Copy]** , um das generierte Bestätigungs-Code-META-Tag in die Zwischenablage zu kopieren.

     ![Bestätigungs-Code generieren](./assets/scan-site2.png){width="400" zoomable="yes"}

   - Gehen Sie zum Projektverzeichnis der PWA Studio-Storefront und gehen Sie folgendermaßen vor:

      - Wechseln Sie im PWA Studio-Projektverzeichnis zu `packages > venia-concept > template.html`.
      - Fügen Sie den kopierten Bestätigungs-Code (das generierte META-Tag) zum HTML-Head hinzu und speichern Sie die Änderungen.

        ![Bestätigungs-Code kopieren](./assets/code-pwa.png){width="600" zoomable="yes"}

      - Kehren Sie zur PWA Studio-CLI zurück, installieren Sie mithilfe von „Garn“ die Projektabhängigkeiten und führen Sie den Projekterstellungsbefehl aus.

        ```sh
        yarn install &&
        yarn build
        ```

      - *Erstellen Sie* Cloud-Projekt einen `pwa` Ordner und kopieren Sie den Inhalt in den `dist` Ordner Ihres Storefront-Projekts.

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - Verwenden Sie das Git-CLI-Tool, um diese Änderungen zu testen, zu übertragen und in Ihr Cloud-Projekt zu übertragen.

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        Nach Abschluss des Build-Prozesses werden die Änderungen an Ihrer PWA-Storefront bereitgestellt.

1. Kehren Sie zur Seite _[!UICONTROL Security Scan]_&#x200B;in Ihrem Commerce-Konto zurück und klicken Sie auf **[!UICONTROL Verify Confirmation Code]**, um die Eigentümerschaft an der Domain herzustellen.

1. Konfigurieren Sie nach erfolgreicher Bestätigung die **[!UICONTROL Set Automatic Security Scan]** für einen der folgenden Typen:

   **Wöchentlicher Scan (empfohlen)**:

   - Wählen Sie **[!UICONTROL Week Day]**, **[!UICONTROL Time]** und **[!UICONTROL Time Zone]** aus, dass der Scan jede Woche durchgeführt werden soll.
   - Standardmäßig ist der Scan so geplant, dass er jede Woche um Mitternacht Samstag (UTC) beginnt und bis zum frühen Sonntag fortgesetzt wird.

     ![Wöchentlicher Scan](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **Tägliche Suche**:

   - Wählen Sie die **[!UICONTROL Time]** aus und **[!UICONTROL Time Zone]** Sie, dass der Scan jeden Tag stattfinden soll.
   - Standardmäßig ist der Beginn der Suche für jeden Tag um Mitternacht (UTC) geplant.

     ![Tägliche Suche](./assets/scan-daily.png){width="500" zoomable="yes"}

1. Geben Sie die **[!UICONTROL Email Address]** ein, in der Sie Benachrichtigungen über abgeschlossene Suchvorgänge und Sicherheits-Updates erhalten möchten.

   ![E-Mail-](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Submit]**.

   Nachdem das Eigentum an der Domain überprüft wurde, wird die Site in der Liste Überwachte Websites Ihres Commerce-Kontos angezeigt.

1. Wenn Sie mehrere Websites mit unterschiedlichen Domains haben, wiederholen Sie diesen Vorgang, um für jede Website eine Sicherheitsprüfung einzurichten.

## Löschen einer Sicherheitsprüfung

>[!NOTE]
>
>Nur die Person, die den Scan ursprünglich eingerichtet hat, kann ihn aus dem Konto löschen. Wenn sie sich seit August 2022 nicht mehr bei ihrem [Konto](https://account.magento.com) angemeldet haben, müssen sie zunächst sicherstellen, dass sie sich [für eine Adobe ID registriert](https://account.magento.com) haben.

**Löschen eines Scans**

1. Beim [Commerce-/Magento-Konto anmelden](../getting-started/commerce-account-create.md).

1. Klicken Sie im linken Bedienfeld auf die Registerkarte [!UICONTROL Security Scan] . (Überprüfen und akzeptieren Sie bei Bedarf alle aktualisierten Bedingungen für die Verwendung des Security Scan Tools.)

   - Klicken Sie auf **[!UICONTROL Go to Security Scan]**.
   - Lies die **[!UICONTROL Terms and Conditions]**.
   - Zum Fortfahren auf **[!UICONTROL Agree]** klicken.

1. Suchen Sie auf der Seite _[!UICONTROL Monitored Websites]_&#x200B;das Dropdown-Menü unter der Spalte [!UICONTROL Actions] und wählen Sie dann **[!UICONTROL Delete]**&#x200B;für die entsprechenden Websites aus.
