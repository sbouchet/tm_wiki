

DSDP/TM/Committer Phone Meeting 13-Feb-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Feb 13, 2007](./index.php?title=Feb_13,_2007&action=edit&redlink=1 "Feb 13, 2007 (page does not exist)") at [1700 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=2&day=13&hour=17&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
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
    *   [2.3 Communications](#Communications)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave McKnight, Dave Dykstal, Kushal Munir
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber (Michael Scharf n/a, Ted Williams n/a)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help: **being responsive**
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site

### Latest News

| Martin | 50% | RXTX improvements. Move RSE on M5. Making stuff "internal". | 50% |
| --- | --- | --- | --- |
| DaveD | 80% | UI/Non-UI refactoring; roadblock finishing up today; UA:IPzilla expected later today | 10% |
| DaveM | 50% | passing filter into getChildren | 50% |
| Kushal | 100% | encodings; javier's bug | 80% |
| Javier | 50% | ftp passive mode; need to fix ui | 50% |
| Ted | 0% |  | 0% |
| Uwe | 0% | dynamic systemTypes; subsystem<->systemtype association; new conn.wizard | 0% |
| Michael | 20% |  | 20% |

*   Growing Communities: Robert Norton doing Launch Actions; Oliver Hardt doing EFS; 1245 downloads of RSE 1.0.1
*   Getting the APIs right

### Upcoming Work

*   **Top priority** this week is getting API things done for M5. Plan items are currently more important than bug priorities.
    *   [163820](https://bugs.eclipse.org/bugs/show_bug.cgi?id=163820) (Kushal) Encodings
        *   Code done, Test cases to be done
    *   ([Bugzilla#173772](https://bugs.eclipse.org/bugs/show_bug.cgi?id=173772)) **RSE New Connection Wizard Rework**
        *   Work started. Goal is to make the new connection wizard looking and behaving like standard Eclipse new, import or export wizards. This should and will include support of categories in the new connection dialog. Current newConnectionWizardDelegate extension point and implementation is duplicating more or less existing Eclipse wizard framework functionality (via WizardDialog.setWizard(...) and IWizardPage.getWizard()). Fallback to use as much of standard Eclipse interfaces and existing functionality as possible (IWizardNode, IWizardRegistry, IWizardDescription, IWizardCategory, WizardSelectionPage and related).
        *   Does any one has a problem with reworking newConnectionWizardDelegate extension point to be a newConnectionWizard extension point contributing a standard IWizard??
    *   [173042](https://bugs.eclipse.org/bugs/show_bug.cgi?id=173042) (Uwe) Improved / pluggable Refresh
        *   WR can't live with refresh throwing away children and showing "pending".
        *   Unaffected nodes need to remain; when only properties are changed, nodes need to remain;
        *   Subsystems need to be more responsible for the Refresh policy to accomplish this
    *   [170909](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170909) (DaveD) User Actions & Import/Export
        *   Expect initial submission on ipzilla later today
    *   [170923](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170923) (DaveD) UI/Non-UI splitting
        *   Concentrate on bringing .core in one place so it can be refactored later
        *   OK for martin to continue on the IConnectorService thing, it should be fairly straightforward and self-contained
        *   Anonymous login for ftp is also associated with this;
        *   Dave will keep in touch and continue working from Florida, though not full-time
    *   [170627](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170627) (DaveM) ISystemFilter in SystemViewElementAdapter.getChildren()
        *   Tobias looking at a solution where SubSystem.resolveFilterString() returns wrapper objects which also hold a context
            *   Problem: Selection etc. will return the wrapper object, and not the model object. Also, ISVs would contribute against model objects and not the wrapper
            *   Doing this for Windriver now; looking at a solution that can be shared by RSE
        *   Idea from DaveD: Intercept the expand event, and construct an object that contains Element + Context for the Content Provider
            *   Context for IRemoteFile is Subsystem + Filter + Parentnode
            *   Don't want multiple model objects for the same physical thing any more
    *   [170922](https://bugs.eclipse.org/bugs/showdependencytree.cgi?id=170922) (DaveM, Martin) Making as much as possible "internal": SystemView, SystemFilterReferenceAdapter, Subsystem Impls
        *   DaveD: original idea of RSE was to make stuff convenient; now its good to make it internal
        *   AI: component owners to go ahead and make stuff internal
    *   [170915](https://bugs.eclipse.org/bugs/showdependencytree.cgi?id=170915) (DaveM) Getting rid of Platform "internal" access
        *   (done) popupMenus and propertyPages removed; need migration docs, for testAttribute; need to think about what to do with ISV docs
            *   DaveD: Our examples should be complete. We should improve the example to show the list of attributes we can check for through the IActionFilter
            *   DaveM: Create a new enhancement request for that; Martin to do it
            *   Also check Javadoc of ISystemViewElementAdapter, IRemoteFileAdapter
    *   [170916](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170916) (Kushal) EFS
        *   Oliver Hardt looking at it; Kushal to look at limiting API as next task, then do the Streams for IFileService;
        *   DaveM: DStore Streams API: While downloading a file, open a separate stream to look at it while downloading?
    *   Martin & DaveM work on EclipseCon tutorial: fix bugs as needed
    *   [170832](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170832) (Martin) Read-only setting on ssh - what about using EFS on the back-end? (dstore doesnt do streams)
        *   AI timestamp, ro-flags: already done for FTP, still TBD for ssh
    *   add **unit tests** for all new or modified API

### Communications

*   **Next Week is Milestone Week**
    *   Do the [TM 2.0 M5 Testing](./TM_2.0_M5_Testing "TM 2.0 M5 Testing") on Tuesday this time (warmup I-builds on Monday)
*   **Europa Requirements**
    *   (done) [TM 2.0 Ramp down Plan for Europa](./TM_2.0_Ramp_down_Plan_for_Europa "TM 2.0 Ramp down Plan for Europa")
        *   Replace "n PMC members" by "a PMC member + n committers". With that change, everybody is ok with making it public.
    *   (done) Update features and include the words "end-user" and "extender"
    *   **Avoiding non-API from other projects**
        *   AI create bugzilla against CDT; focus more towards M6
    *   Update Wiki to explan whether SDK contains examples --> AI Martin wait for Platform and adapt
*   For bugs, see the [bug process page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) (assigned to inbox, plan items, status new, hi-priority, API, open with patch, assigned to M5) -- pretty many right now
*   **Update Copyright Year to 2007 if you happen to think about it**
*   Please continue on Compiler Warnings
*   Change Requests
*   Vacations, Holidays etc.
    *   DaveD going to Florida in February for a week
    *   Kushal might be away Friday 23rd
    *   Javier away Feb 27th - March 2nd
*   Free discussion -- feelings, comments, critics

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_6-Feb-2007#Action_Items "DSDP/TM/Committer Phone Meeting 6-Feb-2007") Action Items
*   **DaveD** \- attach User Actions on IPZilla; UI/Non-UI Refactoring; Making stuff internal.
*   **DaveM** \- Passing Filter into getChildren; EclipseCon; Making stuff internal.
*   **Kushal** \- Unit Tests for Encodings; Javier's bug; Download Streams API; Making stuff internal; EFS.
*   **Martin** \- ISV docs for propertyPages and popupActions; Making stuff internal; Check r/o flags and timestamps for ssh; Commit Montavista contrib; EclipseCon tutorial; Migrate build to Ted's scripts; create bugzilla against CDT.
*   **Javier** \- FTP passive mode; Improve SD; Making stuff internal.
*   **Ted** -
*   **Michael** \- Terminal Performance Improvements
*   **Uwe** \- newConnectionWizardDelegate.

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 20-Feb-2007](./Committer_Phone_Meeting_20-Feb-2007 "DSDP/TM/Committer Phone Meeting 20-Feb-2007") at [1700 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=2&day=20hour=17&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_13-Feb-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_13-Feb-2007))