

DSDP/TM/Committer Phone Meeting 6-Feb-2007
==========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Feb 6, 2007](/index.php?title=Feb_6,_2007&action=edit&redlink=1 "Feb 6, 2007 (page does not exist)") at [1700 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=2&day=6&hour=17&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
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
*   Wind River - Martin Oberhuber, Uwe Stieber, Michael Scharf, Ted Williams

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help: **being responsive**
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site

### Latest News

| Martin | 50% | EclipseCon; EFS Symlinks; Enabled "internal" warnings; Bugzilla discussions. | 50% |
| --- | --- | --- | --- |
| DaveD | 80% | UDA contribution work, ready to submit next week; cleaned up M5 backlog; moving core UI->core | 100% |
| DaveM | 50% | EclipseCon; IBM stuff; reading+commenting on bugs | 50% |
| Kushal | 100% | Encodings; adding unittests now; discovery w/javier | 100% |
| Javier | 50% | [169680](https://bugs.eclipse.org/bugs/show_bug.cgi?id=169680) passive mode; | 50% |
| Ted | 0% |  | 0% |
| Uwe | 20% | adapting RSE; filing bugs, attaching patches | 20% |
| Michael | 20% | improving Terminal performance | 20% |

*   Javier: PropertySetContainer doesnt persist Boolean -- AI file a bug and write a unit test
*   DaveD: How were the "internal" warnings done? - Martin: in Manifest.mf export-package: statement add;x-internal="true"

### Upcoming Work

*   **Top priority** this week is getting API things done for M5. Plan items are currently more important than bug priorities.
    *   Martin & DaveM work on EclipseCon tutorial: fix bugs as needed
    *   [170923](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170923) (DaveD) UI/Non-UI splitting
    *   [163820](https://bugs.eclipse.org/bugs/show_bug.cgi?id=163820) (Kushal) Encodings
    *   [170916](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170916) (Kushal) EFS
        *   What about putting EFS directly on top of IFileService without using the cache
    *   [170627](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170627) (DaveM) ISystemFilter in SystemViewElementAdapter.getChildren()
    *   [173042](https://bugs.eclipse.org/bugs/show_bug.cgi?id=173042) (Uwe) Improved / pluggable Refresh
    *   [170832](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170832) (Martin) Read-only setting on ssh - what about using EFS on the back-end? (dstore doesnt do streams)
    *   [170922](https://bugs.eclipse.org/bugs/showdependencytree.cgi?id=170922) (DaveM, Martin) Making as much as possible "internal": SystemView, SystemFilterReferenceAdapter, Subsystem Impls
        *   AI: component owners to come up with a list by thursday
    *   [170915](https://bugs.eclipse.org/bugs/showdependencytree.cgi?id=170915) (DaveM) Getting rid of Platform "internal" access
        *   ok with getting rid of popupMenus; testAttribute() already implemented in SystemViewElementAdapter
        *   dynamicPopupMenus? - If we can't live without Platform "internal" access, we should get rid of it - Uwe thinks it can be done with standard Eclipse.
        *   Plan: 1. re-write usage of popupMenus etc. to use plain Eclipse; 2. get rid of EP --> AI DaveM
    *   add **unit tests** for all new or modified API

*   New **Europa Requirements** from [Planning Council Meeting 23-Jan-2007](https://www.eclipse.org/org/councils/20070123PCMinutes.php)
    *   Written ramp down policy by Feb. 23rd --> AI Martin: wait for what Platform does and adapt it
    *   **Avoiding non-API from other projects**
        *   AI create bugzillas for getting rid of Platform Internal access and hook them up with a plan item; Europa requires that these are in the release notes and there is a plan for addressing these in the next major release
    *   Update features and include the words "end-user" and "extender" --> AI Martin wait for Platform and adapt
    *   Update Wiki to explain whether SDK contains examples --> AI Martin wait for Platform and adapt
*   For bugs, see the [bug process page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) (assigned to inbox, plan items, status new, hi-priority, API, open with patch, assigned to M5) -- pretty many right now

### Communications

*   General code cleanup -- to do right after M4:
    *   Get rid of unused icons, e.g. rse.ui/icons/full/obj16/system390\_obj.gif, IBM\_logo.gif
    *   Get rid of commented out source code
    *   Get rid of unused properties (chkpii)
*   Change Requests
*   Vacations, Holidays etc.
    *   DaveD going to Florida on Thursday next week (Feb 15th-21st)
*   Free discussion -- feelings, comments, critics
    *   Decided to fix the committer meeting slot to 1700 UTC (same as today).

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_30-Jan-2007#Action_Items "DSDP/TM/Committer Phone Meeting 30-Jan-2007") Action Items
*   **Everybody** \- Come up with a list of classes from the areas you own, which can be internal (by thursday)
*   **DaveD** \- Refactoring UI/Non-UI; Persistence; Bugzilla bug for User Actions Contribution; Remove RSE Performance Logging; Bugs & Unit tests;
*   **DaveM** \- EclipseCon; re-write rse.popupMenus usage; Bugs & Unit tests; finish permission API; download Streams API;
*   **Kushal** \- Encodings; EFS; Talk to DaveD re Comm Server; Bugs & Unit Tests
*   **Martin** \- EclipseCon tutorial; Check r/o flags and timestamps for ssh; Commit Montavista contrib; Migrate build to Ted's scripts; Migrate Commons.net to single-file-jar; Bugs & Unit Tests; Personal Interviews via Skype; Work on [TM and RSE FAQ](/TM_and_RSE_FAQ "TM and RSE FAQ"), improve Wiki and Website (how to contribute);
*   **Javier** \- Unittest for Boolean Propertyset; Check r/o flags and timestamps for ftp; FTP passive mode; Improve SD
*   **Ted** -
*   **Michael** \- Terminal Performance Improvements
*   **Uwe** -

Next Meeting
------------

*   Open [DSDP/TM/Phone Meeting 7-Feb-2007](/DSDP/TM/Phone_Meeting_7-Feb-2007 "DSDP/TM/Phone Meeting 7-Feb-2007") at 9am PST
*   [DSDP/TM/Committer Phone Meeting 13-Feb-2007](/DSDP/TM/Committer_Phone_Meeting_13-Feb-2007 "DSDP/TM/Committer Phone Meeting 13-Feb-2007") at [1700 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=2&day=13hour=17&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_6-Feb-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_6-Feb-2007))