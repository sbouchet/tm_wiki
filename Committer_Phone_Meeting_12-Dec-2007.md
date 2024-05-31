

DSDP/TM/Committer Phone Meeting 12-Dec-2007
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday Dec 12, 2007 at [1600 UTC / 1100 Eastern](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=12&day=12&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | Martin to call everybody by Skype |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, kevin.j.doyle, xuan.chen886, rupen.mardirossian, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
    *   [2.1 Current Work](#Current-Work)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Xuan Chen, Dave McKnight
*   Wind River - Martin Oberhuber
*   Symbian - Javier Montalvo Orus

Agenda
------

*   Last meeting: [DSDP/TM/Committer Phone Meeting 27-Nov-2007](./Committer_Phone_Meeting_27-Nov-2007 "DSDP/TM/Committer Phone Meeting 27-Nov-2007")

### Current Work

*   **Skype Call Quality**
    *   Excellent with 4 participants
*   **M4 approaching** \- should we arrange for an RC / test round before Christmas?
    *   I-build on Thursday 20th would be candidate for M4
    *   Xuan won't have time for testing; want to finish cancelable fix for archives on dstore (code done but not tested)
*   **DaveD:**
    *   Finished majority of release work for IBM should now be able to concentrate on TM 100%. Will be working between Christmas and New Year's Day.
*   **DaveM:**
    *   [bug 209704](https://bugs.eclipse.org/bugs/show_bug.cgi?id=209704) \- Contribute encoding conversion extension point - finished
    *   [bug 209703](https://bugs.eclipse.org/bugs/show_bug.cgi?id=209703) \- Can one property page affect the contents of another property page?
        *   Have a UI extension point for modifying encoding properties? - Problem is that it's not always applicable; extending an existing property page might be a maintenance nightmare
        *   Better show the "special encoding" stuff on the same page as the original encoding property page - have them register an "enhanced property page" which not only shows their additional controls, but also the original encoding control.
*   **Xuan:**
    *   Working on "cancelable" fix for archive support in dstore
*   **Javier:** -
    *   Will commit some unit tests till christmas; will work on "console input" enhancement for FTP
    *   Participating on DemoDay in London, showed a Symbian Demo on TM - attendance about 15 people
    *   Took a quick look at TCF source code, porting agent to Symbian should be simple
*   **Martin:** \- Been working on TCF mostly; will need more feedback
    *   Need to put Project Plan on the Web; Update Releng scripts to automatically run unit tests at night
*   **Questions** \- support Mac OS as secondary platform
    *   Secondary platform definition:  
        For all IES problems on a Secondary Platform/JRE, first an attempt must be made to replicate the problem on a Primary Platform/JRE. If it can be replicated on a Primary Platform/JRE then it will be entered into the standard Primary Platform/JRE support process and prioritized accordingly. If it cannot be reproduced on a Primary Platform/JRE, then the Eclipse team will rely on the submitter for platform/JRE expertise and equipment to de-bug the problem. It will be added to the support queue, and prioritized with all outstanding defects.
        *   Martin: Our Platform commitments depends on what committer can actually support it. **AI DaveD** decide whether he wants MacOS X as primary or secondary platform.
    *   What TM release to best take for a Service release based on Eclipse 3.3?
        *   TM 2.0.2 is best.
*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   Jan 2 is fine for Xuan, DaveM
*   Javier on vacation Dec.22 until Jan.6
*   DaveM vacation Dec.24 till Jan.1
*   Xuan Dec.21 till Jan.2

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_27-Nov-2007#Action_Items "DSDP/TM/Committer Phone Meeting 27-Nov-2007") Action Items
*   **DaveD**: fixes, unit tests, Mac commitment?
*   **DaveM**: Ask committers about multi-property-dialog; fixes, unit tests; ask Violaine about [bug 209704](https://bugs.eclipse.org/bugs/show_bug.cgi?id=209704)
*   **Xuan**: fixes, unit tests
*   **Martin**: Update bugzilla's; Write-up TM 3.0 Plan; Look at PropertyDescriptor issues; unit tests; Releng Fixes, Newsgroup
*   **Javier**: fixes, unit tests; document the Symbian internal test setup similar to [CVS](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204138#c20) \-\- see also [CVS_Development#Testing](./CVS_Development#Testing "CVS Development")

Next Meeting
------------

*   Committer Phone Meeting 2-Jan-2008: discussed on the [9-Jan-2008 monthly meeting](./Phone_Meeting_9-Jan-2008 "DSDP/TM/Phone Meeting 9-Jan-2008") instead
*   Monthly [DSDP/TM/Phone Meeting 9-Jan-2008](./Phone_Meeting_9-Jan-2008 "DSDP/TM/Phone Meeting 9-Jan-2008") at [9am PST / 1700 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=1&day=9&year=2008&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Committer Phone Meeting 23-Jan-2008](./Committer_Phone_Meeting_23-Jan-2008 "DSDP/TM/Committer Phone Meeting 23-Jan-2008") at [1600 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=1&day=23&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_12-Dec-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_12-Dec-2007))