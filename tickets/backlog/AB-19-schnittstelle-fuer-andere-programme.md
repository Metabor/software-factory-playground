# AB-19: Schnittstelle für andere Programme

Blockiert durch: AB-1, AB-2, AB-3

**Ziel:** Ein anderes Programm kann das Adressbuch benutzen, ohne dass ein Mensch es bedient.

**Akzeptanzkriterien:**
1. Ein anderes Programm kann alle Kontakte abrufen und bekommt sie in einer Form, die es zuverlässig auswerten kann.
2. Es kann einen Kontakt anlegen und einen Kontakt löschen. Dabei gelten dieselben Regeln wie bei der Bedienung durch einen Menschen.
3. Geht etwas schief, erfährt das Programm in auswertbarer Form, was nicht stimmte, und es wurde nichts verändert.
4. Mensch und Programm arbeiten auf denselben Kontakten: Was der eine ändert, sieht der andere.
5. Die Schnittstelle ist so beschrieben, dass jemand sie benutzen kann, ohne den Code zu lesen.

**Nicht enthalten:** Anmeldung und Zugriffsschutz, gleichzeitige Zugriffe mehrerer Programme, Suchen und Ändern über die Schnittstelle.
