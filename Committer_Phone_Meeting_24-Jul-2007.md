

DSDP/TM/Committer Phone Meeting 24-Jul-2007
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday Jul 24, 2007 at [1500 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=7&day=24&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | **asterisk.eclipse.org** ID: **8984** Passcode: **1234** |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, kevin.j.doyle, xuan.chen886, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

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

*   Last meeting: [DSDP/TM/Committer Phone Meeting 18-Jul-2007](./Committer_Phone_Meeting_18-Jul-2007 "DSDP/TM/Committer Phone Meeting 18-Jul-2007")

### News & Review Action Items

| Martin | 100% | Asterisk feedback; Equinox-security people contacted; made [RXTX for Eclipse](http://users.frii.com/jarvi/rxtx/eclipse/site.xml) available - need to embed site URL in features, brush up update site web appearance; CDT Adapter Loading; 2.0.1 fixes | 100% |
| --- | --- | --- | --- |
| DaveD | 50% |  | 50% |
| DaveM | 70% |  | 70% |
| Xuan | 50% | About to become committer; Unit tests (14 test cases ready on local, dstore-win, dstore-linux) | 50% |
| Kevin | 80% |  | 80% |
| Javier | 30% |  | 30% |
| Uwe | 5% | - | 5% |
| Michael | 50% | Terminal performance improvements: Created 3-layer architecture, 50 unit tests - will need new TM-terminal-tests feature and test plugin(s), not yet checked in | 50% |

### Current Work

*   **Asterisk Conferencing**
    *   Quality was good with just Javier and Martin; lots of Echo making it unusable with Xuan and Kevin

  

*   [DSDP/TM/Face-to-face Meeting 19-Sep-2007](./Face-to-face_Meeting_19-Sep-2007 "DSDP/TM/Face-to-face Meeting 19-Sep-2007"): Moving to Toronto? Participants? Agenda Items?
    *   **AI DaveM** talk to Pete Nicholls for a room in Toronto
    *   **AI DaveD** confirm travel budget with IBM mgmt

  

*   Unit Tests / TPTP AGR
    *   Problems with dstore - how to change the daemon port without using the UI? **AI DaveM to help**
    *   Problems with a dialog popping up during the unit tests (SSL enable/disable): should be able to programmatically set that preference (In DStoreConnectorService)
    *   Calling ISubSystem.internalCreateFilterString() worked slightly different

*   [193329](https://bugs.eclipse.org/bugs/show_bug.cgi?id=193329) First Column in Table View
    *   Martin: PropertyDescriptor quirks -- filling PropertyView differently than Tableview -- **AI Martin** to look at it

*   **Bugzilla**: [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)
    *   **DaveD:** [194802](https://bugs.eclipse.org/bugs/show_bug.cgi?id=194802) Persistence issue reported by Greg Watson: UI/Non-UI
        *   [197036](https://bugs.eclipse.org/bugs/show_bug.cgi?id=197036), [181939](https://bugs.eclipse.org/bugs/show_bug.cgi?id=181939) All filter pools created on startup - lazy loading
    *   **DaveM:** [196662](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196662) Refresh on Dispatch thread could be tricky since already in the event handler -- getObject() is there since the adapter has no exists() method
        *   [196664](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196664) Refresh does too much work
    *   **Javier:** [197105](https://bugs.eclipse.org/bugs/show_bug.cgi?id=197105) FTP Solaris - waiting for info from reporter
    *   **Martin:** [197178](https://bugs.eclipse.org/bugs/show_bug.cgi?id=197178) (CDT) Discussing Adapter Loading (we do it synchronously in Activator.start() of the Core plugins which is problematic)
        *   [192610](https://bugs.eclipse.org/bugs/show_bug.cgi?id=192610) EFS to be attacked next thing
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

*   [Last Meeting](./Committer_Phone_Meeting_18-Jul-2007#Action_Items "DSDP/TM/Committer Phone Meeting 18-Jul-2007") Action Items
*   **DaveD**: **Let Martin know whether travel to Chicago/Toronto is possible**; 2.0.1 important fixes, then Doc bugs (Tutorial)
*   **DaveM**: **Ask Pete Nicholls about room for F2F meeting in Toronto**; [196662](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196662) refresh on dispatch thread
*   **Xuan**: **Asterisk:** try to get rid of Echo with Kevin; Unit Tests
*   **Kevin**: **Asterisk:** try to get rid of Echo with Xuan; 2.0.1 fixes
*   **Martin**: Look at PropertyDescriptor issues; EFS fixes; unit tests; Migration Docs, EFS Fixes, Releng Fixes, Newsgroup
*   **Javier**: 2.0.1 fixes, unit tests
*   **Michael**: Terminal performance improvements

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 31-Jul-2007](./Committer_Phone_Meeting_31-Jul-2007 "DSDP/TM/Committer Phone Meeting 31-Jul-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=7&day=31&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 1-Aug-2007](./Phone_Meeting_1-Aug-2007 "DSDP/TM/Phone Meeting 1-Aug-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=8&day=1&year=2007&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007")


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_24-Jul-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_24-Jul-2007))