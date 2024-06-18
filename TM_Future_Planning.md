

TM Future Planning
==================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP") | [TM](./TM "DSDP/TM")

Collect input for the planning process for next year's DSDP Target Management Release (**Eclipse Ganymede train, tentatively TM 3.0, June 2008**) as well as the upcoming service releases (DSDP-TM 2.0.x). Goals of this page are

*   Collect ideas and Requirements for Target Management Ganymede and beyond
*   Find out who needs what features
*   Find out who would be willing to work on what

**This is a collaborative Wiki**, so everyone in the community is welcome to contribute to the discussion by simply modifying the page. **Please sign up by declaring your interest or willingess to contribute** on the individual items below. Our Themes and Priorities need to be aligned with the global and DSDP [Requirements](https://wiki.eclipse.org/RequirementsCouncil06TP#Embedded_Device_Software "RequirementsCouncil06TP"). As soon as a feature description is sufficiently clear and there is some group supporting a feature, Bugzilla entries should be used for tracking requests. When finalizing the plan, bugzilla plan items will be created for grouping related work items together in order to track them.

An initial plan was discussed in the [Committer Phone Meeting on 22-May-2007](./Committer_Phone_Meeting_22-May-2007 "DSDP/TM/Committer Phone Meeting 22-May-2007").

More discussions will be at the [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007").

Contents
--------

*   [1 TM 2.0.x Planning](#TM-2.0.x-Planning)
*   [2 TM 3.0 (Ganymede) Planning](#TM-3.0-.28Ganymede.29-Planning)
    *   [2.1 Bugzilla Plan Input](#Bugzilla-Plan-Input)
    *   [2.2 Planning and Priorities](#Planning-and-Priorities)
    *   [2.3 Themes and Proposals](#Themes-and-Proposals)
        *   [2.3.1 **Theme: Scaling Down**](#Theme:-Scaling-Down)
        *   [2.3.2 **Theme: Be a Better Framework**](#Theme:-Be-a-Better-Framework)
        *   [2.3.3 **Theme: Integrate other remote access solutions** (strong should have)](#Theme:-Integrate-other-remote-access-solutions-.28strong-should-have.29)
        *   [2.3.4 **Theme: Add unique new features**](#Theme:-Add-unique-new-features)
        *   [2.3.5 **Theme: Multicore / Multisystem support**](#Theme:-Multicore-.2F-Multisystem-support)
    *   [2.4 Other ideas carried forward](#Other-ideas-carried-forward)
*   [3 Archive of previous plans](#Archive-of-previous-plans)
    *   [3.1 TM 2.0 (Eclipse Europa, June 2007)](#TM-2.0-.28Eclipse-Europa.2C-June-2007.29)
    *   [3.2 TM 1.0 (Fall 2006)](#TM-1.0-.28Fall-2006.29)

TM 2.0.x Planning
-----------------

*   TM 2.0.1 and 2.0.2 to be aligned with [Europa Simultaneous Release](https://wiki.eclipse.org/Europa_Simultaneous_Release "Europa Simultaneous Release") Service Releases in autumn and spring 08 respectively
    *   No major feature additions; focus on unit tests, ISV Docs
        *   Probably adding RSE Terminal integration
*   Work on unittests, isv docs over the summer can also be done in HEAD, forking off the mainline in autumn
    *   if we have any large things for 3.0 and want to start before 2.0.1 might do that in a branch; but having the branch this or that way is not a big deal

TM 3.0 (Ganymede) Planning
--------------------------

### Bugzilla Plan Input

*   Query Information
    *   The following bugzilla queries cover non-overlapping distinct requests that we currently have in the queue.
    *   Bugs lists are sorted by importance, with the more important ones (i.e. higher priority or severity) first.
    *   Target milestone "Future" is used for bugs that have been discussed and deferred.
    *   Target milestone "---" is uesd for bugs not yet analyzed or discussed.
*   Bugzilla Queries
    *   TM [All Open API Bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi%5D&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&order=Importance) (25 bugs on 10-Jul-2007)
    *   TM [Non-API Enhancement Requests deferred to the Future](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&target_milestone=---&target_milestone=Future&keywords_type=nowords&keywords=api&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=enhancement&cmdtype=doit&order=Importance) (93 bugs on 10-Jul-2007)
    *   TM [Bugs deferred to the Future](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&target_milestone=---&target_milestone=Future&keywords_type=nowords&keywords=api&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&bug_severity=normal&bug_severity=minor&bug_severity=trivial&cmdtype=doit&order=Importance) (108 bugs on 10-Jul-2007)

### Planning and Priorities

*   We have consensus to work towards TM 3.0 for Ganymede (rather than 2.1) so we'll allow API changes but keep them as small as possible. However, "getting things right" is agreed to be more important than being backward compatible.
*   Discussion and finalization of priorities into plan items will be at the [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./Face-to-face_Meeting_Toronto_17-Sep-2007).
*   **Top 10 Priorities:**
    *   1 - (All) **Quality**, Maintenance, Reduce bug backlog. Add unit tests. Clean up old implementations, get rid of obsolete code.
        *   1a - (WR, IBM) **Improve UI**, Adhere to Guidelines, Better Wizard UI, Componentize connection/subsystem/services
    *   2 - (IBM, WR) **Componentize**: UI/Non-UI splitting, avoid unnecessary plugin activation, support RCP
    *   3 - (IBM) **Team Support**: Provide Import/Export of RSE Profiles by XML, provide UI for working with Profiles
    *   4 - (IBM) Contribute IBM **User Action** Framework
    *   5 - (WR) Contribute **Target Communication Framework (TCF)** Agent
    *   6 - (WR) Improve Remote CDT Launch; integrate remote CDT build
    *   7 - (WR, IBM) Improve **Platform Integration**: Drag&Drop ([SWT:196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176)), Command/Handler, Avoid Platform "internal" access, keyboard shortcuts; Improve EFS; Contribute Welcome content; Credentials Management via upcoming Platform JAAS support ([196445](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196445))
        *   Especially driving EFS forward can be important wrt community building - discussing caching / rsync facilities for EFS
    *   8 - (WR, IBM) **Finalize / Clean up APIs**, making them maintainable from 3.0 without API breakage
    *   9 - (Contributors) **Integrating** other remote access solutions - ECF, Platform/Team Synchronization API, WebDAV, Wicked Shell, TPTP, JArchive; important for community building
    *   10 - (WR) Features for **Multi-Core / Multisystem**; flexible grouping of connections / items; investigate collaboration with PTP
*   **"Might Have" Themes and Proposals (Interesting but probably not enough time)**
    *   Finalize Terminal APIs
    *   Generic Filtering Framework / Generic monitoring APIs (possibly related to TCF)
    *   Launch Actions
    *   Remote Lab Manager Integrations
    *   Shell Pattern Matching

### Themes and Proposals

*   In the list of themes below, typically those themes or work items that we feel to be more important appear first. Not all items of a theme may be addressed, especially those appearing further down in the list for a theme would typically receive less attention.
*   Naturally those themes will be carried on first that have most interested parties, and where those interested parties actually contribute code, patches or committers.
*   **Community members can influence the planning process by declaring their interest, and/or especially declaring their willingness to contribute work on the themes.**
*   Contribute: items below do not yet indicate a committment to actually contribute but do declare willingess of the signed up parties.

#### **Theme: Scaling Down**

*   Interest: IBM, WR
*   Contribute: IBM, WR (committers)
*   Further improve UI/Non-UI splitting, supporting
    *   (a) RSE as an EFS provider without having to start up
    *   (b) Remote file export in headless applications
*   Improve usage of the extension registry:
    *   (a) Avoid plugin startup where not necessary - improve initial startup performance
    *   (b) Make plugin registration dynamic, allowing dynamic reconfiguration (registry trackers etc: might be a requirement for the future provisioning story)
*   Improve Componentization:
    *   (a) Support RCP, allowing the use of RSE even if Resources do not exist
    *   (b) Provide a shortcut to RSE Services layer without Subsystems - probably via OSGi Services; might help EFS provider
*   Potentially move to Platform + 0 level --> move CDT Launcher to CDT Project

  

#### **Theme: Be a Better Framework**

*   Interest: WR, IBM, Symbian
*   Contribute: WR, IBM, Symbian (committers)
*   **Improve Quality, Maintainability, strive for small and efficient implementations**
    *   Most important point for IBM and WR
    *   Increase Unit Test Coverage
    *   Do unit tests with a GUI Recorder e.g. TPTP AGR
    *   Reduce the Bug backlog
    *   Collaborate with DSDP-DD and Platform/Debug for a cleaned-up SystemView solution
*   Increase the flexibility of the host/subsystem/service combination after connection creation
    *   Improved more flexible wizards; allow adding and removing services as needed; Inheritable Properties for configuring subsystems
    *   Improved Wizard UI ([176490](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176490), [142493](https://bugs.eclipse.org/bugs/show_bug.cgi?id=142493), [192758](https://bugs.eclipse.org/bugs/show_bug.cgi?id=192758))
*   **Better live with the Platform**
    *   Make use of the Platform Command/Handler framework, including parameterized handlers, to all user-defined keyboard shortcuts, extender modifiable UI and macro recording (eventually)
    *   Contribute Welcome content, [https://www.eclipse.org/eclipse/platform-ua/documents/intro\_3\_3_features.html](https://www.eclipse.org/eclipse/platform-ua/documents/intro_3_3_features.html)
    *   Get rid of Platform Discouraged access ("internal")
*   **Connection Sharing and Team Support**
    *   Import/Export RSE Profiles; A must-have for IBM
*   **Finalize Terminal APIs**
    *   Contribute Terminal Userdocs and API Docs
*   Fix and Improve **Drag and Drop**
    *   Collaborate with Platform/Common Navigator to fix PluginTransfer into the Project Explorer
    *   Collaborate with Platform/SWT to fix deferred drag&drop of remote files to copy into Windows Explorer ([bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176))
    *   Improve the RSE DnD Framework to support extenders plug-in transfer types for specific objects in their own remote systems (Newsgroup: [Uday Kabe, Lotus Notes](http://dev.eclipse.org/newslists/news.eclipse.dsdp.tm/msg00173.html)
*   Provide a generic filtering framework (through OQL)
*   Improve the **connection data model**, being a store for IP-Xact data about hardware
    *   remote system properties as defined by the [Spirit group](https://wiki.eclipse.org/DSDP/DD/Spirit "DSDP/DD/Spirit")
*   Re-think RSE SystemMessages: Do we need XML when we have Eclipse NLS / Java MessageFormat?
    *   E.g. DStore\_Service\_Percent\_Complete\_Message -- multiple transformations for substitution

#### **Theme: Integrate other remote access solutions** (strong should have)

*   Interest: Community, projects mentioned below
*   Contribute:
*   **Integrate Platform/Team WebDAV** provider, and/or Google SoC WebDAV provider (through Apache)
*   **Integrate Platform/Team synchronization framework** (for minimal data transfer on sync or import/export)
*   Integrate TPTP agent controller (file services, launch services) as subsystems
*   Bridge to any registered EFS provider, making RSE an EFS Browser (Note: Can be done transparently through ECF filetransfer API. ECF filetransfer is extremely lightweight and there is an existing bridge from ECF filetransfer to EFS. ECF is graduating to 1.0 with Europa.).
*   Use ECF filetransfer API. Expose/Implement RSE as new ECF filetransfer provider.
*   Use ECF discovery API. Expose current zeroconf implementation as new ECF discovery provider.
*   Collaborate with Wicked Shell, integrating features from it
*   Collaborate with JArchive, providing support for more archive formats (through RSE extension point)

#### **Theme: Add unique new features**

*   Interest: Broadcom, WR, IBM
*   Contribute: Broadcom (Contribute Launch), WR (Lab Manager), IBM (IBM Contributions)
*   Contribute Broadcom **Launch Actions**, improve Launching as defined by the [Launching group](./Launching "DSDP/TM/Launching")
    *   Currently being discussed with Robert Norton on the dsd-tm-dev list
    *   ILaunchAction may also be used for board lab hooks
*   Add hooks for **Remote Lab Manager** support
    *   reserve / unreserve target boards, discover target boards, vague target descriptions
    *   Implementation might be facilitated by ILaunchAction hooks
*   Contribute features from **existing IBM implementations** (need legal review):
    *   **User actions** (probably replace by Command framework) - a must-have for IBM
    *   "External Tools" remote implementation (very interesting!) - potentially consolidate into single User Actions framework
    *   Remote Java Debug
    *   Remote Jar Export
    *   Export to multiple targets;
*   **Wind River Target Communication Framework (TCF)**
    *   A lightweight plain-C portable agent

#### **Theme: Multicore / Multisystem support**

*   Interest: WR
*   Contribute:
*   Support target groups as defined by the [Connection Groups initiative](./Connection_Groups "DSDP/TM/Connection Groups")
*   Filters on 1st level of System View ([164807](https://bugs.eclipse.org/bugs/show_bug.cgi?id=164807))
*   View for working with multiple shells concurrently exists
*   Right now we have grouping by profiles
*   Cluster definitions should be something different (being stored inside a profile)
*   Requirements currently unclear; instead of hacking up something wrong, better have no solution
*   PTP might come up with requirements

  

### Other ideas carried forward

*   Improve **Shell Pattern Matching** on the client
    *   Interest: WR, IBM
    *   Contribute:
    *   Allow user-defined patterns ([153274](https://bugs.eclipse.org/bugs/show_bug.cgi?id=153274))
    *   Provide an extension point for patterns but not let the user edit them
    *   Server-side patterns vs. client-side patterns, want to have them consistent
        *   Server-side file can be modified by the users, located in dstore daemon
        *   Client-side patterns buried inside the jarfile --> copy it out of JAR into preferences on first start, allow users to modify through Preferences

*   Improve RSE **Credentials Management**
    *   Interest:
    *   Contribute:
    *   [196445](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196445) The RSE Credentials Management currently uses the Eclipse Keyring, which just provides weak encryption. It should provide a credentials store similar to Firefox, which is passphrase protected and stores credentials well encrypted. It might be possible to use the Jsch mechanism for accessing stored SSH private keys, since getting strong encryption through Eclipse Legal might be problematic. Another option is using the upcoming Platform / Equinox JAAS framework.

Archive of previous plans
-------------------------

### TM 2.0 (Eclipse Europa, June 2007)

*   See the [official TM 2.0 Project Plan](https://www.eclipse.org/dsdp/tm/development/tm_project_plan_2_0.html) for details on target environment, plans and timing.
*   See bugzilla [plan items](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&keywords_type=allwords&keywords=plan&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&order=Assignee) for latest status of items.
*   See the [Europa Simultaneous Release](https://wiki.eclipse.org/Europa_Simultaneous_Release "Europa Simultaneous Release") page for coordinated release issues.

  

### TM 1.0 (Fall 2006)

See the [official TM 1.0 Project Plan](https://www.eclipse.org/dsdp/tm/development/tm_project_plan_1_0.html) for details on target environment, plans and timing.


(Migrated from [https://wiki.eclipse.org/TM_Future_Planning](https://wiki.eclipse.org/TM_Future_Planning))