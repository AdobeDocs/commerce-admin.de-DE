---
title: Angebotsanforderung
description: Erfahren Sie, wie mit einem Unternehmenskonto verknüpfte Kunden eine Angebotsanfrage stellen können.
exl-id: c52176a7-4076-4cea-8ddb-17e0d1a77fd9
feature: B2B, Quotes
role: Admin, User
source-git-commit: 21361104fa06425df0b44d5c7ae204ef4d9e21ac
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Angebotsanforderung

Wenn Anführungszeichen in der [Konfiguration der Vertriebsfunktionen](configure-quotes.md), kann ein autorisierter Käufer eines Unternehmens die Preisverhandlung einleiten, indem er ein Angebot von seinem Warenkorb anfordert. Ist ein Käufer nicht bereit, ein Angebot zur Verhandlung einzureichen, kann er es als Entwurf speichern.

>[!NOTE]
>
>Ein Angebot kann keine Rabattcodes oder Geschenkkarten enthalten.

## Customer Offer Request-Erlebnis

1. Der Kunde meldet sich bei seinem Benutzerkonto als Käufer an [Berechtigung](account-company-roles-permissions.md) , um ein Angebot anzufordern.

1. Fügt die Produkte, die im Angebot enthalten sein sollen, zum Warenkorb hinzu.

1. Auswahl **[!UICONTROL Request a Quote]**.

   ![Anfordern eines Angebots aus dem Warenkorb](./assets/quote-request-from-cart.png){width="700" zoomable="yes"}

1. Im **[!UICONTROL Add your comment]** gibt eine kurze Anmerkung ein, die die Anfrage beschreibt.

1. Fügt eine **[!UICONTROL Quote Name]**.

   ![Eingabe von Kommentaren und Namen](./assets/quote-request-from-cart-name-comments.png){width="400" zoomable="yes"}

1. Hängt bei Bedarf ein unterstützendes Dokument oder Bild an das Anführungszeichen an:

   - Auswahl **[!UICONTROL Attach file]**.
   - Wählt die Datei aus ihrem System aus.

   Standardmäßig wird ein [angehängte Datei](configure-quotes.md) kann bis zu 2 MB in einem der folgenden Dateiformate betragen: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG oder JPEG, PNG.

1. Erstellt und verarbeitet das Anführungszeichen:

   - Sendet das Angebot durch Auswahl an an den Verkäufer **[!UICONTROL Request a Quote]**.
   - [!BADGE 1.5.0-Beta-Funktion]{type=Informative url="/help/b2b/release-notes.md" tooltip="Nur für Beta-Programmteilnehmer verfügbar"}**[!UICONTROL Save as Draft]**.

     Wenn der Käufer das Angebot als Entwurf speichert, ist das Angebot im [!UICONTROL My Quotes] in `Draft` state. Er ist für den Verkäufer erst sichtbar, wenn der Käufer das Angebot öffnet und einreicht.
