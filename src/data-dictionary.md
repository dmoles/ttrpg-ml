# Data Dictionaryz

## Overview

| Element                               | Definition                                                                                                       |
| -------                               | ----------                                                                                                       |
| [`rpg-systems`](#rpg-systems)         | Container type for a collection of RPG systems.                                                                  |
| [`rpg-system`](#rpg-system)           |                                                                                                                  |
| [`alt-title`](#alt-title)             | An alternative title for a game or game system, such as a nickname, abbreviation, subtitle, or translated title. |
| [`edition`](#edition)                 | An edition of a game or system.                                                                                  |
| [`identifier`](#identifier)           |                                                                                                                  |
| [`scope`](#scope)                     |                                                                                                                  |
| [`resp-stmt`](#resp-stmt)             | A statement of responsibility for a game or system.                                                              |
| [`rights`](#rights)                   | Rights information for a game or system.                                                                         |
| [`style`](#style)                     |                                                                                                                  |
| [`style-name`](#style-name)           |                                                                                                                  |
| [`style-note`](#style-note)           | An explanatory note regarding play style.                                                                        |
| [`games`](#games)                     | A collection of games associated with a game system.                                                             |
| [`game`](#game)                       | A tabletop role-playing game.                                                                                    |
| [`copyright`](#copyright)             | Copyright information for a game or system.                                                                      |
| [`note`](#note)                       | An explanatory note attached to other elements.                                                                  |
| [`dct:creator`](#dct:creator)         |                                                                                                                  |
| [`dct:contributor`](#dct:contributor) |                                                                                                                  |
| [`dct:publisher`](#dct:publisher)     |                                                                                                                  |
| [`dct:date`](#dct:date)               |                                                                                                                  |
| [`dct:title`](#dct:title)             |                                                                                                                  |
| [`dct:source`](#dct:source)           |                                                                                                                  |
| [`dct:description`](#dct:description) |                                                                                                                  |


## Elements


### rpg-systems

|            |                                                 |
| ---        | ---                                             |
| Label      | `rpg-systems`                                   |
| URI        | `https://dmoles.info/ttrpgml-0.1/rpg-systems`   |
| Definition | Container type for a collection of RPG systems. |

**Note:** The collection may bear some intellectual relationship to one another or be organized simply for convenience. Note that empty collections are allowed.


### rpg-system

|            |                                              |
| ---        | ---                                          |
| Label      | `rpg-system`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/rpg-system` |
| Definition |                                              |


### alt-title

|            |                                                                                                                  |
| ---        | ---                                                                                                              |
| Label      | `alt-title`                                                                                                      |
| URI        | `https://dmoles.info/ttrpgml-0.1/alt-title`                                                                      |
| Definition | An alternative title for a game or game system, such as a nickname, abbreviation, subtitle, or translated title. |


### edition

|            |                                           |
| ---        | ---                                       |
| Label      | `edition`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/edition` |
| Definition | An edition of a game or system.           |

**Note:** Different editions of a game or system should be recorded as individual `game` or `rpg-system` elements.


### identifier

|            |                                              |
| ---        | ---                                          |
| Label      | `identifier`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/identifier` |
| Definition |                                              |


### scope

|            |                                         |
| ---        | ---                                     |
| Label      | `scope`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/scope` |
| Definition |                                         |


### resp-stmt

|            |                                                     |
| ---        | ---                                                 |
| Label      | `resp-stmt`                                         |
| URI        | `https://dmoles.info/ttrpgml-0.1/resp-stmt`         |
| Definition | A statement of responsibility for a game or system. |


### rights

|            |                                          |
| ---        | ---                                      |
| Label      | `rights`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/rights` |
| Definition | Rights information for a game or system. |


### style

|            |                                         |
| ---        | ---                                     |
| Label      | `style`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/style` |
| Definition |                                         |


### style-name

|            |                                              |
| ---        | ---                                          |
| Label      | `style-name`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/style-name` |
| Definition |                                              |


### style-note

|            |                                              |
| ---        | ---                                          |
| Label      | `style-note`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/style-note` |
| Definition | An explanatory note regarding play style.    |


### games

|            |                                                      |
| ---        | ---                                                  |
| Label      | `games`                                              |
| URI        | `https://dmoles.info/ttrpgml-0.1/games`              |
| Definition | A collection of games associated with a game system. |


### game

|            |                                        |
| ---        | ---                                    |
| Label      | `game`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/game` |
| Definition | A tabletop role-playing game.          |

**Note:** properties not specified are assumed to be inherited from the parent `rpg-system`.


### copyright

|            |                                             |
| ---        | ---                                         |
| Label      | `copyright`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/copyright` |
| Definition | Copyright information for a game or system. |


### note

|            |                                                 |
| ---        | ---                                             |
| Label      | `note`                                          |
| URI        | `https://dmoles.info/ttrpgml-0.1/note`          |
| Definition | An explanatory note attached to other elements. |


### dct:creator

|            |                                               |
| ---        | ---                                           |
| Label      | `dct:creator`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/dct:creator` |
| Definition |                                               |


### dct:contributor

|            |                                                   |
| ---        | ---                                               |
| Label      | `dct:contributor`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/dct:contributor` |
| Definition |                                                   |


### dct:publisher

|            |                                                 |
| ---        | ---                                             |
| Label      | `dct:publisher`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/dct:publisher` |
| Definition |                                                 |


### dct:date

|            |                                            |
| ---        | ---                                        |
| Label      | `dct:date`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/dct:date` |
| Definition |                                            |


### dct:title

|     |     |
| --- | --- |
| Label | `dct:title` |
| URI | `https://dmoles.info/ttrpgml-0.1/dct:title` |
| Definition |  |


### dct:source

|            |                                              |
| ---        | ---                                          |
| Label      | `dct:source`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/dct:source` |
| Definition |                                              |


### dct:description

|            |                                                   |
| ---        | ---                                               |
| Label      | `dct:description`                                 |
| URI        | `https://dmoles.info/ttrpgml-0.1/dct:description` |
| Definition |                                                   |
