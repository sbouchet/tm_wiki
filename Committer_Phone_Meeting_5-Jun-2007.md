

DSDP/TM/Committer Phone Meeting 5-Jun-2007
==========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday Jun 5, 2007 at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=6&day=5&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
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

*   IBM - Dave McKnight, Dave Dykstal, Kushal Munir, Kevin Doyle, Xuan Chen
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Michael Scharf, Uwe Stieber

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 29-May-2007](./Committer_Phone_Meeting_29-May-2007 "DSDP/TM/Committer Phone Meeting 29-May-2007")

### News & Review Action Items

| Martin | 80% | Reviews were more work than expected; Releng changes; Licensing for Europa; Preparing Release Review (tomorrow!) | 50% |
| --- | --- | --- | --- |
| DaveD | 90% |  | 90% |
| DaveM | 80% |  | 80% |
| Kushal | 40% |  | 40% |
| Javier | 30% |  | 30% |
| Ted | 0% | - | 0% |
| Uwe | 5% | - | 5% |
| Michael | 10% |  | 10% |

### Plan for the TM Future

*   Please review and edit [TM Future Planning](./TM_Future_Planning "TM Future Planning") together with your Requirements / Product Management folk
*   A TM Project Meeting is planned for SEPTEMBER 19th and 20th in Chicago, together with the Members Meeting.

### Ramp Down Plan

*   [TM 2.0 Ramp down Plan for Europa](./TM_2.0_Ramp_down_Plan_for_Europa "TM 2.0 Ramp down Plan for Europa"), based on [Europa Simultaneous Release#Milestones and Release Candidates](./Europa_Simultaneous_Release#Milestones_and_Release_Candidates "Europa Simultaneous Release")
    *   RC2 -- Tue Jun 5 (today)
    *   RC3 -- Thu Jun 14 (7 work days; Martin vacation 12-Jun til 21-Jun!)
    *   RC4 -- Thu Jun 21 (5 work days)
    *   EUROPA -- Jun 29
*   Testing: **Please use RSE RC2 yourselves in daily work**
*   **2-committer-review required from now on**. Doc-only / Comment-only / Testcases fixes allowed without review.
*   Only P1, P2, Major bugs and regressions from now on
    *   Exception: Doc-only/testcases/escalations
    *   Copyright comments all done by Martin, might want to Review / check yours

### Bugs and open work to be discussed

*   **Current Priorities:** Fix bugs by Priority
    *   **Javier**: User docs and ISV docs for Discovery? **AI Martin** help out with releng aspects.
        *   Q: separate books for Discovery ISV and Userdocs, or just plug-in to RSE help book?
        *   [173518](https://bugs.eclipse.org/bugs/show_bug.cgi?id=173518) Read-only changes
    *   **DaveD**: N-builds / I-builds: DaveD to try out N-builds, then learn I-builds and how to contribute to Europa
        *   Rename "Team" view -> "Profiles" view
        *   No Team-support for now; agreed to not write up manual "hack" documentation
    *   **DaveM**: IRemoteObjectAdapter: what about using the new API?
        *   isRemote() used in a couple of places in SystemView; other places still using IRremoteObjectAdapter; **AI DaveM** go through and change all to using isRemote()
        *   dnd: Download-on-Copy resolved for now
        *   Copy as binary although text mode specified
    *   **Martin**: Need to bring Releng scripts up to latest for Orbit; Review and release Telnet fixes; [176461](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176461) expand-to-level; [186315](https://bugs.eclipse.org/bugs/show_bug.cgi?id=186315) EFS problematic URIs;
        *   [170910](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170910) Integrate Terminalview -- **OK to defer?**
        *   UI/Non-UI: ISystemRegistry, SubSystemConfiguration
    *   **Kushal**: [179937](https://bugs.eclipse.org/bugs/show_bug.cgi?id=179937) Single "Encoding" control on the Host (for all subsystems)
        *   [174789](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174789) Property pages added to Wizard automatically: **AI Kushal** investigate
*   **Bugzilla**: [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   Thursday Jun 7 - public holiday in Austria (Martin ooo)
*   Martin Vacation Wed Jun 13 - Fri Jun 22
*   DaveM, DaveD taking a couple weeks in August
*   Javier ooo last two weeks in August

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_29-May-2007#Action_Items "DSDP/TM/Committer Phone Meeting 29-May-2007") Action Items
*   **DaveD**: Translation Testcases; Persistence Provider without IResource
*   **DaveM**: Refresh Bugs
*   **Kushal**: BIDI bugs and Encodings
*   **Martin**: Testing Stats; Refresh improvements; Integrating Terminal with RSE
*   **Javier**:
*   **Michael**:

Next Meeting
------------

*   [Europa Simultaneous Release](./Europa_Simultaneous_Release "Europa Simultaneous Release") Release Review on [6-Jun-2007 at 7am PST / 1400 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=6&day=6&year=2007&hour=7&min=0&sec=0&p1=221)
*   Monthly [DSDP/TM/Phone Meeting 6-Jun-2007](./Phone_Meeting_6-Jun-2007 "DSDP/TM/Phone Meeting 6-Jun-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=6&day=6&year=2007&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Committer Phone Meeting 12-Jun-2007](./Committer_Phone_Meeting_12-Jun-2007 "DSDP/TM/Committer Phone Meeting 12-Jun-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=6&day=12&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_5-Jun-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_5-Jun-2007))