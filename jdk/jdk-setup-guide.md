#JDK Setup Reference Guide
![](images/java.jpg) 

You must start by installing a Java Virtual Machine (JVM) to run Java programs and also the Java Development Kit that brings the java compiler as well as other tools required to develop Java programs. It is recommended that you set up **Oracle JDK (v1.7.0_51)** that will provide  the JDK along with the JVM.

## Dependencies

* Download [**Oracle JDK JDK (v1.7.0_51)**](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html). Choose the correct version for your Operating System (don't forget: x86 stands for 32 bits).
* Download the [**Oracle Java API documentation**](http://www.oracle.com/technetwork/java/javase/documentation/java-se-7-doc-download-435117.html)

## Installation
* Run the downloaded setup installation file
* Install under de name `JavaXX`, where *XX* is a number that identifies the version of the JDK.  
It is important to follow this rule so that multiple java versions can coexist. For example Java 1.6 should be installed on `java16` and Java 1.7 should be installed on `Java17`.  
On Windows avoid installing on a directory with spaces on the name. A good option is installing on `c:/Java/JavaXX`.

## Configuration
* Configure a system variable `JAVA_HOME` to point to to the directory where the JDK was installed.
* Add the binary directory `$JAVA_HOME/bin` to the `PATH` environment variable (`%JAVA_HOME%/bin` for Windows).
* Install the documentation by uncompressing the documentation file and moving it to `$JAVA_HOME/docs`.

## Checking the installation
Open a command shell and execute `java -version` then `javac -version` and finally `javadoc`. The first two commands should return the current version of the tools. The last command should print the correct usage of the command.

* `java` is used to run Java programs (.class files);

		$$java -version
		java version "1.6.0_26"
		Java(TM) SE Runtime Environment (build 1.6.0_26-b03)
		Java HotSpot(TM) Client VM (build 20.1-b02, mixed mode, sharing)

* `javac` is used to compile Java source files (.java);
	
		$$javac -version
		javac 1.6.0_26
	
* `javadoc` is used to generate html documention based on javadoc comments in the source files.
		$$javadoc
		javadoc: error - No packages or classes specified.
		usage: javadoc [options] [packagenames] [sourcefiles] [@files]
		-overview <file>          Read overview documentation from HTML 
