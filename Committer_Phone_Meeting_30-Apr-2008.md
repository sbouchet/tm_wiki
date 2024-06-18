

DSDP/TM/Committer Phone Meeting 30-Apr-2008
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday Apr 30, 2008 at [1500 UTC / 0800 SFO / 1000 Rochester / 1100 Toronto / 1600 London / 1700 Barcelona+Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=4&day=30&hour=15&min=0&sec=0&p1=224&p2=159&p3=250&p4=31&p5=223&iv=1800) |
| Dial-in: | Martin to call everybody by Skype |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kevin.j.doyle, xuan.chen886, rupen.mardirossian, javier.montalvoorus, eugenetarassov, michael\_scharf, uwe.stieber, radoslav.gerganov, wrsfburton.  

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 **New Stuff**](#New-Stuff)
    *   [2.2 Committer Status and Report](#Committer-Status-and-Report)
*   [3 Vacation, away](#Vacation.2C-away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   IBM - Dave McKnight, Dave Dykstal, Rupen Mardirossian
*   Wind River - Martin Oberhuber, Felix Burton
*   ProSyst - Radoslav Gerganov

Committers not at the call today

*   Kevin, Xuan, Michael, Uwe, Eugene, Javier

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 16-Apr-2008](./Committer_Phone_Meeting_16-Apr-2008 "DSDP/TM/Committer Phone Meeting 16-Apr-2008")
*   **Skype Call Quality**
    *   Bad this time, as soon as more than 3 participants. Martin had started the conf via ADSL from home, limited bandwidth was likely the reason -- looks like the meeting organizer needs lots of bandwidth. Fell back to fixed line, Rado used Skype into the 800 conf number successfully.

### **New Stuff**

*   Welcome new Committers - **Felix**, **Rado**
*   [DSDP/TM/3.0 Ramp down Plan for Ganymede](./3.0_Ramp_down_Plan_for_Ganymede "DSDP/TM/3.0 Ramp down Plan for Ganymede") \- **AI Everyone** Review again and comment on dsdp-tm-dev if any questions.
*   Committers be bold and self-confident
*   IP due diligence: "contributed" keyword and tm-log.csv; target milestone - **AI DaveD** update tm-log.csv for rupe. **AI DaveM** add contributed kwd.
*   Javadoc API Tooling API Comments (@noextend and friends) - [bug 227368](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227368), [bug 225529 comment 4](https://bugs.eclipse.org/bugs/show_bug.cgi?id=225529#c6) and [bug 225529 comment 6](https://bugs.eclipse.org/bugs/show_bug.cgi?id=225529#c6) \- **AI Martin** Extract Eclipse SDK onto dsdp.eclipse.org and post the link; **AI Martin** post where to find textual paragraph form "method extend" variant.
*   [bug 227213](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227213) Folder duplication by dragging to parent folder - "Duplicate Of" or Rename? - Need consensus and Owner
    *   Rupen: automatically do "Copy of" because in case of multiselect, users would get n dialogs asking for rename/overwrite
    *   Martin: Should try to auto-select the generated copies such that users can delete easily in case the copy happened unintentionally
    *   DaveM: Be Consistent with Eclipse Workspace ("Copy of")
    *   **Decision to use "Copy of" approach. Rupen has a working prototype.** AI Rupen **attach patch**
*   [PII Bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&product=Target+Management&keywords_type=allwords&keywords=pii&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit) till May 8
*   Hi-pri-bugs; community contributions; apply [patches](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=attachments.ispatch&type0-0-0=equals&value0-0-0=1) (see also the [Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for a query)
    *   **AI Martin** mark Rado's bug fixed

### Committer Status and Report

*   **DaveD** -
    *   [bug 189274](https://bugs.eclipse.org/bugs/show_bug.cgi?id=189274) Import/export connections - this enhancement is finished, but may need some tweaking as it is used.
    *   [bug 226561](https://bugs.eclipse.org/bugs/show_bug.cgi?id=226561) Should finish up with marking today. Will then pass bug report to someone else.
*   **DaveM:** -
*   **Martin:** \- GSoC student Takuya Miyamoto for [bug 185925](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185925)
*   **Rupen:** -
*   **Rado:** -
*   **Felix:** -
*   **Questions**

*   **Bugzilla**:
    *   [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, away
--------------

*   MartinO public holiday Thurs May 1; in Ottawa for [E4/Summit](https://wiki.eclipse.org/E4/Summit "E4/Summit") May 22-23 .. want to meet in Toronto?
*   Rupen May 8-15
*   MartinO vacation June 11 - 22
*   DaveM vacation June 16 - 20
*   DaveD in July -- **AI Martin** finish and test the new Build scripts on dsdp.eclipse.org till then

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_9-Apr-2008#Action_Items "DSDP/TM/Committer Phone Meeting 9-Apr-2008") Action Items
*   **Everyone**: **Fix PII Issues**; **Add @noextend etc** according to [DSDP/TM/Code Ownership](./Code_Ownership "DSDP/TM/Code Ownership") table; Review [DSDP/TM/3.0 Ramp down Plan for Ganymede](./3.0_Ramp_down_Plan_for_Ganymede "DSDP/TM/3.0 Ramp down Plan for Ganymede")
*   **DaveD**: Merge Rupens patches; Update [bug 221211](https://bugs.eclipse.org/bugs/show_bug.cgi?id=221211) IFileService multi-commands Javadoc
*   **DaveM**: create a new "Future" bug for dstore protocol handshake, cloned from [bug 220892](https://bugs.eclipse.org/bugs/show_bug.cgi?id=220892)
*   **Kevin**: Website Updates
*   **Rupen**: Attach prototype patch for [bug 227213](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227213)
*   **Xuan**: Upgrade Skype to fix quality issues; Use Kevin's Properties for Unit Tests
*   **Martin**: New Project Plan; Commons Net Placeholder CQ; UI/Non-UI Splitting; finish new releng; Look at PropertyDescriptor issues; unit tests
*   **Javier**: add unit tests; document the Symbian internal test setup similar to [CVS](https://bugs.eclipse.org/bugs/show_bug.cgi?id=204138#c20) \-\- see also [CVS_Development#Testing](https://wiki.eclipse.org/CVS_Development#Testing "CVS Development")
*   **Michael**: Terminal improvements
*   **Uwe**:
*   **Rado**:
*   **Felix**:

Next Meeting
------------

*   Monthly [DSDP/TM/Phone Meeting 7-May-2008](./Phone_Meeting_7-May-2008 "DSDP/TM/Phone Meeting 7-May-2008") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=5&day=7&year=2008&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Committer Phone Meeting 14-May-2008](./Committer_Phone_Meeting_14-May-2008 "DSDP/TM/Committer Phone Meeting 14-May-2008") (2 weeks) at [1500 UTC / 0800 SFO / 1000 Rochester / 1100 Toronto / 1600 London / 1700 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=5&day=14&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_30-Apr-2008](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_30-Apr-2008))