

DSDP/TM/Committer Phone Meeting 13-Sep-2006
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday Sep 13, 2006 at [8.30am Rochester / 9.30am Toronto / 2.30pm London / 3.30pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=9&day=13&hour=13&min=30&sec=0&p1=159&p2=250&p3=136&p4=223&iv=1800) |
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

*   IBM - Dave Dykstal, Dave McKnight, Kushal Munir
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber (Ted Williams - on Build Symposion)

Agenda
------

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site
*   Latest News
    *   Martin -- Set up [Test Planning page](./RSE_1.0_Testing "RSE 1.0 Testing"), Finished Release Review Draft
    *   DaveD -- Spent some time on automating tests; problem is that the Framework tries to do everything in the background; Reviewed M4 bugs; Finished IBM work, full time for openRSE now
    *   DaveM -- Drag&Drop / Filetransfer: will look at Navigator PluginTransfer next; might mark it as missing feature for 1.0; will have full time openRSE now
    *   Kushal -- got the code for removing rseConfigDefaults, will attach a migration guide to a bug; passwordPersistence: an IBM team wants the Preference Page - They have customers that have other tooling which makes use of this - bug are OK with removing the extension point as long as the page remains the same.
    *   Javier -- Checked in SD in CVS (org.eclipse.tm.core/discovery); feature for Update Site missing; DaveM has problems, version of EMF? DaveD could do testing, if we decide we want an official
    *   Ted -- This week at Europa Build Symposion; maybe move the meeting 1 hour later
    *   Other News --
*   Upcoming Work
    *   Bug Work is top priority now!
    *   **M4 bugs**: PLEASE REVIEW [M4 BUGS](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&target_milestone=1.0+M4&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit)!!
    *   **New bugs**: REVIEW [Assigned to Inbox](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&emailassigned_to1=1&emailtype1=exact&email1=dsdp.tm.rse-inbox%40eclipse.org&cmdtype=doit), [Status NEW](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=NEW&cmdtype=doit)
    *   **P1/P2 bugs MUST be fixed by Sept. 15!**
        *   Open bugs: [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1),
    *   Source Code Style & Cleanness
        *   Missing / Incomplete Copyrights: Please use the Releng tool from the bottom of the [Eclipse 3.2 Download Page](http://download.eclipse.org/eclipse/downloads/drops/R-3.2-200606291905/index.php) \- See "6. Fix Copyrights"
        *   **Compiler Warnings**: See [Committer Howto](https://www.eclipse.org/dsdp/tm/development/compiler_warnings.php)
        *   **Code Ownership** \- [DSDP/TM/Code Ownership](./Code_Ownership "DSDP/TM/Code Ownership")
            *   DaveD would prefer to have clear ownership
            *   Goal: Encourage integrity of the design, the owner is responsible for a solid extendible design
            *   Even non-owners can make bug fixes, but please let the owner know
            *   Dont make design-breaking changes without letting the owner know
            *   Might add a backup person
            *   Code owners should triage bugs in a timely fashion
            *   Ownership table as help for dispatching bugs
            *   Ownership for cross-package functionality is possible, e.g. File Encodings
        *   **Code Style and Format** \-\- defer to next week
    *   **Change Requests**
        *   Default colors for command view - white background, black or dark blue foreground
        *   Remove rseConfigDefaults extension point - Kushal
        *   Remove passwordPersistence extension point - Kushal
        *   Deprecated getRemoteProperty() --> Document property namespaces, reserve "org.eclipse.rse" namespace
    *   **Features**: Jakarta-commons/Net, JUnit-framework, Discovery, EFS-Experimental, WR-Terminal ([bug 152826](https://bugs.eclipse.org/bugs/show_bug.cgi?id=152826))
    *   **Refactorings**: DaveM did most important stuff; consider "finished" for now, continue with hi-pri bugs
        *   Kushal IConnectorService --> if we can afford after addressing hi-pri bugs
        *   Kushal rseConfigDefaults
        *   Kushal passwordPersistence
    *   API Things
        *   **Service Error Reporting** \- [bug 149472](https://bugs.eclipse.org/bugs/show_bug.cgi?id=149472) \- DaveD - API ok so far, final resolution? --> Create new different bug id for that one.
        *   **Parallel Services** \- [bug 142478](https://bugs.eclipse.org/bugs/show_bug.cgi?id=142478) all queries in background - DaveM
        *   **SystemRegistry.createHost** for Javier
            *   [bug 150168](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150168) dont commit immediately - DaveD
                *   Javier: not important at the moment; DaveD: probably fixed already
            *   [bug 150265](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150265) allow specifying subsystem types - DaveM
                *   Example: 1 Host providing shell and FTP (different categories)
                *   Problem: createHost() only creates a host with 1 service -- See video for service discovery, DaveM to take a look at it
                *   Need createHost() with a list of services
                *   Can wait until hi-pri bugs are fixed.
        *   Making stuff **internal** \- ssh, ftp: Martin; Core: List of candidates from DaveD?
    *   Cleanup: API Doc (duplicates in interface and implementation!), JUnit tests, Context help, Test Plans, RSE-7-migration-docs, Copyrights, licenses
*   Other items
    *   Tutorial: Update at the end of the release process, change instructions (re-use example code: We dont want to teach PDE)
    *   Manual test plans - in work by **Martin**
    *   EFS Experimental feature to be created by Martin
*   Vacations, Holidays etc.
    *   Martin - 2 weeks once the baby is here (around Oct.3, but could also be any time now)
    *   DaveD taking Oct.12-13 off
*   Free discussion -- feelings, comments, critics

  

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_6-Sep-2006#Action_Items "DSDP/TM/Committer Phone Meeting 6-Sep-2006") Action Items
*   **DaveD** \- Sign up on [RSE 1.0 Testing](./RSE_1.0_Testing "RSE 1.0 Testing") page, Hi-Pri bugs. Edit Code Ownership. JUnit. Checkin mappings.csv, New bug for moving DTD, Send "Team" test plans to Martin. SystemRegistry API. Team fixes: Check collapsing persistence Properties nodes to fewer files. Compile a list of suggestions for making classes / packages internal.
*   **DaveM** \- Sign up on [RSE 1.0 Testing](./RSE_1.0_Testing "RSE 1.0 Testing") page, Hi-pri bugs; get rid of Service calls on UI thread; hygiene changes
*   **Kushal** \- Hi-pri bugs; refactoring IConnectorService; send file encoding test resources to martin; review & get rid of rseConfigDefaults; talk to Don about passwordPersistence
*   **Martin** \- Manual test plan, Hi-pri bugs; EFS feature, Build scripts for CDT and Discovery, API Review, Jakarta-commons, WR-terminalview; Review if IShellService is sufficient for terminal
*   **Javier** \- Hook up with Scott Lewis once SD is committed
*   **Ted** \- Sign up on [RSE 1.0 Testing](./RSE_1.0_Testing "RSE 1.0 Testing") page; Report about Build Symposion

  

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 20-Sep-2006](./Committer_Phone_Meeting_20-Sep-2006 "DSDP/TM/Committer Phone Meeting 20-Sep-2006") at 8am PST/10am Rochester/11am Toronto/4pm London/5pm Salzburg - NEW TIME TO HELP TED JOIN
*   Release Review Meeting on [27-Sep-2006 at 8am PDT](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=9&day=27&hour=15&min=0&sec=0&p1=224&p2=421&p3=250&p4=136&p5=223)
*   Open [DSDP/TM/Phone Meeting 4-Oct-2006](./Phone_Meeting_4-Oct-2006 "DSDP/TM/Phone Meeting 4-Oct-2006") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_13-Sep-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_13-Sep-2006))