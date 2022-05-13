# damage (Schaden)

Die folgende Entität wird für die [Schadensmeldung](Damagenotification.md) und den Reparaturauftrag verwendet.

| Attribut              | Typ            | Beschreibung                                              | Pflicht |
| --------------------- | -------------- | --------------------------------------------------------- | :-----: |
| room                  | string         | Raumbezeichnung                                           |    -    |
| roomtype              | integer (enum) | [Raumtyp](/types/roomtypes.md)                            |    x    |
| appliance             | string         | Gerätebezeichnung                                         |    -    |
| appliancetype         | integer (enum) | [Gerätetyp](/types/appliancetypes.md)                     |    x    |
| model                 | string         | Modell                                                    |    -    |
| manufacturer          | string         | Hersteller                                                |    -    |
| manufacturertype      | integer (enum) | [Herstellertyp](/types/manufacturertypes.md)              |    -    |
| serialnumber          | string         | Seriennummer                                              |    -    |
| serialnumberimage     | Image          | Bild der Seriennummer                                     |    -    |
| productionnumber      | string         | Produktionsnummer                                         |    -    |
| productionnumberimage | Image          | Bild der Produktionsnummer                                |    -    |
| damagedescription     | string         |                                                           |    x    |
| damageimage1          | Image          | Bild des Schadens                                         |    -    |
| damageimage2          | Image          | Bild des Schadens                                         |    -    |
| reachability          | Reachability   | Telefonische Erreichbarkeit als Aufzählung von Zeiträumen |    -    |
| remarks               | string         | Bemerkungen der Verwaltung                                |    -    |
| customattributes      | json Key-Value | -                                                         |    -    |

## Image

Bilder werden als [Base64](https://de.wikipedia.org/wiki/Base64) encodierter String angegeben.

## Reachability

Das Feld Reachability steht für die telefonische Erreichbarkeit derjenigen Person, die Zugang zum Objekt der Schadensmeldung. Die telefonische Erreichbarkeit wird als Array von Zeiträumen (Reachabilities) angegeben:


| Attribut | Typ       | Beschreibung                     | Pflicht |
| -------- | --------- | -------------------------------- | :-----: |
| date     | datetime  | Datum                            |    -    |
| from     | string    | Zeitraum Beginn                  |    x    |
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
