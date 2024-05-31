

DSDP/TM/Committer Phone Meeting 13-Mar-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Mar 13, 2007](./index.php?title=Mar_13,_2007&action=edit&redlink=1 "Mar 13, 2007 (page does not exist)") at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=3&day=13&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 News & Review Action Items](#News-.26-Review-Action-Items)
    *   [2.2 Upcoming Work](#Upcoming-Work)
    *   [2.3 Other Stuff to Do](#Other-Stuff-to-Do)
    *   [2.4 Communications](#Communications)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave McKnight, Dave Dykstal, (Kushal Munir n/a)
*   Symbian - (Javier Montalvo Orús n/a)
*   Wind River - Martin Oberhuber, Uwe Stieber, Michael Scharf, (Ted Williams n/a)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help: **being responsive**
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site

### News & Review Action Items

| Martin | 100% | EclipseCon | 70% |
| --- | --- | --- | --- |
| DaveD | 100% | UI Refactoring - Conn.Svc today or tomorrow | 100% |
| DaveM | 50% | EclipseCon | 10% |
| Kushal | 50% | n/a |  |
| Javier | 50% | n/a |  |
| Ted | 0% | n/a | 0% |
| Uwe | 5% | Wizard fixes and cleanups | 5% |
| Michael | 20% | Terminal Performance | 20% |

### Upcoming Work

*   See also [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_28-Feb-2007#Upcoming_Work "DSDP/TM/Committer Phone Meeting 28-Feb-2007") for notes
*   **Top priority** is getting API things done for M6. Plan items are currently more important than bug priorities. We have 3 weeks to go.
    *   [170909](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170909) (DaveD, Kushal) User Actions: Still waiting for IP review. Found many icons related to UA and import/export in rse.ui which will need to be moved.
    *   [170923](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170923) (DaveD) UI/Non-UI splitting: Conn.Svc almost done, others will fall nicely into place afterwards. rse.ui/plugin.xml/systemTypes need to go to core
    *   [170932](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170932) (DaveD) Default Persistence Provider: mostly non-API
    *   [170936](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170936) (DaveD) Macintosh - machine for unittests? - **AI Kushal**
    *   [170926](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170926) (DaveM) Improve IFileService: mostly done; Returnvalue for copy; Streams on the Subsystem Layer - **AI Kushal file 2 bugs**
    *   [150498](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150498) (Javier) More service-oriented; Multiple subsystems of the same kind - extenders ok? Discovery? "No subsystems"? [176490](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176490) new wizard request, see also "Improve SystemType" below
    *   [170911](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170911) (Javier) Discovery
    *   [170916](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170916) (Kushal) EFS
    *   [163820](https://bugs.eclipse.org/bugs/show_bug.cgi?id=163820) (Kushal) Encodings - **AI Kushal UnitTests**
    *   [170915](https://bugs.eclipse.org/bugs/showdependencytree.cgi?id=170915) (Martin) Adopt 3.3 Concepts: Jsch -> switch to Platform I-builds? DaveD would like it; Uwe would have problems adopting RSE in Workbench; **AI Martin** switch to new build, consume Platform I-builds as Target Platform after next week; tell others when it is time to update
    *   [170922](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170922) (Martin) Optimize RSE API: ISystemRegistry
    *   [170910](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170910) (Martin) Integrate Terminal
    *   [170918](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170918) (Martin) Improve SystemType and Wizard: Replace Name by IRSESystemType wherever possible, but keep it for now in Persistence (**AI DaveD verify**) and if() queries -> these are implementation details later, even replacing Name by Properties since the systemType does have Properties already

*   **Other API things** not directly marked as plan item
    *   [173042](https://bugs.eclipse.org/bugs/show_bug.cgi?id=173042) Improved / pluggable **Refresh**:
        *   Subsystems must be able to **refresh without flickering and without losing selection** \- systemView contents must remain until updated results are in the model and a refresh event comes from the model. Selection must be maintained wherever possible.
        *   DaveM: RSE has always been like throwing away children on refresh; it was synchronous, so Expand would hang the UI
        *   DaveM: Eclipse Deferred Query Framework currently used. Michael: Refresh and deferred loading are two very different things - refresh "patches" the tree with obtained data
        *   We must be asynchronous: user's refresh operation must not remove tree items but rather just call the subsystem with a refresh query.
        *   Currently: SystemRefreshAction fires Event.REFRESH. Event is handled by the tree, actually doing the query. Old RSE was very synchronous.
            *   Now we'd have two different kinds of events - (a) REFRESH meaning "get new information" and (b) REFRESH meaning "I've got new information in the model"
        *   **Requirements**
            *   1\. Framework must not throw away children on Event.REFRESH, and properly merge them when results are available. All subsystems would benefit from that. Also because there would be 2 queries if we did not have caching
            *   2\. Subsystems are themselves responsible for updating their model.
            *   3\. Once the model is up-to-date, it tells the RSE views that new data is available
        *   DaveM is currently busy; **AI Martin** to make a start this week, Dave to review
    *   [166338](https://bugs.eclipse.org/bugs/show_bug.cgi?id=166338) Asynchronous **Callbacks** \- **AI Martin** to start
    *   **expandTo()** API for the RSE System View - Events are not sufficient: due to lazy evaluation only one level works. Want a TreePath to expand - similar to SystemRemoteFolderDialog.setPreSelection(): Dave currently turning off deferred queries temporarily to make that happen
        *   Need a Utility class for operations on the SystemView; even without a view, a single multi-level query would be nice... need both a non-UI multi-level query ("walk the tree from here to here") and a view-level expand operation.
        *   View-level operation is just a utility class... non-UI expand functionality would perhaps just fire the right expand events ... might go hand-in-hand with the new Refresh mechanism.
    *   [170922](https://bugs.eclipse.org/bugs/showdependencytree.cgi?id=170922) (DaveM, Martin) Making as much as possible "internal"

*   **Other Business**
    *   **Cleanup**: If we want to run the JDT Cleanup wizard to bring our code to Eclipse Standards, we better do so before M6 since we want to more closely monitor code changes after M6... or is it sufficient for M7? Copyright Wizard to run for M7.
        *   DaveD likes sun style; DaveM accustomed to curly braces on separate line but is ok with changing (happy to conform with a standard); DaveM uses cleanup-on-save
        *   Agree to have cleanup as soon as possible **AI Martin start with one plugin**
        *   Uwe to delete IRSEUIRegistry and implementation and getters
    *   [170915](https://bugs.eclipse.org/bugs/showdependencytree.cgi?id=170915) (DaveM) Getting rid of Platform "internal" access
    *   add **unit tests** for all new or modified API

**Priorities** are folded into the Action Items below

### Other Stuff to Do

*   **1\. Play well with the Platform**
    *   capabilities; icu4j; Orbit; ssh prefs; drag&drop
    *   retargetable actions/commands instead of actionsets;
*   **2\. Improve overall quality (unit tests; special characters; long filenames; background jobs; parallel access; logging; ...)**
*   **3\. New Features**
    *   Persistence-as-xmlfile; Service enablement
*   **4\. Cleanup/Optimization**
    *   Remove RSE Performance Logging; place contents of logging into core
    *   Reduce number of plugins (once UI/Non-UI separation is done, and once we have Capabilities: have e.g. ssh.core and ssh.ui but not more)
        *   Move org.eclipse.rse.connectorservice.local into org.eclipse.rse.subsystems.core
        *   org.eclipse.rse.subsystems.core (collapse files.core, processes.core, shells.core)
        *   org.eclipse.rse.subsystems.dstore (collapse files.dstore, processes.dsore, shells.dstore)
    *   **Build Process Improvements**
        *   Orbit bundles to be added differently
        *   Unittests to run every night (Ted's scripts)
        *   Version Number Changes to be done by Martin
    *   [174945](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174945) General code cleanup - get rid of unused icons, comments, properties
    *   **Update Copyright Year to 2007 if you happen to think about it**
    *   Please continue on Compiler Warnings

### Communications

*   **Europa Requirements**
    *   **Avoiding non-API from other projects**
        *   **AI Martin** create bugzilla against CDT
    *   Update Wiki to explain whether SDK contains examples --> **AI Martin** wait for Platform and adapt
*   For bugs, see the [bug process page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) (assigned to inbox, plan items, status new, hi-priority, API, open with patch, assigned to M6) -- 54 right now
*   Change Requests
*   Vacations, Holidays etc.
*   Free discussion -- feelings, comments, critics
    *   **May need another meeting this week once we get hold of Kushal and Javier**

Action Items
------------

*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_28-Feb-2007#Action_Items "DSDP/TM/Committer Phone Meeting 28-Feb-2007") Action Items
*   **DaveD** \- Check whether systemType name is persisted; Refactoring UI/Non-UI
*   **DaveM** \- Review Refresh; Bugs & Unit tests
*   **Kushal** \- EFS, Subsystem Bugs, Encoding Tests; Talk to DaveD re Comm Server; Bugs & Unit Tests
*   **Martin** \- Orbit changes; Website updates (M5); Migrate build to Ted's scripts; Bugs & Unit Tests; Personal Interviews via Skype; Work on [TM and RSE FAQ](./TM_and_RSE_FAQ "TM and RSE FAQ"), improve Wiki and Website (how to contribute);
*   **Javier** \- Improve SD; Bugs & Unit Tests
*   **Ted** -
*   **Michael** \- Terminal Performance Improvements
*   **Uwe** -

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 20-Mar-2007](./DSDP/TM/Committer_Phone_Meeting_20-Mar-2007 "DSDP/TM/Committer Phone Meeting 20-Mar-2007") at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=3&day=20&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_13-Mar-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_13-Mar-2007))