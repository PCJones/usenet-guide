# Usenet Einsteiger Guide
Ein deutscher Guide für das Usenet. Wenn du Fragen, Probleme oder Verbesserungsvorschläge hast, erstelle gerne ein Issue oder einen Pull Request!

## Status des Guides
Der erste Teil des Guides ist fertig, was noch fehlt ist die Automatisierung mit Radarr & Sonarr - das wird in den nächsten Tagen folgen.

## Zuletzt aktualisiert: 06.09.2024 20:41

---

### Das Usenet verstehen

Das Usenet wurde ursprünglich in den 1980er Jahren als ein globales, verteiltes Diskussionsforum für Textnachrichten entwickelt. Heute wird es jedoch hauptsächlich zum Teilen von Dateien genutzt.

Filesharing im Usenet funktioniert durch das Hochladen von Dateien in "Newsgroups". Dabei wird die Datei in tausende kleine Dateien aufgesplittet, die dann als "Text" im Usenet gepostet werden. Sobald eine Datei hochgeladen ist, wird sie auf Usenet-Servern weltweit repliziert und kann von jedem, der Zugang zu diesen Servern hat, heruntergeladen werden.

---

### Wichtige Begriffe

- **Usenet-Provider**: Anbieter, die den Zugang zu Usenet-Servern ermöglichen. Die Speicherzeiträume variieren typischerweise zwischen 5 und 15+ Jahren.

- **Usenet-Indexer**: Sie sind Suchmaschinen für das Usenet. Da heutzutage fast alle Uploads verschlüsselt sind sind Indexer unerlässlich, da man ohne sie keine Dateien mehr finden kann.

- **NZB-Dateien**: Ein "Rezept" oder eine "Schatzkarte" für deinen Downloader. Sie informieren den Downloader, wie er die verschlüsselten, in tausende kleine Teile ("Postings") aufgesplittete Datei aus dem Usenet herunterladen und rekonstruieren kann.

---

### Tools

- **Downloader**: **SABnzbd** nimmt NZB-Dateien entgegen und lädt die eigentlichen Dateien herunter.

Diese Tools sind optional und werden in einem späteren Teil ausführlicher besprochen:

- **Automatisierung**: **Radarr** (für Filme), **Sonarr** (für Serien) und **Prowlarr** (Indexer-Management) können den Downloadprozess automatisieren.

- **Streaming**: Mit **Jellyfin** kannst du einen eigenen Streamingdienst betreiben.

- **Jellyseerr**: Mit **Jellyseerr** können in einer schönen Benutzeroberfläche Filme und Serien entdeckt sowie mit einem Klick automatisch angefragt werden.

---

### Vorbereitung

#### 1. **Usenet-Provider**:

   - **Für regelmäßige Nutzer**: **Ewaka** bietet Zugriff auf Uploads, die bis zu 15+ Jahre alt sind.  
Mit diesem [Aktionslink](https://www.eweka.nl/en/landing/best-usenet-promo) kostet es nur 3,99€/Monat. Wenn du erst einmal nur für einen Monat testen möchtest, besuche die [Ewaka-Startseite](https://www.eweka.nl/en).
Tipp: Am Black Friday und Koningsdag gibt es oft Angebote für nur 3€/Monat. Falls du bis dahin warten möchtest, könnte ein Block-Account (siehe unten) eine gute vorübergehende Lösung sein.

   - **Für gelegentliche Nutzer**: Ein Block-Account ermöglicht es dir, eine Datenmenge zu kaufen und diese ohne Zeitdruck zu verbrauchen. Bei **newsgroupdirect.com** bekommst du 2 TB für 16$ oder 4 TB für 25$. Siehe hier ganz unten: [Usenet-Angebote](https://newsgroupdirect.com/usenet-deals). Beachte, dass die Aufbewahrungszeit hier maximal 12 Jahre beträgt, aber Block-Accounts mit einer 15+-jährigen Vorhaltezeit kosten oft 5-10x mehr. Es sollte keinen großen Unterschied machen, aber es ist erwähnenswert. **Achtung**: Direkt nach dem Kauf werden euch eure Zugangsdaten angezeigt, an diese kommt ihr danach nicht mehr ran - also am besten direkt sichern!

   - **Hinweis: Da sich die Angebote der Provider sehr häufig ändern könnt ihr mich mich auch gerne anschreiben und nach den aktuell besten Deals fragen. [Kontakt & Support](#kontakt--support)**

#### 2. **Usenet-Indexer**:

Hinweis: Ich verlinke hier keinen Indexer, wenn ihr danach sucht sollten sie aber alle der erste Google-Treffer sein ;)

Für deutsche Produktionen, deutsche Vertonung sowie sogenannte "German DL" Releases (DL = Dual Language, also deutsche + originale Tonspur) gibt es eigentlich nur einen Usenet-Indexer: **SceneNZBs**.

Für Gelegenheitsnutzer lassen sich Indexer oftmals sogar komplett kostenlos nutzen. Wer jedoch viel oder sogar automatisiert downloaden möchte, kommt um eine jährliche Zahlung von 10-20€ nicht herum.

Hier meine Indexer-Empfehlung mit Ranking nach eigener Erfahrung. Zu Beginn reicht SceneNZBs völlig aus. Die anderen Indexer haben deutlich weniger deutschen Content, aber es gibt manchmal ältere Releases, die es (noch) nicht auf SceneNZBs gibt. Außerdem haben sie englischen Content oftmals früher und in mehr Varianten.

| Rank | Indexer       | Kostenlose Downloads/Tag | Premium pro Jahr       | Registrierung geöffnet | Löschung von kostenlosen Accounts bei Inaktivität | Weitere Info                                                                           |
|------|---------------|--------------------------|------------------------|------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------|
| 1.   | SceneNZBs | 5                       | 15-20€                 | Dauerhaft              | 1 Jahr                                            | Unverzichtbar für deutschen Content - dieser Indexer ist darauf spezialisiert                      |
| 2.   | NewzBay | 30 Tage Testzeitraum, dann 0       | 10€                    | Geschlossen, Invite aber leicht erhältlich       | 180 Tage                                            | Ein neuer, moderner Indexer, der auf deutschen Content spezialisiert ist. Sehr gut für Anime(Deutsche Synchro & Original mit Untertitel). Im Vergleich zu SceneNZBs fehlt allerdings noch ein größeres Archiv an älteren Sachen - dafür werden Anfragen nach fehlendem Content aber schnell erfüllt. Die perfekte Ergänzung zu SceneNZBs.  |
| 3.   | NZB.su   | ?                        | 15$                 | Dauerhaft | ?                                                  | Ebenfalls ein sehr guter Indexer, der auch viel an deutschem Content hat.
| 4.   | NzbGeek       | Einmalig 15 zum testen   | 12$                    | Dauerhaft              | -                                                 | Sehr gute Ergänzung zu SceneNZBs, da günstig, offene Registrierung und einiges an älterem deutschem Content vorhanden                          |
| 5.   | DrunkenSlug   | 5                        | 15-25€                 | Alle paar Monate | ?                                                  | Ebenfalls ein sehr guter Indexer, der auch einiges an deutschem Content hat, allerdings im Vergleich zu NzbGeek etwas teuer                    |
| 6.   | AnimeTosho    | ∞                        | 0€                     | Nicht nötig            | -                                                 | Kostenloser Indexer für Anime (allerdings wenig deutsches)                    

NzbGeek und DrunkenSlug haben eine wirklich sehr große Überschneidung, weshalb ihr davon eigentlich - wenn überhaupt - nur einen braucht.

**Kostenlose Alternative:**
Wer - bis auf den Usenet Provider - wirklich komplett kostenlos fahren möchte kann Alternativ auch auf so genannte Boards(Foren) zurückgreifen. Hier kann man nichts automatisieren und es sind ggf. ein paar mehr Klicks nötig, aber dafür sind die Boards komplett kostenlos. Es gibt im deutschen Raum ein bekanntes öffentliches Usenet-Board: house-of-usenet.com

#### 3. Downloader(Usenet-Client):

Es gibt zahlreiche Download-Clients für das Usenet, doch der unangefochtene Spitzenreiter ist **SABnzbd**. Dies hat mehrere Gründe:

- **Open Source**: Die Software ist transparent und kann von der Community weiterentwickelt und überprüft werden.
  
- **Kostenlos**: SABnzbd ist völlig kostenfrei nutzbar.
  
- **Vielseitigkeit**: Es funktioniert einwandfrei und ist verfügbar für Windows, MacOS und Linux.
  
- **(Für Profis)**: Da es eine Webanwendung ist lässt sich SABnzbd hervorragend als Docker-Container ausführen.

**Download**: [SABnzbd Download](https://sabnzbd.org/downloads)

**Installation**: Führe das Installationsprogramm aus und folge den Anweisungen.

---

**Erste Schritte mit SABnzbd**

Nach der Installation kannst du SABnzbd starten, indem du beispielsweise das Symbol auf deinem Desktop doppelklickst oder in der Suche danach suchst. Beim Starten öffnet sich dein Standardbrowser mit der Webanwendung von SABnzbd.

**Ersteinrichtung**:
| Bild | Anleitung |
|:----:|-----------|
| ![Assistent](https://github.com/PCJones/usenet-guide/blob/main/img/sabnzbd1.png?raw=true) | **Schritt 1:** Wähle als Sprache "Deutsch" und klicke dann auf "Assistenten starten". |
| ![Zugangsdaten eintragen](https://github.com/PCJones/usenet-guide/blob/main/img/sabnzbd2.png?raw=true) | **Schritt 2:** Hier gibst du die Zugangsdaten von Ewaka oder deinem Block-Account ein. Diese Informationen solltest du direkt nach dem Kauf bekommen haben und zudem per E-Mail. Stelle sicher, dass die SSL-Option aktiviert ist, damit alle Downloads verschlüsselt sind. Dies macht einen VPN oder ähnliches überflüssig. |
| ![Dritter Schritt](https://github.com/PCJones/usenet-guide/blob/main/img/sabnzbd3.png?raw=true) | **Schritt 3:** Der Assistent empfiehlt, das Webinterface von SABnzbd (`http://127.0.0.1:8080/sabnzbd/`) als Lesezeichen im Browser zu speichern. Dies ist nützlich, wenn SABnzbd bereits im Hintergrund läuft. Alternativ kannst du SABnzbd aber auch über das Desktop-Symbol oder die Programmsuche starten. Eventuell möchtest du die Pfade für den temporären Ordner und den Download-Ordner anpassen, was hier ebenfalls möglich ist. Am Ende musst du nur noch auf "SABnzbd anzeigen" klicken. |
| ![SABnzbd Oberfläche](https://github.com/PCJones/usenet-guide/blob/main/img/sabnzbd4.png?raw=true) | Du siehst nun die SABnzbd Oberfläche - das war's mit der Konfiguration für den Anfang! Es empfiehlt sich, bei Gelegenheit die Einstellungen von SABnzbd zu durchstöbern und sich mit den Optionen vertraut zu machen. Aber für den Anfang bist du jetzt bereit, Downloads zu starten. |

---

### Downloaden

Wenn du es bis hier geschafft hast, dann hast du den schwierigsten Teil geschafft. Ab jetzt wird es wirklich einfach! Alle von mir erwähnten Indexer sehen mehr oder weniger gleich aus, weshalb du keine großen Schwierigkeiten haben solltest, falls du verschiedene nutzt.

| Bild | Beschreibung |
|------|--------------|
| ![Einloggen bei Indexer](https://github.com/PCJones/usenet-guide/blob/main/img/indexer1.png?raw=true) | 1. Einloggen bei Indexer (z.B. SceneNZBs) |
| ![Suche](https://github.com/PCJones/usenet-guide/blob/main/img/indexer2.png?raw=true) | 2. Oben rechts in der Suche können wir nach etwas suchen, also zum Beispiel Filme oder Serien. |
| ![Suchergebnisse](https://github.com/PCJones/usenet-guide/blob/main/img/indexer3.png?raw=true) | 3. In meinem Fall habe ich nach Tatort gesucht und finde dementsprechend alle Möglichen Tatort-Filme. Sucht ihr nach bestimmten Folgen, z.B. Staffel 2 Folge 8 so ist das Suchformat immer "Serienname S02E08". Ihr findet hier auch wichtige Informationen wie die Dateigröße. das Upload-Datum und im Titel auch noch vieles weiteres, wie z.B. die Ursprungsquelle (Blu-Ray, WEB, DVD, etc) oder die Qualität (720p, 1080p, 4k, etc). Worauf genau ihr da achten könnt & solltet erkläre ich später noch genauer. |
| ![View Series](https://github.com/PCJones/usenet-guide/blob/main/img/indexer4.png?raw=true) | 4. Tipp: Bei Filmreihen und insbesondere Serien gibt es bei den meisten Indexern einen Button wie View Series, mit der man eine geordnete Übersicht über alle verfügbaren Staffeln, Folgen & verfügbare Releases hat. |
| ![Download oder Warenkorb](https://github.com/PCJones/usenet-guide/blob/main/img/indexer5.png?raw=true) | 5. Haben wir uns für ein Release entschieden, so haben wir bei den meisten Indexern zwei Möglichkeiten - Entweder downloaden wir die NZB-Datei direkt, oder wir fügen sie in unseren "Warenkorb" hinzu. Das ist nützlich, falls wir viele Dateien downloaden möchten. Falls ihr die Releases in den Warenkorb packt, so findet ihr unter Profile->My Cart (oder in der Nähe, je nach Indexer) alle hinzugefügten Downloads. Die könnt ihr dann mit einem Klick allesamt markieren um sie als .zip Datei gebündelt herunterzuladen - so erspart ihr euch dutzende einzelne .nzb Dateien. Ihr müsst die .zip Datei auch nicht entpacken, das macht SABnzbd automatisch für euch. |
| ![Heruntergeladene Datei](https://github.com/PCJones/usenet-guide/blob/main/img/downloadfolder1.png?raw=true) | 6. Ich habe jetzt eine .nzb Datei gedownloaded, es können aber auch mehrere sein (und wie erwähnt auch .zip Dateien die mehrere .nzbs beinhalten)
| ![SABnzbd Import](https://github.com/PCJones/usenet-guide/blob/main/img/sabnzbd4.png?raw=true) | 7. Nun gehen wir zu SABnzbd und ziehen die Dateien entweder per Drag&Drop herein oder klicken auf den großen "NZB hinzufügen" Button. |
| ![Downloadvorgang](https://github.com/PCJones/usenet-guide/blob/main/img/sabnzbd5.png?raw=true) | 8. SABnzbd startet den Download automatisch. Sobald dieser abgeschlossen und entpackt ist, findet man den Inhalt im festgelegten Download-Ordner. Das wars! :) |

---

### Wichtige Begriffe im Releasenamen

Der Releasename (also z.B. sowas wie "Game of Thrones S01E01 German EAC3 DL 1080p BluRay x265-VECTOR") liefert euch einige wichtige Infos.

Ganz am Ende hinter dem Bindestrich seht ihr immer die Releasegroup, also die Gruppe die den Film oder die Folge tatsächlich von einer BluRay gerippt oder von einem Streamingdienst heruntergeladen hat. Das kann für manche interessant sein, könnt ihr aber erstmal vernachlässigen.

| Begriff            | Erklärung                                                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| x264, h264         | Codec für Videokompression. Er erzeugt Dateien, die im Vergleich zu x265 größer sind, bietet jedoch eine bessere Kompatibilität mit älteren Geräten. Für 720p und 1080p und hohe Qualitätsansprüche empfohlen. |
| x265, h265, HEVC   | High Efficiency Video Coding (HEVC), oft als h.265 oder x265 bezeichnet, ist ein modernerer Codec, der Videos mit etwa halber Dateigröße von h.264, aber mit gleicher Qualität komprimiert. Ideal für 4K Videos oder wenn Speicherplatz begrenzt ist.    |
| 720p, 1080p, 2160p | Qualität des Releases. 720p = HD, 1080p = Full HD, 2160p = 4K Ultra HD.                                                                                                                                                                                 |
| German             | Das Release verfügt über eine deutsche Tonspur.                                                                                                                                                                                                         |
| German DL          | Dual Language - Das Release ist zweisprachig, in der Regel Deutsch und Originalsprache. Das DL kann auch später im Dateinamen auftreten, z.B. "German EAC3 DL".                                                                                         |
| WEB-DL             | Die Quelle stammt aus dem Internet, meist von Streamingdiensten. Nicht zu verwechseln mit "German DL". Bei deutschen Releases meist nur als "WEB" oder "WebHD" bezeichnet.                                                                                            |
| WEBRip             | Auch von einem Streamingdienst, jedoch oft (nicht immer) mit niedrigerer Bitrate als WEB-DL.                                                                                                                                                            |
| BluRay, Blu-Ray    | BluRay-RIP. Bessere Qualität als WEB-DL
| Remux              | Unveränderter, originaler BluRay-Rip. Es wurden nur ggf. nicht gewünschte Sprachen sowie Menüs entfernt. Bestmögliche Qualität.
| MD, MIC DUBBED, MIC| Tonspur wurde im Kino aufgezeichnet. Oft schlechte Audioqualität mit Störgeräuschen. Meine Empfehlung: Nach einem besseren Release suchen bzw. darauf warten :-)
| REPACK, PROPER     | Diese Releases sind Überarbeitungen oder Korrekturen eines vorherigen Releases. Ein REPACK oder PROPER sollte einem ansonsten exakt gleichnamigen Release ohne diese Kennzeichnung bevorzugt werden.                                                |

### Probleme und Fragen

---

- Mein SABnzbd erreicht nicht die volle Downloadgeschwindigkeit.

  - **Ursachen überprüfen:** Mache einen Geschwindigkeitstest auf einer Seite wie [Speedtest](https://speedtest.net). In der Regel solltest du in SABnzbd mindestens 80-90% der Geschwindigkeit erreichen, die du im Speedtest siehst. Achtung: speedtest.net zeigt die Geschwindigkeit in Megabit, SABnzbd in Megabyte. Hier kannst du umrechnen: https://www.gbmb.org/mbit-to-mb
Falls du eine sehr alte oder langsame Festplatte verwendest, könnte dies ebenfalls der Flaschenhals sein.

  - **Download testen:** Du kannst die Geschwindigkeit entweder mit herkömmlichen NZBs testen oder spezielle Testdownloads in SABnzbd verwenden. Klicke dazu oben rechts auf den Schraubenschlüssel und starte einen Testdownload (100 MB, 1 GB oder 10 GB). Beachte bei Block-Accounts dass die Testdownloads zum verbrauchten Datenvolumen zählen.

  - **Verbindungen anpassen:** Wenn die Geschwindigkeit nicht optimal ist, gehe zu den Servereinstellungen in SABnzbd. Klicke dazu oben rechts auf das Zahnrad, dann auf "Server" und dort bei deinem Server auf "Details anzeigen". Unter "Verbindungen" siehst du eine Zahl, wahrscheinlich "8". Es ist eine Frage des Ausprobierens, um die optimale Anzahl von Verbindungen herauszufinden. Ewaka erlaubt bis zu 50 Verbindungen, mehr als 40 sollte man aber nie verwenden. Ein guter Startwert könnte 20 sein. Dann kannst du die Anzahl der Verbindungen schrittweise erhöhen oder verringern und jeweils die Geschwindigkeit testen - wichtig: auch zu viele Verbindungen können ein Problem sein!

### Automatisierung mit Radarr, Sonarr & Prowlarr

---

Wie genau man Radarr, Sonarr & co einrichtet werde ich in den nächsten Tagen hinzufügen.
Wer sich jetzt schon ranwagen möchte, hier ein paar Links & Infos:
1. Ganz wichtig: Sonarr v4 Beta nutzen, nicht die Version 3. Version 3 wird bald eingestellt und es ändert sich einiges, es wäre ärgerlich wenn ihr dann alles neu konfigurieren müsst. Die Beta läuft auch sehr stabil und löst bald v3 endgültig ab.
2. Hier scheint es ein ganz vernünftiges Englisches Tutorial zu geben: https://www.rapidseedbox.com/blog/ultimate-guide-to-sonarr
Statt Schritt 5. (Torrent-Client) fügt ihr einen Newznab Usenet-Downloader hinzu, die API Keys findet ihr beim Indexer in eurem Profil - dafür braucht ihr aber wie erwähnt dann Premium.
3. Zur weiteren Optimierung empfehlen sich die TraSH-Guides für Radarr & Sonarr: https://trash-guides.info/ **Achtung**: Bei Sonarr nur den v4 Beta Reiter beachteten
4. Falls German DL (Deutsch+Original) Releases bevorzugt werden sollen habe ich dafür einen Guide geschrieben: https://github.com/PCJones/radarr-sonarr-german-dual-language

## Kontakt & Support
- Öffne gerne ein Issue auf GitHub falls du Unterstützung benötigst.
- [Telegram](https://t.me/pc_jones)
- Discord: pcjones1 - oder komm in den UsenetDE Discord Server: [https://discord.gg/pZrrMcJMQM](https://discord.gg/pZrrMcJMQM)

## Spenden
Über eine Spende freue ich mich natürlich immer :D
PayPal: https://paypal.me/pcjones1

Für andere Spendenmöglichkeiten gerne auf Discord oder Telegram melden - danke!

## Changelog:
| Datum         | Änderung                                                                                                      |
|--------------|----------------------------------------------------------------------------------------------------------------|
| 2024-09-06 | SceneNZBs Free Downloads/Tag 10->5, NinjaCentral aus Empfehlungen entfernt (bei deutschen Releases gab es über einen längeren Zeitraum leider häufiger XXX statt dem richtigen Inhalt - das geht gar nicht), NewzBay hinzugefügt  |
