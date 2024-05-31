

DSDP/TM/Committer Phone Meeting 29-Mar-2007
===========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Thursday [Mar 29, 2007](/index.php?title=Mar_29,_2007&action=edit&redlink=1 "Mar 29, 2007 (page does not exist)") at [1400 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=3&day=29&hour=14&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 News & Review Action Items](#News-.26-Review-Action-Items)
    *   [2.2 Upcoming Work](#Upcoming-Work)
    *   [2.3 Other Stuff to Do](#Other-Stuff-to-Do)
    *   [2.4 Communications](#Communications)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave McKnight, Dave Dykstal, Kushal Munir
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber, Michael Scharf, (Ted Williams)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help: **being responsive**
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site

### News & Review Action Items

| Martin | 50% | \[done\] User Actions CQ; multi-subsystem-discussion [bug 174495](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174495); 3 Bugzillas against CDT; | 100% |
| --- | --- | --- | --- |
| DaveD | 100% | UI/Non-UI connectorservice; revisited logging (provides some filtering); moving filters to core now; | 100% |
| DaveM | 10% | Made stuff internal and UI->Core | 50% |
| Kushal | 50% | EFS (remaining problem on restoring Eclipse Workbench with a remote project); [179850](https://bugs.eclipse.org/bugs/show_bug.cgi?id=179850) Streams on Subsystem Layer: will make streams abstract; Mac available | 50%, till end of june |
| Javier | 50% | SD submission | 30%, testing only |
| Ted | 0% | - | 0% |
| Uwe | 5% | - | 5% |
| Michael | 10% | Terminal Performance | 10% |

### Upcoming Work

*   See also [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_20-Mar-2007#Upcoming_Work "DSDP/TM/Committer Phone Meeting 20-Mar-2007") for notes
*   **M6 must-have issues**
    *   All development and testing against Eclipse 3.3M6 now, please!
    *   NLS changes: mostly IBM, not very strict; and need to know what the changes are, so we can report them (notify what files have changed)
        *   Translation Test late april
        *   Adding user actions+importexport for Ganymede only? - Problematic since it's a committed plan item
        *   Useractions is problematic since it has a persistence component.
        *   **Decision:** making all UDA and import/export "internal" and add it with M7, probably as "experimental optional" package
            *   Will need some API for default user actions (configuring dialogs to define own file types)
    *   Source tgz delivery for source IP scans? - Not heard back
    *   [170922](https://bugs.eclipse.org/bugs/showdependencytree.cgi?id=170922) (DaveM, DaveD) **Making stuff internal**
        *   **take care of "discouraged access" warnings!**
        *   rse.core: Should RSESystemType be public? - Uwe: is bound to the extension registry, so OK to be internal
        *   files.ui: Activator should be internal (util methods to go to RemoteFileUtility). FileResources should be internal? Dialogs should be internal? (Some to be reusable); SystemFileNewConnectionWizardPage - why not with ConnectorService, or dstore? SystemFileFilterStringEditPane should be public to derive from?
        *   [170920](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170920) rse.logging is this really complete? Should the bug be split up or the summary changed?
        *   processes.ui: Clean-up Manifest (export with ;x-internal="true"); Fix doc.isv; Kill etc actions should be internal. Activator should be internal. SystemProcessFilterStringEditPane should be public to derive from?
        *   shells.ui: Activator should be internal; SystemViewRemoteOutputAdapter is public but SystemViewRemoteErrorAdapter not? Why is SystemCommandsView public?
        *   subsystems.files.dstore: Almost everything internal, good! What about SearchResultsChangeListener, StatusChangeListener? What about package.html?
        *   subsystems.shells.core: What about OutputRefreshJob, its currently needed
        *   rse.ui/filters: Can we remove SystemFilterStartHere? Looks like convenience, since it is internal now can we remove it? Should SystemFilter be public so clients can derive from it?
        *   rse.ui/UI: OK to have massagers internal? Shouldn't these be re-usable by clients?
            *   SystemNewConnectionAction - how to officially do it (needed by remotecdt);
            *   SystemResources to be internal? (Or we cannot change strings!)
            *   Why did the RefreshAction remain public? Why did the dialogs remain public?
            *   Why did the SystemFilterWorkWithFilterPoolsTreeViewer remain public?
            *   Why did ui.filters.actions package remain public? Why ui.filters.dialogs?
            *   Why did rse.ui.propertypages remain public?
            *   Why is SystemTableView public?
            *   What to do with SystemCommunicationsDaemon? - Kushal: doesnt matter if it is in Open Source - **AI Kushal** Remove it
    *   **ImportExport and User Actions**
        *   Do importexport and useractions have API? Stuff we need to make internal?
        *   Can we add it to the features / downloads?
    *   UI/Non-UI Refactorings
        *   connectorservice have some Javadoc still referring to SuperAbstractConnectorService
    *   **API Changes**
        *   [179910](https://bugs.eclipse.org/bugs/show_bug.cgi?id=179910) (Kushal) removing unnecessary upload/download - do we really need still 2 upload methods?
    *   [TM 2.0 M6 Testing](/TM_2.0_M6_Testing "TM 2.0 M6 Testing") \- What changes / features need to be especially tested?
        *   "internal" refactorings; new connectorservice; encodings; EFS;
    *   **Persistence Provider**
        *   Reason it is in the workspace, is to allow sharing connections with other team members
        *   But this doesnt work very well anyways, most requests are for import/export of connection or filter definitions
        *   We could move persistence out of the workspace for now; and at some point, re-add an idea of "Profiles" which are stored in a single file and associated with a project later on
        *   Migration tools might require multiple persistence providers at some point
        *   Some customers have team environments without source control, so import/export is better than CM-based sharing
        *   DaveM could imagine using ECF (or other AIM clients) to share connections
        *   Use case for different persistence providers:
            *   Migration - Uwe: For Launch Configurations, they added a LaunchConfigurationMigrator extension point
        *   Persistence Provider could be a Product preference
*   **Plan Items**
    *   [170909](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170909) (DaveD, Kushal) User Actions: Still waiting for IP review. Found many icons related to UA and import/export in rse.ui which will need to be moved.
    *   [170923](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170923) (DaveD) UI/Non-UI splitting: Conn.Svc almost done, others will fall nicely into place afterwards. rse.ui/plugin.xml/systemTypes need to go to core
    *   [170932](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170932) (DaveD) Default Persistence Provider: mostly non-API
    *   [170936](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170936) (DaveD) Macintosh - machine for unittests? - Kushal now has access to the box - for M6 testing: Kushal do a sanity test, DaveD do elaborate Mac testing
    *   [170926](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170926) (DaveM) Improve IFileService: Returnvalue for copy
    *   [150498](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150498) (Javier) More service-oriented; Multiple subsystems of the same kind - Javier raised [bug 174495](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174495); [176490](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176490) new "dynamic wizard" request, see also "Improve SystemType" below
    *   [170911](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170911) (Javier) Discovery
    *   [170916](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170916) (Kushal) EFS
    *   [163820](https://bugs.eclipse.org/bugs/show_bug.cgi?id=163820) (Kushal) Encodings - **AI Kushal UnitTests**
    *   [170915](https://bugs.eclipse.org/bugs/showdependencytree.cgi?id=170915) (Martin) Adopt 3.3 Concepts: Jsch
    *   [170922](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170922) (Martin) Optimize RSE API: ISystemRegistry
    *   [170910](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170910) (Martin) Integrate Terminal
    *   [170918](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170918) (Martin) Improve SystemType and Wizard: **AI Martin** Replace Name by IRSESystemType in IHost and wherever possible. **AI DaveD** Start persisting systemType id in addition to name
        *   if() queries -> these are implementation details later, even replacing Name by Properties since the systemType does have Properties already
*   **Other API things** not directly marked as plan item
    *   [173042](https://bugs.eclipse.org/bugs/show_bug.cgi?id=173042) Improved / pluggable **Refresh**: **AI Martin** make a start, DaveM to review
    *   [166338](https://bugs.eclipse.org/bugs/show_bug.cgi?id=166338) Asynchronous **Callbacks** \- **AI Martin** to start
    *   **expandTo()** \- **AI Martin** probably connected to async callbacks, non-UI multi path query and event changes for Refresh
*   **Other Business**
    *   **Cleanup**: JDT Cleanup wizard, **AI Martin start with one plugin**
    *   [170915](https://bugs.eclipse.org/bugs/showdependencytree.cgi?id=170915) (DaveM) Getting rid of Platform "internal" access
    *   add **unit tests** for all new or modified API

**Priorities** are folded into the Action Items below

### Other Stuff to Do

*   **1\. Play well with the Platform**
    *   capabilities; icu4j; Orbit; ssh prefs; drag&drop
    *   retargetable actions/commands instead of actionsets;
*   **2\. Improve overall quality (unit tests; special characters; long filenames; background jobs; parallel access; logging; ...)**
*   **3\. New Features**
    *   Persistence-as-xmlfile; Service enablement
*   **4\. Cleanup/Optimization**
    *   Remove RSE Performance Logging; place contents of logging into core
    *   Reduce number of plugins (once UI/Non-UI separation is done, and once we have Capabilities: have e.g. ssh.core and ssh.ui but not more)
        *   Move org.eclipse.rse.connectorservice.local into org.eclipse.rse.subsystems.core
        *   org.eclipse.rse.subsystems.core (collapse files.core, processes.core, shells.core)
        *   org.eclipse.rse.subsystems.dstore (collapse files.dstore, processes.dsore, shells.dstore)
    *   **Build Process Improvements**
        *   Orbit bundles to be added differently
        *   Unittests to run every night (Ted's scripts)
        *   Version Number Changes to be done by Martin
    *   [174945](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174945) General code cleanup - get rid of unused icons, comments, properties
    *   **Update Copyright Year to 2007 if you happen to think about it**
    *   Please continue on Compiler Warnings

### Communications

*   **Europa Requirements**
    *   **Avoiding non-API from other projects** -\> CDT bugzillas [178831](https://bugs.eclipse.org/bugs/show_bug.cgi?id=178831), [178832](https://bugs.eclipse.org/bugs/show_bug.cgi?id=178832), [178835](https://bugs.eclipse.org/bugs/show_bug.cgi?id=178835)

*   *   Update Wiki to explain whether SDK contains examples --> **AI Martin** wait for Platform and adapt
*   For bugs, see the [bug process page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) (assigned to inbox, plan items, status new, hi-priority, API, open with patch, assigned to M6) -- 54 right now
*   Change Requests
*   Vacations, Holidays etc.
    *   Javier out of office except tues and wed
*   Free discussion -- feelings, comments, critics
    *   IBM contribution of Remote Source Locators and Remote Java Launch - **AI DaveM** talk with DaveD, get this started

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_20-Mar-2007#Action_Items "DSDP/TM/Committer Phone Meeting 20-Mar-2007") Action Items
*   **Everyone** \- Review recent pending API change bugzilla's and comment on them if there are any issues
*   **DaveD** \- Refactoring UI/Non-UI;
*   **DaveM** \- Making stuff internal; Talk with DaveD regarding open-sourcing Remote Source Lookup and Java Launch;
*   **Kushal** \- EFS; Encoding Tests; Remove RSECommunicationsDaemon; Bugs & Unit Tests
*   **Martin** \- Website updates (M5, Eclipsecon, Webinar); Work on Refresh, ExpandTo, Callbacks; Adopt new Platform SSH organization; Replace systemType name by IRSESystemType in IHost; Integrate Terminal in RSE; Test JDT Cleanup Wizard on one plugin; Update feature.properties for Europa; Migrate build to Ted's scripts; Bugs & Unit Tests; Personal Interviews via Skype; RXTX contribution;
*   **Javier** \- Improve SD; Bugs & Unit Tests
*   **Ted** -
*   **Michael** \- Terminal Performance Improvements
*   **Uwe** \- Update PersistenceProvider bug

Next Meeting
------------

*   [TM 2.0 Testing](/TM_2.0_Testing "TM 2.0 Testing") on 3-Apr-2007
*   [DSDP/TM/Committer Phone Meeting 3-Apr-2007](/DSDP/TM/Committer_Phone_Meeting_3-Apr-2007 "DSDP/TM/Committer Phone Meeting 3-Apr-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=4&day=3&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) \- **attention: DST change in Europe**
*   [DSDP/TM/Phone Meeting 4-Apr-2007](/DSDP/TM/Phone_Meeting_4-Apr-2007 "DSDP/TM/Phone Meeting 4-Apr-2007") open phone call
*   TM 2.0M6 - 6-Apr-2007
*   [TM Webinar](https://www.eclipse.org/community/webinars2006.php) pre-call on [10-Apr-2007](/index.php?title=10-Apr-2007&action=edit&redlink=1 "10-Apr-2007 (page does not exist)"); webinar on [12-Apr-2007](/index.php?title=12-Apr-2007&action=edit&redlink=1 "12-Apr-2007 (page does not exist)")


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_29-Mar-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_29-Mar-2007))