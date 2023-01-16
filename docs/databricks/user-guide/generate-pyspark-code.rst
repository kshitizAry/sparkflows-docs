Generate Pyspark Code
====================

Fire Inisghts enable you to Generate Pyspark Code even with spark engine and run the job using python engine.

Below are steps involve in it:

Enable Auto Pyspark Code Generation
---------------

Login to Fire Insights application and Enable Auto Pyspark Code Generation from the Configurations page.

Go to ADMINISTRATION, select configuration, choose MODULE tab and search for 'module.enableAutoPysparkCodeGeneration' and make it to 'true', by default it will be false. 

.. figure:: ..//_assets/user-guide/generate-pyspark-code/1.PNG
   :alt: Pyspark code generate
   :width: 70%

Generate Pyspark Code
----------------

Now once the Configuration is enable for Generating Pyspark Code.

Create an example workflow using spark engine and saved it.

.. figure:: ..//_assets/user-guide/generate-pyspark-code/2.PNG
   :alt: Pyspark code generate
   :width: 70%
   
Once the workflow got saved, Go to workflow editor page, Click on the three dot on the top right corner of workflow editor page, you will see option of Generate Pyspark Code, select it.

.. figure:: ..//_assets/user-guide/generate-pyspark-code/3.PNG
   :alt: Pyspark code generate
   :width: 70%

Once you select option of Generate Pyspark Code, a window will open with Pyspark sample code for the example workflow, copy it and save it into '.py' file.

.. figure:: ..//_assets/user-guide/generate-pyspark-code/4.PNG
   :alt: Pyspark code generate
   :width: 70%

Upload Generated Pyspark Code in DBFS
--------------

Now you have the Generated Pyspark Code in your local system, Upload it into DBFS which is accessible from databricks cluster.

.. figure:: ..//_assets/user-guide/generate-pyspark-code/5.PNG
   :alt: Pyspark code generate
   :width: 70%

Submit Jobs on Databricks cluster
----------

Now once you upload the Generated Pyspark Code in DBFS, you can create Jobs in databricks with Below details:

::

    Task name: Add Unique Task name
    Type : Select Type as Python & Enter the URI of the Python file to be executed
    Cluster : Select any existing databricks cluster or even new one.
    Parameters : If any
    Advanced options : Add dependency if any
    
.. figure:: ..//_assets/user-guide/generate-pyspark-code/6.PNG
   :alt: Pyspark code generate
   :width: 70%    

Once the above parameters got added, Click on Create Button, it will create new job with your selected parameters.

Now you can Run the job.

.. figure:: ..//_assets/user-guide/generate-pyspark-code/6.PNG
   :alt: Pyspark code generate
   :width: 70% 
   
Once the Job Run successfully, you will see the Status of Job as Succeeded.

.. figure:: ..//_assets/user-guide/generate-pyspark-code/7.PNG
   :alt: Pyspark code generate
   :width: 70% 


