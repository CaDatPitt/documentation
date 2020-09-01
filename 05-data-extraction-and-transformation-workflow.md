---
layout: default
title: Data Extraction and Transformation Workflow
nav_order: 5
---
#### [Home](http://cadatpitt.github.io)
# Data Extraction and Transformation Workflow

Creating base layers has two steps: obtaining the source data in the necessary formats, and then running a data extraction and transformation
process to create the base layer.

If the collections data you want to work with is maintained by Pitt's library and archives, this process can be done completely or in part
by a request to the CaD@Pitt team. If you are working with your own collections data, or wish to customize the transformation process, you
can do the transformation yourself.  We describe the steps to run the data extraction and transformation scripts developed by the CaD@Pitt project below.

## Requesting data from CaD@Pitt
1. User submits a [Source Data Request](https://forms.gle/BgF3vsBHpXCCdNve7).
1. CaD team member confirms request with user.
1. CaD team member downloads source data from digital repository and/or catalog.
1. CaD team member uploads source data to a “source-data” directory in the CaD@Pitt GitHub repository
1. CaD team member processes source data with extract/transform script(s) to output CSV and YAML files to the "base-layers" directory in the CaD@Pitt GitHub repository
1. CaD team member notifies requesting user that source data is available, if user will be creating base layers.

## Creating your own base layer
### **Obtain a copy of the CaD@Pitt Data Layers Repository**
Download or clone (optionally, after forking) the CaD@Pitt Data Layers Repository. For instructions, see [Using the Repository: Cloning the Repository](/documentation/03-using-the-repository.html#download-or-clone-the-repository).

### **Obtain the source data**
All source data should be placed within a standardized structure in the repository directories.

Within the source-data directory, create a subdirectory for each separate collection. The best practice is to create the name as all lowercase,
with no spaces (you can use dashes or underscores instead of spaces).

Within the collection subdirectory, create additional subdirectories as appropriate to your content data:
- `dc` - for simple (unqualified) Dublin Core records in XML, one file per record
- `ead` - for Encoded Archival Description records, in XML, one file per collection
- `marcxml` - for MARC records, in MARCXML format, one file per record
- `mods` - for MODS records, in XML, one file per record
- `ocr` - for Optical Character Recognition output associated with collection items

After this is done, you should have a directory structure that looks like this:
`data-layers/source-data/american-left-ephemera/mods`

### **Configure your python environment**
The CaD@Pitt data extraction and transformation scripts are written in Python, specifically for Python 3. If needed, obtain and install Python 3.x on your computer.
There are several ways to obtain Python, and you may already have it installed on your computer without realizing. For more detailed information tailored to your
specific operating system, see the official Python 3 [documentation on Installation and Usage](https://docs.python.org/3/using/index.html).

Once Python is installed, you will also need to ensure that some supporting Python modules used by the CaD@Pitt scripts are installed. Use `requirements.txt` to install needed modules. If you are new (or need a refresher) to installing python modules or using pip and requirements.txt, we recommend consulting the [Installing Packages documentation](https://packaging.python.org/tutorials/installing-packages/) from the Packaging Python User Guide.

### **The transformation scripts**
The main script for running the data extraction and transformation is `extract_base_layer.py`. This script also draws on configuration information stored in
`data_layers_config.py`. That configuration information includes data structures that map fields in the source XML documents to output fields in the tabular
base layer data.

### **Running the script**
When the setup processes described above are complete, you should be ready to run the script on some collections data. The command to run the script is

`python extract_base_layer.py [source collection name] [collection type] [collection sub-type]`

where collection type is one of `archival`, `serial`, `monograph`, and collection sub-type is one of `digital` or `print`.

Specifying the collection type and sub-type will allow the script to look for the appropriate kind of source data in its expected locations, and run the
transformations appropriate to those types of data.

### **Output**
Output from the transformation process is written to the `base-layers/*collection-name*` directory. The collection subdirectory will be created if it does not
already exist. Within that location, the process creates two output files, one each for data at the item and collection level. Both files are encoded as UTF-8 comma-separated value (CSV) files. They are named `item-base-layer.csv` and `collection-base-layer.csv`. If the source data contains no collection-level information (as from an EAD file), the collection base layer file will be empty.
