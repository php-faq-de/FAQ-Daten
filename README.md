FAQ-Daten
=========

In diesem Repo werden alle Daten der deutschen PHP-FAQ für die
Newsgruppe [de.comp.lang.php](news:de.comp.lang.php) gespeichert.

Das sind letztendlich die Daten der FAQ-Kategorien, sowie die
Daten der FAQ-Beiträge der einzelnen Kategorien.

- **Version** : 0.1 
- **Author**  : Ulf [UniKado] Kadner
- **Since**   : 2014-03-27
- **Release** : alpha1
- **License** : Open Publication License

Das Projekt wurde ins Leben gerufen, nachdem die letzte Version der
PHP-FAQ (http://php-faq.de) nur noch über http://web.archive.org/
verfügbar war. Die originale Webseite ist aus bisher unerklärlichen
Gründen nicht mehr erreichbar und der Verantwortliche auch nicht.

Damit das nicht nochmal passiert wurde dieses Projekt hier angelegt
welches alle bisher zusammen gekommenen FAQ-Beiträge in einem oder
mehreren verschiedenen Formaten bereit stellt.

Die Daten
---------

Die folgenden Informationen werden gespeichert:

### Kategorien/Kapitel

Jeder Beitrag der FAQ ist jweils einer Kategorie/Kapitel zugeteilt.

- **Alias** : Der Alias ist eine eindeutige Kennung der Kategorie.
              Dieser darf nur aus alphanumerischen Zeichen, Bindestrich
              Unterstrich und dem Punkt bestehen (A-Za-z0-9_.-), so
              das er ohne Maskierung in eine Webadresse verwendet
              werden kann.
- **Titel** : Der Name/Titel der Kategorie
- **Keywords** : Schlüsselworte die für diese Kategorie genutzt werden.

Mehr Infos sind für die Kategorie nicht nötig.

### FAQ-Beiträge

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
- **Keywords** : Schlüsselworte die für diesen Beitrag genutzt werden.

Mehr Informationen brauchts eigentlich nicht oder?

Wie sind die Informationen persistiert?
---------------------------------------

Die Daten im `xml` Verzeichnis des Projekts sind in folgender Struktur definiert:

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

- `category.xml` beinhaltet jeweils im wesentlichen alle Infos zur Kategorie und
  eine Liste der Aliase aller FAQs die zur Kategorie gehören.
- `faq.xml` beinhaltet jeweils die Infos zur FAQ, ohne den Antwortteil der FAQ
- `answer.html` beinhaltent jeweils den Rest. Also den Antwortteil des FAQ-Beitrags
  mit allem was zur Auszeichnung als HTML dazugehört.
  
Wie nutze ich die Daten?
------------------------

Dafür läst sich leicht eine API konstruieren, die mit den Daten in vorgegebenen
Format umgehen kann.

Eine Api zur Nutzung in MS .NET und Mono Umgebung ist bereits in Planung.
EIne PHP-Api ebenfalls.

Die Daten sind jedenfalls fast vollständig. 2 Beiträge hat der Parser, den ich
gebaut habe, nicht aus dem Webarchiv von [web.archive.org](http://web.archive.org/)
extrahieren können. Die muss ich bei Gelegenheit nochmal manuell eintragen.

Man kann jedenfalls daraus automatisiert eine Webseite machen, auch wenn die API
noch fehlt. Bis die fertig ist bleibt nur do-it-youre-self. ;-)