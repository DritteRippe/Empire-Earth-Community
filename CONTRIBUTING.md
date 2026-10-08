# Mitmachen

Danke, dass du helfen möchtest! Dieses Repository ist das Paket **Empire Earth Community** für Spielerinnen und
Spieler: die Anleitung, die Liste der Änderungen und die Releases mit der ZIP-Datei. Programmcode gibt es hier nicht.
Er liegt in zwei eigenen Repositorys (siehe [Wo liegt der Code?](#wo-liegt-der-code)).

## Fehler melden

- **Beim Installieren, Spielen, Reparieren oder Deinstallieren klappt etwas nicht:**
  [Fehler melden](https://github.com/DritteRippe/Empire-Earth-Community/issues/new/choose). Das Formular fragt nach
  der Version, nach Windows, nach dem Spiel und nach den Protokollen. Was hilft, steht in der README unter
  [Hilfe und Feedback](README.md#hilfe-und-feedback). Du kannst auf Deutsch oder auf Englisch schreiben.
- **Eine Sicherheitslücke:** bitte privat melden, siehe [SECURITY.md](SECURITY.md).
- Issues sind öffentlich. Hänge nie Spieldateien, CD-Keys oder das Paket an.

## Korrekturen und Übersetzungen

Die Anleitung gibt es auf Deutsch in zwei Formen mit demselben Inhalt: [README.md](README.md) für GitHub und
[LIES-MICH.txt](LIES-MICH.txt) als reinen Text, der im Paket neben dem Setup liegt und sich ohne Internet lesen lässt.

- Ein Tippfehler, ein unklarer Satz oder ein Fenster, das bei dir anders aussieht als beschrieben: Eröffne ein Issue
  oder schick einen Pull Request, der `README.md` und `LIES-MICH.txt` gleich ändert.
- So schreibt die Anleitung: Du-Form, kurze Sätze, ein Schritt pro Zeile, verständlich ohne Vorkenntnisse. Texte aus
  Fenstern und Knöpfen stehen wörtlich in „…“, genau so, wie das Programm sie zeigt.
- Benenne keine Überschrift um, auf die etwas verlinkt: das Inhaltsverzeichnis der README, `CHANGELOG.md`,
  `SECURITY.md`, diese Datei und die Formulare in `.github/ISSUE_TEMPLATE/` verlinken Abschnitte der README.
- Jede Änderung, die Spieler betrifft, kommt in [CHANGELOG.md](CHANGELOG.md) unter `[Unreleased]`
  ([Keep a Changelog](https://keepachangelog.com/de/1.1.0/)).
- Spieldateien, CD-Keys und das Setup mit seinen `.bin`-Dateien kommen nie in das Repository. Das Paket liegt nur als
  ZIP-Datei in den Releases.

Die Texte in den Fenstern des Setups und des Launchers werden dort übersetzt, wo der Code liegt:
[Übersetzen des Setups](https://github.com/DritteRippe/Empire-Earth-Setup/blob/main/TRANSLATING.md) und
[Übersetzen des Launchers](https://github.com/DritteRippe/Empire-Earth-Launcher/blob/main/docs/TRANSLATING.md)
(beide auf Englisch).

## Wo liegt der Code?

| Teil | Repository |
|---|---|
| Das Setup „Empire Earth Community Setup“ und die Setups von Empire Earth und NeoEE (Inno Setup) | [DritteRippe/Empire-Earth-Setup](https://github.com/DritteRippe/Empire-Earth-Setup) |
| Der Empire Earth Launcher und der Mod Creator (C#, .NET Framework 4.8) | [DritteRippe/Empire-Earth-Launcher](https://github.com/DritteRippe/Empire-Earth-Launcher) |

Beide stehen unter der GPL-3.0, sind auf Englisch dokumentiert und haben eine eigene Anleitung zum Mitmachen
(`CONTRIBUTING.md`). Fehler im Code meldest du am besten direkt dort.

## Wie entsteht ein Release?

Ein Release des Pakets entsteht in drei Schritten, in dieser Reihenfolge:

1. **Launcher:** Ein Tag `vX.Y.Z` im Launcher-Repository
   ([Checkliste](https://github.com/DritteRippe/Empire-Earth-Launcher/blob/main/docs/RELEASING.md)).
2. **Setup:** Ein Tag `suite-vX.Y.Z` im Setup-Repository
   ([Checkliste](https://github.com/DritteRippe/Empire-Earth-Setup/blob/main/docs/RELEASING.md)). Aus diesem Tag baut
   der Maintainer auf Windows das Setup „Empire Earth Community Setup“ mit den Spieldaten. `SHA256SUMS.txt` und
   `BUILD-INFO.txt` entstehen dabei.
3. **Paket (dieses Repository):** `README.md`, `LIES-MICH.txt`, `CHANGELOG.md`, `VERSION`, `BUILD-INFO.txt`,
   `SHA256SUMS.txt` und `Lizenzen/` beschreiben die neue Version. Dann bekommt `main` den Tag `vX.Y.Z`, und das Release
   dazu bekommt die ZIP-Datei `Empire-Earth-Community-X.Y.Z.zip` unter „Assets“ und ihre Prüfsumme (SHA-256) im Text.
   Testversionen erscheinen als „Pre-release“, zum Beispiel `v1.1.1-rc1`.

Ein veröffentlichter Tag wird nie verschoben oder gelöscht, ein veröffentlichtes Release nicht nachträglich geändert,
und die Historie von `main` wird nicht umgeschrieben. Ein Fehler nach dem Release bekommt eine neue Version.
