Installation
^^^^^^^^^^^^

Sparkflows can be installed to run independently on Windows.


Installation Steps of Fire Insights with H2 DB
----------------------------------------------

* Download the fire tgz file from:

  * https://www.sparkflows.io/download
  
  
* Unpack the downloaded tgz file. Below are some tools which can be used for it::

    WinRar : https://www.rarlab.com/download.htm
    WinZip : https://www.winzip.com
    7-Zip : https://www.7-zip.org/download.html

    
* Create H2 DB::

    cd <fire install_dir>
    .\create-h2-db.bat
    
* Launch Fire Server::

    cd <fire install_dir>
    .\run-fire-server.bat start

* Open your web browser and navigate to:: 
  
    <machine_name>:8080

* Login with:: 

    admin/admin or test/test

    
    
.. note::  Two user accounts come preconfigured with Fire Insights.

           * admin/admin
           * test/test
    
    You may change these usernames and passwords in Fire under the menu Administration/Users 

Stopping Fire Insights
=================

Stopping the Fire Server
------------------------

Stop the Fire Server with the below::

    .\run-fire-server.bat stop


Stopping Fire Helper Processes
-------------

Stop Fire helper processes with the below::

    .\run-fire.bat stop


.. note::  On Windows, the PySpark engine will not get installed. Below are he functionalities that will not be available on bare metal windows install. We recommend either docker on windows to access all functionalities or install Fire Insights on Linux

           * AutoML
           * Prophet
           * ARIMA
           * Scikit learn models
           * Keras/Tensorflow models
           * A few other python native packages.    
    
    

    
    

