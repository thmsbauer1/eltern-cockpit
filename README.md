# Lernweg (früher Eltern-Cockpit)

Übersicht für Thomas und Nadine über Philips Lernstände aus Lern-Match, Spürnase und dem Testtrainer.
Läuft unter `https://thmsbauer1.github.io/lernweg/`. Anmeldung mit dem eigenen Konto des Familienspeichers (Eltern und Philip).

## Für wen

Für die ganze Familie. Jeder meldet sich mit seinem eigenen Konto an. Eltern sehen alles in Elternsprache, Philip sieht alles in Kindersprache und ohne Prozentzahlen (Spürnase-Kapitel erst, wenn er sie gelesen hat).

## Weg und Manifest

- **Weg:** die drei Stationen, Leitsätze, KI-Regeln und Signale (aus dem früheren Lernweg-Artifact), dazu „Für Philip“ mit Forscher-Pass, Lern-Tricks und Projekt-Werkstatt sowie „Für Eltern“.
- **Manifest:** was die Eltern Philip versprechen und was Philip sich wünscht. Philips Teil ist ein Entwurf, den er selbst umschreibt.
- Beide liegen als Fassungen in `family_docs`. Jeder kann eine Änderung vorschlagen; sie gilt, wenn alle zugestimmt haben (`doc_approvals`). Der Verlauf bleibt erhalten.
- „Was wir unterwegs merken“ (`family_notes`) sammelt Erfahrungen als Grundlage für Änderungen.
- Philips Pass und Projekte liegen in `app_progress` unter `lernweg`.

## Lernstände: drei Bereiche

- **Überblick:** Trainingstage der letzten zwei Wochen, Trefferquote je Fach im Vergleich zur Vorwoche, Hinweise, wo es hakt, und der Stand in jeder App (Mathe-Stufen, Vokabel-Boxen, Deutsch, Tie-Break-Texte mit Fehlern, Lesen, Tests).
- **Aufgaben:** alle Inhalte zum Durchblättern, mit Lösung und Philips Stand je Aufgabe. Bei Mathe steht, was jede Stufe verlangt, weil die Aufgaben in der App gewürfelt werden.
- **Entwicklung:** Trefferquote über die Zeit, Übungsmenge, Wortschatz, Mathe-Stufen, Lesetempo, Schreiben und ein Wochenvergleich.

## Woher die Daten kommen

- `app_progress` – aktueller Stand je App (schreiben die Apps über `familie-sync.js`)
- `activity_log` – Ereignisse wie gelesene Kapitel oder Tie-Breaks
- `progress_daily` – tägliche Momentaufnahme jedes Stands. Ein Trigger in der Datenbank legt sie an, sobald eine App speichert; die Apps selbst mussten dafür nicht geändert werden. Seit 7.11.2026.

Die Inhalte (Vokabeln, Fälle, Testkarten) lädt das Cockpit direkt aus den anderen Repos (`../lern-match/inhalte.js` usw.). Neue Inhalte erscheinen dadurch automatisch.

Neuer Test im Testtrainer: Eintrag in `testtrainer/tests.js` genügt, das Cockpit zeigt ihn dann mit an.

Wenn sich Rechenbereiche oder Stufen in Lern-Match ändern, die Tabellen `SKILLS`, `KAP` und `LEVELS` in `index.html` mitziehen.

## Anmeldung

Gleiche Anmeldung wie in den Apps (`familie-sync.js`, gemeinsamer Browserspeicher unter thmsbauer1.github.io). Diese Kopie hat zusätzlich `FS.rest()` für lesende Abfragen; die Datei kann so auch in die anderen Repos übernommen werden.
