

DSDP/TM/Committer Phone Meeting 5-Sep-2007
==========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Sep 5, 2007](./index.php?title=Sep_5,_2007&action=edit&redlink=1 "Sep 5, 2007 (page does not exist)") at [1500 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=9&day=5&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
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

*   IBM - Xuan Chen, Dave Dykstal, Dave McKnight
*   Wind River - Martin Oberhuber, Uwe Stieber, Michael Scharf
*   Symbian - Javier Montalvo Orus

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Agenda
------

*   Last meeting: [DSDP/TM/Committer Phone Meeting 28-Aug-2007](./DSDP/TM/Committer_Phone_Meeting_28-Aug-2007 "DSDP/TM/Committer Phone Meeting 28-Aug-2007")

### Current Work

*   **Skype Call Quality**
    *   Pretty good even though 7 participants; DaveM dropped off once
*   **Reminder: Aug 30th was RC1** as per [TM 2.0 Ramp down Plan for Europa#Ramp\_down\_for\_Europa\_SR1_.2828-Sep-2007.29](./TM_2.0_Ramp_down_Plan_for_Europa#Ramp_down_for_Europa_SR1_.2828-Sep-2007.29 "TM 2.0 Ramp down Plan for Europa"), no risky fixes for 2.0.1 after the 30th!
    *   Bugzilla TM "3.0" target milestone has been created; creating also "2.0.2" milestone; note that 2.0.2 bugs MUST be checked in to the branch, which is some effort, so this should be reserved for really important things only
    *   Branch not yet forked off, but policies do apply (need review)
    *   OK to check in to HEAD, Martin can merge to the branch
    *   Need 1-committer review, and Verification of fixes in an I-build after that time (RC1)
*   **Reminder: Start preparing / planning** for the [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./DSDP/TM/Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007")
    *   Room with outside internet access should be available in customer briefing center
    *   DaveD: Persistence, User-Defined Actions - Explain the plans, discuss them
    *   DaveM: Need to think
    *   MartinO: UI/Non-UI; New-connection-wizard: more user friendly while keeping it pluggable
    *   Kevin will be dedicating some time (up to 20 hrs a week)
    *   Rupen will be continuing (tentative)
*   **DaveD:** -
    *   [bug 194802](https://bugs.eclipse.org/bugs/show_bug.cgi?id=194802) \- NPE when restoring; might be gone in the meantime, analyze / reproduce? - **closing**
    *   [bug 198395](https://bugs.eclipse.org/bugs/show_bug.cgi?id=198395) \- Connect dstore with expired password - **need to look at perl APIs for pwd access**
    *   [bug 197036](https://bugs.eclipse.org/bugs/show_bug.cgi?id=197036) \- Avoid plugin activation, dont create all filterpools on startup - **not for 2.0.1**
    *   [bug 176577](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176577) \- Moving hosts up+down - **looking at for 2.0.1**
*   **DaveM:** \- **looking at these this week**
    *   [bug 196662](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196662) \- Refresh queries on dispatch thread - is it all fixed now?
    *   [bug 200557](https://bugs.eclipse.org/bugs/show_bug.cgi?id=200557) \- Review dnd from Project Explorer ([bug 192704](https://bugs.eclipse.org/bugs/show_bug.cgi?id=192704)
    *   [bug 199565](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199565), [bug 199566](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199566), [bug 199568](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199568) \- Deadlock issues due to synchronized methods calling out
*   **Kevin:** \- **n/a today**
    *   [bug 168219](https://bugs.eclipse.org/bugs/show_bug.cgi?id=168219) \- how to treat recursive delete of a tree where some elements are read-only
        *   **delete what we can delete**, and leave the read-only files untouched (That's what EFS does) --> Will need a change of implementation (Local and DStore) to avoid giving up as soon as one error occurs during delete, return a MultiStatus; might also add API for "force" in the future
*   **Javier:** \- Just back from vacation; will look at [bug 199773](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199773)
*   **Martin:** \- BugDay activities
*   **Uwe:** Included RSE JUnittests into our nightly product test suite.
*   **Rupen:** [bug 198728](https://bugs.eclipse.org/bugs/show_bug.cgi?id=198728) \- assign it to myself if Xuan does not mind. (working on same bug for artemis)
*   [BugDayAugust2007](./BugDayAugust2007 "BugDayAugust2007") \-\- August 31 -- Results:
    *   3 bugs fixed, reviewed by Martin; IRC was really quiet; more communication on bugzilla than IRC
*   **Questions**

*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   DaveD vacation Spt 27 - Oct 6

  

Action Items
------------

*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_28-Aug-2007#Action_Items "DSDP/TM/Committer Phone Meeting 28-Aug-2007") Action Items
*   **DaveD**: 2.0.1 important fixes, then Doc bugs (Tutorial)
*   **DaveM**: [bug 196662](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196662) refresh on dispatch thread
*   **Xuan**: Unit Tests
*   **Kevin**: 2.0.1 fixes
*   **Martin**: Look at PropertyDescriptor issues; EFS fixes; unit tests; Migration Docs, Releng Fixes, Newsgroup
*   **Javier**: 2.0.1 fixes, unit tests
*   **Michael**: Terminal performance improvements

Next Meeting
------------

*   Monthly [DSDP/TM/Phone Meeting 5-Sep-2007](./DSDP/TM/Phone_Meeting_5-Sep-2007 "DSDP/TM/Phone Meeting 5-Sep-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=9&day=5&year=2007&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Committer Phone Meeting 11-Sep-2007](./DSDP/TM/Committer_Phone_Meeting_11-Sep-2007 "DSDP/TM/Committer Phone Meeting 11-Sep-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=9&day=11&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./DSDP/TM/Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007")


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_5-Sep-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_5-Sep-2007))