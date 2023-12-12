# Related Standards

## Related schemas

| Schema            | Namespace URI                                  |
| ---               | ---                                            |
| Dublin Core Terms | `http://purl.org/dc/terms/`                    |
| DataCite 4        | `https://schema.datacite.org/meta/kernel-4.4/` |
| MODS              | `http://www.loc.gov/mods/v3`                   |

I have chosen to include here only very general XML schemas that
I either leveraged directly, or that inspired some elements of the design.

The Dublin Core Terms[^dcmi-nd] schema is referenced directly for
domain-agnostic metadata such as creator, date, rights, and so on. 

The use of an `<alt-title>` element to represent abbreviations, nicknames,
and so on, and an associated attribute `@alt-title-type` to represent the
semantics of the alternate title, is inspired by the `<Title>` element and
`@titleType` attribute from DataCite 4[^datacite-2021], but I decided
against incorporating the DataCite element and attribute directly in order
to separate main and alternate titles, and to be able to incorporate
additional (alternate) title types.

I also considered including MODS[^mods-2022] to represent bibliographic
references for specific game publications, such as the game book in which a
particular system was introduced, or later games based on the same system,
but in the end decided to keep bibliographic information minimal, pro tem.

## Other related work

I found no previous work on representing tabletop role-playing game systems
or rulesets, and only a limited amount of work on representing the games
themselves, or even related works such as boardgames; what I did find was
generally not oriented toward XML, e.g. McCulloch[^mcculloch-2017], on
cataloging boardgames with MARC, or Franco et al.[^franco-2018], on
representing semantics of either computer or tabletop role-playing games in
UML. There is a considerable if scattershot literature on representing
video games, including computer role playing games, and some on
representing rules or game semantics, including again Franco et al., and
also e.g. Zagal et al.[^zagal-2005] on identifying game design elements and
their relationships; but again, none of it is XML-based (most, in fact,
seems to give very little consideration to interoperability or reuse at
all).

### Test

That said, there is also a rich if informal literature among gameplayers
and designers discussing game systems, rules, and mechanics, and essays
like Edwards[^edwards-2004] on the relevance of mechanics to gameplay or
Mary Kuhner’s “threefold model”[^kim-2008] seem likely to provide fruitful
avenues for developing taxonomy and vocabulary.

---

[^dcmi-nd]: DCMI. (n.d.). XML schemas to support the Guidelines for implementing Dublin Core&#8482; in XML. _Dublin Core._ [https://www.dublincore.org/schemas/xmls/](https://www.dublincore.org/schemas/xmls/)

[^datacite-2021]: DataCite Metadata Working Group. (2021). _DataCite Metadata Schema Documentation for the Publication and Citation of Research Data and Other Research Outputs. Version 4.4._ DataCite e.V. [https://doi.org/10.14454/3w3z-sa82](https://doi.org/10.14454/3w3z-sa82)

[^mods-2022]: Library of Congress. (2022). Metadata Object Description Schema: MODS. _Library of Congress Standards._ [https://www.loc.gov/standards/mods/](https://www.loc.gov/standards/mods/)

[^mcculloch-2017]: McCulloch, A. (2017). Cataloguing and Classifying Board and Tabletop Games. _Catalogue and Index,_ 189, 20–24. 

[^franco-2018]: Franco, A. O. R., Rolim, T. V., Santos, A. M. M., Silva, J. W. F., Vidal, V. M. P., Gomes, F. A. C., Castro, M. F., & Maia, J. G. R. (2018). An Ontology for Role Playing Games. _SBC - Proceedings of SBGames 2018._ XVII SBGames, Foz do Iguaçu, Brazil. [https://www.sbgames.org/sbgames2018/files/papers/ComputacaoShort/188294.pdf](https://www.sbgames.org/sbgames2018/files/papers/ComputacaoShort/188294.pdf)

[^zagal-2005]: Zagal, J. P., Michael, M., Clara, F.-V., Brian, H., & Nolan, L. (2005). Towards an Ontological Language for Game Analysis. _Proceedings of the 2005 DiGRA International Conference: Changing Views: Worlds in Play, 3._ [http://www.digra.org/wp-content/uploads/digital-library/06276.09313.pdf](http://www.digra.org/wp-content/uploads/digital-library/06276.09313.pdf)

[^edwards-2004]: Edwards, R. (2004). System Does Matter. _The Forge._ http://www.indie-rpgs.com/_articles/system_does_matter.html

[^kim-2008]: Kim, J. H. (2008). _The Threefold Model FAQ._ [https://www.darkshire.net/~jhkim/rpg/theory/threefold/faq_v1.html](https://www.darkshire.net/~jhkim/rpg/theory/threefold/faq_v1.html)
