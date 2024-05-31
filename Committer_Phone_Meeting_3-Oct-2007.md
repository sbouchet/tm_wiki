

DSDP/TM/Committer Phone Meeting 3-Oct-2007
==========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Oct 3, 2007](./index.php?title=Oct_3,_2007&action=edit&redlink=1 "Oct 3, 2007 (page does not exist)") at [1500 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=10&day=3&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | Martin to call everybody by Skype |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, kevin.j.doyle, xuan.chen886, rupen.mardirossian, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
    *   [2.1 Current Work](#Current-Work)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Xuan Chen, Dave McKnight, Kevin Doyle, Rupen Mardirossian, (Dave Dykstal n/a)
*   Wind River - Martin Oberhuber, (Uwe Stieber n/a), (Michael Scharf n/a)
*   Symbian - Javier Montalvo Orus

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Agenda
------

*   Last meeting: [DSDP/TM/Committer Phone Meeting 11-Sep-2007](./Committer_Phone_Meeting_11-Sep-2007 "DSDP/TM/Committer Phone Meeting 11-Sep-2007")
*   F2F meeting: [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007")

### Current Work

*   **Skype Call Quality**
    *   Javier's mic not working - trying to fix it; echos
*   **Code and Branching**
    *   Dont have a 3.0M2 contribution -- using 2.0.1 instead
    *   No reviews for 3.0 but take care; ask for review if something should go into 2.0.2
    *   Branch R2\_0\_maintenance for 2.0.2 fixes; all the rest goes into HEAD (3.0)
        *   Normal checkins to HEAD, just let everybody know in case of an API change
        *   For checkin to the branch, create a separate bug for the same issue
    *   When marking a bug fixed, **please set target milestone (3.0 M3)**
*   Committer Calls less frequently now
    *   Martin proposes meetings every 2 weeks - if issues come up anybody can request a meeting
    *   DaveM might need more frequent meetings to address questions
*   **Planning** \- **AI Martin** to write up what we discussed in Toronto
*   Bug Fixing - **Remember our 2-fix-per-week / 3 unittests-per-milestone plan**
*   **DaveD:** \- vacation - [bug 202630](https://bugs.eclipse.org/bugs/show_bug.cgi?id=202630) new meaning of "default private system profile"?
*   **DaveM:** \- [bug 187739](https://bugs.eclipse.org/bugs/show_bug.cgi?id=187739) exists() method in the SystemViewElementAdapter
*   **Kevin:** -
*   **Xuan:** \- fixed a bug + added unittest, checkin pending; will need to do IBM stuff the next 2 weeks
*   **Javier:** \- will look at [bug 199773](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199773) FTP upload as binary
*   **Martin:**
    *   [bug 202416](https://bugs.eclipse.org/bugs/show_bug.cgi?id=202416) **Question for DaveD:** NPE when loading profile: made it more robust, but how could it come that RSE profile data is wiped with zeros? What happens when an IOException occurs while saving a profile, can it become corrupted or is there a safeguard?
*   **Uwe:** -
*   **Rupen:** \- busy with IBM stuff
*   **Michael:** -
*   **Questions**

*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   DaveD vacation Spt 27 - Oct 9
*   Martin at ESE Oct 9 - 12
*   Canadian Thanksgiving Monday Oct 8

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_11-Sep-2007#Action_Items "DSDP/TM/Committer Phone Meeting 11-Sep-2007") Action Items
*   **DaveD**: fixes, unit tests
*   **DaveM**: fixes, unit tests
*   **Xuan**: fixes, unit tests
*   **Kevin**: fixes, unit tests
*   **Martin**: Write-up TM 3.0 Plan; Look at PropertyDescriptor issues; unit tests; Releng Fixes, Newsgroup
*   **Javier**: fixes, unit tests
*   **Michael**: Terminal performance improvements

Next Meeting
------------

*   Monthly [DSDP/TM/Phone Meeting 3-Oct-2007](./Phone_Meeting_3-Oct-2007 "DSDP/TM/Phone Meeting 3-Oct-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=10&day=3&year=2007&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Committer Phone Meeting 17-Oct-2007](./Committer_Phone_Meeting_17-Oct-2007 "DSDP/TM/Committer Phone Meeting 17-Oct-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=10&day=17&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_3-Oct-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_3-Oct-2007))