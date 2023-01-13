Install OpenNLP Model JAR
=============================

When running locally
--------------------

* Create a directory called opennlp-models-1.5 on the local file system.
* Download the OpenNLP model jar from : http://opennlp.sourceforge.net/models-1.5/

  * For example: wget http://opennlp.sourceforge.net/models-1.5/en-ner-person.bin
  
* Copy the OpenNLP model jar into the opennlp-models-1.5 directory created.

 

When running on Apache Spark Cluster
-----------------------------

* Copy the model file onto HDFS into a directory called opennlp-models-1.5
* For example, /user/centos/opennlp-models-1.5/en-ner-person.bin
* The model file should be accessible by all the users who would use it.

Using OpenNLP Model Jars
------------------------

* Specify the path of the jar file in the dialog box of the OpenNLP nodes in the workflow.
* For example, for the OpenNLPNameFinder node the path can be : /user/centos/opennlp-models-1.5/en-ner-person.bin

.. figure:: ..//_assets/user-guide/opennlp-1.png
   :alt: OpenNLP
   :align: center
   
