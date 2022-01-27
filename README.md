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

An artifact is a file, usually a JAR, that gets deployed to a Maven repository. A Maven build produces one or more artifacts, such as a compiled JAR and a "sources" JAR.<br>
Each artifact has a group ID (usually a reversed domain name, like com. example. foo), an artifact ID (just a name), and a version string.

### What is POM

POM stands for "Project Object Model".<br>
It is an XML representation of a Maven project held in a file named pom.xml.<br>
When in the presence of Maven folks, speaking of a project is speaking in the philosophical sense, beyond a mere collection of files containing code.<br>
A project contains configuration files, as well as the developers involved and the roles they play, the defect tracking system, the organization and licenses, the URL of where the project lives, the project's dependencies, and all of the other little pieces that come into play to give code life.<br>
It is a one-stop-shop for all things concerning the project. In fact, in the Maven world, a project does not need to contain any code at all, merely a pom.xml.

### Maven Coordinates

The POM defined above is the bare minimum that Maven allows. groupId:artifactId:version are all required fields (although, groupId and version do not need to be explicitly defined if they are inherited from a parent - more on inheritance later). The three fields act much like an address and timestamp in one. This marks a specific place in a repository, acting like a coordinate system for Maven projects:<br>

<b>groupId:</b> This is generally unique amongst an organization or a project. For example, all core Maven artifacts do (well, should) live under the groupId org.apache.maven. Group ID's do not necessarily use the dot notation, for example, the junit project. Note that the dot-notated groupId does not have to correspond to the package structure that the project contains. It is, however, a good practice to follow. When stored within a repository, the group acts much like the Java packaging structure does in an operating system. The dots are replaced by OS specific directory separators (such as '/' in Unix) which becomes a relative directory structure from the base repository. In the example given, the org.codehaus.mojo group lives within the directory $M2_REPO/org/codehaus/mojo.<br>

<b>artifactId:</b> The artifactId is generally the name that the project is known by. Although the groupId is important, people within the group will rarely mention the groupId in discussion (they are often all be the same ID, such as the MojoHaus project groupId: org.codehaus.mojo). It, along with the groupId, creates a key that separates this project from every other project in the world (at least, it should :) ). Along with the groupId, the artifactId fully defines the artifact's living quarters within the repository. In the case of the above project, my-project lives in $M2_REPO/org/codehaus/mojo/my-project.<br>

<b>version:</b> This is the last piece of the naming puzzle. groupId:artifactId denotes a single project but they cannot delineate which incarnation of that project we are talking about. Do we want the junit:junit of 2018 (version 4.12), or of 2007 (version 3.8.2)? In short: code changes, those changes should be versioned, and this element keeps those versions in line. It is also used within an artifact's repository to separate versions from each other. my-project version 1.0 files live in the directory structure $M2_REPO/org/codehaus/mojo/my-project/1.0.<br>

The three elements given above point to a specific version of a project, letting Maven know who we are dealing with, and when in its software lifecycle we want them.

### Maven Packaging

<b>Now that we have our address structure of groupId:artifactId:version, there is one more standard label to give us a really complete what: that is the project's packaging. In our case, the example POM for org.codehaus.mojo:my-project:1.0 defined above will be packaged as a jar. We could make it into a war by declaring a different packaging:</b><br>

When no packaging is declared, Maven assumes the packaging is the default: jar.<br>
The valid types are Plexus role-hints (read more on Plexus for a explanation of roles and role-hints) of the component role org.apache.maven.lifecycle.mapping.LifecycleMapping.<br>
The current core packaging values are: pom, jar, maven-plugin, ejb, war, ear, rar. These define the default list of goals which execute on each corresponding build lifecycle stage for a particular package structure: see Plugin Bindings for default Lifecycle Reference for details.

### What are Maven Plugins

Maven is actually a plugin execution framework where every task is actually done by plugins.<br>

A plugin generally provides a set of goals.<br>

<b>Maven Plugins are generally used to − </b>

===> create jar file<br>
===> create war file<br>
===> compile code files<br>
===> unit testing of code<br>
===> create project documentation<br>
===> create project reports<br>

### Plugin Types
<b>Build plugins</b><br>
They execute during the build process and should be configured in the <build/> element of pom.xml.

<b>Reporting plugins</b><br>
They execute during the site generation process and they should be configured in the <reporting/> element of the pom.xml.

### What is SNAPSHOT?

SNAPSHOT is a special version that indicates a current development copy. Unlike regular versions, Maven checks for a new SNAPSHOT version in a remote repository for every build.<br>

Now data-service team will release SNAPSHOT of its updated code every time to repository, say data-service: 1.0-SNAPSHOT, replacing an older SNAPSHOT jar.<br>






