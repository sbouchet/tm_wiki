

DSDP/TM/Committer Phone Meeting 28-May-2008
===========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [May 28, 2008](/index.php?title=May_28,_2008&action=edit&redlink=1 "May 28, 2008 (page does not exist)") at [1500 UTC / 0800 SFO / 1000 Rochester / 1100 Toronto / 1600 London / 1700 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=5&day=28&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | SkypeOut: +99008275601400 (free!) - powered by [Highspeedconferencing.com](http://share.highspeedconferencing.com/skype_new/signin.jsp) |

Backup1: Martin to call everybody by Skype  
Backup2 dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kevin.j.doyle, xuan.chen886, rupen.mardirossian, javier.montalvoorus, eugenetarassov, michael\_scharf, uwe.stieber, radoslav.gerganov, wrsfburton.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 **New Stuff**](#New-Stuff)
    *   [2.2 **Steps Towards Ganymede**](#Steps-Towards-Ganymede)
    *   [2.3 What will happen after Ganymede?](#What-will-happen-after-Ganymede.3F)
*   [3 Vacation, away](#Vacation.2C-away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Xuan Chen, Dave McKnight, Dave Dykstal, Kevin Doyle
*   Wind River - Martin Oberhuber, Michael Scharf
*   ProSyst - Radoslav Gerganov
*   **Regrets:** Uwe, Eugene, Felix, Javier, Rupen

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 21-May-2008](/DSDP/TM/Committer_Phone_Meeting_21-May-2008 "DSDP/TM/Committer Phone Meeting 21-May-2008")
*   **Skype Call Quality**
    *   [Highspeedconferencing.com](http://share.highspeedconferencing.com/skype_new/signin.jsp) \-\- 7 participants: speaker hard to understand at times; much background noise for Michael; bad for Rado, but bearable
    *   Looks like non-speakers are totally muted, system needs some time to adapt when somebody starts talking
    *   Will use normal direct Skype again next week, but can use HSCNF as fallback if there are more than 8 participants.

### **New Stuff**

*   [Release Review](https://www.eclipse.org/projects/whatsnew.php) next Wed June 4 at [8am PST](http://www.timeanddate.com/worldclock/fixedtime.html?month=6&day=4&year=2008&hour=15&min=00&sec=0&p1=0) (our usual committer meeting time)
    *   Want to move next committer meeting to [Thursday Jun 5](/DSDP/TM/Committer_Phone_Meeting_5-Jun-2008 "DSDP/TM/Committer Phone Meeting 5-Jun-2008") at 8am PST (same time), ok? Or do it after/at our [Monthly Meeting Jun4](/DSDP/TM/Phone_Meeting_4-Jun-2008 "DSDP/TM/Phone Meeting 4-Jun-2008") at 9am PST?
    *   Our slides: Minideck ([PPT](http://download.eclipse.org/dsdp/tm/presentations/TM_3.0_Release_Review_Minideck.ppt) | [PDF](http://download.eclipse.org/dsdp/tm/presentations/TM_3.0_Release_Review_Minideck.pdf), All slides ([PPT](http://download.eclipse.org/dsdp/tm/presentations/TM_3.0_Release_Review.ppt) | [PDF](http://download.eclipse.org/dsdp/tm/presentations/TM_3.0_Release_Review.pdf))
    *   Full [Ganymede Slides](https://www.eclipse.org/projects/slides/Ganymede_04June2008.zip) \- We are #22ff on the Overview deck, alphabetically pretty soon
    *   For our project: Community looks very healthy; Code and API additions look very good, healthy in terms of size; Bug backlog is a problem; Multiple APIs, disconnect of "Remote Development Tools" initiative

*   **Project Plan**: [Development Resources/Project Plan](/Development_Resources/Project_Plan "Development Resources/Project Plan") Status
    *   Ours is XML now, on [https://www.eclipse.org/dsdp/tm/development/tm\_plan\_3_0.xml](https://www.eclipse.org/dsdp/tm/development/tm_plan_3_0.xml) \-\- also in your www-tm-development project
    *   Bjorn's tooling [renders it to PHP](https://www.eclipse.org/projects/project-plan.php?projectid=dsdp.tm) \- bottom has a [link for raw XML](https://www.eclipse.org/projects/project-plan.php?projectid=dsdp.tm&raw=1)
    *   Everybody can edit the plan at any time to fix typos etc
    *   Target Operating Environments (Reference Platforms):
        *   Get rid of Win2K, Ubuntu
        *   Mark Mac "Secondary" Platform; up to Java 1.5; not allow deliberate regressions!
    *   Automated bug queries in Project Plan
        *   Use bugzilla "plan" keyword plus "Other related bugs..." hyperlink in a paragraph after the bug list
    *   **AI Martin** update the project plan as discussed

*   Ganymede Promotions
    *   Will do a 15-minute Screencast of TM for EMO Marketing - Ideas for things to show?
        *   Creating Connections, Filters, Drag&Drop, ...
        *   Useractions: Should work for users
    *   Listing New&Noteworthy for ZX
    *   [BugDay/May 2008](/BugDay/May_2008 "BugDay/May 2008") on May 30, who will be on IRC?

*   Late API Changes / Additions
    *   Must decide how we want to handle Apidoc bugs
    *   **Take the time now** to review and improve unclear API descriptions
    *   [All open API](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&order=Assignee) bugs
    *   [bug 234215](https://bugs.eclipse.org/bugs/show_bug.cgi?id=234215) [bug 234030](https://bugs.eclipse.org/bugs/show_bug.cgi?id=234030): AbstractSystemViewElementAdapter#doDelete*(): Treat Exception same as SystemMessageException? Treat "cancelled" same as Exception? -- **AI DaveD** take [bug 234215](https://bugs.eclipse.org/bugs/show_bug.cgi?id=234215) and talk to DaveM about [bug 234030](https://bugs.eclipse.org/bugs/show_bug.cgi?id=234030) \- Probably write a Unittest
        *   **Strive for documentation in one place**, typically the interface; Get rid of docs from implementations completely, or use {@inheritDoc}
        *   Especially now during endgame we shouldn't change the codebase so much, but invest heavily in cleaning up API Docs to clarify expected semantics -- basically reengineer current code to come up with textual description of expected semantics. A very good investment in the future (less work on future bug fixes).
        *   For current production code, it's now OK to keep existing behavior (only refactor), even if it looks suspicious. Keep logic but mark with TODO or FIXME what's suspicious and update the Docs to have clear description of expected behavior (even if current behavior is not 100% what's expected -- file a bug in such a case to address this in the future!
        *   Working pro-actively on Documentation helps avoiding support issues! Don't sit idle before 3.0 just because we cannot change the codebase so much. Focus on testing, Unittests, Documentation, FAQs, ...
        *   Unittests, cleanup, ... (see also below)
        *   DaveD will have time; DaveM, Xuan on and off
    *   [bug 165171](https://bugs.eclipse.org/bugs/show_bug.cgi?id=165171) Should the File Permissions Property Page be extendable? Close bug, file a new one?
        *   DaveM: Currently not extendable / exchangeable; **AI Martin** file a new bug for open questions, close current one
    *   [bug 190231](https://bugs.eclipse.org/bugs/show_bug.cgi?id=190231) Subsystem UI->non-UI: Go for it? Have it in 3.0 or 3.1 but not in 3.0.1. DaveD: Go, DaveM: Too risky, defer to 3.1
    *   [bug 230298](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230298) (api)(breaking) ISystemPropertyConstants should not extend IBasicPropertyConstants -- Already fixed, **AI Martin** mark bug fixed
    *   [bug 185348](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185348), [bug 204796](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204796) Terminal non-API **Michael to try**
    *   [bug 233480](https://bugs.eclipse.org/bugs/show_bug.cgi?id=233480), UI Change for ServerLauncher -- suggest proposing a newConnectionWizard (bound to systemType) -- see Discovery

  

### **Steps Towards Ganymede**

*   [DSDP/TM/3.0 Ramp down Plan for Ganymede](/DSDP/TM/3.0_Ramp_down_Plan_for_Ganymede "DSDP/TM/3.0 Ramp down Plan for Ganymede")
    *   We have RC2, so from now on EVERY checkin must get a +1 by a reviewer BEFORE (except emergencies, documentation-only or unittest-only things). Also applies to "incubation". Rules do not apply to TCF
    *   Please do NOT only ask me for reviewing, it doesn't scale

*   [TM 3.0 RC2 Testing](/TM_3.0_RC2_Testing "TM 3.0 RC2 Testing") Status
    *   Committers step up with good example to draw community members to it!
    *   Somebody must test our integration with the JEE EPP Package
    *   Every committer to invest 2 hours minimum in testing; Hi-pri fixes OK, martin will releng to update site so testers can update easily;

*   **Bug Triage**
    *   **AI Everyone** **must review your assigned bugs** and move to 3.0.1 where possible
    *   All "3.0" assigned bugs must be triaged now and either assigned a proper RC milestone or 3.0.1 (with the exception of Documentation-only fixes)
    *   Work on remaining ones by priority
    *   [Open RC2 Assigned](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&target_milestone=3.0+M5&target_milestone=3.0+M6&target_milestone=3.0+M7&target_milestone=3.0+RC1&target_milestone=3.0+RC2&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) bugs, [open 3.0 Assigned](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&target_milestone=3.0+RC2&target_milestone=3.0+RC3&target_milestone=3.0+RC4&target_milestone=3.0&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) bugs
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [Hi-Priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)
    *   Current Statistics: 1 blocker (Martin), 1 critical (Martin), 8 major (DaveD, Kevin, Martin, Michael), 23 other P2's -- was 10 major / 20 P2's last week
    *   Community contributions: Only few [unapplied patches](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1) right now, last chance to apply now before 3.0 (see also the [Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for a query)

*   Martin's new Build System for Dave
    *   In the works

*   **New and Noteworthy**
    *   I'll need a list of new features for a New&Noteworthy, and for the Release Review. Release Review material is due next week.
    *   See [CDT/User/NewIn50](/CDT/User/NewIn50 "CDT/User/NewIn50") for example; for TM, I put most news into our Build Notes already, so it should be possible to compile the N&N out of the build notes
    *   For the N&N, please make screenshots and work on "your" new features, e.g.
        *   Useractions

*   **Cleanup Work**
    *   Besides the hi-priority issues, there is a LOT of cleanup to do. What do we consider must-have's?
        *   Unittests, unittests, unittests!
        *   **New releng scripts** on dsdp.eclipse.org (Martin: must-have before his vacation)
        *   **Copyright Year Updates** (Run the releng Copyrights Tool)
        *   Migration Notes (for 2.0 / for 1.0?)
        *   API Tooling Javadocs(@noextend and friends) - [bug 227368](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227368), [bug 225529 comment 4](https://bugs.eclipse.org/bugs/show_bug.cgi?id=225529#c6) and [bug 225529 comment 6](https://bugs.eclipse.org/bugs/show_bug.cgi?id=225529#c6) \- [DSDP/TM/Code Ownership](/DSDP/TM/Code_Ownership "DSDP/TM/Code Ownership")
        *   Review and improve Userdocs; we have several open bugs here
        *   Review and improve Javadocs; lots still missing, unclear, duplicated
        *   Fix broken hyperlinks in the docs, fix HTML/XML errors (which can make the indexer not work)
        *   Get rid of compiler warnings wherever possible
        *   Add more Unittests -- ideally write an accompanying unittest for every bugfix
        *   Run Findbugs -- Update site on [http://findbugs.cs.umd.edu/eclipse](http://findbugs.cs.umd.edu/eclipse), Quickdocs by Rado in [tm-dev E-Mail](http://dev.eclipse.org/mhonarc/lists/dsdp-tm-dev/msg01869.html)
            *   Question about filtering false positives posted on fb-discuss [link](https://mailman.cs.umd.edu/pipermail/findbugs-discuss/2008-May/002374.html)
    *   **TM Website:** revamp should really be complete for Ganymede! Kevin and Martin won't have time. DaveD will try to get to it, but cannot promise.

### What will happen after Ganymede?

*   Going for 3.1 next year?
    *   Not breaking API in 3.1 means that we may introduce new concepts as duplicated new API at places, and deprecate the old one so I cannot see anything against 3.1
    *   DaveD: 3.1 is harder than 4.0 but it's worth it -- need to be careful with making changes
    *   Create a bugzilla 3.1 target milestone to start the planning process / reassign bugs on review
    *   Martin recommends going 3.1, but reserving the right to require **Java5 on the Client**, 1.4 on the Server.

*   [TM Future Planning](/TM_Future_Planning "TM Future Planning") Wiki for collecting ideas. Some first thoughts on Priorities?
    *   **AI Martin** create an initial 3.1 plan, update the Planning Wiki
    *   Connection Grouping - be Multicore aware
    *   Rewrite the Tableview to be really aware of Properties
    *   More dynamic subsystem enablement and configuration (e.g. detect UNIX vs Windows automatically at runtime)
    *   Hi-Performance, caching EFS provider
    *   Bring TCF to Maturity
    *   Quality: Add unittest coverage, reduce bloat, improve performance, streamline APIs

Vacation, away
--------------

*   Martin vacation June 11 - 22 -- **AI Martin** finish and test the new Build scripts on dsdp.eclipse.org till then
*   DaveM vacation June 16 - 20
*   DaveD in July

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_21-May-2008#Action_Items "DSDP/TM/Committer Phone Meeting 21-May-2008") Action Items
*   **Everyone**:
    *   Sign up on [TM 3.0 RC2 Testing](/TM_3.0_RC2_Testing "TM 3.0 RC2 Testing") page and invest 2 hours
    *   Triage 3.0 and earlier assigned bugs and move to 3.0.1 / 3.1 what we can
    *   **Add @noextend etc** according to [DSDP/TM/Code Ownership](/DSDP/TM/Code_Ownership "DSDP/TM/Code Ownership") table;
    *   Update the New&Noteworthy (Martin will send a separate E-Mail)
    *   Bug fixes, cleanup, unittests
*   **DaveD**: Take [bug 234215](https://bugs.eclipse.org/bugs/show_bug.cgi?id=234215) and talk to DaveM about [bug 234030](https://bugs.eclipse.org/bugs/show_bug.cgi?id=234030); Dial in at Release Review
*   **DaveM**: [bug 233480](https://bugs.eclipse.org/bugs/show_bug.cgi?id=233480) \- tell the team to use custom newConnectionWizards extension
*   **Kevin**: -
*   **Rupen**: -
*   **Xuan**: -
*   **Martin**: Update Project Plan; Mark [bug 230298](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230298) fixed; File new bug for [bug 165171](https://bugs.eclipse.org/bugs/show_bug.cgi?id=165171); Critical EFS bugs; Finish new Releng and tell DaveD; Get started on New&Noteworthy; Create Bugzilla 3.1 target milestone; Create an initial 3.1 plan
*   **Javier**: Hi-PRI FTP BUGS
*   **Michael**: Terminal: Try to fix [bug 185348](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185348), [bug 204796](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204796)
*   **Uwe**: -
*   **Rado**: Fix [bug 230919](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230919) IFileService.delete()
*   **Felix**: -
*   **Eugene**: -

Next Meeting
------------

*   Monthly [DSDP/TM/Phone Meeting 4-Jun-2008](/DSDP/TM/Phone_Meeting_4-Jun-2008 "DSDP/TM/Phone Meeting 4-Jun-2008") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=6&day=4&year=2008&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Committer Phone Meeting 5-Jun-2008](/DSDP/TM/Committer_Phone_Meeting_5-Jun-2008 "DSDP/TM/Committer Phone Meeting 5-Jun-2008") (8 days) at [1500 UTC / 0800 SFO / 1000 Rochester / 1100 Toronto / 1600 London / 1700 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=6&day=5&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) \- Normal Skype call again


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_28-May-2008](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_28-May-2008))