---
title: Anführungszeichen konfigurieren
description: Erfahren Sie mehr über die Konfiguration von Anführungszeichen, die den erforderlichen Mindestbestellbetrag für Anführungszeichenanfragen, die Lebensdauer von Anführungszeichen und Dateianhänge steuert.
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
source-git-commit: d4c3ea4b49e30ae3af249516d32fb28437d218b8
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Anführungszeichen konfigurieren

Wenn Anführungszeichen in den allgemeinen [B2B-Funktionen](enable-basic-features.md) aktiviert sind, können Sie die Unterstützung für Anführungszeichen in Admin konfigurieren. Die Anführungszeichenkonfiguration bestimmt den erforderlichen Mindestbestellbetrag für Anführungsanfragen, die Lebensdauer des Anführungszeichens und die unterstützten Dateiformate für angehängte Dateien.

>[!NOTE]
>
>Die Konfigurationsoptionen für Zitate und die Möglichkeit, Angebotsverhandlungen zu verwenden, werden mithilfe der [Rollenressourcen](../systems/permissions-user-roles.md#role-resources) gesteuert. Diese Rollenressourcen müssen für die Administrator-Benutzerrolle ausgewählt sein, die dem Admin-Benutzerkonto zugewiesen ist. Um Zugriff auf Anführungszeichenfunktionen im Admin zu gewähren, gehen Sie zu &quot;**[!UICONTROL System]**&quot;> &quot;_[!UICONTROL Permissions]_&quot;> &quot;**[!UICONTROL User Roles]**&quot;, wählen Sie die Rolle aus und navigieren Sie zu &quot;[!UICONTROL Sales]&quot;> &quot;[!UICONTROL Operations]&quot;> &quot;[!UICONTROL Quotes]&quot;im Baum &quot;_ Rollenressourcen _&quot;.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Quotes]** aus.

1. Erweitern Sie den Abschnitt **[!UICONTROL General]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   ![Konfiguration der Verkaufs-Anführungszeichen - Allgemein](./assets/quotes-general.png){width="700" zoomable="yes"}

   Eine vollständige Liste der Anführungsoptionen und deren Funktionen finden Sie unter [Anführungszeichen](../configuration-reference/sales/quotes.md) in der _Konfigurationsreferenz_ .

   - Geben Sie den Wert **[!UICONTROL Minimum Amount]** in den Warenkorb ein, der erfüllt sein muss, bevor eine Angebotsanforderung gesendet werden kann.

   - Geben Sie für &quot;**[!UICONTROL Minimum Amount Message]**&quot;die Meldung ein, die angezeigt werden soll, wenn die Gesamtsumme des Warenkorbs nicht den erforderlichen Mindestbetrag erreicht.

   - Geben Sie für **[!UICONTROL Default Expiration Period]** die Anzahl der Werte **[!UICONTROL days]**, **[!UICONTROL weeks]** oder **[!UICONTROL months]** ein, die ein Anführungszeichen gültig bleiben soll.

1. Erweitern Sie den Abschnitt **[!UICONTROL Attached files]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   - Geben Sie für &quot;**[!UICONTROL File formats for upload]**&quot;das Suffix jedes Dateityps ein, den Sie für Dateien unterstützen, die an ein Anführungszeichen angehängt sind.

     Geben Sie jedes Dateisuffix in Kleinbuchstaben und durch ein Komma getrennt ein.

     Standardmäßig werden die folgenden Formate unterstützt: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` und `jpeg`

   - Geben Sie für &quot;**[!UICONTROL Maximum file size]**&quot; die maximale Größe einer angehängten Datei in Megabyte ein.

     Der von Ihnen eingegebene Wert wird möglicherweise von der Servereinstellung überschrieben.

     ![Konfiguration der Verkaufs-Anführungszeichen - angehängte Dateien](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
