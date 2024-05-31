

DSDP/TM/Committer Phone Meeting 31-Oct-2006
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday Oct 31, 2006 at [8.00am San Francisco / 10.00am Rochester / 11.00am Toronto / 4.00pm London / 5.00pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=10&day=31&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_sharf, and uwe.stieber.  
MartinO will start Skype chat just prior to call.

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
*   Wind River - Martin Oberhuber, Uwe Stieber; Michael Scharf (absent), Ted Williams (absent)
*   Tradescape - Lothar Werzinger

Agenda
------

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site
*   Latest News
    *   Martin -- [RSE 1.0 Testing round 3](./RSE_1.0_Testing_round_3 "RSE 1.0 Testing round 3"); bugfixes; releasing RC3; about files still pending!
    *   DaveD -- bugfixing, verification; some lo-pri filter bugs still pending
    *   DaveM -- testing & verification
    *   Kushal -- testing & verification
    *   Javier -- bug verification, FTP testing
    *   Ted -- n/a (jury duty)
    *   Uwe -- Windriver stuff
    *   Michael --n/a
    *   Other News --
*   Top Priorities this week:
    *   **#1 - Hi-priority bugfixing** \- please observe the priorities.
    *   **#2 - Being responsive**
*   Looking back on [RSE 1.0 Testing round 3](./RSE_1.0_Testing_round_3 "RSE 1.0 Testing round 3")
    *   committers can set to CLOSED right away instead of setting VERIFIED
    *   Filter questions by LotharW
        *   Programmatically use the remote file selection dialog to restrict it to some filter
        *   DaveM: Changing the root of the remote systems tree in the dialog should be possible
        *   DaveM: would like a dialog that's not tree-based but table-based, with a predefined filter
*   Upcoming Work
    *   Endgame Plan
        *   Automatic nightly I-builds until the release
        *   Martin to update the mapfiles for now, will review checkins and release
        *   Continue fixing bugs: P1,P2 first - then choose the P3 ones you like best, or are easy / riskless to fix
        *   Everybody feel free to promote P3 bugs they feel important into P2 bugs such that they get visible to others
        *   Everybody feel free to make checkins since we'll review anyway
        *   Lothar can do bug Verification
        *   Everybody: Also file non-reproducable bugs, use Bugzilla for tracking
    *   **New bugs**: REVIEW [Assigned to Inbox](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&emailassigned_to1=1&emailtype1=exact&email1=dsdp.tm.rse-inbox%40eclipse.org&cmdtype=doit), [Status NEW](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=NEW&cmdtype=doit)
        *   Open bugs: [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1),
    *   Our biggest problems right now
        *   Drag&Drop
            *   Upload's OK, download not -- COM translates all dnd into Strings, so it needs to be a local file; we'd need to download on drag already
            *   Navigator should work, Project Explorer tbd
            *   Split up the "monster" dnd bugreport into separate ones for the separate issues
            *   dnd won't be supported on MacOS; should be addressed fairly quickly after 1.0; seems to be a problem with dragStart
        *   Events/Updates/Refresh/Treeview
            *   After copy&paste, remote directory is collapsed
            *   Might be just a little annoyance, but it leads users to lose confidence!
*   Communications
    *   API changes: we'll not introduce any more api changes for 1.0
        *   Lothar confirms that provisional API is fine for 1.0
        *   Dont want lots of deprecatedes in 2.0 --> it will be fine to have incompatible API changes in 2.0
    *   FTP dnd: copy vs. move
        *   API needs to be observed, FTPFileService.copy() should raise an exception
    *   Extend Uwe's commit rights to RSE?
        *   Dave's & Kushal OK with extending, will publicly vote
    *   Shall we get rid of unused icons, e.g. rse.ui/icons/full/obj16/system390_obj.gif ?
    *   Shall we get rid of commented out source code ?
        *   too late for 1.0 but want to get rid of both soon after
*   Change Requests
*   [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") \- First tasks after 1.0 is completed:
    *   Start IBM and EMO review process for User Actions and Import/Export (DaveD)
    *   Start creating Unit Tests, Testing feature (DaveD, Uwe)
    *   Continue bug fixing on HEAD (All)
    *   Add ISV Javadoc where it is still missing or incorrect; review all docs
    *   Finalize the 2.0 Project Plan
*   Vacations, Holidays etc.
    *   Martin - public holidays Nov 1
    *   US Thanksgiving - End of November
    *   Kushal - Business trip Nov 9 and 10
*   Free discussion -- feelings, comments, critics
    *   [DSDP/TM/Code_Ownership](./Code_Ownership "DSDP/TM/Code Ownership")
    *   **Can we move next weeks meeting 1 hour earlier in order to accomodate the Orbit call?**
    *   EclipseCon 2007 coming in March. Call for Papers has been issued. Martin and DaveM will submit proposal for 2 hour tutorial.

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_25-Oct-2006#Action_Items "DSDP/TM/Committer Phone Meeting 25-Oct-2006") Action Items
*   **DaveD** \- Edit Code Ownership. Hi-Pri bugs. New bug for moving DTD.
*   **DaveM** \- Hi-pri bugs
*   **Kushal** \- Hi-pri bugs; Encoding bugs?
*   **Martin** \- Create empty project plan; TM FAQ on the Wiki; Hi-pri bugs;
*   **Javier** \- FTP bugs; Hook up with Scott Lewis once SD is committed and works
*   **Ted** \- Terminalview; Document the build process

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 7-Nov-2006](./Committer_Phone_Meeting_7-Nov-2006 "DSDP/TM/Committer Phone Meeting 7-Nov-2006") at [7am SFO / 9.00am Rochester / 10.00pm Toronto / 3pm London / 4pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=11&day=7&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Open [DSDP/TM/Phone Meeting 8-Nov-2006](./Phone_Meeting_8-Nov-2006 "DSDP/TM/Phone Meeting 8-Nov-2006") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_31-Oct-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_31-Oct-2006))