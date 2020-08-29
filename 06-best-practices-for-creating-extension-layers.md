---
layout: default
title: Best Practices for Creating Extension Layers
nav_order: 6
---

#### [Home](http://cadatpitt.github.io)

# Best Practices for Creating Extension Layers

## Introducing Extension Layers
_For instructors_: When introducing a researcher to the process of creating an extension layer, consider following the sequence from the [instructional modules](https://cadatpitt.github.io/modules/). Dividing the process into steps can provide structure for researchers who are not sure how to get started.

## Designing Extension Layers
- When developing ideas for extension layers, creating new data elements or enriching existing data may be based on a desire to:
  - Add information in order to answer a research question
  - Enhance functionality (e.g. search, faceting, and filtering) by adding information such as geographic coordinates, genres, item types, etc.
  - Correct, refine, or create consistency within existing fields by filling in missing values, correcting mistakes, replacing vague or uncertain information with more specific information, and/or making data from different sources consistent.
- When creating a new extension layer, it is important to link items to the base layer. This ensures that the base layer and any associated extension layers remain associated so that data can be identified, located, and merged later. The best way to do this is by including an item’s unique identifier as a foreign key in the new extension layer.
- Don’t be afraid to make liberal use of base layer data! An extension layer may be composed primarily of base layer data with one or more data elements enhanced or added, or even by adding additional elements from the source data that are not included in the base layer.
- _For instructors_: Consider where instruction might be required or useful. The Collections as Data project can be a powerful opportunity to introduce researchers who are new to data work to core concepts such as spreadsheet design and techniques for creating consistent and useful data.
- Consider how creators will be attributed at the design stage. Single creators may be attributed in metadata for the extension layer when it is published. If there are multiple creators, consider including an attribution field within the layer itself.

## Creating Extension Layers
- Consider which tools might be most appropriate for the creator(s).
  - General audiences, one-off events, and classes which do not have a technology focus might benefit from the use of more lightweight tools such as a clearly-designed spreadsheet presented via Google Sheets or Excel. These spreadsheets will be simple to create and can be easily changed on the fly in response to learners’ needs, allowing for a flexible instruction experience.
  - If you intend to crowdsource data or otherwise ask people to create or contribute to extension layers without going through a tailored orientation, a custom web application or crowdsourcing platform (e.g. [Zooniverse](https://www.zooniverse.org/)) may offer a more controlled environment for data creation and a consistent format for data output. These environments will be more work to set up, but offer the benefit of increased functionality and flexibility.
- Create a data dictionary and metadata for extension layers in order to document important information about their content and creation.
  - Metadata for extension layers should include:
    - Attribution of creator(s) of extension layer
    - Source(s) of base layer data (sources of base layer data and/or links to location of base layer data)
    - Data elements that have been added or transformed
    - Descriptive information about the purpose of and materials included in the extension layer
  - A data dictionary will contain a description of the different data elements contained in the extension layer. Although you may be able to copy information about unchanged base layer data elements from the associated data dictionary, for each new or enriched data element the data dictionary should include:
    - Data labels and any context that is necessary to understand them
    - Accepted values (integer-only, Boolean, controlled vocabulary list, free-text, etc.)
    - Whether the element is required
    - Whether multiple values can be entered in the same field and what delimiter is used if so
    - (Optional) notes
    - (Optional) examples

## Publishing and sharing extension layers
Robust advice about how to make extension layers available can be found in the [Publishing an Extension Layer](07-publishing-an-extension-layer.md) document.
