.. _ontobrapi:

Submitting Metadata in PHENO
============================

| This example based section will showcase how to submit your **MIAPPE** compliant Excel file in **PHENO**.
| If you don't have this file ready, start with the :ref:`Fill a MIAPPE Template<miappe_template>` tutorial.

Go to the OntoBrAPI Submission page
-----------------------------------

1. Click on **Submit Data**.

.. figure:: /images/submit_arrow.png
   :scale: 8%
   :alt: Submit data

| This will take you to the **OntoBrAPI** submission tool.

.. figure:: /images/ontobrapiv2.png
   :scale: 50%
   :alt: OntoBrAPI submission tool

| Each of the following examples will showcase possible outcomes when trying to submit your file in `PHENO <https://brapi.biodata.pt/>`_.

Example 1 - Valid File
----------------------

| In the first example, the user has a simple **MIAPPE** compliant excel file:

| 📁 `OntoBrAPI Example File 1 (Valid) <https://github.com/forestbiotech-lab/ontobrapi-web/raw/master/public/assets/Miappe_compliant_Excel.xlsx>`_

To submit your metadata:

1. Click on **upload file**, and select your file of choice ➡️ for this example, choose the ``Miappe_compliant_Excel.xlsx``

.. figure:: /images/OntoBrAPI.png
   :scale: 50%
   :align: center
   :target: https://brapi.biodata.pt/submit

|
| A preliminary validation report will appear in the top right corner.
| After a sucessfull validation check, the following prompt will appear:

.. figure:: /images/OntoBrapi_validationsucess.png
   :scale: 26%

| Alongside the Mapping Section and a preview of the uploaded file:

.. figure:: /images/OntoBrapi_uploadsucess.png
   :scale: 50%

2. After validation, the file needs to be mapped to the Plant Ontology. Click on **Load Mapping**

| This will open a list of Predefined Mapping Templates.

3. Select the ``[JSON] MIAPPEV1.1`` option

| Since our input file is a standard MIAPPE file, this will automaticaly conclude the mapping.
| The mapping success is seen on the color and number in the file sheet names, like shown bellow:

.. figure:: /images/OntoBrapi_uploadsucess.png
   :scale: 50%

4. Lastly, click **Run**
   
| That's it! Your metadata was sucessfuly submitted in PHENO.
| The submitted dataset will be private, and only made public:

* Until the **Public release date** specified in the **Investigation sheet** is reached;
* After approval by a **PHENO curator**.

| Once the dataset is made public, all phenotypic data associated with your submitted metadata will be readily accessible in BrAPI compliant databases, such as the case of PHENO and `FAIDARE <https://urgi.versailles.inra.fr/faidare/>`_.

Example 2 - Invalid File
------------------------

| The second example will showcase working with an invalid input file:

| 📁 `OntoBrAPI Example File 2 (Invalid) <https://github.com/forestbiotech-lab/ontobrapi-web/raw/master/public/assets/Miappe_INCOMPLIANT_Excel.xlsx>`_

| Let's try and submit this file and try to identify and fix eventual errors during submission.

1. Click Input File and select the ``Miappe_INCOMPLIANT_Excel.xlsx``

As we can see, the loading failed due to an input file validation error.

.. figure:: /images/OntoBrapi_validationsucess.png
   :scale: 26%

| By clicking in the *FAILED* button within the validation report menu, a drop-down of messages indicate a "CHECK FAILED - Invalid Input File Sheet Names" entry.
| This means that one or more sheets in the Excel file are missing or have different names from the ones described in the MIAPPE standards.
| Let's take a closer look to the invalid file sheet names:

.. figure:: /images/OntoBrapi_invalidsheets.png
   :scale: 50%

* The Person sheet name is not in English. Fix → "Pessoa" to **Person**.
* The Data file sheet name is incomplete. Fix → "Data" to **Data file**.
* | In addition, the Environment sheet is missing. FIX → create a new sheet called **Environment**,
  | and write **Study unique ID\***, **Environment parameter\*** and **Environment parameter value\*** in the first row

.. figure:: /images/OntoBrapi_fixedsheets.png
   :scale: 26%

| After fixing these problems, retry file submission:

2. Click Input File and select the fixed *``Miappe_INCOMPLIANT_Excel.xlsx``*

| Once again, upload fails. By looking at the validation report, we see a "CHECK FAILED - Invalid Investigation Sheet Names".
| In this case, by looking at the file, we see that the first two column headers within the Investigation sheet are incorrect.

* FIX → The column name "Investigation ID" should be **Investigation unique ID\***
* FIX → The column name "investigation title" should be **Investigation title\***.

.. note::

   If you use the provided MIAPPE template, errors of this nature will be prevented.

| For this last example, we will supply a valid Excel file, but use an incorrect mapping file (Invalid_Mapping_example.json).

Example 3 - Invalid Mapping
---------------------------

1. Click Input File and select the *Miappe_compliant_Excel_file.xlsx*
2. Click the **Load Mapping** option, and select the - *Invalid_Mapping_example.json*
3. Press Submit

As we can check by the warning, the supplied mapping was insufficient to properly connect the supplied Miappe metadata.
