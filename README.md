shelfscan
=========

# Installation Steps

Clone this repo.
Clone yalelibrary/accservices
Clone yalelibrary/accservices-web

Import all three projects into IntelliJ Idea (or your favorite IDE). Make sure all the standard Java dependecies are installed (JDK, Maven).

Run these steps:

```
cd shelfscan
mvn clean install -P prod
```

Copy the war file in accservices-web/target/ to your Tomcat directory. 

Go to localhost:8080/shelfscan

# Configuration

Adjust web.xml as necessary. Set the datasource in context.xml for blues (SqlServer) and Oracle Voyager.

The current application (running on deleon) is IP restricted. 
