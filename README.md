shelfscan
=========

# Installation Steps

Clone this repo.
Clone yalelibrary/accservices
Clone yalelibrary/accservices-web

Import all three projects into IntelliJ Idea (or your favorite IDE).

Run 

```
cd shelfscan
mvn clean install -P prod
```

Copy the war file in accservices-web/target/ to your Tomcat directory. 

# Configuration

Adjust web.xml as necessary. Set the datasource in context.xml for blues and Oracle Voyager.
