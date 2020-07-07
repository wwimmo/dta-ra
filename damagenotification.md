# damagenotification (Schadensmeldung)

Die folgende Entität erläutert den Aufbau einer Schadensmeldung.

| Attribut          | Typ                               | Beschreibung                                     | Pflicht |
| ----------------- | --------------------------------- | ------------------------------------------------ | :-----: |
| version           | string                            | Version der Schnittstelle, z.B. "0.1" oder "1.1" |    x    |
| id                | uuid                              | ID der Meldung                                   |    x    |
| notificationdate  | datetime                          | Zeitpunkt der Schadensmeldung                    |    x    |
| location          | [Location](/entities/location.md) |                                                  |    x    |
| damage            | [Damage](/entities/damage.md)     |                                                  |    x    |
| sendingperson     | [Person](/entities/person.md)     |                                                  |    x    |
| sendingpersontype | integer (enum)                    | [Persontypes](/types/persontypes.md)             |    x    |
| contactperson     | [Person](/entities/person.md)     |                                                  |    -    |
| contactpersontype | integer (enum)                    | [Persontypes](/types/persontypes.md)             |    -    |
| customattributes  | json Key-Value                    |                                                  |    -    |

## Beispiel

[Beispiel](damagenotification-example.md)
