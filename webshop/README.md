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

This sample includes a simple model and sample data about a fictional
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


Generation of sample data
-------------------------

SQLite database and model are included in this directory. If you however wish to generate your own
database and model, sample data was generated using CubETL (https://github.com/jjmontesl/cubetl).

Configuration file and data for the "webshop" Cubes sample is included in the CubeTL source (cubetl/examples).

Create and load database:

    $ PYTHONPATH=~/git/cubetl python ~/git/cubetl/bin/cubetl ~/git/cubetl/library/*.yaml webshop.yaml webshop.process -q
    2015-10-18 06:53:01,361 - INFO - Starting CubETL 0.4-devel
    2015-10-18 06:53:01,524 - INFO - Connecting to database: sqlite:///webshop.sqlite
    2015-10-18 06:53:01,530 - INFO - Creating table dates
    2015-10-18 06:53:01,783 - INFO - Creating table customer
    2015-10-18 06:53:01,949 - INFO - Creating table product
    2015-10-18 06:53:02,084 - INFO - Creating table country
    2015-10-18 06:53:02,232 - INFO - Creating table webshop_sales
    2015-10-18 06:53:02,382 - INFO - Creating table browser
    2015-10-18 06:53:02,530 - INFO - Creating table webshop_visits
    2015-10-18 06:53:02,703 - INFO - Processing webshop.process
    2015-10-18 06:53:02,705 - INFO - Starting database transaction
    2015-10-18 06:53:07,021 - INFO - SQLTable Totals  ins/upd/sel: 2041/0/2846
    2015-10-18 06:53:07,026 - INFO - Total time: 5  Total messages: 1192  Global rate: 211.434 msg/s

Cubes model was generated using:

    $ PYTHONPATH=~/git/cubetl python ~/git/cubetl/bin/cubetl ~/git/cubetl/library/*.yaml webshop.yaml webshop.export-cubes > model.json

Note that the configuration for the "webshop" sample data is included with
