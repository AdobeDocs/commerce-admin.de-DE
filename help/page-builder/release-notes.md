---
title: Versionshinweise für [!DNL Page Builder]
description: In den Versionshinweisen finden Sie Informationen zu allen [!DNL Page Builder] veröffentlicht.
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2747'
ht-degree: 0%

---

# Versionshinweise für [!DNL Page Builder]

Diese Versionshinweise beschreiben Versionen von [!DNL Page Builder] und umfassen:

![Neu](../assets/new.svg) Neue Funktionen

![Problem behoben](../assets/fix.svg) Fehlerbehebungen und Verbesserungen

![Bekanntes Problem](../assets/bug.svg) Bekannte Probleme

>[!IMPORTANT]
>
>Ab Version 2.4.3 [!DNL Page Builder] ist jetzt als gebündelte Erweiterung in Magento Open Source verfügbar. Es ist jetzt das Standard-Tool zur Inhaltsbearbeitung für Adobe Commerce und Magento Open Source und kann den WYSIWG-Editor durch ein beliebiges Drittanbietermodul ersetzen.

## 1.7.2 für Commerce 2.4.5

![Neu](../assets/new.svg) **Neue Wrapper-Entität - [!DNL Columns] Für Spaltenlayouts eingeführter Container** - Zuvor konnten Benutzer Spalten nur in einem anderen Container-/Wrapper-Inhaltstyp hinzufügen, z. B. [!DNL Tab] oder [!DNL Row]. Nun, die [!DNL Column] hat einen eigenen Wrapper und kann direkt auf der Bühne hinzugefügt werden. Außerdem wird die [!DNL Columns] -Container verfügt über ein settings-Element, in dem Benutzer die Konfiguration für diese Wrapper-Entität angeben können.<!--- PB-500-->

![Neu](../assets/new.svg) **Neue Menüoptionen zum Duplizieren, Ausblenden und Löschen von Spalten-Gruppen** - Mit diesen neuen Optionen können Benutzer duplizieren, ausblenden und löschen. [!DNL Columns] -Gruppen - genau wie sie es mit Inhaltstypen können.<!--- PB-507-->

![Neu](../assets/new.svg) <!-- Issue 594 -->**Neue mehrzeilige Spaltenunterstützung zur Spaltengruppe hinzugefügt** - Mit diesem Zusatz können Benutzer mehrere Zeilen von Spalten in einer Zeile bearbeiten [!DNL Columns] -Gruppe, um die Spaltenlayouts viel flexibler zu gestalten.<!--- PB-108-->

Siehe [Layout - Spalte](./column.md) für Informationen zur Verwendung der neuen [!DNL Columns] hinzugefügt.

## 1.7.1 für Commerce 2.4.4

![Problem behoben](../assets/fix.svg) Page Builder ist jetzt mit PHP 8.1 kompatibel.<!--- AC-1300-->

![Problem behoben](../assets/fix.svg) Händler können jetzt alternativen Text hinzufügen (`alt_text`) in Bilder (Bild, Banner, Folie), um die Barrierefreiheit von Inhalten zu verbessern.<!--- PB-1193-->

![Problem behoben](../assets/fix.svg) Admin-Benutzer mit Berechtigungen, die auf die Inhaltsbearbeitung beschränkt sind, sehen nur dann einen Fehler mehr, wenn sie mit dem Seitenaufbau ein Produkt-Widget zu einer CMS-Seite hinzufügen. Der Seitenaufbau zeigt außerdem eine genaue Produktanzahl auf der Seite mit den Widget-Einstellungen an. Zuvor benötigte Page Builder beim Abrufen der Produktanzahl Berechtigungen für das Catalog-Modul und zeigte diesen Fehler an: `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![Problem behoben](../assets/fix.svg) Anzeigeprobleme mit dem Menü &quot;Seitenaufbau-Format&quot;wurden jetzt mit dem Upgrade der TinyMCE 5-Bibliothek behoben. <!--- AC-446-->

![Problem behoben](../assets/fix.svg) Sie können jetzt die Maus verwenden, um eine **Anzuzeigender Text** im Popup-Fenster Link einfügen. <!--- AC-982-->

![Problem behoben](../assets/fix.svg) Der Seitenaufbau zeigt jetzt alle Optionen wie erwartet im Menü mit den Schriftgrößenoptionen an. Zuvor wurden nicht alle Optionen angezeigt. <!--- AC-1056-->

![Problem behoben](../assets/fix.svg) Die `phpgt/dom` Komponentenabhängigkeit für die `magento/magento2-page-builder` Erweiterung auf die neuesten Versionen. <!--- magento/magento2-page-builder/pull/779-->

![Problem behoben](../assets/fix.svg) Die Größe der Dialogfelder &quot;Link einfügen&quot;und &quot;Bild einfügen&quot;wird im Seitenaufbau nicht mehr geändert, wenn der Regler in einer kleinen Spalte angezeigt wird. <!--- AC-973-->

![Problem behoben](../assets/fix.svg) Das Menü &quot;Tabelleneigenschaften&quot;im Seitenaufbau wird jetzt erwartungsgemäß angezeigt. <!--- AC-407-->

![Problem behoben](../assets/fix.svg) Reglerpunkte werden nicht mehr auf dem Link &quot;Einfügen&quot;oder Bild-Modal angezeigt, wenn der Mauszeiger nicht über den Regler bewegt wird. <!--- AC-406-->

![Problem behoben](../assets/fix.svg) Die Schriftgröße zur Anzeige der Menüoptionen im Menü Tabelle wurde optimiert. <!--- AC-396-->

![Problem behoben](../assets/fix.svg) Fehlerkorrektur - die Positionierung der Dialogfelder &quot;Bild einfügen/bearbeiten&quot;und &quot;Link einfügen/bearbeiten&quot;wurde korrigiert. <!--- AC-397-->

![Problem behoben](../assets/fix.svg) Der Seitenaufbau gibt keinen Fehler mehr aus, wenn Sie auf **Texteditor** für ein Banner. <!--- AC-398-->

![Problem behoben](../assets/fix.svg) Der Seitenaufbau konvertiert während der Aktualisierung nicht mehr alle dynamischen Blöcke in eine Sprache. <!--- MC-42265-->

## 1.6.0 für Adobe Commerce 2.4.2

![Neu](../assets/new.svg) <!-- Issue 558 -->**Neu [!DNL Page Builder] Stile** - [!DNL Page Builder] hat die Formatierung von Inhalten massiv verbessert. Die Änderungen erleichtern es nun, einfache CSS-Selektoren zu erstellen, um die vorhandenen Inhaltstypstile zu überschreiben. Diese Änderungen ermöglichen die Erstellung von [!DNL Page Builder] Themen mit umfassender Reaktionsfähigkeit für alle Inhaltstypen.

![Neu](../assets/new.svg) <!-- Issue 429 -->**Zeilencontainer jetzt optional** - Sie können jetzt Inhalte in erstellen. [!DNL Page Builder] , ohne dass ein Zeilencontainer erforderlich ist. Neben der Zeile können nun die folgenden Inhaltstypen direkt auf die Bühne gezogen und dort abgelegt werden: HTML, Block, dynamischer Block, Spalten und Registerkarten.

![Neu](../assets/new.svg) <!-- Issue 636 -->**Neuer responsiver Viewport-Umschalter** - Sie können jetzt eine Vorschau Ihrer [!DNL Page Builder] Inhalt in verschiedenen Gerätebreiten (Haltepunkten) mithilfe der neuen Schaltflächen für den Admin Viewport-Umschalter oberhalb der Bühne. Der Viewport-Umschalter simuliert, wie Ihr Inhalt formatiert wird, wenn er auf verschiedenen Geräten auf der Storefront angezeigt wird.

![Neu](../assets/new.svg) <!-- Issue 637 -->**Neue Breakpoint-spezifische Formularfelder** - Feldwerte vom Typ Inhalt können jetzt auf bestimmte Viewport-Haltepunkte festgelegt werden. Symbolindikatoren neben den Feldern zeigen den Viewport an, auf den der Feldwert für den Inhaltstyp angewendet wird.

![Neu](../assets/new.svg) <!-- Issue 559 -->**Vordefinierte Formularfeldeinträge entfernt** - Erweiterte Formulareinstellungen für Ränder, Paddings und mit Rahmen verbundene Eigenschaften (Rahmen, Rahmenbreite und Rahmenradius) werden jetzt als `default`, sodass Werte durch das CSS eines Moduls definiert werden können.

![Neu](../assets/new.svg) <!-- Issue 635, 557,  -->**Staging-Abstand hinzugefügt** - Zeilen und Spalten bieten jetzt zusätzliche Abstandsberechtigungen für enthaltene Inhaltstypen auf der Bühne, aber nicht auf der Storefront. Der zusätzliche Staging-Abstand erleichtert den Zugriff auf die Mouseover-Optionsmenüs für Container und enthaltene Inhaltstypen.

![Problem behoben](../assets/fix.svg) <!-- MC-37348 -->**Automatischer Bildlauf bei Überprüfungen korrigiert** - Der automatische Bildlauf zu Produktbewertungen auf der Storefront ist jetzt behoben.

![Problem behoben](../assets/fix.svg) <!-- MC-36227 -->**Korrigierter Inhalt** - Lange Kategorie- und Produktbeschreibungen werden nicht mehr zugeschnitten.

![Problem behoben](../assets/fix.svg) <!-- MC-35402 -->**Inhalt der Kategorie mit fester Breite und voller Anschnitt** - Der Inhalt von Kategorien kann jetzt in einem Layout mit voller Breite oder mit voller Anschnitt angezeigt werden.

![Problem behoben](../assets/fix.svg) <!-- MC-37989 -->**Sicherheitsverbesserungen**

## 1.5.1 für Adobe Commerce 2.4.1-p1

![Problem behoben](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**Fehleranzeige** - Es wurde ein Problem behoben, bei dem [!DNL Page Builder] beim Hinzufügen von Katalogunterkategorien in der Admin-Konsole einen Fehler angezeigt.

## 1.5.0 für Adobe Commerce 2.4.1

![Neu](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**Ideal für umfassende Vollbildbearbeitung** - Bearbeiten [!DNL Page Builder] Der Inhalt ist jetzt nur für alle Bereiche im Vollbildmodus verfügbar, die von [!DNL Page Builder]. Diese Änderung umfasst CMS-Seiten, Produkt- und Kategorieseiten, Blöcke und dynamische Blöcke. Die Bearbeitung im Vollbildmodus konzentriert sich auf Ihren Inhalt und bietet eine Ansicht, die dem Benutzererlebnis auf der Storefront besser entspricht.

![Neu](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder] Inhaltsvorschau **- Standardmäßig [!DNL Page Builder] bietet jetzt eine Inhaltsvorschau nicht nur für CMS-Seiten, -Blöcke und dynamische Blöcke, sondern auch für Produkt- und Kategorieseiten. Sie können diese Funktion für Produkt- und Kategorieseiten mithilfe der neuen [!DNL Page Builder] Einstellung für die Inhaltsvorschau, auf die in der Store-Konfiguration unter Content Management > Erweiterte Inhaltswerkzeuge zugegriffen wird.

![Neu](../assets/new.svg) <!-- Issue 543 -->**Verbesserter Zugriff auf kurze Produktbeschreibungen** - Standardmäßig wird jetzt vor der längeren Beschreibung eine kurze Beschreibung des Produkts angezeigt. Diese Änderung entspricht der Reihenfolge, in der sie auf der Storefront angezeigt werden, und verhindert, dass der längere Beschreibungsinhalt durchblättert werden muss, um Zugriff auf die kurze Beschreibung zu erhalten.

![Neu](../assets/new.svg) <!-- Issue 419 -->**Verhindern verschachtelter Links in Bannern und Folien** - Durch das Hinzufügen von Links zum Inhalt und zu den äußeren Elementen von Bannern und Folien wurden verschachtelte Links erstellt, die auf der Storefront nicht korrekt angezeigt wurden oder sich nicht korrekt verhalten haben. Um das Problem zu beheben, können Links nicht mehr zu *both* den Bereich Nachrichtentext und das Attribut Link für Banner und Folien.

![Problem behoben](../assets/fix.svg) <!-- Issue 421 --> Es wurde ein Problem behoben, bei dem das Festlegen eines leeren Rahmenradius für ein Registerkartenelement Fehler verursachte und den Inhalt des Registerkartenelements beschädigte.

![Problem behoben](../assets/fix.svg) <!-- Issue 422 --> Es wurde ein Problem behoben, bei dem das Hinzufügen bestimmter Bedingungskombinationen zum Filter &quot;Bedingungen für Produkte&quot;Fehler verursachte, die das Speichern des Formulars &quot;Produkte&quot;verhinderten.

![Problem behoben](../assets/fix.svg) <!-- Issue 425 -->Es wurde ein Problem behoben, bei dem sich der Slider-Inhaltstyp nicht ordnungsgemäß verhielt, wenn die Einstellung &quot;Unendliche Schleife&quot;deaktiviert war.

![Problem behoben](../assets/fix.svg) <!-- Issue 426 -->Korrektur des Mindestpreises für Werbung, sodass er jetzt in [!DNL Page Builder].

![Problem behoben](../assets/fix.svg) <!-- Issue 436 -->Es wurde ein Problem in Safari und IE 11 behoben, das das Ziehen und Ablegen eines Bildes in den Upload-Bereich in Bannern und Folien verhinderte.

![Problem behoben](../assets/fix.svg) <!-- Issue 525 -->Es wurde ein Problem behoben, durch das der Slider-Inhaltstyp in Firefox nicht responsiv war.

![Problem behoben](../assets/fix.svg) <!-- Issue 567 -->Es wurde ein Problem behoben, bei dem die Widget-Konfiguration falsche Selektoren im DOM für die verschiedenen Erscheinungen erstellte.

![Problem behoben](../assets/fix.svg) <!-- Issue 609 -->Fehlerkorrektur - Das Optionsmenü des Inhaltstyps wird jetzt in der Kopfzeilen-Symbolleiste angezeigt, sodass der Zugriff auf das Formular und andere Optionen nicht mehr möglich ist.

![Problem behoben](../assets/fix.svg) <!-- Issue 612, 613 -->Es wurde ein Problem behoben, bei dem Regler und mehrere Zeilen mit einem parallax-Hintergrund nach mehrmaligem Umschalten des Vollbildmodus nicht korrekt dargestellt wurden.

![Problem behoben](../assets/fix.svg) <!--MC-35220-->Es wurde ein Problem behoben, bei dem der Versuch, den Inhalt aus einem Überschrifteninhaltstyp in einen Textinhalttyp zu kopieren, verhindert wurde. [!DNL Page Builder] nicht speichern.

![Problem behoben](../assets/fix.svg) <!-- MC-34620 -->Der Inhaltstyp Text wurde dahingehend korrigiert, dass nicht-lateinische 1-Zeichen korrekt verarbeitet und gespeichert werden.

![Problem behoben](../assets/fix.svg) <!-- MC-34679 -->Fest [!DNL Page Builder] CSS-Stile, die dazu geführt haben, dass Safari 13.1 das Site-Menü des Luma-Designs für kleine Viewports und mobile Bildschirme falsch gerendert hat.

![Problem behoben](../assets/fix.svg) <!-- MC-34848 -->Der Inhaltstyp HTML wurde dahingehend korrigiert, dass eingebettete Widgets wie &quot;Sortieren nach SKU&quot;korrekt in der Storefront angezeigt werden.

## 1.4.1 für Adobe Commerce 2.4.0-p1

![Neu](../assets/new.svg) <!-- PB-590 --> Aktualisierung auf TinyMCE 4. TinyMCE 3 wurde entfernt, um die Sicherheit zu verbessern.

## 1.4.0 für Adobe Commerce 2.4.0

![Neu](../assets/new.svg) <!-- PB-494 -->Unterstützung für PHP 7.4 hinzugefügt.

![Problem behoben](../assets/fix.svg) <!-- MC-31247 -->Es wurde ein Problem behoben, bei dem der Inhaltstyp Produkte keine konfigurierbaren Produkte anzeigte, wenn die Bedingung auf &quot;Preis&quot;festgelegt war.

![Problem behoben](../assets/fix.svg) <!-- PB-179 -->Die Konfiguration der Produktausrichtung wurde dahingehend korrigiert, dass nur der Produktcontainer selbst positioniert wurde, nicht der Inhalt des Produktcontainers, wie z. B. Produktname, Preis, Schaltflächen, Bilder und andere Elemente.

![Problem behoben](../assets/fix.svg) <!-- MC-33556 -->Leistungsverbesserungen.

![Problem behoben](../assets/fix.svg) Sicherheitsverbesserungen.

## 1.3.3-p1 für Adobe Commerce 2.3.6-p1

![Problem behoben](../assets/fix.svg) Sicherheitsverbesserungen.

## 1.3.3 für Adobe Commerce 2.3.6

![Problem behoben](../assets/fix.svg) <!-- MC-32766 -->Der Inhaltstyp Text wurde dahingehend korrigiert, dass die den HTML-Attributen hinzugefügten Variablenanweisungen korrekt gespeichert wurden.

![Problem behoben](../assets/fix.svg) <!-- MC-34590 -->Der Inhaltstyp Text wurde dahingehend korrigiert, dass nicht-lateinische 1-Zeichen korrekt verarbeitet und gespeichert werden.

![Problem behoben](../assets/fix.svg) <!-- MC-34677 -->Fest [!DNL Page Builder] CSS-Stile, die dazu geführt haben, dass Safari 13.1 das Site-Menü des Luma-Designs für kleine Viewports und mobile Bildschirme falsch gerendert hat.

![Problem behoben](../assets/fix.svg) <!-- MC-34846 -->Der Inhaltstyp HTML wurde dahingehend korrigiert, dass eingebettete Widgets wie _Bestellung nach SKU_ auf der Storefront.

![Problem behoben](../assets/fix.svg) Fehlerkorrektur - das Speichern von Formularen vom Typ Inhalt ist nun problemlos möglich. Der Fehler (&quot;[!DNL Page Builder] 5 Sekunden lang gerendert wurde, ohne Sperren freizugeben&quot;), wurde das Lader-Symbol nach dem Speichern eines Formulars unbegrenzt rotiert.

## 1.3.2 für Adobe Commerce 2.3.5-p2

![Neu](../assets/new.svg) Sicherheitsverbesserungen.

## 1.3.1 für Adobe Commerce 2.3.5-p1

Diese Version von [!DNL Page Builder] ist nur ein Update der Versionsnummer für Adobe Commerce 2.3.5-p1. Alle für Version 1.3.0 beschriebenen Funktionen gelten auch für diese Version.

## 1.3.0 für Adobe Commerce 2.3.5

![Neu](../assets/new.svg) **Vorlagen** - [!DNL Page Builder] verfügt jetzt über Vorlagen, die aus vorhandenen Inhalten erstellt und auf neue Inhaltsbereiche angewendet werden können. [!DNL Page Builder] Vorlagen speichern sowohl Inhalte als auch Layouts von vorhandenen Seiten, Bausteinen, dynamischen Bausteinen, Produktattributen und Kategoriebeschreibungen. Sie können beispielsweise eine vorhandene [!DNL Page Builder] CMS-Seite als Vorlage verwenden und diese Vorlage (mit allen Inhalten und Layouts) anwenden, um schnell CMS-Seiten für Ihre Site zu erstellen. Diese neue Funktion wird hier beschrieben: [Vorlagen](templates.md).

![Neu](../assets/new.svg) **Videohintergründe für Zeilen, Banner und Regler** - [!DNL Page Builder] Zeilen, Banner und Regler können jetzt Videos für ihren Hintergrund verwenden. Diese neuen Funktionen werden hier beschrieben: [Zeilen](row.md), [Banner](banner.md), [Regler](slider.md).

![Neu](../assets/new.svg) **Ergänzungen und Verbesserungen der Videounterstützung** - [!DNL Page Builder] unterstützt jetzt eine größere Anzahl von Videoformaten. Zusätzlich zu YouTube- und Vimeo-Videos unterstützen der Videoinhaltstyp und der Videoband jetzt Video-URL-Links zu Videoformaten wie `.mp4` und anderen browserunterstützten Formaten. Der Content-Typ Video fügt außerdem eine Funktion für die automatische Wiedergabe hinzu. Diese neuen Funktionen werden hier beschrieben: [Videoinhaltstyp](video.md).

![Neu](../assets/new.svg) **Zeilen, Banner und Regler mit voller Höhe** - [!DNL Page Builder] Zeilen, Banner und Regler können jetzt ihre Höhe auf die volle Höhe der Seite festlegen, indem eine Zahl mit jeder CSS-Einheit (px, %, vh, em) oder eine Berechnung zwischen Einheiten (100vh - 237px) verwendet wird. Diese neuen Funktionen werden hier beschrieben: [Zeilen](row.md), [Banner](banner.md), [Regler](slider.md).

![Neu](../assets/new.svg) **Aktualisierungsbibliothek für Inhaltstypen** - Entwickler können jetzt Versionen von erstellen [!DNL Page Builder] Inhaltstypen ohne Einführung abwärtsinkompatibler Probleme mit früheren Versionen. Vor dieser Version führten wesentliche Änderungen an den Inhaltstypkonfigurationen zu Anzeige- und Datenverlusten bei zuvor gespeicherten Inhalten [!DNL Page Builder] Inhaltstypen. Die neue Upgrade-Bibliothek behebt diese Probleme. Die Bibliothek dient der Aktualisierung früherer Versionen von in der Datenbank gespeicherten Inhaltstypen, sodass sie mit den Konfigurationsänderungen in den neuen Versionen übereinstimmen. [!DNL Page Builder] führt die Upgrade-Bibliothek nach Bedarf für native Inhaltstypen aus, die für eine neue Version erforderlich sind. Durch diese Änderung wird sichergestellt, dass die integrierte [!DNL Page Builder] Inhaltstypen werden immer so aktualisiert, dass sie mit allen Änderungen übereinstimmen, die für eine neuere Version an Inhaltstypen vorgenommen wurden.

>[!IMPORTANT]
>
>Wenn Sie zusätzliche Datenbankentitäten zum Speichern erstellt haben [!DNL Page Builder] Inhalt, _must_ Fügen Sie diese Entitäten zu Ihren `etc/di.xml`. Wenn nicht, wird die Variable [!DNL Page Builder] In Ihrer Entität gespeicherte Inhalte werden nicht aktualisiert, was zu möglichen Datenverlusten und Anzeigeproblemen führt. Wenn Sie beispielsweise eine Blog-Entität erstellt haben, die [!DNL Page Builder] Inhalt, müssen Sie Ihre Blog-Entität zu Ihrer `etc/di.xml` als `UpgradableEntitiesPool` Typ, damit die Upgrade-Bibliothek die [!DNL Page Builder] Inhaltstypen, die in Ihrem Blog verwendet werden. Weitere Informationen und Anweisungen zur Verwendung der Upgrade-Bibliothek finden Sie unter [Aktualisierungstypen](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) im _Entwicklerhandbuch für Page Builder_.

![Neu](../assets/new.svg) **Dokumentation zum Hinzufügen neuer Erscheinungen** - Informationen für Entwickler werden jetzt veröffentlicht über [Hinzufügen von Erscheinungen](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) für vorhandene oder benutzerdefinierte Inhaltstypen.

![Problem behoben](../assets/fix.svg) **Verschiedene Fehlerbehebungen**

- <!-- PB-50 -->Es wurde ein Problem behoben, bei dem das Menü TinyMCE für Diaseinhalte unter anderen Inhaltstypen angezeigt wurde, wenn der übergeordnete Container der Folie dupliziert wurde.
- <!-- PB-166 -->Aktualisiert [!DNL Page Builder] , um in einigen Szenarien Speicherlecks zu vermeiden.
- <!-- PB-170 -->Verbesserte TinyMCE-Leistung bei Verwendung mehrerer Instanzen in der Admin-Phase.
- <!-- PB-252 -->Es wurde ein Problem behoben, bei dem der Content-Typ Dynamischer Block nicht auf der Admin-Bühne gerendert wurde, wenn die oberste Zeile als ausgeblendet markiert wurde.
- <!-- PB-273 -->Verfeinerte Mauszeiger-Ereignisse auf der Admin-Bühne durch Entfernen einer Verzögerung von 200 ms aus verschiedenen Benutzeroberflächensteuerelementen. Diese Änderung erleichtert die Arbeit mit verschachtelten Inhaltselementen auf der Bühne.
- <!-- PB-294 -->Es wurde ein Problem behoben, bei dem das Währungssymbol im Widget Produktliste im Block/Dynamischer Block auf der Admin-Bühne nicht richtig maskiert wurde.
- <!-- PB-296 -->Es wurde ein Problem behoben, bei dem die Produktsumme auf der [!DNL Page Builder] Das Bearbeitungsfenster funktionierte nicht für benutzerdefinierte MSI Stock-Produkte.
- <!-- PB-317 -->Es wurde ein Problem behoben, bei dem das Speichern [!DNL Page Builder] Inhalte mit Hintergrundbildern in Microsoft Edge rendern diese Bilder nicht auf der Storefront.
- <!-- PB-390 -->Es wurde ein Problem behoben, durch das verschachtelte [!DNL Page Builder] Inhalt kann nicht gespeichert werden, wenn Benutzer auf die Schaltfläche Speichern klicken, bevor die Seite vollständig gerendert wird.
- <!-- PB-418 -->Es wurde ein Ausnahmefehler behoben, der in Cron-Aufträgen aufgrund von [!DNL Page Builder] Analytics.

## 1.2.2 für Adobe Commerce 2.3.4-p2

![Neu](../assets/new.svg) Sicherheitsverbesserungen.

## 1.2.1 für Adobe Commerce 2.3.4-p1

![Neu](../assets/new.svg) Sicherheitsverbesserungen.

## 1.2.0 für Adobe Commerce 2.3.4

![Neu](../assets/new.svg)  **[!DNL Page Builder]Integration mit PWA Studio** - hinzugefügt [!DNL Page Builder] Inhaltswiedergabe an die Venia-App in PWA Studio. [!DNL Page Builder] Der Inhalt kann jetzt in der Venia-App von PWA Studio angezeigt werden. Siehe [!DNL Page Builder] Dokumentation in [PWA Studio] für alle Informationen zu dieser neuen Funktion.

![Neu](../assets/new.svg) **Produktkarussell hinzugefügt** - <!-- PB-77, PB-173, PB-175 -->Der Inhaltstyp Produkte bietet jetzt eine Option, Ihre Produkte im Karussell-/Reglerformat anzuzeigen, einschließlich verschiedener Optionen, um das Karussell an Ihre Anforderungen anzupassen.

![Neu](../assets/new.svg) **Produkt-SKU-Sortierung hinzugefügt** - <!-- PB-69 -->Der Inhaltstyp Produkte bietet jetzt eine Option, Ihre Produkte nach SKU zu sortieren, sodass Sie sie einer Liste innerhalb des Administrators hinzufügen können.

![Neu](../assets/new.svg) **Sortierung der Produktkategorie hinzugefügt** - <!-- PB-181 -->. Der Inhaltstyp Produkte bietet jetzt eine Option, Ihre Produkte nach Kategorie zu sortieren _position_ angezeigt werden, und zwar in derselben Reihenfolge, in der sie in Ihrem Commerce-Katalog angezeigt werden.

![Neu](../assets/new.svg) **Hinzufügung der Gesamtwerte für die Produktauswahl** - <!-- PB-107 -->. Der Content-Typ Admin-Editor für Produkte zeigt jetzt die Gesamtzahl der Produkte an, die mit Ihren Produktauswahloptionen übereinstimmen.

![Problem behoben](../assets/fix.svg) **Verschiedene Fehlerbehebungen**

- <!-- PB-237 -->Sicherheitsverbesserungen.
- <!-- PB-41 -->Es wurden Suchvorgänge innerhalb von Benutzeroberflächen-Auswahlkomponenten korrigiert, sodass pro Suchbegriff nur eine AJAX Anfrage gestellt wird.
- <!-- PB-76, PB-84-->Die Produktvorschau in Admin wurde aktualisiert, um sie an die Storefront anzupassen, einschließlich der Optionen für Stern-Bewertung, Farbe und Größe des Produkts, sofern relevant.
- <!-- PB-169 -->Es wurde ein Problem behoben, bei dem [!DNL Page Builder] konnte nicht gespeichert werden, wenn JavaScript-Minimierung und -Bundling in Commerce aktiviert sind.
- <!-- PB-241 -->Die Admin-Vorschau von Produkten, Bausteinen und dynamischen Bausteinen wurde dahingehend korrigiert, dass sie auf Commerce-Installationen korrekt dargestellt wird, die unterschiedliche URLs für Admin und Frontend definieren.
- <!-- PB-238 -->Die Admin-Vorschau von Produkten, Bausteinen und dynamischen Bausteinen wurde dahingehend korrigiert, dass sie auf Commerce-Installationen korrekt dargestellt wird, bei denen B2B mit der Variablen _Nur Anmeldung_ aktiviert ist. Vor dieser Korrektur muss die Variable [!DNL Page Builder] -Vorschau bewirkt, dass die Seite zur Kundenkontoanmeldung weitergeleitet wird.
- <!-- PB-239 -->Es wurde ein Sitzungsfehler behoben, der bei der Vorschau einer großen Seite im [!DNL Page Builder] Admin.
- <!-- PB-248 -->Aktualisiert [!DNL Page Builder] WENIGER Stile, um eine Duplizierung des Storefront-Stils zu verhindern.

## 1.1.1 für Adobe Commerce 2.3.3-p1

![Neu](../assets/new.svg) Sicherheitsverbesserungen.

## 1.1.0 für Adobe Commerce 2.3.3

![Neu](../assets/new.svg) <!-- MC-15250 -->Eine explizite Produktsortierung zum Inhaltstyp Produkte wurde hinzugefügt.

![Neu](../assets/new.svg) <!-- MC-17823 -->Es wurden Schaltflächen zum Einfügen von Bildern, Widgets und Variablen in den Inhaltstyp HTML hinzugefügt.

![Problem behoben](../assets/fix.svg) Verbessert [!DNL Page Builder] Sicherheit.

![Problem behoben](../assets/fix.svg) <!-- MC-1805 -->Aktualisiert [!DNL Page Builder] um PHP Version 7.3 zu unterstützen.

![Problem behoben](../assets/fix.svg) <!-- MC-4137 -->TinyMCE wurde auf Version 4.9.5 aktualisiert. Diese Aktualisierung sowie die zusätzlichen Verbesserungen haben mehrere Inline-Editor-Probleme mit TinyMCE behoben:

- Variablen, Bilder und Bildlinks werden an der Stelle hinzugefügt, an der der Cursor platziert wird.
- Tabellen und Tabellenzellen können zentriert ausgerichtet werden.
- Beim Kopieren/Einfügen wird jetzt Inhalt an der Cursorposition eingefügt.
- Links können auf ausgewählten Text angewendet werden.
- Aufzählungszeichen sind korrekt ausgerichtet.
- Änderungen im Inline-Editor können gespeichert werden, ohne dass Sie zuvor außerhalb des Editors klicken.

![Problem behoben](../assets/fix.svg) <!-- MC-3880 -->Es wurde ein Problem behoben, bei dem die minimale Höhe und vertikale Ausrichtung zwischen den Abschnitten im Bearbeitungsbereich für jeden Inhaltstyp inkonsistent waren.

![Problem behoben](../assets/fix.svg) <!-- MC-14994 -->Es wurde ein Problem behoben, bei dem die Symbolleiste des Inhaltstyps Überschrift falsch positioniert wurde, wenn sie zum ersten Mal auf der Bühne abgelegt wurde.

![Problem behoben](../assets/fix.svg) <!-- MC-15742 -->Korrektur hartcodierter Ränder in den Inhaltstypen Regler und Video .

![Problem behoben](../assets/fix.svg) <!-- MC-16241 -->Es wurde ein Problem behoben, bei dem das erforderliche Sternchen-Symbol in Formularfeldern zweimal angezeigt wurde.

## 1.0.3 für Adobe Commerce 2.3.2-p2

![Neu](../assets/new.svg) Sicherheitsverbesserungen.

## 1.0.2 für Adobe Commerce 2.3.2-p1

![Neu](../assets/new.svg) Sicherheitsverbesserungen.

## 1.0.1 für Adobe Commerce 2.3.2

![Neu](../assets/new.svg) Sicherstellung der Kompatibilität mit Adobe Commerce 2.3.2.

## 1.0.0 für Adobe Commerce 2.3.1

![Neu](../assets/new.svg) Allgemeine Verfügbarkeitsversion


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
