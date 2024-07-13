---
title: Sicherheit
description: Erfahren Sie mehr über die verfügbaren Tools zum Sichern Ihrer Stores und Daten sowie Richtlinien für einen Sicherheitsaktionsplan, wenn Sie einen Kompromiss erkennen.
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
source-git-commit: fede05a413428520eec89d46f41a1cdd9c9c3a2e
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Sicherheit

Es gibt mehrere Möglichkeiten, Ihren Speicher zu sichern und Ihre Datensicherheit zu wahren:

- Einrichten der [Zwei-Faktor-Authentifizierung](security-two-factor-authentication.md)
- Implementieren von [CAPTCHA](security-captcha.md) oder [reCAPTCHA](security-google-recaptcha.md)
- Richten Sie für jede Domäne in Ihrer Adobe Commerce- oder Magento Open Source-Installation eine [Sicherheitsprüfung](security-scan.md) ein.

>[!NOTE]
>
>Bei Stores, für die die Authentifizierung mit [!DNL Adobe Identity Management Services] (IMS) aktiviert wurde, sind native Adobe Commerce und Magento Open Source 2FA deaktiviert. Admin-Benutzer, die mit ihren Adobe-Anmeldeinformationen bei ihrer Commerce-Instanz angemeldet sind, müssen sich nicht für viele Administratoraufgaben erneut authentifizieren. Die Authentifizierung wird von Adobe IMS verarbeitet, wenn sich der Administrator in seiner aktuellen Sitzung anmeldet. Siehe [[!DNL Adobe Identity Management Service]  (IMS)-Integrationsübersicht](../getting-started/adobe-ims-integration-overview.md).

Besuchen Sie das [Sicherheitszentrum](https://helpx.adobe.com/security.html){:target=&quot;_blank&quot;}, um aktuelle Informationen über potenzielle Sicherheitslücken zu erhalten, sich für Adobe-Sicherheitsbenachrichtigungen zu registrieren und auf das Adobe Trust Center zuzugreifen.

![Sicherheitscenter](./assets/product-security-home.png){width="700" zoomable="yes"}

Informationen zu Best Practices für die Sicherheit finden Sie unter [Sichern der Commerce-Site und -Infrastruktur](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) im _Playbook für die Implementierung_.

## Aktionsplan für Sicherheit

Wenn Sie vermuten, dass Ihre Adobe Commerce- oder Magento Open Source-Site gefährdet ist, folgen Sie diesem Aktionsplan unverzüglich.

1. **Diagnose**: Führen Sie eine Prüfung durch, um den Sicherheitsstatus Ihres Commerce-Stores festzustellen. Commerce [Security Scan](security-scan.md) ist ein kostenloser Service von Adobe, mit dem Sie Ihre Commerce-Websites auf bekannte Sicherheitsrisiken und Malware überwachen und Sicherheitsbenachrichtigungen erhalten können.

1. **Bereinigen**: Leihen Sie einen [qualifizierten Berater](https://solutionpartners.adobe.com/s/directory/?partner_type=1) oder einen Online-Dienst an, um Ihre Site von allen schädlichen Codes zu bereinigen. Einige Commerce-Community-Mitglieder empfehlen [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). Überprüfen Sie den Ordner &quot;`/media`&quot; auf den ausführbaren Code für den Rest. Entfernen Sie alle unbekannten Admin-Benutzer und setzen Sie alle Admin-Passwörter zurück.

1. **Protect**: Halten Sie Ihre Commerce-Installation mit der neuesten Version auf dem neuesten Stand. Wenn Sie eine ältere Version verwenden, wenden Sie alle Sicherheits-Patches an, sobald sie verfügbar werden. Überprüfen und befolgen Sie die [Commerce-Best Practices für die Sicherheit](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). Abonnieren Sie [Commerce-Sicherheitswarnungen](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Bericht**: Wenn Sie der Ansicht sind, dass Sie eine bestimmte Schwachstelle in Commerce gefunden haben, öffnen Sie [ein Problem mit Adobe](https://hackerone.com/adobe?type=team) und fügen Sie technische Details hinzu.

1. **Upgrade**: Für den zusätzlichen, vom Support rund um die Uhr erreichbaren Support, planen Sie jetzt Ihr Upgrade auf [Adobe Commerce in unserer Cloud-Architektur](https://business.adobe.com/products/magento/cloud-delivery.html).
