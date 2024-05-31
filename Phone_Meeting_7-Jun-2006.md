

DSDP/TM/Phone Meeting 7-Jun-2006
================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Wednesday [June 7, 2006](./index.php?title=June_7,_2006&action=edit&redlink=1 "June 7, 2006 (page does not exist)") at 9am PST |
| Primary International Dial-in: | **+44 (0)1452 567588** |
| USA Freephone Dial-In: | +1 (866) 6161738 |
| UK National Dial-In: | 08712460713 |
| Passcode: | **0587322148 #** |

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Notes](#Notes)
    *   [2.1 RSE Status (Dave D)](#RSE-Status-.28Dave-D.29)
    *   [2.2 Communications](#Communications)
    *   [2.3 Community Status and Feedback](#Community-Status-and-Feedback)
    *   [2.4 Technology sub-groups](#Technology-sub-groups)
    *   [2.5 Closed Action Items](#Closed-Action-Items)
*   [3 New Action Items](#New-Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   Accelerated Technology - Aaron Spear
*   IBM - David Dykstal, Kushal Munir, Dave McKnight, Michael Berger
*   Montavista - Joe Green
*   PTP Project - Greg Watson
*   QNX - Doug Schaefer
*   Symbian - Javier Montalvo, Neil Taylor
*   Wind River - Martin Oberhuber

Notes
-----

### RSE Status (Dave D)

*   M2 Delivered, Bugzilla situation: [DSDP/TM Report - Severity against OS](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=bug_severity&y_axis_field=op_sys&z_axis_field=bug_status&query_format=report-table&short_desc_type=allwordssubstr&short_desc=&classification=DSDP&product=Target+Management&component=RSE&format=table&action=wrap)
*   [Project Plan](https://www.eclipse.org/dsdp/tm/development/plan.php) changes accepted
*   Community's Most Wanted: ssh, mac support, docs and examples
    *   Automated builds, including docs, will be running on build.eclipse.org -- switched the drivers from Ruby to Perl
    *   Will create N-builds once this is set up; community encouraged to use those, since lots of fixes went in after M2
    *   DaveD currently working on Mac; GregW is happy to do another round of testing when asked (as we are going to approach M3)
*   Interesting Recent RSE Changes
    *   New persistence provider added; going to hide implementation
    *   All "resolve" operations are now non-UI jobs; This allows to get rid of UI dependency in the Services; affects Files and Processes subsystems
*   RSE and EFS - See [Eclipse File Service APIs Compared](./Eclipse_File_Service_APIs_Compared "Eclipse File Service APIs Compared")
    *   Found problems, because RSE stores downloaded TempFiles in an Eclipse Project. This needs Platform APIs (Property Manager) which lead to a race condition when a .project file is accessed through EFS for project creation, or when Eclipse is shut down.
        *   Fixes might be possible but need experimentation. No resources to address this soon, also since EFS still has bugs in the Platform, CDT and JDT implementations are lacking. Therefore RSE EFS support will remain experimental and not go into the 1.0 release (no plan item).
        *   OK for PTP - Resources on Remote Support have to be cut down anyway, though PTP will continue try to help out.
    *   Keep EFS on the radar. Helpwanted for three areas where EFS touches RSE:
        *   implementing an EFS browser on top of RSE,
        *   fixing the RSE EFS provider problems,
        *   Investigating EFS implementations to serve as RSE file service
*   PTP found problems in RSE Command Service, unable to get the output of a command?
    *   For ssh, command implementation is not complete yet
    *   Otherwise, this should work, please file bug or ask on dsdp-tm-dev list

### Communications

*   Goal of the monthly meetings is to inform, but also collect feedback from the larger community
*   [RSE API Discussion](./RSE_API_Discussion "RSE API Discussion") \- Wiki page to serve as directory into API discussions held on Bugzilla
    *   Please file Enhancement Requests for API changes, put \[api\] in the subject
*   [RSE 2.0 Planning](./RSE_2.0_Planning "RSE 2.0 Planning") for next year
    *   For now, this page is a container & directory for (bugzilla) feature requests that are not going to make it into RSE 1.0
    *   Shall serve as the input for planning 2.0
    *   Want to have a face-to-face meeting (september?) for planning 2.0
*   Wiki notifications
    *   You can turn on "watch" for a Wiki page. The Wiki will collect changes to watched pages on the [my watchlist](./Special:Watchlist "Special:Watchlist") page.
*   [TM Development Homepage](https://www.eclipse.org/dsdp/tm/development/index.php) \- a nice collection of links and tools
    *   Reachable from the [TM Homepage](https://www.eclipse.org/dsdp/tm), Navigation bar, last item "Development Tools"
    *   Includes CVS information like *.psf Project Sets and the link to the [CVS Changelog](http://download.eclipse.org/dsdp/tm/downloads/drops/N-changelog/index.html)

### Community Status and Feedback

*   Montavista -- JoeG just starting to work with RSE: want to support **targets that do not have Java**
    *   MartinO - WindRiver going to add proprietary subsystems for this. Other option is subsystems that collect data through the shell-based command service (ssh, telnet etc).
    *   Aaron - Mentor going to add proprietary subsystems
*   Symbian - also want to monitor processes; think about a **standard protocol for sending processes**, perhaps with some abstraction layer
    *   Aaron: want to have a common open protocol for such services, probably something debugger oriented. Ideal would be a common base protocol that can be extended for various services.
        *   DataStore might be generic enough for being the base protocol for this
        *   Native implementation of a datastore agent might be desirable
        *   TPTP Common Base Event (CBE)? - Javier: this is too heavy on the device
*   Martin: Level of abstraction in RSE is high; common base protocol would be low level of abstraction, something that we have not looked at so far
*   Aaron would love a standard protocol rather than just rolling our own again
*   Unfortunately, nobody has resources to lead this right now. Keep it on the radar until we have more experience with RSE.

### Technology sub-groups

*   Not covered:
    *   CDT Launching -- Ewa did not show up
    *   [Autodetect](./Autodetect "DSDP/TM/Autodetect") \-\- Javier dropped off early
    *   [Connectors](./Flexible_Target_Connection_Adaptors "DSDP/TM/Flexible Target Connection Adaptors") \-\- Peter L did not show up
*   Update on [SPIRIT](./DD/Spirit "DSDP/DD/Spirit") (Aaron)
    *   Lots of discussions held on DD mailinglist (partly embedded in other subjects)
    *   Debug specific needs been added to the SPIRIT roadmap, but lots of action items are still open
    *   What do people perceive as the ways they want to use the information? C++ debugger back-ends?
        *   MVista: gdb -- translate SPIRIT into something suitable for gdb
        *   Size of files might be an issue (when pulling files from the target)
        *   Aaron want to work on debugger-specific objects that may or may not be serialized in various ways
        *   SPIRIT to get the information from the manufacturers
    *   Want a hierarchy of target descriptions?
        *   Need a standard framework for cataloging a set of targets
        *   This is an issue that TM should deal with. Aaron to re-post corresponding question to dsdp-tm-dev list.

### Closed Action Items

*   Last meeting: [DSDP/TM/Phone Meeting 3-May-2006](./Phone_Meeting_3-May-2006 "DSDP/TM/Phone Meeting 3-May-2006")
*   Symbian -- Write up interface description for "Service" as understood by Symbian -- no longer needed
*   MartinO -- EFS discussion started, Jakarta Commons submitted to EMO, Wiki notifications explained

New Action Items
----------------

*   AaronS -- re-post target description e-mail to dsdp-tm-dev
*   DaveD -- inform dsdp-tm-dev list once N-builds are available; send instructions for automated builds to GregW
*   DaveM -- \[old\] Review daytime & ssh code and look for possible simplifications for adding a service
*   MartinO -- \[old\] Create TM press text, introduction, tutorial on website
*   Everyone:
    *   RSE usage and API reviews --> Bugzilla (Use forms at [TM homepage](https://www.eclipse.org/dsdp/tm))

Next Meeting
------------

*   Next [DSDP/TM/Phone Meeting 5-Jul-2006](./Phone_Meeting_5-Jul-2006 "DSDP/TM/Phone Meeting 5-Jul-2006") (wednesday, 4 weeks)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_7-Jun-2006](https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_7-Jun-2006))