

DSDP/TM/Committer Phone Meeting 2-Aug-2006
==========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday Aug 2, 2006 at [6.30am PDT / 8.30am CDT / 9.30am Toronto / 3.30pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=7&day=19&hour=13&min=30&sec=0&p1=223&p2=250&p3=421&p4=224) |
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

*   IBM - Dave Dykstal, Dave McKnight, Kushal Munir
*   Wind River - Martin Oberhuber

Agenda
------

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site
*   Latest News
    *   Martin -- Updated ISV doc build process, fixed some warnings; optimized update site generation; started manual test plans
    *   DaveD -- Docs update - fixed bad links in guide & tutorial; doing TOC today; making notes of things that should probably not be API; tutorial should probably be taken out of help and reference the project only
    *   DaveM -- defect cleanup of straightforward things (IBM things) - helpContexts: remove links? Can wait for now since it's a user thing. Remove compileCommands.exsd.
    *   Kushal -- defect cleanup; hi-pri first; checkin pending today
    *   Others
        *   DaveD to do some refactoring of persistency from UI into core, and Message stuff into core.
        *   DaveD to look at Mike's spreadsheet and decide what to do
*   Urgent work to do
    *   Legal: JUnit (Some IBM signoffs needed, but not too hard); Jakarta-commons (EMO working on it)
    *   What is API? --> Move to "internal"?
        *   The more we hide by making "internal", the easier it will be for clients to find the relevant stuff.
        *   What about things in the Platform? E.g. Extension-point **rseConfigDefaults** vs. **plugin_customization.ini**
        *   Bring ISV docs up-to-date -- needed for API discussions. [bug 150548](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150548) has the mapping from Mike.
            *   Do a search&Replace for "com.ibm.etools" first, use a broken-link-tool then (e.g. download the site from [http://dsdp.eclipse.org/help/latest/](http://dsdp.eclipse.org/help/latest/) with firefox; or just expand the jar)
            *   Tutorial docs: DaveD or Kushal
    *   "Big Rock" API issues --> see [RSE API Discussion](./RSE_API_Discussion "RSE API Discussion"), [Meeting 19-Jul-2006 Notes](./Committer_Phone_Meeting_19-Jul-2006 "DSDP/TM/Committer Phone Meeting 19-Jul-2006")
    *   Work on open bugs by priority
        *   Open bugs: [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1), [P1 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit)
*   Other items
    *   Thanks for updating bugzilla - Kushal?
    *   bugzilla: dsdp.tm.rse-inbox@eclipse.org
        *   Assign bugs to the inbox when you don't know what to do with them; DaveD and I will review them again later
        *   It's also OK to defer bugs past 1.0 by setting status to LATER
    *   committing: Please include bugzilla references on the FIRST LINE of the commit message
        *   Easier to track checkins from the [CVS Changelog](http://download.eclipse.org/dsdp/tm/downloads/drops/N-changelog/index.html)
        *   Example: "**Bug 149331 - updating extension point schemata to remove etools references.**"
        *   Commit messages like this are not harder to write, but much more helpful to read in the changelog
    *   Please focus on "big rocks" (hi-pri bugs)
    *   Manual test plans - in work by **Martin**
    *   EFS feature, Examples feature to be created by Martin
*   Free discussion -- feelings, comments, critics
    *   Martin wants to stabilize M4 early --> label an I-build early, then create another label for the M-build and move it until release. This gives us more freedom for checkins during the integration phase (but requires that features are in earlier)
    *   Friday & Monday - holiday in Canada --> Aug 11 will be I-build, Aug 18 the M-build
    *   Javier to join us for the next committer meeting(s)

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_26-Jul-2006#Action_Items "DSDP/TM/Committer Phone Meeting 26-Jul-2006") Action Items
*   **DaveD** \- Review Mike's mappings, Doc update, JUnit legal, Service Error Reporting API, No-Password-API, SystemRegistry API
*   **DaveM** \- bug fixing, Parallel Services API, hygiene changes
*   **Kushal** \- refactoring checkin, doc review (with DaveD), bug fixing
*   **Martin** \- EFS & Examples features, build scripts, Manual test plan, API Review

Next Meeting
------------

*   Open [DSDP/TM/Phone Meeting 2-Aug-2006](./Phone_Meeting_2-Aug-2006 "DSDP/TM/Phone Meeting 2-Aug-2006") at 9am PST
*   [DSDP/TM/Committer Phone Meeting 9-Aug-2006](./Committer_Phone_Meeting_9-Aug-2006 "DSDP/TM/Committer Phone Meeting 9-Aug-2006") at 9.30am Toronto


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_2-Aug-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_2-Aug-2006))