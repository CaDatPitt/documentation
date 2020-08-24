---
layout: default
title: Serial Collection Metadata Element Set
parent: Data Dictionary
nav_order: 4
---

# Serial Collection Metadata Element Set

## Metadata Element List
Serial collections may contain items from the catalog and/or the digital repository. For this reason, there is a catalog version and a digital repository (hence, "digital") version of the metadata element set. The digital version includes elements in addition to those in the catalog version, which are indicated in the metadata element list as "digital only." By default, the metadata element list for serial collections includes only item-level description in a single base layer CSV, but serial collections with items from the digital repository may also use the collection-level base layer from the metadata element list for archival collections.

### Item Level
* [Identifier](#identifier)
* [Title](#title)
* [Uniform Title](#title)
* [Alternative Title](#title)
* [Enumeration and Chronology](#enumeration-and-chronology) (digital only)
* [Associated Name](#associated-name)
* [Publication Place](#publication-place)
* [Publisher](#publisher)
* [Start Date](#start-date)
* [End Date](#end-date)
* [Edition](#edition)
* [Issuance](#issuance)
* [Frequency](#frequency)
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
* [Preceded By](#preceded-by)
* [Succeeded By](#succeeded-by)
* [Copyright Status](#copyright-status) (digital only)
* [Copyright Holder](#copyright-holder) (digital only)
* [Copyright Note](#copyright-note) (digital only)
* [ISSN](#issn)
* [LCCN](#lccn)
* [OCLCCN](#oclccn)
* [URL](#url)
* [Collection Identifier](#collection-identifier) (digital only)
* [Depositor](#depositor) (digital only)

&nbsp;

## Metadata Element Descriptions
Descriptions below may apply only to the catalog version or the digital version of the metadata element set, indicated by "catalog only" or "digital only," respectively. **Note**: Multiple element values are separated by a triple pipe (`|||`) unless stated otherwise.

### Item Level

#### IDENTIFIER

|CSV Element|id|
|:---|:---|
|**Description**|A unique identifier that serves as an unambiguous reference to the resource in the institutional catalog system or digital repository.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element Node(s)**|<ul><li>mods:recordInfo/mods:recordIdentifier **(catalog only)**</li><li>mods:identifier[@type="pitt"] **(digital only)**</li></ul>|
|**Dublin Core Mapping**|dc.identifier|
|**Vocabulary/Encoding Scheme(s)**|Must be a unique string in the catalog or digital repository system.|
|**Notes**|Alpha-numeric or numeric string, with or without special characters like periods (.) or dashes (-)|
|**Example(s)**|<ul><li>999022363406236</li><li>31735047439264</li></ul>|

[Jump to Item Level](#item-level)

#### TITLE

|CSV Element|title|
|:---|:---|
|**Description**|A name given to the resource.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element Node(s)**|mods:titleInfo<ul><li>mods:title</li><li>mods:subTitle</li><li>mods:nonSort</li></ul>|
|**Dublin Core Mapping**|dc.title|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|<ul><li>Title is formatted as following (less the subTitle and/or nonSort where they do not exist): [title]: [subTitle], [nonSort]</li><li>If value of subTitle is parenthetical, it should be formatted as following (less the nonSort where if it does not exist): [title] [subTitle], [nonSort] </li><li>Excludes any Title elements (i.e., mods:titleInfo) with the following @type attribute values: abbreviated, translated, alternative, uniform.</li></ul>|
|**Example(s)**|<ul><li>Courier</li><li>Critical Studies in Teaching and Learning (CriSTaL)</li><li>Tip top weekly: an ideal publication for the American youth</li><li>Shooting Star Review</li></ul>|

[Jump to Item Level](#item-level)

#### UNIFORM TITLE

|CSV Element|uniform title|
|:---|:---|
|**Description**|A distinctive title assigned to a work which has no title or has appeared under more than one title; also used to provide identification for a work when the title by which it is known differs from the title proper of a particular issue or when different publications have identical titles.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|mods:titleInfo[@type="uniform"]/mods:title|
|**Dublin Core Mapping**|dc.title|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|<ul><li>Courier (Pittsburgh, Pa. : City edition)</li><li>Shooting star review</li></ul>|

[Jump to Item Level](#item-level)

#### ALTERNATIVE TITLE

|CSV Element|alternative title|
|:---|:---|
|**Description**|An alternative form or variant of the title.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:titleInfo[@type="alternative"]/mods:title|
|**Dublin Core Mapping**|dc.title|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|<ul><li>CriSTaL</li><li>Shooting star</li></ul>|

[Jump to Item Level](#item-level)

#### ENUMERATION AND CHRONOLOGY

|CSV Element|enumeration_chronology|
|:---|:---|
|**Description**|A numeric and/or alphabetic designation used to identify the resource and its sequential and/or chronological relationship to a serial, of which it is a part, as a whole.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|mods:titleInfo/partNumber|
|**Dublin Core Mapping**|dc.title|
|**Vocabulary/Encoding Scheme(s)**|<ul><li>[ANSI/NISO Z39.71-2006 (R2011) Holdings Statements for Bibliographic Items](https://www.niso.org/publications/z3971-2006-r2011)</li><li>NISO Z39.44 Serial Holdings Standard (superseded by ANSI/NISO Z39.71-2006)</li><li>Free text. No limitations.</li></ul>|
|**Notes**||
|**Example(s)**|vol. 12, no. 8|

[Jump to Item Level](#item-level)

#### ASSOCIATED NAME

|CSV Element|associated_name|
|:---|:---|
|**Description**|A name of an entity associated in some way with the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:name/mods:namePart _with_ mods:role/mods:roleterm<ul><li>**Exception for possible @roleTerm attribute values**: depositor</li></ul>|
|**Dublin Core Mapping**|<ul><li>dc.creator</li><li>dc.contributor</li></ul>|
|**Vocabulary/Encoding Scheme(s)**|<ul><li>Free text. No limitations.</li><li>[Library of Congress Name Authority File (LCNAF)](https://id.loc.gov/authorities/names.html)</li></ul>|
|**Notes**|Multiple values within the <mods:name> element are separated by comma (,).|
|**Example(s)**|<ul><li>International Union of Mine, Mill, and Smelter Workers</li><li>Meinhof, Carl, 1857-1944</li></ul>|

[Jump to Item Level](#item-level)

#### PUBLICATION PLACE

|CSV Element|publication_place|
|:---|:---|
|**Description**|Name of a place associated with the publication or issuance of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:originInfo/mods:place/mods:placeTerm[@type="text]|
|**Dublin Core Mapping**|dc.publisher|
|**Vocabulary/Encoding Scheme(s)**|<ul><li>[MARC Code List for Countries](https://www.loc.gov/marc/countries/countries_code.html)</li><li>[ISO 3166 — Country Codes](https://www.iso.org/iso-3166-country-codes.html)</li></ul>|
|**Notes**||
|**Example(s)**|<ul><li>Berlin [etc.]</li><li>Minneapolis and St. Paul</li><li>Petersburg, VA</li><li>New Delhi]</li></ul>|

[Jump to Item Level](#item-level)

#### PUBLISHER

|CSV Element|publisher|
|:---|:---|
|**Description**|A name of an entity that published, printed, distributed, released, issued, or produced the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|<ul><li>mods:originInfo/mods:publisher</li><li>mods:name/namePart _with_ mods:role/mods:roleTerm="publisher"</li></ul>|
|**Dublin Core Mapping**|dc.publisher|
|**Vocabulary/Encoding Scheme(s)**|<ul><li>Free text. No Limitations.</li><li>[Library of Congress Name Authority File (LCNAF)](http://id.loc.gov/authorities/names.html)</li></ul>|
|**Notes**||
|**Example(s)**|<ul><li>Afro-Hispanic Institute</li><li>Sandra Gould Ford</li></ul>|

[Jump to Item Level](#item-level)

#### PUBLICATION DATE

|CSV Element|publication_date|
|:---|:---|
|**Description**|A date associated with the publication or issuance of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|<ul><li>mods:originInfo/mods:dateIssued</li><li>mods:originInfo/mods:dateOther[@type="sort"] **(digital only)**</li></ul>|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|
|**Notes**|For more information, see [MARC 21 Format for Bibliographic Data  — 260 - Publication, Distribution, etc.](https://www.loc.gov/marc/bibliographic/bd260.html).|
|**Example(s)**|<ul><li>[1994]-</li><li>2011-</li><li>1940-02-01T00:00:00 **(digital only)**</li></ul>|

[Jump to Item Level](#item-level)

#### START DATE

|CSV Element|start_date|
|:---|:---|
|**Description**|A date associated with the beginning of publication of the resource or the serial of which it is a part.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|<ul><li>mods:originInfo/mods:dateIssued[@point="start"]</li><li>mods:originInfo/mods:dateCreated[@point="start"] **(digital only)**</li></ul>|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|For more information, see [MARC 21 Format for Bibliographic Data  — 008 - All Materials (NR)](https://www.loc.gov/marc/bibliographic/bd008a.html).|
|**Example(s)**|<ul><li>19uu</li><li>1965</li></ul>|

[Jump to Item Level](#item-level)

#### END DATE

|CSV Element|end_date|
|:---|:---|
|**Description**|A date associated with the end of publication of the resource or the continuing resource (e.g., serial) of which it is a part.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|<ul><li>mods:originInfo/mods:dateIssued[@point="end"]</li><li>mods:originInfo/mods:dateCreated[@point="end"]</li></ul>|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|<ul><li>1992</li><li>9999</li><li>uuuu</li></ul>|

[Jump to Item Level](#item-level)

#### EDITION

|CSV Element|edition|
|:---|:---|
|**Description**|An identification of the version of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:originInfo/mods:edition|
|**Dublin Core Mapping**|dc.title|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|For more information, see [MARC 21 Format for Bibliographic Data  — 250 - Edition Statement](http://www.loc.gov/marc/bibliographic/bd250.html).|
|**Example(s)**|City ed.|

[Jump to Item Level](#item-level)

#### ISSUANCE

|CSV Element|issuance|
|:---|:---|
|**Description**|A term that designates how the resource is issued (e.g., monographic, serial, continuing).|
|**Required**|Yes|
|**Repeatable**|No|
|**Element Node(s)**|mods:originInfo/mods:issuance|
|**Dublin Core Mapping**|n/a|
|**Vocabulary/Encoding Scheme(s)**|**Restricted schema data values for issuance subelement**: serial, monographic, multipart monograph, single unit, integrating resource|
|**Notes**|For more information, see [MARC Mapping to MODS for the <originInfo>](https://www.loc.gov/standards/mods/mods-mapping.html#publication).|
|**Example(s)**|serial|

[Jump to Item Level](#item-level)

#### FREQUENCY

|CSV Element|frequency|
|:---|:---|
|**Description**|A statement of publication frequency or pattern of the resource or the serial of which it is a part.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:originInfo/mods:frequency|
|**Dublin Core Mapping**|n/a|
|**Vocabulary/Encoding Scheme(s)**|[MARC 21 Frequency of Issue Term List](https://www.loc.gov/standards/valuelist/marcfrequency.html)|
|**Notes**||
|**Example(s)**|<ul><li>Weekly</li><li>Unknown</li></ul>|

[Jump to Item Level](#item-level)

#### LANGUAGE

|CSV Element|language|
|:---|:---|
|**Description**|A language in which the content of the resource is expressed.|
|**Required**|Yes|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:language/mods:languageTerm|
|**Dublin Core Mapping**|dc.language|
|**Vocabulary/Encoding Scheme(s)**|<ul><li>[ISO 639-2 Language Code List - Codes for the Representation of Names of Languages](https://www.loc.gov/standards/iso639-2/php/code_list.php)</li><li>[MARC Code List for Language](http://www.loc.gov/marc/languages/)</li><ul>|
|**Notes**||
|**Example(s)**|eng|

[Jump to Item Level](#item-level)

#### TYPE OF RESOURCE

|CSV Element|type_of_resource|
|:---|:---|
|**Description**|A term that specifies the characteristics and general type of content of the resource.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element Node(s)**|mods:typeOfResource|
|**Dublin Core Mapping**|dc.type|
|**Vocabulary/Encoding Scheme(s)**|**Restricted scheme data values for typeOfResource element**: text, cartographic, notated music, sound recording, sound recording - nonmusical, sound recording - musical, still image, moving image, kit three dimensional object, software, multimedia, mixed material|
|**Notes**|For more information, see [MARC 21 Format for Bibliographic Data — Leader](http://www.loc.gov/marc/bibliographic/bdleader.html).|
|**Example(s)**|text|

[Jump to Item Level](#item-level)

#### FORMAT

|CSV Element|format|
|:---|:---|
|**Description**|A designation of a particular physical presentation of a resource, including the physical form or medium of material for a resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:physicalDescription/mods:form|
|**Dublin Core Mapping**|dc.format|
|**Vocabulary/Encoding Scheme(s)**|<ul><li>[MARC Form Category Term List](https://www.loc.gov/standards/valuelist/marccategory.html)</li><li>[Term and Code List for RDA Media Types](https://www.loc.gov/standards/valuelist/rdamedia.html)</li><li>[Term and Code List for RDA Carrier Types](https://www.loc.gov/standards/valuelist/rdacarrier.html)</li><li>Anglo-American Cataloguing Rules general material designation (Rule 1.1C)</li><li>Others: [Genre/Form Code and Term Source Codes](http://www.loc.gov/standards/sourcelist/genre-form.html)</li><li>Free text. No limitations.</li></ul>|
|**Notes**||
|**Example(s)**|<ul><li>print</li><li>print\|\|\|unmediated\|\|\|volume</li></ul>|

[Jump to Item Level](#item-level)

#### EXTENT

|CSV Element|extent|
|:---|:---|
|**Description**|A statement about the physical extent of the resource, in terms of units of measurement and material.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:physicalDescription/mods:extent|
|**Dublin Core Mapping**|dc.format|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|For more information, see MARC 21 Format for Bibliographic Data  — 300 - Physical Description: http://www.loc.gov/marc/bibliographic/bd300.html|
|**Example(s)**|93 v. in 91. : ill. ; 23 cm.|

[Jump to Item Level](#item-level)

#### GENRE

|CSV Element|genre|
|:---|:---|
|**Description**|A term that designates a category characterizing a particular style, form, or content embodied by the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|<ul><li>mods:genre</li><li>mods:subject/mods:genre</li></ul>|
|**Dublin Core Mapping**|dc.type|
|**Vocabulary/Encoding Scheme(s)** *|<ul><li>[MARC Genre Term List](https://www.loc.gov/standards/valuelist/marcgt.html)</li><li>[Art & Architecture Thesaurus (AAT)](https://www.getty.edu/research/tools/vocabularies/aat/)</li><li>[Faceted Application of Subject Terminology (FAST)](https://www.oclc.org/research/themes/data-science/fast/download.html)</li><li>[MARC Form of Musical Composition Code List](https://www.loc.gov/standards/valuelist/marcmuscomp.html)</li><li>[Library of Congress Genre/Form Terms](https://www.loc.gov/rr/print/tgm2/)</li><li>[RBMS Controlled Vocabularies: Genre Terms](https://rbms.info/vocabularies/genre/alphabetical_list.htm)</li><li>[Thesaurus for graphic materialsTGM II, Genre and physical characteristic terms](https://www.loc.gov/rr/print/tgm2/)</li><li>[RBMS Controlled Vocabularies: Provenance Evidence Terms](https://rbms.info/vocabularies/provenance/alphabetical_list.htm)</li><li>[Guidelines on Subject Access to Individual Works of Fiction, Drama, Etc., 2nd edition](http://experimental.worldcat.org/gsafd/)</li><li>[Term and Code List for RDA Content Types](https://www.loc.gov/standards/valuelist/rdacontent.html)</li><li>[Form terms for archival and manuscripts control](http://id.loc.gov/vocabulary/genreFormSchemes/ftamc.html)</li></ul>&nbsp;***Note:** This is a working list.|
|**Notes**||
|**Example(s)**|<ul><li>text</li><li>Periodicals.</li><li>newspaper</li></ul>|

[Jump to Item Level](#item-level)

#### ABSTRACT

|CSV Element|abstract|
|:---|:---|
|**Description**|A summary of the content of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:abstract|
|**Dublin Core Mapping**|dc.description|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|<ul><li>Some special issues devoted to the literatures of other minorities.</li><li>Describes political and economic policy, the domestic economy, foreign trade and payments. Provides 18-24 month forecasts.</li></ul>|

[Jump to Item Level](#item-level)

#### SUBJECT

|CSV Element|subject|
|:---|:---|
|**Description**|A term or phrase representing the primary topic(s) on which the resource is focused.|
|**Required**|No
|**Repeatable**|Yes|
|**Element Node(s)**|mods:subject<ul><li>mods:topic</li><li>mods:name</li><li>mods:titleInfo</li><li>mods:occupation</li></ul>|
|**Dublin Core Mapping**|dc.subject|
|**Vocabulary/Encoding Scheme(s)** *|<ul><li>[Library of Congress Name Authority File (LCNAF)](http://id.loc.gov/authorities/names.html)</li><li>[Faceted Application of Subject Terminology (FAST)](https://www.oclc.org/research/themes/data-science/fast/download.html)</li><li>[Children's Subject Headings (CSH)](https://www.loc.gov/aba/cyac/childsubjhead.html)</li><li>[Library of Congress Subject Headings Supplemental Vocabularies: Children’s Headings (LCSHAC)](http://id.loc.gov/authorities/childrensSubjects.html)</li><li>[Medical Subject Headings (MeSH)](https://www.nlm.nih.gov/mesh/meshhome.html)</li><li>[National Agricultural Library](https://agclass.nal.usda.gov/)</li><li>[Répertoire de vedettes-matière (RVM)](https://rvmweb.bibl.ulaval.ca/eccueil)</li></ul>&nbsp;***Note:** This is a working list.|
|**Notes**||
|**Example(s)**|<ul><li>Advertising</li><li>Pittsburgh</li></ul>|

[Jump to Item Level](#item-level)

#### TEMPORAL COVERAGE

|CSV Element|temporal_coverage|
|:---|:---|
|**Description**|A chronological statement that indicates the date(s) or time period covered by the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:subject/mods:temporal|
|**Dublin Core Mapping**|dc.coverage|
|**Vocabulary/Encoding Scheme(s)**|<ul><li>Free text. No limitations.</li><li>[ISO 8601 — Date and Time Format](https://www.iso.org/iso-8601-date-and-time-format.html)</li></ul>|
|**Notes**||
|**Example(s)**|<ul><li>20th century</li><li>1978-1989</li></ul>|

[Jump to Item Level](#item-level)

#### GEOGRAPHIC COVERAGE

|CSV Element|geographic_coverage|
|:---|:---|
|**Description**|A geographical name or geographical data that indicates the spatial coverage of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:subject<ul><li>mods:geographic</li><li>mods:geographicCode</li><li>mods:hierarchicalGeographic</li><ul><li>mods:continent</li><li>mods:country</li><li>mods:region</li><li>mods:state</li><li>mods:territory</li><li>mods:county</li><li>mods:city</li><li>mods:island</li><li>mods:area</li><li>mods:extraterrestrialArea</li><li>mods:citySection</li></ul><li>mods:cartographics</li><ul><li>mods:scale</li><li>mods:projection</li><li>mods:coordinates</li></ul><li>mods:geographicCoordinates</li></ul>|
|**Vocabulary/Encoding Scheme(s)**|<ul><li>[MARC Code List for Geographic Areas](https://www.loc.gov/marc/geoareas/)</li><li>[MARC Code List for Countries](https://www.loc.gov/marc/countries/countries_code.html)</li><li>[ISO 3166 — Country Codes](https://www.iso.org/iso-3166-country-codes.html)</li><li>Free text. No limitations.</li></ul>|
|**Notes**|May be a simple or hierarchical geographical name or area code (e.g., city section, city, county, territory, state, region, country, continent, island, area, extraterrestrial area), cartographic data (e.g., coordinates, scale, projection)|
|**Example(s)**|<ul><li>South African</li><li>Iowa, Des Moines, United States</ul>|

[Jump to Item Level](#item-level)

#### TARGET AUDIENCE

|CSV Element|target_audience|
|:---|:---|
|**Description**|A description of the intellectual level, motivation/interest level, subject interest, or special characteristics of the audience for which the resource is intended.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:targetAudience|
|**Dublin Core Mapping**|n/a|
|**Vocabulary/Encoding Scheme(s)**|<ul><li>[MARC Target Audience Term List](https://www.loc.gov/standards/valuelist/marctarget.html)</li><li>[Medietilsynets aldersmerking for film (Medietilsynet)](https://medietilsynet.no/barn-og-medier/aldersgrenser/)</li><li>[Målgrupper (National Library of Norway)](https://bibliotekutvikling.no/ressurser/kunnskapsorganisering/verktoykasse-for-kunnskapsorganisering/vokabularer/)</li><li>[Age ratings for computer games (Pan European Game Information (PEGI))](http://www.pegi.info/en/index/id/33/)</li><li>Free text. No limitations.</li></ul>|
|**Notes**|For more information, see [MARC 21 Format for Bibliographic Data  — 521 - Target Audience Note](https://www.loc.gov/marc/bibliographic/bd521.html).|
|**Example(s)**|<ul><li>Black newspaper." Cf. Black periodicals and newspapers.</li><li>Juvenile</li></ul>|

[Jump to Item Level](#item-level)

#### PREECEDED BY

|CSV Element|preceeded_by|
|:---|:---|
|**Description**|A predecessor to the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:relatedItem[@type="preceding"]|
|**Dublin Core Mapping**|dc.relation|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|Semi-weekly Louisianian|

[Jump to Item Level](#item-level)

#### SUCCEDED BY

|CSV Element|succeeded_by|
|:---|:---|
|**Description**|A successor to the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:relatedItem[@type="succeeding"]|
|**Dublin Core Mapping**|dc.relation|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|Beeton's boy's annual|

[Jump to Item Level](#item-level)

#### COPYRIGHT STATUS

|CSV Element|copyright_status|
|:---|:---|
|**Description**|An indication of the copyright status for the resource.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|mods:accessCondition/copyrightMD:copyright[@copyright.status]|
|**Dublin Core Mapping**|dc.rights|
|**Vocabulary/Encoding Scheme(s)**|**Restricted scheme data values for typeOfResource element**:&nbsp;<ul><li>copyrighted — Under copyright.</li><li>pd — Public domain: No further information.</li><li>pd_usfed — Public domain: US Federal document.</li><li>pd_holder — Public domain: Item dedicated to the public domain by the rights holder.</li><li>pd_expired — Public domain: Item in the public domain because of expiration of copyright based on U.S. law.</li><li>unknown — Copyright status of the resource is unknown.</li></ul>|
|**Notes**||
|**Example(s)**|copyrighted|

[Jump to Item Level](#item-level)

#### COPYRIGHT HOLDER

|CSV Element|copyright_holder|
|:---|:---|
|**Description**|A name of either an entity responsible for creating the resource or an entity identified as a copyright holder for the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:accessCondition/copyrightMD:copyright/copyrightMD:name|
|**Dublin Core Mapping**|dc.rights|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|Sandra Gould Ford|

[Jump to Item Level](#item-level)

#### COPYRIGHT NOTE

|CSV Element|copyright_note|
|:---|:---|
|**Description**|A general note relating to one of the following aspects of the resource: its creator(s), its publication, its rights holder(s), or services available pertaining to it.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:accessCondition/copyrightMD:copyright/copyrightMD:note|
|**Dublin Core Mapping**|dc.rights|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|Permission granted by owner/publisher|

[Jump to Item Level](#item-level)

<!--#### RECORD IDENTIFIER
|CSV Element|record_id|
|:---|:---|
|**Description**|A unique identifier that serves as an unambiguous reference to the resource in the institutional catalog system.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|mods:recordInfo/mods:recordIdentifier **(digital only)**|
|**Dublin Core Mapping**|dc.identifier|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|A numeric string.|
|**Example(s)**|<ul><li>861413</li><li>9978119533406236</li></ul>|

[Jump to Item Level](#item-level)-->

#### ISSN

|CSV Element|issn|
|:---|:---|
|**Description**|International Standard Serial Number: A persistent and unique identifier that serves as an unambiguous reference to the resource to distinguish it from other continuing resources worldwide.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|mods:identifier[@type="issn"]|
|**Dublin Core Mapping**|dc.identifier|
|**Vocabulary/Encoding Scheme(s)**|[International Standard Serial Number (ISSN)](https://www.issn.org/)|
|**Notes**|An 8-digit numeric code, divided by a hyphen into two four-digit numbers.|
|**Example(s)**|0744-7647|

[Jump to Item Level](#item-level)

#### LCCN

|CSV Element|lccn|
|:---|:---|
|**Description**|Library of Congress Control Number: A persistent and unique identifier that serves as an unambiguous reference to the resource to distinguish it from other resources worldwide.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|mods:identifier[@type="lccn"]|
|**Dublin Core Mapping**|dc.identifier|
|**Vocabulary/Encoding Scheme(s)**|[LC (Library of Congress) control numbering system](http://www.loc.gov/marc/lccn_structure.html)|
|**Notes**|A numeric code.|
|**Example(s)**|04014482|

[Jump to Item Level](#item-level)

#### OCLCCN

|CSV Element|oclccn|
|:---|:---|
|**Description**|Online Computer Library Center Control Number: A persistent and unique identifier that serves as an unambiguous reference to the resource to distinguish it from other resources in the WorldCat and other bibliographic contexts.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|<ul><li>mods:identifier[@type="oclc"]</li><li>mods:identifier[@type="local"] when value contains "(OCoLC)"</li></ul>|
|**Dublin Core Mapping**|dc.identifier|
|**Vocabulary/Encoding Scheme(s)**|[OCLC Control Number](https://www.oclc.org/ )|
|**Notes**|<ul><li>A numeric or alph-numeric string.</li><li>For more information, see ["OCLC control number expansion in 2013"](https://www.oclc.org/developer/news/2012/oclc-control-number-expansion-in-2013.en.html).</ul>|
|**Example(s)**|<ul><li>04184089</li><li>(OCoLC)760926034</li></ul>|

[Jump to Item Level](#item-level)

#### URL

|CSV Element|url|
|:---|:---|
|**Description**|A Uniform Resource Location (URL) of the resource; an electronic location from which the resource is available.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:location/mods:url|
|**Dublin Core Mapping**|dc.identifier|
|**Vocabulary/Encoding Scheme(s)**|[Uniform Resource Location (URL)](https://www.w3.org/Addressing/URL/url-spec.html)|
|**Notes**|URL links to proprietary resources include an EZProxy URL to enable access to library e-resources from off campus.|
|**Example(s)**|http://pitt.idm.oclc.org/login?url=http://www.jstor.org/journals/10624783.html|

[Jump to Item Level](#item-level)

#### COLLECTION IDENTIFIER

|CSV Element|collection_id|
|:---|:---|
|**Description**|A digital collection to which the resource belongs.|
|**Required**|Yes|
|**Repeatable**|Yes|
|**Element Node(s)**|rdf:Description/fedora:isMemberOfCollection[@rdf:resource]|
|**Dublin Core Mapping**|dc.relation|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|Alpha-numeric string with special characters, i.e. a colon (:) and a period (.), formatted as follows: pitt:collection_nnn|
|**Example(s)**|pitt:collection.299|

[Jump to Item Level](#item-level)

#### DEPOSITOR

|CSV Element|depositor|
|:---|:---|
|**Description**|An official name of the institution responsible for depositing the resource.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element Node(s)**|mods:name/mods:namePart _with_ mods:role/mods:roleTerm="depositor"|
|**Dublin Core Mapping**|n/a|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|University of Pittsburgh|

[Jump to Item Level](#item-level)
