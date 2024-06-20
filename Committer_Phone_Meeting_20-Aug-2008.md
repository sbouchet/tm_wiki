

DSDP/TM/Committer Phone Meeting 20-Aug-2008
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday August 20, 2008 at [1600 UTC / 0900 SFO / 1100 Rochester / 1200 Toronto / 1800 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=8&day=20&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)   ![Html.gif](./images/Html.gif)[HTML](http://www.google.com/calendar/embed?src=vn70im36r00qeusu8nme50cils@group.calendar.google.com&ctz=Canada/Toronto) \| ![Ical.gif](./images/Ical.gif)[iCal](http://www.google.com/calendar/ical/vn70im36r00qeusu8nme50cils@group.calendar.google.com/public/basic.ics) |
| Dial-in: | Martin to call everybody by Skype |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kevin.j.doyle, xuan.chen886, eugenetarassov, michael\_scharf, uwe.stieber, radoslav.gerganov, wrsfburton.  

Contents
--------

*   [1 Invited Attendees](#Invited-Attendees)
*   [2 Attendees](#Attendees)
*   [3 Agenda](#Agenda)
    *   [3.1 **Status**](#Status)
    *   [3.2 **Bugs**](#Bugs)
    *   [3.3 **Old Stuff**](#Old-Stuff)
    *   [3.4 Cleanup Work](#Cleanup-Work)
    *   [3.5 Questions](#Questions)
*   [4 Vacation, away](#Vacation.2C-away)
*   [5 Action Items](#Action-Items)
*   [6 Next Meeting](#Next-Meeting)

Invited Attendees
-----------------

*   IBM - Xuan Chen, Dave McKnight, Dave Dykstal, Kevin Doyle
*   Wind River - Martin Oberhuber, Michael Scharf, Uwe Stieber, Eugene Tarassov, Felix Burton
*   ProSyst - Radoslav Gerganov
*   MontaVista - Anna Dushistova

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Attendees
---------

*   Attendees:
*   Regrets: Martin, Xuan, Michael, Uwe (vacation)

Agenda
------

*   Last meeting: [DSDP/TM/Phone Meeting 6-Aug-2008](./Phone_Meeting_6-Aug-2008 "DSDP/TM/Phone Meeting 6-Aug-2008")
*   Prev meeting: [DSDP/TM/Committer Phone Meeting 16-Jul-2008](./Committer_Phone_Meeting_16-Jul-2008 "DSDP/TM/Committer Phone Meeting 16-Jul-2008")
*   **Skype Call Quality**

### **Status**

*   Shooting for 3.0.1 final run this week, will branch off on Aug 26 as per [DSDP/TM/3.0 Ramp down Plan for Ganymede#Ramp down for Ganymede SR1 (Sep 24, 2008)](./3.0_Ramp_down_Plan_for_Ganymede#Ramp_down_for_Ganymede_SR1_.28Sep_24.2C_2008.29 "DSDP/TM/3.0 Ramp down Plan for Ganymede"), see also [#Bugs](#Bugs) below.
    *   **Please get anything risky and hi-priority in this week!**
*   **Anna**: Now also contributing to TCF. Working on 3.0.1 bugs.
    *   [bug 244637](https://bugs.eclipse.org/bugs/show_bug.cgi?id=244637) Do we have any way to get absolute path without using IRemoteFile?
*   **DaveD**:
*   **DaveM**: EFS planning for 3.1, lower priority?
*   **Kevin**:
*   **Xuan**:
*   **Martin**:
    *   New builder - need to defer until 3.1M2
    *   Website revamp - image from the Community is good, need some time to revamp the contents
    *   [bug 227750](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227750) IRSEInteractionProvider would prefer fix in 3.1 HEAD after branching, do we need it in 3.0.1?
    *   DSDP Board Presentation - Project input is now on [DSDP/TML/BoardReport2008](https://wiki.eclipse.org/DSDP/TML/BoardReport2008 "DSDP/TML/BoardReport2008") and [DSDP/MTJ/BoardReport2008](https://wiki.eclipse.org/DSDP/MTJ/BoardReport2008 "DSDP/MTJ/BoardReport2008"). Follow the [PMC mailinglist](http://dev.eclipse.org/mhonarc/lists/dsdp-pmc/maillist.html) for updates, and see [DSDP/PMC](https://wiki.eclipse.org/DSDP/PMC "DSDP/PMC") \-\- deadline for input is end August, presentation will be Sep 17.
    *   [bug 234026](https://bugs.eclipse.org/bugs/show_bug.cgi?id=234026) \[apidoc\] IFileService#createFolder() does not specify whether parent folders are created -- fixed: on the Service level, Services **may** create parent folders, on the Subsystem level I fixed IFileServiceSubSystem#createFolders() to do it automatically if the service doesn't do it. Question: should IFileServiceSubSystem#createFolder() throw exception if the parent is missing, is it worth the extra effort?
    *   [bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176) \- Rado's SWT deferred DND not yet reviewed, see also [DSDP/TM/Phone Meeting 2-Jul-2008](./Phone_Meeting_2-Jul-2008 "DSDP/TM/Phone Meeting 2-Jul-2008") notes

### **Bugs**

*   54 bugs still assigned 3.0 - **AI Everyone** **must review your assigned bugs** and move to 3.0.1 / 3.1 as appropriate
*   [Open 3.0 Assigned](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&target_milestone=3.0+M5&target_milestone=3.0+M6&target_milestone=3.0+M7&target_milestone=3.0+RC1&target_milestone=3.0+RC2&target_milestone=3.0+RC3&target_milestone=3.0+RC4&target_milestone=3.0+RC5&target_milestone=3.0&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) bugs
*   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [Hi-Priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)
*   Current Statistics: 45 hi-pri bugs: 1 critical (Martin), 11 major (4x DaveD, 4x Martin, DaveM, Inbox), 33 other P2's -- **mostly DaveD, assigned 3.0.1!**
*   Community contributions: 38 [Open bugs with patches](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1) right now, should apply after the 3.0.1 final run (see also the [Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for a query)

### **Old Stuff**

*   [bug 240991](https://bugs.eclipse.org/bugs/show_bug.cgi?id=240991) Startup creates Display on Worker Thread
    *   Workarounds seem to be good for now. Martin would prefer experimenting with IRSEPersistenceProvider in HEAD after the branch is created, to avoid destabilizing the branch. Can we release 3.0.1 without the IRSEPersistenceProvider fix?

*   Unittests
    *   Xuan: Kevin trying some Abbot stuff, might contribute -- Abbot is under CPL
    *   [bug 230917](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230917) \[regression\] Some DStore Archive Testcases fail -- **AI Xuan** look at

*   Findbugs and other cleanup
    *   Broken Links in Docs: Xenu's LinkSleuth

*   **Quality, Backlog and Unit Tests**
    *   Remember our 2-fix-per-week / 3 unittests-per-milestone plan
    *   Current situation is on [this bugzilla report](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=&y_axis_field=assigned_to&z_axis_field=&query_format=report-table&classification=DSDP&product=Target+Management&bug_status=RESOLVED&bug_status=VERIFIED&bug_status=CLOSED&chfieldfrom=2007-09-17&chfieldto=Now&chfield=bug_status&chfieldvalue=RESOLVED&format=table&action=wrap&negate0=1&field0-0-0=resolution&type0-0-0=equals&value0-0-0=DUPLICATE)

### Cleanup Work

*   Anything we want to do for 3.0.1 ?
    *   Unittests, unittests, unittests! -- ideally write an accompanying unittest for every bugfix
    *   Migration Notes (for 2.0 / for 1.0?)
    *   Review and improve Userdocs; we have several open bugs here
    *   Review and improve Javadocs; lots still missing, unclear, duplicated
    *   Fix broken hyperlinks in the docs, fix HTML/XML errors (which can make the indexer not work)
    *   Get rid of compiler warnings wherever possible
    *   Run Findbugs -- Update site on [http://findbugs.cs.umd.edu/eclipse](http://findbugs.cs.umd.edu/eclipse), Quickdocs by Rado in [tm-dev E-Mail](http://dev.eclipse.org/mhonarc/lists/dsdp-tm-dev/msg01869.html)
        *   Question about filtering false positives posted on fb-discuss [link](https://mailman.cs.umd.edu/pipermail/findbugs-discuss/2008-May/002374.html)
*   Stuff for 3.1
    *   API Tooling Javadocs(@noextend and friends) - cannot limit existing API more than it was before, unless it was textually documented already, but can deprecate stuff, even in 3.0.1.

### Questions

Vacation, away
--------------

*   Michael vacation Aug 18-Sep 1
*   Xuan vacation Aug 18-26
*   Martin vacation Aug 20/21

Action Items
------------

*   [Last Meeting](#Notes) Action Items
*   **Everyone**: **old** triage 3.0 assigned bugs; discuss [3.1 project plan](https://www.eclipse.org/projects/project-plan.php?projectid=dsdp.tm) with Project Teams, consider staffing or removing themes; attach "plan" keyword to "interesting" bugs for 3.1
*   **Anna**:
*   **DaveD**:
*   **DaveM**: **old** comment on EFS in project plan; [bug 234045](https://bugs.eclipse.org/bugs/show_bug.cgi?id=234045) handling errors in File Property Page; [bug 199596](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199596) Read-Only attribute doesn't always update IRemoteFile;
*   **Kevin**:
*   **Xuan**: **old** check deadline for PMC Board Presentation review; Look at [bug 230917](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230917) Archive Handler Unittests
*   **Martin**: **old** [bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176) review Rado's deferred D&D; [bug 238574](https://bugs.eclipse.org/bugs/show_bug.cgi?id=238574) Website revamp; new Builder **until 3.1M2**; [bug 227750](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227750) Display in non-UI write fix **until mid August**; Run performance tests for [bug 236065](https://bugs.eclipse.org/bugs/show_bug.cgi?id=236065) IFileService improvements; Critical EFS bugs;
*   **Javier**: **old** Hi-PRI FTP BUGS
*   **Michael**: **old** Terminal: Work on [bug 185348](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185348) Terminal API
*   **Uwe**: -
*   **Rado**: -
*   **Felix**: -
*   **Eugene**: -

Next Meeting
------------

*   Monthly [DSDP/TM/Phone Meeting 3-Sep-2008](./Phone_Meeting_3-Sep-2008 "DSDP/TM/Phone Meeting 3-Sep-2008") (2 weeks) at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=8&day=6&year=2008&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Committer Phone Meeting 17-Sep-2008](./Committer_Phone_Meeting_17-Sep-2008 "DSDP/TM/Committer Phone Meeting 17-Sep-2008") (4 weeks) at [1500 UTC / 0800 SFO / 1000 Rochester / 1100 Toronto / 1700 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=8&day=20&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_20-Aug-2008](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_20-Aug-2008))