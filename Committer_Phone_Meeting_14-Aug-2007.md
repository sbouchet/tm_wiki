

DSDP/TM/Committer Phone Meeting 14-Aug-2007
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday Aug 14, 2007 at [1500 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=8&day=14&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | **asterisk.eclipse.org** ID: **8988** Passcode: **12345** |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, kevin.j.doyle, xuan.chen886, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

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

*   IBM - Xuan Chen, Kevin Doyle
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 8-Aug-2007](./Committer_Phone_Meeting_8-Aug-2007 "DSDP/TM/Committer Phone Meeting 8-Aug-2007")

### Current Work

*   **Asterisk Conferencing**
    *   Totally Failed today -- Martin could login, Xuan and Kevin not - connection very choppy

*   **Kevin Read-Only Questions**
    *   [bug 197855](https://bugs.eclipse.org/bugs/show_bug.cgi?id=197855) \- when to enable the move / delete actions? - Depends on the File System: since we have no IFileService#canDelete(), we should always enable the action. Worst case is, that an error occurs when actually moving / deleting. That error should then be displayed to the user. But we have to rely on the user knowing what he does.
    *   Same bug -- NPE's in DecoratorManager after a file has been deleted, because the DSToreHostFile's name is null: DStore uses name==null to indicate deleted files. Therefore, IHostFile#isFile(), exists() etc. all need to return "false" if the name==null. Need to document this in the code.
    *   [bug 168219](https://bugs.eclipse.org/bugs/show_bug.cgi?id=168219) \- confirmation dialog for delete / move when a file/folder is read-only: always show the dialog. Live with the case that on UNIX, user can press "OK" to delete file, but the action could still fail (because parent is read-only). Should we try "setWritable" before trying to delete it?
        *   EFS Eclipse LocalFile#delete() does not set writable -- it fails with an exception in case Java cannot do java.io.File.delete()
        *   We should not make the IFileService too intelligent -- don't try to setWritable in IFileService.delete()
        *   But the File subsystem, when showing the confirmation dialog, could try to setWritable when the user confirmed deletion
        *   One problem could be, that when recursively deleting a tree in which some files are read-only, we are not asked for them
        *   Windows explorer asks for confirmation of read-only files ... can do "Yes for all"
        *   Don't get a MultiStatus with delete errors
*   **Another BugDay on August 31st** \-\- TM to take part (was announced on PlanetEclipse)

  

*   **Rupen Question**
    *   When shell is being created, the inputLine is disabled -- so it cannot get the focus. Is there a reason for having it disabled in createControl()?
    *   don't know, try it out

  

*   **Xuan Question**
    *   Logging: how to install the handler
    *   Won't have much time this week, because DaveM is not here
    *   One P1 for blocking in archive handler - may need to defer, because API does not allow for cancel

  

*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   Xuan week off end of August
*   DaveD vacation Aug.8 till Aug.20
*   DaveM vacation Aug.6 till Aug.21
*   Javier vacation Aug.13 till Aug.31

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_8-Aug-2007#Action_Items "DSDP/TM/Committer Phone Meeting 8-Aug-2007") Action Items
*   **DaveD**: 2.0.1 important fixes, then Doc bugs (Tutorial)
*   **DaveM**: **Ask Pete Nicholls about room for F2F meeting in Toronto**; [bug 196662](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196662) refresh on dispatch thread
*   **Xuan**: Unit Tests
*   **Kevin**: 2.0.1 fixes
*   **Martin**: Look at PropertyDescriptor issues; EFS fixes; unit tests; Migration Docs, EFS Fixes, Releng Fixes, Newsgroup
*   **Javier**: 2.0.1 fixes, unit tests
*   **Michael**: Terminal performance improvements

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 21-Aug-2007](./Committer_Phone_Meeting_21-Aug-2007 "DSDP/TM/Committer Phone Meeting 21-Aug-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=8&day=21&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 5-Sep-2007](./Phone_Meeting_5-Sep-2007 "DSDP/TM/Phone Meeting 5-Sep-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=9&day=5&year=2007&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007")


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_14-Aug-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_14-Aug-2007))