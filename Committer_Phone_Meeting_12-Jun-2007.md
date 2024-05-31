

DSDP/TM/Committer Phone Meeting 12-Jun-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Jun 12, 2007](./index.php?title=Jun_12,_2007&action=edit&redlink=1 "Jun 12, 2007 (page does not exist)") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=6&day=12&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Invited Attendees](#Invited-Attendees)
*   [2 Notes](#Notes)
    *   [2.1 News & Review Action Items](#News-.26-Review-Action-Items)
    *   [2.2 Plan for the TM Future](#Plan-for-the-TM-Future)
    *   [2.3 Ramp Down Plan](#Ramp-Down-Plan)
    *   [2.4 Bugs and open work to be discussed](#Bugs-and-open-work-to-be-discussed)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Invited Attendees
-----------------

*   IBM - Dave McKnight, Dave Dykstal, Kevin Doyle, Xuan Chen, (Kushal Munir n/a)
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber, (Michael Scharf n/a)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 5-Jun-2007](./Committer_Phone_Meeting_5-Jun-2007 "DSDP/TM/Committer Phone Meeting 5-Jun-2007")

### News & Review Action Items

| Martin | 80% | Release Review OK; Code Reviews; Licensing for Europa; Some simple fixes e.g. Terminal | 0% |
| --- | --- | --- | --- |
| DaveD | 90% |  | 90% |
| DaveM | 80% |  | 80% |
| Kushal | 40% |  | 40% |
| Javier | 30% | Added Discovery Docs | 30% |
| Ted | 0% | - | 0% |
| Uwe | 5% | - | 5% |
| Michael | 10% |  | 10% |

### Plan for the TM Future

*   Please review and edit [TM Future Planning](./TM_Future_Planning "TM Future Planning") together with your Requirements / Product Management folk
*   A TM Project Meeting is planned for SEPTEMBER 19th and 20th in Chicago, together with the Members Meeting.

### Ramp Down Plan

*   [TM 2.0 Ramp down Plan for Europa](./TM_2.0_Ramp_down_Plan_for_Europa "TM 2.0 Ramp down Plan for Europa"), based on [Europa Simultaneous Release#Milestones and Release Candidates](./Europa_Simultaneous_Release#Milestones_and_Release_Candidates "Europa Simultaneous Release")
    *   RC3 -- Thu Jun 14 (thursday)
    *   RC4 -- Thu Jun 21 (5 work days)
    *   EUROPA -- Jun 29
*   Testing: **Please use RSE recent I-builds yourselves in daily work**
*   **2-committer-review required from now on**. Doc-only / Comment-only / Testcase fixes allowed without review.
*   **Only P1, P2, Major bugs and regressions** from now on
    *   Exception: Doc-only/testcases/escalations
    *   Javadoc Reviews: @since tag for new API, missing @param tags, ...
    *   Discouraged Access Warnings: **AI Martin** switch off for dstore by using x-friend in Manifest
    *   Currently feels like too many bugs are assigned 2.0.1 -- but we'll decide that after 2.0 is released
    *   Our API is still declared "provisional"
*   **Newsgroup and Mailing List Duty**

### Bugs and open work to be discussed

*   **Current Priorities:** Fix bugs by Priority
    *   **Javier**:
    *   **DaveD**: build master; coordinate committer meeting next week
        *   Fix userdocs wrt team support, user actions / compile commands
    *   **DaveM**: UI blocking for archives - hard and risky; OK deferring for Local; not sure what's the right way to go; better add a warning about local archives into the release notes; there might be more issues with remote since we still cannot cancel things properly (UI would be responsive, but server would be busy) --> Deferring to 2.0.1
        *   Couple of Remote Scratchpad issues, are deferrable
        *   Filter naming - (naming filter pools under the covers) too risky
        *   Remaining one: [188365 dstore version](https://bugs.eclipse.org/bugs/show_bug.cgi?id=188365)
    *   **Xuan**: expand folders [191280 dstore performance](https://bugs.eclipse.org/bugs/show_bug.cgi?id=191280) \- good improvements made (commit for 2.0) - more improvements possible for the Future
    *   **Martin**: SSH using new Jsch API from Platform RC3;
        *   Had to defer much assigned stuff e.g. expand-to-level;
        *   Releng scripts remain as they are for now - might consume Orbit manually at the end;
        *   Review and release Telnet fixes;
        *   [186315](https://bugs.eclipse.org/bugs/show_bug.cgi?id=186315) EFS problematic URIs - would love to see those fixed, if cannot do myself I might reassign;
        *   [170910](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170910) Integrate Terminalview -- **deferred**
        *   UI/Non-UI: would love to move SystemRegistry to non-UI for GregW -- then, extenders could write their own SubSystemConfiguration without using the SubSystemConfiguration abstract base classes, and remain in non-UI only (but no time :-()
    *   **Kushal**: [174789](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174789) Property pages added to Wizard automatically: **AI Kushal** investigate
*   **Bugzilla**: [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   Martin Vacation Wed Jun 13 - Fri Jun 22
*   DaveM, DaveD taking a couple weeks in August
*   Javier ooo last two weeks in August

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_5-Jun-2007#Action_Items "DSDP/TM/Committer Phone Meeting 5-Jun-2007") Action Items
*   **DaveD**: Translation Testcases
*   **DaveM**: Refresh Bugs
*   **Kushal**:
*   **Martin**: Testing Stats; Refresh improvements;
*   **Javier**:
*   **Michael**:

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 19-Jun-2007](./Committer_Phone_Meeting_19-Jun-2007 "DSDP/TM/Committer Phone Meeting 19-Jun-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=6&day=19&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) \- **To be hosted by DaveD**, different dial-in
*   Monthly [DSDP/TM/Phone Meeting 4-Jul-2007](./Phone_Meeting_4-Jul-2007 "DSDP/TM/Phone Meeting 4-Jul-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=7&day=4&year=2007&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_12-Jun-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_12-Jun-2007))