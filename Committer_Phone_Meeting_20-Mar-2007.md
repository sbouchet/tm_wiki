

DSDP/TM/Committer Phone Meeting 20-Mar-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Mar 20, 2007](./index.php?title=Mar_20,_2007&action=edit&redlink=1 "Mar 20, 2007 (page does not exist)") at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=3&day=20&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 News & Review Action Items](#News-.26-Review-Action-Items)
    *   [2.2 Upcoming Work](#Upcoming-Work)
    *   [2.3 Other Stuff to Do](#Other-Stuff-to-Do)
    *   [2.4 Communications](#Communications)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave McKnight, Dave Dykstal (Kushal Munir n/a)
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber, (Michael Scharf n/a, Ted Williams n/a)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help: **being responsive**
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site

### News & Review Action Items

| Martin | 100% | Commons.net Orbit contribution; Wiki how to contribute; [178201](https://bugs.eclipse.org/bugs/show_bug.cgi?id=178201) Telnet contribution | 50% |
| --- | --- | --- | --- |
| DaveD | 100% | Still on UI/Non-UI (got hung up on some validators) | 100% |
| DaveM | 10% | No news - hopefully back to 50% next week | 10% |
| Kushal | 50% | - |  |
| Javier | 10% | No news - working on SD submission | 50% |
| Ted | 0% | - | 0% |
| Uwe | 5% | - | 5% |
| Michael | 20% | Terminal Performance | 20% |

### Upcoming Work

*   See also [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_13-Mar-2007#Upcoming_Work "DSDP/TM/Committer Phone Meeting 13-Mar-2007") for notes
*   **Recent pending API Change Discussions** \- **AI Everyone** to review and comment on bugzilla if any issues
    *   [173468](https://bugs.eclipse.org/bugs/show_bug.cgi?id=173468) Javier standard service name - **ok**
    *   [178020](https://bugs.eclipse.org/bugs/show_bug.cgi?id=178020) Uwe remove obsolete ISystemViewActionFilter
    *   [178023](https://bugs.eclipse.org/bugs/show_bug.cgi?id=178023) Uwe allow extenders return their own extended IHost implementation. WRT persistence, the Dynamic SystemTypeProvider is responsible for serializing / deserializing its extended Host implementation.
    *   [178021](https://bugs.eclipse.org/bugs/show_bug.cgi?id=178021) Uwe forward testAttribute() to RSESystemType; also performance improvement by caching queries in RSECoreRegistry by id or by name
    *   [177930](https://bugs.eclipse.org/bugs/show_bug.cgi?id=177930) Uwe remove getXXXAdapter() from SystemViewAdapterFactory
    *   DaveD: removed some property constants (P\_ORIGIN, P\_COMMAND) will need to re-add for user actions
        *   Martin: These went out of the AbstractSystemViewAdapter namespace when it no longer implements ISystemPropertyConstants. I files [bug 178566](https://bugs.eclipse.org/bugs/show_bug.cgi?id=178566) as a reminder for migration guide. The fix is that these constants now need to be qualified.
*   **Top priority** is getting API things done for M6. Plan items are currently more important than bug priorities. We have 2 weeks to go (plus 1 week for testing)
    *   [170909](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170909) (DaveD, Kushal) User Actions: Still waiting for IP review. Found many icons related to UA and import/export in rse.ui which will need to be moved. **AI Martin Inquire on CQ**
    *   [150498](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150498) (Javier) More service-oriented; Multiple subsystems of the same kind - Javier raised [bug 174495](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174495) for this - what about "No subsystems"? [176490](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176490) new wizard request, see also "Improve SystemType" below;
        *   Martin idea: allow multiple file subsystems.
            *   DaveM: wants to switch service for a given subsystem after created. Wants to share "File" filters between services. Wants to share user actions between multiple shells; Uwe: will need to change context menu actions;
            *   DaveM: What file subsystem to link with the editor?
            *   DaveM: Refresh events - when a new file is created under a folder, all file subsystems should be refreshed -- multiple queries to subsystems; Martin -- we can do it today (and discovered issues when doing so), the only difference is that they are under different Host nodes
            *   DaveM: Save in editor - which file subsystem do we use to upload? - first available or the one we opened with - path in the cache is the same! Right now, we keep track of the connection we used when opening the file (Martin: in the future, keep track of the subsystem)
            *   Capture this discussion on [bug 174495](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174495)
        *   Martin idea: **dynamic wizard** to allow FIRST select the subsystems; then press NEXT: wizard will present property pages for all the selected subsystems;
            *   Captured this idea in [bug 176490](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176490)
    *   [170918](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170918) (Martin) Improve SystemType and Wizard: Replace Name by IRSESystemType wherever possible, but keep it for now in Persistence
        *   DaveD finished AI: the Name is actually persisted -- would be good to have some migration in place for changing name -> id; right thing is to start persisting both id and the name, and then gradually stop reading the name. Starting to persist the id is not an API change. There may be API changes down the road when we stop reading names.
        *   if() queries -> these are implementation details later, even replacing Name by Properties since the systemType does have Properties already
*   **Other API things** not directly marked as plan item
    *   expandTo() - **AI Martin** probably connected to async callbacks, non-UI multi path query and event changes for Refresh
    *   [170922](https://bugs.eclipse.org/bugs/showdependencytree.cgi?id=170922) (DaveM, Martin) Making as much as possible "internal"
        *   **AI DaveM, DaveD try to identify more things to make internal**

### Other Stuff to Do

*   [174945](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174945) General code cleanup - get rid of unused icons, comments, properties
*   **Update Copyright Year to 2007 if you happen to think about it**
*   Please continue on Compiler Warnings

### Communications

*   Vacations, Holidays etc.
    *   Martin on vacation Friday 23-Mar till Wednesday 28-Mar
*   Free discussion -- feelings, comments, critics
    *   Javier: IBM extension for "Attach" launch from the Processes subsystem
        *   DaveM: There is generic Launch support for remote source locator; Also, IBM has a Remote Java Launch Config for RSE; Beyond that, IBM products have support for dealing with "a remote debugger". Given a selection from Processes, it was able to prefill.
            *   Martin: The hard part was finding an existing "attach" kind launch with same properties and re-use it
            *   Uwe: Eclipse 3.3M6 coming up with "contextual Launches" solving much of these issues - in case there multiple similar matching Launches, it pops up a dialog to prompt the user for which one to use
            *   DaveM: Looks like contributing IBM stuff is more work than writing the code from scratch (3 hrs of work for DaveM) - try to do it in a debugger independent, extendable way
            *   Uwe: The DD project thinks about debugger services framework... dont interfere too much with them
        *   Javier doesnt need it right now but may need it in the future - people asked like "what can I do with the processes subsystem"
        *   DaveM: There are 2 more RSE plugins which are not yet in open source but would make sense: Common Source Locator and Remote Java Debug
        *   Decision: **AI DaveM** talk with DaveD, get IBM contribution of these 2 plugins started. No contribution for remote C/C++ debug attach. Should be done from scratch, using 3.3M6 context launches and basing on CDT attach launch as well as current remotecdt launch, by whoever think he can use it for his product.

Action Items
------------

*   [Last Meeting](./DSDP/TM/Committer_Phone_Meeting_13-Mar-2007#Action_Items "DSDP/TM/Committer Phone Meeting 13-Mar-2007") Action Items
*   **Everyone** \- Review recent pending API change bugzilla's and comment on them if there are any issues
*   **DaveD** \- Search more packages and classes to make "internal", report on mailing list; Refactoring UI/Non-UI
*   **DaveM** \- Search more packages and classes to make "internal", report on mailing list; Talk with DaveD regarding open-sourcing Remote Source Lookup and Java Launch;
*   **Kushal** \- EFS, File bugs for Streams on Subsystem Layer; Encoding Tests; Allocate Mac for nightly tests; Talk to DaveD re Comm Server; Bugs & Unit Tests
*   **Martin** \- Inquire User Actions CQ; Put multi-subsystem-discussion on bugzilla; Website updates (M5, Eclipsecon, Webinar); Work on Refresh, ExpandTo, Callbacks; Adopt new Platform SSH organization; Replace systemType name by IRSESystemType in IHost; Integrate Terminal in RSE; Test JDT Cleanup Wizard on one plugin; Bugzilla against CDT; Update feature.properties for Europa; Migrate build to Ted's scripts; Bugs & Unit Tests; Personal Interviews via Skype;
*   **Javier** \- Improve SD; Bugs & Unit Tests
*   **Ted** -
*   **Michael** \- Terminal Performance Improvements
*   **Uwe** -

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 29-Mar-2007](./DSDP/TM/Committer_Phone_Meeting_29-Mar-2007 "DSDP/TM/Committer Phone Meeting 29-Mar-2007") at [1400 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=3&day=29&hour=14&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) \- **attention: DST change in Europe:** 2 hrs / 1 hr earlier!


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_20-Mar-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_20-Mar-2007))