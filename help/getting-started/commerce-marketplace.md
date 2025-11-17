---
title: '[!DNL Adobe Commerce Marketplace]'
description: Erfahren Sie mehr über das  [!DNL Commerce Marketplace], das Händlern eine kuratierte Auswahl an Lösungen bietet und qualifizierten Entwicklern die Tools, die Plattform und den optimalen Standort bietet, um ein florierendes Unternehmen aufzubauen.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 17ec998812d21ab5815546e0f015965c2d35c853
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 0%

---

# Adobe Commerce Marketplace

Der [Adobe Commerce Marketplace][1] ist der Anwendungsspeicher, der Händlern eine kuratierte Auswahl an Lösungen bietet und qualifizierten Entwicklern die Tools, die Plattform und den optimalen Standort bietet, um ein florierendes Unternehmen aufzubauen. [!DNL Commerce Marketplace] bietet eine Auswahl an Erweiterungen, die kostenlos verfügbar sind, und andere, die zum Verkauf stehen. Einkäufe können per Kreditkarte oder [PayPal][2] bezahlt werden.

Alle Erweiterungen, die auf [!DNL Commerce Marketplace] verfügbar sind, wurden einer umfassenden Überprüfung unterzogen. Das [Extension Quality Program][3] (EQP) kombiniert [!DNL Commerce] Fachwissen, Entwicklungsrichtlinien und Verifizierungs-Tools, um sicherzustellen, dass alle Erweiterungen auf Commerce Marketplace Codierungsstandards und Best Practices erfüllen. Der Überprüfungsprozess umfasst sowohl eine automatisierte Überprüfung als auch eine manuelle Überprüfung der Qualitätssicherung. Während des Vorgangs werden Struktur und Code jeder Erweiterung auf Anzeichen einer Virus-/Malware-Infektion sowie auf Plagiate untersucht. Die Überprüfung umfasst eine umfassende technische Untersuchung und eine Integritätsprüfung, die von einem [!DNL Commerce] durchgeführt wurde und sich auf Dokumentation, Codierungsstruktur, Leistung, Skalierbarkeit, Sicherheit und Kompatibilität mit dem [!DNL Commerce]-Kern konzentriert.

Sie können zwar Erweiterungen aus anderen Quellen erwerben, aber nur die auf [!DNL Commerce Marketplace] verfügbaren Erweiterungen werden im Rahmen des Qualitätsprogramms für Erweiterungen durch eine umfassende technische und Marketing-Prüfung überprüft.

## App-Ressourcen

Traditionell haben Entwickler PHP verwendet, um prozessinterne Erweiterungen zu erstellen, um Features, Funktionen, Services und Integrationen zu Adobe Commerce hinzuzufügen. Durch das Erstellen von Apps mit prozessexterner Erweiterbarkeit (im Gegensatz zu Erweiterungen) können Sie Kompatibilitätsprobleme vermeiden.

Die folgenden Ressourcen bieten einen Ausgangspunkt für neue Benutzende, um sich mit -Programmen vertraut zu machen:

### Commerce-Ressourcen

- [Einrichten von I/O-Ereignissen für Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/)
- [Konfigurieren von Ereignissen für Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [Einrichten der Admin-Benutzeroberfläche SDK](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [Konvertieren einer Erweiterung in eine App](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### App Builder-Ressourcen

- [Übersicht über Commerce App Builder](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Einrichten von API Mesh für Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [Bereitstellen von App Builder-Apps](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [CI/CD für App Builder Apps](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Erste Schritte mit App Builder/Developer Console
   - [Erste Schritte mit App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [Projekte und Arbeitsbereiche](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace]

Bevor Sie eine von [!DNL Commerce Marketplace] erworbene Erweiterung installieren können, melden Sie sich bei Ihrem [!DNL Commerce] Konto an und stellen Sie sicher, dass Sie über einen aktiven Zugriffsschlüssel verfügen. Sie können sich über die Kopfzeile von [!DNL Commerce] oder [[!DNL Marketplace]][1]Magento.com&rbrace; bei Ihrem [-Konto ][6].

Ihr Zugriffsschlüssel ist ein Satz öffentlicher und privater Schlüssel, mit denen Sie Ihre [!DNL Commerce] mit Ihrem [!DNL Commerce] synchronisieren und Ihre Anmeldeinformationen überprüfen können. Nachdem Ihr Konto synchronisiert wurde, müssen Sie bei jeder Installation einer Erweiterung oder eines Moduls aus Commerce Marketplace bzw. bei jedem Upgrade Ihrer [!DNL Commerce] Ihren privaten Schlüssel eingeben.

Sie können mehrere Zugriffsschlüssel für verschiedene Zwecke erstellen und sie nach Bedarf aktivieren oder deaktivieren. Sie müssen jedoch denselben Zugriffsschlüssel verwenden, der für die Installation der [!DNL Commerce]-Software verwendet wurde. Sie können beispielsweise keinen Magento Open Source-Zugriffsschlüssel verwenden, um Adobe Commerce zu aktualisieren oder zu aktualisieren, oder umgekehrt. Sie können auch keinen Zugriffsschlüssel verwenden, der zu einem anderen Benutzer gehört oder aus einem [freigegebenen Konto](commerce-account-share.md).

### Zugriffsschlüssel erstellen

1. Melden Sie sich bei Ihrem [!DNL Commerce] Konto an.

1. Wählen Sie auf der Seite _[!UICONTROL My Account]_&#x200B;die Registerkarte **[!UICONTROL Marketplace]**&#x200B;aus.

1. Klicken Sie oben rechts neben Ihrem Namen auf den Abwärtspfeil und wählen Sie **[!UICONTROL My Profile]** aus.

   ![Ihr [!DNL Marketplace] Profil](./assets/marketplace-profile.png){width="600"}

1. Klicken Sie auf der Registerkarte _[!UICONTROL Marketplace]_&#x200B;unter&#x200B;_[!UICONTROL My Products]_ auf **[!UICONTROL Access Keys]**, und führen Sie dann einen der folgenden Schritte aus:

   - Überprüfen Sie, ob Sie bereits über einen Satz von Zugriffsschlüsseln für Ihre Marketplace-Käufe verfügen. Sie können mehrere Sets von Zugriffsschlüsseln für verschiedene Zwecke erstellen.

   ![Zugriffsschlüssel](./assets/access-keys.png){width="600"}

   - Klicken Sie auf **[!UICONTROL Create a New Access Key]**. Geben Sie einen Namen für das neue Schlüsselpaar ein und klicken Sie auf **[!UICONTROL OK]**. Gültige Zeichen sind Groß- und Kleinbuchstaben sowie Bindestriche anstelle von Leerzeichen.

1. Klicken Sie abschließend auf **[!UICONTROL OK]**.

   Ihr neuer Zugriffsschlüssel ist aktiviert und wird in der Liste angezeigt.

   Beachten Sie den _Kopieren_-Link nach jedem öffentlichen und privaten Schlüssel. Im nächsten Schritt kopieren Sie diese Werte und fügen sie ein, um Ihren Store mit Commerce Marketplace zu synchronisieren.

## Installationsprozess

>[!IMPORTANT]
>
>Ab Adobe Commerce und Magento Open Source 2.4.0 wird der Websetup-Assistent entfernt, und Sie müssen die Befehlszeile verwenden, um Ihre Instanz [installieren](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html?lang=de) oder [aktualisieren](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html?lang=de). Diese Anforderung umfasst auch [Module](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=de) und [Erweiterungen](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html?lang=de).

Der Installationsprozess für [!DNL Marketplace] Käufe unterscheidet sich bei On _Premise-Installationen_ Commerce von den auf [Adobe Cloud Architecture][4] gehosteten Installationen.

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## Support

Wenn Sie Hilfe bei der Installation oder bei der Verwendung einer Erweiterung benötigen, lesen Sie zunächst die Dokumentation, die der Erweiterung beiliegt. Wenn Sie keine Antwort auf Ihre Frage finden können, verwenden Sie die Kontaktinformationen in der Erweiterungsliste, um den Entwickler direkt zu kontaktieren. Wenn das, was Sie auf Marketplace kaufen, nicht Ihren Bedürfnissen entspricht, können [eine Rückerstattung anfordern](#refund-requests) innerhalb von 25 Tagen ab Kaufdatum. Adobe prüft alle Erstattungsanträge und stellt (falls genehmigt) die entsprechende Rückerstattung aus. Für Probleme im Zusammenhang mit Commerce Marketplace:

Methode 1: Senden Sie eine Support-Anfrage über das Formular [Adobe Commerce Marketplace - Contact Us](https://commercemarketplace.adobe.com/contact-us/) .

Methode 2: [E-Mail-](mailto:commercemarketplacesupport@adobe.com).

### Checkout-Probleme

Die Adressfelder in Ihrem Account-Profil müssen zu Verifizierungszwecken im Marketplace-Einkaufssystem ausgefüllt werden.

1. Fügen Sie die Adressfelder in Ihrem Marketplace-Kontoprofil hinzu.
1. Speichern Sie das aktualisierte Profil.
1. Fahren Sie mit dem Checkout fort.

### Anmeldeprobleme

Anmeldeprobleme hängen normalerweise mit einer Diskrepanz zwischen Ihrer MAGEID und Ihrer E-Mail-Adresse in der Kontodatenbank zusammen. Wenden Sie sich an den Marketplace-Support, um Hilfe zu erhalten.

>[!INFO]
>
>Käufe von Mobile Apps und Erweiterungen können nicht [&#x200B; ein neues &#x200B;](#purchase-transfers) übertragen werden.

### Open Source-Fragen

Das Marketplace-Supportteam löst Probleme, die mit den Sites [commerceMarketplace.adobe.com/](https://commercemarketplace.adobe.com/) und [commerceDeveloper.adobe.com/](https://commercedeveloper.adobe.com/) zusammenhängen. Bitte richten Sie Fragen zu Magento Open Source an das [Community-Forum](https://community.magento.com/) oder [kontaktieren Sie einen Partner](https://business.adobe.com/de/products/magento/partners.html) der Magento Open Source unterstützen kann.

### Erstattungsanträge

Um eine Rückerstattung für einen Marketplace-Kauf anzufordern, melden Sie sich bei Ihrem Konto an und führen Sie die folgenden Schritte aus:

1. Klicken Sie [!UICONTROL **Mein Profil**] > [!UICONTROL **Kaufverlauf**].
1. Suchen Sie den Kauf und klicken Sie auf [!UICONTROL **Rückerstattung anfordern**].
1. Füllen Sie das Rückerstattungsformular aus.

Der Marketplace-Support fordert Informationen an, nachdem die Rückerstattungsanfrage generiert wurde. Die Rückerstattungsoption ist für 25 Tage nach dem Kaufdatum verfügbar. Siehe &quot;[-Kundenvereinbarung](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html).

### Auftragsrechnungen

Sie können Auftragsrechnungen über den [!UICONTROL **Kaufverlauf) in**] Marketplace-Konto herunterladen. Die Rechnung enthält weder die MwSt. noch die Anschrift des Verkäufers, da es sich derzeit nicht um eine Marktplatz-Anforderung handelt.

Um eine Auftragsrechnung für einen Marketplace-Kauf herunterzuladen, melden Sie sich bei Ihrem Marketplace-Konto an und führen Sie die folgenden Schritte aus:

1. Klicken Sie [!UICONTROL **Mein Profil**] > [!UICONTROL **Kaufverlauf**].
1. Suchen Sie den Kauf.
1. Klicken Sie auf das Druckersymbol in der oberen rechten Ecke der Bestellung.

### Kaufübertragungen

Das Marketplace-Supportteam hat keine Möglichkeit, Käufe auf ein anderes Konto zu übertragen. Sie müssen alle Apps und Erweiterungen unter dem primären Commerce-Konto erwerben, um Installations- und Bereitstellungsprobleme zu vermeiden. Adobe Commerce ist zu einer eindeutigen Kennung berechtigt. Da Composer für die Installation verwendet wird, kann nur ein Satz von [Zugriffsschlüsseln](#create-an-access-key) verwendet werden, die mit dem primären Konto verknüpft sind. Die einzige verfügbare Lösung besteht darin[&#x200B; eine Rückerstattung &#x200B;](#refund-requests) dem Marketplace-Kaufkonto anzufordern (sofern gemäß der Rückerstattungsrichtlinie von Adobe Commerce zulässig).

Sie können [&#x200B; Commerce](commerce-account-share.md)Instanz über das Primärkonto freigeben. Der freigegebene Zugriff gewährt einem untergeordneten Konto von einem primären Konto aus spezielle Berechtigungen. Der freigegebene Zugriffspunkt wird vom primären Konto generiert. Das primäre Konto kann das berechtigte Commerce-Konto, das Haupt-Händlerkonto oder ein innerhalb eines Unternehmens freigegebenes Konto sein.

Diese Sonderberechtigungen gewähren dieselbe Zugriffsebene auf Adobe Commerce wie die primäre Instanz, sie werden jedoch nicht in den Adobe Commerce Marketplace oder das Entwicklerportal übertragen. Das bedeutet, dass der Kauf einer Erweiterung von einem untergeordneten Konto auf dem Marketplace nicht mit dem primären Konto geteilt werden kann. Shared Access ist eine Einbahnstraße (primäres Konto untergeordnet). Dies funktioniert nicht, wenn ein untergeordnetes Konto versucht, eine Freigabe für die primäre Instanz durchzuführen.

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[6]: https://business.adobe.com/de/products/magento/magento-commerce.html
