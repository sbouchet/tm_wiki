

DSDP/TM/Phone Meeting 7-Feb-2007
================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Wednesday February 7, 2007 at [1700 UTC / 9am PST](http://www.timeanddate.com/worldclock/fixedtime.html?month=2&day=7&year=2007&hour=17&min=00&sec=0&p1=0) |
| Primary International Dial-in: | **+44 (0)1452 567588** |
| USA Freephone Dial-In: | +1 (866) 6161738 |
| UK National Dial-In: | 08712460713 |
| Passcode: | **0587322148 #** |

Contents
--------

*   [1 Invited Attendees](#Invited-Attendees)
*   [2 Actual Attendees](#Actual-Attendees)
*   [3 Agenda](#Agenda)
    *   [3.1 Recent Download Statistics](#Recent-Download-Statistics)
    *   [3.2 Update on RSE Status](#Update-on-RSE-Status)
    *   [3.3 Community Feedback and Status](#Community-Feedback-and-Status)
    *   [3.4 Technology sub-groups](#Technology-sub-groups)
*   [4 Action Items to Review](#Action-Items-to-Review)
*   [5 New Action Items](#New-Action-Items)
*   [6 Next Meeting](#Next-Meeting)

Invited Attendees
-----------------

This meeting is free for everyone to attend. We specially encourage those people to attend who are actively working on, or have shown interest in TM before:

*   Wind River - Martin Oberhuber, Ted Williams, Doug Gaff, Michael Scharf, Uwe Stieber
*   IBM - Dave McKnight, Dave Dykstal, Kushal Munir
*   LANL / PTP Project - Greg Watson
*   QNX - Doug Schaefer
*   Symbian - Javier Montalvo
*   ARM - Anthony Berent
*   TI - Dobrin Alexey
*   Motorola - Christian Kurzke, Maureen Brenner, Ruth Soliani
*   Accelerated Technology - Aaron Spear, Mark Bozeman
*   Freescale - Kirk Beitz
*   Montavista - Joe Green
*   Palm Source - Ewa Matejska

Actual Attendees
----------------

*   Wind River - Martin Oberhuber, Michael Scharf
*   IBM - Dave McKnight, Dave Dykstal, Kushal Munir
*   Symbian - Javier Montalvo
*   Motorola - Maureen Brenner, Ruth Soliani

Agenda
------

### Recent Download Statistics

RSE 1.0.1 Download statistics as per 7-Feb-2007
| Component | RC3 | RC4 | 1.0 | 1.0.1 | 2.0M4 | Note |
| --- | --- | --- | --- | --- | --- | --- |
| Date | 30-Oct | 03-Nov | 12-Nov | 15-Dec | 4-Jan |  |
| RSE-SDK | 113 | 146 | 491 | 607 | 86 |  |
| rse-runtime-core |  | 14 | 121 | 94 | 9 |  |
| rseserver-windows | 24 | 63 | 192 | 105 | 16 |  |
| rseserver-linux | 19 | 25 | 139 | 93 | 19 |  |
| rse.core (Update Site) | 64 | 52 | 172 | 524 | 3 | 1.0 src is 156 |
| Total | 177 | 212 | 784 | 1225 | 98 |  |
| examples |  | 27 | 85 | 86 + 301 | 15 |  |
| remotecdt |  | 7 | 67 | 103 + 159 | 22 | per 1.0.1, remotecdt is no longer in SDK |
| discovery |  | 13 | 68 | 62 + 223 | 14 |  |
| efs |  | 12 | 42 | 64 + 262 | 17 |  |
| terminal |  | - | - | 113 + 205 | 26 |  |

*   For previous stats and analysis, see [16-Jan-2007](./DSDP/TM/Committer_Phone_Meeting_16-Jan-2007 "DSDP/TM/Committer Phone Meeting 16-Jan-2007"), [19-Dec-2006](./DSDP/TM/Committer_Phone_Meeting_19-Dec-2006 "DSDP/TM/Committer Phone Meeting 19-Dec-2006") and [8-Nov-2006](./DSDP/TM/Phone_Meeting_8-Nov-2006 "DSDP/TM/Phone Meeting 8-Nov-2006")
*   85 examples -- people do want to code against RSE APIs
*   68 discovery -- some interest
*   update site gaining significance with 1.0.1, especially for examples, discovery, efs, terminal

### Update on RSE Status

*   **2.0 Planning**
    *   [Project plan](https://www.eclipse.org/dsdp/tm/development/tm_project_plan_2_0.html) posted
    *   Upcoming refactorings - making stuff internal; extension points to disappear. If you're working against RSE APIs, be sure to watch the dsdp-tm-dev list, you'll be informed about API changes so you can veto them.
*   **EclipseCon**
    *   TM Short Tutorial: [(3651) Building Tools on the Target Management RSE Framework](http://www.eclipsecon.org/2007/index.php?page=sub/&id=3651)
    *   TM Short Talk: [Target Management: Embedded to Enterprise](http://www.eclipsecon.org/2007/index.php?not_accepted=0&page=sub/&id=3781&conference=2007)
    *   DSDP and TM BoF: [DSDP TM, DD and TmL BoF](http://www.eclipsecon.org/2007/index.php?not_accepted=0&page=sub/&id=4201&conference=2007)
    *   There's a 10% discount possibility for people who've never been at EclipseCon before and don't get any other EclipseCon discount (like committer, or member company). If you want that 10% discount, send an E-mail to dsdp-tm-dev
*   **Collaborations** with other projects (Platform/Team, PTP, CDT, TPTP, WTP, ECF, Aperi, g-Eclipse)
    *   jsch to be upgraded and moved to Orbit
    *   Symbolic Links added to Platform EFS
    *   RXTX.org to host Eclipse bundles for serial line access (discussions ongoing)

### Community Feedback and Status

Community's most wanted - who's working on what?

*   Nothing right now, no questions.

### Technology sub-groups

*   CDT Launching (Ewa) - CDT "internal" access: going to discuss on cdt-dev list
*   Update on [Autodetect](./DSDP/TM/Autodetect "DSDP/TM/Autodetect") (Javier)

Action Items to Review
----------------------

*   Last meeting: [DSDP/TM/Phone Meeting 10-Jan-2007](./DSDP/TM/Phone_Meeting_10-Jan-2007 "DSDP/TM/Phone Meeting 10-Jan-2007")
*   \[done\] Everybody - Review and edit the [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") page
*   Maureen to try RSE, review docs, and get in contact with the dsdp-tm-dev list Martin
    *   Maureen tried RSE, made progress, docs are ok, but had to stop because it's no priority for the project now
    *   Q: How to transfer files to a device? A: join the TM tutorial at EclipseCon, or look at the slides which are already posted.
*   \[done\] Martin to inquire IP Review about MV submission - done, will commit processes.shell.linux next days
*   \[done\] Martin to add a project set for the terminal

New Action Items
----------------

*   No new action items right now.

Next Meeting
------------

*   4 weeks: [March 6, 2007 at 20.45 PST](http://www.timeanddate.com/worldclock/personal.html?month=3&day=6&year=2007&hour=20&min=45&sec=0&p1=221) at the [DSDP BoF at EclipseCon](http://www.eclipsecon.org/2007/index.php?page=sub/&id=4201) instead of a Phone Meeting
*   Next [DSDP/TM/Phone Meeting 4-Apr-2007](./DSDP/TM/Phone_Meeting_4-Apr-2007 "DSDP/TM/Phone Meeting 4-Apr-2007") (4 weeks after)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_7-Feb-2007](https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_7-Feb-2007))