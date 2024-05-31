

DSDP/TM/Committer Phone Meeting 9-Jun-2008
==========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Monday June 9, 2008 at [1600 UTC / 0900 SFO / 1100 Rochester / 1200 Toronto / 1800 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=6&day=9&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | Martin to call everybody by Skype |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kevin.j.doyle, xuan.chen886, rupen.mardirossian, javier.montalvoorus, eugenetarassov, michael\_scharf, uwe.stieber, radoslav.gerganov, wrsfburton.  

Contents
--------

*   [1 Invited Attendees](#Invited-Attendees)
*   [2 Agenda](#Agenda)
    *   [2.1 **New Stuff**](#New-Stuff)
    *   [2.2 **Hot Bugs being discussed**](#Hot-Bugs-being-discussed)
    *   [2.3 **Plan for Next Steps**](#Plan-for-Next-Steps)
    *   [2.4 Questions](#Questions)
    *   [2.5 **Old Stuff**](#Old-Stuff)
*   [3 Vacation, away](#Vacation.2C-away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Invited Attendees
-----------------

*   IBM - Xuan Chen, Dave McKnight, Dave Dykstal, Rupen Mardirossian, Kevin Doyle
*   Wind River - Martin Oberhuber, Michael Scharf, Uwe Stieber, Eugene Tarassov, Felix Burton
*   Symbian - Javier Montalvo Orus
*   ProSyst - Radoslav Gerganov
*   MontaVista - Anna Dushistova

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Agenda
------

*   Last meeting: [DSDP/TM/Committer Phone Meeting 5-Jun-2008](./Committer_Phone_Meeting_5-Jun-2008 "DSDP/TM/Committer Phone Meeting 5-Jun-2008")
*   **Skype Call Quality**
*   **Welcome Anna!**

### **New Stuff**

*   [DSDP/TM/3.0 Ramp down Plan for Ganymede](./3.0_Ramp_down_Plan_for_Ganymede "DSDP/TM/3.0 Ramp down Plan for Ganymede")
    *   We have RC3, so from now on EVERY checkin must get a **+1 by two reviewers BEFORE** (except emergencies, documentation-only or unittest-only things). Also applies to "incubation". Rules do not apply to TCF
    *   Please do NOT only ask me for reviewing, it doesn't scale

*   [TM 3.0 RC2 Testing](./TM_3.0_RC2_Testing "TM 3.0 RC2 Testing") Status (as per yesterday's E-Mail)
    *   Test Configurations -- especially for [bug 231453](https://bugs.eclipse.org/bugs/show_bug.cgi?id=231453) from cross-project list
        *   TM installed into Eclipse 3.4 dropins/ -- That's what we always do
        *   TM installed into Eclipse 3.3. -- Martin has target platform against 3.3 now
        *   TM as part of the JEE Package -- **AI DaveD**, or Kevin; **AI Martin** tell Dave when JEE has TM RC3
        *   TM initial install from TM Update Site -- Martin
        *   **Ganymede** TM initial install from Ganymede --
            *   Dependencies: When Remotecdt / Discovery selected, CDT / EMF must be installed automatically
            *   DaveD: Quicktest on official Ganymede Site with RC2 (today), RC3 again when available
        *   **Update Scenarios**
            *   Updating 3.0 to 3.0.1 -- referencing TM site, not Gany site -- 3.0RC3 to I-build -- **AI Martin**
            *   Updating TM 2.0 to 3.0 -- Eclipse 3.3/TM 2.0 (including discovery, cdt), use TM 3.0 update site, update to TM 3.0 -- **AI Martin**

*   *   Test Areas
        *   Connection Import / Export -- **AI Xuan**
        *   Documentation: Correct hyperlinks
        *   Feature Versions, About Files, ...

### **Hot Bugs being discussed**

*   [bug 233461](https://bugs.eclipse.org/bugs/show_bug.cgi?id=233461) Refresh expanded Folders -- IFileService#list to return children and parent in one step, how to be API compatible?
    *   DaveM: Not in favor of changing API, don't expect getFile() to be expensive, Cache in Service Layer. Against explicit API change. Plain semantic change is the least of the evils.
    *   Martin against Caching on Service Layer.
    *   Original bug as specified must be fixed - want the fix in there as soon as possible, because it fixes IRemoteFile problems
    *   **AI Martin** can easily adapt unittests to run performance metrics
    *   Split up the bug: Original [bug 233461](https://bugs.eclipse.org/bugs/show_bug.cgi?id=233461) for the original problem only, include a small patch WITHOUT API change but with unittests. Create a new bug for the API Changes / Preformance Improvements, with the 2nd part of the patch. Discuss API separately. Original bug to be committed into an I-build today. **AI Martin and Dave** to hook up on Skype later today.
*   [bug 235600](https://bugs.eclipse.org/bugs/show_bug.cgi?id=235600) Downrev ftp, local, ssh, telnet features to 2.1.0 was intentional!
*   [bug 235221](https://bugs.eclipse.org/bugs/show_bug.cgi?id=235221) Files truncated on exit of Eclipse -- **AI DaveD** prioritize bug
*   [bug 199596](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199596) \[refresh\]\[ftp\] Changing a file/folder's Read-Only attribute doesn't always update IRemoteFile -- is it fixed now? -- patch not yet committed?
*   [bug 234038](https://bugs.eclipse.org/bugs/show_bug.cgi?id=234038) \[files\]\[refresh\] Changing file permissions does not update property sheet or refresh tree -- is it fixed? -- patch not yet committed? -- **AI DaveM** create new bug for Tableview
*   [bug 235145](https://bugs.eclipse.org/bugs/show_bug.cgi?id=235145) Remove Create Project Action -- DaveD: Document the process of creating a remote project, but get rid of the action? - Martin: See FAQ,
    *   Decision: Action is not ready for products, therefore remove it now or allow to programmatically disable it
*   [bug 234026](https://bugs.eclipse.org/bugs/show_bug.cgi?id=234026) \[apidoc\] IFileService#createFolder() does not specify whether parent folders are created
    *   Update Service Docs and Impl to make the Service create parent folders
*   [bug 227750](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227750) \[efs\]\[regression\] Eclipse with RSE 3.0 don't start or Display problems -- DaveD: Sounds like should be deferred to 3.1
*   [bug 230917](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230917) \[regression\] Some DStore Archive Testcases fail -- **AI Xuan** look at, probably move to 3.0.1 during weekend

### **Plan for Next Steps**

*   **Bug Triage**
    *   **AI Everyone** **must review your assigned bugs** and move to 3.0.1 where possible
    *   All "3.0" assigned bugs must be triaged now and either assigned a proper RC milestone or 3.0.1 (with the exception of Documentation-only fixes)
    *   Work on remaining ones by priority
    *   [Open RC2 Assigned](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&target_milestone=3.0+M5&target_milestone=3.0+M6&target_milestone=3.0+M7&target_milestone=3.0+RC1&target_milestone=3.0+RC2&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) bugs, [open 3.0 Assigned](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&target_milestone=3.0+RC2&target_milestone=3.0+RC3&target_milestone=3.0+RC4&target_milestone=3.0&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) bugs
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [Hi-Priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)
    *   Current Statistics: 1 blocker (Martin), 1 critical (Martin), 8 major (DaveD, Kevin, Martin, Michael), 23 other P2's -- was 10 major / 20 P2's last week
    *   Community contributions: Only few [unapplied patches](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1) right now, last chance to apply now before 3.0 (see also the [Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for a query)

*   Martin's new Build System for Dave
    *   In the works

*   **New and Noteworthy**
    *   I'll need a list of new features for a New&Noteworthy, and for the Release Review. Release Review material is due next week.
    *   See [CDT/User/NewIn50](https://wiki.eclipse.org/CDT/User/NewIn50 "CDT/User/NewIn50") for example; for TM, I put most news into our Build Notes already, so it should be possible to compile the N&N out of the build notes
    *   For the N&N, please make screenshots and work on "your" new features, e.g.
        *   Useractions

*   **Cleanup Work**
    *   Besides the hi-priority issues, there is a LOT of cleanup to do. What do we consider must-have's?
        *   Unittests, unittests, unittests!
        *   **New releng scripts** on dsdp.eclipse.org (Martin: must-have before his vacation)
        *   **Copyright Year Updates** (Run the releng Copyrights Tool)
        *   Migration Notes (for 2.0 / for 1.0?)
        *   API Tooling Javadocs(@noextend and friends) - [bug 227368](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227368), [bug 225529 comment 4](https://bugs.eclipse.org/bugs/show_bug.cgi?id=225529#c6) and [bug 225529 comment 6](https://bugs.eclipse.org/bugs/show_bug.cgi?id=225529#c6) \- [DSDP/TM/Code Ownership](./Code_Ownership "DSDP/TM/Code Ownership")
        *   Review and improve Userdocs; we have several open bugs here
        *   Review and improve Javadocs; lots still missing, unclear, duplicated
        *   Fix broken hyperlinks in the docs, fix HTML/XML errors (which can make the indexer not work)
        *   Get rid of compiler warnings wherever possible
        *   Add more Unittests -- ideally write an accompanying unittest for every bugfix
        *   Run Findbugs -- Update site on [http://findbugs.cs.umd.edu/eclipse](http://findbugs.cs.umd.edu/eclipse), Quickdocs by Rado in [tm-dev E-Mail](http://dev.eclipse.org/mhonarc/lists/dsdp-tm-dev/msg01869.html)
            *   Question about filtering false positives posted on fb-discuss [link](https://mailman.cs.umd.edu/pipermail/findbugs-discuss/2008-May/002374.html)
    *   **TM Website:** revamp should really be complete for Ganymede! Kevin and Martin won't have time. DaveD will try to get to it, but cannot promise.

  

### Questions

*   **DaveD** context menu on SystemView / TeamView: something going on with the way how items are being added. Bringing up the context menu immediately after startup shows some debugger related stuff. Martin: [bug 208062](https://bugs.eclipse.org/bugs/show_bug.cgi?id=208062)

### **Old Stuff**

*   **Unit Tests** \- next priority after API
*   Migrating to new Releng on dsdp.eclipse.org (adopt P2, nightly tests, signing etc)

*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

*   **Quality, Backlog and Unit Tests**
    *   Remember our 2-fix-per-week / 3 unittests-per-milestone plan
    *   Current situation is on [this bugzilla report](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=&y_axis_field=assigned_to&z_axis_field=&query_format=report-table&classification=DSDP&product=Target+Management&bug_status=RESOLVED&bug_status=VERIFIED&bug_status=CLOSED&chfieldfrom=2007-09-17&chfieldto=Now&chfield=bug_status&chfieldvalue=RESOLVED&format=table&action=wrap&negate0=1&field0-0-0=resolution&type0-0-0=equals&value0-0-0=DUPLICATE)

Vacation, away
--------------

*   Martin vacation June 11 - 22 -- **AI Martin** finish and test the new Build scripts on dsdp.eclipse.org till then
*   DaveM vacation June 16 - 20
*   DaveD in July

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_5-Jun-2008#Action_Items "DSDP/TM/Committer Phone Meeting 5-Jun-2008") Action Items
*   **Everyone**:
    *   Triage 3.0 and earlier assigned bugs and move to 3.0.1 / 3.1 what we can
    *   **Add @noextend etc** according to [DSDP/TM/Code Ownership](./Code_Ownership "DSDP/TM/Code Ownership") table;
    *   Update the New&Noteworthy (Martin will send a separate E-Mail)
    *   Bug fixes, cleanup, unittests
*   **DaveD**: Test initial install of RC2 from Ganymede (CDT, EMF dependencies!); Test JEE package (when available as RC3); Prioritize [bug 235221](https://bugs.eclipse.org/bugs/show_bug.cgi?id=235221); Commit [bug 234215](https://bugs.eclipse.org/bugs/show_bug.cgi?id=234215); Prepare EFS Userdocs along the lines of [TM and RSE FAQ#Why is the Outline View empty when editing a remote PHP or C file?](./TM_and_RSE_FAQ#Why_is_the_Outline_View_empty_when_editing_a_remote_PHP_or_C_file.3F "TM and RSE FAQ")
*   **DaveM**: Commit [bug 199596](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199596), [bug 234038](https://bugs.eclipse.org/bugs/show_bug.cgi?id=234038); File new bug for tableview issue; work with Martin on [bug 233461](https://bugs.eclipse.org/bugs/show_bug.cgi?id=233461); [bug 233480](https://bugs.eclipse.org/bugs/show_bug.cgi?id=233480) \- tell the team to use custom newConnectionWizards extension
*   **Kevin**: -
*   **Rupen**: -
*   **Xuan**: Text Import/Export; Look at [bug 230917](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230917) Archive Handler Unittests
*   **Martin**: Run performance tests for [bug 233461](https://bugs.eclipse.org/bugs/show_bug.cgi?id=233461); Test 2.0->3.0 Update; Tell DaveD when JEE RC3 is ready; Prepare I-build for [bug 233461](https://bugs.eclipse.org/bugs/show_bug.cgi?id=233461) when done; Update Project Plan; File new bug for [bug 165171](https://bugs.eclipse.org/bugs/show_bug.cgi?id=165171); Critical EFS bugs; Finish new Releng and tell DaveD; Get started on New&Noteworthy; Create an initial 3.1 plan
*   **Javier**: Hi-PRI FTP BUGS
*   **Michael**: Terminal: Try to fix [bug 185348](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185348), [bug 204796](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204796)
*   **Uwe**: -
*   **Rado**: -
*   **Felix**: -
*   **Eugene**: -

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 25-Jun-2008](./Committer_Phone_Meeting_25-Jun-2008 "DSDP/TM/Committer Phone Meeting 25-Jun-2008") at [1500 UTC / 0800 SFO / 1000 Rochester / 1100 Toronto / 1700 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=6&day=25&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 2-Jul-2008](./Phone_Meeting_2-Jul-2008 "DSDP/TM/Phone Meeting 2-Jul-2008") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=7&day=2&year=2008&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_9-Jun-2008](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_9-Jun-2008))