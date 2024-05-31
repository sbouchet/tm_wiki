

DSDP/TM/Committer Phone Meeting 21-Aug-2007
===========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Aug 21, 2007](/index.php?title=Aug_21,_2007&action=edit&redlink=1 "Aug 21, 2007 (page does not exist)") at [1500 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=8&day=21&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
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

*   IBM - Xuan Chen, Kevin Doyle, Dave Dykstal, Rupen Mardirossian
*   Wind River - Martin Oberhuber, Uwe Stieber

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Agenda
------

*   Last meeting: [DSDP/TM/Committer Phone Meeting 14-Aug-2007](/DSDP/TM/Committer_Phone_Meeting_14-Aug-2007 "DSDP/TM/Committer Phone Meeting 14-Aug-2007")

### Current Work

*   **Skype Call Quality**
    *   Very good for everyone (6 attendees, Rupen listening only)
*   **Reminder: Aug 30th is RC1** as per [TM 2.0 Ramp down Plan for Europa#Ramp\_down\_for\_Europa\_SR1_.2828-Sep-2007.29](/TM_2.0_Ramp_down_Plan_for_Europa#Ramp_down_for_Europa_SR1_.2828-Sep-2007.29 "TM 2.0 Ramp down Plan for Europa"), no risky fixes for 2.0.1 after the 30th! (Will fork off a 2.0.1 branch by then)
*   **Reminder: Start preparing / planning** for the [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](/DSDP/TM/Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007")
*   **DaveD:** [bug 194802](https://bugs.eclipse.org/bugs/show_bug.cgi?id=194802) \- NPE when restoring; might be gone in the meantime, analyze / reproduce?
    *   Analysis by Martin: should be gone by new method of waiting for InitRSEJob; supposedly the problem
    *   [bug 198395](https://bugs.eclipse.org/bugs/show_bug.cgi?id=198395) \- Connect dstore with expired password - Dave will look at it (IBM only thing)
    *   [bug 197036](https://bugs.eclipse.org/bugs/show_bug.cgi?id=197036) \- Avoid plugin activation, dont create all filterpools on startup - will be looking at this week, might be possible without API change
*   **DaveM:** [bug 196662](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196662) \- Refresh queries on dispatch thread - is it all fixed now?
    *   [bug 200557](https://bugs.eclipse.org/bugs/show_bug.cgi?id=200557) \- Review dnd from Project Explorer ([bug 192704](https://bugs.eclipse.org/bugs/show_bug.cgi?id=192704)
    *   [bug 199565](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199565), [bug 199566](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199566), [bug 199568](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199568) \- Deadlock issues due to synchronized methods calling out
*   **Kevin:** [bug 168219](https://bugs.eclipse.org/bugs/show_bug.cgi?id=168219) \- how to treat recursive delete of a tree where some elements are read-only
    *   Users will want recursive-delete including deleting read-only files. What's the best UI to give it to them?
    *   DaveD: How are symlinks treated? - will delete the link, not the file linked
        *   What if there are other authorization problems?
        *   Right way seems to be to **delete what we can delete**, and leave the read-only files untouched (That's what EFS does) --> Will need a change of implementation (Local and DStore) to avoid giving up as soon as one error occurs during delete
        *   Return a MultiStatus to report an accumulate of all the errors (EFS does this, but it's not an absolute must since the read-only ones remain so they can be explored)
        *   In addition to that, it may be nice to provide additional API in IFileService#delete(), to ask "force" (delete read-only elements by setting them writable before deletion). That API might also go into EFS. Such additional API is more client-server-friendly. After trying delete without "force", users could review the MultiStatus, and then try again with "force".
    *   **Uwe:** No news
    *   **Xuan:** Investigation on IBM RSE shows that Cmd processing uses a lot of memory (Hashmap, Array of output Strings) - will look at with DaveM
    *   **Rupen:** No news
*   [BugDayAugust2007](/BugDayAugust2007 "BugDayAugust2007") \-\- August 31 -- TM taking part: committers sign up if they can hang out on [IRC](/IRC "IRC") (channel #eclipse-bugs), add "bugday" keyword to applicable bugs
*   **Questions**
    *   Nothing except what's mentioned above

*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   Labor Day (Sep.3rd in US, CDN also Sep.4th)
*   Xuan vacation next week (Aug.27- Sep.2)
*   DaveM vacation Aug.6 till Aug.23
*   Javier vacation Aug.13 till Aug.31

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_14-Aug-2007#Action_Items "DSDP/TM/Committer Phone Meeting 14-Aug-2007") Action Items
*   **DaveD**: 2.0.1 important fixes, then Doc bugs (Tutorial)
*   **DaveM**: **Ask Pete Nicholls about room for F2F meeting in Toronto**; [bug 196662](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196662) refresh on dispatch thread
*   **Xuan**: Unit Tests
*   **Kevin**: 2.0.1 fixes
*   **Martin**: Look at PropertyDescriptor issues; EFS fixes; unit tests; Migration Docs, EFS Fixes, Releng Fixes, Newsgroup
*   **Javier**: 2.0.1 fixes, unit tests
*   **Michael**: Terminal performance improvements

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 28-Aug-2007](/DSDP/TM/Committer_Phone_Meeting_28-Aug-2007 "DSDP/TM/Committer Phone Meeting 28-Aug-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=8&day=28&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 5-Sep-2007](/DSDP/TM/Phone_Meeting_5-Sep-2007 "DSDP/TM/Phone Meeting 5-Sep-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=9&day=5&year=2007&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](/DSDP/TM/Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007")


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_21-Aug-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_21-Aug-2007))