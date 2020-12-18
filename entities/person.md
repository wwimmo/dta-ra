# person (Person)

Die folgende Entität wird für die [Schadensmeldung](damagenotification.md) und den Reparaturauftrag verwendet.

| Attribut         | Typ            | Beschreibung                                 | Pflicht |
| ---------------- | -------------- | -------------------------------------------- | :-----: |
| personid         | uuid           | ID der Person                                |    x    |
| legal            | boolean        | Juristische Person                           |    x    |
| salutation       | integer (enum) | [Anrede](types/salutationtypes.md)           |    x    |
| name1            | string         | Vorname/Zeile 1                              |    x    |
| name2            | string         | Nachname/Zeile 2                             |    x    |
| email            | string         | E-Mail-Adresse                               |    -    |
| mobile           | string         | Mobiltelefonnummer                           |    -    |
| phoneprivate     | string         | Telefonnummer privat                         |    -    |
| phonebusiness    | string         | Telefonnummer geschäftlich                   |    -    |
| reachability     | Reachability   | Telefonische Erreichbarkeit (Zeiten, Blöcke) |    -    |
| customattributes | json Key-Value |                                              |    -    |

## Reachability

Die telefonische Erreichbarkeit kann nach dem folgenden Schema angegeben werden.

    "reachability": [
        "date": {
            "from": "time"
            "to": "time"
        },
    ]

Beispiel

    "reachability": [
        "2020-07-30": {
            "from": "09:00:00"
            "to": "10:00:00"
        },
        "2020-07-31": {
            "from": "09:00:00"
            "to": "10:00:00"
        },
        "2020-07-31": {
            "from": "11:00:00"
            "to": "12:00:00"
        }
    ]

Zusammen ergeben die Werte ein Datum nach dem Format ISO 8601:

    "YYYY-MM-DDThh:mm:ss"
