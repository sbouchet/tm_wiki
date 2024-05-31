

DSDP/TM/Meetings/16-Apr-2009 Committer
======================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")‎ | [Meetings](./Meetings "DSDP/TM/Meetings")

| Meeting Title: | **TM Committer Meeting** |
| --- | --- |
| Date & Time: | Thursday [Apr 16, 2009](./index.php?title=Apr_16,_2009&action=edit&redlink=1 "Apr 16, 2009 (page does not exist)") at [1600 UTC / 12pm Toronto](http://www.timeanddate.com/worldclock/fixedtime.html?month=4&day=16&year=2009&hour=16&min=00&sec=0&p1=0)   ![Html.gif](./images/Html.gif)[HTML](http://www.google.com/calendar/embed?src=vn70im36r00qeusu8nme50cils@group.calendar.google.com&ctz=Canada/Toronto) \| ![Ical.gif](./images/Ical.gif)[iCal](http://www.google.com/calendar/ical/vn70im36r00qeusu8nme50cils@group.calendar.google.com/public/basic.ics) |
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
*   [3 Vacations](#Vacations)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   Committers:
    *   IBM - Xuan Chen, Kevin Doyle, Dave Dykstal, Dave McKnight
    *   Wind River - Martin Oberhuber
    *   MontaVista - Anna Dushistova

Agenda
------

### Last Meetings

*   Last [DSDP/TM/Meetings/1-Apr-2009](./Meetings/1-Apr-2009 "DSDP/TM/Meetings/1-Apr-2009")
*   Last [DSDP/TM/Meetings/18-Mar-2009 Committer](./Meetings/18-Mar-2009_Committer "DSDP/TM/Meetings/18-Mar-2009 Committer")

### Status round call

*   DaveM - Import / Export / Synchronize
    *   Current code is very broken: UI not persisted properly; inconsistencies; not exported to the right place; comparison fails
    *   After DaveM's fixes, at least the UI handling works; started on a different path (timestamp comparison)
    *   [bug 185925](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185925) SOC bug, and [RSESync/Status and Ideas](./RSESync/Status_and_Ideas "RSESync/Status and Ideas") Wiki - DaveM to commit what he has today, and then decide how to proceed (perhaps ask for Community patches).
*   Xuan - [bug 270618](https://bugs.eclipse.org/bugs/show_bug.cgi?id=270618) Terminal Accessibility
    *   Preference for disabling some keys to be sent to the remote?
    *   Injecting a keyboard handler into the Terminal widget? - Provisional API
    *   Martin: Please list the requirements first. **AI Xuan** follow up with DaveD on accessibility requirements.
*   Anna - Remotecdt move
    *   DougS needs to make the move - **AI Martin** kick Doug
*   Martin - SSH initialization
    *   [bug 271244](https://bugs.eclipse.org/bugs/show_bug.cgi?id=271244) \- DaveM is right. initService() just connects the CHANNEL whereas the session is done by connector service. Same as initializing a miner in dstore. **AI Dave** to commit his patch and update the Javadocs.
*   Uwe - 2 files subsystems
    *   [bug 271243](https://bugs.eclipse.org/bugs/show_bug.cgi?id=271243) \- **AI Martin** to ask Uwe reproduce and comment on the bug. Also, add ref to dependent bug for regression.

  

### TM 3.1 status

*   **Big Rocks** see [DSDP/TM/Committer Phone Meeting 17-Dec-2008](./Committer_Phone_Meeting_17-Dec-2008 "DSDP/TM/Committer Phone Meeting 17-Dec-2008")
*   [3.1M6 Assigned Open bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&product=Target+Management&target_milestone=3.0&target_milestone=3.0.1&target_milestone=3.0.2&target_milestone=3.1+M2&target_milestone=3.1+M3&target_milestone=3.1+M4&target_milestone=3.1+M5&target_milestone=3.1+M6&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) \- **AI Everyone** reassign target milestone as appropriate
*   [3.1M7 Assigned Open bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&product=Target+Management&target_milestone=3.1+M7&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) \- [Galileo](./Galileo "Galileo") M7 is on Tue May 5!
*   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit) open bugs, [High Priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor) open bugs, [DSDP/TM/3.0 Known Issues and Workarounds](./3.0_Known_Issues_and_Workarounds "DSDP/TM/3.0 Known Issues and Workarounds")
*   Many patches on bugzilla, feel free to commit to 3.1 stream... avoid too many patches
    *   Community contributions: 42 [Open bugs with patches](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1) right now, should apply before patches get outdated (see also the [Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for a query)

Vacations
---------

*   DaveD busy in June, won't be able to handle builds in June; find somebody or have everything ready early

  

Action Items
------------

*   Last [DSDP/TM/Meetings/1-Apr-2009](./Meetings/1-Apr-2009 "DSDP/TM/Meetings/1-Apr-2009")
*   **Everyone** Fix target milestone of 3.1m6 assigned bugs.
*   **Martin** [bug 256581](https://bugs.eclipse.org/bugs/show_bug.cgi?id=256581) SSH performance; **old** review [bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176) Rado's deferred D&D; [bug 227750](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227750) IRSEInteractionProvider; [bug 240991](https://bugs.eclipse.org/bugs/show_bug.cgi?id=240991), [bug 239230](https://bugs.eclipse.org/bugs/show_bug.cgi?id=239230) Early startup; Run performance tests for [bug 236065](https://bugs.eclipse.org/bugs/show_bug.cgi?id=236065) IFileService improvements; Critical EFS bugs; RXTX 2.2;
*   **Anna**: Remotecdt; new builder based on CBI tutorial
*   **Xuan**: **old** Look at [bug 230917](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230917) Archive Handler Unittests
*   **DaveD**: **old** Create bug for partial model export; [bug 238574](https://bugs.eclipse.org/bugs/show_bug.cgi?id=238574) Make new website available and E-mail questions on mailinglist
*   **DaveM**: **old** [bug 199596](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199596) Read-Only attribute doesn't always update IRemoteFile;

Next Meeting
------------

*   Next [DSDP/TM/Meetings/6-May-2009](./Meetings/6-May-2009 "DSDP/TM/Meetings/6-May-2009") (3 weeks after)
*   Next [DSDP/TM/Meetings/20-May-2009 Committer](./Meetings/20-May-2009_Committer "DSDP/TM/Meetings/20-May-2009 Committer") (5 weeks after)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Meetings/16-Apr-2009_Committer](https://wiki.eclipse.org//DSDP/TM/Meetings/16-Apr-2009_Committer))