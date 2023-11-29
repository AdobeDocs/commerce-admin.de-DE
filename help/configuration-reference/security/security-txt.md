---
title: '[!UICONTROL Security] &gt; [!UICONTROL Security.txt]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL Security] &gt; [!UICONTROL Security.txt] Seite des Commerce-Administrators.
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

Weitere Informationen zum Ändern dieser Konfigurationseinstellungen finden Sie unter [Sicherheitsfehlerberichte](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![Allgemein](./assets/txt-general.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable] | Webseite | Wenn diese Option aktiviert ist, wird eine `security.txt` -Datei gespeichert wird, die Informationen enthält, die von Sicherheitsexperten benötigt werden, um potenzielle Sicherheitslücken zu melden. Optionen:<br />**`Yes`**- Erstellt die `security.txt` -Datei anhand der in der Variablen _Kontaktangaben_ und _Weitere Informationen_ Abschnitte.<br />**`No`** - (Standard) Erstellt nicht die `security.txt` -Datei. |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![Kontaktangaben](./assets/txt-contact-info.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Email] | Webseite | Die E-Mail-Adresse, an die Sicherheitsberichte gesendet werden können. |
| [!UICONTROL Phone] | Webseite | Eine Telefonnummer, mit der Sicherheitsbedenken gemeldet werden können. |
| [!UICONTROL Contact Page] | Webseite | Die URL einer Seite auf Ihrer Site, auf der Sicherheitskontakte aufgelistet werden, oder Ihre _Kontakt_ Seite. Beispiele: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![Weitere Informationen](./assets/txt-other-info.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Encryption] | Webseite | Eine URL, die auf den Speicherort eines Verschlüsselungsschlüssels verweist, mit dem Sicherheitsforscher verschlüsselte Nachrichten senden können. _**Geben Sie in diesem Feld nicht den Verschlüsselungsschlüssel ein.**_ <br/><br/>Es liegt in der Verantwortung des Forschers zu überprüfen, ob der Schlüssel aus einer vertrauenswürdigen Quelle stammt. Forscher dürfen nicht davon ausgehen, dass der Schlüssel mit dem Schlüssel übereinstimmt, der zum Generieren der digitalen Signatur verwendet wurde. Beispiel:<br />OpenPGP-Schlüssel vom Webserver - `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Webseite | Eine URL, die auf eine Seite in Ihrem Store verweist, auf der Sicherheitsforscher quittiert werden, z. B.`https://mystore.com/hall-of-fame.html`. Um künftige Angriffe zu verhindern, fügen Sie nur eine allgemeine Beschreibung hinzu, ohne spezifische Informationen zu Schwachstellenproblemen anzuzeigen. Beispiel:<br />Wir danken den folgenden Forschern:<br />(jjjj/mm/tt) Justin Thyme - SQL - Injektion |
| [!UICONTROL Preferred Languages] | Webseite | Gibt mindestens eine bevorzugte Sicherheitsberichtssprache an. Mehrere zwei Zeichen trennen [Sprachcodes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) mit einem Komma. Alle angegebenen Sprachen haben dieselbe Priorität. Um beispielsweise Englisch, Spanisch und Französisch anzugeben, geben Sie `en, es, fr`. |
| [!UICONTROL Hiring] | Webseite | Die URL einer Seite auf der Site, die sicherheitsrelevante Auftragspositionen auflistet. Beispiel: `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Webseite | Die URL der Seite, die Ihre Sicherheitsrichtlinien und die Best Practices für die Meldung von Sicherheitslücken beschreibt. Beispiel: `https://mystore.com/security-reporting.html` Standard: `https://mystore.com/security` |
| [!UICONTROL Signature] | Webseite | Ein Link zu Ihrer digitalen Signaturdatei. Die digitale Signatur muss über die Befehlszeile generiert und im `.well-known` -Ordner auf dem Server. Weitere Informationen finden Sie unter [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) auf GitHub. Beispiel: `https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
