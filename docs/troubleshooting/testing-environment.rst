Testing Environment
--------------

It is a good idea to run the below steps to ensure that the environment is set up and working right.

Run the steps which are relevant for your environment.

Check Java version
+++++++++

``java --version``

Check if python 3.7+ has been set up
+++++++++

``python --version``

Check if the machine has access to the internet
++++++++++


Check available storage on disk
+++++++++++

``du -sh *``

Check the memory and vcpu on the machine
++++++++++++

top

It is recommended to have at least 16GB of RAM and 4+vCPU's on the machine.


Check if fire-ui process is running
+++++++++

``ps -ef | grep fire-ui``

fire-ui is the main webserver process.

Check the ports on which fire-ui is running
++++++++++

By default Fire Insights listens on 2 ports : 8080 and 8443

Run SparkPi on the cluster
+++++++++

Run SparkPi to ensure that the Apache Spark cluster has been set up correctly.

spark-submit ...

Check if Airflow has been correctly set up
+++++++++++


Check Kerberos Setup
++++++++

Check if the kerberos keytab is correct.

Kinit:

``kinit -kt keytab_file principal``

Access HDFS:

``hdfs dfs -ls /tmp``

Check Logs for erros
+++++

Check there are no major errors in the fire-ui log file.

grep -i exception fireserver.log

Check there are no major errors in fire log file.

grep -i exception fire.log

Check HIVE setup
++++

Log into HIVE with Beeline and check if we are able to list the databases and tables. And also able to query a table.


Check Livy Configuration
++++

Check if SparkPi submission to Livy works good.

curl

Check AWS S3 access
++

Check if we are able to access files on S3


Check Airflow Setup
+++++++

Check if we are able to submit a DAG to Airflow and execute it.

DAG 1
======

- SparkPi via spark-submit

DAG 2
=====

- A spark program which reads data from S3 and writes the output to another S3 location


DAG 3
=====

- Use MACROS



