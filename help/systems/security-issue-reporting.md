---
title: Sicherheitsfehlerberichte
description: Erfahren Sie, wie Sie die Kontaktinformationen und sicherheitsbezogenen Links konfigurieren, die von Sicherheitsexperten verwendet werden können, um Sicherheitsbedenken über Ihre Site zu melden.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 1%

---

# Sicherheitsfehlerberichte

Die `security.txt` enthält Kontaktinformationen und sicherheitsbezogene Links, die von Sicherheitsexperten verwendet werden können, um Sicherheitsbedenken über Ihre Site zu melden. Wenn sich Ihre Sicherheitsinformationen im Laufe der Zeit ändern, stellen Sie sicher, dass die Informationen in der `security.txt` ist auf dem neuesten Stand.

**_So konfigurieren Sie security.txt:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Bereich unter _[!UICONTROL Security]_klicken **[!UICONTROL Security.txt]**.

1. Im _[!UICONTROL General]_Abschnitt, festlegen **[!UICONTROL Enable]**nach `Yes`.

   ![Allgemeine Sicherheitskonfiguration](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. under _[!UICONTROL Contact Information]_Geben Sie Folgendes ein:

   - Die E-Mail-Adresse und die Telefonnummer der Person, die Sicherheitsprobleme für Ihren Store verwaltet.

   - Die URL der **[!UICONTROL Contact Page]**. Diese Seite kann entweder eine Liste von Sicherheitskontakten für den Store oder Ihre _Kontakt_ Seite.

   ![Konfiguration von Kontaktinformationen](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. under _[!UICONTROL Other Information]_Geben Sie Folgendes ein:

   - Die URL Ihrer öffentlichen **[!UICONTROL Encryption]** Schlüssel. Beispiel: `https://example.com/pgp-key.txt`

   - Die URL eines **[!UICONTROL Acknowledgments]** Seite, auf der Sicherheitsforscher für ihre Bemühungen im Namen Ihres Stores anerkannt werden.

   - Ihre **[!UICONTROL Preferred Languages]** für sicherheitsbezogene Kommunikation. Standardmäßige zweistellige Angabe [Sprachcode](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) für jede unterstützte Sprache, durch ein Komma getrennt. Um beispielsweise Englisch, Spanisch und Französisch anzugeben, geben Sie `en, es, fr`. Alle angegebenen Sprachen haben unabhängig von ihrer Reihenfolge dieselbe Priorität.

   - Die URL einer **[!UICONTROL Hiring]** -Seite, die sicherheitsbezogene Beschäftigungsmöglichkeiten für Ihren Store auflistet.

   - Die URL Ihrer Sicherheit **[!UICONTROL Policy]** Seite.

   - Die URL eines digitalen **[!UICONTROL Signature]** -Datei, die auf Ihrem Server gespeichert ist. Beispiel: `https://mystore.com/.well-known/security.txt.sig`

   Die digitale Signatur muss über die Befehlszeilenschnittstelle (CLI) des Servers eingerichtet werden. Weitere Informationen finden Sie unter [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) auf GitHub.

   ![Weitere Informationen](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
