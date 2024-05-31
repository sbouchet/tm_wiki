

DSDP/TM/Meetings/18-Mar-2009 Committer
======================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")‎ | [Meetings](./DSDP/TM/Meetings "DSDP/TM/Meetings")

| Meeting Title: | **TM Monthly Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Mar 18, 2009](./index.php?title=Mar_18,_2009&action=edit&redlink=1 "Mar 18, 2009 (page does not exist)") at [1700 UTC / 12pm Toronto](http://www.timeanddate.com/worldclock/fixedtime.html?month=3&day=18&year=2009&hour=17&min=00&sec=0&p1=0)   ![Html.gif](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/Html.gif)[HTML](http://www.google.com/calendar/embed?src=vn70im36r00qeusu8nme50cils@group.calendar.google.com&ctz=Canada/Toronto) \| ![Ical.gif](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/Ical.gif)[iCal](http://www.google.com/calendar/ical/vn70im36r00qeusu8nme50cils@group.calendar.google.com/public/basic.ics) |
| Dial-in: | Martin to call everybody by Skype   Interested Parties ping **martin.oberhuber** on Skype Chat for getting added to the call. |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kevin.j.doyle, xuan.chen886, eugenetarassov, michael\_scharf, uwe.stieber, radoslav.gerganov, wrsfburton, anna_dushistova.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
    *   [2.1 Last Meetings](#Last-Meetings)
    *   [2.2 EclipseCon](#EclipseCon)
    *   [2.3 TCF](#TCF)
    *   [2.4 Update on RSE Status](#Update-on-RSE-Status)
        *   [2.4.1 TM 3.1 status](#TM-3.1-status)
        *   [2.4.2 Individual Status](#Individual-Status)
*   [3 Vacations](#Vacations)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

This meeting is free for everyone to attend. It's a service of the TM developers and committers to community, fostering exchange of upcoming news, status and asking questions. Committers are expected to attend.

*   Committers:
    *   IBM - Xuan Chen, Dave Dykstal, Dave McKnight
    *   Wind River - Martin Oberhuber
    *   MontaVista - Anna Dushistova

  

Agenda
------

### Last Meetings

*   Last [DSDP/TM/Meetings/4-Mar-2009](./DSDP/TM/Meetings/4-Mar-2009 "DSDP/TM/Meetings/4-Mar-2009")
*   Last [DSDP/TM/Meetings/18-Feb-2009 Committer](./DSDP/TM/Meetings/18-Feb-2009_Committer "DSDP/TM/Meetings/18-Feb-2009 Committer")

### EclipseCon

*   Anna to join CBI tutorial on Monday

### TCF

*   New, separate mailing list [dsdp-tcf-dev@eclipse.org](https://dev.eclipse.org/mailman/listinfo/dsdp-tcf-dev)
*   [Round-table meeting](http://dev.eclipse.org/mhonarc/lists/dsdp-tcf-dev/msg00001.html) likely on Thu Mar 12

### Update on RSE Status

#### TM 3.1 status

*   3.1M6 on Wed 18-Mar-2009, TODAY is API FREEZE!
    *   RemoteCDT move: [bug 263178](https://bugs.eclipse.org/bugs/show_bug.cgi?id=263178) Anna refactoring ran out of time - try to put in but cannot guarantee
        *   CDT will adopt Remotecdt for their M7, we will move out for M7
    *   [bug 261486](https://bugs.eclipse.org/bugs/show_bug.cgi?id=261486) @noextend for interfaces - compiler warnings in general
        *   Leave noextend for now. For future, maybe add a new interface to be extended in order to fix user actions warning
    *   When is the UI Freeze ?
        *   First drop mid April, more changes possible later... due to Galileo / Babel, lets **declare M7 our UI Freeze**.
    *   Flexibility for import/export parts of the model (e.g. User actions)? Preemptively do the UI stuff? - **AI DaveD create bug**, defer decision for now
*   Rado [bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176) \- Deferred drag&drop SWT
*   **Martin** \- who's going to fix the SOC Synchronize contribution?
*   **DaveD** \- Website: some work done, where to place some items? - AI Dave to post current results and ask on Mailing list
*   **Martin** \- [bug 254129](https://bugs.eclipse.org/bugs/show_bug.cgi?id=254129) Capabilities - ![Ok green.gif](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/Ok_green.gif)Martin E-Mail cross-project
    *   [bug 196337](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196337) \- TM Local Terminal Connector - waiting on fix for CDT Spawner

*   **Big Rocks** see [DSDP/TM/Committer Phone Meeting 17-Dec-2008](./DSDP/TM/Committer_Phone_Meeting_17-Dec-2008 "DSDP/TM/Committer Phone Meeting 17-Dec-2008")
*   [3.1M5 Assigned Open bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&product=Target+Management&target_milestone=3.0&target_milestone=3.0.1&target_milestone=3.0.2&target_milestone=3.1+M2&target_milestone=3.1+M3&target_milestone=3.1+M4&target_milestone=3.1+M5&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) \- **AI Everyone** reassign target milestone as appropriate
*   [3.1M6 Assigned Open bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&product=Target+Management&target_milestone=3.1+M6&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) \- [Galileo](./Galileo "Galileo") M6 is on Wed Mar 18 already!
*   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit) open bugs, [High Priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor) open bugs, [DSDP/TM/3.0 Known Issues and Workarounds](./DSDP/TM/3.0_Known_Issues_and_Workarounds "DSDP/TM/3.0 Known Issues and Workarounds")
*   Many patches on bugzilla, feel free to commit to 3.1 stream... avoid too many patches
    *   Community contributions: 42 [Open bugs with patches](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1) right now, should apply before patches get outdated (see also the [Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for a query)

  

#### Individual Status

*   **Anna**: RemoteCDT new API
*   **DaveM**:
*   **DaveD**: noextend, website Webpage update: should do along with trying the new [Nova topic](http://dev.eclipse.org/mhonarc/lists/eclipse.org-committers/msg00725.html), focus on the homepage for now
*   **Kevin**:
*   **Xuan**:
*   **Michael**:
*   **Martin**: RXTX 2.2; RSE-build: CBI tutorial: Anna?, big rock bugs after: [bug 227750](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227750) IRSEInteractionProvider, [bug 239230](https://bugs.eclipse.org/bugs/show_bug.cgi?id=239230) Early startup
*   **Rado**: WinCE, [bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176) \- Deferred drag&drop SWT

  

  

Vacations
---------

*   Martin, Anna Eclipsecon next week;
*   DaveD busy in June, won't be able to handle builds in June; find somebody or have everything ready early
*   Anna travelling Apr 1

Action Items
------------

*   Last [DSDP/TM/Meetings/4-Mar-2009](./DSDP/TM/Meetings/4-Mar-2009 "DSDP/TM/Meetings/4-Mar-2009")
*   **Everyone** Fix target milestone of 3.1m6 assigned bugs.
*   **Martin** **old** review [bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176) Rado's deferred D&D; new Builder; [bug 227750](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227750) Display in non-UI write fix; Run performance tests for [bug 236065](https://bugs.eclipse.org/bugs/show_bug.cgi?id=236065) IFileService improvements; Critical EFS bugs;
*   **Anna**: Remotecdt; CBI tutorial
*   **Xuan**: **old** Look at [bug 230917](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230917) Archive Handler Unittests
*   **DaveD**: Create bug for partial model export; [bug 238574](https://bugs.eclipse.org/bugs/show_bug.cgi?id=238574) Make new website available and E-mail questions on mailinglist
*   **DaveM**: test [bug 261478](https://bugs.eclipse.org/bugs/show_bug.cgi?id=261478) SSH services change; **old** [bug 199596](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199596) Read-Only attribute doesn't always update IRemoteFile;

Next Meeting
------------

*   Next [DSDP/TM/Meetings/1-Apr-2009](./DSDP/TM/Meetings/1-Apr-2009 "DSDP/TM/Meetings/1-Apr-2009") (2 weeks after)
*   Next [DSDP/TM/Meetings/15-Apr-2009 Committer](./DSDP/TM/Meetings/15-Apr-2009_Committer "DSDP/TM/Meetings/15-Apr-2009 Committer") (4 weeks after)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Meetings/18-Mar-2009_Committer](https://wiki.eclipse.org//DSDP/TM/Meetings/18-Mar-2009_Committer))