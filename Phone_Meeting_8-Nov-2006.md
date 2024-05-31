

DSDP/TM/Phone Meeting 8-Nov-2006
================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

Dial-in numbers and passcodes have changed for this call only. We'll revert to our regular numbers next month.

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Wednesday [November 8, 2006](./index.php?title=November_8,_2006&action=edit&redlink=1 "November 8, 2006 (page does not exist)") at [1700 UTC / 9am PST](http://www.timeanddate.com/worldclock/fixedtime.html?month=11&day=8&year=2006&hour=17&min=00&sec=0&p1=0) |
| International Dial-in | **+1 314 655 1411** |
| North American Dial-In | **+1 877 422 0035** |
| Passcode: | **764918#** |

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
    *   [2.1 Recent Download Statistics](#Recent-Download-Statistics)
    *   [2.2 Update on RSE Status](#Update-on-RSE-Status)
        *   [2.2.1 Documentation: Which are the best places to start with?](#Documentation:-Which-are-the-best-places-to-start-with.3F)
    *   [2.3 Motorola - Christian Kurzke](#Motorola---Christian-Kurzke)
    *   [2.4 Community's most wanted - who's working on what?](#Community.27s-most-wanted---who.27s-working-on-what.3F)
    *   [2.5 Communications](#Communications)
*   [3 Action Items to Review](#Action-Items-to-Review)
*   [4 New Action Items](#New-Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   Wind River - Martin Oberhuber, Ted Williams, Michael Scharf
*   IBM - Dave McKnight, Dave Dykstal
*   Symbian - Javier Montalvo
*   Motorola - Christian Kurzke, Ruth Soliani, Maureen Brenner

Agenda
------

### Recent Download Statistics

RSE 1.0 Download statistics as per 7-Nov-2006
| Component | M4 | M5 | RC1 | RC2 | RC3 | RC4 |
| --- | --- | --- | --- | --- | --- | --- |
| Date | 18-Aug | 22-Sep | 08-Oct | 20-Oct | 30-Oct | 03-Nov |
| RSE-SDK | 4 | 38 | 164 | 177 | 113 | 68 |
| rseserver-windows | 1 | 11 | 70 | 62 | 24 | 34 |
| rseserver-linux | 1 | 6 | 39 | 28 | 19 | 9 |
| rse.core (Update Site) |  |  | 66 | 46 | 72 | 28 |
| Total |  |  | 230 | 223 | 185 |  |

*   Download Statistics Analysis
    *   RC1 was just after the "getting mature" blog (18-Sep)
    *   RC2 was just after the "release test" blog (11-Oct); also, 20-Oct was the originally planned release date
    *   Most people still prefer the SDK, although the update site is gaining momentum
        *   On the update site, 60% get the .jar.pack.gz but 40 % get the .jar file
    *   Looking at RC1, Grouping by country is:
        *   RSE-SDK: Germany=38, China=26, US=25, France=10, Canada=8, Turkey=7, Austria=6
        *   Update Site: US=23, France=10, Sweden=4, Austria=3 China=3, Denkmark=3, Germany=3, Italy=3
        *   rseserver: Germany=20, US=19, China=7, France=6, Belgium=6

### Update on RSE Status

*   All blockers towards RSE 1.0 resolved finally - about files review finally done by emo
*   New TM FAQ on [TM and RSE FAQ](./TM_and_RSE_FAQ "TM and RSE FAQ")
*   [Project Plan](https://www.eclipse.org/dsdp/tm/development/plan.php) status
    *   CDT Launcher now works on dstore as well
    *   Jakarta commons-net - working fine for FTP
    *   JUnit tests - due to slow legal approval, we now have a framework but no tests yet
    *   Going to join Europa Simultaneous Release
*   Comments regarding the 1.0 release?
    *   Great work - using RSE almost daily (Michael Scharf)

#### Documentation: Which are the best places to start with?

*   [RSE Developer Docs](http://dsdp.eclipse.org/help/latest/index.jsp?topic=/org.eclipse.rse.doc.isv/guide/rse_int.html)
*   From the [TM Getting Started](https://www.eclipse.org/dsdp/tm/tutorial/index.php) page: [Eclipse Summit Europe Architecture Overview Slides](https://www.eclipse.org/downloads/download.php?file=/dsdp/tm/presentations/2006-9-29_SummitEurope_TMOverview.pdf)
    *   From the [Developer Docs](https://www.eclipse.org/dsdp/tm/doc/index.php): [Chicago Meeting Brainstorming Notes](https://www.eclipse.org/dsdp/tm/meetingnotes/ff01_chicago/DSDPTM_Brainstorming_2005-10-14.htm), [Chicago Meeting Overview Slides](https://www.eclipse.org/dsdp/tm/meetingnotes/ff01_chicago/DSDPTM_Overview.ppt)
    *   [Use Cases document](https://www.eclipse.org/dsdp/tm/doc/DSDPTM_Use_Cases_v1.1c.pdf) (old now but still up-to-date -- everybody agreed that this is where we want to get to)
    *   Upcoming Tutorial for EclipseCon2007

### Motorola - Christian Kurzke

*   Dev.environment for all Motorola hardware, going Eclipse now (also new TmL project)
    *   Interested in contributing towards version 2: bring requirements to the table, TM for cellphones, embedded settop boxes
    *   Looks like there is a lot of existing support for Linux workstations; new requirements coming for "bare metal" stuff; Motorola's requirements are somewhere in the middle
        *   Maureen to get in closer touch technically

### Community's most wanted - who's working on what?

*   [Wicked Shell](http://eclipse-plugins.info/eclipse/plugin_details.jsp?id=1392)
*   WR Terminalview: Michael Scharf currently heavily refactoring this, such that connection can be exchanged; hopes to be finished in the next few days --> FAQ
*   There is usage for both commandview (line-based text output) and terminalview
*   Plans to extend RSE more to the target? (native agent) FAQ
    *   Until recently, the strategy was that companies already have proprietary agents, and they'd write extensions to RSE that integrates with the existing proprietary agent
    *   There seems to be field demand for an Open Source agent solution; TPTP already has a Framework for agents; might investigate an integration of RSE with the TPTP agent in the future, rather than developing yet another agent. Symbian thinks about adding this to RSE 2.0
    *   TPTP is C++, which might be a problem on some very small devices; but Motorola to look at it
    *   Motorola has proprietarty C-based agent now; want an agent framework that can be extended, such that agent extensions (modules) can be downloaded
    *   Writing a native C implementation of the DStore agent might also be an option
    *   Christian wrote something like an OSGi framework in native code for dynamic loading of modules, might be an interesting starting point
*   Questions? Requests?

### Communications

*   After 1.0, committers will have a 6-week phase of maintenance, doc update, polishing etc. culminating in RSE 1.0.1 mid december; gives time to work on themes and priorities for RSE 2.0
*   Please fill in [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") \- your "wishlist"
*   Collaborations with other projects (Platform/Team, PTP, CDT, TPTP, WTP, ECF, Aperi, g-Eclipse)
    *   Martin wants Platform/Team to get ssh2 preference page under category "Connections"
    *   Javier in contact with ECF for service discovery
    *   Michael: DD project has new views for async updates of trees; might be a better view for the RSE tree
*   Technology sub-groups
    *   Update on [Autodetect](./Autodetect "DSDP/TM/Autodetect") (Javier)
        *   Currently no plans to extend discovery beyond what's already there; waiting for community input
*   What's the preferred way of communicating - newsgroup or dev-mailing list?
    *   The newsgroup is not very active, we are using the [dsdp-tm-dev list](https://dev.eclipse.org/mailman/listinfo/dsdp-tm-dev) for most communications (probably because most users are also interested in contributing)

Action Items to Review
----------------------

*   Last meeting: [DSDP/TM/Phone Meeting 4-Oct-2006](./Phone_Meeting_4-Oct-2006 "DSDP/TM/Phone Meeting 4-Oct-2006")

New Action Items
----------------

*   Everybody - Get latest RSE I-builds ([download page](http://download.eclipse.org/dsdp/tm/)), sanity-check ([RSE 1.0 Test Instructions](./RSE_1.0_Test_Instructions "RSE 1.0 Test Instructions") page) and verify late bug fixes ([Bugzilla: RSE bugs fixed last week](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=RESOLVED&resolution=FIXED&resolution=INVALID&resolution=WONTFIX&resolution=DUPLICATE&resolution=WORKSFORME&chfieldfrom=7d&chfieldto=Now&chfield=resolution&cmdtype=doit))
*   Everybody - Review and edit the [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") page
*   Maureen to try RSE, review docs, and get in contact with the [dsdp-tm-dev list](https://dev.eclipse.org/mailman/listinfo/dsdp-tm-dev) (probably setup a 1-on-1 talk)
*   Christian to look at options for Open Remote Agents (TPTP and others)
*   Martin - add FAQ items for Commandview vs. Terminal, Remote Native Agents
*   DaveD - begin EMO review submission for SSH/Processes patch from MontaVista

Next Meeting
------------

*   Next [DSDP/TM/Phone Meeting 6-Dec-2006](./Phone_Meeting_6-Dec-2006 "DSDP/TM/Phone Meeting 6-Dec-2006") (Wednesday, 4 weeks)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_8-Nov-2006](https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_8-Nov-2006))