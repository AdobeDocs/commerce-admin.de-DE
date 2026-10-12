---
title: Anforderungslisten-Maximum konfigurieren
description: Erfahren Sie mehr über die Konfiguration der Anforderungsliste, die die maximale Anzahl steuert, die für jedes Kundenkonto gepflegt werden kann.
exl-id: a36dda0e-c00f-4182-9046-717b9d811f71
feature: B2B, Companies, Configuration
role: Admin
TQID: 'https://experienceleague.adobe.com/we9sPvRg20kEV4EpfemuA7WW-rjv7G6evjr5MwzRGyM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
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
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%
---
# Anforderungslisten-Maximum konfigurieren

Wenn die Anforderungslisten-Funktion aktiviert ist, können Kunden mehrere Listen häufig gekaufter Artikel erstellen und diese Listen für die Auftragserteilung verwenden. Es ist sowohl für angemeldete Benutzer als auch für Gäste verfügbar. Anforderungslisten können aktiviert werden, wenn Sie [die B2B-Funktionen konfigurieren](enable-basic-features.md).

Ein Kunde kann über mehrere Listen verfügen, die sich auf Produkte verschiedener Anbieter, Käufer, Teams, Kampagnen oder auf alles andere konzentrieren, was gängige Workflows optimiert. [Funktionalität der Anforderungsliste](requisition-lists.md) ähnelt Wunschlisten, mit den folgenden Unterschieden:

- Eine Anforderungsliste wird nach dem Versand von Artikeln an den Warenkorb nicht gelöscht. Es kann mehrmals verwendet werden.
- Die Benutzeroberfläche für Anforderungslisten verwendet eine kompakte Ansicht, um viele Elemente anzuzeigen.

Standardmäßig können Kunden bis zu 999 Anforderungslisten für ihr Konto verwalten. Sie können jedoch die Konfiguration ändern und eine niedrigere Zahl angeben, um die Belastung Ihres Stores zu verringern.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Requisition Lists]**.

   ![Anforderungslisten - Allgemeine Einstellung](./assets/requisition-lists-general.png){width="600" zoomable="yes"}

1. Geben Sie **[!UICONTROL Number of Requisition Lists]** die maximale Anzahl von Anforderungslisten ein, die für jedes Kundenkonto gepflegt werden können.

   Die Mindestzahl ist `2`, die Höchstzahl `999`.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
