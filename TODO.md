TODO-Liste für php-faq-de/FAQ-Daten
===================================

Es gibt immer was zu tun! :-)

Version 0.1
-----------

- **Externe Links** : Alle in den Beiträgen enthaltenen externen Links müssen bzgl. ihrer Aktualität
  überprüft werden.
- **Code-Highlighting** : <del>Der meiste PHP-Code in vorformatierten HTML-Abschnitten (pre-Elemente)
  liegt in einer Form vor, der den Code highlightet. Das ist zwar am Ende eine hübsche Sache, aber
  innerhalb des Datensatzes vollkommen unnötiger, und schwer zu wartender Overhead. Das muss raus!</del>
  __[Erledigt]__ Es wurden 190 Beiträge (answer.html) von Highlighting-Code befreit.
- **Fehlende Dokumente** : <del>Beim Parsen der Daten aus dem Webcache konnten
  2 Dokumente der alten FAQ nicht eingelesen werden. Zuerst mal müssen diese beiden Dokumente
  lokalisiert werden und dann müssen sie noch manuell zu den XML-Daten hinzugefügt werden.</del>
  __[Erledigt]__ Gefehlt haben <tt>Wie ist die Charta dieser Newsgroup?
  (newsgroup-charta)</tt> und <tt>Warum kann ich nicht mehr auf de.comp.lang.php.* zugreifen?
  (newsgroup-old)</tt>, beide aus der Kategorie <tt>Über diese FAQ (about)</tt>.
- **Ungültige answer.html** : <del>Bei Extrahieren der Daten von web.cache.org
  scheinen die Daten einer Antwort nicht korrekt zu sein. (Zu viele Daten im Dokument) Da ich nicht
  mehr weis welcher Beitrag genau das war baue ich einen kleinen Parser der die Aufgabe automatisch
  erledigt.</del>
  __[Erledigt]__ Das Problem bestand in der Datei `xml/security/apache-passwort/answer.html`
- **FAQ interne Links** : <del>Da in den geparsten Dokumenten auch Links enthalten sind, die FAQ-intern
  auf FAQ-Beiträge verweisen müssen diese Links noch in was generelleres umgewandelt werden.
  Momentan sehen die Links so aus (Kategorielinks: http://php-faq.de/ch_kategoriealias.html und
  Beitragslinks http://php-faq.de/q-beitragalias.html). Diese werden umgeschrieben zu
  @{kategoriealias} für Kategorielinks und ${beitragsalias} für Beitragslinks.</del>
  __[Erledigt]__ Es wurden FAQ-interne Links in insgesamt 32 answer.html Dateien umgeschrieben.
  