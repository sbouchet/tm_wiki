

DSDP/TM/Committer Phone Meeting 30-Jan-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Jan 30, 2007](./index.php?title=Jan_30,_2007&action=edit&redlink=1 "Jan 30, 2007 (page does not exist)") at [1700 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=1&day=30&hour=17&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
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

*   IBM - Dave McKnight, (Dave Dykstal n/a, Kushal Munir n/a)
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber, Michael Scharf, (Ted Williams n/a)

Notes
-----

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help: **being responsive**
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site

### Latest News

| Martin | 50% | Created project plan; PluginFest; Worked with Platform on ssh prefs; Added symlinks to EFS; mail&news; EclipseCon | 50% |
| --- | --- | --- | --- |
| DaveD | 80% | Preparations in Persistence for User Actions | 80% |
| DaveM | 50% | EclipseCon; Bugs; | 50% |
| Kushal | 0% | Encodings; starting [bug 150265](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150265) for Javier; EFS | 100% |
| Javier | 20% | PluginFest; Going to do FTP passive mode and FTP anonymous login this week | 50% |
| Ted | 0% |  | 0% |
| Uwe | 0% |  | 0% |
| Michael | 0% | Started work on Terminal performance improvements | 20% |

*   PluginFest: Javier might extend the Symbian internal remote framebuffer work to allow other RFB protocols, e.g. VNC
    *   Motorola is interested
    *   Michael: the Visual Editor (ve) people seem to do something similar - copying a screen from some external window
    *   Michael: IBM integrated Lotus Notes in Eclipse, mapping the Notes views into Eclipse
    *   Javier registered for a Short Talk at EclipseCon

### Upcoming Work

*   **Top priority** this week is work on the feature "big rocks" in bugzilla, for [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning")
    *   Martin & DaveM work on EclipseCon tutorial
    *   add **unit tests** for all new or modified API
*   New **Europa Requirements** from [Planning Council Meeting 23-Jan-2007](https://www.eclipse.org/org/councils/20070123PCMinutes.php)
    *   Written ramp down policy by Feb. 23rd --> AI Martin: wait for what Platform does and adapt it
    *   **Avoiding non-API from other projects**
        *   AI create bugzillas for getting rid of Platform Internal access and hook them up with a plan item; Europa requires that these are in the release notes and there is a plan for addressing these in the next major release
        *   AI re-enable compiler warnings for non-API; fix still open compiler warnings
    *   Report Strings for translation --> AI DaveD report to Bjorn
    *   Update features and include the words "end-user" and "extender" --> AI Martin wait for Platform and adapt
    *   Update Wiki to explan whether SDK contains examples --> AI Martin wait for Platform and adapt
*   For bugs, see the [bug process page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) (assigned to inbox, plan items, status new, hi-priority, API, open with patch, assigned to M5) -- pretty many right now
*   [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning")
    *   **1\. Play well with the Platform**
        *   get rid of platform "internal" access; this may also mean getting rid of customized extension points for adding actions
        *   retargetable actions/commands; capabilities; icu4j; Orbit; ssh prefs; drag&drop
        *   AI: Martin to enable compiler warnings for internal access
        *   DaveM to check
    *   **2\. Make APIs usable for clients, harden the APIs, improve documentation**
        *   Make stuff internal: SystemView, SystemFilterReferenceAdapter, Subsystem Impls
*   **Compiler Warnings**
    *   Good progress, please continue. Most warnings are javadoc warnings now. See the [Committer Howto](https://www.eclipse.org/dsdp/tm/development/committer_howto.php#check_code) for settings
        *   109 -> 113 -> 113 -> 3 connectorservice.dstore
        *   176 -> 265 -> 161 -> 12 rse.core
        *   474 -> 558 -> 558 -> 94 files.ui
        *   637 -> 662 -> 662 -> 23 services (javadoc)
        *   221 -> 250 -> 248 -> 27 subsystems.files.core
        *   1622 -> 346 -> 293 -> 192 rse.ui (mostly javadoc)

### Communications

*   Vacations, Holidays etc.
    *   DaveD going to Chicago end of the month; Florida in February for a week
*   Free discussion -- feelings, comments, critics
    *   Decided to fix the committer meeting slot to 1700 UTC (same as today) to avoid confusion due to changing meeting time.

Action Items
------------

*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_16-Jan-2007#Action_Items "DSDP/TM/Committer Phone Meeting 16-Jan-2007") Action Items
*   **DaveD** \- Remove RSE Performance Logging; Refactoring UI/Non-UI; Persistence; Bugzilla bug for User Actions Contribution until Jan.31st; Bugs & Unit tests;
*   **DaveM** \- EclipseCon; Bugs & Unit tests; finish permission API; download Streams API;
*   **Kushal** \- Encodings; EFS; Talk to DaveD re Comm Server; Bugs & Unit Tests
*   **Martin** \- EclipseCon tutorial; Check r/o flags and timestamps for ssh; Commit Montavista contrib; Migrate build to Ted's scripts; Migrate Commons.net to single-file-jar; Bugs & Unit Tests; Personal Interviews via Skype; Work on [TM and RSE FAQ](./TM_and_RSE_FAQ "TM and RSE FAQ"), improve Wiki and Website (how to contribute);
*   **Javier** \- Check r/o flags and timestamps for ftp; FTP passive mode; Improve SD; Bugs & Unit Tests
*   **Ted** -
*   **Michael** \- Terminal Performance Improvements
*   **Uwe** -

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 6-Feb-2007](./DSDP/TM/Committer_Phone_Meeting_6-Feb-2007 "DSDP/TM/Committer Phone Meeting 6-Feb-2007") at [1700 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=2&day=6hour=17&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Open [DSDP/TM/Phone Meeting 7-Feb-2007](./DSDP/TM/Phone_Meeting_7-Feb-2007 "DSDP/TM/Phone Meeting 7-Feb-2007") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_30-Jan-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_30-Jan-2007))