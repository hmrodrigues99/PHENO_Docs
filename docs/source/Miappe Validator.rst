.. _miappe_validator:

Input File Format
=================

OntoBrAPI checks for the extension of your input file. The following lists all currently accepted file extensions:

* .xls
* .xlsx
* .ods

.. warning::

   | If your file has a different extension than the ones described above, your file will fail to upload ("Invalid extension" error message).
   | To try and fix this error, open your excel file and click *File*, *Save as*, *Save as type*: **Excel Workbook** (.xlsx).

OntoBrAPI's validator checks if the input file has all the minimum required sheets present, which are:

* Investigation
* Study
* Person
* Data file
* Biological Material
* Sample
* Observation Unit
* Observed Variable
* Environment
* Factor
* Event

Additional sheets can be present, but will require a custom mapping template or manual mapping.

.. note::

    Even if a mandatory sheet is left empty, it must still be present in the uploaded file.

| The validator also performs additional checks in specific columns, to see if they are filled correctly. This includes:

1. Mandatory columns (indicated with a * in the column name [*e.g.*, Investigation title*]) give an error if left empty.
2. Columns suposed to accept only numbers are checked as to not contain letters.
3. Columns supposed to hold dates are checked as to meet valid data formats (*e.g.*, DD/MM/YYYY).

| For a complete spreadsheet detailing the valid MIAPPE v1.1 specifications, check the :ref:`References - MIAPPE Section<miappe>`.