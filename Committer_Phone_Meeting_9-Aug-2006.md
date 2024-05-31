

DSDP/TM/Committer Phone Meeting 9-Aug-2006
==========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [Aug 9, 2006](/index.php?title=Aug_9,_2006&action=edit&redlink=1 "Aug 9, 2006 (page does not exist)") at [8.30am Rochester / 9.30am Toronto / 2.30pm London / 3.30pm Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=8&day=9&hour=13&min=30&sec=0&p1=223&p2=250&p3=421&p4=136&iv=1800) |
| Skype Dial-in: | **+99008275601400** (this call is **free** from Skype) |
| Fixed-line Dial-in: | US, call **1-712-432-4000** (long distance charges)    Austria: **0820 400 01562** (national call charges)   In UK: **0870 119 2350** (national call charges)   |
| Passcode: | **5601400** |

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

*   IBM - Dave Dykstal, Dave McKnight (Kushal Munir - sick)
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber

Agenda
------

*   Our top goals
    *   **Grow the Communities** \- active users and adopters --> tutorial, docs, mailinglist help
    *   **Get the APIs Right** --\> enable public API discussion --> ISV docs, Wiki API discussion, \[api\] bugzilla's
    *   Get our **Processes** in place --> JUnit, nightly builds, infocenter, update site
*   Latest News
    *   Martin -- Javier; Ericsson probably joining; PMC:Europa; ssh enhancements (pattern parsing)
        *   DKM: local pattern parsing also done on iSeries QShell; common preference page for patterns?
    *   DaveD -- Almost all docs links fixed; users can file bugs against docs now; now working on signon without password
        *   DKM: pathes too long for Windows (256 chars)
        *   MOB: take path components and use as prefix for keys, in order to collapse dir structure? - DD: already done partially. Change areas for team support and merging? - MO: If the contents is sorted, the areas of change will not overlap. DD to check possibility of collapsing
    *   DaveM -- Fixing bugs; will look at P1 bugs. MOB -- use Java Exception Breakpoints
    *   Kushal -- sick
    *   Javier -- Updates - catchup with everything
    *   Other News --
*   Urgent work to do
    *   Bug Work
        *   bugs [149186](https://bugs.eclipse.org/bugs/show_bug.cgi?id=149186) still open, [149133](https://bugs.eclipse.org/bugs/show_bug.cgi?id=149133) reopened, [148981](https://bugs.eclipse.org/bugs/show_bug.cgi?id=148981) easily reproducable
        *   Please try a bit harder to reproduce problems, and verify fixes. It's OK to ask reporters more questions if you cannot reproduce something; it's annoying for reporters if the assigneed doesnt even to try reproduce something. In order to fix a bug, we should first understand it, then fix it.
        *   Kushal where are your checkins? Why are your bugs still in "NEW" state?
        *   We should be **accountable and honest**: promises should be kept. If we are not able to keep a promise, we should be honest enough to tell others we're not going to make it. Only like that, our project will be plannable and forseeable. It's ok if we have other duties, get sick or on vacation. But please let others know, and keep the status of your bug tracked so that everybody knows what's going on. **Dont** keep bugs in NEW state forever.
            *   You can now assign back to **dsdp.tm.rse-inbox@eclipse.org**
        *   Open bugs: [Open with Patch](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1), [P1 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&cmdtype=doit), [API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit), [P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit)
    *   API Things
        *   **M4 is API freeze - what does API freeze mean?**
            *   Like most Eclipse projects: after M4, we'll need to vote among committers before making API changes
            *   API changes will not be impossible, but they will be harder
            *   With M5, the API will be finally frozen (including scripts to check for API changes).
        *   Parallel Services --> see [RSE API Discussion](/RSE_API_Discussion "RSE API Discussion"), [Meeting 19-Jul-2006 Notes](/DSDP/TM/Committer_Phone_Meeting_19-Jul-2006 "DSDP/TM/Committer Phone Meeting 19-Jul-2006"). We might need to support parallel access in the services, because clients can request the service UI-Less and make requests in arbitrary parallel threads
            *   Javier: use java 1.5 util.concurrent? - Better **stay with 1.4** for now.
            *   Here's a [How to set up a plugin to force using Java 1.4 even if 1.5 is available](http://michaelscharf.blogspot.com/2006/07/how-to-setup-some-plugins-to-use-java.html)
            *   MOB to implement a queue for ssh
            *   Get rid of service calls on UI thread
        *   Other "Big Rock" API issues
        *   Making stuff **internal**: EFS, Service and Subsystem implementations, what else? -- DD to compile a list of suggestions
            *   Make all framework external, all implementation internal. It doesnt make sense to derive from an implementation in order to create a modified implementation. Make FTP, ssh, local internal; Have a closer look at dstore since it is designed to be extendible.
        *   What about things in the Platform? E.g. Extension-point **rseConfigDefaults** vs. **plugin_customization.ini**
            *   Kushal to review, remove if possible.
            *   Create a list of potentially obsolete things on the [RSE 2.0 Planning](/RSE_2.0_Planning "RSE 2.0 Planning") page.
    *   Legal: JUnit (Some IBM signoffs needed, but not too hard); Jakarta-commons (TBD aug.24 latest)
        *   Windriver has submitted the terminalview; to be refactored and hooked up with IShellService
        *   DKM: are IShellService streams sufficient? Its a tty after all
*   Other items
    *   Keeping Tutorial up-to-date vs. review at the end of the release process
    *   Javier & Martin Fixing things in RSE -- e.g. casts and deprecated implementations -- what process to use?
        *   Subscribe to **dsdp-tm-cvs-commit@eclipse.org**
            *   Can be subscribed from the [TM Developer Home Page](https://www.eclipse.org/dsdp/tm/developers/index.php)
            *   Mark minor changes as **\[cleanup\]** in the commit comment
        *   Review changes on the [changelog](http://download.eclipse.org/dsdp/tm/downloads/drops/N-changelog/index.html)
        *   e.g. ISubSystem.setVendorAttribute() vs. SubSystem.setVendorAttribute()
        *   e.g. RemoteCommandHelpers:93, IRemoteCmdSubSystem cmdSubSystem = (RemoteCmdSubSystem)sses\[i\]
        *   e.g. SubSystem.getRemoteAttribute() used by RemoteCmdSubSystem
            *   decide about deprecated for M5
        *   e.g. SubsystemConfiguration vs. SubSystemConfiguration
        *   e.g. unnecessary checks: if (x instanceof X && x!=null)
        *   e.g. adding documentation to interfaces
            *   Documentation being repeated in the abstract superclass impl of the interface: put correct docs into the interface, and have the abstract class just refer to the interface with @see
        *   e.g. adding //$NON-NLS-1$ for Strings that are clearly not to be translated
            *   DONT do that for example code
    *   Please focus on "big rocks" (hi-pri bugs)
    *   Manual test plans - in work by **Martin**
    *   EFS feature, Examples feature to be created by Martin
*   Free discussion -- feelings, comments, critics
    *   Move M4 ? Not if we are able to make the P1, P2 things and most \[api\] things
    *   Try to keep current, and see how we're getting along. If it turns out we have too many big things after I-build, we'll move by another week
    *   Javier still talking with Scott Lewis -- Javier to talk to him again once SD is integrated with Eclipse
    *   Javier on holiday till September

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_2-Aug-2006#Action_Items "DSDP/TM/Committer Phone Meeting 2-Aug-2006") Action Items
*   **DaveD** \- JUnit legal, No-Password-API, Service Error Reporting API, SystemRegistry API. Check collapsing persistence Properties nodes to fewer files. Compile a list of suggestions for making classes / packages internal.
*   **DaveM** \- bug fixing (download-upload P1); get rid of Service calls on UI thread; hygiene changes
*   **Kushal** \- refactoring checkin, BUG TRIAGE, bug fixing; review & get rid of rseConfigDefaults
*   **Martin** \- Move pattern parsing to core, Service queue for ssh, EFS & Examples features, build scripts, Manual test plan, API Review, Jakarta-commons, WR-terminalview; Review if IShellService is sufficient for terminal
*   **Javier** \- vacation; hook up with Scott Lewis once SD is committed
*   **Everyone** \- List obsolete API on [RSE 2.0 Planning](/RSE_2.0_Planning "RSE 2.0 Planning") page; Mark hygiene changes as \[cleanup\] in commit comment, subscribe dsdp-tm-cvs-commit@eclipse.org

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 16-Aug-2006](/DSDP/TM/Committer_Phone_Meeting_16-Aug-2006 "DSDP/TM/Committer Phone Meeting 16-Aug-2006") at 9.30am Toronto
*   Open [DSDP/TM/Phone Meeting 6-Sep-2006](/DSDP/TM/Phone_Meeting_6-Sep-2006 "DSDP/TM/Phone Meeting 6-Sep-2006") at 9am PST


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_9-Aug-2006](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_9-Aug-2006))