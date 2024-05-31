

DSDP/TM/Committer Phone Meeting 19-Jun-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Jun 19, 2007](./index.php?title=Jun_19,_2007&action=edit&redlink=1 "Jun 19, 2007 (page does not exist)") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=6&day=19&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in (this week only): | International **+1-314-655-1411**   North America **+1-877-422-0035** (toll free)   Passcode: **764918#** |

DaveD to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** DaveD will start Skype chat just prior to call.  
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
*   Wind River - (Martin Oberhuber n/a), Uwe Stieber, (Michael Scharf n/a)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 12-Jun-2007](./Committer_Phone_Meeting_12-Jun-2007 "DSDP/TM/Committer Phone Meeting 12-Jun-2007")

### News & Review Action Items

| Martin | 0% |  | 0% |
| --- | --- | --- | --- |
| DaveD | 90% | Builds, documentation, some late fixes | 90% |
| DaveM | 20% |  | 0% |
| Kushal | 0% |  | 0% |
| Javier | 30% |  | 30% |
| Ted | 0% | - | 0% |
| Uwe | 5% | - | 5% |
| Michael | 10% |  | 10% |

### Plan for the TM Future

*   Please review and edit [TM Future Planning](./TM_Future_Planning "TM Future Planning") together with your Requirements / Product Management folk
*   A TM Project Meeting is planned for SEPTEMBER 19th and 20th in Chicago, together with the Members Meeting.

### Ramp Down Plan

*   [TM 2.0 Ramp down Plan for Europa](./TM_2.0_Ramp_down_Plan_for_Europa "TM 2.0 Ramp down Plan for Europa"), based on [Europa Simultaneous Release#Milestones and Release Candidates](./Europa_Simultaneous_Release#Milestones_and_Release_Candidates "Europa Simultaneous Release")
    *   RC4 -- Thu Jun 21 (5 work days) - build will be sometime Wednesday afternoon Central Time.
    *   EUROPA -- Jun 29
*   Testing: **Please use RSE recent I-builds yourselves in daily work**
*   **2-committer-review required from now on**. Doc-only / Comment-only / Testcase fixes allowed without review.
*   **Only P1 and critical bugs this week**
    *   Exceptions: Doc-only/testcases/escalations
    *   Javadoc Reviews: @since tag for new API, missing @param tags, ...
    *   Discouraged Access Warnings: **AI Martin** switch off for dstore by using x-friend in Manifest
    *   Currently feels like too many bugs are assigned 2.0.1 -- but we'll decide that after 2.0 is released
    *   Our API is still declared "provisional"
    *   2.0.1 work can be done in branches - e.g. "temp201_dwd"? Merge immediately after 2.0 declared. **Caution:** 2.0.1 must be binary compatible with 2.0.0. Ensure that you have read the Eclipse API Guidelines again to understand what the restrictions are.
*   **Newsgroup and Mailing List Duty**

### Bugs and open work to be discussed

*   **Current Priorities:** Fix bugs by Priority
    *   **Javier**: There appears to be a problem in the underlying EFS support (see [192610](https://bugs.eclipse.org/bugs/show_bug.cgi?id=192610)). Continuing investigation, but will likely require a note of caution on using EFS remote projects.
    *   **DaveD**: build master for RC4; documentation fixes
        *   Fix userdocs wrt team support, user actions / compile commands
    *   **DaveM**: no open items
    *   **Xuan**: no open items
    *   **Martin**: SSH using new Jsch API from Platform RC3;
        *   Had to defer much assigned stuff e.g. expand-to-level;
        *   Releng scripts remain as they are for now - might consume Orbit manually at the end;
        *   Review and release Telnet fixes;
        *   [186315](https://bugs.eclipse.org/bugs/show_bug.cgi?id=186315) EFS problematic URIs - would love to see those fixed, if cannot do myself I might reassign;
        *   [170910](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170910) Integrate Terminalview -- **deferred**
        *   UI/Non-UI: would love to move SystemRegistry to non-UI for GregW -- then, extenders could write their own SubSystemConfiguration without using the SubSystemConfiguration abstract base classes, and remain in non-UI only (but no time :-()
    *   **Kushal**: [174789](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174789) Property pages added to Wizard automatically: **AI Kushal** investigate (will likely be taken by DaveD)
*   **Bugzilla**: [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   Martin Vacation Wed Jun 13 - Fri Jun 22
*   DaveM, DaveD taking a couple weeks in August
*   Javier ooo last two weeks in August

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_5-Jun-2007#Action_Items "DSDP/TM/Committer Phone Meeting 5-Jun-2007") Action Items
*   **DaveD**: RC4 Build, Doc items
*   **DaveM**: 2.0.1 fixes
*   **Kushal**:
*   **Martin**:
*   **Javier**:
*   **Michael**:

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 26-Jun-2007](./Committer_Phone_Meeting_26-Jun-2007 "DSDP/TM/Committer Phone Meeting 26-Jun-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=6&day=26&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) \- **To be hosted by MartinO**, back to our normal dial-in
*   Monthly [DSDP/TM/Phone Meeting 4-Jul-2007](./Phone_Meeting_4-Jul-2007 "DSDP/TM/Phone Meeting 4-Jul-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=7&day=4&year=2007&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_19-Jun-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_19-Jun-2007))