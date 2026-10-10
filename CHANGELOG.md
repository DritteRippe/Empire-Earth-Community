# Changelog

Hier stehen alle Änderungen an diesem Paket, die neueste Version zuerst.

Das Format folgt [Keep a Changelog](https://keepachangelog.com/de/1.1.0/), die Versionsnummern folgen [Semantic Versioning](https://semver.org/lang/de/). Jede Version ist ein Tag `vX.Y.Z` auf `main` mit einem GitHub-Release. Ab 1.1.0 liegt das Paket in diesem Release als eine ZIP-Datei unter „Assets“. Ältere Versionen bleiben über ihren Tag erreichbar, die Historie wird nicht umgeschrieben. Wie du eine ältere Version herunterlädst, steht in der [README](README.md#versionen).

## [Unreleased]

### Geplant

Für spätere Versionen ist geplant (ohne festes Datum):

- Discord-Status: Discord zeigt an, was du gerade spielst.
- Weitere Grafik-Einstellungen: Wrapper und Anzeigemodus wählen, Auflösungen über 1920 × 1200. Seit 1.1.0 stellt die Seite „Grafik“ die Größe des Spielfensters ein (bis 1920 × 1200) und zeigt den Wrapper und seine `dgVoodoo.conf` nur an. Die Seite „Mods“ liest nur.

## [1.1.1] – 2026-10-10

Eine Version mit Fehlerbehebungen. Setup 1.1.1 und Launcher 1.1.1 bringen die Korrekturen aus einer Durchsicht des Codes nach 1.1.0. Am meisten merkst du davon: Der Launcher schickt eine Installation aus diesem Paket nie mehr zum Setup von empireearth.eu, das die Verbesserungen des Pakets rückgängig machen würde, sondern zur Release-Seite dieses Pakets. Die Spiele und ihre Setups (Version 1.7.2) haben keine neuen Funktionen. Dazu kommen eine überarbeitete Anleitung und neue Dateien für ein öffentliches Repository.

Enthalten: Empire Earth Community Setup 1.1.1 (Tag `suite-v1.1.1`, Commit `164e561`), Empire Earth Launcher 1.1.1 mit dem Mod Creator (Tag `v1.1.1`, Commit `90a35a4`), die Setups von Empire Earth und NeoEE (Setup 1.7.2, neu gebaut mit der Kennung `suite-1.1.1-164e561`) und dgVoodoo 2.87.5.

**Nicht auf echter Hardware getestet.** Setup und Launcher 1.1.1 wurden am 2026-10-08 freigegeben, ohne dass bis dahin ein Fall des Testplans mit 1.1.1 auf einem echten Computer lief. Der erste Teil des Tests auf dem Laptop (Update von 1.0.0, Spielen, die Seiten des Launchers) lief nur mit 1.1.0 und wurde mit 1.1.1 nicht wiederholt. Der zweite Teil lief weder mit 1.1.0 noch mit 1.1.1: Abbrechen bei installierten Spielen (auch der Abbruch einer Reparatur), Deinstallieren mit „Behalten“ und mit „Löschen“, Abbrechen ohne Spiele, Neuinstallation, die Übernahme eines einzeln installierten Spiels, das Setup in anderen Sprachen und der Wechsel des Wrappers über „Erweitert“. Davon liefen Deinstallieren und Neuinstallation zuletzt mit 1.0.0 auf echter Hardware (am 2026-10-06, siehe den Eintrag zu 1.0.0), Abbrechen (das es seit 1.1.0 gibt), die Übernahme, andere Sprachen und „Erweitert“ mit keiner Version. Auch alles, was in 1.1.1 neu ist, lief noch nicht auf echter Hardware. Automatisch geprüft sind Installation, Übernahme, Reparatur, Abbrechen und Deinstallation, jetzt auch mit „Löschen“: Der Ende-zu-Ende-Test des Setups (Szenarien S1 bis S15 auf einem Windows-Rechner von GitHub, mit Platzhaltern statt der Spiele) lief ohne Fehler für die Setup-Commits `2fc0e76` und `e597714`. Danach änderte sich bis zum Commit `164e561` am Setup selbst nur noch die Versionsnummer. Die übrigen Änderungen betrafen Dokumente, ein Formular und einen Workflow zum Veröffentlichen. Die Fehler, die 1.1.1 behebt, stammen also nicht aus einem Test auf echter Hardware, sondern aus der Durchsicht des Codes.

### Hinzugefügt

- **Launcher, Seite „Werkzeuge“:** Unter „Updates“ steht neben „Nach Updates suchen“ der Knopf „Release-Seite öffnen“. Er öffnet die Release-Seite dieses Pakets im Browser, erst nach deinem Klick. Der Launcher selbst fragt nichts bei GitHub ab. Kann er den Browser nicht öffnen, nennt er die Adresse zum Kopieren.
- **Eine Kennung für die Setups der Spiele:** Die Setups von Empire Earth und NeoEE tragen weiter die Version 1.7.2, jetzt aber auch die Kennung `suite-1.1.1-164e561` (SetupBuild). `BUILD-INFO.txt` nennt sie. So lassen sich die Setups dieses Pakets von denen anderer Versionen des Pakets unterscheiden.
- **Fehler melden:** Ein Formular für Issues in diesem Repository fragt nach der Version des Pakets, nach Windows, nach dem Spiel und dem Spielmodus, nach dem, was passiert ist, und nach den Protokollen. Fragen zum Code gehen über die Auswahl direkt zum Repository des Setups oder des Launchers.
- **Sicherheit:** `SECURITY.md` erklärt, wie du eine Sicherheitslücke privat meldest (über „Private vulnerability reporting“ von GitHub) und wie du die Echtheit des Pakets prüfst.
- **Mitmachen:** `CONTRIBUTING.md` erklärt, wie du Fehler meldest und die Anleitung verbesserst, wo der Code liegt und wie ein Release entsteht.

### Geändert

- **„Nach Updates suchen“ im Launcher:** Die Erklärung daneben sagt jetzt, was geprüft wird: das installierte Spiel und das Setup des Spiels (Empire Earth oder NeoEE) beim Server von empireearth.eu, nicht dieses Paket. Neue Versionen des Pakets erscheinen auf seiner Release-Seite. Die Zeile mit dem Ergebnis nennt das Setup mit dem Namen des Spiels, damit sie nicht wie der Stand des Pakets klingt.
- **Zustand „Unbekannt“ im Launcher** nach einem älteren Setup: Die Erklärung sagt jetzt „Reparieren Sie die Installation mit den Schritten der Reparatur-Hinweise.“ Vorher stand dort „Führen Sie das aktuelle Setup aus.“, und das klang nach dem Setup von empireearth.eu, das den Zustand gerade erst verursacht hatte.
- **Eintrag in Windows „Apps“:** Die Links für Hilfe und Updates des Eintrags „Empire Earth Community (Launcher, EE, NeoEE)“ führen jetzt zu diesem Repository und seinen Releases statt zu empireearth.eu. Die Website bietet das Paket weder an, noch hilft sie dazu.
- **Anleitung für 1.1.1:** `README.md` und `LIES-MICH.txt` beschreiben 1.1.1. Neu ist der Abschnitt „Update von 1.1.0“. „Bekannte Probleme“ und „Technische Details“ sagen, was mit 1.1.1 getestet ist, was nicht und mit welcher Version ein Fall zuletzt auf echter Hardware lief.
- **Anleitung für ein öffentliches Repository:** `README.md` und `LIES-MICH.txt` nennen die Adresse der Release-Seite (<https://github.com/DritteRippe/Empire-Earth-Community/releases/latest>), für den Download brauchst du kein Konto. Fehler meldest du in den Issues dieses Repositorys, Sicherheitslücken privat (siehe `SECURITY.md`). Der Hinweis, dass das Paket nur für Besitzer des Originalspiels ist und die Rechte an den Spieldaten bei ihren Inhabern liegen, bleibt im Abschnitt „Rechtlicher Hinweis“.
- **Übersichtlichere README:** ein Banner, Abzeichen für Version, Downloads, Windows und Lizenz, ein großer Knopf „Neueste Version herunterladen“, der Abschnitt „In 3 Schritten spielen“ (statt „Schnellstart“), ein Bild des Launchers, farbige Hinweiskästen für das Wichtigste und zum Aufklappen die Fehlermeldungen, die Prüfung der entpackten Dateien und die älteren Versionen. Neu ist der Abschnitt „Häufige Fragen“. `LIES-MICH.txt` hat denselben Inhalt als reinen Text.
- **Erst prüfen, dann freigeben:** Schritt 2 zeigt, wie du die Prüfsumme der ZIP-Datei mit der im Text des Release vergleichst, bevor du die Datei mit „Zulassen“ freigibst. „Paket prüfen“ erklärt, dass `SHA256SUMS.txt` nur Schäden zeigt, nicht die Herkunft.
- **Neue Versionen:** Der Abschnitt „Versionen“ erklärt, wie du von einer neuen Version erfährst (auf GitHub „Watch“ > „Custom“ > „Releases“ oder der RSS-Feed der Releases), und dass „Version prüfen“ und „Nach Updates suchen“ im Launcher nur das Spiel und sein Setup beim Server von empireearth.eu prüfen, nicht dieses Paket.
- **Reparieren:** Die Anleitung warnt davor, das Setup von empireearth.eu zu nehmen. Es ersetzt die Installation des Pakets und macht seine Verbesserungen rückgängig. Die „Reparatur-Hinweise“ des Launchers 1.1.0 nannten es noch, die des Launchers 1.1.1 nicht mehr (siehe „Behoben“).
- **Ehrlich, was noch nicht getestet ist:** Abbrechen, Deinstallieren und der Wechsel des Wrappers über „Erweitert“ stehen in der Anleitung als vorgesehen, nicht als geprüft. Dass ein Spiel mit „Als Administrator ausführen“ das Aktivierungssignal nicht annimmt, steht dort als erwartet, nicht als Tatsache.
- **Lizenzen:** Der Ordner `Lizenzen/` hat den Stand der Tags `v1.1.1` des Launchers und `suite-v1.1.1` des Setups: `THIRD-PARTY-NOTICES.md` nennt ZipStorer 3.7.0 mit seinen lokalen Korrekturen, `THIRD-PARTY-NOTICES-Setup.md` zusätzlich BASS und die anderen mitgelieferten Programmdateien der Spiel-Setups, und `licenses/THIRD-PARTY-LICENSES.txt` nennt das Repository DritteRippe/Empire-Earth-Launcher als Quelle. Die Fassung aus der ZIP-Datei von 1.1.0 bleibt beim Tag `v1.1.0`.

### Behoben

- **Reparatur-Hinweise des Launchers ohne den entpackten Ordner:** Für eine Installation aus diesem Paket nannten sie die Downloadseite von empireearth.eu. Deren Setup ist eine andere Fassung mit derselben Version 1.7.2. Es installierte über das Paket und machte seine Verbesserungen rückgängig. Danach zeigte der Launcher „Unbekannt“ und wieder dieselbe Seite. Jetzt nennen die Hinweise für jede Installation aus diesem Paket die Release-Seite des Pakets. Fehlt der Ordner, sagen sie, dass du das Paket neu herunterlädst, entpackst und daraus „Empire Earth Community Setup“ startest. Ist der Ordner da, bleibt der erste Schritt, das Setup daraus erneut zu starten, und die Release-Seite ist der zweite Weg. Für Spiele, die nicht mit diesem Paket installiert wurden, bleibt die Downloadseite des Spiels.
- **Reparatur-Hinweise bei einem gemeldeten Update:** Für eine Installation aus diesem Paket sagten sie, du sollst „Empire Earth Community Setup“ erneut aus seinem Ordner starten. Das installiert aber dieselben Versionen noch einmal. Als zweiten Weg boten sie das Setup der Website an. Jetzt sagen sie, dass das Paket neuere Versionen nur als neues Release bekommt, und nennen seine Release-Seite.
- **Protokoll des Launchers:** Ein zweiter Start des Launchers (zum Beispiel ein Doppelklick auf das Symbol, während der Launcher schon läuft) konnte `log.txt` nicht öffnen und schrieb seine Zeilen in eine neue Datei neben `log.txt`, deren Name mit einer langen Kennung beginnt (`<Kennung>log.txt`). Jetzt schreibt jeder Start in die eine Datei `log.txt`. Solche Dateien, die 1.1.0 in `%LOCALAPPDATA%\Empire Earth Launcher` hinterlassen hat, kannst du löschen.
- **„Nach Updates suchen“, „Version prüfen“ und „Netzwerk prüfen“** endeten mit einem unerwarteten Fehler, wenn die Antwort des Update-Servers oder eines Proxys dazwischen einen Zeichensatz nannte, den Windows nicht kennt. Der Launcher liest die Antwort jetzt selbst.
- **Mod Creator:**
  - Manche Archive des Mod Creators (etwa 3 von 1000) konnte die Mod-Bibliothek nicht wieder lesen.
  - Beim Export löschte er jedes `Banner*.png` eines Variantenordners, auch eigene Dateien wie `BannerSource.png`. Jetzt löscht er nur die Banner, die er selbst schreibt.
  - Dateien, die er als ignoriert meldete, kamen trotzdem ins veröffentlichte Archiv. Jetzt enthält das Archiv nur den beschriebenen Aufbau.
  - Dateien und Archive ab 4 GB ergaben ohne Fehlermeldung ein kaputtes Archiv. Jetzt bricht er mit einer Meldung ab, und ein vorhandenes Archiv bleibt, wie es war.
  - Die gewählten Bilder für Symbol und Banner blieben gesperrt, bis das Programm endete. Jetzt lädt er sie in den Speicher, die Dateien bleiben frei. Eine Datei, die kein Bild ist, meldet er als solche, nicht mehr als Mangel an Speicher.
  - Eine Datei, die kein ZIP-Archiv ist, meldet die Mod-Bibliothek jetzt klar als „kein ZIP-Archiv oder beschädigt“.
- **Abbrechen:** Beendete sich das Setup eines Spiels genau in dem Moment, in dem du abbrichst, behandelte das Setup den Abbruch als unklar und versuchte ihn noch einmal. Ein Setup, das sich gerade beendet, gilt jetzt als beendet.
- **Deinstallieren:** Bleibt ein Spiel installiert, erkennt das Setup es jetzt auch, wenn sein Ordner in der kurzen Schreibweise von Windows eingetragen ist (zum Beispiel `C:\PROGRA~2\…`). Die Spielstände und Profile, die es mit dem entfernten Spiel teilt, bietet das Setup dann nicht zum Löschen an.
- `Lizenzen/Quellcode.txt` nannte als Stand des Quellcodes den Branch `v2`, den es nicht mehr gibt. Jetzt nennt die Datei die Tags `suite-v1.1.1` und `v1.1.1`, aus denen dieses Paket gebaut ist, mit ihren Commits und Links.
- Der Eintrag zu 1.1.0 beschrieb die Seite „Grafik“ des Launchers falsch: Sie ändert sehr wohl etwas, nämlich die Größe des Spielfensters. Der Eintrag ist korrigiert und als Korrektur gekennzeichnet. Die Anleitung war schon richtig.
- Der Link in `Lizenzen/THIRD-PARTY-NOTICES.md` auf die Hinweise des Setups zeigte auf eine Seite, die es nicht gibt. Er führt jetzt zu DritteRippe/Empire-Earth-Setup.

### Sicherheit

- **Deinstallieren mit „Löschen“:** Das Setup prüft jeden Ordner mit Spielständen, Profilen, Mods und Sicherungen direkt vor dem Löschen noch einmal auf Verknüpfungen (Junctions). Bisher prüfte es nur vor der Frage. Eine Verknüpfung, die jemand anlegte, während die Frage offen war (zum Beispiel bei `Data\dxm`), konnte das Setup, das mit Administratorrechten läuft, dazu bringen, außerhalb der Installation zu löschen. Einen Ordner, den es nicht prüfen kann, behandelt es jetzt wie eine Verknüpfung. Offen bleibt nur der kurze Moment zwischen dieser zweiten Prüfung und dem Ende des Löschens.
- **Mod-Bibliothek:** Ein beschädigtes oder absichtlich verändertes Mod-Archiv (`.eem`) von wenigen Byte konnte beim Lesen bis zu 2 GB Speicher belegen. Solche Archive werden jetzt abgelehnt. Außerdem müssen die Dateien einer Mod in ihrem Spielordner bleiben: Archive mit anderen Pfaden lehnt die Bibliothek ab, und der Mod Creator schreibt keine. Das schützt einen späteren Installer für Mods, Mods installieren kann der Launcher noch nicht.

### Bekannte Probleme

- Die Maus bleibt tot, wenn du das Spiel ohne den Launcher startest, den Launcher früh schließt oder das Spiel mit „Als Administrator ausführen“ läuft. Abhilfe: einmal Alt+Tab hinaus und zurück.
- Eine Windows-Benachrichtigung kann das Spiel minimieren. Das macht das Spielprogramm selbst. Vorbeugen: Benachrichtigungen stummschalten.
- Die Online-Spielerliste von NeoEE im Launcher zeigt „nicht verfügbar“, weil der Statusserver titan.empireearth.eu keinen DNS-Eintrag mehr hat.
- 1.1.1 ist nicht auf echter Hardware getestet. Abbrechen, die Übernahme eines einzeln installierten Spiels, andere Sprachen und der Weg über „Erweitert“ sind es mit keiner Version, Deinstallieren und Neuinstallation zuletzt mit 1.0.0 (siehe oben).

## [1.1.0] – 2026-10-07

Getestet am 2026-10-07 auf einem echten Laptop mit Windows 11 und einem Bildschirm mit 1920 × 1200, mit genau diesen Setup-Dateien: der erste Teil des Tests (Update von 1.0.0 auf 1.1.0, Spielen, die Seiten des Launchers) ist bestanden. Die Maus reagiert direkt nach dem Start ohne Alt+Tab.

Der zweite Teil des Tests lief nicht. Nicht auf echter Hardware getestet sind deshalb: Abbrechen bei installierten Spielen (auch der Abbruch einer Reparatur), Deinstallieren mit „Behalten“ und mit „Löschen“, Abbrechen ohne Spiele, Neuinstallation, die Übernahme eines einzeln installierten Spiels, das Setup in anderen Sprachen und der Wechsel des Wrappers über „Erweitert“. Abbrechen, Neuinstallation, Übernahme und Deinstallation prüft bisher nur der automatische Ende-zu-Ende-Test (Szenarien S1 bis S14 auf einem Windows-Rechner von GitHub, mit Platzhaltern statt der Spiele, ohne Fehler für die Setup-Commits `2b764e4` und `75923f3`). 1.1.0 wurde trotzdem freigegeben. Findet der zweite Teil später ein Problem, wird es in 1.1.1 behoben.

### Hinzugefügt

- **Ein Fenster für die ganze Installation:** Statuszeile, Balken und eine Liste der fertigen Schritte. Die Setups der beiden Spiele zeigen keine eigenen Fenster mehr (außer im Pfad „Erweitert“).
- **Abbrechen** geht, bis ein Spiel installiert wird, auch bei einer Reparatur oder einem Update. Danach ist „Abbrechen“ grau, mit einer Zeile unter dem Balken, die sagt, warum.
- **Ein Symbol** „Empire Earth Community“ auf dem Desktop statt zwei. Der **Launcher 1.1.0** zeigt alle vier Spiele in einer Liste und merkt sich deine Wahl. Ein Setup oder eine Reparatur entfernt die zwei alten Symbole von 1.0.0.
- **Launcher:** neue Seite „Grafik“ (die Größe des Spielfensters wählen, bis 1920 × 1200, mit einer Sicherung der alten Werte; den Wrapper und seine `dgVoodoo.conf` zeigt sie nur an), neue Seite „Mods“ (nur lesend), ein Fenster, das du größer ziehen kannst, und „Reparatur-Hinweise“ mit Links zu den Downloadseiten der Website. *(Korrektur vom 2026-10-08: Hier stand zuerst, die Seite „Grafik“ zeige die Werte der Spiele an, ohne etwas zu ändern. Das war falsch, die Größe des Spielfensters lässt sich dort ändern.)*
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

[Unreleased]: https://github.com/DritteRippe/Empire-Earth-Community/compare/v1.1.1...HEAD
[1.1.1]: https://github.com/DritteRippe/Empire-Earth-Community/compare/v1.1.0...v1.1.1
[1.1.0]: https://github.com/DritteRippe/Empire-Earth-Community/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/DritteRippe/Empire-Earth-Community/releases/tag/v1.0.0
