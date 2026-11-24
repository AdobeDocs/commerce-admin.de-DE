---
title: Erstellen von Regeln für die Kataloganreicherung von Marken
description: Erfahren Sie, wie Sie Governance-Regeln für die Kataloganreicherung erstellen und verwalten, Anforderungen für Produktkopien definieren und Regeln auf Kataloganreicherungsaufträge anwenden.
role: Admin, User, Leader
source-git-commit: 9d7a4f4e98fe2d2d51261d96a2e072c28925babd
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 1%
---
# Erstellen von Regeln für Kataloganreicherungen bei Marken

Regeln für Brand Governance und Brand Governance sind nur für die Kataloganreicherung verfügbar. Sie gelten nicht für die PDP-Anreicherung. Diese Regeln definieren Anforderungen für Produktnamen und Beschreibungen, die von [!DNL Commerce Catalog Agent] generiert werden. Bearbeiten oder konfigurieren Sie eine Standardregel für Ihre standardmäßigen Markenstandards und erstellen Sie dann benutzerdefinierte Regeln für bestimmte Kampagnen, Produktkategorien oder Untermarken. Wählen Sie beim Erstellen eines Vorgangs [Kataloganreicherung](catalog-enrichment.md) eine Regel aus.

## Offene Marken-Governance

1. Navigieren Sie in der Admin-Liste zu **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**.
1. Öffnen Sie die Registerkarte **[!UICONTROL Brand Governance]** .

Die Registerkarte **Markenverwaltung** enthält die Standardregel und alle benutzerdefinierten Regeln, die Sie erstellt haben. Sie können nach Regeln suchen oder die Tabelle mit Regeln filtern.

Für jede Zeile werden die Felder **Regelname**, **Felder**, **Tone**, **Zuletzt geändert** und **Status** angezeigt. Die Standardregel ist als **[!UICONTROL Default]** markiert.

Im **[!UICONTROL Needs your attention]** Bereich werden die Regeln hervorgehoben, die überarbeitet werden müssen, z. B. Entwürfe, die eingerichtet werden müssen, oder Regeln mit Konflikten. Überprüfen Sie die Regeldetails und verwenden Sie die verfügbare Aktion, z. B. **[!UICONTROL Finish setup]** oder **[!UICONTROL Fix conflict]**.

## Typen von Regeln verstehen

Die Kataloganreicherung unterstützt eine Standardregel und benutzerdefinierte Regeln.

### Standardregel

Jede [!DNL Adobe Commerce] hat genau eine Standardregel. [!DNL Adobe Commerce] erstellt diese Regel mit leeren Feldern. Sein Name ist als **[!UICONTROL Global]** festgelegt. Sie können die Regel bearbeiten, sie jedoch nicht löschen.

[!DNL Adobe Commerce] wendet die Standardregel standardmäßig an, wenn Sie einen Auftrag zur Kataloganreicherung erstellen, ohne eine benutzerdefinierte Regel auszuwählen. Die Standardregel stellt die grundlegende Governance für die Kataloganreicherung bereit.

### Benutzerdefinierte Regeln

Sie können eine beliebige Anzahl benutzerdefinierter Regeln für eine Kampagne, Produktkategorie oder Untermarke erstellen. Eine benutzerdefinierte Regel wird nicht automatisch angewendet. Wählen Sie diese beim Erstellen eines Auftrags zur Kataloganreicherung aus.

Eine benutzerdefinierte Regel übernimmt keine Werte von der Standardregel. Wenn Sie eine benutzerdefinierte Regel erstellen, können Sie die aktuellen Werte der Standardregel als einmaligen Ausgangspunkt kopieren. Spätere Änderungen an der Standardregel aktualisieren die benutzerdefinierte Regel nicht.

Verwenden Sie die Standardregel für Standards, die gelten sollen, wenn ein Benutzer keine benutzerdefinierte Regel auswählt. Erstellen Sie eine benutzerdefinierte Regel für eine Kampagne oder Kategorie mit unterschiedlichen Anforderungen. Fügen Sie alle globalen Anforderungen hinzu, die auch die benutzerdefinierte Regel erfordert, da benutzerdefinierte Regeln keine globalen Werte erben.

## Erstellen einer benutzerdefinierten Regel

In diesem Abschnitt erfahren Sie, wie Sie eine Brand Governance-Regel erstellen.

![Erstellen einer Brand Governance-Regel](./assets/brand-gov-create-rule.png)

1. Klicken Sie auf der **Brand Governance** auf **[!UICONTROL Create Rule]**.
1. Wählen Sie aus, wie die Regel gestartet werden soll:
   - **[!UICONTROL Blank]**: Setzt alle Werte selbst.
   - **[!UICONTROL Copy Global enrichment]**: Beginnen Sie mit den aktuellen Standardregelwerten als einmalige Kopie.
   - **[!UICONTROL Draft with AI]**: (**in Kürze verfügbar** Beschreiben Sie Ihre Markenstimme, um vorgeschlagene Regelwerte zu erhalten.
1. Geben Sie einen **Regelnamen** ein, der den Zweck angibt, z. B. eine Kampagne, Kategorie oder Untermarke.
1. Konfigurieren **unter „Zu** Felder“ die Anforderungen an den Produktnamen und die Produktbeschreibung.

   Konfigurieren Sie Produktnamen und -beschreibungen separat. Jedes Feld hat seine eigenen Anforderungen an Schalter und Governance aktivieren .

1. Legen Sie **Länge des Produktnamens** fest.

   Legen Sie die minimale und maximale Namenslänge für einen angereicherten Produktnamen fest. Für eine Regel können beispielsweise mindestens 20 und höchstens 200 Zeichen erforderlich sein.

1. Legen Sie die Option **Schreibweise** fest:

   - **[!UICONTROL Sentence case]**: `Waterproof hiking boots`
   - **[!UICONTROL Title Case]**: `Waterproof Hiking Boots`
   - **[!UICONTROL As written]**: Groß-/Kleinschreibung des Quelltexts beibehalten.

1. Beschreiben Sie den **Markenton**. Siehe [Festlegen des Markentons](#set-brand-tone) für Anleitungen.
1. Festlegen der erforderlichen und ausgeschlossenen Phrasen

   **[!UICONTROL Must include]** hinzufügen.
   **[!UICONTROL Never use]** hinzufügen.

1. Klicken Sie auf **[!UICONTROL Save as draft]** , um den Vorgang zu einem späteren Zeitpunkt abzuschließen, oder klicken Sie auf **[!UICONTROL Publish rule]** , um die Regel beim Erstellen einer Kataloganreicherungsregel für die Auswahl verfügbar zu machen. Klicken Sie auf **[!UICONTROL Cancel]** , um den Vorgang ohne Speichern zu beenden.

1. Sie können die Regel jetzt auf einen Vorgang [Kataloganreicherung](catalog-enrichment.md) anwenden.

### Festlegen des Markentons

Geben Sie Anleitungen im mehrzeiligen **[!UICONTROL Brand tone]** ein, um die Stimme und den Stil des angereicherten Namens zu beschreiben.

Im Folgenden finden Sie einige Beispiele für den Ton, den Sie für die **Beschreibung** verwenden können:

- **B2B-Industrie**: `Write for the operator and the buyer. Open with what the unit does and where it fits in the kitchen, then throughput, utility requirements, footprint, and certifications. Plain, technical language. Mention cleaning and maintenance, because total cost of ownership drives the decision. No lifestyle language.`
- **Luxusmode**: `Quiet confidence. Lead with craftsmanship and provenance (atelier, tannery, technique), then how the piece wears and ages. Short, measured sentences. Sensory detail is fine. Never compare to other brands or mention price or value.`
- **Unterhaltungselektronik**: `Clear and benefit-led. Turn every spec into what it does for the user. Scannable short paragraphs or bullets. Put compatibility and what's in the box up front. Don't make performance claims without a source, and don't use comparative claims like "fastest"`
- **Spezialitätenlebensmittel und Lebensmittelgeschäft**: `Warm and appetizing, but honest. Describe taste, texture, and aroma in concrete terms, then origin and how it's made, then serving ideas. Plain, friendly language. Put allergens and dietary attributes in a consistent closing line. Don't make health claims.`
- **Wohnungseinrichtung**: `Inviting and practical. Open with how the piece is used, then dimensions, materials, and care. Help the shopper picture it in their space without overselling. Always mention assembly, delivery, and weight, since those drive returns.`
