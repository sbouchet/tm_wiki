

DSDP/TM/Committer Phone Meeting 28-Jun-2006
===========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Jun 28, 2006](/index.php?title=Jun_28,_2006&action=edit&redlink=1 "Jun 28, 2006 (page does not exist)") at [6.30am PDT / 8.30am CDT / 9.30am Toronto / 3.30pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=6&day=28&hour=13&min=30&sec=0&p1=223&p2=250&p3=421&p4=224) |
| Dial-in: | Skype **martin.oberhuber**, ddykstal, david-k-mcknight, kushal\_munir, mikey\_yo |

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

*   IBM - Dave Dykstal, Dave McKnight, Kushal Munir, Michael Berger
*   Wind River - Martin Oberhuber

Agenda
------

*   Our top goals
    *   **Grow the Communities** \- active users and adopters. Provide something useful, and help them adopt it (tutorial, docs, mailinglist help).
    *   **Get the APIs Right** \-\- We need to enable API discussions in public.
    *   Get our **Processes** in place.
*   Latest News
    *   Thanks for handling the Project IP Log properly
    *   Nightly builds in place as cron job on build.eclipse.org
    *   dsdp.eclipse.org vserver is set up, ready to serve online docs
*   Status wrt to the [Project Plan](https://www.eclipse.org/dsdp/tm/development/plan.php)
    *   Finishing up M3 - Jun 30 - Functional Complete
        *   Wizard replaceable - Kushal committed the change, some more bug fixes to come
        *   Builds of User doc, Extension point doc, Dstore doc - **DaveD**
        *   Unit tests - Mike?
            *   Have ported the Framework + Tests -- 50 classes in 3 plugins -- but problems running it, keep working on it.
        *   DaveM status? EFS status? Tom Hochstein help?
            *   Some EFS bugs fixed, but not yet quite mature enough.
            *   Want to deliver as a separate "optional" feature, similar to "Team Extras" feature; needs half a day to assemble automated build for this.
        *   Open [major and critical bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit)
        *   Automatic Update Site - **Martin** to look at after M3
        *   Manual test plans - **Martin** to start putting together something
        *   Testing - As sent on dsdp-tm-dev list
    *   Features to be deferred
        *   Examples as separate download - defer, together with experimental EFS download
        *   User actions, Import/Export -- will be needed by IBM clients; deliver as "Experimental" but not part of 1.0, in order to have more time for the IP review
            *   What about "external tools" integration?
    *   Anything missing we need to do?
        *   FTP: How to do remote copy & move? - Wait for Jakarta Commons
*   Work ahead (while DaveD is on vacation)
    *   Overhaul docs to be in sync with current code
        *   Userdoc: not in bad shape - needs manual review and update
        *   ISV doc: structural changes,
            *   link fixup (where ISV doc references the Javadoc) -- package name changes, classname changes -- get some tool help (import into a web building tool once it is built completely -- e.g. Adobe GoLive)
            *   **Mike** could do a first pass (catalog things to be fixed), **Kushal** can do a second one after some more refactoring
    *   More unit tests; server infrastrucure for automated testing
    *   **Kushal** \- More refactoring (until end of july -- to be finished before M4)
    *   Drive the community [RSE API Discussion](/RSE_API_Discussion "RSE API Discussion") \-\- API bug entries -- **DaveM**
    *   Remove references to "IBM", "etools" and similar strings -- **DaveM**
    *   Build warnings, usage of Platform Internal packages / classes
        *   DaveD already removed "deprecated" stuff and tried to find alternatives to "internal" stuff
        *   Some areas might not be easy (or even impossible) to remove -- most of them show up as warnings in PDE (currently 600)
        *   "hygiene" changes -- make changes as we go along for now: fix build warnings when a file is edited anyway; everybody to use default warnings; have a separate task for remaining the rest after M4
    *   Drive [RSE 2.0 Planning](/RSE_2.0_Planning "RSE 2.0 Planning")
        *   Want Requirements for 2.0 by the Release Review (1 week after M5, end of september)
        *   Shall we have another F2F meeting? - Probably helpful if architectural things are to be discussed
        *   CDT developer summit will be end of september
        *   DD F2F not yet scheduled
        *   Plans: All Experimental stuff; New protocols on connection side; F2F meeting probably in November?
    *   Incorporate Jakarta Commons Net (as soon as approved by EMO)
*   Free discussion -- feelings, comments, critics

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_23-May-2006#Action_Items "DSDP/TM/Committer Phone Meeting 23-May-2006") Action Items
*   **DaveD** \- Doc build, presistency bugs
*   **DaveM** \- bug fixing, hygiene changes, drive API discussion
*   **Kushal** \- bug fixing, refactoring, doc review
*   **Mike** \- junit delivery, doc review
*   **Martin** \- document bugzilla process and markups on website
    *   Setup vserver for serving online docs
    *   Review bug assignments, priorities, target milestones
    *   Update Project Plan, manual test plan, update site

Next Meeting
------------

*   Open [DSDP/TM/Phone Meeting 5-Jul-2006](/DSDP/TM/Phone_Meeting_5-Jul-2006 "DSDP/TM/Phone Meeting 5-Jul-2006") at 9am PST
*   [DSDP/TM/Committer Phone Meeting 19-Jul-2006](/DSDP/TM/Committer_Phone_Meeting_19-Jul-2006 "DSDP/TM/Committer Phone Meeting 19-Jul-2006") at 9.30am Toronto
*   Dave D on vacation Jul 1-15


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_28-Jun-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_28-Jun-2006))