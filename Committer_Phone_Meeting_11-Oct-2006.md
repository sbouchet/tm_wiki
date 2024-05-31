

DSDP/TM/Committer Phone Meeting 11-Oct-2006
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday Oct 11, 2006 at [8.00am San Francisco / 10.00am Rochester / 11.00am Toronto / 4.00pm London / 5.00pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=10&day=11&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+1 314-655-1411**   North America **+1 877-422-0035** (toll free)   Passcode: **764918** |

Skype fallback dial-in - only if less than 5 participants:  
DaveD to start a Skype chat- you'll be called:  
Skype **martin.oberhuber**, ddykstal (or david_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, uwe.stieber

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave Dykstal, Dave McKnight, Kushal Munir
*   Wind River - Ted Williams

Agenda
------

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site
*   Latest News
    *   Martin -- still on leave
    *   DaveD -- Continuing work on bugs, testing, bookkeeping, builds
    *   DaveM -- Working on read/dispatch bug from Michael S. (critical P1)
    *   Kushal -- Working on bugs, testing
    *   Javier -- not available
    *   Ted -- will get to testing today
    *   Uwe -- not available
    *   Michael -- Attending Eclipse Summit today
    *   Other News --
*   Top Priorities from the previous week:
    *   **#1 - Bookkeeping**: Copyright Checks
    *   **#2 - Hi-priority bugfixing**
*   Upcoming Work
    *   **New bugs**: REVIEW [Assigned to Inbox](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&emailassigned_to1=1&emailtype1=exact&email1=dsdp.tm.rse-inbox%40eclipse.org&cmdtype=doit), [Status NEW](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=NEW&cmdtype=doit)
        *   Open bugs: [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1),
        *   DaveD: [150128](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150168) harder than expected, would like to defer: bugfix to persist each of 3 persist-jobs in a row is easier than adding the API for persist on demand
        *   DaveM: [153652](https://bugs.eclipse.org/bugs/show_bug.cgi?id=153652) copy&paste - drag&drop works always, copy&paste fails from remote FS to windows explorer.
            *   Dave & Kushal could not reproduce problems with Drag&Drop files when folders worked
            *   --\> Martin to re-test once Commons_Net builds ok
    *   Communications
        *   We need a **RSE 2.0 Project Plan!** \- Work on the [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") page (not discussed)
            *   Martin to create an empty Milestone Plan in a hidden area of the webserver; DaveD to fill in features for dates
    *   Source Code Style & Cleanness (not discussed)
        *   Missing / Incomplete Copyrights - fixes look good, please use UTF-8 as character set for projects
        *   **Compiler Warnings**: See [Committer Howto](https://www.eclipse.org/dsdp/tm/development/compiler_warnings.php)
        *   **Code Ownership** \- [DSDP/TM/Code Ownership](./Code_Ownership "DSDP/TM/Code Ownership") \- DaveD to edit (for self).
            *   Propose FTP to be transferred from Martin to Javier (OK)
            *   Propose CDT Launcer to be transferred from Martin to Ewa (OK with committers, DaveD to clear with Ewa)
    *   **Change Requests**
        *   SystemRegistry.getTheSystemRegistry() vs. RSEUIPlugin.getSystemRegistry()
        *   Default colors for command view - white background, black or dark blue foreground
        *   Remove rseConfigDefaults extension point - Kushal
        *   Remove passwordPersistence extension point - Kushal
        *   Deprecated getRemoteProperty() --> Document property namespaces, reserve "org.eclipse.rse" namespace
    *   **Features**: Jakarta-commons/Net, JUnit-framework, Discovery, EFS-Experimental, WR-Terminal ([bug 152826](https://bugs.eclipse.org/bugs/show_bug.cgi?id=152826))
    *   **Refactorings**: DaveM did most important stuff; consider "finished" for now, continue with hi-pri bugs
        *   SystemRegistry.getTheSystemRegistry() vs. RSEUIPlugin.getSystemRegistry() -- need to keep this for now
        *   Kushal IConnectorService --> if we can afford after addressing hi-pri bugs
    *   API Things
        *   **Service Error Reporting** \- [bug 149472](https://bugs.eclipse.org/bugs/show_bug.cgi?id=149472) \- DaveD - API ok so far, final resolution? --> Create new different bug id for that one.
        *   **Parallel Services** \- [bug 142478](https://bugs.eclipse.org/bugs/show_bug.cgi?id=142478) all queries in background - DaveM
        *   **SystemRegistry.createHost** for Javier
            *   [bug 150168](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150168) dont commit immediately - DaveD
                *   Javier: not important at the moment; DaveD: probably fixed already (Still under investigation)
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
*   Vacations, Holidays etc.
    *   Martin - 2 weeks once the baby is here (October 1st!)
    *   Javier taking Oct 12-13.
    *   DaveD taking Oct.12-13 off, 20 as well
*   Free discussion -- feelings, comments, critics
    *   EclipseCon 2007 coming in March. Call for Papers has been issued. Martin (and perhaps DaveM) will submit proposal for 2 hour tutorial.

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_4-Oct-2006#Action_Items "DSDP/TM/Committer Phone Meeting 4-Oct-2006") Action Items
*   **DaveD** \- Testing, Edit Code Ownership. Hi-Pri bugs. JUnit. Checkin mappings.csv, New bug for moving DTD, Send "Team" test plans to Martin. SystemRegistry API. Compile a list of suggestions for making classes / packages internal. Check with Ewa regarding CDT Remote Launch
*   **DaveM** \- Testing, Bookkeeping; meet Kushal for Dirty Editors. Fix Copyrights. Hi-pri bugs
*   **Kushal** \- Testing, Bookkeeping; Meet DaveM for Dirty Editors; Fix Copyrights. Hi-pri bugs; refactoring IConnectorService; send file encoding test resources to martin;
*   **Martin** \- Care for baby; create empty project plan; re-test drag&drop; Hi-pri bugs; API Review, Review if IShellService is sufficient for terminal
*   **Javier** \- Hook up with Scott Lewis once SD is committed and works
*   **Ted** \- Care for the baby; Terminalview; Document the build process

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 18-Oct-2006](./Committer_Phone_Meeting_18-Oct-2006 "DSDP/TM/Committer Phone Meeting 18-Oct-2006") at 8am SFO/10.00am Rochester/11.00pm Toronto/4pm London/5pm Salzburg


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_11-Oct-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_11-Oct-2006))