---
title: Sicherheit
description: Erfahren Sie mehr über die verfügbaren Tools zur Sicherung Ihrer Stores und Daten und Richtlinien für einen Sicherheitsaktionsplan, wenn Sie einen Kompromiss erkennen.
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
TQID: https://experienceleague.adobe.com/9aJ-ZVqwaIr2IJTY6e2hp3eoZe2v6sxz6WdqP2FiPTc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 0%

---

# Sicherheit

Es gibt mehrere Möglichkeiten, Ihren Speicher zu schützen und Ihre Datensicherheit zu gewährleisten:

- Einrichten [Zwei-Faktor-Authentifizierung](security-two-factor-authentication.md)
- Implementieren von [CAPTCHA](security-captcha.md) oder [reCAPTCHA](security-google-recaptcha.md)
- Richten Sie für jede Domain [&#x200B; Ihrer Adobe Commerce- oder Magento Open Source](security-scan.md)Installation eine Sicherheitsüberprüfung ein.

>[!NOTE]
>
>Bei Stores mit aktivierter [!DNL Adobe Identity Management Services]-Authentifizierung (IMS) sind die native Adobe Commerce und Magento Open Source 2FA deaktiviert. Admin-Benutzende, die mit ihren Adobe-Anmeldeinformationen bei ihrer Commerce-Instanz angemeldet sind, müssen sich für viele Admin-Aufgaben nicht erneut authentifizieren. Die Authentifizierung wird von Adobe IMS durchgeführt, wenn sich der Administrator bei seiner aktuellen Sitzung anmeldet. Siehe Übersicht über die [[!DNL Adobe Identity Management Service] (IMS)-Integration](../getting-started/adobe-ims-integration-overview.md).

Besuchen Sie das [Sicherheitscenter](https://helpx.adobe.com/de/security.html){:target="_blank"}, um die neuesten Informationen über potenzielle Sicherheitslücken zu erhalten, sich für Adobe-Sicherheitsbenachrichtigungen zu registrieren und auf das Adobe Trust Center zuzugreifen.

![Sicherheitszentrum](./assets/product-security-home.png){width="700" zoomable="yes"}

Informationen zu Best Practices für die Sicherheit finden Sie unter [Sichern der Commerce-Site und &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=de)) im _Implementierungs-Playbook_.

## Sicherheits-Aktionsplan

Wenn Sie vermuten, dass Ihre Adobe Commerce- oder Magento Open Source-Site gefährdet ist, befolgen Sie diesen Aktionsplan unverzüglich.

1. **Diagnose**: Führen Sie eine Suche durch, um den Sicherheitsstatus Ihres Commerce-Stores zu ermitteln. Commerce [Security Scan](security-scan.md) ist ein kostenloser Service von Adobe, mit dem Sie Ihre Commerce-Sites auf bekannte Sicherheitsrisiken und Malware überwachen und Sicherheitsbenachrichtigungen erhalten können.

1. **Säubern**: Bestellen Sie einen [qualifizierten Berater](https://solutionpartners.adobe.com/s/directory/?partner_type=1) oder Online-Service, um Ihre Website von allen bösartigen Code zu säubern. Einige Mitglieder der Commerce-Community empfehlen [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). Überprüfen Sie den `/media` Ordner auf übrig gebliebenen ausführbaren Code. Entfernen Sie alle unbekannten Admin-Benutzer und setzen Sie alle Admin-Kennwörter zurück.

1. **Protect**: Halten Sie Ihre Commerce-Installation mit der neuesten Version auf dem neuesten Stand. Wenn Sie eine ältere Version verwenden, wenden Sie alle Sicherheits-Patches an, sobald sie verfügbar werden. Überprüfen und befolgen Sie die [Best Practices für die Sicherheit von Commerce](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). [Commerce-Sicherheitswarnungen abonnieren](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Bericht**: Wenn Sie glauben, dass Sie eine bestimmte Sicherheitslücke in Commerce gefunden haben, [eröffnen Sie ein Problem mit Adobe](https://hackerone.com/adobe?type=team) und fügen Sie technische Details hinzu.

1. **Upgrade**: Planen Sie jetzt Ihr Upgrade auf [Adobe Commerce in unserer Cloud-Architektur, um die zusätzliche Sicherheit zu &#x200B;](https://business.adobe.com/de/products/magento/cloud-delivery.html), die durch den 24/7-Support entsteht.
