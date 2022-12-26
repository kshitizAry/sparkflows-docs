H2 Database
===========

Fire can be setup up easily to run with H2 database. Fire runs H2 in embedded mode. The H2 database is used for storing the metadata of the DataSets, Workflows, Dashboards, Users, Groups, Roles etc.

More details of the H2 database can be found here : http://www.h2database.com/html/main.html

 
If you want to run multiple instances of Fire for high availability, configure Fire to run with MySQL.

Creating/Upgrading the H2 Database
----------------------------------

Execute the following steps on your CLI:


* Mac/Linux::

    cd <install_dir>/fire-x.y.z
    ./create-h2-db.sh

* Windows::

    cd <install_dir>\fire-x.y.z
    .\create-h2-db.bat

 

If you would like to use different values for the DB, username, password, update them in ``<install_dir>/fire-1.4.0/conf/db.properties``::


    spring.datasource.url = jdbc:h2:file:~/firedb

    spring.datasource.username = fire

    spring.datasource.password = fire

    spring.datasource.driverClassName = org.h2.Driver

 

.. note::  firedb is created in the users home directory and the name is firedb.mv.db



Recreating H2 Database
----------------------
 
If you need to recreate the H2 database, follow the steps below to create a new empty H2 DB::
 
    Stop the running Fire server.
    
    Move the existing firedb files to another temp location on your disk.
    
    Recreate the H2 DB using the steps in the above section for creating a brand new empty H2 DB for Fire.


