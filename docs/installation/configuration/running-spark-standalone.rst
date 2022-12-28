Running Apache Spark Standalone
=======================

Fire can be run on Spark Standalone cluster. In this case, Hadoop need not to be installed.

Installing Spark Standalone
---------------------------

- Install Java: 

  - wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "https://download.oracle.com/otn-pub/java/jdk/8u201-b09/42970487e3af4f5aa5bca3f542482c60/jdk-8u201-linux-x64.rpm"
  - yum localinstall jdk-8u201-linux-x64.rpm
  - Java -version
  
  .. figure:: ../../_assets/user-guide/spark_standalone_java_version.PNG
   :scale: 100%
   :alt: Standalone spark
   

Install Scala
---------------------------

- Install Scala:

  - wget http://www.scala-lang.org/files/archive/scala-2.10.1.tgz
  - tar xvf scala-2.10.1.tgz
  - sudo mv scala-2.10.1 /usr/lib
  - sudo ln -s /usr/lib/scala-2.10.1 /usr/lib/scala
  - export PATH=$PATH:/usr/lib/scala/bin ( we can add in .bash_profile)
  - scala -version
  
  
  .. figure:: ../../_assets/user-guide/spark_standalone_scala_version.PNG
   :scale: 100%
   :alt: Standalone spark
   

Install Apache Spark
--------------------

- Download Spark:

  - wget http://d3kbcqa49mib13.cloudfront.net/spark-2.1.0-bin-hadoop2.7.tgz

- Extract, create a new directory under the /usr/local called spark and copy the extracted connect into it:

  - tar xf spark-2.1.0-bin-hadoop2.7.tgz
  - mkdir /usr/local/spark
  - cp -r spark-2.1.0-bin-hadoop2.7/* /usr/local/spark

- Setup some Environment variables before you start spark-shell ( in .bash_profile):

  - export SPARK_EXAMPLES_JAR=/usr/local/spark/examples/jars/spark-examples_2.11-2.0.0.jar
  - PATH=$PATH:$HOME/bin:/usr/local/spark/bin

- Start you Scala Shell and run  Spark:

  - Go to sparkflows home directory
  - cd /usr/local/spark/bin
  - ./spark-shell
  
  .. figure:: ../../_assets/user-guide/spark_standalone_spark_version.PNG
   :scale: 100%
   :alt: Standalone spark
  
  
- Start a standalone master server by executing:

  - ./sbin/start-master.sh  ( from spark home directory)

- Once started, the master will print out a spark://HOST:PORT URL
- You can also find this URL on the master’s web UI: 

  -  http://Master_host_ip:8080/ by default
  
  
  
  .. figure:: ../../_assets/user-guide/spark_standalone_master_url.PNG
   :scale: 100%
   :alt: Standalone spark

Setup Spark Slave(Worker) Node
------------------------------

- Go to SPARK_HOME/conf/ directory.
- Edit the file spark-env.sh – Set SPARK_MASTER_HOST

  - If spark-env.sh is not present, spark-env.sh.template would be present. Make a copy of spark-env.sh.template with name spark-env.sh and add/edit the field SPARK_MASTER_HOST. Part of the file with SPARK_MASTER_HOST
  - cp ./conf/spark-env.sh.template ./conf/spark-env.sh
- Add a line in spark-env.sh :

  - SPARK_MASTER_HOST='MASTER_HOST_IP' 

Start Spark as Slave
-----------------------

- Goto SPARK_HOME/sbin and execute the following command:

  - ./start-slave.sh spark://MASTER_HOST_IP:7077 


Installing Fire
---------------

Install Fire on the master node.

- Download Fire Jar from website:

  - wget https://s3.amazonaws.com/sparkflows-release/fire/rel-x.y.z/2/fire-x.y.z.tgz
  - tar xvf fire-x.y.z.tgz

- Go to below directory:

  - cd fire-x.y.z
  - Update the port of Fire-ui & Fire to 8090 & 8082 as default port 8080 & 8081 is used by standalone spark, we can chose any other also.
  - From fire-x.y.z directory, we need to go conf/application.properties and update the port No.
  
  .. figure:: ../../_assets/user-guide/spark_standalone_port_configurations.PNG
   :scale: 100%
   :alt: Standalone spark

- Create database & run fire & fire-ui server:

  - ./create-h2-db.sh
  - ./run-fire.sh start
  - ./run-fire-server.sh start


Configuring Fire
----------------

Below are the configuration for Fire to submit the jobs to the Spark Standalone Cluster:

- Once The server fire & fire-ui start:
   - Login to "http://Machine_ip:8090/#/dashboard".
   - With password admin/admin.
   - Upload default applications.
   - Create a user ec2-user.
   - Login with ec2-user.
  
Configurations in Spark 
------------------------

The following configurations have to be set appropriately:

- Go to administration section and open Spark configuration. There you need to add following details in specific setup like below:
   - spark.master: spark://Master_host_ip:7077
   - spark.deploy-mode: client
   - spark.sql-context: SQLContext
   - After above updates, save the configurations.

  .. figure:: ../../_assets/user-guide/spark_configuration_standalonespark.PNG
   :scale: 100%
   :alt: Standalone spark

Running the Workflows on Application
-------------------------------------------------------
Now, go to application and try to run any workflows.

  .. figure:: ../../_assets/user-guide/spark_standalone_workflow_executions.PNG
   :scale: 100%
   :alt: Standalone spark
