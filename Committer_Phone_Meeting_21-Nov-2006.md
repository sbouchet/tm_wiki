

DSDP/TM/Committer Phone Meeting 21-Nov-2006
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday Nov 21, 2006 at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=11&day=21&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 Latest News](#Latest-News)
    *   [2.2 Upcoming Work](#Upcoming-Work)
    *   [2.3 Communications](#Communications)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave Dykstal, Dave McKnight, Kushal Munir
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber, Michael Scharf, Ted Williams
*   Tradescape - (Lothar Werzinger n/a)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site

### Latest News

| Martin | 30% | Bug triage; prepared M-builds; signed Jars [bug 163421](https://bugs.eclipse.org/bugs/show_bug.cgi?id=163421); Windriver work towards RSE | 80% |
| --- | --- | --- | --- |
| DaveD | 80% | Bug triage \[6 hrs\] and fixing; Montavista CQ submitted; some IBM work needed for User Commands and Import/Export | 20% |
| DaveM | 90% | Bug triage \[6-8 hrs\] and fixing; EFS with Kushal | 80% |
| Kushal | 50% | looked at EFS with DaveM, and encodings; bug triage and fixing. AI assign target milestones | 50% |
| Javier | 80% | Fixing FTP bugs | 50% |
| Ted | 5% | working on Build for DD; decided not to use buckminster | 5% |
| Uwe | 10% | Nothing new this week, going to work on Unit Tests for RSE | 50% |
| Michael | 50% | Refactoring the Terminal View [bug 165177](https://bugs.eclipse.org/bugs/show_bug.cgi?id=165177) | 50% |

*   Bug triage took some time, especially verifying what was still a bug - but time was well invested
    *   Some bugs might need a state like "need to be divided", for example the RemoteTempFiles thing
    *   Others might need combining into plan items; this will be part of 2.0 planning
    *   Perhaps we could be more effective by (a) getting the bugcount down and (b) "doing the right thing right away"
*   Get the bugcount down for 1.0.1, get simple things off the table
*   TempFilesCache: Pathlength; Case sensitivity; think about pathname mangling is separate from the decision whether we want the project in the workspace
    *   EFS problems are mostly due to Eclipse Jobs locking the Resource during EFS access -- but on the other hand, we'll need RemoteTempFiles as an Eclipse Resource in order to get the Outline View

  

### Upcoming Work

*   Top Priorities this week
    *   **#1 - Being responsive** \- on Newsgroup, Mailinglist and bug reports. We'll probably get lots of new users as we have RSE 1.0. Let's nurture our user community and encourage them to become contributors in case they have requests. Make sure that E-Mail notifications are turned on for bugzilla (and probably also the Wiki FAQ etc.)
    *   **#2 - Continue fixing bugs and improving documentation** \- Let's make sure that users who have problems with 1.0 can get a subsequent I-build as patch soon after. Let's make sure users get missing documentation wherever needed. Instead of answering a question by E-Mail, let's fix the corresponding documentation or FAQ and point the users to it.
    *   **#3 - Plan RSE 1.0.1 and RSE 2.0**
*   Work towards RSE 1.0.1
    *   Start IBM and EMO review process for User Actions and Import/Export (DaveD)
        *   Also need a CQ for two Userdoc files for the Internal Comms Daemon
    *   Start creating Unit Tests, Testing feature (DaveD, Uwe)
    *   Continue bug fixing on HEAD (All)
    *   Continue bug verifications for all fixed bugs. Sombody else than the person fixing a bug should verify it.
    *   Fix compiler warnings (Kushal) - prepare for running FindBugs
        *   There is also the TPTP StaticAnalysis thing
    *   Add ISV Javadoc where it is still missing or incorrect; review, and improve all docs
    *   1.0.1 non-breaking API changes: See [Evolving Java-based APIs](https://wiki.eclipse.org/Evolving_Java-based_APIs "Evolving Java-based APIs")
*   Work towards RSE 2.0
    *   [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") \- Finalize the 2.0 Project Plan

### Communications

*   [DSDP/TM/Code_Ownership](./Code_Ownership "DSDP/TM/Code Ownership") \- is it complete now?
*   [bug 160783](https://bugs.eclipse.org/bugs/show_bug.cgi?id=160783): "Remote Commands View" vs. "Remote Shell View"
    *   What was the IBM Rationale behind renaming it to "Remote Shell"?
    *   A Shell is something long-running, interactive whereas a command is something run only once
    *   The Terminal will provide access to interactive shells including full terminal emulation; we'll need a clear separation between what a "Terminal" and what a "Command Shell" is
*   Place for Prototyping:
    *   Projects rarely exchange prototypy code across company boundaries
    *   We could have org.eclipse.tm.rse/playground/{plugin} but then all code checked in there must be EPL -- do we want this, or can we set up something more private?
    *   Should we attach the multi-command stuff to [bug 159164](https://bugs.eclipse.org/bugs/show_bug.cgi?id=159164) for now?
*   Vacations, Holidays etc.
*   Free discussion -- feelings, comments, critics

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_14-Nov-2006#Action_Items "DSDP/TM/Committer Phone Meeting 14-Nov-2006") Action Items
*   **DaveD** \- CQ for Internal Communications Server Userdocs; Edit Code Ownership. Submit UDA and Import/Export for IBM internal review; JUnit tests; Hi-Pri bugs. New bug for moving DTD.
*   **DaveM** \- Bugs
*   **Kushal** \- Assign Target Milestones; Bugs
*   **Martin** \- Personal Interviews via Skype; Work on [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning"); [TM and RSE FAQ](./TM_and_RSE_FAQ "TM and RSE FAQ"), improve Wiki and Website (how to contribute); Hi-pri bugs;
*   **Javier** \- Bugs
*   **Ted** \- Document the build process (DD project), prepare for Europa build
*   **Michael** \- Terminalview
*   **Uwe** \- RSE Systemview performance unit tests

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 28-Nov-2006](./Committer_Phone_Meeting_28-Nov-2006 "DSDP/TM/Committer Phone Meeting 28-Nov-2006") at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=11&day=28hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Open [DSDP/TM/Phone Meeting 6-Dec-2006](./Phone_Meeting_6-Dec-2006 "DSDP/TM/Phone Meeting 6-Dec-2006") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_21-Nov-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_21-Nov-2006))