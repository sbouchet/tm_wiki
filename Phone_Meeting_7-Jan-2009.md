

DSDP/TM/Phone Meeting 7-Jan-2009
================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Jan 7, 2009](/index.php?title=Jan_7,_2009&action=edit&redlink=1 "Jan 7, 2009 (page does not exist)") at [1700 UTC / 12pm Toronto](http://www.timeanddate.com/worldclock/fixedtime.html?month=1&day=7&year=2009&hour=17&min=00&sec=0&p1=0)   ![Html.gif](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/Html.gif)[HTML](http://www.google.com/calendar/embed?src=vn70im36r00qeusu8nme50cils@group.calendar.google.com&ctz=Canada/Toronto) \| ![Ical.gif](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/Ical.gif)[iCal](http://www.google.com/calendar/ical/vn70im36r00qeusu8nme50cils@group.calendar.google.com/public/basic.ics) |
| Dial-in: | Martin to call everybody by Skype   Interested Parties ping **martin.oberhuber** on Skype Chat for getting added to the call. |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kevin.j.doyle, xuan.chen886, eugenetarassov, michael\_scharf, uwe.stieber, radoslav.gerganov, wrsfburton, anna_dushistova.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
    *   [2.1 Last Meetings](#Last-Meetings)
    *   [2.2 Update on RSE Status](#Update-on-RSE-Status)
        *   [2.2.1 TM 3.1 status](#TM-3.1-status)
        *   [2.2.2 Individual Status](#Individual-Status)
        *   [2.2.3 Other Stuff](#Other-Stuff)
*   [3 Vacations](#Vacations)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

This meeting is free for everyone to attend. It's a service of the TM developers and committers to community, fostering exchange of upcoming news, status and asking questions. Committers are expected to attend.

*   IBM - Xuan Chen, Kevin Doyle, Dave Dykstal, Dave McKnight
*   Wind River - Martin Oberhuber

Agenda
------

### Last Meetings

*   Last [DSDP/TM/Phone Meeting 3-Dec-2008](/DSDP/TM/Phone_Meeting_3-Dec-2008 "DSDP/TM/Phone Meeting 3-Dec-2008")
*   Last [DSDP/TM/Committer Phone Meeting 17-Dec-2008](/DSDP/TM/Committer_Phone_Meeting_17-Dec-2008 "DSDP/TM/Committer Phone Meeting 17-Dec-2008")
*   Skype Call Quality - excellent this time

### Update on RSE Status

#### TM 3.1 status

*   **big rocks** see [DSDP/TM/Committer Phone Meeting 17-Dec-2008](/DSDP/TM/Committer_Phone_Meeting_17-Dec-2008 "DSDP/TM/Committer Phone Meeting 17-Dec-2008")
*   [3.1M4 Assigned Open bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&product=Target+Management&target_milestone=3.0&target_milestone=3.0.1&target_milestone=3.1+M2&target_milestone=3.1+M3&target_milestone=3.1+M4&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) \- **AI Everyone** reassign target milestone as appropriate
*   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit) open bugs, [High Priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor) open bugs, [DSDP/TM/3.0 Known Issues and Workarounds](/DSDP/TM/3.0_Known_Issues_and_Workarounds "DSDP/TM/3.0 Known Issues and Workarounds")
*   Many patches on bugzilla, feel free to commit to 3.1 stream... avoid too many patches
    *   Community contributions: 47 [Open bugs with patches](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1) right now, should apply before patches get outdated (see also the [Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for a query)

#### Individual Status

*   **Anna**: RemoteCDT feature addition
*   **DaveD**:
*   **DaveM**: First 3.0.3 backport - **AI Dave** need to update the enclosing features' versions as well (SDK), **AI Martin** update the site.xml
*   **Kevin**:
*   **Xuan**:
*   **Martin**: RXTX this week; RSE-build/releng next week, big rock bugs after: [bug 227750](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227750) IRSEInteractionProvider, [bug 239230](https://bugs.eclipse.org/bugs/show_bug.cgi?id=239230) Early startup
*   **Rado**: WinCE, [bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176) \- Deferred drag&drop SWT

#### Other Stuff

*   **DaveM** \- API Tooling Warnings:
    *   noimplement warnings - Martin: Use Platform M4, Platform API Tooling behavior was changed
    *   RSESafeTreeViewer extends TreeViewer - Martin: for now, live with the warning, it's lower priority than others
*   [bug 238574](https://bugs.eclipse.org/bugs/show_bug.cgi?id=238574) Website Revamp - image from the Community is good, need some time to revamp the contents - **AI DaveD** next week
    *   Improve homepage at least, use the Community photoshopped screenshot; PDT, Mylyn are nice
*   Need to confirm the supported platforms. - Xuan
    *   DaveD: Just take the table from the [Project Plan](https://www.eclipse.org/projects/project-plan.php?projectid=dsdp.tm#target_environments)
    *   Martin: Contributors can contribute HP-UX support if they agree to do the testing and contribute fixes. Don't need to be committers. We can support them.

Vacations
---------

*   Anna Jan1 - Jan10

Action Items
------------

*   Last meeting: [DSDP/TM/Phone Meeting 3-Dec-2008](/DSDP/TM/Phone_Meeting_3-Dec-2008 "DSDP/TM/Phone Meeting 3-Dec-2008")
*   Last [DSDP/TM/Committer Phone Meeting 17-Dec-2008](/DSDP/TM/Committer_Phone_Meeting_17-Dec-2008 "DSDP/TM/Committer Phone Meeting 17-Dec-2008")
*   **Everyone** "big rock" bugs for 3.1 and increase priority / set target milestone (may decrease priority on others).
*   **Martin** **old** review [bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176) Rado's deferred D&D; new Builder **until 3.1M5**; [bug 227750](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227750) Display in non-UI write fix **until 3.1M4**; Run performance tests for [bug 236065](https://bugs.eclipse.org/bugs/show_bug.cgi?id=236065) IFileService improvements; Critical EFS bugs;
*   **Xuan**: **old** Look at [bug 230917](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230917) Archive Handler Unittests
*   **DaveD** [bug 238574](https://bugs.eclipse.org/bugs/show_bug.cgi?id=238574) Website revamp; **old** get rid of 3.0 assigned open bugs;
*   **DaveM** **old** [bug 199596](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199596) Read-Only attribute doesn't always update IRemoteFile;

Next Meeting
------------

*   Next [DSDP/TM/Meetings/21-Jan-2009 Committer](/DSDP/TM/Meetings/21-Jan-2009_Committer "DSDP/TM/Meetings/21-Jan-2009 Committer") (2 weeks after)
*   Next [DSDP/TM/Meetings/4-Feb-2009](/DSDP/TM/Meetings/4-Feb-2009 "DSDP/TM/Meetings/4-Feb-2009") (4 weeks after)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_7-Jan-2009](https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_7-Jan-2009))