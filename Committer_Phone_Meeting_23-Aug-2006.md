

DSDP/TM/Committer Phone Meeting 23-Aug-2006
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Aug 23, 2006](./index.php?title=Aug_23,_2006&action=edit&redlink=1 "Aug 23, 2006 (page does not exist)") at [8.30am Rochester / 9.30am Toronto / 2.30pm London / 3.30pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=8&day=16&hour=13&min=30&sec=0&p1=223&p2=250&p3=421&p4=136&iv=1800) |
| Skype Dial-in: | **+99008275601400** (this call is **free** from Skype) |
| Fixed-line Dial-in: | US, call **1-712-432-4000** (long distance charges)    Austria: **0820 400 01562** (national call charges)   In UK: **0870 119 2350** (national call charges)   |
| Passcode: | **5601400** |

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
*   (Symbian - Javier Montalvo Orús - vacation)
*   Wind River - Martin Oberhuber

Agenda
------

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site
*   Latest News
    *   Martin -- Finished up M4: New "Getting Started" tutorial, updated update site, website, blog; some ssh fixes; sort of prepared the nightly build for unit tests (using "basebuilder"), but some work to be done
    *   DaveD -- JUnit to be integrated today; scripting framework for "semi-automated" tests
    *   DaveM -- Some defects (drag&drop)
    *   Kushal -- RSE7 fixes (till thursday), Refactoring
    *   Javier -- vacation
    *   Other News --
*   Looking back on [M4](http://download.eclipse.org/dsdp/tm/downloads/drops/S-1.0M4-200608182355/index.php)
    *   Downloads to-date: 42 (SDK), 10 (win-server), 6 (examples), 5 (linux-server); plus 16 from the update site
    *   Advertisments: What will be our next steps? - [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") page
        *   Probably build RSE 1.1 in december, probably out of the HEAD stream.
    *   [Bugs assigned to M4 milestone](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&target_milestone=1.0+M4&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit)
    *   Comments?
*   Upcoming Work
    *   [M5 plan - Sep 22](https://www.eclipse.org/dsdp/tm/development/plan.php#M5): Localization, API Polish, Avoid Platform internal access, JUnit\]
        *   Localization not an issue for 1.0
    *   **Be Bold:** Address "big rocks", major or risky changes, structure changes/additions at the beginning of this milestone iteration!
    *   **Be Smart:** Add JUnit early!
    *   Release Review to be scheduled Wed, Sep.27. Any P1,P2 bug we have by then needs explanation.
    *   **Features**: Jakarta-commons, JUnit-framework, Discovery, EFS-Experimental, WR-Terminal ([bug 152826](https://bugs.eclipse.org/bugs/show_bug.cgi?id=152826))
    *   **Refactorings**: 2 more weeks, then we should really be done!
        *   Kushal IConnectorService
        *   Subsystem Factory vs. Configuration: API most probably to change by 2.0 so dont invest too much right now. Make a note that the name is in transition ("factory..configuration") in the ISV docs (not the javadoc) - architecture overview
    *   **Drag & Drop** \- DKM
    *   API Things
        *   **Service Error Reporting** \- [bug 149472](https://bugs.eclipse.org/bugs/show_bug.cgi?id=149472) \- DaveD - API ok so far, final resolution? --> Create new different bug id for that one.
        *   **Parallel Services** \- [bug 142478](https://bugs.eclipse.org/bugs/show_bug.cgi?id=142478) all queries in background - DaveM
        *   **SystemRegistry.createHost** for Javier
            *   [bug 150168](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150168) dont commit immediately - DaveD
            *   [bug 150265](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150265) allow specifying subsystem types - DaveM - wait for Javier to return
        *   Making stuff **internal** \- ssh, ftp: Martin; Core: List of candidates from DaveD?
        *   Simple API enhancements from bugzilla? - Most can be deferred to later; Martin to review and update priority if needed.
        *   Obsolete API that's in the Platform now --> See [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") page
            *   Martin wants to get rid of obsolete code for 1.0 if possible
            *   Kushal to investigate rseConfigDefaults
            *   popupMenus extension point - because we are not dealing with Eclipse Resources; makes it a bit easier to define filters; to be reviewed again for 2.0
            *   passwordPersistence: Kushal to chat with Don and find out what these are for (Password Preference Page: Add password button)
    *   Cleanup: API Doc (duplicates in interface and implementation!), *.exsd doc, JUnit tests, Context help, Test Plans, RSE-7-migration-docs, Copyrights, licenses
    *   **Bug Work - please observe priorities**
        *   DaveD: Team stuff
            *   Martin doesnt understand how Profiles, Filter pools etc. are intded to work, therefore cannot write test plans... perhasp DaveD's old test plans could help?
        *   Open bugs: [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1),
    *   Legal: JUnit (to be checked in today!); Jakarta-commons (TBD aug.24 latest); WR Terminalview
*   Other items
    *   Tutorial: Update at the end of the release process, change instructions (re-use example code: We dont want to teach PDE)
    *   Manual test plans - in work by **Martin**
    *   EFS Experimental feature to be created by Martin
*   Free discussion -- feelings, comments, critics

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_16-Aug-2006#Action_Items "DSDP/TM/Committer Phone Meeting 16-Aug-2006") Action Items
*   **DaveD** \- JUnit, Review bugs assigned to M4, Checkin mappings.csv, New bug for moving DTD, Send "Team" test plans to Martin. SystemRegistry API. Team fixes: Check collapsing persistence Properties nodes to fewer files. Compile a list of suggestions for making classes / packages internal.
*   **DaveM** \- bug fixing by priority; look at Kushal's bugs and assign yourself; get rid of Service calls on UI thread; hygiene changes
*   **Kushal** \- Review bugs assigned to M4, refactoring IConnectorService / Persistence provider (send out proposal); send file encoding test resources to martin; review & get rid of rseConfigDefaults; talk to Don about persistenceProvider; bug fixing
*   **Martin** \- EFS feature, Add Discovery, Build scripts, Manual test plan, API Review, Jakarta-commons, WR-terminalview; Review if IShellService is sufficient for terminal
*   **Javier** \- vacation; hook up with Scott Lewis once SD is committed
*   **Everyone** \- List obsolete API on [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") page

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 30-Aug-2006](./Committer_Phone_Meeting_30-Aug-2006 "DSDP/TM/Committer Phone Meeting 30-Aug-2006") at 9.30am Toronto
*   Open [DSDP/TM/Phone Meeting 6-Sep-2006](./Phone_Meeting_6-Sep-2006 "DSDP/TM/Phone Meeting 6-Sep-2006") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_23-Aug-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_23-Aug-2006))