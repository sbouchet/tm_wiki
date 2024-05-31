

DSDP/TM/Committer Phone Meeting 16-Aug-2006
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday Aug 16, 2006 at [8.30am Rochester / 9.30am Toronto / 2.30pm London / 3.30pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=8&day=16&hour=13&min=30&sec=0&p1=223&p2=250&p3=421&p4=136&iv=1800) |
| Skype Dial-in: | **+99008275601400** (this call is **free** from Skype) |
| Fixed-line Dial-in: | US, call **1-712-432-4000** (long distance charges)    Austria: **0820 400 01562** (national call charges)   In UK: **0870 119 2350** (national call charges)   |
| Passcode: | **5601400** |

Fixed-line fallback dial-in:

*   International **+1 314-655-1411**
*   North America **+1 877-422-0035** (toll free)
*   Passcode: **764918**

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave Dykstal, Dave McKnight, Kushal Munir
*   (Symbian - Javier Montalvo Orús - vacation)
*   Wind River - Martin Oberhuber

Agenda
------

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site
*   Latest News
    *   Martin -- Added Mutex; I-builds fixed; Discussions with Buckminster; Simple renamings
        *   Who'll need Mutex? FTP yes, Dstore no (should be thread-safe)
        *   Going to move Mutex to clientserver
    *   DaveD -- Signon without password; working on SystemException stuff now
    *   DaveM -- Some hi-pri bugs fixed
        *   Daemon port range: will have separate args for daemon port and server port range. User-specified port outside the range should return an error
        *   Deadline for other project this week, so no more time this week
    *   Kushal -- Refactorings checked in; will need Persistence stuff go to core (model stuff - especially ConnectorService)
        *   Will need IConnectorService to take ICredentialProvider instead of Shell
        *   Still couple of weeks of work in the Workspace, which cannot be checked in now
    *   Javier -- vacation
    *   Other News --
*   Upcoming Work
    *   **What can we achieve till the 1.0 release?**
        *   111 bugs open, not counting enhancements (See "Reporter vs. Severity" on the [Bug Process page](https://www.eclipse.org/dsdp/tm/development/bug_process.php))
        *   3 P1 bugs, 17 P2 bugs open - most of them since 4 weeks (See "Assignee vs. Priority" on the [Bug Process page](https://www.eclipse.org/dsdp/tm/development/bug_process.php))
        *   Team Support is almost totally broken and mostly untested
        *   \> 700 Javadoc errors (Preferences > Compiler > Javadoc > Report errors, Missing tags)
            *   To be fixed manually!
            *   Get rid of implementation comments (reference to interface comments instead) wherever possible
        *   Jakarta-commons, WR Terminalview? Junit tests, tutorials
        *   5 weeks = 25 days until RC0; 4 weeks = 20 days after, for "planned & coordinated testing + fixing"
        *   bugfix rate to-date is 1 "hard" one or 3 "easy" ones per day
        *   What do we expect from M4? -> Growing community by a stable release available through Update Manager
        *   What do we expect from 1.0? -> Growing community by something reliable to base on
            *   Will need to communicate intended refactorings between 1.0 and 2.0 early --> Keep the [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") page up-to-date
            *   For Refactorings after 1.0, we'll need migration docs
        *   **Kushal will continue refactoring, others focus on bug work**
            *   Please document on the mailing list what's about to change, we'll vote for the change.
            *   Try to make IConnectorService UI-less, probably all model and persistence provider -> will help with unit tests
            *   Focus on API clarification, making APIs smaller (internal) -- less API means less migration docs in 1.0
            *   Kushal is expert on: File Encodings, TAR archive reader, Remote Search. Such bugs to remain assigned to Kushal. Other bugs can be grabbed by others and fixed.
    *   **Refactorings**
        *   \[cleanup\] vs. \[refactoring\] in commit comments
            *   Use \[refactoring\] for moving and renaming
            *   Use \[cleanup\] for fixes in docs or implementation, that do not change the structure
        *   Who's maintaining MikeB's Change Map ([bug 150548](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150548))
            *   DaveD to check in as CSV as soon as M4 is out
        *   Discuss before implement
        *   SubSystemConfiguration -> SubSystemFactory?
            *   248 matches for "SystemFactory" (case insensitive, not whole word) - extension points, docs, local variables
            *   963 matches for "factory" (case sensitive, whole word) - 374 of these in comments, with "subsystem" on the same line
            *   141 matches for "factories" (case sensitive, whole word) - 61 of these in comments
            *   Java search: 50 declarations of "\*SubSystemConfiguration\*" types
            *   330 matches for "subsystem configuration" in comments
            *   Ultimate goals:
                *   separate the factory from the configuration, such that ISVs that re-use an existing factory can only implement the configuration but not the factory
                *   ISVs which do their own factory will have to implement both factory and the config
                *   allow headless launch, connect and use of services through a UI-less extension point for (factory? configuration?)
            *   **Want to split up subsystem : service more cleanly** by having separate Factory and Configuration: separation will allow for more safety, as every creation of the FileServiceSubsystem will happen in one single place only.
                *   Might probably need a ServiceFactory, ConnectorServiceFactory, ??? -- Probably not necessary since everything is connected to the Configuration.
        *   Shell Pattern Parsers: moved to org.eclipse.services/src/org.eclipse.services.shells
        *   Mutex: move to org.eclipse.services/src, or org.eclipse.services/clientserver?
    *   API Things
        *   **Service Error Reporting** \- [bug 149472](https://bugs.eclipse.org/bugs/show_bug.cgi?id=149472) \- DaveD
        *   **Parallel Services** \- Martins Mutex to be applied to FTP; [bug 142478](https://bugs.eclipse.org/bugs/show_bug.cgi?id=142478) all queries in background - DaveM
        *   **SystemRegistry.createHost** for Javier
            *   [bug 150168](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150168) dont commit immediately - DaveD
            *   [bug 150265](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150265) allow specifying subsystem types - DaveM
        *   Making stuff **internal** \- ssh, ftp: Martin
        *   Obsolete API that's in the Platform now (ActionSets, rseConfigDefaults) --> See [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") page
    *   **Bug Work - please observe priorities**
        *   Open bugs: [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1),
        *   [bug 153253](https://bugs.eclipse.org/bugs/show_bug.cgi?id=153253) \- Persistence of local filters - to be addressed by DaveD for M4
    *   Legal: JUnit (Some IBM signoffs needed, but not too hard); Jakarta-commons (TBD aug.24 latest); WR Terminalview
*   Other items
    *   Keeping Tutorial up-to-date vs. review at the end of the release process
    *   Manual test plans - in work by **Martin**
    *   EFS feature, Examples feature to be created by Martin
*   Free discussion -- feelings, comments, critics

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_9-Aug-2006#Action_Items "DSDP/TM/Committer Phone Meeting 9-Aug-2006") Action Items
*   **DaveD** \- JUnit legal, Service Error Reporting API, Persistence bug 153253, Checkin mappings.csv, SystemRegistry API. Check collapsing persistence Properties nodes to fewer files. Compile a list of suggestions for making classes / packages internal.
*   **DaveM** \- bug fixing by priority; look at Kushal's bugs and assign yourself; get rid of Service calls on UI thread; hygiene changes
*   **Kushal** \- bug fixing, refactoring IConnectorService with help from DaveD; send file encoding test resources to martin; review & get rid of rseConfigDefaults
*   **Martin** \- EFS & Examples features, build scripts, Manual test plan, API Review, Jakarta-commons, WR-terminalview; Review if IShellService is sufficient for terminal
*   **Javier** \- vacation; hook up with Scott Lewis once SD is committed
*   **Everyone** \- List obsolete API on [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") page; Mark hygiene changes as \[cleanup\] in commit comment

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 23-Aug-2006](./Committer_Phone_Meeting_23-Aug-2006 "DSDP/TM/Committer Phone Meeting 23-Aug-2006") at 9.30am Toronto
    *   Continue using the Skype/Fixed-line bridge, fallback to plain Skype during the call if possible
*   Open [DSDP/TM/Phone Meeting 6-Sep-2006](./Phone_Meeting_6-Sep-2006 "DSDP/TM/Phone Meeting 6-Sep-2006") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_16-Aug-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_16-Aug-2006))