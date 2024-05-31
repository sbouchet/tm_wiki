

DSDP/TM/Phone Meeting 5-Nov-2008
================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Wednesday [Nov 5, 2008](./index.php?title=Nov_5,_2008&action=edit&redlink=1 "Nov 5, 2008 (page does not exist)") at [1700 UTC / 9am PST](http://www.timeanddate.com/worldclock/fixedtime.html?month=11&day=5&year=2008&hour=17&min=00&sec=0&p1=0)   ![Html.gif](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/Html.gif)[HTML](http://www.google.com/calendar/embed?src=vn70im36r00qeusu8nme50cils@group.calendar.google.com&ctz=Canada/Toronto) \| ![Ical.gif](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/Ical.gif)[iCal](http://www.google.com/calendar/ical/vn70im36r00qeusu8nme50cils@group.calendar.google.com/public/basic.ics) |
| Primary International Dial-in: | **+44 (0)1452 567588** |
| USA Freephone Dial-In: | +1 (866) 6161738 |
| UK National Dial-In: | 08712460713 |
| Passcode: | **0587322148 #** |

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 Update on RSE Status](#Update-on-RSE-Status)
        *   [2.1.1 TM 3.1](#TM-3.1)
        *   [2.1.2 TM 3.0.2](#TM-3.0.2)
        *   [2.1.3 Other Stuff](#Other-Stuff)
        *   [2.1.4 Individual Status](#Individual-Status)
    *   [2.2 Community Feedback and Status](#Community-Feedback-and-Status)
*   [3 Vacations](#Vacations)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   Wind River - Martin Oberhuber
*   IBM - Kevin Doyle, Dave McKnight, Xuan Chen, Dave Dykstal
*   MontaVista - Anna Dushistova

Notes
-----

*   Last [DSDP/TM/Phone Meeting 1-Oct-2008](./DSDP/TM/Phone_Meeting_1-Oct-2008 "DSDP/TM/Phone Meeting 1-Oct-2008")
*   Last [DSDP/TM/Committer Phone Meeting 15-Oct-2008](./DSDP/TM/Committer_Phone_Meeting_15-Oct-2008 "DSDP/TM/Committer Phone Meeting 15-Oct-2008")

### Update on RSE Status

*   Switching to Skype for monthly calls - **AI Martin update the Wiki**

#### TM 3.1

*   M3 is next week - no testing, just create a N&N
*   [TM 3.1 plan](https://www.eclipse.org/projects/project-plan.php?projectid=dsdp.tm), along with a [DSDP/TM/3.1 Ramp down Plan](./DSDP/TM/3.1_Ramp_down_Plan "DSDP/TM/3.1 Ramp down Plan")
    *   Remove EFS from the project plan ... **ok for everyone**
    *   [bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176) \- Deferred drag&drop SWT bug - need to find out how to report progress for the background file transfer, Rado?
*   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit) open bugs, [High Priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor) open bugs, [DSDP/TM/3.0 Known Issues and Workarounds](./DSDP/TM/3.0_Known_Issues_and_Workarounds "DSDP/TM/3.0 Known Issues and Workarounds")
*   [Galileo Simultaneous Release#Requirements For Participation](./Galileo_Simultaneous_Release#Requirements_For_Participation "Galileo Simultaneous Release"): Participate in Babel (done)
    *   Get rid of Platform "internal" usage - IBM Product work hopefully winding down next month, schedule some time in Dec/Jan
    *   Build process maturity: repeatable, scriptable, usable by others
    *   Basic Capability / Activity definitions
*   Many patches on bugzilla, feel free to commit to 3.1 stream... avoid too many patches

#### TM 3.0.2

*   Need a fixed date for 3.0.2 -- mid december? - **AI DaveM** follow up with product team to get exact date
*   Need to release into the Mapfile for M-builds to pick up fixes
*   Testing: give 3 weeks for product teams to test, no official open source testing

#### Other Stuff

*   [bug 238574](https://bugs.eclipse.org/bugs/show_bug.cgi?id=238574) Website Revamp? We have a bugzilla "Website" component now... still no volunteers
*   **Target Communication Framework** \- [DSDP/TM/TCF FAQ](./DSDP/TM/TCF_FAQ "DSDP/TM/TCF FAQ") available and plan theme, shooting for 1.0 under discussion.
*   Bugs [still assigned to 3.0](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&target_milestone=3.0+M5&target_milestone=3.0+M6&target_milestone=3.0+M7&target_milestone=3.0+RC1&target_milestone=3.0+RC2&target_milestone=3.0+RC3&target_milestone=3.0+RC4&target_milestone=3.0+RC5&target_milestone=3.0&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) \-\- Xuan, DaveD!
*   Abbot pretty much dead -- looking at SWTBot now
*   Unittests, Findbugs?

#### Individual Status

*   Martin - mostly switching to Platform/Core, E4 and EAC and RXTX work. For TM doing bug reviews, releng, and few selected fixes as interesting for WR.
*   DaveD - will look at M3 assigned bugs, product work winding down
*   DaveM - continuing 60% fixes on open RSE
*   Kevin - catching up on backport reviews, fair amount on open RSE
*   Xuan - mostly product work but winding down, helping Kevin on reviews, start looking on own bugs
*   Anna - mostly on generic Terminal / Telnet, but without automatic service creation via adapter (Telnet and SSH only for now)

### Community Feedback and Status

*   Community contributions
    *   Patrick Juhl - SSH Tunnel - no news. In JSch Session.setPortForwardingL() there seems to be an incompatibility between Eclipse 3.3 and 3.4 (according to JSch mailing list). SSH Tunnel being used by [Collabnet Cubit](http://desktop-eclipse.open.collab.net/source/browse/desktop-eclipse/trunk/plugins/com.collabnet.cubit/)
    *   [bug 196337](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196337) \- TM Local Terminal Connector - waiting on fix for CDT Spawner
    *   Freescale contributions to be reviewed - [bug 247876](https://bugs.eclipse.org/bugs/show_bug.cgi?id=247876) apply host to project; [bug 247878](https://bugs.eclipse.org/bugs/show_bug.cgi?id=247878) systemHostCombo with subsystems; [bug 247879](https://bugs.eclipse.org/bugs/show_bug.cgi?id=247879) project cache for RSE host settings
    *   [bug 236205](https://bugs.eclipse.org/bugs/show_bug.cgi?id=236205) Generic Display subsystem (as a host for vnc etc)

Vacations
---------

*   Vacations, away times
    *   Anna Nov 8 - 15;
    *   Anna, Martin on ESE Nov 17-20
    *   DaveDMartin last week of dec and 1st week of Jan
*   Questions

Action Items
------------

*   Last meeting: [DSDP/TM/Phone Meeting 1-Oct-2008](./DSDP/TM/Phone_Meeting_1-Oct-2008 "DSDP/TM/Phone Meeting 1-Oct-2008")
*   Last [DSDP/TM/Committer Phone Meeting 15-Oct-2008](./DSDP/TM/Committer_Phone_Meeting_15-Oct-2008 "DSDP/TM/Committer Phone Meeting 15-Oct-2008")
*   **Martin** **old** review [bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176) Rado's deferred D&D
*   Martin - modify Wiki template for using Skype on monthly calls; contact Rado; remove EFS from project plan; N&N for TM 3.1M3, link into Portal?
*   Xuan, DaveD - get rid of 3.0 assigned open bugs
*   DaveM - come up with 3.0.2 release date

Next Meeting
------------

*   Next [DSDP/TM/Committer Phone Meeting 19-Nov-2008](./DSDP/TM/Committer_Phone_Meeting_19-Nov-2008 "DSDP/TM/Committer Phone Meeting 19-Nov-2008") (2 weeks after)
*   Next [DSDP/TM/Phone Meeting 3-Dec-2008](./DSDP/TM/Phone_Meeting_3-Dec-2008 "DSDP/TM/Phone Meeting 3-Dec-2008") (4 weeks after)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_5-Nov-2008](https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_5-Nov-2008))