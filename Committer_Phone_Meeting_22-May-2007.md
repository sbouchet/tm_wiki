

DSDP/TM/Committer Phone Meeting 22-May-2007
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [May 22, 2007](./index.php?title=May_22,_2007&action=edit&redlink=1 "May 22, 2007 (page does not exist)") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=5&day=22&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 News & Review Action Items](#News-.26-Review-Action-Items)
    *   [2.2 Plan for the TM Future](#Plan-for-the-TM-Future)
    *   [2.3 Ramp Down Plan](#Ramp-Down-Plan)
    *   [2.4 Bugs and open work to be discussed](#Bugs-and-open-work-to-be-discussed)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave McKnight, Dave Dykstal, Kushal Munir, Kevin Doyle
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 15-May-2007](./Committer_Phone_Meeting_15-May-2007 "DSDP/TM/Committer Phone Meeting 15-May-2007")

### News & Review Action Items

| Martin | 100% | RSE bugs (see bugzilla), releaseing M7 | 100% |
| --- | --- | --- | --- |
| DaveD | 80% | Persistence in metadata, Translations, Mnemonics | 80% |
| DaveM | 50% | Bugfixes | 50% |
| Kushal | 40% | BIDI Encodings | 40% |
| Javier | 30% | FTP Parser Extension Point | 30% |
| Ted | 0% | - | 0% |
| Uwe | 5% | - | 5% |
| Michael | 10% | Terminal API cleanup, plus small fixes; performance improvements | 10% |

### Plan for the TM Future

Beginning of next week, the Europa Release Review slides are due. I'd like to have a rough idea where we are heading. It's also important to know when deciding what bugs can be deferred to later. Here is an outline as a discussion start: See also [TM Future Planning](./TM_Future_Planning "TM Future Planning")

*   TM 2.0.1 with Europa (in autumn) or slightly earlier
    *   Wind River might need 2.0.1 slightly before Europa SR1;
    *   DaveD taking off 2 weeks in August (7th-20th) and large part (end of) September, heading to Prague
    *   Work on unittests, isv docs over the summer in HEAD
    *   Fork off from mainline in autumn; if we have any large things for 3.0 and want to start before 2.0.1 might do that in a branch; but having the branch this or that way is not a big deal
    *   User actions: consider replacing it entirely by command framework
*   Will the next TM release (Ganymade coordinated release) be TM 2.1 or TM 3.0?
    *   We'd probably need 3.0 for further UI/Non-UI, API Polish, finalizing terminal API
    *   Doing 2.1 might be possible but harder than going for 3.0 right away; Finishing the UI/Non-UI refactoring is essential to complete for the next release
        *   TM 3.0 probably not a problem at IBM
        *   Javier comfortable with what RSE looks like at the moment
        *   Better going for 3.0 since not yet happy with API
    *   We could shoot for a 3.0 but strive to keep API changes small and potentially have a compatibility plugin
    *   **Integrate** in next release - strong should:
        *   WebDAV, Team Sync (minimal data transfer), Wicked Shell, JArchive (through RSE extension point)
    *   **Add** in next release:
        *   User actions (probably replace by Command framework), Launch Actions, VLM Lab Manager, IPxAct data, Connection Groups
        *   DaveM: tings existing with IBM already: Remote Java Debug, Remote Jar Export (need legal review); export to multiple targets;
        *   Contribute IBM "External Tools" implementation (very interesting!) - potentially consolidate into single User Actions framework
    *   Potentially move to Platform + 0 level --> move CDT Launcher to CDT Project

### Ramp Down Plan

*   [TM 2.0 Ramp down Plan for Europa](./TM_2.0_Ramp_down_Plan_for_Europa "TM 2.0 Ramp down Plan for Europa"), based on [Europa Simultaneous Release#Milestones and Release Candidates](./Europa_Simultaneous_Release#Milestones_and_Release_Candidates "Europa Simultaneous Release")
    *   RC1 -- Fri May 25 (5 work days) -- May 30: Release Review Slide Decks due
    *   RC2 -- Tue Jun 5 (6 work days)
    *   RC3 -- Thu Jun 14 (7 work days; Martin vacation 12-Jun til 21-Jun!)
    *   RC4 -- Thu Jun 21 (5 work days)
    *   EUROPA -- Jun 29
*   1-committer-review recommended for RC1, required afterwards.
*   If there are any risky fixes, make them as early as possible, less risky fixes later
*   **Reviewing assigned bugs** regarding priority and potential to defer past 2.0: Individual committers, DaveD+Martin, or Martin alone?
    *   Have a review phase on Friday; Kushal reviewing his; fields to change are "Priority" and "Target Milestone"
    *   Have each committer do a first pass on his own assigned bugs; DaveD and Martin go through the list again on Monday.
*   Avoid breaking API changes from now on (though we can still break API if absolutely necessary)

### Bugs and open work to be discussed

*   **Current Priorities:** Fix bugs by Priority
    *   **Javier**: Some FTP related bugs; Happy to help out with other stuff; User docs and ISV docs for Discovery? Javier fine with doing it in RC2/RC3; Martin help out with releng aspects.
    *   **DaveD**: Translation / Menmonics stuff, [187647](https://bugs.eclipse.org/bugs/show_bug.cgi?id=187647) Persistence in Metadata - dont see problems but needs fairly thorough testing
        *   [153632](https://bugs.eclipse.org/bugs/show_bug.cgi?id=153632) incorrect filterpool for dstore - are we really converging to a single filter pool?
    *   **DaveM**: Refresh related bugs; single filter pool? - DaveM does want to get to it this week: coordinate with DaveD since some issues might come up in the Persistence area
    *   **Martin**: Need to bring Releng scripts up to latest for Orbit; Review and release Telnet fixes; [172650](https://bugs.eclipse.org/bugs/show_bug.cgi?id=172650) Capabilities; [176461](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176461) expand-to-level; [186315](https://bugs.eclipse.org/bugs/show_bug.cgi?id=186315) EFS problematic URIs;
        *   [170910](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170910) Integrate Terminalview -- **OK to defer** past 2.0? Add in 2.0.1?
            *   Kushal: make it available as experimental download?
            *   DaveM: make it in two pathes (separate subsystem first, integrate into commandview later)?
            *   IBM has a very loose terminal integration: select host, "Open Terminal" opens a separate terminal view; that would give us some kind of integration. But for TM Terminal, there are no translations, no clearance etc.
            *   **Decision**: Better invest time into 2.0 bugfixes, and adding the Terminal in an early 3.0 milestone.
        *   Would like to **Rename org.eclipse.rse.eclipse.filesystem to org.eclipse.rse.efs** \-\- OK?
            *   DaveD: Files in there need to be retargeted - should not be a big problem
        *   API: Would like to add some "throws" clauses to ISystemRegistry and others to ensure that nobody expects it to show messages (necessary when it is to go into non-UI in the future) -- OK?
            *   Kushal: Better make API change now rather than later
        *   EFS: Copy(), Move(); minimal plugin activations; UI/Non-UI
    *   **Kushal**: Single "Encoding" control on the Host (for all subsystems); will be removing encoding control on the Shells property page
*   **Bugzilla**: [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   DaveD travelling this week, but that shouldn't affect anything
*   Monday May 28 - Pentecost Monday in Austria (Martin OOO), Memorial Day in US (public holiday, but DaveD probably working)

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_15-May-2007#Action_Items "DSDP/TM/Committer Phone Meeting 15-May-2007") Action Items
*   **DaveD**: Translation Testcases; Persistence Provider without IResource; Get started on ICU4J with [bug 183631](https://bugs.eclipse.org/bugs/show_bug.cgi?id=183631)
*   **DaveM**: Refresh Bugs
*   **Kushal**: BIDI bugs and Encodings
*   **Martin**: Testing Stats; Refresh improvements; Integrating Terminal with RSE
*   **Javier**:
*   **Michael**:

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 29-May-2007](./Committer_Phone_Meeting_29-May-2007 "DSDP/TM/Committer Phone Meeting 29-May-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=5&day=29&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 6-Jun-2007](./Phone_Meeting_6-Jun-2007 "DSDP/TM/Phone Meeting 6-Jun-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=6&day=6&year=2007&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_22-May-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_22-May-2007))