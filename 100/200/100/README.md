# 100 Components and Formats

## Objectives
By the end of this lesson, you will be able to:

- Describe what components are in Nexus Repository Manager.
- Explain how Nexus Repository manages components.
- Describe what formats are and which are supported in Nexus Repository Manager. 
- Determine how Nexus Repository Manager will work with components and formats in your environment. 

## What are Components
In Nexus Repository Manager, the term component describes items like a package, library, binary, container, or any other resource produced or used by your software application. In different tool-chains, components are called artifacts, packages, bundles, archives and so on. The concept and idea remains the same, and component is used to make the term more broad and encompass multiple languages.

Components provide all the building blocks and features that allow your development team to create applications. Millions of components exist and more are created every day by the open source community and proprietary vendors. It has become commonplace to build applications by combining the features of open source components with your own custom components to create an application for a specific domain. One of the many benefits of open source, component-based software development is reduction in rework. For example, if a developer builds a calendar widget and adds it to a public repository, that component can be reused without a team having to build it from the ground up, enabling efficiency within the development process.

## Component Metadata
Typically components are archive files, composed of a large variety of other files and their metadata such as:

- Java byte code in class files
- C object files
- text files e.g. properties files, XML files, JavaScript code, HTML, CSS
- binary files such as images, PDF files, sound files

The component archive files encode information for storage such as:

- Java .jar, .war, .ear file extensions
- plain .zip or .tar.gz file extensions
- package formats like nupkg, RPM, and gem
- executable formats like .exe, .sh files, or Android APK files

Many times, open source components are added to public repositories, such as the Central Repository (Maven Central) and NuGet Gallery. Components in these repositories can be accessed by various tools like package managers, build tools, and integrated developer environments (IDEs), or downloaded directly from the repository. A repository manager lets you assemble remote components and add your own internal components to create applications.

## How does Nexus Repository Manage Components?
With Nexus Repository Manager, you can manage components from development to delivery including binaries, containers, assemblies, and finished applications. In a repository manager, components are identified by a set of specific values defined by the format. For example, components from Maven use a generic set of coordinate values called group, artifact ID, and version.

Nexus Repository Manager provides built-in searches that let you easily locate and inspect component details. Searching downloaded components in the repository manager lets you access specific details such as different versions that are available and license data. This information is essential for build tool migrations, download of deployment packages, and other component-related development and operations activities. 

## What are Formats?
A repository format is a communication protocol for storing, retrieving, and indexing components and the metadata about those components. Repository formats use varying technologies to store and expose the content in them to client tools. For example, the Maven repository format relies on a specific directory structure defined by the component identifiers (GAV) and a number of XML formatted files for metadata. On the other hand, the Bower repository format is simply metadata with components stored in Git. 

All repositories store some sort of content. This content varies depending on the format, and could be anything from Docker layers and manifests to Java .jar files. In general, a format contains some package, or any other content, that can be retrieved and incorporated into a larger project like a software application in development. As noted above, formats may also store other related information like metadata about the various content contained in the format. In addition to storing and retrieving content, some formats can also act as an index of a remote repository.

## Supported Formats in Nexus Repository Manager
Most formats have a single, designated central repository maintained on behalf of the community, such as PyPI’s Python Package Index and Bower’s registry. Other formats may have one or more major alternatives. A few formats, such as Yum, do not have a central repository, but have common repositories like CentOS or Red Hat repositories. With Nexus Repository Manager, you can proxy any of these remote repositories and cache components for distribution. 

As of this publication, Nexus Repository Manager supports the following formats:

- Bower
- Docker
- git-lfs
- Maven 2
- npm
- NuGet
- PyPI
- RubyGems
- Raw (Site)
- Yum

For the latest updates, refer to [Supported Formats](https://help.sonatype.com/display/NXRM3/Supported+Formats?_ga=2.177743712.436252390.1609239928-894119647.1609239928) in the Nexus Repository Manager help site.
