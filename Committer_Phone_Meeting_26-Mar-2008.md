

DSDP/TM/Committer Phone Meeting 26-Mar-2008
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Mar 26, 2008](./index.php?title=Mar_26,_2008&action=edit&redlink=1 "Mar 26, 2008 (page does not exist)") at [1600 UTC / 0900 SFO / 1100 Rochester / 1200 Toronto / 1600 London / 1700 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=3&day=26&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | Martin to call everybody by Skype |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, kevin.j.doyle, xuan.chen886, rupen.mardirossian, javier.montalvoorus, eugenetarassov, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 **EclipseCon 2008 in a Nutshell**](#EclipseCon-2008-in-a-Nutshell)
    *   [2.2 **M6 Focus**](#M6-Focus)
    *   [2.3 **Hi-pri-bugs; community contributions; apply patches**](#Hi-pri-bugs.3B-community-contributions.3B-apply-patches)
    *   [2.4 **Bug Discussions**](#Bug-Discussions)
    *   [2.5 Committer Status and Report](#Committer-Status-and-Report)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Xuan Chen, Dave McKnight, Dave Dykstal, Rupen Mardirossian, (Kevin Doyle n/a)
*   Wind River - Martin Oberhuber, Michael Scharf, (Uwe Stieber n/a), (Eugene Tarassov n/a)
*   Symbian - Javier Montalvo Orus

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 5-Mar-2008](./DSDP/TM/Committer_Phone_Meeting_5-Mar-2008 "DSDP/TM/Committer Phone Meeting 5-Mar-2008")
*   **Skype Call Quality**
    *   Good most of the time with few dropouts (7 participants). Javier had trouble connecting, needed 4 retries.

### **EclipseCon 2008 in a Nutshell**

*   Best EclipseCon Ever :-)
*   DSDP and TM stuff:
    *   [TM Tutorial](http://www.eclipsecon.org/2008/?page=sub/&id=38) \- focus on 50% TCF and 50% rse; about 30 people, very positive feedback
    *   [TM Short Talk](http://www.eclipsecon.org/2008/?page=sub/&id=39) \- may re-use slides
    *   [Blog Post about TCF](http://tmober.blogspot.com/2008/03/target-communication-framework-tcf.html)
    *   [CDT Remote / RDT](http://www.eclipsecon.org/2008/?page=sub/&id=323) call for participation, being discussed on cdt-dev list for now
    *   [DSDP BOF](http://www.eclipsecon.org/2008/?page=sub/&id=582) \- towards two "packages" of DSDP projects for mobile Java / device development, likely with P2 installer but on SourceForge due to needing GPL for cross-compilers / emulators
    *   [RTSC](http://www.eclipsecon.org/2008/?page=sub/&id=213) and [NAB](http://www.eclipsecon.org/2008/?page=sub/&id=37) were excellent talks from DSDP
*   Big Press hype about Microsoft envolvement in Eclipse but rather [disappointing keynote](http://douggaff.blogspot.com/2008/03/eclipsecon-08-we-barely-knew-ye.html) by Sam Ramji - though the EMO likes to [see things positive](http://feeds.feedburner.com/~r/IanSkerrett/~3/254405704/). Still, the [facts are](http://ed-merks.blogspot.com/2008/03/eclipsecon-wednesday.html): no commitment yet by MS but wants to help out in SWT-WPF port and Higgins-Cardspace
*   Eclipse 4.0 aka [E4](./E4 "E4"): IBM/RAP want to webalize SWT, which may be a good thing in terms of architecture but is not the whole story: need to collect requirements from all the community in a suitable forum, and a face-to-face kickoff meeting
    *   In general, it looks like the community is dozing a little wrt Platform - no exciting new talks, no exciting new features but much more breadth of community. Also, OSGi is gaining even more momentum, new Eclipse RT (Runtime) toplevel project started
*   Played with [DTP / SQL Query Builder](http://www.eclipsecon.org/2008/?page=sub/&id=117), [BIRT Charting](http://www.eclipsecon.org/2008/?page=sub/&id=173)
*   [Eclipse Command Language (ECL)](http://www.eclipsecon.org/2008/?page=sub/&id=272) looked very interesting
*   Automated UI testing: [RCP Robot and FIT](http://www.eclipsecon.org/2008/?page=sub/&id=440) was extremely hot - FIT tables in Excel (idea by Ward Cunningham) together with [Fixtures maintained by the developer](http://www.eclipsecon.org/2008/?page=sub/&id=238) and [SWT Bot](http://www.eclipsecon.org/2008/?page=sub/&id=254) for the actual test execution
*   Had some discussions with Scott Lewis about [ECF](https://www.eclipse.org/ecf) especially comparing against TCF and integrating into RSE: we should really do an RSE ECF file provider, they got the browsing APIs now
*   Most funny EclipseCon stuff: [Vista SP1 Features](http://jonathancarter.co.za/vista-toilet-paper), How to [get IP approved quicly](http://eclipsewebmaster.blogspot.com/2008/03/eclipse-ip-done-easy.html), the most [awsome guy at Eclipse](http://pookzilla.net/wp/2008/03/are-you-experienced/) and its [Fake](http://inside-swt.blogspot.com/2008/03/fake-steve-northover.html), stuff from the [Fake Steve Jobs](http://eclipse-ecosystem.blogspot.com/2008/03/fake-steve-uncensored-eclipsecon.html) blog

### **M6 Focus**

*   M6 is Apr 07 -- Testing Apr 1 or 2 -- Should do better than last time
*   Currently [39 bugs assigned M6](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&target_milestone=3.0+M6&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) \- especially DaveD - what can we really get done
*   NLS Fixes - few still missing, see [mailing list](http://dev.eclipse.org/mhonarc/lists/dsdp-tm-dev/msg01723.html) \- **must have for M6** \- **AI Javier, DaveM**
*   **Unit Tests** \- next priority after API
*   Will migrate to new Releng after M6 (adopt P2, nightly tests, signing etc... too risky for now, focus on API)
*   Adopting [Api Tooling](./Api_Tooling "Api Tooling"): Martin tried it out for some plugins - renaming (CANCELLED->CANCELED) is not very well reflected - martin filed [bug 222905](https://bugs.eclipse.org/bugs/show_bug.cgi?id=222905) \- but we might want to rev down org.eclipse.rse.services from 3.0.0 back to 2.1.0
    *   No action item for us right now, Martin will adopt after M6

### **Hi-pri-bugs; community contributions; apply patches**

*   [bug 210682](https://bugs.eclipse.org/bugs/show_bug.cgi?id=210682) Rupen's multi-file copy/move/overwrite dialog **AI Rupen** merge again, **AI DaveM** apply patch soon
*   [bug 214887](https://bugs.eclipse.org/bugs/show_bug.cgi?id=214887) WinCE Subsystem - pending EMO Review
*   [bug 170910](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170910) RSE Terminal Integration - Montavista Contribution pending this friday for API change to allow Streams API for IHostShell
    *   Michael: we should probably help them making their Job easier by providing API for programmatic terminal connection
*   See the [Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for a query for open bugs with patches attached

### **Bug Discussions**

*   [bug 190231](https://bugs.eclipse.org/bugs/show_bug.cgi?id=190231) subsystem UI -> Core: **AI Martin** to ask Dave if questions - idea is an IAdaptable to adapt the Wizard Pages into something consumable in non-UI for configuring subsystems, e.g. Property Sets
*   [bug 220892](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220892) reving down dstore protocol version - will keep as-is at DataStore.8.0.0 for now, doing protocol handshake after Ganymede. **AI DaveM** create a new bug for the protocol handshake assign to Future
    *   Waiting for Code Contribution from another team - **AI DaveM** make them contribute real soon
    *   Martin: Will not accept any new feature into M6 after this Friday. After M6, API changes are subject to discussion, nobody has a right to change API so in the worst case they may have missed the train and need to fork off their private branch of RSE / DStore.
*   [bug 221211](https://bugs.eclipse.org/bugs/show_bug.cgi?id=221211) MultiStatus for IFileService batch operations - exception on first failure for modifying operations. No exceptions/multistatus on non-modifying operations. **AI DaveD/DaveM** update Javadocs when it's clear what we want
*   [bug 220379](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220379) Make DStoreFileService API - encodingHandler - wait on reporter - **AI DaveM** ask reporters
*   [bug 220547](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220547) SimpleSystemMessage message ID - globally unique message id vs. plugin-local status - Dialog Title: MessageID if globally unique / generic title based on severity if plugin-local - **AI DaveM** think about
*   [bug 218947](https://bugs.eclipse.org/bugs/show_bug.cgi?id=218947) IRemotePath idea - not for M6.
    *   DaveM: Naming convention -- IHostPath instead of IRemotePath since located in the Service?

*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

### Committer Status and Report

*   **Javier** leaving Symbian, going to work in Barcelona - will remain involved with DSDP; somebody else from Symbian to take over
    *   Fix NLS issues **AI Javier**
    *   [bug 212382](https://bugs.eclipse.org/bugs/show_bug.cgi?id=212382) ftpListingParser initCommands **AI Javier**
    *   Martin updating Commons Net to 1.5.0
*   **DaveD**
    *   [bug 217894](https://bugs.eclipse.org/bugs/show_bug.cgi?id=217894) Subsystem Configuration Families - not for M6 - **AI All** comment on the bug
    *   [bug 189274](https://bugs.eclipse.org/bugs/show_bug.cgi?id=189274) Import/export connections internal but TBD for M6
*   **DaveM:** -
    *   [bug 222404](https://bugs.eclipse.org/bugs/show_bug.cgi?id=222404) Associate property sets with RSE objects and keep those associated in the event of a rename or move - an interesting feature in exchange for events - DaveD: Looks interesting but need to look at closely; Martin - should do Events suggestion for now; maybe could use an adapter factory for data payload, but need more investigation
    *   EFS and encodings - No response from platform - off our radar for now
*   **Kevin:** -
*   **Xuan:** \- Will only have time for PropertyFileAdapter stuff: Property adapters for User actions -- will need some NLS changes
    *   Compile Commands Problem: Key in property sets is case insensitive in hashmap
    *   IPZilla: Getting only notifications for WinCE - Martin: Commons Net 1.5 not yet filed, JSch-0.1.37 is approved and in Platform M6
*   **Martin:** \- [bug 215301](https://bugs.eclipse.org/bugs/show_bug.cgi?id=215301) New project plan format -- Need to put Project Plan on the Web; **AI Martin** written ramp-down plan; Update Releng scripts to automatically run unit tests at night
    *   Searchcvs, Relnotes done; Little more work needed on web-build and promote.sh
    *   JSch-0.1.37 done in Platform M6, Commons.Net 1.5.0 not yet released - **AI Martin** create placeholder CQ
    *   Next tasks - Move SubsystemConfiguration implementation into non-UI; Lazy loading of SubsystemConfiguration (use the Proxy more); Lazy loading of UI adapters; some exceptions observed by Uwe (Wind River) in our nightly wheels
    *   [bug 221190](https://bugs.eclipse.org/bugs/show_bug.cgi?id=221190) EFS getChild() with relative path - perhaps need to check whether our impl still works properly
*   **Uwe:** -
*   **Rupen:** \- Merging multi-copy & rename
*   **Michael:** -
*   **Questions**

Vacation, Away
--------------

*   Martin in SFO Apr 14-18 for ESC and PluginFest
*   DaveD probably taking some time off

Action Items
------------

*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_5-Mar-2008#Action_Items "DSDP/TM/Committer Phone Meeting 5-Mar-2008") Action Items
*   **Everyone**: Review [bug 217894](https://bugs.eclipse.org/bugs/show_bug.cgi?id=217894) subsystem configuration families
*   **Rupen**: Merge [bug 210682](https://bugs.eclipse.org/bugs/show_bug.cgi?id=210682) multi-copy patch
*   **DaveD**: Finish profile import/export; Update [bug 221211](https://bugs.eclipse.org/bugs/show_bug.cgi?id=221211) IFileService multi-commands Javadoc
*   **DaveM**: NLS fixes in dstore.security; contact IBM teams for [bug 220892](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220892) new dstore features, and [bug 220379](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220379) DStoreFileService API; apply Rupen's patch; think about [bug 216252](https://bugs.eclipse.org/bugs/show_bug.cgi?id=216252) SystemMessages global vs. local message ID; create a new "Future" bug for dstore protocol handshake, cloned from [bug 220892](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220892)
*   **Xuan**: Finish PropertyFileAdapter stuff; Use Kevin's Properties for Unit Tests
*   **Kevin**: Website Updates
*   **Martin**: New Project Plan; Ganymede Rampdown Plan; Commons Net Placeholder CQ; UI/Non-UI Splitting; finish new releng; Look at PropertyDescriptor issues; unit tests
*   **Javier**: NLS fixes in discovery and FTP; [bug 212382](https://bugs.eclipse.org/bugs/show_bug.cgi?id=212382) ftp initCommands; add unit tests; document the Symbian internal test setup similar to [CVS](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204138#c20) \-\- see also [CVS_Development#Testing](./CVS_Development#Testing "CVS Development")
*   **Michael**: Terminal improvements

Next Meeting
------------

*   Next [BugDay/March_2008](./BugDay/March_2008 "BugDay/March 2008") on Mar 28
*   Monthly [DSDP/TM/Phone Meeting 2-Apr-2008](./DSDP/TM/Phone_Meeting_2-Apr-2008 "DSDP/TM/Phone Meeting 2-Apr-2008") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=4&day=2&year=2008&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Committer Phone Meeting 9-Apr-2008](./DSDP/TM/Committer_Phone_Meeting_9-Apr-2008 "DSDP/TM/Committer Phone Meeting 9-Apr-2008") (2 weeks) at [1500 UTC / 0800 SFO / 1000 Rochester / 1100 Toronto / 1600 London / 1700 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=4&day=9&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) \-\- take care of DST differences!


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_26-Mar-2008](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_26-Mar-2008))