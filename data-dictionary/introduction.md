---
layout: default
title: Introduction
parent: Data Dictionary
nav_order: 1
---

#### [Home](http://cadatpitt.github.io)

# Introduction

The CaD@Pitt Data Dictionary defines and describes the _data layers_ (datasets) in the [Data Layers Repository](https://github.com/CaDatPitt/data-layers), which are categorized into three [3] types:
* **[source data](https://github.com/CaDatPitt/data-layers/tree/master/source-data)**: snapshots of library collections metadata files in their original source format (e.g., EAD, MODS, RELS-EXT) stored in either the Library’s digital repository (Islandora) or catalog system (Alma);
* **[base layers](https://github.com/CaDatPitt/data-layers/tree/master/base-layers)**: curated datasets (CSV files) derived and simplified from the source data layers, as defined and described by this data dictionary and the application profiles;
* **[extension layers](https://github.com/CaDatPitt/data-layers/tree/master/extension-layers)**: scholar-created datasets or outputs that enrich/augment library collections data (i.e., source data and base layers), with accompanying documentation.

## Overview of the Data Layers

### **Source data**
_Source data_ are metadata records exported from either the library’s catalog system (Alma) or the library’s digital repository system (Islandora). Source data may be binary MARC21 (ISO 2709 implementation), MODS XML converted from MARC21, or data from one of the following Islandora (metadata) datastreams listed below:

#### **Prioritized Datastreams**
_Always included in collections data, when available; used to create base layers_
* **EAD (Encoded Archival Description)**: descriptive EAD XML metadata based on digital finding aids
* **MODS (Metadata Object Description Schema)**: descriptive MODS XML metadata filled out during ingest (more robust)
* **RELS-EXT (Relationships-External)**: Fedora digital object relationship XML metadata that contains exterior relationship information defining the relationship of a digital object to other objects in the repository system

#### **Other Available Datastreams**
_Available upon request_
* **DC (Dublin Core)**: descriptive DC XML metadata (simple)
<!--* **FITS (File Information Tool Set)**: identifies, validates, and extracts technical metadata for various file formats. It wraps several third-party open source tools, normalizes and consolidates their output, and reports any errors-->
* **FULL_TEXT**: text of a PDF, pulled from the PDF format's text (as opposed to being pulled via OCR)
* **HOCR (HTML Optical Character Recognition)**: formatted OCR text (formatting information embedded HTML or XHTML) used to more accurately display OCR output
* **JP2**: web-viewable JPEG2000 image created from TIFF files
* **JPG**: plain JPG derivative created from TIFF files
* **MARC (Machine-readable cataloging)**: descriptive binary MARC record metadata for items that were catalogued before ingested in Islandora
* **MKV**: Matroska video derivative
* **MP4**: MPEG-4 video derivative
* **OCR (Optical Character Recognition)**: OCR text files
* **OBJ (Object)**: default datastream for the actual original binary ingested with an object, usually stored in TIFF format
* **OGG**: OGG Vorbis video derivative (audio only)
* **PDF**: PDF derivative created either during ingest of a page, or stitched together into an entire book, newspaper, or other paged content
* **PREVIEW**: binary preview of a PDF used for viewing
* **PROXY_MP3**: derivative web-suitable file for download and display
* **RELS-INT (Relationships-Internal)**: Fedora digital object relationship XML metadata that contains interior relationship information defining a page's relationship to other pages and the book (or other paged content) as a whole
* **TN (Thumbnail)**: thumbnail image used to represent the object in lists
* **TECH-MD (Technical Metadata)**: technical metadata FITS (File Information Tool Set) XML record filled out during ingest, including media type, file name and size, creating software program name, image dimensions, color model, and orientation
* **TRANSCRIPT**: text file (saved in WebVTT format) containing supplementary information about a video, including subtitles, captions, chapters, and other metadata.

Despite being encoded in standards/schemes, the data records are often non-standardized and incomplete due to variation in data entry practices and conversions of data from one standard/scheme to another. For example, dates may appear or be missing in one or more fields in the source data and use varying formats/encoding. To avoid excluding date information when it exists for an item by selecting a single field, multiple date elements have been included in the base layers to capture date information when possible; however, users of the dataset may have to normalize dates across fields for computational methods using date information.

### **Base layers**
_Base layers_ are derived from the source data and have a flattened (i.e., tabular, two-dimensional) data model and simplified metadata elements sets for increased readability. The data in the base layers have also been pared down from that in the source data to avoid representing an overwhelming amount of information and to include data points that we expect to be most useful for scholars in general. However, metadata elements that have been excluded in the base layer may be incorporated in an extended version of the base layer by request; in other words, scholars may customize the base layer to include one or more additional elements from the source data.

### **Extension layers**
Unlike the other, library-generated data layers, _extension layers_ are (co-)created by researchers as a site for explicitly interpretive and scholarly data. While they make use of the source data/base layers, they are not constrained by conventions of library-based descriptive frameworks. They may improve the quality of the metadata in the source data/base layers, introduce new elements/data points, or not only (or at all) take the form of spreadsheet files; for example, an extension layer might include data visualizations.


## Outline of the Data Dictionary
The [Data Standards/Schemas, Controlled Vocabularies & Encoding Schemes](standards.md) section of this data dictionary enumerates the controlled vocabularies and encoding schemes/standards to which the source data and base layers adhere.

### **Metadata Element Sets**

The sections for the metadata element sets (i.e., [Archival Collections Metadata Element Set](archival-collections.md), [Serial Collections Metadata Element Set](serial-collections.md), [Monograph Collections Metadata Element Set](monograph-collections.md)) enumerate, define, and describe the metadata elements and input guidelines for base layers. The base layers are organized by four collection types: archival, serial, monograph, and mixed (includes items from more than one collection). These distinction account for variations in the data source (i.e., catalog or digital repository) and the schemas/standards for source data records (see table below) as well as the ranges of available data points (see the [Metadata Element Set Chart](metadata-element-set-chart.md)):

|Collection Type|Data Source|Metadata Standards/Schemas|Base Layer(s)|
|---|---|---|---|
|archival|digital repository|EAD, FITS, MODS, RELS-EXT|collection-level and item-level|
|serial|catalog;<br>digital repository<br>mixed|MARC, MODS;<br>EAD, MODS, RELS-EXT;<br>EAD, MARC, MODS, RELS-EX|collection-level and/or item-level|
|monograph|catalog;<br>digital repository<br>mixed|MARC, MODS;<br>EAD, MODS, RELS-EXT;<br>EAD, MARC, MODS, RELS-EX|collection-level and/or item-level|
|mixed|catalog;<br>digital repository<br>mixed|MARC, MODS;<br>EAD, MODS, RELS-EXT;<br>EAD, MARC, MODS, RELS-EX|collection-level and/or item-level|

Collections in the digital repository have base layers for two [2] levels of description (i.e., collection-level and item-level). Collections in the catalog have only one level of description (i.e., item-level). Serial and monograph collections may contain items from the catalog and/or the digital repository. For this reason, there are catalog versions and digital repository (hence, "digital") versions of the metadata element sets. The digital versions include elements in addition to those in the catalog versions. If a researcher's collection contains items from both sources, they may decide to use either the catalog or digital version of the metadata element set, or to use the "mixed" version, which includes all elements from both the catalog and digital versions. If there is at least one finding aid associated with (items in) the collection, serial and monograph collections may also have a collection-level base layer because they are a part of an archival collection.

### **Application Profiles**
Linked in the final section of this data dictionary, the [Application Profiles](application-profiles.md) organize the information presented in sections 3-5 into spreadsheets (one for each collection type), which represent the elements, attributes, and values in the source data from which the base layer element sets are derived.

Please note that, as the base layers are derivatives of metadata that have already been created, this data dictionary _does not prescribe_ how data should be input. Hence, the guidelines in the data dictionary and the application profiles have been retroactively applied in this project to reflect the ways in which library metadata has been entered up until this point. Accordingly, an element is considered “mandatory” when all metadata records contain a value for that data point, and “repeatable” when more than one value appears in any metadata record or the encoding scheme/standard dictates. The definitions and descriptions of the metadata in the base layers in this data dictionary are a work in progress and will be updated as we learn more about the nature of the source data.

Data documentation for extension layers (found in the directory for the respective extension layer) may draw from this data dictionary, if elements from the base layer are included in the extension layer.
