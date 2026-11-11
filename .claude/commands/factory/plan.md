---
description: "Software-Fabrik, Station 4: Kontext zum Auftrag holen und den Plan schreiben, bevor gebaut wird. Nur lesend."
argument-hint: "<Auftrag>"
---

# Station 4 — Kontext und Plan: $ARGUMENTS

**Lies zuerst `.claude/commands/factory/regeln.md`** (Leitplanken und Verhalten).

## Ziel
Erst verstehen, dann bauen. Am Ende steht ein Plan, der ohne offene Frage umsetzbar ist.

## Was zu tun ist
Nichts verändern außer dem Plan selbst: kein Code, keine Änderung am Auftrag.

1. **Auftrag vollständig lesen**, mit allem, was dazugehört. Die Diskussion zu einem Auftrag enthält oft die
   entscheidende Klarstellung. Die Akzeptanzkriterien wörtlich festhalten.
2. **Kontext holen.** Was sagt die Dokumentation zu dem Thema (Regeln, Prozesse, frühere
   Entscheidungen)? Was gilt im Projekt (Kontextquellen in „Bei euch")? Ein Widerspruch zwischen
   Doku, Auftrag und Code ist ein Befund.
3. **Ist-Zustand im Code.** Wo sitzt das Verhalten heute? Fundstellen mit Datei und Zeile, bezogen auf
   einen festen Stand.
4. **Vorbilder suchen.** Wie ist dasselbe Muster an anderer Stelle schon gelöst? Dem Vorbild folgen,
   statt ein neues Muster einzuführen.
5. **Unklarheiten einordnen.** Teuer rückgängig zu machen und ändert, was geliefert wird: offene Frage
   mit Optionen und Empfehlung. Billig zu korrigieren: Annahme. Fällt eine Entscheidung unter
   „Entscheidungen vor dem Bauen" (siehe „Bei euch"), ist sie immer eine offene Frage, auch wenn du
   eine klare Empfehlung hast.
6. **Bei großer Unsicherheit erst zur Probe bauen:** einen kleinen Wegwerf-Versuch vorschlagen, der die
   Unsicherheit klärt, statt sie in den Plan zu schreiben.
7. **Plan schreiben** und am vereinbarten Ort ablegen.

## Ergebnis
Der Plan, mit diesen Abschnitten (leere bleiben mit „—" stehen):
Ziel und Akzeptanzkriterien (wörtlich) · Kontext aus der Dokumentation · Ist-Zustand (Fundstellen) ·
Vorbilder · Lösungsansatz · betroffene Teile · Teststrategie (welche Tests neu sind und welche ohne die
Änderung rot wären) · benötigte Ressourcen · Risiken, auch für das Ausrollen · Annahmen · offene Fragen ·
Umfang.

Statuszeile: `FERTIG` ohne offene Frage, sonst `FRAGE: …`.

## Methode
Spike oder Prototyp („erst zur Probe bauen, dann richtig", Royce); Architecture Decision Records
(Nygard) für Entscheidungen, die bleiben.

## Bei euch
| Lücke | Leitfrage | Wert |
|---|---|---|
| Kontextquellen | Was muss ein Agent bei euch wissen, bevor er anfängt, und wo steht das? | {{OFFEN}} |
| Verbindliche Entscheidungen | Wo stehen Entscheidungen, denen ein Plan nicht widersprechen darf? | {{OFFEN}} |
| Entscheidungsspeicher | Wo stehen Entscheidungen und Annahmen zu diesem Auftrag? | `.tmp/<Auftrag>/entscheidungen.md` |
| Entscheidungen vor dem Bauen | Welche Entscheidungen werden mit dem Menschen besprochen, bevor gebaut wird (zum Beispiel Aufbau, Datenformat, Schnittstellen)? | {{OFFEN}} |
| Plan-Ablage | Der Plan liegt in `.tmp/<Auftrag>/plan.md`. Wer muss ihn sehen, bevor gebaut wird? | {{OFFEN}} |
| Plan-Prüfung | Bei welchen Aufträgen prüft jemand Unabhängiges den Plan, bevor gebaut wird? | {{OFFEN}} |
