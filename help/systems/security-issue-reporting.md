---
title: Meldung von Sicherheitsproblemen
description: Erfahren Sie, wie Sie die Kontaktinformationen und sicherheitsbezogenen Links konfigurieren, die von Sicherheitsforschern verwendet werden können, um Sicherheitsbedenken bezüglich Ihrer Site zu melden.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/tXZFSpgx9r2t-tN2Oc7L2aiPDlL6hSZBRC9pHjzcjQk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 315
ht-degree: 0%

---

# Meldung von Sicherheitsproblemen

Die `security.txt`-Datei enthält Kontaktinformationen und sicherheitsbezogene Links, die von Sicherheitsforschern verwendet werden können, um Sicherheitsbedenken über Ihre Website zu melden. Wenn sich Ihre Sicherheitsinformationen im Laufe der Zeit ändern, stellen Sie sicher, dass die Informationen in der `security.txt`-Datei auf dem neuesten Stand sind.

**_So konfigurieren Sie security.txt:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Klicken Sie im linken Bedienfeld unter _[!UICONTROL Security]_auf **[!UICONTROL Security.txt]**.

1. Legen Sie im _[!UICONTROL General]_Abschnitt **[!UICONTROL Enable]**auf `Yes` fest.

   ![Allgemeine Sicherheitskonfiguration](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. Geben Sie unter _[!UICONTROL Contact Information]_Folgendes ein:

   - Die E-Mail-Adresse und Telefonnummer der Person, die Sicherheitsprobleme für Ihren Store verwaltet.

   - Die URL der **[!UICONTROL Contact Page]** Ihres Stores. Bei dieser Seite kann es sich entweder um eine Liste von Store-Sicherheitskontakten oder um Ihre Seite _Kontakt_ handeln.

   ![Konfiguration der Kontaktinformationen](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. Geben Sie unter _[!UICONTROL Other Information]_Folgendes ein:

   - Die URL Ihres öffentlichen **[!UICONTROL Encryption]**. Beispiel: `https://example.com/pgp-key.txt`

   - Die URL einer **[!UICONTROL Acknowledgments]**, auf der Sicherheitsexperten für ihre Arbeit im Namen Ihres Stores ausgezeichnet werden.

   - Ihr **[!UICONTROL Preferred Languages]** für sicherheitsbezogene Kommunikation. Geben Sie für jede unterstützte Sprache den standardmäßigen [-Sprach](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)Code, getrennt durch ein Komma, ein. Um beispielsweise Englisch, Spanisch und Französisch anzugeben, geben Sie `en, es, fr` ein. Alle angegebenen Sprachen haben die gleiche Priorität, unabhängig von ihrer Reihenfolge ihres Erscheinungsbildes.

   - Die URL einer **[!UICONTROL Hiring]**, die sicherheitsbezogene Beschäftigungsmöglichkeiten mit Ihrem Geschäft auflistet.

   - Die URL Ihrer **[!UICONTROL Policy]**.

   - Die URL einer digitalen **[!UICONTROL Signature]**, die auf Ihrem Server gespeichert wird. Beispiel: `https://mystore.com/.well-known/security.txt.sig`

   Die digitale Signatur muss über die CLI (Befehlszeilenschnittstelle) des Servers eingerichtet werden. Weitere Informationen finden Sie unter [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) auf GitHub.

   ![Weitere Informationen](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
