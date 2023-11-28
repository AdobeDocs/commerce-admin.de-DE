---
title: Sicherheit
description: Erfahren Sie mehr über die verfügbaren Tools zum Sichern Ihrer Stores und Daten sowie Richtlinien für einen Sicherheitsaktionsplan, wenn Sie einen Kompromiss erkennen.
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
source-git-commit: 671ec7015c37b24ca0acc615ae3715b8b870a453
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Sicherheit

Es gibt mehrere Möglichkeiten, Ihren Speicher zu sichern und Ihre Datensicherheit zu wahren:

- Einrichten [Zweifaktorauthentifizierung](security-two-factor-authentication.md)
- Implementierung [CAPTCHA](security-captcha.md) oder [reCAPTCHA](security-google-recaptcha.md)
- Richten Sie eine [Sicherheitsscan](security-scan.md) für jede Domäne in Ihrer Adobe Commerce- oder Magento Open Source-Installation.

Besuchen Sie die [Sicherheitszentrum](https://helpx.adobe.com/security.html){:target=&quot;_blank&quot;} und in der Sicherheitswarnungsregistrierung finden Sie aktuelle Informationen zu möglichen Sicherheitslücken. Informationen zu Best Practices für die Sicherheit finden Sie unter [Sichern Ihrer Commerce-Site und -Infrastruktur](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) im _Implementierungs-Playbook_.

>[!NOTE]
>
>Stores, die aktiviert wurden [!DNL Adobe Identity Management Services] (IMS)-Authentifizierung, bei der die native Adobe Commerce und Magento Open Source 2FA deaktiviert sind. Admin-Benutzer, die mit ihren Adobe-Anmeldedaten in ihrer Commerce-Instanz angemeldet sind, müssen sich nicht für viele Admin-Aufgaben erneut authentifizieren. Die Authentifizierung wird von Adobe IMS verarbeitet, wenn sich der Administrator in seiner aktuellen Sitzung anmeldet. Siehe [[!DNL Adobe Identity Management Service] (IMS) Integrationsübersicht](../getting-started/adobe-ims-integration-overview.md).

![Sicherheitszentrum](./assets/product-security-home.png){width="700" zoomable="yes"}

## Aktionsplan für Sicherheit

Wenn Sie vermuten, dass Ihre Adobe Commerce- oder Magento Open Source-Site gefährdet ist, folgen Sie diesem Aktionsplan unverzüglich.

1. **Diagnose**: Führen Sie eine Prüfung durch, um den Sicherheitsstatus Ihres Commerce-Stores festzustellen. Handel [Sicherheitsscan](security-scan.md) ist ein kostenloser Service von Adobe, mit dem Sie Ihre Commerce-Sites auf bekannte Sicherheitsrisiken und Malware überwachen und Sicherheitsbenachrichtigungen erhalten können.

1. **Clean**: Vermietung eines [qualifizierter Berater](https://solutionpartners.adobe.com/s/directory/?partner_type=1) oder Online-Dienst, um Ihre Website von allen schädlichen Code zu bereinigen. Einige Mitglieder der Commerce-Community empfehlen [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). Überprüfen Sie die `/media` Ordner für den ausführbaren Restcode. Entfernen Sie alle unbekannten Admin-Benutzer und setzen Sie alle Admin-Passwörter zurück.

1. **Protect**: Halten Sie Ihre Commerce-Installation mit der neuesten Version auf dem neuesten Stand. Wenn Sie eine ältere Version verwenden, wenden Sie alle Sicherheits-Patches an, sobald sie verfügbar werden. Überprüfen und verfolgen [Best Practices für die Commerce-Sicherheit](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). Abonnieren Sie [Warnungen zur Commerce-Sicherheit](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Bericht**: Wenn Sie der Meinung sind, dass Sie eine bestimmte Schwachstelle in Commerce gefunden haben, [Öffnen eines Problems mit Adobe](https://hackerone.com/adobe?type=team) und technische Details enthalten.

1. **Upgrade**: Planen Sie Ihr Upgrade auf [Adobe Commerce in unserer Cloud-Architektur](https://business.adobe.com/products/magento/cloud-delivery.html) jetzt.
