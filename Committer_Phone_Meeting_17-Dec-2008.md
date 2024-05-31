

DSDP/TM/Committer Phone Meeting 17-Dec-2008
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Dec 17, 2008](./index.php?title=Dec_17,_2008&action=edit&redlink=1 "Dec 17, 2008 (page does not exist)") at [1700 UTC / 12pm Toronto](http://www.timeanddate.com/worldclock/fixedtime.html?month=12&day=17&year=2008&hour=17&min=00&sec=0&p1=0)   ![Html.gif](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/Html.gif)[HTML](http://www.google.com/calendar/embed?src=vn70im36r00qeusu8nme50cils@group.calendar.google.com&ctz=Canada/Toronto) \| ![Ical.gif](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/Ical.gif)[iCal](http://www.google.com/calendar/ical/vn70im36r00qeusu8nme50cils@group.calendar.google.com/public/basic.ics) |
| Dial-in: | Martin to call everybody by Skype   Interested Parties ping **martin.oberhuber** on Skype Chat for getting added to the call. |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kevin.j.doyle, xuan.chen886, eugenetarassov, michael\_scharf, uwe.stieber, radoslav.gerganov, wrsfburton, anna_dushistova.  

  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
    *   [2.1 Last Meetings](#Last-Meetings)
    *   [2.2 Update on RSE Status](#Update-on-RSE-Status)
        *   [2.2.1 TM 3.0.2](#TM-3.0.2)
        *   [2.2.2 TM 3.1 Big Rocks](#TM-3.1-Big-Rocks)
        *   [2.2.3 TM 3.1 Current status](#TM-3.1-Current-status)
    *   [2.3 Questions](#Questions)
*   [3 Vacations](#Vacations)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

This meeting is free for everyone to attend. It's a service of the TM developers and committers to community, fostering exchange of upcoming news, status and asking questions. Committers are expected to attend.

*   Committers:
    *   IBM - Dave Dykstal, Dave McKnight
    *   Wind River - Martin Oberhuber
    *   ProSyst - Radoslav Gerganov
    *   MontaVista - Anna Dushistova

Agenda
------

### Last Meetings

*   Last [DSDP/TM/Phone Meeting 3-Dec-2008](./DSDP/TM/Phone_Meeting_3-Dec-2008 "DSDP/TM/Phone Meeting 3-Dec-2008")
*   Last [DSDP/TM/Committer Phone Meeting 26-Nov-2008](./DSDP/TM/Committer_Phone_Meeting_26-Nov-2008 "DSDP/TM/Committer Phone Meeting 26-Nov-2008")
*   Skype Call Quality - excellent this time

### Update on RSE Status

#### TM 3.0.2

*   Post-mortem: DaveM - worked reasonably well, 1 consumer wants something fixed after the fact but have a workaround
*   Martin: Build infra for 3.0.3 in place. Commits + Release into Mapfile should suffice. Version numbers must be updated (don't forget feature versions and site.xml). Martin wants committers to release and upversion themselves but is there to help in case of issues.

#### TM 3.1 Big Rocks

*   **TM 3.1 Big Rocks / New Features** \- See also the [TM 3.1 plan](https://www.eclipse.org/projects/project-plan.php?projectid=dsdp.tm)
    *   See also the [TM and RSE FAQ](./TM_and_RSE_FAQ "TM and RSE FAQ")
*   **Martin:**
    *   [bug 185925](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185925) RSE Synchronisation (GSOC contribution) - planned for M4
    *   [bug 256581](https://bugs.eclipse.org/bugs/show_bug.cgi?id=256581) SSH performance improvement
    *   [bug 227750](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227750) IRSEInteractionProvider
    *   [bug 224465](https://bugs.eclipse.org/bugs/show_bug.cgi?id=224465) releng based on CBI
    *   [bug 257402](https://bugs.eclipse.org/bugs/show_bug.cgi?id=257402) get rid of CDT non-API use
    *   [bug 227207](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227207) threaded FTP download
    *   [bug 196337](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196337) Local terminal connector (Community contribution, cannot commit)
    *   Make TCF user-consumable
*   **Rado:**
    *   [bug 196176](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196176) [bug 181458](https://bugs.eclipse.org/bugs/show_bug.cgi?id=181458) [bug 153652](https://bugs.eclipse.org/bugs/show_bug.cgi?id=153652) SWT deferred drag&drop - committed, Martin may be able to help with getting the ball rolling
    *   [bug 242381](https://bugs.eclipse.org/bugs/show_bug.cgi?id=242381) [bug 239432](https://bugs.eclipse.org/bugs/show_bug.cgi?id=239432) [bug 231431](https://bugs.eclipse.org/bugs/show_bug.cgi?id=231431) WinCE processes subsystem, bring WinCE component to maturity (out of incubation)
*   **DaveM:**
    *   [bug 218227](https://bugs.eclipse.org/bugs/show_bug.cgi?id=218227) locating a resource in the remote systems view - related to [bug 160105](https://bugs.eclipse.org/bugs/show_bug.cgi?id=160105) but higher-priority.
    *   [bug 253481](https://bugs.eclipse.org/bugs/show_bug.cgi?id=253481) get rid of Platform non-API use (probably part of it)
    *   [bug 245260](https://bugs.eclipse.org/bugs/show_bug.cgi?id=245260) UI Preference to support different RSE tempfiles caches for different users / ports on the same host
    *   [bug 212742](https://bugs.eclipse.org/bugs/show_bug.cgi?id=212742) Utility to send commands without receiving output - works for dstore, not for others. probably want a callback.
    *   [bug 176461](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176461) API to expand Systemview nodes to arbitrary level (specifying a path) - command stuff already has some infrastructure for this
    *   [bug 218227](https://bugs.eclipse.org/bugs/show_bug.cgi?id=218227) contribute a "Show in RSE" action to project explorer
*   **DaveD:**
    *   [bug 222380](https://bugs.eclipse.org/bugs/show_bug.cgi?id=222380) [bug 239158](https://bugs.eclipse.org/bugs/show_bug.cgi?id=239158) merging subsystems on import - goes together with performance - committed
    *   [bug 244172](https://bugs.eclipse.org/bugs/show_bug.cgi?id=244172) [bug 233748](https://bugs.eclipse.org/bugs/show_bug.cgi?id=233748) Persistence Provider Performance - goes together with merging - committed
    *   [bug 243949](https://bugs.eclipse.org/bugs/show_bug.cgi?id=243949) persist only what was changed - start investigating, even if it can not be completed
    *   [bug 225320](https://bugs.eclipse.org/bugs/show_bug.cgi?id=225320) Equinox Secure Storage for RSE passwords - committed
    *   [bug 192970](https://bugs.eclipse.org/bugs/show_bug.cgi?id=192970) deterministic mnemonics everywhere - we likely cannot get rid of the support for auto-computing mnemonics (too many products)
        *   Martin: include an optional "logger" in the mnemonics generation system: warn about auto-generated mnemonics, log the mnemonic assigned in a format that allows applying the generated mnemonic to the original property file
    *   [bug 189238](https://bugs.eclipse.org/bugs/show_bug.cgi?id=189238) (regression) connection order is not persisted - make it a property of the View
    *   The following are not "big rocks" but will be added to the schedule for M5
    *   [bug 169422](https://bugs.eclipse.org/bugs/show_bug.cgi?id=169422) Eclipse conform table sort icons - small UI
    *   [bug 148977](https://bugs.eclipse.org/bugs/show_bug.cgi?id=148977) propose default filter names - small
    *   [bug 153249](https://bugs.eclipse.org/bugs/show_bug.cgi?id=153249) launch-shell contextmenu on filter nodes - small
    *   [bug 193477](https://bugs.eclipse.org/bugs/show_bug.cgi?id=193477) link-with instead of lock icon in details view toolbar - small UI
*   **Michael:**
    *   [bug 185348](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185348) Terminal API - committed
    *   [bug 209875](https://bugs.eclipse.org/bugs/show_bug.cgi?id=209875) allow capturing terminal output
    *   [bug 196462](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196462) optional fixed-width terminal
    *   Make TCF user-consumable
*   **Anna:**
    *   [bug 259363](https://bugs.eclipse.org/bugs/show_bug.cgi?id=259363) Move terminal subsystem out of incubation - committed
    *   [bug 181517](https://bugs.eclipse.org/bugs/show_bug.cgi?id=181517) [bug 181402](https://bugs.eclipse.org/bugs/show_bug.cgi?id=181402) Remotecdt commands before application launch / before opening a shell or terminal - committed
    *   [bug 164959](https://bugs.eclipse.org/bugs/show_bug.cgi?id=164959) API for IHostShell#waitFor(), IHostShell#writeToShellAndWait() - need to check
    *   [bug 246987](https://bugs.eclipse.org/bugs/show_bug.cgi?id=246987) [bug 246997](https://bugs.eclipse.org/bugs/show_bug.cgi?id=246997) Launching commands through TCF - committed
*   **Kevin:** \- cannot commit to anything, but will look following items in order
    *   [bug 168000](https://bugs.eclipse.org/bugs/show_bug.cgi?id=168000) remote search folder editing
    *   [bug 245039](https://bugs.eclipse.org/bugs/show_bug.cgi?id=245039) migrate actionSets to commands
    *   [bug 185925](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185925) bugfix RSE Sync GSOC contribution
    *   [bug 214403](https://bugs.eclipse.org/bugs/show_bug.cgi?id=214403) remote search features
*   **Xuan:** \- cannot commit to anything, but will look following items in order
    *   [bug 225211](https://bugs.eclipse.org/bugs/show_bug.cgi?id=225211) support for WAR archives
    *   [bug 254129](https://bugs.eclipse.org/bugs/show_bug.cgi?id=254129) [bug 172650](https://bugs.eclipse.org/bugs/show_bug.cgi?id=172650) Galileo basic activity definitions
    *   [bug 196317](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196317) [bug 199858](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199858) [bug 142184](https://bugs.eclipse.org/bugs/show_bug.cgi?id=142184) some RSE logging should go into a hidden log rather than the PDE Errorlog (investigate java.util.logging / commons logging) -- unsure
    *   Add Unittests (SWTBot) -- unsure
*   **3.1 Deferred Big Rocks / Features**
    *   [bug 158770](https://bugs.eclipse.org/bugs/show_bug.cgi?id=158770) [bug 160100](https://bugs.eclipse.org/bugs/show_bug.cgi?id=160100) do not use Projects to cache RSE tempfiles (due to case sensitivity and charset differences)
    *   [bug 174495](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174495) Multiple subsystems of the same kind under 1 host (e.g. ftp files + dstore files) - need investigation
    *   [bug 176490](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176490) improve connection property and wizard pages - too big
    *   [bug 203001](https://bugs.eclipse.org/bugs/show_bug.cgi?id=203001) support remote folder compares -- depends on gsoc synchronize

#### TM 3.1 Current status

*   TM 3.1m4 officially due on Monday Dec 29 -- Martin can release on Dec 23 -- need a candidate ready by Friday Dec 19 !
*   [3.1M3 Assigned Open bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&product=Target+Management&target_milestone=3.0&target_milestone=3.0.1&target_milestone=3.1+M2&target_milestone=3.1+M3&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) \- **AI Everyone** reassign target milestone as appropriate
*   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit) open bugs, [High Priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor) open bugs, [DSDP/TM/3.0 Known Issues and Workarounds](./DSDP/TM/3.0_Known_Issues_and_Workarounds "DSDP/TM/3.0 Known Issues and Workarounds")

### Questions

Vacations
---------

*   DaveD, Martin last week of dec and 1st week of Jan
*   DaveM vacation Dec 18,19 - only in half days afterwards (part time until Jan 6)
*   Rado working Mon 22,23 - vacation until Jan 6
*   Anna Jan1 - Jan10

Action Items
------------

*   Last meeting: [DSDP/TM/Phone Meeting 3-Dec-2008](./DSDP/TM/Phone_Meeting_3-Dec-2008 "DSDP/TM/Phone Meeting 3-Dec-2008")
*   Last [DSDP/TM/Committer Phone Meeting 26-Nov-2008](./DSDP/TM/Committer_Phone_Meeting_26-Nov-2008 "DSDP/TM/Committer Phone Meeting 26-Nov-2008")
*   **Everyone** find/triage "big rock" bugs for 3.1 and increase priority / set target milestone (may decrease priority on others).
*   **Martin** send E-Mail to Xuan and Kevin asking for another meeting for big rocks

Next Meeting
------------

*   Next [DSDP/TM/Phone Meeting 7-Jan-2009](./DSDP/TM/Phone_Meeting_7-Jan-2009 "DSDP/TM/Phone Meeting 7-Jan-2009") (2 weeks after)
*   Next [DSDP/TM/Meetings/21-Jan-2009 Committer](./DSDP/TM/Meetings/21-Jan-2009_Committer "DSDP/TM/Meetings/21-Jan-2009 Committer") (4 weeks after)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_17-Dec-2008](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_17-Dec-2008))