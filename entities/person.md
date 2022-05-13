# person (Person)

Die folgende Entität wird für die [Schadensmeldung](damagenotification.md) und den Reparaturauftrag verwendet.

| Attribut         | Typ            | Beschreibung                                 | Pflicht |
| ---------------- | -------------- | -------------------------------------------- | :-----: |
| personid         | uuid           | ID der Person                                |    -    |
| legal            | boolean        | Juristische Person                           |    x    |
| salutation       | integer (enum) | [Anrede](/types/salutationtypes.md)          |    x    |
| name1            | string         | Vorname / Zeile 1                            |    x    |
| name2            | string         | Nachname / Zeile 2 / Leerer String           |    x    |
| email            | string         | E-Mail-Adresse                               |    -    |
| mobile           | string         | Mobiltelefonnummer                           |    -    |
| phoneprivate     | string         | Telefonnummer privat                         |    -    |
| phonebusiness    | string         | Telefonnummer geschäftlich                   |    -    |
| customattributes | json Key-Value |                                              |    -    |