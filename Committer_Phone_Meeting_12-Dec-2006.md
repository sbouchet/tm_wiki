

DSDP/TM/Committer Phone Meeting 12-Dec-2006
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Dec 12, 2006](./index.php?title=Dec_12,_2006&action=edit&redlink=1 "Dec 12, 2006 (page does not exist)") at [1700 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=12&day=12&hour=17&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 Recent Download Statistics](#Recent-Download-Statistics)
    *   [2.2 Latest News](#Latest-News)
    *   [2.3 Upcoming Work](#Upcoming-Work)
    *   [2.4 Communications](#Communications)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave Dykstal, Dave McKnight, Kushal Munir
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber, (Michael Scharf n/a, Ted Williams n/a)
*   Tradescape - Lothar Werzinger

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help: **being responsive**
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site

### Recent Download Statistics

Still disabled; for analysis, see [DSDP/TM/Phone Meeting 8-Nov-2006](./Phone_Meeting_8-Nov-2006 "DSDP/TM/Phone Meeting 8-Nov-2006")

### Latest News

| Martin | 50% | Fix Terminal Copyright Headers; Resolve MV Ssh Processes IP; Remove RSE/ssh dependency from Team/CVS; Prepare Testing; public holiday. TODO: Testing & Releng | 80% |
| --- | --- | --- | --- |
| DaveD | 20% | bugs | 80% |
| DaveM | 80% | bugs | 80% |
| Kushal | 50% | bugs | 50% |
| Javier | 50% | bugs | 50% |
| Ted | 5% | n/a |  |
| Uwe | 50% | submit Testframework patches to DaveD | 50% |
| Michael | 50% | Finish Terminal Work, mark bugzilla fixed |  |

*   Lothar be able to squeeze in an hour or so for testing 1.0.1

### Upcoming Work

*   **last day** for RSE 1.0.1 fixes ([bugzilla report](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=priority&y_axis_field=assigned_to&z_axis_field=&query_format=report-table&classification=DSDP&product=Target+Management&target_milestone=1.0.1&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&format=table&action=wrap))
    *   Kushal fixed his P2
    *   Martin wants to add the Terminal to the Update Site and the Downloads -- ok for everybody
*   **Adding JUnit Tests** (Uwe, DaveD)
    *   1st patch applied by DaveD, 2nd not yet applied
    *   Dave:Uwe 1-on-1 after the last meeting, issues resolved -> DaveD need to look at the patches
    *   DaveD working on Test Framework allowing different settings on a test run, ran into problems
    *   DaveD will look at the patch
    *   DaveD: As long as we don't eliminate the ability to run inside the framework from a normal launch, DaveD is fine if Uwe commits
    *   Uwe will have the framework in place, but not many tests yet (only creating/removing connections, creating/removing filter) -> skip for 1.0.1
*   **RSE SystemView and Performance**
    *   DaveM looking at Tobias' bug [167620](https://bugs.eclipse.org/bugs/show_bug.cgi?id=167620); improvement already made, working on more improvements
    *   DaveM to correctly revert his change from earlier today
*   **Compiler Warnings**
    *   See the [Committer Howto](https://www.eclipse.org/dsdp/tm/development/committer_howto.php#check_code) for settings
    *   DaveM to look at those that are easy
        *   109 -> 113 -> 113 connectorservice.dstore
        *   176 -> 265 -> 161 rse.core
        *   474 -> 558 -> 558 files.ui
        *   637 -> 662 -> 662 services
        *   221 -> 250 -> 248 subsystems.files.core
        *   1622 -> 346 -> 293 rse.ui
*   **Quality**
    *   Will have a 1-day public round of testing on Wednesday Dec.13, see [RSE 1.0.1 Testing](./RSE_1.0.1_Testing "RSE 1.0.1 Testing")
    *   **Testing on Wednesday is a Priority. Dont squeeze in more bug fixes for wednesday.**
    *   Need to VERIFY all 1.0.1 fixes, and do another round of sanity checks
    *   Martin to assign bug lists to verify
*   Planning 2.0
    *   Start IBM and EMO review process for User Actions and Import/Export (DaveD) - no news
        *   Also need a CQ for two Userdoc files for the Internal Comms Daemon
    *   Lothar: RSE System Viewer doesnt provide StructuredSelection to other parts of Eclipse, want this fixed for 2.0 -> file a defect, probably just not registering RSE
    *   [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") \- Finalize the 2.0 Project Plan
    *   **New bugs**: REVIEW [Assigned to Inbox](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&emailassigned_to1=1&emailtype1=exact&email1=dsdp.tm.rse-inbox%40eclipse.org&cmdtype=doit), [Status NEW](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=NEW&cmdtype=doit)
        *   Open bugs: [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1),

### Communications

*   Vacations, Holidays etc.
    *   Kushal away from 18th, but will try to attend committer meeting next week
    *   Martin, DaveM away from 25th to 1st
    *   Javier away from 25th to 8th
*   Free discussion -- feelings, comments, critics

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_5-Dec-2006#Action_Items "DSDP/TM/Committer Phone Meeting 5-Dec-2006") Action Items
*   **DaveD** \- Fixing & Testing; Submit UDA and Import/Export for IBM internal review; New bug for moving DTD.
*   **DaveM** \- Fixing & Testing; Compiler Warnings (dstore);
*   **Kushal** \- Fixing & Testing; Compiler Warnings (UI); Talk to DaveD re Comm Server;
*   **Martin** \- Add Terminal to Downloads; Signup bugs for verification; Personal Interviews via Skype; Work on [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning"); [TM and RSE FAQ](./TM_and_RSE_FAQ "TM and RSE FAQ"), improve Wiki and Website (how to contribute); Bugs;
*   **Javier** \- Fixing & Testing;
*   **Ted** \- Document the build process (DD project), prepare for Europa build
*   **Michael** -
*   **Uwe** \- Commit Testframework changes; RSE Systemview performance unit tests
*   **Lothar** \- File bug for missing StructuredSelection

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 19-Dec-2006](./Committer_Phone_Meeting_19-Dec-2006 "DSDP/TM/Committer Phone Meeting 19-Dec-2006") at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=12&day=19hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Open [DSDP/TM/Phone Meeting 10-Jan-2007](./Phone_Meeting_10-Jan-2007 "DSDP/TM/Phone Meeting 10-Jan-2007") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_12-Dec-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_12-Dec-2006))