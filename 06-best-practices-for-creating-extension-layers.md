---
layout: default
title: Best Practices for Creating Extension Layers
nav_order: 6
---

#### [Home](http://cadatpitt.github.io)

# Best Practices for Creating Extension Layers

## Introducing extension layers
_For instructors_: When introducing a researcher to the process of creating an extension layer, consider following the sequence from the [instructional modules](https://cadatpitt.github.io/modules/). Dividing the process into steps can provide structure for researchers who are not sure how to get started.

## Designing extension layers
- When developing ideas for extension layers, creating new data elements or enriching existing data may be based on a desire to:
  - Add information in order to answer a research question;
  - Enhance functionality (e.g. search, faceting, and filtering) by adding information such as geographic coordinates, genres, item types, etc.;
  - Correct, refine, or create consistency within existing fields by filling in missing values, correcting mistakes, replacing vague or uncertain information with more specific information, and/or making data from different sources consistent.
- When creating a new extension layer, make sure to include a column for the items' unique identifiers; the identifier will serve as a [foreign key](https://www.techopedia.com/definition/7272/foreign-key) to the base layer in which the item appears. This ensures that the base layer and any associated extension layers remain associated so that data can be identified, located, and merged later. In the base layer, the unique identifier is the `identifier` element (see it in the metadata element set for [archival](https://cadatpitt.github.io/documentation/data-dictionary/archival-collections.html#identifier), [serial](https://cadatpitt.github.io/documentation/data-dictionary/serial-collections.html#identifier), or [monograph](https://cadatpitt.github.io/documentation/data-dictionary/monograph-collections.html#identifier) collections).
- Don’t be afraid to make liberal use of base layer data! An extension layer may be composed primarily of base layer data with one or more data elements enhanced or added; additional elements may be entirely new or extracted from the source data (if not already included in the base layer).
- _For instructors_: Consider where instruction might be required or useful. The Collections as Data project can be a powerful opportunity to introduce researchers who are new to data work to core concepts such as spreadsheet design and techniques for creating consistent and useful data.
- Consider how creators will be attributed at the design stage. Single creators may be attributed in metadata for the extension layer when it is published. If there are multiple creators, consider including an attribution field within the layer itself.

## Creating extension layers
- Consider which tools might be most appropriate for the creator(s).
  - General audiences, one-off events, and classes that do not have a technology focus might benefit from the use of more lightweight tools, such as a clearly-designed spreadsheet presented via Google Sheets or Excel. These spreadsheets will be simple to create and can be easily changed on the fly in response to learners’ needs, allowing for a flexible instruction experience.
  - If you intend to crowdsource data or otherwise ask people to create or contribute to extension layers without going through a tailored orientation, a custom web application or crowdsourcing platform (e.g. [Zooniverse](https://www.zooniverse.org/)) may offer a more controlled environment for data creation and a consistent format for data output. These environments will be more work to set up but offer the benefit of increased functionality and flexibility.
- Create metadata and a [data dictionary](http://www.lib.uiowa.edu/data/manage/documenting/readme/#dictionaries) or [README file](http://www.lib.uiowa.edu/data/manage/documenting/readme/#readme) for extension layers in order to document important information about their content and creation.
  - Metadata for extension layers should include:
    - Attribution of creator(s) of extension layer
    - Source(s) of base layer data (if possible, include links to location of base layer data)
    - Data elements that have been added or transformed
    - Descriptive information about the purpose of and materials included in the extension layer
  - A data dictionary/README file will contain a description of each data element contained in the extension layer. You may copy information about unchanged base layer data elements from the associated metadata element set ([archival](https://cadatpitt.github.io/documentation/data-dictionary/archival-collections.html#identifier), [serial](https://cadatpitt.github.io/documentation/data-dictionary/serial-collections.html#identifier), or [monograph](https://cadatpitt.github.io/documentation/data-dictionary/monograph-collections.html#identifier) collection) description in the [CaD@Pitt Data Dictionary](https://cadatpitt.github.io/documentation/04-data-dictionary). For each new or enriched data element, the data dictionary should include:
    - Element labels (as they appear in the CSV spreadsheet) and any context that is necessary to understand them
    - Accepted values (integer-only, Boolean, controlled vocabulary list, free-text, etc.)
    - Whether or not the element is required
    - Whether multiple values can be entered in the same field and, if so, what delimiter is used (pipe, semicolon, comma, etc.)
    - Notes (optional)
    - Examples (optional)

## Publishing and sharing extension layers
Advice about how to make extension layers available can be found in the [Publishing an Extension Layer](07-publishing-an-extension-layer.md) document.
