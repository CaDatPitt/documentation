---
layout: default
title: Publishing an Extension Layer
nav_order: 8
---

#### [Home](http://cadatpitt.github.io)
# Publishing an Extension Layer
An extension data layer is both a dataset and a work of scholarship. Therefore, the goals for publishing an extension layer include 
1) supporting its use and re-use as data (e.g. accessibility, intelligibility, validation, computational tractability), as well as 
2) supporting it as a publication within the scholarly communications ecosystem (e.g., discoverability, citability, attribution, provenance)

The CaD@Pitt project does not suggest a single path for publishing extension layers. There are different options available for making data 
available while still addressing the functions of scholarly communication. This section of the documentation offers general principles and 
suggestions for publishing extension layers. It also hopes to provide information that will help you evaluate the pros and cons of various 
repository options.

## Preparing your extension layer
The following steps are generalized, and many of them apply to preparing any dataset for publication. Some of the specifics of these steps 
may be influenced by the choice of publication venue. For example, many repositories will mandate a certain metadata schema, or define a 
data quality and integrity standard. However, these steps should provide a sense of overall good practice.
- Remove fields copied from base layer, except linking identifier(s)
- Review data for completeness / integrity / legibility
- Create data dictionary / README that describes the individual fields, how they are populated, and any conventions of format
- Create metadata for dataset
  - As mentioned, your publication venue may have its own required schema. However, for an example of a general practice, see the
    [DataCite Schema](https://schema.datacite.org/), a discipline-agnostic dataset metadata schema
  - Because an extension layer has an important relationship to its base layer(s), make a clear reference to those sources in your metadata
  - Remember to include attribution for all contributors to your extension layer

## Choosing a venue for publication
There are many options for publishing data, and many for publishing scholarly outputs. Choosing the most appropriate venue for your extension
layer will depend on evaluating a number of different factors. If you are making this decision for the first time, we offer some pros and cons 
of three different options: GitHub or similar open code repository, an academic/disciplinary data repository, and an institutional repository.

### GitHub or other open code repository
|pros                                                                          |cons                                                        | 
|------------------------------------------------------------------------------|------------------------------------------------------------|  
|in the workflow and toolchain of developers and experienced data users        |some technical and cultural barriers to non-technical users |
|support for version control management                                        |not optimized for scholarly communications considerations   |
|highly open user community; platform connects many other users and depositors |optimized for code rather than data                         |

### Academic/Disciplinary Data repository
|pros                                                                          |cons                                                        | 
|------------------------------------------------------------------------------|------------------------------------------------------------|  
|Optimized for scholarly communication considerations                          |May not support versioning or frequent changes to dataset |
|Moderately open user community; datasets can likely be deposited by users with many different affiliations |

### Institutional Repository
|pros                                                                          |cons                                                        | 
|------------------------------------------------------------------------------|------------------------------------------------------------|  
|Optimized for scholarly communication considerations                          |May not be optimized for datasets |
|Often managed by libraries                                                    |Restricted depositor community; e.g., may be limited to depositors with institutional affiliation   |
|Strongly retains institutional brand |optimized for code rather than data     |May not handle versioning or frequent changes to dataset |



