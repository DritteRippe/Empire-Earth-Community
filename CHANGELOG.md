# Changelog

Hier stehen alle Änderungen an diesem Paket, die neueste Version zuerst.

Das Format folgt [Keep a Changelog](https://keepachangelog.com/de/1.1.0/), die Versionsnummern folgen [Semantic Versioning](https://semver.org/lang/de/). Jede Version ist ein Tag `vX.Y.Z` auf `main` mit einem GitHub-Release. Ab 1.1.0 liegt das Paket in diesem Release als eine ZIP-Datei unter „Assets“. Ältere Versionen bleiben über ihren Tag erreichbar, die Historie wird nicht umgeschrieben. Wie du eine ältere Version herunterlädst, steht in der [README](README.md#versionen).

## [Unreleased]

### Hinzugefügt

- **Fehler melden:** Ein Formular für Issues in diesem Repository fragt nach der Version des Pakets, nach Windows, nach dem Spiel und dem Spielmodus, nach dem, was passiert ist, und nach den Protokollen. Fragen zum Code gehen über die Auswahl direkt zum Repository des Setups oder des Launchers.
- **Sicherheit:** `SECURITY.md` erklärt, wie du eine Sicherheitslücke privat meldest (über „Private vulnerability reporting“ von GitHub) und wie du die Echtheit des Pakets prüfst.
- **Mitmachen:** `CONTRIBUTING.md` erklärt, wie du Fehler meldest und die Anleitung verbesserst, wo der Code liegt und wie ein Release entsteht.

### Geändert

- **Lizenzen:** Der Ordner `Lizenzen/` im Repository ist die Vorlage für das nächste Paket und hat jetzt den Stand der Repositorys des Launchers und des Setups: `THIRD-PARTY-NOTICES.md` nennt ZipStorer 3.7.0 mit seinen lokalen Korrekturen, `THIRD-PARTY-NOTICES-Setup.md` zusätzlich BASS und die anderen mitgelieferten Programmdateien der Spiel-Setups, und `licenses/THIRD-PARTY-LICENSES.txt` nennt das Repository DritteRippe/Empire-Earth-Launcher als Quelle. Die Fassung aus der ZIP-Datei von 1.1.0 bleibt beim Tag `v1.1.0`.

### Behoben

- `Lizenzen/Quellcode.txt` nannte als Stand des Quellcodes den Branch `v2`, den es nicht mehr gibt. Jetzt nennt die Datei die Tags `suite-v1.1.0` und `v1.1.0` mit ihren Commits und Links. Die Commits selbst sind unverändert.
- Der Link in `Lizenzen/THIRD-PARTY-NOTICES.md` auf die Hinweise des Setups zeigte auf eine Seite, die es nicht gibt. Er führt jetzt zu DritteRippe/Empire-Earth-Setup.

### Geplant

Für spätere Versionen ist geplant (ohne festes Datum):

- Discord-Status: Discord zeigt an, was du gerade spielst.
- Grafik-Einstellungen, die Werte ändern: Wrapper, Anzeigemodus und Auflösung einstellen. Die Seite „Grafik“ in 1.1.0 zeigt die Werte nur an, und die Seite „Mods“ liest nur.

## [1.1.0] – 2026-10-07

Getestet am 2026-10-07 auf einem echten Laptop mit Windows 11 und einem Bildschirm mit 1920 × 1200, mit genau diesen Setup-Dateien: der erste Teil des Tests (Update von 1.0.0 auf 1.1.0, Spielen, die Seiten des Launchers) ist bestanden. Die Maus reagiert direkt nach dem Start ohne Alt+Tab.

Der zweite Teil des Tests lief nicht. Nicht auf echter Hardware getestet sind deshalb: Abbrechen bei installierten Spielen (auch der Abbruch einer Reparatur), Deinstallieren mit „Behalten“ und mit „Löschen“, Abbrechen ohne Spiele, Neuinstallation, die Übernahme eines einzeln installierten Spiels, das Setup in anderen Sprachen und der Wechsel des Wrappers über „Erweitert“. Abbrechen, Neuinstallation, Übernahme und Deinstallation prüft bisher nur der automatische Ende-zu-Ende-Test (Szenarien S1 bis S14 auf einem Windows-Rechner von GitHub, mit Platzhaltern statt der Spiele, ohne Fehler für die Setup-Commits `2b764e4` und `75923f3`). 1.1.0 wurde trotzdem freigegeben. Findet der zweite Teil später ein Problem, wird es in 1.1.1 behoben.

### Hinzugefügt

- **Ein Fenster für die ganze Installation:** Statuszeile, Balken und eine Liste der fertigen Schritte. Die Setups der beiden Spiele zeigen keine eigenen Fenster mehr (außer im Pfad „Erweitert“).
- **Abbrechen** geht, bis ein Spiel installiert wird, auch bei einer Reparatur oder einem Update. Danach ist „Abbrechen“ grau, mit einer Zeile unter dem Balken, die sagt, warum.
- **Ein Symbol** „Empire Earth Community“ auf dem Desktop statt zwei. Der **Launcher 1.1.0** zeigt alle vier Spiele in einer Liste und merkt sich deine Wahl. Ein Setup oder eine Reparatur entfernt die zwei alten Symbole von 1.0.0.
- **Launcher:** neue Seite „Grafik“ (zeigt die Werte der Spiele an, ohne etwas zu ändern), neue Seite „Mods“ (nur lesend), ein Fenster, das du größer ziehen kannst, und „Reparatur-Hinweise“ mit Links zu den Downloadseiten der Website.
- **Aktivierungssignal des Launchers:** Nach dem Start über den Launcher bekommt das Spiel ein Signal, das die Maus ohne Alt+Tab weckt.
- **dgVoodoo 2.87.5** in allen fünf Stufen, mit neuen Fenstereinstellungen. Das Spielfenster kann bis 1920 × 1200 groß sein (bisher höchstens 1080 Zeilen).
- **Intro-Videos** werden standardmäßig mit installiert. Bei einem Update bekommst du sie einmal nachgeliefert, danach bleibt deine Auswahl.

### Geändert

- **Download als GitHub-Release:** Das Paket ist eine einzige ZIP-Datei `Empire-Earth-Community-1.1.0.zip` (etwa 1,3 GB) unter „Assets“ im Release `v1.1.0`. Darin liegt der Ordner `Empire-Earth-Community-1.1.0` mit dem Setup, den 26 .bin-Dateien, `SHA256SUMS.txt`, `BUILD-INFO.txt`, `README.md`, `LIES-MICH.txt`, `CHANGELOG.md`, `VERSION` und `Lizenzen/`. „Source code (zip)“ und „Source code (tar.gz)“ dieses Release enthalten nur die Dokumente, nicht das Spiel. Das Repository enthält nur noch die Dokumente der neuesten Version. Das Setup und die .bin-Dateien von 1.0.0 sind nicht mehr im aktuellen Stand, bleiben aber in der Historie beim Tag `v1.0.0`. Testversionen erscheinen künftig als „Pre-release“, zum Beispiel `v1.1.1-rc1`.
- Die Seite „Einstellungen“ des Launchers hat keine überlappenden Texte und keine verdeckten Knöpfe mehr.
- „Empire Earth Diagnostic“ bekommt keine Verknüpfung mehr. Es liegt weiter im Spielordner unter `Tools\Diagnostic`.

### Behoben

- Die Maus reagiert nach dem Start über den Launcher sofort, ohne Alt+Tab (auf dem Test-Laptop bestätigt).
- Während der Installation gab es neben dem Fenster der Suite eigene Fortschrittsfenster der Spiel-Setups.
- Die Seite „Einstellungen“ des Launchers: überlappende Texte und ein Bild über zwei Knöpfen.

### Bekannte Probleme

- Die Maus bleibt tot, wenn du das Spiel ohne den Launcher startest, den Launcher früh schließt oder das Spiel mit „Als Administrator ausführen“ läuft. Abhilfe: einmal Alt+Tab hinaus und zurück.
- Eine Windows-Benachrichtigung kann das Spiel minimieren. Das macht das Spielprogramm selbst. Vorbeugen: Benachrichtigungen stummschalten.
- Die Online-Spielerliste von NeoEE im Launcher zeigt „nicht verfügbar“, weil der Statusserver titan.empireearth.eu keinen DNS-Eintrag mehr hat.
- Abbrechen, Deinstallieren, Neuinstallation, andere Sprachen und der Weg über „Erweitert“ sind auf echter Hardware noch nicht getestet (siehe oben).

## [1.0.0] – 2026-10-06

Die erste Version. Getestet am 2026-10-06 auf einem echten Laptop mit Windows 11: Installation beider Spiele mit den Standard-Einstellungen, Spielen über die Desktop-Verknüpfungen, Deinstallation mit „Behalten“, Neuinstallation und Deinstallation mit „Löschen“.

### Hinzugefügt

- **Ein Setup für alles:** „Empire Earth Community Setup“ 1.0.0 installiert nacheinander Empire Earth mit der Erweiterung The Art of Conquest (Setup 1.7.2) und Neo Empire Earth 2.0.0.5. Du kannst auch nur eines der beiden Spiele auswählen.
- **Empire Earth Launcher 1.0.0 und Mod Creator** werden mit installiert, wenn das .NET Framework 4.8 vorhanden ist. Ohne .NET starten die Verknüpfungen die Spiele direkt.
- Die NeoEE-CD-Keys werden während der Installation online registriert.
- Verknüpfungen auf dem Desktop und der Ordner „Empire Earth Community“ im Startmenü.
- **Reparieren:** Das Setup erneut starten repariert installierte Spiele und legt die Verknüpfungen neu an.
- **Deinstallieren** über einen einzigen Eintrag „Empire Earth Community (Launcher, EE, NeoEE)“. Am Ende entscheidest du, ob Spielstände, Profile und Launcher-Sicherungen behalten oder gelöscht werden.
- Klare Meldungen, bevor etwas installiert wird: Start aus der ZIP-Datei, unvollständiges oder beschädigtes Paket, zu wenig Platz auf C:, laufendes Spiel oder laufender Launcher, fehlendes .NET Framework 4.8.
- Die letzte Seite des Setups zeigt, was installiert wurde und wo die Protokolle liegen.
- `SHA256SUMS.txt` mit den Prüfsummen der 27 Setup-Dateien (.exe und .bin) und `BUILD-INFO.txt` mit den genauen Quellen des Builds.
- Anleitung für Spieler ohne Vorkenntnisse in `README.md` und `LIES-MICH.txt`, dazu `CHANGELOG.md` und `VERSION`.
- Lizenzen und Hinweise zum Quellcode im Ordner `Lizenzen/`.

### Behoben

- Der Launcher hat den Ordner der Suite fälschlich als beschädigte Installation aufgelistet. Ein erster Build vom selben Tag wurde deshalb noch vor der Veröffentlichung ersetzt. Behoben in Launcher `b4fd570` und Suite `36b0e09` (Vertragsrevision 5).

### Bekannte Probleme

- Die Maus reagiert direkt nach dem Spielstart nicht. Abhilfe: das Spiel einmal minimieren und wiederherstellen, zum Beispiel mit zweimal Alt+Tab. Wird untersucht, Behebung für 1.1.0 geplant.
- Eine Windows-Benachrichtigung kann das Spiel minimieren. Danach ist das Bild nicht mehr im Vollbild oder kleiner. Vorbeugen: Benachrichtigungen beim Spielen stummschalten („Nicht stören“). Wird untersucht, Behebung für 1.1.0 geplant.
- Die Online-Spielerliste von NeoEE im Launcher zeigt „nicht erreichbar“, weil der Statusserver titan.empireearth.eu keinen DNS-Eintrag mehr hat. Das liegt am Server, nicht an deinem Computer.
- Launcher-Seite „Einstellungen“: Oben überlappen Texte, und ein Bild verdeckt zwei Knöpfe. Behebung für 1.1.0 geplant.
- Während der Installation zeigen die Setups von EE und NeoEE eigene Fortschrittsfenster neben dem Fenster der Suite. Ein einziges Fortschrittsfenster ist für 1.1.0 geplant.

[Unreleased]: https://github.com/DritteRippe/Empire-Earth-Community/compare/v1.1.0...HEAD
[1.1.0]: https://github.com/DritteRippe/Empire-Earth-Community/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/DritteRippe/Empire-Earth-Community/releases/tag/v1.0.0
