---
description: "Software-Fabrik, Station 6 (das Wie): den Testplan am laufenden System ausführen, Funde zu Tests machen und einen Bericht hinterlassen."
argument-hint: "<Auftrag>"
---

# Station 6 — Prüfen, das Wie: $ARGUMENTS

**Lies zuerst `.claude/commands/factory/regeln.md`** (Leitplanken und Verhalten).

## Ziel
Der Beweis am laufenden System, dass die Änderung das Geforderte tut.

## Was zu tun ist
Voraussetzung ist der Testplan. Ohne Plan wird nicht getestet. Bezieht sich der Plan auf einen älteren
Stand der Änderung: melden (`BLOCKIERT`), nicht trotzdem testen.

1. **Je Fall die passende Ebene wählen:** die niedrigste, auf der er sich beweisen lässt. Ein
   Komponententest vor einem Test über mehrere Teile, der vor dem Bedienen der Oberfläche.
2. **Umgebung herstellen**, die der Fall braucht. Was der Fall voraussetzt, ist deine Aufgabe; abgegeben
   wird nur, was wirklich einen Menschen braucht (eine fachliche Entscheidung, ein Zugang).
3. **Fall für Fall:** ausführen, das Ergebnis als Beleg festhalten, Urteil fällen. Ein Fall ohne Beleg
   ist nicht bestanden.
4. **Urteile unabhängig prüfen lassen.** Ein Prüfer mit frischem Kontext liest Fall und Beleg und sagt,
   ob der Beleg das Urteil trägt.
5. **Ein Fund wird ein Test.** Erst ein automatischer Test, der den Fehler zeigt, dann die Korrektur.
   Ist die Korrektur eine fachliche Entscheidung: melden, nicht selbst entscheiden. Der Stand bleibt nie
   rot zurück.
6. **Akzeptanzkriterien abgleichen:** Für jedes Kriterium: belegt, teilweise, fehlt.
7. **Aufräumen.** Die Umgebung so hinterlassen, wie sie war.

Teste, was Auftrag und Entscheidungen verlangen, nicht mehr. Ein Lauf ohne Fund ist ein gutes Ergebnis.

## Ergebnis
Der Bericht am vereinbarten Ort: Stand der Änderung, den der Lauf vertritt · Tabelle der Fälle mit
Urteil und Beleg · Abgleich der Kriterien · neue Tests · was nicht ausgeführt werden konnte und warum ·
offene Fragen.

**Bestanden** nur, wenn jeder Fall ausgeführt und beurteilt ist und kein Kriterium fehlt oder nur
teilweise belegt ist. Ein nicht ausgeführter Fall ist kein bestandener Fall.

## Methode
Testpyramide (Cohn) für die Wahl der Ebene. Exploratives Testen mit Test-Chartern, wo ein Fall
Erkundung braucht.

## Bei euch
| Lücke | Leitfrage | Wert |
|---|---|---|
| Testumgebung | Wo läuft das System für den Test, und wie kommt man an Testdaten? | {{OFFEN}} |
| Testebenen | Welche Ebenen gibt es bei euch, und wie startet man jede? | {{OFFEN}} |
| Belege | Was gilt als Beleg, und wo wird er abgelegt? | {{OFFEN}} |
| Bericht-Ablage | Wo liegt der Testbericht? | `.tmp/<Auftrag>/testbericht.md` |
| Auftragszustand danach | In welchen Zustand geht der Auftrag nach bestandenem Lauf, und wer setzt ihn? | {{OFFEN}} |
