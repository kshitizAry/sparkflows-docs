Docker Image on Windows
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Sparkflows can be installed and run on Windows 10 using the Docker image from the Docker Hub.


Prerequisites
-------------
* Windows 10 Pro / Enterprise / Education with support for Hyper-V
    (https://learn.microsoft.com/en-us/virtualization/hyper-v-on-windows/reference/hyper-v-requirements)

* Enable Hyper-V on Windows if disaled by following the steps below::
    * Goto ``Control Panel`` >> ``Programs`` >> ``Turn Windows Features on or off`` >> ``Enable below Hyper-V features``.
    
      .. figure:: ../../_assets/docker-install/hyperv.png
         :alt: hyperv
         :width: 50%
         
    * Restart the System.
    * Once the system starts, verify whether the Hyper-V Manager is running.

* Docker Desktop (https://docs.docker.com/docker-for-windows/install/)
    * Download the Docker Desktop Installer (As of this writing, tested with version: ``4.13.1``)
    * Use the below Configuration (The option should be ``un-checked`` ):
    
      .. figure:: ../../_assets/docker-install/hyperv-docker.png
         :alt: hyperv-docker
         :width: 50%
    * Adjust the amount of cores, memory given to Docker as seen below:
    
      .. figure:: ../../_assets/docker-install/docker-resources.png
         :alt: docker-resources
         :width: 50%
    * Verify that the docker is up and running and the the docker version by running ``docker --version``

    * Goto Settings -> Shared Drive and then Share the entire Drive with Docker and click Apply.

Installation Steps
---------------------------

* Pull the latest Sparkflows docker image from Docker hub::

    docker pull sparkflows/fire:py_3.2.1_3.1.0
   
* Start the docker image using the `docker run` command below::
    
    docker run -p 8080:8080 -p 9443:9443 -v  C:\Users\sparkflows:/usr/local/fire-3.1.0_spark_3.2.1 -e KEYSTORE_PASSWORD=12345678 -e FIRE_HTTP_PORT=8080 -e FIRE_HTTPS_PORT=9443  sparkflows/fire:py_3.2.1_3.1.0
    
    The local mount directory is (C:\Users\sparkflows) in the above docker run command. Please update it to directory structure on your machine.

* For the ``h2db`` to be accessible on the mounted directory, please edit the path in ``conf/db.properties`` to working directory and restart docker image::
   
   spring.datasource.url = jdbc:h2:file:./firedb  (By default it would be ~/firedb)

* Open your web browser and navigate to:: 
  
    http://localhost:8080

* Login with:: 

    admin/admin or test/test

    
.. note::  Two user accounts come preconfigured with Sparkflows.

           * admin/admin
           * test/test
    
    You may change the default passwords in Sparkflows from User Profile or Create new users using Menu Administration/Users. 


Stopping the Sparkflows docker image
------------------------------------
* Get the running container name of the Sparkflows image::

     docker ps
     
* Stop the container by::

     docker stop image_name

    
