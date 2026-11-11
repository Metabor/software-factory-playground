---
description: "Software-Fabrik: Nacharbeit an einer bestehenden Änderung. Änderungswünsche aus Prüfung und Review, rote Prüfungen, Konflikte mit dem Hauptstand."
argument-hint: "<Auftrag> <was zu tun ist>"
---

# Nacharbeit: $ARGUMENTS

**Lies zuerst `.claude/commands/factory/regeln.md`** (Leitplanken und Verhalten).

## Ziel
Die Rückschleife der Fabrik: Eine eingereichte Änderung wird korrigiert und geht zurück in die Station,
aus der der Wunsch kam.

## Was zu tun ist
Es gelten die Regeln von Station 5 (`.claude/commands/factory/umsetzen.md`, Schritte 2 bis 6). Alles,
was an einer Änderung offen ist, wird in einem Durchgang erledigt.

- **Prüfung rot.** Ursache finden und belegen, dann beheben. Ein Test, der absichtlich rot ist, weil er
  einen gemeldeten Fehler zeigt, wird nicht „repariert", sondern gemeldet.
- **Konflikt mit dem Hauptstand.** Erst verstehen, was die andere Änderung wollte (ihr Auftrag, ihre
  Beschreibung), dann auflösen. Nie raten, welche Seite gewinnt.
- **Änderungswünsche: kritisch, nicht gehorsam.** Je Wunsch die Absicht verstehen. Im Zweifel folgen.
  Aber anhalten und mit Begründung und Alternative melden, wenn der Wunsch
  - das Problem gegen ein schwereres tauscht,
  - Nebenwirkungen hat, die der Wünschende vermutlich nicht bedacht hat,
  - einer Anforderung oder festgehaltenen Entscheidung widerspricht,
  - einen Umbau über den Auftrag hinaus verlangt.
- **Offene Punkte nicht stillschweigend vertagen.** Was im selben Auftrag gelöst wird und was ein
  Folgeauftrag wird, regelt „Bei euch".
- **Danach:** die betroffenen Prüfungen und, bei mehr als einer Kleinigkeit, den zweiten Blick
  wiederholen. Erledigte Anmerkungen als erledigt kennzeichnen; offen bleibt nur, was bewusst nicht
  umgesetzt wurde. Antworten an Dritte schreibt der Mensch.

## Ergebnis
Neuer Stand der Änderung mit grüner Prüfung. Bericht: je Wunsch angenommen, abgelehnt oder gemeldet, mit
Grund · ob sich seit dem Testlauf Verhalten geändert hat (dann dort nur die betroffenen Fälle neu) · ob
die Dokumentation betroffen ist · Statuszeile.

## Methode
Ursachenanalyse statt Symptombehandlung (z. B. „5 Why").

## Bei euch
| Lücke | Leitfrage | Wert |
|---|---|---|
| Anmerkungen | Wo stehen Änderungswünsche, und wie werden sie als erledigt gekennzeichnet? | {{OFFEN}} |
| Umfang | Was wird im selben Auftrag gelöst, was wird ein Folgeauftrag? Was geschieht mit optionalen Wünschen? | {{OFFEN}} |
| Erneute Prüfung | Wann muss nach einer Nacharbeit erneut getestet oder erneut reviewt werden? | {{OFFEN}} |
