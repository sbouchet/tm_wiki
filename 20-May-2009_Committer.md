

DSDP/TM/Meetings/20-May-2009 Committer
======================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")‎ | [Meetings](/DSDP/TM/Meetings "DSDP/TM/Meetings")

| Meeting Title: | **TM Committer Meeting** |
| --- | --- |
| Date & Time: | Wednesday [May 20, 2009](/index.php?title=May_20,_2009&action=edit&redlink=1 "May 20, 2009 (page does not exist)") at [1600 UTC / 12pm Toronto](http://www.timeanddate.com/worldclock/fixedtime.html?month=5&day=20&year=2009&hour=16&min=00&sec=0&p1=0)   ![Html.gif](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/Html.gif)[HTML](http://www.google.com/calendar/embed?src=vn70im36r00qeusu8nme50cils@group.calendar.google.com&ctz=Canada/Toronto) \| ![Ical.gif](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/Ical.gif)[iCal](http://www.google.com/calendar/ical/vn70im36r00qeusu8nme50cils@group.calendar.google.com/public/basic.ics) |
| Dial-in: | Martin to call everybody by Skype   Interested Parties ping **martin.oberhuber** on Skype Chat for getting added to the call. |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kevin.j.doyle, xuan.chen886, eugenetarassov, michael\_scharf, uwe.stieber, radoslav.gerganov, wrsfburton, anna_dushistova.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
    *   [2.1 Last Meetings](#Last-Meetings)
    *   [2.2 Status round call](#Status-round-call)
    *   [2.3 TM 3.1 status](#TM-3.1-status)
    *   [2.4 Cleanup Work](#Cleanup-Work)
    *   [2.5 Questions](#Questions)
*   [3 Vacations](#Vacations)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

Agenda
------

### Last Meetings

*   Last [DSDP/TM/Meetings/6-May-2009](/DSDP/TM/Meetings/6-May-2009 "DSDP/TM/Meetings/6-May-2009")
*   Last [DSDP/TM/Meetings/15-Apr-2009 Committer](/DSDP/TM/Meetings/15-Apr-2009_Committer "DSDP/TM/Meetings/15-Apr-2009 Committer")

### Status round call

### TM 3.1 status

*   [3.1M6 Assigned Open bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&product=Target+Management&target_milestone=3.0&target_milestone=3.0.1&target_milestone=3.0.2&target_milestone=3.1+M2&target_milestone=3.1+M3&target_milestone=3.1+M4&target_milestone=3.1+M5&target_milestone=3.1+M6&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) \- **AI Everyone** reassign target milestone as appropriate
*   [3.1M7 Assigned Open bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&product=Target+Management&target_milestone=3.1+M7&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) \- [Galileo](/Galileo "Galileo") M7 is on Tue May 5!
*   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit) open bugs, [High Priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor) open bugs, [DSDP/TM/3.0 Known Issues and Workarounds](/DSDP/TM/3.0_Known_Issues_and_Workarounds "DSDP/TM/3.0 Known Issues and Workarounds")
*   Many patches on bugzilla, feel free to commit to 3.1 stream... avoid too many patches
    *   Community contributions: 42 [Open bugs with patches](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1) right now, should apply before patches get outdated (see also the [Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for a query)

  

### Cleanup Work

*   Unittests, unittests, unittests! -- ideally write an accompanying unittest for every bugfix
    *   [bug 230917](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230917) \[regression\] Some DStore Archive Testcases fail -- **AI Xuan** look at
    *   Abbot pretty much dead -- looking at SWTBot now
    *   Remember our 2-fix-per-week / 3 unittests-per-milestone plan
    *   Current situation is on [this bugzilla report](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=&y_axis_field=assigned_to&z_axis_field=&query_format=report-table&classification=DSDP&product=Target+Management&bug_status=RESOLVED&bug_status=VERIFIED&bug_status=CLOSED&chfieldfrom=2007-09-17&chfieldto=Now&chfield=bug_status&chfieldvalue=RESOLVED&format=table&action=wrap&negate0=1&field0-0-0=resolution&type0-0-0=equals&value0-0-0=DUPLICATE)
*   Migration Notes (for 2.0 / for 1.0?)
*   Review and improve Userdocs; we have several open bugs here
*   Review and improve Javadocs; lots still missing, unclear, duplicated
*   Fix broken hyperlinks in the docs:Xenu's LinkSleuth, fix HTML/XML errors (which can make the indexer not work)
*   Get rid of compiler warnings wherever possible
*   Run Findbugs -- Update site on [http://findbugs.cs.umd.edu/eclipse](http://findbugs.cs.umd.edu/eclipse), Quickdocs by Rado in [tm-dev E-Mail](http://dev.eclipse.org/mhonarc/lists/dsdp-tm-dev/msg01869.html)
    *   Question about filtering false positives posted on fb-discuss [link](https://mailman.cs.umd.edu/pipermail/findbugs-discuss/2008-May/002374.html)
*   Stuff for 3.1
    *   API Tooling Javadocs(@noextend and friends) - cannot limit existing API more than it was before, unless it was textually documented already, but can deprecate stuff, even in 3.0.1.

### Questions

Vacations
---------

*   DaveD busy in June, won't be able to handle builds in June; find somebody or have everything ready early

  

Action Items
------------

*   Last [DSDP/TM/Meetings/6-May-2009](/DSDP/TM/Meetings/6-May-2009 "DSDP/TM/Meetings/6-May-2009")
*   **Everyone** Fix target milestone of 3.1m7 assigned bugs.
*   **Martin** [bug 256581](https://bugs.eclipse.org/bugs/show_bug.cgi?id=256581) SSH performance; **old** review [bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176) Rado's deferred D&D; [bug 227750](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227750) IRSEInteractionProvider; [bug 240991](https://bugs.eclipse.org/bugs/show_bug.cgi?id=240991), [bug 239230](https://bugs.eclipse.org/bugs/show_bug.cgi?id=239230) Early startup; Run performance tests for [bug 236065](https://bugs.eclipse.org/bugs/show_bug.cgi?id=236065) IFileService improvements; Critical EFS bugs; RXTX 2.2;
*   **Anna**: Remotecdt; new builder based on CBI tutorial
*   **Xuan**: **old** Look at [bug 230917](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230917) Archive Handler Unittests
*   **DaveD**: **old** Create bug for partial model export; [bug 238574](https://bugs.eclipse.org/bugs/show_bug.cgi?id=238574) Make new website available and E-mail questions on mailinglist
*   **DaveM**: **old** [bug 199596](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199596) Read-Only attribute doesn't always update IRemoteFile;

Next Meeting
------------

*   Next [DSDP/TM/Meetings/3-Jun-2009](/DSDP/TM/Meetings/3-Jun-2009 "DSDP/TM/Meetings/3-Jun-2009") (2 weeks after)
*   Next [DSDP/TM/Meetings/17-Jun-2009 Committer](/DSDP/TM/Meetings/17-Jun-2009_Committer "DSDP/TM/Meetings/17-Jun-2009 Committer") (4 weeks after)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Meetings/20-May-2009_Committer](https://wiki.eclipse.org//DSDP/TM/Meetings/20-May-2009_Committer))