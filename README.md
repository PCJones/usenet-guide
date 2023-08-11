# Usenet Einsteiger Guide
Ein deutscher Guide für das Usenet

## WORK IN PROGRESS 
## Zuletzt aktualisiert: 11.08.20203 16:45

---

### Das Usenet verstehen

Das Usenet, ursprünglich in den 1980er Jahren als globales Diskussionsforum für Textnachrichten entwickelt, dient heute vorwiegend dem Filesharing.

- **Filesharing**: Dateien werden in "Newsgroups" hochgeladen. Einmal hochgeladen, werden sie weltweit auf Usenet-Servern repliziert.

---

### Wichtige Begriffe

- **Usenet-Provider**: Anbieter, die den Zugang zu Usenet-Servern ermöglichen. Die Speicherzeiträume variieren typischerweise zwischen 5 und 15+ Jahren.

- **Usenet-Indexer**: Sie sind Suchmaschinen für das Usenet. Da heutzutage fast alle Uploads verschlüsselt sind sind Indexer unerlässlich, da man ohne sie keine Dateien mehr finden kann.

- **NZB-Dateien**: Ein "Rezept" oder eine "Schatzakrte" für deinen Downloader. Sie informieren den Downloader, wie er die in tausende verschlüsselte kleine Teile ("Postings") aufgesplittete Datei aus dem Usenet herunterladen und rekonstruieren kann.

---

### Tools

- **Downloader**: **SABnzbd** nimmt NZB-Dateien entgegen und lädt die eigentlichen Dateien herunter.

Diese Tools sind optional und werden in einem späteren Teil ausführlicher besprochen:

- **Automatisierung**: **Radarr** (für Filme), **Sonarr** (für Serien) und **Prowlarr** (Indexer-Management) können den Downloadprozess automatisieren.

- **Streaming**: Mit **Jellyfin** kannst du einen eigenen Streamingdienst betreiben.

- **Jellyseerr**: Mit **Jellyseerr** können in einer schönen Benutzeroberfläche Filme und Serien entdeckt sowie mit einem Klick automatisch angefragt werden.

---

### Vorbereitung

1. **Usenet-Provider**:

   - **Für regelmäßige Nutzer**: **Ewaka** bietet Zugriff auf Uploads, die bis zu 15+ Jahre alt sind.  
Mit diesem [Aktionslink](https://www.eweka.nl/en/landing/special-deal) kostet es nur 4€/Monat. Wenn du erst einmal nur für einen Monat testen möchtest, besuche die [Ewaka-Startseite](https://www.eweka.nl/en).
Tipp: Am Black Friday und Koningsdag gibt es oft Angebote für nur 3€/Monat. Falls du bis dahin warten möchtest, könnte ein Block-Account (siehe unten) eine gute vorübergehende Lösung sein.

   - **Für gelegentliche Nutzer**: Ein Block-Account ermöglicht es dir, eine Datenmenge zu kaufen und diese ohne Zeitdruck zu verbrauchen. Bei **newsgroupdirect.com** bekommst du 2 TB für 16$ oder 4 TB für 25$. Siehe hier ganz unten: [Usenet-Angebote](https://newsgroupdirect.com/usenet-deals). Beachte, dass die Aufbewahrungszeit hier maximal 12 Jahre beträgt, aber Block-Accounts mit einer 15+-jährigen Vorhaltezeit kosten oft 5-10x mehr. Es sollte keinen großen Unterschied machen, aber es ist erwähnenswert.

2. **Usenet-Indexer**:

Für deutsche Produktionen, deutsche Vertonung sowie sogenannte "German DL" Releases (DL = Dual Language, also deutsche + originale Tonspur) gibt es eigentlich nur einen Usenet-Indexer: **sceneNZBs.com**.

Für Gelegenheitsnutzer lassen sich Indexer oftmals sogar komplett kostenlos nutzen. Wer jedoch viel oder sogar automatisiert downloaden möchte, kommt um eine monatliche Zahlung von 15-25€ nicht herum.

Hier meine Indexer-Empfehlung mit Ranking nach eigener Erfahrung. Zu Beginn reicht sceneNZBs.com völlig aus. Die anderen Indexer haben deutlich weniger deutschen Content, aber es gibt manchmal ältere Releases, die es (noch) nicht auf sceneNZBs.com gibt. Außerdem haben sie englischen Content oftmals früher und in mehr Varianten.

| Rank | Indexer       | Kostenlose Downloads/Tag | Premium pro Jahr       | Registrierung geöffnet | Löschung von kostenlosen Accounts bei Inaktivität | Weitere Info                                                                           |
|------|---------------|--------------------------|------------------------|------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------|
| 1.   | SceneNZBs.com | 10                       | 15-20€                 | Dauerhaft              | 1 Jahr                                            | Unverzichtbar für deutschen Content                                                  |
| 2.   | Ninja Central | 5                        | 12€                    | Alle paar Monate       | 7 Tage                                            | Kostenlose Accounts werden schnell gesperrt, aber Premium ist es auf jeden Fall Wert - dieser Indexer hat oft Sachen, die es kaum woanders gibt  |
| 3.   | NzbGeek       | Einmalig 15 zum testen   | 12$                    | Dauerhaft              | -                                                 | Sehr gute Ergänzung zu SceneNZBs, da günstig, offene Registrierung und einiges an älterem deutschem Content vorhanden                          |
| 4.   | DrunkenSlug   | 5                        | 15-25€                 | Alle paar Monate (**11.08.2023: gerade offen!**)  | ?                                                  | Ebenfalls ein sehr guter Indexer, der auch einiges an deutschem Content hat, allerdings im Vergleich zu NzbGeek recht teuer                    |
| 5.   | AnimeTosho    | ∞                        | 0€                     | Nicht nötig            | -                                                 | Kostenloser Indexer für Anime                    
---

## Ich arbeite gerade noch an dem Guide und er wird alle paar Minuten aktualisiert.


## Kontakt & Support
- Öffne gerne ein Issue auf GitHub falls du Unterstützung benötigst.
- [Telegram](https://t.me/pc_jones)
- Discord: pcjones1
