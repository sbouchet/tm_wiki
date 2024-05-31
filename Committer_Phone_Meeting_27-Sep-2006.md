

DSDP/TM/Committer Phone Meeting 27-Sep-2006
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Sep 27, 2006](./index.php?title=Sep_27,_2006&action=edit&redlink=1 "Sep 27, 2006 (page does not exist)") at [9.00am San Francisco / 11.00am Rochester / 12.00am Toronto / 5.00pm London / 6.00pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=9&day=27&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | Martin to start a Skype conference - you'll be called:   Skype **martin.oberhuber**, ddykstal (or david_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet |

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
*   Wind River - Martin Oberhuber, Ted Williams

Agenda
------

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site
*   Latest News
    *   Martin -- Prepared & released M5 - lots of new features (Commons_Net,Remotecdt,EFS,Discovery); Prepared, organized and joined the [RSE 1.0 Testing](./RSE_1.0_Testing "RSE 1.0 Testing") effort; Release Review (passed!);
    *   DaveD -- Bug reporting & fixing
    *   DaveM -- Bug reporting & fixing
    *   Kushal -- Bug reporting & fixing
    *   Javier -- Bug reporting & fixing
    *   Ted -- Terminalview; need a few more days, Baby is here
    *   Other News --
*   Looking back on [1.0 M5](http://download.eclipse.org/dsdp/tm/downloads/drops/S-1.0M5-200609221723/index.php)
    *   Downloads to-date: 31 (SDK), 10 (win-server), 8 (linux-server), 5 (examples); 5 efs, 4 disscovery; plus 11 from the update site (.pack.gz, +9 .jar)
    *   **Please Review [Bugs assigned to M5 milestone](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&target_milestone=1.0+M5&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit)** and set FIXED as appropriate (or change Target Milestone=1.0 RC1)
    *   Comments?
        *   Javier: Will FTP be tested? - Martin: Yes once the Service uses Commons_Net
        *   Javier will implement the glue from RSE File Service -> Commons_Net
        *   Martin needs to fix the unattended builds
*   Top Priorities this week:
    *   **#1 - Fulfill the testing assignments** (4h each; but not more) - [RSE 1.0 Testing](./RSE_1.0_Testing "RSE 1.0 Testing")
    *   **#2 - Bookkeeping**: Bugzilla M5 bugs status, Bugzilla NEW->ASSIGNED, Code Ownership, Copyright Checks
    *   **#3 - Hi-priority bugfixing**
*   Upcoming Work
    *   **New bugs**: REVIEW [Assigned to Inbox](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&emailassigned_to1=1&emailtype1=exact&email1=dsdp.tm.rse-inbox%40eclipse.org&cmdtype=doit), [Status NEW](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=NEW&cmdtype=doit)
        *   Open bugs: [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1),
        *   DaveD: [150128](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150168) harder than expected, would like to defer: bugfix to persist each of 3 persist-jobs in a row is easier than adding the API for persist on demand
        *   DaveM: [153652](https://bugs.eclipse.org/bugs/show_bug.cgi?id=153652) copy&paste - drag&drop works always, copy&paste fails from remote FS to windows explorer.
            *   Dave & Kushal could not reproduce problems with Drag&Drop files when folders worked
            *   --\> Martin to re-test once Commons_Net builds ok
    *   Communications
        *   We need a **RSE 2.0 Project Plan!** \- Work on the [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") page
            *   Martin to create an empty Milestone Plan in a hidden area of the webserver; DaveD to fill in features for dates
        *   Should we reduce noise on the dsdp-tm-dev list?
            *   **Decision: No - it's a developer list**, so we're going to keep everything public.
            *   Perform feature specific discussions in bugreports
            *   Encourage users to use the newsgroup for questions
                *   Anybody know a good newsreader? Problem is that most dont poll automatically. - Ted: Opera? Any Eclpse Plugin for newsreading?
    *   Source Code Style & Cleanness
        *   Missing / Incomplete Copyrights - **PLEASE FIX NOW**
            *   Please use the Releng tool from the bottom of the [Eclipse 3.2 Download Page](http://download.eclipse.org/eclipse/downloads/drops/R-3.2-200606291905/index.php) \- See the description there: "6. Fix Copyrights"
            *   Martin to post instructions here and in committer HOWTO
        *   **Compiler Warnings**: See [Committer Howto](https://www.eclipse.org/dsdp/tm/development/compiler_warnings.php)
        *   **Code Ownership** \- [DSDP/TM/Code Ownership](./Code_Ownership "DSDP/TM/Code Ownership") \- DaveD to edit
        *   **Code Style and Format**
            *   Not been a focus so far
            *   RSE itself is inconsistent - e.g. if... without {} block is problematic
            *   Use JDT autoformat as much as possible: perhaps define an RSE-style and check in with the projects?
            *   Or use the standard eclipse style: might be problematic when merging RSE7 code into openRSE
                *   DaveD likes the Sun (Eclipse Standard) convention
                *   If one has trouble understanding some code, reformat it on the fly
                *   Historically, some RSE code was generated out of modelling tools; no objection to reformatting
                *   Additional RSE7 stuff merging is not a problem; back-porting bugfixes may be a problem though.
                *   **Decision: wait with auto-formatting until there are no bugfixes to back-port any more**
*   Vacations, Holidays etc.
    *   Martin - 2 weeks once the baby is here (around Oct.3, but could also be any time now)
    *   DaveD taking Oct.12-13 off, 19-20 as well
    *   Canadian Thanksgiving - Oct.9
*   Free discussion -- feelings, comments, critics
    *   Javier - Updatesite: Discovery doesnt work from the update site
        *   Martin: please try downloads, review build.properties
        *   DaveD: What Environment is needed? - Javier: e.g. iTunes, DaveD will test

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_20-Sep-2006#Action_Items "DSDP/TM/Committer Phone Meeting 20-Sep-2006") Action Items
*   **DaveD** \- Testing, Bookkeeping; Edit Code Ownership. Fix Copyrights. Hi-Pri bugs. JUnit. Checkin mappings.csv, New bug for moving DTD, Send "Team" test plans to Martin. SystemRegistry API. Team fixes: Check collapsing persistence Properties nodes to fewer files. Compile a list of suggestions for making classes / packages internal.
*   **DaveM** \- Testing, Bookkeeping; meet Kushal for Dirty Editors. Fix Copyrights. Hi-pri bugs
*   **Kushal** \- Testing, Bookkeeping; Meet DaveM for Dirty Editors; Fix Copyrights. Hi-pri bugs; refactoring IConnectorService; send file encoding test resources to martin;
*   **Martin** \- Testing; Fix Commons_Net unattended build; create empty project plan; re-test drag&drop; Hi-pri bugs; API Review, Review if IShellService is sufficient for terminal
*   **Javier** \- Testing; Hook up FTP Service with Commons/Net; Fix SD build.properties; Hook up with Scott Lewis once SD is committed and works
*   **Ted** \- Care for the baby

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 4-Oct-2006](./Committer_Phone_Meeting_4-Oct-2006 "DSDP/TM/Committer Phone Meeting 4-Oct-2006") at 8am SFO/10.00am Rochester/11.00pm Toronto/4pm London/5pm Salzburg
*   Open [DSDP/TM/Phone Meeting 4-Oct-2006](./Phone_Meeting_4-Oct-2006 "DSDP/TM/Phone Meeting 4-Oct-2006") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_27-Sep-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_27-Sep-2006))