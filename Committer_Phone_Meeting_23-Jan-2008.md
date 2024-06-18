

DSDP/TM/Committer Phone Meeting 23-Jan-2008
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday Jan 23, 2007 at [1600 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=1&day=23&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | Martin to call everybody by Skype |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, kevin.j.doyle, xuan.chen886, rupen.mardirossian, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
    *   [2.1 Current Work](#Current-Work)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Xuan Chen, Dave McKnight, Dave Dykstal, Rupen Mardirossian
*   Wind River - Martin Oberhuber
*   Symbian - Javier Montalvo Orus

Agenda
------

*   Last meeting: [DSDP/TM/Phone Meeting 9-Jan-2008](./Phone_Meeting_9-Jan-2008 "DSDP/TM/Phone Meeting 9-Jan-2008")
*   Prev meeting: [DSDP/TM/Committer Phone Meeting 12-Dec-2007](./Committer_Phone_Meeting_12-Dec-2007 "DSDP/TM/Committer Phone Meeting 12-Dec-2007")

### Current Work

*   **Skype Call Quality**
*   **Planning** \- **AI Martin** to write up what we discussed in Toronto
    *   Think about assigning bugs to target milestones. What goes into 3.0 and what not?
*   Eugene new committer
*   TM Website
    *   [bug 216197](https://bugs.eclipse.org/bugs/show_bug.cgi?id=216197) Bugs link on the side nav bar is broken by that latest changes
    *   Kevin: Would like to change the TM website to be more like the Mylyn/RAP sites. Custom Nav bar, front page showing the product instead of a mission statement, etc. Is it okay to make changes in a new folder tm-new? Then can push it to the main site if everyone likes the changes?
    *   Martin: Would like to discuss the intended changes before going ahead. But sure you can create any new pages that are not linked from the main page at any time.
    *   Martin: Would like to get more dynamic information onto the homepage in an automated manner e.g. automated release notes with milestones
*   Bug Fixing - **Remember our 2-fix-per-week / 3 unittests-per-milestone plan**
    *   Since our [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007") it's now 14 weeks / 3 milestones, so each committer is due 28 fixes / 6 unittests
    *   Current situation is on [this bugzilla report](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=&y_axis_field=assigned_to&z_axis_field=&query_format=report-table&classification=DSDP&product=Target+Management&bug_status=RESOLVED&bug_status=VERIFIED&bug_status=CLOSED&chfieldfrom=2007-09-17&chfieldto=Now&chfield=bug_status&chfieldvalue=RESOLVED&format=table&action=wrap)
    *   Unittests: Xuan, DaveM, Javier added some; Martin 0; not sure about others; Martin working on Releng scripts next
*   **Javier** busy until end of Feb; hoping to get time for hi-pri bugs (but not new features)
*   **DaveD's** bugs are largely interrelated, currently working on [bug 197036](https://bugs.eclipse.org/bugs/show_bug.cgi?id=197036) \- some impacts on teamview, nopefully get done today or tomorrow
    *   RDC people want to import/export connections rather than profiles - want to see filters self-contained in connection. Might want to solve this by treating connection as a profile with a single connection, and merge it into a different profile. Or store the stuff under the connection itself.
    *   This is maybe related to [bug 160403](https://bugs.eclipse.org/bugs/show_bug.cgi?id=160403) Filters should be connection-private by default
*   **DaveM:** -
    *   [bug 209703](https://bugs.eclipse.org/bugs/show_bug.cgi?id=209703) \- Can one property page affect the contents of another property page?
    *   EFS and encodings - DaveM to put Martin on CC of the bug(s) he filed against Platform
    *   documenting plugin_customization.ini -- does it work out of the box? Problems in self-hosting scenario
    *   (TPF) product teams extended SystemView in the past, which is now internal: provide a public Composite that wraps SystemView and that they can extend? E.g. they provided workspace objects along remote objects. AI file bugzilla items for concrete use cases and discuss them there.
    *   [bug 207180](https://bugs.eclipse.org/bugs/show_bug.cgi?id=207180) \- Remove "Encoding" control from the Property Pages. Martin: Encodings are consumed by subsystems. Might want a "usesEncodings()" API in the subsystem, and if no subsystem is interested it can be removed. **AI Martin** comment on the bug
    *   [bug 209593](https://bugs.eclipse.org/bugs/show_bug.cgi?id=209593) \- UNIX permissions and ownership
        *   The separation between subsystem layer and service layer gets more and more polluted as concepts from the service layer are introduced into the subsystem layer... (e.g. IHostFilePermissions; constants from IFileService). Should these be kept separate in order to support an IRemoteFileSubsystem that does not need services?
            *   Subsystem should be able to work without an exchangeable Service, but may re-use constructs from the service layer. Maybe want to add getFilePermissions() on the subsystem layer? - It's an exercise of how to extend subsystem without actually modifying it. It was good to see how permission service could be added in a backward compatible way without changing core APIs; but it's making the subsystem layer a little inconsistent. The alternative is doing everything twice (on both layers) ... better to live with the "pollution".
        *   Martin finds it odd that IRemoteFile adapts to IFilePermissionsService... shouldn't the IFileService adapt to it? -
        *   Martin thinks that IHostFile objects should be immutable in order to make caching and threading safer - can we get rid of IHostFile#renameTo() ? Only the actual (Service) implementation should be able to create / change IHostFile objects. How to deal with "pending" permissions? Use a queue to avoid duplicate queries in dstore?
            *   unlike permissions, "name" identifies a file via getAbsoluteName() -- that led to problems in the past
            *   boils down to the question how reiably we think we understand the remote system
            *   similar to what we had with setReadOnly() -- need to know when we need to refresh
            *   Martin: The SERVICE should decide whether it wants to re-query or use the (locally modified) object
            *   Dave: But if it's delegated to the service, we need to make the UI aware of the changes
*   **Kevin:** \- n/a today
*   **Xuan:** \- Making archive operations cancelable - mostly finished;
    *   Some more work with property pages
    *   Some search related issues (on dstore)
    *   Performance issues not encountered any more, will verify, going to close
        *   Martin seen performance problems with dangling symbolic links - **AI Martin completed:** [bug 191374](https://bugs.eclipse.org/bugs/show_bug.cgi?id=191374) seems to be resolved now
    *   Xuan can look at FTP hidden files preferences issue
    *   **First PII drop on Feb 25th, Deadline until end of M6**; try to minimize any wholesale changes after Feb.25th
    *   Xuan to write testcases for NL testing
*   **Martin:** \- Need to put Project Plan on the Web; Update Releng scripts to automatically run unit tests at night
*   **Uwe:** \- n/a today
*   **Rupen:** \- [bug 210682](https://bugs.eclipse.org/bugs/show_bug.cgi?id=210682) \- Multi-file conflict resolution on Copy - dialog ready, jpeg posted on the bug
*   **Michael:** \- n/a today
*   **Questions**

*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   DaveD friday off; a week out of Rochester middle of Feb
*   Feb.18 is Family Day in Ontario
*   Martin at a Conference on Jan.28/29th

  

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_12-Dec-2007#Action_Items "DSDP/TM/Committer Phone Meeting 12-Dec-2007") Action Items
*   **Everyone**: review target milestone assignments of bugs (3.0); Review Rupen's Multi-file-conflict dialog proposal
*   **Kevin**: propose changes to TM homepage for discussion
*   **DaveM**: \[done\] put Martin on CC of EFS/Encodign Platform bug(s); Create (or make TPF people create) bugs with use cases for extending SystemView or not
*   **Martin**: (done) Comment on [bug 207180](https://bugs.eclipse.org/bugs/show_bug.cgi?id=207180) "Encoding Control in Host Property Page"; (done) Add [bug 191374](https://bugs.eclipse.org/bugs/show_bug.cgi?id=191374)number regarding performance issues with dangling symlinks

*   Old Action Items from previous meetings:
    *   **DaveD**: Decide whether Mac should be "primary" or "secondary" supported platform.
    *   **Martin**: Write-up TM 3.0 Plan; Look at PropertyDescriptor issues; unit tests; Releng Fixes, Newsgroup
    *   **Javier**: document the Symbian internal test setup similar to [CVS](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204138#c20) \-\- see also [CVS_Development#Testing](https://wiki.eclipse.org/CVS_Development#Testing "CVS Development")

Next Meeting
------------

*   Monthly [DSDP/TM/Phone Meeting 6-Feb-2008](./Phone_Meeting_6-Feb-2008 "DSDP/TM/Phone Meeting 6-Feb-2008") at [9am PST / 1700 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=2&day=6&year=2008&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Committer Phone Meeting 6-Feb-2008](./Committer_Phone_Meeting_6-Feb-2008 "DSDP/TM/Committer Phone Meeting 6-Feb-2008") (2 weeks) at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=2&day=6&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_23-Jan-2008](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_23-Jan-2008))