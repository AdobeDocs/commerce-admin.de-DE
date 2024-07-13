---
title: '[!DNL Adobe Commerce Marketplace]'
description: Erfahren Sie mehr über die [!DNL Commerce Marketplace], die Händlern eine kuratierte Auswahl von Lösungen anbietet und qualifizierten Entwicklern die Tools, die Plattform und den besten Standort für den Aufbau eines florierenden Unternehmens bietet.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 20e1439810891b0d19cda62cc2646701ec5a778c
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace][1] ist der Anwendungsspeicher, der Händlern eine kuratierte Auswahl von Lösungen anbietet und qualifizierten Entwicklern die Tools, die Plattform und den besten Standort zum Aufbau eines florierenden Unternehmens bietet. [!DNL Commerce Marketplace] bietet eine Auswahl von Erweiterungen, die kostenlos verfügbar sind, und anderen, die zum Verkauf angeboten werden. Käufe können mit Kreditkarte oder [PayPal][2] bezahlt werden.

Alle Erweiterungen, die für [!DNL Commerce Marketplace] verfügbar sind, haben eine umfassende Überprüfung bestanden. Das [Erweiterungs-Qualitätsprogramm][3] (EQP) kombiniert [!DNL Commerce]-Kenntnisse, Entwicklungsrichtlinien und Verifizierungswerkzeuge, um sicherzustellen, dass alle Erweiterungen auf dem Commerce Marketplace Kodierungsstandards und Best Practices erfüllen. Der Überprüfungsprozess umfasst sowohl eine automatisierte Prüfung als auch eine manuelle Qualitätssicherung. Während des Prozesses wird die Struktur und der Code jeder Erweiterung geprüft und auf Beweise für eine Virus-/Malware-Infektion sowie auf Hinweise auf Plagiate getestet. Die Überprüfung umfasst eine tief greifende technische Untersuchung und eine Prüfung der Zuverlässigkeit, die von einem [!DNL Commerce] -Ingenieur durchgeführt wurde, wobei der Schwerpunkt auf Dokumentation, Kodierungsstruktur, Leistung, Skalierbarkeit, Sicherheit und Kompatibilität mit dem [!DNL Commerce] -Kern liegt.

Obwohl Sie Erweiterungen aus anderen Quellen kaufen können, werden nur die Erweiterungen, die in [!DNL Commerce Marketplace] verfügbar sind, durch umfassende technische und Marketing-Überprüfungen im Extension Quality Program überprüft.

## App-Ressourcen

Entwickler haben PHP traditionell verwendet, um in Prozessen enthaltene Erweiterungen zu erstellen, um Funktionen, Dienste und Integrationen zu Adobe Commerce hinzuzufügen. Durch das Erstellen von Apps mit Out-of-Process-Erweiterbarkeit im Gegensatz zu Erweiterungen können Sie Kompatibilitätsprobleme vermeiden.

Die folgenden Ressourcen bieten einen Ausgangspunkt für neue Anwender, um sich mit Apps vertraut zu machen:

### Commerce-Ressourcen

- [Einrichten von I/O-Ereignissen für Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/)
- [Konfigurieren von Ereignissen für Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [Einrichten des Admin UI SDK](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [Konvertieren einer Erweiterung in eine App](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### App Builder-Ressourcen

- [Überblick über Commerce App Builder](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Einrichten eines API-Gitters für Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [ Bereitstellen von App Builder-Apps](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [CI/CD für App Builder-Apps](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Erste Schritte mit App Builder/Developer Console
   - [Erste Schritte mit App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [Grundlegendes zu Projekten und Arbeitsbereichen](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] Anmeldedaten

Bevor Sie eine von [!DNL Commerce Marketplace] erworbene Erweiterung installieren können, melden Sie sich bei Ihrem [!DNL Commerce] -Konto an und stellen Sie sicher, dass Sie über einen aktiven Zugriffsschlüssel verfügen. Sie können sich über die Kopfzeile von [[!DNL Marketplace]][1] oder [Magento.com][6] bei Ihrem [!DNL Commerce]-Konto anmelden.

Ihr Zugriffsschlüssel ist ein Satz öffentlicher und privater Schlüssel, mit denen Sie Ihre [!DNL Commerce]-Installation mit Ihrem [!DNL Commerce]-Konto synchronisieren und Ihre Anmeldedaten überprüfen können. Nachdem Ihr Konto synchronisiert wurde, müssen Sie Ihren privaten Schlüssel jedes Mal eingeben, wenn Sie eine Erweiterung oder ein Modul von Commerce Marketplace installieren oder Ihre [!DNL Commerce] -Installation aktualisieren.

Sie können mehrere Zugriffsschlüssel für verschiedene Zwecke erstellen und sie nach Bedarf aktivieren oder deaktivieren. Sie müssen jedoch denselben Zugriffsschlüssel verwenden, der für die Installation der [!DNL Commerce] -Software verwendet wurde. Beispielsweise können Sie keinen Magento Open Source-Zugriffsschlüssel verwenden, um Adobe Commerce zu aktualisieren oder zu aktualisieren oder umgekehrt. Sie können auch keinen Zugriffsschlüssel verwenden, der zu einem anderen Benutzer gehört oder von einem [freigegebenen Konto](commerce-account-share.md) stammt.

### Zugriffsschlüssel erstellen

1. Melden Sie sich bei Ihrem [!DNL Commerce] -Konto an.

1. Wählen Sie auf der Seite _[!UICONTROL My Account]_die Registerkarte **[!UICONTROL Marketplace]**aus.

1. Klicken Sie in der rechten oberen Ecke neben Ihrem Namen auf den Pfeil nach unten und wählen Sie **[!UICONTROL My Profile]**.

   ![Ihr [!DNL Marketplace] Profil](./assets/marketplace-profile.png){width="600"}

1. Klicken Sie auf der Registerkarte _[!UICONTROL Marketplace]_unter_[!UICONTROL My Products]_ auf **[!UICONTROL Access Keys]** und führen Sie dann einen der folgenden Schritte aus:

   - Überprüfen Sie, ob Sie bereits über eine Reihe von Zugriffsschlüsseln für Ihre Marketplace-Käufe verfügen. Sie können mehrere Sätze von Zugriffsschlüsseln für verschiedene Zwecke erstellen.

   ![Zugriffsschlüssel](./assets/access-keys.png){width="600"}

   - Klicken Sie auf **[!UICONTROL Create a New Access Key]**. Geben Sie einen Namen für das neue Schlüsselpaar ein und klicken Sie auf **[!UICONTROL OK]**. Gültige Zeichen sind Groß- und Kleinbuchstaben und Bindestriche anstelle von Leerzeichen.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL OK]**.

   Ihr neuer Zugriffsschlüssel ist aktiviert und wird in der Liste angezeigt.

   Beachten Sie den Link _Kopieren_ nach jedem öffentlichen und privaten Schlüssel. Im nächsten Schritt kopieren Sie diese Werte und fügen Sie sie ein, um Ihren Speicher mit Commerce Marketplace zu synchronisieren.

## Installationsprozess

>[!IMPORTANT]
>
>Ab Adobe Commerce und Magento Open Source 2.4.0 wird der Web-Einrichtungsassistent entfernt. Sie müssen die Befehlszeile für [install](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) oder [upgrade](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) Ihrer Instanz verwenden. Diese Anforderung umfasst auch [module](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) und [extensions](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

Der Installationsprozess für [!DNL Marketplace]-Käufe unterscheidet sich bei _On-Premise_-Installationen von Commerce von den Installationen, die auf [der Adobe Cloud Architecture][4] gehostet werden.

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## Support

Wenn Sie Hilfe bei der Installation oder Verwendung einer Erweiterung benötigen, lesen Sie zuerst in der Dokumentation, die der Erweiterung beigefügt ist. Wenn Sie die Antwort auf Ihre Frage nicht finden können, verwenden Sie die Kontaktinformationen in der Erweiterungsliste, um den Entwickler direkt zu kontaktieren. Wenn das, was Sie in Marketplace kaufen, Ihre Anforderungen nicht erfüllt, können Sie [innerhalb von 25 Tagen nach dem Kaufdatum eine Rückerstattung anfordern](#refund-requests). Adobe prüft alle Erstattungsanträge und gibt (falls genehmigt) die entsprechende Erstattung aus. Wenden Sie sich bei Problemen im Zusammenhang mit dem Commerce Marketplace an [Support](mailto:commercemarketplacesupport@adobe.com).

### Checkout-Probleme

Die Adressfelder in Ihrem Kontoprofil müssen zur Verifizierung im Marketplace-Einkaufssystem ausgefüllt werden.

1. Fügen Sie die Adressfelder in Ihr Marketplace-Kontoprofil ein.
1. Speichern Sie das aktualisierte Profil.
1. Fahren Sie mit Ihrem Checkout fort.

### Anmeldungsprobleme

Anmeldungsprobleme beziehen sich normalerweise auf eine Abweichung zwischen Ihrer MAGEID- und E-Mail-Adresse in der Kontodatenbank. Wenden Sie sich für Unterstützung an den Support von Marketplace.

>[!INFO]
>
>App- und Erweiterungskäufe können nicht [auf ein neues Konto übertragen](#purchase-transfers) werden.

### Open-Source-Fragen

Das Support-Team von Marketplace behebt nur Probleme im Zusammenhang mit den Sites [commerceMarketplace.adobe.com/](https://commercemarketplace.adobe.com/) und [commerceDeveloper.adobe.com/](https://commercedeveloper.adobe.com/). Bitte richten Sie Fragen zur Magento Open Source an das [Community-Forum](https://community.magento.com/) oder [wenden Sie sich an einen Partner](https://business.adobe.com/products/magento/partners.html), der bei der Magento Open Source behilflich sein kann.

### Erstattungsanträge

Um eine Rückerstattung für einen Einkauf in Marketplace anzufordern, melden Sie sich bei Ihrem Konto an und führen Sie die folgenden Schritte aus:

1. Klicken Sie auf [!UICONTROL **Mein Profil**] > [!UICONTROL **Kaufverlauf**].
1. Suchen Sie den Kauf und klicken Sie auf [!UICONTROL **Erstattungen anfordern**].
1. Füllen Sie das Formular für die Erstattungsbestellung aus.

Der Support von Marketplace fordert Informationen an, nachdem die Rückerstattungsanforderung generiert wurde. Die Rückerstattungsoption ist 25 Tage nach dem Kaufdatum verfügbar. Weitere Informationen finden Sie in der [Marketplace-Kundenvereinbarung](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html).

### Bestellrechnungen

Sie können die Bestellrechnungen aus dem [!UICONTROL **Kaufverlauf**] in Ihrem Marketplace-Konto herunterladen. Die Rechnung liefert weder die MwSt noch die Adresse des Verkäufers, da sie derzeit keine Marketplace-Anforderung ist.

Um eine Bestellrechnung für einen Kauf in Marketplace herunterzuladen, melden Sie sich bei Ihrem Marketplace-Konto an und führen Sie die folgenden Schritte aus:

1. Klicken Sie auf [!UICONTROL **Mein Profil**] > [!UICONTROL **Kaufverlauf**].
1. Suchen Sie den Kauf.
1. Klicken Sie auf das Druckersymbol in der oberen rechten Ecke der Bestellung.

### Kaufüberweisungen

Das Support-Team von Marketplace kann Käufe nicht auf ein anderes Konto übertragen. Sie müssen alle Apps und Erweiterungen unter dem primären Commerce-Konto erwerben, um Installations- und Bereitstellungsprobleme zu vermeiden. Adobe Commerce hat eine Berechtigung für eine eindeutige Kennung. Da Composer für die Installation verwendet wird, kann nur ein Satz von [Zugriffsschlüsseln](#create-an-access-key) verwendet werden, die mit dem primären Konto verknüpft sind. Die einzige verfügbare Lösung besteht darin, [eine Rückerstattung ](#refund-requests) vom Marktplatz-Kaufkonto anzufordern (sofern dies durch die Adobe Commerce-Rückerstattungsrichtlinie erlaubt ist).

Sie können eine Commerce-Instanz [über das primäre Konto freigeben](commerce-account-share.md). Der gemeinsame Zugriff gewährt einem untergeordneten Konto aus einem primären Konto spezielle Berechtigungen. Der freigegebene Zugriffspunkt wird aus dem primären Konto generiert. Das Hauptkonto kann das Konto mit Berechtigung für Commerce, das Hauptkaufmännische oder ein innerhalb eines Unternehmens freigegebenes Konto sein.

Diese speziellen Berechtigungen gewähren auf Adobe Commerce denselben Zugriff wie auf die primäre Instanz. Sie werden jedoch nicht auf den Adobe Commerce Marketplace oder das Entwicklerportal übertragen. Das bedeutet, dass der Kauf einer Erweiterung über ein untergeordnetes Konto im Marketplace nicht für das primäre Konto freigegeben werden kann. Der freigegebene Zugriff ist eine Einbahnstraße (Hauptkonto, das untergeordnet werden soll). Es funktioniert nicht, wenn ein untergeordnetes Konto versucht, es an die primäre Instanz zu teilen.

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[6]: https://business.adobe.com/products/magento/magento-commerce.html
