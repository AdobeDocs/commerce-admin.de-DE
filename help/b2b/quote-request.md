---
title: Angebotsanforderung
description: Erfahren Sie, wie mit einem Unternehmenskonto verknüpfte Kunden eine Angebotsanfrage stellen können.
exl-id: c52176a7-4076-4cea-8ddb-17e0d1a77fd9
feature: B2B, Quotes
role: Admin, User
source-git-commit: b53d77364f09e587813c50221ebd85ac633f1296
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Angebotsanforderung

Wenn Anführungszeichen in der Konfiguration der [Verkaufsfunktionen](configure-quotes.md) aktiviert sind, kann ein autorisierter Käufer eines Unternehmens den Preisverhandelungsprozess starten, indem er ein Angebot aus seinem Warenkorb anfordert. Ist ein Käufer nicht bereit, ein Angebot zur Verhandlung einzureichen, kann er es als Entwurf speichern.

>[!NOTE]
>
>Ein Angebot kann keine Rabattcodes oder Geschenkkarten enthalten.

## Customer Offer Request-Erlebnis

1. Der Kunde meldet sich bei seinem Benutzerkonto als Käufer mit [Berechtigung](account-company-roles-permissions.md) an, um ein Angebot anzufordern.

1. Fügt die Produkte hinzu, die in das Angebot aufgenommen werden sollen, und zwar zum Warenkorb.

   >[!TIP]
   > 
   >Kunden können mit [Quick Order](quick-order.md) schneller eine Liste von Produkt-SKUs zum Warenkorb hinzufügen.

1. Wählt **[!UICONTROL Request a Quote]** aus.

   ![Anfordern eines Angebots aus dem Warenkorb](./assets/quote-request-from-cart.png){width="700" zoomable="yes"}

1. In das Feld **[!UICONTROL Add your comment]** gibt der Kunde eine kurze Anmerkung ein, um die Anfrage zu beschreiben.

1. Fügt einen **[!UICONTROL Quote Name]** ein.

   ![Eingabe der Anführungszeichen, Kommentare und Namen](./assets/quote-request-from-cart-name-comments.png){width="400" zoomable="yes"}

1. Hängt bei Bedarf ein unterstützendes Dokument oder Bild an das Anführungszeichen an:

   - Wählt **[!UICONTROL Attach file]** aus.
   - Wählt die Datei aus ihrem System aus.

   Standardmäßig kann eine [angehängte Datei](configure-quotes.md) in einem der folgenden Dateiformate bis zu 2 MB groß sein: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG oder JPEG, PNG.

1. Erstellt und verarbeitet das Anführungszeichen:

   - Sendet das Angebot durch Auswahl von **[!UICONTROL Request a Quote]** an den Verkäufer.
   - [!BADGE 1.5.0-Beta-Funktion]{type=Informative url="/help/b2b/release-notes.md" tooltip="Nur für Beta-Programmteilnehmer verfügbar"}**[!UICONTROL Save as Draft]**.

     Wenn der Käufer das Angebot als Entwurf speichert, ist das Angebot im Status [!UICONTROL My Quotes] im Status `Draft` verfügbar. Für den Verkäufer sind die Angebote nicht sichtbar, bis der Käufer sie zur Überprüfung sendet.
