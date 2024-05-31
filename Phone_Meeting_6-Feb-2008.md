

DSDP/TM/Phone Meeting 6-Feb-2008
================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Wednesday Feb 6, 2008 at [1600 UTC / 9am PST](http://www.timeanddate.com/worldclock/fixedtime.html?month=2&day=6&year=2008&hour=16&min=00&sec=0&p1=0) |
| Primary International Dial-in: | **+44 (0)1452 567588** |
| USA Freephone Dial-In: | +1 (866) 6161738 |
| UK National Dial-In: | 08712460713 |
| Passcode: | **0587322148 #** |

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 Update on RSE Status](#Update-on-RSE-Status)
    *   [2.2 User Actions](#User-Actions)
    *   [2.3 Community Feedback and Status](#Community-Feedback-and-Status)
*   [3 Action Items to Review](#Action-Items-to-Review)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   Wind River - Martin Oberhuber
*   IBM - Dave Dykstal, Dave McKnight, Xuan Chen
*   Symbian - Javier Montalvo Orus

Notes
-----

### Update on RSE Status

*   **Target Communication Framework** \- [DSDP/TM/TCF FAQ](./TCF_FAQ "DSDP/TM/TCF FAQ") available and approved by EMO. Now working on SVN Repository at Eclipse.org
*   **Project Plan Status** \- still on the [TM Future Planning](./TM_Future_Planning "TM Future Planning") page only
    *   Bugzilla plan items as well as an "official" project plan will be done
    *   Focus on TCF; RSE bug-fixes and quality; UI/Non-UI splitting; Import/Export of Profiles
*   **Codebase status** \- API changes for TM 3.0 in HEAD stream - See recent 3.0M4 build notes
    *   Collecting requested backport changes for TM 2.0.3
    *   Latest information about API changes are in the build notes of recent I-builds (weekly every Thursday)
    *   Working on improved release engineering scripts, especially for running unit tests nightly
*   **EclipseCon**
    *   Accepted TM Tutorial (with focus on TCF), and a Short Talk (TM Ganymede News).
    *   RSE also referenced in some other talks

### User Actions

*   Xuan: Discussed how the rse useractions can go into Open Source

*   **Subsystem Families** ([bug 217894](https://bugs.eclipse.org/bugs/show_bug.cgi?id=217894):
    *   Want to contribute user actions to subsystem families
    *   Martin would tie "family" to the connectorservice. Then it's orthogonal to the subsystem category. Add a "connectorserviceid" to SubsytemConfiguration plugin.xml
    *   SystemType is also some kind of grouping. What's the definition of a Family compared to SystemType?
        *   Martin had the idea of making systemType more flexible with Properties, or "derived" systemType - [bug 170918](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170918)

### Community Feedback and Status

*   Community's most wanted
    *   PHP / PDT people hot on EFS fixes and improvements
*   Community contributions
    *   Francesco Crivelli - Terminal integration with RSE - no code received yet, currently not available
    *   Patrick Juhl - SSH Tunnel - no more news
    *   [bug 214887](https://bugs.eclipse.org/bugs/show_bug.cgi?id=214887) Windows CE - interesting contribution
    *   RSE being used by the Community, but no contributions for BugDay
*   Questions

Action Items to Review
----------------------

*   Last meeting: [DSDP/TM/Phone Meeting 9-Jan-2008](./Phone_Meeting_9-Jan-2008 "DSDP/TM/Phone Meeting 9-Jan-2008")

Next Meeting
------------

*   Next [DSDP/TM/Phone Meeting 5-Mar-2008](./Phone_Meeting_5-Mar-2008 "DSDP/TM/Phone Meeting 5-Mar-2008") (4 weeks after)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_6-Feb-2008](https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_6-Feb-2008))