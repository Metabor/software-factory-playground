# Übungsaufträge: Adressbuch

> **BEISPIEL.** Erfundene Aufträge für eine Testanwendung.

Jeder Auftrag ist eine Datei. Sein Zustand ist der Ordner, in dem er liegt; ein Auftrag wechselt den
Zustand, indem er verschoben wird. Was ein Zustand bedeutet, steht in der `README.md` des Ordners.

| Ordner | Zustand |
|---|---|
| `backlog/` | noch nicht fertig, wird nicht begonnen |
| `selected-for-development/` | fertig zum Entwickeln, kann begonnen werden |
| `in-progress/` | in Arbeit |
| `in-review/` | in Prüfung |
| `done/` | erledigt |

## Gilt für alle Aufträge
- Die Aufträge beschreiben, was das Adressbuch können soll, nicht wie es gebaut wird. Wie Befehle,
  Dateien und Meldungen heißen, entscheidet die Umsetzung.
- Eine Fehlbedienung wird verständlich gemeldet und verändert nichts.
- Jeder Auftrag bringt automatische Tests mit.
