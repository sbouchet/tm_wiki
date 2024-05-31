

DSDP TM Notes 2005x12x19
========================

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Monday [December 19, 2005](/index.php?title=December_19,_2005&action=edit&redlink=1 "December 19, 2005 (page does not exist)") at 9am PST |
| Primary Dial-in: | +1 (866) 278-2164 |
| Alternate Dial-In: | +1 (630) 424-7895 |
| Passcode: | 5585626# |

Contents
--------

*   [1 Invited Attendants](#Invited-Attendants)
*   [2 Agenda](#Agenda)
    *   [2.1 Action Items completed since last meeting](#Action-Items-completed-since-last-meeting)
    *   [2.2 Recent News](#Recent-News)
    *   [2.3 Discussions regarding TM Design](#Discussions-regarding-TM-Design)
*   [3 Next Steps](#Next-Steps)
    *   [3.1 Action Items](#Action-Items)
    *   [3.2 Next Meeting](#Next-Meeting)

Invited Attendants
------------------

*   Martin Oberhuber, Wind River
*   Pierre-Alexandre Masse, MontaVista
*   David Dykstal, IBM
*   Peter Lachner, Intel
*   Victor Palau, Symbian
*   Javier Montalvo, Symbian
*   Neil Taylor, Symbian

Agenda
------

### Action Items completed since last meeting

*   MartinO:
    *   Send reminder regarding hardware description files: sent to dsdp-tm list
    *   Post Pierre-Alexandre's proposal on Wiki: [DSDP-TM Draft API Proposal by Pierre-Alexandre 2005x11x21](/DSDP-TM_Draft_API_Proposal_by_Pierre-Alexandre_2005x11x21 "DSDP-TM Draft API Proposal by Pierre-Alexandre 2005x11x21")
    *   Post Dave Dykstal's "RSE-Hierarchy" on Wiki: [DSDP-TM Proposal for RSE Hierarchy by Dave Dykstal 2005x11x09](/DSDP-TM_Proposal_for_RSE_Hierarchy_by_Dave_Dykstal_2005x11x09 "DSDP-TM Proposal for RSE Hierarchy by Dave Dykstal 2005x11x09")
*   Victor Palau:
    *   Sent [Scenario for TM / Testing @ Symbian](/images/c/cb/Symbian_UseCase.gif "Symbian UseCase.gif") on the dsdp-tm list

### Recent News

*   A long talk on TM was accepted at EclipseCON: [http://canuck.gda.itesm.mx/eclipsezilla/show_bug.cgi?id=287](http://canuck.gda.itesm.mx/eclipsezilla/show_bug.cgi?id=287)
*   DSDP PMC had its first meeting: DSDP in Japan
    *   New DSDP projects in Proposal phase:
        *   [Native Application Builder](https://www.eclipse.org/proposals/nab/)
        *   [Mobile Tools for Java](https://www.eclipse.org/proposals/mtj/)
    *   PMC Tasks: Ensure IP due diligence, coordinate releases, help new projects, ensure presence of projects on conferences, vote on committers
*   RSE: Important meetings on Dec/20 and Jan/10

### Discussions regarding TM Design

*   Pierre Alexandre describes [DSDP-TM Draft API Proposal by Pierre-Alexandre 2005x11x21](/DSDP-TM_Draft_API_Proposal_by_Pierre-Alexandre_2005x11x21 "DSDP-TM Draft API Proposal by Pierre-Alexandre 2005x11x21")
    *   Has some implementation for the interfaces based on [STAF](http://staf.sourceforge.net/index.php)
*   Dave: RSE structure is very similar; there is some experience with STAF; RSE should match Pierre Alexandre's structure quite nicely
    *   IRemoteSystem corresponds to RSE Connection
    *   ServiceTypeModel corresponds to RSE Subsystem ... RSE SystemType act as a registry to hold services
    *   An RSE subsystem is an implementation of a particular service -- RSE is adding a service layer now to add GUI-less exchangeability of services

*   **Symbian Use Cases - Javier**:
    *   See [Media:Symbian_UseCase.gif](/images/c/cb/Symbian_UseCase.gif "Symbian UseCase.gif")
    *   Services Request: There might be different service agents, e.g. for executing a test, installing a package (need to know if setup service is available) - availability of services may depend on version of the target OS
    *   DSDP-TM has service plugins
    *   What could the interface for a "service" look like? - AI: Symbian to write up interface definitions for services
    *   Pierre-Alexandre is very interested in STAF ... hook up directly with Symbian, have discussions on the dsdp-tm-list

*   **Pierre Alexandre: When will RSE really be available?**
    *   Dave: As soon as OK from IBM Management is there, the mechanics of fixing EPL comments etc. can start; not sure if it is feasible to make available before final

*   Neil: Are there any other use cases for testing with STAF?
    *   Have the use case as an [Enterprise Architect](http://www.sparxsystems.com.au) file; send it to the list
    *   AI Pierre Alexandre will write down a use case and send to the mailing list

*   **Connector Proposal**: Martin updating Notes on Wiki: [DSDP-TM Connector Meeting Salzburg 2005x11x14](/DSDP-TM_Connector_Meeting_Salzburg_2005x11x14 "DSDP-TM Connector Meeting Salzburg 2005x11x14")
    *   Peter having some internal discussion, expect some news in january.

Next Steps
----------

### Action Items

*   MartinO:
    *   Launch Actions - Initial Design
    *   Contact Greg Watson (LANL, PTP)
    *   Post "connector" notes on Wiki: [DSDP-TM Connector Meeting Salzburg 2005x11x14](/DSDP-TM_Connector_Meeting_Salzburg_2005x11x14 "DSDP-TM Connector Meeting Salzburg 2005x11x14")
*   George Clark:
    *   Approach ARM regarding Register file definitions
*   DaveD:
    *   Continue working on making RSE available to the group as early as possible
*   Symbian:
    *   Write up interface description for "Service" as understood by Symbian
    *   Send Enterprise Architect file and XMI file for use case to the dsdp-tm list
*   Pierre-Alexandre
    *   Write up additional use case for STAF
*   Everyone:
    *   Bring schema / example for Register Files & Boardfiles

### Next Meeting

*   Next Meeting on Monday, [January 23, 2006](/index.php?title=January_23,_2006&action=edit&redlink=1 "January 23, 2006 (page does not exist)") at 9am PST -- 5 weeks due to Christmas
    *   [DSDP-TM Notes 2006x01x23](/DSDP-TM_Notes_2006x01x23 "DSDP-TM Notes 2006x01x23")


(Migrated from [https://wiki.eclipse.org//DSDP_TM_Notes_2005x12x19](https://wiki.eclipse.org//DSDP_TM_Notes_2005x12x19))