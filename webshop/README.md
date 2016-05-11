Webshop (Online shop example)
=============================

Example includes:

* SQLite database
* Model
* Files used to generate model and data

Version
-------

This sample is tested with cubes-1.0.1.

Description
-----------

This sample includes a simple model and sample data from a fictional
online shop.

It contains a fact table "sales" with information about product sales,
customer country, product and product category, and invoice amount.

It also contains a fact table "webvisits" with information about
fictional web visits (country of visitor, page views, browser...).

Slicer Use
----------

Execute:

    $ slicer serve slicer.ini

Documentation: http://packages.python.org/cubes/server.html

CubesViewer
-----------

You can use a client tool like CubesViewer to inspect these cubes:

Live example: http://jjmontesl.github.io/cubesviewer/

Documentation: https://github.com/jjmontesl/cubesviewer/

