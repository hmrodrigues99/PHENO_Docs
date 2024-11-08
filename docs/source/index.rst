Welcome to PHENO's documentation!
=================================

.. toctree::
   :maxdepth: 4
   :hidden:
   :caption: 🚀 Getting Started

   Getting Started

.. toctree::
   :maxdepth: 4
   :hidden:
   :caption: 📂 OntoBrAPI

   PHENO Submission
   Validator
   Mapping

.. toctree::
   :maxdepth: 4
   :hidden:
   :caption: 💡 Guides

   Dataverse
   MIAPPE Template

.. toctree::
   :maxdepth: 4
   :hidden:
   :caption: 📚 References

   References

| `PHENO <https://brapi.biodata.pt/>`_ is a data portal for the submission, storage and sharing of metadata for plant phenotypic experiments.
| If you're looking for a comprehensive guide of both `PHENO <https://brapi.biodata.pt/>`_ and the `OntoBrAPI <https://brapi.biodata.pt/submit>`_ platform, then you've come to the right place.

.. admonition:: In a Nutshell, **PHENO**:

   1. Receives as input a MIAPPE compliant Excel file
   2. Validates it according to the MIAPPE specifications
   3. Makes your metadata and associated phenotypic data FAIRly available worldwide through BrAPI compatible search engines

Make your data FAIR using PHENO
-------------------------------

| **FAIR** data is increasingly more valued in research, with new projects tending to follow **FAIR** guidelines when working with their data.
| **PHENO** aims to increase data FAIRness by making plant phenotypic data searchable and readily accessible by specialized databases, such as `FAIDARE <https://urgi.versailles.inra.fr/faidare/>`_.
| This is achieved by making your data compatible with the **Breeding API (BrAPI)**.

Getting Started
---------------

| To submit metadata in **PHENO**, users are required beforehand to deposit the actual phenotypic data (e.g., tables, images) in another data holder of choice, for example:

1. Dataverse*
2. Google Drive / Microsoft OneDrive
3. Other specialized data repositories

| \*Dataverse is a database for agnostic scientific data. For portuguese users, learn here on :ref:`how to submit your data in DMPortal<dataverse>`, the portuguese instance of Dataverse.
|
| To use PHENO for the first time, please check the :ref:`Getting started with PHENO <start>` section.
| To get acquainted with the **FAIR** and **MIAPPE standards**, and terms such as **BrAPI** or **FAIDARE**, feel free to check the :ref:`References <references>` section.
| If you require additional assistance, feel free to contact us directly (hm.rodrigues@itqb.unl.pt).

PHENO in Detail
---------------

.. figure:: /images/PHENO_structure.jpg
   :scale: 100%
   :align: center
   :alt: PHENO structure overview

   PHENO structure overview

| **PHENO** ensures data FAIRness by integrating 3 main modules based on international standards:

1. Data submission (MIAPPE)
2. Data storage (RDF)
3. Data sharing (BrAPI)

| 1) In data submission, a Graphical User Interface (GUI) allows the conversion of MIAPPE compliant spreadsheets into n-triples format.
|     The GUI allows users to dynamically map the MIAPPE spreadsheet to the appropriate `Plant Phenotype Experiment Ontology (PPEO) <https://d2kab.agroportal.lirmm.fr/ontologies/PPEO>`_
|     in Javascript Object Notation (JSON). The user can use a predefined MIAPPE - PPEO mapping template available, or adjust any fields as
|     deemed necessary. The GUI uses the constraints of the ontology to validate the mapping.
|
| 2) PHENO relies on `OpenLink Virtuoso <https://docs.openlinksw.com/virtuoso/>`_ to store the metadata in triples and create a database
|     management system for data curators to validate datasets and select which ones are ready for sharing.
|
| 3) PHENO serves as a BrAPI endpoint where the data stored is made available in JSON to BrAPI calls, in accordance with the `BrAPI specifications <https://brapi.org/specification>`_.
|
| To submit medata in PHENO, check the :ref:`Submitting Metadata in PHENO<ontobrapi>` section.
| To learn how to browse PHENO for a specific project \(meta\)data, check the :ref:`Getting started with PHENO <start>` section.