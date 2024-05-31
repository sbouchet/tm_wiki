

DSDP/TM/Committer Phone Meeting 16-Jul-2008
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Wednesday [July 16, 2008](./index.php?title=July_16,_2008&action=edit&redlink=1 "July 16, 2008 (page does not exist)") at [1600 UTC / 0900 SFO / 1100 Rochester / 1200 Toronto / 1800 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=7&day=16&hour=16&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | Martin to call everybody by Skype |

Backup dial-in: International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713** / Passcode: **0587322148 #**

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype dial-in: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kevin.j.doyle, xuan.chen886, rupen.mardirossian, javier.montalvoorus, eugenetarassov, michael\_scharf, uwe.stieber, radoslav.gerganov, wrsfburton.  

Contents
--------

*   [1 Invited Attendees](#Invited-Attendees)
*   [2 Attendees](#Attendees)
*   [3 Notes](#Notes)
    *   [3.1 **New Stuff**](#New-Stuff)
*   [4 Vacation, away](#Vacation.2C-away)
*   [5 Action Items](#Action-Items)
*   [6 Next Meeting](#Next-Meeting)

Invited Attendees
-----------------

*   IBM - Xuan Chen, Dave McKnight, Dave Dykstal, Kevin Doyle
*   Wind River - Martin Oberhuber, Michael Scharf, Uwe Stieber, Eugene Tarassov, Felix Burton
*   ProSyst - Radoslav Gerganov
*   MontaVista - Anna Dushistova

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Attendees
---------

*   Attendees: Martin, Uwe, DaveM, Kevin, Xuan
*   Regrets: Anna, DaveD, Rado, Michael, Eugene, Felix

Notes
-----

*   Last meeting: [DSDP/TM/Phone Meeting 2-Jul-2008](./Phone_Meeting_2-Jul-2008 "DSDP/TM/Phone Meeting 2-Jul-2008")
*   Prev meeting: [DSDP/TM/Committer Phone Meeting 9-Jun-2008](./Committer_Phone_Meeting_9-Jun-2008 "DSDP/TM/Committer Phone Meeting 9-Jun-2008")
*   **Skype Call Quality**

### **New Stuff**

*   [bug 240991](https://bugs.eclipse.org/bugs/show_bug.cgi?id=240991) Startup creates Display on Worker Thread
    *   DaveM: RSEUIPlugin.start() is not on the Main thread! Seems to be reproducable when Eclipse is "Restarted" rather than "Started". Issue is hit because Logger is instantiated from RSEUIPlugin.start(), registers Preference / ModelChangeEvent, which leads to DaveD's workaround for [bug 227750](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227750) to fail
    *   Martin: How is the backtrace (Restart) created? Even the intended fix (using a non-UI IRSEInteractionProvider) would not fix this
    *   Uwe: Swing/SWT Integration? Is any plugin directly using Bundle.loadClass? That's dangerous since it changes the startlevel
    *   Martin: Could instantiation of the Logger be deferred from RSEUIPlugin.start() to somewhere else (later)?
    *   People are concerned about using Display.getDefault() -- using IWorkbench.getDisplay() is recommended instead (or, use PlatformUI.isWorkbenchRunning())
    *   **AI DaveM** Comment on Bugzilla what is done in the debuggee to get the backtrace on StartLevelEventThread (Martin cannot reproduce)
    *   **AI DaveM** Try to instantiate the Logger later, or at least try deferring addition of the ModelChangeListeners
    *   **AI Martin** Write the real fix (interaction providers) mid August

*   [bug 240998](https://bugs.eclipse.org/bugs/show_bug.cgi?id=240998) Extension Point for User Actions
    *   Kevin: EP used to add compile commands -- will eventually want to get rid of this extension point, will look at workarounds - **AI Kevin** mark bug as INVALID or WONTFIX

*   [bug 238574](https://bugs.eclipse.org/bugs/show_bug.cgi?id=238574) **Website Revamp**
    *   **AI Martin** ask the Community (Remy, Nick)

*   Unittests
    *   Martin added "soft disable" capability for Unittests -- when writing new tests, please add the if(isTestDisabled()) return;
    *   Multi-Target: RSEFileStoreTest and FileServiceTest;
    *   Xuan: Kevin trying some Abbot stuff, might contribute -- Abbot is under CPL
    *   **AI Martin** New build driver -- deadline Jul/31
    *   Xuan: Want to release themselves
        *   **AI Martin** Add M-build Cronjob for Tue 0600 Ottawa time
        *   Relengtool: [Download](http://download.eclipse.org/eclipse/downloads/drops/R-3.4-200806172000/index.php#org.eclipse.releng)
        *   **AI Xuan** Release yourself - Process: Select plugins to release, right-click > Team > Release **Be sure to not release inconsistent stuff**, i.e. fixes that depend on other stuff that you're not releasing
    *   [bug 230917](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230917) \[regression\] Some DStore Archive Testcases fail -- **AI Xuan** look at
    *   New Build System due Jul 31 (**AI Martin**)

*   Findbugs and other cleanup
    *   Broken Links in Docs: Xenu's LinkSleuth
    *   Xuan: DVT, [bug 240940](https://bugs.eclipse.org/bugs/show_bug.cgi?id=240940), [bug 240972](https://bugs.eclipse.org/bugs/show_bug.cgi?id=240972) high priority fixes - **AI DaveM** address

*   3.1 Plan
    *   Martin marked some bugzilla items with "plan" keyword
    *   **AI Everyone** attach "plan" keyword to "interesting" i.e. larger or important bugs, until end July
    *   DSDP presentation to the Board on Sep 17, IBM wants to review the draft, **AI Martin** check, **AI Xuan** check deadline

Vacation, away
--------------

*   Martin vacation Jul 21-22, on and off on Thurs and Fri Jul 17-18
*   DaveM vacation first week of August
*   DaveD in July
*   Anna in July

Action Items
------------

*   [Last Meeting](#Notes) Action Items
*   **Everyone**: attach "plan" keyword to "interesting" bugs for 3.1 **until end July**
*   **Anna**:
*   **DaveD**:
*   **DaveM**: [bug 240991](https://bugs.eclipse.org/bugs/show_bug.cgi?id=240991): comment on bug how the backtrace is created in the debugger, try registering logger events later; DVT [bug 240940](https://bugs.eclipse.org/bugs/show_bug.cgi?id=240940), [bug 240972](https://bugs.eclipse.org/bugs/show_bug.cgi?id=240972) fix; **old:** commit [bug 199596](https://bugs.eclipse.org/bugs/show_bug.cgi?id=199596); [bug 233480](https://bugs.eclipse.org/bugs/show_bug.cgi?id=233480) \- tell the team to use custom newConnectionWizards extension
*   **Kevin**: [bug 240998](https://bugs.eclipse.org/bugs/show_bug.cgi?id=240998) compile commands extension point mark INVALID or WONTFIX
*   **Xuan**: Get Releng tool and release fixes yourself for bi-weekly M-builds; check deadline for PMC Board Presentation review; **old** Look at [bug 230917](https://bugs.eclipse.org/bugs/show_bug.cgi?id=230917) Archive Handler Unittests
*   **Martin**: Cronjob for Tue 0600 M-builds; [bug 238574](https://bugs.eclipse.org/bugs/show_bug.cgi?id=238574) Website ask for Community Help; new Builder **until end July**; [bug 227750](https://bugs.eclipse.org/bugs/show_bug.cgi?id=227750) Display in non-UI write fix **until mid August**; **old** Run performance tests for [bug 233461](https://bugs.eclipse.org/bugs/show_bug.cgi?id=233461); Test 2.0->3.0 Update; Update Project Plan; File new bug for [bug 165171](https://bugs.eclipse.org/bugs/show_bug.cgi?id=165171); Critical EFS bugs; Finish new Releng and tell DaveD; Get started on New&Noteworthy; Create an initial 3.1 plan
*   **Javier**: Hi-PRI FTP BUGS
*   **Michael**: Terminal: Work on [bug 185348](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185348) Terminal API
*   **Uwe**: -
*   **Rado**: -
*   **Felix**: -
*   **Eugene**: -

Next Meeting
------------

*   Monthly [DSDP/TM/Phone Meeting 6-Aug-2008](./Phone_Meeting_6-Aug-2008 "DSDP/TM/Phone Meeting 6-Aug-2008") (3 weeks) at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=8&day=6&year=2008&hour=16&min=00&sec=0&p1=0)
*   [DSDP/TM/Committer Phone Meeting 20-Aug-2008](./Committer_Phone_Meeting_20-Aug-2008 "DSDP/TM/Committer Phone Meeting 20-Aug-2008") (5 weeks) at [1500 UTC / 0800 SFO / 1000 Rochester / 1100 Toronto / 1700 Salzburg](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2008&month=8&day=20&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_16-Jul-2008](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_16-Jul-2008))