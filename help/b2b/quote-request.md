---
title: Angebotsanfrage
description: Erfahren Sie, wie Kunden, die mit einem Unternehmenskonto verknüpft sind, eine Angebotsanfrage senden können.
exl-id: c52176a7-4076-4cea-8ddb-17e0d1a77fd9
feature: B2B, Quotes
role: Admin, User
TQID: 'https://experienceleague.adobe.com/lRPDBgKHCTklbiZ1QWsvXD--n86T-IySJDu9nv-umsU'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 792a7e9b-6519-5e99-a913-56c3dd2408da
    internal-label: Quotes
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%
---
# Angebotsanfrage

Wenn Angebote in der Konfiguration [Verkaufsfunktionen](configure-quotes.md) aktiviert sind, kann ein autorisierter Käufer eines Unternehmens den Preisaushandlungsprozess starten, indem er ein Angebot aus seinem Warenkorb anfordert. Wenn ein Käufer nicht bereit ist, ein Angebot zur Verhandlung einzureichen, kann er es als Entwurf speichern.

>[!NOTE]
>
>Eine Angebotsanfrage darf keine Rabattcodes oder Geschenkgutscheine enthalten.

## Kundenerlebnis bei Angebotsanfrage

1. Der Kunde meldet sich bei seinem Benutzerkonto als Käufer mit ([) &#x200B;](account-company-roles-permissions.md), um ein Angebot anzufordern.

1. Fügt die Produkte, die im Angebot enthalten sein sollen, zum Warenkorb hinzu.

   >[!TIP]
   > 
   >Kunden können eine Liste von Produkt-SKUs mithilfe von &quot;[&quot; schneller in den Warenkorb &#x200B;](quick-order.md).

1. Wählt **[!UICONTROL Request a Quote]** aus.

   ![Ein Angebot aus dem Warenkorb anfordern](./assets/quote-request-from-cart.png){width="700" zoomable="yes"}

1. Im **[!UICONTROL Add your comment]** Feld gibt der Kunde eine kurze Anmerkung ein, um die Anfrage zu beschreiben.

1. Gibt einen **[!UICONTROL Quote Name]** ein.

   ![Eingeben der Angebotskommentare und des Namens](./assets/quote-request-from-cart-name-comments.png){width="400" zoomable="yes"}

1. Hängt bei Bedarf ein unterstützendes Dokument oder Bild an das Angebot an:

   - Wählt **[!UICONTROL Attach file]** aus.
   - Wählt die Datei aus ihrem System aus.

   Standardmäßig kann eine [angehängte Datei](configure-quotes.md) bis zu 2 MB in einem der folgenden Dateiformate betragen: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG oder JPEG, PNG.

1. Erstellt und verarbeitet das Angebot:

   - Sendet das Angebot an den Verkäufer durch Auswahl von **[!UICONTROL Request a Quote]**.
   - Speichert das Angebot als Entwurf, indem **[!UICONTROL Save as Draft]** ausgewählt wird.

     Wenn der Käufer das Angebot als Entwurf speichert, ist das Angebot in [!UICONTROL My Quotes] in `Draft` verfügbar. Angebotsentwürfe sind für den Verkäufer erst sichtbar, wenn der Käufer sie zur Überprüfung sendet.
