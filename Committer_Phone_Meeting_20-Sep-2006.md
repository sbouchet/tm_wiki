

DSDP/TM/Committer Phone Meeting 20-Sep-2006
===========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Sep 20, 2006](/index.php?title=Sep_20,_2006&action=edit&redlink=1 "Sep 20, 2006 (page does not exist)") at [8.00am San Francisco / 10.00am Rochester / 11.00am Toronto / 4.00pm London / 5.00pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=9&day=20&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Primary Dial-in: | **+44 (0)1452 567588** |
| USA Freephone Dial-In: | +1 (866) 6161738 |
| UK National Dial-In: | 08712460713 |
| Passcode: | **0587322148 #** |

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave Dykstal, Dave McKnight, Kushal Munir
*   Wind River - Martin Oberhuber, Ted Williams
*   (Symbian - Javier Montalvo Orús - vacation)

Agenda
------

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site
*   Latest News
    *   Martin -- Updated the [Committer HOWTO](https://www.eclipse.org/dsdp/tm/development/committer_howto.php): Counting lines of code, bug states; Checked in Jakarta Commons Net and Ewas Launch Patch; Release Review Slides; Checked IP-Log... Will we need EMO for [144226 dstore spirit patch](https://bugs.eclipse.org/bugs/show_bug.cgi?id=144226)? \- No
    *   DaveD -- Bug work, formatting and fixing javadoc along the way; fixed macbugs, working on profile/team stuff now
    *   DaveM -- Bug work, e.g. dstore shell exit problem - harder than expected, output readers dont get notified
    *   Kushal -- IBM & Bug work; might need a "Refresh completed" event - Dave and Kushal to discuss this together; rseConfigDefaults removed from ISV docs, but other refactorings not complete yet
    *   Javier -- Vacation
    *   Ted -- Europa Build Symposion
        *   [https://wiki.eclipse.org/index.php/Europa\_Build\_Workshop_Report](https://wiki.eclipse.org/index.php/Europa_Build_Workshop_Report)
        *   Recommended to use buckminster as much as possible, as a build tool replacing ant
        *   Complaints regarding build process - docs is 34 pages, which are the 3 that everyone wants?
        *   All projects are encouraged to have Wiki updated with instructions how to build everyting from source
        *   All projects to have RSS feeds in place by January
        *   Separate the Build from the Publish
        *   **Terminalview**: want to have something checked in early next week
    *   Other News --
*   Upcoming Work
    *   **Testing** and Bug Work are top priorities this week.
        *   Sign up on the [RSE 1.0 Testing](/RSE_1.0_Testing "RSE 1.0 Testing") page!
        *   Sanity testing I-builds towards M5/RC0: install + 30 minutes
            *   Test Update Site at [http://download.eclipse.org/dsdp/tm/testUpdates/](http://download.eclipse.org/dsdp/tm/testUpdates/)
            *   Martin: Windows XP, Sun j2sdk1.4.2_12, Dstore-Linux, Dstore-unix; normal download minimal install
            *   DaveD: Mac, Mac-local, Dstore-local-mac, ssh, dstore; probably Team example (go through tutorial); updateSite; core-install first, upgrade to sdk later
            *   DaveM: Linux, Linux-local, Dstore-windows, ; normal download
            *   Kushal: Linux, Linux-local, dstore-aix, ssh; updateSite;
            *   Ted: Windows, ssh, ftp; normal download SDK
    *   **New bugs**: REVIEW [Assigned to Inbox](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&emailassigned_to1=1&emailtype1=exact&email1=dsdp.tm.rse-inbox%40eclipse.org&cmdtype=doit), [Status NEW](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=NEW&cmdtype=doit)
    *   Focus on **Stabilization** now. Its ok to have a few P2 bugs. Dont destabilize while we are approaching M5/RC0.
        *   Open bugs: [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1),
        *   Kushal, DaveM to set status ASSIGNED for their new bugs
        *   DaveD: [150128](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150168) harder than expected, would like to defer: bugfix to persist each of 3 persist-jobs in a row is easier than adding the API for persist on demand
        *   DaveM: [153652](https://bugs.eclipse.org/bugs/show_bug.cgi?id=153652) copy&paste - drag&drop works always, copy&past fails from remote FS to windows explorer
        *   How to defer bugs - lowering priority vs. RESOLUTION=LATER: See the [Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) available from the [Committer Howto](https://www.eclipse.org/dsdp/tm/development/committer_howto.php)
    *   **Test Signup** on [RSE 1.0 Testing](/RSE_1.0_Testing "RSE 1.0 Testing")
    *   Source Code Style & Cleanness
        *   Missing / Incomplete Copyrights: Please use the Releng tool from the bottom of the [Eclipse 3.2 Download Page](http://download.eclipse.org/eclipse/downloads/drops/R-3.2-200606291905/index.php) \- See "6. Fix Copyrights"
        *   Component owners please run the tool
        *   **Compiler Warnings**: See [Committer Howto](https://www.eclipse.org/dsdp/tm/development/compiler_warnings.php)
        *   **Code Ownership** \- [DSDP/TM/Code Ownership](/DSDP/TM/Code_Ownership "DSDP/TM/Code Ownership")
        *   **Code Style and Format** \- defer once more :-)
    *   **Change Requests**
        *   SystemRegistry.getTheSystemRegistry() vs. RSEUIPlugin.getSystemRegistry() -- due to pragmatic refactoring, not possible to fix rightnow
    *   **Features**: Jakarta-commons/Net, JUnit-framework, Discovery, EFS-Experimental, WR-Terminal ([bug 152826](https://bugs.eclipse.org/bugs/show_bug.cgi?id=152826))
        *   Making stuff **internal** \- ssh, ftp: Martin; Core: List of candidates from DaveD?
    *   Cleanup: API Doc (duplicates in interface and implementation!), JUnit tests, Context help, Test Plans, RSE-7-migration-docs, Copyrights, licenses
*   Other items
    *   Tutorial: Update at the end of the release process, change instructions (re-use example code: We dont want to teach PDE)
    *   Manual test plans - in work by **Martin**
    *   EFS Experimental feature to be created by Martin
*   Vacations, Holidays etc.
    *   Martin - 2 weeks once the baby is here (around Oct.3, but could also be any time now)
    *   DaveD taking Oct.12-13 off, 19-20 as well
*   Free discussion -- feelings, comments, critics

  

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_13-Sep-2006#Action_Items "DSDP/TM/Committer Phone Meeting 13-Sep-2006") Action Items
*   **DaveD** \- Sign up on [RSE 1.0 Testing](/RSE_1.0_Testing "RSE 1.0 Testing") page, Edit Code Ownership. Fix Copyrights. Sanity-check I-build, Hi-Pri bugs. JUnit. Checkin mappings.csv, New bug for moving DTD, Send "Team" test plans to Martin. SystemRegistry API. Team fixes: Check collapsing persistence Properties nodes to fewer files. Compile a list of suggestions for making classes / packages internal.
*   **DaveM** \- ASSIGN or reassign your NEW bugs; Sign up on [RSE 1.0 Testing](/RSE_1.0_Testing "RSE 1.0 Testing") page, meet Kushal for Dirty Editors. Fix Copyrights. Sanity-check I-build, Hi-pri bugs, Safe bugs; hygiene changes
*   **Kushal** \- ASSIGN or reassign your NEW bugs; Meet DaveM for Dirty Editors; Fix Copyrights. Sanity-check I-build, Hi-pri bugs, Safe bugs; refactoring IConnectorService; send file encoding test resources to martin; review & get rid of rseConfigDefaults; talk to Don about passwordPersistence
*   **Martin** \- Verify [153652](https://bugs.eclipse.org/bugs/show_bug.cgi?id=153652); Manual test plan, Create I-build; Bugfixes; EFS feature, Build scripts for CDT and Discovery, API Review, Jakarta-commons; Review if IShellService is sufficient for terminal
*   **Javier** \- Hook up with Scott Lewis once SD is committed
*   **Ted** \- Sanity-check I-build; Terminalview; Document build process

  

Next Meeting
------------

*   Release Review Meeting on [27-Sep-2006 at 8am PDT/11am Toronto/4pm London/5pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=9&day=27&hour=15&min=0&sec=0&p1=224&p2=421&p3=250&p4=136&p5=223)
*   [DSDP/TM/Committer Phone Meeting 27-Sep-2006](/DSDP/TM/Committer_Phone_Meeting_27-Sep-2006 "DSDP/TM/Committer Phone Meeting 27-Sep-2006") at 9am SFO/11.00am Rochester/12.00pm Toronto/5pm London/6pm Salzburg : 1 HOUR LATER DUE TO RELEASE REVIEW
*   Open [DSDP/TM/Phone Meeting 4-Oct-2006](/DSDP/TM/Phone_Meeting_4-Oct-2006 "DSDP/TM/Phone Meeting 4-Oct-2006") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_20-Sep-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_20-Sep-2006))