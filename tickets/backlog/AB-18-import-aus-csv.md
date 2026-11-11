# AB-18: Import aus CSV

Blockiert durch: AB-1, AB-2, AB-3, AB-15

**Ziel:** Kontakte aus einer Tabellenkalkulation übernehmen.

**Akzeptanzkriterien:**
1. Ich kann eine CSV-Datei einlesen, die so aufgebaut ist wie der Export; die Kontakte daraus sind danach gespeichert.
2. Exportiere ich ein Adressbuch und lese die Datei in ein leeres Adressbuch ein, enthält es dieselben Kontakte.
3. Bereits gespeicherte Kontakte bleiben unverändert; die eingelesenen kommen hinzu.
4. Eine Zeile ohne Name oder ohne Telefonnummer wird nicht übernommen. Die übrigen Zeilen werden trotzdem übernommen.
5. Am Ende erfahre ich, wie viele Kontakte übernommen und wie viele Zeilen abgelehnt wurden, und für jede abgelehnte Zeile, welche es war und warum.
6. Lässt sich die Datei nicht lesen oder ist sie nicht wie der Export aufgebaut, wird nichts verändert, und ich bekomme eine verständliche Fehlermeldung.

**Nicht enthalten:** andere Formate, Abgleich mit bereits vorhandenen Kontakten gleichen Namens, Rückgängigmachen eines Imports.
