

DSDP/TM/Committer Phone Meeting 25-Oct-2006
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Oct 25, 2006](./index.php?title=Oct_25,_2006&action=edit&redlink=1 "Oct 25, 2006 (page does not exist)") at [8.00am San Francisco / 10.00am Rochester / 11.00am Toronto / 4.00pm London / 5.00pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=10&day=25&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
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
*   Wind River - Martin Oberhuber, Ted Williams, Uwe Stieber (absent), Michael Scharf (absent)
*   Tradescape - Lothar Werzinger (tentative, did not come)

Agenda
------

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site
*   Latest News
    *   Martin -- Eclipse.org about files review; updating TM website; joining Orbit for Commons Net
    *   DaveD -- fixed few bugs for IBM (accessibility), full time now on P2 bugs
    *   DaveM -- bug work; pondering some "intended behavior" things
        *   **New scheme for deferring bugs**: set Target Milestone="---" and probably lower priority. This is because "RESOLVED LATER" is uncomfortable to handle -- cannot reopen multiple at once, comment needed for reopen, easily confused against regression of bugs
    *   Kushal -- fixing P2s first, then going to look at easy P3
    *   Javier -- fixing P2s; looking at P3s now; stress testing on FTP;
    *   Ted -- no news
    *   Uwe -- not available
    *   Michael -- not available
    *   Other News --
        *   Stefan Reichert, maintainer of Wicked Shell, wants to join RSE as contributor
        *   Lothar Werzinger of Tradescape submitted 2 patches, which is making him contributor
*   Top Priorities this week:
    *   **#1 - Hi-priority bugfixing** \- please observe the priorities.
    *   **#2 - Being responsive**
        *   When you are personally addressed in a bug comment, please answer timely. Bugzilla E-Mail notifications should tell you so. It's important to answer and give your comment but not invest too much time -- the bulk of your time should still go into hi-priority bugfixing.
        *   Saved searches: Every committer should have at least 3 saved searches: **Assigned to me**, **RSE P1/P2**, **RSE Open changed last week**
        *   You can then e.g. sort the **Assigned to me** search by Status to see what's in NEW state and should be accepted (set ASSIGNED)
        *   See the [Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for templates of these searches. You can just click on them and "Save as..." in bugzilla for your personal use
*   Upcoming Work
    *   **New bugs**: REVIEW [Assigned to Inbox](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&emailassigned_to1=1&emailtype1=exact&email1=dsdp.tm.rse-inbox%40eclipse.org&cmdtype=doit), [Status NEW](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=NEW&cmdtype=doit)
        *   Open bugs: [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1),
    *   Our biggest problems right now
        *   Drag&Drop
        *   Events/Updates/Refresh; Dirty Editors
*   Communications
    *   Extend Uwe's commit rights to RSE? - Let him submit patches for 1 more week and decide then. Basically OK with plain \[cleanup\] changes in RSE, but need to be careful with changing terminology or API changes.
        *   Martin agrees that for API changes, the process is propose first - vote next - code only then.
*   Change Requests
    *   [Bug 161773](https://bugs.eclipse.org/bugs/show_bug.cgi?id=161773): IHostShell.getLines() should return IHostOutput\[\] instead of Object\[\]
    *   Ted Terminal view: Will go forward splitting it up such that the Transport can be contributed. Expects a version in 2 weeks
*   [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning")
    *   Europa Milestones fixed, our first Europa delivery is Jan.3rd to be compiled against Eclipse 3.3
    *   We will have a service release (RSE 1.0.1) in december, out of the HEAD stream; then start a branch for RSE 1.0.2 (probably end of february, along with Eclipse 3.2.2)
    *   So we will compile against Eclipse 3.2 until beginning of december, and not make any API changes till then
    *   Focus till then will be on bug fixing, and starting the IP review process for User Actions and Import/Export
    *   User Actions and Import/Export will not make it in december; to be ready for EclipseCon
    *   RSE 1.0.1 content will be bug fixes and the new Terminal
*   Vacations, Holidays etc.
    *   Martin - public holidays Oct 26, Nov 1-2
    *   US Thanksgiving - End of November
*   Free discussion -- feelings, comments, critics
    *   EclipseCon 2007 coming in March. Call for Papers has been issued. Martin and DaveM will submit proposal for 2 hour tutorial.

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_18-Oct-2006#Action_Items "DSDP/TM/Committer Phone Meeting 18-Oct-2006") Action Items
*   **DaveD** \- Edit Code Ownership. Hi-Pri bugs. New bug for moving DTD.
*   **DaveM** \- Hi-pri bugs
*   **Kushal** \- Hi-pri bugs; Encoding bugs?
*   **Martin** \- Create empty project plan; TM FAQ on the Wiki; Hi-pri bugs;
*   **Javier** \- FTP bugs; Hook up with Scott Lewis once SD is committed and works
*   **Ted** \- Terminalview; Document the build process

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 31-Oct-2006](./Committer_Phone_Meeting_31-Oct-2006 "DSDP/TM/Committer Phone Meeting 31-Oct-2006") at 8am SFO/10.00am Rochester/11.00pm Toronto/4pm London/5pm Salzburg
*   Open [DSDP/TM/Phone Meeting 8-Nov-2006](./Phone_Meeting_8-Nov-2006 "DSDP/TM/Phone Meeting 8-Nov-2006") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_25-Oct-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_25-Oct-2006))