.. _tutorial:

Getting started with OntoBrAPI
==============================

| This section will showcase how to submit your **MIAPPE** compliant Excel file in OntoBrAPI.
| If you don't have this file ready, start by downloading and filling this `MIAPPE template <https://github.com/MIAPPE/MIAPPE/tree/master/MIAPPE_Checklist-Data-Model-v1.1/MIAPPE_templates>`_.

Example based Tutorials
=======================

| The following tutorials will showcase possible outcomes when using OntoBrAPI.
| In the first example, the user has a simple **MIAPPE** compliant excel file:

| 📁 `OntoBrAPI Example Files 1 <https://docs.google.com/spreadsheets/d/1_m-XS7KS-xt76Rl8rvzvCmrwdpqH5oIp/edit#gid=615880277>`_

| The second example will showcase working with an invalid input file:

| 📁 `OntoBrAPI Example Files 2 <https://docs.google.com/spreadsheets/d/10bELWxuROGh1JAyxlkG_qIFgNn505wII/edit#gid=615880277>`_

Example 1 - Valid File
----------------------

We will start with a MIAPPE compliant Excel file:

1. Open **OntoBrAPI**
2. Click **Input file** and select → ``Miappe_compliant_Excel.xlsx``

| After a sucessfull validation check, the following prompt will appear:

.. figure:: /images/OntoBrapi_validationsucess.png
   :scale: 26%

| Alongside the Mapping Section and a preview of the uploaded file:

.. figure:: /images/OntoBrapi_uploadsucess.png
   :scale: 50%

3. Click **Load Mapping**

| This will open a list of Predefined Mapping Templates list.

4. Select the → ``Example_mapping.json``

| This will automaticaly conclude the mapping of our input (all sheet names turn green).

4. Lastly, click **Run**
   
| That's it! Your data and respective metadata is now readily accessible in databases using BrAPI, such as the case of `FAIDARE <https://urgi.versailles.inra.fr/faidare/>`_.

Example 2 - Invalid File
------------------------

Now, let's submit a invalid input file to identify errors and try to fix them.

1. Click Input File and select the *``Miappe_INCOMPLIANT_Excel.xlsx``*

As we can see, the loading failed due to a input file validation error.

.. figure:: /images/OntoBrapi_validationsucess.png
   :scale: 26%

| By clicking in the *FAILED* button, a drop-down of messages shows a "CHECK FAILED - Invalid Input File Sheet Names" entry.
| This means that one or more sheets in your Excel file are different from the MIAPPE standards.
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

|
| For this last example, we will supply a valid Excel file, but use an incorrect mapping file (Invalid_Mapping_example.json).

Example 3 - Invalid Mapping
---------------------------

1. Click Input File and select the *Miappe_compliant_Excel_file.xlsx*
2. Click the **Load Mapping** option, and select the - *Invalid_Mapping_example.json*
3. Press Submit

As we can check by the warning, the supplied mapping was insufficient to properly connect the supplied Miappe metadata.



