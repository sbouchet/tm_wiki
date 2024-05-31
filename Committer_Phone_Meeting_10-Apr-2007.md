

DSDP/TM/Committer Phone Meeting 10-Apr-2007
===========================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Apr 10, 2007](./index.php?title=Apr_10,_2007&action=edit&redlink=1 "Apr 10, 2007 (page does not exist)") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=4&day=10&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 TM 2.0M6 Testing](#TM-2.0M6-Testing)
    *   [2.2 Bugs and open work to be discussed](#Bugs-and-open-work-to-be-discussed)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave McKnight, Dave Dykstal, Kushal Munir
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber (Michael Scharf n/a, Ted Williams n/a)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 3-Apr-2007](./Committer_Phone_Meeting_3-Apr-2007 "DSDP/TM/Committer Phone Meeting 3-Apr-2007")

### TM 2.0M6 Testing

*   **AI Martin** Prepare statistics on testing and downloads for the next committer meeting
    *   Kushal: A couple of students going to help with testing internal and Open Source RSE in April - testing on Vista
    *   Another students will be working 4 months starting in May, using openRSE for an internal project

### Bugs and open work to be discussed

*   **Plan towards M7**
    *   **Priority #1: Open Major Bugs** \- hanging dstore, Copying issues, NPEs
        *   **NLS bugs**: BIDI, DBCS - Kushal has access to one of the BIDI machines, and can set up a DBCS environment on his Linux box. Priority: 2 rounds of testing: Enablement test - assure that assistence from knowledgeable people is there; assistence test in May. Want Enablement bugs fixed by this or next I-bugs.
        *   Enablement Testers may be able to help fixing bugs and submitting patches - point them to the [TM\_and\_RSE_FAQ](./TM_and_RSE_FAQ "TM and RSE FAQ")
    *   **Priority #2: EFS**: Project is closed on workspace re-start
        *   Workaround: use local projects with linked resources instead
        *   DaveD: CredentialsProvider should not need a shell when credentials are stored
        *   **AI DaveM** Fix ISubSystem.connect(IProgressMonitor, boolean forcePrompt) to take a boolean force; keep old method as a delegate with default forcePrompt=false to avoid unnecessary API breaking change
        *   Might come up with a point patch on update site for adding RSEFileStore.copy() and move() methods
    *   **Priority #3: Remaining API changes** for Persistence, Refresh etc.
        *   Mostly DaveD and Martin
        *   Try to stay API compatible until the EFS and Major Bug fixes are in an I-build
    *   **Javier**: FTP parallel download, allowing to register directory listing parser by extension point
    *   Useractions / Importexport: - **AI Martin** Move packages to "internal"; add to nightly builds; **AI DaveD, Kushal** persistence with User Actions; Dave working on API prerequisites now; **AI DaveM** Import/Export
    *   **Migration Guide**
        *   Open Source: openRSE 1 -> openRSE 2 can be done by Martin
        *   IBM internal RSE7 -> openRSE - a huge change, radically different than openRSE 1 -> openRSE 2, not done with some simple renamings; no hurry doing an RSE7 migration guide before the 2.0 release, people will not be moving before August.
    *   Usersguide: - Will not be taken for translations before the 2.0 Golden Master

  

*   **General Guidelines**
    *   Avoid breaking API changes if possible (keep delegate methods, use deprecation)

Vacation, Away
--------------

*   Javier coming back to London tonight
*   DaveM will be here but just about 10% on Open Source this week
*   Kushal out 1/2 day on Tuesday (during meeting time), another 1/2 day on Wed and full day on Thur
*   DaveD out on Friday 20th

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_3-Apr-2007#Action_Items "DSDP/TM/Committer Phone Meeting 3-Apr-2007") Action Items
*   **DaveD**: Remaining changes for Persistence (will be required for User Actions)
*   **DaveM**: Major bugs for dstore, copying; Create ISubSystem.connect(IProgressMonitor, boolean)
*   **Kushal**: EFS improvements, BIDI bugs
*   **Martin**: Preparing Webinar; Prepare Testing and Download Statistics; Add Import/Export and UDA to I-builds; Refresh improvements; Integrating Terminal with RSE
*   **Javier**: FTP parallel download, registering FTP Parser by extension point

Next Meeting
------------

*   [TM Webinar 12-Apr-2007](https://www.eclipse.org/community/webinars.php#TM)
*   [DSDP/TM/Committer Phone Meeting 17-Apr-2007](./Committer_Phone_Meeting_17-Apr-2007 "DSDP/TM/Committer Phone Meeting 17-Apr-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=4&day=17&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_10-Apr-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_10-Apr-2007))