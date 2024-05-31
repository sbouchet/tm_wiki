

DSDP/TM/Committer Phone Meeting 14-Nov-2006
===========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Nov 14, 2006](/index.php?title=Nov_14,_2006&action=edit&redlink=1 "Nov 14, 2006 (page does not exist)") at [8am SFO / 10.00am Rochester / 11.00pm Toronto / 4pm London / 5pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=11&day=14&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 C'mon and celebrate!](#C.27mon-and-celebrate.21)
    *   [2.2 Top Priorities this week](#Top-Priorities-this-week)
    *   [2.3 Upcoming Work](#Upcoming-Work)
    *   [2.4 Communications](#Communications)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave Dykstal, Dave McKnight, Kushal Munir
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber, Ted Williams (dropped off early)

Notes
-----

### C'mon and celebrate!

*   RSE 1.0 is released - just in time
    *   Fabulous press coverage on Eclipse Website: [https://www.eclipse.org/org/press-release/20061112dsdp_milestone.php](https://www.eclipse.org/org/press-release/20061112dsdp_milestone.php)
    *   Doug Gaff talking to 13 press people: [http://dev.eclipse.org/mhonarc/lists/dsdp-pmc/msg00387.html](http://dev.eclipse.org/mhonarc/lists/dsdp-pmc/msg00387.html)
    *   Blogs by [Martin](http://tmober.blogspot.com) and [Doug](http://douggaff.blogspot.com/2006/11/dsdp-yesterday-today-and-tomorrow.html)
    *   Looks like we are riding the wave of general excitement around Eclipse and Embedded
    *   Release looks good, one very late bugfix by Michael [bug 164223: FTP binary transfer](https://bugs.eclipse.org/bugs/show_bug.cgi?id=164223)
    *   [TM and RSE FAQ](/TM_and_RSE_FAQ "TM and RSE FAQ"), Tutorial, [Getting Started](https://www.eclipse.org/dsdp/tm/tutorial/index.php), Website etc. all done
        *   First-time users should be directed to the main [Website](https://www.eclipse.org/dsdp/tm)
    *   Downloads today at 1200UTC (4 hours ago): SDK 72, rseserver-win 16, linux 15, update-site 13
*   What did we accomplish in the past year?
    *   Created infrastructure - project, website, wiki, mailing list, newsgroup, bugzilla, processes for everything
    *   Got all the code through legal review, implemented nightly build system
    *   Grew the community - contributors and users, 220 downloads on 1.0RC2; EclipseCon talk, upcoming tutorial
    *   Refactored RSE (service/subsystem approach; UI/Non-UI separation), implemented deferred queries; new Persistence implementation
    *   Added ssh and ftp subsystems, remotecdt launcher, discovery component
*   In the past year: What did you like? What's the favorite thing you want to do next?
    *   DaveD: Wants to do many little things (e.g. testframework: have testcase for creating 10 connections & deleting them)
    *   DaveM: Wants to do Many little things; multi-commands for cluster management
    *   Kushal: Liked to see ssh and ftp getting implemented -- RSE was prepared for 3rd party extensions from the very beginning, but it took openRSE to make it real; Wants to do Encoding support, EFS
    *   Javier: Liked to see the project getting mature, things fitting together in the end; wants to continue work on Service Discovery; Wizard for creating new subsystems
    *   Ted: Not long enough with the project
    *   Uwe: Wants to learn internals of RSE, make it work for Windriver product
    *   Martin: Liked to see Jakarta Commons get approved; Liked the Refactoring session with DaveM; Wants to improve overall quality and user experience, using RSE himself for daily work
*   Martin to also make personal interviews regarding our processes, improvements, suggestions, bugzilla, testing etc.
*   Any Latest News?
    *   Michael -- Good progress on Terminalview
    *   Ted -- Busy with building DD; will migrate TM build after Dec.15th to the Europa standards
    *   Other News --

### Top Priorities this week

*   **#1 - Convert Downloaders to Contributors - by Being responsive** \- on Newsgroup, Mailinglist and bug reports. We'll probably get lots of new users as we have RSE 1.0. Let's nurture our user community and encourage them to become contributors in case they have requests. Make sure that E-Mail notifications are turned on for bugzilla (and probably also the Wiki FAQ etc.)
*   **#2 - Plan RSE 1.0.1 and 2.0**
*   **#3 - Continue fixing bugs and improving documentation** \- Let's make sure that users who have problems with 1.0 can get a subsequent I-build as patch soon after. Let's make sure users get missing documentation wherever needed. Instead of answering a question by E-Mail, let's fix the corresponding documentation or FAQ and point the users to it.
    *   Build Schedule: Will do an M-build on thursday at 8am Ottawa every week.
    *   Consume our own stuff as much as we can!

### Upcoming Work

*   Triage your assigned Bugs - [Bug Process Page](https://www.eclipse.org/dsdp/tm/developmnet/bug_process.php)
    *   Status NEW --> ASSIGNED (if you are confident)
    *   Assign Target Milestones: 1.0.1 or 2.0 to indicate committed fixes; --- for yet unknown
        *   Better be conservative assigning target milestones -- it should be a firm commitment
        *   The [GMF Project Plan#Plan\_Item\_Queries](/GMF_Project_Plan#Plan_Item_Queries "GMF Project Plan") has some queries that explain how they use target milestone and bug status
    *   Bugzilla: When fixing a bug, please add a short note where it was fixed, e.g. "Fixed in DStoreRemoteFile". This helps tremendously to find and understand the fix, in case it should be needed again later
        *   Kushal, DaveM: How to get notified when a new bug is reported?
        *   On [Bugzilla Email Prefs](https://bugs.eclipse.org/bugs/userprefs.cgi?tab=email) page, enter "Users to Watch": dsdp.tm.core-inbox@eclipse.org,dsdp.tm.rse-inbox@eclipse.org,dsdp.general-inbox@eclipse.org
*   Start IBM and EMO review process for Montavista SSH Processes, User Actions and Import/Export (DaveD)
*   Start creating Unit Tests, Testing feature (DaveD, Uwe)
*   [RSE 2.0 Planning](/RSE_2.0_Planning "RSE 2.0 Planning") \- Finalize the 2.0 Project Plan
*   [DSDP/TM/Code Ownership](/DSDP/TM/Code_Ownership "DSDP/TM/Code Ownership")

### Communications

*   Upcoming Milestones:
    *   **RSE 1.0.1 -- December 15, 2006** (4 weeks from now!)
    *   **RSE 2.0M4 (with Europa M4) -- January 4, 2007** (3 weeks later)
        *   Build system needs to be switched from 3.2.1 based build to Europa build after Dec.15 -- Ted
    *   For more Europa dates, see the [Europa Simultaneous Release](/Europa_Simultaneous_Release "Europa Simultaneous Release") page
*   API changes: we'll not introduce any api changes between 1.0 and 1.0.1; instead, DOCUMENT the APIs, along the way we'll see what needs to be improved. Prepare for API changes soon after 1.0.1
*   Change Requests
    *   Meet 1hr later next week -- ok
*   Vacations, Holidays etc.
    *   DaveD out of office Wed-Fri next week; Christmas - New Year
    *   US Thanksgiving - End of November
*   Free discussion -- feelings, comments, critics

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_7-Nov-2006#Action_Items "DSDP/TM/Committer Phone Meeting 7-Nov-2006") Action Items
*   **DaveD** \- Bug Triage. Edit Code Ownership. Submit 3 CQs to IPZilla; \[next week\] JUnit tests;
*   **DaveM** \- Enter Resume into www.eclipsecon.org; Bug Triage.
*   **Kushal** \- Bug Triage.
*   **Martin** \- Personal Interviews via Skype; Work on [RSE 2.0 Planning](/RSE_2.0_Planning "RSE 2.0 Planning"); [TM and RSE FAQ](/TM_and_RSE_FAQ "TM and RSE FAQ"), improve Wiki and Website (how to contribute); Bug Triage.
*   **Javier** \- Bug Triage.
*   **Ted** \- Make the Build ready for Europa
*   **Michael** \- Terminalview

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 21-Nov-2006](/DSDP/TM/Committer_Phone_Meeting_21-Nov-2006 "DSDP/TM/Committer Phone Meeting 21-Nov-2006") at [9am SFO / 11.00am Rochester / 12.00pm Toronto / 5pm London / 6pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=11&day=21&hour=17&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Open [DSDP/TM/Phone Meeting 6-Dec-2006](/DSDP/TM/Phone_Meeting_6-Dec-2006 "DSDP/TM/Phone Meeting 6-Dec-2006") at [1700 UTC / 9am PST](http://www.timeanddate.com/worldclock/fixedtime.html?month=12&day=6&year=2006&hour=17&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_14-Nov-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_14-Nov-2006))