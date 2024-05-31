

DSDP/TM/Phone Meeting 2-Jul-2008
================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Wednesday [Jul 2, 2008](/index.php?title=Jul_2,_2008&action=edit&redlink=1 "Jul 2, 2008 (page does not exist)") at [1600 UTC / 9am PST](http://www.timeanddate.com/worldclock/fixedtime.html?month=7&day=2&year=2008&hour=16&min=00&sec=0&p1=0) |
| Primary International Dial-in: | **+44 (0)1452 567588** |
| USA Freephone Dial-In: | +1 (866) 6161738 |
| UK National Dial-In: | 08712460713 |
| Passcode: | **0587322148 #** |

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 Last Meetings](#Last-Meetings)
    *   [2.2 Update on RSE Status](#Update-on-RSE-Status)
    *   [2.3 TCF and other initiatives Status](#TCF-and-other-initiatives-Status)
    *   [2.4 Operations](#Operations)
    *   [2.5 TM 3.1 / Future Planning](#TM-3.1-.2F-Future-Planning)
    *   [2.6 Community Feedback and Status](#Community-Feedback-and-Status)
    *   [2.7 Technology sub-groups](#Technology-sub-groups)
*   [3 Vacations, Next Meetings](#Vacations.2C-Next-Meetings)
    *   [3.1 Action Items to Review](#Action-Items-to-Review)
    *   [3.2 New Action Items](#New-Action-Items)
    *   [3.3 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave McKnight
*   ProSyst - Rado Gerganov
*   Wind River - Martin Oberhuber
*   MontaVista - Anna Dushistova

Notes
-----

### Last Meetings

*   Last [DSDP/TM/Phone Meeting 4-Jun-2008](/DSDP/TM/Phone_Meeting_4-Jun-2008 "DSDP/TM/Phone Meeting 4-Jun-2008")
*   Prev [DSDP/TM/Committer Phone Meeting 9-Jun-2008](/DSDP/TM/Committer_Phone_Meeting_9-Jun-2008 "DSDP/TM/Committer Phone Meeting 9-Jun-2008")

### Update on RSE Status

*   TM 3.0 Release: [New&Noteworthy](https://www.eclipse.org/dsdp/tm/development/relnotes/3.0/tm-news-3.0.html), [Release Notes](https://www.eclipse.org/dsdp/tm/development/relnotes/3.0/readme_tm_3.0.html), Build Process, Bugzilla
    *   Is the information that we give enough? (New&Noteworthy); build notes accurate until M6 only, some API changes + feature additions likely missing. Also, the concept of referencing build notes from download.eclipse.org is problematic since milestones are moved to archive.eclipse.org and even deleted eventually --> need a "summary of build notes" on a more persistent place
    *   Ganymede TM Video: features to show beyond what we have in our N&N?
    *   [bug 238574](https://bugs.eclipse.org/bugs/show_bug.cgi?id=238574) Website Revamp? We have a bugzilla "Website" component now
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit) open bugs, [High Priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor) open bugs, [DSDP/TM/3.0 Known Issues and Workarounds](/DSDP/TM/3.0_Known_Issues_and_Workarounds "DSDP/TM/3.0 Known Issues and Workarounds")
    *   EFS deadlock problems during early startup currently being discussed, [bug 239230](https://bugs.eclipse.org/bugs/show_bug.cgi?id=239230)
*   **TM 3.0.1 Build Schedule**
    *   Focus on keeping and improving reliability since WR and IBM will pick up 3.0.1 into commercial products
    *   Continue working in HEAD with care; will likely fork off a maintenance-only branch in August
    *   [bug 172483](https://bugs.eclipse.org/bugs/show_bug.cgi?id=172483) Secondary Terminals for TM 3.0.1 ? - No objections against 3.0.1
    *   [bug 238773](https://bugs.eclipse.org/bugs/show_bug.cgi?id=238773) WinCE RAPI enhancement for calling remote methods for 3.0.1 ? - Will continue in HEAD but not release into the Mapfiles
    *   [bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176) \- Deferred drag&drop from RSE to Windows Explorer is possible but it needs more work and collaboration with the SWT team. We need to find out how to report progress for the background file transfer.
        *   Can patch SWT + RSE to try it out (win32 only): when patching SWT, may have issues with other drag&drop operations. Currently all D&D is async, would need API flag whether async is wanted or not
        *   Proof of concept for now, need feedback / opinions about this approach
*   **Bugzilla Target Milestone**: use the "3.0.1" milestone for what "will be fixed" or what "can be fixed" in 3.0.1 ?
    *   Will do same as last year: use "3.0.1" for "can be fixed" even if we cannot handle all
    *   Committers please update target milestone of your [3.0 assigned bugs](https://bugs.eclipse.org/bugs/buglist.cgi?bug_file_loc=&bug_file_loc_type=allwordssubstr&bug_id=&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bugidtype=include&chfieldfrom=&chfieldto=Now&chfieldvalue=&classification=DSDP&email1=&email2=&emailtype1=substring&emailtype2=substring&field-1-0-0=classification&field-1-1-0=product&field-1-2-0=target_milestone&field-1-3-0=bug_status&field0-0-0=noop&keywords=&keywords_type=allwords&long_desc=&long_desc_type=allwordssubstr&product=Target%20Management&query_format=advanced&remaction=&short_desc=&short_desc_type=allwordssubstr&status_whiteboard=&status_whiteboard_type=allwordssubstr&target_milestone=3.0&target_milestone=3.0%20M3&target_milestone=3.0%20M4&target_milestone=3.0%20M5&target_milestone=3.0%20M6&target_milestone=3.0%20M7&target_milestone=3.0%20RC1&target_milestone=3.0%20RC2&target_milestone=3.0%20RC3&target_milestone=3.0%20RC4&target_milestone=3.0%20RC5&type-1-0-0=anyexact&type-1-1-0=anyexact&type-1-2-0=anyexact&type-1-3-0=anyexact&type0-0-0=noop&value-1-0-0=DSDP&value-1-1-0=Target%20Management&value-1-2-0=3.0%2C3.0%20M3%2C3.0%20M4%2C3.0%20M5%2C3.0%20M6%2C3.0%20M7%2C3.0%20RC1%2C3.0%20RC2%2C3.0%20RC3%2C3.0%20RC4%2C3.0%20RC5&value-1-3-0=UNCONFIRMED%2CNEW%2CASSIGNED%2CREOPENED&value0-0-0=&votes=&order=map_assigned_to.login_name%2Cbugs.priority%2Cbugs.priority%2Cbugs.bug_severity%2Cmap_assigned_to.login_name%2Cbugs.bug_status%2Cbugs.priority%2Cbugs.bug_id&query_based_on=) (currently 98)
    *   Use "Edit Query" to show only yours, then query, then "Change Several Bugs at Once"

### TCF and other initiatives Status

*   **Target Communication Framework** \- [DSDP/TM/TCF FAQ](/DSDP/TM/TCF_FAQ "DSDP/TM/TCF FAQ") available and approved by EMO. Now working on SVN Repository at Eclipse.org. EclipseCon Tutorial and Short Talk available from [TM Homepage](https://www.eclipse.org/dsdp/tm)
*   EPL / EDL dual licensing approved by Eclipse Board for the TCF Agent. Creating new CQ and changing the Copyright / about files now.
*   Picked up TM 3.0 and DD-DSF 1.0 so it's compatible with Ganymede now
*   [bug 238564](https://bugs.eclipse.org/bugs/show_bug.cgi?id=238564) has some very good notes about migrating from TM 2.0 to TM 3.0
*   Working towards scheduled builds and downloadable artifacts.

### Operations

*   Anna introduction - working for MV in Moscow, Russia
*   Newsgroup Duty
*   The new iplog+ flag: [Development Resources/Automatic IP Log](/Development_Resources/Automatic_IP_Log "Development Resources/Automatic IP Log"), [bug 233291](https://bugs.eclipse.org/bugs/show_bug.cgi?id=233291), [bug 220977](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220977)
    *   [Automatic IP Log for TM](https://www.eclipse.org/projects/ip_log.php?projectid=dsdp.tm) doesn't work yet due to a bug in the generator (won't accept space char in bugzilla project name)
    *   But we should be prepared to do automatic log, so we should fully comply
    *   **Mark any Patch or other Attachment** that's contributed with **iplog+** when it is committed into CVS
    *   **Mark the Bug** with iplog+ if a contribution comes in as bugzilla comment
    *   In addition to that, for now, please also mark the bug with the "contributed" keyword (that's the legacy way of doing things) and edit the manual tm-log.csv. I know it's painful but I'd like to continue doing so until the automated log works for us.

### TM 3.1 / Future Planning

*   **Project Plan Status** \- New XML project plan format available, incubation of plan on the [TM Future Planning](/TM_Future_Planning "TM Future Planning") Wiki
    *   Bugzilla plan items as well as an "official" project plan will be done
    *   Wind River: Focus on TCF; RSE bug-fixes and quality; Multi-System/Connection Grouping
    *   IBM: RSE bug-fixes and quality; EFS; Import/Export of Profiles
    *   Prosyst: WinCE (but not going to adopt RSE for now)
    *   Rado private: SWT deferred drag&drop;
    *   Anna/MV: RSE Terminals; have Shell Processes work with Terminal only (would like in 3.0.1); more integration of RSE with CDT and DD
    *    ?? UI/Non-UI splitting;

### Community Feedback and Status

*   Community contributions
    *   Patrick Juhl - SSH Tunnel - no news

### Technology sub-groups

Vacations, Next Meetings
------------------------

*   Call quality fine even though Rado using Skype (but dropped off once)
*   Meeting schedule fine for everybody:
    *   Monthly meeting every 1st wed of the month at 9am PST
    *   Committer meeting every 3rd wed of the month at 8am PST

*   Vacations, away times
    *   Anna: 10 days end July
    *   DaveD: 2 weeks end July / beg August
    *   DaveM: 1st week of August
    *   Rado: 1st 2 weeks of August
*   Questions

### Action Items to Review

*   Last meeting: [DSDP/TM/Phone Meeting 4-Jun-2008](/DSDP/TM/Phone_Meeting_4-Jun-2008 "DSDP/TM/Phone Meeting 4-Jun-2008")

### New Action Items

*   All committers fix target milestone of bugs assigned to 3.0
*   **Martin** review Rado's deferred D&D

### Next Meeting

*   Next [DSDP/TM/Committer Phone Meeting 16-Jul-2008](/DSDP/TM/Committer_Phone_Meeting_16-Jul-2008 "DSDP/TM/Committer Phone Meeting 16-Jul-2008") (2 weeks after)
*   Next [DSDP/TM/Phone Meeting 6-Aug-2008](/DSDP/TM/Phone_Meeting_6-Aug-2008 "DSDP/TM/Phone Meeting 6-Aug-2008") (5 weeks after)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_2-Jul-2008](https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_2-Jul-2008))