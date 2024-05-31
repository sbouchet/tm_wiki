

DSDP/TM/Committer Phone Meeting 31-Oct-2007
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday Oct 31, 2007 at [1500 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=10&day=31&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
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
*   Wind River - Martin Oberhuber, Uwe Stieber, (Michael Scharf n/a)
*   Symbian - Javier Montalvo Orus

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Agenda
------

*   Last meeting: [DSDP/TM/Committer Phone Meeting 17-Oct-2007](./Committer_Phone_Meeting_17-Oct-2007 "DSDP/TM/Committer Phone Meeting 17-Oct-2007")

### Current Work

*   **Skype Call Quality**
    *   Excellent Quality with 8 participants; Rupen had trouble connecting (Martin invited him 5 times), Uwe was muted for unknown reason.
*   Committer Calls frequency - 2 weeks ok
*   **Planning** \- **AI Martin** to write up what we discussed in Toronto
*   Bug Fixing - **Remember our 2-fix-per-week / 3 unittests-per-milestone plan**
*   **DaveD:** \- Working on Profile / Persistence issues - writing test cases to reproduce issues, finding issues along the way thanks to the test cases ... going to roll out fixes over the next week
*   **DaveM:** \- [bug 187739](https://bugs.eclipse.org/bugs/show_bug.cgi?id=187739) exists() method in the SystemViewElementAdapter
    *   [bug 207178](https://bugs.eclipse.org/bugs/show_bug.cgi?id=207178) listFoldersAndFiles, consolidate the API?
        *   Consolidate: **Yes** \- listItems() or simply list() with an additional parameter to limit the kinds of items returned, e.g. as an int constant
        *   Add API: **Yes** \- listMultiple() with an array of parents; also get() and getMultiple() to get multiple individual files
        *   Keep old methods around as deprecated delegators for 1 milestone cycle
    *   [bug 207095](https://bugs.eclipse.org/bugs/show_bug.cgi?id=207095) Implicit connect now on getRemoteFileObject() -- now have a unit test for it ("FileSubsystemConsistencyTest")
*   **Kevin:** \- [bug 204810](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204810) Editor Upload fix -- consequence of moving upload from main thread to secondary thread -- might have been a regression in 2.0.1
    *   Looking at encoding bug where changing encoding of a file is not reflected when it was opened before. Should have a fix for it today or tomorrow.
    *   [bug 207189](https://bugs.eclipse.org/bugs/show_bug.cgi?id=207189) Better wizard for linking folders as EFS into projects - Martin wants to try and get more Community Participation
        *   Some IBM groups might be hopping on EFS
        *   Javier - Symbian not going to use EFS
        *   DaveM: Most annoying: When opening a remote project shared from EFS, files are missing - they are not refreshed automatically; Martin: Recommend linking folders into local projects for that reason
*   **Xuan:** \- [bug 160775](https://bugs.eclipse.org/bugs/show_bug.cgi?id=160775) Currently looking at "Rename running in UI thread" - will need changed API adding progress monitor. Concurrency issues with stuff going on while rename is running in background, e.g. getting properties of virtual files
    *   Concurrency: Will need a lock on the archive, which clients need to acquire (with progress monitor!) before they can access the archive
    *   Queries for Properties and List are good, because new information is updated in a cache immediately
    *   Problem with ZIP implementation: file is locked on disk
    *   Could use Martin's Mutex class (in clientserver package) for waiting; but since it also needs to go on the Server side, would need a variant of Mutex which uses a variant of progress monitor that works on the server. Cannot use synchronized because cancellation and a FIFO queue is needed
    *   DaveM has CancelableHandler for DStore - might need something different for Local
    *   After Rename, will look at cancellation issues
    *   Can put archive stuff aside and look at other things if necessary
    *   Time contributed to OpenSource depends on customer issues around debugger
*   **Javier:** \- working on couple of features (recursive delete in FTP, drag&drop, copy&paste with workaround by Download/upload) - thanks to Kevin!
    *   Martin asking about Unit Tests
    *   will look at [bug 199773](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199773) FTP upload as binary
*   **Martin:** \- Terminal fixes; backporting [bug 204810](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204810) for 2.0.x
    *   Need to put Project Plan on the Web; Update Releng scripts to automatically run unit tests at night
*   **Uwe:** \- no news
*   **Rupen:** \- no news
*   **Michael:** \- n/a today
*   **Questions**
    *   M3 milestone: testing? - DaveD: At least run the Unit tests; Martin has been doing that manually so far. Would also like to have 1 day of testing.
        *   **Martin created [TM 3.0 M3 Testing](./TM_3.0_M3_Testing "TM 3.0 M3 Testing") page TBD on Thursday 8-Nov-2007**
    *   EclipseCon: Will be discussed in PMC meeting this friday -- probably have a Tutorial on TM, and a Short Talk on New & Noteworthy

*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   Nov 1 is public holiday in Austria

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_17-Oct-2007#Action_Items "DSDP/TM/Committer Phone Meeting 17-Oct-2007") Action Items
*   **DaveD**: fixes, unit tests
*   **DaveM**: fixes, unit tests
*   **Xuan**: fixes, unit tests
*   **Kevin**: fixes, unit tests
*   **Martin**: Write-up TM 3.0 Plan; Look at PropertyDescriptor issues; unit tests; Releng Fixes, Newsgroup
*   **Javier**: fixes, unit tests
*   **Michael**: Terminal performance improvements

Next Meeting
------------

*   Monthly [DSDP/TM/Phone Meeting 7-Nov-2007](./Phone_Meeting_7-Nov-2007 "DSDP/TM/Phone Meeting 7-Nov-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=11&day=7&year=2007&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Committer Phone Meeting 14-Nov-2007](./Committer_Phone_Meeting_14-Nov-2007 "DSDP/TM/Committer Phone Meeting 14-Nov-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=11&day=14&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_31-Oct-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_31-Oct-2007))