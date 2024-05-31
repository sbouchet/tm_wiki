

DSDP/TM/Committer Phone Meeting 31-May-2006
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday May 31, 2006 at [6.30am PDT / 8.30am CDT / 9.30am Toronto / 3.30pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=5&day=31&hour=13&min=30&sec=0&p1=223&p2=250&p3=421&p4=224) |
| Dial-in: | Skype **martin.oberhuber**, ddykstal, david-k-mcknight, kushal\_munir, mikey\_yo |

Fixed-line fallback dial-in:

*   International **+1 314-655-1411**
*   North America **+1 877-422-0035** (toll free)
*   Passcode: **764918**

Attendees
---------

*   IBM - Dave Dykstal, Dave McKnight, Kushal Munir, Michael Berger
*   Wind River - Martin Oberhuber

Agenda
------

*   Our top goals
    *   Enable Community Participation, grow the Community
        *   That's the #1 requirement for release review - active user and adopter communities.
        *   We get those through providing something useful for them, and helping them adopt it (tutorial, docs, mailinglist help)
    *   Get the APIs Right
        *   We need to enable API discussions in public.
    *   Get our Processes in place
*   Process/IP/Legal
    *   Comfortable with bugzilla and CVS processes? - [TM Developer Resources](https://www.eclipse.org/dsdp/tm/development/index.php)
    *   tm-log.csv -- questions?
        *   Logging on a per-contribution basis: if multiple patches are on a single bugzilla, each is a line in the log.
        *   Update-change-Commit the log early to avoid merging or making it a bottleneck.
    *   recent contributions: docs, junit, user-actions, import/export
*   RSE/EFS discussion
    *   [RSE API Discussion](./RSE_API_Discussion "RSE API Discussion")
        *   Don't want to make this page a duplicate of the docs. Want to drive API discussions over the javadoc.
        *   Need to reconcile the javadoc with the Wiki page -- make some classes / interfaces internal
        *   Want the Wiki page to be a directory into what's going on / being planned.
        *   SystemMessages API?
    *   [Eclipse File Service APIs Compared](./Eclipse_File_Service_APIs_Compared "Eclipse File Service APIs Compared")
        *   Can we make EFS a Plan item? Any big rocks to overcome? Get help from Tianchao?
        *   Continue discussion with Tianchao; concerned that he only sees "files" while there are other subsystems.
        *   Eclipse 3.2 has chicken&egg problems when creating projects, because temp files are stored in the RemoteSystemsTempFiles project. This leads to race conditions - not sure how to address this, DaveM has a patch for Eclipse to make it work. For now, JDT or CDT do not yet support EFS (Patch from Tianchao for CDT is on [bug 142092](https://bugs.eclipse.org/bugs/show_bug.cgi?id=142092))
        *   There are other EFS problems, e.g. [bug 134270](https://bugs.eclipse.org/bugs/show_bug.cgi?id=134270) being deferred to Eclipse 3.3 -- they want to wait until there are more EFS clients
        *   EFS support will most probably remain a Toy until release.
        *   An EFS Browser in RSE seems to be a valuable thing -- could be based on the "Local" system type. Would be a great project for somebody to do, but the RSE core team will not have time to address this soon -- perhaps as an Example late in August.
    *   [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning")
*   Give better access to docs?
    *   Online browseable docs? - AI Martin: Get this set up
    *   Downloadable compiled docs?
    *   Update Site?
*   Mailing List Duty
    *   All committers should be active on the mailing lists
*   Bugzilla Situation - use "Rember Search as.." in Bugzilla
    *   [RSE Open Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit)
    *   [RSE Hi-pri Enhancements](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=enhancement&priority=P1&priority=P2&cmdtype=doit)
    *   [141835](https://bugs.eclipse.org/bugs/show_bug.cgi?id=141835) \- user id is not stored
    *   Edit searches and let bugzilla remember the new ones... e.g. "Assigned to Me"
*   [Last meeting](./Committer_Phone_Meeting_23-May-2006 "DSDP/TM/Committer Phone Meeting 23-May-2006") action items
*   Free discussion -- feelings, comments, critics
*   Next steps
    *   DaveD - contributions(junit, user-actions, import/export), automated builds, bugfixing
    *   DaveM - bugfixing, drive the API discussions, ML duty
    *   Kushal - wizard completely replaceable, ui/non-ui refactoring
    *   Martin - Process Docs, Press Text, Tutorial/Getting Started, ssh fixes, api and doc reviews, Doc Server

Next Meeting
------------

*   Open [DSDP/TM/Phone Meeting 7-Jun-2006](./Phone_Meeting_7-Jun-2006 "DSDP/TM/Phone Meeting 7-Jun-2006") at 9am PST
*   Martin O on vacation Jun 12-23
*   [DSDP/TM/Committer Phone Meeting 28-Jun-2006](./Committer_Phone_Meeting_28-Jun-2006 "DSDP/TM/Committer Phone Meeting 28-Jun-2006") at 9.30am Toronto
*   Dave D on vacation Jul 1-15


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_31-May-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_31-May-2006))