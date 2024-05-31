

DSDP/TM/Committer Phone Meeting 19-Jul-2006
===========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Jul 19, 2006](/index.php?title=Jul_19,_2006&action=edit&redlink=1 "Jul 19, 2006 (page does not exist)") at [6.30am PDT / 8.30am CDT / 9.30am Toronto / 3.30pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=7&day=19&hour=13&min=30&sec=0&p1=223&p2=250&p3=421&p4=224) |
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
    *   Get our **Processes** in place --> JUnit
*   Latest News
    *   Martin -- **Tutorial project** checked in, **Update Site** Project ready but not yet checked in
        *   Martin has also made a few minor fixes in RSE code. Created bug entries for each, attached a patch to allow easy review, but committed the patch himself in order to keep the workspace clean --> IBM people please take the bugs, review the patch and close the bug. A bugzilla query for "All open bugs with a patch attached" is below.
    *   Mike -- Patch for docs, JUnit patch, RSE 7 translation map
    *   DaveM -- bugfixes, IBM strings
    *   Kushal -- Met with Mike; legal work on test framework (Legal representative at IBM passed away!); WizardSelectionPage
*   Urgent work to do
    *   DaveD will continue the Legal process from Kushal for the **JUnit test framework** \- [bug 149080](https://bugs.eclipse.org/bugs/show_bug.cgi?id=149080)
    *   "Big Rock" API issues --> [RSE API Discussion](/RSE_API_Discussion "RSE API Discussion")
        *   Clarify and implement **"No password" API** \- [bug 142471](https://bugs.eclipse.org/bugs/show_bug.cgi?id=142471), [bug 147532](https://bugs.eclipse.org/bugs/show_bug.cgi?id=147532)
            *   DaveD to look at this; review martin's patch on [bug 150929](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150929)
        *   Clarify **Service Error Reporting** \- [bug 149472](https://bugs.eclipse.org/bugs/show_bug.cgi?id=149472)
            *   want a more easy way to construct SystemMessageException (without message-id or the need to use XML message files)
            *   still use SystemMessageException as the means of reporting errors (re-enable the corresponding code).
            *   DaveD to look into that in more detail
        *   Clarify **Multiple parallel service requests**
            *   DaveM to look into that in more detail - [bugs 142478,149133,149179](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&bug_id=142478,149133,149179)
            *   Suggestion: allow parallel queries for some long-running requests (download, upload) but make sure that core RSE does the Job scheduling such that short-lived requests like directory queries are always queued and synchronized properly. Document File Service APIs for that suggestion. Probably we'll have a series or Reuqest classes, and have a separate ISchedulingRule for each of them in Eclipse jobs.
        *   **SystemRegistry.createHost()** modifications
            *   DaveD to look at [bug 150168](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150168)
            *   DaveM to look at [bug 150265](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150265)
    *   Work on open bugs by priority (first review existing patches, then P1, then P2 and \[api\])
        *   Open bugs: [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1), [P1 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit)
    *   Bring ISV docs up-to-date -- needed for API discussions - Kushal merged [bug 149331](https://bugs.eclipse.org/bugs/show_bug.cgi?id=149331) but more work to do
        *   Who will bring Tutorial docs up to date?
*   Other items
    *   Please triage bugs in "New" state such that we get a handle which we won't work on for 1.0
    *   vserver for serving online docs -- set up, but still problems, webmasters are not responsive
    *   Automatic Update Site - **Martin** has it, will commit the next days
        *   Building the update site needs manual interaction; OK for now since we want to know when we update the site anyway
        *   Update Site URL to go into the RSE Features
    *   Manual test plans - **Martin** to start putting together something
    *   EFS feature
    *   Jakarta Commons - hopefully EMO will complete review soon
*   Free discussion -- feelings, comments, critics

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_28-Jun-2006#Action_Items "DSDP/TM/Committer Phone Meeting 28-Jun-2006") Action Items
*   **DaveD** \- Review Patches, JUnit legal, No-Password-API, Service Error Reporting API, SystemRegistry API, bug fixing (persistency)
*   **DaveM** \- Parallel Services API, bug fixing, hygiene changes, drive API discussion
*   **Kushal** \- follow-up with Mike; bug fixing, refactoring, doc review
*   **Martin** \- Setup vserver for serving online docs, Update site, Manual test plan, API Review

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 26-Jul-2006](/DSDP/TM/Committer_Phone_Meeting_26-Jul-2006 "DSDP/TM/Committer Phone Meeting 26-Jul-2006") at 9.30am Toronto
*   Open [DSDP/TM/Phone Meeting 2-Aug-2006](/DSDP/TM/Phone_Meeting_2-Aug-2006 "DSDP/TM/Phone Meeting 2-Aug-2006") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_19-Jul-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_19-Jul-2006))