---
title: Konfigurieren von Anführungszeichen
description: Erfahren Sie mehr über die Angebotskonfiguration, die den erforderlichen Mindestbestellwert für Angebotsanfragen, die Angebotslebensdauer und Dateianhänge steuert.
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
TQID: https://experienceleague.adobe.com/RenH7-cnfF8qVEqFQc7IPMVsIp0alug5OgvYlr5piTM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 0%

---

# Konfigurieren von Anführungszeichen

Wenn Anführungszeichen in den allgemeinen B2B[Funktionen aktiviert sind](enable-basic-features.md) können Sie die Unterstützung für Anführungszeichen im Admin konfigurieren. Die Angebotskonfiguration bestimmt den minimalen erforderlichen Bestellbetrag für Angebotsanfragen, die Angebotslebensdauer und die unterstützten Dateiformate für angehängte Dateien.

>[!NOTE]
>
>Die Konfigurationsoptionen für Angebote und die Möglichkeit, Funktionen für die Angebotsaushandlung zu verwenden, werden mithilfe der [Rollenressourcen](../systems/permissions-user-roles.md#role-resources) gesteuert. Diese Rollenressourcen müssen für die Administratorbenutzerrolle ausgewählt werden, die dem Administratorbenutzerkonto zugewiesen ist. Um Zugriff auf Angebotsfunktionen in Admin zu gewähren, gehen Sie zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, wählen Sie die Rolle aus und navigieren Sie in der Struktur_ Rollenressourcen _zu [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] .

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Quotes]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL General]** und führen Sie folgende Schritte aus:

   ![Konfiguration von Angeboten - Allgemein](./assets/quotes-general.png){width="700" zoomable="yes"}

   Unter [Anführungszeichen](../configuration-reference/sales/quotes.md) in der _Konfigurationsreferenz_ finden Sie eine vollständige Liste der Angebotsfeatures und ihrer Funktionen.

   - Geben Sie die **[!UICONTROL Minimum Amount]** im Warenkorb ein, die erfüllt sein müssen, bevor eine Angebotsanfrage gesendet werden kann.

   - Geben Sie **[!UICONTROL Minimum Amount Message]** die Nachricht ein, die angezeigt werden soll, wenn die Summe des Warenkorbs nicht dem erforderlichen Mindestbetrag entspricht.

   - Geben Sie **[!UICONTROL Default Expiration Period]** die Anzahl der **[!UICONTROL days]**, **[!UICONTROL weeks]** oder **[!UICONTROL months]** ein, für die ein Angebot gültig bleiben soll.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Attached files]** und führen Sie folgende Schritte aus:

   - Geben Sie **[!UICONTROL File formats for upload]** das Suffix jedes Dateityps ein, den Sie für Dateien unterstützen, die an ein Anführungszeichen angehängt sind.

     Geben Sie jedes Dateisuffix in Kleinbuchstaben und durch ein Komma getrennt ein.

     Standardmäßig werden die folgenden Formate unterstützt: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` und `jpeg`

   - Geben Sie **[!UICONTROL Maximum file size]** die maximale Größe einer angehängten Datei in Megabyte ein.

     Der eingegebene Wert wird möglicherweise von der Server-Einstellung überschrieben.

     ![Konfiguration von Angeboten - angehängte Dateien](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
