.. _tutorial:

Getting started with OntoBrAPI
==============================

| This section will showcase how to submit your MIAPPE compliant Excel file in OntoBrAPI.
| Brief explanation/motivation here

Example based Tutorial
======================

| Follow along this tutorial with the given example files to get familiar with OntoBrAPI:

| 📁 `OntoBrAPI Example Files <https://drive.google.com/drive/folders/1AceOedJPjrAk3SmkuLnw9GdqDE6y4fMo?usp=sharing>`_

Example 1 - Valid File
----------------------

We will start with a MIAPPE compliant Excel file:

1. Open **OntoBrAPI**
2. Click **Input file** and select → ``Miappe_compliant_Excel.xlsx``
3. In Templates, select the Predefined Mapping File → ``Example_mapping.json``
4. Click **Run**

| The following prompt will appear:
| Put here submitted sucessfully message prompt here (to potentialy add in OntoBrAPI)
| That's it! Your data and respective metadata is now readily accessible in databases using BrAPI, such as the case of `FAIDARE <https://urgi.versailles.inra.fr/faidare/>`_.

Example 2 - Invalid File
------------------------

Now, let's submit a invalid input file to identify errors and fix them.

1. Click Input File and select the *Faulty_Miappe_Excel_file.xlsx*
2. Select the Predefined Mapping File - *Example_mapping.json*
3. Press Submit

As we can see, the loading failed due to a input file validation error.
By looking at the *OntoBrAPI_Validator.logs* file, we can see a "CHECK FAILED - Invalid Input File Sheet Names" message.
This means that one or more sheets in your Excel file differs from the MIAPPE standards.
Let's take a closer look to the invalid file:

.. figure:: /images/prov.png
   :alt: Provisory image
   :scale: 70%

   *Place a screenshot here of an invalid file where you can clearly see the sheet names*

As shown, the Investigation sheet is misspeled as invesgation (this validation is also case-sensitive, so make sure that the sheet names are identical to the valid excel example).
After fixing this problem, we retry the submission.

Once again, the submission failed. By looking at the new .logs file, we can see a "CHECK FAILED - Invalid Investigation Sheet Names".
In this case, we learn that one or more columns within the Investigation sheet of our Excel file are incorrect.
In this case, we see this and that. After fixing this, the file is now valid for submission!

For this last example, we will supply a valid Excel file but an incorrect mapping file (Invalid_Mapping_example.json)

Example 3 - Invalid Mapping
---------------------------

1. Click Input File and select the *Miappe_compliant_Excel_file.xlsx*
2. Click the **Load Mapping** option, and select the - *Invalid_Mapping_example.json*
3. Press Submit

As we can check by the warning, the supplied mapping was insufficient to properly connect the supplied Miappe metadata.



