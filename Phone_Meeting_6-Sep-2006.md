

DSDP/TM/Phone Meeting 6-Sep-2006
================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Wednesday [September 6, 2006](./index.php?title=September_6,_2006&action=edit&redlink=1 "September 6, 2006 (page does not exist)") at 9am PST |
| Primary International Dial-in: | **+44 (0)1452 567588** |
| USA Freephone Dial-In: | +1 (866) 6161738 |
| UK National Dial-In: | 08712460713 |
| Passcode: | **0587322148 #** |

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Meeting Notes](#Meeting-Notes)
*   [3 Action Items to Review](#Action-Items-to-Review)
*   [4 New Action Items](#New-Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   Wind River - Doug Gaff, Martin Oberhuber, Ted Williams, Michael Scharf
*   IBM - Dave Dykstal, Dave McKnight
*   LANL / PTP Project - Greg Watson
*   QNX - Doug Schaefer
*   Symbian - Javier Montalvo
*   ARM - Anthony Berent
*   TI - Dobrin Alexey

Meeting Notes
-------------

*   Update on RSE Status
    *   Downloads as per 5-Sep-2006:
        *   144 RSE-SDK-1.0M4, 41 rseserver-windows, 23 rseserver-linux; 8 unix, 5 aix, 3 macos;
        *   50 from the update site (includes 47 dstore, 46 local, 46 ftp, 45 ssh, 32 SDK)
        *   **Total 194 downloads of RSE!**
    *   [Project Plan](https://www.eclipse.org/dsdp/tm/development/plan.php) status
        *   Docs are now online on the infocenter at [http://dsdp.eclipse.org/help/latest/](http://dsdp.eclipse.org/help/latest/)
        *   Getting the latest RSE is now easy by using the update site at [http://download.eclipse.org/dsdp/tm/updates/](http://download.eclipse.org/dsdp/tm/updates/)
        *   A tutorial is now part of the docs / [https://www.eclipse.org/dsdp/tm/tutorial/](https://www.eclipse.org/dsdp/tm/tutorial/)
        *   [JUnit framework](https://bugs.eclipse.org/bugs/show_bug.cgi?id=149080) passed EMO review
        *   Working on Code Cleanups ([Compiler warnings](https://bugs.eclipse.org/bugs/show_bug.cgi?id=149080), Javadoc fixes, ...) and [bug fixes](https://www.eclipse.org/dsdp/tm/development/bug_process.php)
        *   **Recent refactorings** \- see Build Notes of recent nightly builds on [http://download.eclipse.org/dsdp/tm/downloads/](http://download.eclipse.org/dsdp/tm/downloads/)
        *   Release Review is scheduled for [27-Sep-2006, 8:00 PST](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=9&day=27&hour=15&min=0&sec=0&p1=224&p2=421&p3=250&p4=136&p5=223). We might need TM advocates to join and say "yes"
            *   See [Eclipse.org-committers announcement](http://dev.eclipse.org/mhonarc/lists/eclipse.org-committers/msg00236.html) for dialin numbers:
            *   866-362-7064 or 613-287-8000, participant passcode 874551#
    *   What's behind schedule
        *   CDT Launcher
        *   Jakarta commons-net - EMO approval still pending
        *   JUnit tests - due to slow legal approval, we now have a framework but no tests yet
    *   What's being added in addition to the plan
        *   Initial version of Discovery passed review, to be checked in tomorrow, get it through the [rse-anonymous.psf](https://www.eclipse.org/dsdp/tm/development/rse-anonymous.psf) project set
        *   Wind River got its [Terminal View](https://bugs.eclipse.org/bugs/show_bug.cgi?id=152826) through EMO Review
        *   EFS plugin to be added as "experimental technology preview"
        *   Going to join Europa Simultaneous Release
    *   **Community's most wanted - who's working on what?**
        *   Montavista - ssh processes subsystem?
        *   [Wicked Shell](http://eclipse-plugins.info/eclipse/plugin_details.jsp?id=1392)
        *   Mac support: Quite a few fixed, few remaining
        *   Questions? Requests? - none right now
*   **Sign up for testing!**
    *   After M5, we need people to walk through the test plans on various different host/target combinations
    *   Official test period will start with M5 as RC0 candidate; RC1 will be 2 weeks after, RC2 1 week after
    *   Please sign up in the [RSE 1.0 Testing](./RSE_1.0_Testing "RSE 1.0 Testing") page
    *   Testing M5 early just takes 2 hour or so -- we need those bugs early!
*   Communications
    *   Please fill in [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning")
    *   Collaborations with other projects (Platform/Team, PTP, CDT, TPTP, WTP, ECF, Aperi, g-Eclipse)
        *   Greg (PTP) has some loose connection, the focus is quite different; EFS
*   **Technology sub-groups**
    *   CDT Launching (Ewa)
    *   Update on [SPIRIT](./DD/Spirit "DSDP/DD/Spirit") (Anthony)
        *   [Spirit DWG Kick-off Meeting](http://dev.eclipse.org/mhonarc/lists/dsdp-dd-dev/msg00395.html) \- [Sept 13, 4-6pm UK, 11-1pm EDT](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=9&day=13&hour=15&min=0&sec=0&p1=224&p2=43&p3=223&p4=136)
        *   Anthony is doing some work on an Eclipse-based SPIRIT editor that they intend to open source. Both are experimental and not ready for contribution.
    *   Update on [Autodetect](./Autodetect "DSDP/TM/Autodetect") (Javier)
        *   To be committed tomorrow into org.eclipse.tm.core/discovery

Action Items to Review
----------------------

*   Last meeting: [DSDP/TM/Phone Meeting 2-Aug-2006](./Phone_Meeting_2-Aug-2006 "DSDP/TM/Phone Meeting 2-Aug-2006")

New Action Items
----------------

*   Everybody - Sign up on the [RSE 1.0 Testing](./RSE_1.0_Testing "RSE 1.0 Testing") page
*   Everybody - Review and edit the [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") page

Next Meeting
------------

*   Release Review on [27-Sep-2006, 8:00 PST](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2006&month=9&day=27&hour=15&min=0&sec=0&p1=224&p2=421&p3=250&p4=136&p5=223) (wednesday, 3 weeks)
*   Next [DSDP/TM/Phone Meeting 4-Oct-2006](./Phone_Meeting_4-Oct-2006 "DSDP/TM/Phone Meeting 4-Oct-2006") (wednesday, 4 weeks)
*   Michael Scharf is doing a [Talk on TM/RSE](http://www.eclipsecon.org/summiteurope2006/index.php?page=detail/&id=25) on Wednesday, Oct. 11 at [Eclipse Summit Europe](http://www.eclipsecon.org/summiteurope2006)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_6-Sep-2006](https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_6-Sep-2006))