

DSDP/TM/Committer Phone Meeting 6-Sep-2006
==========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Sep 6, 2006](/index.php?title=Sep_6,_2006&action=edit&redlink=1 "Sep 6, 2006 (page does not exist)") at [8.30am Rochester / 9.30am Toronto / 2.30pm London / 3.30pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=9&day=6&hour=13&min=30&sec=0&p1=223&p2=250&p3=421&p4=136&iv=1800) |
| Dial-in: | Martin to start a Skype conference - you'll be called:   Skype **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal\_munir, javier.montalvoorus |

Fixed-line fallback dial-in:

*   International **+1 314-655-1411**
*   North America **+1 877-422-0035** (toll free)
*   Passcode: **764918**

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave Dykstal, Dave McKnight (Kushal Munir on vacation)
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber

Agenda
------

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site
*   Latest News
    *   Martin -- No news; Javiers stuff not yet committed
    *   DaveD -- JUnit adapted to refactorings; will look at M4 bugs
    *   DaveM -- Refactored UI/Non-UI: "Organize Imports" should be sufficient for client code
    *   Kushal -- vacation
    *   Javier -- just returned from vacation; vote on Ted as committer
    *   Other News --
*   Upcoming Work
    *   **M4 bugs**: PLEASE REVIEW [M4 BUGS](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&target_milestone=1.0+M4&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit)!!
    *   **Inbox**: REVIEW [Assigned to Inbox](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&emailassigned_to1=1&emailtype1=exact&email1=dsdp.tm.rse-inbox%40eclipse.org&cmdtype=doit)
    *   **Timing**: Martin on vacation most of October; Release Review Sept.27, M5 is Sept.22
        *   P1/P2 bugs MUST be fixed by Sept. 15!
        *   Fallback for Martin on the Sep27 presentation: DaveD or Michael Scharf
    *   **Source Code Style & Cleanness**
        *   **Compiler Warnings**: See [Committer Howto](https://www.eclipse.org/dsdp/tm/development/compiler_warnings.php)
            *   When you change a code, please make it warning-free before checkin (but dont go and chase compilerwarnings yet)
            *   Target VM is Java-1.4 with the satandard settings (i.e. no assert unless set up in build.properties)
        *   **Code Ownership** \-\- See (and edit) [DSDP/TM/Code Ownership](/DSDP/TM/Code_Ownership "DSDP/TM/Code Ownership")
        *   **Code Style and Format** \-\- defer to next week
    *   **Change Requests** \-\- defer to next week
    *   **Features**: Jakarta-commons, JUnit-framework, Discovery, EFS-Experimental, WR-Terminal ([bug 152826](https://bugs.eclipse.org/bugs/show_bug.cgi?id=152826))
        *   Jakarta-commons still important for Symbian
        *   Discovery: Martin to hook up with Javier directly for initial checkin
    *   **Refactorings**: DaveM did most important stuff; consider "finished" for now, continue with hi-pri bugs
        *   Martin to fix ISV docs and document the changes in build notes
        *   Subsystem Factory vs. Configuration: Please rename \*factory to \*configuration whenever you see it (Javadoc, local variables, parameter names)
    *   API Things
        *   Martin did some minor extension point cleanup (rename), see [build notes of N-builds](http://download.eclipse.org/dsdp/tm/downloads/drops/N20060829-0100/buildNotes.php)
        *   **Service Error Reporting** \- [bug 149472](https://bugs.eclipse.org/bugs/show_bug.cgi?id=149472) \- DaveD - API ok so far, final resolution? --> Create new different bug id for that one.
        *   **Parallel Services** \- [bug 142478](https://bugs.eclipse.org/bugs/show_bug.cgi?id=142478) all queries in background - DaveM
        *   **SystemRegistry.createHost** for Javier
            *   [bug 150168](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150168) dont commit immediately - DaveD
                *   Javier: not important at the moment; DaveD: probably fixed already
            *   [bug 150265](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150265) allow specifying subsystem types - DaveM to discuss with Javier once discovery is committed
                *   Example: 1 Host providing shell and FTP (different categories)
                *   Problem: createHost() only creates a host with 1 service -- See video for service discovery, DaveM to take a look at it
                *   Need createHost() with a list of services
                *   Look at this again next week
        *   Making stuff **internal** \- ssh, ftp: Martin; Core: List of candidates from DaveD?
    *   Cleanup: API Doc (duplicates in interface and implementation!), JUnit tests, Context help, Test Plans, RSE-7-migration-docs, Copyrights, licenses, Tutorial code in Javadoc
    *   **Bug Work - please observe priorities**
        *   DaveD: Team stuff
        *   Open bugs: [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1),
    *   Legal: JUnit (next monday?); Jakarta-commons (deferred!); WR Terminalview (passed!)
*   Other items
    *   Manual test plans - in work by **Martin**
    *   EFS Experimental feature to be created by Martin
*   Free discussion -- feelings, comments, critics

  

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_30-Aug-2006#Action_Items "DSDP/TM/Committer Phone Meeting 30-Aug-2006") Action Items
*   **DaveD** \- Edit Code Ownership; JUnit, Review bugs assigned to M4, Hi-Pri bugs. Checkin mappings.csv, New bug for moving DTD, Send "Team" test plans to Martin. SystemRegistry API. Team fixes: Check collapsing persistence Properties nodes to fewer files. Compile a list of suggestions for making classes / packages internal.
*   **DaveM** \- Edit Code Ownership; Hi-pri bugs; get rid of Service calls on UI thread; hygiene changes
*   **Kushal** \- Hi-pri bugs; send file encoding test resources to martin; review & get rid of rseConfigDefaults; talk to Don about persistenceProvider
*   **Martin** \- Fixup & document refactorings; Release Review Slides, Manual test plan, Hi-pri bugs; Hook up with WickedShell; EFS feature, Add Discovery, Build scripts for CDT and Discovery, API Review, Jakarta-commons, WR-terminalview; Review if IShellService is sufficient for terminal
*   **Javier** \- Discovery initial checkin; hook up with Scott Lewis once SD is committed
*   **Everyone** \- List obsolete API on [RSE 2.0 Planning](/RSE_2.0_Planning "RSE 2.0 Planning") page

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 13-Sep-2006](/DSDP/TM/Committer_Phone_Meeting_13-Sep-2006 "DSDP/TM/Committer Phone Meeting 13-Sep-2006") at 9.30am Toronto
*   Release Review Meeting on [27-Sep-2006 at 8am PDT](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=9&day=27&hour=15&min=0&sec=0&p1=224&p2=421&p3=250&p4=136&p5=223)
*   Open [DSDP/TM/Phone Meeting 4-Oct-2006](/DSDP/TM/Phone_Meeting_4-Oct-2006 "DSDP/TM/Phone Meeting 4-Oct-2006") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_6-Sep-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_6-Sep-2006))