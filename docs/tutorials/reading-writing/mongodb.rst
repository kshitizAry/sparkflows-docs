Read and Write MongoDB
================================

MongoDB is a document database with the scalability and flexibility that you want with the querying and indexing that you need. Here we are loading data from HDFS  and saving it into MongoDB.

Workflow for Loading data into MongoDB
---------------------------------------

The below workflow reads in the Sample Dataset which is in CSV format from HDFS.
It then saves the data into MongoDB.

.. figure:: ../../_assets/tutorials/mongodb/MongoDB.png
   :alt: SaveMongoDB
   :width: 45%

The below diagram shows the dialog box for the SaveMongoDB Processor.

.. figure:: ../../_assets/tutorials/mongodb/savemongodbprocessor.PNG
   :alt: SaveMongoDB
   :width: 80%
   
Workflow Execution
------------------

When we execute the workflow, it reads in the dataset from HDFS and loads it into MongoDB.

.. figure:: ../../_assets/tutorials/mongodb/workflowexecutionsavemongodb.PNG
   :alt: SaveMongoDB
   :width: 75%

Workflow for Reading Data from MongoDB
---------------------------------------

The below workflow reads Data in MongoDB.It then prints the data.


.. figure:: ../../_assets/tutorials/mongodb/ReadMongoDB.png
   :alt: ReadMongoDB
   :width: 45%

The below diagram shows the dialog box for the ReadMongoDB Processor.

.. figure:: ../../_assets/tutorials/mongodb/Readmongodbprocessor.PNG
   :alt: ReadMongoDB
   :width: 80%
   
In the above dialog, the 'Refresh Schema' button infers the schema of the collections. Thus, it is able to pass down the output schema to the next Processor making it easy for us to build the workflow.   
   
Workflow Execution
------------------

When we execute the workflow, it reads in the Sample collection from MongoDB and displays the first few lines.

We see that the Sample Data records that we wrote to MongoDB in the first workflow is read back now.

.. figure:: ../../_assets/tutorials/mongodb/workflowexecutionreadmongodb.PNG
   :alt: ReadMongoDB
   :width: 65%

