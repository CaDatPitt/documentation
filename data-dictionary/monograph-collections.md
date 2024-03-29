---
layout: default
title: Monograph Collection Metadata Element Set
parent: Data Dictionary
nav_order: 5
---

#### [Home](http://cadatpitt.github.io)

# Monograph Collection Metadata Element Set

## Metadata Element List
Monograph collections may contain items from the catalog and/or the digital repository. For this reason, there are catalog, digital repository (hence, "digital"), and mixed versions of the metadata element set. The digital version includes elements in addition to those in the catalog version, which are indicated in the metadata element list as "digital only." The mixed version includes elements from both the catalog and digital versions. By default, the metadata element list for monograph collections includes only item-level description in a single base layer CSV, but monograph collections with items from the digital repository may also use the collection-level base layer from the [archival collection metadata element list](/archival-collections.md).

### Item Level
* [Identifier](#identifier)
* [Title](#title)
* [Uniform Title](#uniform-title)
* [Alternative Title](#alternative-title)
* [Creator](#creator)
* [Contributor](#contributor)
* [Publication Place](#publication-place)
* [Publisher](#publisher)
* [Publication Date](#publication-date)
* [Encoded Date](#encoded-date)
* [Creation Date](#creation-date)
* [Copyright Date](#copyright-date)
* [Edition](#edition)
* [Issuance](#issuance)
* [Language](#language)
* [Type of Resource](#type-of-resource)
* [Format](#format)
* [Extent](#extent)
* [Genre](#genre)
* [Abstract](#abstract)
* [Subject](#subject)
* [Temporal Coverage](#temporal-coverage)
* [Geographic Coverage](#geographic-coverage)
* [Target Audience](#target-audience)
* [Record Identifier](#record-identifier) (digital only)
* [ISBN](#isbn)
* [LCCN](#lccn)
* [OCLCCN](#oclccn)
* [URL](#url)
* [Depositor](#depositor) (digital only)
* [Collection Identifier](#collection-identifier) (digital only)

&nbsp;

## Metadata Element Descriptions
Descriptions below may apply only to the catalog version or the digital version of the metadata element set, indicated by "catalog only" or "digital only," respectively. **Note**: Multiple element values are separated by a triple pipe (`|||`) unless stated otherwise.

### Item Level

#### IDENTIFIER

|CSV Element|id|
|---|---|
|**Description**|A unique identifier that serves as an unambiguous reference to the resource in the institutional catalog system or digital repository.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element Node(s)**|{::nomarkdown}<ul><li>mods:recordInfo/mods:recordIdentifier <strong>(catalog only)</strong></li><li>mods:identifier type="pitt" <strong>(digital only)</strong></li></ul>{:/}|
|**Dublin Core Mapping**|dc.identifier|
|**Vocabulary/Encoding Scheme(s)**|Must be a unique string in the catalog system.|
|**Notes**|Numeric or alpha-numeric string.|
|**Example(s)**|{::nomarkdown}<ul><li>999022363406236</li><li>US-PPiU-ctc197602</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### TITLE

|CSV Element|title|
|---|---|
|**Description**|A name given to the resource.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element Node(s)**|mods:titleInfo{::nomarkdown}<ul><li>mods:title</li><li>mods:subTitle</li><li>mods:nonSort</li></ul>{:/}|
|**Dublin Core Mapping**|dc.title|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|{::nomarkdown}<ul><li>Title is formatted as follows (less the subTitle and/or nonSort where they do not exist): [title]: [subTitle], [nonSort]</li><li>Excludes any Title elements (i.e., mods:titleInfo) with the following @type attribute values: abbreviated, translated, alternative, uniform.</li></ul>{:/}|
|**Example(s)**|{::nomarkdown}<ul><li>Alice's adventures in Wonderland: Through the looking-glass</li><li></li>peace egg: and, A Christmas mumming play, The </li><li>Der Struwwelpeter</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### UNIFORM TITLE

|CSV Element|uniform title|
|---|---|
|**Description**|A distinctive title assigned to a work which has no title or has appeared under more than one title; also used to provide identification for a work when the title by which it is known differs from the title proper of a particular issue or when different publications have identical titles.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|mods:titleInfo[@type="uniform"]/mods:title|
|**Dublin Core Mapping**|dc.title|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>Tales. English. (Dulcken)</li><li>Rime of the ancient mariner</li><li>Struwwelpeter. English</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### ALTERNATIVE TITLE

|CSV Element|alternative title|
|---|---|
|**Description**|An alternative form or variant of the title.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:titleInfo[@type="alternative"]/mods:title|
|**Dublin Core Mapping**|dc.title|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|Struwwelpeter|

[Jump to Item Level](#item-level)

#### CREATOR

|CSV Element|creator|
|---|---|
|Description|A name of an entity responsible for making the content of the resource.|
|Required|No|
|Repeatable|Yes|
|Element Node(s)|{::nomarkdown}<ul><li>mods:name/mods:namePart <em>with</em> mods:role/mods:roleTerm</li><ul><li><strong>Restricted values for roleTerm attribute (ignoring trailing punctuation)</strong>: author, authors, aut, composer, composers, cmp, creator, creators, cre, dubious author, dub, editor, editors, edt, joint author, joint authors, screenwriter, aus, supposed author, supposed authors</li></ul><li>mods:name/mods:namePart[@usage="primary"] <em>without</em> mods:role/mods:roleTerm</li></ul>{:/}|
|Dublin Core Mapping|dc.creator|
|Vocabulary/Encoding Scheme(s)|{::nomarkdown}<ul><li>Free text. No limitations.</li><li><a href="https://id.loc.gov/authorities/names.html" target="_blank">Library of Congress Name Authority File (LCNAF)</a></li><li><a href="http://id.loc.gov/vocabulary/relators.htm" target="_blank">MARC Relators</a> (for roleTerm attribute values)</li></ul>{:/}|
|Notes|Multiple values within the <mods:name> element are separated by comma (,).|
|Example(s)|{::nomarkdown}<ul><li>Boisrobert, Anouck</li><li>Goodrich, Samuel G. (Samuel Griswold), 1793-1860</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### CONTRIBUTOR

|CSV Element|contributor|
|---|---|
|Description|A name of an entity responsible for making contributions to the creation or distribution of the resource.|
|Required|No|
|Repeatable|Yes|
|Element Node(s)|{::nomarkdown}<ul><li>mods:name/mods:namePart <em>with</em> mods:role/mods:roleTerm="contributor"</li><ul><li><strong>Exceptions for possible @roleTerm attribute values</strong>: author, aut, composer, cmp, creator, cre, dubious author, dub, editor, edt, screenwriter, aus</li></ul><li>mods:name/mods:namePart[not(@usage="primary")] <em>without</em> mods:role/mods:roleTerm</li></ul>{:/}|
|Dublin Core Mapping|dc.contributor|
|Vocabulary/Encoding Scheme(s)|{::nomarkdown}<ul><li>Free text. No limitations.</li><li><a href="https://id.loc.gov/authorities/names.htm" target="_blank">Library of Congress Name Authority File (LCNAF)</a></li><li><a href="http://id.loc.gov/vocabulary/relators.htm" target="_blank">MARC Relators</a> (for roleTerm attribute values)</li></ul>{:/}|
|Notes||
|Example(s)|Sinclair, Thomas S., approximately 1805-1881 (lithographer)|<!-- Include the roleTerm value?-->

[Jump to Item Level](#item-level)

#### PUBLICATION PLACE

|CSV Element|publication_place|
|---|---|
|**Description**|Name of a place associated with the publication or issuance of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:originInfo/mods:place/mods:placeTerm[@type="text]|
|**Dublin Core Mapping**|dc.publisher|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/marc/countries/countries_code.html" target="_blank">MARC Code List for Countries</a></li><li><a href="https://www.iso.org/iso-3166-country-codes.html" target="_blank">ISO 3166 — Country Codes</a></li></ul>{:/}|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>London :</li><li>New York</li><li>Philadelphia, Pa. :</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### PUBLISHER

|CSV Element|publisher|
|---|---|
|**Description**|A name of an entity that published, printed, distributed, released, issued, or produced the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|{::nomarkdown}<ul><li>mods:originInfo/mods:publisher</li><li>mods:name/mods:namePart <em>with</em> mods:role/mods:roleterm="publisher"</li></ul>{:/}|
|**Dublin Core Mapping**|dc.publisher|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul><li>Free text. No limitations.</li><li><a href="http://id.loc.gov/authorities/names.html" target="_blank">Library of Congress Name Authority File (LCNAF)</li></ul>{:/}|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>Elliott Publishing Company,</li><li>McLoughlin Bros., 30 Beekman</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### PUBLICATION DATE

|CSV Element|publication_date|
|---|---|
|**Description**|A date associated with the publication or issuance of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:originInfo/mods:dateIssued _without_ attributes|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/marc/bibliographic/" target="_blank">MARC 21 Format for Bibliographic Data</a></li><li>Free text. No limitations.</li></ul>{:/}|
|**Notes**|For more information, see [MARC 21 Format for Bibliographic Data  — 260 - Publication, Distribution, etc.](https://www.loc.gov/marc/bibliographic/bd260.html) and [MARC 21 Format for Bibliographic Data  — 264 - Production, Publication, Distribution, Manufacture, and Copyright Notice (R)](https://www.loc.gov/marc/bibliographic/bd264.html).|
|**Example(s)**|{::nomarkdown}<ul></li><li>[not before 1852?]</li><li>2014.</li><li>1855, ©1853</li><li>[©1924]</li><li>187-?⁾</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### ENCODED DATE

|CSV Element|encoded_date|
|---|---|
|**Description**|A date associated with the creation of the resource and encoded for sorting or other purposes that necessitate normalization.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|mods:originInfo/mods:dateIssued[@encoding="marc"]{::nomarkdown}<ul><li><em>with</em> @encoding="start"</li><li><em>with</em> @encoding="end"</ul>{:/}|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/marc/bibliographic/" target="_blank">MARC 21 Format for Bibliographic Data</a></li><li>Free text. No limitations.</li></ul>{:/}|
|**Notes**|{::nomarkdown}<ul><li>Dates in this field may fall under the following cases:</li><ul><li>Before Common Era (B.C.E.) date</li><li>publication or copyright date</li><li>reprint/reissue date or original date</li><li>modification or creation date</li><li>incorrect date</li><li>date span when resources are valid</li><li>date span recorded in addition to appearing elsewhere</li><li>date range of publication of a multipart item</li><li>date range with earliest and latest possible dates for a questionable date</li></ul><li>Start and end date values are combined and separated by a forward slash (/).</li><li>For more information, see <a href="https://www.loc.gov/marc/bibliographic/bd008a.html" target="_blank">MARC 21 Format for Bibliographic Data  — 008 - All Materials (NR)</a> and <a href="https://www.loc.gov/marc/bibliographic/bd046.html" target="_blank">MARC 21 Format for Bibliographic Data  — 046 - Special Coded Dates.</a></li></ul>{:/}|
|**Example(s)**|{::nomarkdown}<ul></li><li>[191-?]</li><li>1910/1919</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### CREATION DATE

|CSV Element|creation_date|
|---|---|
|**Description**|A date associated with the creation of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:originInfo/mods:dateCreated|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/marc/bibliographic/" target="_blank">MARC 21 Format for Bibliographic Data</a></li><li>Free text. No limitations.</li></ul>{:/}|
|**Notes**|For more information, see [MARC 21 Format for Bibliographic Data  — 260 - Publication, Distribution, etc.](https://www.loc.gov/marc/bibliographic/bd260.html).|
|**Example(s)**|{::nomarkdown}<ul><li>1872</li><li>1972-2010</li><li>(1985 printing)</li><li>184u/uuuu</li><li>1962-01-29</li><li>195u</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### COPYRIGHT DATE

|CSV Element|copyright_date|
|---|---|
|**Description**|A date associated with the creation and copyrighting of the resource; to be used to determine copyright status.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|mods:originInfo/mods:copyrightDate|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/marc/bibliographic/" target="_blank">MARC 21 Format for Bibliographic Data</a></li><li>Free text. No limitations.</li></ul>{:/}|
|**Notes**|For more information, see [MARC 21 Format for Bibliographic Data  — 008 - All Materials (NR)](https://www.loc.gov/marc/bibliographic/bd008a.html).|
|**Example(s)**|1940|

[Jump to Item Level](#item-level)

#### EDITION

|CSV Element|edition|
|---|---|
|**Description**|An identification of the version of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:originInfo/mods:edition|
|**Dublin Core Mapping**|dc.title|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>2. vydání.</li><li>Fifth edition.</li><li>[1st ed.].</li><li>Running Press miniature ed.</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### ISSUANCE

|CSV Element|issuance|
|---|---|
|**Description**|A term that designates how the resource is issued (e.g., monographic, serial, continuing).|
|**Required**|Yes|
|**Repeatable**|No|
|**Element Node(s)**|mods:originInfo/mods:issuance|
|**Dublin Core Mapping**|n/a|
|**Vocabulary/Encoding Scheme(s)**|**Restricted schema data values for issuance subelement**: serial, monographic, multipart monograph, single unit, integrating resource|
|**Notes**|For more information, see [MARC Mapping to MODS for the \<originInfo\>](https://www.loc.gov/standards/mods/mods-mapping.html#publication).|
|**Example(s)**|monographic|

[Jump to Item Level](#item-level)

#### LANGUAGE

|CSV Element|language|
|---|---|
|**Description**|A language in which the content of the resource is expressed.|
|**Required**|Yes|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:language/mods:languageTerm|
|**Dublin Core Mapping**|dc.language|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/standards/iso639-2/php/code_list.php" target="_blank">ISO 639-2b: Codes for the Representation of Names of Languages</li><li><a href="http://www.loc.gov/marc/languages/" target="_blank">MARC Code List for Language</a></li></ul>{:/}|
|**Notes**||
|**Example(s)**|slo|

[Jump to Item Level](#item-level)

#### TYPE OF RESOURCE

|CSV Element|type_of_resource|
|---|---|
|**Description**|A term that specifies the characteristics and general type of content of the resource.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element Node(s)**|mods:typeOfResource|
|**Dublin Core Mapping**|dc.type|
|**Vocabulary/Encoding Scheme(s)**|**Restricted scheme data values for typeOfResource element**: text, cartographic, notated music, sound recording, sound recording - nonmusical, sound recording - musical, still image, moving image, kit three dimensional object, software, multimedia, mixed material|
|**Notes**|For more information, see [MARC Mapping to MODS for the \<typeOfResource\>](https://www.loc.gov/standards/mods/mods-mapping.html#typeofresource) and [MARC 21 Format for Bibliographic Data — Leader](http://www.loc.gov/marc/bibliographic/bdleader.html).|
|**Example(s)**|text|

[Jump to Item Level](#item-level)

#### FORMAT

|CSV Element|format|
|---|---|
|**Description**|A designation of a particular physical presentation of a resource, including the physical form or medium of material for a resource.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element Node(s)**|mods:physicalDescription/mods:form|
|**Dublin Core Mapping**|dc.format|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/standards/valuelist/marccategory.html" target="_blank">MARC Form Category Term List</li><li><a href="https://www.loc.gov/standards/valuelist/rdamedia.html" target="_blank">Term and Code List for RDA Media Types</li><li><a href="https://www.loc.gov/standards/valuelist/rdacarrier.html" target="_blank">Term and Code List for RDA Carrier Types</a></li><li>Anglo-American Cataloguing Rules general material designation (Rule 1.1C)</li><li>Others: <a href="http://www.loc.gov/standards/sourcelist/genre-form.html" target="_blank">Genre/Form Code and Term Source Codes</a></li><li>Free text. No limitations.</li></ul>{:/}|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>print</li><li>unmediated</li><li>volume</li><li>art reproduction</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### EXTENT

|CSV Element|extent|
|---|---|
|**Description**|A statement about the physical extent of the resource, in terms of units of measurement and material.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:physicalDescription/mods:extent|
|**Dublin Core Mapping**|dc.format|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|For more information, see [MARC 21 Format for Bibliographic Data  — 300 - Physical Description](http://www.loc.gov/marc/bibliographic/bd300.html).|
|**Example(s)**|[5] p. : ill. ; 19 x 21 cm.|

[Jump to Item Level](#item-level)

#### GENRE

|CSV Element|genre|
|---|---|
|**Description**|A term that designates a category characterizing a particular style, form, or content embodied by the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|{::nomarkdown}<ul><li>mods:genre</li><li>mods:subject/mods:genre</li></ul>{:/}|
|**Dublin Core Mapping**|dc.type|
|**Vocabulary/Encoding Scheme(s)** *|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/standards/valuelist/marcgt.html" target="_blank">MARC Genre Term List</li><li><a href="https://www.getty.edu/research/tools/vocabularies/aat/" target="_blank">Art & Architecture Thesaurus (AAT)</a></li><li><a href="https://www.oclc.org/research/themes/data-science/fast/download.html" target="_blank">Faceted Application of Subject Terminology (FAST)</a></li><li><a href="https://www.loc.gov/standards/valuelist/marcmuscomp.html" target="_blank">MARC Form of Musical Composition Code List</a></li><li><a href="https://www.loc.gov/rr/print/tgm2/" target="_blank">Library of Congress Genre/Form Terms</a></li><li><a href="https://rbms.info/vocabularies/genre/alphabetical_list.htm" target="_blank">RBMS Controlled Vocabularies: Genre Terms</a></li><li><a href="https://www.loc.gov/rr/print/tgm2/" target="_blank">Thesaurus for graphic materials (TGM II, Genre and physical characteristic terms)</li><li><a href="https://rbms.info/vocabularies/provenance/alphabetical_list.htm" target="_blank">RBMS Controlled Vocabularies: Provenance Evidence Terms</a></li><li><a href="http://experimental.worldcat.org/gsafd/" target="_blank">Guidelines on Subject Access to Individual Works of Fiction, Drama, Etc., 2nd edition</a></li><li><a href="https://www.loc.gov/standards/valuelist/rdacontent.html" target="_blank">Term and Code List for RDA Content Types</a></li><li><a href="http://id.loc.gov/vocabulary/genreFormSchemes/ftamc.html" target="_blank">Form terms for archival and manuscripts control</a></li></ul>{:/}&nbsp;***Note:** This is a working list.|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>Specimens.</li><li>Poetry.</li><li>text</li><li>Juvenile literature</li><li>Printed wrappers (Binding)</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### ABSTRACT

|CSV Element|abstract|
|---|---|
|**Description**|A summary of the content of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:abstract|
|**Dublin Core Mapping**|dc.description|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|Recounts the adventures of the brave and attractive youth, Aurelius, who is apprenticed to a London merchant after his beauty attracts the unwanted attention of the young women of his town. Aurelius ingratiates himself with his master, falls in love with the master's daughter, but, having his love unreciprocated, asks to be sent to Turkey. In Constantinople, Aurelius kills a Turkish prince at a tournament, is imprisoned and sentenced to death, but easily overpowers the two lions sent to eat him, and is rewarded for his valor.|

[Jump to Item Level](#item-level)

#### SUBJECT

|CSV Element|subject|
|---|---|
|**Description**|A term or phrase representing the primary topic(s) on which the resource is focused.|
|**Required**|No
|**Repeatable**|Yes|
|**Element Node(s)**|mods:subject{::nomarkdown}<ul><li>mods:topic</li><li>mods:name</li><li>mods:titleInfo</li><li>mods:occupation</li></ul>{:/}|
|**Dublin Core Mapping**|dc.subject|
|**Vocabulary/Encoding Scheme(s)** *|{::nomarkdown}<ul></li><li><a href="http://id.loc.gov/authorities/names.html" target="_blank">Library of Congress Name Authority File (LCNAF)</li><li><a href="https://www.oclc.org/research/themes/data-science/fast/download.html" target="_blank">Faceted Application of Subject Terminology (FAST)</li><li><a href="https://www.loc.gov/aba/cyac/childsubjhead.html" target="_blank">Children's Subject Headings (CSH)</li><li><a href="http://id.loc.gov/authorities/childrensSubjects.html" target="_blank">Library of Congress Subject Headings Supplemental Vocabularies: Children’s Headings (LCSHAC)</li><li><a href="https://www.nlm.nih.gov/mesh/meshhome.html" target="_blank">Medical Subject Headings (MeSH)</li><li><a href="https://agclass.nal.usda.gov/" target="_blank">National Agricultural Library</li><li><a href="https://rvmweb.bibl.ulaval.ca/eccueil" target="_blank">Répertoire de vedettes-matière (RVM)</a></li></ul>{:/}&nbsp;***Note:** This is a working list.|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>Apprentices</li><li>Chapbooks, English</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### TEMPORAL COVERAGE

|CSV Element|temporal_coverage|
|---|---|
|**Description**|A chronological statement that indicates the date(s) or time period covered by the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:subject/mods:temporal|
|**Dublin Core Mapping**|dc.coverage|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul><li>Free text. No limitations.</li><li><a href="https://www.iso.org/iso-8601-date-and-time-format.html" target="_blank">ISO 8601: Date and Time Format</a></li></ul>{:/}|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>1775-1783</li><li>French occupation, 1798-1801</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### GEOGRAPHIC COVERAGE

|CSV Element|geographic_coverage|
|---|---|
|**Description**|A geographical name or geographical data that indicates the spatial coverage of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:subject{::nomarkdown}<ul><li>mods:geographic</li><li>mods:geographicCode</li><li>mods:hierarchicalGeographic</li><ul><li>mods:continent</li><li>mods:country</li><li>mods:region</li><li>mods:state</li><li>mods:territory</li><li>mods:county</li><li>mods:city</li><li>mods:island</li><li>mods:area</li><li>mods:extraterrestrialArea</li><li>mods:citySection</li></ul><li>mods:cartographics</li><ul><li>mods:scale</li><li>mods:projection</li><li>mods:coordinates</li></ul><li>mods:geographicCoordinates</li></ul>{:/}|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul><li><a href="https://www.loc.gov/marc/geoareas/" target="_blank">MARC Code List for Geographic Areas</a></li><li><a href="https://www.loc.gov/marc/countries/countries_code.html" target="_blank">MARC Code List for Countries</a></li><li><a href="https://www.iso.org/iso-3166-country-codes.html" target="_blank">ISO 3166 — Country Codes</a></li><li>Free text. No limitations.</li></ul>{:/}|
|**Notes**|May be a simple or hierarchical geographical name or area code (e.g., city section, city, county, territory, state, region, country, continent, island, area, extraterrestrial area), cartographic data (e.g., coordinates, scale, projection)|
|**Example(s)**|{::nomarkdown}<ul><li>London, England, Great Britain</li><li>Mississippi</li><li>Saintes-Maries (France)</li><li>n-mx---</li><li>Great Plains</li><li>West (U.S.)</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### TARGET AUDIENCE

|CSV Element|target_audience|
|---|---|
|**Description**|A description of the intellectual level, motivation/interest level, subject interest, or special characteristics of the audience for which the resource is intended.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:targetAudience|
|**Dublin Core Mapping**|n/a|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/marc/bibliographic/bd521.html" target="_blank">MARC 21 Format for Bibliographic Data  — 521 - Target Audience Note</a></li><li><a href="https://www.loc.gov/standards/valuelist/marctarget.html" target="_blank">MARC Target Audience Term List</li><li><a href="https://medietilsynet.no/barn-og-medier/aldersgrenser/" target="_blank">Medietilsynets aldersmerking for film (Medietilsynet)</a></li><li><a href="https://bibliotekutvikling.no/ressurser/kunnskapsorganisering/verktoykasse-for-kunnskapsorganisering/vokabularer/" target="_blank">Målgrupper (National Library of Norway)</a></li><li><a href="http://www.pegi.info/en/index/id/33/" target="_blank">Age ratings for computer games (Pan European Game Information (PEGI)</a></li><li>Free text. No limitations.</li></ul>{:/}|
|**Notes**||
|**Example(s)**|juvenile|

[Jump to Item Level](#item-level)

#### Record Identifier

|CSV Element|record_id|
|---|---|
|**Description**|A unique identifier that serves as an unambiguous reference to the resource in the institutional catalog system.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element Node(s)**|mods:recordInfo/mods:recordIdentifier|
|**Dublin Core Mapping**|dc.identifier|
|**Vocabulary/Encoding Scheme(s)**|Must be a unique string in the catalog system.|
|**Notes**|Numeric code.|
|**Example(s)**|{::nomarkdown}<ul><li>995806413406236</li><li>580641</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### ISBN

|CSV Element|isbn|
|---|---|
|**Description**|International Standard Book Number: A numeric commercial book identifier that is intended to be a unique and unambiguous reference to the resource to distinguish it from other books worldwide.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|mods:identifier[@type="isbn"]|
|**Dublin Core Mapping**|dc.identifier|
|**Vocabulary/Encoding Scheme(s)**|[ISBN Standard](https://www.isbn.org/about_ISBN_standard)|
|**Notes**|A 10- or 13-digita numeric code, sometimes followed by a parenthetical indication of the edition of the book (e.g., hardback, paperback, audiobook, e-book).|
|**Example(s)**|9781250012579 (hardback)|

[Jump to Item Level](#item-level)

#### LCCN

|CSV Element|lccn|
|---|---|
|**Description**|Library of Congress Control Number: A persistent and unique identifier that serves as an unambiguous reference to the resource to distinguish it from other resources worldwide.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|mods:identifier[@type="lccn"]|
|**Dublin Core Mapping**|dc.identifier|
|**Vocabulary/Encoding Scheme(s)**|[LC (Library of Congress) control numbering system](http://www.loc.gov/marc/lccn_structure.html)|
|**Notes**|A numeric code.|
|**Example(s)**|2012042136|

[Jump to Item Level](#item-level)

#### OCLCCN

|CSV Element|oclccn|
|---|---|
|**Description**|Online Computer Library Center Control Number: A persistent and unique identifier that serves as an unambiguous reference to the resource to distinguish it from other resources in the WorldCat and other bibliographic contexts.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|{::nomarkdown}<ul><li>mods:identifier[@type="oclc"]</li><li>mods:identifier[@type="local"] when value contains "(OCoLC)"</li></ul>{:/}|
|**Dublin Core Mapping**|dc.identifier|
|**Vocabulary/Encoding Scheme(s)**|[OCLC Control Number](https://www.oclc.org/ )|
|**Notes**|{::nomarkdown}<ul><li>A numeric or alph-numeric string.</li><li>For more information, see <a href="https://www.oclc.org/developer/news/2012/oclc-control-number-expansion-in-2013.en.html" target="_blank">"OCLC control number expansion in 2013"</a>.</ul>{:/}|
|**Example(s)**|{::nomarkdown}<ul><li>ocn819860760</li><li>819860760</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### URL

|CSV Element|url|
|---|---|
|**Description**|A Uniform Resource Location (URL) of the resource; an electronic location from which the resource is available.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:location/mods:url|
|**Dublin Core Mapping**|dc.identifier|
|**Vocabulary/Encoding Scheme(s)**|[Uniform Resource Location (URL)](https://www.w3.org/Addressing/URL/url-spec.html)|
|**Notes**|URL links to proprietary resources include an EZProxy URL to enable access to library e-resources from off campus.|
|**Example(s)**|http://www.archive.org/details/littlegirlinoldp00indoug|

[Jump to Item Level](#item-level)

#### DEPOSITOR

|CSV Element|depositor|
|---|---|
|**Description**|An official name of the institution responsible for depositing the resource.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element Node(s)**|mods:name/mods:namePart _with_ mods:role/mods:roleTerm="depositor"|
|**Dublin Core Mapping**|n/a|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|University of Pittsburgh|

[Jump to Item Level](#item-level)

#### COLLECTION IDENTIFIER

|CSV Element|collection_id|
|---|---|
|**Description**|A digital collection to which the resource belongs.|
|**Required**|Yes|
|**Repeatable**|Yes|
|**Element Node(s)**|rdf:Description/fedora:isMemberOfCollection[@rdf:resource]|
|**Dublin Core Mapping**|dc.relation|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|Alpha-numeric string with special characters, i.e. a colon (:) and a period (.), formatted as follows: pitt:collection_nnn|
|**Example(s)**|pitt:collection.120|

[Jump to Item Level](#item-level)
