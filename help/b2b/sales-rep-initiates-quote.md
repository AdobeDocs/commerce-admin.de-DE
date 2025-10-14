---
title: Angebot für einen Käufer initiieren
description: Erfahren Sie, wie ein Verkäufer ein Angebot für einen bestimmten Käufer erstellen kann, um den Verhandlungsprozess zu starten. Der Verkäufer kann Angebote nur für Kunden einreichen, die mit einem Unternehmenskonto auf der ausgewählten Website verbunden sind.
exl-id: 7bbb281f-7b6a-45fa-b906-da314d159bc8
feature: B2B, Quotes
role: Admin, User
source-git-commit: 69396421bae610ff02b12054bdea2278a8c0efe5
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Starten eines Angebots für einen Käufer

Wenn Angebote in der Konfiguration [Verkaufsfunktionen](configure-quotes.md) aktiviert sind, kann ein Vertriebsmitarbeiter den Verhandlungsprozess mit einem Firmenkäufer starten, indem er ein Angebot vom Administrator erstellt.

- Angebotsentwürfe sind nur für den Verkäufer sichtbar.
- Angebotsentwürfe können erst eingereicht werden, wenn der Vertriebsmitarbeiter Artikel, relevante Rabatte und Notizen hinzufügt, um das erste Angebot für den Käufer zu erstellen.
- Ein Verkäufer kann ein Angebot aus dem Angebots- oder Kundenraster erstellen.

Der Vertriebsmitarbeiter sendet das Angebot an den Käufer, um den Verhandlungsprozess einzuleiten. Siehe [Aushandeln eines Angebots](quote-price-negotiation.md).

## Erlebnis bei der Angebotserstellung durch Vertriebsmitarbeiter

Ein Vertriebsmitarbeiter kann ein Angebot aus dem Angebots- oder Kundenraster erstellen.

>[!NOTE]
>
>Eine Videodemo eines Verkäufers, der ein Angebot für einen Käufer erstellt, finden Sie unter [Vertriebsmitarbeiter initiiert das Angebot](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/b2b/b2b-quote/sales-rep-initiates-quote.html?lang=de) in _Commerce-Videos und -Tutorials_.

### Erstellen eines Angebots aus dem Anführungsraster

1. Der Vertriebsmitarbeiter meldet sich beim Administrator als Administrator mit „Berechtigungen für [&#x200B; Vorgänge“ an](../systems/permissions.md) um Angebote zu verwalten.

1. Wechseln Sie in der Admin-Liste zum [!UICONTROL Quotes] Raster, indem Sie **[!UICONTROL Sales]** auswählen, und wählen Sie dann **[!UICONTROL Quotes]** aus.

1. Erstellen Sie ein Angebot für einen Einkäufer.

   - Wählen Sie im Raster Anführungszeichen die Option **[!UICONTROL Create New Quote]** aus.

     ![Verkäufer, der ein Kaufangebot vom Administrator initiiert](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}

   - Wählen Sie auf der Seite [!UICONTROL Create New Quote] den Kunden (Firmenkäufer) aus, um das Angebot zu erstellen.

     ![Kunden für neues Angebot auswählen](./assets/quote-draft-from-admin-select-buyer.png){width="700" zoomable="yes"}

     Im Status `Draft` wird ein neues Angebot angezeigt.

     ![Neuer Angebotsentwurf vom Verkäufer erstellt](./assets/quote-create-by-seller.png){width="700" zoomable="yes"}

   - Aktualisieren Sie den Angebotsnamen und ändern Sie das Ablaufdatum nach Bedarf.

   - Speichern Sie das Angebot als Entwurf.

## Angebot für den Käufer vorbereiten

Fügen Sie nach der Erstellung des Angebotsentwurfs Produktelemente hinzu, wenden Sie Rabatte an und kommunizieren Sie mit dem Käufer, indem Sie Kommentare und alle zugehörigen Dateien zum Angebot hinzufügen. Senden Sie dann das Angebot zur Überprüfung an den Käufer oder speichern Sie es als Entwurf.

1. Fügen Sie dem Angebot Elemente hinzu, indem Sie **[!UICONTROL Add Product By SKU]** auswählen. Geben Sie die SKU-Nummer und die Menge ein, und wählen Sie dann **[!UICONTROL Add Product]**.

   ![Verkäufer fügt Artikel zum Angebotsentwurf für Käufer hinzu](./assets/quote-draft-add-items.png){width="675" zoomable="yes"}

1. Wenden Sie bei Bedarf Positionsrabatte auf Produkte an.

   - Wählen Sie im Menü [!UICONTROL Select] die Option **[!UICONTROL Discount Item]** aus.

   - Wählen Sie im [!UICONTROL Discount Line item] Formular die **[!UICONTROL Discount Type]** aus.

     ![Positionsrabatt auf Angebot anwenden](./assets/quote-discount-line-item.png){width="675" zoomable="yes"}

   - Geben Sie im Feld [!UICONTROL Discount] den Wert für den Rabatttyp ein. Wenn Sie beispielsweise einen prozentualen Rabatt ausgewählt haben, geben Sie 10 ein, um dem Zeileneintrag einen Rabatt von 10 % zuzuweisen.

   - Optional können Sie den Rabattwert für den Einzelposten sperren, damit der Produktpreis nicht durch Rabatte auf der Angebotsebene weiter reduziert wird.

     Nach Bestätigung der Änderung werden die Positionsattribute im Produktraster aktualisiert, um den angewendeten Rabattbetrag anzuzeigen. Wenn der Rabatt gesperrt ist, wird ein Sperrsymbol angezeigt.

   Ein Vertriebsmitarbeiter kann einen Rabatt für einen bestimmten Zeileneintrag in einem Angebot anfordern.

   >[!NOTE]
   >
   >Eine Videodemo zur Funktionsweise von Rabatten bei dem Zeileneintrag finden Sie unter [Der Vertriebsmitarbeiter wendet Rabatt auf einen Angebotspositionselement an](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/b2b/b2b-quote/quote-line-item-discount.html?lang=de) in _Commerce-Videos und -Tutorials_.

1. Wenden Sie bei Bedarf einen Rabatt auf Angebotsebene an:

   - Wählen Sie im Abschnitt [!UICONTROL Quote Totals - Negotiated Price] den Rabatttyp aus und geben Sie dann den anzuwendenden Wert ein.

     ![Verkäufer fügt Rabatt auf Angebotsebene hinzu](./assets/quote-draft-total-discount.png){width="700" zoomable="yes"}

   Das Produktraster wird aktualisiert, um den Rabatt anzuzeigen.

1. Zusätzliche Informationen für den Käufer hinzufügen.

   Fügen Sie auf der Registerkarte **[!UICONTROL Negotiation - Comments]** einen Hinweis hinzu und fügen Sie alle unterstützenden Dateien hinzu, die für den Käufer erforderlich sind.

   ![Der Verkäufer fügt Informationen für den Käufer hinzu](./assets/quote-draft-add-info-for-buyer.png){width="700" zoomable="yes"}

   Standardmäßig kann eine [angehängte Datei](configure-quotes.md) bis zu 2 MB in einem der folgenden Dateiformate betragen: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG oder JPEG, PNG.

1. Lieferadresse während der Verhandlungen hinzufügen.

   Ein Vertriebsmitarbeiter kann eine Versand- und Lieferauswahl treffen, sobald der Käufer eine Lieferadresse zum Angebot hinzugefügt hat.

   Versandoptionen sind beim Checkout gesperrt.

   Weitere Informationen finden Sie unter [Meine Anführungszeichen](account-dashboard-my-quotes.md#adding-a-shipping-address).

1. Verarbeiten Sie das Angebot.

   Speichern Sie das Angebot als Entwurf oder senden Sie es an den Käufer.

   - Wenn Sie das Angebot als Entwurf speichern, wird der Status auf `Draft` aktualisiert und eine Bestätigungsmeldung wird angezeigt.

   - Wenn Sie das Angebot an den Käufer senden, ändert sich der Status in `Submitted`. Der Käufer erhält eine E-Mail-Benachrichtigung, um das Angebot zu überprüfen. Das Angebot ist gesperrt, bis der Käufer es zur weiteren Verhandlung zurückgibt. Der Verkäufer kann das Angebot im Angebotsraster oder im Kundenraster anzeigen.

## Angebote aus dem Kundenraster anzeigen und erstellen

1. Wechseln Sie in der Admin-Liste zum [!UICONTROL Customer] Raster, indem Sie **[!UICONTROL Customers]** auswählen, und wählen Sie dann **[!UICONTROL All Customers]** aus.

1. Wählen Sie die Kunden-ID für einen Unternehmenskäufer aus.

   ![Bestätigungsentwurf für Angebot an Käufer gesendet](./assets/quote-view-customer-quotes.png){width="700" zoomable="yes"}

1. Wählen Sie **[!UICONTROL Edit]** aus, um die Kundeninformationen anzuzeigen.

1. Erstellen Sie ein Angebot für den Kunden, indem Sie den Prozess zum Aktualisieren des Angebotsentwurfs und zum Senden an den Kunden auswählen, **[!UICONTROL Create Quote]** und befolgen.

1. Zeigen Sie die vorhandenen Angebote der Kunden an, indem Sie **[!UICONTROL Quotes]** auswählen.

   ![Bestätigungsentwurf für Angebot an Käufer gesendet](./assets/quote-list-from-customer-information.png){width="700" zoomable="yes"}

1. Öffnen Sie ein Angebot, indem Sie **[!UICONTROL View]** auswählen.

Weitere Informationen zur Verwaltung des Angebotsaushandlungsprozesses finden Sie unter [Angebot aushandeln](quote-price-negotiation.md)
