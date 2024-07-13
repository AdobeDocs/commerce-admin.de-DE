---
title: '[!UICONTROL Security] &gt; [!UICONTROL Security.txt]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Security] &gt; [!UICONTROL Security.txt] des Commerce-Administrators.
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

Weitere Informationen zum Ändern dieser Konfigurationseinstellungen finden Sie unter [Berichterstellung zu Sicherheitsproblemen](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![Allgemein](./assets/txt-general.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable] | Webseite | Wenn diese Option aktiviert ist, wird eine `security.txt` -Datei gespeichert, die Informationen enthält, die von Sicherheitsexperten benötigt werden, um potenzielle Sicherheitslücken zu melden. Optionen:<br />**`Yes`**- Erstellt die Datei `security.txt` anhand der Informationen, die in den Abschnitten _Kontaktdaten_ und _Weitere Informationen_ eingegeben wurden.<br />**`No`** - (Standard) Erstellt die Datei `security.txt` nicht. |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![Kontaktinformationen](./assets/txt-contact-info.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Email] | Webseite | Die E-Mail-Adresse, an die Sicherheitsberichte gesendet werden können. |
| [!UICONTROL Phone] | Webseite | Eine Telefonnummer, mit der Sicherheitsbedenken gemeldet werden können. |
| [!UICONTROL Contact Page] | Webseite | Die URL einer Seite auf Ihrer Site, auf der Sicherheitskontakte aufgelistet werden, oder Ihre Seite _Kontakt zu uns aufnehmen_ . Beispiele: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![Weitere Informationen](./assets/txt-other-info.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Encryption] | Webseite | Eine URL, die auf den Speicherort eines Verschlüsselungsschlüssels verweist, mit dem Sicherheitsforscher verschlüsselte Nachrichten senden können. _**Geben Sie den Verschlüsselungsschlüssel nicht in dieses Feld ein.**_ <br/><br/>Der Forscher muss sicherstellen, dass der Schlüssel aus einer vertrauenswürdigen Quelle stammt. Forscher dürfen nicht davon ausgehen, dass der Schlüssel mit dem Schlüssel übereinstimmt, der zum Generieren der digitalen Signatur verwendet wurde. Beispiel:<br />OpenPGP-Schlüssel vom Webserver - `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Webseite | Eine URL, die auf eine Seite in Ihrem Store verweist, auf der Sicherheitsforscher quittiert werden, z. B.`https://mystore.com/hall-of-fame.html`. Um künftige Angriffe zu verhindern, fügen Sie nur eine allgemeine Beschreibung hinzu, ohne spezifische Informationen zu Schwachstellenproblemen anzuzeigen. Beispiel:<br />Wir möchten den folgenden Forschern danken:<br />(jjjj/mm/tt) Justin Thyme - SQL-Injektion |
| [!UICONTROL Preferred Languages] | Webseite | Gibt mindestens eine bevorzugte Sicherheitsberichtssprache an. Trennen Sie mehrere zweistellige [Sprachcodes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) durch ein Komma. Alle angegebenen Sprachen haben dieselbe Priorität. Geben Sie beispielsweise `en, es, fr` ein, um Englisch, Spanisch und Französisch anzugeben. |
| [!UICONTROL Hiring] | Webseite | Die URL einer Seite auf der Site, die sicherheitsrelevante Auftragspositionen auflistet. Beispiel: `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Webseite | Die URL der Seite, die Ihre Sicherheitsrichtlinien und die Best Practices für die Meldung von Sicherheitslücken beschreibt. Beispiel: `https://mystore.com/security-reporting.html` Standard: `https://mystore.com/security` |
| [!UICONTROL Signature] | Webseite | Ein Link zu Ihrer digitalen Signaturdatei. Die digitale Signatur muss über die Befehlszeile generiert und im Ordner &quot;`.well-known`&quot;auf dem Server gespeichert werden. Weitere Informationen finden Sie unter [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) auf GitHub. Beispiel: `https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
