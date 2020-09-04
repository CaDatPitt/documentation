---
layout: default
title: Principles and Objectives
nav_order: 3
---

#### [Home](http://cadatpitt.github.io)
# Principles and Objectives

The CaD@Pitt project is based in the University of Pittsburgh Library System and aims to increase the visibility and discoverability of library collections, make library collections data accessible for computational use, and enable scholars to extend/enrich collections data with critical, research-driven layers of additional data.

## Target Audiences

This project was developed by and for library workers, scholars (researchers, students, and instructors), and the public. Accordingly, we have these audiences and their various use cases in mind:
- Libraries and information professionals seeking to…  
  - use this project as an implementation model for a similar endeavor at their own institution
  - collaborate with the CaD@Project Team to develop a cross-institutional collections data platform
- Scholars and community members seeking to...
  - acquire metadata describing library collections at Pitt for research projects
  - create scholarly and interpretive datasets for library collections
- Instructors seeking to…
  - incorporate library collections and data-centered modules in their curriculum
  - teach critical and computationally minded data practices in their courses

## Collections

The collections in the CaD@Pitt project currently include items from...
- archival collections that have been at least partially digitized, stored in the Library’s digital repository (Islandora 7), and published on one of the Library’s digital collection sites (i.e., [ULS Digital Collections](https://digital.library.pitt.edu/), [Historic Pittsburgh](http://historicpittsburgh.org/), and [Documenting Pitt](https://documenting.pitt.edu/)); and
- general, special, and distinctive collections in the Library's [catalog](https://pitt.primo.exlibrisgroup.com/discovery/search?vid=01PITT_INST:01PITT_INST&lang=en).
In addition to collections developed by the Library, the CaD@Pitt project includes collections developed by researchers, who can curate new collections by selecting items from the Library’s collections.

While our project is intended to support any and all library collections, it has prioritized those reflecting the perspectives of underrepresented groups,  which are often given inadequate attention for structural or systemic reasons. These collections have strong potential to tell as-yet untold stories and can increase institutional commitment to bringing underrepresented histories to light. Our target collections feature the following:
- the voices of African and African diasporic communities, American Labor Unionists, American left-wing organizations, the LGBTQ community, and feminists;
- a diverse array of serials (e.g., journals, magazines, newspapers, newsletters) and ephemera (e.g., broadsides, flyers, cartoons).
Serials and ephemera are foregrounded in this project because, historically, the conditions of their production and reception often made serials and ephemera more desirable venues for specific counterpublics than monograph publication.

<!--A list of collections for which the CaD@Pitt repository contains datasets can be viewed here. This list continues to grow as scholars request access to data for existing library collections or develop their own collections.-->

## Data Layers

Our project takes a “data layers” approach, which diverges from a monolithic data model (i.e.,  singular, non-interpretive, and exhaustive). Instead, it presents an interface made up of data from multiple sources that vary in encoding scheme, granularity of description, and completeness/richness. This approach liberates data creation and curation from the expectation of perfection or singularity of authority, and it allows data to be enriched, augmented and interpreted incrementally over time through a layering process. It also provides a practical and low-barrier entry point for scholars to create datasets, or data layers, based on their research priorities and to share those layers. The CaD@Pitt repository houses three [3] types of data layers:
- **source data**: snapshots of library collections metadata files in their original source format (e.g., MARC 21, EAD, DC, MODS, RELS-EXT, RELS-INT, FITS);
- **base layers**: curated datasets (CSV files) derived and simplified from the source data layers, defined and described by the data dictionary and application profiles;
- **extension layers**: scholar-created datasets that enrich/augment library collections data (i.e., source data and base layers), with accompanying documentation.

_Source data_ are metadata records exported from either the library’s catalog system (Alma) or the library’s digital repository system (Islandora). Source data use either MARC 21 (for catalog records) or XML standards/schemas for encoding resource metadata (e.g., EAD, Dublin Core, MODS, RELS-EXT, RELS-INT, FITS).

While the source data files are the most complete version of library metadata, they may not be amenable to many computational use cases due to their complex, hierarchical data structure and metadata quality issues. Despite being encoded in standards/schemes, the data records are often non-standardized and incomplete due to variation in data entry practices and conversions of data from one standard/scheme to another. Further, the source data may not be particularly accessible to users who are not familiar with hierarchical data structures or (specialized) encoding standards.

_Base layers_ address some of the computational and readability issues of source data. Derived from source data, they have a flattened (i.e., tabular, two-dimensional) data model and simplified elements sets that are more readable for most users. The data in the base layers have also been pared down from that in the source data to avoid representing an overwhelming amount of information and to include data points that we expect to be most useful for scholars in general. However, metadata elements that have been excluded in the base layer may be incorporated in an extended version of the base layer by request; in other words, scholars may customize the base layer to include one or more additional elements from the source data.   

_Extension layers_—unlike the other, library-generated data layers—are (co-)created by researchers as a site for explicitly interpretive and scholarly data. While they make use of the source data/base layers, they are not constrained by conventions of library-based descriptive frameworks. They may improve the quality of the metadata in the source data/base layers, introduce new elements/data points, or not only (or at all) take the form of spreadsheet files; for example, an extension layer might include data visualizations.  

The data layers are accompanied by Python and XSLT scripts for extracting and transforming source data to create base layers, as well as resources for creating extension layers. Scholars can download data layers in the repository, request source data and base layers for library collections not already represented in the repository, and share their own extension layers in the repository. Our project serves as a model for how other libraries can share collections data, and our repository can support data layers for collections from other libraries, though local and (inter)national element sets and controlled vocabularies may be used differently across institutions.

## Instructional Modules

This project facilitates scholars’ engagement with and enrichment of library collections data through five [5] instructional modules that 1) orient learners to collections as data and as products of curation and 2) teach critical and computationally minded data practices:
- **Develop a custom collection**: Create a collection drawing from any combination of the Library’s general, archival, special, and/or distinctive collections;
- **Design a layer**: Propose a data collection plan for a dataset (extension layer), based on a custom or pre-existing collection, that answers a research question or meets a particular need;
- **Critique a layer**: Critique the utility, feasibility, and ethicality of an extension layer;
- **Implement a layer**: Implement an extension layer by entering data into a spreadsheet;
- **Visualize a layer**: Visualize collections data using a visualization tool.

These modules have been designed as a sequence but may be used for individual lessons and otherwise modified to suit varying contexts.
