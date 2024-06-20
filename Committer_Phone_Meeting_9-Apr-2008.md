

DSDP/TM/Committer Phone Meeting 9-Apr-2008
==========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday Apr 9, 2008 at [1500 UTC / 0800 SFO / 1000 Rochester / 1100 Toronto / 1600 London / 1700 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=4&day=9&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | Martin to call everybody by Skype |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, kevin.j.doyle, xuan.chen886, rupen.mardirossian, javier.montalvoorus, eugenetarassov, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 **Current Focus**](#Current-Focus)
    *   [2.2 **Bug Discussions**](#Bug-Discussions)
    *   [2.3 Committer Status and Report](#Committer-Status-and-Report)
    *   [2.4 Future and Planning](#Future-and-Planning)
*   [3 Vacation, away](#Vacation.2C-away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Xuan Chen, Dave McKnight, Dave Dykstal, Rupen Mardirossian, Kevin Doyle
*   Wind River - Martin Oberhuber, Michael Scharf, (Uwe Stieber n/a), (Eugene Tarassov n/a)
*   Symbian - (Javier Montalvo Orus could not connect)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 26-Mar-2008](./Committer_Phone_Meeting_26-Mar-2008 "DSDP/TM/Committer Phone Meeting 26-Mar-2008")
*   **Skype Call Quality**
    *   Dropouts for Xuan today, rest was good; Javier failed to join

### **Current Focus**

*   **Unit Tests** \- next priority after API
*   Will migrate to new Releng after M6 (adopt P2, nightly tests, signing etc... too risky for now, focus on API)
*   Adopting [Api Tooling](https://wiki.eclipse.org/Api_Tooling "Api Tooling"): all API Leaks done except one, see below

*   **API changes to vote on:**
    *   [bug 218685](https://bugs.eclipse.org/bugs/show_bug.cgi?id=218685) \- SSH timeout - **AI DaveM** to contact the reporter
    *   [bug 220547](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220547) \- SystemMessage - **AI DaveM** Document namespaces for SystemMessageID
    *   [bug 221138](https://bugs.eclipse.org/bugs/show_bug.cgi?id=221138) \- Get rid of SystemSelectRemoteFileOrFolderDialog and friends - **AI Xuan** move to "internal" package
    *   [bug 216252](https://bugs.eclipse.org/bugs/show_bug.cgi?id=216252) \- Revert Cancelled to Canceled - **AI Martin** decide and implement, either decision good for all
    *   [bug 225506](https://bugs.eclipse.org/bugs/show_bug.cgi?id=225506) \- API Leakage in RSEUIPlugin - **AI Martin** create bug for restoring behavior and move the method
    *   [bug 190231](https://bugs.eclipse.org/bugs/show_bug.cgi?id=190231) \- Subsystem to non-UI - **AI Martin** create patch, others to review soon
    *   [bug 170910](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170910) \- Terminal APIs - **AI Martin** create patch, others to review soon
    *   [bug 196942](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196942) \- final methods in ISubSystemConfiguration - **AI Martin** Defer
    *   [bug 226262](https://bugs.eclipse.org/bugs/show_bug.cgi?id=226262) \- IService IAdaptable - **AI Martin** attach patch, others give +1 on the bug
    *   [bug 226301](https://bugs.eclipse.org/bugs/show_bug.cgi?id=226301) \- IShellService methods should throw SystemMessageException - **AI Martin** attach patch, others give +1 on the bug

### **Bug Discussions**

*   [bug 214887](https://bugs.eclipse.org/bugs/show_bug.cgi?id=214887) WinCE Subsystem - integrated
*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

### Committer Status and Report

*   **Javier** \- [bug 212382](https://bugs.eclipse.org/bugs/show_bug.cgi?id=212382) ftpListingParser initCommands
*   **DaveM**
    *   JUnit should autotest dstore against old servers as well - an IBM thing
    *   When will we create 3.0.x service packs? - can do at any time; by default will use Ganymede train, mid september
    *   Artemis EMF IBM discussion
*   **MartinO**
    *   GSoC student Takuya Miyamoto for [bug 185925](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185925)
*   **Xuan**
    *   Only one IPZilla 3rd party code addition (WindowsCE) - Martin: its an optional download, marked as Incubation
    *   Commons Net 1.5 -- release expected real soon, Martin going to try and bring into 3.0 if accepted by EMO legal

### Future and Planning

*   **Planning** \- **AI Martin** to write up what we discussed in Toronto
    *   Think about assigning bugs to target milestones. What goes into 3.0 and what not? - DaveD Mylyn is nice for bug review!
    *   [bug 215301](https://bugs.eclipse.org/bugs/show_bug.cgi?id=215301) New Standard Project Plan Format
*   TM Website
    *   **AI Kevin** follow up on his website proposals

Vacation, away
--------------

*   DaveM vacation June 16 - 20
*   DaveD in July -- **AI Martin** finish and test the new Build scripts on dsdp.eclipse.org till then
*   MartinO vacation June 11 - 22

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_26-Mar-2008#Action_Items "DSDP/TM/Committer Phone Meeting 26-Mar-2008") Action Items
*   **Everyone**: Review API patches as announced on mailing list, vote +1 on the bug
*   **Rupen**:
*   **DaveD**: Finish profile import/export; Update [bug 221211](https://bugs.eclipse.org/bugs/show_bug.cgi?id=221211) IFileService multi-commands Javadoc
*   **DaveM**: contact IBM teams for [bug 218685](https://bugs.eclipse.org/bugs/show_bug.cgi?id=218685) SSH timeout, [bug 220379](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220379) DStoreFileService API; add Javadoc on Thursday for [bug 216252](https://bugs.eclipse.org/bugs/show_bug.cgi?id=216252) SystemMessages message ID; create a new "Future" bug for dstore protocol handshake, cloned from [bug 220892](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220892)
*   **Xuan**: [bug 221138](https://bugs.eclipse.org/bugs/show_bug.cgi?id=221138) move SystemSelectRemoteFileOrFolderDialog and related to internal; Use Kevin's Properties for Unit Tests
*   **Kevin**: Website Updates
*   **Martin**: Add API patches; New Project Plan; Ganymede Rampdown Plan; Commons Net Placeholder CQ; UI/Non-UI Splitting; finish new releng; Look at PropertyDescriptor issues; unit tests
*   **Javier**: add unit tests; document the Symbian internal test setup similar to [CVS](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204138#c20) \-\- see also [CVS_Development#Testing](https://wiki.eclipse.org/CVS_Development#Testing "CVS Development")
*   **Michael**: Terminal improvements

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 16-Apr-2008](./Committer_Phone_Meeting_16-Apr-2008 "DSDP/TM/Committer Phone Meeting 16-Apr-2008") (2 weeks) at [1500 UTC / 0800 SFO / 1000 Rochester / 1100 Toronto / 1600 London / 1700 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=4&day=16&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Next [BugDay/April_2008](https://wiki.eclipse.org/BugDay/April_2008 "BugDay/April 2008") on Apr 25
*   Monthly [DSDP/TM/Phone Meeting 7-May-2008](./Phone_Meeting_7-May-2008 "DSDP/TM/Phone Meeting 7-May-2008") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=5&day=7&year=2008&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_9-Apr-2008](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_9-Apr-2008))