Maven Archetypes
================

This repository contains maven [archehtypes] (http://maven.apache.org/guides/introduction/introduction-to-archetypes.html)
i.e. templates, for creating new projects.

The archetypes currently available are:

    java-quickstart:  java, junit, mockito, hamcrest

Usage
=====

\# Checkout project<br/>
$ git clone git@github.com:aem999/archetypes.git

\# Change into project directory<br/>
$ cd archetypes

\# Build archetypes and install into the local maven repository<br/>
$ mvn install

\# Check that the archetypes have been added to the local archetype catalogue (which resides in your .m2 directory)<br/>
$ cat $USERPROFILE/.m2/archetype-catalog.xml

\# Create a new project using the archetype (follow the prompts)<br/>
$ mvn archetype:generate -DarchetypeCatalog=local

Example output:

    $ mvn archetype:generate -DarchetypeCatalog=local
    [INFO] Scanning for projects...
    [INFO]
    [INFO] ------------------------------------------------------------------------
    [INFO] Building Maven Stub Project (No POM) 1
    [INFO] ------------------------------------------------------------------------
    [INFO]
    [INFO] >>> maven-archetype-plugin:2.2:generate (default-cli) @ standalone-pom >>>
    [INFO]
    [INFO] <<< maven-archetype-plugin:2.2:generate (default-cli) @ standalone-pom <<<
    [INFO]
    [INFO] --- maven-archetype-plugin:2.2:generate (default-cli) @ standalone-pom ---
    [INFO] Generating project in Interactive mode
    [INFO] No archetype defined. Using maven-archetype-quickstart (org.apache.maven.archetypes:maven-archetype-quickstart:1.0)
    Choose archetype:
    1: local -> com.aem999:java-quickstart (Java project with junit, hamcrest and mockito dependencies)
    Choose a number or apply filter (format: [groupId:]artifactId, case sensitive contains): : 1
    Define value for property 'groupId': : com.aem999
    Define value for property 'artifactId': : myapp
    Define value for property 'version':  1.0-SNAPSHOT: :
    Define value for property 'package':  com.aem999.myapp: :
    Confirm properties configuration:
    groupId: com.aem999
    artifactId: myapp
    version: 1.0-SNAPSHOT
    package: com.aem999.myapp
     Y: : Y
    [INFO] ----------------------------------------------------------------------------
    [INFO] Using following parameters for creating project from Archetype: java-quickstart:1.0
    [INFO] ----------------------------------------------------------------------------
    [INFO] Parameter: groupId, Value: com.aem999
    [INFO] Parameter: artifactId, Value: myapp
    [INFO] Parameter: version, Value: 1.0-SNAPSHOT
    [INFO] Parameter: package, Value: com.aem999.myapp
    [INFO] Parameter: packageInPathFormat, Value: com/aem999/myapp
    [INFO] Parameter: package, Value: com.aem999.myapp
    [INFO] Parameter: version, Value: 1.0-SNAPSHOT
    [INFO] Parameter: groupId, Value: com.aem999
    [INFO] Parameter: artifactId, Value: myapp
    [INFO] project created from Archetype in dir: C:\dev\workspace\myapp
    [INFO] ------------------------------------------------------------------------
    [INFO] BUILD SUCCESS
    [INFO] ------------------------------------------------------------------------
    [INFO] Total time: 32.163s
    [INFO] Finished at: Thu May 03 09:53:07 CST 2012
    [INFO] Final Memory: 8M/20M
    [INFO] ------------------------------------------------------------------------
