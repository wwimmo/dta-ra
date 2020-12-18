# damage (Schaden)

Die folgende Entität wird für die [Schadensmeldung](Damagenotification.md) und den Reparaturauftrag verwendet.

| Attribut              | Typ            | Beschreibung                                 | Pflicht |
| --------------------- | -------------- | -------------------------------------------- | :-----: |
| room                  | string         | Raumbezeichnung                              |    -    |
| roomtype              | integer (enum) | [Raumtyp](/types/roomtypes.md)               |    x    |
| appliance             | string         | Gerätebezeichnung                            |    -    |
| appliancetype         | integer (enum) | [Gerätetyp](/types/appliancetypes.md)        |    x    |
| model                 | string         | Modell                                       |    -    |
| manufacturer          | string         | Hersteller                                   |    -    |
| manufacturertype      | integer (enum) | [Herstellertyp](/types/manufacturertypes.md) |    -    |
| serialnumber          | string         | Seriennummer                                 |    -    |
| serialnumberimage     | Image          | Bild der Seriennummer                        |    -    |
| productionnumber      | string         | Produktionsnummer                            |    -    |
| productionnumberimage | Image          | Bild der Produktionsnummer                   |    -    |
| damagedescription     | string         |                                              |    x    |
| damageimage1          | Image          | Bild des Schadens                            |    -    |
| damageimage2          | Image          | Bild des Schadens                            |    -    |
| remarks               | string         | Bemerkungen der Verwaltung                   |    -    |
| customattributes      | json Key-Value |                                              |    -    |

## Image

Bilder werden als [Base64](https://de.wikipedia.org/wiki/Base64) encodierter String angegeben.
