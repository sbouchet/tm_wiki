

DSDP/TM/Committer Phone Meeting 14-Nov-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Nov 14, 2007](./index.php?title=Nov_14,_2007&action=edit&redlink=1 "Nov 14, 2007 (page does not exist)") at [1500 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=11&day=14&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
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
*   Wind River - Martin Oberhuber, (Uwe Stieber n/a), (Michael Scharf n/a)
*   Symbian - Javier Montalvo Orus

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Agenda
------

*   Last meeting: [DSDP/TM/Committer Phone Meeting 31-Oct-2007](./DSDP/TM/Committer_Phone_Meeting_31-Oct-2007 "DSDP/TM/Committer Phone Meeting 31-Oct-2007")

### Current Work

*   **Skype Call Quality**
    *   Javier not able to join today (worked after computer restart), others quality seems good
    *   Xuan had quality issues - heard DaveM badly though others heard him alrighty
*   **Planning** \- **AI Martin** to write up what we discussed in Toronto
    *   M3 Testing - how much time invested? (Martin: 2 hrs; Xuan: brief try; Kevin: 2.5 hrs; DaveM: .5 hrs; Javier: 2 hrs - verify some defects, some sanity)
        *   For next milestone, decide effort and if testing or not / when we know what's being changed
        *   Work on getting more Unit tests
        *   Javier: how to add tests to existing test suites
    *   EclipseCon
        *   IBM Travel bugdget: might get for conferences where there is a chance to talk to users
        *   Martin submitted a short tutorial and short talk again - for others, user-related talks are interesting
*   Bug Fixing - **Remember our 2-fix-per-week / 3 unittests-per-milestone plan**
*   **DaveD:** \- no news (got swamped by final IBM testing stuff)
*   **DaveM:** \- Multi-APIs -- significant performance gain for dstore (up to 10 times faster!); Unittests also look at performance; integrated with copy&paste / dnd
    *   Martin: slight inconsistency - uploadMulti() but getFileMultiple()
    *   [bug 208951](https://bugs.eclipse.org/bugs/show_bug.cgi?id=208951), [bug 207308](https://bugs.eclipse.org/bugs/show_bug.cgi?id=207308) Preferences for File Types: maintain own separate list (similar to what Team does)
        *   Artemis extension point for file types: how to resolve conflicts? User prefs have precedence over extension point
        *   Martin: Do we need ascii vs. binary transfer? - DaveM: On zSeries, text files are EBCDIC; some (external) tools, e.g. "make" might only understand UTF-8 or other standard encoding; further complicated with BIDI since that's handled very differently on EBCDIC
        *   What happens on "ASCII" type? - Download as binary, then convert into the "Default Local Encoding" according to java.io Property
        *   Originally, dstore did some conversions on the server but it turned out that BIDI is too complex and requires user interaction -- therefore doing it on the client now. This means, that it also works for FTP and SSH.
        *   Would FTP servers do some EBCDIC decoding in ASCII mode? - DaveD probably yes in the I5 filesystem, convert to some standard codepage
        *   EFS: Probably do two separate EFS providers, "rse" and "rsetext"
    *   [bug 187739](https://bugs.eclipse.org/bugs/show_bug.cgi?id=187739) exists() method in the SystemViewElementAdapter
*   **Kevin:** \- [bug 168000](https://bugs.eclipse.org/bugs/show_bug.cgi?id=168000) Remote Search improvements
*   **Xuan:** \- [bug 160775](https://bugs.eclipse.org/bugs/show_bug.cgi?id=160775) \[api\] \[breaking\] \[nl\] rename (at least within a zip) blocks UI thread: Jobs, ISystemCancelableOperation in Archives API
    *   Check in main API changes today; will work on Tar separately.
    *   Unittests: Lots of operations involve user interaction; WR has some work on TPTP AGR, Martin to probably leverage that after adding Unittests to N-builds and RSE UI/Non-UI splitting
*   **Javier:** \- [bug 199773](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199773) FTP upload as binary fixed; remaining fixes for hardcoded settings through DaveM's fixes for [bug 207308](https://bugs.eclipse.org/bugs/show_bug.cgi?id=207308) \-\- XML would be binary
    *   FTP: would we ever want to do encoding conversion when it's in the hands of the server?
    *   DaveM: Should we take the simple String based encoding conversions out of dstore and move into the general subsystem?
    *   Martin: Better not change anything unless we understand what we're doing, or have bug report requesting the change. So better keep the simple String conversions in dstore unless somebody asks to have them in SSH. For the user-contributed custom conversions, need to understand against what patterns / subsystems they are contributed... better keep the stuff dstore-specific for now. Ensure that corresponding Prefs pages are clearly dstore specific.
        *   Need to have a better understanding what the UI should look like for [bug 209704](https://bugs.eclipse.org/bugs/show_bug.cgi?id=209704) user-contributed conversions for BIDI -- **AI DaveM** ask Violaine about intended UI for this
    *   Javier working on Tests -- using an internal FTP server at Symbian for now -- how to move that into Open Source?
    *   Martin has root access on dsdp.eclipse.org -- install an FTP server that only allows access from "localhost"
        *   **AI Javier** document the Symbian internal test setup similar to [CVS](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204138#c20) \-\- see also [CVS_Development#Testing](./CVS_Development#Testing "CVS Development")
*   **Martin:** \- Released [TM 2.0.2](http://download.eclipse.org/dsdp/tm/downloads/drops/R-2.0.2-200711131300/index.php) and [TM 3.0M3](http://download.eclipse.org/dsdp/tm/downloads/drops/S-3.0M3-200711141025/index.php); Need to put Project Plan on the Web; Update Releng scripts to automatically run unit tests at night
*   **Uwe:** \- cleanup of 2 open-source bugs
*   **Rupen:** \- little bit Open Source bugfixes - not too much time
*   **Michael:** \- adding bytestream debug logging to Terminal
*   **Questions**
    *   Xuan: Today's fixes into M3? - Now

*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   Javier offsite next week, so not available
*   US Thanksgiving Thurs and Fri next week (Nov 22nd / 23rd)

Action Items
------------

*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_31-Oct-2007#Action_Items "DSDP/TM/Committer Phone Meeting 31-Oct-2007") Action Items
*   **DaveD**: fixes, unit tests
*   **DaveM**: fixes, unit tests; ask Violaine about [bug 209704](https://bugs.eclipse.org/bugs/show_bug.cgi?id=209704)
*   **Xuan**: fixes, unit tests
*   **Kevin**: fixes, unit tests
*   **Martin**: Write-up TM 3.0 Plan; Look at PropertyDescriptor issues; unit tests; Releng Fixes, Newsgroup
*   **Javier**: fixes, unit tests; document the Symbian internal test setup similar to [CVS](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204138#c20) \-\- see also [CVS_Development#Testing](./CVS_Development#Testing "CVS Development")
*   **Michael**: Terminal improvements

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 27-Nov-2007](./DSDP/TM/Committer_Phone_Meeting_27-Nov-2007 "DSDP/TM/Committer Phone Meeting 27-Nov-2007") at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=11&day=27&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 5-Dec-2007](./DSDP/TM/Phone_Meeting_5-Dec-2007 "DSDP/TM/Phone Meeting 5-Dec-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=12&day=5&year=2007&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_14-Nov-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_14-Nov-2007))