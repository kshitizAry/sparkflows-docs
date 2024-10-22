Installation
================


Installation Steps of Fire with H2 Database
----------------------------------------------

* Download the fire ``TGZ`` file from:

  * https://www.sparkflows.io/download

* Create a new directory named ``sparkflows`` and copy the TGZ file into it::

    mkdir sparkflows

  ::

    cp fire-x.y.z.tgz sparkflows

  ::

    cd sparkflows
  
  
* Unpack it::

    tar xvf fire-x.y.z.tgz

* Create H2 Database::

      cd <sparklows/fire-3.X.YY_spark_3.2.1>

  ::

      ./create-h2-db.sh

* Sparkflows can be configured to run with H2 Database or MySQL. H2 Database is very easy to set up with Sparkflows. For production deployments, MySQL is recommended.
    
* Launch Fire Server::

    ./run-fire-server.sh start

* Open your web browser and navigate to:: 
  
    http://<machine_name>:8080 OR https://<machine_name>:8443

* Login with:: 

    admin/admin or test/test

Installing and starting the Python engine
------------------------------------------------

Sparkflows comes with Java engine and Python engine. Following the above steps, we have installed Sparkflows and started it only with Java engine. If you want to leverage the capabilities of python Machine Learning libraries as well, please install the Python engine by following the link: https://docs.sparkflows.io/en/latest/installation/installation/python-install-macos.html

Stopping the Fire Server
------------------------

Stop the Fire Server with the below::

    ./run-fire-server.sh stop
    


Forwarding traffic to a port
------------------------

::

    sudo firewall-cmd --add-forward-port=port=443:proto=tcp:toport=8443 --permanent

::

    sudo firewall-cmd --reload

