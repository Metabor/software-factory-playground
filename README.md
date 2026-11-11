# Adressbuch

Hier entsteht ein kleines Adressbuch als Kommandozeilenprogramm.

- **Sprache:** Python 3, nur Standardbibliothek. Tests mit `unittest` (`python3 -m unittest`).
- **Speicherung:** lokal in einer Datei im Dateisystem, keine Datenbank, kein Netzwerk.

## Aufträge

Die Aufträge liegen im Dateisystem unter `tickets/`. Jeder Auftrag ist eine Markdown-Datei. Sein
Zustand ist der Ordner, in dem er liegt; ein Auftrag wechselt den Zustand, indem er verschoben wird.
Was ein Zustand bedeutet, steht in der `README.md` des jeweiligen Ordners.
