

DSDP/TM/Committer Phone Meeting 31-Jul-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Jul 31, 2007](./index.php?title=Jul_31,_2007&action=edit&redlink=1 "Jul 31, 2007 (page does not exist)") at [1500 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=7&day=31&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | **asterisk.eclipse.org** ID: **8985** Passcode: **12345** |

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

*   IBM - Dave McKnight, Dave Dykstal, Xuan Chen, Kevin Doyle
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber
*   Eclipse Foundation - Karl Matthias (joined late)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 24-Jul-2007](./Committer_Phone_Meeting_24-Jul-2007 "DSDP/TM/Committer Phone Meeting 24-Jul-2007")

### Current Work

*   **Asterisk Conferencing**
    *   When Kevin and Xuan hooked up 1-on-1 last week, quality was good
    *   Martin heard all others well but was very hard to understand (with SJPhone).
    *   Javier and Martin had troubles getting dialed in with Idefisk
    *   Karl found 3 errors in the Asterisk logs, will investigate; one perhaps due to the Asterisk server swapping, others due to network issues
    *   Falling back to fixed line (once again)

  

*   [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007")
    *   **Confirmed** Toronto Mon/Tue Sep 17/18 (+Wed half day)
    *   DaveD confirmed, Javier and Martin confirmed & booked flights
    *   **AI DaveM** talk to Pete Nicholls for a room 6-10 persons Mon Sep17 - Wed Sep19

*   Unit Tests / TPTP AGR
    *   Xuan adding more test cases for copyBatch()
        *   Martin's advice: do small tests with small data if you can;
        *   For large data, generate it on the fly (e.g. create 2000 files of 2 meg size each)
        *   Fuzz testing: have a random number generator; in case it fails, save the files on which it failed and/or the Random number seed
        *   Platform Core Tests: **AI Martin** direct Xuan to Symlink test
    *   Xuan knows now how to change the daemon port and avoid the UI popup
    *   Calling ISubSystem.internalResolveFilterString() worked slightly different in test than interactively - related to earlier supertransfer issue: when doing unit test, there is no cache whereas interactively there is already a cache
        *   To work around: query the parent of archive first (in order to get the cache), then query the archive itself

*   **Bugzilla**:
    *   Bugzilla 3.0 deployed - Saved Searches: [Userprefs](https://bugs.eclipse.org/bugs/userprefs.cgi?tab=saved-searches), import **RSE open with patch**, **TM Hi-Pri**, **TM Review Requested**
    *   Pls dont forget setting the **contributed** kwd when setting a bug with a contributed patch FIXED
    *   **Wiki:** Template notation for bugzilla bugs, see [Eugene Kuleshov's Blog](http://www.jroller.com/eu/entry/a_handy_tip_for_the)
    *   **tm-log.csv**: Pls edit in text editor; or refresh after using Excel
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)
    *   **DaveD:**
        *   [bug 197937](https://bugs.eclipse.org/bugs/show_bug.cgi?id=197937) AbstractSystemWizardPage: SystemMessageLine in title area of wizard dialogs, fix OK?
            *   DaveD: broadcast the change to IBM RSE Users and didnt hear back - ok to go ahead
            *   For certain error messages, IBM writes two levels of text (error itself, and procedure for fixing the error); but that's not being used in wizards; this feature is embedded in the SystemMessageLine construct
            *   In other dialogs which do have a SystemMessageLine, this may be important; would need at least a procedure that allows getting the 2nd level text
            *   **AI Martin** review whether AbstractSystemWizardPage did have a 2nd level access control before; but Dave not too concerned about it for the case of wizards
        *   [bug 194802](https://bugs.eclipse.org/bugs/show_bug.cgi?id=194802) Persistence issue reported by Greg Watson: UI/Non-UI
            *   DaveD has 1 more week before going on vacation; wants to address hi-pri issues before leaving (substitute: Xuan?)
        *   [bug 197036](https://bugs.eclipse.org/bugs/show_bug.cgi?id=197036), [bug 181939](https://bugs.eclipse.org/bugs/show_bug.cgi?id=181939) All filter pools created on startup - lazy loading - likely to go to **Future**
    *   **DaveM:** [bug 196632](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196632) FTP Passive Mode Setting: **Dont create PropertySet in the Constructor**
        *   [bug 196662](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196662) Refresh on Dispatch thread could be tricky since already in the event handler -- getObject() is there since the adapter has no exists() method; Service level API works different for missing parent directory on dstore and ssh
        *   **AI Martin** schedule a separate call with DaveM to discuss this on Thursday

Vacation, Away
--------------

*   Xuan -public holidays beginning of August (Aug 3rd, Aug 6th) in Toronto; one week off end of August
*   DaveD here next week, OOO afterwards
*   DaveM taking a couple weeks in August coming back 21nd
*   Javier OOO next tuesday, and last two weeks in August

--\> moving next week's meeting to Wed

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_24-Jul-2007#Action_Items "DSDP/TM/Committer Phone Meeting 24-Jul-2007") Action Items
*   **All** subscribe to Bugzilla 3.0 shared searches from Martin
*   **DaveD**: call Xuan regarding filling-in for Persistence during his vacation; 2.0.1 important fixes, then Doc bugs (Tutorial)
*   **DaveM**: **Ask Pete Nicholls about room for F2F meeting in Toronto**; [bug 196662](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196662) refresh on dispatch thread
*   **Xuan**: Xuan fix up tm-log.csv; Unit Tests; dstore performance issue
*   **Kevin**: 2.0.1 fixes
*   **Martin**: Review SystemMessageLine for 2nd level messages; Look at PropertyDescriptor issues; EFS fixes; unit tests; Migration Docs, EFS Fixes, Releng Fixes, Newsgroup
*   **Javier**: 2.0.1 fixes, unit tests
*   **Michael**: Terminal performance improvements

Next Meeting
------------

*   Monthly [DSDP/TM/Phone Meeting 1-Aug-2007](./Phone_Meeting_1-Aug-2007 "DSDP/TM/Phone Meeting 1-Aug-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=8&day=1&year=2007&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Committer Phone Meeting 8-Aug-2007](./Committer_Phone_Meeting_8-Aug-2007 "DSDP/TM/Committer Phone Meeting 8-Aug-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=8&day=8&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007")


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_31-Jul-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_31-Jul-2007))