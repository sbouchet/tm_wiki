

DSDP/TM/Committer Phone Meeting 23-May-2006
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday May 23, 2006 at [6.30am PDT / 9.30am Toronto / 3.30pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=5&day=23&hour=13&min=30&sec=0&p1=223&p2=250&p3=421&p4=224) |
| Dial-in: | Skype **martin.oberhuber**, ddykstal (works better than david_dykstal), david-k-mcknight |

Fixed-line fallback dial-in:

*   International **+44 (0)1452 567588**
*   USA Freephone +1 (866) 6161738
*   Passcode: **0587322148 #**

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave Dykstal, Dave McKnight (Kushal Munir was sick)
*   Wind River - Martin Oberhuber

Agenda
------

*   M2 Process Review
    *   Distracted by changing topics?
        *   not really. Getting dicussions going was a good thing. Solicitated extra contributions from Tianchao and Greg.
        *   many bugs were on Linux/Mac - had not been covered yet
    *   Stressed finishing up M2?
    *   Process Improvements for M3?
        *   more nightly and integration drivers
        *   schedule the actual S-build towards M3 on the 29th instead of the 30th; more I-builds 1.5 weeks before the M-build
        *   advantage I-builds: allows reporters to verify builds fixed. To be done on demand when a major feature has been added
            *   N-builds make sense only when Unit tests are in place -- currently everybody seems to be working on CVS
        *   Other commitments - time on Open RSE: DaveD 80%, Kushal 80%, DaveM 25%-50%
        *   Martin added cvschangelog on build.eclipse.org, we can run cron jobs there
*   Bugzilla usage, tips and tricks
    *   Want to use markups like \[api\], \[apidoc\] -- others?
        *   \[mac\] for macos-specific things
        *   Agree that textual tagging is better than multiple RSE components; components are often set wrongly and are more hassle then good.
        *   Dont do an extra step going over all the bugs -- apply the markers only when we are looking at a bug anyways
    *   How to defer bugs
        *   Set target milestone M4 (or other) for deferring
        *   Not use the priority field officially (can use for personal management).
        *   Resolution category WONTFIX for things we'll never address; LATER for "not for 1.0 release"; this will group deferred bugs nicely
    *   How to find a bug to work on: Bugzilla [Status / Assignee / Severity](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=bug_severity&y_axis_field=assigned_to&z_axis_field=bug_status&query_format=report-table&short_desc_type=allwordssubstr&short_desc=&classification=DSDP&product=Target+Management&component=RSE&long_desc_type=allwordssubstr&long_desc=&bug_file_loc_type=allwordssubstr&bug_file_loc=&status_whiteboard_type=allwordssubstr&status_whiteboard=&keywords_type=allwords&keywords=&emailtype1=substring&email1=&emailtype2=substring&email2=&bugidtype=include&bug_id=&votes=&chfieldfrom=&chfieldto=Now&chfieldvalue=&format=table&action=wrap&field0-0-0=noop&type0-0-0=noop&value0-0-0=)
    *   Using Bookmarks (from [TM home page](https://www.eclipse.org/dsdp/tm) and [M2 build notes](http://download.eclipse.org/dsdp/tm/downloads/drops/S-1.0M2-200605191648/buildNotes.php), saved searches, change-multiple-at-once
    *   How to fix a bug: commit comment, when to mark fixed
    *   How to verify and close
*   IP Due Diligence
    *   See [committer HOWTO](https://www.eclipse.org/dsdp/tm/development/committer_howto.php)
    *   How to apply a patch
    *   How to add legacy code
*   Coding Conventions
    *   Toronto folks use a coding style different than the Sun style -- docs available
*   M3 Planning and Priorities
    *   Assign tasks to individual committers?
    *   Getting the API right is the toughest thing!
    *   **1.** Start EMO Review for **all** upcoming legacy contributions:
        *   Docs, user commands, import/export, anything else? -- **DaveD**
        *   commands: needs merging of two components
        *   each added component needs a couple of days of cleanup before it can be submitted
        *   Dave Daniency write some IBM internal unit tests
        *   MartinO to check back with EMO if review is required
    *   **2.** Add Examples to CVS -- **MartinO**
    *   **3.** Make Wizard completely replacable -- **Kushal**; need current status
    *   **4.** UI/Non-UI Refactoring (subsystem/filter) -- Kushal
    *   **5.** Fix critical, major and obvious bugs -- **DaveM**
        *   Feel free to defer bugs you don't find appropriate;
            *   set target milestone M4 is you want it in the release but not quite fix it yet
            *   set resolution type LATER if that's something for RSE 2.0
        *   Write unit tests on the way where appropriate
        *   API improvements; fix "hard" bugs
    *   **6.** Start daily driver schedule - prepare driver for M3 deliverables early -- **DaveD**
        *   Run the driver on demand; add docs to driver; prepare to run it on build.eclipse.org
    *   **7.** Work on ISV Docs
    *   **8.** Add Unit Test Framework -- **DaveD**
        *   The framework that DaveD has just makes it possible to ship them to customers
        *   Suggestion: go ahead and write Unit Tests where it makes sense to have them
        *   Will add them to the framework later
    *   [RSE API Discussion](./RSE_API_Discussion "RSE API Discussion")
    *   [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning")
*   Want regular committer meetings?
    *   IBM people have a weekly meeting currently; could piggypack on that; wednesday 11am
    *   Move to 9.30; try doing with Skype; starting next week.

Action Items
------------

*   Martin to check with Eclipse Legal what's required for legacy contributions
*   Martin to add examples to CVS
*   Martin to document our agreed bugzilla process on the website or wiki (this is a release review item) - including a list of markups we want to use
*   DaveD, DaveM and Kushal to add copyright attributions for merged patches
*   DaveD to re-schedule next week's wednesday meeting
*   DaveD to prepare contributions on bugzilla: Docs, Unittest-driver, User-commands, Import/Export (in this order)
    *   We want to have at least one unit test for something in the repository soon, so we can use it as template for new ones
*   DaveM to create bugzilla entry and tm-log.csv entry for Mike Berger's Spirit patch
*   DaveM and DaveD to review and correct [RSE API Discussion](./RSE_API_Discussion "RSE API Discussion") where necessary
*   DaveM to work on fixing major and critical bugs
*   Kushal to make Wizard completely replacable and continue UI/Non-UI refactoring

Next Meeting
------------

*   Wed 31-May-2006 at 9.30am Toronto time: [DSDP/TM/Committer Phone Meeting 31-May-2006](./Committer_Phone_Meeting_31-May-2006 "DSDP/TM/Committer Phone Meeting 31-May-2006")


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_23-May-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_23-May-2006))