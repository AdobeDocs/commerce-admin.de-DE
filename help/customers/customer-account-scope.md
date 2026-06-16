---
title: Kundenkontobereich
description: Der Umfang von Kundenkonten kann auf die Website beschränkt sein, auf der das Konto erstellt wurde, oder für alle Websites und Stores in der Store-Hierarchie freigegeben werden.
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/ah5XmCeeX4Kc9czcllRq9zZX4W3rkkqkzcoUXtJjo5I
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 356
ht-degree: 0%

---

# Kundenkontobereich

Der Header jeder Seite in Ihrem Store erweitert eine Einladung für Käufer, sich _ein Konto bei Ihrem Store anzumelden_ zu registrieren. Kunden, die ein Konto eröffnen, profitieren von einer Reihe von Vorteilen, darunter:

* **Kundenkonto erstellen** - Besucher können ein Kundenkonto erstellen, damit sie die Storefront als registrierter Kunde verwenden können.
* **Erstellen eines Unternehmenskontos** Je nach Konfiguration kann ein Besucher Ihres Geschäfts ein Unternehmenskonto erstellen. Weitere Informationen finden Sie unter [Adobe Commerce B2B](../b2b/introduction.md).
* **Schnellerer Checkout** - Registrierte Kunden durchlaufen den Checkout schneller, da ein Großteil der Informationen bereits in ihren Konten vorhanden ist.
* **Self-Service** - Registrierte Kunden können ihre Informationen aktualisieren, den Status von Bestellungen überprüfen und sogar von ihren Konten neu bestellen.

Kunden können auf ihr Konto zugreifen, indem sie auf den **[!UICONTROL My Account]** Link in der Kopfzeile des Stores klicken. Über ihr -Konto können Kundinnen und Kunden Informationen anzeigen und ändern, einschließlich vergangener und aktueller Adressen, Abrechnungs- und Versandvoreinstellungen, Newsletter-Abonnements, Wunschlisten und mehr.

![Mein Konto](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## Festlegen des Umfangs von Kundenkonten

Der Umfang von Kundenkonten kann auf die Website beschränkt sein, auf der das Konto erstellt wurde, oder für alle Websites und Stores in der Store-Hierarchie freigegeben werden.

>[!NOTE]
>
>Wenn die Website aus der Kundengruppe ausgeschlossen ist, darf sich der Kunde nicht bei der Website anmelden, wenn der Umfang der Kundenkonten auf die Website beschränkt oder für alle Websites freigegeben ist. Weitere Informationen [ Ausschließen von Websites aus Gruppen finden ](customer-groups.md#create-a-customer-group) unter „Erstellen einer Kundengruppe“.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Customer Configuration]**.

1. Erweitern Sie den Abschnitt **[!UICONTROL Account Sharing Options]** .

   ![Optionen zur Kontofreigabe](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Share Customer Accounts]** auf eine der folgenden Einstellungen fest:

   | Option | Beschreibung |
   | --- | --- |
   | `Global` | Gibt Kundenkontoinformationen für jede Website frei und speichert sie in der Installation. |
   | `Per Website` | Beschränkt Kundenkontoinformationen auf die Website, auf der das Konto erstellt wurde. |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL User system value]** , um die Änderung vorzunehmen.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

   >[!NOTE]
   >
   >Wenn `Global` ausgewählt ist, werden die Kundeninformationen in **Mein Konto** (Adressen und Kontoinformationen wie Kontaktdaten) freigegeben.
