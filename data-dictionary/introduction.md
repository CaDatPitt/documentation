---
layout: default
title: Introduction
parent: Data Dictionary
nav_order: 1
---

#### [Home](http://cadatpitt.github.io)

# Introduction

The CaD@Pitt Data Dictionary defines and describes the **data layers** (datasets) in the [Data Layers Repository](https://github.com/CaDatPitt/data-layers), which are categorized into three [3] types:
* **[source data](https://github.com/CaDatPitt/data-layers/tree/master/source-data)**: snapshots of library collections metadata files in their original source format (e.g., MARC21, EAD, DC, MODS, RELS-EXT) stored in either the Library’s digital repository (Islandora) or catalog system (Alma);
* **[base layers](https://github.com/CaDatPitt/data-layers/tree/master/base-layers)**: curated datasets (CSV files) derived and simplified from the source data layers, as defined and described by this data dictionary and the application profiles;
* **[extension layers](https://github.com/CaDatPitt/data-layers/tree/master/extension-layers)**: scholar-created datasets or outputs that enrich/augment library collections data (i.e., source data and base layers), with accompanying documentation.

## Overview of the Data Layers

**Source data** are metadata records exported from either the library’s catalog system (Alma) or the library’s digital repository system (Islandora). Source data may be binary MARC21 (ISO 2709 implementation), MODS XML (converted from MARC21), or one of the following Islandora metadata datastreams (XML standards/schemas for encoding resource metadata):
* Machine-readable cataloging (MARC21): contains descriptive MARC record metadata for items that were catalogued before ingested in Islandora
* Encoded Archival Description (EAD): contains descriptive EAD based on digital finding aids
* Dublin Core (DC): contains descriptive DC metadata (simple)
* MODS: contains descriptive MODS Metadata filled out during ingest (more robust)
* Relationships-External (RELS-EXT): Fedora digital object relationship metadata that contains exterior relationship information defining the relationship of a digital object to other objects in the repository system

Despite being encoded in standards/schemes, the data records are often non-standardized and incomplete due to variation in data entry practices and conversions of data from one standard/scheme to another. For example, dates may appear or be missing in one or more fields in the source data and use varying formats/encoding. To avoid excluding date information when it exists for an item by selecting a single field, multiple date elements have been included in the base layers to capture date information when possible; however, users of the dataset may have to normalize dates across fields for computational methods using date information.

**Base layers** are derived from the source data and have a flattened (i.e., tabular, two-dimensional) data model and simplified metadata elements sets for increased readability. The data in the base layers have also been pared down from that in the source data to avoid representing an overwhelming amount of information and to include data points that we expect to be most useful for scholars in general. However, metadata elements that have been excluded in the base layer may be incorporated in an extended version of the base layer by request; in other words, scholars may customize the base layer to include one or more additional elements from the source data.

**Extension layers**—unlike the other, library-generated data layers—are (co-)created by researchers as a site for explicitly interpretive and scholarly data. While they make use of the source data/base layers, they are not constrained by conventions of library-based descriptive frameworks. They may improve the quality of the metadata in the source data/base layers, introduce new elements/data points, or not only (or at all) take the form of spreadsheet files; for example, an extension layer might include data visualizations.


## Outline of the Data Dictionary
The [Metadata Standards/Schemas, Controlled Vocabularies & Encoding Schemes](https://github.com/CaDatPitt/data-layers/wiki/2.-Metadata-Standards-Schemas,-Controlled-Vocabularies-&-Encoding-Schemes) section of this data dictionary enumerates the controlled vocabularies and encoding schemes/standards to which the source data and base layers adhere.

The sections for the metadata element sets (i.e., 3. [Metadata Element Set for Archival Collections](https://github.com/CaDatPitt/data-layers/wiki/3.-Metadata-Element-Set-for-Archival-Collections),  4. [Metadata Element Set for Serial Collections](https://github.com/CaDatPitt/data-layers/wiki/4.-Metadata-Element-Set-for-Serial-Collections),  and 5. [Metadata Element Set for Monograph Collections](https://github.com/CaDatPitt/data-layers/wiki/5.-Metadata-Element-Set-for-Monograph-Collections) enumerate, define,  and describe the metadata elements and input guidelines for base layers. The base layers are organized by three collection types to account for variations in the data source (i.e., catalog or digital repository) and the schemas/standards for source data records (see table below) as well as the ranges of available data points (see the Metadata Element Set Comparison Chart):

|Collection Type|Data Source|Metadata Standards/Schemas|Base Layer(s)|
|---|---|---|---|
|Archival|digital repository|EAD, FITS, MODS, RELS-EXT|collection-level and item-level|
|Serial|catalog;<br>digital repository|MARC;<br>EAD, MODS, RELS-EXT|collection-level and/or item-level|
|Monograph|catalog|MARC|item-level|

Collections in the digital repository have base layers for two [2] levels of description (i.e., collection-level and item-level). Collections in the catalog have only one level of description (i.e., item-level). Serial collections may contain items from the catalog and/or the digital repository. For this reason, there is a catalog version and a digital repository (hence, "digital") version of the metadata element set. The digital version includes elements in addition to those in the catalog version. If a researcher's collection contains items from both sources, they may decide to use either the catalog or digital version of the metadata element set, depending on what elements are relevant for their research. Monograph collections may also contain items from both the catalog and the digital repository; researchers may choose the metadata element set for either archival collections or monograph collections, depending on which contains the most relevant elements.

Linked in the final section of this data dictionary, the [Application Profiles](application-profiles.md) organize the information presented in sections 3-5 into spreadsheets (one for each collection type), which represent the elements, attributes, and values in the source data from which the base layer element sets are derived.

Please note that, as the base layers are derivatives of metadata that have already been created, this data dictionary _does not prescribe_ how data should be input. Hence, the guidelines in the data dictionary and the application profiles have been retroactively applied in this project to reflect the ways in which library metadata has been entered up until this point. Accordingly, an element is considered “mandatory” when all metadata records contain a value for that data point, and “repeatable” when more than one value appears in any metadata record or the encoding scheme/standard dictates. The definitions and descriptions of the metadata in the base layers in this data dictionary are a work in progress and will be updated as we learn more about the nature of the source data.

Data documentation for extension layers (found in the directory for the respective extension layer) may draw from this data dictionary, if elements from the base layer are included in the extension layer.
