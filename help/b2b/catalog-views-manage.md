---
title: Konfiguration der Katalogansicht verwalten
description: Erfahren Sie, wie Sie die für freigegebene B2B-Kataloge erstellten Adobe Commerce Optimizer-Katalogansichten überprüfen und die eingeschränkten Zugriffsschlüssel zuweisen, die sie schützen.
feature: B2B, Companies, Catalog Management
last-update: 2026-10-01
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e9004f3c-09ae-5d24-acd2-fa0987fdb66e
    internal-label: Companies
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 15f1e2ee152fb047443da68dec2cc69551e6c7a0
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%
---
# Konfiguration der Katalogansicht verwalten

Wenn die [!DNL Adobe Commerce Optimizer Connector for B2B]-Erweiterung installiert ist, werden auf der Seite Katalogansichten die [!DNL Adobe Commerce Optimizer] ([) aufgelistet](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"} die für benutzerdefinierten freigegebenen Katalog erstellt wurden.  Eine _Projektion_ ist die Katalogansicht, die erstellt wird, wenn der Connector freigegebene Katalogdaten mit [!DNL Adobe Commerce Optimizer] synchronisiert. Der Connector erstellt für jede Shop-Ansicht im freigegebenen Katalog eine separate Projektion, sodass ein freigegebener Katalog mehrere Katalogansichten haben kann. In Storefront-Erlebnissen sind diese Katalogansichten nur für Unternehmen zugänglich, die dem zugehörigen freigegebenen Katalog zugewiesen sind.

Angenommen, Acme Industrial wird einem gemeinsamen Katalog, EU Business, zugewiesen, der zur EU-Website gehört. Diese Website hat zwei Store-Ansichten:

- `English (UK)`

- `German (Germany)`

Der Connector projiziert den freigegebenen Katalog in zwei [!DNL Adobe Commerce Optimizer] Katalogansichten:

- `EU Business – English (UK)`

- `EU Business – German (Germany)`

Das Unternehmen verfügt über englische und deutsche Katalogansichten, aber nur über eine gemeinsame Katalogzuweisung. Jede Shop-Ansicht zeigt Daten aus der entsprechenden Katalogansicht an.

Beide Katalogansichten können dasselbe Preisbuch verwenden, wenn sie dieselbe Website und denselben Preisbereich für Kundengruppen verwenden.

## Authentifizierung für Katalogansicht

Der Connector schützt Katalogansichten mit eingeschränkten Zugriffsschlüsseln. Adobe Commerce verwendet den privaten Schlüssel zum Signieren eines Zugriffstokens für einen autorisierten Käufer. Bevor geschützte Katalogdaten zurückgegeben werden, validiert [!DNL Adobe Commerce Optimizer] das Token anhand des entsprechenden öffentlichen Schlüssels, der mit der angeforderten Katalogansicht verknüpft ist.

Informationen zum Konfigurieren der Token-Lebensdauer oder Deaktivieren der Token-Ausgabe finden Sie unter [Services > ACO-Katalogansicht](/help/configuration-reference/services/aco-catalog-view.md).

Sie können diese Katalogansichten überprüfen und ihre zugewiesenen Schlüssel entweder über die Registerkarte _[!UICONTROL Catalog Views]_&#x200B;des freigegebenen Katalogs oder den Abschnitt&#x200B;_[!UICONTROL Catalog Views]_ des zugehörigen Unternehmens verwalten. Beide listen dieselben Katalogansichten und aktuelle Schlüsselzuweisungen auf. Unter [Bearbeiten von eingeschränkten Zugriffsschlüsseln](#edit-restricted-access-keys) finden Sie den genauen Navigationspfad zu den einzelnen Speicherorten.

Informationen zum Überwachen der Synchronisierung freigegebener Katalogdaten mit [!DNL Adobe Commerce Optimizer] finden Sie [Überwachung des Synchronisierungsstatus der Katalogansicht](/help/systems/catalog-view-sync-status.md).

## Referenz zu Katalogansichten

{{$include /help/_includes/catalog-views-reference-table.md}}

## Bearbeiten von eingeschränkten Zugriffsschlüsseln

{{$include /help/_includes/edit-restricted-access-keys.md}}

Weitere Informationen finden Sie unter [Verwalten von eingeschränkten Zugriffsschlüsseln](/help/systems/restricted-access-keys.md).

>[!MORELIKETHIS]
>
> - [Projektion des freigegebenen B2B-Katalogs](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"}
> - [Services > ACO-Katalogansicht](/help/configuration-reference/services/aco-catalog-view.md)
> - [Überwachung des Synchronisationsstatus der Katalogansicht](/help/systems/catalog-view-sync-status.md)
> - [Freigegebene Kataloge verwalten](catalog-shared-manage.md)
> - [Verwalten von Unternehmenskonten](account-company-manage.md)
