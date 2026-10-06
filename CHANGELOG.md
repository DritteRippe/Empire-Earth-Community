# Changelog

Hier stehen alle Änderungen an diesem Paket, die neueste Version zuerst.

Das Format folgt [Keep a Changelog](https://keepachangelog.com/de/1.1.0/), die Versionsnummern folgen [Semantic Versioning](https://semver.org/lang/de/). Jede Version ist ein Tag `vX.Y.Z` auf `main` mit einem GitHub-Release. Ältere Versionen bleiben über ihren Tag erreichbar, die Historie wird nicht umgeschrieben. Wie du eine ältere Version herunterlädst, steht in der [README](README.md#versionen).

## [Unreleased]

### Geplant

Für Version 1.1.0 ist geplant (ohne festes Datum):

- Die Maus reagiert direkt nach dem Spielstart, ohne das Spiel erst minimieren zu müssen.
- Nach einer Windows-Benachrichtigung bleibt das Spiel im Vollbild.
- Die Launcher-Seite „Einstellungen“ wird aufgeräumt: keine überlappenden Texte und keine verdeckten Knöpfe mehr.
- Während der Installation zeigt nur noch ein einziges Fenster den Fortschritt.
- Eine neue Grafik-Seite im Launcher: Wrapper, Anzeigemodus und Auflösung einstellen.
- Discord-Status: Discord zeigt an, was du gerade spielst.
- Eine Mods-Seite im Launcher (dreXmod).

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

[Unreleased]: https://github.com/DritteRippe/ee-paket/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/DritteRippe/ee-paket/releases/tag/v1.0.0
