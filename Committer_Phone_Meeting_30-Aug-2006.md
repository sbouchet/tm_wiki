

DSDP/TM/Committer Phone Meeting 30-Aug-2006
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Aug 30, 2006](./index.php?title=Aug_30,_2006&action=edit&redlink=1 "Aug 30, 2006 (page does not exist)") at [8.30am Rochester / 9.30am Toronto / 2.30pm London / 3.30pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=8&day=30&hour=13&min=30&sec=0&p1=223&p2=250&p3=421&p4=136&iv=1800) |
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
*   (Symbian - Javier Montalvo Orús - vacation)
*   Wind River - Martin Oberhuber

Agenda
------

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site
*   Latest News
    *   Martin -- compiler warnings, extension point cleanup (*.exsd doc), scheduled release review
        *   Found [Wicked Shell](http://eclipse-plugins.info/eclipse/plugin_details.jsp?id=1392), will try to ask the developer to join RSE; want to make RSE Local Shell as slick as possible, so the developer is likely to join us!
    *   DaveD -- not much time this week, JUnit submitted
    *   DaveM -- not much time either, fixed a few bugs, going to do drag&drop next
    *   Kushal -- not much time either;
        *   rseConfigDefaults: IBM specific config.ini, setting System Properties; Kushal to **document this** (Reference docs for System Properties in ISV docs); Write Migration docs for IBM;
        *   passwordPersistence: Dont allow password add/edit on the Prefs page, only remove. Do any IBM products (TPF) pre-populate the passwords? - Kushal to find out. Martin: probably use an "earlyStartup" extension point?
        *   refactoring: persistence provider is very tightly integrated with model objects like filters, IHost, ISystemProfile etc. Can we move the interfaces only for now? - This would be a first step on the path.
            *   **DaveM to try moving interfaces on Thursday; others, NO CHECKIN on Thursday!**
    *   Javier -- vacation
    *   Other News --
*   Upcoming Work
    *   **M4 bugs**: PLEASE REVIEW [M4 BUGS](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&target_milestone=1.0+M4&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit)!!
    *   **Inbox**: REVIEW [Assigned to Inbox](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&emailassigned_to1=1&emailtype1=exact&email1=dsdp.tm.rse-inbox%40eclipse.org&cmdtype=doit)
    *   **Timing**: Martin on vacation most of October; Release Review Sept.27, M5 is Sept.22
        *   Martins fixes will be in by Sept.27; manual test plans will exist
        *   Executing the test plans, and bugfixing after that to be done by IBM mostly
        *   Currently 142 bugs open, 18 P1/P2: P1/P2 bugs MUST be fixed by Sept. 15!
    *   **Source Code Style & Cleanness**
        *   We deliver not only a "working product" but also source code
        *   Clean source code increases contributor confidence, improves code readability, helps avoiding bugs
        *   **Compiler Warnings**: See [Committer Howto](https://www.eclipse.org/dsdp/tm/development/compiler_warnings.php)
            *   Currently 484 Java warnings + 642 Javadoc warnings (Martin already fixed about 150 + 250)
            *   Find bugs, Fix javadoc
            *   Dont chase the warnings (yet) but fix them while you are working: You can apply a filter in the Problems view if you want, e.g. "don't show String Javadoc:"
            *   No more checkins of code with warnings (may be checked automatically in the future)
            *   Be **careful** when fixing warnings: assume side effects of method calls!
        *   **Code Ownership**:
            *   It is beneficial to have clear ownership and responsibility
            *   External contributors can also be owners, but have an associated committer as well
            *   See (and edit) [DSDP/TM/Code Ownership](./Code_Ownership "DSDP/TM/Code Ownership")
            *   Martin to take Ssh, Releng; Examples; FTP, Local, Contentassist for now
        *   **Code Style and Format** \- deferred to next meeting
    *   **Change Requests**
        *   Default colors for command view - white background, black or dark blue foreground - accepted
        *   Deprecated getRemoteProperty() --> Document property namespaces, reserve "org.eclipse.rse" namespace - deferred to next meeting
    *   **Features**: Jakarta-commons, JUnit-framework, Discovery, EFS-Experimental, WR-Terminal ([bug 152826](https://bugs.eclipse.org/bugs/show_bug.cgi?id=152826))
    *   **Refactorings**: This week we should really be done!
        *   Subsystem Factory vs. Configuration: Going with Configuration for now, Martin started renaming *factory where he found it while working on compiler warnings.
        *   Kushal IConnectorService - Its not only the ConnectorService. DaveM to try moving the interfaces.
    *   **Bug Work - please observe priorities**
        *   DaveD: Team stuff
        *   Open bugs: [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1),
    *   Legal: JUnit (next monday?); Jakarta-commons (deferred!); WR Terminalview (passed!)
*   Other items
    *   Tutorial: Update at the end of the release process, change instructions (re-use example code: We dont want to teach PDE)
    *   Manual test plans - in work by **Martin**
    *   EFS Experimental feature to be created by Martin
*   Free discussion -- feelings, comments, critics
    *   Want to do a committer call next week in addition to the open call
    *   Monday - Labor Day in US + Canada

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_23-Aug-2006#Action_Items "DSDP/TM/Committer Phone Meeting 23-Aug-2006") Action Items
*   **DaveD** \- JUnit, Review bugs assigned to M4, Checkin mappings.csv, New bug for moving DTD, Send "Team" test plans to Martin. SystemRegistry API for Javier. Team fixes: Check collapsing persistence Properties nodes to fewer files. Compile a list of suggestions for making classes / packages internal.
*   **DaveM** \- Refactoring Interfaces on Thursday; bug fixing by priority
*   **Kushal** \- implement rseConfigDefaults changes; ask TPF regarding passwordPersistence changes; Review bugs assigned to M4, refactoring together with DaveM; send file encoding test resources to martin; bug fixing
*   **Martin** \- Contact WickedShell developer, Prepare Release Review Slides, Initial checkin of discovery, EFS feature, Build scripts for CDT and Discovery, Manual test plan, API Review, Jakarta-commons, WR-terminalview; Review if IShellService is sufficient for terminal
*   **Javier** \- vacation; hook up with Scott Lewis once SD is committed
*   **Everyone** -
    *   **Setup [Compiler Warnings](https://www.eclipse.org/dsdp/tm/development/compiler_warnings.php) in your Workspaces**
    *   **Update [DSDP/TM/Code Ownership](./Code_Ownership "DSDP/TM/Code Ownership")**;
    *   **NO CHECKINS ON THURSDAY**;
    *   List obsolete API on [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") page

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 6-Sep-2006](./Committer_Phone_Meeting_6-Sep-2006 "DSDP/TM/Committer Phone Meeting 6-Sep-2006") at 9.30am Toronto
*   Open [DSDP/TM/Phone Meeting 6-Sep-2006](./Phone_Meeting_6-Sep-2006 "DSDP/TM/Phone Meeting 6-Sep-2006") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_30-Aug-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_30-Aug-2006))