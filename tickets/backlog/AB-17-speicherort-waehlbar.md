# AB-17: Speicherort wählbar

Blockiert durch: AB-1, AB-2, AB-3

**Ziel:** Mehrere Adressbücher nebeneinander führen.

**Akzeptanzkriterien:**
1. Ich kann bei jedem Aufruf angeben, mit welchem Adressbuch ich arbeite; das gilt dann für alles, was dieser Aufruf tut.
2. Ich kann ein Adressbuch dauerhaft für meine Arbeitsumgebung voreinstellen, sodass ich es nicht bei jedem Aufruf angeben muss.
3. Die Angabe beim Aufruf geht der Voreinstellung vor. Ohne beides gilt das bisherige Standard-Adressbuch.
4. Zeigt die Angabe auf einen Ort, den es nicht gibt, wird nichts angelegt, und ich bekomme eine Fehlermeldung.

**Nicht enthalten:** Zusammenführen mehrerer Adressbücher.
