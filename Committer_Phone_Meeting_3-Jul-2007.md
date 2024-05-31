

DSDP/TM/Committer Phone Meeting 3-Jul-2007
==========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Jul 3, 2007](./index.php?title=Jul_3,_2007&action=edit&redlink=1 "Jul 3, 2007 (page does not exist)") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=7&day=3&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Invited Attendees](#Invited-Attendees)
*   [2 Notes](#Notes)
    *   [2.1 News & Review Action Items](#News-.26-Review-Action-Items)
    *   [2.2 Plan for the TM Future](#Plan-for-the-TM-Future)
    *   [2.3 Looking back on Europa](#Looking-back-on-Europa)
    *   [2.4 CM Strategy going forward](#CM-Strategy-going-forward)
    *   [2.5 Open Work for 2.0.1](#Open-Work-for-2.0.1)
    *   [2.6 Work post 2.0.1](#Work-post-2.0.1)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Invited Attendees
-----------------

*   IBM - Dave McKnight, Dave Dykstal, Xuan Chen, Kevin Doyle
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, (Uwe Stieber n/a), (Michael Scharf n/a)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 26-Jun-2007](./DSDP/TM/Committer_Phone_Meeting_26-Jun-2007 "DSDP/TM/Committer Phone Meeting 26-Jun-2007")

### News & Review Action Items

| Martin | 100% | Release Notes, Releng stuff for maintenance | 100% |
| --- | --- | --- | --- |
| DaveD | 90% |  | 90% |
| DaveM | 30% | some 2.0.1 fixes | 30% |
| Javier | 30% | critical "ftp moves" fix | 30% |
| Uwe | 5% | - | 5% |
| Michael | 10% | 1 bugfix for terminal | 10% |

### Plan for the TM Future

*   A TM Project Meeting is planned for SEPTEMBER 19th and 20th in Chicago, together with the Members Meeting.
*   Please review and edit [TM Future Planning](./TM_Future_Planning "TM Future Planning") together with your Requirements / Product Management folk
    *   WR: Main focus on quality / decrease bug backlog (focus on 2.0.1)
    *   IBM: Focus on reducing bug backlog; team support (import and export profiles); user-defined actions (might need feature branch if started before 2.0.1)
    *   Symbian: At the moment just 30% on open source - maintenance and bug fixing; Unit tests
    *   TPTP AGR for Unit Tests?
*   --\> Everybody most interested in reducing the bug backlog and adding unit tests for now. Will discuss feature additions at the F2F meeting mid September, probably earlier.
*   Martin would like to see a new unit test for every issue fixed (such that we shield against regressions). Will help others getting started with the unit tests.

### Looking back on Europa

*   Two critical bugs late in the game - we should have put more focus on these and try a fix for 2.0 -- creating patches now is a lot of effort:
    *   [192741](https://bugs.eclipse.org/bugs/show_bug.cgi?id=192741) Archive move/copy when deeper than level 1
    *   [194204](https://bugs.eclipse.org/bugs/show_bug.cgi?id=194204) FTP moves on Rename
*   **New & Noteworthy** \- is it correct and complete?
*   **Release Notes** \- these mostly delegate to dynamic Wiki content (for Migration, Known Issues)
*   Next time, we should attack critical issues earlier - anything we can avoid having to deliver as patch (but rather squeeze into the release) is less effort.

### CM Strategy going forward

*   Repository is open for 2.0.1 checkins.
*   **2.0.1 work in HEAD** for now. Since all of us are interested in bugfixes only for now, and we have no pending API changes. We can branch off at any time - decide it when we are at the point where we want work on new features / API changes.
*   **Avoid API changes**, both breaking backward and upward compatibility: NO new methods, no method signature changes in any public classes unless in an "internal" package. Create bugzilla's and defer work if you come across something that you think needs an API change - we can discuss these case by case.
*   **Avoid unnecessary changes** for now - focus on minmal changes if possible. We want to keep as many plugins as possible unchanged.
    *   However, when already working on some code, **Make it warning free before checkin** (Especially fix Javadoc @param, @since tags, compiler warnings).
*   **Martin will take care of plugin version changes**.
*   For critical bug fixes only, Martin created **branch R2\_0\_maintencance on the mapfile project (org.eclipse.rse.build) only**. In this branch we handle hotfixes which are delivered as M-builds and patches on the update site. These are only hand-selected bug fixes for critical issues which need to be deployed before 2.0.1 ships. Projects are NOT branched for now until it turns out to be necessary.
*   2.0.1 builds are I-builds since they come from HEAD. The M-builds are hand-selected bug fixes from R2\_0\_maintenance.
*   **Terminal:** want to do a feature branch?

### Open Work for 2.0.1

*   [Severity Major Bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit):
    *   [193858](https://bugs.eclipse.org/bugs/show_bug.cgi?id=193858) RSE folder tree problem - tempfiles do not take connection name or user id on remote side into account; similar to tempfiles structure does not support tunnelling - remoteMountPathMappers extension point should be working
    *   **Martin:** Telnet, EFS, Releng (consume Orbit officially), Configurable port for SSH / Telnet
    *   Any Doc issues still open? (**AI DaveD**) \- some Tutorial issues; defer until late in the 2.0.1 cycle? DaveD like to do it a little earlier than in the absolute end.
    *   Kushal to reassign almost all of his bugs to the Inbox

### Work post 2.0.1

*   Javadoc Reviews: @since tag for new API, missing @param tags, ... better don't change since these force rebuild of many plugins
*   Currently feels like too many bugs are assigned 2.0.1 -- but we'll decide that after 2.0 is released
*   **Bugzilla**: [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   DaveD working on and off
*   DaveM, DaveD taking a couple weeks in August
*   Javier ooo last two weeks in August

Action Items
------------

*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_26-Jun-2007#Action_Items "DSDP/TM/Committer Phone Meeting 26-Jun-2007") Action Items
*   **DaveD**: 2.0.1 important fixes, then Doc bugs (Tutorial)
*   **DaveM**: 2.0.1 fixes, Check whether mountPathMappers can workaround [193858](https://bugs.eclipse.org/bugs/show_bug.cgi?id=193858), comment on the bug about reason and possible workarounds
*   **Kushal**:
*   **Martin**: 2.0.1 fixes, unit tests; Release Notes, Migration Docs, EFS Fixes, Releng Fixes, Newsgroup
*   **Javier**: 2.0.1 fixes, unit tests
*   **Michael**: Terminal performance improvements

Next Meeting
------------

*   Monthly [DSDP/TM/Phone Meeting 4-Jul-2007](./DSDP/TM/Phone_Meeting_4-Jul-2007 "DSDP/TM/Phone Meeting 4-Jul-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=7&day=4&year=2007&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Committer Phone Meeting 10-Jul-2007](./DSDP/TM/Committer_Phone_Meeting_10-Jul-2007 "DSDP/TM/Committer Phone Meeting 10-Jul-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=7&day=10&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_3-Jul-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_3-Jul-2007))