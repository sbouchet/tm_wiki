

DSDP/TM/Committer Phone Meeting 21-May-2008
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday May 21, 2008 at [1500 UTC / 0800 SFO / 1000 Rochester / 1100 Toronto / 1600 London / 1700 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=5&day=21&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | Join [Skypecast](https://skypecasts.skype.com/skypecasts/skypecast/detailed.html?id_talk=4486475&hash=b8c0f4b4f982e86cfb0c) |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kevin.j.doyle, xuan.chen886, rupen.mardirossian, javier.montalvoorus, eugenetarassov, michael\_scharf, uwe.stieber, radoslav.gerganov, wrsfburton.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 **New Stuff**](#New-Stuff)
    *   [2.2 **Steps Towards Ganymede**](#Steps-Towards-Ganymede)
    *   [2.3 What will happen after Ganymede?](#What-will-happen-after-Ganymede.3F)
    *   [2.4 Questions](#Questions)
*   [3 Vacation, away](#Vacation.2C-away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Xuan Chen, Dave McKnight, Dave Dykstal, Rupen Mardirossian, Kevin Doyle
*   Wind River - Martin Oberhuber, Uwe Stieber
*   ProSyst - Radoslav Gerganov
*   **Regrets this time**: Michael Scharf, Eugene Tarassov, Felix Burton, Javier Montalvo Orus

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 30-Apr-2008](./Committer_Phone_Meeting_30-Apr-2008 "DSDP/TM/Committer Phone Meeting 30-Apr-2008")
*   **Skype Call Quality**
    *   Skypecast quality was OK in the beginning with up to 4 participants, but became unbearable shortly later. Rado was unable to dial into the Skypecast (sitting behind an HTTP proxy).
    *   Normal Skype conference worked very fine for all 8 participants this time, but 8 really is the limit here (9th person trying to accept invitation cannot join).

### **New Stuff**

*   Late API Change Requests
    *   We really need to draw a finishing line now!
    *   [bug 233068](https://bugs.eclipse.org/bugs/show_bug.cgi?id=233068) \- \[api\]\[breaking\] Remove tm.discovery.edit reexport of EMF -- **accepted, Martin**
    *   [bug 231209](https://bugs.eclipse.org/bugs/show_bug.cgi?id=231209) \- \[api\]\[breaking\] IRemoteFile.getSystemConnection() should be changed to IRemoteFile.getHost() -- **accepted, DaveM**
    *   [bug 230821](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230821) \- \[api\]\[breaking\] IRemoteFileSubsystem is inconsistent with IFileService -- **DaveD to investigate impact**, committers in favor of the change if doable.
    *   [bug 230919](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230919) \- \[api\]\[breaking\]\[files\] IFileService.delete() should not return a boolean -- Rado: can handle all cases with exceptions, inconvenient to do both. Martin: boolean value would hardly ever be used. Rado: Not checking return values is bad practice. Martin: It boils down to the question whether it is an error to try and delete a file that's not there. -- **accepted, Rado to make the change**
    *   [bug 212742](https://bugs.eclipse.org/bugs/show_bug.cgi?id=212742) \- \[api\] Need a Utility to send commands and receive output without prompt -- DaveM: We have RemoteCommandShellOperation with BEGIN-END-TAGS (but how reliable is it?) -- **denied**, due to lack of time
    *   Changes to go into RC2

### **Steps Towards Ganymede**

*   [DSDP/TM/3.0 Ramp down Plan for Ganymede](./3.0_Ramp_down_Plan_for_Ganymede "DSDP/TM/3.0 Ramp down Plan for Ganymede")
    *   We have RC1, so from now on EVERY checkin must be tracked in bugzilla, even simple cleanups (except documentation-only or unittest-only things). Also applies to "incubation". Rules do not apply to TCF
    *   there MUST be a +1 vote on the bug (though the vote can happen after the fact)
    *   Please do NOT only ask me for reviewing, it doesn't scale

*   **Testing**
    *   We should do another round of coordinated testing with TM 3.0 RC2 in order to find bugs important enough to get fixed
    *   Who can organize it? - **DaveD** write up wiki page, **Martin** E-mail testers

  

*   **Bug Triage**
    *   Please take the time and triage your still 3.0 assigned bugs to see which of them can be deferred to 3.0.1
    *   All "3.0" assigned bugs must be triaged now and either assigned a proper RC milestone or 3.0.1 (with the exception of Documentation-only fixes)

*   **New and Noteworthy**
    *   I'll need a list of new features for a New&Noteworthy, and for the Release Review. Release Review material is due next week.
    *   See [CDT/User/NewIn50](./CDT/User/NewIn50 "CDT/User/NewIn50") for example; for TM, I put most news into our Build Notes already, so it should be possible to compile the N&N out of the build notes
    *   For the N&N, please make screenshots and work on "your" new features, e.g.
        *   Useractions

*   **Hi-priority-bugs**
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [Hi-Priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)
    *   Current Statistics: 1 blocker (Martin), 1 critical (Martin), 10 major (DaveD, DaveM, Kevin, Martin, Michael), 20 other P2's
    *   Please fix the known hi-priority bugs as soon as possible -- best before the coordinated testing on RC2, to ensure we get good test coverage
    *   Community contributions: Only few [unapplied patches](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1) right now, should apply now if possible (see also the [Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for a query)

*   **Cleanup Work**
    *   Besides the hi-priority issues, there is a LOT of cleanup to do:
        *   New releng scripts on dsdp.eclipse.org (Martin: must-have before his vacation)
        *   Copyright Year Updates (Run the releng Copyrights Tool)
        *   API Tooling Javadocs(@noextend and friends) - [bug 227368](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227368), [bug 225529 comment 4](https://bugs.eclipse.org/bugs/show_bug.cgi?id=225529#c6) and [bug 225529 comment 6](https://bugs.eclipse.org/bugs/show_bug.cgi?id=225529#c6) \- [DSDP/TM/Code Ownership](./Code_Ownership "DSDP/TM/Code Ownership")
        *   Review and improve Userdocs; we have several open bugs here
        *   Review and improve Javadocs; lots still missing
        *   Fix broken hyperlinks in the docs, fix HTML/XML errors (which can make the indexer not work)
        *   Get rid of compiler warnings wherever possible
        *   Add more Unittests -- ideally write an accompanying unittest for every bugfix
        *   Run Findbugs -- Update site on [http://findbugs.cs.umd.edu/eclipse](http://findbugs.cs.umd.edu/eclipse), Quickdocs by Rado in [tm-dev E-Mail](http://dev.eclipse.org/mhonarc/lists/dsdp-tm-dev/msg01869.html)
            *   Question about filtering false positives posted on fb-discuss [link](https://mailman.cs.umd.edu/pipermail/findbugs-discuss/2008-May/002374.html)
    *   **TM Website:** revamp should really be complete for Ganymede! Kevin and Martin won't have time. DaveD will try to get to it, but cannot promise.

### What will happen after Ganymede?

*   Propose working on TM 3.0.1 (bugfixes only) in HEAD until fall
*   Start coming up with "Big Rocks" to address in the next cycle; re-use the [TM Future Planning](./TM_Future_Planning "TM Future Planning") page? Some examples:
    *   Connection Grouping - be Multicore aware
    *   Rewrite the Tableview to be really aware of Properties
    *   More dynamic subsystem enablement and configuration (e.g. detect UNIX vs Windows automatically at runtime)
    *   Hi-Performance, caching EFS provider
    *   Bring TCF to Maturity
    *   Quality: Add unittest coverage, reduce bloat, improve performance, streamline APIs
*   Shoot for TM 3.1 or 4.0? - DaveD: Attempt 3.1; Xuan: lots of classes moved to "internal" e.g. SystemRemoteCommand; Martin: discuss such issues on bugzilla
    *   Martin: Agree, a non-breaking release seems better; Dave: Will increase community confidence
    *   Related: Move to Java5? - DaveM: Keep Java 1.4 on the Server, allow 1.5 on the client
    *   Martin: Parallel 4.0 and 3.1 development? - DaveD: Try not to do that!

### Questions

*   **DaveD** context menu on SystemView / TeamView: something going on with the way how items are being added. Bringing up the context menu immediately after startup shows some debugger related stuff. Martin: [bug 208062](https://bugs.eclipse.org/bugs/show_bug.cgi?id=208062)

  

Vacation, away
--------------

*   Martin public holiday Thursday May 22
*   Martin NOT in Ottawa for [E4/Summit](./E4/Summit "E4/Summit") May 22-23
*   DaveD Monday May 26 public holiday in US
*   Martin vacation June 11 - 22 -- **AI Martin** finish and test the new Build scripts on dsdp.eclipse.org till then
*   DaveM vacation June 16 - 20
*   DaveD in July

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_30-Apr-2008#Action_Items "DSDP/TM/Committer Phone Meeting 30-Apr-2008") Action Items
*   **Everyone**: **Add @noextend etc** according to [DSDP/TM/Code Ownership](./Code_Ownership "DSDP/TM/Code Ownership") table;
    *   Triage 3.0 and earlier assigned bugs and move to 3.0.1 what we can
    *   Bug fixes, cleanup, unittests
*   **DaveD**: Investigate [bug 230821](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230821) exceptions in IRemoteFileSubSystem; write up coordinated testing Wiki page until Thurs May 22 evening
*   **DaveM**: Fix [bug 231209](https://bugs.eclipse.org/bugs/show_bug.cgi?id=231209) IRemoteFile.getSystemConnection()
*   **Kevin**: -
*   **Rupen**: -
*   **Xuan**: -
*   **Martin**: Fix [bug 233068](https://bugs.eclipse.org/bugs/show_bug.cgi?id=233068) Discovery reexport; Prepare Release Review material; New Project Plan; Critical EFS bugs; UI/Non-UI Splitting; Finish new Releng and tell DaveD; E-Mail potential participants of Coordinated Testing; Commons Net Placeholder CQ
*   **Javier**: Hi-PRI FTP BUGS
*   **Michael**: Terminal improvements
*   **Uwe**: -
*   **Rado**: Fix [bug 230919](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230919) IFileService.delete()
*   **Felix**: -
*   **Eugene**: -

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 28-May-2008](./Committer_Phone_Meeting_28-May-2008 "DSDP/TM/Committer Phone Meeting 28-May-2008") (1 week) at [1500 UTC / 0800 SFO / 1000 Rochester / 1100 Toronto / 1600 London / 1700 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=5&day=28&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 4-Jun-2008](./Phone_Meeting_4-Jun-2008 "DSDP/TM/Phone Meeting 4-Jun-2008") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=6&day=4&year=2008&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_21-May-2008](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_21-May-2008))