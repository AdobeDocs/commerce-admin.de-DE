---
title: Versionshinweise für [!DNL Page Builder]
description: Informationen zu allen Versionen finden  [!DNL Page Builder]  in den Versionshinweisen .
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2813'
ht-degree: 0%

---

# Versionshinweise für [!DNL Page Builder]

Diese Versionshinweise beschreiben Versionen von [!DNL Page Builder] und umfassen Folgendes:

![Neu](../assets/new.svg) Neue Funktionen

![Problem behoben](../assets/fix.svg) Fehlerbehebungen und Verbesserungen

![Bekanntes Problem](../assets/bug.svg) Bekannte Probleme

>[!IMPORTANT]
>
>Ab Version 2.4.3 ist [!DNL Page Builder] jetzt als gebündelte Erweiterung in Magento Open Source verfügbar. Es ist jetzt das standardmäßige Tool zur Inhaltsbearbeitung für Adobe Commerce und Magento Open Source und kann den WYSIWG-Editor durch beliebige Drittanbietermodule ersetzen.

## 1.7.2 für Commerce 2.4.5

![Neu](../assets/new.svg) **Neue Wrapper-Entität - [!DNL Columns] für Spalten-Layouts eingeführte Container** - Zuvor konnten Benutzer Spalten nur innerhalb eines anderen Container-/Wrapper-Inhaltstyps hinzufügen, z. B. einer [!DNL Tab] oder [!DNL Row]. Jetzt hat die [!DNL Column] einen eigenen Wrapper und kann direkt auf der Bühne hinzugefügt werden. Außerdem verfügt der [!DNL Columns]-Container über ein settings-Element, in dem Benutzerinnen und Benutzer die Konfiguration für diese Wrapper-Entität angeben können.<!--- PB-500-->

![Neu](../assets/new.svg) **Neue Menüoptionen zum Duplizieren, Ausblenden und Löschen von Spaltengruppen** - Mit diesen neuen Optionen können Benutzende [!DNL Columns] Gruppen duplizieren, ausblenden und löschen - genau wie dies mit Inhaltstypen möglich ist.<!--- PB-507-->

![Neu](../assets/new.svg) <!-- Issue 594 -->**Neue Unterstützung für mehrzeilige Spalten zur Spaltengruppe hinzugefügt** - Durch diese Hinzufügung können Benutzende mehrere Zeilen von Spalten innerhalb einer [!DNL Columns] bearbeiten, um Spaltenlayouts viel flexibler zu gestalten.<!--- PB-108-->

Informationen [&#x200B; Verwendung der neuen [!DNL Columns]-Gruppe finden &#x200B;](./column.md) unter „Layout - Spalte“.

## 1.7.1 für Commerce 2.4.4

![Problem behoben](../assets/fix.svg) Page Builder ist jetzt mit PHP 8.1 kompatibel.<!--- AC-1300-->

![Problem behoben](../assets/fix.svg) Händler können jetzt Alternativtext (`alt_text`) zu Bildern (Bild, Banner, Folie) hinzufügen, um die Barrierefreiheit der Inhalte zu verbessern.<!--- PB-1193-->

![Es wurde ein Problem &#x200B;](../assets/fix.svg): Admin-Benutzende mit Berechtigungen, die auf die Inhaltsbearbeitung beschränkt sind, sehen bei Verwendung von Page Builder zum Hinzufügen eines Produkt-Widgets zu einer CMS-Seite keinen Fehler mehr. Page Builder zeigt auch eine genaue Produktanzahl auf der Seite mit den Widget-Einstellungen an. Zuvor benötigte Page Builder beim Abrufen der Produktzahl Berechtigungen für das Katalogmodul. Daraufhin wurde folgender Fehler angezeigt: `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![Problem behoben](../assets/fix.svg) Anzeigeprobleme mit dem Menü Page Builder-Format werden jetzt mit dem TinyMCE 5-Bibliotheks-Upgrade behoben. <!--- AC-446-->

![Es wurde ein Problem &#x200B;](../assets/fix.svg). Sie können jetzt die Maus verwenden, um einen Wert **Anzuzeigender Text** im Popup Link einfügen zu bearbeiten. <!--- AC-982-->

![Problem behoben](../assets/fix.svg) Page Builder zeigt jetzt im Optionsmenü Schriftgröße alle Optionen wie erwartet an. Zuvor wurden nicht alle Optionen angezeigt. <!--- AC-1056-->

![Problem behoben](../assets/fix.svg) Die `phpgt/dom` Composer-Abhängigkeit für die `magento/magento2-page-builder`-Erweiterung wurde auf die neuesten Versionen aktualisiert. <!--- magento/magento2-page-builder/pull/779-->

![Problem behoben](../assets/fix.svg) Page Builder ändert die Größe der Dialogfelder „Link einfügen“ und „Bild einfügen“ nicht mehr, wenn der Schieberegler in einer kleinen Spalte angezeigt wird. <!--- AC-973-->

![Es wurde &#x200B;](../assets/fix.svg) Problem behoben: Das Menü Seitenbuilder-Tabelleneigenschaften wird jetzt erwartungsgemäß angezeigt. <!--- AC-407-->

![Problem behoben](../assets/fix.svg) Schieberpunkte werden nicht mehr im Modal Link einfügen oder Bild angezeigt, wenn die Maus nicht über den Schieberegler bewegt wird. <!--- AC-406-->

![Problem behoben](../assets/fix.svg) Die Schriftgröße, die zum Anzeigen der Menüoptionen „Tabelle“ verwendet wird, wurde optimiert. <!--- AC-396-->

![Es wurde &#x200B;](../assets/fix.svg) Problem behoben, dass Anomalien bei der Positionierung der Dialogfelder „Bild einfügen/bearbeiten“ und „Link einfügen/bearbeiten“ korrigiert wurden. <!--- AC-397-->

![Problem behoben](../assets/fix.svg) Page Builder gibt keinen Fehler mehr aus, wenn Sie für ein Banner auf **Text-**&quot; klicken. <!--- AC-398-->

![Problem behoben](../assets/fix.svg) Page Builder konvertiert beim Upgrade nicht mehr alle dynamischen Blöcke in eine Sprache. <!--- MC-42265-->

## 1.6.0 für Adobe Commerce 2.4.2

![Neu](../assets/new.svg) <!-- Issue 558 -->**Neues [!DNL Page Builder]-** - [!DNL Page Builder] hat die Formatierung von Inhalten massiv verbessert. Die Änderungen erleichtern jetzt die Erstellung einfacher CSS-Selektoren, um die vorhandenen Inhaltstypstile zu überschreiben. Diese Änderungen ermöglichen es, [!DNL Page Builder] Designs mit hoher Reaktionsgeschwindigkeit für alle Inhaltstypen zu erstellen.

![Neu](../assets/new.svg) <!-- Issue 429 -->**Zeilen-Container jetzt optional** - Sie können jetzt Inhalte in [!DNL Page Builder] erstellen, ohne dass ein Zeilen-Container erforderlich ist. Zusätzlich zur Zeile können die folgenden Inhaltstypen jetzt per Drag-and-Drop direkt auf die Bühne gezogen werden: HTML, Block, Dynamischer Block, Spalten und Registerkarten.

![Neu](../assets/new.svg) <!-- Issue 636 -->**Neuer responsiver Viewport-Umschalter** - Sie können jetzt eine Vorschau Ihres [!DNL Page Builder]-Inhalts in verschiedenen Gerätebreiten (Breakpoints) anzeigen, indem Sie die neuen Viewport-Umschalter-Schaltflächen für Admins über dem Staging verwenden. Der Viewport-Umschalter simuliert, wie Ihre Inhalte formatiert werden, wenn sie auf der Storefront mit verschiedenen Geräten angezeigt werden.

![Neu](../assets/new.svg) <!-- Issue 637 -->**Neue Breakpoint-spezifische Formularfelder** - Content-Typ-Feldwerte können jetzt auf bestimmte Viewport-Breakpoints festgelegt werden. Symbolindikatoren neben den Feldern zeigen den Viewport an, auf den der Feldwert für den Inhaltstyp angewendet wird.

![Neu](../assets/new.svg) <!-- Issue 559 -->**Vordefinierte Formularfeldeinträge wurden entfernt** - Erweiterte Formulareinstellungen für Ränder, Abstände und randbezogene Eigenschaften (Rahmen, Rahmenbreite und Rahmenradius) sind jetzt als `default` festgelegt, sodass Werte durch das CSS eines Moduls definiert werden können.

![Neu](../assets/new.svg) <!-- Issue 635, 557,  -->**Hinzugefügter Phasenabstand** - Zeilen und Spalten bieten jetzt zusätzliche Leerzeichen um enthaltene Inhaltstypen auf der Bühne, aber nicht in der Storefront. Der zusätzliche Phasenabstand erleichtert den Zugriff auf die Menüs der Mouseover-Optionen für den Container- und den enthaltenen Inhaltstyp.

![Problem behoben](../assets/fix.svg) <!-- MC-37348 -->**Automatisches Scrollen zu Überprüfungen wurde behoben** - Das automatische Scrollen zu Produktüberprüfungen in der Storefront wurde jetzt behoben.

![Behobenes Problem](../assets/fix.svg) <!-- MC-36227 -->**Korrigierter zugeschnittener Inhalt** - Lange Kategorie- und Produktbeschreibungen werden nicht mehr zugeschnitten.

![Behobenes Problem](../assets/fix.svg) <!-- MC-35402 -->**Behobene Inhalte mit voller Breite, voller Anschnitt** - Kategorieinhalte können jetzt in einem Layout mit voller Breite oder voller Anschnitt angezeigt werden.

![Behobenes Problem](../assets/fix.svg) <!-- MC-37989 -->**Sicherheitsverbesserungen**

## 1.5.1 für Adobe Commerce 2.4.1-p1

![Behobenes Problem](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**Fehleranzeige** - Es wurde ein Problem behoben, bei dem [!DNL Page Builder] beim Hinzufügen von Katalogunterkategorien in der Admin-Liste einen Fehler angezeigt haben.

## 1.5.0 für Adobe Commerce 2.4.1

![Neu](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**Immersive Bearbeitung im Vollbildmodus** - Die Bearbeitung [!DNL Page Builder] Inhalte ist jetzt nur noch für alle von [!DNL Page Builder] kontrollierten Bereiche im Vollbildmodus möglich. Diese Änderung betrifft CMS-Seiten, Produkt- und Kategorieseiten, Bausteine und dynamische Bausteine. Die Bearbeitung im Vollbildmodus legt den Fokus auf Ihren Inhalt und bietet eine Ansicht, die dem Benutzererlebnis auf der Storefront besser entspricht.

![Neu](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder] Inhaltsvorschauen &#x200B;**- [!DNL Page Builder] bietet jetzt standardmäßig Inhaltsvorschauen nicht nur für CMS-Seiten, -Blöcke und -dynamischen Blöcke, sondern auch für Produkt- und Kategorieseiten. Sie können diese Funktion für Produkt- und Kategorieseiten mit der neuen Einstellung Inhaltsvorschau [!DNL Page Builder] aktivieren oder deaktivieren, die in der Store-Konfiguration unter Content-Management > Erweiterte Content-Tools aufgerufen wird.

![Neu](../assets/new.svg) <!-- Issue 543 -->**Verbesserter Zugriff auf Produktkurzbeschreibungen** - Standardmäßig wird eine Produktkurzbeschreibung jetzt vor der längeren Beschreibung angezeigt. Diese Änderung führt zu einer Übereinstimmung mit der Reihenfolge, in der sie in der Storefront angezeigt werden, und verhindert, dass durch den längeren Beschreibungsinhalt gescrollt werden muss, um Zugriff auf die Kurzbeschreibung zu erhalten.

![Neu](../assets/new.svg) <!-- Issue 419 -->**Verschachtelte Links in Bannern und Folien wurden verhindert** - Durch das Hinzufügen von Links zum Inhalt und zu den äußeren Elementen von Bannern und Folien wurden verschachtelte Links erstellt, die in der Storefront nicht korrekt angezeigt wurden oder sich nicht korrekt verhielten. Um das Problem zu beheben, können Links für Banner *Folien nicht mehr sowohl* Bereich Nachrichtentext als auch zum Link-Attribut hinzugefügt werden.

![Problem behoben](../assets/fix.svg) <!-- Issue 421 --> Es wurde ein Problem behoben, bei dem das Festlegen eines leeren Rahmenradius für ein Registerkartenelement Fehler verursachte und den Inhalt des Registerkartenelements beschädigte.

![Problem behoben](../assets/fix.svg) <!-- Issue 422 --> Es wurde ein Problem behoben, bei dem das Hinzufügen bestimmter Bedingungskombinationen zum Filter Produktbedingung zu Fehlern führte, die das Speichern des Formulars Produkte verhinderten.

![Problem behoben](../assets/fix.svg) <!-- Issue 425 --> Es wurde ein Problem behoben, bei dem sich der Inhaltstyp des Schiebereglers nicht korrekt verhalten hat, wenn die Einstellung für Endlosschleife deaktiviert wurde.

![Problem behoben](../assets/fix.svg) <!-- Issue 426 -->Der Mindestpreis für Werbung wurde korrigiert, sodass er jetzt in [!DNL Page Builder] funktioniert.

![Problem behoben](../assets/fix.svg) <!-- Issue 436 -->Es wurde das Problem in Safari und IE 11 behoben, durch das das Ziehen und Ablegen eines Bildes in den Upload-Bereich in Bannern und Folien verhindert wurde.

![Problem behoben](../assets/fix.svg) <!-- Issue 525 --> Es wurde ein Problem behoben, bei dem der Inhaltstyp „Regler“ in Firefox nicht reagierte.

![Problem behoben](../assets/fix.svg) <!-- Issue 567 --> Es wurde ein Problem behoben, bei dem die Widget-Konfiguration falsche Selektoren im DOM für die verschiedenen Erscheinungsbilder erstellte.

![Problem behoben](../assets/fix.svg) <!-- Issue 609 --> Es wurde ein Problem behoben, bei dem in der Kopfzeilen-Symbolleiste das Optionsmenü des Inhaltstyps ausgeblendet wurde, wodurch der Zugriff auf das Formular und andere Optionen verhindert wurde.

![Problem behoben](../assets/fix.svg) <!-- Issue 612, 613 --> Es wurden Probleme behoben, bei denen Schieberegler und mehrere Zeilen mit Parallaxenhintergrund nach mehrmaligem Umschalten des Vollbildmodus nicht korrekt wiedergegeben wurden.

![Problem behoben](../assets/fix.svg) <!--MC-35220--> Es wurde ein Problem behoben, bei dem der Versuch, den Inhalt aus einem Inhaltstyp für die Überschrift in einen Textinhaltstyp zu kopieren, [!DNL Page Builder] Speichern verhinderte.

![Problem behoben](../assets/fix.svg) <!-- MC-34620 -->Content-Typ Text wurde korrigiert, um Nicht-Latin-1-Zeichen korrekt zu verarbeiten und zu speichern.

![Problem behoben](../assets/fix.svg) <!-- MC-34679 -->Es wurden [!DNL Page Builder] CSS-Stile behoben, die dazu führten, dass Safari 13.1 das Site-Menü des Luma-Designs für kleine Ansichts-Ports und mobile Bildschirme falsch renderte.

![Problem behoben](../assets/fix.svg) <!-- MC-34848 -->Der HTML-Inhaltstyp wurde behoben, um eingebettete Widgets wie „Nach SKU sortieren“ auf der Storefront korrekt anzuzeigen.

## 1.4.1 für Adobe Commerce 2.4.0-P1

![Neu](../assets/new.svg) <!-- PB-590 --> Aktualisierung auf TinyMCE 4. TinyMCE 3 entfernt, um die Sicherheit zu verbessern.

## 1.4.0 für Adobe Commerce 2.4.0

![Neu](../assets/new.svg) <!-- PB-494 -->Hinzugefügte Unterstützung für PHP 7.4.

![Problem behoben](../assets/fix.svg) <!-- MC-31247 --> Es wurde ein Problem behoben, bei dem der Inhaltstyp „Produkte“ keine konfigurierbaren Produkte anzeigte, wenn die Bedingung auf „Preis“ gesetzt war.

![Problem behoben](../assets/fix.svg) <!-- PB-179 --> Die Konfiguration der Produktausrichtung wurde behoben, sodass nur der Produkt-Container selbst positioniert wurde, nicht aber der Inhalt des Produkt-Containers, z. B. Produktname, Preis, Schaltflächen, Bilder und andere Elemente.

![Problem behoben](../assets/fix.svg) <!-- MC-33556 -->Leistungsverbesserungen.

![Problem behoben](../assets/fix.svg) Sicherheitsverbesserungen.

## 1.3.3-P1 für Adobe Commerce 2.3.6-P1

![Problem behoben](../assets/fix.svg) Sicherheitsverbesserungen.

## 1.3.3 für Adobe Commerce 2.3.6

![Problem behoben](../assets/fix.svg) <!-- MC-32766 --> Der Inhaltstyp Text wurde behoben, um die zu HTML-Attributen hinzugefügten Variablenanweisungen korrekt zu speichern.

![Problem behoben](../assets/fix.svg) <!-- MC-34590 -->Content-Typ Text wurde korrigiert, um Nicht-Latin-1-Zeichen korrekt zu verarbeiten und zu speichern.

![Problem behoben](../assets/fix.svg) <!-- MC-34677 -->Es wurden [!DNL Page Builder] CSS-Stile behoben, die dazu führten, dass Safari 13.1 das Site-Menü des Luma-Designs für kleine Ansichts-Ports und mobile Bildschirme falsch renderte.

![Problem behoben](../assets/fix.svg) <!-- MC-34846 -->Der HTML-Inhaltstyp wurde behoben, um eingebettete Widgets wie &quot;_nach SKU“_ der Storefront korrekt anzuzeigen.

![Problem behoben](../assets/fix.svg) Es wurde ein Fehler behoben, der Benutzer manchmal daran hinderte, Formulare vom Typ Inhalt zu speichern. Der Fehler (“[!DNL Page Builder] wurde 5 Sekunden lang gerendert, ohne Sperren freizugeben„) führte dazu, dass sich das Ladersymbol nach dem Versuch, ein Formular zu speichern, unbegrenzt drehte.

## 1.3.2 für Adobe Commerce 2.3.5-p2

![Neu](../assets/new.svg) Sicherheitsverbesserungen.

## 1.3.1 für Adobe Commerce 2.3.5-P1

Diese Version von [!DNL Page Builder] ist nur ein Versionsnummernupdate für Adobe Commerce 2.3.5-p1. Alle für Version 1.3.0 beschriebenen Funktionen gelten auch für diese Version.

## 1.3.0 für Adobe Commerce 2.3.5

![Neu](../assets/new.svg) **Vorlagen** - [!DNL Page Builder] verfügt jetzt über Vorlagen, die aus vorhandenen Inhalten erstellt und auf neue Inhaltsbereiche angewendet werden können. [!DNL Page Builder] Vorlagen speichern sowohl Inhalte als auch Layouts vorhandener Seiten, Blöcke, dynamischer Blöcke, Produktattribute und Kategoriebeschreibungen. Sie können beispielsweise eine bestehende [!DNL Page Builder] CMS-Seite als Vorlage speichern und diese Vorlage (mit allen Inhalten und Layouts) anwenden, um schnell CMS-Seiten für Ihre Site zu erstellen. Diese neue Funktion ist hier dokumentiert: [Vorlagen](templates.md).

![Neu](../assets/new.svg) **Videohintergründe für Zeilen, Banner und Schieberegler** - [!DNL Page Builder] Zeilen, Banner und Schieberegler können jetzt Videos für ihren Hintergrund verwenden. Diese neuen Funktionen sind hier dokumentiert: [Zeilen](row.md), [Banner](banner.md), [Sliders](slider.md).

![Neu](../assets/new.svg) **Video-Support-Ergänzungen und -**) - [!DNL Page Builder] unterstützt jetzt eine größere Auswahl an Videoformaten. Zusätzlich zu YouTube- und Vimeo-Videos unterstützen der Videoinhaltstyp und die Videohintergründe jetzt Video-URL-Links zu Videoformaten wie `.mp4` und anderen Browser-unterstützten Formaten. Der Content-Typ Video fügt auch eine Funktion zur automatischen Wiedergabe hinzu. Diese neuen Funktionen sind hier dokumentiert: [Video Content Type](video.md).

![Neu](../assets/new.svg) **Zeilen, Banner und Schieberegler mit voller Höhe** - [!DNL Page Builder] Zeilen, Banner und Schieberegler können jetzt ihre Höhen auf die volle Höhe der Seite festlegen, indem sie eine Zahl mit einer beliebigen CSS-Einheit (px, %, vh, em) oder eine Berechnung zwischen Einheiten (100vh - 237px) verwenden. Diese neuen Funktionen sind hier dokumentiert: [Zeilen](row.md), [Banner](banner.md), [Sliders](slider.md).

![Neu](../assets/new.svg) **Bibliothek mit Inhaltstyp-Upgrades** - Entwicklerinnen und Entwickler können jetzt Versionen [!DNL Page Builder] Inhaltstypen erstellen, ohne Probleme mit der Abwärtskompatibilität mit früheren Versionen einzuführen. Vor dieser Version würden signifikante Änderungen an den Inhaltstypkonfigurationen Probleme mit der Anzeige und dem Datenverlust bei zuvor gespeicherten [!DNL Page Builder] Inhaltstypen verursachen. Die neue Upgrade-Bibliothek beseitigt diese Probleme. Die -Bibliothek ist so konzipiert, dass frühere Versionen von in der Datenbank gespeicherten Inhaltstypen so aktualisiert werden, dass sie den Konfigurationsänderungen in den neuen Versionen entsprechen. [!DNL Page Builder] führt die Upgrade-Bibliothek für native Inhaltstypen aus, wie für eine neue Version erforderlich. Durch diese Änderung wird sichergestellt, dass die integrierten [!DNL Page Builder]-Inhaltstypen immer so aktualisiert werden, dass sie allen Änderungen entsprechen, die an Inhaltstypen für eine neuere Version vorgenommen wurden.

>[!IMPORTANT]
>
>Wenn Sie zusätzliche Datenbankentitäten zum Speichern [!DNL Page Builder] Inhalte erstellt haben, _müssen_ fügen Sie diese Entitäten zu Ihrer `etc/di.xml` hinzu. Andernfalls wird der in Ihrer Entität gespeicherte [!DNL Page Builder]-Inhalt nicht aktualisiert, was zu potenziellen Datenverlust- und Anzeigeproblemen führt. Wenn Sie beispielsweise eine Blog-Entität erstellt haben, die [!DNL Page Builder] speichert, müssen Sie Ihre Blog-Entität als `UpgradableEntitiesPool`-Typ zu Ihrer `etc/di.xml`-Datei hinzufügen, damit die Upgrade-Bibliothek die in Ihrem Blog verwendeten [!DNL Page Builder]-Inhaltstypen aktualisieren kann. Weitere Informationen und Anweisungen zur Verwendung der Upgrade-Bibliothek finden Sie unter [Aktualisieren von Inhaltstypen](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) im _Page Builder-Entwicklerhandbuch_.

![Neu](../assets/new.svg) **Dokumentation zum Hinzufügen neuer Erscheinungsbilder** - Entwicklerinformationen, die jetzt über [Hinzufügen von Erscheinungsbildern](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) für vorhandene oder benutzerdefinierte Inhaltstypen veröffentlicht wurden.

![Problem behoben](../assets/fix.svg) **Verschiedene Fehlerbehebungen**

- &#x200B;<!-- PB-50 -->Es wurde ein Problem behoben, bei dem das TinyMCE-Menü für Folieninhalte unter anderen Inhaltstypen angezeigt wurde, wenn der übergeordnete Container der Folie dupliziert wurde.
- &#x200B;<!-- PB-166 -->[!DNL Page Builder] wurde aktualisiert, um eine Methode zum Zerstören zu implementieren, um Speicherlecks in einigen Szenarien zu verhindern.
- &#x200B;<!-- PB-170 -->Die TinyMCE-Leistung wurde verbessert, wenn mehrere Instanzen in der Admin-Phase verwendet werden.
- &#x200B;<!-- PB-252 -->Es wurde ein Problem behoben, bei dem der Inhaltstyp Dynamischer Block in der Admin-Phase nicht gerendert wird, wenn die oberste Zeile als ausgeblendet markiert ist.
- &#x200B;<!-- PB-273 -->Verfeinerte Mauszeigerereignisse in der Admin-Phase durch Entfernen einer Verzögerung von 200 ms aus verschiedenen Benutzeroberflächen-Steuerelementen. Diese Änderung erleichtert die Arbeit mit verschachtelten Inhaltselementen auf der Bühne.
- &#x200B;<!-- PB-294 -->Es wurde ein Problem behoben, bei dem das Währungssymbol im Produktlisten-Widget innerhalb des Blocks/dynamischen Blocks auf der Admin-Phase falsch maskiert wurde.
- &#x200B;<!-- PB-296 -->Es wurde ein Problem behoben, bei dem die Produktsumme im [!DNL Page Builder] Bearbeitungsbereich für benutzerdefinierte MSI-Stock-Produkte nicht funktionierte.
- &#x200B;<!-- PB-317 -->Es wurde ein Problem behoben, bei dem beim Speichern [!DNL Page Builder] Inhalte mit Hintergrundbildern auf Microsoft Edge diese Bilder in der Storefront nicht gerendert werden.
- &#x200B;<!-- PB-390 -->Es wurde ein Problem behoben, bei dem verschachtelter [!DNL Page Builder]-Inhalt nicht gespeichert werden kann, wenn Benutzer auf die Schaltfläche Speichern klicken, bevor die Seite vollständig gerendert wird.
- &#x200B;<!-- PB-418 -->Es wurde ein Ausnahmefehler behoben, der aufgrund von [!DNL Page Builder] Analytics in Cron-Aufträgen ausgelöst wurde.

## 1.2.2 für Adobe Commerce 2.3.4-p2

![Neu](../assets/new.svg) Sicherheitsverbesserungen.

## 1.2.1 für Adobe Commerce 2.3.4-p1

![Neu](../assets/new.svg) Sicherheitsverbesserungen.

## 1.2.0 für Adobe Commerce 2.3.4

![Neu](../assets/new.svg) **[!DNL Page Builder]Integration mit PWA Studio** - [!DNL Page Builder] Content-Rendering zur Venia-App in PWA Studio hinzugefügt. [!DNL Page Builder] Inhalte können jetzt in der PWA Studio Venia-App angezeigt werden. In der [!DNL Page Builder] Dokumentation im [PWA Studio ] finden Sie alle Informationen zu dieser neuen Funktion.

![Neu](../assets/new.svg) **Hinzugefügtes Produktkarussell** - <!-- PB-77, PB-173, PB-175 -->Der Inhaltstyp Produkte bietet jetzt eine Option zum Anzeigen Ihrer Produkte in einem Karussell-/Schiebereglerformat, einschließlich mehrerer Optionen zum Anpassen des Karussells an Ihre Anforderungen.

![Neu](../assets/new.svg) Sortierung **Hinzugefügte Produkt-SKU** - <!-- PB-69 -->Der Content-Typ Produkte bietet jetzt eine Option, mit der Sie Ihre Produkte nach SKU in der Reihenfolge sortieren können, in der Sie sie in der Admin-Liste hinzufügen.

![Neu](../assets/new.svg) **Sortierung der Produktkategorie hinzugefügt** - <!-- PB-181 -->. Der Content-Typ Produkte bietet jetzt eine Option zum Sortieren Ihrer Produkte nach Kategorie _Position_ und zeigt sie in der gleichen Reihenfolge an, in der sie in Ihrem Commerce-Katalog angezeigt werden.

![Neu](../assets/new.svg) **Hinzugefügte Produktauswahlsummen** - <!-- PB-107 -->. Der Admin-Editor für den Inhaltstyp „Produkte“ zeigt jetzt die Gesamtzahl der Produkte an, die Ihren Produktauswahloptionen entsprechen.

![Problem behoben](../assets/fix.svg) **Verschiedene Fehlerbehebungen**

- &#x200B;<!-- PB-237 -->Sicherheitsverbesserungen.
- &#x200B;<!-- PB-41 -->Es wurden Suchvorgänge in UI-Auswahlkomponenten korrigiert, damit pro Suchbegriff nur eine AJAX-Anfrage ausgeführt wird.
- &#x200B;<!-- PB-76, PB-84-->Die Produktvorschauen wurden im Admin-Bereich aktualisiert, damit sie mit der Storefront übereinstimmen, einschließlich der Optionen für Sternebewertung, Farbe und Größe des Produkts, falls relevant.
- &#x200B;<!-- PB-169 -->Es wurde ein Problem behoben, bei dem [!DNL Page Builder] nicht gespeichert werden konnten, wenn die JavaScript-Minimierung und -Bündelung in Commerce aktiviert waren.
- &#x200B;<!-- PB-241 -->Es wurde ein Problem mit der Admin-Vorschau von Produkten, Blöcken und dynamischen Blöcken behoben, die auf Commerce-Installationen korrekt gerendert werden sollen, welche unterschiedliche URLs für den Admin und das Frontend definieren.
- &#x200B;<!-- PB-238 -->Es wurde ein Problem mit der Admin-Vorschau von Produkten, Blöcken und dynamischen Blöcken behoben, die bei Commerce-Installationen mit B2B-Installation und aktivierter Option _Nur Anmeldung_ korrekt gerendert werden sollen. Vor dieser Fehlerbehebung führte die [!DNL Page Builder] Vorschau dazu, dass die Seite zur Anmeldung beim Kundenkonto umgeleitet wurde.
- &#x200B;<!-- PB-239 -->Es wurde ein Sitzungsfehler behoben, der bei der Vorschau einer großen Seite in [!DNL Page Builder] Admin auftreten konnte.
- &#x200B;<!-- PB-248 -->[!DNL Page Builder] LESS-Stile wurden aktualisiert, um eine Duplizierung des Storefront-Stils zu verhindern.

## 1.1.1 für Adobe Commerce 2.3.3-P1

![Neu](../assets/new.svg) Sicherheitsverbesserungen.

## 1.1.0 für Adobe Commerce 2.3.3

![Neu](../assets/new.svg) <!-- MC-15250 -->Es wurde eine explizite Produktsortierung zum Inhaltstyp „Produkte“ hinzugefügt.

![Neu](../assets/new.svg) <!-- MC-17823 -->Es wurden Schaltflächen zum Einfügen von Bildern, Widgets und Variablen in den HTML-Inhaltstyp hinzugefügt.

![Problem behoben](../assets/fix.svg) Verbesserte [!DNL Page Builder].

![Problem behoben](../assets/fix.svg) <!-- MC-1805 -->Aktualisierte [!DNL Page Builder] zur Unterstützung von PHP Version 7.3.

![Problem behoben](../assets/fix.svg) <!-- MC-4137 -->TinyMCE wurde auf Version 4.9.5 aktualisiert. Dieses Update sowie die zusätzlichen Verbesserungen behoben mehrere TinyMCE Inline Editor Probleme:

- Variablen, Bilder und Bild-Links werden dort hinzugefügt, wo sich der Cursor befindet.
- Tabellen und Tabellenzellen können zentriert ausgerichtet werden.
- Kopieren/Einfügen fügt nun Inhalte an der Cursorposition ein.
- Links können auf ausgewählten Text angewendet werden.
- Aufzählungszeichen sind ordnungsgemäß ausgerichtet.
- Änderungen innerhalb des Inline-Editors können gespeichert werden, ohne zuvor außerhalb des Editors zu klicken.

![Problem behoben](../assets/fix.svg) <!-- MC-3880 --> Es wurde ein Problem behoben, bei dem die minimale Höhe und die vertikale Ausrichtung zwischen Abschnitten im Bearbeitungsbereich für jeden Inhaltstyp inkonsistent waren.

![Problem behoben](../assets/fix.svg) <!-- MC-14994 --> Es wurde ein Problem behoben, bei dem die Symbolleiste aus dem Inhaltstyp „Überschrift“ falsch positioniert wurde, wenn sie zum ersten Mal auf der Bühne abgelegt wurde.

![Problem behoben](../assets/fix.svg) <!-- MC-15742 -->Es wurden hartcodierte Ränder in den Inhaltstypen „Schieberegler“ und „Video“ behoben.

![Problem behoben](../assets/fix.svg) <!-- MC-16241 --> Es wurde ein Problem behoben, bei dem das erforderliche Sternsymbol zweimal in Formularfeldern angezeigt wurde.

## 1.0.3 für Adobe Commerce 2.3.2-p2

![Neu](../assets/new.svg) Sicherheitsverbesserungen.

## 1.0.2 für Adobe Commerce 2.3.2-p1

![Neu](../assets/new.svg) Sicherheitsverbesserungen.

## 1.0.1 für Adobe Commerce 2.3.2

![Neu](../assets/new.svg) Stellt die Kompatibilität mit Adobe Commerce 2.3.2 sicher.

## 1.0.0 für Adobe Commerce 2.3.1

![Neu](../assets/new.svg) Allgemeine Verfügbarkeitsversion


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
