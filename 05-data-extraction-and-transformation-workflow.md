---
layout: default
title: Data Extraction and Transformation Workflow
nav_order: 5
---

<html lang="en">
  <head>
    <meta charset="utf-8">

    <!-- Font Awesome Icons css -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

  </head>
</html>

#### [Home](http://cadatpitt.github.io)
# Data Extraction and Transformation Workflow

Creating base layers has two steps: obtaining the source data in the necessary formats, and then running a data extraction and transformation process to create the base layer.

If the collections data you want to work with is maintained by Pitt's library and archives, this process can be done completely or in part by a request to the CaD@Pitt team. If you are working with your own collections data, or wish to customize the transformation process, you can do the transformation yourself. We describe the steps to run the data extraction and transformation scripts developed by the CaD@Pitt project below.

## Requesting data from CaD@Pitt
1. User submits a {::nomarkdown}<a href="https://forms.gle/BgF3vsBHpXCCdNve7" target="_blank">Source Data Request <font size="-1"><i class="fa fa-external-link"></i></font></a>{:/}.
2. CaD team member confirms request with user.
3. CaD team member downloads source data from ULS's digital repository and/or catalog.
4. CaD team member uploads source data to a “source-data” directory in the CaD@Pitt Data Layers Repository.
5. If requested by user, CaD team member processes source data with extraction/transformation script to output CSV files to the "base-layers" directory in the CaD@Pitt Data Layers Repository.
6. CaD team member notifies requesting user that source data (and base layers) are available.

## Creating your own base layer
### **Obtain a copy of the CaD@Pitt Data Layers Repository**
Download or clone (optionally, after forking) the CaD@Pitt Data Layers Repository. For instructions, see [Using the Repository: Cloning the Repository](03-using-the-repository.html#download-or-clone-the-repository).

If you would rather not download or clone the entire repository, you can download the necessary source data and Python files (listed in the directory tree under "transformation-scripts") to the run the script. All files should be placed within a standardized structure in the repository directories, as shown below:

 `[data-layers](https://github.com/CaDatPitt/data-layers)
  |__ [base-layers](https://github.com/CaDatPitt/data-layers/tree/master/base-layers)
  |__ [source-data](https://github.com/CaDatPitt/data-layers/tree/master/source-data)
  |   |__ [collection-directory]
  |       |__ ead
  |       |   |__ [*.xml files]
  |       |__ mods
  |       |   |__ [*.xml files]
  |       |__ rels-ext
  |           |__ [*.xml or .*rdf files]
  |__ [transformation-scripts](https://github.com/CaDatPitt/data-layers/tree/master/transformation-scripts)
      |__ data_layers_config.py
      |__ encoding_schemes.py
      |__ extract_base_layer.py
      |__ requirements.txt`

Within the 'source-data' directory, create a subdirectory for each separate collection. The best practice is to create the name as all lowercase, with no spaces (you can use dashes or underscores instead of spaces).

Within the collection directory, create additional subdirectories as appropriate to your content data:
- `ead` — for EAD (Encoded Archival Description) records, in XML, one file per collection (only available for archival items in the ULS Digital Collection, or similar)
- `mods` — for MODS (Metadata Object Description Schema) records, in XML, one file per record
- `rels-ext` — for RDF (Resource Description Framework) records, in XML or RDF, one file per record (only available for archival items in the ULS Digital Collection, or similar)
There are other types of metadata records available, such as Dublin Core, but the script only supports EAD, MODS, and RELS-EXT. For more information about all the available types of (meta)data, see the [Source Data](data-dictionary/introduction.md#source-data) section of the CaD@Pitt Data Dictionary Introduction.

After this is done, you should have a directory structure that looks like this:
`data-layers/source-data/american-left-ephemera/mods`

### **Configure your python environment**
The CaD@Pitt data extraction and transformation scripts are written in Python, specifically for Python 3. If needed, obtain and install Python 3.x on your computer. There are several ways to obtain Python, and you may already have it installed on your computer without realizing. For more detailed information tailored to your specific operating system, see the official Python 3 [Setup and Usage](https://docs.python.org/3/using/index.html) documentation.

Once Python is installed, you will also need to ensure that some supporting Python modules used by the CaD@Pitt scripts are installed. Use `requirements.txt` to install the necessary packages and libraries. If you are new (or need a refresher) to installing Python modules or using pip, we recommend consulting the [Installing Packages](https://packaging.python.org/tutorials/installing-packages/) documentation from the Packaging Python User Guide. As a quick reference, you can install required modules by running the following command in the Command Prompt/Terminal:
`pip install -r requirements.txt`.

### **The transformation scripts**
The transformation scripts can be found in the transformation-scripts directory. The main script for running the data extraction and transformation is `extract_base_layer.py`. This script also draws on configuration information stored in `data_layers_config.py` and `encoding_schemes.py`. That configuration information includes data structures that map fields in the source XML documents to output fields in the tabular base layer data.

### **Running the script**
When the setup processes described above are complete, you should be ready to run the script on some collections data. In the Command Prompt/Terminal, navigate to the "transformation-scripts" directory and run the following command, replacing the bracketed text with the correct information:

`python extract_base_layer.py [location] [collection_type] [collection_subtype]`

The `location` value is the name of a directory in the 'source-data' directory that contains the source data for your collection. The `collection_type` and `collection_subtype` values, listed in the table below, specify which [metadata element set](data-dictionary/introduction.md#metadata-element-sets) (archival, serial, monograph, mixed) and which type(s) of source data should be used to create the base layers.

|collection types|collection sub-types|
|---|---|
|**archival**|{::nomarkdown}<ul><li>digital</li><li>physical</li></ul>{:/}|
|**monograph**|{::nomarkdown}<ul><li>catalog</li><li>digital</li><li>mixed</li></ul>{:/}|
|**serial**|{::nomarkdown}<ul><li>catalog</li><li>digital</li><li>mixed</li></ul>{:/}|
|**mixed**|{::nomarkdown}<ul><li>catalog</li><li>digital</li><li>mixed</li></ul>{:/}|

For example, your command should look something like this:

`python extract_base_layer.py american-left-ephemera archival digital`

If you need help or a handy reference to run the script, you can call up the help menu by running the following command:

`python extract_base_layer.py --help` or `python extract_base_layer.py -h`

### **Output**
Output from the transformation process is written to the `base-layers/[collection-name]` directory. The collection subdirectory will be created if it does not already exist. Within that location, the process creates two output files, one each for data at the item and collection level. Both files are encoded as UTF-8 comma-separated value (CSV) files. They collection-level output file will include the name of collection subdirectory in the "source-data" directory followed by the suffix "_collection-base-layer.csv", such as "american-left-ephemera_collection-base-layer.csv". The name of the item-level file will include the collection subdirectory, and the suffix will depend on the specified collection type and subtype, such as `american-left-ephemera_item-base-layer_archival-digital.csv`. If the source data contains no collection-level metadata (i.e., an EAD file), the collection base layer file will be empty. <!--This information can be added manually.-->
