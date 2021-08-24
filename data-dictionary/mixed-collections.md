---
layout: default
title: Archival Collection Metadata Element Set
parent: Data Dictionary
nav_order: 6
---

#### [Home](http://cadatpitt.github.io)

<html lang="en">
  <head>
    <meta charset="utf-8">

    <!-- Font Awesome Icons css -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

  </head>
</html>

# Mixed Collection Metadata Element Set

## Metadata Element List
Mixed collections are described at the collection-level and the item-level and, thus, have two [2] base layer CSVs, one for each level of description.

### Collection Level
* [Finding Aid Identifier](#finding-aid-identifier)
* [Title of Finding Aid](#title-of-finding-aid)
* [Creator of Finding Aid](#creator-of-finding-aid)
* [Creation Date of Finding Aid](#creation-date-of-finding-aid)
* [Publisher of Finding Aid](#publisher-of-finding-aid)
* [Publication Date of Finding Aid](#publication-date-of-finding-aid)
* [Acquisition Number](#acquisition-number)
* [Title of Collection](#title-of-collection)
* [Creator of Collection](#creator-of-collection)
* [Language of Collection](#language-of-collection)
* [Extent of Collection](#extent-of-collection)
* [Temporal Coverage of Collection](#temporal-coverage-of-collection)
* [Scope and Content of Collection](#scope-and-content-of-collection)
* [Biography or History](#biography-or-history)
* [Collection Abstract](#collection-abstract)
* [Collection Subject Headings](#collection-subject-headings)
* [Related Material](#related-material)
* [Repository](#repository)
* [Preferred Citation](#preferred-citation)
* [Conditions Governing Use](#conditions-governing-use)
* [Collection Identifier](#collection-identifier)

### Item Level
* [Identifier](#identifier)
* [Title](#title)
* [Uniform Title](#uniform-title)
* [Alternative Title](#alternative-title)
* [Enumeration and Chronology](#enumeration-and-chronology) (digital only)
* [Creator](#creator)
* [Contributor](#contributor)
* [Associated Name](#associated-name)
* [Publication Place](#publication-place)
* [Publisher](#publisher)
* [Publication Date](#publication-date)
* [Sort Date](#sort-date)
* [Start Date](#start-date)
* [End Date](#end-date)
* [Encoded Date](#encoded-date)
* [Creation Date](#creation-date)
* [Display Date](#display-date)
* [Copyright Date](#copyright-date)
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
* [Record Identifier](#record-identifier)
* [ISBN](#isbn)
* [ISSN](#issn)
* [LCCN](#lccn)
* [OCLCCN](#oclccn)
* [URL](#url)
* [Host](#host)
* [Series of Collection](#series-of-collection)
* [Container](#container)
* [Owner](#owner)
* [Depositor](#depositor)
* [Collection Identifier](#collection-identifier)

&nbsp;

## Metadata Element Descriptions
Multiple element values are separated by a triple pipe (`|||`) unless stated otherwise.

### Collection Level

#### FINDING AID IDENTIFIER

|CSV Element|finding_aid_id|
|---|---|
|**Description**|A unique identifier that serves as an unambiguous reference to the finding aid in the institutional repository.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|ead:eadheader/ead:eadid|
|**Dublin Core Mapping**|dc.identifier|
|**Vocabulary/Encoding Scheme(s)**|Must be a unique string in the digital repository system.|
|**Notes**|Alpha-numeric or numeric string, with or without special characters like periods (.) or dashes (-).|
|**Example(s)**|US-PPiU-ais200711|

[Jump to Collection Level](#collection-level)

#### TITLE OF FINDING AID

|CSV Element|finding_aid_title|
|---|---|
|**Description**|An official name given to the finding aid.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|ead:eadheader/ead:filedesc/ead:titlestmt/ead:titleproper|
|**Dublin Core Mapping**|dc.title|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|typically includes the Title of Collection and the Temporal Coverage of Collection.|
|**Example(s)**|Guide to the American Left Ephemera Collection, 1875-2015|

[Jump to Collection Level](#collection-level)

#### CREATOR OF FINDING AID

|CSV Element|finding_aid_creator|
|---|---|
|**Description**|A name of an entity primarily responsible for making the content of the finding aid.|
|**Required**|Yes|
|**Repeatable**|Yes|
|**Element(s)**|ead:eadheader/ead:filedesc/ead:titlestmt/ead:titleproper/ead:author|
|**Dublin Core Mapping**|dc.creator|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul><li>Free text. No limitations.</li><li><a href="https://id.loc.gov/authorities/names.html" target="_blank">Library of Congress Name Authority File (LCNAF)</a></li></ul>{:/}|
|**Notes**||
|**Example(s)**|Finding aid prepared by Lindsay Bedford and Patrick Trembeth with assistance provided by Dr. Richard Oestreicher.|

[Jump to Collection Level](#collection-level)

#### CREATION DATE OF FINDING AID

|CSV Element|finding_aid_creation_date|
|---|---|
|**Description**|A date associated with the creation of the finding aid.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|ead:profiledesc/ead:creation/ead:date|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|[ISO 8601: Date and Time Format](https://www.iso.org/iso-8601-date-and-time-format.html)|
|**Notes**|Complete date plus hours, minutes, and time zone: YYYY-MM-DDThh:mm-TZD|
|**Example(s)**|2017-08-29T07:46-0400|

[Jump to Collection Level](#collection-level)

#### PUBLISHER OF FINDING AID

|CSV Element|finding_aid_publisher|
|---|---|
|**Description**|An institution or agency responsible for the distribution of the finding aid.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|ead:eadheader/ead:filedesc/ead:publicationstmt/ead:publisher|
|**Dublin Core Mapping**|dc.publisher|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|ULS Archives &amp; Special Collections|

[Jump to Collection Level](#collection-level)

#### PUBLICATION DATE OF FINDING AID

|CSV Element|finding_aid_publication_date|
|---|---|
|**Description**|A date associated with the publication of the finding aid.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|ead:eadheader/ead:filedesc/ead:publicationstmt/ead:date|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|July 2012|

[Jump to Collection Level](#collection-level)

#### ACQUISITION NUMBER

|CSV Element|acquisition_number|
|---|---|
|**Description**|A unique identifier that serves as an unambiguous reference to the collection in the institutional repository.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:did/ead:unitid|
|**Dublin Core Mapping**|dc.identifier|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|Alpha-numeric or numeric string, with or without special characters like periods (.)|
|**Example(s)**|AIS.2007.11|

[Jump to Collection Level](#collection-level)

#### TITLE OF COLLECTION

|CSV Element|collection_title|
|---|---|
|**Description**|An official name given to the collection.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:did/ead:unittitle|
|**Dublin Core Mapping**|dc.title|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|American Left Ephemera Collection|

[Jump to Collection Level](#collection-level)

#### CREATOR OF COLLECTION

|CSV Element|creator_of_collection|
|---|---|
|**Description**|A name of an entity primarily responsible for the creation, accumulation, or assembly of the collection.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:did/ead:origination|
|**Dublin Core Mapping**|dc.creator|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul><li>Free text. No limitations.</li><li><a href="https://id.loc.gov/authorities/names.html">Library of Congress Name Authority File (LCNAF)</a></li><li><a href="http://id.loc.gov/authorities/subjects.html" target="_blank">Library of Congress Subject Headings (LCSH)</a></li><li><a href="https://www2.archivists.org/groups/technical-subcommittee-on-describing-archives-a-content-standard-dacs/describing-archives-a-content-standard-dacs-second-" target="_blank">Describing Archives: A Content Standard (DACS)</a></li><li><a href="https://www.oclc.org/en/rda/about.html" target="_blank">Resource Description and Access (RDA)</a></li></ul>{:/}|
|**Notes**||
|**Example(s)**|Oestreicher, Richard Jules, 1947-|

[Jump to Collection Level](#collection-level)

#### LANGUAGE OF COLLECTION

|CSV Element|collection_language|
|---|---|
|**Description**|A language in which the materials in the collection are expressed.|
|**Required**|Yes|
|**Repeatable**|Yes|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:did/ead:langmaterial/language[@langcode]|
|**Dublin Core Mapping**|dc.language|
|**Vocabulary/Encoding Scheme(s)**|[ISO 639-2b: Codes for the Representation of Names of Languages](https://www.loc.gov/standards/iso639-2/)|
|**Notes**||
|**Example(s)**|eng|

[Jump to Collection Level](#collection-level)

#### EXTENT OF COLLECTION

|CSV Element|collection_extent|
|---|---|
|**Description**|A statement about the quantity of the materials in the collection or of the physical space they occupy.|
|**Required**|Yes|
|**Repeatable**|Yes|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:did/ead:physdesc/ead:extent|
|**Dublin Core Mapping**|dc.extent|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>22.75 linear feet</li><li>(37 boxes)</a></li></ul>{:/}|

[Jump to Collection Level](#collection-level)

#### TEMPORAL COVERAGE OF COLLECTION

|CSV Element|collection_temporal_coverage|
|---|---|
|**Description**|A statement of the date(s) covered by the materials in the collection.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:did/ead:unitdate|
|**Dublin Core Mapping**|dc.coverage|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|1875-2015|

[Jump to Collection Level](#collection-level)

#### SCOPE AND CONTENT OF COLLECTION

|CSV Element|collection_scope_and_content|
|---|---|
|**Description**|A narrative statement that summarizes the range and topical coverage of the materials in the collection.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:scopecontent/p|
|**Dublin Core Mapping**|dc.description|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|The collection includes items from the 1870s to the present including periodicals, photographs, letters, pamphlets, books, posters, flyers, labels, pins and other objects, but it emphasizes ephemeral items (e.g., items made for one time or brief usage and then likely to be discarded). While the majority of these items were produced by the Socialist Party USA (SPUSA), Communist Party USA (CPUSA), Students for a Democratic Society (SDS), or organizations linked to them, the collection also includes material from a wide variety of other organizations and movements as well as from unaffiliated activists and radical intellectuals. <br><br>Dr. Richard Oestreicher wrote all of the scope and content notes within the collection as well as writing the History section.|

[Jump to Collection Level](#collection-level)

#### BIOGRAPHY OR HISTORY

|CSV Element|biography_or_history|
|---|---|
|**Description**|A concise essay or chronology that places the materials of the collection in context by providing information about their creator(s).|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:bioghist/p|
|**Dublin Core Mapping**|dc.description|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|Left and Right as political designations date to the French Revolution when the Jacobins sat on the left in the National Assembly and the Girondins on the right. The Left has come to mean movements, organizations, and intellectual or cultural tendencies that emphasize an egalitarian ethos, a utopian vision of social reconstruction, and a commitment to agitation and action to advance that ethos and vision.|

[Jump to Collection Level](#collection-level)

#### COLLECTION ABSTRACT

|CSV Element|collection_abstract|
|---|---|
|**Description**|A brief characterization of the materials in the collection.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:did/ead:abstract|
|**Dublin Core Mapping**|dc.description|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|Dr. Richard Oestreicher, Associate Professor of History at the University of Pittsburgh, amassed the American Left Ephemera Collection over a 35-year period to document the history of the American Left from the 1870s to the present. Digital reproductions of the collection are available online.|

[Jump to Collection Level](#collection-level)

#### COLLECTION SUBJECT HEADINGS

|CSV Element|subject_headings|
|---|---|
|**Description**|A term or phrase representing the primary topic(s) of the materials in the collection.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:controlaccess|
|**Dublin Core Mapping**|dc.subject|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul><li><a href="http://id.loc.gov/authorities/names.html" target="_blank">Library of Congress Name Authority File (LCNAF)</a></li><li><a href="https://www.getty.edu/research/tools/vocabularies/aat/" target="_blank">Art & Architecture Thesaurus (AAT)</a></li><li><a href="https://www.oclc.org/research/themes/data-science/fast/download.html" target="_blank">Faceted Application of Subject Terminology (FAST)</a></li><li><a href="https://www.loc.gov/aba/cyac/childsubjhead.html" target="_blank">Children's Subject Headings (CSH)</a></li><li><a href="http://id.loc.gov/authorities/childrensSubjects.html" target="_blank">Library of Congress Subject Headings Supplemental Vocabularies: Children’s Headings (LCSHAC)</a></li><li><a href="https://www.nlm.nih.gov/mesh/meshhome.html" target="_blank">Medical Subject Headings (MeSH)</a></li><li><a href="https://agclass.nal.usda.gov/" target="_blank">National Agricultural Library</a></li><li><a href="https://rvmweb.bibl.ulaval.ca/eccueil" target="_blank">Répertoire de vedettes-matière (RVM)</a></li><li><a href="https://www.iso.org/iso-8601-date-and-time-format.html" target="_blank">ISO 8601: Date and Time Format</a></li><li><a href="https://www.loc.gov/marc/geoareas/" target="_blank">MARC Code List for Geographic Areas</a></li><li><a href="https://www.loc.gov/marc/countries/countries_code.html" target="_blank">MARC Code List for Countries</a></li><li><a href="https://www.iso.org/iso-3166-country-codes.html" target="_blank">ISO 3166 — Country Codes</a></li></ul>{:/}|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>Communist Party of the United States of America. -- History -- Sources</li><li>Buttons (Information artifacts</a></li><li>Christian socialism -- United States -- History -- Sources</li><li>Pamphlets</li><li>Politics</li><li>Vietnam War, 1961-1975</li></ul>{:/}|

[Jump to Collection Level](#collection-level)

#### RELATED MATERIAL

|CSV Element|related_material|
|---|---|
|**Description**|Archival materials that have an association to the materials in the collection; often another collection.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:relatedmaterial|
|**Dublin Core Mapping**|dc.relation|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|Often the Preferred Citation for related collection, including collection title, date range for collection, Acquition Number, Repository, and Depositor.|
|**Example(s)**|A.E. Forbes Communist Collection, 1921-1972, AIS.2000.07, Archives &amp; Special Collections, University of Pittsburgh Library System|

[Jump to Collection Level](#collection-level)

#### REPOSITORY

|CSV Element|repository|
|---|---|
|**Description**|An institution, person, or family responsible for providing intellectual access to the materials in the collection.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:did/ead:repository|
|**Dublin Core Mapping**|n/a|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|ULS Archives &amp; Special Collections|

[Jump to Collection Level](#collection-level)

#### PREFERRED CITATION

|CSV Element|preferred_citation|
|---|---|
|**Description**|A prescribed wording or format for citing (the materials in) the collection.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:prefercite/p|
|**Dublin Core Mapping**|n/a|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|Typically includes Title of Collection, Temporal Coverage, Repository, and Depositor.|
|**Example(s)**|American Left Ephemera Collection, 1875-2015, AIS.2007.11, Archives &amp; Special Collections, University of Pittsburgh Library System|

[Jump to Collection Level](#collection-level)

#### CONDITIONS GOVERNING USE

|CSV Element|conditions_governing_use|
|---|---|
|**Description**|Any conditions that affect the use of the materials in the collection.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:userestrict/p|
|**Dublin Core Mapping**|dc.rights|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|The University of Pittsburgh holds the property rights to the material in this collection, but the copyright may still be held by the original creator/author. Researchers are therefore advised to follow the regulations set forth in the U.S. Copyright Code when publishing, quoting, or reproducing material from this collection without the consent of the creator/author or that go beyond what is allowed by fair use.|

[Jump to Collection Level](#collection-level)

#### COLLECTION IDENTIFIER

|CSV Element|collection_id|
|---|---|
|**Description**|A digital collection to which the resource belongs.|
|**Required**|Yes|
|**Repeatable**|Yes|
|**Element(s)**|rdf:Description/fedora:isMemberOfCollection[@rdf:resource]|
|**Dublin Core Mapping**|dc.relation|
|**Vocabulary/Encoding Scheme(s)**||
|**Notes**|Alpha-numeric string with special characters, i.e. a colon (:) and a period (.), formatted as follows: pitt:collection_nnn|
|**Example(s)**|pitt:collection.299|

[Jump to Collection Level](#collection-level) &nbsp;\|&nbsp; [Jump to Item Level](#item-level)

&nbsp;

### Item Level

#### IDENTIFIER

|CSV Element|id|
|---|---|
|**Description**|A unique identifier that serves as an unambiguous reference to the resource in the institutional repository.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|mods:identifier[@type="pitt"]|
|**Dublin Core Mapping**|dc.identifier|
|**Vocabulary/Encoding Scheme(s)**|Must be a unique string in the digital repository system.|
|**Notes**|Alpha-numeric or numeric string, with or without special characters like periods (.) or dashes (-)|
|**Example(s)**|{::nomarkdown}<ul><li>31735070074590</li><li>ue13.1.0611a</li><li>000010.PI</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### TITLE

|CSV Element|title|
|---|---|
|**Description**|A name given to the resource.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|mods:titleInfo{::nomarkdown}<ul><li>mods:title</li><li>mods:subTitle</li><li>mods:nonSort</li></ul>{:/}|
|**Dublin Core Mapping**|dc.title|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|{::nomarkdown}<ul><li>Title is formatted as follows (less the subTitle and/or nonSort where they do not exist): [title]: [subTitle], [nonSort]</li><li>Excludes any Title elements (i.e., mods:titleInfo) with the following @type attribute values: abbreviated, translated, alternative, uniform.</li></ul>{:/}|
|**Example(s)**|{::nomarkdown}<ul><li>Zhou zong li-Ruisidun hui tan quan wen</li><li>Tip top weekly</li><li>Allegheny County Soldiers and Sailors Memorial</li></ul>{:/}|

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
|**Example(s)**|{::nomarkdown}<ul><li>Courier (Pittsburgh, Pa. : City edition</a></li><li>Shooting star review</li></ul>{:/}|

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
|**Example(s)**|{::nomarkdown}<ul><li>CriSTaL</li><li>Shooting star</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### ENUMERATION AND CHRONOLOGY

|CSV Element|enumeration_chronology|
|---|---|
|**Description**|A numeric and/or alphabetic designation used to identify the resource and its sequential and/or chronological relationship to a serial, of which it is a part, as a whole.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|mods:titleInfo/partNumber|
|**Dublin Core Mapping**|dc.title|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.niso.org/publications/z3971-2006-r2011" target="_blank">ANSI/NISO Z39.71-2006 (R2011) Holdings Statements for Bibliographic Items</a></li><li>NISO Z39.44 Serial Holdings Standard (superseded by ANSI/NISO Z39.71-2006)</a></li><li>Free text. No limitations.</li></ul>{:/}|
|**Notes**||
|**Example(s)**|vol. 12, no. 8|

[Jump to Item Level](#item-level)


#### CREATOR

|CSV Element|creator|
|---|---|
|**Description**|A name of an entity responsible for making the content of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|{::nomarkdown}<ul><li>mods:name/mods:namePart <em>with</em> mods:role/mods:roleTerm="creator"</li><li>mods:name/mods:namePart[@usage="primary"] <em>without</em> mods:role/mods:roleTerm</li></ul>{:/}|
|**Dublin Core Mapping**|dc.creator|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul><li>Free text. No Limitations.</li><li><a href="https://id.loc.gov/authorities/names.html" target="_blank">Library of Congress Name Authority File (LCNAF)</a></li><li><a href="http://id.loc.gov/vocabulary/relators.htm" target="_blank">MARC Relators</a></li></ul>{:/}|
|**Notes**|Multiple values within the <mods:name> element are separated by comma (,).|
|**Example(s)**|Stockton, Frank R., 1834-1902|

[Jump to Item Level](#item-level)

#### CONTRIBUTOR

|CSV Element|contributor|
|---|---|
|**Description**|A name of an entity responsible for making contributions to the creation or distribution of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|{::nomarkdown}<ul><li>mods:name/mods:namePart <em>with</em> mods:role/mods:roleTerm="contributor"</li><li>mods:name/mods:namePart[not(@usage="primary")] <em>without</em> mods:role/mods:roleTerm</li></ul>{:/}|
|**Dublin Core Mapping**|dc.contributor|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul><li>Free text. No Limitations.</li><li><a href="https://id.loc.gov/authorities/names.html" target="_blank">Library of Congress Name Authority File (LCNAF)</a></li><li><a href="http://id.loc.gov/vocabulary/relators.htm" target="_blank">MARC Relators</a></li></ul>{:/}|
|**Notes**|Multiple values within the <mods:name> element are separated by comma (,).|
|**Example(s)**|Abbot Renaud de Semur|

[Jump to Item Level](#item-level)

#### ASSOCIATED NAME

|CSV Element|associated_name|
|---|---|
|**Description**|A name of an entity associated in some way with the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:name/mods:namePart _with_ mods:role/mods:roleterm{::nomarkdown}<ul><li>Exception for possible @roleTerm attribute values: depositor</li></ul>{:/}|
|**Dublin Core Mapping**|{::nomarkdown}<ul><li>dc.creator</li><li>dc.contributor</li></ul>{:/}|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul><li>Free text. No limitations.</li><li><a href="https://id.loc.gov/authorities/names.html" target="_blank">Library of Congress Name Authority File (LCNAF)</a></li></ul>{:/}|
|**Notes**|Multiple values within the <mods:name> element are separated by comma (,).|
|**Example(s)**|{::nomarkdown}<ul><li>International Union of Mine, Mill, and Smelter Workers</li><li>Meinhof, Carl, 1857-1944</li></ul>{:/}|

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
|**Example(s)**|{::nomarkdown}<ul><li>Berlin [etc.]</li><li>Minneapolis and St. Paul</li><li>Petersburg, VA</li><li>New Delhi]</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### PUBLISHER

|CSV Element|publisher|
|---|---|
|**Description**|A name of an entity that published, printed, distributed, released, issued, or produced the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|{::nomarkdown}<ul><li>mods:originInfo/mods:publisher</li><li>mods:name/namePart <em>with</em> mods:role/mods:roleTerm="publisher"</li></ul>{:/}|
|**Dublin Core Mapping**|dc.publisher|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul><li>Free text. No Limitations.</li><li><a href="http://id.loc.gov/authorities/names.html" target="_blank">Library of Congress Name Authority File (LCNAF)</a></li></ul>{:/}|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>Afro-Hispanic Institute</li><li>Sandra Gould Ford</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### PUBLICATION DATE

|CSV Element|publication_date|
|---|---|
|**Description**|A date associated with the publication or issuance of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|{::nomarkdown}<ul><li>mods:originInfo/mods:dateIssued</li><li>mods:originInfo/mods:dateOther[@type="sort"] <strong>(digital only)</strong></li></ul>{:/}|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|
|**Notes**|For more information, see [MARC 21 Format for Bibliographic Data  — 260 - Publication, Distribution, etc.](https://www.loc.gov/marc/bibliographic/bd260.html).|
|**Example(s)**|{::nomarkdown}<ul><li>1994]-</li><li>2011-</li><li>1940-02-01T00:00:00 <strong>(digital only)</strong></li></ul>{:/}|

[Jump to Item Level](#item-level)

#### SORT DATE

|CSV Element|sort_date|
|---|---|
|**Description**|A date associated with the creation of the resource and encoded for sorting or other purposes that necessitate normalization.|
|**Required**|No|
|**Repeatable**|No|
|**Element(s)**|mods:originInfo/mods:dateOther[@type="sort"]|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|[ISO 8601: Date and Time Format](https://www.iso.org/iso-8601-date-and-time-format.html)|
|**Notes**|Complete date plus hours and minutes: YYYY-MM-DDThh:mm:ss|
|**Example(s)**|1872-01-01T00:00:00|

[Jump to Item Level](#item-level)

#### START DATE

|CSV Element|start_date|
|---|---|
|**Description**|A date associated with the beginning of publication of the resource or the serial of which it is a part.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|{::nomarkdown}<ul><li>mods:originInfo/mods:dateIssued[@point="start"]</li><li>mods:originInfo/mods:dateCreated[@point="start"] <strong>(digital only)</strong></li></ul>{:/}|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|For more information, see [MARC 21 Format for Bibliographic Data  — 008 - All Materials (NR)](https://www.loc.gov/marc/bibliographic/bd008a.html).|
|**Example(s)**|{::nomarkdown}<ul><li>19uu</li><li>1965</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### END DATE

|CSV Element|end_date|
|---|---|
|**Description**|A date associated with the end of publication of the resource or the continuing resource (e.g., serial) of which it is a part.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|{::nomarkdown}<ul><li>mods:originInfo/mods:dateIssued[@point="end"]</li><li>mods:originInfo/mods:dateCreated[@point="end"]</li></ul>{:/}|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>1992</li><li>9999</li><li>uuuu</li></ul>{:/}|

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
|**Repeatable**|No|
|**Element(s)**|mods:originInfo/mods:dateCreated|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**||
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>1872</li><li>1972-2010</li><li>1940/1950</li><li>184u/uuuu</li><li>1962-01-29</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### DISPLAY DATE

|CSV Element|display_date|
|---|---|
|**Description**|A date associated with the creation of the resource and formatted for display.|
|**Required**|No|
|**Repeatable**|No|
|**Element(s)**|mods:originInfo/mods:dateOther[@type="display"]|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>November 23, 2004</li><li>1977</li><li>ca. 1950-1960</li><li>Undated</li><li>Post-marked October 31, 1888</li><li>Likely during 80's</li><li>[189?]</li><li>February 9</li></ul>{:/}|

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

#### FREQUENCY

|CSV Element|frequency|
|---|---|
|**Description**|A statement of publication frequency or pattern of the resource or the serial of which it is a part.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:originInfo/mods:frequency|
|**Dublin Core Mapping**|n/a|
|**Vocabulary/Encoding Scheme(s)**|[MARC 21 Frequency of Issue Term List](https://www.loc.gov/standards/valuelist/marcfrequency.html)|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>Weekly</li><li>Unknown</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### LANGUAGE

|CSV Element|language|
|---|---|
|**Description**|A language in which the content of the resource is expressed.|
|**Required**|Yes|
|**Repeatable**|Yes|
|**Element(s)**|mods:language/mods:languageTerm|
|**Dublin Core Mapping**|dc.language|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/standards/iso639-2/php/code_list.php" target="_blank">ISO 639-2: Codes for the Representation of Names of Languages</a></li><li><a href="http://www.loc.gov/marc/languages/" target="_blank">MARC Code List for Language</a></li></ul>{:/}|
|**Notes**||
|**Example(s)**|eng|

[Jump to Item Level](#item-level)

#### TYPE OF RESOURCE

|CSV Element|type_of_resource|
|---|---|
|**Description**|A term that specifies the characteristics and general type of content of the resource.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|mods:typeOfResource|
|**Dublin Core Mapping**|dc.type|
|**Vocabulary/Encoding Scheme(s)**|**Restricted scheme data values for typeOfResource element**: text, cartographic, notated music, sound recording, sound recording - nonmusical, sound recording - musical, still image, moving image, kit three dimensional object, software, multimedia, mixed material|
|**Notes**|For more information, see [MARC 21 Format for Bibliographic Data — Leader](http://www.loc.gov/marc/bibliographic/bdleader.html).|
|**Example(s)**|text|

[Jump to Item Level](#item-level)

#### FORMAT

|CSV Element|format|
|---|---|
|**Description**|A designation of a particular physical presentation of a resource, including the physical form or medium of material for a resource.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|mods:physicalDescription/mods:form|
|**Dublin Core Mapping**|dc.format|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/standards/valuelist/marccategory.html" target="_blank">MARC Form Category Term List</a></li><li><a href="https://www.loc.gov/standards/valuelist/marcform.html" target="_blank">MARC Form of Item Term List</a></li><li><a href="https://www.loc.gov/standards/valuelist/marcsmd.html<" target="_blank">Specific Material Form Term List</a></li><li>General Material Designation (GMD)</a></li><li>Free text. No limitations.</li></ul>{:/}|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>print</il><li>gelatin silver prints</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### EXTENT

|CSV Element|extent|
|---|---|
|**Description**|A statement about the physical extent of the resource, in terms of units of measurement and material.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|mods:physicalDescription/mods:extent|
|**Dublin Core Mapping**|dc.format|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|For more information, see [MARC 21 Format for Bibliographic Data  — 300 - Physical Description](http://www.loc.gov/marc/bibliographic/bd300.html).|
|**Example(s)**|2 volumes (378 pages) ; 29 cm|

[Jump to Item Level](#item-level)

#### GENRE

|CSV Element|genre|
|---|---|
|**Description**|A term that designates a category characterizing a particular style, form, or content embodied by the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|{::nomarkdown}<ul><li>mods:genre</li><li>mods:subject/mods:genre</li></ul>{:/}|
|**Dublin Core Mapping**|dc.type|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/standards/valuelist/marcgt.html" target="_blank">MARC Genre Term List</a></li><li><a href="https://www.getty.edu/research/tools/vocabularies/aat/" target="_blank">Art & Architecture Thesaurus (AAT)</a></li><li><a href="https://www.oclc.org/research/themes/data-science/fast/download.html" target="_blank">Faceted Application of Subject Terminology (FAST)</a></li><li><a href="https://www.loc.gov/standards/valuelist/marcmuscomp.html" target="_blank">MARC Form of Musical Composition Code List</a></li><li><a href="https://www.loc.gov/rr/print/tgm2/" target="_blank">Library of Congress Genre/Form Terms</a></li><li><a href="https://rbms.info/vocabularies/genre/alphabetical_list.htm" target="_blank">RBMS Controlled Vocabularies: Genre Terms</a></li><li><a href="https://www.loc.gov/rr/print/tgm2/" target="_blank">Thesaurus for graphic materials (TGM II, Genre and physical characteristic terms)</a></li><li><a href="https://rbms.info/vocabularies/provenance/alphabetical_list.htm" target="_blank">RBMS Controlled Vocabularies: Provenance Evidence Terms</a></li><li><a href="http://experimental.worldcat.org/gsafd/" target="_blank">Guidelines on Subject Access to Individual Works of Fiction, Drama, Etc., 2nd edition</a></li><li><a href="https://www.loc.gov/standards/valuelist/rdacontent.html" target="_blank">Term and Code List for RDA Content Types</a></li><li><a href="http://id.loc.gov/vocabulary/genreFormSchemes/ftamc.html" target="_blank">Form terms for archival and manuscripts control</a></li></ul>{:/}|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>text</li><li>novel</li><li>Embossed cloth binding (Binding)-1851</li><li>Fiction.</li><li>archival document</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### ABSTRACT

|CSV Element|abstract|
|---|---|
|**Description**|A summary of the content of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|mods:abstract|
|**Dublin Core Mapping**|dc.description|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>Tom and Mary delight in their baby brother Charlie, while Tom befriends a boy from Georgia.</li><li>92 verso</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### SUBJECT

|CSV Element|subject|
|---|---|
|**Description**|A term or phrase representing the primary topic(s) on which the resource is focused.|
|**Required**|No
|**Repeatable**|Yes|
|**Element(s)**|mods:subject{::nomarkdown}<ul><li>mods:topic</li><li>mods:name</li><li>mods:titleInfo</li><li>mods:occupation</li></ul>{:/}|
|**Dublin Core Mapping**|dc.subject|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="http://id.loc.gov/authorities/names.html" target="_blank">Library of Congress Name Authority File (LCNAF)</a></li><li><a href="https://www.oclc.org/research/themes/data-science/fast/download.html" target="_blank">Faceted Application of Subject Terminology (FAST)</a></li><li><a href="https://www.loc.gov/aba/cyac/childsubjhead.html" target="_blank">Children's Subject Headings (CSH)</a></li><li><a href="http://id.loc.gov/authorities/childrensSubjects.html" target="_blank">Library of Congress Subject Headings Supplemental Vocabularies: Children’s Headings (LCSHAC)</a></li><li><a href="https://www.nlm.nih.gov/mesh/meshhome.html" target="_blank">Medical Subject Headings (MeSH)</a></li><li><a href="https://agclass.nal.usda.gov/" target="_blank">National Agricultural Library</a></li><li><a href="https://rvmweb.bibl.ulaval.ca/eccueil" target="_blank">Répertoire de vedettes-matière (RVM)</a></li></ul>{:/}|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>Advertising</li><li>Pittsburgh</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### TEMPORAL COVERAGE

|CSV Element|temporal_coverage|
|---|---|
|**Description**|A chronological statement that indicates the date(s) or time period covered by the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|mods:subject/mods:temporal|
|**Dublin Core Mapping**|dc.coverage|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul><li>Free text. No limitations.</li><li><a href="https://www.iso.org/iso-8601-date-and-time-format.html" target="_blank">ISO 8601: Date and Time Format</a></li></ul>{:/}|
|**Notes**|May be a simple or hierarchical geographical name or area code (e.g., city section, city, county, territory, state, region, country, continent, island, area, extraterrestrial area), cartographic data (e.g., coordinates, scale, projection)|
|**Example(s)**|{::nomarkdown}<ul><li>19th century</li><li>1775-1783</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### GEOGRAPHIC COVERAGE

|CSV Element|geographic_coverage|
|---|---|
|**Description**|A geographical name or geographical data that indicates the spatial coverage of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|mods:subject{::nomarkdown}<ul><li>mods:geographic</li><li>mods:geographicCode</li><li>mods:hierarchicalGeographic</li><ul><li>mods:continent</li><li>mods:country</li><li>mods:region</li><li>mods:state</li><li>mods:territory</li><li>mods:county</li><li>mods:city</li><li>mods:island</li><li>mods:area</li><li>mods:extraterrestrialArea</li><li>mods:citySection</li></ul><li>mods:cartographics</li><ul><li>mods:scale</li><li>mods:projection</li><li>mods:coordinates</li></ul><li>mods:geographicCoordinates</li></ul>{:/}|
|**Dublin Core Mapping**|dc.coverage|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/marc/geoareas/" target="_blank">MARC Code List for Geographic Areas</a></li><li><a href="https://www.loc.gov/marc/countries/countries_code.html" target="_blank">MARC Code List for Countries</a></li><li><a href="https://www.iso.org/iso-3166-country-codes.html" target="_blank">ISO 3166 — Country Codes</a></li><li>Free text. No limitations.</li></ul>{:/}|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>Downtown</li><li>n------</li><li>North America</li></ul>{:/}|

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

#### PREECEDED BY

|CSV Element|preceeded_by|
|---|---|
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
|---|---|
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
|---|---|
|**Description**|An indication of the copyright status for the resource.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|mods:accessCondition/copyrightMD:copyright[@copyright.status]|
|**Dublin Core Mapping**|dc.rights|
|**Vocabulary/Encoding Scheme(s)**|**Restricted scheme data values for typeOfResource element**:&nbsp;{::nomarkdown}<ul><li>copyrighted — Under copyright.</li><li>pd — Public domain: No further information.</li><li>pd_usfed — Public domain: US Federal document.</li><li>pd_holder — Public domain: Item dedicated to the public domain by the rights holder.</li><li>pd_expired — Public domain: Item in the public domain because of expiration of copyright based on U.S. law.</li><li>unknown — Copyright status of the resource is unknown.</li></ul>{:/}|
|**Notes**||
|**Example(s)**|copyrighted|

[Jump to Item Level](#item-level)

#### COPYRIGHT HOLDER

|CSV Element|copyright_holder|
|---|---|
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
|---|---|
|**Description**|A general note relating to one of the following aspects of the resource: its creator(s), its publication, its rights holder(s), or services available pertaining to it.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element Node(s)**|mods:accessCondition/copyrightMD:copyright/copyrightMD:note|
|**Dublin Core Mapping**|dc.rights|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|Permission granted by owner/publisher|

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
|**Example(s)**|{::nomarkdown}<ul><li>9939005533406236</li><li>3900553</li></ul>{:/}|

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

#### ISSN

|CSV Element|issn|
|---|---|
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
|---|---|
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
|---|---|
|**Description**|Online Computer Library Center Control Number: A persistent and unique identifier that serves as an unambiguous reference to the resource to distinguish it from other resources in the WorldCat and other bibliographic contexts.|
|**Required**|No|
|**Repeatable**|No|
|**Element Node(s)**|{::nomarkdown}<ul><li>mods:identifier[@type="oclc"]</li><li>mods:identifier[@type="local"] when value contains "(OCoLC)"</li></ul>{:/}|
|**Dublin Core Mapping**|dc.identifier|
|**Vocabulary/Encoding Scheme(s)**|[OCLC Control Number](https://www.oclc.org/ )|
|**Notes**|{::nomarkdown}<ul><li>A numeric or alph-numeric string.</li><li>For more information, see <a href="https://www.oclc.org/developer/news/2012/oclc-control-number-expansion-in-2013.en.html" target="_blank">"OCLC control number expansion in 2013"</a>.</ul>{:/}|
|**Example(s)**|{::nomarkdown}<ul><li>04184089</li><li>(OCoLC)760926034</li></ul>{:/}|

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
|**Example(s)**|http://pitt.idm.oclc.org/login?url=http://www.jstor.org/journals/10624783.html|

[Jump to Item Level](#item-level)

#### HOST

|CSV Element|host|
|---|---|
|**Description**|A host or parent resource for the collection described; typically the parent collection.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|mods:relatedItem[@type="host"]/mods:titleInfo/mods:title|
|**Dublin Core Mapping**|dc.relation|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|Arlen Specter Senatorial Papers, Group 6. Public Relations and Media Files|

[Jump to Item Level](#item-level)


#### SERIES OF COLLECTION

|CSV Element|series_of_collection|
|---|---|
|**Description**|A series of the parent collection to which the resource belongs.|
|**Required**|No|
|**Repeatable**|No|
|**Element(s)**|{::nomarkdown}<ul><li>mods:note[@type="series"]</li><li>mods:note[@type="subseries"]</li></ul>{:/}|
|**Dublin Core Mapping**|dc.relation|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|Multiple values are separated by a semicolon (;), from broadest to narrowest series level.|
|**Example(s)**|IV. Press Office, 1981-2005; 1. Press Releases 1981-2005|

[Jump to Item Level](#item-level)

#### CONTAINER

|CSV Element|container|
|---|---|
|**Description**|An indication of the kind of container that physically holds the resource and any sequential number(s) assigned to the container.|
|**Required**|No|
|**Repeatable**|No|
|**Element(s)**|mods:relatedItem[@type="host"]/mods:note[@type="container"]|
|**Dublin Core Mapping**|n/a|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|Value may include one or more of the following: box, folder, shelf, drawer, reel, etc.|
|**Example(s)**|{::nomarkdown}<ul><li>Box 14, Folder 32</li><li>Microfilm-cabinet Drawer 2 3, Reel 1</li><li>Reel 8</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### OWNER

|CSV Element|owner|
|---|---|
|**Description**|A name of an entity that possesses physical and/or intellectual ownership of the resource.|
|**Required**|No|
|**Repeatable**|No|
|**Element(s)**|mods:relatedItem[@type="host"]/mods:note[@type="ownership"]|
|**Dublin Core Mapping**|n/a|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|ULS Archives &amp; Special Collections|

[Jump to Item Level](#item-level)


#### DEPOSITOR

|CSV Element|depositor|
|---|---|
|**Description**|An official name of the institution responsible for depositing the resource.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|mods:name/mods:namePart _with_ mods:role/mods:roleTerm="depositor"|
|**Dublin Core Mapping**|n/a|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>University of Pittsburgh</li><li>African American Chamber of Commerce of Western Pennsylvania</li><li>Rodef Shalom Congregation</li></ul>{:/}|

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
|**Example(s)**|pitt:collection.299|

[Jump to Item Level](#item-level)
