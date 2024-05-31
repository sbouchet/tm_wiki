

DSDP/TM/Committer Phone Meeting 27-Nov-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Nov 27, 2007](./index.php?title=Nov_27,_2007&action=edit&redlink=1 "Nov 27, 2007 (page does not exist)") at [1600 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=11&day=27&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
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

*   IBM - Xuan Chen, Dave McKnight, Kevin Doyle, Dave Dykstal, Rupen Mardirossian
*   Wind River - Martin Oberhuber, Uwe Stieber (Michael Scharf n/a)
*   Symbian - Javier Montalvo Orus

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Agenda
------

*   Last meeting: [DSDP/TM/Committer Phone Meeting 14-Nov-2007](./DSDP/TM/Committer_Phone_Meeting_14-Nov-2007 "DSDP/TM/Committer Phone Meeting 14-Nov-2007")

### Current Work

*   **Skype Call Quality**
    *   Some quality problems (Echo, break-ups) with Rupen, Kevin and Xuan. Resolved by kicking and re-dialing
    *   Conference setup was hard until everybody was in (multiple tries), but in the end it worked OK with 8 participants.
*   **Planning** \- **AI Martin** to write up what we discussed in Toronto
*   **[BugDay](https://wiki.eclipse.org/BugDay/November_2007)** this Friday November 30 -- currently 23 bugs marked for BugDay
    *   Kushal and Kevin started the [RSE World blog](http://rseworld.blogspot.com/2007/11/target-management-202-released.html), will write about BugDay
*   Bug Fixing - **Remember our 2-fix-per-week / 3 unittests-per-milestone plan**
    *   Since our [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./DSDP/TM/Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007") it's now 10 weeks / 2 milestones, so each committer is due 20 fixes / 6 unittests
    *   Current situation is on [this bugzilla report](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=&y_axis_field=assigned_to&z_axis_field=&query_format=report-table&classification=DSDP&product=Target+Management&bug_status=RESOLVED&bug_status=VERIFIED&bug_status=CLOSED&chfieldfrom=2007-09-17&chfieldto=Now&chfield=bug_status&chfieldvalue=RESOLVED&format=table&action=wrap): DaveM 43, MichaelS 31, Martin 20, Xuan 13, Kevin 12, Javier 4, Uwe 3, DaveD 3
    *   Also grab simple bugs to get the count down -- that's what Rupen's doing
    *   Unittests: Xuan, DaveM, Javier added some; Martin 0; not sure about others; Martin will add Releng scripts next
*   **DaveD:** \- [bug 160403](https://bugs.eclipse.org/bugs/show_bug.cgi?id=160403) Filters should be connection-private by default
    *   Hi-Pri P2/Major bugs -- starting to work on the bug backlog;
    *   What should we do with the RSE Programmer Guide [Extensions.html](http://dsdp.eclipse.org/help/latest/topic/org.eclipse.rse.doc.isv/guide/Extensions.html) document compared to the [Extension Points Reference](http://dsdp.eclipse.org/help/latest/topic/org.eclipse.rse.doc.isv/reference/extension-points/org_eclipse_rse_subsystems_files_core_remoteFileTypes.html)? Should we try to keep them in sync manually, or replace with a link to the Reference?
        *   Probably just change the wording: "These are the most useful extension points... see the reference for others" -- **New** [bug 211095](https://bugs.eclipse.org/bugs/show_bug.cgi?id=211095)
*   **DaveM:** \- New P2 Regressions to be fixed in M4 urgently:
    *   [bug 209704](https://bugs.eclipse.org/bugs/show_bug.cgi?id=209704) \- Contribute encoding conversion extension point
        *   Upload and download are slightly different; receive-all-then-convert or convert-on-the-fly
        *   Have it in subsystem or in service? - Martin: What happens if user selects a conversion but service does not provide/support it?
        *   Perhaps have a supportsEncodingConversion() in IFileService with a default returning false in AbstractFileService; and subsystem to check
    *   [bug 210555](https://bugs.eclipse.org/bugs/show_bug.cgi?id=210555) \- NPE during ssh files / delete - fixed by Xuan, by putting code in "Local" only
        *   [bug 211067](https://bugs.eclipse.org/bugs/show_bug.cgi?id=211067) \- (Xuan) get rid of SystemMessages in Service layer
            *   DaveD: SystemMessages are heavily used in IBM products, they rely on having message ID's
            *   There are two problems: (a) the whole interface, and (b) the format in which messages are stored
            *   Martin: What does SystemMessage have, that could not be mapped to an IStatus object? --> The Level 2 Text
                *   The namespace spanned by IStatus is more general, SystemMessage codes need to be "administered" to ensure uniqueness
            *   Could we define an "RSEStatus" object that has all the properties we need from SystemMessage but still conforms to IStatus
            *   DaveD: There must be an associated Property with the IStatus (to do something useful, in case the message is not being translated)
            *   **AI Martin** Cover these ideas in the bug
    *   [bug 210563](https://bugs.eclipse.org/bugs/show_bug.cgi?id=210563) \- No error message shown when failure during expanding a filter
    *   [bug 209703](https://bugs.eclipse.org/bugs/show_bug.cgi?id=209703) \- Can one property page affect the contents of another property page?
        *   Martin's recommendation: keep property pages self-contained wherever possible; cross-modification may be possible
        *   Alternative was to have an extension point to modify the existing property page
            *   Uwe: The Property Dialog now has IPageChangeListener (new API since Eclipse 3.1) -- might help to fix the problem; the only undefined point is when the event occurs, before or after the actual change; together with IPropertyChangeListener
            *   **AI DaveM** Look at IPageChangeListener / E-Mail to [eclipse.org-committers@eclipse.org](mailto:eclipse.org-committers@eclipse.org)
*   **Kevin:** \- [bug 208778](https://bugs.eclipse.org/bugs/show_bug.cgi?id=208778) EFS#APPEND
*   **Xuan:** \- Tar handling; some IBM issues on the side
*   **Javier:** \- Been on vacation last week; some Symbian stuff right now; cannot promise the bugcount promise
*   **Martin:** \- Worked on [TCF](./DSDP/TM/TCF_FAQ "DSDP/TM/TCF FAQ"); Need to put Project Plan on the Web; Update Releng scripts to automatically run unit tests at night
*   **Uwe:** \- Did some fix to the New Connection Wizard first page (systemType selection)
*   **Rupen:** \- [bug 210682](https://bugs.eclipse.org/bugs/show_bug.cgi?id=210682) \- Discussion on scope of enhancement? Discussions on which buttons will/should be used in the new renaming dialog. Should the rename button even exist?
    *   DaveM: Rename makes sense for a single file, but not for multiple files (one easily loses track)
    *   Martin: Compare directories first, come up with a table of conflicts; allow user to select each line in turn, then compare/cancel etc. DaveM: Similar to the "Rename Multiple" Dialog
    *   Renaming is just a workaround anyways. People don't want to rename. They want to diff the files to see what's the right version
    *   Gravitating towards something very simple -- show all conflicts, overwrite all / cancel all; keep advanced operations like overwrite / diff / etc to the Team/Sync integration; **AI Martin** add on the bug
*   **Michael:** -
*   **Questions**

*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

Action Items
------------

*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_14-Nov-2007#Action_Items "DSDP/TM/Committer Phone Meeting 14-Nov-2007") Action Items
*   **DaveD**: fixes, unit tests
*   **DaveM**: Ask committers about multi-property-dialog; fixes, unit tests; ask Violaine about [bug 209704](https://bugs.eclipse.org/bugs/show_bug.cgi?id=209704)
*   **Xuan**: fixes, unit tests
*   **Kevin**: fixes, unit tests
*   **Martin**: Update bugzilla's; Write-up TM 3.0 Plan; Look at PropertyDescriptor issues; unit tests; Releng Fixes, Newsgroup
*   **Javier**: fixes, unit tests; document the Symbian internal test setup similar to [CVS](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204138#c20) \-\- see also [CVS_Development#Testing](./CVS_Development#Testing "CVS Development")
*   **Michael**: Terminal improvements

Next Meeting
------------

*   Monthly [DSDP/TM/Phone Meeting 5-Dec-2007](./DSDP/TM/Phone_Meeting_5-Dec-2007 "DSDP/TM/Phone Meeting 5-Dec-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=12&day=5&year=2007&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Committer Phone Meeting 12-Dec-2007](./DSDP/TM/Committer_Phone_Meeting_12-Dec-2007 "DSDP/TM/Committer Phone Meeting 12-Dec-2007") at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=12&day=12&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) (without Kevin and Rupen)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_27-Nov-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_27-Nov-2007))