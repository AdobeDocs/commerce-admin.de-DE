---
title: Anführungszeichen konfigurieren
description: Erfahren Sie mehr über die Konfiguration von Anführungszeichen, die den erforderlichen Mindestbestellbetrag für Anführungszeichenanfragen, die Lebensdauer von Anführungszeichen und Dateianhänge steuert.
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
source-git-commit: d4c3ea4b49e30ae3af249516d32fb28437d218b8
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Anführungszeichen konfigurieren

Wenn Anführungszeichen im Allgemeinen aktiviert sind [B2B-Funktionen](enable-basic-features.md)können Sie die Unterstützung für Anführungszeichen in Admin konfigurieren. Die Anführungszeichenkonfiguration bestimmt den erforderlichen Mindestbestellbetrag für Anführungsanfragen, die Lebensdauer des Anführungszeichens und die unterstützten Dateiformate für angehängte Dateien.

>[!NOTE]
>
>Konfigurationsoptionen für Anführungszeichen und die Möglichkeit zur Verwendung von Anführungszeichen-Verhandlungsfunktionen werden mithilfe der Variablen [Rollenressourcen](../systems/permissions-user-roles.md#role-resources). Diese Rollenressourcen müssen für die Administrator-Benutzerrolle ausgewählt sein, die dem Admin-Benutzerkonto zugewiesen ist. Um Zugriff auf Anführungsfunktionen im Admin zu gewähren, gehen Sie zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, wählen Sie die Rolle aus und navigieren Sie zu [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] im_ Rollenressourcen _Baum.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Quotes]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL General]** und führen Sie folgende Schritte aus:

   ![Konfiguration der Verkaufskurse - Allgemein](./assets/quotes-general.png){width="700" zoomable="yes"}

   Siehe [Anführungszeichen](../configuration-reference/sales/quotes.md) im _Konfigurationsreferenz_ für eine vollständige Liste der Anführungsfunktion und ihrer Funktionen.

   - Geben Sie die **[!UICONTROL Minimum Amount]** im Warenkorb, der erfüllt werden muss, bevor eine Angebotsanfrage eingereicht werden kann.

   - Für **[!UICONTROL Minimum Amount Message]** eingeben, geben Sie die Meldung ein, die angezeigt werden soll, wenn die Gesamtsumme des Warenkorbs nicht den erforderlichen Mindestbetrag erreicht.

   - Für **[!UICONTROL Default Expiration Period]**, geben Sie die Anzahl der **[!UICONTROL days]**, **[!UICONTROL weeks]** oder **[!UICONTROL months]** dass ein Anführungszeichen gültig bleiben soll.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Attached files]** und führen Sie folgende Schritte aus:

   - Für **[!UICONTROL File formats for upload]**, geben Sie das Suffix jedes Dateityps ein, den Sie für Dateien unterstützen, die an ein Anführungszeichen angehängt sind.

     Geben Sie jedes Dateisuffix in Kleinbuchstaben und durch ein Komma getrennt ein.

     Standardmäßig werden die folgenden Formate unterstützt: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png`, und `jpeg`

   - Für **[!UICONTROL Maximum file size]**, geben Sie die maximale Größe einer angehängten Datei in Megabyte ein.

     Der von Ihnen eingegebene Wert wird möglicherweise von der Servereinstellung überschrieben.

     ![Konfiguration der Verkaufskurse - angehängte Dateien](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
