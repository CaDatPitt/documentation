# Getting Started
This document outlines and describes how cultural heritage institutions (e.g., libraries, archives, museums) might implement a collections as data project based on the data layers model. If you’re not familiar with the conceptual model of “data layers” or the overall CaD@Pitt project, please read our Principles and Objectives. This implementation model covers the following phases and steps:

I. [Preparing for implementation](#preparing-for-immplementation)
  01. [Form your team](#form-your-team)
  02. [Write project charter](#write-project-charter)
  03. [Set up project infrastructure](#set-up-project-infrastructure)
  04. [Evaluate existing collections data](#evaluate-existing-collections-data)
  05. [Further steps and considerations](#further-steps-and-considerations)
  
II. [Implementing your project](#implementing-your-project)
  01. [Develop data layers](#develop-data-layers)
  02. [Build repository](#build-repository)
  03. [Establish use model](#establish-use-model)
  04. [Prepare for instruction](#prepare-for-instruction)
  05. [Further steps and considerations](#further-steps-and-considerations)

## Preparing for implementation
### Form your team
A data layers-based project requires a number of different skills. It’s most likely that getting these skills together will require forming a team and that this team may comprise people who work in different units of your organization (or even outside of your organization). 

Specifically, consider who might be able to contribute the following:
- Engagement with researchers and knowledge of their relevant needs and interests
- Curatorial knowledge of your local library/archival collections, including the degree to which collections have been described
- Technical knowledge of and access to local library/repository system(s), including the ability to search and export records in bulk from systems' interfaces
- Expertise in collection metadata, including knowledge of local metadata creation and/or cataloging practices
- Facility with GitHub, including creating and administering repositories/organizations, writing to and cloning repositories, and downloading/running code.
- Facility with Python, including scripting with libraries like pandas, NumPy, Beautiful Soup, lxml, and Pymarc.
- Facility with tabular data (especially CSV format), including loading into and manipulating with common desktop applications
- Instructional expertise, particularly at the intersection of collections-based research and digital- and data-centered methods
- Project management, to help coordinate all of the roles described above

Although that may seem like a lot of different roles, it's possible to successfully implement a data layers-based project with a small team in which roles are shared or individuals wear several hats as needed. However, this work is also an excellent opportunity to work collaboratively across traditional organizational boundaries, so we recommend striving to include appropriate colleagues from your organization to the greatest degree possible.

### Write project charter
Once a project team has been formed, it’s beneficial (and highly recommended) to gather team members and stakeholders to develop a project charter together. The charter establishes the nature of the project, including its scope, objectives, assumptions and constraints, deliverables, tasks, timeline, participants, audiences, budget, protocols, and more. The project team and participating stakeholders should agree upon the expectations and commitments of the charter. This document can be preliminary and may change throughout the implementation process. It does not have to be formal unless a funder or administrator requires a formal document.

### Set up project infrastructure
You may very well have your own project management tools and preferences, but we have found that this kind of project benefits from these components of project infrastructure, at minimum:
- Project team communications tool (e.g., email list, Slack, Microsoft Teams)
- Project management tool (e.g., Trello, Asana, Monday, Microsoft Project)
- An access-controlled platform to store and share internal project documentation and data (e.g., Dropbox, Box, Google Drive, another private repository)
- A public-facing web site or repository (e.g., GitHub) to share data layers and user documentation
- For those working on transforming data layers using the project's Python scripts, an up-to-date local Python processing environment, and a cloned copy of the [CaD@Pitt Data Layers](https://github.com/CaDatPitt/data-layers) GitHub repository

### Evaluate existing collections data
With a team in place, the next step is to evaluate your institution's existing collections data and consider what data will be available to you. Drawing from the expertise on your team, you can collaboratively identify:
- What collections may be of interest for data layers-based inquiry?
- What existing metadata is available?
- What systems store that metadata, and how can it be exported?
- What data types (e.g., text, image, geospatial, audio, video), formats (e.g., XML, HTML, PDF, plain text, CSV, JPG, TIFF, WAVE, Shapefile, MPEG-4), standards (e.g., AACR2, RDA, MARC, Dublin Core, MODS), and vocabularies/encoding schemes are in use (e.g., Art & Architecture Thesaurus, Library of Congress Name Authority File, ISO 8601)?
- What local practices or gaps around collection description might be important to know?
- What obstacles or roadblocks might need to be resolved before work with collections data can begin?

This is not a one-time process, and identifying collections of interest may (or should!) be influenced by direct conversations with researchers who use your collections. However, getting a basic lay of the land, including anticipating collections data challenges, will help your project get off to a productive start.

### Further steps and considerations
There are a several other steps and considerations that your team may pursue during the preparation phase:
- Create user personas to articulate various cohorts of your audiences and promote user- centered design. Conducting interviews with representatives of each cohort is recommended.
- Conduct programmatic/computational analysis of your metadata to better understand the nature of your metadata. 

## Implementing your project
### Develop data layers
After evaluating the existing collections data, you can begin developing the data layers for your project:
- Determine the metadata elements for the base layer(s). [See the[CaD@Pitt Data Dictionary Introduction](https://github.com/CaDatPitt/data-layers/wiki/1.-Introduction) for details about how we developed our base layers.]
  - Of the collections metadata that is available, what is well-suited for computation?
  - In addition to metadata elements that are required to identify items (e.g., identifier, title, date, publisher), what are elements that are well-suited for research inquiry? 
  - If you have received requests from scholars seeking to work with collections data, what data have they been or might they be interested in?
  - Will you need one or more base layers/metadata element sets for your collections, depending on the variation in collection type (e.g., archival, special/distinctive, library catalog), item type (e.g., text, image, audio, video), metadata (e.g., quality, granularity, standards), or some other factor?
  - How can the collections metadata in its existing form be translated to be readable for your users?
- Identify what type of source data files are required to harvest the metadata for the base layers, and determine whether source data for all or only particular collection items will be added to the repository. 
  - Note: At this time, only some of the Pitt Library’s collections items are represented in the CaD@Pitt repository. More are being added based on need and interest.
- Export/download identified collections source data from local library/repository system(s). These will be uploaded to the repository later.
- Determine how the metadata in the source data files will map to your base layer element set and how the CaD@Pitt transformation script will need to be modified accordingly.
- Create documentation for your data layers. [See the [CaD@Pitt Data Dictionary](https://github.com/CaDatPitt/data-layers/wiki) for a model.]

### Build repository
The repository for your project not only provides access to your data layers but also enables the production of your base layers. These instructions assume that a GitHub repository is being used as the public-facing repository:
- Create and organize your project’s GitHub organization and/or repository (or repositories).
  - The CaD@Pitt project’s GitHub organization has multiple repositories, for data layers, the project website, project documentation, etc. Your project may also require several repositories or only a single repository for data layers.
- Clone the CaD@Pitt Data Layers repository.
- Upload identified collections source data to GitHub repository.
- Modify the CaD@ Pitt transformation script according to mappings from your source data to base layers. Make sure to document your code.
- Extract and transform source data into base layer(s), using modified transformation script.

### Establish use model
It is important to establish how your users will use your collections as data repository and how you will enable such use. 
- Identify various use cases for your repository and how your team will support them.
  - Will users simply be given access to download data layers? Will they be able to process/create data layers? Will they be able to contribute/publish data layers?
- Determine what services you will offer to support use of collections as data in the repository.
- Identify what human resources are necessary to provide services (positions, specific duties) and fill these roles. 
- Identify and prepare material resources/tools needed for services and usage of collections as data (e.g., Google Forms for submitting data or requests, Google Sheets for editing data layer spreadsheets).
- Develop and publish documentation to enable use of and contribution to the repository. The documentation may include usage documentation, data documentation (e.g., data dictionary, README, codebook), and workflows (e.g., for requesting data or assistance, contributing to the repository). [See the CaD@Pitt [project documentation](https://cadatpitt.github.io/documentation/) for an example.]

### Prepare for instruction
- If your project will involve data layers-based instruction, there are a few things you’ll need to do to prepare.
  - Determine the instructional opportunities and goals you will pursue in your project. 
  - Who is the audience? A class of undergraduate or graduate students? Individual researchers or a group of researchers? A group of participants from your community? Other staff members in your organization?
  - What are your objectives or learning outcomes? 
  - What will be the venue for instruction? Class sessions? Training sessions? An event?
- Establish partnerships with instructors, if you’re collaborating to implement modules in a class. You may find it useful to develop a preliminary module or set of modules to present to potential instructors as an example; or, you may share previously implemented modules.
- Develop lesson plans for your instructional modules, including objectives or learning goals/outcomes, instructional content and methods, activities and assignments, and assessment methods. We suggest creating an itinerary to outline/timeline the sequence of events that make up the lesson(s). [See the CaD@Pitt[instructional modules]() as a model.]
- Identify and prepare the tools and materials needed to implement the module(s).

As you implement these modules in your various instructional contexts, we suggest documenting and assessing these cases and refining your modules as needed.

### Further steps and considerations
There are a several other steps and considerations that your team may pursue during the implementation phase:
- Generate your own extension layers to increase the visibility and discoverability of your institution’s collections; you may use these layers to generate data visualizations for your collections, learn more about the contents of and connections between your collections, and enable targeted marketing for your collections. 
- Develop workflows for incorporating enrichments from extension layers back into your institution’s catalog and/or repository.
- Develop a sustainability plan for the repository and/or related services.
- Develop a dynamic database interface to facilitate exploration and discovery of data layers (features might include browsing, searching, filtering, faceting, visualizations, etc.).
- Develop a workbench interface for processing, visualizing, and/or analyzing data layers.
