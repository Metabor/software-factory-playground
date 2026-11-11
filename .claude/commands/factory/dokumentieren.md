---
description: "Software-Fabrik, Station 7: die Dokumentation nachziehen, die eine Änderung braucht, oder begründen, warum keine nötig ist."
argument-hint: "<Auftrag>"
---

# Station 7 — Dokumentieren: $ARGUMENTS

**Lies zuerst `.claude/commands/factory/regeln.md`** (Leitplanken und Verhalten).

## Ziel
Nach der Freigabe sagt die Dokumentation, was das System tut. Sie wird mit der Änderung geprüft und
freigegeben, nicht irgendwann danach.

## Was zu tun ist
Die Station läuft, wenn die Änderung geprüft und stabil ist, vor dem Review.

1. **Was hat sich geändert** für jemanden, der das System betreibt, anbindet oder weiterentwickelt:
   Verhalten, Abläufe, Schnittstellen, Einstellungen, Datenmodell, Schritte beim Ausrollen?
2. **Wo ist das beschrieben?** Die Seiten suchen, die es betrifft. Je Seite entscheiden: jetzt falsch,
   unvollständig oder weiterhin richtig.
3. **Nachziehen.** Falsches korrigieren, Fehlendes dort ergänzen, wo Leser es suchen würden. Nur
   beschreiben, was du an der Änderung selbst nachgesehen hast, nicht was der Plan vorhatte. Keine
   Entstehungsgeschichte in den Text.
4. **Entscheidungen festhalten.** Geh den Entscheidungsspeicher des Auftrags durch: Er liegt in `.tmp/`
   und kann jederzeit gelöscht werden. Was über den Auftrag hinaus gilt, schreibst du als Architecture
   Decision Record nach `docs/adr/` (oder an den Ort aus „Bei euch"), wenn du das nach „Bei euch"
   darfst; sonst meldest du es und schlägst die Aufzeichnung vor. Widerspricht der Auftrag einer
   früheren Entscheidung: melden. Frühere Entscheidungen werden nicht stillschweigend umgeschrieben.
   Nach dieser Station darf nichts mehr nur in `.tmp/` stehen, das jemand später vermissen würde.
5. **Schon vorher Falsches:** korrigieren, wenn es klein ist und auf einer Seite liegt, die du ohnehin
   anfasst. Sonst melden.
6. **Zur Prüfung stellen**, zusammen mit der Änderung.

## Ergebnis
Die Doku-Änderung mit je einer Zeile pro geänderter Seite. Oder „keine Dokumentationsänderung nötig" mit
den geprüften Seiten und dem Grund: auch das ist ein gültiges Ergebnis. Dazu Vorschläge für
aufzuzeichnende Entscheidungen und gefundene, nicht behobene Abweichungen. Statuszeile.

## Methode
Docs as Code: Dokumentation liegt, entsteht und wird geprüft wie Code. Diátaxis für die Frage, wohin
ein Inhalt gehört (Anleitung, Erklärung, Referenz, Tutorial). Architecture Decision Records (Nygard).

## Bei euch
| Lücke | Leitfrage | Wert |
|---|---|---|
| Doku-Bereiche | Welche Dokumentation gibt es, für wen, und wo liegt sie? Ohne eigenen Ort: `docs/` im Wurzelverzeichnis. | {{OFFEN}} |
| Tabu | Welche Dokumentation wird nie im Rahmen eines Auftrags geändert? | {{OFFEN}} |
| Entscheidungsaufzeichnung | Bleibende Entscheidungen liegen als Architecture Decision Records unter `docs/adr/`, außer es gibt schon einen Ort. Wer darf eine anlegen? | {{OFFEN}} |
| Erzeugte Doku | Welche Dokumentation wird erzeugt statt geschrieben, und wie? | {{OFFEN}} |
