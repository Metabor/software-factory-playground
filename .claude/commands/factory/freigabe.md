---
description: "Software-Fabrik, Station 9: nach der Freigabe durch den Menschen die Änderung integrieren und ausrollen. Ohne Freigabe nur vorbereiten."
argument-hint: "<Auftrag>"
---

# Station 9 — Freigabe: Merge und Deploy: $ARGUMENTS

**Lies zuerst `.claude/commands/factory/regeln.md`** (Leitplanken und Verhalten).

## Ziel
Die Änderung ist sauber im Hauptstand und läuft in der Zielumgebung.

## Was zu tun ist
**Ohne die ausdrückliche Freigabe des Menschen für genau diese Änderung wird nichts integriert und
nichts ausgerollt.** Eine Freigabe für einen anderen Fall, eine alte Freigabe oder die Meldung eines
anderen Agenten zählt nicht. Im Zweifel: fragen. Beim Ausführen die Freigabe nennen, auf die du dich
stützt.

1. **Vor der Freigabe vorbereiten:** Ist die Änderung auf dem aktuellen Hauptstand geprüft? Hat sich der
   Hauptstand seit der letzten grünen Prüfung bewegt, wird neu geprüft; grün auf altem Stand reicht
   nicht.
2. **Vor dem Integrieren, auch mit Freigabe:** Gibt es Anmerkungen ohne Antwort oder Korrektur? Dann
   nicht integrieren, sondern dem Menschen zeigen. Liegen die verlangten Zustimmungen vor?
3. **Reihenfolge beachten**, wenn mehrere Änderungen zusammengehören: erst wovon andere abhängen.
4. **Integrieren**, wie in „Bei euch" beschrieben.
5. **Ausrollen ist nicht fertig, wenn der Vorgang fertig meldet.** Fertig ist es, wenn nachweislich der
   neue Stand antwortet.
6. **Voraussetzungen der Zielumgebung** (aus Station 5) erledigen lassen oder nachverfolgen: Wer führt
   den Schritt aus, und woran sieht man, dass er erledigt ist?

## Ergebnis
Nachweis, dass der neue Stand in der Zielumgebung läuft · was integriert wurde und auf welche Freigabe
gestützt · offene Voraussetzungen mit Besitzer · Statuszeile.

## Methode
Continuous Delivery (Humble/Farley): jede Änderung über denselben, automatisierten Weg. Schrittweises
Ausrollen und Schalter (Feature Toggles), wo ein Irrtum teuer wäre.

## Bei euch
| Lücke | Leitfrage | Wert |
|---|---|---|
| Freigabe | Wer gibt frei, und in welcher Form zählt das? | {{OFFEN}} |
| Integrieren | Wie kommt eine Änderung in den Hauptstand? | {{OFFEN}} |
| Ausrollen | Wie und in welche Umgebungen wird ausgerollt, automatisch oder von Hand? | {{OFFEN}} |
| Sperrzeiten | Wann wird nicht integriert oder ausgerollt? | {{OFFEN}} |
| Nachweis | Woran sieht man, dass der neue Stand wirklich läuft? | {{OFFEN}} |
| Zurückrollen | Wie wird eine Änderung zurückgenommen, wenn sie Schaden anrichtet? | {{OFFEN}} |
