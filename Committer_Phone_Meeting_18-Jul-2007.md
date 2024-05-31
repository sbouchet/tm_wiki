

DSDP/TM/Committer Phone Meeting 18-Jul-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Jul 18, 2007](./index.php?title=Jul_18,_2007&action=edit&redlink=1 "Jul 18, 2007 (page does not exist)") at [1500 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=7&day=18&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | **asterisk.eclipse.org** ID: **8980** Passcode: **1234** |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

  
MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 News & Review Action Items](#News-.26-Review-Action-Items)
    *   [2.2 Current Work](#Current-Work)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave McKnight, Dave Dykstal, Xuan Chen, Kevin Doyle
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Michael Scharf, Uwe Stieber

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 10-Jul-2007](./Committer_Phone_Meeting_10-Jul-2007 "DSDP/TM/Committer Phone Meeting 10-Jul-2007")

### News & Review Action Items

| Martin | 100% | Bug triage, RXTX releng, fixes (e.g. deadlock) | 100% |
| --- | --- | --- | --- |
| DaveD | 50% |  | 50% |
| DaveM | 70% |  | 70% |
| Javier | 30% |  | 30% |
| Uwe | 5% | - | 5% |
| Michael | 10% | Really working on terminal performance now + refactorings | 50% |

### Current Work

*   **Asterisk Conferencing**
    *   Quality too bad 5 people with DaveM calling from home

  

*   [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007"): Participants? Agenda Items? - Martin needs confirmation to book his flight.
    *   DaveD: Extreme travel restrictions at IBM -- asking till Friday 20th whether the Dave's can come
*   [2.0.1 Ramp Down Plan](./TM_2.0_Ramp_down_Plan_for_Europa#Ramp_down_for_Europa_SR1_.2828-Sep-2007.29 "TM 2.0 Ramp down Plan for Europa"): Questions? Thoughts?
    *   End of August cutoff for 2.0.1 is OK -- may not be able to do all assigned 2.0.1 ones
    *   Deferring not a problem, currently it's more of a "what's possible assignment"
*   Unit Tests / TPTP AGR
    *   Xuan spent some time on Unittests, created a test for create/copy/rename of archives, want to create some more
    *   Created some stuff, will check in once promoted to committer
    *   Just calling the APIs -- did not find a similar testcase to re-use; local host for now, dstore as next step.

  

*   **Deadlock:** Everybody please read the text on synchronized at [bug 196919 comment 2](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196919#c2)
    *   Uwe: Is RSE thread aware? - We are using Jobs; some parts are well protected (RSEPersistenceProvider: single-threaded); model objects not so sure; old IBM RSE was mostly dispatch thread, added jobs later, tried to be careful.

*   [193329](https://bugs.eclipse.org/bugs/show_bug.cgi?id=193329) First Column in Table View
    *   Martin: PropertyDescriptor quirks -- filling PropertyView differently than Tableview -- **AI Martin** to look at it

  

*   **Bugzilla**: [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)
    *   **DaveM:** [193858](https://bugs.eclipse.org/bugs/show_bug.cgi?id=193858) RSE folder tree problem -- [195285](https://bugs.eclipse.org/bugs/show_bug.cgi?id=195285) mountPathMappers enhancement needs API change, so have to defer to the Future; Workaround is using different forms of the IP address for the same host.
    *   **DaveM:** [196662](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196662) Refresh on Dispatch thread could be tricky since already in the event handler -- getObject() is there since the adapter has no exists() method
        *   Martin - perhaps solve it with Callbacks as temporary solution, add an exists() method in the future (we just re-get the existing object)
    *   **Martin:** [192610](https://bugs.eclipse.org/bugs/show_bug.cgi?id=192610) EFS to be attacked next thing
    *   **Xuan:** [191374](https://bugs.eclipse.org/bugs/show_bug.cgi?id=191374) SSH Performance on large directory -- fix the dependent bugs, then re-try again

  

*   Javadoc Reviews: @since tag for new API, missing @param tags, ... can be fixed now for RSE since we are rebuilding just about every RSE plugin for 2.0.1 (except discovery, terminal, remotecdt, tests right now)

Vacation, Away
--------------

*   Xuan -public holidays beginning of August (Aug 3rd, Aug 6th) in Toronto
*   DaveD working on and off
*   DaveM, DaveD taking a couple weeks in August
*   Javier ooo last two weeks in August

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_10-Jul-2007#Action_Items "DSDP/TM/Committer Phone Meeting 10-Jul-2007") Action Items
*   **DaveD**: **Let Martin know whether travel to Chicago/Toronto is possible**; Xuan committer form; 2.0.1 important fixes, then Doc bugs (Tutorial)
*   **DaveM**: 2.0.1 fixes, [196662](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196662) refresh on dispatch thread
*   **Xuan**: Fill in committer questionnaire; Unit Tests
*   **Martin**: Look at PropertyDescriptor issues; EFS fixes; unit tests; Migration Docs, EFS Fixes, Releng Fixes, Newsgroup
*   **Javier**: 2.0.1 fixes, unit tests
*   **Michael**: Terminal performance improvements

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 24-Jul-2007](./Committer_Phone_Meeting_24-Jul-2007 "DSDP/TM/Committer Phone Meeting 24-Jul-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=7&day=24&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 1-Aug-2007](./Phone_Meeting_1-Aug-2007 "DSDP/TM/Phone Meeting 1-Aug-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=8&day=1&year=2007&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007")


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_18-Jul-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_18-Jul-2007))