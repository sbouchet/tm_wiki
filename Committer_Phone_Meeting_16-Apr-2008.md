

DSDP/TM/Committer Phone Meeting 16-Apr-2008
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Apr 16, 2008](./index.php?title=Apr_16,_2008&action=edit&redlink=1 "Apr 16, 2008 (page does not exist)") at [1445 UTC / 0745 SFO / 0945 Rochester / 1045 Toronto / 1545 London / 1645 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=4&day=16&hour=14&min=45&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | Martin to call everybody by Skype |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kevin.j.doyle, xuan.chen886, rupen.mardirossian, javier.montalvoorus, eugenetarassov, michael\_scharf, uwe.stieber, radoslav.gerganov.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 **M7 Work Items**](#M7-Work-Items)
*   [3 Vacation, away](#Vacation.2C-away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Xuan Chen, Dave McKnight, Dave Dykstal, Rupen Mardirossian, Kevin Doyle
*   Wind River - Martin Oberhuber, Uwe Stieber, (Eugene Tarassov n/a), (Michael Scharf n/a)
*   Symbian - (Javier Montalvo Orus n/a)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 9-Apr-2008](./Committer_Phone_Meeting_9-Apr-2008 "DSDP/TM/Committer Phone Meeting 9-Apr-2008")
*   **Skype Call Quality**
    *   Xuan has break-offs, it's good for everyone else. **AI Xuan** upgrade Skype, check Task Monitor and network

### **M7 Work Items**

M7 is only 3 weeks (May 7) and it is the **feature freeze**. So we need to get our stuff in!

*   Bugzilla [M7 assigned bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&target_milestone=3.0+M6&target_milestone=3.0+M7&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) \- want any other bugs promoted to M7, then do it now!
*   **Everyone:**
    *   [PII Bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&product=Target+Management&keywords_type=allwords&keywords=pii&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) use "pii" keyword in bugzilla. PII Drop 4 is on Monday Apr 21 -- best get all PII fixes in today such that they are part of tomorrow's I-Build
    *   Marking API as @noextend / @noimplement etc -- [DSDP/TM/Code Ownership](./Code_Ownership "DSDP/TM/Code Ownership")
*   **Martin:**
    *   Releng with Web Interface on dsdp.eclipse.org -- required for DaveD to be Ganymede Contact in June
    *   Finish UI/Non-UI Splitting
    *   [bug 170910](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170910) RSE Terminal Integration - Montavista Contribution
*   **?:** Apply Patches (from Rupen and others) - [Bugzilla Open with Patch attached](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1)
*   **DaveD:** Import/Export Profiles and Connections; **AI DaveD** merge Rupen's patches
*   **Xuan:** User Actions; busy with IBM
*   **Javier:** (n/a) FTP Hang - **AI Martin** contact privately
*   **Kevin:** pretty much gone for M7, back in May & June
*   **Rupen:** dialog patches / enhancements (just display files)
*   **Michael:** (n/a)
*   **DaveM:** DStore file buffer size Preference; FTP Parser for USS on z/OS **AI DaveM** file a bug / enhancement request; protected method regression
*   **Uwe:** **AI Uwe** review New Connection Wizard @noextend
*   Bugzilla [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor) \- see the [Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for more interesting queries
*   Xuan: UI Testing: Helper functions to do the testing - add to "internal" classes
*   Martin: Dont need to send every patch for review
*   Xuan: Tool for querying JUnit Test Owners? - No, queries are manual for now

Vacation, away
--------------

*   MartinO in Ottawa for [E4/Summit](./E4/Summit "E4/Summit") May 22-23 .. want to meet in Toronto?
*   MartinO vacation June 11 - 22
*   DaveM vacation June 16 - 20
*   DaveD in July -- **AI Martin** finish and test the new Build scripts on dsdp.eclipse.org till then

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_9-Apr-2008#Action_Items "DSDP/TM/Committer Phone Meeting 9-Apr-2008") Action Items
*   **Everyone**: **Fix PII Issues**; Reassign bugs away from M7 where possible, or to M7 where necessary in order to properly reflect feature freeze; **Add @noextend etc** according to [DSDP/TM/Code Ownership](./Code_Ownership "DSDP/TM/Code Ownership") table
*   **Rupen**:
*   **DaveD**: Merge Rupens patches; Finish profile import/export; Update [bug 221211](https://bugs.eclipse.org/bugs/show_bug.cgi?id=221211) IFileService multi-commands Javadoc
*   **DaveM**: Create bugs for 2 reported issues; contact IBM teams for [bug 220379](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220379) DStoreFileService API; think about [bug 216252](https://bugs.eclipse.org/bugs/show_bug.cgi?id=216252) SystemMessages global vs. local message ID; create a new "Future" bug for dstore protocol handshake, cloned from [bug 220892](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220892)
*   **Xuan**: Upgrade Skype to fix quality issues; Use Kevin's Properties for Unit Tests
*   **Kevin**: Website Updates
*   **Martin**: New Project Plan; Ganymede Rampdown Plan; Commons Net Placeholder CQ; UI/Non-UI Splitting; finish new releng; Look at PropertyDescriptor issues; unit tests
*   **Javier**: add unit tests; document the Symbian internal test setup similar to [CVS](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204138#c20) \-\- see also [CVS_Development#Testing](./CVS_Development#Testing "CVS Development")
*   **Michael**: Terminal improvements
*   **Uwe**: Add @noextend / @noimplement to New Connection Wizard where appropriate

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 30-Apr-2008](./Committer_Phone_Meeting_30-Apr-2008 "DSDP/TM/Committer Phone Meeting 30-Apr-2008") (2 weeks) at [1500 UTC / 0800 SFO / 1000 Rochester / 1100 Toronto / 1600 London / 1700 Barcelona+Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=4&day=30&hour=15&min=0&sec=0&p1=224&p2=159&p3=250&p4=31&p5=223&iv=1800)
*   Next [BugDay/April_2008](./BugDay/April_2008 "BugDay/April 2008") on Apr 25
*   Monthly [DSDP/TM/Phone Meeting 7-May-2008](./Phone_Meeting_7-May-2008 "DSDP/TM/Phone Meeting 7-May-2008") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=5&day=7&year=2008&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_16-Apr-2008](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_16-Apr-2008))