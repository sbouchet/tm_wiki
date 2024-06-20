

DSDP/TM/Committer Phone Meeting 5-Mar-2008
==========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday Mar 5, 2008 at [1600 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=3&day=5&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | Martin to call everybody by Skype |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, kevin.j.doyle, xuan.chen886, rupen.mardirossian, javier.montalvoorus, eugenetarassov, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 Current Work](#Current-Work)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Xuan Chen, Dave McKnight, Dave Dykstal, Rupen Mardirossian, (Kevin Doyle n/a)
*   Wind River - Martin Oberhuber, Michael Scharf, (Uwe Stieber n/a, Eugene Tarassov n/a)
*   Symbian - Javier Montalvo Orus

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 20-Feb-2008](./Committer_Phone_Meeting_20-Feb-2008 "DSDP/TM/Committer Phone Meeting 20-Feb-2008")

### Current Work

*   **Skype Call Quality**
    *   Problems with Eugene; Problems reaching DaveD; otherwise good. Occasional dropoffs for Xuan.
*   **M6 Focus**
    *   **Focus on finalizing API Changes for M6** \- Please review your bugs and check "target milestone" assignment. If API might be involved, assign to M6.
    *   **PII** \-\- Xuan status - Ran PII on 20080304 Nightly driver, and no check PII error.
        *   Next NLS drops: near end march -- near-final NLS drop (UI-Freeze: M6+2)
        *   Translation only of what IBM ships (not Terminal, Discovery, TCF, RemoteCDT) (only RSE-SDK, DStore-Server, Useractions) - **AI Xuan** add RSE useractions to PII Mapfile
    *   **Xuan: Changes of using or implementing encryption methods?** \- no encryption in TM
    *   **Xuan: Request PMC presentation material for EclipseCon review (will be invited to review later on)** \- ok will consider when invited
        *   **IPZilla**: Strategic Members can subscribe a person on IPZilla mailing list via [http://portal.eclipse.org](http://portal.eclipse.org)
    *   **Unit Tests** \- next priority after API
        *   Need all unit tests enabled in nightly builds - need to use Uwe's Connection Property classes, see **FTPFileSubsystemTestCase** \- **AI Xuan, DaveM, Kevin** Use Properties for unit tests
*   **Hi-pri-bugs; apply patches**
    *   Community Contributions from
        *   [bug 164300](https://bugs.eclipse.org/bugs/show_bug.cgi?id=164300) UNIX server.sh on fixed port (DaveM:done)
        *   [bug 181563](https://bugs.eclipse.org/bugs/show_bug.cgi?id=181563) Radoslav Gerganov: Ctrl+Space in Command View (Martin:done)
        *   [bug 195402](https://bugs.eclipse.org/bugs/show_bug.cgi?id=195402) Johnson Ma: tgz archive handler (**AI Johnson** cleanup required)
        *   [bug 218880](https://bugs.eclipse.org/bugs/show_bug.cgi?id=218880) Johnson Ma: ssh keepalive UI (**AI Johnson** cleanup required)
        *   [bug 210682](https://bugs.eclipse.org/bugs/show_bug.cgi?id=210682) Rupen's multi-file copy/move/overwrite dialog
    *   Bug Discussions
        *   [bug 190231](https://bugs.eclipse.org/bugs/show_bug.cgi?id=190231) subsystem UI -> Core: **AI DaveD** help with Wizard Pages and the way they are registered; make them adaptable somehow
        *   [bug 220892](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220892) reving down dstore protocol version - **AI DaveM** add a Handler Hook for registering handshake handler / error handler
        *   [bug 197167](https://bugs.eclipse.org/bugs/show_bug.cgi?id=197167) Callback to know when RSE model is fully restored - **AI DaveD** Local Connection Preference: move from UI to Core; JobChangeListener join; stampfiles - looks good
        *   [bug 221211](https://bugs.eclipse.org/bugs/show_bug.cgi?id=221211) MultiStatus for IFileService batch operations - exception on first failure for modifying operations. No exceptions/multistatus on non-modifying operations. **AI DaveD/DaveM** update Javadocs when it's clear what we want
        *   [bug 220379](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220379) Make DStoreFileService API - encodingHandler - wait on reporter, **AI Martin** comment on bug (object reference idea)
        *   [bug 220547](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220547) SimpleSystemMessage message ID - globally unique message id vs. plugin-local status - Dialog Title: MessageID if globally unique / generic title based on severity if plugin-local
        *   [bug 220995](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220995) Xuan: Can we remove some interface provided by SystemSelectRemoteFileAction and SystemSelectRemoteFolderAction
        *   [bug 218947](https://bugs.eclipse.org/bugs/show_bug.cgi?id=218947) IRemotePath idea - **AI DaveM** create new defect for the API change
            *   Martin: Migration could be stepwise, if we are able to convert String into IRemotePath and vice versa
            *   DaveM: Naming convention -- IHostPath instead of IRemotePath since located in the Service?

*   **Planning** \- **AI Martin** to write up what we discussed in Toronto
    *   Think about assigning bugs to target milestones. What goes into 3.0 and what not? - DaveD Mylyn is nice for bug review!
*   TM Website
    *   **AI Kevin** follow up on his website proposals
*   **Javier** almost finished on Symbian assignment, will have some time for RSE but needs to talk to Manager
    *   Martin updating Commons Net to 1.5.0
    *   [bug 212382](https://bugs.eclipse.org/bugs/show_bug.cgi?id=212382) ftpListingParser initCommands
*   **DaveD**
    *   [bug 217894](https://bugs.eclipse.org/bugs/show_bug.cgi?id=217894) Subsystem Configuration Families - subsystem category would be orthogonal to subsystem family -- family would be related to connector service -- change wizard pages from API into plugin.xml markup? **AI All** comment on the bug
    *   Import/export connections rather than profiles - extend the persistence provider for import/export. Use one format for export only in the UI,, perhaps allow multiple providers for import (for migration), perhaps allow multiple kinds of export via API.
*   **DaveM:** -
    *   EFS and encodings - No response from platform - suggstion alternative EFS provider, **always convert into UTF-8**, continue discussion on the defect
*   **Kevin:** -
*   **Xuan:** \- Will mostly be busy with IBM / Migration work; add useractions to PII mapfile
*   **Martin:** \- Need to put Project Plan on the Web; Update Releng scripts to automatically run unit tests at night
    *   Searchcvs, Relnotes done; Little more work needed on web-build and promote.sh
    *   JSch-0.1.37, Commons.Net 1.5.0
    *   Next tasks - EclipseCon presentation; Move SubsystemConfiguration implementation into non-UI; Lazy loading of SubsystemConfiguration (use the Proxy more); Lazy loading of UI adapters
*   **Uwe:** -
*   **Rupen:** -
*   **Michael:** -
*   **Questions**

*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   EclipseCon Mar17-21
*   Javier off during easter week Mar17-21
*   Xuan may also take some time off

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_20-Feb-2008#Action_Items "DSDP/TM/Committer Phone Meeting 20-Feb-2008") Action Items
*   **Everyone**: Comment on [bug 217894](https://bugs.eclipse.org/bugs/show_bug.cgi?id=217894) SubsytemConfigurationFamilies
*   **DaveD**: Help on [bug 190231](https://bugs.eclipse.org/bugs/show_bug.cgi?id=190231) Subsytem UI->Core
*   **DaveM**: [bug 220892](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220892) handler hook for dstore protocol backward compatibility; [bug 218947](https://bugs.eclipse.org/bugs/show_bug.cgi?id=218947) Create new bug for proposed IRemotePath API Addition; Use Properties for Unit Tests
*   **Xuan**: Add Useractions to PII Mapfile; Use Properties for Unit Tests
*   **Kevin**: Website Updates
*   **Martin**: EclipseCon; [bug 190231](https://bugs.eclipse.org/bugs/show_bug.cgi?id=190231) Subsytem UI->Core; finish new releng; Write-up TM 3.0 Plan; Look at PropertyDescriptor issues; unit tests; Newsgroup
*   **Javier**: [bug 212382](https://bugs.eclipse.org/bugs/show_bug.cgi?id=212382) ftp initCommands; add unit tests; document the Symbian internal test setup similar to [CVS](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204138#c20) \-\- see also [CVS_Development#Testing](https://wiki.eclipse.org/CVS_Development#Testing "CVS Development")
*   **Michael**: Terminal improvements

Next Meeting
------------

*   Monthly [DSDP/TM/Phone Meeting 5-Mar-2008](./Phone_Meeting_5-Mar-2008 "DSDP/TM/Phone Meeting 5-Mar-2008") at [9am PST / 1700 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=3&day=5&year=2008&hour=16&min=00&sec=0&p1=0)
*   EclipseCon March 17-20: Martin, Michael - no other committers
*   [DSDP/TM/Committer Phone Meeting 26-Mar-2008](./Committer_Phone_Meeting_26-Mar-2008 "DSDP/TM/Committer Phone Meeting 26-Mar-2008") (3 weeks due to EclipseCon) at [1600 UTC / 0900 SFO / 1100 Rochester / 1200 Toronto / 1600 London / 1700 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=3&day=26&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) \-\- take care of DST differences!
*   Next [BugDay/March_2008](https://wiki.eclipse.org/BugDay/March_2008 "BugDay/March 2008") on Mar 28


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_5-Mar-2008](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_5-Mar-2008))