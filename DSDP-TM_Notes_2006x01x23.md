

DSDP-TM Notes 2006x01x23
========================

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Monday [January 23, 2006](/index.php?title=January_23,_2006&action=edit&redlink=1 "January 23, 2006 (page does not exist)") at 9am PST |
| Primary International Dial-in: | **+44 (0)1452 567588** |
| USA Freephone Dial-In: | +1 (866) 6161738 |
| UK National Dial-In: | 08712460713 |
| Passcode: | **0587322148 #** |

Contents
--------

*   [1 Attendants](#Attendants)
*   [2 Agenda](#Agenda)
    *   [2.1 Action Items completed since last meeting](#Action-Items-completed-since-last-meeting)
    *   [2.2 Recent News](#Recent-News)
    *   [2.3 Discussions regarding TM Design](#Discussions-regarding-TM-Design)
*   [3 Next Steps](#Next-Steps)
    *   [3.1 Action Items](#Action-Items)
    *   [3.2 Next Meeting](#Next-Meeting)

Attendants
----------

*   Martin Oberhuber, Wind River
*   Mark Littlefield and Darian Wong, Curtiss-Wright
*   Pierre-Alexandre Masse, MontaVista
*   David Dykstal, IBM
*   Dave McKnight, IBM
*   Michael Scharf, Wind River
*   Victor Palau, Symbian
*   Javier Montalvo, Symbian
*   Peter Lachner, Intel

Agenda
------

*   Welcome Mark and Darian from Curtiss-Wright
    *   Mark: Manager for Applications Engineering, for embedded systems, Virginia
    *   Darian: Lead SW Developer & Marketing Manager for Tools
    *   Building advanced multicomputers - quad DSP board
    *   Want DSDP-TM to provide an integrated approach to debugging their software on multiple processors (64 processing nodes, debug across those); debugging, starting application, managing nodes
    *   Read about PTP but not looked closer
    *   Little experience with Eclipse so far; users of WR Workbench so far
    *   Debugging: distributed memory processing, each node has its own OS; multiple executables running at the same time; suppose to never have one debugger to control everything. So far, used gdb as a point debugger and have multiple windows open. Expect one Launcher window for controlling individual nodes, and allowing to launch a debugger for each node.

### Action Items completed since last meeting

*   MartinO:
    *   Post "connector" notes on Wiki: completed - [DSDP-TM Connector Meeting Salzburg 2005x11x14](/DSDP-TM_Connector_Meeting_Salzburg_2005x11x14 "DSDP-TM Connector Meeting Salzburg 2005x11x14")
*   DaveD:
    *   Continue working on making RSE available to the group as early as possible
    *   All clearances got from IBM
    *   Will do initial submission this week: fill out forms, find out if Bugzilla is the appropriate way for such a significant contribution

### Recent News

*   MartinO to revise Website for the new Phoenix style; fill in the project meta-info and write up the project plan

### Discussions regarding TM Design

*   deferred until RSE code is there

Next Steps
----------

### Action Items

*   MartinO:
    *   Launch Actions - Initial Design
    *   Contact Greg Watson (LANL, PTP)
*   George Clark:
    *   Approach ARM regarding Register file definitions - contact made, waiting for feedback
*   Symbian:
    *   Write up interface description for "Service" as understood by Symbian
    *   Send Enterprise Architect file and XMI file for use case to the dsdp-tm list - to be done later today
*   Pierre-Alexandre
    *   Write up additional use case for STAF
*   Everyone:
    *   Bring schema / example for Register Files & Boardfiles

### Next Meeting

*   **Next Meeting** on Monday, [February 6, 2006](/index.php?title=February_6,_2006&action=edit&redlink=1 "February 6, 2006 (page does not exist)") at 9am PST -- 2 weeks
    *   Agenda and Notes on [DSDP-TM Notes 2006x02x06](/DSDP-TM_Notes_2006x02x06 "DSDP-TM Notes 2006x02x06")
*   **Face-to-face Meeting** confirmed for Wed, [February 22, 2006](/index.php?title=February_22,_2006&action=edit&redlink=1 "February 22, 2006 (page does not exist)") \- Fri, [February 24, 2006](/index.php?title=February_24,_2006&action=edit&redlink=1 "February 24, 2006 (page does not exist)"), IBM Labs Toronto (Pete Nicholls)
    *   DD Meetings on Wednesday + Thursday morning
    *   TM Meetings on Thursday afternoon + Friday
    *   Agenda and Notes on [DSDP-TM F2F 2006x02x23](/index.php?title=DSDP-TM_F2F_2006x02x23&action=edit&redlink=1 "DSDP-TM F2F 2006x02x23 (page does not exist)")
    *   Details on meeting location to follow on dsdp-dd mailing list (north of Toronto, 35 minutes from airport, easy to get there)


(Migrated from [https://wiki.eclipse.org//DSDP-TM_Notes_2006x01x23](https://wiki.eclipse.org//DSDP-TM_Notes_2006x01x23))