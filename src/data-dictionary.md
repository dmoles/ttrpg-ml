# Data Dictionary

## TTRPG•ML Elements

| Element                       | Definition                                                                                                                                                            |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`rpg-systems`](#rpg-systems) | Container type for a collection of RPG systems.                                                                                                                       |
| [`rpg-system`](#rpg-system)   | A tabletop role-playing game system (as distinguished from particular games using the system).                                                                        |
| [`alt-title`](#alt-title)     | An alternative title for a game or game system, such as a nickname, abbreviation, subtitle, or translated title.                                                      |
| [`edition`](#edition)         | An edition of a game or system.                                                                                                                                       |
| [`identifier`](#identifier)   | An identifier for a game or system.                                                                                                                                   |
| [`scope`](#scope)             | The size and scope of a game, e.g. the required/suggested number of players, time per session, whether or not the game is intended for a multi-session campaign, etc. |
| [`resp-stmt`](#resp-stmt)     | A statement of responsibility for a game or system.                                                                                                                   |
| [`rights`](#rights)           | Rights information for a game or system.                                                                                                                              |
| [`style`](#style)             | A style of play associated with a game or system.                                                                                                                     |
| [`style-name`](#style-name)   | The name of a play style, such as gamist, narrativist, or simulationist.                                                                                              |
| [`style-note`](#style-note)   | An explanatory note regarding play style.                                                                                                                             |
| [`games`](#games)             | A collection of games associated with a game system.                                                                                                                  |
| [`game`](#game)               | A tabletop role-playing game.                                                                                                                                         |
| [`copyright`](#copyright)     | Copyright information for a game or system.                                                                                                                           |
| [`note`](#note)               | An explanatory note attached to other elements.                                                                                                                       |

### rpg-systems

|             |                                                 |
|-------------|-------------------------------------------------|
| Label       | `rpg-systems`                                   |
| URI         | `https://dmoles.info/ttrpgml-0.1/rpg-systems`   |
| Definition  | Container type for a collection of RPG systems. |
| Cardinality | Not repeatable.                                 |

**Note:** The collection may bear some intellectual relationship to one another or be organized simply for convenience. Note that empty collections
are allowed.

Data values:
 
- 0 or more [`rpg-system`](#rpg-system) elements.

### rpg-system

|             |                                                                                                |
|-------------|------------------------------------------------------------------------------------------------|
| Label       | `rpg-system`                                                                                   |
| URI         | `https://dmoles.info/ttrpgml-0.1/rpg-system`                                                   |
| Definition  | A tabletop role-playing game system (as distinguished from particular games using the system). |
| Cardinality | Repeatable.                                                                                    |

### alt-title

|            |                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------|
| Label      | `alt-title`                                                                                                      |
| URI        | `https://dmoles.info/ttrpgml-0.1/alt-title`                                                                      |
| Definition | An alternative title for a game or game system, such as a nickname, abbreviation, subtitle, or translated title. |

### edition

|            |                                           |
|------------|-------------------------------------------|
| Label      | `edition`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/edition` |
| Definition | An edition of a game or system.           |

**Note:** Different editions of a game or system should be recorded as individual `game` or `rpg-system` elements.

### identifier

|            |                                              |
|------------|----------------------------------------------|
| Label      | `identifier`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/identifier` |
| Definition | An identifier for a game or system.          |

### scope

|            |                                                                                                                                                                       |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Label      | `scope`                                                                                                                                                               |
| URI        | `https://dmoles.info/ttrpgml-0.1/scope`                                                                                                                               |
| Definition | The size and scope of a game, e.g. the required/suggested number of players, time per session, whether or not the game is intended for a multi-session campaign, etc. |

### resp-stmt

|            |                                                     |
|------------|-----------------------------------------------------|
| Label      | `resp-stmt`                                         |
| URI        | `https://dmoles.info/ttrpgml-0.1/resp-stmt`         |
| Definition | A statement of responsibility for a game or system. |

### rights

|            |                                          |
|------------|------------------------------------------|
| Label      | `rights`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/rights` |
| Definition | Rights information for a game or system. |

### style

|            |                                                   |
|------------|---------------------------------------------------|
| Label      | `style`                                           |
| URI        | `https://dmoles.info/ttrpgml-0.1/style`           |
| Definition | A style of play associated with a game or system. |

### style-name

|            |                                                                          |
|------------|--------------------------------------------------------------------------|
| Label      | `style-name`                                                             |
| URI        | `https://dmoles.info/ttrpgml-0.1/style-name`                             |
| Definition | The name of a play style, such as gamist, narrativist, or simulationist. |

### style-note

|            |                                              |
|------------|----------------------------------------------|
| Label      | `style-note`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/style-note` |
| Definition | An explanatory note regarding play style.    |

### games

|            |                                                      |
|------------|------------------------------------------------------|
| Label      | `games`                                              |
| URI        | `https://dmoles.info/ttrpgml-0.1/games`              |
| Definition | A collection of games associated with a game system. |

### game

|            |                                        |
|------------|----------------------------------------|
| Label      | `game`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/game` |
| Definition | A tabletop role-playing game.          |

**Note:** properties not specified are assumed to be inherited from the parent `rpg-system`.

### copyright

|            |                                             |
|------------|---------------------------------------------|
| Label      | `copyright`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/copyright` |
| Definition | Copyright information for a game or system. |

### note

|            |                                                 |
|------------|-------------------------------------------------|
| Label      | `note`                                          |
| URI        | `https://dmoles.info/ttrpgml-0.1/note`          |
| Definition | An explanatory note attached to other elements. |

## Dublin Core Terms Elements

| Element                               | Definition                                                |
|---------------------------------------|-----------------------------------------------------------|
| [`dct:creator`](#dct:creator)         | A creator of a game or system.                            |
| [`dct:contributor`](#dct:contributor) | A contributor to a game or system.                        |
| [`dct:publisher`](#dct:publisher)     | The publisher of a game or system.                        |
| [`dct:date`](#dct:date)               | A date, time, or period associated with a game or system. |
| [`dct:title`](#dct:title)             | The title of a game or system.                            |
| [`dct:source`](#dct:source)           | The source of information about a game or system.         |
| [`dct:description`](#dct:description) | A description of a game or system.                        |

### dct:creator

|            |                                               |
|------------|-----------------------------------------------|
| Label      | `dct:creator`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/dct:creator` |
| Definition | A creator of a game or system.                |

### dct:contributor

|            |                                                   |
|------------|---------------------------------------------------|
| Label      | `dct:contributor`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/dct:contributor` |
| Definition | A contributor to a game or system.                |

### dct:publisher

|            |                                                 |
|------------|-------------------------------------------------|
| Label      | `dct:publisher`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/dct:publisher` |
| Definition | The publisher of a game or system.              |

### dct:date

|            |                                                           |
|------------|-----------------------------------------------------------|
| Label      | `dct:date`                                                |
| URI        | `https://dmoles.info/ttrpgml-0.1/dct:date`                |
| Definition | A date, time, or period associated with a game or system. |

### dct:title

|            |                                             |
|------------|---------------------------------------------|
| Label      | `dct:title`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/dct:title` |
| Definition | The title of a game or system.              |

### dct:source

|            |                                                   |
|------------|---------------------------------------------------|
| Label      | `dct:source`                                      |
| URI        | `https://dmoles.info/ttrpgml-0.1/dct:source`      |
| Definition | The source of information about a game or system. |

### dct:description

|            |                                                   |
|------------|---------------------------------------------------|
| Label      | `dct:description`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/dct:description` |
| Definition | A description of a game or system.                |

---
