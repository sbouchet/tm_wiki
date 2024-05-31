

DSDP/TM/Committer Phone Meeting 26-Jul-2006
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Jul 26, 2006](./index.php?title=Jul_26,_2006&action=edit&redlink=1 "Jul 26, 2006 (page does not exist)") at [6.30am PDT / 8.30am CDT / 9.30am Toronto / 3.30pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=7&day=19&hour=13&min=30&sec=0&p1=223&p2=250&p3=421&p4=224) |
| Dial-in: | Skype **martin.oberhuber**, ddykstal, david-k-mcknight, kushal_munir |

Fixed-line fallback dial-in:

*   International **+1 314-655-1411**
*   North America **+1 877-422-0035** (toll free)
*   Passcode: **764918**

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave Dykstal, Dave McKnight (Kushal Munir not available)
*   Wind River - Martin Oberhuber

Agenda
------

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site
*   Latest News
    *   Martin -- Created infocenter (at [http://dsdp.eclipse.org/help/latest/](http://dsdp.eclipse.org/help/latest/)), update site (at [http://download.eclipse.org/dsdp/tm/testUpdates](http://download.eclipse.org/dsdp/tm/testUpdates))
    *   DaveD -- Went through bugs and assigned
    *   DaveM -- Vacation; hopefully time for openRSE next week
    *   Kushal -- Progress on refactoring; to be complete end of the week
    *   Others
        *   Mike Berger left, replacement probably starts in August
*   Urgent work to do
    *   Legal - JUnit, Jakarta-commons
    *   "Big Rock" API issues --> see [RSE API Discussion](./RSE_API_Discussion "RSE API Discussion"), [Last Meeting Notes](./Committer_Phone_Meeting_19-Jul-2006 "DSDP/TM/Committer Phone Meeting 19-Jul-2006")
    *   Bring ISV docs up-to-date -- needed for API discussions [bug 149331](https://bugs.eclipse.org/bugs/show_bug.cgi?id=149331) but more work to do.
        *   Do a search&Replace for "com.ibm.etools" first, use a broken-link-tool then (e.g. download the site from [http://dsdp.eclipse.org/help/latest/](http://dsdp.eclipse.org/help/latest/) with firefox; or just expand the jar)
        *   Tutorial docs: DaveD or Kushal
    *   Work on open bugs by priority
        *   Open bugs: [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1), [P1 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit)
*   Other items
    *   Please be responsive on bugs / api discussions
        *   Please triage bugs in "New" state such that we get a handle on what's going on
        *   Set them "Assigned" when you can handle them; Reassign when somebody else should work on them; add a comment and leave them "New" for now when you don't know what to do with them.
        *   It's also OK to defer bugs past 1.0 by setting status to LATER
    *   Manual test plans - **Martin** to start putting together something
    *   EFS feature, Examples feature to be created by Martin
    *   Jakarta Commons - hopefully EMO will complete review soon (currently 119 open!)
*   Free discussion -- feelings, comments, critics
    *   DaveD ok to work on the "big rock" bugs and ISV docs

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_19-Jul-2006#Action_Items "DSDP/TM/Committer Phone Meeting 19-Jul-2006") Action Items
*   **DaveD** \- Review Patches, JUnit legal, Service Error Reporting API, No-Password-API, SystemRegistry API, docs (with Kushal), bug fixing (persistency)
*   **DaveM** \- Parallel Services API, bug fixing, hygiene changes
*   **Kushal** \- refactoring, doc review (DaveD), bug fixing
*   **Martin** \- EFS & Examples features, build scripts, Manual test plan, API Review

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 2-Aug-2006](./Committer_Phone_Meeting_2-Aug-2006 "DSDP/TM/Committer Phone Meeting 2-Aug-2006") at 9.30am Toronto
*   Open [DSDP/TM/Phone Meeting 2-Aug-2006](./Phone_Meeting_2-Aug-2006 "DSDP/TM/Phone Meeting 2-Aug-2006") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_26-Jul-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_26-Jul-2006))