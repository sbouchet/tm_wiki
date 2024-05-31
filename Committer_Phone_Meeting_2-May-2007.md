

DSDP/TM/Committer Phone Meeting 2-May-2007
==========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [May 2, 2007](./index.php?title=May_2,_2007&action=edit&redlink=1 "May 2, 2007 (page does not exist)") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=5&day=2&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 News & Review Action Items](#News-.26-Review-Action-Items)
    *   [2.2 Time Plan and Deadlines toward M7](#Time-Plan-and-Deadlines-toward-M7)
    *   [2.3 Bugs and open work to be discussed](#Bugs-and-open-work-to-be-discussed)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave McKnight, Dave Dykstal, Kushal Munir, Kevin Doyle, Xuan Chen
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Michael Scharf, (Uwe Stieber n/a)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 24-Apr-2007](./DSDP/TM/Committer_Phone_Meeting_24-Apr-2007 "DSDP/TM/Committer Phone Meeting 24-Apr-2007")

### News & Review Action Items

| Martin | 30% | Platform symbolic links; API cleanups; | 100% |
| --- | --- | --- | --- |
| DaveD | 40% | IBM issues; UDA Persistence design; concerned about getting UDA in shape | 80% |
| DaveM | 40% | Bugfixes | 40% |
| Kushal | 40% | BIDI Encodings; UDA | 40% |
| Javier | 50% | FTP Parser Extension Point - Problems persisting Property Set | 50% |
| Ted | 0% | - | 0% |
| Uwe | 5% | - | 5% |
| Michael | 10% |  | 10% |

### Time Plan and Deadlines toward M7

*   **Plan towards M7** \- goals and deadlines for I-builds
    *   I20070503 -- Minor API changes - Final Feature Additions - Feature Freeze (Terminal integration; FTP Parser)
    *   I20070510 -- Stabilization, start [TM 2.0 M7 Testing](./TM_2.0_M7_Testing "TM 2.0 M7 Testing") on May 14th
    *   I20070516 -- TM 2.0M7 (17th is a public holiday in Austria!)
    *   **Reminder: [TM 2.0 Ramp down Plan for Europa](./TM_2.0_Ramp_down_Plan_for_Europa "TM 2.0 Ramp down Plan for Europa")**

### Bugs and open work to be discussed

*   **Current Priorities**
    *   **Priority #1: Finish API Changes**
        *   **Javier**: FTP parallel download, allowing to register directory listing parser by extension point
            *   Javier will move extension point from the service to the subsystem
    *   **Priority #2: Import/Export and User Actions**
        *   *   User Actions is really more of a framework than a concrete implementation. Extenders would need to write UI etc. for handling their own user actions.
            *   It's too late for such a framework if we cannot come up with a good default implementation. Better drop the User Actions plan item. Having it as a committed plan item was due to the misunderstanding that this would ONLY be a concrete implementation of shortcuts for Shell rather than a framework.
    *   **Priority #3: Bugs**
        *   Bugzilla: [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)
        *   Encoding Issues: Kushal single encoding control for all subsystems? [179939](https://bugs.eclipse.org/bugs/show_bug.cgi?id=179939) What about binary vs. ASCII file transfer?
            *   All transfer is now done in binary for dstore and ssh; but some protocols like FTP may make a difference, so keep the ASCII vs. binary Preference page for now.
            *   Dstore now remembers original encoding in the cache rather than re-coding during the transfer (all transfer is done in binary). DaveM is concerned about this approach in the case some resources are exported. We think that the recoding would happen when transferring from the temp location to the target.

*   **General Guidelines**
    *   Avoid breaking API changes after end of this week
    *   Junior Jobs: Bugs marked as JJ: in the subject - similar to "helpwanted" keyword

Vacation, Away
--------------

Action Items
------------

*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_24-Apr-2007#Action_Items "DSDP/TM/Committer Phone Meeting 24-Apr-2007") Action Items
*   **DaveD**: Translation Testcases; Persistence Provider without IResource; Get started on ICU4J with [bug 183631](https://bugs.eclipse.org/bugs/show_bug.cgi?id=183631)
*   **DaveM**: Bugs
*   **Kushal**: BIDI bugs and Encodings
*   **Martin**: API cleanups; Testing Stats; Refresh improvements; Integrating Terminal with RSE
*   **Javier**: FTP parallel download, registering FTP Parser by extension point

Next Meeting
------------

*   Monthly [DSDP/TM/Phone Meeting 2-May-2007](./DSDP/TM/Phone_Meeting_2-May-2007 "DSDP/TM/Phone Meeting 2-May-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=5&day=2&year=2007&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Committer Phone Meeting 8-May-2007](./DSDP/TM/Committer_Phone_Meeting_8-May-2007 "DSDP/TM/Committer Phone Meeting 8-May-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=5&day=8&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_2-May-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_2-May-2007))