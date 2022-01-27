### What is Maven ?
--> It is product of apache<br>

--> All the open source communities  like  Jenkins, tomcat, mysql etc upload their updated API's into maven global server ( search.maven.org )<br>

--> Developers  connect to  the maven global server, download those<br>

--> API  that are necessary for the project development and store them in  Maven local repository<br>

--> All  developers connect   to  maven local repository and perform the development activity<br>

--> In this way, the code is stored separately in github. and API's required for code development are stored in maven local repository<br>

--> This will help in protecting the code from any threats/viruses that might be present in the  API's<br>

--> <b>Maven  is also a build tool. Where it can compile the programs and create an artifact</b>

### Maven's Objectives

<b>Maven's primary goal is to allow a developer to comprehend the complete state of a development effort in the shortest period of time. In order to attain this goal, Maven deals with several areas of concern:</b><br>

1.Making the build process easy<br>
2.Providing a uniform build system<br>
3.Providing quality project information<br>
4.Encouraging better development practices<br>

### What is an artifact
An artifact is a file, usually a JAR, that gets deployed to a Maven repository. A Maven build produces one or more artifacts, such as a compiled JAR and a "sources" JAR. Each artifact has a group ID (usually a reversed domain name, like com. example. foo), an artifact ID (just a name), and a version string
