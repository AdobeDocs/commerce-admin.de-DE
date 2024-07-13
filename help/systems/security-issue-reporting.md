---
title: Sicherheitsfehlerberichte
description: Erfahren Sie, wie Sie die Kontaktinformationen und sicherheitsbezogenen Links konfigurieren, die von Sicherheitsexperten verwendet werden können, um Sicherheitsbedenken über Ihre Site zu melden.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Sicherheitsfehlerberichte

Die Datei `security.txt` enthält Kontaktinformationen und sicherheitsbezogene Links, die von Sicherheitsexperten verwendet werden können, um Sicherheitsbedenken über Ihre Site zu melden. Wenn sich Ihre Sicherheitsinformationen im Laufe der Zeit ändern, stellen Sie sicher, dass die Informationen in der Datei `security.txt` auf dem neuesten Stand sind.

**_So konfigurieren Sie security.txt:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Klicken Sie im linken Bereich unter _[!UICONTROL Security]_auf **[!UICONTROL Security.txt]**.

1. Setzen Sie im Abschnitt _[!UICONTROL General]_**[!UICONTROL Enable]**auf `Yes`.

   ![Allgemeine Sicherheitskonfiguration](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. Geben Sie unter _[!UICONTROL Contact Information]_Folgendes ein:

   - Die E-Mail-Adresse und die Telefonnummer der Person, die Sicherheitsprobleme für Ihren Store verwaltet.

   - Die URL des **[!UICONTROL Contact Page]** Ihres Stores. Diese Seite kann entweder eine Liste von Sicherheitskontakten für den Speicher oder Ihre Seite _Kontakt_ sein.

   ![Konfiguration der Kontaktinformationen](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. Geben Sie unter _[!UICONTROL Other Information]_Folgendes ein:

   - Die URL Ihres öffentlichen **[!UICONTROL Encryption]** -Schlüssels. Beispiel: `https://example.com/pgp-key.txt`

   - Die URL einer **[!UICONTROL Acknowledgments]** -Seite, auf der Sicherheitsforscher für ihre Bemühungen im Namen Ihres Stores erkannt werden.

   - Ihre **[!UICONTROL Preferred Languages]** für sicherheitsbezogene Kommunikation. Geben Sie den standardmäßigen zweistelligen [Sprachcode](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) für jede unterstützte Sprache ein, getrennt durch ein Komma. Geben Sie beispielsweise `en, es, fr` ein, um Englisch, Spanisch und Französisch anzugeben. Alle angegebenen Sprachen haben unabhängig von ihrer Reihenfolge dieselbe Priorität.

   - Die URL einer **[!UICONTROL Hiring]** -Seite, die sicherheitsrelevante Beschäftigungsmöglichkeiten für Ihren Store auflistet.

   - Die URL Ihrer Sicherheitsseite **[!UICONTROL Policy]**.

   - Die URL einer digitalen **[!UICONTROL Signature]** -Datei, die auf Ihrem Server gespeichert wird. Beispiel: `https://mystore.com/.well-known/security.txt.sig`

   Die digitale Signatur muss über die Befehlszeilenschnittstelle (CLI) des Servers eingerichtet werden. Weitere Informationen finden Sie unter [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) auf GitHub.

   ![Weitere Informationen](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
