Installing JDBC Drivers for Workflows
=======================

Fire Insights has JDBC Processors for reading data from JDBC sources or writing to JDBC sinks.

In order to connect to a JDBC source like Oracle/DB2/Postgres etc. the JDBC driver needs to be installed in Fire.

Below are the steps for installing the JDBC driver:

- *Download the JDBC jar file*
- *Copy it into "fire-user-lib" and "fire-server-lib" directory under the Fire installation home directory*
- *Restart fire*

Download the JDBC jar file
--------------------------

Download the JDBC jar file for the Database you are looking to connect to.

Copy it into fire-user-lib & fire-server-lib
--------------------------

Under the Fire installation home directory, there is "fire-user-lib" and "fire-server-lib" directory.

Copy the downloaded JDBC jar file into it.


Restart Fire server
------------

Restart the running Fire server with ``./run-fire-server.sh restart``

They will be restarted automatically.


Running Workflows depending on the jars added
---------------------------

When running workflows which depend on the jar file, select the checkbox for that jar file in the Workflow Execution Page. 

Downloading the JDBC jar files
---------------------------

MySQL
+++++


- MySQL connector can be downloaded from : https://dev.mysql.com/downloads/connector/j/ or you can download it directly from maven repository : https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.11/
- After downloading untar it with : ``tar xvf mysql-connector-java-8.0.11.tar.gz`` 
- After untaring the jdbc jar file is available in the directory
- Use the jar file (mysql-connector-java-8.0.11.jar) for installation in Fire

PostgreSQL
++++++++++

- PostgresSQL JDBC drivers can be downloaded from : https://jdbc.postgresql.org/download

.. note:: Already included in Sparkflows package

Oracle
++++++

- Oracle JDBC drivers can be downloaded from : https://www.oracle.com/technetwork/database/features/jdbc/jdbc-drivers-12c-download-1958347.html

Teradata
++++++++

- Teradata JDBC drivers can be download from : https://downloads.teradata.com/download/connectivity/jdbc-driver

https://dwgeek.com/steps-to-connect-teradata-database-from-spark-examples.html/

Azure Synapse
+++++++++++++

- https://docs.microsoft.com/en-us/azure/synapse-analytics/sql/connect-overview
- https://docs.microsoft.com/en-us/sql/connect/jdbc/microsoft-jdbc-driver-for-sql-server?view=sql-server-ver15


JDBC Drivers
-------

When using the JDBC processors, the following can be used for the JDBC Driver. Below are the JDBC URL's for some databases:

* MySQL : com.mysql.jdbc.Driver
* PostgreSQL : org.postgresql.Driver
* Oracle : oracle.jdbc.driver.OracleDriver

Example JDBC URL
----------------

Below are some example JDBC URL for reading from Relational sources when using the JDBC Processors:

* MySQL : jdbc:mysql://localhost:3306/mydb
* PostgreSQL : jdbc:postgresql://localhost:5432/mydb


