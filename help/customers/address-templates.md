---
title: Vorlagen für Kundenadressen
description: Erfahren Sie, wie Sie die Vorlagen für Kundenadressen anpassen können.
exl-id: 9fd32c0a-ff9a-47f9-84e2-f5d6bf307d8c
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# Vorlagen für Kundenadressen

{{ee-feature}}

Sie können die Vorlage ändern, die das Format der Abrechnungs- und Versandadressen der Kunden steuert, die auf gedruckten Rechnungen, Sendungen und Erstattungen sowie im Adressbuch des Kundenkontos angezeigt werden. Wenn Sie zusätzliche Informationen einbeziehen möchten, können Sie [benutzerdefinierte Attribute](attribute-properties.md) die mit dem Kundenkonto verknüpft sind und [Adresse](address-attributes.md)und fügen Sie sie in die Vorlage ein.

## Beispiel 1: Kurzformat

Für [!UICONTROL Text One Line] Adressenvorlage:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var region}} {{var postcode}}, {{var country}}
```

## Beispiel 2: Langformat

Für [!UICONTROL Text], [!UICONTROL HTML], und [!UICONTROL PDF] Adressenvorlagen:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend company}}{{var company}}{{/depend}}{{if street1}}{{var street1}}{{/if}}{{depend street2}}{{var street2}}{{/depend}}{{depend street3}}{{var street3}}{{/depend}}{{depend street4}}{{var street4}}{{/depend}}{{if city}}{{var city}},  {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}{{var country}}{{depend telephone}}T: {{var telephone}}{{/depend}}{{depend fax}}F: {{var fax}}{{/depend}}{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}
```

![Vorlagen für Kundenadressen](../configuration-reference/customers/assets/customer-configuration-address-templates.png){width="600" zoomable="yes"}

## Ändern der Reihenfolge der Adressfelder

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Seitenbereich **[!UICONTROL Customers]** und wählen **[!UICONTROL Customer Configuration]**.

1. Klicken Sie auf , um die **[!UICONTROL Address Templates]** Abschnitt.

   Der Abschnitt enthält einen separaten Satz von Formatierungsanweisungen für die folgenden Elemente:

   - [!UICONTROL Text]
   - [!UICONTROL Text One Line]
   - [!UICONTROL HTML]
   - [!UICONTROL PDF]

1. Bearbeiten Sie jede Vorlage nach Bedarf mithilfe der Referenzbeispiele.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
