---
description: "Software-Fabrik, Station 6 (das Was): aus Auftrag und Akzeptanzkriterien ableiten, was getestet werden muss. Führt nichts aus."
argument-hint: "<Auftrag>"
---

# Station 6 — Prüfen, das Was: $ARGUMENTS

**Lies zuerst `.claude/commands/factory/regeln.md`** (Leitplanken und Verhalten).

## Ziel
Festlegen, was getestet werden müsste, ohne zu fragen, ob oder wie es testbar ist. Wer das Was und das
Wie mischt, testet das Einfache statt das Wichtige. Darum ist der Testlauf eine eigene Station.

## Was zu tun ist
Nichts ausführen, nichts ändern.

1. **Akzeptanzkriterien zuerst**, wörtlich aus dem Auftrag, bevor du die Änderung liest. Getestet wird
   das Geforderte, nicht das Gebaute.
2. **Die Leitfrage:** Wo würde man zuerst merken, dass etwas nicht funktioniert? Dort ansetzen.
3. **Was ist schon bewiesen?** Nur anrechnen, was ausdrücklich belegt ist: ein vorhandener Test, ein
   Ergebnis der zentralen Prüfung. Vermutungen zählen nicht.
4. **Testfälle schreiben:** Ausgangslage, Handlung, erwartetes Ergebnis, welches Kriterium er belegt.
   Auch Fehlerfälle und Grenzen, nicht nur der gute Fall.
5. **Rückwärts prüfen:** Zu jeder Anforderung mindestens eine Prüfung. Kriterien ohne Prüfung werden
   ausdrücklich als nicht abgedeckt genannt.
6. **Risiken einordnen.** Alles, was kein automatischer Test abdecken wird, bekommt eine Klasse:

   | Klasse | Was der Plan dazu sagt |
   |---|---|
   | Nur ein Mensch kann es testen (Fachwissen, Zugang) | die genauen Schritte |
   | Nur in Produktion sichtbar (echte Daten, echte Last) | was nach dem Ausrollen zu beobachten ist |
   | Vorher nicht testbar (z. B. ein Fremdsystem fällt aus) | woran man merkt, dass es eingetreten ist, und was man dann tut |

   Was sich nicht testen lässt, wird so zum bewussten Risiko statt zu einer Überraschung.

## Ergebnis
Der Testplan am vereinbarten Ort, mit dem Stand der Änderung, auf den er sich bezieht. Bericht: Zahl der
Fälle · Abdeckung je Kriterium · Risiken nach Klasse · offene Fragen · Statuszeile.

## Methode
Risikobasiertes Testen. Anforderungs-Rückverfolgbarkeit („zu jeder Anforderung eine Prüfung",
V-Modell). Äquivalenzklassen und Grenzwerte für die Fallauswahl.

## Bei euch
| Lücke | Leitfrage | Wert |
|---|---|---|
| Plan-Ablage | Wo liegt der Testplan? | `.tmp/<Auftrag>/testplan.md` |
| Regressionsbereiche | Welche Bereiche müssen bei jeder Änderung mitgeprüft werden? | {{OFFEN}} |
| Fachliche Prüfer | Wer kann testen, was der Agent nicht kann? | {{OFFEN}} |
