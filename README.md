This project allows you to start/debug NiFi within your IDE, essentially allowing you to set breakpoints etc.

The project uses Gradle for dependency management and build.


From the root of the project execute the following command:

```./gradlew clean eclipse``` - for Eclipse
```./gradlew clean idea``` - For IntelliJ

This will generate all necessary Eclipse/Idea files. Now you can import the project into your workspace as "regular project" (not Maven, not Gradle).
For example, for Eclipse follow these directions.

```File -> Import -> General -> Existing project into workspace```

Once project is imported you need to set its working directory to point to NiFi installation. For example in Eclipse click on the little black arrow to the right of 'Run' and then 
'Run Configurations -> (right click) Java Aplication -> New
Project Name : nifi-ide-integration
Main Class: org.apache.nifi.NiFi

Switch to Arguments tab and the location of your NiFi installation home as "Working Directory"

That is it. You can "Run" or "Debug" it. 




