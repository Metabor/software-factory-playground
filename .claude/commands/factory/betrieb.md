---
description: "Software-Fabrik, Station 10: nachsehen, ob die ausgerollte Änderung im Betrieb tut, was sie soll, und Signale aus dem Betrieb zu neuen Aufträgen machen."
argument-hint: "<Auftrag>"
---

# Station 10 — Betrieb: läuft es?: $ARGUMENTS

**Lies zuerst `.claude/commands/factory/regeln.md`** (Leitplanken und Verhalten).

## Ziel
Fertig heißt nicht „integriert", sondern „läuft nachweislich". Und nichts bleibt ohne Besitzer.

## Was zu tun ist
Nur in Umgebungen und mit Zugängen, die „Bei euch" dafür nennt. Nie etwas in Produktion
provozieren.

1. **Akzeptanzkriterien nachprüfen**, wo es billig und gefahrlos geht: Tut das System in der
   Zielumgebung, was der Auftrag verlangt? Was du dafür anlegst, räumst du wieder ab.
2. **Betriebssignale ansehen:** Sind seit dem Ausrollen Fehler aufgetreten, die zu dieser Änderung
   passen (betroffener Bereich, erstes Auftreten nach dem Ausrollen)?
3. **War ein Fehler der Anlass des Auftrags:** nachsehen, ob er nach dem Ausrollen noch auftritt. Als
   behoben gilt er erst, wenn die Korrektur überall läuft, wo er auftrat.
4. **Die Risiken aus Station 6** („nur in Produktion sichtbar", „vorher nicht testbar"): Ist das
   Erkennungszeichen eingetreten?
5. **Nachweis festhalten.** Ist ein Nachweis noch nicht möglich: das sagen und die Beobachtung als
   Wiedervorlage stehen lassen.
6. **Auftrag schließen**, wenn der Nachweis da ist. Was danach noch zu tun bleibt (Schritte von Hand,
   Folgeaufträge, Beobachtungen), bekommt einen Besitzer und einen Termin.
7. **Signale werden neue Aufträge.** Ein Fehler oder Befund, der kein Teil dieses Auftrags ist, geht als
   neuer Auftrag in die Auftragsquelle (Station 1), nicht in eine Notiz.

Scheitert ein Akzeptanzkriterium im Betrieb: zurück an Station 5, und der Mensch erfährt es.

## Ergebnis
Je Kriterium: was geprüft wurde, erwartet, tatsächlich, Urteil · Betriebssignale seit dem Ausrollen ·
offene Punkte mit Besitzer · neue Aufträge · Statuszeile.

## Methode
Observability (Protokolle, Kennzahlen, Verläufe) als Grundlage. Smoke-Test nach dem Ausrollen.
Fehlerbudgets (Site Reliability Engineering) für die Frage, wann ein Signal Handeln verlangt.

## Bei euch
| Lücke | Leitfrage | Wert |
|---|---|---|
| Wo prüfen | In welcher Umgebung darf der Agent nachprüfen, mit welchem Zugang? | {{OFFEN}} |
| Signalquellen | Wo erscheinen Fehler und Auffälligkeiten aus dem Betrieb? | {{OFFEN}} |
| Abschluss | Was muss vorliegen, damit ein Auftrag geschlossen wird, und wer schließt ihn? | {{OFFEN}} |
| Wiedervorlagen | Wo werden Beobachtungen und spätere Schritte nachverfolgt? | {{OFFEN}} |
| Neue Aufträge | Wer darf aus einem Signal einen Auftrag machen, und wie? | {{OFFEN}} |
