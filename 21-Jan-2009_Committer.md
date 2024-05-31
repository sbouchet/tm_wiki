

DSDP/TM/Meetings/21-Jan-2009 Committer
======================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")‎ | [Meetings](./DSDP/TM/Meetings "DSDP/TM/Meetings")

| Meeting Title: | **TM Committer Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Jan 21, 2009](./index.php?title=Jan_21,_2009&action=edit&redlink=1 "Jan 21, 2009 (page does not exist)") at [1700 UTC / 12pm Toronto](http://www.timeanddate.com/worldclock/fixedtime.html?month=1&day=21&year=2009&hour=17&min=00&sec=0&p1=0)   ![Html.gif](./images/Html.gif)[HTML](http://www.google.com/calendar/embed?src=vn70im36r00qeusu8nme50cils@group.calendar.google.com&ctz=Canada/Toronto) \| ![Ical.gif](./images/Ical.gif)[iCal](http://www.google.com/calendar/ical/vn70im36r00qeusu8nme50cils@group.calendar.google.com/public/basic.ics) |
| Dial-in: | Martin to call everybody by Skype   Interested Parties ping **martin.oberhuber** on Skype Chat for getting added to the call. |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kevin.j.doyle, xuan.chen886, eugenetarassov, michael\_scharf, uwe.stieber, radoslav.gerganov, wrsfburton, anna_dushistova.  

  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
    *   [2.1 Last Meetings](#Last-Meetings)
    *   [2.2 Update on RSE Status](#Update-on-RSE-Status)
        *   [2.2.1 TM 3.0.3 status](#TM-3.0.3-status)
        *   [2.2.2 TM 3.1 status](#TM-3.1-status)
        *   [2.2.3 Individual Status](#Individual-Status)
        *   [2.2.4 Other Stuff](#Other-Stuff)
*   [3 Vacations](#Vacations)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   Committers:
    *   IBM - Xuan Chen, Kevin Doyle, Dave Dykstal, Dave McKnight
    *   Wind River - Martin Oberhuber, Michael Scharf
    *   MontaVista - Anna Dushistova

Agenda
------

### Last Meetings

*   Last [DSDP/TM/Phone Meeting 7-Jan-2009](./DSDP/TM/Phone_Meeting_7-Jan-2009 "DSDP/TM/Phone Meeting 7-Jan-2009")
*   Last [DSDP/TM/Committer Phone Meeting 17-Dec-2008](./DSDP/TM/Committer_Phone_Meeting_17-Dec-2008 "DSDP/TM/Committer Phone Meeting 17-Dec-2008")

### Update on RSE Status

#### TM 3.0.3 status

*   Builds ongoing; final 3.0.3 is due on Wednesday Feb 18 (RC1: Feb 4, RC2: Feb 11)
    *   **AI Martin** contribute update site for [Ganymede](./Ganymede "Ganymede")

#### TM 3.1 status

*   **Big Rocks** see [DSDP/TM/Committer Phone Meeting 17-Dec-2008](./DSDP/TM/Committer_Phone_Meeting_17-Dec-2008 "DSDP/TM/Committer Phone Meeting 17-Dec-2008")
*   [3.1M4 Assigned Open bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&product=Target+Management&target_milestone=3.0&target_milestone=3.0.1&target_milestone=3.0.2&target_milestone=3.1+M2&target_milestone=3.1+M3&target_milestone=3.1+M4&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) \- **AI Everyone** reassign target milestone as appropriate
*   [3.1M5 Assigned Open bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&product=Target+Management&target_milestone=3.1+M5&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) \- [Galileo](./Galileo "Galileo") M5 is on Friday Feb 6
    *   This will likely go on the Eclipsecon stick: Want a one-day test pass? - Last checkins on Friday Jan 30
    *   **AI Martin** to create I-build on the weekend after the 30th, announce a 1-day testpass on Tuesday by E-Mail
*   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit) open bugs, [High Priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor) open bugs, [DSDP/TM/3.0 Known Issues and Workarounds](./DSDP/TM/3.0_Known_Issues_and_Workarounds "DSDP/TM/3.0 Known Issues and Workarounds")
*   Many patches on bugzilla, feel free to commit to 3.1 stream... avoid too many patches
    *   Community contributions: 47 [Open bugs with patches](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1) right now, should apply before patches get outdated (see also the [Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for a query)
*   Xuan: Creating p2 repositories as build output - Martin: should work.

#### Individual Status

*   **Anna**: RemoteCDT feature addition - martin updated minor version; [bug 261478](https://bugs.eclipse.org/bugs/show_bug.cgi?id=261478) deprecate or remove SshHostShell, SshShellService etc? It's internal so we should remove...
    *   DaveM: SSHShellServiceSubSystem would remain... only underlying Service would be removed.
    *   **AI DaveM**: Try out switching "DStore Shell" service into "SSH Shell" service and back.
    *   Wait for Dave's results before removing the stuff
    *   Martin: Move RemoteCDT integration into the CDT project? Questions:
        *   Keep namespace or change it?
        *   Find a CDT person to commit to accepting patches (Chris Recoskie?)
        *   Probably move TM/RSE to the Platform+1 Train Slot
        *   DaveM: The IBM "Java Launch" Config might eventually go open source... then, the C and Java Launches might want to share some commonality... Martin: Commonality to go into rse.core or rse.ui as API? Perhaps have some "Remote Launch API" in rse.ui for the common tabs?
            *   Anna much in favor of this... want some "remote launch" API anyways, Montavista is currently duplicating a lot of this...
            *   Connection Selection Page is generic... upload tab may be generic...
            *   Remote Source Lookup in the future
            *   **AI DaveM** to think about it a bit more
        *   Is it too late to push IBM internal functionality into Open Source? - Martin: Need to have at least a dummy CQ filed by Jan.31
*   **DaveM**: 60% openRSE, request for comment: [bug 245260](https://bugs.eclipse.org/bugs/show_bug.cgi?id=245260), [bug 260777](https://bugs.eclipse.org/bugs/show_bug.cgi?id=260777) \- **AI Martin** give feedback
*   **DaveD**: Webpage update: should do along with trying the new [Nova topic](http://dev.eclipse.org/mhonarc/lists/eclipse.org-committers/msg00725.html), focus on the homepage for now
    *   Beginning to look at some big rock defects (probably little ones before m5)
*   **Kevin**: Remote Search improvements
*   **Xuan**: Start looking at junit failure, got a "class not load" exception - Kevin got it working
*   **Michael**: programmatically create Terminal API
*   **Martin**: Updated infocenter; SOC Synchronize Contribution; RXTX this week; RSE-build/releng next week, big rock bugs after: [bug 227750](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227750) IRSEInteractionProvider, [bug 239230](https://bugs.eclipse.org/bugs/show_bug.cgi?id=239230) Early startup
*   **Rado**: WinCE, [bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176) \- Deferred drag&drop SWT

#### Other Stuff

*   **Martin** \- [bug 261486](https://bugs.eclipse.org/bugs/show_bug.cgi?id=261486) @noextend for interfaces - compiler warnings in general
    *   Copyright Year Changes
*   [bug 238574](https://bugs.eclipse.org/bugs/show_bug.cgi?id=238574) Website Revamp - image from the Community is good, need some time to revamp the contents - **AI DaveD** next week
    *   Improve homepage at least, use the Community photoshopped screenshot; PDT, Mylyn are nice

  

Vacations
---------

*   Martin vacation 7-Feb till 14-Feb
*   19.Feb - US President's day? -- Martin out of office,
*   DaveD vacation 16-Feb till 20-Feb
*   Anna vacation 1 week in Feb after m5

Action Items
------------

*   Last meeting: [DSDP/TM/Phone Meeting 7-Jan-2009](./DSDP/TM/Phone_Meeting_7-Jan-2009 "DSDP/TM/Phone Meeting 7-Jan-2009")
*   Last [DSDP/TM/Committer Phone Meeting 17-Dec-2008](./DSDP/TM/Committer_Phone_Meeting_17-Dec-2008 "DSDP/TM/Committer Phone Meeting 17-Dec-2008")
*   **Everyone** reassign target milestone for m4 assigned open bugs; **old** "big rock" bugs for 3.1 and increase priority / set target milestone (may decrease priority on others).
*   **Martin** Comment on DaveM's bugs; Contribute 3.0.3 update site for Ganymede; Draft E-Mail for 1-day m5 test pass; **old** review [bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176) Rado's deferred D&D; new Builder **until 3.1M5**; [bug 227750](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227750) Display in non-UI write fix **until 3.1M4**; Run performance tests for [bug 236065](https://bugs.eclipse.org/bugs/show_bug.cgi?id=236065) IFileService improvements; Critical EFS bugs;
*   **Xuan**: **old** Look at [bug 230917](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230917) Archive Handler Unittests
*   **DaveD**: [bug 238574](https://bugs.eclipse.org/bugs/show_bug.cgi?id=238574) Website revamp; **old** get rid of 3.0 assigned open bugs;
*   **DaveM**: Think about remotecdt move; test [bug 261478](https://bugs.eclipse.org/bugs/show_bug.cgi?id=261478) SSH services change; **old** [bug 199596](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199596) Read-Only attribute doesn't always update IRemoteFile;

Next Meeting
------------

*   Next [DSDP/TM/Meetings/4-Feb-2009](./DSDP/TM/Meetings/4-Feb-2009 "DSDP/TM/Meetings/4-Feb-2009") (2 weeks after)
*   Next [DSDP/TM/Committer Phone Meeting 18-Feb-2009](./index.php?title=DSDP/TM/Committer_Phone_Meeting_18-Feb-2009&action=edit&redlink=1 "DSDP/TM/Committer Phone Meeting 18-Feb-2009 (page does not exist)") (4 weeks after)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Meetings/21-Jan-2009_Committer](https://wiki.eclipse.org//DSDP/TM/Meetings/21-Jan-2009_Committer))