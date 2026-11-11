---
description: "Software-Fabrik, Stationen 1–2: Aufträge sammeln und gegen die Bereit-Regel prüfen. Nur lesend."
argument-hint: "[<Auftrag> …]"
---

# Station 1–2 — Auftrag kommt rein, ist er bereit?: $ARGUMENTS

**Lies zuerst `.claude/commands/factory/regeln.md`** (Leitplanken und Verhalten).

## Ziel
Wissen, was es zu tun gibt, und nur das als ziehbar melden, was ohne Raten lieferbar ist.

## Was zu tun ist

**1. Sammeln.** Ohne Argument: alle Aufträge aus der Auftragsquelle, die zum Ziehen anstehen. Mit
Argument: nur die genannten. Je Auftrag alles lesen, was dazugehört, je nach seiner Form: Beschreibung,
Diskussion, Anhänge, Verknüpftes.

**2. Bereit-Regel anwenden.** Ein Auftrag ist bereit, wenn alles gilt:

1. **Er gehört zu uns.** Er liegt in unserem Zuständigkeitsbereich (siehe „Bei euch").
2. **Niemand hat ihn begonnen.** Kein anderer Bearbeiter, kein begonnener Änderungsstand.
3. **Nichts blockiert ihn.** Kein offener Vorgänger, keine unerfüllte Abhängigkeit.
4. **Ziel und Akzeptanzkriterien sind klar.** Was geliefert werden soll und woran man erkennt, dass es
   fertig ist, steht da. Der Umfang ist abgegrenzt.

**3. Nicht bereit heißt: zurück mit konkreten Fragen.** Nie raten. Erst nachsehen, was Dokumentation und
Code beantworten. Was bleibt, sind die konkreten Fragen, die den Auftrag bereit machen würden.

**4. Einordnen.** Die bereiten Aufträge nach Umfang beschreiben (betroffene Teile, Risiken) und nennen, welche exklusiven Ressourcen sie brauchen.

## Ergebnis
Eine Tabelle: Auftrag · bereit? · wenn nicht: welche Regel scheitert und die konkreten Fragen · Umfang ·
benötigte Ressourcen · Auffälligkeiten (Widersprüche, nötige Annahmen). Danach die Statuszeile.

## Methode
Definition of Ready (Scrum); INVEST-Kriterien für gut geschnittene Aufträge.

## Bei euch
| Lücke | Leitfrage | Wert |
|---|---|---|
| Auftragsquelle | Was ist bei euch der Auftrag, und wo liegt er? | {{OFFEN}} |
| Zum Ziehen anstehend | Woran erkennt der Agent die Aufträge, die gezogen werden dürfen? | {{OFFEN}} |
| Zuständigkeit | Welche Aufträge gehören zu euch, welche nie? | {{OFFEN}} |
| Kein Auftrag | Was sieht aus wie ein Auftrag, ist aber keiner? | {{OFFEN}} |
| Bereit-Regel | Was verlangt ihr zusätzlich, bevor ein Auftrag bereit ist, und wer pflegt die Regel? | {{OFFEN}} |
| Rückweg | Wohin gehen die Fragen zu einem nicht bereiten Auftrag? | {{OFFEN}} |
