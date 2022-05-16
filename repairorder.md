# repairorder (Reparaturauftrag)

Die folgende Entität erläutert den Aufbau eines Reparaturauftrags.

| Attribut             | Typ                               | Beschreibung                                     | Pflicht |
| -------------------- | --------------------------------- | ------------------------------------------------ | :-----: |
| version              | string                            | Version der Schnittstelle, z.B. "1.0.0"          |    x    |
| id                   | uuid                              | ID der Meldung                                   |    x    |
| namespace            | string                            | Verwendung wie unter README#ID beschrieben       |    x    |
| state                | integer (enum)                    | Status des Reparaturauftrags                     |    x    |
| lastchange           | datetime                          | Letzte Änderung                                  |    x    |
| contractorperson     | [Person](/entities/person.md)     | Handwerker (Auftragsnehmer)                      |    x    |
| contractorpersontype | integer (enum)                    | [Persontypes](/types/persontypes.md)             |    x    |
| positions            |                                   | Auftragspositionen                               |    x    |
|                      |                                   |                                                  |    x    |
| location             | [Location](/entities/location.md) |                                                  |    x    |
| damagenotificationid | uuid                              | ID der [Schadensmeldung](damagenotification.md)  |    -    |
| clientperson         | [Person](/entities/person.md)     |                                                  |    x    |
| clientpersontype     | integer (enum)                    | [Persontypes](/types/persontypes.md)             |    x    |
| contactperson        | [Person](/entities/person.md)     |                                                  |    -    |
| contactpersontype    | integer (enum)                    | [Persontypes](/types/persontypes.md)             |    -    |
| customattributes     | json Key-Value                    | -                                                |    -    |

## Beispiel

[Beispiel](repairorder-example.md)
