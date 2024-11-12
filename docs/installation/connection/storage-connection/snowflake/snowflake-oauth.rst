Snowflake Oauth Connection
=======

Sparkflows provides the capability to create "Snowflake Connection" and use the connection to access various resources, using Oauth.

Snowflake Connection Configuration
----------

Use the below configurations for creating the connection to Snowflake.


   .. list-table:: 
      :widths: 10 20 20
      :header-rows: 1


      * - Title
        - Description
        - Value
      * - Credential Store  
        - Select the Credential Store from drop-down
        - Choose specific Credential Store from drop-down or Select Do not use Credential Store
      * - Select Category
        - Select Category of Connection Type
        - Select Storage Connection
      * - Connection Type 
        - Select the Connection type from drop-down
        - Choose Snowflake as Connection Type
      * - Authentication Type 
        - Select the USER_CREDENTIAL or OAUTH
        - Choose OAUTH as Authentication Type
      * - Connection Name
        - Connection Name
        - Add an unique Connection Name
      * - Url
        - Url for Snowflake
        - Url for Snowflake

   .. figure:: ../../../../_assets/installation/connection/snowflake_storage.PNG

      :alt: connection
      :width: 60%    

   .. figure:: ../../../../_assets/installation/connection/snowflake_oauth.png
      :alt: connection
      :width: 60%
Test and save the connection
------

Once you save the connection, resouces can be used inside workflow editor etc. using the above connection.

.. Note:: Make Sure Sparkflows User Login(Using OAuth) should have sufficient Privilege of Snowflake resources.


Documentation
-----

Reference guide : https://docs.sparkflows.io/en/latest/snowflake/index.html
