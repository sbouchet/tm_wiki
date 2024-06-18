

DSDP/TM/Board Report 2008
=========================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

**This is the proposed Report for the [Target Management](https://www.eclipse.org/dsdp/tm) project, to be presented to the Eclipse Board on September 17, 2008.**

* * *

  

Contents
--------

*   [1 Review of project scope and charter](#Review-of-project-scope-and-charter)
*   [2 A high-level review of technical progress, strategy and release plans.](#A-high-level-review-of-technical-progress.2C-strategy-and-release-plans.)
*   [3 Self-assessment of the performance of the project](#Self-assessment-of-the-performance-of-the-project)
    *   [3.1 Performance as an Eclipse open source project](#Performance-as-an-Eclipse-open-source-project)
        *   [3.1.1 Openness](#Openness)
        *   [3.1.2 Transparency](#Transparency)
        *   [3.1.3 Meritocracy](#Meritocracy)
        *   [3.1.4 Diversity](#Diversity)
        *   [3.1.5 Compliance with the Purposes (e.g. are they successfully “..supplying frameworks and exemplary, extensible tools..”?)](#Compliance-with-the-Purposes-.28e.g.-are-they-successfully-.E2.80.9C..supplying-frameworks-and-exemplary.2C-extensible-tools...E2.80.9D.3F.29)
    *   [3.2 End user community and adoption.](#End-user-community-and-adoption.)
    *   [3.3 Commercial community and adoption. E.g. is the technology from the project showing up in products.](#Commercial-community-and-adoption.-E.g.-is-the-technology-from-the-project-showing-up-in-products.)
*   [4 Compliance with the Roadmap](#Compliance-with-the-Roadmap)
*   [5 Board Assistance](#Board-Assistance)
*   [6 Noteworthy](#Noteworthy)

Review of project scope and charter
-----------------------------------

Original TM [Mission Statement](https://www.eclipse.org/dsdp/tm/about.php): _The Target Management project creates data models and frameworks to configure and manage remote systems, their connections, and their services_. The work on "data models" as well as "configuring" remote systems is currently underrepresented, but being discussed. I do not see a need to revise the charter at this point.

A high-level review of technical progress, strategy and release plans.
----------------------------------------------------------------------

As outlined on the [project plan](https://www.eclipse.org/projects/project_summary.php?projectid=dsdp.tm), much work is currently centered on maintenance and gradual improvements of the Remote System Explorer (RSE). This work is based on much legacy: some architectural structures in RSE would need more radical changes, but resources for doing so lack and commercial product requirements dictate mostly staying with these structures. Also, the focus is more on TCP/IP based communications as well as usable tooling for file transfer, than deeply embedded targets. Release Engineering and Unit tests are not as full-fledged as desirable, though improving.

At the same time, there is much and very good Community involvement bringing in new ideas, patches and features such as the recent Windows CE integration.

Some new initiative is ongoing with the [Target Communication Framework (TCF)](/DSDP/TM/TCF_FAQ "DSDP/TM/TCF FAQ"). This is centered around the connection and communication protocols for embedded systems specifically, well designed with Community interaction and looks very promising. Collaboration with other Eclipse projects (ECF, DTP, E4) is on the way for improved architectures. Perhaps in the context of [E4/Connection Frameworks](/E4/Connection_Frameworks "E4/Connection Frameworks"), some new and better base architectures are going to evolve together with these other projects.

We're releasing on the yearly coordinated maintenance trains.

Self-assessment of the performance of the project
-------------------------------------------------

_under the following headings (inspired by the Three Communities section of the Development Process):_

### Performance as an Eclipse open source project

Community adoption is great, and we have won new contributors and committers for increased diversity and growth. In terms of Process, the TM project has always been at the forefront of adopting EMO proposed processes (such as the XML [Development Resources/Project Plan](/Development_Resources/Project_Plan "Development Resources/Project Plan") recently).

#### Openness

TM is open to external observers and participants. The large number of [Community Contributors](https://www.eclipse.org/dsdp/tm/development/contributors.php) as well as our open, and inviting [TM and RSE FAQ](/TM_and_RSE_FAQ "TM and RSE FAQ"), documentation and [TM Future Planning](/TM_Future_Planning "TM Future Planning") process show this.

#### Transparency

All our work is documented using the standard Eclipse tools, mailing list, project plan, Bugzilla, IP Zilla, and SVN/CVS commit logs.

#### Meritocracy

We evaluate feature proposals on technical merit, and all participants on the TM committer team have equal voice in the discussions. Contributors have promoted to Committer status based on public review of their contributions.

#### Diversity

Wind River and IBM are driving the project with 40% of committers each. Montavista and ProSyst have 1 committer each. Contributors come from many different companies.

#### Compliance with the Purposes (e.g. are they successfully “..supplying frameworks and exemplary, extensible tools..”?)

Yes: The TM Tooling is used a lot by the Eclipse Community for accessing remote systems, and Community interaction shows that the frameworks are also used to build differentiated commercial applications:

*   The RSE Framework comes with dstore, ssh, ftp, telnet and wince connection plugins as exemplary tools for remote file, process, shell and terminal access.
*   The Terminal Widget comes with exemplary ssh, telnet and serial line connection plugins.
*   The TCF Frameowrk comes with exemplary tools for remote file access on top of RSE, and remote debugging on top of Platform-Debug and DD-DSF.

### End user community and adoption.

Mostly the FTP and SSH offerings for remote file access are adopted by end users, and have led to journal articles covering the project from an end-user point of view. In spite of constant improvements, bug backlog is still an issue.

### Commercial community and adoption. E.g. is the technology from the project showing up in products.

The project is being adopted by at least 6 commercial offerings (MontaVista, Atmel, IBM, EMAC, Wind River, Motorola), which have been metioned in press releases [2008](https://www.eclipse.org/org/press-release/20080415_embedded.php) and [2007](https://www.eclipse.org/org/press-release/20070403embedded.php). More companies have expressed interest in picking up the project or parts of it, or use it internally but don't want to be mentioned officially.

Compliance with the Roadmap
---------------------------

We are currently very well aligned and have a road map to take the project through August 2009.

Board Assistance
----------------

The [DSDP/Package](/DSDP/Package "DSDP/Package") effort, which is loosely related to the project, may probably need some help from an IP / Licensing / Distribution point of view.

Noteworthy
----------

The [PTP Remote Development Tools](/PTP/designs/remote "PTP/designs/remote") effort has expressed interest in taking over the RSE component from TM, or extract RSE as a component separate from TM with a different name. The RDT folks are using parts of the technology, but there is surprisingly little to no communication between them and the TM project team.


(Migrated from [https://wiki.eclipse.org/DSDP/TM/Board_Report_2008](https://wiki.eclipse.org/DSDP/TM/Board_Report_2008))