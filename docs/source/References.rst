.. _references:

FAIR Principles
===============

| The `FAIR principles <https://fair-software.eu/about/>`_ are a concept originated in data management, aiming to make data Findable, Accessible, Interoperable and Reusable.
| They serve as a flagship for promoting good data management practices, and are a key concept in the `Open Science <https://www.fosteropenscience.eu/fair-data>`_ movement.
|
| **PHENO** incorporates the **FAIR principles** in the sense that:
| * Data is stored in a secure, open and accessible repository with version control.
| * Enables data findability and reusability through descriptive metadata of phenotypic experiments using `MIAPPE <https://www.miappe.org/>`_.
| * It is interoplable with other data repositories through the use of the `Breeding API (BRAPI) <https://brapi.org/>`_.

MIAPPE
------

| `MIAPPE <https://www.miappe.org/>`_ is a open, community driven, data standard designed to harmonize data from plant phenotyping experiments.
| It provides templates in the form of excel spreadsheets, with metadata checklists that can be filled by researchers to adequately describe plant phenotyping experiments.
| The current development version of MIAPPE v1.2 is under review by its community, and templates for this version can be found in `MIAPPE templates repository <https://github.com/MIAPPE/MIAPPE/tree/master/Templates>`_.
| More details about MIAPPE can be found in the `MIAPPE Github page <https://github.com/MIAPPE/MIAPPE>`_.

* Download the MIAPPE v1.1 template `here (v1.1) <https://github.com/MIAPPE/MIAPPE/tree/master/MIAPPE_Checklist-Data-Model-v1.1/MIAPPE_templates>`_.
* Download the more recent MIAPPE v1.2 template `here (v1.2) <https://github.com/MIAPPE/MIAPPE/raw/refs/heads/master/Templates/MIAPPE_Spreadsheet_Template.xlsx>`_.
* Download an example of a filled Miappe compliant Excel file `here (filled, v1.1) <https://github.com/forestbiotech-lab/ontobrapi-web/raw/7cde0e0374f19e2f5664c4d873494a3475f77c7d/reference_files/MIAPPE_v1.1_TRACE-RICE.xlsx>`_.

BRAPI
-----

| The `Breeding API (BRAPI) <https://brapi.org/>`_ is a standard developed and widely adopted by the plant breeding community to facilitate data exchange between different systems.
| As a standardized RESTful web service API, BrAPI enables interoperability among agricultural databases and tools.
| You can learn more about BrAPI through their `website <https://brapi.org/>`_, `documentation <https://plant-breeding-api.readthedocs.io/en/latest/>`_ and `GitHub page <https://github.com/plantbreeding/BrAPI>`_.

FAIDARE
-------

| `FAIDARE <https://urgi.versailles.inra.fr/faidare/>`_ is a specialized search engine for agronomic data, which includes plant phenotypic data.
| Through the search box and with help of various filters, users can search data stored in any data repository that is BRAPI compliant, such as the case with **PHENO**.
| For example, the user can specify the species, data type (e.g., Phenotyping Study), and a specific database (e.g., `Ensembl Plants <https://plants.ensembl.org/index.html>`_) to perform a custom query.

.. figure:: /images/faidare.png
   :scale: 50%
   :align: center
   :alt: FAIDARE search engine
   :target: https://urgi.versailles.inra.fr/faidare/
   :class: img-margin-1

   The FAIDARE search engine, showing the search box and filters for data search.

-------------------------------------------------------------------------------------------------------------------------------

PHENO is a open software development project under the `Apache-2.0 license <https://github.com/forestbiotech-lab/PHENO?tab=Apache-2.0-1-ov-file#readme>`_.
