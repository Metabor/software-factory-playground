---
description: "Software-Fabrik, Station 5 (Bau-Loop): den Plan umsetzen, selbst prüfen, einen zweiten Blick mit frischem Kontext holen und die Änderung zur Prüfung stellen."
argument-hint: "<Auftrag>"
---

# Station 5 — Umsetzen (Bau-Loop): $ARGUMENTS

**Lies zuerst `.claude/commands/factory/regeln.md`** (Leitplanken und Verhalten).

## Ziel
Die Änderung, die den Auftrag vollständig liefert: getestet, selbst geprüft, von einem zweiten Blick
gesehen. Der Mensch sieht den Code erst, wenn dieser Loop fertig ist.

## Was zu tun ist
Voraussetzung ist der Plan aus Station 4. Arbeite selbständig: suchen statt fragen, bestehenden Mustern
folgen, nicht mehr ändern als nötig.

1. **Vorbereiten.** Getrennten Änderungsstand anlegen (nie auf dem Hauptstand). Umgebung bauen. Die
   vorhandenen Prüfungen müssen grün sein, bevor du etwas änderst; sonst zuerst die Ursache klären.
2. **Test zuerst.** Neues Verhalten: erst der Test, der es beschreibt, dann der Code. Fehler: erst ein
   Test, der ihn zeigt und rot ist, dann die Korrektur.
3. **Kleine Schritte**, jeder mit Test, nach jedem die Prüfungen laufen lassen. Wandert Logik an eine
   andere Stelle, wandern ihre Tests mit; ein Test verschwindet nur, wenn sein Verhalten verschwindet.
4. **Im Vorbeigehen aufräumen**, was du ohnehin anfasst und was klein und gefahrlos ist. Alles mit
   möglicher Verhaltensänderung oder außerhalb der berührten Stellen nur melden.
5. **Selbst prüfen.** Alle Akzeptanzkriterien erfüllt? Nichts offen gelassen? Was könnte diese Änderung
   an anderer Stelle brechen: Wer ruft das Geänderte auf, wer liest die geänderten Daten?
6. **Zweiter Blick.** Ein unabhängiger Prüfer mit frischem Kontext liest die Änderung: Fehler,
   Randfälle, unnötige Komplexität, fehlende Tests, Verstöße gegen die Projektregeln, Sicherheit. Was
   schwer wiegt, wird behoben; danach erneut prüfen lassen.
7. **Abgleich mit dem Auftrag.** Ein weiterer unabhängiger Prüfer vergleicht Auftrag (mit Kommentaren)
   und Änderung: Ist jedes Kriterium umgesetzt, richtig und getestet?
8. **Läuft es auch dort, wo es hin soll?** Was braucht die Zielumgebung, das nicht in der Änderung
   steckt: Einstellungen, Geheimnisse, Zugänge, Datenänderungen, ein Schritt von Hand? Jeder solche
   Punkt wird nachverfolgt, bis ihn jemand erledigt hat. Ein Satz in der Beschreibung der Änderung
   reicht dafür nicht.
9. **Zur Prüfung stellen.** Die Änderung einreichen, mit einer Beschreibung aus Fakten: was und warum,
   was sich im Verhalten ändert, welche Tests ohne die Änderung rot wären, was bewusst nicht enthalten
   ist. Warten, bis die zentrale Prüfung durch ist.

Nach mehreren gleichartigen Fehlversuchen: anhalten und melden, statt dich festzubeißen.

## Ergebnis
Die eingereichte Änderung mit grüner Prüfung, und ein Bericht: was umgesetzt wurde · Tests ·
Ergebnisse der beiden Prüfer · Annahmen und Abweichungen vom Plan · Voraussetzungen für die
Zielumgebung · Statuszeile.

## Methode
Test-Driven Development: rot, grün, aufräumen (Beck). Mehrmals täglich integrieren (Fowler).
Code-Inspektion (Fagan) als Vorbild für den zweiten Blick. Boy-Scout-Regel (Martin).

## Bei euch
| Lücke | Leitfrage | Wert |
|---|---|---|
| Änderungsweg | Wie entsteht eine Änderung getrennt vom Hauptstand, und wie wird sie zur Prüfung gestellt? | {{OFFEN}} |
| Benennung | Wie heißen Änderungen, und wie sieht ihre Beschreibung aus? | {{OFFEN}} |
| Bauen und Starten | Wie wird das System gebaut und lokal gestartet? | {{OFFEN}} |
| Automatische Prüfungen | Welche Prüfungen gibt es (Tests, statische Analyse), und wie startet man sie? | {{OFFEN}} |
| Zentrale Prüfung | Was prüft eine Änderung automatisch, sobald sie eingereicht ist, und wo sieht man das Ergebnis? | {{OFFEN}} |
| Projektregeln | Welche Regeln muss Code bei euch einhalten, und wo stehen sie? | {{OFFEN}} |
| Zweiter Blick | Wer oder was prüft unabhängig (Skill, Agent, Checkliste)? | {{OFFEN}} |
| Sicherheitsprüfung | Wie wird eine Änderung auf Sicherheit geprüft? | {{OFFEN}} |
| Sichtprüfung | Wie wird geprüft, was nur an der Oberfläche sichtbar ist? | {{OFFEN}} |
| Zielumgebung | Worin unterscheidet sich die Zielumgebung von der lokalen, und wo sieht man das? | {{OFFEN}} |
| Auftragszustand danach | In welchen Zustand geht der Auftrag, wenn die Umsetzung fertig ist? | {{OFFEN}} |
