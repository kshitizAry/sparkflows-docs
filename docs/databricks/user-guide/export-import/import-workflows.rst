Import Workflows
===============

Fire Insights enables you to import workflows as JSON files. These JSON files can be exported to use in another instance of Fire Insights.

Below are the steps for importing a workflow.

Steps for Importing Workflow
-------

You can Login to Fire Insights Web server URL and follow below steps:

* Go to the Project List page.
* Select the project to import workflows to 
* Click the Workflows tab

You should get to a page similar as below:

.. figure:: ../../_assets/user-guide/export-import/wf_list.PNG
     :alt: userguide
     :width: 60%


* Click the ``Import`` button and select ``From Workflow Files``

You should get to a page similar as below:


.. figure:: ../../_assets/user-guide/export-import/wf_import_file.PNG
     :alt: userguide
     :width: 60%  
 
Once you Select From Workflow Files, it will take you to new windows like below:
 
.. figure:: ../../_assets/user-guide/export-import/wf_import_page.PNG
     :alt: userguide
     :width: 60%   

Once you Click on ``Import Workflow`` tab, it will take you to new windows where you can upload workflow JSON file from your local Computer and select any one of the option depending on workflow availablity in that project with UUID's, the available options are listed below:

Import Configuration
-----------------

When importing to an existing Project, there are 3 possible options to choose from:

* OVERWRITE WORKFLOW IF SAME UUID EXISTS IN THE PROJECT
    * In this case, if matching UUIDs are found, the existing project will be removed and replaced with the uploaded file 
* CREATE A NEW UUID IF ONE ALREADY EXISTS
    * In this case, if matching UUIDs are found, the uploaded file will be assigned a new UUID 
* CREATE A NEW UUID
    * In this case, the uploaded file will always be assigned a new UUID

.. figure:: ../../_assets/user-guide/export-import/wf_import_json.PNG
     :alt: userguide
     :width: 60%   
     
Once you Click on ``Import``, the workflow should be available in workflow list page of Specific project.

.. figure:: ../../_assets/user-guide/export-import/wf_imported.PNG
     :alt: userguide
     :width: 60%   
     
.. note:: Make sure that data pointed to the workflow JSON File should be available on new instance of Fire Insights where you are Importing.     
