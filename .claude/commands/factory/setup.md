---
description: "Software-Fabrik: Setup. Sieht sich Projekt und vorhandene Skills an, füllt die Lücken der Vorlage, fragt nur, wo etwas unklar ist oder fehlt, und baut am Ende den Maschinenraum."
argument-hint: "[<Station> …]"
---

# Setup der Software-Fabrik: $ARGUMENTS

Du richtest die Fabrik-Vorlage für dieses Projekt ein. Ohne Argument für alle Stationen, mit Argument
nur für die genannten (zum Nachziehen einzelner Stationen).

Die Vorlage liegt in `.claude/commands/factory.md` und `.claude/commands/factory/`. Jede Lücke ist eine
Tabellenzeile „Lücke | Leitfrage | Wert" mit dem Wert `{{OFFEN}}`: in `factory.md` (Abschnitt 2 und
Station 3) und in jeder Station („Bei euch"). `factory/regeln.md` enthält keine Lücken und wird vom
Setup nicht verändert.

## Schritt 0 — Wofür?

Das ist die eine Frage, die du immer stellst, bevor du etwas tust:

- **Spielwiese:** zum Kennenlernen und Üben. Jede Station darf simuliert werden, auch eine, die möglich
  wäre. Gibt es kein Projekt, schlage einen kleinen erfundenen Auftrag als Übungsstück vor (zum Beispiel
  ein winziges Kommandozeilenprogramm mit drei Akzeptanzkriterien) und frage, welche Stationen der
  Mensch echt ausprobieren will. Empfiehl, mindestens Plan, Umsetzen und Testplan echt laufen zu
  lassen: Sonst entsteht am Ende nichts zum Anfassen, und spätere Stationen bekommen nur simulierte
  Eingaben.
- **Echte Fabrik:** die Grundlage für den eigenen Prozess. Simuliert wird nichts. Was fehlt, bleibt
  leer oder wird entfernt.

Die Antwort hältst du in `factory.md` im „Stand der Fabrik" fest (`Zweck: Spielwiese` oder
`Zweck: echte Fabrik`). Steht dort bei einem erneuten Lauf „Spielwiese", frage, ob sie jetzt zur
echten Fabrik werden soll. Dann entfernst du jeden Simulationsblock und klärst die betroffenen
Stationen neu.

**Grundsätze**
- **Erst selbst nachsehen, dann fragen.** Gefragt wird nur, was die Erkundung nicht klärt.
- **Nichts erfinden.** Ein Wert kommt aus einer Fundstelle oder aus einer Antwort. Was du nur vermutest,
  ist eine Frage. Ein Vorschlag von dir, dem der Mensch zustimmt, ist eine Antwort.
- **„Gibt es bei uns nicht" ist ein Wert**, keine offene Lücke: Trage „keine" ein.
- **Vorhandenes verweisen, nicht kopieren.** Deckt ein vorhandener Skill eine Station oder einen Teil
  ab, trägst du den Verweis auf den Skill ein und nicht dessen Inhalt.
- **Nur die Lücken füllen.** Ziel und Ablauf der Stationen bleiben, wie sie sind, außer der Mensch will
  es anders.
- Du änderst nur Dateien unter `.claude/commands/factory.md` und `.claude/commands/factory/`. Darüber
  hinaus legst du nur den Maschinenraum an und, in der Spielwiese, den Übungsauftrag.

## Schritt 1 — Erkunden (ohne Rückfrage)

Lies zuerst alle Dateien der Vorlage, damit du jede Lücke und ihre Leitfrage kennst. Dann sieh dir an,
was es gibt. Nimm dafür Sub-Agenten, wenn das Projekt groß ist.

| Wo nachsehen | Was es beantwortet |
|---|---|
| Vorhandene Skills und Commands (im Projekt und beim Nutzer) samt ihren Beschreibungen | welche Stationen oder Teilschritte schon beschrieben sind |
| Anweisungsdateien für Agenten und Einstiegsdokumente des Projekts | Projektwissen, Konventionen, Verbote |
| Die angebundenen Werkzeuge dieser Sitzung | Auftragsquelle, Betriebssignale, Maschinenraum, Kommunikationswege |
| Einstiegspunkte für Bauen, Starten und Prüfen | Kommandos, Testebenen, lokale Umgebung |
| Die Einrichtung der zentralen Prüfung und des Ausrollens | was automatisch geprüft wird, wie und wohin ausgerollt wird |
| Die Versionsgeschichte und offene wie abgeschlossene Änderungen | Änderungsweg, Namenskonventionen, wer reviewt, wie zugestimmt wird |
| Vorlagen für Aufträge und Änderungen | was ein Auftrag enthalten muss, wie eine Beschreibung aussieht |
| Dokumentationsordner und festgehaltene Entscheidungen | Doku-Bereiche, Entscheidungsaufzeichnung |
| Tests und Testdaten | Testebenen, Belege, Testumgebung |
| Frühere Sitzungsverläufe, falls zugänglich | was der Mensch regelmäßig fragt und entscheidet |

Halte zu jedem Fund die Fundstelle fest.

## Schritt 2 — Zuordnen

Ordne jeden Fund den Lücken zu und stufe jede Lücke ein:

- **geklärt:** Wert mit Fundstelle.
- **unklar:** mehrere mögliche Werte oder ein Widerspruch.
- **fehlt:** Es gibt dafür nichts.

Stufe danach jede Station ein:

- **bereit:** alle Lücken, die sie zum Arbeiten braucht, sind geklärt.
- **teilweise:** arbeitsfähig, einzelne Lücken unklar.
- **nicht möglich:** Es fehlt, worauf die Station angewiesen ist (zum Beispiel keine lesbare
  Auftragsquelle, keine Testumgebung, kein Zugang zum Betrieb).

Station 3 (Nehmen) gehört zum Leitstand und wird nicht einzeln eingestuft. Die Nacharbeit folgt der
Station Umsetzen: Ist die nicht möglich, ist es die Nacharbeit auch nicht.

Zeige dem Menschen das Ergebnis als eine Tabelle: Station · Einstufung · was gefunden wurde (mit
Fundstelle) · was unklar ist · was fehlt.

## Schritt 3 — Nur das Nötige fragen

Stelle die Fragen gesammelt und gebündelt (lieber wenige Fragen mit je einem Vorschlag für mehrere
zusammengehörige Lücken als eine Frage je Lücke). Zuerst, was die meisten Stationen betrifft. Jede
Frage mit deinem Vorschlag und der Fundstelle, auf die er sich stützt.

- **Ort und Form des Maschinenraums** klärst du schon hier (Schritt 6, Punkt 2), weil Auftragsquelle,
  Entscheidungsspeicher und viele „wohin gehen Fragen"-Lücken daran hängen. Gebaut wird er erst in
  Schritt 6.

- **Unklare Lücken:** die Leitfrage der Lücke, mit den Möglichkeiten, die du gefunden hast.
- **Fehlende Lücken einer sonst arbeitsfähigen Station:** die Leitfrage. Bleibt sie unbeantwortet,
  bleibt der Wert `{{OFFEN}}`.
- **Entscheidungen vor dem Bauen** (Station 4) fragst du immer ab, auch wenn die Erkundung dazu nichts
  Widersprüchliches zeigt: Welche Entscheidungen will der Mensch besprechen, bevor gebaut wird? Schlage
  vor, was im Projekt teuer zu ändern wäre (zum Beispiel Aufbau, Datenformat, Schnittstellen nach
  außen); in der Spielwiese ohne Projekt schlage genau diese drei vor.
- **Lücken von Stationen, die simuliert, ausgelassen oder entfernt werden,** fragst du nicht ab. Sie
  bleiben `{{OFFEN}}`.
- **Stationen, die nicht möglich sind:** Frage je Station, was mit ihr geschehen soll. „Simulieren"
  bietest du nur in der Spielwiese an; dort darf der Mensch es auch für mögliche Stationen wählen:

  | Wahl | Bedeutung |
  |---|---|
  | **simulieren** | Nur in der Spielwiese: Die Fabrik läuft durch, die Station tut so, als ob. Gut, um den Ablauf zu üben, bevor alles angebunden ist. |
  | **leer lassen** | Die Station bleibt als Platz erhalten und wird ausgelassen, bis ihr sie füllt. |
  | **entfernen** | Die Station gibt es bei euch nicht. |

  Weise vor dem Entfernen und dem Leerlassen darauf hin, was dann ungeprüft oder unerledigt bleibt. Die
  Zustimmung des Menschen im Review und seine Freigabe werden nie simuliert.

Entscheide keine dieser drei Fragen selbst.

## Schritt 4 — Eintragen

1. Jeden geklärten Wert in die Spalte „Wert" seiner Lücke schreiben, knapp, mit dem Verweis auf Skill
   oder Fundstelle, wo es einen gibt. Dieselbe Lücke kommt in mehreren Stationen vor
   (zum Beispiel die Auftragsquelle): Trage überall denselben Wert ein. Jede Station muss für sich
   allein lesbar sein, ohne eine zweite Datei.
2. **Entfernen:** die Datei der Station löschen. In `factory.md` ihre Zeile in der Command-Tabelle und
   in der Stationstabelle entfernen und die „Weiter, wenn"-Bedingungen der Nachbarn anpassen, sodass
   keine Station auf ein Ergebnis wartet, das es nicht mehr gibt.
3. **Leer lassen:** direkt unter dem Titel der Station diesen Block einfügen; der Rest der Station
   bleibt stehen:

   > **NOCH NICHT EINGERICHTET.** Führe diese Station nicht aus. Melde, dass sie ausgelassen wurde und
   > was dadurch ungeprüft oder unerledigt bleibt, und ende mit `STATUS: FERTIG`.

4. **Simulieren:** direkt unter dem Titel der Station diesen Block einfügen und mit dem Menschen
   abstimmen, welches Ergebnis die Station vortäuschen soll (Vorschlag: ihr Abschnitt „Ergebnis", jeder
   Punkt als nicht ermittelt):

   > **SPIELWIESE: DIESE STATION IST SIMULIERT.** Führe nichts wirklich aus und verändere nichts.
   > Liefere stattdessen: *<das abgestimmte Ergebnis>*. Beginne deine Meldung mit **SIMULIERT**,
   > kennzeichne jede Aussage darin so und formuliere nie so, als wäre es geschehen. Ende mit
   > `STATUS: FERTIG`.

   Für Review und Freigabe gilt eine eigene Fassung, weil die Entscheidung des Menschen echt bleibt:

   > **SPIELWIESE: DIE VORBEREITUNG DIESER STATION IST SIMULIERT.** Führe nichts wirklich aus und
   > verändere nichts. Liefere stattdessen: *<das abgestimmte Ergebnis>*, als **SIMULIERT**
   > gekennzeichnet. Die Zustimmung oder Freigabe des Menschen holst du trotzdem echt ein und meldest
   > sie nie als erteilt, bevor er sie gegeben hat. Ende mit `STATUS: FERTIG` oder `STATUS: FRAGE: …`.

   Simulation ist kein Zustand der fertigen Fabrik. Sie gehört nur in die Spielwiese.
5. In `factory.md` unter der Stationstabelle den **Stand der Fabrik** eintragen: die Zeile `Zweck: …`
   aus Schritt 0, dann je Station eingerichtet, ausgelassen oder simuliert, und die Zahl der noch
   offenen Lücken. Solange dort eine
   simulierte Station steht, dazu der Satz: „Spielwiese: Ergebnisse dieser Fabrik sind nicht echt."

Wird das Setup später für eine Station erneut aufgerufen und ist sie jetzt möglich, entfernst du ihren
Block wieder und füllst ihre Lücken.

## Schritt 5 — Prüfen und berichten

- Verweist noch etwas auf eine entfernte Station?
- Stimmt jeder eingetragene Verweis (Skill, Datei, Kommando existiert)?
- Welche Lücken sind noch `{{OFFEN}}`?

Bericht an den Menschen, als Tabelle: Station · eingerichtet, ausgelassen, simuliert oder entfernt ·
gefüllte Lücken · offene Lücken. Zähle die offenen Lücken eingerichteter Stationen getrennt von denen
simulierter und ausgelassener: Nur die ersten sind jetzt zu klären. Danach, in dieser Reihenfolge: was
simuliert oder ausgelassen wird und was dadurch ungeprüft bleibt, auch für echte Stationen, die auf
simulierten Ergebnissen aufbauen; dann die offenen Lücken, die als Nächstes zu klären sind.

## Schritt 6 — Den Maschinenraum bauen

Das Setup endet damit, dass der Maschinenraum steht: der eine Ort, an dem der Mensch sieht, was läuft
und was er als Nächstes tun muss. Er entsteht aus dem Prozess, wie er jetzt eingerichtet ist, und aus
den Antworten dieses Setups, nicht aus einer Standardansicht.

**1. Ableiten, was er zeigen muss.**
- **Überblick:** Läuft alles? Jeder begonnene Auftrag mit der Station, in der er steht, und woran er
  gerade hängt. Die Spalten sind die Stationen, die es in dieser Fabrik gibt, in ihrer Reihenfolge;
  entfernte Stationen kommen nicht vor, ausgelassene und simulierte sind als solche erkennbar.
- **Mein Nächstes:** Was braucht die Fabrik vom Menschen? Offene Fragen mit Optionen und Empfehlung,
  Reviews, Freigaben, Schritte von Hand. Sortiert nach der Regel, die der Mensch genannt hat; ohne
  Regel: was die meiste Arbeit blockiert, zuerst.
- **Was sonst regelmäßig gefragt wird:** Lies, falls zugänglich, frühere Sitzungsverläufe: Was fragt der
  Mensch den Agenten immer wieder? Was fragt der Agent ihn immer wieder? Wo wurde erst im Nachhinein
  etwas geklärt? Der Maschinenraum beantwortet diese Fragen, bevor sie gestellt werden.
- **Stand der Fabrik:** welche Stationen eingerichtet, ausgelassen oder simuliert sind, und welche
  Lücken noch offen sind.

**2. Die Form wählen** (schon in Schritt 3 geklärt). Nimm, was die Erkundung gezeigt hat: Gibt es schon einen Ort, an dem der Mensch
täglich nachsieht und in dem er antworten kann und den der Agent lesen und schreiben kann, entsteht
der Maschinenraum dort. Sonst schlage eine lokale Seite im Browser vor, mit einem kleinen lokalen
Dienst dahinter. Eine reine Textdatei reicht nicht: Sie zeigt nur, der Mensch kann darin nicht bequem
antworten. Ist die Form nicht eindeutig, frage, mit Vorschlag.

**Ziel der Seite:** Der Mensch erhält einen guten Überblick, und er spricht mit der Fabrik bevorzugt
durch Klicken und Auswählen statt durch Schreiben. Auch die Rückfragen der Fabrik laufen über diese
Seite, asynchron: Sie warten dort, bis er sie bearbeitet, und die Fabrik arbeitet solange weiter. Wählt
er etwas aus, soll die Fabrik das möglichst unverzüglich bemerken (Punkt 4, „Wächter").

Der Maschinenraum ist eine Kommandozentrale, er arbeitet in beide Richtungen:

| Richtung | Was es braucht |
|---|---|
| Fabrik → Mensch | Auf einen Blick lesbar, Wichtiges oben. Die Ansicht aktualisiert sich selbst und zeigt, von wann ihr Stand ist. |
| Mensch → Fabrik | Zu jedem Eintrag unter „Mein Nächstes" antwortet er direkt am Eintrag: eine Option wählen (die Empfehlung ist vorbelegt), freigeben oder ablehnen, frei schreiben. Dazu ein Feld für eine Nachricht an den Leitstand, ohne Anlass. |

Für die lokale Seite gilt:
- **Eine Quelle.** Der Stand liegt in einer Datei oder einem Speicher, den der Leitstand bei jedem Takt
  liest und schreibt. Die Seite zeigt ihn nur an und schreibt nichts als die Antworten und Nachrichten
  des Menschen dorthin. Der Leitstand kann den Stand auch lesen, wenn der Dienst nicht läuft.
- **Bedienung.** Was der Mensch tun muss, steht oben und ist von dem getrennt, was nur Auskunft ist.
  Jede Rückfrage kommt mit Optionen zum Anklicken, die Empfehlung vorbelegt; freier Text ist immer
  möglich, aber nie nötig, wenn eine Auswahl reicht. Nach dem Senden sieht er, dass sie angekommen ist
  und ob der Leitstand sie schon gelesen hat. Eine angefangene Eingabe geht beim Aktualisieren nicht
  verloren. Lesbar auch auf dem Telefon, hell und dunkel.
- **Nur lokal und nur vom Menschen.** Der Dienst ist nur auf dem eigenen Rechner erreichbar und liefert
  nur aus, was die Seite braucht, nicht das ganze Projekt. Er nimmt Eingaben nur von seiner eigenen
  Seite an: Eine fremde Webseite, die im selben Browser offen ist, darf dem Leitstand keine Nachricht
  unterschieben können. Texte aus Aufträgen und Berichten zeigt die Seite als Text an, nie als
  ausführbaren Inhalt.
- **Mit dem, was da ist.** Baue den Dienst mit dem, was auf dem Rechner und im Projekt ohnehin vorhanden
  ist, ohne neue Abhängigkeit. Er gehört zur Fabrik, nicht zum Produkt.
- **Starten.** Halte fest, wie der Dienst gestartet wird und unter welcher Adresse die Seite liegt, und
  trage beides in die Lücke „Maschinenraum" ein.

**3. Erst zeigen, dann bauen.** Lege dem Menschen den Entwurf vor: was der Maschinenraum zeigt, wie es
angeordnet ist, wo er liegt, wie er antwortet. Baue ihn erst nach seiner Zustimmung.

**4. Bauen und anschließen.**
- **`.tmp/` anlegen und vom Einchecken ausnehmen.** Lege im Wurzelverzeichnis des Projekts `.tmp/` an
  und trage es dort ein, wo das Projekt festlegt, was nicht eingecheckt wird. Prüfe, dass es wirkt (eine
  Probedatei in `.tmp/` taucht nicht als neue Datei auf), und trage den Weg in die Lücke „Artefakte"
  ein. Auch der Maschinenraum, sein Stand und sein Dienst liegen unter `.tmp/`: Er lässt sich aus der
  Auftragsquelle und den Stationen neu aufbauen.
- **Den bleibenden Ort festlegen.** Hat das Projekt schon einen Ort für Dokumentation und
  Entscheidungen, gilt der; trage ihn in die Lücke „Bleibendes" und in Station 7 ein. Sonst lege
  `docs/` im Wurzelverzeichnis an, mit `docs/adr/` für Entscheidungen. `docs/` wird eingecheckt.
- Den Maschinenraum anlegen und mit dem aktuellen Stand füllen: den begonnenen Aufträgen, soweit die
  Auftragsquelle lesbar ist, sonst leer. In der Spielwiese mit dem Übungsauftrag, als Beispiel
  gekennzeichnet.
- In `factory.md` die Lücken „Maschinenraum" und „Entscheidungsspeicher" mit dem Ort füllen und im
  Abschnitt „Takt" festhalten, wie der Leitstand ihn liest (Schritt „Orientieren") und aktualisiert
  (Schritte „Ergebnisse verarbeiten" und „Fragen ablegen").
- In den Stationen jede Lücke füllen, die auf ihn verweist (wohin Fragen gehen, wo Urteile und
  Wiedervorlagen landen).

- **Den Wächter anlegen.** Zusammen mit dem Maschinenraum entsteht ein Wächter: eine Beobachtung im
  Hintergrund der Sitzung, in der der Leitstand läuft, die ihn weckt, sobald der Mensch im
  Maschinenraum etwas ausgewählt, beantwortet oder geschrieben hat. Der Wächter beobachtet nur und
  meldet, dass es etwas Neues gibt; lesen und verarbeiten tut der Leitstand im Schritt „Orientieren".
  Trage in `factory.md` in die Lücke „Wächter" ein, wie er gestartet wird und woran der Leitstand
  erkennt, dass er läuft. Der Leitstand startet ihn bei jedem Start selbst neu und hält ihn am Leben;
  der Mensch muss dafür nichts tun.
- Beide Richtungen einmal ausprobieren: eine Probe-Antwort und eine Probe-Nachricht über den Weg des
  Menschen senden, prüfen, dass der Wächter anschlägt und der Leitstand sie dort findet, wo er nach
  „Takt" nachsieht, und beide wieder entfernen.

**5. Abschluss.** Zeige dem Menschen den fertigen Maschinenraum, wie er dort antwortet, und den ersten
Auftrag, mit dem sich die Fabrik ausprobieren lässt. Sage ihm, wie es weitergeht: `/loop /factory`
startet den Leitstand, `/factory:<station> <Auftrag>` eine einzelne Station. Damit ist das Setup
beendet.
