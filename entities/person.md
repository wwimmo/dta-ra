# person (Person)

Die folgende Entität wird für die [Schadensmeldung](damagenotification.md) und den Reparaturauftrag verwendet.

| Attribut         | Typ            | Beschreibung                                              | Pflicht |
| ---------------- | -------------- | --------------------------------------------------------- | :-----: |
| personid         | uuid           | ID der Person                                             |    -    |
| legal            | boolean        | Juristische Person                                        |    x    |
| salutation       | integer (enum) | [Anrede](/types/salutationtypes.md)                       |    x    |
| name1            | string         | Vorname / Zeile 1                                         |    x    |
| name2            | string         | Nachname / Zeile 2 / Leerer String                        |    x    |
| email            | string         | E-Mail-Adresse                                            |    -    |
| mobile           | string         | Mobiltelefonnummer                                        |    -    |
| phoneprivate     | string         | Telefonnummer privat                                      |    -    |
| phonebusiness    | string         | Telefonnummer geschäftlich                                |    -    |
| reachability     | Reachability   | Telefonische Erreichbarkeit als Aufzählung von Zeiträumen |    -    |
| customattributes | json Key-Value |                                                           |    -    |

## Reachability

Das Feld Reachability steht für die telefonische Erreichbarkeit derjenigen Person, die Zugang zum Objekt der Schadensmeldung hat. Die telefonische Erreichbarkeit wird als Auflistung von Zeiträumen angegeben:


| Attribut | Typ       | Beschreibung                     | Pflicht |
| -------- | --------- | -------------------------------- | :-----: |
| date     | datetime  | Datum                            |    -    |
| from     | string    | Zeitraum Beginn                  |    -    |
| to       | string    | Zeitraum Ende                    |    -    |

Beispiel

    "reachability": [
        {
            "date": "2020-07-30T00:00:00",
            "from": "08:00:00",
            "to": "10:00:00"
        },
        {
            "date": "2020-07-30T00:00:00",
            "from": "10:00:00",
            "to": "12:00:00"
        },
        {
            "date": "2020-07-31T00:00:00",
            "from": "10:00:00",
            "to": "12:00:00"
        }
    ]
