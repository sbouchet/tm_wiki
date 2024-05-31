

DSDP/TM/Committer Phone Meeting 17-Apr-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Apr 17, 2007](./index.php?title=Apr_17,_2007&action=edit&redlink=1 "Apr 17, 2007 (page does not exist)") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=4&day=17&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 TM 2.0M6 Test and Download Stats](#TM-2.0M6-Test-and-Download-Stats)
    *   [2.2 News & Review Action Items](#News-.26-Review-Action-Items)
    *   [2.3 Time Plan and Deadlines toward M7](#Time-Plan-and-Deadlines-toward-M7)
    *   [2.4 Bugs and open work to be discussed](#Bugs-and-open-work-to-be-discussed)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave McKnight, Dave Dykstal (Kushal Munir n/a)
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber (Michael Scharf n/a), (Ted Williams n/a)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 10-Apr-2007](./Committer_Phone_Meeting_10-Apr-2007 "DSDP/TM/Committer Phone Meeting 10-Apr-2007")

### TM 2.0M6 Test and Download Stats

*   See [DSDP/TM/Download Stats 17-Apr-2007](./Download_Stats_17-Apr-2007 "DSDP/TM/Download Stats 17-Apr-2007")
*   Even 1.0 is still being downloaded (+38 downloads since 7-Feb); 1.0.1 +1038 since 7-Feb
*   Bulk of 2.x downloads comes from Europa site!
    *   Europa Downloaders seem to tend to get everything
    *   Terminal slightly gaining significance with M5
*   rseserver-linux is most popular since 1.0.1 (rseserver-windows was it before)
*   When compiling statistics, M6a was not yet announced (only Europa got it from the update site)

  

### News & Review Action Items

| Martin | 100% | \[done\] fix EFS and respin 2.0M6a; \[done\] TM Webinar; \[done\] Update website, blog, promote Webinar and TM 2.0M6a; \[done\] Testing and Download Statistics; | 100% |
| --- | --- | --- | --- |
| DaveD | 100% | Persistence Improvements - really happy with interface now; thinks about properties to change the instanciation of the provider, e.g. in order to tailor it for storing in .metadata - Martin wants persistence to work without org.eclipse.core.resource if possible in order to fix EFS early startup | 70% |
| DaveM | 10% | ISubSystem.connect() for EFS; Bugfixes | 20% |
| (Kushal) | (50%) | (BIDI Encodings) | (?) |
| Javier | 50% | FTP Parser Extension Point - Problems persisting Property Set (DaveD thinks he knows the issue) | 50% |
| Ted | 0% | - | 0% |
| Uwe | 5% | - | 5% |
| Michael | 10% | [173730](https://bugs.eclipse.org/bugs/show_bug.cgi?id=173730) Terminal Separate Input Line | 10% |

### Time Plan and Deadlines toward M7

*   **Plan towards M7** \- goals and deadlines for I-builds
    *   I20070419 -- Fixes for localization enablement testing (BIDI, DBCS)
    *   I20070426 -- Major breaking API changes (Martin: getSystemType(), getInstance(); UI/Non-UI; Persistence)
    *   I20070503 -- Minor API changes - Final Feature Additions - Feature Freeze (Terminal integration; FTP Parser)
    *   I20070510 -- Stabilization, start [TM 2.0M7 Testing](./index.php?title=TM_2.0M7_Testing&action=edit&redlink=1 "TM 2.0M7 Testing (page does not exist)")
    *   I20070516 -- TM 2.0M7 (17th is a public holiday in Austria!)

  

*   Stability of this week's I-build for enablement testing is not too important --> Add importexport, useractions; DaveD to add persistence.
*   All committers are in favor of the persistence changes

### Bugs and open work to be discussed

*   **Current Priorities**
    *   **Priority #1: Open Major Bugs** \- Copying issues, NPEs
        *   Bugzilla: [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)
    *   **Priority #2: EFS**: Martin, done
        *   Open Remote Project on Startup: Get rid of IResource dependencies where possible; minimal plugin activations; UI/Non-UI
        *   Copy(), Move() operations;
    *   **Priority #3: Remaining API changes** for Persistence, Refresh etc.
        *   Mostly DaveD and Martin
        *   [182454](https://bugs.eclipse.org/bugs/show_bug.cgi?id=182454) \- what is the meaning of ISystemViewElementAdapter.getAbsoluteName()
            *   DaveM: Original intent was providing a unique ID similar to an URI - any object should be uniquely identifiable by a string.
            *   Used by Drag&Drop for instance, to allow windows native dnd support with a "filename"; also copy&paste, memento
            *   Should be enforced, null should not be allowed
            *   Should be unique within a single subsystem (multiple subsystems can have different elements with same absolute name)
        *   **Javier**: FTP parallel download, allowing to register directory listing parser by extension point
        *   Useractions / Importexport: - **AI Martin** add to nightly builds; **AI DaveD, Kushal** persistence with User Actions; Dave working on API prerequisites now; **AI DaveM** Import/Export

  

*   **General Guidelines**
    *   Avoid breaking API changes if possible (keep delegate methods, use deprecation)

Vacation, Away
--------------

*   Kushal out 1/2 day on Tuesday (during meeting time), another 1/2 day on Wed and full day on Thur
*   DaveD out on Friday 20th

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_10-Apr-2007#Action_Items "DSDP/TM/Committer Phone Meeting 10-Apr-2007") Action Items
*   **DaveD**: Remaining changes for Persistence (will be required for User Actions)
*   **DaveM**: Major bugs for dstore, copying
*   **Kushal**: BIDI bugs
*   **Martin**: Testing Stats; Add Import/Export and UDA to I-builds; Refresh improvements; Integrating Terminal with RSE
*   **Javier**: FTP parallel download, registering FTP Parser by extension point

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 24-Apr-2007](./Committer_Phone_Meeting_24-Apr-2007 "DSDP/TM/Committer Phone Meeting 24-Apr-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=4&day=24&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_17-Apr-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_17-Apr-2007))