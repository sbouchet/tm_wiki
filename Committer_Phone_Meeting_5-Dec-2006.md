

DSDP/TM/Committer Phone Meeting 5-Dec-2006
==========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Dec 5, 2006](/index.php?title=Dec_5,_2006&action=edit&redlink=1 "Dec 5, 2006 (page does not exist)") at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=12&day=5&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 Latest News](#Latest-News)
    *   [2.2 Upcoming Work](#Upcoming-Work)
    *   [2.3 Communications](#Communications)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave Dykstal, Dave McKnight, Kushal Munir
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber, (Michael Scharf N/A), (Ted Williams N/A)
*   Tradescape - Lothar Werzinger

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help: **being responsive**
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site

### Latest News

| Martin | 50% | Setting J2SE-1.4; Playing with J2ME; Reporting & Verifying bugs; Reviewing & Releasing; Helping out with Terminal | 50% |
| --- | --- | --- | --- |
| DaveD | 50% | warnings cleanup; Performance Logger to be removed for 2.0?; bugs; junit | 80% |
| DaveM | 80% | Bugs; warnings cleanup; | 80% |
| Kushal | 50% | warnings cleanup; "difficult" warnings now; comm daemon - IBM ok with not having it in OSS | 50% |
| Javier | 50% | FTP bugs, warnings cleanup; proposed a new system for SD, could also discover dstore | 50% |
| Ted | 5% | n/a |  |
| Uwe | 50% | Unittests |  |
| Michael | 50% | n/a |  |

### Upcoming Work

*   **1 week to go** for RSE 1.0.1 fixes ([bugzilla report](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=priority&y_axis_field=assigned_to&z_axis_field=&query_format=report-table&classification=DSDP&product=Target+Management&target_milestone=1.0.1&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&format=table&action=wrap))
    *   DaveM - Cannot reproduce some, e.g. 166345 --> reporter needs to verify
*   **Adding JUnit Tests** (Uwe, DaveD)
    *   Uwe or DaveD to check in; Martin to create features and downloads for tests
    *   Nightly Unit Tests to be added as part of Europa changes by Ted after Dec.15th
    *   **RSE SystemView and Performance**
*   **Compiler Warnings**
    *   See the [Committer Howto](https://www.eclipse.org/dsdp/tm/development/committer_howto.php#check_code) for settings
        *   647 -> 2 dstore.core
        *   109 -> 113 connectorservice.dstore
        *   176 -> 265 rse.core
        *   474 -> 558 files.ui
        *   134 -> 0 logging
        *   637 -> 662 services
        *   653 -> 9 services.dstore
        *   221 -> 250 subsystems.files.core
        *   1622 -> 346 rse.ui
    *   Quickfix for NON-NLS-1; "look for similar problems"; found some strings that should be externalized (jobnames)
    *   Currently we have printlns for many exceptions -- should be logging instead (left in english)
    *   Java5 Array settings -> Fixed by setting Target Platform J2SE-1.4 everywhere
*   **Quality**
    *   Will have a 1-day public round of testing on Tuesday Dec.12, see [RSE 1.0.1 Testing](/RSE_1.0.1_Testing "RSE 1.0.1 Testing")
    *   Need to VERIFY all 1.0.1 fixes, and do another round of sanity checks
    *   **Docs are a high priority**. Add ISV Javadoc where it is still missing or incorrect; review, and improve all docs
*   Planning 2.0
    *   Start IBM and EMO review process for User Actions and Import/Export (DaveD)
        *   Also need a CQ for two Userdoc files for the Internal Comms Daemon
    *   [RSE 2.0 Planning](/RSE_2.0_Planning "RSE 2.0 Planning") \- Finalize the 2.0 Project Plan
    *   **New bugs**: REVIEW [Assigned to Inbox](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&emailassigned_to1=1&emailtype1=exact&email1=dsdp.tm.rse-inbox%40eclipse.org&cmdtype=doit), [Status NEW](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=NEW&cmdtype=doit)
        *   Open bugs: [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1),

### Communications

*   Europa: IBM has a request for anything coming back from Eclipse to have an src.zip (sources only) for everything that was included in the build; there is a template for deriving this; needed for IP reviews; DaveD will work with Ted on this, there might be some functionality in basebuilder already
*   Change Requests
    *   Might need to shift next week's meeting by 1 hour due to Orbit call; Martin to send E-Mail invitation
*   Vacations, Holidays etc.
    *   Movie Day on the 8th in Toronto
    *   Kushal away from 18th
    *   Martin, DaveM away from 25th to 1st
    *   Javier away from 25th to 8th
*   Free discussion -- feelings, comments, critics

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_28-Nov-2006#Action_Items "DSDP/TM/Committer Phone Meeting 28-Nov-2006") Action Items
*   **DaveD** \- Submit UDA and Import/Export for IBM internal review; New bug for moving DTD.
*   **DaveM** \- Bugs; Compiler Warnings (dstore);
*   **Kushal** \- Compiler Warnings (UI); Talk to DaveD re Comm Server; Bugs
*   **Martin** \- Personal Interviews via Skype; Work on [RSE 2.0 Planning](/RSE_2.0_Planning "RSE 2.0 Planning"); [TM and RSE FAQ](/TM_and_RSE_FAQ "TM and RSE FAQ"), improve Wiki and Website (how to contribute); Bugs; Terminalview
*   **Javier** \- Bugs;
*   **Ted** \- Document the build process (DD project), prepare for Europa build
*   **Michael** -
*   **Uwe** \- RSE Systemview performance unit tests

Next Meeting
------------

*   Open [DSDP/TM/Phone Meeting 6-Dec-2006](/DSDP/TM/Phone_Meeting_6-Dec-2006 "DSDP/TM/Phone Meeting 6-Dec-2006") at 9am PST
*   [DSDP/TM/Committer Phone Meeting 12-Dec-2006](/DSDP/TM/Committer_Phone_Meeting_12-Dec-2006 "DSDP/TM/Committer Phone Meeting 12-Dec-2006") at [1700 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=12&day=12hour=17&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_5-Dec-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_5-Dec-2006))