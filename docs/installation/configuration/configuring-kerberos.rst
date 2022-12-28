Configuring Kerberos
====================

Fire runs with a kerberized Spark cluster. It needs a keytab file to be able to submit jobs to the cluster.

The user for which the keytab is generated can be configured as a proxy user in the Hadoop cluster. Then Fire can impersonate the logged in users using the keytab file.


Steps for configuring Kerberos on Fire
---------------------------------------
 
* **Generate a keytab for Fire.**
 
 
* **Place it in .../fire-x.y.z/conf directory**::
 
    While this is the recommended location, the keytab file can be placed in any another directory too.
 
* **Make sure only the user running Fire application has read access to the keytab**. For example::
 
    -r-------- 1 fire staff 436 Jun 29 16:06 hive.keytab
 
 
* **Go to Administration/Configuration and update the following configurations to enable Kerberos for Fire.**


.. list-table:: Configurations to enable Kerberos for Fire:
   :widths: 30 30 40
   :header-rows: 1

   * - Configuration
     - Example Value
     - Details 
   * - kerberos.enabled
     - true
     - Set it to true to enable Kerberos for Fire  
   * - kerberos.keytab 
     - /user/ec2-user/fire.keytab
     - Absolute path of the keytab generated for Fire  
   * - kerberos.principal
     - fire@EXAMPLE.COM
     - Kerberos Principal of the keytab of Fire  
   * - kerberos.KERBEROS_REALM 
     - EXAMPLE.COM
     -  Kerberos Realm   
   * - kerberos.KERBEROS_KDC 
     - hostname.example.com
     - KDC Server   
   * - kerberos.hiveServer2Principal 
     - hive/hive2_host@EXAMPLE.COM
     - HIVE Server2 Principal  



Steps for generating the keytab for Fire
----------------------------------------

Below are the steps for generating the keytab file. **We have chosen Fire as the principal name. But you can have it as any user you are running Fire with**.

* **Start kadmin.local and add the new principal** ``fire@EXAMPLE.COM``::

    $ kadmin.local
 
    kadmin.local: addprinc -randkey fire@EXAMPLE.COM
                                         
    WARNING: no policy specified for fire@EXAMPLE.COM; defaulting to no policy
    Principal "fire@EXAMPLE.COM" created.

* **Create fire keytab file**::

    kadmin.local: xst -norandkey -k fire.keytab fire@EXAMPLE.COM

    Entry for principal fire@EXAMPLE.COM with kvno 1, encryption type aes256-cts-hmac-sha1-96 added to keytab

    WRFILE:fire.keytab.

    Entry for principal fire@EXAMPLE.COM with kvno 1, encryption type aes128-cts-hmac-sha1-96 added to keytab

    WRFILE:fire.keytab.

    Entry for principal fire@EXAMPLE.COM with kvno 1, encryption type des3-cbc-sha1 added to keytab     WRFILE:fire.keytab.

    Entry for principal fire@EXAMPLE.COM with kvno 1, encryption type arcfour-hmac added to keytab WRFILE:fire.keytab.

    Entry for principal fire@EXAMPLE.COM with kvno 1, encryption type des-hmac-sha1 added to keytab WRFILE:fire.keytab.

    Entry for principal fire@EXAMPLE.COM with kvno 1, encryption type des-cbc-md5 added to keytab WRFILE:fire.keytab.


* **Exit kadmin.local**::

    kadmin.local: exit
 
 
 
Verifying that the keytab file was correctly created
----------------------------------------------------

Below are the steps for verifying the keytab file:

* **Ensure that the keytab file was created and it has the right permissions**::

    $ ls -l fire.keytab
    
    -rw------- 1 root root 382 Jul 24 17:55 fire.keytab
 
 
* **Further verify the contents of keytab file. A normal keytab file depending on your krb5.conf settings, looks like this**::
 
    $ klist -e -k -t fire.keytab

    Keytab name: FILE:fire.keytab

    KVNO Timestamp Principal
    .....................................................................................................................................................
    1 07/24/16 17:55:07 fire@EXAMPLE.COM (aes256-cts-hmac-sha1-96)

    1 07/24/16 17:55:08 fire@EXAMPLE.COM (aes128-cts-hmac-sha1-96)

    1 07/24/16 17:55:08 fire@EXAMPLE.COM (des3-cbc-sha1)

    1 07/24/16 17:55:08 fire@EXAMPLE.COM (arcfour-hmac)

    1 07/24/16 17:55:08 fire@EXAMPLE.COM (des-hmac-sha1)

    1 07/24/16 17:55:08 fire@EXAMPLE.COM (des-cbc-md5)


Notes
-----

  * When running with a Kerberized cluster, deploy-mode should always be cluster.
  * The proxy user must be set in HDFS config.
  
  
