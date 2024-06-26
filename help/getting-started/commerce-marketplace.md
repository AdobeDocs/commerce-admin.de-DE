---
title: '[!DNL Adobe Commerce Marketplace]'
description: Informationen zum [!DNL Commerce Marketplace], das Händlern eine kuratierte Auswahl an Lösungen anbietet und qualifizierten Entwicklern die Tools, Plattform und den besten Standort für den Aufbau eines florierenden Unternehmens bietet.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 02e7c71fc47e6850371bfbdc1be50f65ec8015e9
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace][1] ist der Appstore, der Händlern eine kuratierte Auswahl von Lösungen anbietet und qualifizierten Entwicklern die Tools, Plattform und den besten Standort zur Verfügung stellt, um ein florierendes Geschäft aufzubauen. [!DNL Commerce Marketplace] bietet eine Auswahl an kostenlosen Erweiterungen und anderen zum Verkauf stehenden Erweiterungen. Käufe können per Kreditkarte bezahlt werden oder [PayPal][2].

Alle verfügbaren Erweiterungen für [!DNL Commerce Marketplace] haben eine ausführliche Überprüfung bestanden. Die [Extension Quality Program][3] (EQP)-Kombinationen [!DNL Commerce] Fachwissen, Entwicklungsrichtlinien und Verifizierungswerkzeuge, um sicherzustellen, dass alle Erweiterungen auf dem Commerce Marketplace Kodierungsstandards und Best Practices erfüllen. Der Überprüfungsprozess umfasst sowohl eine automatisierte Prüfung als auch eine manuelle Qualitätssicherung. Während des Prozesses wird die Struktur und der Code jeder Erweiterung geprüft und auf Beweise für eine Virus-/Malware-Infektion sowie auf Hinweise auf Plagiate getestet. Die Überprüfung umfasst eine eingehende technische Untersuchung und eine Prüfung der Zuverlässigkeit, die von einem [!DNL Commerce] -Techniker mit Schwerpunkt auf Dokumentation, Kodierungsstruktur, Leistung, Skalierbarkeit, Sicherheit und Kompatibilität mit der [!DNL Commerce] Core.

Sie können zwar Erweiterungen aus anderen Quellen erwerben, jedoch nur die Erweiterungen, die in [!DNL Commerce Marketplace] werden durch umfangreiche technische und Marketing-Überprüfungen im Rahmen des Programms für Erweiterungsqualität überprüft.

## App-Ressourcen

Entwickler haben PHP traditionell verwendet, um in Prozessen enthaltene Erweiterungen zu erstellen, um Funktionen, Dienste und Integrationen zu Adobe Commerce hinzuzufügen. Durch das Erstellen von Apps mit Out-of-Process-Erweiterbarkeit im Gegensatz zu Erweiterungen können Sie Kompatibilitätsprobleme vermeiden.

Die folgenden Ressourcen bieten einen Ausgangspunkt für neue Anwender, um sich mit Apps vertraut zu machen:

### Commerce-Ressourcen

- [Einrichten von I/O-Ereignissen für Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/)
- [Konfigurieren von Ereignissen für Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [Einrichten des Admin UI SDK](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [Konvertieren einer Erweiterung in eine App](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### App Builder-Ressourcen

- [Übersicht über Commerce App Builder](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Einrichten des API-Netzwerks für Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [App Builder-Apps bereitstellen](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [CI/CD für App Builder-Apps](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Erste Schritte mit App Builder/Developer Console
   - [Erste Schritte mit App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [Projekte und Arbeitsbereiche](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] Anmeldeinformationen

Vor der Installation einer von [!DNL Commerce Marketplace]anmelden, [!DNL Commerce] und überprüfen Sie, ob Sie über einen aktiven Zugriffsschlüssel verfügen. Sie können sich bei Ihrer [!DNL Commerce] -Konto aus der Kopfzeile von [[!DNL Marketplace]][1] oder [Magento.com][6].

Ihr Zugriffsschlüssel ist ein Satz öffentlicher und privater Schlüssel, die zur Synchronisierung Ihrer [!DNL Commerce] Installation mit [!DNL Commerce] und überprüfen Sie Ihre Anmeldedaten. Nachdem Ihr Konto synchronisiert wurde, müssen Sie Ihren privaten Schlüssel jedes Mal eingeben, wenn Sie eine Erweiterung oder ein Modul von Commerce Marketplace installieren oder Ihre [!DNL Commerce] Installation.

Sie können mehrere Zugriffsschlüssel für verschiedene Zwecke erstellen und sie nach Bedarf aktivieren oder deaktivieren. Sie müssen jedoch denselben Zugriffsschlüssel verwenden, der für die Installation der [!DNL Commerce] Software. Beispielsweise können Sie keinen Magento Open Source-Zugriffsschlüssel verwenden, um Adobe Commerce zu aktualisieren oder zu aktualisieren oder umgekehrt. Sie können auch keinen Zugriffsschlüssel verwenden, der zu einem anderen Benutzer gehört oder von einem [freigegebenes Konto](commerce-account-share.md).

### Zugriffsschlüssel erstellen

1. Anmelden bei [!DNL Commerce] -Konto.

1. Im _[!UICONTROL My Account]_Seite, wählen Sie die **[!UICONTROL Marketplace]**Registerkarte.

1. Klicken Sie oben rechts neben Ihrem Namen auf den Pfeil nach unten und wählen Sie **[!UICONTROL My Profile]**.

   ![Ihre [!DNL Marketplace] profile](./assets/marketplace-profile.png){width="600"}

1. Im _[!UICONTROL Marketplace]_Registerkarte unter_[!UICONTROL My Products]_ klicken **[!UICONTROL Access Keys]** und führen Sie dann einen der folgenden Schritte aus:

   - Überprüfen Sie, ob Sie bereits über eine Reihe von Zugriffsschlüsseln für Ihre Marketplace-Käufe verfügen. Sie können mehrere Sätze von Zugriffsschlüsseln für verschiedene Zwecke erstellen.

   ![Zugriffsschlüssel](./assets/access-keys.png){width="600"}

   - Klicks **[!UICONTROL Create a New Access Key]**. Geben Sie einen Namen für das neue Schlüsselpaar ein und klicken Sie auf **[!UICONTROL OK]**. Gültige Zeichen sind Groß- und Kleinbuchstaben und Bindestriche anstelle von Leerzeichen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL OK]**.

   Ihr neuer Zugriffsschlüssel ist aktiviert und wird in der Liste angezeigt.

   Beachten Sie die _Kopieren_ nach jedem öffentlichen und privaten Schlüssel verknüpfen. Im nächsten Schritt kopieren Sie diese Werte und fügen Sie sie ein, um Ihren Speicher mit Commerce Marketplace zu synchronisieren.

## Installationsprozess

>[!IMPORTANT]
>
>Ab Adobe Commerce und Magento Open Source 2.4.0 ist der Web-Einrichtungs-Assistent entfernt. Sie müssen die Befehlszeile zum [install](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) oder [Upgrade](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) Ihre Instanz. Diese Anforderung umfasst auch [Module](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) und [Erweiterungen](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

Der Installationsprozess für [!DNL Marketplace] -Käufe unterscheiden sich von _On-Premise_ Installationen von Commerce als für Installationen, die auf gehostet werden [Adobe Cloud-Architektur][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## Support

Wenn Sie Hilfe bei der Installation oder Verwendung einer Erweiterung benötigen, lesen Sie zuerst in der Dokumentation, die der Erweiterung beigefügt ist. Wenn Sie die Antwort auf Ihre Frage nicht finden können, verwenden Sie die Kontaktinformationen in der Erweiterungsliste, um den Entwickler direkt zu kontaktieren. Wenn das, was Sie in Marketplace kaufen, Ihren Anforderungen nicht entspricht, können Sie [eine Erstattung verlangen](#refund-requests) innerhalb von 25 Tagen ab Kaufdatum. Adobe prüft alle Erstattungsanträge und gibt (falls genehmigt) die entsprechende Erstattung aus. Support-Probleme im Zusammenhang mit Commerce Marketplace finden Sie im Abschnitt [[!DNL Marketplace] Hilfe-Center][5].

### Checkout-Probleme

Die Adressfelder in Ihrem Kontoprofil müssen zur Verifizierung im Marketplace-Einkaufssystem ausgefüllt werden.

1. Fügen Sie die Adressfelder in Ihr Marketplace-Kontoprofil ein.
1. Speichern Sie das aktualisierte Profil.
1. Fahren Sie mit Ihrem Checkout fort.

### Anmeldungsprobleme

Anmeldungsprobleme beziehen sich normalerweise auf eine Abweichung zwischen Ihrer MAGEID- und E-Mail-Adresse in der Kontodatenbank. Wenden Sie sich für Unterstützung an den Support von Marketplace.

>[!INFO]
>
>App- und Erweiterungskäufe können nicht getätigt werden [übertragen](#purchase-transfers) in ein neues Konto ein.

### Open-Source-Fragen

Das Support-Team von Marketplace löst Probleme im Zusammenhang mit dem [commerce.marketplace.adobe.com/](https://commercemarketplace.adobe.com/) und [commerce.developer.adobe.com/](https://commercedeveloper.adobe.com/) nur Sites. Bitte richten Sie Fragen zur Magento Open Source an die [Community-Forum](https://community.magento.com/) oder [Partner kontaktieren](https://business.adobe.com/products/magento/partners.html) wer bei der Magento Open Source helfen kann.

### Erstattungsanträge

Um eine Rückerstattung für einen Einkauf in Marketplace anzufordern, melden Sie sich bei Ihrem Konto an und führen Sie die folgenden Schritte aus:

1. Klicks [!UICONTROL **Mein Profil**] > [!UICONTROL **Kaufverlauf**].
1. Suchen Sie den Kauf und klicken Sie auf [!UICONTROL **Erstattungsantrag**].
1. Füllen Sie das Formular für die Erstattungsbestellung aus.

Der Support von Marketplace fordert Informationen an, nachdem die Rückerstattungsanforderung generiert wurde. Die Rückerstattungsoption ist 25 Tage nach dem Kaufdatum verfügbar. Siehe [Marketplace-Kundenvereinbarung](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html).

### Bestellrechnungen

Sie können Bestellrechnungen von der [!UICONTROL **Kaufverlauf**] in Ihrem Marketplace-Konto. Die Rechnung liefert weder die MwSt noch die Adresse des Verkäufers, da sie derzeit keine Marketplace-Anforderung ist.

Um eine Bestellrechnung für einen Kauf in Marketplace herunterzuladen, melden Sie sich bei Ihrem Marketplace-Konto an und führen Sie die folgenden Schritte aus:

1. Klicks [!UICONTROL **Mein Profil**] > [!UICONTROL **Kaufverlauf**].
1. Suchen Sie den Kauf.
1. Klicken Sie auf das Druckersymbol in der oberen rechten Ecke der Bestellung.

### Kaufüberweisungen

Das Support-Team von Marketplace kann Käufe nicht auf ein anderes Konto übertragen. Sie müssen alle Apps und Erweiterungen unter dem primären Commerce-Konto erwerben, um Installations- und Bereitstellungsprobleme zu vermeiden. Adobe Commerce hat eine Berechtigung für eine eindeutige Kennung. Da Composer für die Installation verwendet wird, ist nur ein Satz von [Zugriffsschlüssel](#create-an-access-key) mit dem primären Konto verknüpft ist, kann verwendet werden. Die einzige verfügbare Lösung besteht darin, [eine Erstattung verlangen](#refund-requests) über das Kaufkonto von Marketplace (sofern durch die Adobe Commerce-Erstattungsrichtlinie gestattet).

Sie können [share](commerce-account-share.md) eine Commerce-Instanz über das primäre Konto. Der gemeinsame Zugriff gewährt einem untergeordneten Konto aus einem primären Konto spezielle Berechtigungen. Der freigegebene Zugriffspunkt wird aus dem primären Konto generiert. Das Hauptkonto kann das Konto mit Berechtigung für Commerce, das Hauptkaufmännische oder ein innerhalb eines Unternehmens freigegebenes Konto sein.

Diese speziellen Berechtigungen gewähren auf Adobe Commerce denselben Zugriff wie auf die primäre Instanz. Sie werden jedoch nicht auf den Adobe Commerce Marketplace oder das Entwicklerportal übertragen. Das bedeutet, dass der Kauf einer Erweiterung über ein untergeordnetes Konto im Marketplace nicht für das primäre Konto freigegeben werden kann. Der freigegebene Zugriff ist eine Einbahnstraße (Hauptkonto, das untergeordnet werden soll). Es funktioniert nicht, wenn ein untergeordnetes Konto versucht, es an die primäre Instanz zu teilen.

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[5]: https://marketplacesupport.magento.com/hc/en-us
[6]: https://business.adobe.com/products/magento/magento-commerce.html
