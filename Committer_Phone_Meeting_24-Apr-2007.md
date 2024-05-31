

DSDP/TM/Committer Phone Meeting 24-Apr-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Apr 24, 2007](./index.php?title=Apr_24,_2007&action=edit&redlink=1 "Apr 24, 2007 (page does not exist)") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=4&day=24&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 News & Review Action Items](#News-.26-Review-Action-Items)
    *   [2.2 Time Plan and Deadlines toward M7](#Time-Plan-and-Deadlines-toward-M7)
    *   [2.3 Bugs and open work to be discussed](#Bugs-and-open-work-to-be-discussed)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave McKnight, Dave Dykstal, (Kushal Munir n/a), Kevin Doyle, Sanjayan Eladchumanasamy
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber, (Michael Scharf n/a), (Ted Williams n/a)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 17-Apr-2007](./DSDP/TM/Committer_Phone_Meeting_17-Apr-2007 "DSDP/TM/Committer Phone Meeting 17-Apr-2007")

### News & Review Action Items

| Martin | 100% | \[done\] Add Import/Export and UDA to I-builds; updated website; moved events to core; | 100% |
| --- | --- | --- | --- |
| DaveD | 70% | Persistence Improvements; Converting Translation test cases and filing bugs | 100% |
| DaveM | 30% | Bugfixes; \[done\] Fixed Import/Export | 40% |
| Kushal | (?) | BIDI Encodings | (?) |
| Javier | 50% | FTP Parser Extension Point - Problems persisting Property Set | 50% |
| Ted | 0% | - | 0% |
| Uwe | 5% | - | 5% |
| Michael | 10% |  | 10% |

### Time Plan and Deadlines toward M7

*   **Plan towards M7** \- goals and deadlines for I-builds
    *   I20070426 -- Major breaking API changes (Martin: getSystemType(), getInstance(); UI/Non-UI; Persistence)
    *   I20070503 -- Minor API changes - Final Feature Additions - Feature Freeze (Terminal integration; FTP Parser)
    *   I20070510 -- Stabilization, start [TM 2.0 M7 Testing](./TM_2.0_M7_Testing "TM 2.0 M7 Testing") on May 14th
    *   I20070516 -- TM 2.0M7 (17th is a public holiday in Austria!)

### Bugs and open work to be discussed

*   **Current Priorities**
    *   **Priority #1: Finish API Changes**
        *   **Javier**: FTP parallel download, allowing to register directory listing parser by extension point
            *   Please check in changes even if they are partial, so they are part of refactoring
        *   **DaveD**: Persistence (for UDA); UI/Non-UI
            *   Persistence Provider: try to make the configurable one independent of IResource - and probably wrap it in another one that does know the WorkspaceRoot and thus depends on IResource
        *   [bug 182221](https://bugs.eclipse.org/bugs/show_bug.cgi?id=182221): Should IRemoteFileSubSystem handle exceptions (by showing dialogs)? What about ISubSystem in general?
            *   Add API to register a notifier or errorhandler with the Subsystem? One option in the notifier could be to ignore exceptions
            *   Uwe: Eclipse 3.3 unified the concept of the StatusHandlers (in org.eclipse.ui) -- throwing CoreException with IStatus
            *   DaveM, DaveD are in favor of getting exceptions thrown, but are worried about the amount of code to change
            *   Martin: Changing the method signature to throw SystemMessageException should make the compiler show problematic places
            *   DaveD: We have utility methods (in the UI) for handling SystemMessageException
            *   **Future:** SystemMessageException could wrap IStatus at some point, bringing us closer to Eclipse
            *   DaveM: Would adapters (like getChildren()) just pass on exceptions as well? Where do we want to decide to handle the exception
            *   **Decision:** Pragmatically, start converting simple methods in IRemoteFileSubSystem; but not convert ones that look too difficult - bring it up again next week
    *   **Priority #2: Import/Export and User Actions**
        *   DaveM: Import/Export should be complete
        *   **AI DaveD, Kushal** persistence with User Actions; Dave working on API prerequisites now;
    *   **Priority #3: Bugs**
        *   Bugzilla: [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)
        *   Encoding Issues: Kushal single encoding control for all subsystems?
        *   BIDI bugs: Will we adopt [ICU4J](./ICU4J "ICU4J")? (Note according to [RCP FAQ](./RCP_FAQ "RCP FAQ"), ICU4J is required by org.eclipse.help and thus part of the core RCP already - though this may be changed ([bug 183761](https://bugs.eclipse.org/bugs/show_bug.cgi?id=183761)).
            *   ICU4J is part of the Platform already; we should start using it; can defer the changes to later since no API change, try to keep it in UI only
            *   **AI DaveD** to follow up on the concrete [bug 183631](https://bugs.eclipse.org/bugs/show_bug.cgi?id=183631) and fix it, to get experience with ICU4J
        *   Who wants to commit patches from Kevin -- update the [DSDP/TM/Code Ownership](./DSDP/TM/Code_Ownership "DSDP/TM/Code Ownership") page
        *   EFS: Copy(), Move(); Open Remote Project on Startup: Get rid of IResource dependencies where possible; minimal plugin activations; UI/Non-UI
        *   [182454](https://bugs.eclipse.org/bugs/show_bug.cgi?id=182454) \- what is the meaning of ISystemViewElementAdapter.getAbsoluteName()

  

*   **General Guidelines**
    *   Breaking API OK this week, but
        *   Avoid breaking API changes if possible afterwards (keep delegate methods, use deprecation)
    *   Kevin, Sanjayan currently doing Vista testing; some more internal RSE stuff
        *   DaveM talking to them beginning of May about coding
        *   Sanyaan won't be with us for too much longer, but somebody else may be around
        *   Martin sending out the keyword for marking "junior bugs"

Vacation, Away
--------------

Action Items
------------

*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_17-Apr-2007#Action_Items "DSDP/TM/Committer Phone Meeting 17-Apr-2007") Action Items
*   **DaveD**: Translation Testcases; Persistence Provider without IResource; Get started on ICU4J with [bug 183631](https://bugs.eclipse.org/bugs/show_bug.cgi?id=183631); User Actions
*   **DaveM**: Bugs
*   **Kushal**: BIDI bugs and Encodings
*   **Martin**: API cleanups; Testing Stats; Refresh improvements; Integrating Terminal with RSE
*   **Javier**: FTP parallel download, registering FTP Parser by extension point

Next Meeting
------------

*   May 1st is a public holiday in Austria --> Moving to May 2nd, before the Monthly TM Meeting
*   [DSDP/TM/Committer Phone Meeting 2-May-2007](./DSDP/TM/Committer_Phone_Meeting_2-May-2007 "DSDP/TM/Committer Phone Meeting 2-May-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=5&day=2&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 2-May-2007](./DSDP/TM/Phone_Meeting_2-May-2007 "DSDP/TM/Phone Meeting 2-May-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=5&day=2&year=2007&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_24-Apr-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_24-Apr-2007))