---
description: "Software-Fabrik, Station 11 (Lern-Loop): Retro zu einem abgeschlossenen Auftrag. Was hat Runden gekostet, und welche Regel, welcher Skill oder welche Bereit-Regel verhindert es?"
argument-hint: "<Auftrag>"
---

# Station 11 — Lernen (Lern-Loop): $ARGUMENTS

**Lies zuerst `.claude/commands/factory/regeln.md`** (Leitplanken und Verhalten).

## Ziel
Die Fabrik baut sich selbst um. Was schiefging, wird zur Regel oder zum Skill, damit dieselbe Reibung
nicht zweimal passiert.

## Was zu tun ist
Nichts verändern außer dem Retro-Bericht. Quellen: der Verlauf des Auftrags im Maschinenraum, Plan, Testbericht, die Anmerkungen aus
dem Review, die Berichte der Arbeiter.

1. **Zählen, was Runden gekostet hat:** Wie oft ging der Auftrag zurück (aus Prüfung, aus Review, nach
   „fertig")? Wie viele Fragen gingen an den Menschen?
2. **Fragen ansehen:** Welche hätte Dokumentation, Code oder der Auftrag selbst beantwortet? Welche
   kamen spät, obwohl der Plan sie hätte stellen müssen?
3. **Review ansehen:** Was hat der Mensch erklärt oder korrigiert, das über diesen Auftrag hinaus gilt?
4. **Betrieb der Fabrik:** Wo stand ein Arbeiter, wo wurde etwas verweigert oder ausgelassen?
5. **Bereit-Regel prüfen:** War der Auftrag wirklich bereit? Hätte eine schärfere Regel die Lücke
   gefangen?

Jeder Befund wird genau eines:
- eine **Regel** in dem Command der Station, in der sie angewendet wird: Datei, Abschnitt und der
  fertige Text;
- eine Änderung an einem **Skill**: als Vorschlag, wenn andere ihn mitbenutzen;
- eine schärfere **Bereit-Regel** (`factory/eingang.md`);
- **nichts**, wenn es ein Einzelfall war.

**So schreibt man Regeln:** die Regel selbst, kurz, dort, wo sie angewendet wird. Ein Grund nur, wenn
man ihn braucht, um die Regel richtig anzuwenden. Kein Datum, keine Vorfallgeschichte. Eine Anweisung
für einen Einzelfall ist keine Regel.

Regeln ändert der Mensch oder gibt sie frei. Die Fabrik schlägt vor.

## Ergebnis
Die Zahlen · die Befunde mit ihrem Ausgang · die vorgeschlagenen Texte · woran man in den nächsten
Aufträgen merkt, dass es wirkt · Statuszeile.

## Methode
Retrospektive (Derby/Larsen). Blameless Postmortem: Gesucht wird die Lücke im Prozess, nicht ein
Schuldiger. Kaizen und PDCA-Zyklus für kleine, überprüfte Verbesserungen.

## Bei euch
| Lücke | Leitfrage | Wert |
|---|---|---|
| Retro-Ablage | Wo liegt der Bericht der Retro? | `.tmp/<Auftrag>/retro.md` |
| Auslöser | Wann läuft die Retro: je Auftrag, je Woche, nach jedem Vorfall? | {{OFFEN}} |
| Kennzahlen | Woran messt ihr, ob die Fabrik besser wird? | {{OFFEN}} |
| Wer ändert Regeln | Wer darf Regeln, Skills und die Bereit-Regel ändern? | {{OFFEN}} |
| Geteilte Skills | Welche Skills nutzen andere mit, sodass Änderungen abgestimmt werden müssen? | {{OFFEN}} |
