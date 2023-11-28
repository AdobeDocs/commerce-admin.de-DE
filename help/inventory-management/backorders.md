---
title: "Konfigurieren [!DNL Inventory Management] backorders"
description: Erfahren Sie, wie Sie Aufstockungen konfigurieren, um den Verkauf von nicht vorrätigen Produkten zu unterstützen.
exl-id: 2fe778df-781e-4cda-8b85-47cf973c9e94
feature: Inventory, Orders
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Konfigurieren [!DNL Inventory Management] backorders

Rückaufträge ermöglichen es Ihrem Geschäft, Produkte weiter zu verkaufen, nachdem die Menge null erreicht oder praktisch nicht vorrätig ist. Wenn eine Kundenbestellung ein Rückstand ist, werden die Mittel sofort genehmigt und erfasst, der Bearbeitungsstatus der Bestellung ändert sich nicht und der Versand bleibt solange auf Lager, bis ein Lager verfügbar ist.

Abhängig von Ihrem Store und Ihrem Vertrieb können Sie die Rückorder auf den folgenden Ebenen aktivieren oder deaktivieren:

- **[!UICONTROL Global]** - Alle Produkte in Ihrem Katalog auf Site-Ebene

- **[!UICONTROL Product]** - Bestimmte Produkte überschreiben Einstellungen für Site, Quelle und Lager

## Hintergrundeinstellungen verstehen

Es wird dringend empfohlen, bestimmte Schwellenwerte und Einstellungen so zu konfigurieren, dass Rückstände optimal unterstützt werden.

### Schwellenwert für nicht auf Lager

Verwenden Sie einen negativen Wert für diese Schwelle, um die maximale Menge von Produkten festzulegen, die zurückbestellt werden können, bevor das Produkt tatsächlich als nicht vorrätig betrachtet wird. Dieser Betrag erhöht die Verkaufsmenge. Der auf Produktebene festgelegte Wert setzt alle Werte außer Kraft, die auf globaler Ebene festgelegt wurden.

Die Formel für die Verkaufsmenge lautet `(Quantity - (Out-of-Stock Threshold))`.

Im Folgenden finden Sie ein Beispiel:

- Menge: 25
- Meldung für die nachstehende Menge: 10
- Nur X linke Schwelle: 5
- Nicht vorrätiger Schwellenwert: -50

Die Verkaufsmenge für dieses Produkt ist `75 (25 - (-50))`.

![Beispiel: Verkaufte Menge vor aktivierten Rückständen](assets/inventory-backorders-before.png){width="600" zoomable="yes"}

![Beispielverkaufsmenge nach aktivierten Rückständen](assets/inventory-backorders-after.png){width="600" zoomable="yes"}

Wenn Kunden die 25 verfügbaren Produkte kaufen, werden neue Bestellungen als Rückbestellungen erfasst. Da die Verkaufsmenge des Produkts auf 5 reduziert wird (70 Artikel wurden verkauft), wird die _Produkt_ Seite zeigt eine Nachricht an `Only 5 left` auf der Storefront. Wenn die verkaufbare Menge erreicht `0`, wird das Produkt als `Out of Stock` in der Storefront.

>[!NOTE]
>
>Wenn ein Kunde eine Bestellung aufgibt mit _[!UICONTROL backorder qty]_, [!DNL Inventory Management] subtrahiert automatisch die Menge von der verkaufbaren Menge. Wenn eine Bestellung nicht versandt und storniert wird, kehrt die Menge zur aggregierten virtuellen Verkaufsmenge zurück. Die **_die stornierte Bestellmenge keinem der Quellen zugeordnet wird_**, wird jedoch an die Gesamtzahl der zum Verkauf stehenden Produkte zurückgegeben (_[!UICONTROL Salable Quantity]_ im Produktraster).

<!--### Notify for Quantity Below JIRA MDVA-8099 MDVA-33783

The _Notify for Quantity Below_ configuration option is configurable at the global, source, and product levels. When it is enabled, the system sends an email notification when the product quantity reaches a level at or below the configured value. For this example, a notification is triggered when the product has a quantity of 10 or less. When backorders are enabled, _Notify for Quantity Below_ is determined by the Salable Quantity (`Salable Quantity = Quantity - (Out-of-Stock Threshold)`). -->

### Lagerstatus

Produkte müssen auf `In Stock` Status beim Aktivieren von Rückständen. Sie können diesen Wert über die _Produkt_ Seite. Bei Multi-Source-Händlern muss mindestens eine Quelle als `In Stock`. Rufen Sie auf und legen Sie den Status über das _Produkt_ Seite und zugewiesene _Quellen_ Gitter.

## Globale Konfiguration von Rückständen

Diese Schritte ermöglichen Rückläufe für alle Produkte auf Site-Ebene.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Satz **[!UICONTROL Store View]** nach `Default Config`.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Inventory]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Product Stock Options]**.

1. Für **[!UICONTROL Backorders]**, deaktivieren Sie die **[!UICONTROL Use system value]** und wählen Sie eine Option aus:

   | Option | Beschreibung |
   | -- | -- |
   | `No Backorders` | Nicht akzeptieren von Rückständen, wenn das Produkt nicht vorrätig ist. |
   | `Allow Qty Below 0` | Zu akzeptieren Rückstände, wenn die Menge unter null fällt. |
   | `Allow Qty Below 0 and Notify Customer` | Nachbestellungen zu akzeptieren, wenn die Menge unter null fällt, und den Kunden darüber zu informieren, dass die Bestellung noch aufgegeben werden kann. |

1. Für **[!UICONTROL Out-of-Stock Threshold]**, deaktivieren Sie die **[!UICONTROL Use system value]** und geben Sie einen anderen Betrag ein.

   | Wert | Beschreibung |
   | -- | -- |
   | Positiver Betrag | Geben Sie bei deaktivierten Rückständen einen positiven Wert ein. |
   | Null | Wenn Rückstände aktiviert sind, geben Sie `0` ermöglicht unendliche Rückläufe. |
   | Negativer Betrag | Bei aktivierten Rückständen wird die Eingabe eines negativen Werts empfohlen. Der Betrag wird der Verkaufsmenge hinzugefügt. Geben Sie beispielsweise `-50` um Bestellungen bis zu diesem Betrag zuzulassen. |

1. Klicken **[!UICONTROL Save Config]**.

## Konfigurieren von Rückständen für ein Produkt

Konfigurationen auf Produktebene überschreiben globale Konfigurationen. Möglicherweise möchten Sie Rückorder auf Produktebene konfigurieren, um die Einstellungen auf globaler Store- oder Quellebene zu überschreiben. Ihr Store unterstützt beispielsweise möglicherweise global Backorder. Mit den Produkteinstellungen können Sie Rückstände deaktivieren oder den Schwellenwert für &quot;Nicht auf Lager&quot;ändern, ohne andere Produkte und Quellen zu beeinträchtigen.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Öffnen Sie ein Produkt in **[!UICONTROL Edit]** -Modus und scrollen Sie nach unten zur Seite _[!UICONTROL Sources]_Bereich.

   Für Produkte, die ohne [!DNL Inventory Management], wird die Registerkarte nicht angezeigt. Die `Advanced Inventory` wird unter der Schaltfläche _[!UICONTROL Quantity]_-Feld.

1. Klicken **[!UICONTROL Advanced Inventory]**.

   Diese Aktion zeigt eine Seite mit produktspezifischen Konfigurationen an. Alle Einstellungen, die als `global` zeigt die aktuelle globale Einstellung für den Store an.

1. Für **[!UICONTROL Backorders]**, deaktivieren Sie die **[!UICONTROL Use Config Setting]** und wählen Sie eine Option aus:

   | Option | Beschreibung |
   | -- | -- |
   | `No Backorders` | Nicht akzeptieren von Rückständen, wenn das Produkt nicht vorrätig ist. |
   | `Allow Qty Below 0` | Zu akzeptieren Rückstände, wenn die Menge unter null fällt. |
   | `Allow Qty Below 0 and Notify Customer` | Nachbestellungen zu akzeptieren, wenn die Menge unter null fällt, und den Kunden darüber zu informieren, dass die Bestellung noch aufgegeben werden kann. |

1. Für **[!UICONTROL Out-of-Stock Threshold]**, deaktivieren Sie die **[!UICONTROL Use Config Setting]** und geben Sie einen Betrag ein:

   | Wert | Beschreibung |
   | -- | -- |
   | Positiver Betrag | Geben Sie bei deaktivierten Rückständen einen positiven Wert ein. |
   | Null | Wenn Rückstände aktiviert sind, geben Sie `0` ermöglicht unendliche Rückläufe. |
   | Negativer Betrag | Bei aktivierten Rückständen wird die Eingabe eines negativen Werts empfohlen. Der Betrag wird der Verkaufsmenge hinzugefügt. Geben Sie beispielsweise `-50` um Bestellungen bis zu diesem Betrag zuzulassen. |

   ![Erweiterter Bestand, der für Rückorder konfiguriert wurde](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Klicks **[!UICONTROL Done]**, und dann **[!UICONTROL Save]**.
