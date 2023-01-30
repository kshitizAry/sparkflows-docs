Persisting SparkML Models
=========================

Spark ML Models
---------------

Spark ML models are saved into a directory with multiple files in it. Fire Insights has processors to save and load the Spark ML models.

Save Model Processor
+++++++++++++++++++++

NodeModelSave processor, saves the given Apache Spark ML model at the given location.

.. figure:: ../../../_assets/model/savemodelconfigurations.PNG
   :alt: Modelsave
   :width: 80%
   
ML Save Workflow
+++++++++++++++++++++

The workflow given below uses the NodeModelSave to save the Spark ML model at the given location.

.. figure:: ../../../_assets/model/mlmodelsave.png
   :alt: Modelsave
   :width: 80%
   
   
Load Model Processor
+++++++++++++++++++++

ML Load Model reads in the Spark ML model from the specified location.

.. figure:: ../../../_assets/model/loadmodelconfigurations.PNG
   :alt: Modelsave
   :width: 80%   
   
   
   
ML Load Workflow
+++++++++++++++++++++
   
The workflow given below reads in the ML model from the given location. It then uses the Predict node to give the predictions.

.. figure:: ../../../_assets/model/mlmodelload.png
   :alt: Model Load Workflow
   :width: 80%   
   
