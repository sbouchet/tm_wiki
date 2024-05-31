

DSDP/TM/Committer Phone Meeting 28-Feb-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Feb 28, 2007](./index.php?title=Feb_28,_2007&action=edit&redlink=1 "Feb 28, 2007 (page does not exist)") at [1430 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=2&day=28&hour=14&min=30&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 Looking back on TM 2.0M5](#Looking-back-on-TM-2.0M5)
    *   [2.2 News & Review Action Items](#News-.26-Review-Action-Items)
    *   [2.3 Upcoming Work](#Upcoming-Work)
    *   [2.4 Other Stuff to Do](#Other-Stuff-to-Do)
    *   [2.5 Communications](#Communications)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave McKnight, Dave Dykstal, Kushal Munir
*   Symbian - (Javier Montalvo Orús n/a)
*   Wind River - Martin Oberhuber, Uwe Stieber, (Michael Scharf n/a, Ted Williams n/a)

Notes
-----

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help: **being responsive**
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site

### Looking back on TM 2.0M5

*   THANKS to the entire team!
    *   Kushal finished the first **plan item**, and made good progress on the second one
    *   First actual bug **discovered by a JUnit test**
    *   Everybody worked very focused on hi-priority things - **first things first**
    *   Doing [Release Notes](http://download.eclipse.org/dsdp/tm/downloads/drops/S-2.0M5-200702240204/buildNotes.php) was fun thanks to excellent bugzilla \[api\] documentation (everything captured in bugzilla)
    *   Testing effort was split up among the entire team
    *   Even though some fixes came late (NewConnectionWizard with hickups; Systemview IContextObject; userdoc issues due to M5; missing isv docs) we did an excellent job in testing
*   Some [TM 2.0 M5 Testing](./TM_2.0_M5_Testing "TM 2.0 M5 Testing") statistics:
    *   94 bugs fixed for M5, including 28 API bugs (66 verified/closed, 28 not (yet) verified)
    *   [79 new bugs opened](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=resolution&y_axis_field=reporter&z_axis_field=&query_format=report-table&classification=DSDP&product=Target+Management&chfieldfrom=2007-02-20&chfieldto=2007-02-25&chfield=%5BBug+creation%5D&chfieldvalue=&format=table&action=wrap) during testing; **of these, 33 were resolved during testing** and 5 more this week - great contributions from everyone
        *   only 3 duplicates and 2 WORKSFORME during testing
        *   only 6 bugs reopened during testing

*   Comments:
    *   DaveD - working in Airports etc. was kind of weird but fun (used "BBEdit" HTML Editor to fix issues)
    *   MartinO - Free tool for checking broken links: [Xenu's Link Sleuth](http://home.snafu.de/tilman/xenulink.html) \- Run it on the internal webserver of a runnining RSE

### News & Review Action Items

| Martin | 100% | Tested, fixed & released M5. Fixed ISV docs. Fixed versions, names & copyright for features. Made SubSystemConfiguration implementations API for ssh, ftp, local. Now planning M6 and working on EclipseCon. | 70% |
| --- | --- | --- | --- |
| DaveD | 80% | Tested build. Documentation updates. UI/Core refactoring. | 100% |
| DaveM | 50% | Testing & fixing. | 50% |
| Kushal | 100% | Testing & fixing EFS. want to get EFS wrapped up this week | 50% |
| Javier | 50% | n/a |  |
| Ted | 0% |  | 0% |
| Uwe | 0% | Testing & fixing NewConnectionWizard. Continue fixing defects in NewConnectionWizard. | 5% |
| Michael | 20% | n/a |  |

*   Growing Communities: Robert Norton doing Launch Actions; Oliver Hardt doing EFS; 1245 downloads of RSE 1.0.1
*   Getting the APIs right

### Upcoming Work

*   **Regularly scheduled I-builds** Thursday 600am Ottawa time;
    *   Everybody to ensure HEAD is stable by Wednesday evening; Martin do a Sanity in WS on Thursday morning Salzburg time, release everything in HEAD manually; I-build prepared automatically 6am Ottawa time
    *   Respin not be scheduled automatically, but on demand only
*   Tough, tight schedule till end of March (but we'll make it!) - **Focus on plan items and \[api\] changes rather than bugfixes**.
    *   Changes involving user docs will be tagged \[userdoc\].
    *   Changes involving NLS strings will be tagged \[nls\].
    *   **AI DaveD, Kushal, Javier:** Review M5 assigned bugs and assign a proper target milestone. M6 if API or NL Strings are involved or it is very urgent. M7 for other urgent stuff. 2.0 otherwise.
*   **Reviewing Plan items**:
    *   [170909](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170909) (DaveD) User Actions: EMO review started. Merging into RSE - tough part is integrating Persistence with the new Persistence Manager (3-4 days); then, testing & fixing & unittests (3-4 days); will need some help from Kushal
    *   [170923](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170923) (DaveD) UI/Non-UI splitting: Currently highest priority for DaveD (until EMO Review is done for UA). DaveD thinks he can complete this without further help by M6.
    *   [170932](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170932) (DaveD) Default Persistence Provider: will need some minor API changes, mostly additions; try to finish for M6, if things go wrong M7 is also OK
    *   [170936](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170936) (DaveD) Macintosh - basically getting drag&drop working - no API - M7
        *   Martin wants automated nightly unittests
        *   **AI Kushal**: check in Toronto - only license is missing
        *   **AI Martin**: Ping Greg Watson and Eclipse Foundation
    *   [170926](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170926) (DaveM) Improve IFileService: mostly done; changing String by IPath not applicable since it may be used headless without Eclipse; Returnvalue for copy; Streams for dstore can be done by DaveM.
        *   Streams on the Subsystem Layer: **AI Kushal** file a defect
        *   Remove some of the download methods on subsystem layer, **AI Kushal** file a defect
    *   [150498](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150498) (Javier) More service-oriented; Multiple subsystems of the same kind - any architectural limitations? DaveM: There might be extenders having problems with multiple.
        *   Martin: NewConnectionWizard whould allow for "No subsystems"; DaveD: want to be able to get it back later? Martin: not necessarily
    *   [170911](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170911) (Javier) Discovery - not discussed since Javier is not here
    *   [170916](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170916) (Kushal) EFS - Working on it, want it wrapped up till end of the week.
    *   [163820](https://bugs.eclipse.org/bugs/show_bug.cgi?id=163820) (Kushal) Encodings - AI checkin Unit Tests for Encodings: 6 languages done, working on 3 more.
    *   [170915](https://bugs.eclipse.org/bugs/showdependencytree.cgi?id=170915) (Martin) Adopt 3.3 Concepts - CVS Preference going well; will need Capability support; need to get rid of Platform internal access, **will need help from everyone.**
    *   [170922](https://bugs.eclipse.org/bugs/showdependencytree.cgi?id=170922) (Martin) Optimize API / Remove obsolete API: We need to make more packages / classes internal! **Will need help from everyone.**
    *   [170910](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170910) (Martin) Integrate TM Terminal View - May need some IHostShell API changes. May need help from DaveM.
    *   [170918](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170918) (Martin) Improve SystemType and Wizard - mostly done (thanks to Uwe!), what to do with the systemType Name attribute?
        *   Martin: Better use fine-granular Properties rather than the name. Subsystems to query Properties from the IHost first, with a fallback to the SystemType if not defined dynamically on the IHost. This allows for both static and dynamic (discovery!) configuration.
        *   Kushal: Get rid of the name, better have Properties
        *   DaveD: There is quite a lot of usage of the Name at the moment instead of ID; there might be some Persistence usage! This might require us to still keep the name for some time in order to maintain Workspace compatibility

*   **Other things to keep an eye on**
    *   add **unit tests** for all new or modified API

*   **Top priorities** for the next two weeks:
    *   Kushal - EFS, Encoding Unittests
    *   DaveD - UI/Non-UI
    *   DaveM - Eclipsecon, dstore streams
    *   Martin - Eclipsecon, Properties action
    *   Javier - Eclipsecon,
    *   Michael - Terminal Performance

### Other Stuff to Do

*   **1\. API Improvements**
    *   SystemType improvements; retargetable actions/commands;
    *   Asynchronous API/callbacks; How is the client informed about job completion?
    *   IHostShell changes for Terminal;
    *   [173042](https://bugs.eclipse.org/bugs/show_bug.cgi?id=173042) (Uwe) Improved / pluggable Refresh
        *   Looks positive that not too much change might be needed in RSE, will see how commercial implementation goes
*   **2\. Play well with the Platform**
    *   retargetable actions/commands; capabilities; icu4j; Orbit; ssh prefs; drag&drop
*   **3\. Improve overall quality (unit tests; special characters; long filenames; background jobs; parallel access; logging; ...)**
*   **4\. New Features**
    *   Terminal-in-rse; Persistence-as-xmlfile; Service enablement
    *   Montavista shell processes subsystem: Performance improvements - DaveM?
*   **5\. Cleanups**
    *   Remove RSE Performance Logging; place contents of logging into core
    *   Reduce number of plugins (once UI/Non-UI separation is done, have e.g. ssh.core and ssh.ui but not more)
        *   Move org.eclipse.rse.connectorservice.local into org.eclipse.rse.subsystems.core
        *   org.eclipse.rse.subsystems.core (collapse files.core, processes.core, shells.core)
        *   org.eclipse.rse.subsystems.dstore (collapse files.dstore, processes.dsore, shells.dstore)
    *   Orbit bundles to be added differently
    *   Unittests to run every night
    *   Version Number Changes to be done by Martin
    *   Copyright Year Changes
    *   General code cleanup -- to do right after M5:
        *   Get rid of unused icons, e.g. rse.ui/icons/full/obj16/system390\_obj.gif, IBM\_logo.gif
        *   Get rid of commented out source code
        *   Get rid of unused properties (chkpii)

### Communications

*   **Europa Requirements**
    *   **Avoiding non-API from other projects**
        *   **AI Martin** create bugzilla against CDT
    *   Update Wiki to explan whether SDK contains examples --> **AI Martin** wait for Platform and adapt
*   For bugs, see the [bug process page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) (assigned to inbox, plan items, status new, hi-priority, API, open with patch, assigned to M6) -- pretty many right now
*   **Update Copyright Year to 2007 if you happen to think about it**
*   (done) **Fix N-builds** (second workspace, use Ted's scripts)
*   Please continue on Compiler Warnings
*   Change Requests
*   Vacations, Holidays etc.
*   Free discussion -- feelings, comments, critics
    *   DaveD: Outlook Invitations dont work on Macintosh iCal any more - no idea why

Action Items
------------

*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_20-Feb-2007#Action_Items "DSDP/TM/Committer Phone Meeting 20-Feb-2007") Action Items
*   **DaveD** \- Reassign target milestone for M5 open bugs; Refactoring UI/Non-UI; Persistence; User Actions; Remove RSE Performance Logging;
*   **DaveM** \- EclipseCon; Streams for Dstore;
*   **Kushal** \- Reassign target milestone for M5 open bugs; \[api\] bugs for Subsystem Streams, get rid of unnecessarydownload methods; Check for Macintosh for Unit Tests in Toronto; EFS; Unittests for Encodings; Talk to DaveD re Comm Server
*   **Martin** \- EclipseCon tutorial; Arrange a committer meeting at EclipseCon; Upload UA refactorings to Bugzilla; Bugzilla against CDT Internal; Migrate build to Ted's scripts; Migrate Commons.net to single-file-jar; Bugs & Unit Tests; Personal Interviews via Skype; Work on [TM and RSE FAQ](./TM_and_RSE_FAQ "TM and RSE FAQ"), improve Wiki and Website (how to contribute);
*   **Javier** \- Reassign target milestone for M5 open bugs; Improve SD
*   **Ted** -
*   **Michael** \- Terminal Performance Improvements
*   **Uwe** \- Retargetable actions, Improved Refresh

Next Meeting
------------

*   [TM BOF at EclipseCon](http://www.eclipsecon.org/2007/index.php?page=sub/&id=4201), [Tuesday 6-Mar at 20:45 PST](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=3&day=7&hour=4&min=45&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) (San Francisco time)
*   [DSDP/TM/Committer Phone Meeting 13-Mar-2007](./DSDP/TM/Committer_Phone_Meeting_13-Mar-2007 "DSDP/TM/Committer Phone Meeting 13-Mar-2007") at [1700 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=3&day=13&hour=17&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_28-Feb-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_28-Feb-2007))