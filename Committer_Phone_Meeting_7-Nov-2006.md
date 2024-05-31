

DSDP/TM/Committer Phone Meeting 7-Nov-2006
==========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday Nov 7, 2006 at [7am SFO / 9.00am Rochester / 10.00pm Toronto / 3pm London / 4pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=11&day=7&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave Dykstal, Dave McKnight, Kushal Munir
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber, Michael Scharf (n/a), Ted Williams
*   Tradescape - Lothar Werzinger

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Agenda
------

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site
*   Latest News
    *   New Format - including percent of time available for openRSE in the previous, and next week

| Martin | 80% | Preparing signed jars - [bug 163421](https://bugs.eclipse.org/bugs/show_bug.cgi?id=163421); daily I-builds, build notes; about files still pending | 80% |
| --- | --- | --- | --- |
| DaveD | 80% | Bugfixing; getting bugcount down; concentrating on lo-risk stuff now but will be avalable for helping on critical fixes | 60-80% |
| DaveM | 90% | Bugs: Refresh problem; | 90% |
| Kushal | 60% | Refresh & Filter bugs; encodings on IBM-RSE: additional field on a property page, needs to be added to openRSE real soon; AI: Add enhancement requests to bugzilla | 50% |
| Javier | 80% | Fixing FTP bugs - AI Kushal: apply sorting patch | 50% |
| Ted | 5% | Janet still reviewing rxtx licenses; Michael Scharf might start working on refactoring the Terminal; working on Build for DD | 5% |
| Uwe | 10% | Working around RSE peculiarities in order to make it do what he wants for WR | 50-60% |
| Michael |  |  |  |

*   *   Other News --
*   Top Priorities this week:
    *   **#1 - hi-priority bug fixing, testing and verification**
    *   **#2 - Being responsive**
    *   **#3 - Apply doc fixes**
*   Current Work
    *   **Endgame Plan**:
        *   Bug Fixes all tuesday and wednesday
        *   Martin to release the Mapfiles each morning Europe time --> automatic I-build at 7am Ottawa time
            *   Please test and verify late fixes in the I-builds as you can!
            *   Look at the "fixed bugs not yet verified" on the [bug process page](https://www.eclipse.org/dsdp/tm/development/bug_process.php)
        *   **Thursday: testing and doc fixes only**
        *   Martin to release the Mapfiles Friday morning Europe time --> final I-build (RC) at 7am Ottawa time
        *   Plan to release this unchanged on Friday
    *   **New bugs**: REVIEW [Assigned to Inbox](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&emailassigned_to1=1&emailtype1=exact&email1=dsdp.tm.rse-inbox%40eclipse.org&cmdtype=doit), [Status NEW](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=NEW&cmdtype=doit)
        *   Open bugs: [Major, Critical, P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1),
*   Upcoming Work
    *   Start IBM and EMO review process for User Actions and Import/Export (DaveD)
    *   Start creating Unit Tests, Testing feature (DaveD, Uwe)
    *   Continue bug fixing on HEAD (All)
    *   Fix compiler warnings, prepare for FinBugs (Kushal)
    *   Add ISV Javadoc where it is still missing or incorrect; review, and improve all docs (DaveM)
    *   [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") \- Finalize the 2.0 Project Plan
*   Communications
    *   F2F meeting Toronto, Jan.17-18 (tentative)? - Use as brainstorming / architecture / planning meeting for upcoming "larger" 2.0 changes. Is January too late for that? Do we need it?
        *   DaveD probably not available
    *   [DSDP/TM/Code_Ownership](./Code_Ownership "DSDP/TM/Code Ownership")
    *   API changes: we'll not introduce any api changes between 1.0 and 1.0.1
        *   But prepare for API changes soon after 1.0.1
*   Change Requests
*   Vacations, Holidays etc.
    *   Kushal - Business trip Nov 9 and 10
    *   US Thanksgiving - End of November
*   Free discussion -- feelings, comments, critics

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_31-Oct-2006#Action_Items "DSDP/TM/Committer Phone Meeting 31-Oct-2006") Action Items
*   **DaveD** \- Edit Code Ownership. Submit UDA and Import/Export for review; JUnit tests; Hi-Pri bugs. New bug for moving DTD.
*   **DaveM** \- Enter Resume into www.eclipsecon.org; Bugs
*   **Kushal** \- Bugs
*   **Martin** \- Work on 2.0 project plan; TM FAQ on the Wiki; Hi-pri bugs;
*   **Javier** \- Hook up with Scott Lewis once SD is committed and works
*   **Ted** \- Terminalview; Document the build process

Next Meeting
------------

*   Open [DSDP/TM/Phone Meeting 8-Nov-2006](./Phone_Meeting_8-Nov-2006 "DSDP/TM/Phone Meeting 8-Nov-2006") at 9am PST
*   [DSDP/TM/Committer Phone Meeting 14-Nov-2006](./Committer_Phone_Meeting_14-Nov-2006 "DSDP/TM/Committer Phone Meeting 14-Nov-2006") at [8am SFO / 10.00am Rochester / 12.00pm Toronto / 4pm London / 5pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=11&day=14hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_7-Nov-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_7-Nov-2006))