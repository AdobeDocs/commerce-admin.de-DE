---
title: Verwalten von eingeschränkten Zugriffsschlüsseln in Commerce
description: Erstellen, zuweisen und löschen Sie die eingeschränkten Zugriffsschlüssel, die mit Adobe Commerce Optimizer synchronisierte B2B-freigegebene Katalogansichten schützen.
feature: Products, Customers, Data Import/Export
role: Admin
level: Intermediate
last-update: 2026-10-01
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: b974b164-8a4e-43b8-a9e2-8e67ec131677
    internal-label: Commerce on Prem
  - id: cdf0c6dd-1717-4e20-9530-a24eee57088b
    internal-label: Commerce on Cloud
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 22bad240-8308-569b-a9d5-578f1ff890ca
    internal-label: Customers
  - id: 601e4abe-d9bf-58de-a779-32ed6794dcbe
    internal-label: Data Import/Export
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 15f1e2ee152fb047443da68dec2cc69551e6c7a0
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 0%
---

# Verwalten eingeschränkter Zugriffsschlüssel

Verwenden Sie die Seite „Schlüssel für eingeschränkten Zugriff“, um Zugriffsschlüssel für vom [!DNL Adobe Commerce Optimizer Connector for B2B] erstellte private Katalogansichten zu verwalten. Der Connector synchronisiert die Konfigurationen für freigegebene B2B-Kataloge von Adobe Commerce mit Adobe Commerce Optimizer.

>[!NOTE]
>
>Bei manuell erstellten Schlüsseln, mit denen private Kataloge in Nicht-B2B-Szenarien verwaltet werden (z. B. Partnerportale), verwalten Sie Schlüssel von [[!DNL Adobe Commerce Optimizer Studio]](https://experienceleague.adobe.com/de/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"} aus.

## Zielgruppe und Verfügbarkeit {#audience}

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce auf Cloud-Infrastruktur- und lokale Projekte."}

Die [!UICONTROL Restricted Access Keys]-Seite ist für Adobe Commerce in der Cloud-Infrastruktur und für Händler vor Ort verfügbar, die B2B-freigegebene Kataloge mit dem -[!DNL Adobe Commerce Optimizer Connector for B2B] verwenden. Der Connector installiert und aktiviert die Seite automatisch.

Wenn eine Katalogansicht zum ersten Mal für einen freigegebenen Katalog erstellt wird, generiert der Connector automatisch einen Schlüssel und weist ihn zu. Auf dieser Seite können Sie diesen Schlüssel anzeigen und zusätzliche Schlüssel erstellen, zuweisen oder löschen.

## Zugriff auf die Seite „Schlüssel für eingeschränkten Zugriff“ {#access-restricted-access-keys-page}

Navigieren Sie im Admin-Bereich zu **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Restricted Access Keys]**.

![Seite „Schlüssel mit eingeschränktem Zugriff“, auf der Schlüssel und ihre zugewiesenen Katalogansichten aufgelistet sind](assets/restricted-access-keys.png){width="600" zoomable="yes"}

Auf dieser Seite wird jeder Schlüssel aufgelistet, unabhängig davon, ob er einer Katalogansicht zugewiesen ist oder nicht. Um einer bestimmten Katalogansicht einen Schlüssel zuzuweisen, verwenden Sie stattdessen die [!UICONTROL Edit Restricted Access Keys] Aktion in dieser Katalogansicht. Siehe [Zuweisen von Schlüsseln zu einer Katalogansicht](#assign-keys-to-a-catalog-view).

## Zusammenfassung der Schlüssel für eingeschränkten Zugriff {#restricted-access-keys-summary}

Das Raster enthält einen Schlüssel pro Zeile.

| Feld | Beschreibung |
| --- | --- |
| **Schlüssel-ID** | Die eindeutige Schlüsselkennung. |
| **Titel** | Eine Beschriftung, die Sie zum Identifizieren des Schlüssels angeben. |
| **Zugewiesene Katalogansichten** | Die Katalogansichten, denen dieser Schlüssel derzeit zugewiesen ist. |
| **Läuft ab um** | Das Ablaufdatum des Schlüssels. |
| **Aktionen** | Aktionen auf Zeilenebene. Siehe [Schlüssel verwalten](#manage-keys). |

## Schlüssel verwalten {#manage-keys}

- **[!UICONTROL Create Key]** - Erzeugt ein neues, nicht zugewiesenes Schlüsselpaar. Commerce generiert das Schlüsselpaar und speichert den privaten Schlüssel. Der öffentliche Schlüssel wird erst dann bei [!DNL Adobe Commerce Optimizer] registriert, wenn Sie den Schlüssel einer Katalogansicht zuweisen.
- **[!UICONTROL View Public Key]** - Öffnet eine schreibgeschützte Ansicht des öffentlichen Schlüssels des Schlüssels, sodass Sie ihn kopieren können, um ihn bei Bedarf erneut zu registrieren oder zu synchronisieren. Der private Schlüssel wird nie angezeigt.
- **[!UICONTROL Delete]** - Entfernt den Schlüssel und widerruft seine Remote-Registrierung in [!DNL Adobe Commerce Optimizer]. Storefront-Token, die bereits mit diesem Schlüssel ausgestellt wurden, bleiben bis zu ihrem Ablauf gültig. Diese Aktion kann nicht rückgängig gemacht werden.

>[!NOTE]
>
>Ein abgelaufener Schlüssel kann nur gelöscht werden. Die Zuweisung eines abgelaufenen Schlüssels kann nicht aufgehoben werden.

## Schlüssel erstellen

Erstellen Sie auf der Seite [!UICONTROL Restricted Access Keys] einen Schlüssel, indem Sie **[!UICONTROL Create Key]** auswählen.

Commerce generiert ein neues Schlüsselpaar und speichert den privaten Schlüssel. Die Tabelle Schlüssel für eingeschränkten Zugriff wird mit einem neuen Schlüsseleintrag aktualisiert, der die eindeutige Schlüssel-ID anzeigt. Verwenden Sie diese [!UICONTROL Key ID], wenn Sie den Schlüssel einer Katalogansicht zuweisen.

Der öffentliche Schlüssel wird erst dann bei [!DNL Adobe Commerce Optimizer] registriert, wenn Sie den Schlüssel einer Katalogansicht zuweisen. Nach der Registrierung wird der Tabelleneintrag Schlüssel mit eingeschränktem Zugriff aktualisiert und zeigt nun die Katalogzuweisung und das Ablaufdatum an.

## Zuweisen oder Entfernen von eingeschränkten Zugriffsschlüsseln {#assign-keys-to-a-catalog-view}

{{$include /help/_includes/edit-restricted-access-keys.md}}

## Tastenauswahl und -rotation {#key-selection-and-rotation}

Wenn einer Katalogansicht mehr als ein Schlüssel zugewiesen ist, verwendet [!DNL Adobe Commerce] automatisch den zugewiesenen, nicht abgelaufenen Schlüssel mit dem neuesten Ablaufdatum, um Token zu signieren.

>[!IMPORTANT]
>
>Die automatische Tastenrotation ist noch nicht verfügbar. Standardmäßig ist ein langer Gültigkeitszeitraum für Schlüssel festgelegt. Um einen Schlüssel manuell zu drehen, erstellen Sie einen neuen Schlüssel und weisen ihn der Katalogansicht neben dem vorhandenen Schlüssel zu. Nachdem Sie bestätigt haben, dass der neue Schlüssel verwendet wird, löschen Sie den alten Schlüssel.

Um den Standardablaufzeitraum für neu erstellte Schlüssel zu ändern, gehen Sie zu **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Restricted Access Keys]** > **[!UICONTROL Provisioning]** > **[!UICONTROL Default key lifetime (days)]**. Siehe [Services > ACO - Schlüssel für eingeschränkten Zugriff](../configuration-reference/services/aco-restricted-access-keys.md).

## Bekannte Einschränkungen {#known-limitations}

- Im [!UICONTROL Restricted Access Keys] gibt es keine aktive Anzeige oder Statusanzeige.

  Sie können den Link-Status auf der Seite [!UICONTROL Edit Restricted Access Keys] sehen. Verwenden Sie das Dropdown-Menü, um die verfügbaren Schlüssel und deren Status anzuzeigen. Wenn ein Schlüssel einer Katalogansicht zugewiesen ist, ist er verknüpft. Wenn er nicht zugewiesen ist, hat er keinen Status. Sie können diese Schlüssel der Katalogansicht zuweisen, die Sie bearbeiten.

  Auf der Seite &quot;[!UICONTROL Catalog View Sync Status]&quot; können Sie auf der Seite mit den Katalogdetails (**[!UICONTROL View details]**) Schlüssel sehen, die mit einer Katalogansicht verknüpft sind. Die Detailseite zeigt auch den Verlauf des Schlüssels an, einschließlich des Zeitpunkts, zu dem er in einer Katalogansicht zugewiesen oder seine Zuweisung aufgehoben wurde.

- Die automatische Tastenrotation ist noch nicht verfügbar.

>[!MORELIKETHIS]
>
> - [Konfiguration der Katalogansicht verwalten](/help/b2b/catalog-views-manage.md) - Weisen Sie diese Schlüssel aus dem freigegebenen Katalog oder dem Unternehmenskonto zu
> - [Überwachung des Synchronisationsstatus der Katalogansicht](catalog-view-sync-status.md) — Überwachen und Abstimmen der Katalogansichten, die von diesen Schlüsseln geschützt werden
> - [Services > ACO-Schlüssel mit eingeschränktem Zugriff](../configuration-reference/services/aco-restricted-access-keys.md) — Konfigurieren des Standardablaufzeitraums für Schlüssel
> - [Services > ACO-Katalogansicht](../configuration-reference/services/aco-catalog-view.md) — Konfigurieren der Lebensdauer des Zugriffs-Tokens für die Storefront und Aktivieren oder Deaktivieren der Ausgabe
> - [Verwalten von eingeschränkten Zugriffsschlüsseln](https://experienceleague.adobe.com/de/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/restricted-access-keys){target="_blank"} im *Adobe Commerce Optimizer Connector-Handbuch* — Erfahren Sie, wie diese Schlüssel in die Synchronisierung des B2B-freigegebenen Katalogs passen
> - [Eingeschränkte Zugriffsschlüssel](https://experienceleague.adobe.com/de/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"} im *Adobe Commerce Optimizer-Handbuch* - Der manuelle, ACO Studio-basierte Schlüsselfluss für Nicht-B2B-Anwendungsfälle
