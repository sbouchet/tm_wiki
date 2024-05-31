

DSDP/TM/Committer Phone Meeting 8-May-2007
==========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [May 8, 2007](/index.php?title=May_8,_2007&action=edit&redlink=1 "May 8, 2007 (page does not exist)") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=5&day=8&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Invited Attendees](#Invited-Attendees)
*   [2 Notes](#Notes)
    *   [2.1 News & Review Action Items](#News-.26-Review-Action-Items)
    *   [2.2 Time Plan and Deadlines toward M7](#Time-Plan-and-Deadlines-toward-M7)
    *   [2.3 Bugs and open work to be discussed](#Bugs-and-open-work-to-be-discussed)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Invited Attendees
-----------------

*   IBM - Dave McKnight, Dave Dykstal, Kushal Munir, Kevin Doyle, Sanjayan Eladchumanasamy, Xuan Chen
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Michael Scharf, Uwe Stieber

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 2-May-2007](/DSDP/TM/Committer_Phone_Meeting_2-May-2007 "DSDP/TM/Committer Phone Meeting 2-May-2007")

### News & Review Action Items

| Martin | 30% | Platform bugs [176805](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176805), [185734](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185734), [105554](https://bugs.eclipse.org/bugs/show_bug.cgi?id=105554) | 100% |
| --- | --- | --- | --- |
| DaveD | 80% |  | 80% |
| DaveM | 40% | Bugfixes | 40% |
| Kushal | 40% | BIDI Encodings | 40% |
| Javier | 50% | FTP Parser Extension Point | 50% |
| Ted | 0% | - | 0% |
| Uwe | 5% | - | 5% |
| Michael | 10% |  | 10% |

### Time Plan and Deadlines toward M7

*   **Plan towards M7** \- goals and deadlines for I-builds
    *   I20070510 -- Stabilization, start [TM 2.0 M7 Testing](/TM_2.0_M7_Testing "TM 2.0 M7 Testing") on May 14th
    *   I20070516 -- TM 2.0M7 (17th is a public holiday in Austria!)
    *   **Reminder: [TM 2.0 Ramp down Plan for Europa](/TM_2.0_Ramp_down_Plan_for_Europa "TM 2.0 Ramp down Plan for Europa")**

### Bugs and open work to be discussed

*   **Current Priorities**
    *   **Priority #1: Converge to a Stable Build for Testing**
        *   **Javier**: FTP parallel download - have a problem with cancellation, but it looks difficult - not for M7
            *   Directory listing parser extension point: Dont activate too early; translatable label; autodetect parsers registered by extenders - **AI Javier wants to address these**
            *   What about persistence of the parser setting - does it work now? Dont know if it works by now; **AI DaveD check it**
        *   **DaveD**: [177329](https://bugs.eclipse.org/bugs/show_bug.cgi?id=177329) Persistence locks the workspace / thread handling: provider outside workspace / independent of IResource - **AI DaveD fix today**
            *   [163592](https://bugs.eclipse.org/bugs/show_bug.cgi?id=163592) API to explicitly save profiles after model changes - API is there; missing is the ability to turn off some extra saving is mostly finished
            *   [177332](https://bugs.eclipse.org/bugs/show_bug.cgi?id=177332) API to wait until RSE model is fully restored - **AI DaveD API for polling the state of the model (is it fully restored?); query "all providers" vs. "a particular one"**
            *   [168870](https://bugs.eclipse.org/bugs/show_bug.cgi?id=168870) org.eclipse.rse.core in the UI plugin: SystemBasePlugin (reduce usage to 0 and get rid of it?), ISystemRemoteElementAdapter (only Shell!), ISystemRemoteObjectMatcher; org.eclipse.rse.core.comm to go to non-UI together with the keystoreProviders extension point - **AI DaveD committed: most interesting of the lower priority ones**
            *   [176211](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176211) org.eclipse.rse.internal.model in the UI plugin: SystemHostPool (create an interface IRSESystemTypeAdapter) - **tricky**
            *   [142806](https://bugs.eclipse.org/bugs/show_bug.cgi?id=142806) attributes not written to DOM; - probably fixed already, FTP properties is an example of this; [153632](https://bugs.eclipse.org/bugs/show_bug.cgi?id=153632) incorrect filterpool for dstore - **not API: AI DaveD within the next week**
            *   [183771](https://bugs.eclipse.org/bugs/show_bug.cgi?id=183771) StandardCredentialProvider without UI if password is stored; - almost there, not a priority since there are other UI dependencies we won't get around for 2.0
        *   **DaveM**: [184322](https://bugs.eclipse.org/bugs/show_bug.cgi?id=184322) IProgressMonitor added to file system APIs
            *   Need to document whether null is allowed as paramter or not, both for IFileService and IRemoteFileSubSystem!!
                *   DaveD: IResource does allow null as progress monitor; DaveM: dont document that we allow null; MartinO: require clients to pass in real progress monitors.
            *   Should we have a common guideline of having the progress monitor first, or last? - Kushal: IFileService has monitors in a different place than Subsystem; Resources API have monitors at the end typically; **AI Martin** check Eclipse APIs and send E-Mail
            *   [173042](https://bugs.eclipse.org/bugs/show_bug.cgi?id=173042) Refresh in the SystemView: "remote" case vs. "local" case -- ISystemRemoteElementAdapter vs. ISystemViewElementAdapter - **AI DaveM - Hi Prio for WR**
                *   Should we better have a method like doLazyRefresh() vs. doAsyncRefresh() in the ISystemViewElementAdapter?
            *   [167620](https://bugs.eclipse.org/bugs/show_bug.cgi?id=167620) delete many items has remote queries on dispatch thread
            *   [bug 182221](https://bugs.eclipse.org/bugs/show_bug.cgi?id=182221): IRemoteFileSubSystem should forward exceptions rather than handling them with dialogs - Decision was to pragmatically start converting simple methods - who should do it? - No volunteers :-(
        *   **Martin**: [177523](https://bugs.eclipse.org/bugs/show_bug.cgi?id=177523) getInstance; [175680](https://bugs.eclipse.org/bugs/show_bug.cgi?id=175680) cleanup ISystemRegistry - probably bring more into non-UI; [173042](https://bugs.eclipse.org/bugs/show_bug.cgi?id=173042) Refresh; [172650](https://bugs.eclipse.org/bugs/show_bug.cgi?id=172650) Capabilities; [176461](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176461) expand-to-level; [170910](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170910) Integrate Terminalview; [185098](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185098) constants for system types; [185097](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185097) make getCoreRegistry() simpler
            *   Committer Voting: [185552](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185552) remove remoteSystemsViewPreferencesActions extension point - Kushal OK
            *   Committer Voting: [185554](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185554) remove dynamicPopupMenuExtensions extension point - Kushal not sure; one IBM product wanted more control over the menus; Uwe: adding actions dynamically to the menus is possible with extension points - only thing needed is menu groups; org.eclipse.ui.popupMenus can also be used for that - **AI Uwe add some examples on how to do it with org.eclipse.ui.popupMenus on the bug**
        *   **Michael**: [165893](https://bugs.eclipse.org/bugs/show_bug.cgi?id=165893) Terminal xyzmodem, [185348](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185348) programmatic connection creation
            *   Make all Terminal API experimental for now: **AI Martin** lookup how to declare API experimental and do it
        *   **Kushal**: Single "Encoding" control on the Host (for all subsystems) - **checking in today**; should the encoding be applied to the model or the views? - Martin: would like the Unicode model represent the CORRECT strings (recoded if necessary)
    *   **Priority #2: Import/Export**
        *   Is there some mini-docu anywhere how to test Import/Export? - Add to [TM Manual Test Plan](/TM_Manual_Test_Plan "TM Manual Test Plan") \- **DaveM:**
            *   Export: Take a local project, e.g. CDT project with src folder; take project, right-click > export > remote file system; similar to Eclipse "Export to File System" wizard, so it's a plain copy of all files to the remote side, no concept of synchronization
            *   Export to descriptor file: selection of files to export can be saved, this file can later be right-clicked on to re-do the export quickly (similar to Java JAR Export wizard)
            *   Import: Select a remote folder in the system view, right-click > Import: subset by file types, import to local project (modeled after Eclipse Import from File System wizard) - has a descriptor file as well
            *   Use cases:
                *   Import/Export was more useful prior to having EFS - one would just import everything to local to edit there, then export
                *   Deployment; Future: Export to multiple locations
                *   Future: keep track of files changed in the project, or using Platform Team/Synchronization framework
    *   **Priority #3: Bugs**
        *   Bugzilla: [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)
            *   [167620](https://bugs.eclipse.org/bugs/show_bug.cgi?id=167620) Select and Delete in the Main thread
        *   EFS: Copy(), Move(); Open Remote Project on Startup: Get rid of IResource dependencies where possible; minimal plugin activations; UI/Non-UI

*   **General Guidelines**
    *   Avoid breaking API changes after end of this week
    *   Junior Jobs: Bugs marked as JJ: in the subject - similar to "helpwanted" keyword
    *   Compiler Warnings - total 669 in all of RSE, as of today:
        *   360 "Discouraged Access"
        *   114 Javadoc:
        *   97 deprecated
        *   Compiler warnings compared to [30-Jan-2007](/DSDP/TM/Committer_Phone_Meeting_30-Jan-2007 "DSDP/TM/Committer Phone Meeting 30-Jan-2007")
            *   192 -> 99 rse.ui (mostly javadoc)
            *   94 -> 120 files.ui
            *   27 -> 31 subsystems.files.core
            *   23 -> 18 services (javadoc)
            *   12 -> 14 rse.core (deprecated)
            *   3 connectorservice.dstore
            *   (---) -\> 11 importexport
        *   See the [Committer Howto](https://www.eclipse.org/dsdp/tm/development/committer_howto.php#check_code) for settings
        *   **The 'discouraged access** warnings should be looked at since they may indicate API flaws

Vacation, Away
--------------

*   Kushal away on Thursday

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_2-May-2007#Action_Items "DSDP/TM/Committer Phone Meeting 2-May-2007") Action Items
*   **DaveD**: Translation Testcases; Persistence Provider without IResource; Get started on ICU4J with [bug 183631](https://bugs.eclipse.org/bugs/show_bug.cgi?id=183631)
*   **DaveM**: Bugs
*   **Kushal**: BIDI bugs and Encodings
*   **Martin**: Inform the community about dropped user actions; API cleanups; Testing Stats; Refresh improvements; Integrating Terminal with RSE
*   **Javier**: FTP parallel download, registering FTP Parser by extension point
*   **Michael**: Terminal xyzmodem, programmatic terminal connection creation

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 15-May-2007](/DSDP/TM/Committer_Phone_Meeting_15-May-2007 "DSDP/TM/Committer Phone Meeting 15-May-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=5&day=15&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 6-Jun-2007](/DSDP/TM/Phone_Meeting_6-Jun-2007 "DSDP/TM/Phone Meeting 6-Jun-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=6&day=6&year=2007&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_8-May-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_8-May-2007))