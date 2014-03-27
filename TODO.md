TODO-Liste für php-faq-de/FAQ-Daten
===================================

Es gibt immer was zu tun! :-)

Version 0.1
-----------

- **Fehlende Dokumente** : <del>Beim Parsen der Daten aus dem Webcache konnten 2 Dokumente der alten FAQ
  nicht eingelesen werden. Zuerst mal müssen diese beiden Dokumente lokalisiert werden und dann
  müssen sie noch manuell zu den XML-Daten hinzugefügt werden.</del>
  <span style="color: green;">[Erledigt]</span> Gefehlt haben <tt>Wie ist die Charta dieser Newsgroup?
  (newsgroup-charta)</tt> und <tt>Warum kann ich nicht mehr auf de.comp.lang.php.* zugreifen?
  (newsgroup-old)</tt>, beide aus der Kategorie <tt>Über diese FAQ (about)</tt>.
- **Ungültige answer.html** : Bei Extrahieren der Daten von web.cache.org scheinen die Daten einer
  Antwort nicht korrekt zu sein. (Zu viele Daten im Dokument) Da ich nicht mehr weis welcher Beitrag
  genau das war baue ich einen kleinen Parser der die Aufgabe automatisch erledigt.
- **FAQ interne Links** : Da in den geparsten Dokumenten auch Links enthalten sind, die FAQ-intern
  auf FAQ-Beiträge verweisen müssen diese Links noch in was generelleres umgewandelt werden.
  Momentan sehen die Links so aus (Kategorielinks: `http://php-faq.de/ch_kategoriealias.html` und
  Beitragslinks `http://php-faq.de/q-beitragalias.html`). Diese werden umgeschrieben zu
  `@{kategoriealias}` für KAtegorielinks und `${beitragsalias}` für Beitragslinks.
  