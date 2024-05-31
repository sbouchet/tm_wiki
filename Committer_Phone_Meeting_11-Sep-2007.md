

DSDP/TM/Committer Phone Meeting 11-Sep-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Sep 11, 2007](./index.php?title=Sep_11,_2007&action=edit&redlink=1 "Sep 11, 2007 (page does not exist)") at [1500 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=9&day=11&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
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

*   IBM - Xuan Chen, Dave Dykstal, Dave McKnight, Rupen Mardirossian, Kevin Doyle
*   Wind River - Martin Oberhuber, Uwe Stieber, Michael Scharf
*   Symbian - Javier Montalvo Orus

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Agenda
------

*   Last meeting: [DSDP/TM/Committer Phone Meeting 5-Sep-2007](./DSDP/TM/Committer_Phone_Meeting_5-Sep-2007 "DSDP/TM/Committer Phone Meeting 5-Sep-2007")

### Current Work

*   **Skype Call Quality**
*   **Intensive [TM 2.0.1 Testing](./TM_2.0.1_Testing "TM 2.0.1 Testing") on Thursday**
*   **Reminder: Aug 30th was RC1** as per [TM 2.0 Ramp down Plan for Europa#Ramp\_down\_for\_Europa\_SR1_.2828-Sep-2007.29](./TM_2.0_Ramp_down_Plan_for_Europa#Ramp_down_for_Europa_SR1_.2828-Sep-2007.29 "TM 2.0 Ramp down Plan for Europa"), no risky fixes for 2.0.1 after the 30th!
    *   Bugzilla TM "3.0" target milestone has been created; creating also "2.0.2" milestone; note that 2.0.2 bugs MUST be checked in to the branch, which is some effort, so this should be reserved for really important things only
    *   Branch not yet forked off, but policies do apply (need review)
    *   OK to check in to HEAD, Martin can merge to the branch
    *   Need 1-committer review, and Verification of fixes in an I-build after that time (RC1)
*   **Reminder: Start preparing / planning** for the [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./DSDP/TM/Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007")
    *   Room with outside internet access should be available in customer briefing center
    *   Xuan: How to prepare?
        *   1\. Make up your minds WHAT you want to achieve for 3.0; we should come up with plan items, priorities, and target milestones
        *   2\. Get initial ideas how to achieve this, such that we can discuss architecture and approaches.
    *   What's a Coding Camp? - Martin: We'll do a planning meeting, but also with hands on the code for prototyping and experimenting
    *   DaveD: Persistence, User-Defined Actions - Explain the plans, discuss them
    *   DaveM: Need to think
    *   MartinO: UI/Non-UI; New-connection-wizard: more user friendly while keeping it pluggable
    *   Kevin will be dedicating some time (up to 20 hrs a week)
    *   Rupen will be continuing (tentative)
*   **DaveD:** -
    *   [bug 194802](https://bugs.eclipse.org/bugs/show_bug.cgi?id=194802) \- NPE when restoring; might be gone in the meantime, analyze / reproduce? - **closed WORKSFORME**
        *   What to do in the future? - Martin: put a note on [bug 202866](https://bugs.eclipse.org/bugs/show_bug.cgi?id=202866), in the future we should move all SystemRegistry to non-UI and ensure that whatever client gets a SystemRegistry already gets an initialized one (i.e. synchronous initialization, like Eclipse core.resources). But we can discuss this in the future.
    *   [bug 198395](https://bugs.eclipse.org/bugs/show_bug.cgi?id=198395) \- Connect dstore with expired password - **need to look at perl APIs for pwd access** \- **not for 2.0.1**
    *   [bug 197036](https://bugs.eclipse.org/bugs/show_bug.cgi?id=197036) \- Avoid plugin activation, dont create all filterpools on startup - **not for 2.0.1**
    *   [bug 176577](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176577) \- Moving hosts up+down - **looking at for 2.0.1 today**
*   **DaveM:** \- **looking at these this week**
    *   [bug 196662](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196662) \- Refresh queries on dispatch thread - initial problem fixed but not ideally; some additional changes will be needed but they need API related to [bug 187739](https://bugs.eclipse.org/bugs/show_bug.cgi?id=187739) and an exists() method in the SystemViewElementAdapter -- **defer after 2.0.1**
    *   [bug 200557](https://bugs.eclipse.org/bugs/show_bug.cgi?id=200557) \- Review dnd from Project Explorer ([bug 192704](https://bugs.eclipse.org/bugs/show_bug.cgi?id=192704) ok
    *   [bug 199565](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199565), [bug 199566](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199566), [bug 199568](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199568) \- Deadlock issues due to synchronized methods calling out; will be able to fix
*   **Kevin:** \- [bug 168219](https://bugs.eclipse.org/bugs/show_bug.cgi?id=168219) recursive delete w/read-only moved to "Future"
*   **Xuan:** \- [bug 202686](https://bugs.eclipse.org/bugs/show_bug.cgi?id=202686) \- going to disable or fix supertransfer? - Found solution for two issues, a third one (refresh) is still open due to race condition (works during debug but fails in nondebug); if unable to find the issue, will disable supertransfer in the Preferences.
    *   Martin: Can use java.io.File#deleteOnExit() in order to make the temporary zip deleted on disconnect dstore;
    *   Xuan: Seems to be more a view update issue than actually on the Server
*   **Javier:** \- will look at [bug 199773](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199773) FTP upload as binary
    *   Found a problem with UI/Non-UI splitting, because Ascii/Binary properties are living in UI -- FTPService gets wrong isBinary tag (DaveM: DStore - RemoteFile#isBinary() seems to be OK) - Javier will further work on it
    *   [bug 202758](https://bugs.eclipse.org/bugs/show_bug.cgi?id=202758) FTP hangs completely due to missing server answer for completePendingCommand() - not reproducable by Martin, but reproducable by Michael; Michael writing a Unittest
*   **Martin:** \- [bug 202630](https://bugs.eclipse.org/bugs/show_bug.cgi?id=202630) what is the meaning of the "default private system profile"? - WR Workbench automatically fills this from a Registry. Should RSE ensure that there is always exactly one default private profile? Into what profile should connections be auto-generated... should there be a "WR Registry" profile? But then, what if users create connections themselves, would they create them into the "WR Registry" profile?
    *   DaveM: Original design was that there is always exactly one "default private" profile, which is not intended to be shared;
    *   DaveD: The notion of "default private" is legacy -- all profiles should be inherently shareable; default private is a persisted attribute, but probably should not be (Martin is OK with having a persisted attribute "private" - but the attribute "default" can not really be persisted because we don't know who claims to default)
    *   Martin: ensureDefaultPrivate() is not consistent with getDefaultPrivate() -- if it already finds an active default private one, it should not try creating a new one;
    *   Will need to think about how to address in our product
    *   [bug 202416](https://bugs.eclipse.org/bugs/show_bug.cgi?id=202416) NPE when loading profile: made it more robust, but how could it come that RSE profile data is wiped with zeros? What happens when an IOException occurs while saving a profile, can it become corrupted or is there a safeguard?
    *   [bug 202866](https://bugs.eclipse.org/bugs/show_bug.cgi?id=202866) Exceptions when browsing during early init - DaveM please review
*   **Uwe:** -
*   **Rupen:** -
*   **Michael:** \- Terminal Performance branch: 300k lines/sec on Windows, 8000 lines/sec on Linux; **everybody is OK with putting this into 2.0.1**
*   **Questions**

*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   DaveD vacation Spt 27 - Oct 9
*   MartinO mostly away Sep24 - Sep 28 (only doing releng stuff that week)

Action Items
------------

*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_5-Sep-2007#Action_Items "DSDP/TM/Committer Phone Meeting 5-Sep-2007") Action Items
*   **DaveD**: 2.0.1 fixes, then Doc bugs (Tutorial)
*   **DaveM**: 2.0.1 fixes
*   **Xuan**: 2.0.1 fixes (Supertransfer)
*   **Kevin**: testing
*   **Martin**: Look at PropertyDescriptor issues; EFS fixes; unit tests; Migration Docs, Releng Fixes, Newsgroup
*   **Javier**: 2.0.1 fixes, unit tests
*   **Michael**: Terminal performance improvements

Next Meeting
------------

*   [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](./DSDP/TM/Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007")
*   [DSDP/TM/Committer Phone Meeting 3-Oct-2007](./DSDP/TM/Committer_Phone_Meeting_3-Oct-2007 "DSDP/TM/Committer Phone Meeting 3-Oct-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=10&day=3&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 3-Oct-2007](./DSDP/TM/Phone_Meeting_3-Oct-2007 "DSDP/TM/Phone Meeting 3-Oct-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=10&day=3&year=2007&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_11-Sep-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_11-Sep-2007))