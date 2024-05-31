

DSDP/TM/Phone Meeting 3-Sep-2008
================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Wednesday Sep 3, 2008 at [1600 UTC / 9am PST](http://www.timeanddate.com/worldclock/fixedtime.html?month=9&day=3&year=2008&hour=16&min=00&sec=0&p1=0)   ![Html.gif](./images/Html.gif)[HTML](http://www.google.com/calendar/embed?src=vn70im36r00qeusu8nme50cils@group.calendar.google.com&ctz=Canada/Toronto) \| ![Ical.gif](./images/Ical.gif)[iCal](http://www.google.com/calendar/ical/vn70im36r00qeusu8nme50cils@group.calendar.google.com/public/basic.ics) |
| Primary International Dial-in: | **+44 (0)1452 567588** |
| USA Freephone Dial-In: | +1 (866) 6161738 |
| UK National Dial-In: | 08712460713 |
| Passcode: | **0587322148 #** |

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 Last Meetings](#Last-Meetings)
    *   [2.2 Update on RSE Status](#Update-on-RSE-Status)
        *   [2.2.1 TM 3.0.1](#TM-3.0.1)
        *   [2.2.2 TM 3.1](#TM-3.1)
        *   [2.2.3 Other Stuff](#Other-Stuff)
        *   [2.2.4 Individual Status](#Individual-Status)
    *   [2.3 Community Feedback and Status](#Community-Feedback-and-Status)
*   [3 Vacations, Next Meetings](#Vacations.2C-Next-Meetings)
    *   [3.1 Action Items](#Action-Items)
    *   [3.2 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Xuan Chen, Kevin Doyle, Dave Dykstal, Dave McKnight
*   Wind River - Martin Oberhuber
*   MontaVista - Anna Dushistova

Notes
-----

### Last Meetings

*   Last [DSDP/TM/Phone Meeting 6-Aug-2008](./Phone_Meeting_6-Aug-2008 "DSDP/TM/Phone Meeting 6-Aug-2008")
*   Last [DSDP/TM/Committer Phone Meeting 20-Aug-2008](./Committer_Phone_Meeting_20-Aug-2008 "DSDP/TM/Committer Phone Meeting 20-Aug-2008")

### Update on RSE Status

#### TM 3.0.1

*   [DSDP/TM/3.0 Ramp down Plan for Ganymede](./3.0_Ramp_down_Plan_for_Ganymede "DSDP/TM/3.0 Ramp down Plan for Ganymede")
*   Some questions from Martin outstanding: DD: [bug 236516](https://bugs.eclipse.org/bugs/show_bug.cgi?id=236516) ISubSystem patch, DKM: [bug 235284](https://bugs.eclipse.org/bugs/show_bug.cgi?id=235284) dstore ClientConnection patch, DKM: [bug 234045](https://bugs.eclipse.org/bugs/show_bug.cgi?id=234045) permissions property page
*   Will freeze / branch for RC1 today
*   Policy after the branching:
    *   Create a separate Workspace for the branch, where all plugins are at the Mapfile version!
    *   Only fix critical issues in the branch!
    *   Only commit / release after at least 1 person's review!
    *   Before committing: (1) synchronize rse.build (Mapfile) from branch R3\_0\_maintenance, then (2) Team > Replace with Mapfile Contents, then (3) Team > Branch the Plugin
        *   Branch name: R3\_0\_maintenance, Root at Root\_R3\_0_maintenance
        *   When releasing from a branch, release as "r30x_v200809102000" (UTC timestamp) - in order to avoid clashes with I-builds
*   Any Known Issues to be fixed?
    *   Display issues and modelChangeListener working properly now?
    *   EFS deadlock problems during early startup currently being discussed, [bug 239230](https://bugs.eclipse.org/bugs/show_bug.cgi?id=239230) OK now?
*   When / How much Testing?
    *   IBM absorbing builds, unsure what the cycles are.
    *   [bug 187739](https://bugs.eclipse.org/bugs/show_bug.cgi?id=187739) seems risky: scenario is expanding a tree and refreshing a parent node

#### TM 3.1

*   TM Plan rendered [here](https://www.eclipse.org/projects/project-plan.php?projectid=dsdp.tm), along with a [DSDP/TM/3.1 Ramp down Plan](./3.1_Ramp_down_Plan "DSDP/TM/3.1 Ramp down Plan")
    *   Martin not investing in EFS any more, [E4](./E4 "E4") going different ways for remote resources: remotifying transparently is not always right, clients need to be aware of things being remote -- see [E4 Mailing List](http://dev.eclipse.org/mhonarc/lists/eclipse-incubator-e4-dev/msg00616.html) postings
    *   DaveM -- using EFS right now, unsure about plans for the future
*   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit) open bugs, [High Priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor) open bugs, [DSDP/TM/3.0 Known Issues and Workarounds](./3.0_Known_Issues_and_Workarounds "DSDP/TM/3.0 Known Issues and Workarounds")
*   [bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176) \- Deferred drag&drop from RSE to Windows Explorer is possible but it needs more work and collaboration with the SWT team. We need to find out how to report progress for the background file transfer.

#### Other Stuff

*   [DSDP/TM/Board Report 2008](./Board_Report_2008 "DSDP/TM/Board Report 2008")
*   [bug 238574](https://bugs.eclipse.org/bugs/show_bug.cgi?id=238574) Website Revamp? We have a bugzilla "Website" component now
*   **Target Communication Framework** \- [DSDP/TM/TCF FAQ](./TCF_FAQ "DSDP/TM/TCF FAQ") available and plan theme, shooting for 1.0 under discussion. EDL approved for the Agent. Community interest growing
    *   [bug 238564](https://bugs.eclipse.org/bugs/show_bug.cgi?id=238564) has some very good notes about migrating from TM 2.0 to TM 3.0
    *   Working towards scheduled builds and downloadable artifacts.

#### Individual Status

*   Martin now working much on [Architecture Council](https://wiki.eclipse.org/Architecture_Council "Architecture Council"), [E4](https://wiki.eclipse.org/E4 "E4") and RXTX - for TM related status see [DSDP/TM/Committer Phone Meeting 20-Aug-2008](./Committer_Phone_Meeting_20-Aug-2008 "DSDP/TM/Committer Phone Meeting 20-Aug-2008")
*   DaveD hopes to get back to more OpenRSE stuff over time (October)
*   Xuan, Kevin likely continue working heavily on IBM portion until October at least
*   DaveM mostly on OpenRSE (at least 60%)
*   Anna moved away from Open Source, hopes to get back (to Terminal) next month.

### Community Feedback and Status

*   Community contributions
    *   Patrick Juhl - SSH Tunnel - no news
    *   [bug 196337](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196337) \- TM Local Terminal Connector

Vacations, Next Meetings
------------------------

*   Vacations, away times
*   Questions

### Action Items

*   Last meeting: [DSDP/TM/Phone Meeting 6-Aug-2008](./Phone_Meeting_6-Aug-2008 "DSDP/TM/Phone Meeting 6-Aug-2008")
*   Last [DSDP/TM/Committer Phone Meeting 20-Aug-2008](./Committer_Phone_Meeting_20-Aug-2008 "DSDP/TM/Committer Phone Meeting 20-Aug-2008")
*   All committers fix target milestone of bugs assigned to 3.0
*   **Martin** **old** review Rado's deferred D&D

### Next Meeting

*   Next [DSDP/TM/Committer Phone Meeting 17-Sep-2008](./Committer_Phone_Meeting_17-Sep-2008 "DSDP/TM/Committer Phone Meeting 17-Sep-2008") (2 weeks after)
*   Next [DSDP/TM/Phone Meeting 1-Oct-2008](./Phone_Meeting_1-Oct-2008 "DSDP/TM/Phone Meeting 1-Oct-2008") (4 weeks after)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_3-Sep-2008](https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_3-Sep-2008))