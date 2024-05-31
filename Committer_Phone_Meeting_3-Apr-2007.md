

DSDP/TM/Committer Phone Meeting 3-Apr-2007
==========================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday [Apr 3, 2007](/index.php?title=Apr_3,_2007&action=edit&redlink=1 "Apr 3, 2007 (page does not exist)") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=4&day=3&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
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
*   Wind River - Martin Oberhuber, Uwe Stieber, Michael Scharf, (Ted Williams)

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 29-Mar-2007](/DSDP/TM/Committer_Phone_Meeting_29-Mar-2007 "DSDP/TM/Committer Phone Meeting 29-Mar-2007")

### TM 2.0M6 Testing

*   [TM 2.0 M6 Testing](/TM_2.0_M6_Testing "TM 2.0 M6 Testing")
    *   MUST use Eclipse M6
    *   Will do a new test candidate every day, with a note what changed compared to the previous one. Start each morning with testing, fix bugs in the afternoon. Cronjob will build a new candidate over night. (Plan approved)

### Bugs and open work to be discussed

*   **General Info**
    *   Will need to make some API work in the M7 time frame. Try to have not too many of these, though.
    *   Others will need to be deferred to post-2.0. Looks like we'll probably have TM 3.0 next year rather than TM 2.1. Will discuss in the Monthly meeting tomorrow
    *   Fixing functionality has priority over API this week!
    *   Reference Platforms: Solaris-Motif to be discontinued

  

*   **Major and other important bugs**
    *   [Open Major,Critical,Blocker bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit)
        *   (defer M7) Encodings - Kushal, DaveD; mostly BIDI issues (logical vs. visual data); will need ICU, probably some ICU updates; and similar for USS on zSeries
        *   (M6) Copy&Paste, Collapse, Wizard Properties - DaveM: ssh was OK also with multiple files, perhaps an FTP issue?
        *   (M6) Collapse - probably related to [143458](https://bugs.eclipse.org/bugs/show_bug.cgi?id=143458) (Kushal) Refresh changes selection
        *   (try M6) Programmatic Expand - Martin (Jobs, Async Callbacks)
    *   (defer M7) [180313](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180313) Restore only a single connection on restart
    *   (M6) [180091](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180091), [170916](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170916) (Kushal) EFS --> **AI Kushal M6**, do handle operations
    *   (try M6) [173042](https://bugs.eclipse.org/bugs/show_bug.cgi?id=173042) (Martin) Option to avoid deleting children and keeping collapsed state on Refresh --> probably defer
    *   (M6) [175686](https://bugs.eclipse.org/bugs/show_bug.cgi?id=175686), [180692](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180692) (Martin) Bundling for CVS, Discovery - feature.properties / feature.xml changes for Europa

  

*   **NLS bugs**
    *   (M6) [164413](https://bugs.eclipse.org/bugs/show_bug.cgi?id=164413) (Kushal) Removing Default System Type Combo? - Note it is currently storing Labels instead of Names/Ids! --> Captures on Apr 6th and another one; user docs captured separately
        *   DaveM: Sometimes next to a "New Connection" combo
        *   DaveD: Remove the Combo for M6, but leave the NL Strings in there for now
        *   **AI Kushal Remove the Combo, but leave NL Strings**
    *   (defer M7) Renaming Team View --> Profiles View? - **AI DaveD to investigate**; discuss on next meeting
    *   (defer M7) [154508](https://bugs.eclipse.org/bugs/show_bug.cgi?id=154508) (DaveM) User Docs for SSL --> Reassign to DaveD?
    *   (defer M7) [143412](https://bugs.eclipse.org/bugs/show_bug.cgi?id=143412) (DaveD) User Docs for where passwords are stored
    *   (defer RC) DaveD Chkpii to get rid of unused Properties? Unused Strings in messages.xml? - chkpii does not do this; do not clean them up now, better leave extra ones in

  

*   **API bugs**
    *   (done, review) [180575](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180575) (DaveM) supportsDeferredQueries - Patch from Martin attached -- (done; probably some stuff rejected, **AI Martin** to review
    *   (M6) [180562](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180562) (DaveM) "implements" for constants only --> **AI Today**
    *   (done) [180651](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180651) (DaveM) Martin's recent "internal" ones -- (done)
    *   (try M6) [163592](https://bugs.eclipse.org/bugs/show_bug.cgi?id=163592) (DaveD) API to explicitly save profiles -- Dave working right now on API to avoid automatic commit --> not sure if M6 is possible
    *   (defer M7) [168975](https://bugs.eclipse.org/bugs/show_bug.cgi?id=168975) (DaveD) Events in ISystemRegistry --> not yet looked at; M7 or later; view mechanism of "originating view" to be removed - fair bit of work; model change events should be signaled to headless
    *   (M6) [180642](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180642) (DaveD) testframework.scripting internal - **AI DaveD today**
    *   (M6+) [179184](https://bugs.eclipse.org/bugs/show_bug.cgi?id=179184), [177332](https://bugs.eclipse.org/bugs/show_bug.cgi?id=177332) (DaveD) Persistence Provider: ok for M7 -- want to get in before IBM products migrate
        *   DaveM: For Migration, specify persistence providers that only allow import
        *   DaveD: In WDSC, people are creating profiles themselves
    *   (M6+) [180485](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180485) (Kushal) Showhidden as View Preference - suggestion included -- Kushal agrees; what to do with the filters? -- Kushal started, **M6**; FilterReferenceAdapter, override public Object\[\] getChildren(IProgressMonitor monitor, IContextObject contextObject); Add API for SubSystemConfigurationAdapter.applyViewFilter(IContextObject parent, Object\[\] children);
    *   (M6) [177523](https://bugs.eclipse.org/bugs/show_bug.cgi?id=177523) (Martin) Unify getInstance()
    *   (M6) [180688](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180688) [180690](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180690) (Martin) SystemSignonInformation.getSystemType(), ISubSystem.getSystemType() --> agreed
    *   (try M6) [175680](https://bugs.eclipse.org/bugs/show_bug.cgi?id=175680) [177128](https://bugs.eclipse.org/bugs/show_bug.cgi?id=177128) (Martin) Clean up ISystemRegistry --> not for M6

  

*   **Old stuff**
    *   (?) files.ui: Activator should be internal (util methods to go to RemoteFileUtility)
    *   (?) subsystems.shells.core: What about OutputRefreshJob, its currently needed
    *   (?) [179910](https://bugs.eclipse.org/bugs/show_bug.cgi?id=179910) (Kushal) removing unnecessary upload/download - do we really need still 2 upload methods?
    *   (?) [174945](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174945) General code cleanup - get rid of unused icons, comments, properties
    *   (?) Copyright Updates by Martin

  

Vacation, Away
--------------

*   Kushal out of office for business tomorrow, Wednesday

Action Items
------------

*   [Last Meeting](/DSDP/TM/Committer_Phone_Meeting_29-Mar-2007#Action_Items "DSDP/TM/Committer Phone Meeting 29-Mar-2007") Action Items
*   **Everyone** first test (2 hrs max.), then fix major issues, then look at API. GOAL is to have a good test candidate tomorrow.

Next Meeting
------------

*   [DSDP/TM/Phone Meeting 4-Apr-2007](/DSDP/TM/Phone_Meeting_4-Apr-2007 "DSDP/TM/Phone Meeting 4-Apr-2007") open phone call
*   TM 2.0M6 - 6-Apr-2007
*   [TM Webinar](https://www.eclipse.org/community/webinars2006.php) pre-call on [10-Apr-2007](/index.php?title=10-Apr-2007&action=edit&redlink=1 "10-Apr-2007 (page does not exist)") at [1400 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=4&day=10&hour=14&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800); webinar on [12-Apr-2007](/index.php?title=12-Apr-2007&action=edit&redlink=1 "12-Apr-2007 (page does not exist)")
*   [DSDP/TM/Committer Phone Meeting 10-Apr-2007](/DSDP/TM/Committer_Phone_Meeting_10-Apr-2007 "DSDP/TM/Committer Phone Meeting 10-Apr-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=4&day=10&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_3-Apr-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_3-Apr-2007))