

DSDP/TM/Committer Phone Meeting 10-Jul-2007
===========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Jul 10, 2007](/index.php?title=Jul_10,_2007&action=edit&redlink=1 "Jul 10, 2007 (page does not exist)") at [1500 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=7&day=10&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | **asterisk.eclipse.org** ID: **8977** Passcode: **1234** |
| Backup Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 News & Review Action Items](#News-.26-Review-Action-Items)
    *   [2.2 Plan for the TM Future](#Plan-for-the-TM-Future)
    *   [2.3 Current Work](#Current-Work)
    *   [2.4 Work post 2.0.1](#Work-post-2.0.1)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave McKnight, Dave Dykstal, Xuan Chen, Kevin Doyle
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, (Uwe Stieber n/a), (Michael Scharf n/a)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 3-Jul-2007](/DSDP/TM/Committer_Phone_Meeting_3-Jul-2007 "DSDP/TM/Committer Phone Meeting 3-Jul-2007")

### News & Review Action Items

| Martin | 100% | Releng stuff for 2.0.0.1 / patches; Configurable port for SSH / Telnet | 100% |
| --- | --- | --- | --- |
| DaveD | 90% | bugs | 50% |
| DaveM | 30% | some 2.0.1 fixes | 70% |
| Javier | 30% |  | 30% |
| Uwe | 5% | - | 5% |
| Michael | 10% |  | 10% |

### Plan for the TM Future

*   A TM Project Meeting is planned for SEPTEMBER 19th and 20th in Chicago, together with the Members Meeting.
*   Please review and edit [TM Future Planning](/TM_Future_Planning "TM Future Planning") together with your Requirements / Product Management folk
    *   Martin edited the planning page, adding a top-10 list of priorities - everybody welcome to review
    *   TPTP AGR for Unit Tests?
*   **Eclipse Rumors**
    *   Platform thinking about forking off a 4.0 branch in addition to the 3.4 Ganymede branch during the year
    *   Equinox working on Authentication and Authorization with pluggable authentication modules based on [JAAS](http://en.wikipedia.org/wiki/Java_Authentication_and_Authorization_Service) \-\- See [this message on equinox-dev](http://dev.eclipse.org/mhonarc/lists/equinox-dev/msg02455.html) \- Martin seeking contact with them

### Current Work

*   **Asterisk:** New Eclipse.org conferencing solution - Need Idefisk 1.37, see [Asterisk Conference Calls](/Asterisk_Conference_Calls "Asterisk Conference Calls")
    *   VoIP did not work for Xuan and DaveM (did not hear anything, were not asked for password)
    *   VoIP did not work for Javier (firewall issues: port UDP 4569 blocked)
    *   Javier tried US dialin to hook up with Martin only: heard quite some noise, Martin heard Javier but quite silent, also there seemed to be quite some delay. Martin will tell the Foundation people - keep the current phone number for now.
*   **Releng:** TM 2.0.0.1 released to downloads and update site - fixes [bug 192741](https://bugs.eclipse.org/bugs/show_bug.cgi?id=192741) ZIP Archives and [bug 194204](https://bugs.eclipse.org/bugs/show_bug.cgi?id=194204) FTP Move
    *   Releasing this was quite some work, next time we should try hard getting critical fixes into the original release
    *   Should any more patches be needed, these will go into R2\_0\_patches branch of the mapfiles
    *   2.0.1 work done in HEAD, with weekly I-builds on thursday
*   **Applying contributed patches:** Please add the "contributed" kwd when checking in to CVS and adding to the tm-log.csv. Big thanks to Xuan, Kevin and Rupen for all the valuable contributions!
    *   Applying the patches is high priority in order to avoid them getting outdated.
    *   Note there is an [Open Bugs with Patches Attached](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1) query on the [TM Bug Process](https://www.eclipse.org/dsdp/tm/development/bug_process.php) page (8th query from top)
*   [193329](https://bugs.eclipse.org/bugs/show_bug.cgi?id=193329) First Column in Table View - WR would like to see a fix for 2.0.1
    *   DaveM to change the heading to "Label" instead of "Name" for 2.0.1; cannot easily filter it away or split off the Icon
*   What is the intent of drag&drop a Subsystem? (Can currently drag to the Scratchpad; others look enabled but do not work)
    *   Only reason to drag hosts or subsystems is just for the Scratchpad; users might come up with a view where hosts are collected and grouped;
    *   User feedback is not very good (looks like one could drop the host in project explorer, but it does not do anything) - DaveM: not sure if we have control over that (With PluginTransfer we probably do not have enough information to give feedback it won't work) - **AI Martin** to file a bug regarding the canDrop user feedback
*   [Severity Major Bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit):
    *   **DaveM:** [193858](https://bugs.eclipse.org/bugs/show_bug.cgi?id=193858) RSE folder tree problem - tempfiles do not take connection name or user id on remote side into account; similar to tempfiles structure does not support tunnelling - [195285](https://bugs.eclipse.org/bugs/show_bug.cgi?id=195285) mountPathMappers enhancement - **AI DaveM look at this week**
    *   **Martin:** Telnet, EFS, Releng (consume Orbit officially)
    *   Any Doc issues still open? (**AI DaveD**) \- some Tutorial issues; defer until late in the 2.0.1 cycle? DaveD like to do it a little earlier than in the absolute end.
    *   Kushal to reassign almost all of his bugs to the Inbox
*   Javadoc Reviews: @since tag for new API, missing @param tags, ... can be fixed now for RSE since we are rebuilding just about every RSE plugin for 2.0.1 (except discovery, terminal, remotecdt, tests right now)
*   **Adding Unit Tests** will also be a high priority. Archive Handlers are a good candidate to test -- can write a single unit test for create, add, extract, modify, move and then apply to ZIP / Tar / Local / DStore
    *   Currently 19 JUnit tests in the org.eclipse.rse.test - **AI Xuan** to import into workspace, DaveD to answer questions

  

### Work post 2.0.1

*   Currently feels like too many bugs are assigned 2.0.1 -- but we'll decide that after 2.0 is released
*   **Bugzilla**: [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   Xuan - maybe some public holidays beginning of August (Aug 3rd, Aug 6th) in Toronto
*   DaveD working on and off
*   DaveM, DaveD taking a couple weeks in August
*   Javier ooo last two weeks in August

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_3-Jul-2007#Action_Items "DSDP/TM/Committer Phone Meeting 3-Jul-2007") Action Items
*   **Everyone review the [TM Future Planning](/TM_Future_Planning "TM Future Planning") page**
*   **DaveD**: 2.0.1 important fixes, then Doc bugs (Tutorial)
*   **DaveM**: 2.0.1 fixes, [195285](https://bugs.eclipse.org/bugs/show_bug.cgi?id=195285) mountPathMappers enhancement
*   **Kushal**: reassign bugs to Inbox
*   **Xuan**: look at existing org.eclipse.rse.tests, start JUnit tests for archive handlers
*   **Martin**: Contact Equinox people; File bug re. canDrop feedback; 2.0.1 fixes, unit tests; Migration Docs, EFS Fixes, Releng Fixes, Newsgroup
*   **Javier**: 2.0.1 fixes, unit tests
*   **Michael**: Terminal performance improvements

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 18-Jul-2007](/DSDP/TM/Committer_Phone_Meeting_18-Jul-2007 "DSDP/TM/Committer Phone Meeting 18-Jul-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=7&day=18&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 1-Aug-2007](/DSDP/TM/Phone_Meeting_1-Aug-2007 "DSDP/TM/Phone Meeting 1-Aug-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=8&day=1&year=2007&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_10-Jul-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_10-Jul-2007))