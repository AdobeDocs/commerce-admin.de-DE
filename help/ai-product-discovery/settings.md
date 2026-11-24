---
title: Anreicherungseinstellungen
description: Konfigurieren Sie den Versand, monatliche Agentendatenverkehrsaufträge und geeignete KI-Agenten, die von der Kataloganreicherung und der PDP-Anreicherung in der KI-Produkterkennung gemeinsam genutzt werden.
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%
---
# Anreicherungseinstellungen

Verwenden Sie die Registerkarte **[!UICONTROL Settings]** im Arbeitsbereich „KI-Produkterkennung“, um Ihre Adobe Commerce-Instanz zu konfigurieren. Wenn konfiguriert, werden Katalog- und PDP-Anreicherungen im Arbeitsbereich KI-Produkterkennung angezeigt.

Die Felder auf dieser Registerkarte identifizieren die [!DNL Adobe Commerce] Umgebung und die Store-Ansicht, mit der sich AI Product Discovery verbindet. Informationen zu den Anforderungen an die IMS-Anmeldung und die Organisation finden Sie unter [Voraussetzungen für die KI-Produkterkennung](prerequisites.md).

1. Navigieren Sie in Admin zu **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]** oder **[!UICONTROL Product Details Page Enrichment]**.
1. Wählen Sie in der **[!UICONTROL Scope]** oben auf der Seite die Store-Ansicht aus, die Sie konfigurieren möchten, oder lassen Sie **[!UICONTROL All Store Views]**, um die Einstellungen in allen Store-Ansichten zu verwalten.
1. Öffnen Sie die Registerkarte **[!UICONTROL Settings]** .
1. Erweitern Sie in **[!UICONTROL Commerce Configuration]** das Ansichtsfeld Store mit der Bezeichnung und der URL.

   Geben Sie die Details Ihrer [!DNL Adobe Commerce] Umgebung an, um den KI-Produkterkennungs-Service und Audit-Workflows zu aktivieren.

   ![Commerce-Konfiguration auf der Registerkarte „Kataloganreicherungseinstellungen“](./assets/catalog-enrichment-commerce-config.png){zoomable="yes"}

1. Geben Sie die erforderlichen Verbindungsdetails für die Store-Ansicht ein.

   - **[!UICONTROL Store View URL]**: URL, die der Store-Ansicht entspricht (z. B. `https://brand.example.com/fr/`).
   - **[!UICONTROL Environment ID]**: Eindeutige Kennung für die [!DNL Adobe Commerce] Umgebung, auf die die Verbindung zugreift.
   - **[!UICONTROL Website Code]**, **[!UICONTROL Store Code]** und **[!UICONTROL Store View Code]**: Website-, Store- und Store-Ansichtscodes für die Commerce-Website. Diese Werte müssen mit den Codes in Ihrem Commerce-Admin übereinstimmen.
   - **[!UICONTROL Host Name]**: Host-Name Ihrer [!DNL Adobe Commerce].
   - **(Optional - nur für Kataloganreicherung)** Wählen Sie unter **[!UICONTROL Catalog field limits]** die Option **[!UICONTROL Limit maximum characters for product name]** und geben Sie die Zeichenbeschränkung für alle generierten Produktnamen an. Wählen Sie **[!UICONTROL Limit maximum characters for product description]** aus und geben Sie die Zeichenbeschränkung für alle generierten Produktbeschreibungen an.

1. Klicken Sie auf **[!UICONTROL Save]**.

Warten Sie nach dem Speichern, bis ein erster Synchronisierungs- oder Validierungsauftrag abgeschlossen ist, bevor Sie sich auf die Katalog- oder Auditergebnisse für diese Store-Ansicht verlassen. Es kann bis zu 24 Stunden dauern, bis Produktvorschläge auf der **[!UICONTROL Catalog Enrichment]** angezeigt werden.

Um eine Store-Ansichtskonfiguration zu entfernen, erweitern Sie diesen Eintrag und klicken Sie auf **[!UICONTROL Delete]**.

## Feldbeschreibungen {#commerce-connection-fields}

Erforderliche Felder sind im **[!UICONTROL Commerce Configuration]** Formular mit einem Sternchen (*) gekennzeichnet.

| Feld | Erforderlich | Beschreibung |
| --- | --- | --- |
| URL für Store-Ansicht | Ja | URL, die der Store-Ansicht entspricht (z. B. `https://brand.example.com/fr/`) |
| Umgebungs-ID | Ja | Eindeutige Kennung für die [!DNL Adobe Commerce] Umgebung, auf die die Verbindung zugreift. |
| Website-Code | Ja | Website-Code der Commerce-Website. |
| Speichercode | Ja | Store-Code der Commerce-Website. |
| Code für Shop-Ansicht | Ja | Store-Ansicht der Commerce-Website. |
| Host-Name | Ja | Hostname der [!DNL Adobe Commerce]. |
| Begrenzungen für Katalogfelder (nur Kataloganreicherung) | Nein | Definieren Sie Zeichenbeschränkungen für alle generierten Produktnamen und Beschreibungen. |
