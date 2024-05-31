

DSDP/TM/Phone Meeting 2-Aug-2006
================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Wednesday [August 2, 2006](/index.php?title=August_2,_2006&action=edit&redlink=1 "August 2, 2006 (page does not exist)") at 9am PST |
| Primary International Dial-in: | **+44 (0)1452 567588** |
| USA Freephone Dial-In: | +1 (866) 6161738 |
| UK National Dial-In: | 08712460713 |
| Passcode: | **0587322148 #** |

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
*   [3 Action Items to Review](#Action-Items-to-Review)
*   [4 New Action Items](#New-Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Attendees
---------

*   Accelerated Technology - Aaron Spear
*   IBM - Dave Dykstal, Dave McKnight, Kushal Munir
*   Palm Source - Ewa Matejska
*   QNX - Doug Schaefer
*   Symbian - Javier Montalvo
*   Wind River - Doug Gaff, Martin Oberhuber

Agenda
------

*   Update on RSE Status
    *   [Project Plan](https://www.eclipse.org/dsdp/tm/development/plan.php) status
        *   Docs are now online on the infocenter at [http://dsdp.eclipse.org/help/latest/](http://dsdp.eclipse.org/help/latest/)
        *   Getting the latest RSE is now easy by using the update site at [http://download.eclipse.org/dsdp/tm/updates/](http://download.eclipse.org/dsdp/tm/updates/)
        *   Tutorial project added to examples, docs updated
        *   Working on API freeze - get in your change requests now!
        *   Schedule to **move by 1 week**: I-build on Aug.11, followed by S-build on Aug.18
    *   **Lower the bar:** press text, Japan DSDP Workshop
    *   Community's most wanted - who's working on what?
        *   Greg interested in Mac support - to be addressed after M4
*   Communications
    *   [RSE API Discussion](/RSE_API_Discussion "RSE API Discussion")
    *   [RSE 2.0 Planning](/RSE_2.0_Planning "RSE 2.0 Planning")
    *   Collaborations with other projects (Platform/Team, PTP, CDT, TPTP, WTP, ECF, Aperi)
*   Technology sub-groups
    *   CDT Launching (Ewa)
        *   Want the CDT Remote Launch more official instead of just an example;
        *   Want to push into CDT in the future - for now, leave it in TM and make it a feature installable via update site.
        *   Ewa wants feedback on the feature from the community --> Need to give easy access to it (via TM update site).
        *   Refer to the TM repository via softlinks in CDT?
    *   Update on [SPIRIT](/DSDP/DD/Spirit "DSDP/DD/Spirit") (Aaron)
        *   Trying to get contributions of SPIRIT parsing code, but not much community feedback so far... parsing lib could be C/C++ as well, need not be restricted to Java (ARM has such libs)
        *   Many consumers but few contributors - nobody has an opinion until they see something
        *   DougS - nobody has a burning need right now? - But more for debugger back-ends than the Eclipse pieces
        *   Want pluggable debuggers in RSE - reading the generalized HW descriptions
        *   Windriver has integrated their commercial debugger at a coarse granular level - the WR debugger is a component in the tree
            *   More fine-granular integration will be a 2nd step (launching, target descriptions)
    *   Update on [Autodetect](/DSDP/TM/Autodetect "DSDP/TM/Autodetect") (Javier)
        *   Contribution in EMO review, things look positive that it'll be finished soon
        *   Javier to become committer :-)

Action Items to Review
----------------------

*   Last meeting: [DSDP/TM/Phone Meeting 5-Jul-2006](/DSDP/TM/Phone_Meeting_5-Jul-2006 "DSDP/TM/Phone Meeting 5-Jul-2006")

New Action Items
----------------

*   Ewa to update CDT Launch integration
*   Martin to create Feature for it and serve it from the RSE Update Site
*   DougS to direct parties interested in remote launching to Ewa / dsdp-tm-dev

Next Meeting
------------

*   Next [DSDP/TM/Phone Meeting 6-Sep-2006](/DSDP/TM/Phone_Meeting_6-Sep-2006 "DSDP/TM/Phone Meeting 6-Sep-2006") (wednesday, 6 weeks)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_2-Aug-2006](https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_2-Aug-2006))