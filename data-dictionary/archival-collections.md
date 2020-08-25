---
layout: default
title: Archival Collection Metadata Element Set
parent: Data Dictionary
nav_order: 3
---

<html lang="en">
  <head>
    <meta charset="utf-8">

    <!-- Font Awesome Icons css -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

  </head>
</html>

# Archival Collection Metadata Element Set

## Metadata Element List
Archival collections are described at the collection-level and the item-level and, thus, have two [2] base layer CSVs, one for each level of description.

### **Collection Level**
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

### **Item Level**
* [Identifier](#identifier)
* [Title](#title)
* [Creator](#creator)
* [Contributor](#contributor)
* [Creation Date](#creation-date)
* [Sort Date](#sort-date)
* [Display Date](#display-date)
* [Language](#language)
* [Type of Resource](#type-of-resource)
* [Format](#format)
* [Extent](#extent)
* [Genre](#genre)
* [Abstract](#abstract)
* [Subject](#subject)
* [Temporal Coverage](#temporal-coverage)
* [Geographic Coverage](#geographic-coverage)
* [Collection Identifier](#collection-identifier)
* [Host](#host)
* [Series of Collection](#series-of-collection)
* [Container](#container)
* [Owner](#owner)
* [Depositor](#depositor)

&nbsp;

## Metadata Element Descriptions
**Note**: Multiple element values are separated by a triple pipe (`|||`) unless stated otherwise.

### Collection Level

#### FINDING AID IDENTIFIER

|CSV Element|finding_aid_id|
|:---|:---|
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
|:---|:---|
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
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul><li>Free text. No limitations.</li></li><li><a href="https://id.loc.gov/authorities/names.html" target="_blank">Library of Congress Name Authority File (LCNAF</a></li></ul>{:/}|
|**Notes**||
|**Example(s)**|Finding aid prepared by Lindsay Bedford and Patrick Trembeth with assistance provided by Dr. Richard Oestreicher.|

[Jump to Collection Level](#collection-level)

#### CREATION DATE OF FINDING AID

|CSV Element|finding_aid_creation_date|
|:---|:---|
|**Description**|A date associated with the creation of the finding aid.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|ead:profiledesc/ead:creation/ead:date|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|[ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html)|
|**Notes**|Complete date plus hours, minutes, and time zone: YYYY-MM-DDThh:mm-TZD|
|**Example(s)**|2017-08-29T07:46-0400|

[Jump to Collection Level](#collection-level)

#### PUBLISHER OF FINDING AID

|CSV Element|finding_aid_publisher|
|:---|:---|
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
|:---|:---|
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
|:---|:---|
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
|:---|:---|
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
|:---|:---|
|**Description**|A name of an entity primarily responsible for the creation, accumulation, or assembly of the collection.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:did/ead:origination|
|**Dublin Core Mapping**|dc.creator|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul><li>Free text. No limitations.</li><li><a href="https://id.loc.gov/authorities/names.html">Library of Congress Name Authority File (LCNAF)</a></li></li><li><a href="http://id.loc.gov/authorities/subjects.html" target="_blank">Library of Congress Subject Headings (LCSH</a></li><li>Anglo-American Cataloguing Rules (AACR)</a></li></li><li><a href="https://www2.archivists.org/groups/technical-subcommittee-on-describing-archives-a-content-standard-dacs/describing-archives-a-content-standard-dacs-second-" target="_blank">Describing Archives: A Content Standard (DACS)</a></li></li><li><a href="https://www.oclc.org/en/rda/about.html" target="_blank">Resource Description and Access (RDA)</a></li></ul>{:/}|
|**Notes**||
|**Example(s)**|Oestreicher, Richard Jules, 1947-|

[Jump to Collection Level](#collection-level)

#### LANGUAGE OF COLLECTION

|CSV Element|collection_language|
|:---|:---|
|**Description**|A language in which the materials in the collection is expressed.|
|**Required**|Yes|
|**Repeatable**|Yes|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:did/ead:langmaterial/language[@langcode]|
|**Dublin Core Mapping**|dc.language|
|**Vocabulary/Encoding Scheme(s)**|[ISO 639-2b](https://www.loc.gov/standards/iso639-2/php/code_list.php)|
|**Notes**||
|**Example(s)**|eng|

[Jump to Collection Level](#collection-level)

#### EXTENT OF COLLECTION

|CSV Element|collection_extent|
|:---|:---|
|**Description**|A statement about the quantity of the materials in the collection or of the physical space they occupy.|
|**Required**|Yes|
|**Repeatable**|Yes|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:did/ead:physdesc/ead:extent|
|**Dublin Core Mapping**|dc.extent|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>22.75 linear feet</li><li>(37 boxes</a></li></ul>{:/}|

[Jump to Collection Level](#collection-level)

#### TEMPORAL COVERAGE OF COLLECTION

|CSV Element|collection_temporal_coverage|
|:---|:---|
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
|:---|:---|
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
|:---|:---|
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
|:---|:---|
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
|:---|:---|
|**Description**|A term or phrase representing the primary topic(s) of the materials in the collection.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:controlaccess|
|**Dublin Core Mapping**|dc.subject|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="http://id.loc.gov/authorities/names.html" target="_blank">Library of Congress Name Authority File (LCNAF)</a></li></li><li><a href="https://www.getty.edu/research/tools/vocabularies/aat/" target="_blank">Art & Architecture Thesaurus (AAT)</a></li></li><li><a href="https://www.oclc.org/research/themes/data-science/fast/download.html" target="_blank">Faceted Application of Subject Terminology (FAST)</a></li></li><li><a href="https://www.loc.gov/aba/cyac/childsubjhead.html" target="_blank">Children's Subject Headings (CSH)</a></li></li><li><a href="http://id.loc.gov/authorities/childrensSubjects.html" target="_blank">Library of Congress Subject Headings Supplemental Vocabularies: Children’s Headings (LCSHAC)</a></li></li><li><a href="https://www.nlm.nih.gov/mesh/meshhome.html" target="_blank">Medical Subject Headings (MeSH)</a></li></li><li><a href="" target="_blank">National Agricultural Library](https://agclass.nal.usda.gov/</a></li></li><li><a href="https://rvmweb.bibl.ulaval.ca/eccueil" target="_blank">Répertoire de vedettes-matière (RVM)</a></li></li><li><a href="https://www.iso.org/iso-8601-date-and-time-format.html" target="_blank">ISO 8601 — Date and Time Format</a></li></li><li><a href="" target="_blank">MARC Code List for Geographic Areas](https://www.loc.gov/marc/geoareas/</a></li></li><li><a href="https://www.loc.gov/marc/countries/countries_code.html" target="_blank">MARC Code List for Countries</a></li></li><li><a href="https://www.iso.org/iso-3166-country-codes.html" target="_blank">ISO 3166 — Country Codes</a></li></ul>{:/}|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>Communist Party of the United States of America. -- History -- Sources</li><li>Buttons (Information artifacts</a></li><li>Christian socialism -- United States -- History -- Sources</li><li>Pamphlets</li><li>Politics</li><li>Vietnam War, 1961-1975</li></ul>{:/}|

[Jump to Collection Level](#collection-level)

#### RELATED MATERIAL

|CSV Element|related_material|
|:---|:---|
|**Description**|Archival materials that have an association to the materials in the collection; often another collection.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:relatedmaterial|
|**Dublin Core Mapping**|dc.relation|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|Preferred Citation for related collection, including collection title, date range for collection, Acquition Number, Repository, and Depositor.|
|**Example(s)**|A.E. Forbes Communist Collection, 1921-1972, AIS.2000.07, Archives &amp; Special Collections, University of Pittsburgh Library System|

[Jump to Collection Level](#collection-level)

#### REPOSITORY

|CSV Element|repository|
|:---|:---|
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
|:---|:---|
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
|:---|:---|
|**Description**|Any conditions that affect the use of the materials in the collection.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|ead:archdesc[@level="collection"]/ead:userestrict/p|
|**Dublin Core Mapping**|dc.rights|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|The University of Pittsburgh holds the property rights to the material in this collection, but the copyright may still be held by the original creator/author. Researchers are therefore advised to follow the regulations set forth in the U.S. Copyright Code when publishing, quoting, or reproducing material from this collection without the consent of the creator/author or that go beyond what is allowed by fair use.|

[Jump to Collection Level](#collection-level)

&nbsp;
### Item Level

#### IDENTIFIER

|CSV Element|id|
|:---|:---|
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
|:---|:---|
|**Description**|A name given to the resource.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|mods:titleInfo{::nomarkdown}<ul><li>mods:title</li><li>mods:subTitle</li><li>mods:nonSort</li></ul>{:/}|
|**Dublin Core Mapping**|dc.title|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**|{::nomarkdown}<ul><li>Title is formatted as following (less the subTitle and/or nonSort where they do not exist): [title]: [subTitle], [nonSort]</li><li>Excludes any Title elements (i.e., mods:titleInfo) with the following @type attribute values: abbreviated, translated, alternative, uniform.</li></ul>{:/}|
|**Example(s)**|{::nomarkdown}<ul><li>Zhou zong li-Ruisidun hui tan quan wen</li><li>Tip top weekly</li><li>Allegheny County Soldiers and Sailors Memorial</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### CREATOR

|CSV Element|creator|
|:---|:---|
|**Description**|A name of an entity responsible for making the content of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|mods:name/mods:namePart _with_ mods:role/mods:roleTerm="creator"|
|**Dublin Core Mapping**|dc.creator|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul><li>Free text. No Limitations.</li></li><li><a href="https://id.loc.gov/authorities/names.html" target="_blank">Library of Congress Name Authority File (LCNAF)</a></li></li><li><a href="http://id.loc.gov/vocabulary/relators.htm" target="_blank">MARC Relators</a></li></ul>{:/}|
|**Notes**|Multiple values within the <mods:name> element are separated by comma (,).|
|**Example(s)**|Stockton, Frank R., 1834-1902|

[Jump to Item Level](#item-level)

#### CONTRIBUTOR

|CSV Element|contributor|
|:---|:---|
|**Description**|A name of an entity responsible for making contributions to the creation or distribution of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|mods:name/mods:namePart _with_ mods:role/mods:roleTerm="contributor"|
|**Dublin Core Mapping**|dc.contributor|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul><li>Free text. No Limitations.</li></li><li><a href="" target="_blank">Library of Congress Name Authority File (LCNAF)](https://id.loc.gov/authorities/names.html</a></li></li><li><a href="http://id.loc.gov/vocabulary/relators.htm" target="_blank">MARC Relators</a></li></ul>{:/}|
|**Notes**|Multiple values within the <mods:name> element are separated by comma (,).|
|**Example(s)**|Abbot Renaud de Semur|

[Jump to Item Level](#item-level)

#### CREATION DATE

|CSV Element|creation_date|
|:---|:---|
|**Description**|A date associated with the creation of the resource.|
|**Required**|No|
|**Repeatable**|No|
|**Element(s)**|mods:originInfo/mods:dateCreated|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**||
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>1872</li><li>1972-2010</li><li>1940/1950</li><li>184u/uuuu</li><li>1962-01-29</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### SORT DATE

|CSV Element|sort_date|
|:---|:---|
|**Description**|A date associated with the creation of the resource and encoded for sorting or other purposes that necessitate normalization.|
|**Required**|No|
|**Repeatable**|No|
|**Element(s)**|mods:originInfo/mods:dateOther[@type="sort"]|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|[ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html)|
|**Notes**|Complete date plus hours and minutes: YYYY-MM-DDThh:mm:ss|
|**Example(s)**|1872-01-01T00:00:00|

[Jump to Item Level](#item-level)

#### DISPLAY DATE

|CSV Element|display_date|
|:---|:---|
|**Description**|A date associated with the creation of the resource and formatted for display.|
|**Required**|No|
|**Repeatable**|No|
|**Element(s)**|mods:originInfo/mods:dateOther[@type="display"]|
|**Dublin Core Mapping**|dc.date|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>November 23, 2004</li><li>1977</li><li>ca. 1950-1960</li><li>Undated</li><li>Post-marked October 31, 1888</li><li>Likely during 80's</li></li><li><a href="" target="_blank">189?]</li><li>February 9</li></li></ul>{:/}|

[Jump to Item Level](#item-level)

#### LANGUAGE

|CSV Element|language|
|:---|:---|
|**Description**|A language in which the content of the resource is expressed.|
|**Required**|Yes|
|**Repeatable**|Yes|
|**Element(s)**|mods:language/mods:languageTerm|
|**Dublin Core Mapping**|dc.language|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/standards/iso639-2/php/code_list.php" target="_blank">ISO 639-2 Language Code List - Codes for the Representation of Names of Languages</a></li></li><li><a href="http://www.loc.gov/marc/languages/" target="_blank">MARC Code List for Language]</a></li>{::nomarkdown}<ul>|
|**Notes**||
|**Example(s)**|eng|

[Jump to Item Level](#item-level)

#### TYPE OF RESOURCE

|CSV Element|type_of_resource|
|:---|:---|
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
|:---|:---|
|**Description**|A designation of a particular physical presentation of a resource, including the physical form or medium of material for a resource.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|mods:physicalDescription/mods:form|
|**Dublin Core Mapping**|dc.format|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/standards/valuelist/marccategory.html" target="_blank">MARC Form Category Term List]</a></li></li><li><a href="https://www.loc.gov/standards/valuelist/marcform.html" target="_blank">MARC Form of Item Term List</a></li></li><li><a href="https://www.loc.gov/standards/valuelist/marcsmd.html<" target="_blank">Specific Material Form Term List/a></li><li>General Material Designation (GMD</a></li><li>Free text. No limitations.</li></ul>{:/}|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>print</il><li>gelatin silver prints</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### EXTENT

|CSV Element|extent|
|:---|:---|
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
|:---|:---|
|**Description**|A term that designates a category characterizing a particular style, form, or content embodied by the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|{::nomarkdown}<ul><li>mods:genre</li><li>mods:subject/mods:genre</li></ul>{:/}|
|**Dublin Core Mapping**|dc.type|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/standards/valuelist/marcgt.html" target="_blank">MARC Genre Term List]</a></li></li><li><a href="https://www.getty.edu/research/tools/vocabularies/aat/" target="_blank">Art & Architecture Thesaurus (AAT)</a></li></li><li><a href="https://www.oclc.org/research/themes/data-science/fast/download.html" target="_blank">Faceted Application of Subject Terminology (FAST)</a></li></li><li><a href="https://www.loc.gov/standards/valuelist/marcmuscomp.html" target="_blank">MARC Form of Musical Composition Code List</a></li></li><li><a href="https://www.loc.gov/rr/print/tgm2/" target="_blank">Library of Congress Genre/Form Terms</a></li></li><li><a href="https://rbms.info/vocabularies/genre/alphabetical_list.htm" target="_blank">RBMS Controlled Vocabularies: Genre Terms</a></li></li><li><a href="https://www.loc.gov/rr/print/tgm2/" target="_blank">Thesaurus for graphic materials (TGM II, Genre and physical characteristic terms)</a></li></li><li><a href="https://rbms.info/vocabularies/provenance/alphabetical_list.htm" target="_blank">RBMS Controlled Vocabularies: Provenance Evidence Terms</a></li></li><li><a href="http://experimental.worldcat.org/gsafd/" target="_blank">Guidelines on Subject Access to Individual Works of Fiction, Drama, Etc., 2nd edition</a></li></li><li><a href="" target="_blank">Term and Code List for RDA Content Types](https://www.loc.gov/standards/valuelist/rdacontent.html</a></li></li><li><a href="http://id.loc.gov/vocabulary/genreFormSchemes/ftamc.html" target="_blank">Form terms for archival and manuscripts control</a></li></ul>{:/}|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>text</li><li>novel</li><li>Embossed cloth binding (Binding)-1851</li><li>Fiction.</li><li>archival document</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### ABSTRACT

|CSV Element|abstract|
|:---|:---|
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
|:---|:---|
|**Description**|A term or phrase representing the primary topic(s) on which the resource is focused.|
|**Required**|No
|**Repeatable**|Yes|
|**Element(s)**|mods:subject{::nomarkdown}<ul><li>mods:topic</li><li>mods:name</li><li>mods:titleInfo</li><li>mods:occupation</li></ul>{:/}|
|**Dublin Core Mapping**|dc.subject|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="http://id.loc.gov/authorities/names.html" target="_blank">Library of Congress Name Authority File (LCNAF)</a></li></li><li><a href="https://www.oclc.org/research/themes/data-science/fast/download.html" target="_blank">Faceted Application of Subject Terminology (FAST)</a></li></li><li><a href="https://www.loc.gov/aba/cyac/childsubjhead.html" target="_blank">Children's Subject Headings (CSH)</a></li></li><li><a href="http://id.loc.gov/authorities/childrensSubjects.html" target="_blank">Library of Congress Subject Headings Supplemental Vocabularies: Children’s Headings (LCSHAC)</a></li></li><li><a href="https://www.nlm.nih.gov/mesh/meshhome.html" target="_blank">Medical Subject Headings (MeSH)</a></li></li><li><a href="" target="_blank">National Agricultural Library](https://agclass.nal.usda.gov/</a></li></li><li><a href="https://rvmweb.bibl.ulaval.ca/eccueil" target="_blank">Répertoire de vedettes-matière (RVM)</a></li></ul>{:/}|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>Advertising</li><li>Pittsburgh</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### TEMPORAL COVERAGE

|CSV Element|temporal_coverage|
|:---|:---|
|**Description**|A chronological statement that indicates the date(s) or time period covered by the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|mods:subject/mods:temporal|
|**Dublin Core Mapping**|dc.coverage|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul><li>Free text. No limitations.</li></li><li><a href="https://www.iso.org/iso-8601-date-and-time-format.html" target="_blank">ISO 8601 — Date and Time Format</a></li></ul>{:/}|
|**Notes**|May be a simple or hierarchical geographical name or area code (e.g., city section, city, county, territory, state, region, country, continent, island, area, extraterrestrial area), cartographic data (e.g., coordinates, scale, projection)|
|**Example(s)**|{::nomarkdown}<ul><li>19th century</li><li>1775-1783</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### GEOGRAPHIC COVERAGE

|CSV Element|geographic_coverage|
|:---|:---|
|**Description**|A geographical name or geographical data that indicates the spatial coverage of the resource.|
|**Required**|No|
|**Repeatable**|Yes|
|**Element(s)**|mods:subject{::nomarkdown}<ul><li>mods:geographic</li><li>mods:geographicCode</li><li>mods:hierarchicalGeographic</li>{::nomarkdown}<ul><li>mods:continent</li><li>mods:country</li><li>mods:region</li><li>mods:state</li><li>mods:territory</li><li>mods:county</li><li>mods:city</li><li>mods:island</li><li>mods:area</li><li>mods:extraterrestrialArea</li><li>mods:citySection</li></ul>{:/}<li>mods:cartographics</li>{::nomarkdown}<ul><li>mods:scale</li><li>mods:projection</li><li>mods:coordinates</li></ul>{:/}<li>mods:geographicCoordinates</li></ul>{:/}|
|**Dublin Core Mapping**|dc.coverage|
|**Vocabulary/Encoding Scheme(s)**|{::nomarkdown}<ul></li><li><a href="https://www.loc.gov/marc/geoareas/" target="_blank">MARC Code List for Geographic Areas</a></li></li><li><a href="" target="_blank">MARC Code List for Countries](https://www.loc.gov/marc/countries/countries_code.html</a></li></li><li><a href="https://www.iso.org/iso-3166-country-codes.html" target="_blank">ISO 3166 — Country Codes</a></li><li>Free text. No limitations.</li></ul>{:/}|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>Downtown</li><li>n------</li><li>North America</li></ul>{:/}|

[Jump to Item Level](#item-level)

#### COLLECTION IDENTIFIER

|CSV Element|collection_id|
|:---|:---|
|**Description**|A digital collection to which the resource belongs.|
|**Required**|Yes|
|**Repeatable**|Yes|
|**Element(s)**|rdf:Description/fedora:isMemberOfCollection[@rdf:resource]|
|**Dublin Core Mapping**|dc.relation|
|**Vocabulary/Encoding Scheme(s)**||
|**Notes**|Alpha-numeric string with special characters, i.e. a colon (:) and a period (.), formatted as follows: pitt:collection_nnn|
|**Example(s)**|pitt:collection.299|

[Jump to Item Level](#item-level)

#### HOST

|CSV Element|host|
|:---|:---|
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
|:---|:---|
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
|:---|:---|
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
|:---|:---|
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
|:---|:---|
|**Description**|An official name of the institution responsible for depositing the resource.|
|**Required**|Yes|
|**Repeatable**|No|
|**Element(s)**|mods:name/mods:namePart _with_ mods:role/mods:roleTerm="depositor"|
|**Dublin Core Mapping**|n/a|
|**Vocabulary/Encoding Scheme(s)**|Free text. No limitations.|
|**Notes**||
|**Example(s)**|{::nomarkdown}<ul><li>University of Pittsburgh</li><li>African American Chamber of Commerce of Western Pennsylvania</li><li>Rodef Shalom Congregation</li></ul>{:/}|

[Jump to Item Level](#item-level)
