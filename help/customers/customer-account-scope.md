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

Die Kopfzeile jeder Seite in Ihrem Store erweitert eine Einladung für Käufer, sich bei Ihrem Geschäft für ein Konto bei _Anmelden oder registrieren_ anzumelden. Kunden, die ein Konto öffnen, profitieren von einer Reihe von Vorteilen, darunter:

* **Kundenkonto erstellen** - Besucher können ein Kundenkonto erstellen, damit sie die Storefront als registrierten Kunden verwenden können.
* **Erstellen eines Unternehmenskontos** Je nach Konfiguration kann ein Besucher in Ihrem Store wählen, ein Unternehmenskonto zu erstellen. Weitere Informationen finden Sie unter [Adobe Commerce B2B](../b2b/introduction.md).
* **Schnellerer Checkout** - Registrierte Kunden durchlaufen schneller den Checkout, da ein Großteil der Informationen bereits in ihren Konten enthalten ist.
* **Self-Service** - Registrierte Kunden können ihre Informationen aktualisieren, den Status von Bestellungen überprüfen und sogar ihre Konten neu anordnen.

Kunden können auf ihr Konto zugreifen, indem sie auf den Link **[!UICONTROL My Account]** in der Kopfzeile des Stores klicken. Über ihr Konto können Kunden Informationen anzeigen und ändern, einschließlich vergangener und aktueller Adressen, Abrechnungs- und Versandeinstellungen, Newsletter-Abonnements, Wunschlisten und mehr.

![Mein Konto](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## Festlegen des Umfangs von Kundenkonten

Der Umfang der Kundenkonten kann auf die Website beschränkt werden, auf der das Konto erstellt wurde, oder für alle Websites und Stores in der Store-Hierarchie freigegeben werden.

>[!NOTE]
>
>Wenn die Website aus der Kundengruppe ausgeschlossen ist, darf sich der Kunde nicht bei der Website anmelden, wenn der Umfang der Kundenkonten auf die Website beschränkt oder für alle Websites freigegeben ist. Weitere Informationen zum Ausschließen von Websites aus Gruppen finden Sie unter [Erstellen einer Kundengruppe](customer-groups.md#create-a-customer-group) .

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Customer Configuration]** aus.

1. Erweitern Sie den Abschnitt **[!UICONTROL Account Sharing Options]** .

   ![Optionen für die Kontofreigabe](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Share Customer Accounts]** auf einen der folgenden Werte:

   | Option | Beschreibung |
   | --- | --- |
   | `Global` | Teilt Kundenkontoinformationen mit jeder Website und speichert sie in der Installation. |
   | `Per Website` | Beschränkt Kundenkontoinformationen auf die Website, auf der das Konto erstellt wurde. |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL User system value]** , um die Änderung vorzunehmen.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

   >[!NOTE]
   >
   >Wenn `Global` ausgewählt ist, werden die Kundeninformationen in **Mein Konto** (Adressen und Kontoinformationen, z. B. Kontaktdaten) freigegeben.
