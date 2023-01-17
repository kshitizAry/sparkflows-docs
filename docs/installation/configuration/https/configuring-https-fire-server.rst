Configuring HTTPS for Fire Server
=================================

You can choose to run the Fire Server either on http or https connection.

The ports for http and https are configured in the file ``conf/application.properties``::

    http.port=8080
    https.port=8443

 
HTTP
----
 
http://hostname:8080/login

 
HTTPS
-----
 
https://hostname:8443/login
 
keystore.jks
------------

Fire Server comes with a pre-configured keystore in the ``conf`` folder of the install.

* conf/keystore.jks
* conf/keystore.properties : Stores the keystore password

Generating New Keystore
-----------------------

You can use the following command for generating a new keystore::

    keytool -genkeypair -alias sparkflows -keyalg RSA -validity 365 -keystore keystore.jks

You will be prompted with the following questions where you should enter something similar to the Sample answers as below::

    Enter keystore password: 
    Re-enter new password: 
    What is your first and last name?
      [Unknown]:  John Smith
    What is the name of your organizational unit?
      [Unknown]:  BigData
    What is the name of your organization?
      [Unknown]:  MyOrg
    What is the name of your City or Locality?
      [Unknown]:  San Francisco
    What is the name of your State or Province?
      [Unknown]:  California
    What is the two-letter country code for this unit?
      [Unknown]:  CA
    Is CN=John Smith, OU=BigData, O=MyOrg, L=San Francisco, ST=California, C=CA correct?
      [no]:  yes
    Enter key password for <sparkflows>
            (RETURN if same as keystore password): Press the return key or Type and note down the password



Copy the keystore into the Fire installation directory
----------------------------------------------

* Copy the generated ``keystore.jks`` file into the ``conf`` folder of your installation.
* Update ``keystore.properties`` with the new password.
 
.. Note::  When the keystore is updated, the password has also to be updated in case it changes. 

           The Fire web server would also have to be restarted for the changes to take effect.
           

Use keytool commands
--------------------

Listing entries in Keystore
+++++++++++++++++++++++++++

List entries in keystore::

    keytool -list -keystore keystore.jks


Importing a Certificate to an existing Keystore
++++++++++++++++++++++++++++++++++++++++++++

Importing a Certificate to an existing Keystore::

    keytool -import -trustcacerts -alias <Name of Cert> -file <Absolute Path to .crt File> -keystore <Absolute Path to Desired Keystore> -storepass <KEYSTORE_PASSWORD>

 
Install certificate on EMR Cluster
--------------------------------------------
 
When using EMR cluster to run the Spark jobs, the certificate needs to be imported in the Java keystore, in order  to track the status of the Spark jobs. Follow the steps below to import certificate on cluster creation:
 
* Create a **bootstrap** script with the following content::
    
    #!/bin/sh
    aws s3 cp s3://my_bucket/certs/sparkflows_cert.pem .
    keytool -importcert -trustcacerts -keystore $JAVA_HOME/lib/security/cacerts -file sparkflows_cert.pem \
    -alias sparkflowsCert \
    -storepass changeit \
    -noprompt
    
* Configure the EMR cluster to use the above bootstrap script.
   
