EMR Livy Connection
=============

This is a stepwise guide to enable you to create an Apache Livy Connection in Sparkflows and then run jobs or workflows using the connection.

Detailed Steps
+++++++

Following the steps given below would allow you to successfully create a Livy Connection.

1. Enable Livy in Sparkflows

Login to ``Sparkflows`` application -> ``Administration`` -> ``Configurations`` -> ``Connection`` -> and enable Livy connection by setting the parameter given below:

::

    connection.livy.enabled : true

.. figure:: ../../../_assets/aws/livy/livy_configuration.PNG
   :alt: livy
   :width: 60%

2. Create Global Connections

Once you have saved the above configuration, navigate to ``Administration`` -> ``Global Connections`` -> ``Add Connections`` as shown below:

.. figure:: ../../../_assets/aws/livy/administration.PNG
   :alt: livy
   :width: 60%
   
3. Add Connection for Group

Navigate to ``Administration`` -> ``Global Connections`` -> ``Add Connections`` -> ``Add Connection For Group`` which pop up new windows -> Select ``Compute Connection`` and other parameters as shown below:

.. figure:: ../../../_assets/aws/livy/add_connection.PNG
   :alt: livy
   :width: 60%
   
.. figure:: ../../../_assets/aws/livy/add_livy_connection.PNG
   :alt: livy
   :width: 60%   
   
4. Additional parameter as per your environment

Once you have selected Connection Type & Groups, add the additonal connection parameters as needed.

For GENERAL tab :

.. list-table:: 
   :widths: 10 20 30
   :header-rows: 1

   * - Title
     - Description
     - Value
   * - Connection name
     - Connection Name
     - Name of Connection
   * - Postback Url
     - Postback URL
     - Postback URL through which Livy sent result back to Fire Insights
   * - Title 
     - Title of selected Connection
     - Title of selected Connection  
   * - Description 
     - Connection Description 
     - Connection Description
   * - Url
     - URL for selected Connection type
     - Add URL for Livy Connection
   * - Driver Class
     - Driver Class for selected Connection type 
     - It Comes with default value  
     
.. figure:: ../../../_assets/aws/livy/add_general.PNG
   :alt: livy
   :width: 60%

For LIVY tab :

.. list-table:: 
   :widths: 10 20 30
   :header-rows: 1

   * - Title
     - Description
     - Value
   * - Jars
     - Jars to be used in EMR Livy session
     - Jars path located in S3 Location
   * - Pyspark Files
     - Pyspark Files to be used in EMR Livy session
     - Pyspark file located in S3 Location  
   * - Files
     - Files to be used in EMR Livy session
     - Any Files if needed
   * - Archives Files
     - Archives Files to be used in EMR Livy session
     - Value  
   * - Driver Memory 
     - Driver Memory to be used in EMR Livy session
     - Driver Memory if any specific memory you need to pass
   * - Driver Cores
     - Driver Cores to be used in EMR Livy session
     - Driver Cores if any specific Cores you need to pass  
   * - Executor Memory
     - Executor Memory to be used in EMR Livy session
     - Executor Memory if any specific Executor Memory you need to pass  
   * - Executor Cores
     - Executor Cores to be used in EMR Livy session
     - Executor Cores if any specific Executor Cores you need to pass  
   * - Num Executors
     - Num Executors to be used in EMR Livy session
     - Num Executors if any specific Num Executors you need to pass  
     
.. figure:: ../../../_assets/aws/livy/add_livy.PNG
   :alt: livy
   :width: 70%     

.. Note:: Make sure to upload ``fire-spark_x.y.z-core-x.y.z-jar-with-dependencies.jar`` to S3 bucket and that it is accessible from Saprkflows webserver UI. This jar is available in Sparkflows binary. Untar the binary to find it inside ``fire-x.y.z/fire-core-lib``. 

.. figure:: ../../../_assets/aws/livy/livy_jar.PNG
   :alt: livy
   :width: 70% 


For HDFS tab :

.. list-table:: 
   :widths: 10 20 30
   :header-rows: 1

   * - Title
     - Description
     - Value
   * - NameNode URI
     - NameNode URI 
     - NameNode URI for HDFS
   * - Home Dir
     - Home Dir under which various directories exist
     - Value  
 
.. figure:: ../../../_assets/aws/livy/add_hdfs.PNG
   :alt: livy
   :width: 60%

For HIVE tab :

.. list-table:: 
   :widths: 10 20 30
   :header-rows: 1

   * - Title
     - Description
     - Value
   * - JDBC Driver
     - JDBC Driver
     - JDBC Driver for Hive
   * - JDBC DB URL
     - JDBC DB URL
     - JDBC DB URL for Hive
     
.. figure:: ../../../_assets/aws/livy/add_hive.PNG
   :alt: livy
   :width: 60%    

For KERBEROS tab :

.. list-table:: 
   :widths: 10 20 30
   :header-rows: 1

   * - Title
     - Description
     - Value
   * - Keytab
     - Keytab
     - Kerberos Keytab for Fire user   
   * - Principal
     - Principal 
     - Kerberos Principal for Fire user  
   * - REALM
     - REALM
     - Value   
   * - KDC
     - KDC
     - Value 
   * - HiveServer2 Principal
     - Kerberos Principal for HiveServer2
     - Value  
     
.. figure:: ../../../_assets/aws/livy/add_kerberos.PNG
   :alt: livy
   :width: 60%      

For YARN tab :

.. list-table:: 
   :widths: 10 20 30
   :header-rows: 1

   * - Title
     - Description
     - Value
   * - Resource Manager URL
     - Resource Manager URL
     - Value  
     
.. figure:: ../../../_assets/aws/livy/add_yarn.PNG
   :alt: livy
   :width: 60%      

5. Test Connection and Save

Once you have updated the above parameters, click on ``Test Connection``, if the Connection is Successful, ``Save`` the connection.

.. figure:: ../../../_assets/aws/livy/add_test_connection.PNG
   :alt: livy
   :width: 60%
   
.. figure:: ../../../_assets/aws/livy/add_list.PNG
   :alt: livy
   :width: 60%   

.. Note:: Make sure that Apache Livy URL is accessible from Sparkflows webserver URL.
