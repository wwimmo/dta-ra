# location

Die folgenden Entitäten werden für die [Schadensmeldung](Damagenotification.md) und den Reparaturauftrag verwendet.

| Attribut         | Typ                           | Beschreibung                       | Pflicht |
| ---------------- | ----------------------------- | ---------------------------------- | :-----: |
| realestateid     | uuid                          | ID der Liegenschaft                |    -    |
| realestatenumber | string                        | Technische Nummer der Liegenschaft |    -    |
| realestatename   | string                        | Bezeichnung der Liegenschaft       |    -    |
| houseid          | uuid                          | ID des Hauses                      |    -    |
| housenumber      | string                        | Technische Nummer des Hauses       |    -    |
| unitid           | uuid                          | ID des Objekts                     |    -    |
| unitnumber       | string                        | Technische Nummer des Objekts      |    -    |
| unitname         | string                        | Bezeichnung des Objekts            |    -    |
| street           | string                        | Strasse (und Nummer)               |    x    |
| number           | string                        | Nummer (wenn nicht in Strasse)     |    -    |
| zip              | string                        | Postleitzahl                       |    x    |
| city             | string                        | Ort                                |    x    |
| floor            | integer                       | Stockwerk                          |    -    |
| manager          | [Person](/entities/person.md) | Bewirtschafter                     |    -    |
| management       | [Person](/entities/person.md) | Verwaltung                         |    x    |
| owner            | [Person](/entities/person.md) | Eigentümer                         |    -    |
| tenant           | [Person](/entities/person.md) | Mieter/Bewohner                    |    -    |
| maintenance      | [Person](/entities/person.md) | Hauswart(-firma)                   |    -    |
| customattributes | json Key-Value                |                                    |    -    |
