

DSDP/TM/Committer Phone Meeting 6-Feb-2008
==========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Feb 6, 2007](./index.php?title=Feb_6,_2007&action=edit&redlink=1 "Feb 6, 2007 (page does not exist)") at [1600 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=2&day=6&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | Martin to call everybody by Skype |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, kevin.j.doyle, xuan.chen886, rupen.mardirossian, javier.montalvoorus, eugenetarassov, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 Current Work](#Current-Work)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Xuan Chen, Dave McKnight, Kevin Doyle, Dave Dykstal, Rupen Mardirossian
*   Wind River - Martin Oberhuber, Uwe Stieber, Eugene Tarassov
*   Symbian - Javier Montalvo Orus

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 23-Jan-2008](./DSDP/TM/Committer_Phone_Meeting_23-Jan-2008 "DSDP/TM/Committer Phone Meeting 23-Jan-2008")

### Current Work

*   **Skype Call Quality**
    *   Excellent even with 9 participants (8 + organizer). This is the Maximum that Skype supports, so we could meet on Skype only because Michael had another appointment.
*   **M5 upcoming** \- Test and endgame plan?
    *   Want M5 finished by Friday Feb 15 --> Risky checkins to be complete by Friday Feb 8 --> Test run on Tuesday Feb 12
    *   **First PII drop on Feb 25th, Deadline until end of M6**; try to minimize any wholesale changes after Feb.25th
    *   PII Changes for UI/Non-UI Splitting e.g. [bug 190231](https://bugs.eclipse.org/bugs/show_bug.cgi?id=190231) SubSystem, [bug 211067](https://bugs.eclipse.org/bugs/show_bug.cgi?id=211067) SystemMessages in Services
    *   **[3.0 M5 assigned open bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&target_milestone=3.0+M5&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit)**
        *   SystemMessages UI/Core separation - **AI DaveM to investigate**
            *   DaveD prefer to have standard NLS strings only
*   **[TM 2.0.3](./TM_2.0_Ramp_down_Plan_for_Europa#Ramp_down_for_Europa_SR2_.2829-Feb-2007.29 "TM 2.0 Ramp down Plan for Europa")** upcoming Feb.29 -- [2.0.3 assigned bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&target_milestone=2.0.3&cmdtype=doit), any else?
    *   **AI All** file 'backport' bugs for 2.0.3 until end of this week
*   Eugene new committer
    *   Martin wants TCF to be discussed more in the Open. Currently mostly Wind River engagement, but more to come (Power.org; ECSI Debug Standards Workshop).
    *   TCF is mostly separate from RSE technology. **AI Martin** create separate Bugzilla component for TCF.
*   Can we commit to support Java 6 (just runtime)?
    *   YES. Develop against Java 1.4 and test against Java 6. Main topic is incorporation of scripting. Eclipse Debugger supports finding references of objects.
*   TM Website
    *   [bug 216197](https://bugs.eclipse.org/bugs/show_bug.cgi?id=216197) Bugs link on the side nav bar is broken by that latest changes
    *   Kevin: Discussions fine so far, not touched the code yet?
    *   Martin: Would like to get more dynamic information onto the homepage in an automated manner e.g. automated release notes with milestones. Avoid merging errors if starting work end this week.
*   Bug Fixing - **Remember our 2-fix-per-week / 3 unittests-per-milestone plan**
    *   Since our [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./DSDP/TM/Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007") it's now 20 weeks / 4 milestones, so each committer is due 40 fixes / 8 unittests
    *   Current situation is on [this bugzilla report](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=&y_axis_field=assigned_to&z_axis_field=&query_format=report-table&classification=DSDP&product=Target+Management&bug_status=RESOLVED&bug_status=VERIFIED&bug_status=CLOSED&chfieldfrom=2007-09-17&chfieldto=Now&chfield=bug_status&chfieldvalue=RESOLVED&format=table&action=wrap&negate0=1&field0-0-0=resolution&type0-0-0=equals&value0-0-0=DUPLICATE)
    *   Unittests: Xuan, DaveM, Javier added some; Martin 0; not sure about others; Martin working on Releng scripts next
*   Next [BugDay/February_2008](./BugDay/February_2008 "BugDay/February 2008") on Feb 29
*   **Javier** busy until end of Feb; no time for Eclipse currently
*   **DaveD's** lazy init done. [bug 217556](https://bugs.eclipse.org/bugs/show_bug.cgi?id=217556) ServiceSubSystem
    *   What if a subsystem does not have a service layer? - Return null for getServiceType()
    *   Existing code that checks whether something has a service needs to be changed: **AI DaveD** Find references to IServiceSubSystem
    *   [bug 217894](https://bugs.eclipse.org/bugs/show_bug.cgi?id=217894) Subsystem Configuration Families - subsystem category would be orthogonal to subsystem family -- family would be related to connector service -- **AI All** comment on the bug
    *   Import/export connections rather than profiles - extend the persistence provider for import/export. Use a profile that only contains those things relevant to the exported elements, and merge it on import (or instantiate + copy).
        *   Uwe: Contributors may have their own format for import/export already
        *   This is maybe related to [bug 160403](https://bugs.eclipse.org/bugs/show_bug.cgi?id=160403) Filters should be connection-private by default
*   **DaveM:** -
    *   [bug 212742](https://bugs.eclipse.org/bugs/show_bug.cgi?id=212742) Util for sending commands and receiving output without echo
        *   Martin would like to see with M5 for EclipseCon tutorial; but it seems to work OK with SSH and dstore? **AI Martin review the bug**
    *   [bug 216252](https://bugs.eclipse.org/bugs/show_bug.cgi?id=216252), [bug 190231](https://bugs.eclipse.org/bugs/show_bug.cgi?id=190231) and [bug 211067](https://bugs.eclipse.org/bugs/show_bug.cgi?id=211067) split resource strings and systemMessages into UI and Core - would like to get NLS refactorings done for the PII drop on Feb 25
    *   EFS and encodings - No response from platform or TPF teams
    *   (TPF) product teams extended SystemView in the past, no response from them
*   **Kevin:** -
*   **Xuan:** \- Need to add plugin org.eclipse.rse.useractions into build. Needed by IBM (after M5)
    *   Martin: will need to be a separate downloadable component.
*   **Martin:** \- Need to put Project Plan on the Web; Update Releng scripts to automatically run unit tests at night
*   **Uwe:** -
*   **Rupen:** \- [bug 210682](https://bugs.eclipse.org/bugs/show_bug.cgi?id=210682) \- Multi-file conflict resolution on Copy - dialog ready, jpeg posted on the bug
    *   Want to get current state (functional dialog) committed and treat changes via separate bugs. Issues with cross-subsystem copies
*   **Michael:** -
*   **Questions**

*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   DaveD on vacation Feb 18-21
*   Feb.18 is Family Day in Ontario

Action Items
------------

*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_23-Jan-2008#Action_Items "DSDP/TM/Committer Phone Meeting 23-Jan-2008") Action Items
*   **Everyone**: consider fixes for 2.0.3 backport until end of this week; comment on [bug 217894](https://bugs.eclipse.org/bugs/show_bug.cgi?id=217894) by DaveD
*   **DaveD**: Find references to IServiceSubSystem, review refactoring
*   **DaveM**: Investigate [bug 190231](https://bugs.eclipse.org/bugs/show_bug.cgi?id=190231), [bug 211067](https://bugs.eclipse.org/bugs/show_bug.cgi?id=211067) SystemMessages UI/Core Separation
*   **Xuan**:
*   **Kevin**: webpage redesign (next week)
*   **Martin**: Review [bug 212742](https://bugs.eclipse.org/bugs/show_bug.cgi?id=212742) util for commands+results; TCF Bugzilla Component; New RSE Releng + unit tests; Write-up TM 3.0 Plan; Look at PropertyDescriptor issues;
*   **Javier**: fixes, unit tests; document the Symbian internal test setup similar to [CVS](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204138#c20) \-\- see also [CVS_Development#Testing](./CVS_Development#Testing "CVS Development")
*   **Michael**: Terminal improvements

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 20-Feb-2008](./DSDP/TM/Committer_Phone_Meeting_20-Feb-2008 "DSDP/TM/Committer Phone Meeting 20-Feb-2008") (2 weeks) at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=2&day=20&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 5-Mar-2008](./DSDP/TM/Phone_Meeting_5-Mar-2008 "DSDP/TM/Phone Meeting 5-Mar-2008") at [9am PST / 1700 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=3&day=5&year=2008&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_6-Feb-2008](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_6-Feb-2008))