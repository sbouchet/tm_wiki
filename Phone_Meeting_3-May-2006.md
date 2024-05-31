

DSDP/TM/Phone Meeting 3-May-2006
================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Wednesday [May 3, 2006](./index.php?title=May_3,_2006&action=edit&redlink=1 "May 3, 2006 (page does not exist)") at 9am PST |
| Primary International Dial-in: | **+44 (0)1452 567588** |
| USA Freephone Dial-In: | +1 (866) 6161738 |
| UK National Dial-In: | 08712460713 |
| Passcode: | **0587322148 #** |

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Meeting Notes](#Meeting-Notes)
    *   [2.1 Update on RSE Status (Dave D)](#Update-on-RSE-Status-.28Dave-D.29)
    *   [2.2 How to communicate (MartinO)](#How-to-communicate-.28MartinO.29)
    *   [2.3 Eclipse Release Review Requirements (MartinO)](#Eclipse-Release-Review-Requirements-.28MartinO.29)
    *   [2.4 Update on Autodetect (Javier)](#Update-on-Autodetect-.28Javier.29)
    *   [2.5 PTP Needs / Collaboration (Greg W)](#PTP-Needs-.2F-Collaboration-.28Greg-W.29)
    *   [2.6 Other Technology Sub-Groups](#Other-Technology-Sub-Groups)
*   [3 Action Items still open from last meetings](#Action-Items-still-open-from-last-meetings)
*   [4 New Action Items](#New-Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   Martin Oberhuber, Brian Netteleton - Wind River
*   David Dykstal, Kushal Munir, Dave McKnight - IBM
*   Ewa Matejska, Palm Source
*   Javier Montalvo and Neil Taylor, Symbian
*   NNN - Montavista
*   Doug Schaefer - QNX
*   Aaron Spear, Mentor Graphics
*   Mark Bozeman,
*   Peter Lachner, Intel
*   Kirk Beitz, Freescale
*   Greg Watson, LANL (PTP lead)
*   Tianchao Li - Technische Universitaet Muenchen (work with LANL on PTP)

The call is open for everyone else to attend.

Meeting Notes
-------------

### Update on RSE Status (Dave D)

*   *   M1 delivered 18-Apr-2006. Tested and reasonably stable, but some features had to be dropped (see the [release notes](http://download.eclipse.org/dsdp/tm/downloads/drops/S-1.0M1-200604270100/releaseNotes.php)).
    *   Will need some replanning for M2 and beyond
        *   M2 to include planned M1 features plus probably a few more
        *   user actions and import/export to be delayed to M3, community is OK with that.
        *   Might need another milestone before achieving release status
*   Next steps on RSE: Most wanted by the community
    *   DaveD: do a **daily driver** schedule, i.e. 2-3 automated builds each week
    *   Ewa: need **ssh service** integrated to CVS
        *   MartinO: have an updated ssh service including file transfer via sftp, expect on bugzilla the next days
    *   Greg: Need client on **MacOS** and probably Power Linux. Probably make MacOS a reference platform? Could contribute resources for build and testing.
        *   DaveD to send instructions for automated builds on the mailing list.
    *   Ewa: Workflow for **adding a Service to be made simpler**.
        *   Good ISV docs are available but outdated, DaveD wants to add them to M3
        *   Add Daytime and SSH examples, Dave McKnight to review if they can be made simpler (does the API really require a ConnectorServiceManager? Which classes are the absolute minimum for a Service?)
    *   Put **contributions from Bugzilla into CVS** soon (ssh, daytime, cdtremote), in order to make sure they take part in refactorings
        *   Provide CVS Project Set files (*.psf) to make it easier for developers to pick up newly added projects
    *   Update site is not an immediate issue, this is more for users but currently it's more developers working on RSE. Want to do an update site but probably after M2.
    *   **Lower the bar**: overview and getting-started on website (MartinO)

### How to communicate (MartinO)

*   Do more in Bugzilla!
    *   RSE bugreports and enhancement requests
    *   **API Review** is an important task for M2 and beyond. File Bugzilla entries for discussions on APIs
    *   Technology sub-groups to track their discussions in Bugzilla instead of the mailing list
        *   Easier to find, associate and get started for newcomers
        *   Wiki pages for technology sub-groups will hold links to Bugzilla discussions
        *   Send an E-Mail to dsdp-tm-dev when a new Bugzilla Entry is created for a discussion. MartinO, or other committers, to update the Wiki with links to Bugzilla entries.
        *   MartinO to find out if Wiki notifications can be configured to go to the tm-dev list

### Eclipse Release Review Requirements (MartinO)

*   We're currently in Incubation phase. In order to be able to make a 1.0 release, we'll have to go through a [release review](https://www.eclipse.org/projects/dev_process/release-review.php). Before we pass the release review, we can only do 0.x releases.
*   Release Reviews are not an easy thing, Eclipse Foundation puts the bar pretty high
*   The actual Review typically takes place around the time a first release candidate is built
*   Start addressing issues required by Release Review early, in order to avoid a big bang late in the game:
    *   Work on [Eclipse Quality](https://www.eclipse.org/projects/dev_process/eclipse-quality.php) APIs
        *   Tool **and** API usability (for users **and** for programmers)
        *   Non-code aspects e.g. documentation
        *   IP Logs
    *   Grow the community

### Update on Autodetect (Javier)

*   looked at Zeroconf (used by Apple for Plug&Play)
    *   plugins for discovery through Zeroconf in ECF
    *   Community seems to accept that Zeroconf is the right thing - also implemented in very small devices
*   Javier to capture mailinglist discussions in a Bugzilla entry
*   MartinO: Zeroconf is good, but make sure that APIs can also be implemented by an alternative service that does not necessarily use a protocol on the wire (e.g. discover services by looking at JTAG config files, kernel images)
*   Aaron: Legacy devices connected via Serial
    *   Javier: Proxy server attached to Legacy device
    *   Might want to connect to JTAG etc

### PTP Needs / Collaboration (Greg W)

*   Remote Services aspect is very important to PTP
*   Remote Launch capabilities
*   Remote Build
*   Looked into Eclipse Filesystem (EFS)
*   Looked at EFS implementation in RSE; looks like RSE is duplicating a lot from the Platform; currently working more towards the platform
*   Want to work closely with TM and CDT communities
*   Dave McKnight to work with PTP community on EFS
    *   Should start discussion on EFS vs. RSE
*   PTP monthly telecon next week

### Other Technology Sub-Groups

*   [Connectors](./Flexible_Target_Connection_Adaptors "DSDP/TM/Flexible Target Connection Adaptors"): Peter L been busy lately, will start on Connectors in 1 week
*   [Shared Board Labs](./Shared_Board_Labs "DSDP/TM/Shared Board Labs"): Interest by Windriver, Freescale, Mentor; probably no deliverables till M1, but start planning / design in time (we should make plans for next year just before 1.0 is released)

Action Items still open from last meetings
------------------------------------------

*   Symbian:
    *   Write up interface description for "Service" as understood by Symbian
*   MartinO:
    *   Start EMO process for Jakarta Commons

New Action Items
----------------

*   DaveD:
    *   Send instructions for automated builds (on MacOS / LinuxPPC) to GregW
*   Dave McKnight:
    *   Review daytime & ssh code and look for possible simplifications for adding a service
    *   Start feature discussion RSE vs. Platform / EFS with PTP people (bugzilla or mailinglist; a feature document should eventually be available from the website)
*   MartinO:
    *   Update Project Plan, Website
    *   Deliver ssh service enhancements
    *   Check Wiki notifications
*   Javier:
    *   Capture autodetect on bugzilla
*   Everyone:
    *   RSE usage and API reviews --> Bugzilla

Next Meeting
------------

*   Keep the schedule (1st wednesday of the month)
*   Next [DSDP/TM/Phone Meeting 7-Jun-2006](./Phone_Meeting_7-Jun-2006 "DSDP/TM/Phone Meeting 7-Jun-2006") (wednesday, 5 weeks)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_3-May-2006](https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_3-May-2006))