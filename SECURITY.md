# Sicherheit

## Welche Versionen werden unterstützt?

| Version | Unterstützt |
|---|---|
| Das neueste Release ([Release-Seite](https://github.com/DritteRippe/Empire-Earth-Community/releases/latest)) | Ja |
| Ältere Versionen | Nein, bitte nimm das neueste Release |

Eine Behebung erscheint als neues Release dieses Pakets. Ein veröffentlichtes Release wird nachträglich nicht geändert.

## Eine Sicherheitslücke melden

Bitte melde eine Sicherheitslücke **nicht** in einem öffentlichen Issue, einem Pull Request oder einem Forum.

Melde sie stattdessen privat:
**[Sicherheitslücke melden](https://github.com/DritteRippe/Empire-Earth-Community/security/advisories/new)**
(Reiter *Security* dieses Repositorys, „Private vulnerability reporting“ von GitHub). Die Meldung sehen nur du und die
Maintainer des Repositorys. Schreib bitte dazu:

- die Version des Pakets (Datei `VERSION` im entpackten Ordner oder der Name der ZIP-Datei) und deine Windows-Version,
- was passiert und wie man es nachstellt,
- was ein Angreifer damit erreichen könnte.

Funktioniert das Formular bei dir nicht, eröffne ein Issue mit der Vorlage
[„Privaten Kontakt für eine Sicherheitsmeldung anfragen“](https://github.com/DritteRippe/Empire-Earth-Community/issues/new/choose),
ohne Einzelheiten zur Lücke. Dann wird mit dir ein privater Weg vereinbart.

Das ist ein ehrenamtliches Projekt: Du bekommst eine Antwort, sobald der Maintainer kann. Bestätigt sich die Meldung,
kommt die Behebung in einem neuen Release, und die Sicherheitsmeldung (Advisory) nennt dich, wenn du das möchtest.
Eine Belohnung (Bug-Bounty) gibt es nicht.

## Was gehört hierher?

- **Hierher:** das Paket selbst, also die ZIP-Datei eines Release, ihr Inhalt, wie er im Release liegt, und diese
  Anleitung, zum Beispiel ein Schritt, der dich zu etwas Unsicherem anleitet. Auch ein verändertes Paket, das jemand an
  anderer Stelle anbietet, meldest du bitte hier.
- **Fehler im Code des Setups oder des Launchers:** bitte direkt und ebenfalls privat im Repository, in dem der Code
  liegt:
  [Setup](https://github.com/DritteRippe/Empire-Earth-Setup/security/advisories/new) (das Setup „Empire Earth Community
  Setup“ und die Setups von Empire Earth und NeoEE) oder
  [Launcher](https://github.com/DritteRippe/Empire-Earth-Launcher/security/advisories/new) (der Empire Earth Launcher
  und der Mod Creator). Weißt du nicht, wohin es gehört, melde es hier. Die Meldung wird dann weitergegeben.
- **Nicht hierher:** das Spiel selbst, Software Dritter wie dgVoodoo und die Server der Community, zum Beispiel
  empireearth.eu.

## Echtheit des Pakets

Das Setup hat keine digitale Signatur. Lade das Paket deshalb nur von der
[Release-Seite](https://github.com/DritteRippe/Empire-Earth-Community/releases/latest) und vergleiche die Prüfsumme
der ZIP-Datei mit der im Text des Release, bevor du die Datei freigibst oder das Setup startest. Wie das geht, steht in
der README unter [Paket prüfen (Prüfsummen)](README.md#paket-prüfen-prüfsummen). Die Datei `SHA256SUMS.txt` liegt mit
im Paket. Sie zeigt nur, ob beim Herunterladen oder Entpacken etwas kaputtgegangen ist, nicht, ob das Paket aus dem
Release stammt.
