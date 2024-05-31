

DSDP/TM/Phone Meeting 9-Jan-2008
================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Wednesday [Jan 9, 2008](./index.php?title=Jan_9,_2008&action=edit&redlink=1 "Jan 9, 2008 (page does not exist)") at [1600 UTC / 9am PST](http://www.timeanddate.com/worldclock/fixedtime.html?month=1&day=9&year=2008&hour=16&min=00&sec=0&p1=0) |
| Primary International Dial-in: | **+44 (0)1452 567588** |
| USA Freephone Dial-In: | +1 (866) 6161738 |
| UK National Dial-In: | 08712460713 |
| Passcode: | **0587322148 #** |

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 Update on RSE Status](#Update-on-RSE-Status)
    *   [2.2 Committer Discussions](#Committer-Discussions)
    *   [2.3 Community Feedback and Status](#Community-Feedback-and-Status)
    *   [2.4 Technology sub-groups](#Technology-sub-groups)
*   [3 Action Items to Review](#Action-Items-to-Review)
*   [4 New Action Items](#New-Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   Wind River - Martin Oberhuber
*   IBM - Dave Dykstal, Dave McKnight

Notes
-----

### Update on RSE Status

*   **Target Communication Framework** \- [DSDP/TM/TCF FAQ](./DSDP/TM/TCF_FAQ "DSDP/TM/TCF FAQ") available and approved by EMO. Now working on SVN Repository at Eclipse.org
*   **Project Plan Status** \- still on the [TM Future Planning](./TM_Future_Planning "TM Future Planning") page only
*   **Codebase status** \- API changes for TM 3.0 in HEAD stream - See recent 3.0M4 build notes; nothing yet form TM 2.0.3
    *   Latest information about API changes are in the build notes of recent I-builds (weekly every Thursday)
    *   Working on improved release engineering scripts, especially for running unit tests nightly
*   **EclipseCon**
    *   Accepted TM Tutorial (with focus on TCF), and a Short Talk (TM Ganymede News).
    *   RSE also referenced in some other talks

### Committer Discussions

*   DaveM: IBM needs UI for changing ownership and permission bits on remote files
    *   Want a common UI for Dstore, FTP, SSH.
    *   Martin: Remote file systems are different... implement it in the specific subsystem(s) only?
    *   DaveD: Use an Adaptor pattern on the Service? - Would be very flexible since 3rd parties can register an additional Adaptor even for an existing Service
*   DaveM: What about a "DStore-only" connection type?
*   Filter Pools: problems in wizard, might be created against default subsystem instead of the selected one -- DaveD to look into deferring filter creation; Martin: Wizard UI improvement bug (select services first)
*   Remove Kushal and Ted as committers? - Ask Ted and Kushal directly
*   TCF vs ECF - clarified through conf.call -- Scott Lewis wants integration - will work on.

### Community Feedback and Status

*   Community's most wanted
    *   PHP / PDT people hot on EFS fixes and improvements
*   Community contributions
    *   Francesco Crivelli - working on Terminal integration with RSE - To be contributed by end of January
    *   Proposed contribution from Patrick Juhl for SSH Tunnel integration with RSE
    *   RSE being used by the Community, but no contributions for BugDay
*   Questions

### Technology sub-groups

Action Items to Review
----------------------

*   Last meeting: [DSDP/TM/Phone Meeting 5-Dec-2007](./DSDP/TM/Phone_Meeting_5-Dec-2007 "DSDP/TM/Phone Meeting 5-Dec-2007")

New Action Items
----------------

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 23-Jan-2008](./DSDP/TM/Committer_Phone_Meeting_23-Jan-2008 "DSDP/TM/Committer Phone Meeting 23-Jan-2008") at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=1&day=23&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Next [DSDP/TM/Phone Meeting 6-Feb-2008](./DSDP/TM/Phone_Meeting_6-Feb-2008 "DSDP/TM/Phone Meeting 6-Feb-2008") (4 weeks after)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_9-Jan-2008](https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_9-Jan-2008))