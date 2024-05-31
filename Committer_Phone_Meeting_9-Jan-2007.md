

DSDP/TM/Committer Phone Meeting 9-Jan-2007
==========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Jan 9, 2007](/index.php?title=Jan_9,_2007&action=edit&redlink=1 "Jan 9, 2007 (page does not exist)") at [1700 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=1&day=9&hour=17&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) \-\- 1 hr later due to Orbit call |
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

*   IBM - Dave Dykstal, Dave McKnight (Kushal Munir - sick)
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Michael Scharf, (Uwe Stieber n/a, Ted Williams n/a)

Notes
-----

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help: **being responsive**
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site

### Latest News

| Martin | 50% | Finished Europa M4 delivery. Not got to adding plan itmes yet | 50% |
| --- | --- | --- | --- |
| DaveD | 80% | Refactorings; working with lawyers on new submissions; improved persistence, will add unittests for persistence | 80% |
| DaveM | 60% | Bug work, compiler warnings; api change for file properties for some bugs (timestamps, permissions); EclipseCon | 60% |
| Kushal | 50% | Encodings; sick | 20% |
| Javier | 50% | Passive FTP; Look at moving away from EMF? | 50% |
| Ted | 80% | finished initial "new build" scripts, to be looked at by martin | 0% |
| Uwe | 50% | Unittest framework finished, docs added | 0% |
| Michael | 20% | Working on performance improvements in Terminal; created test connection, analyzed with OptimizeIt | 20% |

### Upcoming Work

*   **Top priority** this week is getting started with the "big rocks" in bugzilla, for [RSE 2.0 Planning](/RSE_2.0_Planning "RSE 2.0 Planning")
    *   add **unit tests** for all new or modified API
    *   document API changes:
        *   ALL API changes need to have an associate bugzilla item tagged with \[api\]
        *   At time of API freeze, we will search all \[api\] bugs and generate migration docs (manually out of them)
        *   When making an API change, not only look at the code but also look at ISV docs
            *   Text search for package names or class names
            *   Usually javadoc is sufficient - there are rare cases where overview is affected as well
*   [RSE 2.0 Planning](/RSE_2.0_Planning "RSE 2.0 Planning")
    *   Plan not made yet, but looks like everyone is working on proper items already. Martin to finish plan items this week
*   Think about limiting the API: Make APIs internal along the way of updating documentation, and making Unit tests, we'll see some API we want "internal".
    *   DaveD: Is there a tool that looks for cycles in package reference graph?
    *   Michael: Lattix - shows dependencies as a matrix
    *   Martin: API Scanner from the WTP project

### Communications

*   Vacations, Holidays etc.
    *   Michael travelling next 2 weeks
    *   Kushal busy with IBM until Jan.19
    *   DaveD going to Chicago end of the month; Florida in February for a week
*   Free discussion -- feelings, comments, critics
    *   DaveM to meet Martin regarding EclipseCon, will need quite some time
    *   DaveM to meet DD folks in Toronto

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_2-Jan-2007#Action_Items "DSDP/TM/Committer Phone Meeting 2-Jan-2007") Action Items
*   **DaveD** \- Refactoring UI/Non-UI; Persistence; Bugs & Unit tests; New bug for moving DTD.
*   **DaveM** \- Meet Martin re. EclipseCon; Bugs & Unit tests; API for setting timestamp & permissions
*   **Kushal** \- Encodings; Compiler Warnings (UI); Talk to DaveD re Comm Server; Bugs & Unit Tests
*   **Martin** \- Meet DaveM re. EclipseCon; Bugs & Unit Tests; Plan Item Specifications; Personal Interviews via Skype; Work on [RSE 2.0 Planning](/RSE_2.0_Planning "RSE 2.0 Planning"); [TM and RSE FAQ](/TM_and_RSE_FAQ "TM and RSE FAQ"), improve Wiki and Website (how to contribute);
*   **Javier** \- Bugs & Unit Tests, FTP passive mode
*   **Ted** -
*   **Michael** \- Terminal Performance Improvements
*   **Uwe** -

Next Meeting
------------

*   Open [DSDP/TM/Phone Meeting 10-Jan-2007](/DSDP/TM/Phone_Meeting_10-Jan-2007 "DSDP/TM/Phone Meeting 10-Jan-2007") at 9am PST
*   [DSDP/TM/Committer Phone Meeting 16-Jan-2007](/DSDP/TM/Committer_Phone_Meeting_16-Jan-2007 "DSDP/TM/Committer Phone Meeting 16-Jan-2007") at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=1&day=16hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_9-Jan-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_9-Jan-2007))