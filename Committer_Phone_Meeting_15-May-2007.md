

DSDP/TM/Committer Phone Meeting 15-May-2007
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [May 15, 2007](./index.php?title=May_15,_2007&action=edit&redlink=1 "May 15, 2007 (page does not exist)") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=5&day=15&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Invited Attendees](#Invited-Attendees)
*   [2 Notes](#Notes)
    *   [2.1 News & Review Action Items](#News-.26-Review-Action-Items)
    *   [2.2 Pending Approvals for API Changes](#Pending-Approvals-for-API-Changes)
    *   [2.3 M7 Testing](#M7-Testing)
    *   [2.4 Ramp Down Plan](#Ramp-Down-Plan)
    *   [2.5 Bugs and open work to be discussed](#Bugs-and-open-work-to-be-discussed)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Invited Attendees
-----------------

*   IBM - Dave McKnight, Dave Dykstal, Kushal Munir, Kevin Doyle, Xuan Chen
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 8-May-2007](./Committer_Phone_Meeting_8-May-2007 "DSDP/TM/Committer Phone Meeting 8-May-2007")

### News & Review Action Items

| Martin | 100% | RSE bugs and API changes as documented on bugzilla | 100% |
| --- | --- | --- | --- |
| DaveD | 80% |  | 80% |
| DaveM | 25% | Bugfixes | 50% |
| Kushal | 40% | BIDI Encodings | 40% |
| Javier | 30% | FTP Parser Extension Point | 30% |
| Ted | 0% | - | 0% |
| Uwe | 5% | - | 5% |
| Michael | 10% |  | 10% |

### Pending Approvals for API Changes

*   [186640](https://bugs.eclipse.org/bugs/show_bug.cgi?id=186640) IRSESystemType.testProperty(), isLocal() and isWindows()
*   [186779](https://bugs.eclipse.org/bugs/show_bug.cgi?id=186779) IRSESystemType.getAdapter()
*   [185098](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185098) Constants in IRSESystemType for the ID's for SSH, FTP, Discovery
*   [186773](https://bugs.eclipse.org/bugs/show_bug.cgi?id=186773) Splitting ISystemRegistryUI from ISystemRegistry
*   [186748](https://bugs.eclipse.org/bugs/show_bug.cgi?id=186748) Move ISubSystemConfigurationAdapter to org.eclipse.rse.ui.subsystems
*   [186525](https://bugs.eclipse.org/bugs/show_bug.cgi?id=186525) Move keystoreProvider to Core

### M7 Testing

*   [TM 2.0 M7 Testing](./TM_2.0_M7_Testing "TM 2.0 M7 Testing")
    *   Thanks Kevin and Xuan -- 'ok' flag; Martin's assignments
    *   I20070516 -- TM 2.0M7 (17th is a public holiday in Austria!)

### Ramp Down Plan

*   [TM 2.0 Ramp down Plan for Europa](./TM_2.0_Ramp_down_Plan_for_Europa "TM 2.0 Ramp down Plan for Europa"), based on [Europa Simultaneous Release#Milestones and Release Candidates](./Europa_Simultaneous_Release#Milestones_and_Release_Candidates "Europa Simultaneous Release")
    *   RC1 -- Fri May 25 (5 work days) -- May 30: Release Review Slide Decks due
    *   RC2 -- Tue Jun 5 (6 work days)
    *   RC3 -- Thu Jun 14 (7 work days; Martin vacation 12-Jun til 21-Jun!)
    *   RC4 -- Thu Jun 21 (5 work days)
    *   EUROPA -- Jun 29
*   More risky fixes OK for M7, less risky afterwards; don't want to re-test everything with the RC's but only verify bug fixes
*   Lots of bugs still assigned to M7 / RC1 -- please review and fix target milestone
*   Do we really want to force 1-committer-approval for RC1?
    *   Make approval recommended but not required for RC1
    *   DaveD to do RC3 and RC4 instead of Martin -- do RC1 and RC2 together; DaveD supervising translation tests during RC1 -- do RC1 early morning on friday

### Bugs and open work to be discussed

*   **Current Priorities**
    *   **Priority #1: Converge to a Stable Build for Testing**
        *   **Javier**: [176216](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176216) Try to improve FTPListingParser as per Martin's suggestions as much as possible -- persistence of the parser setting (see DaveD below: 142806, 153632)
        *   **DaveD**: [177329](https://bugs.eclipse.org/bugs/show_bug.cgi?id=177329) Persistence locks the workspace / thread handling: provider outside workspace / independent of IResource - APIs done, provider in metadata TBD **AI DaveD fix today**
            *   [168870](https://bugs.eclipse.org/bugs/show_bug.cgi?id=168870) org.eclipse.rse.core in the UI plugin: SystemBasePlugin (reduce usage to 0 and get rid of it?), ISystemRemoteElementAdapter (only Shell!), ISystemRemoteObjectMatcher; **AI Martin take from DaveD**
            *   [142806](https://bugs.eclipse.org/bugs/show_bug.cgi?id=142806) attributes not written to DOM; - probably fixed already, FTP properties is an example of this; [153632](https://bugs.eclipse.org/bugs/show_bug.cgi?id=153632) incorrect filterpool for dstore - **AI DaveD checking today**
            *   [176211](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176211) org.eclipse.rse.internal.model in the UI plugin: SystemHostPool (create an interface IRSESystemTypeAdapter) - **tricky, not for 2.0**
            *   [183771](https://bugs.eclipse.org/bugs/show_bug.cgi?id=183771) StandardCredentialProvider without UI if password is stored; - almost there, not a priority since there are other UI dependencies we won't get around for 2.0 -- leave as is for now
        *   **DaveM**: Delete Local Connection: going forward with the change
            *   Switching service of an existing connection: filter pool dstore.files is different than ssh.files -- when switching the service type, the filters are lost. When switching on "create in this connection only", would it be kept? Should this option be default? - Solution for the future to make it explicit: "Do you want to copy the filters to the new service?"
                *   **Decision:** We should be able to share file filters among all subsystems that can handle files. **AI DaveM to take a look at it** but it is technically difficult, will break workspace compatibility and he's not sure if he can get it done. If breaking workspace compatibility, now is the time to do so.
            *   [173042](https://bugs.eclipse.org/bugs/show_bug.cgi?id=173042) Refresh in the SystemView - being handled by Martin now
            *   [167620](https://bugs.eclipse.org/bugs/show_bug.cgi?id=167620) delete many items has remote queries on dispatch thread - delete being done on SystemView itself, so adapter is called on dispatch thread -- envision solving it by doing delete in a Job and then doing a refresh on the view. Martin: delete should also work in a non-UI scenario without any SystemView. Risky but better do it now. **AI DaveM to look at it**
        *   **Martin**: [175680](https://bugs.eclipse.org/bugs/show_bug.cgi?id=175680) cleanup ISystemRegistry - probably bring more into non-UI; [173042](https://bugs.eclipse.org/bugs/show_bug.cgi?id=173042) Refresh; [172650](https://bugs.eclipse.org/bugs/show_bug.cgi?id=172650) Capabilities; [176461](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176461) expand-to-level; [170910](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170910) Integrate Terminalview;
        *   **Kushal**: Single "Encoding" control on the Host (for all subsystems) - **AI Wanted to check in last week?**
    *   **Priority #3: Bugs**
        *   Bugzilla: [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)
        *   EFS: Copy(), Move(); Open Remote Project on Startup: Get rid of IResource dependencies where possible; minimal plugin activations; UI/Non-UI

*   **General Guidelines**
    *   Avoid breaking API changes after end of this week

Vacation, Away
--------------

*   Monday May 21st is Victoria day in Canada (public holiday)
*   DaveD travelling next week, but that shouldn't affect anything

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_8-May-2007#Action_Items "DSDP/TM/Committer Phone Meeting 8-May-2007") Action Items
*   **DaveD**: Translation Testcases; Persistence Provider without IResource; Get started on ICU4J with [bug 183631](https://bugs.eclipse.org/bugs/show_bug.cgi?id=183631)
*   **DaveM**: Bugs
*   **Kushal**: BIDI bugs and Encodings
*   **Martin**: Inform the community about dropped user actions; API cleanups; Testing Stats; Refresh improvements; Integrating Terminal with RSE
*   **Javier**: Registering FTP Parser by extension point
*   **Michael**: Marking Terminal as provisional API

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 22-May-2007](./Committer_Phone_Meeting_22-May-2007 "DSDP/TM/Committer Phone Meeting 22-May-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=5&day=22&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 6-Jun-2007](./Phone_Meeting_6-Jun-2007 "DSDP/TM/Phone Meeting 6-Jun-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=6&day=6&year=2007&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_15-May-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_15-May-2007))