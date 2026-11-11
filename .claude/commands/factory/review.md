---
description: "Software-Fabrik, Station 8: das Review vorbereiten. Der Agent stellt die Änderung als ihr Autor vor, der Mensch fragt nach. Nur lesend."
argument-hint: "<Auftrag>"
---

# Station 8 — Review: $ARGUMENTS

**Lies zuerst `.claude/commands/factory/regeln.md`** (Leitplanken und Verhalten).

## Ziel
Wissen teilen, nicht kontrollieren. Ein Programm lebt als Theorie im Team: warum es so ist, wie es ist.
Schreibt der Agent, entsteht diese Theorie nicht mehr nebenbei. Das Review ist der Ort, an dem sie
entsteht. Am Ende ist es auch der Code des Menschen.

Die Qualitätsschleife (Stationen 5 und 6) ist vorher abgeschlossen. Das Review sucht nicht nach
Tippfehlern.

## Was zu tun ist
Nichts verändern. Du bist der Autor und erklärst; der Mensch ist der Kollege und fragt.

**1. Die Änderung prüfen, bevor du sie vorstellst.**
- Enthält sie nur, was der Auftrag verlangt?
- Ist ihre Beschreibung aktuell und aus Fakten?
- Liegt das Ergebnis von Station 7 vor?
- Ist benannt, was ausgelassen wurde und deshalb ungeprüft ist?

**2. Als Autor vorstellen**, kurz, in genau diesen Teilen:
1. **Was und warum:** was die Änderung tut und warum so. Welche Anforderungen wie belegt sind.
2. **Entscheidungen beim Bauen:** Annahmen, Abweichungen vom Plan, Abwägungen.
3. **Nur verschoben, extrahiert, umbenannt:** was keine Aufmerksamkeit braucht, getrennt von dem, was
   sich wirklich ändert.
4. **Hier brauche ich deinen Blick:** die Stellen, an denen nachgefragt werden sollte, mit Datei und
   Zeile.
5. **Tests:** welcher Test welche Anforderung belegt, welche ohne die Änderung rot wären.
6. **Risiken:** was nicht testbar war und bewusst getragen wird.

**3. Das Gespräch.** Der Mensch fragt, bis es klar ist, bringt Kontext ein, den du nicht hast, und
schleift die Lösung nach. Muss er viel fragen, ist das ein Befund: Es ist nicht klar, was passiert und
warum. Gibt es eine bessere Lösung, wird sie gebaut (`factory:nacharbeit`).

**4. Was über den Einzelfall hinausgeht**, was er erklärt oder korrigiert hat, geht an Station 11.

## Ergebnis
Die Befunde aus Schritt 1 · die Vorstellung · wer nach „Bei euch" noch reviewen sollte · Statuszeile. Die Station ist erst fertig, wenn der Mensch verstanden und zugestimmt
hat.

## Methode
Structured Walkthrough (Yourdon): Der Autor führt durch, der Kollege fragt. „Programming as Theory
Building" (Naur) für das Warum. Modern Code Review (Bacchelli/Bird): Der Hauptnutzen ist Verständnis
und bessere Lösungen, nicht Fehlersuche.

## Bei euch
| Lücke | Leitfrage | Wert |
|---|---|---|
| Wer reviewt | Wer reviewt welche Änderung? | {{OFFEN}} |
| Wo | Wo findet das Review statt, und wo landen Nachfragen und Urteile? | {{OFFEN}} |
| Weitere Reviewer | Wann kommen weitere Reviewer dazu, und wie erfahren sie davon? | {{OFFEN}} |
| Zustimmung | Was gilt als Zustimmung, und was passiert, wenn niemand reagiert? | {{OFFEN}} |
