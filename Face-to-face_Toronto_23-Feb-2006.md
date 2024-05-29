

DSDP/TM/Face-to-face Toronto 23-Feb-2006
========================================

< [TM](./TM)

Contents
--------

*   [1 Agenda & Attendee List](#Agenda-.26-Attendee-List)
*   [2 Presentations](#Presentations)
*   [3 Minutes - Thursday TM session](#Minutes---Thursday-TM-session)
    *   [3.1 Symbian TM Demo](#Symbian-TM-Demo)
    *   [3.2 RSE Demo and Architecture](#RSE-Demo-and-Architecture)
    *   [3.3 Component-Based Launching](#Component-Based-Launching)
*   [4 Minutes - Friday TM session](#Minutes---Friday-TM-session)
    *   [4.1 TM Project Plan](#TM-Project-Plan)
    *   [4.2 Target Connection Adapter Update](#Target-Connection-Adapter-Update)
    *   [4.3 Connection Properties and Wizards in RSE](#Connection-Properties-and-Wizards-in-RSE)
    *   [4.4 Technology Subgroups and Future Plans](#Technology-Subgroups-and-Future-Plans)
*   [5 Action Items](#Action-Items)

Agenda & Attendee List
----------------------

*   [Agenda](./Toronto_23-Feb-2006_Agenda "DSDP/TM/Toronto 23-Feb-2006 Agenda")
*   [Photos from the Meeting](./Toronto_23-Feb-2006_Photos "DSDP/TM/Toronto 23-Feb-2006 Photos")

Presentations
-------------

*   [Dave McKnight - RSE for TM](https://www.eclipse.org/downloads/download.php?file=/dsdp/tm/presentations/2006-2-23_Toronto_TM_RSE.ppt)
*   [Martin O - Component-Based Launching](https://www.eclipse.org/downloads/download.php?file=/dsdp/tm/presentations/2006-2-23_Toronto_TM_LaunchActions.ppt)
*   [Peter L - Target Connection Adapter Update](https://www.eclipse.org/downloads/download.php?file=/dsdp/tm/presentations/2006-2-23_Toronto_TM_Connectors.ppt)

Minutes - Thursday TM session
-----------------------------

See [DD Meeting Notes](https://wiki.eclipse.org/DSDP/DD/Face-to-face_Toronto_22-Feb-2006 "DSDP/DD/Face-to-face Toronto 22-Feb-2006") for the Joint Session:

*   Doug G - Update on DSDP, Plans for EclipseCon
*   Hobson Bullman - Introduction to SPIRIT
*   Doug G - WR's data file standards
*   Aaron Spear - Hardware Descriptions at Mentor / SPIRIT Requirements for DSDP

### Symbian TM Demo

*   Presentation to be posted
*   Test Automation Tool (STAT), with an FTP Proxy on the host (for translation)
*   Browse / Send / Execute / Install / Restart; FTP Proxy supporting multiple PC clients (and 1 target) - with semaphore: only 1 client allowed at any time.
*   New system: multiple services on the target (STAT broken up) - SMDCP: Simple Multiplexed Device Control Protocol, Symbian specific
*   TM Daemon: Based on proposal from Pierre-Alexandre: query availability of ServiceTypes, TM UI to display available ones
    *   Planning to contribute the "yellow" parts in Open Source (the interfaces) ; "green" implementation to remain proprietory at Symbian.
    *   Debugging TBD as just another service
*   FileZilla: Raw FTP commands for installing and launching
*   Future: Want services like install, uninstall, process list ... defined and available in TM system.

  

### RSE Demo and Architecture

*   [Presentation](https://www.eclipse.org/downloads/download.php?file=/dsdp/tm/presentations/2006-2-23_Toronto_TM_RSE.ppt) by Dave McKnight
*   RSE Demo
    *   Ability to cancel shell commands?
    *   RSE Files View: Contextmenu, Run > Host C/C++ Application
        *   Remote Source Locator integrated with Remote Launch
    *   "Attach" Launches directly from the RSE View:
        *   Re-uses existing Launch with same properties (potentially overwrite old "similar" launch)
    *   Same for Remote Java Launches
    *   Classifying remote files: dstore running a "file" command on the remote in order to find out the file type
    *   Seamless File Transfer: need conflict detection on multi-user machines (if file is simultaneously modified while edited on client)
*   RSE Architecture
    *   IHostFile: the simple data
    *   Connector Service: Manage passwords etc.
    *   As long as no subsystem extension for Files exists, the Subsystem definition won't be loaded
    *   Pete Nicholls: Can bundle RSE in Rich Client Platform?
        *   Should be possible.. no more strong dependencies
    *   Persistence: Persistence Providers can be registered to persist the RSE DOM.
        *   DOM is everything above the actual RSE objects: connections, filters, actions, ...
        *   FelixB: Use Persistence Providers to auto-discover remote systems?
            *   MartinO: Looking at use-cases, detecting a new remote system is an explicit step that can be done via an import wizard. There is littel use in automiatically populating the list of local connections ("my favorites") with automatically detected connections.
    *   System Registry API
        *   Used by the Persistence Provider to create RSE objects, read them and persist them.
        *   Persistence Provider is called whenever something is modified
    *   Creating the FTP Subsystem
        *   Subclass AbstractFileService, implementing IFileService
        *   Subclass FileSubsystemConfiguration and register it as SubSystemConfiguration extension
        *   Reason for layering: Once filters etc. are defined for a subsystem, these shold remain available when you switch protocols
        *   Most of the work in FTP was the parsers for directory listings etc. (which depend on the host system type with the Sun FTP client)
    *   Contributing a brand-new subsystem type
        *   Doing the layering (subystem - service) is possible, but not required. Vendor can choose to make the separation or not (in practice, the separationg might make sense... in case it turns out that the original choice of protocol is to be revised at some later time
        *   Shared Protocol is possible: a single service can be used to populate multiple subsystems
        *   Subsystem is providing a lot of re-usable code... e.g. integration with the Eclipse Jobs model
    *   Debugging / Attaching: Is Debugging a Service?
        *   So far, more used it as an Action (making use of the Files / Processes subsystem) and not a service
        *   Pete Nicholls created a Debug Subsystem, allowing to register various things there
        *   Martin O: Two usage models - (a) launching a debugger, (b) using a debugger to retrieve system info or manipulate the remote system (to populate a subsystem)
        *   Tom Hochstein: Want to use (reference) connection data in the Launches - Martin O: That's already there (referencing a connection by dropdown)
    *   File Export / Import: can take a list of local files and transfer them to the remote system, and save the configuration information (about the list of files) in a configuration -- very much like the JAR export
    *   External Tools > Remote Build, Remoe Command
    *   Associate a local project with RSE connections (such that local changes are automatically synced to the remote system)?
    *   Creating a new SubSystem:
        *   Extend abstract SubSystem
            *   Methods to override: connect(), disconnect(),
            *   Every query (expansion) comes down to resolveFilterString()
            *   Initial List of Objects need to adapt to SystemViewElementAdapter; these adapters define what should happen when they are further expanded. That way, the elements (objects) can decide if they want to do caching etc.
            *   The master implementation of SubSystem implements resolveFilterString() itself, in order to create Jobs for retrieving the information -- subsystems only need to implement InternalResolveFilterString()
            *   See IBM "Universal Sample"
                *   getObjectWithAbsoluteName()
        *   AaronS: It might make sense to even have a dummy server on some port , just for showing how the subsystem works
    *   MartinO: How are events from the target handled?
        *   RSE allows asynchronous retrieval of information: when a large directory (e.g. lib) is expanded, DataStore first returns the list of file names and forks off a job for analyzing the type of files. Decorartors are create later, in response to a DataStore Event from the target
        *   Dstore should be able to transfer any classes (miners) to the remote system and execute them there - but this has not really been explored so far
    *   Aaron: Relation to TPTP?
        *   RSE works in User Space, whereas the TPTP agent lives in System space
    *   FelixB: The new Debug Model with its Flexible Hierarchy - might it make sense using this for the RSE Tree?
        *   Since the RSE view is totally Adapter diven, it is pretty flexible already now, so there is probably no need for adopting the Debug Model
    *   Pawel P: Performance Issues?
        *   Yes, there can exist queries that are extremely large or extremely costly to run...
        *   UI Rendering can get pretty expensive, though not seen a very expensive rendering for a long time
            *   MartinO: Yes rendering Search Results can be expensive when it's 10000s of results
            *   As long as the query is cancelable (in a job) and the UI isnt blocked, it's OK
*   AaronS: People want to just monitor remote systems (e.g. with TPTP) without attaching a debugger... RSE should allow to select a particular context, and choose "Attach Profiler" from the contextmenu, such that profiling information is recorded...
    *   Mentor already have an adaptor for their proprietory protocol to what TPTP expects (the adapter runs on the host) - TPPT thinks it connects to the localhost
    *   TPTP also talking to BIRT folks for getting reports

### Component-Based Launching

*   [Presentation](https://www.eclipse.org/downloads/download.php?file=/dsdp/tm/presentations/2006-2-23_Toronto_TM_LaunchActions.ppt) by Martin O
*   KenRyall: Better decouple the Launch Action Framework from RSE, such that it can be used independently of RSE
*   KenRyall: What script to use? - A slippery slope... would like to script debuggers, or the whole Eclipse IDE
    *   MartinO: yes -- perhaps best keep the Launch scripts extremely simple though it is tempting to make them more complex
*   PawelP: Expect that the Generic Launch UI would not be exposed to the user, but specialized Launch UIs would make use of the component framework
*   JohnCortell: Consider using ANT for the Launch scripts
*   Darian Wong, Felix Burton: will need Target Groups to execute same action on a list of targets
*   Paul Gingrich: Suggest scripts to be stored-away components of their own: users tend having to execute the same sequence of steps again and again, with different parameters
    *   Martin O: might use Eclipse Variables in order to make actions (and scripts) configurable; create "super Actions" that just reference other actions. Doing that in the UI is difficult.

Minutes - Friday TM session
---------------------------

### TM Project Plan

*   See the [Plan](https://www.eclipse.org/dsdp/tm/development/plan.php) on the main website
*   Discussions:
    *   What does testing mean?
        *   In the minimal case, it means a developer working actively with the product on that OS / VM combination
        *   The next level, is that automated (nightly) tests run on that OS / VM combination
            *   We will need more automated test scripts! Who can help out here?
        *   The third level is that some defined test scripts are executed manually by a tester
            *   TBD: Automated UI testing (at WR) ?
    *   Internationalization (Externalized Strings) in all RSE - using a Message Framework that goes beyond what Eclipse does in the Platform
    *   Who can help out with working on RSE?
        *   API Review, Doc Review - Symbian (1/2 Engineer)
        *   API Review, Extension Verification - Wind River (3/4 Engineer)

### Target Connection Adapter Update

*   [Presentation](https://www.eclipse.org/downloads/download.php?file=/dsdp/tm/presentations/2006-2-23_Toronto_TM_Connectors.ppt) by Peter L
*   Paul G: OS Vendor and Silicon Vendor both supplying a debugger: have 2 debug sessions, or how would they cooperate?
    *   PL: That depends. Might have OS-aware debugging through the JTAG connection; might have both debuggers in parallel
    *   MartinO: Have both scenarios in the WR Workbench.
        *   Hardware Debugger running in parallel to a software debugger; when HW suspends the system, it looks to the software as if the connection were dropped. There is a need for the debuggers to communicate, such that this can be handled gracefully.
        *   Hardware Debugger providing a virtual network / communication link for the software debugger ("Transparent Mode"); this would refer to the "adaptor talking to another adaptor" scenario
*   Pawel P: Where would the adapters run? Inside the Eclipse IDE or outside?
    *   PL: No fixed opinion
*   Pawel P: Will the CDI meet these needs?
    *   PL: CDI is interface to the debug engine. Connectors are below the Debug Engine.
*   Aaron S: Would the API be flat asynchronous, or how would that work?
    *   PL: Need to work on the APIs, need community help
*   Neil T: How does this low-level functionality relate to the RSE high-level functionality?
    *   PL: Connectors may be the connection to the RSE
*   Neil T: How can we get sort of a hierarchy, RSE being the tool and connectors below?
    *   Need to create a workgroup
*   Felix B:
    *   Confused: Proposing to define some specific interfaces for specific purposes (like file browsing, debugging, ...).... or proposing a generic method for discovering services and connection methods / communication channels?
    *   PL: Mainly looking at Debugging: Hardware debugging and OS-Aware debugging
    *   Felix: There are lots of more applications than debugging... tracing, profiling, redirecting I/O, file transfer, ... want a generic infrastructure for putting in applications that nobody thought about so far, that's open for the future
    *   Felix: Part of Multi-Core association trying to define a generic debug interface. Which is important, but it does not belong to Target Management -- TM should go beyond debugging only... TM is more of a broker than actually implementing the various pieces
*   Paul G: If we were not from different companies, but different divisions in one company, we'd probably do what TI has done - one target access method that's being used by multiple different groups / applications
    *   Abstracting debuggers is hard. If WR were to create a debugger for the TI DSP's they'd still have to re-implement lots of the low-level debugging stuff, this cannot be abstracted easily ... have to share more than just the connection! For instance, the DSP vendor would have to supply a pluggable disassembler (or data-driven disassembler?)
*   PL: We are not talking about the debug engine; just talking about the target connection part.
*   FelixB: CDI is too big
*   Aaron S: Chaining Things Together for Kernel Awareness in their product now, and works OK; the painful point is, that when chaining things together you get dependencies both ways. Layer X needs symbol information from upper layer Y; which makes implementation in the various layers more complex; an object interface for that kind of layering is a bad idea
*   PaulG: Its a good idea to have standard interfaces for the various connectors; people would use the standard interfaces, it would make things easier - people would implement against the standard interfaces
*   PL: Already have an approach similar to the list of interfaces on the slide in their commercial product
*   How are we moving forward?
    *   PaulG: Interested in attending, not leading; want generic interfaces first, specific ones later
    *   WR-MOB: Interested in the generic part; but no resources short term;
    *   WR-Felix: interested in generic part; probably need to learn with generic interfaces; when doing the Debug Interfaces, not be blind - reach out to other parts of the world (WR Targetserver; TI targetserver; Interfaces at JTAG Vendors; Multicore initiative; OS vendors \[depending on the interface\]);
    *   Aaron: Mentor Debug Engine is Native, not in Java - Java based interfaces would be useless. Perhaps better define protocols than Java interfaces?
        *   MartinO: Adapters can be programs, C/C++ modules, Java programs, even hardware devices. We need a generic description of
            *   What an adapter provides and what it requires
            *   The protocols
            *   How to start it up and configure it
        *   Felix: Agree, it would be good if Target Manager could start up target servers (and other daemons, executables, ...) without knowing them specifically:
*   **Working Group**:
    *   led by Peter Lachner
    *   Contribute: Paul G, Felix B, Aaron S, Tom H
*   Martin O wants that Peter L has committer rights in order to update the Website, such that information can be published - AI Doug find out what Eclipse Foundation thinks about that

### Connection Properties and Wizards in RSE

*   First Page is generic - everybody inherits this for creating the new connection
    *   Some remote systems do not necessarily have a name; want to be able to get rid of the first wizard completely
    *   First page when Remote System Type has not been selected yet: want to split up the current page in two - first page just for selecting the system type, second like when the system type was selected initially
    *   DMK: Should be possible to provide an extension point where an entire wizard can be contributed (instead of just
    *   PeteN: Perhaps get rid of the "New Connection..." abilities in the tree?
        *   Martin O: Everybody he talked to found it weird
        *   DaveD: These are a legacy; Preference to get rid of it already exists; when they are not in the tree, "New > Connection" can be done from the generic New... menu -- problem is labelling, since "Connection" is used in a variety of contexts
        *   KenR: Likes the "New..." Tree
*   Interfaces for storing connection properties
    *   IRSEModelObject: Hierarchy - IHost
    *   IPropertySetContainer - gets persisted automatically in the RSE DOM
    *   Validators are in the UI, not in the model
*   Relation of Property Pages to Wizard Pages
    *   Switching the Service while the subsystem is alive is problematic - different PropertyPages would be associated with the different services... DaveMcK wants to potentially get rid of the specialized PropertyPages, in favor of the generic ones
    *   MartinO wants to have two separate file subsystems for the two different services of same subsystem; e.g. Flash Filesystem plus NFS Mounted Filesystem; mark them as Files \[dstore\] vs Files\[ftp\]
        *   DMK thinks that some users want to re-use filters they have defined for a subsystem with the other service (e.g. depending on how the dstore server has been launched only); MartinO questions whether re-using the filters make sense in all cases
        *   Separate Subsystem per service can be done by doing another SubSystemConfiguration, and hardcoding the list of Services (or the only service) that's allowed for it
    *   PropertySetContainer has String values; more complex objects would choose themselves how they want to persist themselves in the PropertySetContainer

### Technology Subgroups and Future Plans

*   Reviewing the Brainstorming Notes from Chicago
*   New Working Groups are boldface, below
*   Short Term (Sept. 2006)
    *   ECF (For Filesharing) - IBM, WR
    *   **Hardware Descriptions** \- Mentor, ARM?
        *   Related to Inter-Debugger Communications
    *   Component-Based **Launching** \- WR, Nokia, Freescale
        *   CDT Launch - Nokia, PalmSource
    *   **Associations** (Connection / Project / Build ) - WR, Mentor
    *   **Connectors** (Flexible Pluggable Target Connection Adapters) - Intel, TI (Paul), WR (Felix), Freescale (Tom), Mentor (Aaron)
*   Middle Term (June 2007 - next TM major release to be aligned with Eclipse Platform)
    *   **Inter-Debugger Communications** \- Freescale
        *   Events; Related to HW Descriptions
        *   Are Events just another service (between TM-aware tools)?
            *   At what level should events be exchanged?
            *   Is this just a debugger API issue?
            *   Allow Services to provide not only host-target communications, but also host-host communications (among tools registered to the same TM)
    *   More explicit Analysis, Requirements, Workflow documents
        *   For next release: create as "Living Documents" on the TM Homepage
    *   **Shared Board Labs** \- WR, Mentor, Freescale
        *   Related to Autodetect
    *   **Connection Groups** (Mentor, Freescale, Curtiss-Wright)
        *   Synchronous Run-Control
        *   Downloads to multiple targets (not synchronous; parallel; sequential)
        *   Multi-Language Debugging (coordinated Java / JNI debuggers; related to inter-debugger events)
    *   **Autodetect** \- WR, Freescale
        *   Autodetect boards on the local network or in a lab
        *   Autodetect connection mechanisms to a board (connectors)
        *   Autodetect services on a remote system
*   Long Term
    *   Drop into Hardware Debugging (Re-use current context in another debugger in case of an exception)
        *   Related to Inter-debugger communications, connection groups/multi-language debugging
    *   Security
        *   Authentication to the target
        *   tunneling: through connectors
    *   DSM (e.g. tracking kernel versions, installed software, automatic software updates, ...)
        *   TM is just a broker for various services

Action Items
------------

*   Aaron Spear: Be TM's advocate on SPIRIT / Hardware Descriptions (collaborating with the DD group on Hardware Descriptions)
*   Doug Gaff: Contribute WR's cleanroom telnet implementation
*   Everybody: Get RSE, prototyping, bugzilla's


(Migrated from [https://wiki.eclipse.org/DSDP/TM/Face-to-face_Toronto_23-Feb-2006](https://wiki.eclipse.org/DSDP/TM/Face-to-face_Toronto_23-Feb-2006))