

DSDP/TM/Committer Phone Meeting 17-Oct-2007
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday Oct 17, 2007 at [1500 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=10&day=17&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
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
*   Symbian - (Javier Montalvo Orus n/a)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Agenda
------

*   Last meeting: [DSDP/TM/Committer Phone Meeting 3-Oct-2007](./Committer_Phone_Meeting_3-Oct-2007 "DSDP/TM/Committer Phone Meeting 3-Oct-2007")

### Current Work

*   **Skype Call Quality**
    *   Excellent for everyone today (7 participants)
*   **Code and Branching**
    *   continue working on HEAD; Martin can merge fixes to maintenance branch
    *   If a fix is a candidate for M-builds, please attach the patch on bugzilla and let Martin know
    *   Releasing into the M-builds is not painful for Martin but may be painful if not done before; Instructions are on [Bug 205297 comment 11](https://bugs.eclipse.org/bugs/show_bug.cgi?id=205297#c11)
    *   N-builds good for now, no need for I-builds
*   Committer Calls frequency
    *   keep 2 weeks
*   **Planning** \- **AI Martin** to write up what we discussed in Toronto
    *   Project Plan tbd; Xuan won't send notes because stuff is on the "Future Planning" page anyways.
*   Bug Fixing - **Remember our 2-fix-per-week / 3 unittests-per-milestone plan**
    *   DaveD is positive to hit the fix rate, hopefully more
    *   Deadline today at IBM for non-opensource stuff, should be better afterwards
    *   DaveM will merge some dstore specific stuff
    *   Migration going forward without too much help from core openRSE team
*   **Reminder:** [BugDay](https://wiki.eclipse.org/BugDay/October_2007) next Friday (October 26)
*   **DaveD:** \- vacation - [bug 202630](https://bugs.eclipse.org/bugs/show_bug.cgi?id=202630) new meaning of "default private system profile"?
    *   taken some time to check Terminal on the Mac
    *   compile error in HEAD! Cannot compile on the Mac! protected VirtualCanvas.getBackgroundColor() does not override private Control.getBackgroundColor()
        *   --\> filed [bug 206643](https://bugs.eclipse.org/bugs/show_bug.cgi?id=206643)
*   **DaveM:** \- [bug 187739](https://bugs.eclipse.org/bugs/show_bug.cgi?id=187739) exists() method in the SystemViewElementAdapter
*   **Kevin:** -
*   **Xuan:** \- any stuff involving NLS need to be finished by M6 (end of march); docs freeze is June 27
    *   Platform re-releasing 3.3.1 -- Martin: If Europa is updated, TM will also have updates there from the M-branch.
*   **Javier:** \- n/a today (will look at [bug 199773](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199773) FTP upload as binary)
*   **Martin:**
    *   Mostly been working on Terminal / M-builds
    *   [bug 202416](https://bugs.eclipse.org/bugs/show_bug.cgi?id=202416) **Question for DaveD:** NPE when loading profile: made it more robust, but how could it come that RSE profile data is wiped with zeros? What happens when an IOException occurs while saving a profile, can it become corrupted or is there a safeguard?
        *   DaveD: Never seen an exception - exceptions are logged but profile save fails silently; there is no recovery
        *   Martin: Potentially inform the user about exceptions during save; workspace on NFS drive is not recommended; perhaps fall back to different file name
        *   Profile save is below UI layer - would need new API allow catching exceptions!
        *   --\> Filed new [bug 206640](https://bugs.eclipse.org/bugs/show_bug.cgi?id=206640) \- could perhaps register with the Manager
    *   Was at ESE2007 - good attendance at TM talk;
        *   SAP ([link to slides](http://www.eclipsecon.org/summiteurope2007/index.php?page=detail/&id=65)) making [Memory Analyzer](https://www.sdn.sap.com/irj/sdn/wiki?path=/display/Java/Java+Memory+Analysis) available for free now, a great fast tool for analyzing heap dumps
        *   Xuan was not sure how to send a "stop" signal to a remote server process (Martin: do ps, then kill -QUIT process_id)
*   **Uwe:** \- working on commercial product
*   **Rupen:** \- [bug 204307](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204307) Should listFolders(IRemoteFile parent, String fileNameFilter, IProgressMonitor monitor) passing a null FileNameFilter parameter, be dealt with in the same way as listFiles and listFoldersAndFiles. This would require that all folders are returned by assigning a '*' to the fileNameFilter as oppose to leaving it null which is causing a NPE whenever listFolders(IRemoteFile parent, IProgressMonitor monitor) is called. This will require a javadoc change as well.
    *   DaveM: should be treated the same, accepting patch
*   **Michael:** \- n/a
*   **Questions**

*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_3-Oct-2007#Action_Items "DSDP/TM/Committer Phone Meeting 3-Oct-2007") Action Items
*   **DaveD**: fixes, unit tests
*   **DaveM**: fixes, unit tests
*   **Xuan**: fixes, unit tests
*   **Kevin**: fixes, unit tests
*   **Martin**: Write-up TM 3.0 Plan; Look at PropertyDescriptor issues; unit tests; Releng Fixes, Newsgroup
*   **Javier**: fixes, unit tests
*   **Michael**: Terminal performance improvements

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 31-Oct-2007](./Committer_Phone_Meeting_31-Oct-2007 "DSDP/TM/Committer Phone Meeting 31-Oct-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=10&day=31&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 7-Nov-2007](./Phone_Meeting_7-Nov-2007 "DSDP/TM/Phone Meeting 7-Nov-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=11&day=7&year=2007&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_17-Oct-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_17-Oct-2007))