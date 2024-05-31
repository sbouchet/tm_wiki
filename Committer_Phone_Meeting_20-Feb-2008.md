

DSDP/TM/Committer Phone Meeting 20-Feb-2008
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Feb 20, 2008](./index.php?title=Feb_20,_2008&action=edit&redlink=1 "Feb 20, 2008 (page does not exist)") at [1600 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=2&day=20&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
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

*   IBM - Xuan Chen, Dave McKnight
*   Wind River - Martin Oberhuber, Uwe Stieber, Michael Scharf
*   Symbian - Javier Montalvo Orus

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 6-Feb-2008](./DSDP/TM/Committer_Phone_Meeting_6-Feb-2008 "DSDP/TM/Committer Phone Meeting 6-Feb-2008")

### Current Work

*   **Skype Call Quality** \- excellent, no probs
*   **M5 retrospective**
    *   First bugs found thanks to Unit tests (Yeah!): TAR archive handling
    *   [bug 219086](https://bugs.eclipse.org/bugs/show_bug.cgi?id=219086) fixed in unit tests: Flush event loop in tearDown -- leads to other bugs in HostMoveTest, [bug 219101](https://bugs.eclipse.org/bugs/show_bug.cgi?id=219101)
    *   Late-breaking [bug 219260](https://bugs.eclipse.org/bugs/show_bug.cgi?id=219260) :-(
    *   Need all unit tests enabled in nightly builds - need to use Uwe's Connection Property classes, see **FTPFileSubsystemTestCase** \- **AI Xuan, DaveM, Kevin** Use Properties for unit tests
*   **Next Steps**
    *   **First PII drop on Feb 25th, Deadline until end of M6**; try to minimize any wholesale changes after Feb.25th
    *   PII Changes for UI/Non-UI Splitting e.g. [bug 190231](https://bugs.eclipse.org/bugs/show_bug.cgi?id=190231) SubSystem, [bug 211067](https://bugs.eclipse.org/bugs/show_bug.cgi?id=211067) SystemMessages in Services, [bug 216252](https://bugs.eclipse.org/bugs/show_bug.cgi?id=216252) SystemMessages refactoring - **AI Everyone** Review [bug 216252](https://bugs.eclipse.org/bugs/show_bug.cgi?id=216252)
        *   Xuan will be running checkpii tool
    *   **Hi-pri-bugs; apply patches**
        *   Community Contributions from **Radoslav Gerganov**, **Johnson Ma** (tgz handler)
    *   **[TM 2.0.3](./TM_2.0_Ramp_down_Plan_for_Europa#Ramp_down_for_Europa_SR2_.2829-Feb-2007.29 "TM 2.0 Ramp down Plan for Europa")** upcoming Feb.29 -- [2.0.3 assigned bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&target_milestone=2.0.3&cmdtype=doit)
*   **Planning** \- **AI Martin** to write up what we discussed in Toronto
    *   Think about assigning bugs to target milestones. What goes into 3.0 and what not?
*   TM Website
    *   Martin added [searchcvs](http://dsdp.eclipse.org/dsdp/tm/searchcvs.php?q=&project=0), [relnotes](http://dsdp.eclipse.org/dsdp/tm/news/relnotes.php?project=rse&version=HEAD), [RSS-Feed](http://dsdp.eclipse.org/dsdp/tm/feeds/builds-rse.xml) (manually created for now); required changing the left-bar-menu into hardcoded items
    *   dsdp.eclipse.org now also holds the website (build.eclipse.org will do soon) in order to support auto-builds, relnotes, searchcvs
    *   Martin incorporated some of Kevin's suggestions (new "Bugs" link; left-menu)
*   Bug Fixing - **Remember our 2-fix-per-week / 3 unittests-per-milestone plan**
    *   Since our [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./DSDP/TM/Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007") it's now 22 weeks / 4 milestones, so each committer is due 44 fixes / 8 unittests
    *   Current situation is on [this bugzilla report](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=&y_axis_field=assigned_to&z_axis_field=&query_format=report-table&classification=DSDP&product=Target+Management&bug_status=RESOLVED&bug_status=VERIFIED&bug_status=CLOSED&chfieldfrom=2007-09-17&chfieldto=Now&chfield=bug_status&chfieldvalue=RESOLVED&format=table&action=wrap&negate0=1&field0-0-0=resolution&type0-0-0=equals&value0-0-0=DUPLICATE)
    *   Unittests: when adding a test, please add the tag **//-test-author:YourName** in front of it
        *   DaveM - 5
        *   DaveD - 21
        *   KevinD - 11
        *   MartinO - 3
        *   TobiasS - 3
        *   UweS - 7
        *   XuanC - 51
        *   **Total - 101**
        *   Javier - 0
*   **Javier** busy until end of Feb; no time for Eclipse currently
*   **DaveD's** \- n/a today
*   **DaveM:** -
    *   [bug 216252](https://bugs.eclipse.org/bugs/show_bug.cgi?id=216252) SystemMessages refactoring
    *   EFS and encodings - No response from platform or TPF teams
    *   (TPF) product teams extended SystemView in the past, no response from them
*   **Kevin:** \- n/a today
*   **Xuan:** \- Need to add plugin org.eclipse.rse.useractions into build. Needed by IBM (after M5) - **AI Martin** want a separate download
    *   [bug 185554](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185554) dynamic menus
    *   Will mostly be busy with IBM / Migration work
    *   NL Testing: want to be finished by March 21, how much work? - Martin: Try SearchCVS: It knows all files in CVS, all commits, all dates etc in a database
*   **Martin:** \- Need to put Project Plan on the Web; Update Releng scripts to automatically run unit tests at night
    *   Searchcvs, Relnotes done; Little more work needed on web-build and promote.sh
    *   Next tasks - TM 2.0.3; Move SubsystemConfiguration implementation into non-UI; Lazy loading of SubsystemConfiguration (use the Proxy more); Lazy loading of UI adapters
    *   [bug 218947](https://bugs.eclipse.org/bugs/show_bug.cgi?id=218947) **IRemotePath** idea
        *   DaveM: Could we use IHostFile instead of IRemotePath? - Martin: Looks like IHostPath only exists when connected
        *   Xuan: API changes are problematic - Migration will start in 1 month
            *   API Freeze by M6 - would that also mean we cannot add classes, methods? - Martin: dont need to be super strict.
            *   Martin: Migration could be stepwise, if we are able to convert String into IRemotePath and vice versa
        *   DaveM: Naming convention -- IHostPath instead of IRemotePath since located in the Service?
*   **Uwe:** \- Won't have much time for Open Source
*   **Rupen:** \- n/a today
*   **Michael:** \- nothing new
*   **Questions**

*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   DaveD on vacation Feb 18-21

Action Items
------------

*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_6-Feb-2008#Action_Items "DSDP/TM/Committer Phone Meeting 6-Feb-2008") Action Items
*   **Everyone**: Review [bug 216252](https://bugs.eclipse.org/bugs/show_bug.cgi?id=216252) SystemMessages refactoring
*   **DaveD**: Fix [bug 219101](https://bugs.eclipse.org/bugs/show_bug.cgi?id=219101) HostMoveTest
*   **DaveM**: Use Properties for Unit Tests
*   **Xuan**: Use Properties for Unit Tests
*   **Kevin**: Use Properties for Unit Tests; Website Updates
*   **Martin**: Add UserActions to build/downloads; finish new releng; Write-up TM 3.0 Plan; Look at PropertyDescriptor issues; unit tests; Newsgroup
*   **Javier**: add unit tests; document the Symbian internal test setup similar to [CVS](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204138#c20) \-\- see also [CVS_Development#Testing](./CVS_Development#Testing "CVS Development")
*   **Michael**: Terminal improvements

Next Meeting
------------

*   Next [BugDay/February_2008](./BugDay/February_2008 "BugDay/February 2008") on Feb 29
*   EclipseCon March 17-20: Martin, Michael - no other committers
*   [DSDP/TM/Committer Phone Meeting 5-Mar-2008](./DSDP/TM/Committer_Phone_Meeting_5-Mar-2008 "DSDP/TM/Committer Phone Meeting 5-Mar-2008") (2 weeks) at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=3&day=5&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 5-Mar-2008](./DSDP/TM/Phone_Meeting_5-Mar-2008 "DSDP/TM/Phone Meeting 5-Mar-2008") at [9am PST / 1700 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=3&day=5&year=2008&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_20-Feb-2008](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_20-Feb-2008))