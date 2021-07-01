<h1 align="center"> Application Basics </h1>

### JAVA Introduction

+ Free and open-source
+ java -version : to check the  current version of java.

#### Java Development Kit (JDK)

JDK is set of tools that will help to develop, build and run java application on system.

+ Develop
	* jdb : It is debugger tool, which is to debug the java code.
	* javadoc : It is tool to document the application source code.
	
+ Build
	* javac : It is tool, which is to build and compile the application once the source code is developed.
	* jar - The tool is to help archive the code in related libraries into single file.
	
+ Run
	* JRE (Java Runtime Environment) : It is needed to run Java application on any system.
	* Java command-line utility or loader : It is used to run the application.

### JAVA Build & Packaging

jar (Java Archive) helps compress and combine multple java.class files and dependent libraries and assets into single distrubutable packages. <br />
Syntax : jar cf <FILE_Name>.jar <File 1> <File 2>.............. <File N>

	+ To run jar file use the command <br />
		java -jar <File_Name>.jar

war (Web archive) : convert static files and images in web applications into packages.

### Node JS  Introduction

Node.js is a server-side Java Script environment,that can be used to develop application.

+ Free and open-source
+ node -v : to check the  current version of Node.js

### Node JS - NPM

NPM (Node package Management) allows developers to develop new reusable packages or modules and share on the public repository.

+ npm -v : to check the version of NPM CLI utility.
+ npm search <PACKAGE> : to search for packages.
+ npm install <PACKAGE> - to install package
+ npm -e "console.log(module.paths)" : it will list all the path node would look at while importing package.

There are two type of Modules.

*  Built-In Module : Which are installed automatically when Node.js runtime is installed and it is located in user/lib/node_modules on Linux Systems.

Some Built-In Modules <br />

| | Built-In Modules |
|---- | ----------|
| fs | To handle filesystem |
| http | To host an HTTP server |
| os | To work with the Operating system |
| events | To handle events |
| tls | To implement TLS and SSL |
| url | To Parse URL Strings |

* External Modules : Which needs to be installed externally using npm install <PACKAGE>.

Some External Modules <br />

| | External Modules |
|---- | ----------|
| express | Fast, unopinioated, minimalist web framework |
| react | To create user interfaces |
| debug | To debug applications |
| asynch | To work with asynchronous JS  |
| lodash | To Work with arrays, objects, Strings etc.|

### Python  - pip

Pip ( Python package manager ) is a tool install modules in python.

* pip --version : to check version of PIP 
* pip uninstall <PACKAGE?NAME)-  to uninstall the package
* pip list - to list the installed package in system
* pip install -r requirements.txt - to install list of modules in python, thelist will be save in requirements.txt
		


### Labs

1. Java Introduction : Debuging, compilation and running java application.
2. Java - jars : Question related the archieve, compressing the java application.
3. Java - Build & Package : Building, Packaging the java applications.
4. Node.js - Introduction : Basic Node.js question
5. Node JS -NPM - checking the version of npm, searching and Installing external packages using npm etc.
6. Python  - pip : Installing packages using pip, maintaining the list of modules in requirements.txt etc.