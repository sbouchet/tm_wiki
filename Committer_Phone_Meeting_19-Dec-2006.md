

DSDP/TM/Committer Phone Meeting 19-Dec-2006
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Dec 19, 2006](./index.php?title=Dec_19,_2006&action=edit&redlink=1 "Dec 19, 2006 (page does not exist)") at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=12&day=19&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 Recent Download Statistics](#Recent-Download-Statistics)
    *   [2.2 Latest News](#Latest-News)
    *   [2.3 Looking back on 1.0.1](#Looking-back-on-1.0.1)
    *   [2.4 Upcoming Work](#Upcoming-Work)
    *   [2.5 Communications](#Communications)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave Dykstal, Dave McKnight, (Kushal Munir n/a)
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber, (Michael Scharf n/a, Ted Williams n/a)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help: **being responsive**
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site

### Recent Download Statistics

RSE 1.0 Download statistics as per 19-Dec-2006
| Component | RC3 | RC4 | 1.0 | 1.0.1 | Note |
| --- | --- | --- | --- | --- | --- |
| Date | 30-Oct | 03-Nov | 12-Nov | 15-Dec |  |
| RSE-SDK | 113 | 146 | 458 | 40 |  |
| rseserver-windows | 24 | 63 | 185 | 7 |  |
| rseserver-linux | 19 | 25 | 133 | 11 |  |
| rse.core (Update Site) | 72 | 28 | 172 | 52 | 1.0 src is 156 |
| Total | 185 | 174 | 630 | 92 |  |
| examples |  | 27 | 85 | 7 |  |
| remotecdt |  | 7 | 66 | 7 | per 1.0.1, remotecdt is no longer in SDK |
| discovery |  | 13 | 68 | 9 |  |
| efs |  | 12 | 42 | 8 |  |
| terminal |  | - | - | 12 |  |

*   1.0: 85 examples -- people do want to code against RSE APIs
*   68 discovery -- some interest
*   update site gaining significance with 1.0.1
*   For more analysis, see [DSDP/TM/Phone Meeting 8-Nov-2006](./Phone_Meeting_8-Nov-2006 "DSDP/TM/Phone Meeting 8-Nov-2006")

### Latest News

| Martin | 80% | Packaging Terminal, Releasing 1.0.1, Fixing, Planning 2.0 | 50% |
| --- | --- | --- | --- |
| DaveD | 80% |  | 80% |
| DaveM | 80% |  | 80% |
| Kushal | 50% |  | 0% |
| Javier | 50% | compiler warnings | 50% |
| Ted | 5% | creating org.eclipse.rse.releng.builder | 80% |
| Uwe | 50% | test framework, unit tests | 50% |
| Michael | 40% | terminal fixes |  |

### Looking back on 1.0.1

*   [RSE 1.0.1 Testing](./RSE_1.0.1_Testing "RSE 1.0.1 Testing") statistics (links on bottom of page):
    *   63 bugs fixed, 40 verified, 7 reopened, 6 new:
        *   16 not yet verified; **more than 11% reopened!**
    *   We need to improve the quality of our bug fixes, and decrease the time for verification: using **unit tests**
    *   When picking a bug, pick one that's "testable" and start writing a unit test for it. Then, fix it.
        *   After jumping over an initial hurdle of unit tests, we'll soon earn the fruit of enhanced quality and less time needed for testing
    *   bugs assigned to target 1.0.1 but left open are now assigned to 2.0M4 (currently 46 bugs) - see the [bug process page](https://www.eclipse.org/dsdp/tm/development/bug_process.php)

### Upcoming Work

*   **Top priority** this week is a stable 2.0M4 --> **Finish off some cleanup**, **add unit tests**
*   When to fork off 2.0 API changes?
    *   Can start right away (e.g. "anonymous" ftp access), but quality must be high:
    *   add **unit tests** for all new or modified API
    *   document API changes (on build notes, tm-dev list or where?)
*   Planning 2.0
    *   Dates are governed by Europa: M4=**Jan 4**, M5=**Feb 23**==EclipseCon, M6=**Apr 6**==API Freeze, M7=**May 18**==RC0
    *   Start IBM and EMO review process for User Actions and Import/Export (DaveD)
        *   Also need a CQ for two Userdoc files for the Internal Comms Daemon? (Kushal, DaveD)
    *   [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") \- Finalize the 2.0 Project Plan, **Priorities:**
        *   **1\. Make APIs usable for clients, harden the APIs, improve documentation**
            *   SystemType improvements; retargetable actions/commands; read-only flags; Streams for IHostShell, IFileService; UI/Non-UI Refactoring; make RSE more service-oriented
        *   **2\. Make EFS work**
        *   **3\. Play well with the Platform**
        *   **4\. Improve overall quality (unit tests; special characters; long filenames; background jobs; parallel access; ...)**
    *   Think about limiting the API: Make APIs internal along the way of updating documentation, and making Unit tests, we'll see some API we want "internal".
    *   For bugs, see the [bug process page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) (assigned to inbox, status new, hi-priority, API, open with patch)

### Communications

*   Vacations, Holidays etc.
    *   Kushal away from 18th
    *   DaveD away 22nd and most of Thu 21st but may work a little 25th to 1st
    *   Martin, DaveM away from 25th to 1st
    *   Javier away from 25th to 8th
*   Free discussion -- feelings, comments, critics

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_12-Dec-2006#Action_Items "DSDP/TM/Committer Phone Meeting 12-Dec-2006") Action Items
*   **DaveD** \- Bugs & Unit tests; New bug for moving DTD.
*   **DaveM** \- Bugs & Unit tests; Compiler Warnings (dstore);
*   **Kushal** \- Compiler Warnings (UI); Talk to DaveD re Comm Server; Bugs & Unit Tests
*   **Martin** \- Bugs & Unit Tests; Features for Unittests; Add Jakarta Commons to Orbit; Plan Item Specifications; Personal Interviews via Skype; Work on [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning"); [TM and RSE FAQ](./TM_and_RSE_FAQ "TM and RSE FAQ"), improve Wiki and Website (how to contribute);
*   **Javier** \- Bugs & Unit Tests; Specification for "RSE should be more service oriented"
*   **Ted** \- Prepare Europa build (in org.eclipse.rse.releng.builder)
*   **Michael** -
*   **Uwe** \- RSE Systemview performance unit tests

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 2-Jan-2007](./Committer_Phone_Meeting_2-Jan-2007 "DSDP/TM/Committer Phone Meeting 2-Jan-2007") at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=1&day=2hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Open [DSDP/TM/Phone Meeting 10-Jan-2007](./Phone_Meeting_10-Jan-2007 "DSDP/TM/Phone Meeting 10-Jan-2007") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_19-Dec-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_19-Dec-2006))