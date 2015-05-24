#Tesla Model S Rest API

A Java implementation of the client side interface to the Tesla Model S API documented at:

+	[Tesla Model S REST API](http://docs.timdorr.apiary.io/)
+	[Tesla Model S Remote Access Protocol](http://tinyurl.com/mnjyhbb)

**Note:** This version of the library corresponds to the "owner" API from Tesla which came about in the same timeframe as version 6 of the car software. This version is completely incompatible with the old Tesla API and the old version of this library. If you want to continue to use the older library, please refer to tag 0.5.

This is unofficial documentation of the Tesla Model S REST API used by the iOS and Android apps. It features functionality to monitor and control the Model S remotely. The documents are updated as new information is found.

This software and documentation do not come from Tesla Motors Inc.

*Be careful* when using this software as it can lock and unlock your car as well as control various functions relating to the charging system, sun roof, lights, horn, and other subsystems of the car.

*Be careful* not to send your login and password to anyone other than Tesla or you are giving away the authentication details required to control your car.

#Disclaimer

Use these programs at your own risk. The authors do not guaranteed the proper functioning of these applications. This code attempts to use the same interfaces used by the official Tesla phone apps. However, it is possible that use of this code may cause unexpected damage for which nobody but you are responsible. Use of these functions can change the settings on your car and may have negative consequences such as (but not limited to) unlocking the doors, opening the sun roof, or reducing the available charge in the battery.

#Contributors
[Joe Pasqua](https://github.com/jpasqua)

[Greyson Fischer](https://github.com/greyson)

# Preparing your build environment (maven)

The following command will resolve and download all dependencies, set
up the classpath, and create the JAR file.  This allows the Tesla
project to be included in other maven builds in the usual way 

        > mvn clean install

#Tests and Samples
There are two test programs included in the project: <code>BasicTest</code> and <code>Interactive</code>. The former simply runs through a sequence of functions in the client library to demonstrate that it is connecting and working. The second presents an interactive shell that allows the user to issue the various commands that are available through the client library.

To use either of these programs you must have active credentials for a Tesla vehicle that has remote access enabled. If you have more than one vehicle, you may select which vehicle to use in the Interactive program. BasicTest will always use the first vehicle returned by the Tesla portal.
