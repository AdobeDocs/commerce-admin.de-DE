---
title: Versionshinweise für  [!DNL Page Builder]
description: Informationen zu allen [!DNL Page Builder] Versionen finden Sie in den Versionshinweisen .
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2813'
ht-degree: 0%

---

# Versionshinweise für [!DNL Page Builder]

Diese Versionshinweise beschreiben die Versionen von [!DNL Page Builder] und umfassen:

![Neu](../assets/new.svg) Neue Funktionen

![Korrektur eines Problems](../assets/fix.svg) Fehlerbehebungen und Verbesserungen

![Bekanntes Problem](../assets/bug.svg) Bekannte Probleme

>[!IMPORTANT]
>
>Ab Version 2.4.3 ist [!DNL Page Builder] jetzt als gebündelte Erweiterung in Magento Open Source verfügbar. Es ist jetzt das Standard-Tool zur Inhaltsbearbeitung für Adobe Commerce und Magento Open Source und kann den WYSIWG-Editor durch ein beliebiges Drittanbietermodul ersetzen.

## 1.7.2 für Commerce 2.4.5

![Neu](../assets/new.svg) **Neue Wrapper-Entität - [!DNL Columns] für Spaltenlayouts eingeführt** - Zuvor konnten Benutzer Spalten nur innerhalb eines anderen Container-/Wrapper-Inhaltstyps hinzufügen, z. B. [!DNL Tab] oder [!DNL Row]. Jetzt hat der [!DNL Column] einen eigenen Wrapper und kann direkt auf der Bühne hinzugefügt werden. Außerdem verfügt der [!DNL Columns] -Container über ein Einstellungselement, in dem Benutzer die Konfiguration für diese Wrapper-Entität angeben können.<!--- PB-500-->

![Neu](../assets/new.svg) **Neue Menüoptionen zum Duplizieren, Ausblenden und Löschen von Spalten-Gruppen** - Mit diesen neuen Optionen können Benutzer [!DNL Columns]-Gruppen duplizieren, ausblenden und löschen - genau wie bei Inhaltstypen.<!--- PB-507-->

![Neu](../assets/new.svg) <!-- Issue 594 -->**Neue mehrzeilige Spaltenunterstützung zur Spaltengruppe** hinzugefügt - Mit diesem Zusatz können Benutzer mehrere Zeilen mit Spalten innerhalb einer [!DNL Columns] -Gruppe bearbeiten, um Spaltenlayouts viel flexibler zu gestalten.<!--- PB-108-->

Informationen zur Verwendung der neuen [!DNL Columns] -Gruppe finden Sie unter [Layout - Spalte](./column.md) .

## 1.7.1 für Commerce 2.4.4

![Problem behoben](../assets/fix.svg) Seitenaufbau ist jetzt mit PHP 8.1 kompatibel.<!--- AC-1300-->

![Problem behoben](../assets/fix.svg) Händler können Bildern (Bild, Banner, Folie) jetzt alternativen Text (`alt_text`) hinzufügen, um die Barrierefreiheit von Inhalten zu verbessern.<!--- PB-1193-->

![Problem behoben](../assets/fix.svg) Admin-Benutzer mit Berechtigungen, die auf die Inhaltsbearbeitung beschränkt sind, sehen keinen Fehler mehr, wenn sie mit dem Seitenaufbau ein Produkt-Widget zu einer CMS-Seite hinzufügen. Der Seitenaufbau zeigt außerdem eine genaue Produktanzahl auf der Seite mit den Widget-Einstellungen an. Zuvor benötigte Page Builder Berechtigungen für das Catalog-Modul beim Abrufen der Produktanzahl und zeigte diesen Fehler an: `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![Korrektur eines Problems](../assets/fix.svg) Anzeigeprobleme mit dem Menü &quot;Seitenaufbau-Format&quot;wurden jetzt mit dem Upgrade der TinyMCE 5-Bibliothek behoben. <!--- AC-446-->

![Korrektur des Fehlers](../assets/fix.svg) Jetzt können Sie mit der Maus einen **Text zur Anzeige** -Wert im Popup &quot;Link einfügen&quot;bearbeiten. <!--- AC-982-->

![Problem behoben](../assets/fix.svg) Der Seitenaufbau zeigt jetzt alle Optionen wie erwartet im Menü &quot;Schriftgrößenoptionen&quot;an. Zuvor wurden nicht alle Optionen angezeigt. <!--- AC-1056-->

![ Problem behoben](../assets/fix.svg) Aktualisierung der `phpgt/dom` Composer-Abhängigkeit für die `magento/magento2-page-builder` -Erweiterung auf die neuesten Versionen. <!--- magento/magento2-page-builder/pull/779-->

![Korrektur des Fehlers](../assets/fix.svg) Der Seitenaufbau ändert die Größe der Dialogfelder &quot;Link einfügen&quot;und &quot;Bild einfügen&quot;nicht mehr, wenn der Regler in einer kleinen Spalte angezeigt wird. <!--- AC-973-->

![Problem behoben](../assets/fix.svg) Das Menü &quot;Seitenaufbau-Tabelleneigenschaften&quot;wird jetzt erwartungsgemäß angezeigt. <!--- AC-407-->

![Korrektur des Fehlers](../assets/fix.svg) Reglerpunkte werden nicht mehr auf dem Link &quot;Einfügen&quot;oder Bild-Modal angezeigt, wenn der Mauszeiger nicht über den Regler bewegt wird. <!--- AC-406-->

![Problem behoben](../assets/fix.svg) Die Schriftgröße zur Anzeige der Tabellenmenüoptionen wurde optimiert. <!--- AC-396-->

![Korrektur des Fehlers](../assets/fix.svg) Korrektur von Anomalien bei der Positionierung der Dialogfelder &quot;Bild einfügen/bearbeiten&quot;und &quot;Link einfügen/bearbeiten&quot;. <!--- AC-397-->

![Korrektur des Fehlers](../assets/fix.svg) Der Seitenaufbau gibt keinen Fehler mehr aus, wenn Sie für ein Banner auf **Texteditor** klicken. <!--- AC-398-->

![Problem behoben](../assets/fix.svg) Der Seitenaufbau konvertiert während der Aktualisierung nicht mehr alle dynamischen Blöcke in eine Sprache. <!--- MC-42265-->

## 1.6.0 für Adobe Commerce 2.4.2

![Neu](../assets/new.svg) <!-- Issue 558 -->**Neuer [!DNL Page Builder] Stil** - [!DNL Page Builder] hat die Formatierung von Inhalten massiv verbessert. Die Änderungen erleichtern es nun, einfache CSS-Selektoren zu erstellen, um die vorhandenen Inhaltstypstile zu überschreiben. Diese Änderungen ermöglichen die Erstellung von [!DNL Page Builder] Designs mit umfassender Reaktionsfähigkeit für alle Inhaltstypen.

![Neu](../assets/new.svg) <!-- Issue 429 -->**Zeilencontainer jetzt optional** - Sie können jetzt Inhalte in [!DNL Page Builder] erstellen, ohne einen Zeilencontainer zu benötigen. Neben der Zeile können nun die folgenden Inhaltstypen direkt auf die Bühne gezogen und dort abgelegt werden: HTML, Block, dynamischer Block, Spalten und Registerkarten.

![Neu](../assets/new.svg) <!-- Issue 636 -->**Neuer responsiver Viewport-Umschalter** - Sie können jetzt Ihre [!DNL Page Builder] -Inhalte in verschiedenen Gerätebreiten (Haltepunkten) mit den neuen Schaltflächen des Admin Viewport-Switchers über der Bühne in der Vorschau anzeigen. Der Viewport-Umschalter simuliert, wie Ihr Inhalt formatiert wird, wenn er auf verschiedenen Geräten auf der Storefront angezeigt wird.

![Neu](../assets/new.svg) <!-- Issue 637 -->**Neue Breakpoint-spezifische Formularfelder** - Feldwerte vom Typ Inhalt können jetzt auf bestimmte Viewport-Haltepunkte festgelegt werden. Symbolindikatoren neben den Feldern zeigen den Viewport an, auf den der Feldwert für den Inhaltstyp angewendet wird.

![Neu](../assets/new.svg) <!-- Issue 559 -->**Vordefinierte Formularfeldeinträge entfernt** - Erweiterte Formulareinstellungen für Ränder, Paddings und randbezogene Eigenschaften (Rahmen, Rahmenbreite und Rahmenradius) werden jetzt auf `default` festgelegt, sodass Werte durch das CSS eines Moduls definiert werden können.

![Neu](../assets/new.svg) <!-- Issue 635, 557,  -->**Hinzugefügter Staging-Abstand** - Zeilen und Spalten bieten jetzt zusätzliche Abstände um die enthaltenen Inhaltstypen auf der Bühne, aber nicht auf der Storefront. Der zusätzliche Staging-Abstand erleichtert den Zugriff auf die Mouseover-Optionsmenüs für Container und enthaltene Inhaltstypen.

![Korrektur des Fehlers](../assets/fix.svg) <!-- MC-37348 -->**Korrektur des automatischen Bildlaufs zu Bewertungen** - Der automatische Bildlauf zu Produktüberprüfungen auf der Storefront wurde jetzt behoben.

![Korrektur des Problems](../assets/fix.svg) <!-- MC-36227 -->**Korrektur des beschnittenen Inhalts** - Lange Kategorie- und Produktbeschreibungen werden nicht mehr zugeschnitten.

![Problem behoben](../assets/fix.svg) <!-- MC-35402 -->**Es wurde ein Problem mit dem Inhalt der Kategorie mit voller Breite behoben** - Der Inhalt der Kategorie kann jetzt in einem Layout mit voller Breite oder mit voller Füllung angezeigt werden.

![Problem behoben](../assets/fix.svg) <!-- MC-37989 -->**Verbesserungen der Sicherheit**

## 1.5.1 für Adobe Commerce 2.4.1-p1

![Korrektur des Fehlers](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**Fehleranzeige** - Es wurde ein Problem behoben, bei dem [!DNL Page Builder] beim Hinzufügen von Katalog-Unterkategorien zum Admin einen Fehler anzeigte.

## 1.5.0 für Adobe Commerce 2.4.1

![Neu](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**Reduzierende Vollbildbearbeitung** - Die Bearbeitung von [!DNL Page Builder] -Inhalt ist jetzt nur für alle Bereiche im Vollbildmodus, die von [!DNL Page Builder] gesteuert werden. Diese Änderung umfasst CMS-Seiten, Produkt- und Kategorieseiten, Blöcke und dynamische Blöcke. Die Bearbeitung im Vollbildmodus konzentriert sich auf Ihren Inhalt und bietet eine Ansicht, die dem Benutzererlebnis auf der Storefront besser entspricht.

![Neu](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder] Inhaltsvorschau **- Standardmäßig bietet [!DNL Page Builder] jetzt Inhaltsvorschau nicht nur für CMS-Seiten, Blöcke und dynamische Blöcke, sondern auch für Produkt- und Kategorieseiten. Sie können diese Funktion mithilfe der neuen Einstellung &quot;[!DNL Page Builder] Inhaltsvorschau&quot;für Produkt- und Kategorieseiten aktivieren oder deaktivieren, auf die Sie in der Speicherkonfiguration unter Content Management > Erweiterte Inhaltswerkzeuge zugreifen können.

![Neu](../assets/new.svg) <!-- Issue 543 -->**Verbesserter Zugriff auf kurze Produktbeschreibungen** - Standardmäßig wird jetzt vor der längeren Beschreibung eine kurze Beschreibung des Produkts angezeigt. Diese Änderung entspricht der Reihenfolge, in der sie auf der Storefront angezeigt werden, und verhindert, dass der längere Beschreibungsinhalt durchblättert werden muss, um Zugriff auf die kurze Beschreibung zu erhalten.

![Neu](../assets/new.svg) <!-- Issue 419 -->**Verhindern verschachtelter Links in Bannern und Folien** - Hinzufügen von Links zum Inhalt und zu den äußeren Elementen von Bannern und Folien, die verschachtelte Links erstellt haben, die auf der Storefront nicht korrekt angezeigt wurden oder sich nicht korrekt verhalten haben. Um das Problem zu beheben, können dem Bereich Nachrichtentext und dem Attribut Link für Banner und Folien nicht mehr *beide* Links hinzugefügt werden.

![Korrektur des Fehlers](../assets/fix.svg) <!-- Issue 421 --> Es wurde ein Problem behoben, bei dem das Festlegen eines leeren Rahmenradius auf einem Registerkartenelement Fehler verursachte und den Inhalt eines Registerkartenelements beschädigte.

![Korrektur des Fehlers](../assets/fix.svg) <!-- Issue 422 --> Korrektur des Fehlers, der dazu führte, dass beim Hinzufügen bestimmter Bedingungskombinationen zum Filter &quot;Bedingungen für Produkte&quot;Fehler verursacht wurden, die das Speichern des Formulars &quot;Produkte&quot;verhinderten.

![Korrektur des Fehlers](../assets/fix.svg) <!-- Issue 425 -->Korrektur des Fehlers, der dazu führte, dass sich der Slider-Inhaltstyp nicht korrekt verhielt, wenn die Einstellung &quot;Unendliche Schleife&quot;deaktiviert war.

![Korrektur des Fehlers](../assets/fix.svg) <!-- Issue 426 -->Korrektur des Mindestpreises für Werbung, sodass er jetzt in [!DNL Page Builder] funktioniert.

![Korrektur des Fehlers](../assets/fix.svg) <!-- Issue 436 -->Korrektur des Fehlers in Safari und IE 11, der das Ziehen und Ablegen eines Bildes in den Upload-Bereich in Bannern und Folien verhindert hat.

![Korrektur des Fehlers](../assets/fix.svg) <!-- Issue 525 -->Korrektur des Problems, bei dem der Slider-Inhaltstyp in Firefox nicht responsiv war.

![Korrektur des Fehlers](../assets/fix.svg) <!-- Issue 567 -->Korrektur des Problems, bei dem die Widget-Konfiguration falsche Selektoren im DOM für die verschiedenen Erscheinungen erstellte.

![Korrektur des Fehlers](../assets/fix.svg) <!-- Issue 609 -->Korrektur des Fehlers, der dazu führte, dass in der Kopfzeilen-Symbolleiste das Optionsmenü des Inhaltstyps ausgeblendet wurde, wodurch der Zugriff auf das Formular und andere Optionen verhindert wurde.

![Korrektur des Fehlers](../assets/fix.svg) <!-- Issue 612, 613 -->Korrektur des Fehlers, bei dem Regler und mehrere Zeilen, die parallax-Hintergründe verwenden, nach mehrmaligem Umschalten des Vollbildmodus nicht korrekt dargestellt wurden.

![Korrektur des Fehlers](../assets/fix.svg) <!--MC-35220-->Korrektur des Fehlers, der dazu führte, dass beim Versuch, den Inhalt aus einem Überschrifteninhaltstyp in einen Textinhalttyp zu kopieren, [!DNL Page Builder] nicht gespeichert werden konnte.

![Korrektur des Fehlers](../assets/fix.svg) <!-- MC-34620 -->Korrektur des Textinhaltstyps, um nicht-lateinische 1 Zeichen korrekt zu verarbeiten und zu speichern.

![Korrektur des Fehlers](../assets/fix.svg) <!-- MC-34679 -->Korrektur des [!DNL Page Builder] CSS-Stils, der dazu führte, dass Safari 13.1 das Site-Menü des Luma-Designs für kleine Viewports und mobile Bildschirme fälschlicherweise renderte.

![Korrektur des Problems](../assets/fix.svg) <!-- MC-34848 -->Korrektur des HTML-Inhaltstyps, um eingebettete Widgets wie &quot;Sortieren nach SKU&quot;auf der Storefront korrekt anzuzeigen.

## 1.4.1 für Adobe Commerce 2.4.0-p1

![Neu](../assets/new.svg) <!-- PB-590 --> Upgrade auf TinyMCE 4. TinyMCE 3 wurde entfernt, um die Sicherheit zu verbessern.

## 1.4.0 für Adobe Commerce 2.4.0

![Neu](../assets/new.svg) <!-- PB-494 -->Unterstützung für PHP 7.4 hinzugefügt.

![Korrektur des Fehlers](../assets/fix.svg) <!-- MC-31247 -->Korrektur des Fehlers, der dazu führte, dass der Inhaltstyp &quot;Produkte&quot;keine konfigurierbaren Produkte anzeigte, wenn die Bedingung auf &quot;Preis&quot;festgelegt war.

![Korrektur des Problems](../assets/fix.svg) <!-- PB-179 -->Korrektur des Fehlers, der dazu führte, dass die Konfiguration zur Produktausrichtung nur den Produktcontainer selbst positionierte, nicht aber den Inhalt des Produktcontainers, wie z. B. Produktname, Preis, Schaltflächen, Bilder und andere Elemente.

![Problem behoben](../assets/fix.svg) <!-- MC-33556 -->Leistungsverbesserungen.

![Es wurden Sicherheitserweiterungen behoben.](../assets/fix.svg)

## 1.3.3-p1 für Adobe Commerce 2.3.6-p1

![Es wurden Sicherheitserweiterungen behoben.](../assets/fix.svg)

## 1.3.3 für Adobe Commerce 2.3.6

![Korrektur des Fehlers](../assets/fix.svg) <!-- MC-32766 -->Korrektur des Textinhaltstyps, um die den HTML-Attributen hinzugefügten Variablenanweisungen korrekt zu speichern.

![Korrektur des Fehlers](../assets/fix.svg) <!-- MC-34590 -->Korrektur des Textinhaltstyps, um nicht-lateinische 1 Zeichen korrekt zu verarbeiten und zu speichern.

![Korrektur des Fehlers](../assets/fix.svg) <!-- MC-34677 -->Korrektur des [!DNL Page Builder] CSS-Stils, der dazu führte, dass Safari 13.1 das Site-Menü des Luma-Designs für kleine Viewports und mobile Bildschirme fälschlicherweise renderte.

![Korrektur des Problems](../assets/fix.svg) <!-- MC-34846 -->Korrektur des HTML-Inhaltstyps, um eingebettete Widgets wie _Bestellung durch SKU_ auf der Storefront korrekt anzuzeigen.

![Problem behoben](../assets/fix.svg) Es wurde ein Fehler behoben, der manchmal verhinderte, dass Benutzer Formulare vom Typ Inhalt speichern konnten. Der Fehler (&quot;[!DNL Page Builder]&quot; wurde 5 Sekunden lang gerendert, ohne Sperren freizugeben&quot;) führte dazu, dass das Lader-Symbol nach dem Speichern eines Formulars unbegrenzt rotiert wurde.

## 1.3.2 für Adobe Commerce 2.3.5-p2

![Neu](../assets/new.svg) Verbesserungen bei der Sicherheit.

## 1.3.1 für Adobe Commerce 2.3.5-p1

Diese Version von [!DNL Page Builder] ist nur ein Update der Versionsnummer für Adobe Commerce 2.3.5-p1. Alle für Version 1.3.0 beschriebenen Funktionen gelten auch für diese Version.

## 1.3.0 für Adobe Commerce 2.3.5

![Neu](../assets/new.svg) **Vorlagen** - [!DNL Page Builder] enthält jetzt Vorlagen, die aus vorhandenen Inhalten erstellt und auf neue Inhaltsbereiche angewendet werden können. [!DNL Page Builder] Vorlagen speichern sowohl Inhalte als auch Layouts vorhandener Seiten, Blöcke, dynamischer Blöcke, Produktattribute und Kategoriebeschreibungen. Sie können beispielsweise eine vorhandene [!DNL Page Builder] CMS-Seite als Vorlage speichern und diese Vorlage (mit allen Inhalten und Layouts) anwenden, um schnell CMS-Seiten für Ihre Site zu erstellen. Diese neue Funktion wird hier dokumentiert: [Vorlagen](templates.md).

![Neu](../assets/new.svg) **Videobintergründe für Zeilen, Banner und Regler** - [!DNL Page Builder] Zeilen, Banner und Regler können jetzt Videos für ihren Hintergrund verwenden. Diese neuen Funktionen sind hier dokumentiert: [Zeilen](row.md), [Banner](banner.md), [Regler](slider.md).

![Neu](../assets/new.svg) **Ergänzungen und Verbesserungen der Videounterstützung** - [!DNL Page Builder] unterstützt jetzt eine größere Anzahl von Videoformaten. Zusätzlich zu YouTube- und Vimeo-Videos unterstützen der Videoinhaltstyp und der Videoband jetzt Video-URL-Links zu Videoformaten wie `.mp4` und anderen browserunterstützten Formaten. Der Content-Typ Video fügt außerdem eine Funktion für die automatische Wiedergabe hinzu. Diese neuen Funktionen sind hier dokumentiert: [Videoinhaltstyp](video.md).

![Neu](../assets/new.svg) **Zeilen, Banner und Schieberegler mit voller Höhe** - [!DNL Page Builder] Zeilen, Banner und Schieberegler können ihre Höhe jetzt mit einer Zahl mit beliebiger CSS-Einheit (px, %, vh, em) oder einer Berechnung zwischen Einheiten (100vh - 237px) auf die volle Höhe der Seite festlegen. Diese neuen Funktionen sind hier dokumentiert: [Zeilen](row.md), [Banner](banner.md), [Regler](slider.md).

![Neu](../assets/new.svg) **Aktualisierungsbibliothek für Inhaltstypen** - Entwickler können jetzt Versionen von [!DNL Page Builder] -Inhaltstypen erstellen, ohne rückwärtskompatible Probleme mit früheren Versionen einzuführen. Vor dieser Version führten wesentliche Änderungen an den Inhaltstypkonfigurationen zu Anzeige- und Datenverlusten bei zuvor gespeicherten [!DNL Page Builder] -Inhaltstypen. Die neue Upgrade-Bibliothek behebt diese Probleme. Die Bibliothek dient der Aktualisierung früherer Versionen von in der Datenbank gespeicherten Inhaltstypen, sodass sie mit den Konfigurationsänderungen in den neuen Versionen übereinstimmen. [!DNL Page Builder] führt die Upgrade-Bibliothek nach Bedarf für eine neue Version auf nativen Inhaltstypen aus. Diese Änderung stellt sicher, dass die integrierten [!DNL Page Builder] Inhaltstypen immer aktualisiert werden, um alle Änderungen an Inhaltstypen für eine neuere Version abzugleichen.

>[!IMPORTANT]
>
>Wenn Sie zusätzliche Datenbankentitäten zum Speichern von [!DNL Page Builder] -Inhalt erstellt haben, müssen Sie diese Entitäten _zu Ihrem `etc/di.xml` hinzufügen._ Andernfalls wird der in Ihrer Entität gespeicherte [!DNL Page Builder] -Inhalt nicht aktualisiert, was zu möglichen Datenverlusten und Anzeigeproblemen führt. Wenn Sie beispielsweise eine Blog-Entität erstellt haben, in der [!DNL Page Builder] -Inhalte gespeichert werden, müssen Sie Ihre Blog-Entität Ihrer `etc/di.xml` -Datei als `UpgradableEntitiesPool`-Typ hinzufügen, damit die Upgrade-Bibliothek die in Ihrem Blog verwendeten Inhaltstypen [!DNL Page Builder] aktualisieren kann. Weitere Informationen und Anweisungen zur Verwendung der Upgrade-Bibliothek finden Sie unter [Aktualisierungsinhaltstypen](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) im _Entwicklerhandbuch für Seiten-Builder_.

![Neu](../assets/new.svg) **Dokumentation zum Hinzufügen neuer Erscheinungen** - Entwicklerinformationen wurden jetzt über das Hinzufügen von Erscheinungen](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) für vorhandene oder benutzerdefinierte Inhaltstypen veröffentlicht.[

![Problem behoben](../assets/fix.svg) **Verschiedene Fehlerbehebungen**

- <!-- PB-50 -->Es wurde ein Problem behoben, bei dem das Menü TinyMCE für Diaseinhalte unter anderen Inhaltstypen angezeigt wurde, wenn der übergeordnete Container der Folie dupliziert wurde.
- <!-- PB-166 -->[!DNL Page Builder] wurde aktualisiert, um eine Zerstörungsmethode zu implementieren, um Speicherlecks in einigen Szenarien zu verhindern.
- <!-- PB-170 -->Verbesserte TinyMCE-Leistung bei Verwendung mehrerer Instanzen in der Admin-Phase.
- <!-- PB-252 -->Es wurde ein Problem behoben, bei dem der Content-Typ Dynamischer Block nicht auf der Admin-Bühne gerendert wurde, wenn die oberste Zeile als ausgeblendet markiert wurde.
- <!-- PB-273 -->Verfeinerte Mauszeiger-Ereignisse auf der Admin-Bühne durch Entfernen einer Verzögerung von 200 ms aus verschiedenen Benutzeroberflächensteuerelementen. Diese Änderung erleichtert die Arbeit mit verschachtelten Inhaltselementen auf der Bühne.
- <!-- PB-294 -->Es wurde ein Problem behoben, bei dem das Währungssymbol im Widget Produktliste im Block/Dynamischer Block auf der Admin-Bühne nicht richtig maskiert wurde.
- <!-- PB-296 -->Es wurde ein Problem behoben, bei dem die Produktsumme im Bearbeitungsfeld [!DNL Page Builder] für benutzerdefinierte MSI-Stock-Produkte nicht funktionierte.
- <!-- PB-317 -->Es wurde ein Problem behoben, durch das beim Speichern von [!DNL Page Builder] -Inhalten mit Hintergrundbildern in Microsoft Edge diese Bilder nicht im Storefront gerendert wurden.
- <!-- PB-390 -->Fehlerkorrektur - verschachtelte [!DNL Page Builder] -Inhalte können jetzt gespeichert werden, wenn Benutzer auf die Schaltfläche Speichern klicken, bevor die Seite vollständig gerendert wird.
- <!-- PB-418 -->Es wurde ein Ausnahmefehler behoben, der in Cron-Aufträgen aufgrund von [!DNL Page Builder] Analytics ausgelöst wurde.

## 1.2.2 für Adobe Commerce 2.3.4-p2

![Neu](../assets/new.svg) Verbesserungen bei der Sicherheit.

## 1.2.1 für Adobe Commerce 2.3.4-p1

![Neu](../assets/new.svg) Verbesserungen bei der Sicherheit.

## 1.2.0 für Adobe Commerce 2.3.4

![Neu](../assets/new.svg) **[!DNL Page Builder]Integration in PWA Studio** - Das Rendering von [!DNL Page Builder] Inhalten wurde zur Venia-App in PWA Studio hinzugefügt. [!DNL Page Builder] -Inhalte können jetzt in der Venia-App von PWA Studio angezeigt werden. Alle Informationen zu dieser neuen Funktion finden Sie in der Dokumentation zu [!DNL Page Builder] in [PWA Studio] .

![Neu](../assets/new.svg) **Produktkarussell hinzugefügt** - <!-- PB-77, PB-173, PB-175 -->Der Inhaltstyp &quot;Produkte&quot;bietet jetzt eine Option zum Anzeigen Ihrer Produkte im Karussell-/Reglerformat, einschließlich verschiedener Optionen zum Anpassen des Karussells an Ihre Anforderungen.

![Neu](../assets/new.svg) **Produkt-SKU-Sortierung hinzugefügt** - <!-- PB-69 -->Der Produktinhaltstyp bietet jetzt eine Option zum Sortieren Ihrer Produkte nach SKU in der Reihenfolge, in der Sie sie zu einer Liste innerhalb des Administrators hinzufügen.

![Neu](../assets/new.svg) **Sortierung der Produktkategorie** - <!-- PB-181 --> hinzugefügt. Der Inhaltstyp &quot;Produkte&quot;bietet jetzt eine Option zum Sortieren Ihrer Produkte nach Kategorie _Position_ und zeigt sie in der Reihenfolge an, in der sie im Commerce-Katalog angezeigt werden.

![Neu](../assets/new.svg) **Die Gesamtwerte der Produktauswahl wurden hinzugefügt** - <!-- PB-107 -->. Der Content-Typ Admin-Editor für Produkte zeigt jetzt die Gesamtzahl der Produkte an, die mit Ihren Produktauswahloptionen übereinstimmen.

![Problem behoben](../assets/fix.svg) **Verschiedene Fehlerbehebungen**

- <!-- PB-237 -->Sicherheitsverbesserungen.
- <!-- PB-41 -->Es wurden Suchvorgänge innerhalb von Benutzeroberflächen-Auswahlkomponenten korrigiert, sodass pro Suchbegriff nur eine AJAX Anfrage gestellt wird.
- <!-- PB-76, PB-84-->Die Produktvorschau in Admin wurde aktualisiert, um sie an die Storefront anzupassen, einschließlich der Optionen für Stern-Bewertung, Farbe und Größe des Produkts, sofern relevant.
- <!-- PB-169 -->Es wurde ein Problem behoben, bei dem [!DNL Page Builder] nicht gespeichert werden konnte, wenn die Minimierung und das Bundling von JavaScript in Commerce aktiviert waren.
- <!-- PB-241 -->Die Admin-Vorschau von Produkten, Bausteinen und dynamischen Bausteinen wurde dahingehend korrigiert, dass sie auf Commerce-Installationen korrekt dargestellt werden, die unterschiedliche URLs für Admin und Frontend definieren.
- <!-- PB-238 -->Die Admin-Vorschau von Produkten, Bausteinen und dynamischen Bausteinen wurde dahingehend korrigiert, dass sie auf Commerce-Installationen korrekt dargestellt werden, bei denen B2B mit aktivierter Option _Nur Anmeldung_ installiert ist. Vor dieser Fehlerbehebung führte die Vorschau von [!DNL Page Builder] dazu, dass die Seite zur Anmeldung des Kundenkontos weitergeleitet wurde.
- <!-- PB-239 -->Es wurde ein Sitzungsfehler behoben, der bei der Vorschau einer großen Seite in der [!DNL Page Builder] Admin-Konsole auftreten kann.
- <!-- PB-248 -->Die [!DNL Page Builder] LESS-Stile wurden aktualisiert, um eine Duplizierung des Storefront-Stils zu verhindern.

## 1.1.1 für Adobe Commerce 2.3.3-p1

![Neu](../assets/new.svg) Verbesserungen bei der Sicherheit.

## 1.1.0 für Adobe Commerce 2.3.3

![Neu](../assets/new.svg) <!-- MC-15250 -->Dem Inhaltstyp &quot;Produkte&quot;wurde eine explizite Produktsortierung hinzugefügt.

![Neu](../assets/new.svg) <!-- MC-17823 -->Es wurden Schaltflächen zum Einfügen von Bildern, Widgets und Variablen in den HTML-Inhaltstyp hinzugefügt.

![Korrektur des Problems](../assets/fix.svg) Verbesserte [!DNL Page Builder]-Sicherheit.

![Korrektur des Problems](../assets/fix.svg) <!-- MC-1805 -->Aktualisierte [!DNL Page Builder], um PHP Version 7.3 zu unterstützen.

![Problem behoben](../assets/fix.svg) <!-- MC-4137 -->TinyMCE wurde auf Version 4.9.5 aktualisiert. Diese Aktualisierung sowie die zusätzlichen Verbesserungen haben mehrere Inline-Editor-Probleme mit TinyMCE behoben:

- Variablen, Bilder und Bildlinks werden an der Stelle hinzugefügt, an der der Cursor platziert wird.
- Tabellen und Tabellenzellen können zentriert ausgerichtet werden.
- Beim Kopieren/Einfügen wird jetzt Inhalt an der Cursorposition eingefügt.
- Links können auf ausgewählten Text angewendet werden.
- Aufzählungszeichen sind korrekt ausgerichtet.
- Änderungen im Inline-Editor können gespeichert werden, ohne dass Sie zuvor außerhalb des Editors klicken.

![Korrektur des Fehlers](../assets/fix.svg) <!-- MC-3880 -->Es wurde ein Problem behoben, bei dem die minimale Höhe und vertikale Ausrichtung zwischen den Abschnitten im Bearbeitungsbereich für jeden Inhaltstyp inkonsistent waren.

![Korrektur des Fehlers](../assets/fix.svg) <!-- MC-14994 -->Korrektur des Fehlers, der dazu führte, dass die Symbolleiste des Inhaltstyps Überschrift beim ersten Ablegen auf der Bühne falsch positioniert wurde.

![Korrektur des Fehlers](../assets/fix.svg) <!-- MC-15742 -->Korrektur hartcodierter Ränder sowohl im Slider- als auch im Video-Inhaltstyp.

![Korrektur des Fehlers](../assets/fix.svg) <!-- MC-16241 -->Korrektur des Fehlers, der dazu führte, dass das erforderliche Sternchen-Symbol in Formularfeldern zweimal angezeigt wurde.

## 1.0.3 für Adobe Commerce 2.3.2-p2

![Neu](../assets/new.svg) Verbesserungen bei der Sicherheit.

## 1.0.2 für Adobe Commerce 2.3.2-p1

![Neu](../assets/new.svg) Verbesserungen bei der Sicherheit.

## 1.0.1 für Adobe Commerce 2.3.2

![Neu](../assets/new.svg) Gewährt die Kompatibilität mit Adobe Commerce 2.3.2.

## 1.0.0 für Adobe Commerce 2.3.1

![Neu](../assets/new.svg) Allgemeine Verfügbarkeitsversion


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
