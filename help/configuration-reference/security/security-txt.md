---
title: '[!UICONTROL Security] &gt; [!UICONTROL Security.txt]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Security] &gt; [!UICONTROL Security.txt] des Commerce Admin-Bereichs.
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

Weitere Informationen zum Ändern dieser Konfigurationseinstellungen finden Sie unter [Sicherheitsproblemberichte](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![Allgemein](./assets/txt-general.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable] | Website | Wenn diese Option aktiviert ist, wird eine `security.txt`-Datei gespeichert, die Informationen enthält, die von Sicherheitsforschern benötigt werden, um potenzielle Sicherheitslücken an Sie zu melden. Optionen: <br />**`Yes`**- Erstellt die `security.txt` basierend auf den Informationen, die in den Abschnitten _Kontaktinformationen_ und _Sonstige Informationen_ eingegeben wurden.<br />**`No`** - (Standard) Erstellt nicht die `security.txt`. |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![Kontaktinformationen](./assets/txt-contact-info.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Email] | Website | Die E-Mail-Adresse, an die Sicherheitsberichte gesendet werden können. |
| [!UICONTROL Phone] | Website | Eine Telefonnummer, unter der Sicherheitsbedenken gemeldet werden können. |
| [!UICONTROL Contact Page] | Website | Die URL einer Seite auf Ihrer Site, auf der Sicherheitskontakte aufgelistet sind, oder Ihre Seite _Kontakt_. Beispiele: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![Weitere Informationen](./assets/txt-other-info.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Encryption] | Website | Eine URL, die auf den Speicherort eines Verschlüsselungsschlüssels verweist, den Sicherheitsforscher zum Senden verschlüsselter Nachrichten verwenden können. _&#x200B;**Geben Sie den Verschlüsselungsschlüssel nicht in dieses Feld ein.**&#x200B;_ <br/><br/>Es liegt in der Verantwortung des Forschers zu überprüfen, ob der Schlüssel aus einer vertrauenswürdigen Quelle stammt. Forscher dürfen nicht davon ausgehen, dass der Schlüssel mit dem zur Erzeugung der digitalen Signatur verwendeten Schlüssel identisch ist. Beispiel: <br />OpenPGP-Schlüssel vom Webserver - `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Website | Eine URL, die auf eine Seite in Ihrem Geschäft verweist, auf der Sicherheitsforscher anerkannt werden, z. B`https://mystore.com/hall-of-fame.html`. Um zukünftige Angriffe zu verhindern, fügen Sie nur eine allgemeine Beschreibung hinzu, ohne spezifische Informationen zu Schwachstellenproblemen preiszugeben. Beispiel:<br />Wir möchten den folgenden Forschern danken:<br />(jjjj/mm/tt) Justin Thyme - SQL Injection |
| [!UICONTROL Preferred Languages] | Website | Gibt mindestens eine bevorzugte Sprache für Sicherheitsberichte an. Trennen Sie mehrere zweistellige [Sprach-Codes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) durch ein Komma. Alle angegebenen Sprachen haben dieselbe Priorität. Um beispielsweise Englisch, Spanisch und Französisch anzugeben, geben Sie `en, es, fr` ein. |
| [!UICONTROL Hiring] | Website | Die URL einer Seite auf der Website, die sicherheitsbezogene Auftragspositionen auflistet. Beispiel: `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Website | Die URL der Seite, die Ihre Sicherheitsrichtlinien und die Verfahren zur Meldung von Sicherheitslücken beschreibt. Beispiel: `https://mystore.com/security-reporting.html` Standard: `https://mystore.com/security` |
| [!UICONTROL Signature] | Website | Ein Link zu Ihrer digitalen Signaturdatei. Die digitale Signatur muss über die Befehlszeile generiert und im `.well-known` auf dem Server gespeichert werden. Weitere Informationen finden Sie unter [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) auf GitHub. Beispiel: `https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
