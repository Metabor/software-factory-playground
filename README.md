# Adressbuch

Hier entsteht ein kleines Adressbuch als Kommandozeilenprogramm.

- **Sprache:** Python 3, nur Standardbibliothek. Tests mit `unittest` (`python3 -m unittest`).
- **Speicherung:** lokal in einer Datei im Dateisystem, keine Datenbank, kein Netzwerk.

## Aufträge

Die Aufträge liegen im Dateisystem unter `tickets/`. Jeder Auftrag ist eine Markdown-Datei. Sein
Zustand ist der Ordner, in dem er liegt; ein Auftrag wechselt den Zustand, indem er verschoben wird.
Was ein Zustand bedeutet, steht in der `README.md` des jeweiligen Ordners.

## Software-Fabrik (Playground)

Dieses Repo ist ein Playground: ein kleines Übungsprojekt, an dem sich eine Software-Fabrik mit Agenten
ausprobieren lässt. Oben kommt ein Auftrag rein, unten kommt laufende Software raus, und jeder Auftrag
läuft durch alle Stationen.

Die Fabrik liegt als Vorlage unter `.claude/commands/`. Sie ist bewusst leer von Werkzeugen, Sprachen
und Projekten: Jede Station beschreibt ihr Ziel und was zu tun ist. Was hier konkret gilt, füllt das
Setup.

### Einrichten

1. Das Repo klonen und in Claude Code öffnen.
2. `/factory:setup` ausführen. Das Setup sieht sich das Projekt an, füllt die Lücken der Vorlage, fragt
   nur, wo etwas unklar ist oder fehlt, und baut am Ende den Maschinenraum: die Seite, auf der ihr seht,
   was läuft, und der Fabrik antwortet.
3. `/loop /factory` startet den Leitstand. Eine einzelne Station läuft mit
   `/factory:<station> <Auftrag>`, zum Beispiel `/factory:plan AB-1`.

### Was das hier ist, und was nicht

Die Vorlage taugt als Gerüst für eine echte Fabrik. In dem Zustand, in dem sie hier liegt, ist sie aber
keine: Sie muss dafür noch stark individuell erweitert und gefestigt werden. Jede Station braucht eure
Werkzeuge, eure Regeln und eure Erfahrung, und was eine Station bei euch wirklich leisten muss, zeigt
sich erst an echten Aufträgen. Verlasst euch im Playground auf nichts, was ihr nicht selbst geprüft
habt.

Der wichtigste Tipp für den Ausbau: Bevor ihr eine Station füllt, klärt, wie dieser Schritt richtig
wäre, mit aller Zeit und allen Ressourcen der Welt. Erst das Ideal, dann Stück für Stück übertragen,
was mit Agenten möglich ist. Für jeden Teilschritt klärt ihr: Was bleibt beim Menschen, und was muss
der Agent dafür verdichten?
