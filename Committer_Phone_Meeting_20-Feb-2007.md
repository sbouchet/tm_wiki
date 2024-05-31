

DSDP/TM/Committer Phone Meeting 20-Feb-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Feb 20, 2007](./index.php?title=Feb_20,_2007&action=edit&redlink=1 "Feb 20, 2007 (page does not exist)") at [1700 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=2&day=20&hour=17&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 Latest News](#Latest-News)
    *   [2.2 Upcoming Work](#Upcoming-Work)
    *   [2.3 Other Stuff to Do](#Other-Stuff-to-Do)
    *   [2.4 Communications](#Communications)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave McKnight, Dave Dykstal, Kushal Munir
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber, Michael Scharf, Ted Williams

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help: **being responsive**
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site

### Latest News

| Martin | 50% | Making stuff internal, preparing testing | 100% |
| --- | --- | --- | --- |
| DaveD | 80% | UI/Non-UI refactorings | 50% |
| DaveM | 50% | IContextObject for SystemView, SystemView bugs | 60% |
| Kushal | 100% | Encodings, Streams for IFileService, EFS, SystemRegistry improvements for SD | 70% |
| Javier | 50% | SD improvements, making FTP internal | 50% |
| Ted | 0% |  | 0% |
| Uwe | 100% | dynamic systemTypes, newConnectionWizard extension point | 90% |
| Michael | 20% | making Terminal internal, Terminal performance | 20% |

### Upcoming Work

*   **Top priority** this week is getting M5 stable.
    *   [TM 2.0 M5 Testing](./TM_2.0_M5_Testing "TM 2.0 M5 Testing")
    *   New build on [I20070220-1126](http://download.eclipse.org/dsdp/tm/downloads/drops/I20070220-1126)
        *   New wizard problems fixed
        *   Please test thoroughly today!
    *   We'll have more I-builds at least once every day until M5. But lets find the issues first before we start fixing minor ones
    *   Invest 2-3 hours of testing before starting the bugfix cycle
*   **Current plan items and API things:**
    *   Changes in Platform M5 and M6:
        *   Official API for ssh prefs
        *   ssh now part of cvs feature
        *   Helpserver changed, Userdocs not accessible right now; DaveD will check
    *   ([Bugzilla#173772](https://bugs.eclipse.org/bugs/show_bug.cgi?id=173772)) **RSE New Connection Wizard Rework**
    *   [170909](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170909) (DaveD) User Actions & Import/Export
        *   Attached on bugzilla; **AI Martin** will upload refactored version after M5
        *   No need to rush anything into bugzilla, DaveD to work with Kushal on finishing the contribution
    *   [170923](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170923) (DaveD) UI/Non-UI splitting
        *   Preferences finished, these were the hardest; more stuff to do - DaveD really wants to get it done soon after M5
    *   [170627](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170627) (DaveM) ISystemFilter in SystemViewElementAdapter.getChildren()
        *   DaveM wants to get rid of the FilterString stuff in IRemoteFile now that IContextObject works
        *   getImageDescriptor, getLabel should also get the context
        *   more to do to get closer aligned with Platform (bugzilla bug exists)
    *   [170922](https://bugs.eclipse.org/bugs/showdependencytree.cgi?id=170922) (DaveM, Martin) Making as much as possible "internal": SystemView, SystemFilterReferenceAdapter, Subsystem Impls
        *   What should be the recommended way of re-using existing subsystems against a new systemType
        *   Registering FTP or ssh against Windows will not be case insensitive; roots, drives etc are all unix-style
        *   DaveM: Dstore overrides SubSystemConfiguration for Windows in order to provide different filters etc; The SubsystemConfiguration defines the filters etc
        *   If we make SubsystemConfiguration public, we'll also need to make stuff API that is being returned; probably make some methods final that return non-API interfaces
        *   What people win: createDefaultFilterPools(), isCaseSensitive(), for UDA it might also be important
        *   **Decision:** make the SubSystemConfigurations API again for M5, **AI Martin** make it API
        *   Kushal: API Scanner? - Martin: too early to use yet, do it for M6
    *   [170915](https://bugs.eclipse.org/bugs/showdependencytree.cgi?id=170915) (DaveM) Getting rid of Platform "internal" access
        *   **AI Martin** fix the ISV docs
    *   [163820](https://bugs.eclipse.org/bugs/show_bug.cgi?id=163820) (Kushal) Encodings
        *   Test cases? Manual Tests?
    *   [170916](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170916) (Kushal) EFS
        *   Oliver Hardt looking at it; Kushal prepared Streams for ftp, ssh
        *   Kushal trying to fix it for M5
    *   Martin & DaveM work on EclipseCon tutorial: fix bugs as needed
        *   **AI Martin** write bug for preselection
    *   [170832](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170832) (Martin) Read-only setting on ssh - what about using EFS on the back-end? (dstore doesnt do streams)
        *   **AI Martin**: timestamp, ro-flags still TBD for ssh
    *   add **unit tests** for all new or modified API

### Other Stuff to Do

*   Reduce number of plugins (once UI/Non-UI separation is done, have e.g. ssh.core and ssh.ui but not more)
    *   Prerequisite: need to be able and disable registered stuff; TBD through Capabilities
    *   Move org.eclipse.rse.connectorservice.local into org.eclipse.rse.subsystems.core
    *   org.eclipse.rse.subsystems.core (collapse files.core, processes.core, shells.core)
    *   org.eclipse.rse.subsystems.dstore (collapse files.dstore, processes.dstore, shells.dstore)
    *   Have it split up now in order to allow people "get what they need"; and as an example for ISVs "here's how to do your processes" - having stuff bundled together gives people the impression that they can't change it
*   Add Montavista shell processes subsystem
    *   Martin wants to put it into processes.core
    *   DaveM: confusing for people who want to use it
    *   Would it be better to have a Process Service to interface with the Shell Service rather than doing a subsystem --> Allows to take the ProcessServiceSubsystem and choose which service to use
    *   **Decision:** Put it into its own plugin but part of the core feature for now, think about consolidating plugins in next iteration
*   Other stuff
    *   Orbit bundles to be added differently
    *   Unittests to run every night
    *   **AI Martin** Version Number Changes in plugins and features - any more to do?
    *   Copyright Year Changes

### Communications

*   **Europa Requirements**
    *   (done) [TM 2.0 Ramp down Plan for Europa](./TM_2.0_Ramp_down_Plan_for_Europa "TM 2.0 Ramp down Plan for Europa")
    *   (done) Update features and include the words "end-user" and "extender"
    *   **Avoiding non-API from other projects**
        *   **AI Martin** create bugzilla against CDT
    *   Update Wiki to explan whether SDK contains examples --> **AI Martin** wait for Platform and adapt
*   For bugs, see the [bug process page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) (assigned to inbox, plan items, status new, hi-priority, API, open with patch, assigned to M5) -- pretty many right now
*   **Update Copyright Year to 2007 if you happen to think about it**
*   (done) **Fix N-builds** (second workspace, use Ted's scripts)
*   Please continue on Compiler Warnings
*   Change Requests
*   Vacations, Holidays etc.
    *   DaveM, MichaelS, Martin, Javier coming to EclipseCon - DaveM flying in Sunday afternoon, staying at the Hyatt;
        *   **AI Martin** arrange a committer meeting in addition to the BoF
    *   DaveD going to Florida in February for a week
*   Free discussion -- feelings, comments, critics

Action Items
------------

*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_13-Feb-2007#Action_Items "DSDP/TM/Committer Phone Meeting 13-Feb-2007") Action Items
*   **DaveD** \- Filter testing, Fix User Docs; Remove RSE Performance Logging; Refactoring UI/Non-UI; Persistence; Bugzilla bug for User Actions Contribution until Jan.31st; Bugs & Unit tests;
*   **DaveM** \- EclipseCon; Bugs & Unit tests
*   **Kushal** \- EFS; Talk to DaveD re Comm Server; Bugs & Unit Tests
*   **Martin** \- EclipseCon tutorial; Check r/o flags and timestamps for ssh; Commit Montavista contrib; Migrate build to Ted's scripts; Migrate Commons.net to single-file-jar; Bugs & Unit Tests; Personal Interviews via Skype; Work on [TM and RSE FAQ](./TM_and_RSE_FAQ "TM and RSE FAQ"), improve Wiki and Website (how to contribute);
*   **Javier** \- Make discovery internal; Improve SD; Bugs & Unit Tests
*   **Ted** -
*   **Michael** \- Terminal Performance Improvements
*   **Uwe** \- Retargetable actions, Improved Refresh

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 28-Feb-2007](./DSDP/TM/Committer_Phone_Meeting_28-Feb-2007 "DSDP/TM/Committer Phone Meeting 28-Feb-2007") at [1430 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=2&day=28&hour=14&min=30&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_20-Feb-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_20-Feb-2007))