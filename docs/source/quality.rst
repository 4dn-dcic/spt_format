.. _quality:

Spot Quality table
==================

Requirement level: optional

Recommended: **Yes**

Namespace: *4dn_SPT_quality*

Summary
-------


The table is mandatorily indexed by ``Spot_ID`` and each row corresponds to a DNA bright Spot. The order of all other columns (including those conditionally required) and of the rows are at the user's discretion.

.. warning:: All **MANDATORY** header fields and column names are indicated in **bold**. All *conditionally required* header fields and column names are indicated in *italics*.

File Header
-----------
- For full instructions see :ref:`headers-reference-label`
- The first line in the header is always ``##FOF-CT_Version=vX.X``.
- The second line in the header is always ``##Table_Namespace=4dn_FOF-CT_mapping``.

.. tip:: The header **MUST** contain a mandatory set of fields that describe any Software tool that was used to produce/process data in this table. If more than one software tool was used, please repeat a set of Software-fields for describing each of them.

The header **MUST** include a detailed description of each optional columns used. 

.. tip:: The table **MUST** contain at least 1 Optional or Conditionally Required Column. 

.. csv-table::
  :file: tables/quality_header.csv
  :header-rows: 1

Data Columns
------------
- For full instructions see :ref:`columns-reference-label`

As with all other Spot Data tables in this format, each row corresponds to
data associated with an individual Spot.

The first columns of this table are always ``Spot_ID``, ``Channel_Name``, and ``Fluorophore_Name``.

This table **MUST** contain at least 1 Optional or Conditionally Required Column. 

The content and order of all other columns is largely at user's discretion.
However, in order to align with existing `4DN-BINA-OME <https://doi.org/10.1038/s41592-021-01327-9>`_ Microscopy Metadata specifications, the use of specific column names and descriptions is *conditionally required* as indicated below. The order of the rows are at
the user's discretion.

.. csv-table::
  :file: tables/quality_columns.csv
  :header-rows: 1

Example
-------
The only mandatory column in this table are ``Spot_ID``, ``Channel_Name``, and ``Fluorophore_Name``. 

All other columns are either *Conditionally required* or Optional. *Conditionally required* columns should be drawn from the list provided in the file header or MUST be defined by the user using a Header line starting with ``#^``. 

.. tip:: The optional columns in this example table are included for illustrative purposes only and describe a case in which the user is reporting the Spot fit quality using metrics that align with existing `4DN-BINA-OME <https://doi.org/10.1038/s41592-021-01327-9>`_ Microscopy Metadata specifications. 

.. include:: examples/quality
  :code:

