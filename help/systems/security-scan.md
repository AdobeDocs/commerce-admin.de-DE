---
title: Sicherheitsscan
description: Erfahren Sie, wie Sie eine erweiterte Sicherheitsprüfung durchführen und die einzelnen Adobe Commerce- und Magento Open Source-Sites überwachen.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 1f3173d17cc43227f7d44637f1ef0b62606cd0fd
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Sicherheitsscan

Mit dem erweiterten Sicherheitsscan können Sie jede Ihrer Adobe Commerce- und Magento Open Source-Sites, einschließlich PWA, auf bekannte Sicherheitsrisiken und Malware überwachen und Patchaktualisierungen und Sicherheitsbenachrichtigungen erhalten.

- Erhalten Sie Einblicke in den Echtzeit-Sicherheitsstatus Ihres Stores.
- Erhalten Sie Vorschläge basierend auf Best Practices, um Probleme zu beheben.
- Planen Sie die Durchführung der Sicherheitsprüfung wöchentlich, täglich oder auf Anfrage.
- Führen Sie über 21.000 Sicherheitstests durch, um potenzielle Malware zu identifizieren.
- Rufen Sie historische Sicherheitsberichte auf, die den Fortschritt Ihrer Sites verfolgen und überwachen.
- Rufen Sie den Überprüfungsbericht auf, der erfolgreiche und fehlgeschlagene Prüfungen mit empfohlenen Aktionen anzeigt.

Das Sicherheitsscan-Tool ist im Dashboard Ihres [Commerce/Magento-Kontos](../getting-started/commerce-account-create.md) kostenlos verfügbar. Technische Informationen finden Sie unter [Einrichten des Sicherheitsscan-Tools](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html#set-up-the-security-scan-tool) im _Commerce on Cloud Infrastructure Guide_.

![Sicherheits-Scan-Tool](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## Ausführen einer Sicherheitsprüfung

1. Melden Sie sich auf der Commerce-Startseite bei Ihrem [Commerce/Magento-Konto](../getting-started/commerce-account-create.md) an.

1. Überprüfen und akzeptieren Sie die Bedingungen für die Verwendung des Sicherheitsscan-Tools.

   - Wählen Sie im linken Bereich **[!UICONTROL Security Scan]** aus.
   - Klicken Sie auf **[!UICONTROL Go to Security Scan]**.
   - Lesen Sie die **[!UICONTROL Terms and Conditions]**.
   - Klicken Sie auf **[!UICONTROL Agree]** , um fortzufahren.

1. Klicken Sie auf der Seite _[!UICONTROL Monitored Websites]_auf **[!UICONTROL +Add Site]**.

   Wenn Sie mehrere Sites mit unterschiedlichen Domänen haben, konfigurieren Sie für jede Domäne eine separate Prüfung.

   ![Überwachte Sites](./assets/monitored-website.png){width="600" zoomable="yes"}

1. Führen Sie einen der folgenden Schritte aus, um durch Hinzufügen eines Bestätigungscodes zu überprüfen, ob Sie Eigentümer der Website-Domäne sind:

   **Commerce storefront**:

   - Geben Sie die Werte **[!UICONTROL Site URL]** und **[!UICONTROL Site Name]** ein.
   - Klicken Sie auf **[!UICONTROL Generate Confirmation Code]**.
   - Klicken Sie auf **Kopieren** , um Ihren Bestätigungscode in die Zwischenablage zu kopieren.

     ![Generieren von Bestätigungscode](./assets/scan-site1.png){width="400" zoomable="yes"}

   - Melden Sie sich beim Administrator Ihres Stores als Benutzer mit vollständigen Administratorrechten an und führen Sie die folgenden Schritte aus:

      - Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - Suchen Sie Ihre Site in der Liste und klicken Sie auf **[!UICONTROL Edit]**.
      - Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL HTML Head]** .
      - Scrollen Sie nach unten zu &quot;**[!UICONTROL Scripts and Style Sheets]**&quot;, klicken Sie am Ende eines vorhandenen Codes auf das Textfeld und fügen Sie den Bestätigungscode in das Textfeld ein.

        ![Skripte und Stylesheets](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Configuration]**.

   **PWA storefront**:

   - Geben Sie die Werte **[!UICONTROL Site URL]** und **[!UICONTROL Site Name]** ein.

   - Wählen Sie für **[!UICONTROL Confirmation Code]** die Option `META Tag` und klicken Sie dann auf **[!UICONTROL Generate Code]**.

   - Klicken Sie auf **[!UICONTROL Copy]** , um den generierten Bestätigungscode-META-Tag in die Zwischenablage zu kopieren.

     ![Generieren von Bestätigungscode](./assets/scan-site2.png){width="400" zoomable="yes"}

   - Wechseln Sie zum Projektverzeichnis für das PWA Studio-Storefront-Projekt und führen Sie die folgenden Schritte aus:

      - Wechseln Sie im Projektverzeichnis des PWA Studios zu &quot;`packages > venia-concept > template.html`&quot;.
      - Fügen Sie den kopierten Bestätigungscode (das generierte META-Tag) zum HTML-Head hinzu und speichern Sie die Änderungen.

        ![Bestätigungscode kopieren](./assets/code-pwa.png){width="600" zoomable="yes"}

      - Gehen Sie zurück zur PWA Studio-CLI und verwenden Sie Garn, um Projektabhängigkeiten zu installieren und den Projekterstellungsbefehl auszuführen.

        ```sh
        yarn install &&
        yarn build
        ```

      - *Erstellen Sie in Ihrem Cloud-Projekt* einen Ordner &quot;`pwa`&quot;und kopieren Sie den Inhalt in den Ordner &quot;`dist`&quot;Ihres Storefront-Projekts.

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - Verwenden Sie das Git-CLI-Tool, um diese Änderungen zu inszenieren, zu übertragen und in Ihr Cloud-Projekt zu übertragen.

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        Nachdem der Build-Prozess abgeschlossen ist, werden die Änderungen auf Ihrer PWA Store-Front bereitgestellt.

1. Kehren Sie zur Seite &quot;_[!UICONTROL Security Scan]_&quot;in Ihrem Commerce-Konto zurück und klicken Sie auf &quot;**[!UICONTROL Verify Confirmation Code]**&quot;, um das Eigentum an der Domäne zu erlangen.

1. Konfigurieren Sie nach einer erfolgreichen Bestätigung die **[!UICONTROL Set Automatic Security Scan]** -Optionen für einen der folgenden Typen:

   **Wöchentlichen Scan (empfohlen)**:

   - Wählen Sie die **[!UICONTROL Week Day]**, **[!UICONTROL Time]** und **[!UICONTROL Time Zone]** aus, die wöchentlich überprüft werden sollen.
   - Standardmäßig ist geplant, die Prüfung jede Woche um Mitternacht Samstag, UTC zu beginnen und am frühen Sonntag weiterzumachen.

     ![Wöchentlichen Scan](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **Täglich scannen**:

   - Wählen Sie die **[!UICONTROL Time]** und **[!UICONTROL Time Zone]** aus, die täglich überprüft werden sollen.
   - Standardmäßig ist geplant, die Prüfung jeden Tag um Mitternacht (UTC) zu starten.

     ![Täglich scannen](./assets/scan-daily.png){width="500" zoomable="yes"}

1. Geben Sie den **[!UICONTROL Email Address]** -Wert ein, an den Sie Benachrichtigungen über abgeschlossene Prüfungen und Sicherheitsupdates erhalten möchten.

   ![E-Mail-Adresse](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Submit]**.

   Nachdem das Eigentum an der Domäne überprüft wurde, wird die Site in der Liste &quot;Überwachte Websites&quot;Ihres Commerce-Kontos angezeigt.

1. Wenn Sie mehrere Websites mit unterschiedlichen Domänen haben, wiederholen Sie diesen Vorgang, um für jede Website eine Sicherheitsprüfung einzurichten.
