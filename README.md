FAQ-Daten
=========

In diesem Repo werden alle Daten der PHP-FAQ gespeichert.

Das sind letztendlich die Daten der FAQ-Kategorien, sowie die
Daten der FAQ-Beiträge der einzelnen Kategorien.

Die folgenden Informationen werden gespeichert:

Kategorien/Kapitel
------------------

Jeder Beitrag der FAQ ist jweils einer Kategorie/Kapitel zugeteilt.

- **Alias** : Der Alias ist eine eindeutige Kennung der Kategorie.
              Dieser darf nur aus alphanumerischen Zeichen, Bindestrich
              Unterstrich und dem Punkt bestehen (A-Za-z0-9_.-), so
              das er ohne Maskierung in eine Webadresse verwendet
              werden kann.
- **Titel** : Der Name/Titel der Kategorie

Mehr Infos sind für die Kategorie nicht nötig.

FAQ-Beiträge
------------

Jeder Beitragskategorie können 0-n Beiträge zugeordnet sein.

- **Alias** : Der Alias ist eine eindeutige Kennung des Beitrags.
              Dieser darf nur aus alphanumerischen Zeichen, Bindestrich
              Unterstrich und dem Punkt bestehen (A-Za-z0-9_.-), so
              das er ohne Maskierung in eine Webadresse verwendet
              werden kann.
- **Frage** : Die Frage die der Beitrag beantwortet.
- **Autor** : Der Name des Autors vom Beitrag
- **Editor**: Für jeden Bearbeiter des Beitrags wird hinterlegt wer er ist,
              und wann er zuletzt etwas am Beitrag geändert hat.
- **Antwort** Die Anwort ist das HTML, das die Beantwortung der Frage
              darstellt. Erstaunlich oder? ;-)

Mehr Informationen brauchts eigentlich nicht oder?

Wie sollten die Informationen persistiert sein?
-----------------------------------------------

Gute Frage!

Vorstellbar wäre z.B. eine XML Struktur wie diese:

<pre>
 <strong>[xml]</strong>
    +- <strong>[Kategorie-Alias-1]</strong>
        +- category.xml
        +- <strong>[Beitrags-Alias-1]</strong>
           +- faq.xml
           +- answer.html
        +- <strong>[Beitrags-Alias-2]</strong>
           +- faq.xml
           +- answer.html
        +- ...
   +- <strong>[Kategorie-Alias-2]</strong>
        +- category.xml
        +- <strong>[Beitrags-Alias-3]</strong>
           +- faq.xml
           +- answer.html
        +- ...
   +- ...
</pre>

...ohne das jetzt im Detail zu erklären. (erstmal)

Ist halt nicht so gut vom Menschen lesbar, da XML.

Alternativ fällt mir das INI Konfigurationsdateiformat ein. Das ist halt besser
vom Menschen lesbar und sollte auch ausreichen um die Infos aufzunehmen.

Man kann das sicher auch in nur wenige, oder gar eine Datei alles reinpacken,
aber da leidet die Wartbarkeit und allgemein auch die Bearbeitbarkeit doch
schon sehr.
