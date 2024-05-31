

DSDP/TM/Committer Phone Meeting 29-May-2007
===========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [May 29, 2007](/index.php?title=May_29,_2007&action=edit&redlink=1 "May 29, 2007 (page does not exist)") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=5&day=29&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
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
    *   [2.3 Ramp Down Plan](#Ramp-Down-Plan)
    *   [2.4 Bugs and open work to be discussed](#Bugs-and-open-work-to-be-discussed)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Invited Attendees
-----------------

*   IBM - Dave McKnight, Dave Dykstal, Kushal Munir, Kevin Doyle, Xuan Chen
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber (Michael Scharf n/a, Uwe Stieber n/a)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 22-May-2007](/DSDP/TM/Committer_Phone_Meeting_22-May-2007 "DSDP/TM/Committer Phone Meeting 22-May-2007")

### News & Review Action Items

| Martin | 100% | Final API fixes, bugs, releasing RC1; [TM Future Planning](/TM_Future_Planning "TM Future Planning"), Release Review Slides | 80% |
| --- | --- | --- | --- |
| DaveD | 80% | Persistence in metadata, Translations | 90% |
| DaveM | 50% | Bugfixes | 80% |
| Kushal | 40% | BIDI Encodings | 40% |
| Javier | 30% | Bugfixes | 30% |
| Ted | 0% | - | 0% |
| Uwe | 5% | - | 5% |
| Michael | 10% | Terminal API cleanup, plus small fixes; performance improvements | 10% |

### Plan for the TM Future

*   Please review and edit [TM Future Planning](/TM_Future_Planning "TM Future Planning") together with your Requirements / Product Management folk

### Ramp Down Plan

*   [TM 2.0 Ramp down Plan for Europa](/TM_2.0_Ramp_down_Plan_for_Europa "TM 2.0 Ramp down Plan for Europa"), based on [Europa Simultaneous Release#Milestones and Release Candidates](/Europa_Simultaneous_Release#Milestones_and_Release_Candidates "Europa Simultaneous Release")
    *   Tomorrow Wed May 30: Release Review Slide Decks due
    *   RC2 -- Tue Jun 5 (6 work days)
    *   RC3 -- Thu Jun 14 (7 work days; Martin vacation 12-Jun til 21-Jun!)
    *   RC4 -- Thu Jun 21 (5 work days)
    *   EUROPA -- Jun 29
*   Testing: **Please use RSE yourselves in daily work**
*   **1-committer-review required from now on**. Doc-only / Comment-only / Testcases fixes allowed without review.
*   Focus on hi-priority bugs (bugs been triaged?)
    *   Strive for all code changes done for RC2, with doc-only/testcases/escalations only for RC3 and later
    *   Compiler Warnings (esp. Javadoc warnings), Copyright data updates
    *   Copyright comments: please add contribution entries at the END of the list
    *   Our IP Log needs to be frozen by the time of the Release review; **AI Martin** check whether we can accept patches from Xuan and Kevin after June 6
*   Avoid breaking API changes (though we can still break API if absolutely necessary)

### Bugs and open work to be discussed

*   **Current Priorities:** Fix bugs by Priority
    *   **Javier**: User docs and ISV docs for Discovery? **AI Martin** help out with releng aspects.
    *   **DaveD**: [187647](https://bugs.eclipse.org/bugs/show_bug.cgi?id=187647) Persistence in Metadata
        *   [153632](https://bugs.eclipse.org/bugs/show_bug.cgi?id=153632) incorrect filterpool for dstore - not converging to a single filter pool - how serious is it? - **AI DaveD reevaluate**
            *   Tobias will test, there might be some SchedulingRule
            *   DaveM: Migration of an existing workspace into the metadata area?
        *   Martin: Dont persist stuff that has not been activated?
            *   DaveD dont know of a good way of doing that - when a subsystem is created, everything is scheduled for persisting
        *   Empty List bug: DaveD to put Preference in, Tobias to respect it
        *   N-builds / I-builds: DaveD to try out N-builds, then learn I-builds and how to contribute to Europa
    *   **DaveM**: Single filter pool: Looks like a lot of work - not for 2.0, needs an architectural change: **AI DaveM** file an enhancement request for the future
    *   Refresh related bugs: need to limit what you can "Go Into" or "Open New Window" on. Historically, the InputProvider only supported certain objects (Only connections, subsystems etc. were allowed previously) - disable the action for objects other than those?
        *   IRemoteObjectAdapter: remote vs. local refresh in the SystemView - view historically had this destinction: "remote" things can exist multiple times, "local" things only once; objects above the filter are known RSE artifacts; objects above the filter potentially do not require a query; special handling (e.g. get the parent) only on "remote" artifacts
            *   Alternatives for making the distinction between "remote" and "non-remote": have the non-remote model object implement a certain interface (e.g. IRSEModelObject); add an isRemote() method in ISystemViewElementAdapter already; DaveM likes the isRemote() on the adapter approach best
        *   dnd: Download-on-Copy - have a Preference? How to do remote-only manipulations without downloading? - it works nicely with few small files but fails for lots of large files. Separate jobs per directory are necessary because files need to be created upfront for FileTransfer to work. DaveD: Governor Job that submits the others? **AI Martin** test the large file situation
        *   [176601](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176601) fireEvent switch to display thread automatically
        *   Do we need to markStale the parent of a child we are marking stale? - **AI DaveM** try getting rid of markStale() on the parent; get rid of remote access during markStale(). Kushal: Do we just mark the contents of the parent stale rather than the properties?
        *   Copy as binary although text mode specified: FTP and dstore should honor the preference of line endings and store files accordingly. We transfer binary now but convert before the transfer. Writers should take care of the line ends automatically.
    *   **Martin**: Need to bring Releng scripts up to latest for Orbit; Review and release Telnet fixes; [172650](https://bugs.eclipse.org/bugs/show_bug.cgi?id=172650) Capabilities; [176461](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176461) expand-to-level; [186315](https://bugs.eclipse.org/bugs/show_bug.cgi?id=186315) EFS problematic URIs;
        *   [170910](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170910) Integrate Terminalview -- **OK to defer?**
        *   EFS: Copy(), Move(); minimal plugin activations; UI/Non-UI
    *   **Kushal**: [179937](https://bugs.eclipse.org/bugs/show_bug.cgi?id=179937) Single "Encoding" control on the Host (for all subsystems)
        *   Deprecation: with 2.0 we have the chance of getting rid of stuff we don't like. So we should remove unwanted API if we can. If we cannot remove it yet, we can choose to rather deprecate it - then we need to tell users an alternative way with the @deprecated.
        *   [174789](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174789) Property pages added to Wizard automatically: **AI Kushal** investigate
*   **Bugzilla**: [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   Thursday Jun 7 - public holiday in Austria (Martin ooo)
*   Martin Vacation Wed Jun 13 - Fri Jun 22

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_22-May-2007#Action_Items "DSDP/TM/Committer Phone Meeting 22-May-2007") Action Items
*   **DaveD**: Translation Testcases; Persistence Provider without IResource
*   **DaveM**: Refresh Bugs
*   **Kushal**: BIDI bugs and Encodings
*   **Martin**: Testing Stats; Refresh improvements; Integrating Terminal with RSE
*   **Javier**:
*   **Michael**:

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 5-Jun-2007](/DSDP/TM/Committer_Phone_Meeting_5-Jun-2007 "DSDP/TM/Committer Phone Meeting 5-Jun-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=6&day=5&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 6-Jun-2007](/DSDP/TM/Phone_Meeting_6-Jun-2007 "DSDP/TM/Phone Meeting 6-Jun-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=6&day=6&year=2007&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_29-May-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_29-May-2007))