#### Allows you to start/debug NiFi within your IDE, essentially allowing you to set breakpoints etc.

The project uses Gradle for dependency management and build which means it will self-provision if you don't have it therefore below directions shoudl work without any pre-requisites. 

From the root of the project execute the following command:

```./gradlew clean eclipse``` - for Eclipse

```./gradlew clean idea``` - For IntelliJ

This will generate all necessary Eclipse/Idea files. Now you can import the project into your workspace as _regular project_ (not Maven, not Gradle).
For example, for Eclipse follow these directions:

```File -> Import -> General -> Existing project into workspace```

Once project is imported you need to set its _Working Directory_ to point to the root of NiFi installation. For example in Eclipse click on the little black arrow to the right of _Run_ and then:

```Run Configurations -> (right click) Java Aplication -> New```

_Project Name:_ - ```nifi-ide-integration```

_Main Class:_ - ```org.apache.nifi.NiFi```

Switch to _Arguments_ tab and enter the location of your NiFi installation as 'Other' in _Working Directory_ section.

One last thing is to add sources

Switch to _Source_ tab ```Add -> External System Directory``` and browse to the root of your NiFi clone.

That is it. You can "Run" or "Debug" it. 




