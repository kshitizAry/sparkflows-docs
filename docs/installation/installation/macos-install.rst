MacOS Installation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Sparkflows can run independently on a machine since we package Apache Spark along with it. It can also be connected to a Spark cluster to submit jobs.

Prerequisites
=============

Supported MacOS Versions
-------------------------

::

  - MacOS released not older than 1 year is supported


Below are required for installing Sparkflows on Mac::

  - JDK 1.8+ installed.
  - java and jar have to be in the PATH
  - 8 GB+ of RAM.
  - Python 3.7+ (when running Python and PySpark, otherwise not needed)

    
Downloading and Installing Java 8
---------------------------------

Java 8 can be downloaded and installed from here : https://www.oracle.com/java/technologies/javase/javase8-archive-downloads.html

You would need to set ``JAVA_HOME`` as well.

There are various ways for Installing Java 8 on MacOS X. Some are listed below.


Installing JDK on Mac
+++++++++++++++++

- Download the ``DMG`` file
- Install it by double clicking on it
- Installing using ``brew``


Quick Installation Steps of Fire with H2 Database
===========================================

* Download the fire ``TGZ`` file from:

  * https://www.sparkflows.io/download  OR   
  * https://www.sparkflows.io/archives
  
  
* Unpack it::

    tar xvf fire-x.y.z.tgz

* Create H2 Database::

      cd <fire install_dir>
      ./create-h2-db.sh
    
* Launch Fire Server::

    cd <fire install_dir>
    ./run-fire-server.sh start

* Open your web browser and navigate to:: 
  
    <machine_name>:8080

* Login with:: 

    admin/admin or test/test

    

Detailed Installation Steps
===========================

* Glossary

  * ``<install_dir>`` : location where you unzipped Sparkflows tgz file. For example this can be your home directory.
  * ``<machine_name>`` : hostname where your installed Sparkflows
  * ``#`` : used for comments and documentation


* Download the Sparkflows tgz file from:

  * https://www.sparkflows.io/download  OR   
  * https://www.sparkflows.io/archives
  
  
* Unzip it::

    tar xvf fire-x.y.z.tgz


* Set up H2 or MySQL Database

  Sparkflows can be configured to run with H2 Database or MySQL. H2 Database is very easy to set up with Sparkflows. For production deployments, MySQL is recommended.
    
   
* Launch Fire server::

    cd <fire install_dir>
    ./run-fire-server.sh start
    
* Test by opening your web browser and going to::

    http://localhost:8080

    OR

    http://<machine_name>:8080
    
    OR
    
    https://localhost:8443
    
    OR
    
    https://<machine_name>:8443

* Login with::

    Username: admin
    Password: admin


.. note::  Two user accounts come preconfigured with Fire.

           * admin/admin
           * test/test
    
    You may change these usernames and passwords in Fire under the menu Administration/Users
    
  
Stopping the Fire Server
------------------------

Stop the Fire Server with the below::

    ./run-fire-server.sh stop
    


Forwarding traffic to a port
+++++++++++++++++++++++++++++

::

    sudo firewall-cmd --add-forward-port=port=443:proto=tcp:toport=8443 --permanent
    sudo firewall-cmd --reload

