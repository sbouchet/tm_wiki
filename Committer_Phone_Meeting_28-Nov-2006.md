

DSDP/TM/Committer Phone Meeting 28-Nov-2006
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday Nov 28, 2006 at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=11&day=28&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
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
*   Wind River - Martin Oberhuber, Uwe Stieber, (n/a Michael Scharf), Ted Williams

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help: **being responsive**
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site

### Latest News

| Martin | 80% | Bugzilla work: reproducing, discussing, specifying, assigning target milestones | 80% |
| --- | --- | --- | --- |
| DaveD | 20% | Not much this past week due to vacation and holidays - documentation bugs, test cases | 50% |
| DaveM | 80% | Bugfixes | 80% |
| Kushal | 15% | Need to look at bugs this week | 90% |
| Javier | 50% | FTP Bugfixes; want to continue on SD, want to have SD "official" | 50% |
| Ted | 5% | No news, working on DD, waiting for Terminal from Michael | 5% |
| Uwe | 50% | JUnit | 50% |
| Michael | 50% | Terminal (checkin probably tomorrow), Bugzilla | 50% |

*   Javadoc: we should think about style in javadoc - what are preconditions, postconditions, timing / threading issues?
    *   Better not refer to users as "you" (Kushal: Eclipse uses the word "client")
    *   DaveD enjoys writing up javadocs

### Upcoming Work

*   **Adding JUnit Tests** (Uwe, DaveD)
    *   CQ required? - E-Mailed Janet
    *   RSE Testview allows to run in the "host" eclipse, PDE requires an additional "target" Eclipse
    *   Uwe: is it possible to eliminate the layers between UnitTest and BaseConnectionTest? - PDE JUnit view is more functional e.g. jump to line; suggest shipping JDT with RSE for "integrated" tests and move to the JUnit view
    *   DaveD: If we can eliminate the framework he has no problems, want to make it as simple as possible - only condition is that it should be possible to ship the tests without including (JDT|PDE); Uwe OK to send patches -- identify the additional plugins that need to be shipped in order to get the JUnit view
*   **RSE SystemView and Performance**
    *   Is the Selection maintained when the view contents changes? \[Calls to setSelection(getSelection())
        *   If a refresh event comes in (e.g. new file under the selected directory), selection is maintained - same as for Memento
        *   Selection Scanning to determine enabled state of actions
        *   Uwe: State changes on nodes need to trigger "selectionChanged" for the actions that select the element - WR has some code to optimize the amount of selectionChanged events: code that finds out if a refresh affects the current selection and fires selectionChanged (or not)
    *   Are refresh events on hidden elements (elements below a collapsed node) filtered out?
        *   Kushal: Code looks at expanded state, so maybe these are filtered out
        *   Martin: "push" mode by events from the remote system instead of "pull" mode -- DaveM has experience with something similar; RSE view is not really designed for push mode, it was originally designed for synchronous operation
    *   Are label provider queries on elements outside the visible area filtered out? \[VirtualTree\]
        *   IBM team very interested in playing with VirtualTree / VirtualTable -- had performance problems with the Shell view in the past when there are lots of items, search was probably the biggest one
*   **Compiler Warnings**
    *   See the [Committer Howto](https://www.eclipse.org/dsdp/tm/development/committer_howto.php#check_code) for settings: changed **NON-NLS-1 enabled**, **Javadoc consider protected**
    *   Do not check in code with warnings
    *   Fix compiler warnings (Kushal) - prepare for running FindBugs or the TPTP StaticAnalysis thing
        *   647 dstore.core
        *   109 connectorservice.dstore
        *   176 rse.core
        *   474 files.ui
        *   134 logging
        *   637 services
        *   653 services.dstore
        *   221 subsystems.files.core
        *   1622 rse.ui
    *   Java5 Array settings ?
    *   DaveD to logging
    *   DaveM to dstore
    *   Kushal to look at UI
*   **Quality**
    *   1.0.1 planning finished - **Target Milestone assignments are firm commitments**
        *   1.0.1 Fixes must be in by Monday Dec.11th
    *   Do we consume RSE ourselves?
    *   Continue bug verifications for all fixed bugs. Sombody else than the person fixing a bug should verify it.
    *   Will have a 1-day public round of testing on Tuesday Dec.12, see [RSE 1.0.1 Testing](./RSE_1.0.1_Testing "RSE 1.0.1 Testing")
    *   **Docs are a high priority**. Add ISV Javadoc where it is still missing or incorrect; review, and improve all docs
    *   [DSDP/TM/Code_Ownership](./Code_Ownership "DSDP/TM/Code Ownership")
*   Planning 2.0
    *   Start IBM and EMO review process for User Actions and Import/Export (DaveD)
        *   Also need a CQ for two Userdoc files for the Internal Comms Daemon
        *   Internal Comms Daemon is for tools running on the server that need to connect back to the client; might want to factor it out of open source so it's just in IBM products
            *   It was intended to be genericly used -> Kushal to talk to Don to find out if it makes sense in OpenSource
    *   [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") \- Finalize the 2.0 Project Plan
    *   Think about limiting the API: Make APIs internal along the way of updating documentation, and making Unit tests, we'll see some API we want "internal". We should DOCUMENT these for now and DO it soon after 1.0.1
    *   **New bugs**: REVIEW [Assigned to Inbox](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&emailassigned_to1=1&emailtype1=exact&email1=dsdp.tm.rse-inbox%40eclipse.org&cmdtype=doit), [Status NEW](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=NEW&cmdtype=doit)
        *   Open bugs: [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1),

### Communications

*   Shall we get rid of unused icons, e.g. rse.ui/icons/full/obj16/system390_obj.gif ? - not yet
*   Shall we get rid of commented out source code ? - not yet
*   Change Requests
*   Vacations, Holidays etc.
    *   Javier away Nov. 29th/30th and Christmas
    *   Movie Day on the 8th in Toronto
    *   Kushal away from 18th
    *   Martin, DaveM away from 25th to 1st
*   Free discussion -- feelings, comments, critics

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_21-Nov-2006#Action_Items "DSDP/TM/Committer Phone Meeting 21-Nov-2006") Action Items
*   **DaveD** \- Submit UDA and Import/Export for IBM internal review; Compiler Warnings (logging); New bug for moving DTD.
*   **DaveM** \- Bugs; Compiler Warnings (dstore);
*   **Kushal** \- Compiler Warnings (UI); Talk to Don re Comm Server; Bugs
*   **Martin** \- Personal Interviews via Skype; Work on [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning"); [TM and RSE FAQ](./TM_and_RSE_FAQ "TM and RSE FAQ"), improve Wiki and Website (how to contribute); Bugs; Set Java1.4 EE on all projects
*   **Javier** \- Bugs; Compiler Warnings (discovery);
*   **Ted** \- Document the build process (DD project), prepare for Europa build
*   **Michael** \- Terminalview
*   **Uwe** \- RSE Systemview performance unit tests, hook up with DaveD

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 5-Dec-2006](./Committer_Phone_Meeting_5-Dec-2006 "DSDP/TM/Committer Phone Meeting 5-Dec-2006") at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=12&day=5hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Open [DSDP/TM/Phone Meeting 6-Dec-2006](./Phone_Meeting_6-Dec-2006 "DSDP/TM/Phone Meeting 6-Dec-2006") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_28-Nov-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_28-Nov-2006))