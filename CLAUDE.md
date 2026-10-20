# Hinweise für die Arbeit an diesem Repo

Kurse für das Tool Turtle (`masta-nksa/turtle`). Fachliche Doku: `README.md` hier; das
Aufgabenformat steht im README des Tools («Kursmodus», «Aufgabenformat»).

## Konventionen

- Ein Ordner pro Kurs mit `kurs.json` (und evtl. `bilder/`). GitHub Pages aus `main`, Root;
  `.nojekyll` muss bleiben. Pages-Einstellungen richtet die Lehrperson selbst ein.
- Texte auf Deutsch (Schweiz, «ss» statt «ß»), Anrede «Sie», Anführungszeichen «…».
- Alle Programme mit `from turtle import *` (Befehle ohne Objekt); erst in den Spielbausteinen
  `kopf = Turtle()` usw.
- **Keine Lösungen und keine Testskripte im Repo.** Zielbilder entstehen mit dem
  Zielbild-Werkzeug des Tools (`?werkzeug=ziel`) aus einer Lösung, die nicht eingecheckt wird.
- Aufgaben-`id`s nie ändern oder wiederverwenden (Fortschritt und Programme im Browser hängen
  daran). Neue Aufgaben bekommen neue ids.
- Text so genau, dass das Zielbild eindeutig ist (Start, Längen, Drehrichtung, Farbnamen, wenn
  geprüft). Der Startcode darf die Aufgabe nicht schon lösen.
- Gliederung des Beispielkurses: Einheiten mit `abschnitt` «Entdecken» → «Konzepte sichern» →
  «Lernkontrolle», danach Projekt Snake; ★ = `zusatz`.
- Felder, die das Tool noch nicht kennt, erst im Tool einbauen (`kurs.js` prüft streng).

## Testen

Beide Repos nebeneinander, Server im Ordner darüber, `…/turtle/?kurs=turtle-aufgaben/<kurs>`.
Testskripte nur im Scratchpad. Prüfen: Kurs lädt ohne Warnung in der Konsole, jede Lösung
besteht ihr Zielbild, kein Startcode besteht es schon.
