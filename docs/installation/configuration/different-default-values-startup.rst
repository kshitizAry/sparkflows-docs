Different Default Values on Startup
===================================

Overview
---------

 
Fire has a number of properties under Administration / Configuration. When initially installed they have certain default values. Administrators can log into Fire through their Browser and update the properties.

However, there might be cases where you want Fire to come up with different default values for the Configurations when installed. This enables more automation and the Administrator does not have to go in and manually change the default values.

Steps
-----

Below are the Steps to override the default Configuration values:

 * Update the file **conf/configuration.properties** with the new key/value pairs.


Now the default values are populated with the values provided in ``configuration.properties``.

Fire comes with an empty ``conf/configuration.properties`` file. You can put in your values into it.


Removing properties from conf/configuration.properties
------------------------------------

Fire will continue to take the final values from ``conf/configuration.properties`` for any property which is there in the file.

If you would like Fire not to use any of the properties from ``conf/configuration.properties``, but take it from the database, then remove or comment out those properties in ``conf/configuration.properties``.

Saving the new values into the DB
---------------------------------

When the configuration values are saved, they get updated in the database.

Even if they are removed from ``configuration.properties``, they would be saved in the database.



