

RequirementsCouncilThemesAndPriorities
======================================

Contents
--------

*   [1 Previous Versions](#Previous-Versions)
*   [2 Theme Categorization](#Theme-Categorization)
*   [3 Active Themes](#Active-Themes)
    *   [3.1 Platform Support](#Platform-Support)
        *   [3.1.1 Windows XP, 7 and Beyond](#Windows-XP.2C-7-and-Beyond)
        *   [3.1.2 Linux](#Linux)
        *   [3.1.3 Mac OS X](#Mac-OS-X)
        *   [3.1.4 Support for the latest Java(tm) versions](#Support-for-the-latest-Java.28tm.29-versions)
    *   [3.2 Rich Client Platform (RCP)](#Rich-Client-Platform-.28RCP.29)
    *   [3.3 Rich Internet Applications (RIA)](#Rich-Internet-Applications-.28RIA.29)
    *   [3.4 Embedded Device Software](#Embedded-Device-Software)
    *   [3.5 Ease Of Use](#Ease-Of-Use)
        *   [3.5.1 Improving the "Out of the Box" Experience](#Improving-the-.22Out-of-the-Box.22-Experience)
        *   [3.5.2 Maturity and Project Readiness](#Maturity-and-Project-Readiness)
    *   [3.6 Technology Trends](#Technology-Trends)
        *   [3.6.1 Cloud Computing](#Cloud-Computing)
        *   [3.6.2 Multi-Core CPU](#Multi-Core-CPU)
        *   [3.6.3 64-bit CPU](#64-bit-CPU)
    *   [3.7 Scaling Up](#Scaling-Up)
    *   [3.8 Enterprise Ready](#Enterprise-Ready)
        *   [3.8.1 Provisioning](#Provisioning)
        *   [3.8.2 Ease of Deployment, Servicability & Managability of Large Scale Installations](#Ease-of-Deployment.2C-Servicability-.26-Managability-of-Large-Scale-Installations)
        *   [3.8.3 Facilitated On-Boarding](#Facilitated-On-Boarding)
    *   [3.9 Design for Extensibility](#Design-for-Extensibility)
    *   [3.10 Consistent Multi Programming Language Support](#Consistent-Multi-Programming-Language-Support)
*   [4 Persistent & Pervasive Themes](#Persistent-.26-Pervasive-Themes)
    *   [4.1 Accessibility Compliance](#Accessibility-Compliance)
    *   [4.2 Internationalization & Localization](#Internationalization-.26-Localization)
    *   [4.3 Upgrade Path](#Upgrade-Path)
*   [5 Deferred Themes](#Deferred-Themes)
*   [6 Pending Themes](#Pending-Themes)
    *   [6.1 Vertical market-specific initiatives](#Vertical-market-specific-initiatives)
    *   [6.2 Identity (& Security) Management](#Identity-.28.26-Security.29-Management)
    *   [6.3 Extending to be Life-cycle Platform](#Extending-to-be-Life-cycle-Platform)
*   [7 Known Issues](#Known-Issues)

Previous Versions
-----------------

*   [v1 Themes and Priorities (2005)](https://www.eclipse.org/org/councils/themes.html)
*   [v2 Themes and Priorities (2006)](https://www.eclipse.org/org/councils/roadmap_v2_0/themes_v2_0.php)
*   [v3 Themes and Priorities (2007)](https://www.eclipse.org/org/councils/roadmap_v3_0/themes_v3_0.php)
*   [v4 Themes and Priorities (2008/2009)](https://www.eclipse.org/org/councils/roadmap_v4_0/themesandpriorities.html)
*   [v5 Themes and Priorities (2010)](https://www.eclipse.org/org/councils/roadmap_v5_0/themes50.php)

Theme Categorization
--------------------

Eclipse themes are described in one of four categories.

*   Active themes are those that are ongoing and changing. From time to time, some Active themes will become Persistent and Pervasive.
*   Persistent and Pervasive themes are not time or release specific. Persistent and Pervasive themes are not only a signal of importance, but permanence.
*   Deferred Themes are not an indication of priority, but are an indication that there are technical or resource inhibitors preventing them from becoming an Active Theme. Deferred themes are a signal to the ecosystem that help is needed.
*   Pending Themes are new and interesting themes that have not yet been properly explored and discussed to become an Active theme.

Active Themes
-------------

### Platform Support

While Eclipse has been very successful with Java developers on Windows systems, we endeavour to provide platform support for additional existing and upcoming platforms.

#### Windows XP, 7 and Beyond

Approximately 80% of Eclipse download requests are for the Windows OS. Windows 7 is important as both a platform used by developers, as well as one to which the resultant applications and/or products will be deployed.

Given Eclipse's ongoing use in the development of enterprise software, support for use of the Eclipse platform is desirable across the popular Windows OS variants.

#### Linux

Linux continues to grow in market share as a platform for projects at all levels. We need to offer strong support for Linux on two dimensions:

*   As a deployment platform for applications developed using Eclipse technology
*   As a platform used by developers as their primary working environment

#### Mac OS X

Mac OS X is used in many development, open source and end user environments and is a very active community. Throughout recent years there has been a stable percentage of Mac platform downloads of Eclipse packages of about 5% of downloads. Eclipse needs to continue to provide some level of support for users of this platform.

#### Support for the latest Java(tm) versions

Eclipse endeavors to support next generations of the Java platform in a timely manner. The first stage of support is that end users can build applications that target the latest JDK versions. The next stage of support is that projects themselves are able to take advantage of the latest JDK changes.

### Rich Client Platform (RCP)

RCP adoption has been strong by the ecosystem. The goal is for projects to support and use the Eclipse RCP as much as possible.

Aside from general use of RCP, there are two additional dimensions to this theme.

1.  Enabling broader use of RCP on smart devices such as PDAs and enhancing the abilities of RCP to work in these environments.
2.  Making RCP as easy as possible to use so that it's easier for application developers to adopt.

The Equinox project is an example of the focus on the OSGi component model within Eclipse. The Ecosystem requires Additional PDE enhancements to facilitate developing and deploying RCP-based applications, and for OSGi bundle manifest tooling.

### Rich Internet Applications (RIA)

Flex, Ajax and other "Web 2.0" technology (see [Wikipedia discussion on Web 2.0](http://en.wikipedia.org/wiki/Web_2.0)) has enabled the development of a new generation of web sites that provide a rich and user-friendly experience in a wide variety of applications. While the initial adopters of this technology have been social web sites, it's adoption is increasingly seen in business applications such as CRM systems.

As developers shift from the development of traditional web sites to Web 2.0-style sites, the role of Eclipse as a development framework for these applications must be considered. In order to retain these developers, the Eclipse platform could provide strong support for developing applications that leverage Web 2.0 technologies such as Flex, Ajax and Web Services APIs.

The Orion Project is an example of such technology. Orion endeavors to provide a development platform and tools for developers of RIA. More an increased investment in projects such as Orion is expected and encouraged.

### Embedded Device Software

This theme describes additions to Eclipse to provide standardization and extensibility to enable embedded tools providers, real-time operating system providers, semiconductor vendors, and hardware developers to create embedded-specific capabilities on top of standard Eclipse projects such as the Platform, JDT, eRCP, CDT, and TPTP. These capabilities could include the following.

*   Drive consistency in the workflow for embedded development tools and projects.
*   Continue evolving the debug platform API’s to support embedded debugging. This debug model will enable integration of debug engines from multiple vendors for debugging bare metal hardware, bringing up operating systems, and developing applications on single and multi-core hardware. This implementation will also enable vendors to integrate target simulation and emulation environments with Eclipse.
*   Build a remote target launching, exploring, and management framework with extensible real-time operating system visibility. This framework will provide complex launching capabilities for deploying multiple target images to multiple devices.
*   Enable C++ GUI application design, build, and deployment for mobile devices running any operating system. Also enable vendors to customize run-time libraries for their operating systems.
*   Provide mobile Java application development support for J2ME mobile profiles, including extensible frameworks for devices and emulators and capabilities for application build and deployment, code obfuscation, code optimization, image signing, and localization.
*   Enable mobile Linux application development, including design, development, debug, and deployment of cross-compiled applications.
*   Provide embedded testing capabilities - monitoring, profiling, and unit testing.

### Ease Of Use

The Eclipse components need to not only provide features that advanced users demand, but also be something that users find simple to use. The goal of this theme is to ensure that Eclipse-based products are simple to use for users with widely-varying backgrounds and skill sets performing a variety of tasks. Examples include:

*   Provide Eclipse User Experience Guidelines to ensure consistency and usability (including Accessibility) across projects.
*   Usability reviews and updates to new and existing user interfaces to streamline common processes and clarify concepts and terminology.
*   Improving support for Cheat Sheets to assist users in performing tasks.
*   User personas/roles to streamline the user interface to adapt to specific user needs.
*   Continue improvements on the Java editor towards tolerating broken code .
*   Enhanced user documentation, tutorials, white papers, demonstrations.

For example, if a user interface wizard provides a short path to performing a task, make sure that usability studies have identified the most common task performed by the target users.

#### Improving the "Out of the Box" Experience

All projects should consider improved packaging, installation and "out-of-the-box" experience to be a critical objective.

Through efforts such as the Eclipse Packaging Project, Eclipse should continue to expand out-of-the-box role-based offerings.

#### Maturity and Project Readiness

Every project has the capability to damage the reputation and brand of Eclipse if it is claimed to be "release" quality, but clearly is not. Quality refers not only to the reliable execution of typical use cases, but also to documentation, feature completeness, etc. Moreover, when new functionality or architecture replaces old between versions, it is important that features be maintained (or a plan for doing so made available) to not give the appearance of eliminating features.

### Technology Trends

Existing and new Eclipse projects need to consider key technology trends in the market to ensure that the Eclipse platform continues to retain it's leadership as the framework and tool of choice for developers.

#### Cloud Computing

More and more applications are being built to handle bursts of high volume traffic and data by making use of "cloud computing" architectures. By deploying to the "cloud", application developers are more frequently building applications to run on servers where they have little control or knowledge of the underlying technology infrastructure. In many cases this also means relying on non traditional data formats, planning for redundency and fail-over and keeping interactions low-state.

Having tools and projects that support a tools ecosystem for Cloud Computing application developers would be an enormous benefit to Eclipse.

#### Multi-Core CPU

Due to power constraints, there is a trend towards multiple cores on a CPU instead of merely increasing the CPU frequency. Eclipse could enable developers to write multi-threaded programs to take advantage of the increasing miltiple cores. Moreover, Eclipse itself could be optimized where possible for running on multiple cores.

#### 64-bit CPU

Diverse application software such as payroll, datawarehousing, and reporting now routinely manipulate large amounts of data that exceed 2GB. Using 64-bit CPUs enables these applications to manipulate large data in memory rather than having to write and read intermediate results to much slower disks.

The availability of 64-bit CPUs and matching 64-bit versions of supported OSs is growing, not only on the server but on the desktop. As these 64-bit environments become more popular and Eclipse technology-based server applications become more prevalent, Eclipse could be optimized to run within these environments and aide developers who building on, and/or targeting to, 64-bit solutions.

### Scaling Up

This refers to the need for Eclipse to deal with development and deployment on a larger and more complex scale. Increasing complexities arise from:

*   Large development teams distributed in different locations,
*   Large source code bases, large amounts of data, multiple scripting and programming languages, complex build environments that have been developed incrementally over time the dynamic nature of new source code bases and their interaction with configuration management, and build environments involving many different tool chains and build rules.
*   Large volumes of data

Possibilities:

*   Performance improvements in memory footprint, user perceived response times, and start-up times as the complexity and number of projects, files, users, and plug-ins grow (10X-100X over the next two years). This is particularly important in client/server environments where a single Solaris, AIX, Linux or HP-UX server must support dozens of concurrent Eclipse users and where Eclipse competes mostly with command line tools.
*   Improve support for and performance with Motif based window managers on Solaris (drag and drop, etc)
*   Improve remote X window performance
*   Improve performance when creating, loading, importing and closing projects with slow file systems (networks)
*   All Eclipse projects could identify common use cases and publish performance benchmarks on every milestone.
*   Ability to deal with extremely large projects and workspaces where there is a large number of developers working on different, and sometimes overlapping parts of the source tree simultaneously. This may include a more efficient way to manage multiple workspaces. Examples of large projects include Mozilla and Open Office.

### Enterprise Ready

Large organisations have a need to support large numbers of users have and maintain similar Eclipse set-ups. This could involve various aspects of the system, eg. what Eclipse components are installed, what preferences and other values are set etc. On one level this could be a convenience thing so that this would enable central management to help developer workstations be up-to-date, on a different level some organizations might want a policy of strict control where the maintenance of the environment is also about enforcing a development policy and toolset, this would need more work in that it would require Eclipse internal policy management.

#### Provisioning

Ease of installation, deployment, of pre-canned packages (or products) while allowing easy discovery and mixing-in of additional functionality. This includes not only traditional Eclipse features and plugins but could also include the ability to pick from and install various runtimes, servers, libraries, or databases. I also could include not only the initial installation by one end-user, but could also include maintenance, remote installation or management of several installations, etc.

#### Ease of Deployment, Servicability & Managability of Large Scale Installations

*   Zero-conf discovery of Update Site & Pref/Config Repositories
*   Shared Hierarchical Configuration (First-class Preferences, Perspective Configurations, Team Share Preferences, Update Site Preferences, etc.)
*   Simplified Update of the Platform Bits
*   Plug-in Cross-Dependency Awareness / Version Incompatibility
*   Improve the Eclipse project and workspace concept to allow overlapping environments
*   Ability to fit into an existing environment of source files, build artifacts and version control repositories with minimal disruption to let developers complete a full edit-compile-debug cycle in the shortest possible time. This may include better support for multiple programming languages across language toolkits for improved usability. This would also include a more flexible project model.

#### Facilitated On-Boarding

Features to enable a developer to get started as part of a (new or existing) team. This could include

1.  Making sure that the person has the correct software set-up,
2.  That the software settings are appropriate for the team and then finally (which falls outside perhaps of the above management) that the projects and the project content can be easily "bootstrapped" to the new workstation.

Example Story: _Here the ultimate goal could be that once a "team manager" has been told the IP address of a new member's PC, he would have 10 minutes later a fully configured Eclipse workstation with all the project's Eclipse project and all related settings on his/her machine._

### Design for Extensibility

Within the Eclipse community, many development projects are defining new development platforms on top of other Eclipse projects. Concrete examples include the Business Intelligence Reporting Tools, the Data Tools, and the Device Software Development Platform projects. It is recognized, however, that some function is not strictly required by the underlying projects but are important to enable other platforms to succeed. This theme also includes effort to assure platform integrity.

Some identified key requirements for this theme are:

*   Robust API documentation
*   API tools to detect use of internal interfaces
*   Expose meaningful building block APIs
*   Open the internal JDT (UI) interfaces to enable tools to seamlessly facilitate and interact with the JDT core and UI layers. For example the parsing and AST functionality.
*   Enhance the Debug API to enable seamless debugging across mixed (Java+native) languages
*   Provide a more flexible mechanism that can be used to debug non-Java programs. This is both in the debug model and presentation
*   Provide for debugging a system comprised of multiple languages
*   Enable task automation
    *   Provide access to Eclipse APIs and resources from scripting languages
    *   Provide the capability to record, edit, playback macros, representing a set of user interface actions.
*   Provide a better experience for the co-existence of offerings from multiple vendors in a single Eclipse installation
*   Permit offering brand/identity to show through (e.g. On the splash screen)
*   Allow for license management of "products" (i.e. Aggregations of features)
*   Integrated diagnostic capabilities - e.g. When a user encounters a problem, providing assistance on the where the problem originated, which product
*   Loosen the strong file orientation by providing an abstraction layer of logical objects to allow one to extend Eclipse functionality tools working at a higher abstraction level.
*   Authoring, deploying and managing components/features/etc.
    *   Bolster OSGi Adoption (via authoring assistance, etc.)
    *   Headless Execution
    *   Server-side Runtime Infrastructure
    *   Core & UI Split

### Consistent Multi Programming Language Support

The original vision of Eclipse was to accelerate the creation of IDEs. There is a lot of work to do to make it simpler to create language-specific IDEs. Our vision is to:

*   Make it easier to create language specific tools in a consistent way
*   Enabling source files written in multiple languages within the same project.

Persistent & Pervasive Themes
-----------------------------

### Accessibility Compliance

Every project could support and make a statement on their accessibility compliance. In the U.S., this means Section 508 compliance; in the European Union, this is the Web Accessibility Initiative of the World Wide Web Consortium (W3C).

### Internationalization & Localization

Every project could support both internationalization and localization:

*   Internationalization (I18N)  
    Each project could be able to work in an international environment, including support for operating in different locales and processing/displaying international data (dates, strings, etc.).
*   Localization  
    Each project could provide an environment that supports the localization of the technology (i.e. translation). This includes, but is not limited to, ensuring that strings are externalized for easy translation.

Where possible, projects should use an open and transparent process to create, maintain and deliver language packs translated into multiple languages in a timely manner. The primary languages to consider are: English, Simplified Chinese, Traditional Chinese, Japanese, French, German, Spanish.

### Upgrade Path

Upward compatibility is a critical aspect of developer satisfaction and community growth. Developers need to be able to adopt the latest release of Eclipse technology without reworking their applications. Extensive rework incurred during a migration will lead to developer frustration and the possibility that they will evaluate and adopt other tools. Smooth upward migration is therefore a core Theme that all projects must consider.

This includes:

*   Assuring release-to-release migration is supported (e.g., resources, workspaces, API, as appropriate).
*   Assuring API compatibility release-to-release, including testing for upward compatibility
*   Clear statements indicating which APIs are intended for internal use only (and are not guaranteed to be upward compatible)
*   Providing tools that automate the migration process where possible

Deferred Themes
---------------

None currently.

Pending Themes
--------------

These items will need more investigation before they can be described and prioritized effectively.

### Vertical market-specific initiatives

With the establishment of Eclipse as a dominant platform for building tools and applications, it is logical that Eclipse technology begin to play a major role in vertical industry initiatives. Vertical markets should not be confused with Technology Segments where Eclipse technology is generally consumed very rapidly. Examples of quick Eclipse adoption in new technology segments include Ajax and other Web2.0 tools and applications. Vertical markets are much more solutions oriented and have broad reach into a technology stack. The Eclipse projects should be aware that Eclipse is becoming a major player in the Healthcare and Automotive verticals, and there are signs of it becoming a key platform in a number of other verticals. In Automotive, for example, Eclipse based technology is used in CAD tools, workflow tools, embedded design tools, etc.

### Identity (& Security) Management

*   KeyStore
*   JAAS
*   JCA
*   SAML
*   Federated Identity
*   SSO (Single Sign-On)

### Extending to be Life-cycle Platform

TBD

Known Issues
------------

*   Linux Localization Lacking
*   Mac OS X Cocoa
*   Mac OS X Carbon Accessibility (S 508 compliance) and I18N/L10N

*   PM
    *   Cross-Project Coordination of UX
    *   Eclipse.org to Sponsor Independent UX Focus Groups?

*   My 1st Week w/ Eclipse
    *   How can we encourage downloaders to become dedicated users?
    *   Focus on the "majority user" personas and their use cases.
    *   "That first mile"

The individual projects are great at delivering new features and improved capabilities, but access to these features is gated by the experience that an individual already has with the project providing the features. For example, <<insert cool but esoteric JDT feature here that you wouldn't know about unless you religiously read the What's New for the JDT for each release>>.

"My 1st Week with Eclipse" is a theme that asks the projects to consider the new downloader who may be evaluating Eclipse to help them with the typical work-- and then create assistive assets-- "wizards", forms, cheat sheets and other (already present) usability features, to assist those new users during their evaluation.

This body of "typical work" will most often take the form of a set of use cases or scenarios, that can be facilitated by hard-to-miss assistive assets.

Sadly, the use of Welcome Page content is deemed too easy to gloss over, and many people never find the cheat sheets. A typical initial interaction with Eclipse is that users disable the Welcome Page, and frequently close any residual documentation Views and set-about the work of solving some specific problem (such as debugging a web app, creating a web app, writing code, running unit tests, etc.).

Measures need to be taken to bring the assistive assets back into the field-of-view of even these users. Concern for the much-maligned Microsoft(tm) "Clippy(tm)" metaphor needs to be considered here too, as the goal is not to create an obtrusive experience-- but a "sticky" one, where users will be enabled to "keep using eclipse" and develop a rapport with Eclipse that will lead them to discover the less common and more valuable aspects of the platform.

*   *   As a JEE developer
    *   As a PHP developer


(Migrated from [https://wiki.eclipse.org/RequirementsCouncilThemesAndPriorities](https://wiki.eclipse.org/RequirementsCouncilThemesAndPriorities))