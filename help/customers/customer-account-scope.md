---
title: Umfang des Kundenkontos
description: Der Umfang der Kundenkonten kann auf die Website beschränkt werden, auf der das Konto erstellt wurde, oder für alle Websites und Stores in der Store-Hierarchie freigegeben werden.
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Umfang des Kundenkontos

Die Kopfzeile jeder Seite in Ihrem Store erweitert eine Einladung für Käufer auf _Anmelden oder registrieren_ für ein Konto bei Ihrem Geschäft. Kunden, die ein Konto öffnen, profitieren von einer Reihe von Vorteilen, darunter:

* **Kundenkonto erstellen** - Besucher können ein Kundenkonto erstellen, damit sie die Storefront als registrierten Kunden verwenden können.
* **Unternehmenskonto erstellen** Je nach Konfiguration kann ein Besucher Ihres Geschäfts ein Unternehmenskonto erstellen. Weitere Informationen finden Sie unter [Adobe Commerce B2B](../b2b/introduction.md).
* **Schnellerer Checkout** — Registrierte Kunden durchlaufen schneller den Checkout, da ein Großteil der Informationen bereits in ihren Konten enthalten ist.
* **Self-Service** — Registrierte Kunden können ihre Informationen aktualisieren, den Status von Bestellungen überprüfen und sogar von ihren Konten aus neu anordnen.

Kunden können auf ihr Konto zugreifen, indem sie auf **[!UICONTROL My Account]** -Link in der Kopfzeile des Stores. Über ihr Konto können Kunden Informationen anzeigen und ändern, einschließlich vergangener und aktueller Adressen, Abrechnungs- und Versandeinstellungen, Newsletter-Abonnements, Wunschlisten und mehr.

![Mein Konto](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## Festlegen des Umfangs von Kundenkonten

Der Umfang der Kundenkonten kann auf die Website beschränkt werden, auf der das Konto erstellt wurde, oder für alle Websites und Stores in der Store-Hierarchie freigegeben werden.

>[!NOTE]
>
>Wenn die Website aus der Kundengruppe ausgeschlossen ist, darf sich der Kunde nicht bei der Website anmelden, wenn der Umfang der Kundenkonten auf die Website beschränkt oder für alle Websites freigegeben ist. Siehe [Erstellen einer Kundengruppe](customer-groups.md#create-a-customer-group) für weitere Informationen zum Ausschließen von Websites aus Gruppen.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen **[!UICONTROL Customer Configuration]**.

1. Erweitern Sie die **[!UICONTROL Account Sharing Options]** Abschnitt.

   ![Optionen für Kontofreigabe](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Share Customer Accounts]** auf einen der folgenden Werte zu:

   | Option | Beschreibung |
   | --- | --- |
   | `Global` | Teilt Kundenkontoinformationen mit jeder Website und speichert sie in der Installation. |
   | `Per Website` | Beschränkt Kundenkontoinformationen auf die Website, auf der das Konto erstellt wurde. |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > Falls erforderlich, löschen Sie die **[!UICONTROL User system value]** aktivieren, um die Änderung vorzunehmen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

   >[!NOTE]
   >
   >Wann `Global` ausgewählt ist, werden die Kundeninformationen unter **Mein Konto** (Adressen und Kontoinformationen, wie z. B. Kontaktdaten) freigegeben werden.
