# Data Dictionary

_Note:_ The TTRPG•ML schema uses both [original elements](#ttrpgml-elements) and
[embedded elements from Dublin Core Terms](#dublin-core-terms-elements).

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

## Element definitions

---

### rpg-systems

|                 |                                                 |
|-----------------|-------------------------------------------------|
| **Label**       | `rpg-systems`                                   |
| **URI**         | `https://dmoles.info/ttrpgml-0.1/rpg-systems`   |
| **Definition**  | Container type for a collection of RPG systems. |
| **Cardinality** | Not repeatable.                                 |

| Child element               | Cardinality |
|-----------------------------|-------------|
| [`rpg-system`](#rpg-system) | 0 or more   |

> **Note:** The systems in the collection may bear some intellectual
> relationship to one another or be organized simply for convenience.
> Empty collections are allowed.

---

### rpg-system

|                 |                                                                                                |
|-----------------|------------------------------------------------------------------------------------------------|
| **Label**       | `rpg-system`                                                                                   |
| **URI**         | `https://dmoles.info/ttrpgml-0.1/rpg-system`                                                   |
| **Definition**  | A tabletop role-playing game system (as distinguished from particular games using the system). |
| **Cardinality** | Repeatable.                                                                                    |

| Child element                        | Cardinality |
|--------------------------------------|-------------|
| [`dct:title`](#dcttitle)             | exactly one |
| [`alt-title`](#alt-title)            | 0 or more   |
| [`edition`](#edition)                | optional    |
| [`identifier`](#identifier)          | optional    |
| [`dct:source`](#dctsource)           | 0 or more   |
| [`scope`](#scope)                    | optional    |
| [`dct:description`](#dctdescription) | exactly one |
| [`resp-stmt`](#resp-stmt)            | optional    |
| [`rights`](#rights)                  | optional    |
| [`style`](#style)                    | 0 or more   |
| [`games`](#games)                    | optional    |

> **Note:** These properties, with the exception of [`style`](#style),
> and [`games`](#games), can also be specified at the [`game`](#game) level.
> Properties not specified for a `game` are presumed to be inherited from
> the parent `rpg-system`.

---

### alt-title

|                  |                                                                                                                  |
|------------------|------------------------------------------------------------------------------------------------------------------|
| **Label**        | `alt-title`                                                                                                      |
| **URI**          | `https://dmoles.info/ttrpgml-0.1/alt-title`                                                                      |
| **Definition**   | An alternative title for a game or game system, such as a nickname, abbreviation, subtitle, or translated title. |
| **Text content** | Any string                                                                                                       |

| **Attribute**               | Values                                                             |
|-----------------------------|--------------------------------------------------------------------|
| `alt-title-type` (required) | `abbreviation`, `nickname`, `subtitle`, `translation`, or `other`. |

---

### edition

|                  |                                           |
|------------------|-------------------------------------------|
| **Label**        | `edition`                                 |
| **URI**          | `https://dmoles.info/ttrpgml-0.1/edition` |
| **Definition**   | An edition of a game or system.           |
| **Text content** | Any string                                |

**Note:** Different editions of a game or system should be recorded as
individual [`game`](#game) or [`rpg-system`](#rpg-system) elements.

---

### identifier

|                  |                                              |
|------------------|----------------------------------------------|
| **Label**        | `identifier`                                 |
| **URI**          | `https://dmoles.info/ttrpgml-0.1/identifier` |
| **Definition**   | An identifier for a game or system.          |
| **Text content** | Any string                                   |

| **Attribute**     | Values                                                  |
|-------------------|---------------------------------------------------------|
| `type` (required) | The identifier type or source (e.g. `wikidata`, `LCCN`) |

---

### scope

|                  |                                                                                                                                                                       |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Label**        | `scope`                                                                                                                                                               |
| **URI**          | `https://dmoles.info/ttrpgml-0.1/scope`                                                                                                                               |
| **Definition**   | The size and scope of a game, e.g. the required/suggested number of players, time per session, whether or not the game is intended for a multi-session campaign, etc. |
| **Text content** | Any string                                                                                                                                                            |

| **Attribute**             | Values                                                                                                                                                  |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `players` (optional)      | The required or suggested number of players of a game. Often expressed as a range, e.g. `3-6`                                                           |
| `session-time` (optional) | The required or suggested time for a game session. Often expressed as a range, e.g. `2-3 hours`.                                                        |
| `campaign` (optional)     | Whether or not the game is intended to be played as a multi-session campaign, expressed as a [boolean value](http://www.w3.org/TR/xmlschema-2/#boolean) |

---

### resp-stmt

|                |                                                     |
|----------------|-----------------------------------------------------|
| **Label**      | `resp-stmt`                                         |
| **URI**        | `https://dmoles.info/ttrpgml-0.1/resp-stmt`         |
| **Definition** | A statement of responsibility for a game or system. |

| Child element                        | Cardinality |
|--------------------------------------|-------------|
| [`dct:creator`](#dctcreator)         | 0 or more   |
| [`dct:contributor`](#dctcontributor) | 0 or more   |
| [`dct:publisher`](#dctpublisher)     | 0 or more   |
| [`dct:date`](#dctdate)               | 0 or more   |
| [`note`](#note)                      | optional    |

> **Note:** At least one of `dct:creator`, `dct:contributor`, or `dct:publisher` must be specified;
> however, any number can be specified, in any order.

---

### rights

|                |                                          |
|----------------|------------------------------------------|
| **Label**      | `rights`                                 |
| **URI**        | `https://dmoles.info/ttrpgml-0.1/rights` |
| **Definition** | Rights information for a game or system. |

| Child element               | Cardinality |
|-----------------------------|-------------|
| [`copyright`](#copyright)   | 0 or more   |
| [`rights-uri`](#rights-uri) | 0 or more   |

---

### style

|                |                                                   |
|----------------|---------------------------------------------------|
| **Label**      | `style`                                           |
| **URI**        | `https://dmoles.info/ttrpgml-0.1/style`           |
| **Definition** | A style of play associated with a game or system. |

| Child element               | Cardinality  |
|-----------------------------|--------------|
| [`style-name`](#style-name) | at least one |
| [`style-note`](#style-note) | optional     |

---

### style-name

|                  |                                                                          |
|------------------|--------------------------------------------------------------------------|
| **Label**        | `style-name`                                                             |
| **URI**          | `https://dmoles.info/ttrpgml-0.1/style-name`                             |
| **Definition**   | The name of a play style, such as gamist, narrativist, or simulationist. |
| **Text content** | `gamist`, `narrativist`, `simulationist`, or `freeform`                  |

> **Note:** For other play styles not captured by this controlled vocabulary, use
> [`style-note`](#style-note).

---

### style-note

|                  |                                              |
|------------------|----------------------------------------------|
| **Label**        | `style-note`                                 |
| **URI**          | `https://dmoles.info/ttrpgml-0.1/style-note` |
| **Definition**   | An explanatory note regarding play style.    |
| **Text content** | Any string.                                  |

---

### games

|                |                                                      |
|----------------|------------------------------------------------------|
| **Label**      | `games`                                              |
| **URI**        | `https://dmoles.info/ttrpgml-0.1/games`              |
| **Definition** | A collection of games associated with a game system. |

| Child element   | Cardinality |
|-----------------|-------------|
| [`game`](#game) | 0 or more   |

> **Note:** Empty collections are allowed.

---

### game

|                |                                        |
|----------------|----------------------------------------|
| **Label**      | `game`                                 |
| **URI**        | `https://dmoles.info/ttrpgml-0.1/game` |
| **Definition** | A tabletop role-playing game.          |

| Child element                        | Cardinality |
|--------------------------------------|-------------|
| [`dct:title`](#dcttitle)             | exactly one |
| [`alt-title`](#alt-title)            | 0 or more   |
| [`edition`](#edition)                | optional    |
| [`identifier`](#identifier)          | optional    |
| [`dct:source`](#dctsource)           | 0 or more   |
| [`scope`](#scope)                    | optional    |
| [`dct:description`](#dctdescription) | exactly one |
| [`resp-stmt`](#resp-stmt)            | optional    |
| [`rights`](#rights)                  | optional    |

> **Note:** This is the same set of properties as [`rpg-system`](#rpg-system),
> except that [`style`](#style) and [`games`](#games) are omitted.
> Properties not specified for a `game` are assumed to be inherited from the
> parent `rpg-system`.

---

### copyright

|                  |                                             |
|------------------|---------------------------------------------|
| **Label**        | `copyright`                                 |
| **URI**          | `https://dmoles.info/ttrpgml-0.1/copyright` |
| **Definition**   | Copyright information for a game or system. |
| **Text content** | Any string.                                 |

---

### rights-uri

|                  |                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------|
| **Label**        | `rights-uri`                                                                                             |
| **URI**          | `https://dmoles.info/ttrpgml-0.1/rights-uri`                                                             |
| **Definition**   | URI for rights information for a game or system, such as a canonical identifier or link to license text. |
| **Text content** | Any URI.                                                                                                 |

---

### note

|                  |                                                 |
|------------------|-------------------------------------------------|
| **Label**        | `note`                                          |
| **URI**          | `https://dmoles.info/ttrpgml-0.1/note`          |
| **Definition**   | An explanatory note attached to other elements. |
| **Text content** | Any string.                                     |

---

### dct:creator

|                  |                                                                                                                                                                                                                    |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Label**        | `dct:creator`                                                                                                                                                                                                      |
| **URI**          | `http://purl.org/dc/terms/creator`                                                                                                                                                                                 |
| **Definition**   | A creator of a game or system.                                                                                                                                                                                     |
| **Text content** | Any string, but note that the [Dublin Core Terms `creator` documentation](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#http://purl.org/dc/terms/creator) recommmends using a URI if possible. |

---

### dct:contributor

|                  |                                        |
|------------------|----------------------------------------|
| **Label**        | `dct:contributor`                      |
| **URI**          | `http://purl.org/dc/terms/contributor` |
| **Definition**   | A contributor to a game or system.     |
| **Text content** | Any string.                            |

---

### dct:publisher

|                  |                                      |
|------------------|--------------------------------------|
| **Label**        | `dct:publisher`                      |
| **URI**          | `http://purl.org/dc/terms/publisher` |
| **Definition**   | The publisher of a game or system.   |
| **Text content** | Any string.                          |

---

### dct:date

|                  |                                                                                                                                                                                                                |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Label**        | `dct:date`                                                                                                                                                                                                     |
| **URI**          | `http://purl.org/dc/terms/date`                                                                                                                                                                                |
| **Definition**   | A date, time, or period associated with a game or system.                                                                                                                                                      |
| **Text content** | Any date, time, or date/time range. See the [Dublin Core Terms `date` documentation](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#http://purl.org/dc/terms/date) for recommended formats. |

---

### dct:title

|                  |                                  |
|------------------|----------------------------------|
| **Label**        | `dct:title`                      |
| **URI**          | `http://purl.org/dc/terms/title` |
| **Definition**   | The title of a game or system.   |
| **Text content** | Any string.                      |

---

### dct:source

|                  |                                                                                                                                                                                                                       |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Label**        | `dct:source`                                                                                                                                                                                                          |
| **URI**          | `http://purl.org/dc/terms/source`                                                                                                                                                                                     |
| **Definition**   | The source of information about a game or system.                                                                                                                                                                     |
| **Text content** | Any string, but note that the [Dublin Core Terms `source` documentation](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#http://purl.org/dc/terms/source) recommmends using a URI or an identifier. |

---

### dct:description

|                  |                                        |
|------------------|----------------------------------------|
| **Label**        | `dct:description`                      |
| **URI**          | `http://purl.org/dc/terms/description` |
| **Definition**   | A description of a game or system.     |
| **Text content** | Any string.                            |
