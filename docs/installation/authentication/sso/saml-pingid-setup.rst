Ping Identity Setup
========

Below are steps to setup SAML 2.0 Ping Identity:

Create an account in Ping Identity
------

.. figure:: ../../../_assets/authentication/pingid/ping_id.PNG
   :alt: sso
   :width: 60%
   
Sign in to Ping Identity
------

.. figure:: ../../../_assets/authentication/pingid/ping_id_1.PNG
   :alt: sso
   :width: 60%

After login go to home and click on "Administrators" in Environments
------

.. figure:: ../../../_assets/authentication/pingid/pingid_2.PNG
   :alt: sso
   :width: 60%

Click on "Connections"
------

.. figure:: ../../../_assets/authentication/pingid/pingid_3.PNG
   :alt: sso
   :width: 60%

Select "Applications" & click on "+" sign to create new application
------

.. figure:: ../../../_assets/authentication/pingid/pingid_4.PNG
   :alt: sso
   :width: 60%

Add "Name" and "Descriptions" of the application
------

.. figure:: ../../../_assets/authentication/pingid/pingid_5.PNG
   :alt: sso
   :width: 60%
   
Choose "Application Type" as SAML Application
------

.. figure:: ../../../_assets/authentication/pingid/pingid_6.PNG
   :alt: sso
   :width: 60%
   
Click on "Configure" and provide application metadata as per your configuration
------

.. figure:: ../../../_assets/authentication/pingid/pingid_7.PNG
   :alt: sso
   :width: 60%
   
Update "ACS URLs" & "Entity ID" & save the application
------

.. figure:: ../../../_assets/authentication/pingid/pingid_8.PNG
   :alt: sso
   :width: 60%
   
Activate the application and download the metadata from application which will be used while configuring Fire Insights
------

.. figure:: ../../../_assets/authentication/pingid/pingid_9.PNG
   :alt: sso
   :width: 60%

.. note::  Make sure to change localhost to your domain name or your ip, Where Fire is Running.
