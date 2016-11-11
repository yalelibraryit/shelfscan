Shelfscan
=========

# Installation Steps

First, clone the three repos (shelfscan, accservices, accservices-web)

1. Clone this repo.
2. Clone yalelibrary/accservices
3. Clone yalelibrary/accservices-web

Import all three projects into IntelliJ IDEA (or your favorite IDE). The project is set up as Maven multi-module project.

Make sure that all the standard Java dependecies are installed (JDK, Maven, Microsoft JDBC driver). Install the JDBC driver through Maven.

After installing the Java stack, build the Maven project:

```
cd shelfscan
mvn clean install -P prod
```

Copy the resulting war file in accservices-web/target/ to your Tomcat directory (assuming you are installing it to Tomcat). 

Browse to localhost:8080/shelfscan

# Configuration

You may need to change the path to the log file directory as well. 

Set the datasource in context.xml for blues (SqlServer) and Oracle Voyager.

Note that the current application (running on deleon) is IP restricted. 

Adjust the IP in web.xml as necessary. Make sure that you grep for IPs in the directory and change all the IPs to the server where you are running the application, otherwise the application will overwrite the data in the production database.

# Authentication

Most pages are CAS restricted (in addition to IP restricted). There is no particular reason for that, but it can help enforce authorization for future purposes. Currently, the application only supports CAS authentication (there is no built in login mechanism). 
The application data comprises of just book scanning (inventory) reports, so it is not sensitive.

# Interface

A test version can be turned on the MacMini server in 607, and it can accessed here:

agile dot library.yale.edu:8080/shelfscan
