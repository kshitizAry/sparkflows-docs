HTTPS : Import Self-Signed Certificates
================================

Fire Insights comes with a self-signed certificate. It is available in "conf/keystore.jks" of fire-x.y.z directory.

When you try to use a self-signed certificate, the browser will complain as it has not been issued by a Certificate Authority.

You can import self-signed certificate into the browser inside ``Trusted Root Certification Authorities`` to suppress the warning message.

Below are the steps to import self-signed certificate into your browser:

Export Certificate to Machine
--------------------------------------------

Below are the steps to export the certifiate to your machine.

Go to URL for the HTTPS port
+++++

https://host_name:8443/login

.. figure:: ../../../_assets/configuration/1.PNG
   :alt: certificate
   :width: 50%
   
Select Not Secure
++++++

Click on ``Not secure`` option.

 
.. figure:: ../../../_assets/configuration/2.PNG
   :alt: certificate
   :width: 50%
   
Click on Certificate
+++++

.. figure:: ../../../_assets/configuration/3.PNG
   :alt: certificate
   :width: 45%
   
   

View Certificate
+++++

.. figure:: ../../../_assets/configuration/viewcertificate.PNG
   :alt: certificate
   :width: 45%

Click on Details
++++++

Click on ``Details`` option to see detailed information of certificate.

.. figure:: ../../../_assets/configuration/Certificatedetails.PNG
   :alt: certificate
   :width: 45%

Copy Certificate to local machine
+++++++

Click on ``copy to  file`` option to copy certificate to ``local machine``.

.. figure:: ../../../_assets/configuration/Copyfile.PNG
   :alt: certificate
   :width: 45%

Choose file format
++++++

Select the below option and press ``Next``.

.. figure:: ../../../_assets/configuration/Exportfile.PNG
   :alt: certificate
   :width: 45%
   
Choose Name and File Location
++++

Select the ``Name & file location`` of the certificate using browse button.

.. figure:: ../../../_assets/configuration/filelocation.PNG
   :alt: certificate
   :width: 45%

Success Message
++++++

On updation of details a ``Success message`` will be displayed on the screen.

.. figure:: ../../../_assets/configuration/4.png
   :alt: certificate
   :width: 45%

Next, you need to add the exported certificate to the browser.

   
Adding Certificate to Browser
--------------------------

You can add certificate to the browser using **Google Chrome** by following the below steps:

* Open Google Chrome and go to Settings.

* Navigate to Settings -> Advanced -> Privacy and Security-> Manage Certificates.
   

.. figure:: ../../../_assets/configuration/managecertificate.PNG
   :alt: certificate
   :width: 45%

* Click on the ``Manage Certificates`` icon.


.. figure:: ../../../_assets/configuration/Managebrowsecert.PNG
   :alt: certificate
   :width: 45%

* Click on ``Import`` button.


.. figure:: ../../../_assets/configuration/import.PNG
   :alt: certificate
   :width: 45%


* Select ``certificate from local system``, then select ``Trusted Root Certification Authorities`` option and click on ``yes`` to save it.

.. figure:: ../../../_assets/configuration/Trustedroot.PNG
   :alt: certificate
   :width: 55%
   

.. figure:: ../../../_assets/configuration/Savingcertificate.PNG
   :alt: certificate
   :width: 55%

.. figure:: ../../../_assets/configuration/successmsg.PNG
   :alt: certificate
   :width: 55%

* Once the above process is completed, close the browser and start again and try to login with above URL. It should work without any warnings.

.. figure:: ../../../_assets/configuration/5.png
   :alt: certificate
   :width: 55%
   


* URL for further assistance: https://peacocksoftware.com/blog/make-chrome-auto-accept-your-self-signed-certificate 

