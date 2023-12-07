---
title: Store-URLs
description: Erfahren Sie mehr über Store-URLs und wie Sie die Basis-URL und Store-Codes konfigurieren.
exl-id: dd7a6317-b0cf-4d0c-9b31-a963c467026b
feature: Site Management, System
source-git-commit: 555c54e9a980aa181e0b4380412ad027d80ee10f
workflow-type: tm+mt
source-wordcount: '1512'
ht-degree: 0%

---

# Store-URLs

Jede Website in einer Adobe Commerce- oder Magento Open Source-Installation verfügt über eine Basis-URL, die der Storefront zugewiesen ist, und eine andere URL, die dem Administrator zugewiesen ist. Adobe verwendet Variablen, um interne Links im Verhältnis zur Basis-URL zu definieren, wodurch ein gesamter Speicher von einem Speicherort zum anderen verschoben werden kann, ohne die Links zu aktualisieren. Standard-Basis-URLs beginnen mit `http`, und sichere Basis-URLs beginnen mit `https`.

- **Basis-URL** — `http://www.yourdomain.com/magento/`
- **Sichere Basis-URL** — `https://www.yourdomain.com/magento/`
- **URL mit IP-Adresse** — `http://###.###.###.###/magento/` oder `https://###.###.###.###/magento/`

>[!IMPORTANT]
>
>Ändern Sie die Admin-URL nicht von der standardmäßigen Basis-URL-Konfiguration. Informationen zum Ändern der Admin-URL oder des Pfads finden Sie unter [Verwenden einer benutzerdefinierten Admin-URL](#use-a-custom-admin-url).

## Verwenden eines sicheren Protokolls

Die Basis-URLs für Ihren Store wurden während der Adobe Commerce-Installation eingerichtet. Wenn damals ein Sicherheitszertifikat verfügbar war, können Sie `HTTPS` URLs, die für den Store, Admin oder beides verwendet werden sollen. Wenn Ihre Adobe Commerce-Installation mehrere Stores umfasst oder Sie später weitere Stores hinzufügen möchten, können Sie den Store-Code in die URL aufnehmen. Alle Adobe-Ressourcen und -Vorgänge können mit dem sicheren Protokoll verwendet werden.

Wenn zum Zeitpunkt der Installation für die Domäne kein Sicherheitszertifikat verfügbar war, müssen Sie die Konfiguration aktualisieren, bevor Sie den Store starten. Nachdem ein Sicherheitszertifikat für Ihre Domäne eingerichtet wurde, können Sie eine oder beide Basis-URLs für den Betrieb mit verschlüsselter Secure Sockets Layer (SSL) konfigurieren und [Transport Layer Security][1] (TLS).

>[!IMPORTANT]
>
>Adobe empfiehlt dringend, alle Seiten einer Produktions-Site, einschließlich Inhalts- und Produktseiten, mit einem sicheren Protokoll zu übertragen.

Adobe Commerce und Magento Open Source können so konfiguriert werden, dass alle Seiten über `HTTPS` Standardmäßig. Wenn Ihr Store mit dem Standardprotokoll ausgeführt wird, können Sie die Sicherheit verbessern, indem Sie [Strenge HTTP-Transportsicherheit][2] (HSTS) und ein Upgrade aller unsicheren Seitenanfragen durchführen. HSTS ist ein Opt-in-Protokoll, das verhindert, dass Browser den Standard rendern `HTTP` Seiten, die mit unsicherem Protokoll für die angegebene Domäne übertragen werden. Da Suchmaschinen möglicherweise bereits jede Seite Ihres Stores mit dem Standard indiziert haben `HTTP` URLs, können Sie Commerce so konfigurieren, dass alle unsicheren Seitenanfragen auf aktualisiert werden `HTTPS` automatisch, sodass Sie keinen Traffic verlieren. Wenn Commerce für die Verwendung sicherer URLs für Storefront und Admin konfiguriert ist, werden zwei zusätzliche Felder angezeigt, mit denen Sie Folgendes aktivieren können: `HSTS`.

## Basis-URL konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. under _Allgemein_ Wählen Sie im linken Bereich **[!UICONTROL Web]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Base URL]** Abschnitt.

   - **[!UICONTROL Base URL]** — Geben Sie die vollständig qualifizierte Basis-URL für Ihren Store ein. Stellen Sie sicher, dass Sie die URL mit einem Schrägstrich enden, damit sie mit zusätzlichen URL-Schlüsseln aus Ihrem Store erweitert werden kann. Beispiel: `http://yourdomain.com/`

     >[!NOTE]
     >
     >Ändern Sie den Platzhalter im _[!UICONTROL Base Link URL]_-Feld. Es ist ein Platzhalter, der zum Erstellen relativer Links zur Basis-URL verwendet wird.

   - **[!UICONTROL Base URL for Static View Files]** — (Optional) Geben Sie einen alternativen Speicherort für die Basis-URL für statische Ansichtsdateien an, indem Sie den Pfad eingeben, der mit dem folgenden Platzhalter beginnt:

     \{\{unsecure_base_url}}

   - **[!UICONTROL Base URL for User Media Files]** — (Optional) Geben Sie einen alternativen Speicherort für die Basis-URL für Benutzermediendateien an, indem Sie den Pfad eingeben, der mit dem folgenden Platzhalter beginnt:

     \{\{unsecure_base_url}}

     Bei einer typischen Installation müssen die Pfade für statische Ansichtsdateien oder Mediendateien nicht aktualisiert werden, da sie relativ zur Basis-URL sind.

   ![Allgemeine Konfiguration - Web-Basis-URLs](../configuration-reference/general/assets/web-base-urls.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Platzhalter, die in doppelte Klammern eingeschlossen sind, sind Markup-Tags für Variablen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Sichere Basis-URL konfigurieren

Wenn Ihre Domäne über ein gültiges Sicherheitszertifikat verfügt, können Sie die URLs der Storefront und des Administrators so konfigurieren, dass Daten über einen sicheren (HTTPS-)Kanal übertragen werden. Ohne ein gültiges Sicherheitszertifikat kann Ihr Store nicht mit dem sicheren (SSL/TLS) Protokoll funktionieren.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die _[!UICONTROL Base URLs (Secure])_ und führen Sie folgende Schritte aus:

   ![Allgemeine Konfiguration - sichere Basis-URLs](../configuration-reference/general/assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - **[!UICONTROL Secure Base URL]** — Geben Sie die vollständige sichere Basis-URL ein, gefolgt von einem Schrägstrich. Beispiel: `https://yourdomain.com/`

   - **[!UICONTROL Secure Base Link URL]** — Ändern Sie den Platzhalter nicht im Feld &quot;Sichere Basis-Link-URL&quot;. Sie wird verwendet, um relative Links zur sicheren Basis-URL zu erstellen.

   - **[!UICONTROL Secure Base URL for Static View Files]** — (Optional) Geben Sie einen alternativen Speicherort für die sichere Basis-URL für statische Ansichtsdateien an, indem Sie den Pfad eingeben, der mit dem folgenden Platzhalter beginnt:

     \{\{secure_base_url}}

   - **[!UICONTROL Secure Base URL for User Media Files]** — (Optional) Geben Sie einen alternativen Speicherort für die sichere Basis-URL für Benutzermediendateien an, indem Sie den Pfad eingeben, der mit dem folgenden Platzhalter beginnt:

     \{\{secure_base_url}}

1. Um die Sicherheit zu erhöhen, setzen Sie die beiden folgenden Optionen auf `Yes`.

   - **[!UICONTROL Use Secure URLs on Storefront]**
   - **[!UICONTROL Use Secure URLs in Admin]**

1. Für _[!UICONTROL Enhanced Security Settings]_führen Sie folgende Schritte aus:

   - **[!UICONTROL Enable HTTP Strict Transport Security (HSTS)]** — Wenn Ihr Store nur sichere HTTPS-Seitenanforderungen anzeigen soll, setzen Sie auf `Yes`.

   - **[!UICONTROL Upgrade Insecure Requests]** — Um alle Anforderungen für standardmäßige ungesicherte HTTP-Seiten auf HTTPS zu aktualisieren, setzen Sie auf `Yes`.

1. Legen Sie die **[!UICONTROL Offloader Header]** für Ihren Server.

   Die meisten Commerce-Installationen verwenden den Standard `X-Forward-Proto` zur Identifizierung des Protokolls als `HTTP` oder `HTTPS`. Wenn Ihre Serverkonfiguration einen anderen offloader_header verwendet, geben Sie ihn hier ein.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Speichern Sie den Code in URLs.

>[!NOTE]
>
>Wenn die Variable _Hinzufügen von Store-Code zu URLs_ ist auf `Yes`müssen Sie Store-Codes in Ihre Browser-URLs aufnehmen. Diese Einstellung stellt sicher, dass URL-Neuschreibungen korrekt zugeordnet werden und alle Seiten erfolgreich geöffnet werden, ohne _&quot;404 Seite nicht gefunden&quot;_ Fehler.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. under _[!UICONTROL General]_Wählen Sie im linken Bereich **[!UICONTROL Web]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL URL Options]** Abschnitt.

1. Satz **[!UICONTROL Add Store Code]** nach Ihren Wünschen:

   - **[!UICONTROL URL with Store Code]**: `http://www.yourdomain.com/magento/[store-code]/index.php/url-identifier`
   - **[!UICONTROL URL without Store Code]**: `http://www.yourdomain.com/magento/index.php/url-identifier`

   ![Allgemeine Konfiguration - Web-URL-Optionen](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

1. Klicken Sie auf **[!UICONTROL Cache Management]** in der Nachricht am oberen Rand des Arbeitsbereichs. Befolgen Sie dann die Anweisungen zum Aktualisieren des Caches.

   ![Cache-Management-Nachricht](./assets/msg-cache-management.png)

## Fehlerbehebung bei URLs

Wenn nach Befolgen der Konfigurationsanweisungen einige Seiten weiterhin mit der unsicheren URL (`http://`), führen Sie die folgenden Schritte aus:

- Ändern Sie die (unsichere) Basis-URL in die sichere HTTPS-URL.
- Bearbeiten Sie auf dem Server die `.htaccess` Datei (oder Lastenausgleich), sodass die unsichere URL an die sichere URL umgeleitet wird.

## Verwenden einer benutzerdefinierten Admin-URL

Als [Best Practices für die Sicherheit](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html)empfiehlt Adobe, dass Sie eine eindeutige Admin-URL anstelle der standardmäßigen _admin_ oder einen gemeinsamen Begriff wie _Backend_. Obwohl Ihre Site nicht direkt vor einem bestimmten fehlerhaften Schauspieler geschützt wird, kann dies die Exposition gegenüber Skripten verringern, die versuchen, unberechtigten Zugriff zu erhalten.

>[!NOTE]
>
>Wenden Sie sich an Ihren Hosting-Provider, bevor Sie eine benutzerdefinierte Admin-URL implementieren. Einige Hosting-Provider benötigen eine Standard-URL, um die Firewall-Schutzregeln zu erfüllen.

In einer typischen Installation folgen die Admin-URL und der Pfad sofort der Basis-URL. Der Admin-Pfad ist ein Ordner unter dem Stammverzeichnis.

- **Standard-Basis-URL**: `http://yourdomain.com/magento/`
- **Standard-Administratorpfad**: `admin`
- **Standard-Admin-URL und -Pfad**: `http://yourdomain.com/magento/admin`

Obwohl es möglich ist, die Admin-URL und den Pfad zu einem anderen Speicherort zu ändern, entfernt jeder Fehler den Zugriff auf den Admin und muss vom Server korrigiert werden.

>[!NOTE]
>
>Versuchen Sie als Vorsichtsmaßnahme nicht, die Admin-URL selbst zu ändern, es sei denn, Sie wissen, wie Sie Konfigurationsdateien auf dem Server bearbeiten können. Ändern Sie bei in der Cloud-Infrastruktur bereitgestellten Adobe Commerce-Projekten die Admin-URL wie folgt: [instructions](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html?lang=en#admin-url) im *Handbuch zu Adobe Commerce on Cloud Infrastructure*.

### Methode 1: Änderung gegenüber dem Administrator

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL Admin]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Admin Base URL]** Abschnitt.

1. Legen Sie die Konfigurationsoptionen für die benutzerdefinierte URL fest:

   ![Erweiterte Konfiguration - Admin-Basis-URL](../configuration-reference/advanced/assets/admin-admin-base-url.png){width="600" zoomable="yes"}

   Falls erforderlich, löschen Sie die **[!UICONTROL Use system value]** zum Ändern der Einstellung.

   - Satz **[!UICONTROL Use Custom Admin URL]** nach `Yes`.

   - Geben Sie die **[!UICONTROL Custom Admin URL]**: `http://yourdomain.com/magento/`

     >[!NOTE]
     >
     >Die Admin-URL muss sich in derselben Commerce-Installation befinden und denselben Dokumentenstamm wie die Storefront aufweisen.

   - Satz **[!UICONTROL Custom Admin Path]** nach `Yes`.

   - Für **[!UICONTROL Custom Admin Path]** Geben Sie den Pfad ein, der als benutzerdefinierter Admin-Ordnername verwendet werden soll.

     Beispiel: `sample_custom_admin`

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

1. Nachdem die Änderungen gespeichert wurden, melden Sie sich beim Administrator ab und melden Sie sich mit der neuen Admin-URL und dem neuen Pfad wieder an.

### Methode 2: Ändern Sie den Administratorpfad über die Server-Befehlszeile.

1. Öffnen Sie die `app/etc/env.php` in einem Texteditor und ändern Sie den Wert der `frontName` Parameter der `backend` Abschnitt. Speichern Sie dann die Datei.

   Verwenden Sie nur Kleinbuchstaben.

   >[!NOTE]
   >
   >   Mit dieser Methode können Sie den Admin-Pfad ändern, nicht aber die Admin-URL.

   >[!TIP]
   >
   >Für Adobe Commerce in der Cloud-Infrastruktur können Sie einen benutzerdefinierten Administratorpfad mithilfe der `ADMIN_URL` in der Cloud-Benutzeroberfläche. Siehe [Admin-Variablen-Thema](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html) im _Benutzerhandbuch zu Commerce on Cloud Infrastructure_.

   - **Standard-Administratorpfad**

     ```php?start_inline=1
     'backend' => [
      'frontName' => 'admin'
     ],
     ```

   - **Neuer Administratorpfad**

     ```php?start_inline=1
     'backend' => [
         'frontName' => 'backend'
     ],
     ```

1. Verwenden Sie eine der folgenden Methoden, um den Cache zu löschen:

   - Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**. Klicken Sie anschließend auf **[!UICONTROL Flush Magento Cache]**.
   - Führen Sie auf dem Server Folgendes aus:

     ```terminal
     php bin/magento cache:flush
     ```

   >[!NOTE]
   >
   >Die mit der Methode 1 vorgenommenen Änderungen haben Vorrang vor den Änderungen, die in der Variablen `app/etc/env.php` -Datei.

### Methode 3: Ändern des Admin-Pfads mithilfe der Commerce-CLI

Sie können die CLI verwenden `setup:config:set` -Befehl zum Ändern des Admin-Pfads. Im folgenden Beispiel wird die `--backend-frontname` Option zum Ändern des Pfads vom Commerce-Stamm in einen neuen Admin-Pfad:

```terminal
bin/magento setup:config:set --backend-frontname="backend_front_name"
```

Dieser Befehl aktualisiert die `backend` > `frontName` Konfigurationsoption in der `app/etc/env.php` -Datei.

## Standardmäßige Admin-URL und Administratorpfad wiederherstellen

Wenn Sie eine ungültige Admin-URL oder einen Admin-Pfad festgelegt und den Zugriff auf das Backend verloren haben, können Sie dies über die Befehlszeile beheben.

1. Führen Sie folgenden Befehl aus, um zur Standard-Admin-URL zurückzukehren:

   ```terminal
   php bin/magento config:set admin/url/use_custom 0
   ```

1. So kehren Sie zum standardmäßigen Administratorpfad zurück (festgelegt im `app/etc/env.php` wie in Methode 2 beschrieben), führen Sie diesen Befehl aus:

   ```terminal
   php bin/magento config:set admin/url/use_custom_path 0
   ```

1. Verwenden Sie eine der folgenden Methoden, um den Cache zu löschen:

   - Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**. Klicken Sie anschließend auf **[!UICONTROL Flush Magento Cache]**.
   - Führen Sie auf dem Server Folgendes aus:

     ```terminal
     php bin/magento cache:flush
     ```


[1]: https://en.wikipedia.org/wiki/Transport_Layer_Security
[2]: https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
