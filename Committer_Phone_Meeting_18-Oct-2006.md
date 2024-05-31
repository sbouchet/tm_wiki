

DSDP/TM/Committer Phone Meeting 18-Oct-2006
===========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Oct 18, 2006](/index.php?title=Oct_18,_2006&action=edit&redlink=1 "Oct 18, 2006 (page does not exist)") at [8.00am San Francisco / 10.00am Rochester / 11.00am Toronto / 4.00pm London / 5.00pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=10&day=18&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+1 314-655-1411**   North America **+1 877-422-0035** (toll free)   Passcode: **764918** |

DaveD to start conference call - please dial in using the numbers above. Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, and uwe.stieber. DaveD will start Skype chat just prior to call.

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
*   Wind River - Martin Oberhuber, Ted Williams, Uwe Stieber (not present), Michael Scharf

Agenda
------

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site
*   Latest News
    *   Martin -- [RSE 1.0 Testing round 2](/RSE_1.0_Testing_round_2 "RSE 1.0 Testing round 2")
    *   DaveD -- Fixing bugs - concentrating on migrating fixes from IBM previous release
    *   DaveM -- bug queue is large, but perhaps can manage
    *   Kushal -- ditto, fixed several bugs
    *   Javier -- fixed FTP bugs, continuing to work on the few that remain
    *   Ted -- nothing to report
    *   Uwe --
    *   Michael -- presented at Eclipse Summit Europe
    *   Other News --
*   Top Priorities this week:
    *   **#1 - Hi-priority bugfixing**
    *   **Deciding a schedule for the Release**
        *   Weekly release candidates each Friday (10/20, 10/27), release as soon as we have a "go" from all committers. Oct.20 will not be final release candidate.
        *   Shooting for Oct.27 for final release candidate & fixing all hi-pri bugs. One more build may be required on Nov.4 after testing.
        *   Exit criteria: all P1/P2 bugs fixed; defer bugs to a service release.
        *   Discussed pros and cons of an early release.
*   Upcoming Work
    *   **New bugs**: REVIEW [Assigned to Inbox](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&emailassigned_to1=1&emailtype1=exact&email1=dsdp.tm.rse-inbox%40eclipse.org&cmdtype=doit), [Status NEW](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=NEW&cmdtype=doit)
        *   Open bugs: [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1),
    *   Our biggest problems right now
        *   Drag&Drop
        *   Events/Updates/Refresh; Dirty Editors
*   Communications
    *   Missing / Incomplete **Copyrights** \- fixes look good, please use UTF-8 as character set for projects
    *   **Code Ownership** \- [DSDP/TM/Code Ownership](/DSDP/TM/Code_Ownership "DSDP/TM/Code Ownership") \- DaveD to edit (for self).
    *   **Questions from ESE RSE Demo** \- DaveM to comment on these at some point
        *   File locking? No locking mechanism yet. May include synchronize perspective in future releases. RSE will detect remote file changes, though.
        *   How do you write agents?
        *   Is there any tools support for writing agents? Not yet. TPTP?
        *   Any standardization of agents between projects? Not to our knowledge. TPTP?
        *   Can I share a connection with a debugger? Yes, but you will need to build some smarts in to support this.
        *   If the connection to the target system is lost, can I continue editing, reconnect, and then synchronize?
*   Change Requests
    *   "Remote Shell" -> "**RSE Shell**" ? Implications for other views? Decided against doing this for now since this can be quite disruptive to documentation. Not sure "RSE Shell" is the right term.
*   Vacations, Holidays etc.
    *   Martin - 1 more week until Oct.23; public holidays Oct 26, Nov 1-2
    *   DaveD taking Oct 20 off
*   Free discussion -- feelings, comments, critics
    *   EclipseCon 2007 coming in March. Call for Papers has been issued. Martin (and perhaps DaveM) will submit proposal for 2 hour tutorial.

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_11-Oct-2006#Action_Items "DSDP/TM/Committer Phone Meeting 11-Oct-2006") Action Items
*   **DaveD** \- Edit Code Ownership. Hi-Pri bugs.
*   **DaveM** \- Meet Kushal for Dirty Editors. Hi-pri bugs
*   **Kushal** \- Meet DaveM for Dirty Editors; Hi-pri bugs; Encoding bugs?
*   **Martin** \- Create empty project plan; TM FAQ on the Wiki; Hi-pri bugs; Do RC builds; Send community note on release schedule.
*   **Javier** \- FTP bugs; Hook up with Scott Lewis once SD is committed and works
*   **Ted** \- Terminalview; Document the build process

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 25-Oct-2006](/DSDP/TM/Committer_Phone_Meeting_25-Oct-2006 "DSDP/TM/Committer Phone Meeting 25-Oct-2006") at 8am SFO/10.00am Rochester/11.00pm Toronto/4pm London/5pm Salzburg
*   Open [DSDP/TM/Phone Meeting 8-Nov-2006](/DSDP/TM/Phone_Meeting_8-Nov-2006 "DSDP/TM/Phone Meeting 8-Nov-2006") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_18-Oct-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_18-Oct-2006))