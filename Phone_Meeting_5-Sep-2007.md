

DSDP/TM/Phone Meeting 5-Sep-2007
================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Wednesday Sep 5, 2007 at [1600 UTC / 9am PST](http://www.timeanddate.com/worldclock/fixedtime.html?month=9&day=5&year=2007&hour=16&min=00&sec=0&p1=0) |
| Primary International Dial-in: | **+44 (0)1452 567588** |
| USA Freephone Dial-In: | +1 (866) 6161738 |
| UK National Dial-In: | 08712460713 |
| Passcode: | **0587322148 #** |

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 Update on RSE Status](#Update-on-RSE-Status)
    *   [2.2 TM Project Meeting / Coding Camp](#TM-Project-Meeting-.2F-Coding-Camp)
    *   [2.3 Community Feedback and Status](#Community-Feedback-and-Status)
*   [3 Action Items to Review](#Action-Items-to-Review)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave Dykstal, Dave McKnight
*   Motorola - Maureen Brenner, Fabio Fantato
*   Wind River - Martin Oberhuber
*   Symbian - Javier Montalvo

Notes
-----

### Update on RSE Status

*   **Project Plan Status** \- ideas on Future Planning, to be finalized at the F2F meeting
    *   Q from Mauren: Project structure that TM uses - currently a single project, storing info about each subsystem in a project
    *   Martin: Persistence with TM 2.0 is in the metadata area now by default, persistence providers can be registered to store stuff somewhere else. For the future, we are looking at export/import to XML files or projects - single-project-profiles are legacy only.
    *   Problem with persistence tied to a project, is that CM system can modify / update connections (even while connections are live). But the use-case is more a single-time import of connection info, then the user wants to have control over his connection, so we've been more moving toward an explicit import scenario, and after that the user would have full control over his connections.
    *   Mauren: Connection tied to an emulator, also contains a state file for the virtual machine; that would be different for each user, not meant to be team-shared; will analyze whether Metadata is an alternative
*   **Codebase status** \- working on TM 2.0.1 in HEAD stream
*   **Future Planning** \- see [TM Future Planning](./TM_Future_Planning "TM Future Planning")
*   **Windriver Target Communication Framework** \- moving forward

### TM Project Meeting / Coding Camp

*   See [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./DSDP/TM/Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007"). Our coding camp will be aimed for developers and committers to discuss architectural ideas and try them out right on the code. There will be limited time (perhaps 2 hours) for manager-like presentations if the community is interested. Everybody is invited to join the coding camp, preferredly bringing code to integrate with RSE or concrete ideas to discuss for the future.

### Community Feedback and Status

*   TmL / Motorola Status: Started integrating code with TM/RSE - no news, currently working on internal requirements

Action Items to Review
----------------------

*   Last meeting: [DSDP/TM/Phone Meeting 1-Aug-2007](./DSDP/TM/Phone_Meeting_1-Aug-2007 "DSDP/TM/Phone Meeting 1-Aug-2007")

Next Meeting
------------

*   Next [DSDP/TM/Phone Meeting 3-Oct-2007](./DSDP/TM/Phone_Meeting_3-Oct-2007 "DSDP/TM/Phone Meeting 3-Oct-2007") (4 weeks after)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_5-Sep-2007](https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_5-Sep-2007))