# Turtle-Aufgaben

Lernaufgaben für [Turtle](https://masta-nksa.github.io/turtle/) (Python mit der Turtle im
Browser, Repo [masta-nksa/turtle](https://github.com/masta-nksa/turtle)). Das Tool bleibt
kursunabhängig; die Kurse liegen hier, ein Ordner pro Kurs. Für die Schülerinnen und Schüler sieht
es aus, als wären die Aufgaben im Tool eingebaut.

## Kurse

| Ordner | Kurs | Link für die Klasse |
| --- | --- | --- |
| `beispiel/` | Programmieren mit der Turtle: 6 Einheiten und Projekt Snake (ca. 20 Lektionen) | <https://masta-nksa.github.io/turtle/?kurs=turtle-aufgaben/beispiel> |

Ein Link auf eine bestimmte Aufgabe: `…?kurs=turtle-aufgaben/beispiel&aufgabe=achteck`
(in der Aufgabe: «Link zum Teilen kopieren»).

## Aufbau eines Kurses

```
<kurs>/kurs.json     Reihen, Aufgaben, Konzepte (Format: README des Tools, «Aufgabenformat»)
<kurs>/bilder/…      optional, Bilder zu Aufgaben («bild»: "bilder/blume.png")
```

Der Beispielkurs ist so gegliedert:

- **Einheiten 1–6** (Reihen): Zeichnen · Wiederholen · Eigene Befehle · Veränderung · Entscheiden ·
  Spielbausteine. Jede Einheit hat die Abschnitte
  - **Entdecken**: ein Programm lesen und vorhersagen (`vorhersage`, `fragen`), dann verändern und
    erweitern (`weiterVon`: die Erweiterung beginnt mit dem eigenen Programm);
  - **Konzepte sichern**: kleine Aufgaben zu den Konzepten der Einheit: Fehler finden, ergänzen,
    vorhersagen;
  - **Lernkontrolle** (`kontrolle`): 2–3 Aufgaben mit Zielbild, ohne Hinweise.
- **Projekt Snake**: sechs Meilensteine, die aufeinander aufbauen, mit Checklisten zum Selbst-Prüfen.
- ★-Aufgaben (`zusatz`) für Schnelle; sie zählen nicht zum Fortschritt der Reihe.
- **Konzepte**: Erklärungen zum Nachlesen (Knopf «Konzepte», Etiketten bei den Aufgaben),
  angepasst aus <https://oinf.hexcode.ch/konzepte>.

## Aufgaben schreiben

1. Aufgabe in `kurs.json` eintragen (`id` eindeutig im ganzen Kurs; nie nachträglich ändern,
   sonst verlieren die Schülerinnen und Schüler Programm und Haken).
2. Soll das Tool automatisch prüfen: Zielbild erzeugen.
   - Tool mit `?werkzeug=ziel` öffnen: <https://masta-nksa.github.io/turtle/?werkzeug=ziel>.
   - Die eigene Lösung einfügen und «Start» drücken.
   - Unter dem Feld steht das Zielbild als JSON; «Farben übernehmen» nur ankreuzen, wenn die
     Farbe Teil der Aufgabe ist. «Kopieren» und als `"ziel"` in die Aufgabe einfügen.
   - **Die Lösung selbst kommt nicht ins Repo**, nur das Ziel.
3. Den Text so genau schreiben, dass das Ziel eindeutig ist: Startpunkt, Längen, Drehrichtung
   («nach links drehend»), Farbnamen, wenn sie geprüft werden.
4. Den Startcode prüfen: Er darf die Aufgabe nicht schon lösen.
5. Ohne Zielbild (Spiele, Zufall, freie Aufgaben): `checkliste` angeben; erledigt wird durch
   Selbst-Abhaken.

Ist `kurs.json` fehlerhaft, nennt das Tool die Stelle («Reihe 2, Aufgabe 5, text: fehlt.») und
läuft ohne Kurs weiter. Darum vor dem Hochladen lokal testen.

### Lokal testen

Beide Repos nebeneinander auschecken (`…/turtle` und `…/turtle-aufgaben`), im Ordner darüber

```
python3 -m http.server 8000
```

und <http://localhost:8000/turtle/?kurs=turtle-aufgaben/beispiel> öffnen.

## Eigene Kurse anderer Lehrpersonen

Ein eigenes Repo mit GitHub Pages genügt, z. B. `kollegin/turtle-kurse` mit dem Ordner `3b/`.
Aufruf: `https://masta-nksa.github.io/turtle/?kurs=kollegin/turtle-kurse/3b`.

## GitHub Pages

Settings → Pages → Source: «Deploy from a branch», Branch `main`, Ordner `/ (root)`.
Die leere Datei `.nojekyll` im Root muss bestehen bleiben.

## Herkunft

Aufgaben und Konzepttexte stützen sich auf das bisherige Unterrichtsmaterial der Lehrperson
(oinf.hexcode.ch, OneNote).
