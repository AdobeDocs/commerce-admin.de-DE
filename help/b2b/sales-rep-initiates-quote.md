---
title: Ankündigung eines Angebots für einen Käufer
description: Erfahren Sie, wie ein Verkäufer ein Angebot für einen bestimmten Käufer erstellen kann, um den Verhandlungsprozess zu starten. Der Verkäufer kann Angebote nur für Kunden einreichen, die mit einem Unternehmenskonto auf der ausgewählten Website verbunden sind.
exl-id: 7bbb281f-7b6a-45fa-b906-da314d159bc8
feature: B2B, Quotes
role: Admin, User
source-git-commit: 8130ccb809a6aec80db63c5a6ea9f47488248805
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# Initiieren eines Angebots für einen Käufer

Wenn Anführungszeichen in der [Konfiguration der Vertriebsfunktionen](configure-quotes.md)kann ein Vertriebsmitarbeiter den Verhandlungsprozess mit einem Firmenkäufer einleiten, indem er ein Angebot vom Administrator erstellt.

- Entwurfsangebote sind nur für den Verkäufer sichtbar.
- Kostenentwürfe können erst eingereicht werden, wenn der Vertriebsmitarbeiter Artikel, relevante Rabatte und Hinweise zur Erstellung des ersten Angebots für den Käufer hinzufügt.
- Ein Verkäufer kann ein Angebot aus den Anführungszeichen oder dem Kundenraster erstellen.

Der Vertriebsmitarbeiter sendet das Angebot an den Käufer, um den Verhandlungsprozess einzuleiten. Siehe [Anführungszeichen verhandeln](quote-price-negotiation.md).

## Angebotserstellung für Vertriebsmitarbeiter

Ein Vertriebsmitarbeiter kann ein Angebot aus den Anführungszeichen oder dem Kundenraster erstellen.

>[!NOTE]
>
>Eine Videodemo eines Verkäufers, der ein Angebot für einen Käufer erstellt, finden Sie unter [Kundenbetreuer initiiert das Angebot](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/b2b/b2b-quote/sales-rep-initiates-quote.html) in _Handelsvideos und Tutorials_.

### Erstellen eines Zitats aus dem Raster &quot;Anführungszeichen&quot;

1. Der Vertriebsmitarbeiter meldet sich als Administrator mit [Berechtigungen für Verkaufsvorgänge](../systems/permissions.md) , um Anführungszeichen zu verwalten.

1. Navigieren Sie im Admin zur [!UICONTROL Quotes] Raster durch Auswahl **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Quotes]**.

1. Erstellen Sie ein Angebot für einen Käufer.

   - Wählen Sie im Raster Anführungszeichen die Option **[!UICONTROL Create New Quote]**.

     ![Verkäufer, der vom Administrator ein Kaufangebot initiiert](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}

   - Im [!UICONTROL Create New Quote] auf, wählen Sie den Kunden (Firmenkäufer) aus, um das Angebot zu erstellen.

     ![Kunden für neues Angebot auswählen](./assets/quote-draft-from-admin-select-buyer.png){width="700" zoomable="yes"}

     Ein neues Anführungszeichen wird in `Draft` -Status.

     ![Neuer Entwurf eines Angebots, der vom Verkäufer erstellt wurde](./assets/quote-create-by-seller.png){width="700" zoomable="yes"}

   - Aktualisieren Sie den Anführungszeichen und ändern Sie das Ablaufdatum nach Bedarf.

   - Speichern Sie das Anführungszeichen als Entwurf.

## Vorbereiten des Kurses für den Käufer

Fügen Sie nach der Erstellung des Angebotsentwurfs Produktartikel hinzu, gewähren Sie Rabatte und kommunizieren Sie mit dem Käufer, indem Sie Kommentare und alle damit verbundenen Dateien zum Angebot hinzufügen. Senden Sie dann das Angebot an den Käufer zur Überprüfung oder speichern Sie es als Entwurf.

1. Hinzufügen von Elementen zum Anführungszeichen durch Auswahl von **[!UICONTROL Add Product By SKU]**. Geben Sie die SKU-Nummer und -Menge ein und wählen Sie **[!UICONTROL Add Product]**.

   ![Verkäufer, der Artikel zu einem Preisentwurf hinzufügt](./assets/quote-draft-add-items.png){width="675" zoomable="yes"}

1. Wenden Sie bei Bedarf Rabatte für Zeileneinträge auf Produkte an.

   - Aus dem [!UICONTROL Select] Aktionsmenü auswählen **[!UICONTROL Discount Item]**.

   - Im [!UICONTROL Discount Line item] Formular, wählen Sie die **[!UICONTROL Discount Type]**.

     ![Anwenden von Zeileneintrag-Rabatt auf Zitat](./assets/quote-discount-line-item.png){width="675" zoomable="yes"}

   - Im [!UICONTROL Discount] Geben Sie den Wert für den Rabatttyp ein. Wenn Sie beispielsweise einen prozentualen Rabatt ausgewählt haben, geben Sie 10 ein, um einen 10-%-Rabatt auf den Zeileneintrag anzuwenden.

   - [!BADGE 1.5.0-Beta-Funktionen]{type=Informative url="/help/b2b/release-notes.md" tooltip="Nur für Beta-Programmteilnehmer verfügbar"}

     Nach Bestätigung der Änderung wird der angewendete Rabattbetrag durch die Zeileneintrag-Attribute im Produktraster aktualisiert. Wenn der Rabatt gesperrt ist, wird ein Sperrsymbol angezeigt.

1. Wenden Sie bei Bedarf einen Rabatt auf Anführungszeichen an:

   - Im [!UICONTROL Quote Totals - Negotiated Price] wählen Sie den Rabatttyp aus und geben Sie dann den anzuwendenden Wert ein.

     ![Verkäufer fügt Rabatt auf Anführungsebene hinzu](./assets/quote-draft-total-discount.png){width="700" zoomable="yes"}

   Das Produktraster wird aktualisiert, um den Rabatt anzuzeigen.

1. Zusätzliche Informationen für den Käufer hinzufügen.

   Im **[!UICONTROL Negotiation - Comments]** hinzufügen, einen Hinweis hinzufügen und alle für den Käufer erforderlichen unterstützenden Dateien anhängen.

   ![Verkäufer fügt Informationen zum Käufer hinzu](./assets/quote-draft-add-info-for-buyer.png){width="700" zoomable="yes"}

   Standardmäßig wird ein [angehängte Datei](configure-quotes.md) kann bis zu 2 MB in einem der folgenden Dateiformate betragen: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG oder JPEG, PNG.

1. Verarbeiten Sie das Anführungszeichen.

   Speichern Sie das Angebot als Entwurf oder schicken Sie es an den Käufer.

   - Wenn Sie das Anführungszeichen als Entwurf speichern, wird der Status in `Draft` und eine Bestätigungsmeldung angezeigt wird.

   - Wenn Sie das Angebot an den Käufer senden, ändert sich der Status in `Submitted`. Der Käufer erhält eine E-Mail-Benachrichtigung, um das Angebot zu überprüfen. Das Angebot ist gesperrt, bis der Käufer es zur weiteren Verhandlung zurückgibt. Der Verkäufer kann das Angebot über das Zitat-Raster oder das Kundenraster anzeigen.

## Anzeigen und Erstellen von Anführungszeichen aus dem Kundenraster

1. Navigieren Sie im Admin zur [!UICONTROL Customer] Raster durch Auswahl **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL All Customers]**.

1. Wählen Sie die Kunden-ID für einen Firmenkäufer aus.

   ![Dem Käufer vorgelegter Angebotsentwurf](./assets/quote-view-customer-quotes.png){width="700" zoomable="yes"}

1. Auswählen **[!UICONTROL Edit]** , um die Kundeninformationen anzuzeigen.

1. Erstellen Sie ein Angebot für den Kunden, indem Sie **[!UICONTROL Create Quote]** und dem Prozess folgen, um das Angebot zu aktualisieren und an den Kunden zu senden.

1. Zeigen Sie die vorhandenen Angebote des Kunden an, indem Sie **[!UICONTROL Quotes]**.

   ![Dem Käufer vorgelegter Angebotsentwurf](./assets/quote-list-from-customer-information.png){width="700" zoomable="yes"}

1. Öffnen Sie ein Angebot durch Auswahl von **[!UICONTROL View]**.

Einzelheiten zur Verwaltung des Anführungsgesprächs finden Sie unter [Anführungszeichen verhandeln](quote-price-negotiation.md)
