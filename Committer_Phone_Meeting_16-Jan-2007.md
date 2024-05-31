

DSDP/TM/Committer Phone Meeting 16-Jan-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Jan 16, 2007](./index.php?title=Jan_16,_2007&action=edit&redlink=1 "Jan 16, 2007 (page does not exist)") at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=1&day=16&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 Recent Download Statistics](#Recent-Download-Statistics)
    *   [2.2 Latest News](#Latest-News)
    *   [2.3 Upcoming Work](#Upcoming-Work)
    *   [2.4 Communications](#Communications)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave Dykstal, Dave McKnight, Kushal Munir
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber, Michael Scharf, Ted Williams

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help: **being responsive**
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site

### Recent Download Statistics

RSE 1.0 Download statistics as per 16-Jan-2007
| Component | RC3 | RC4 | 1.0 | 1.0.1 | 2.0M4 | Note |
| --- | --- | --- | --- | --- | --- | --- |
| Date | 30-Oct | 03-Nov | 12-Nov | 15-Dec | 4-Jan |  |
| RSE-SDK | 113 | 146 | 469 | 363 | 22 |  |
| rse-runtime-core |  | 14 | 105 | 64 | 4 |  |
| rseserver-windows | 24 | 63 | 190 | 54 | 5 |  |
| rseserver-linux | 19 | 25 | 138 | 53 | 8 |  |
| rse.core (Update Site) | 64 | 52 | 172 | 317 |  | 1.0 src is 156 |
| Total | 177 | 212 | 746 | 744 |  |  |
| examples |  | 27 | 85 | 48 + 177 | 8 |  |
| remotecdt |  | 7 | 66 | 61 + 87 | 13 | per 1.0.1, remotecdt is no longer in SDK |
| discovery |  | 13 | 68 | 39 + 138 | 7 |  |
| efs |  | 12 | 42 | 39 + 162 | 10 |  |
| terminal |  | - | - | 73 + 109 | 13 |  |

*   For previous stats, see [DSDP/TM/Committer Phone Meeting 19-Dec-2006](./DSDP/TM/Committer_Phone_Meeting_19-Dec-2006 "DSDP/TM/Committer Phone Meeting 19-Dec-2006") and [DSDP/TM/Phone Meeting 8-Nov-2006](./DSDP/TM/Phone_Meeting_8-Nov-2006 "DSDP/TM/Phone Meeting 8-Nov-2006")
*   1.0: 85 examples -- people do want to code against RSE APIs
*   68 discovery -- some interest
*   update site gaining significance with 1.0.1, especially for examples, discovery, efs, terminal

### Latest News

| Martin | 50% | EclipseCon tutorial; SVN eval; 2.0 planning; newsgroup-launching; terminal; builds; Platform communications | 50% |
| --- | --- | --- | --- |
| DaveD | 80% | UI/Non-UI; Got UserActions into IBM legal; Design for Persistence | 80% |
| DaveM | 60% | EclipseCon tutorial; fixed some bugs related to SimpleCommands; read-only flags; | 70% |
| Kushal | 0% | Encodings | 0% |
| Javier | 20% | Preparing the PluginFest | 20% |
| Ted | 0% |  | 0% |
| Uwe | 0% | Filing bugs | 0% |
| Michael | 20% | Terminal record&play, performance; | 0% |

*   Connection Testcases and Montavista Processes accepted by EMO

### Upcoming Work

*   **Top priority** this week is getting started with the "big rocks" in bugzilla, for [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning")
    *   add **unit tests** for all new or modified API
*   [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning")
    *   **1\. Make APIs usable for clients, harden the APIs, improve documentation**
        *   UI/Non-UI separation (Condition of Satisfaction: be able to do a headless launch; try to reduce number of plugins? - DaveM be able to use service layer without profiles, persistence etc.; DaveM could envision service layer as part of ECF or similar; put subsystem.files together with subsystem.files)
        *   Be able to do ssh non-ui only? Would need an API for password / passphrase prompting in RSE core.
        *   SystemType improvements; retargetable actions/commands;
        *   read-only flags \[java.io: cannot change a file to read-only;\] want a capability API for services to report if they can set r-o or not? - Not yet, just report an error.
        *   timestamp, ro-flags: still TBD for ssh and ftp
        *   Streams for IHostShell, IFileService - upload already allows an InputStream; download will need new API; may be a problem for dstore since the agent "pushes" the file; ftp allows canceling the download
        *   Asynchronous API/callbacks; How is the client informed about job completion? Event? Callback? Progressmonitor? - Progressmonitor is created by the job typically, so we have no control over the progress \[could use a SubProgressMonitor\]? Use Java5 Concurrency classes?
        *   IHostShell changes for Terminal;
    *   **2\. Make EFS work**
        *   Kushal looking at it - problem is the strictness of resource locking / scheduling rules
    *   **3\. Play well with the Platform**
        *   retargetable actions/commands; capabilities; icu4j; Orbit; ssh prefs; drag&drop
    *   **4\. Improve overall quality (unit tests; special characters; long filenames; background jobs; parallel access; logging; ...)**
    *   **5\. New Features**
        *   Import/Export & User actions; Terminal-in-rse; Persistence-as-xmlfile; Service enablement
*   Think about **limiting the API**: Make APIs internal along the way of updating documentation, and making Unit tests, we'll see some API we want "internal".
    *   Remove RSE Performance Logging; place contents of logging into core
    *   Reduce number of plugins (once UI/Non-UI separation is done, have e.g. ssh.core and ssh.ui but not more)
*   Add Montavista shell processes subsystem
*   Add DaveM's multishell? - Could help with Terminal integration;
    *   would need lots of cleanup; would raise questions why there are two shellviews;
    *   better wait for cleaner grouping concepts to come next year
*   **Fix N-builds** (second workspace, use Ted's scripts)
    *   Orbit bundles to be added differently
    *   Unittests to run every night
    *   Version Number Changes to be done by Martin
    *   Copyright Year Changes
*   For bugs, see the [bug process page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) (assigned to inbox, plan items, status new, hi-priority, API, open with patch)
*   **Compiler Warnings**
    *   Good progress, please continue. See the [Committer Howto](https://www.eclipse.org/dsdp/tm/development/committer_howto.php#check_code) for settings
        *   109 -> 113 -> 113 -> 3 connectorservice.dstore
        *   176 -> 265 -> 161 -> 12 rse.core
        *   474 -> 558 -> 558 -> 94 files.ui
        *   637 -> 662 -> 662 -> 23 services
        *   221 -> 250 -> 248 -> 27 subsystems.files.core
        *   1622 -> 346 -> 293 -> 192 rse.ui
*   **Quality**
    *   **Docs are a high priority**. Add ISV Javadoc where it is still missing or incorrect; review, and improve all docs

### Communications

*   General code cleanup -- to do right after M4:
    *   Get rid of unused icons, e.g. rse.ui/icons/full/obj16/system390\_obj.gif, IBM\_logo.gif
    *   Get rid of commented out source code
    *   Get rid of unused properties (chkpii)
*   Change Requests
*   Vacations, Holidays etc.
    *   Michael travelling next 2 weeks
    *   Kushal busy with IBM until Jan.19
    *   DaveD going to Chicago end of the month; Florida in February for a week
*   Free discussion -- feelings, comments, critics

Action Items
------------

*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_9-Jan-2007#Action_Items "DSDP/TM/Committer Phone Meeting 9-Jan-2007") Action Items
*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_2-Jan-2007#Action_Items "DSDP/TM/Committer Phone Meeting 2-Jan-2007") Action Items
*   **DaveD** \- Remove RSE Performance Logging; Refactoring UI/Non-UI; Persistence; Bugzilla bug for User Actions Contribution until Jan.31st; Bugs & Unit tests;
*   **DaveM** \- EclipseCon; Bugs & Unit tests; finish permission API; download Streams API;
*   **Kushal** \- Encodings; EFS; Talk to DaveD re Comm Server; Bugs & Unit Tests
*   **Martin** \- Check r/o flags and timestamps for ssh; Commit Montavista contrib; Fix build; EclipseCon tutorial; Bugs & Unit Tests; Plan Item Specifications; Personal Interviews via Skype; Work on [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning"); [TM and RSE FAQ](./TM_and_RSE_FAQ "TM and RSE FAQ"), improve Wiki and Website (how to contribute);
*   **Javier** \- Check r/o flags and timestamps for ftp; FTP passive mode; Bugs & Unit Tests,
*   **Ted** -
*   **Michael** \- Terminal Performance Improvements
*   **Uwe** -

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 30-Jan-2007](./DSDP/TM/Committer_Phone_Meeting_30-Jan-2007 "DSDP/TM/Committer Phone Meeting 30-Jan-2007") at [1700 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=1&day=30hour=17&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) (2 weeks due to Symbian PluginFest; 1 hr later due to Orbit call)
*   Open [DSDP/TM/Phone Meeting 7-Feb-2007](./DSDP/TM/Phone_Meeting_7-Feb-2007 "DSDP/TM/Phone Meeting 7-Feb-2007") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_16-Jan-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_16-Jan-2007))