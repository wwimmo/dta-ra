# adr - architecture decission records

Im folgenden werden diskutierte Architekturentscheide für zukünftige Diskussionen festgehalten.

## ID

## Format JSON vs. XML

    XML oder JSON? XML kann mittels XSD einfach validiert werden. XML kann auch optimal als Datei ausgetauscht werden.

Da der Austausch primär über Web-APIs laufen soll und primär Web-basierte Anwendungen mit diesen Daten arbeiten, haben wir uns für JSON als Format entschieden.
