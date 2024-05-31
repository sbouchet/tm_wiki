

DSDP/TM/Phone Meeting 2-May-2007
================================

< [DSDP](./DSDP "DSDP")‎ | [TM](./DSDP/TM "DSDP/TM")

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Wednesday May 2, 2007 at [1600 UTC / 9am PST](http://www.timeanddate.com/worldclock/fixedtime.html?month=5&day=2&year=2007&hour=16&min=00&sec=0&p1=0) |
| Primary International Dial-in: | **+44 (0)1452 567588** |
| USA Freephone Dial-In: | +1 (866) 6161738 |
| UK National Dial-In: | 08712460713 |
| Passcode: | **0587322148 #** |

Contents
--------

*   [1 Invited Attendees](#Invited-Attendees)
*   [2 Attendees](#Attendees)
*   [3 Notes](#Notes)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Invited Attendees
-----------------

This meeting is free for everyone to attend. We specially encourage those people to attend who are actively working on, or have shown interest in TM before:

Attendees
---------

*   Wind River - Martin Oberhuber
*   IBM - Dave McKnight, Dave Dykstal, Kushal Munir
*   Symbian - Javier Montalvo
*   Self-employed startup - Uday Kabe

Notes
-----

*   Uday: Using Eclipse RCP for a Lotus Notes extension with EMF, wants to upload with FTP through RCP, finding problems with editing in RCP: e.g. WST XML editor depending on Debug
    *   Not using some RSE plugins e.g. shell; created a couple of patches to **modify plugin.xml files e.g. to remove system types** \- how to get a particular version of RSE out of CVS?
        *   MartinO: val-tags not properly filled, will try to fix that; workaround for now is to get HEAD from the cvs_setup page which also holds the Team Project Sets, then "Team > Switch to another branch or version" afterwards: After "Refresh", correct tags should be shown
        *   MartinO: Only releases are tagged as R1\_0, R1\_0_1; for Milestones, the releng maps are used in (org.eclipse.tm.rse/releng/org.eclipse.rse.build/maps/rse.map)
        *   Want to drag&drop stuff from the "Notes" View to FTP - **PluginTransfer callback not activated?**
        *   **Resource exceptions at the very startup**, because it tries to create dom.properties as soon as a resource modification comes in, this throws exceptions and do more workspace modification stuff in the same thread
            *   DaveD - currently refactoring the persistence provider; can probably clean it up
*   Where is TM heading?
    *   Consolidating, API cleanup for 2.0 - making stuff internal
    *   Want to have "internal" stuff re-usable as well - Martin: "internal" packages are also exported, as per Eclipse common practice
*   Please keep the RCP perspective in mind
*   Where to get Architecture information?
    *   Use the [TM and RSE FAQ](./TM_and_RSE_FAQ "TM and RSE FAQ"), [EclipseCon07 Tutorial](http://www.eclipsecon.org/2007/index.php?page=sub/&id=3651), or [RSE ISV Docs](http://dsdp.eclipse.org/help/latest/index.jsp?topic=/org.eclipse.rse.doc.isv/guide/rse_int.html)
*   **Aptana also has some SSH / Upload** facility
*   **Platform/Team FTP and WebDAV - Discontinued**, to be replaced by DSDP-TM / RSE

Action Items
------------

*   **Martin**: Fix the "Versions" node for DSDP-TM Repository in Eclipse CVS Repository Explorer (**done** 3-May-2007)
*   **DaveD**: Cleanup persistence provider to fix resource exceptions at early startup
*   **Uday**: Test cleaned-up persistence provider from HEAD as soon as a stable build towards M7 is announced
*   **Uday**: Create bugzilla reports for any issues found (e.g. PluginTransfer issue).

Next Meeting
------------

*   Next [DSDP/TM/Phone Meeting 6-Jun-2007](./DSDP/TM/Phone_Meeting_6-Jun-2007 "DSDP/TM/Phone Meeting 6-Jun-2007") (5 weeks after)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_2-May-2007](https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_2-May-2007))