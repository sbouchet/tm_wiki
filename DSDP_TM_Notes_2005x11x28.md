

DSDP TM Notes 2005x11x28
========================

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Monday [November 28, 2005](/index.php?title=November_28,_2005&action=edit&redlink=1 "November 28, 2005 (page does not exist)") at 9am PST |
| Primary Dial-in: | +1 (866) 278-2164 |
| Alternate Dial-In: | +1 (630) 424-7895 |
| Passcode: | 5585626# |

Contents
--------

*   [1 Invited Attendants](#Invited-Attendants)
*   [2 Meeting Notes](#Meeting-Notes)
    *   [2.1 Action Items open from last meeting](#Action-Items-open-from-last-meeting)
    *   [2.2 Recent News](#Recent-News)
    *   [2.3 Discussions regarding TM Design](#Discussions-regarding-TM-Design)
*   [3 Next Steps](#Next-Steps)

Invited Attendants
------------------

*   Martin Oberhuber, Wind River
*   Felix Burton, Wind River
*   Doug Schaefer, QNX
*   David Inglis, QNX
*   Pierre-Alexandre Masse, MontaVista
*   David Dykstal, IBM
*   Victor Palau, Symbian
*   Javier Montalvo, Symbian

Meeting Notes
-------------

### Action Items open from last meeting

*   DavidD:
    *   Approach ssh / team people for opening interfaces to TM - Michael Valenta on the team component says they are looking at this for 3.2. Talked to Scott Lewis, perhaps ECF would be willing to provide a home? See Bugzilla [bug 84677](https://bugs.eclipse.org/bugs/show_bug.cgi?id=84677). Problem for making ssh API external is testing (only want to test against CVS).
    *   RSE Docs, Sample, Release - getting closer with IP Law stuff; need an Eclipse proposal to go to the DSDP PMC and maybe Eclipse board (need to work with Martin on that). Dave still wants to submit the FTP sample to dsdp-tm-list. Want to reconcile the File API with what Pierre-Alexandre proposed.
        *   Found that EMF implementation for persistency is quite fragile to refactoring; looking for a very lightweight persitency framework to replace EMF. This is a must-have for releasing a first version of RSE, because the EMF MOF format doesnt allow for good migration between different releases.
*   MartinO:
    *   Launch Actions - Initial Design - still open
    *   Contact Greg Watson (LANL, PTP) - still open
*   George Clark:
    *   Approach ARM regarding Register file definitions - still open
*   Everyone:
    *   Scenarios for YOUR most important TM use-case
    *   Bring schema / example for Register Files & Boardfiles

### Recent News

*   DSDP-TM Wiki at [https://wiki.eclipse.org/index.php/DSDP/TM](https://wiki.eclipse.org/index.php/DSDP/TM)
*   EclipseCon 2006
    *   Martin O. to present a long talk on Target Management together with Dave D. Please vote for it on [http://www.eclipsecon.org](http://www.eclipsecon.org)

### Discussions regarding TM Design

*   [Connector Meeting in Salzburg - Notes](/DSDP-TM_Connector_Meeting_Salzburg_2005x11x14 "DSDP-TM Connector Meeting Salzburg 2005x11x14") ([November 14, 2005](/index.php?title=November_14,_2005&action=edit&redlink=1 "November 14, 2005 (page does not exist)"))
    *   Hard to think about the generic connector concept
    *   The hardest thing is to define interfaces for services that are not yet known -- idea:
        *   TM should only understand very basic interfaces (e.g. for service discovery), rest to be provided by plug-ins - leave as little intelligence as possible to the connector boxes, they should focus on doing their special task
        *   TM should only hold the meta-information for connectors (that can also be programs outside Eclipse): provided-protocol, required-protocol
        *   Felix Burton worked on "Receptacles" 1980 -- showcase that composition and configuration of connection chains can actually work
        *   As a result, updated PeterL's connector paper (to be posted together with full meeting notes)
*   Draft API - Pierre-Alexandre
    *   Documents did not go through on the mailing list -- AI: MartinO to upload
    *   Wrote down what RSF was like, currently not much time for TM
*   Draft API - Martin O. (as presented at the CDT conference) -- The CDT Integration needs to
    *   Show a widget for selecting (or potentially creating) a connection for the given Launch -- Interface will need some filtering capability (still missing)
    *   Persist the target connection reference as a String in the Launch, and re-create it from its String representation
    *   Get target connection data that is relevant for attaching the debugger properly (and potentially store additional data that is relevant for the debugger only, like a default Source Path Mapping for the given connection)

interface ITargetUI {
  ITargetSelectWidget makeTargetSelectWidget(Composite parentControl);
  ITargetConnectionReference showTargetSelectDialog();
}

interface ITargetService {
  ITargetConnection getConnectionData(ITargetConnectionReference ref);
  void connect(ITargetConnection tc, IProgressMonitor progress);
  ITargetAction getAvailableActions(ITargetConnection tc);
}

interface ITargetModelFactory {
  ITargetConnectionReference makeTargetConnectionReference(String rep);
}

Next Steps
----------

*   MartinO:
    *   Launch Actions - Initial Design
    *   Contact Greg Watson (LANL, PTP)
    *   Send reminder regarding hardware description files
    *   Post "connector" notes on Wiki
    *   Post Pierre-Alexandre's proposal on Wiki
    *   Post Dave Dykstal's "RSE-Hierarchy" on Wiki
*   Dave Dykstal:
    *   Work with Martin O on RSE Proposal for Eclipse / DSDP PMC
*   Victor Palau:
    *   Send Scenario for TM / Testing @ Symbian
*   George Clark:
    *   Approach ARM regarding Register file definitions
*   Everyone:
    *   Review Pierre-Alexandre's proposal
    *   Scenarios for YOUR most important TM use-case
    *   Bring schema / example for Register Files & Boardfiles

*   **Next Meeting** on Monday, [December 19, 2005](/index.php?title=December_19,_2005&action=edit&redlink=1 "December 19, 2005 (page does not exist)") at 9am PST
    *   [Agenda / Meeting Notes](/DSDP_TM_Notes_2005x12x19 "DSDP TM Notes 2005x12x19")


(Migrated from [https://wiki.eclipse.org//DSDP_TM_Notes_2005x11x28](https://wiki.eclipse.org//DSDP_TM_Notes_2005x11x28))