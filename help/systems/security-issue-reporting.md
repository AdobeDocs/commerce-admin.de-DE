---
title: Meldung von Sicherheitsproblemen
description: Erfahren Sie, wie Sie die Kontaktinformationen und sicherheitsbezogenen Links konfigurieren, die von Sicherheitsforschern verwendet werden können, um Sicherheitsbedenken bezüglich Ihrer Site zu melden.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Meldung von Sicherheitsproblemen

Die `security.txt`-Datei enthält Kontaktinformationen und sicherheitsbezogene Links, die von Sicherheitsforschern verwendet werden können, um Sicherheitsbedenken über Ihre Website zu melden. Wenn sich Ihre Sicherheitsinformationen im Laufe der Zeit ändern, stellen Sie sicher, dass die Informationen in der `security.txt`-Datei auf dem neuesten Stand sind.

**_So konfigurieren Sie security.txt:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Klicken Sie im linken Bedienfeld unter _[!UICONTROL Security]_&#x200B;auf **[!UICONTROL Security.txt]**.

1. Legen Sie im _[!UICONTROL General]_&#x200B;Abschnitt **[!UICONTROL Enable]**&#x200B;auf `Yes` fest.

   ![Allgemeine Sicherheitskonfiguration](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. Geben Sie unter _[!UICONTROL Contact Information]_&#x200B;Folgendes ein:

   - Die E-Mail-Adresse und Telefonnummer der Person, die Sicherheitsprobleme für Ihren Store verwaltet.

   - Die URL der **[!UICONTROL Contact Page]** Ihres Stores. Bei dieser Seite kann es sich entweder um eine Liste von Store-Sicherheitskontakten oder um Ihre Seite _Kontakt_ handeln.

   ![Konfiguration der Kontaktinformationen](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. Geben Sie unter _[!UICONTROL Other Information]_&#x200B;Folgendes ein:

   - Die URL Ihres öffentlichen **[!UICONTROL Encryption]**. Beispiel: `https://example.com/pgp-key.txt`

   - Die URL einer **[!UICONTROL Acknowledgments]**, auf der Sicherheitsexperten für ihre Arbeit im Namen Ihres Stores ausgezeichnet werden.

   - Ihr **[!UICONTROL Preferred Languages]** für sicherheitsbezogene Kommunikation. Geben Sie für jede unterstützte Sprache den standardmäßigen [-Sprach](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)Code, getrennt durch ein Komma, ein. Um beispielsweise Englisch, Spanisch und Französisch anzugeben, geben Sie `en, es, fr` ein. Alle angegebenen Sprachen haben die gleiche Priorität, unabhängig von ihrer Reihenfolge ihres Erscheinungsbildes.

   - Die URL einer **[!UICONTROL Hiring]**, die sicherheitsbezogene Beschäftigungsmöglichkeiten mit Ihrem Geschäft auflistet.

   - Die URL Ihrer **[!UICONTROL Policy]**.

   - Die URL einer digitalen **[!UICONTROL Signature]**, die auf Ihrem Server gespeichert wird. Beispiel: `https://mystore.com/.well-known/security.txt.sig`

   Die digitale Signatur muss über die CLI (Befehlszeilenschnittstelle) des Servers eingerichtet werden. Weitere Informationen finden Sie unter [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) auf GitHub.

   ![Weitere Informationen](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
