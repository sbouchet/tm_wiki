

TM/Code Ownership
=================

< [TM](/TM "TM")

What do we want to achieve by explicit code ownership?

*   **Integrity of the Design**: The owner is responsible for a solid extensible design.
    *   People other than the owner can make bug fixes, but please let the owner know.
    *   Don't make design-breaking changes without letting the owner know.
    *   Typically, there is a single owner for each functionality. Multiple "two-in-a-box" owners are only possible if they work very closely together.
    *   There may be a backup person for an owner, in case the owner is out-of-office.
*   **Timely Bug Triage**: The owner is responsible for reviewing (and probably reassigning) bugs of his area in a timely fashion.
    *   Helps dispatching new bugs to component owners first.
    *   Ownership can be for functionality that spans multiple packages (if functionality is seen by user as a single entity).
*   **Credit for Quality through Visibility**.
    *   Owners of a component should be publicly visible, so they can get the credit for good work.
*   **Ownership of Copyright and Intellectual Property (IP) issues**.
    *   Component owners are responsible for keeping the IP of their component clean.

<p/>

Clarification of Ambiguities
----------------------------

*   RSE Team Support (Team View, Profiles, Docs, Persistence wrt team support) -- rse.ui.view.team belongs to dmcknigh
    *   Teamview (better called Profiles View) is its own beast - DaveD to handle this (team is different than the rest) - to be improved by 2.0
*   Drag&Drop, Copy&Paste -- closely tied to the views, using view-dependent Eclipse Framework --> DaveM
*   Rse.core.filters --> DaveD (Filter creation, UI, change notification etc); filterreferences / view adapters --> DaveM
*   EFS - not yet assigned --> Kushal, Backup DaveM

Code Ownership Table
--------------------

</tr>

  

| Owner | Area | Plugin/Package | Backup owner |
| --- | --- | --- | --- |
| Dave Dykstal   (IBM) | RSE Persistency |   org.eclipse.rse.core/persistence   org.eclipse.rse.core/src/org.eclipse.rse.core.filters (persistence aspects)   org.eclipse.rse.core/src/org.eclipse.rse.core.model (persistence aspects)   org.eclipse.rse.core/src/org.eclipse.rse.core.persistance   org.eclipse.rse.core/src/org.eclipse.rse.core.references (persistence aspects)   org.eclipse.rse.core/src/org.eclipse.rse.internal.references (persistence aspects)   org.eclipse.rse.ui/filters (persistence aspects)   org.eclipse.rse.ui/model (persistence aspects)   org.eclipse.rse.ui/subsystems (persistence aspects)   org.eclipse.rse.ui/systems (persistence aspects)   | Xuan Chen |
| RSE password prompt |   org.eclipse.rse.core/src/org.eclipse.rse.core.subsystems (credential aspects)   org.eclipse.rse.ui/src/org.eclipse.rse.core.subsystems (credential aspects)   org.eclipse.rse.ui/UI/org.eclipse.rse.ui.dialogs (credential aspects)   |   |
| RSE logging |   org.eclipse.rse.logging - all packages   | Xuan Chen |
| RSE message support |   /org.eclipse.rse.services/clientserver/org.eclipse.rse.services.clientserver.messages   org.eclipse.rse.ui/UI/org.eclipse.rse.ui.messages   |   |
| RSE filtering |   org.eclipse.rse.core/src/org.eclipse.rse.core.filters   org.eclipse.rse.ui/filters   org.eclipse.rse.ui/UI/org.eclipse.rse.ui.propertypages - classes for filters   |   |
| Dialog Accessibility / UI Controls |   org.eclipse.rse.ui/UI/org.eclipse.rse.ui.Mnemonics   org.eclipse.rse.ui/UI/org.eclipse.rse.ui.widgets.InheritButton   org.eclipse.rse.ui/UI/org.eclipse.rse.ui.widgets.SystemHistoryCombo   org.eclipse.rse.ui - accessibility aspects   |   |
| RSE Documentation |   org.eclipse.dstore.doc.isv   org.eclipse.rse.doc.user   org.eclipse.rse.doc.isv   | Martin O |
| RSE JUnit tests |   org.eclipse.rse.tests   org.eclipse.rse.tests.framework   org.eclipse.rse.tests.framework.examples   | Xuan Chen |
| Dave McKnight   (IBM) | RSE dstore |   org.eclipse.dstore.core   org.eclipse.dstore.extra   org.eclipse.rse.connectorservice.dstore   org.eclipse.rse.dstore.security   org.eclipse.rse.services.dstore   org.eclipse.rse.subsystems.files.dstore   org.eclipse.rse.subsystems.processes.dstore   org.eclipse.rse.subsystems.shells.dstore      | Xuan Chen |
| RSE services |   org.eclipse.rse.services.files   org.eclipse.rse.services.processes   org.eclipse.rse.services.search   org.eclipse.rse.services.shells      | Xuan Chen |
| RSE core model |   org.eclipse.rse.core   org.eclipse.rse.core.filters   org.eclipse.rse.core.model   org.eclipse.rse.core.subsystems   org.eclipse.rse.subsystems.files.core   org.eclipse.rse.subsystems.processes.core   org.eclipse.rse.subsystems.shells.core      |   |
| RSE views |   org.eclipse.rse.ui.view   org.eclipse.rse.ui.view.monitor   org.eclipse.rse.ui.view.scratchpad   org.eclipse.rse.ui.view.search   org.eclipse.rse.ui.view.team   org.eclipse.rse.ui.widgets   org.eclipse.rse.ui.widgets.services      |   |
| Kushal Munir, Xuan Chen   (IBM) | RSE Archive Handlers | org.eclipse.rse.services.clientserver.archivehandlers |   |
| RSE core comm | org.eclipse.rse.core.comm |   |
| RSE search |   org.eclipse.rse.files.ui.search   org.eclipse.rse.ui.view.search   |   |
| RSE file encodings | (multiple) |   |
| Uwe Stieber   (Wind River) | RSE New Connection Wizard | org.eclipse.rse.ui/org.eclipse.rse.ui.wizards    org.eclipse.rse.ui/org.eclipse.rse.ui.wizards.newconnection   org.eclipse.rse.ui/org.eclipse.rse.ui.wizards.registries      | Kushal Munir |
| Martin Oberhuber   (Wind River) |
| RSE ssh |   org.eclipse.rse.connectorservice.ssh   org.eclipse.rse.services.ssh   org.eclipse.rse.ssh-feature   org.eclipse.rse.subsystems.files.ssh   org.eclipse.rse.subsystems.shells.ssh   |   |
| RSE local |   org.eclipse.rse.connectorservice.local   org.eclipse.rse.local-feature   org.eclipse.rse.services.local   org.eclipse.rse.subsystems.files.local   org.eclipse.rse.subsystems.processes.local   org.eclipse.rse.subsystems.shells.local   | Kushal Munir |
| RSE examples |   org.eclipse.rse.examples.daytime   org.eclipse.rse.examples.tutorial      | Dave Dykstal |
| RSE content assist | org.eclipse.rse.shells.ui/org.eclipse.rse.shells.ui.view | Dave McKnight |
|   RSE nightly builds,   Legal docs (about files, licenses),   Update Site,   build notes   |   org.eclipse.rse.build   org.eclipse.rse.core-feature   org.eclipse.rse.dstore-feature   org.eclipse.rse.efs-feature   org.eclipse.rse.examples-feature   org.eclipse.rse.remotecdt-feature   org.eclipse.rse.sdk   org.eclipse.rse.sdk-feature   org.eclipse.rse.releng.infocenter   org.eclipse.rse.updatesite   |   Ted Williams,   Dave Dykstal   |
| Third Party Libs   (Jakarta Commons Net, ORO) |   org.eclipse.tm.core/thirdparty/*   |   Dave Dykstal   |
| RSE manual tests | org.eclipse.rse.tests.manual |   |
| Javier Montalvo   (Symbian) | Discovery | (org.eclipse.tm.core) discovery/* |   |
| RSE ftp |   org.eclipse.rse.ftp-feature   org.eclipse.rse.services.files.ftp   org.eclipse.rse.subsystems.files.ftp   |   Dave McKnight,   Martin Oberhuber   |
| Michael Scharf   (Wind River) | Terminalview | (org.eclipse.tm.core) terminal/* | Ted Williams |
| Ewa Matejska   (ACCESS) | CDT Remote Launch |   org.eclipse.rse.remotecdt   | Martin Oberhuber |
| Radoslav Gerganov   (ProSyst) | WinCE subsystems |   org.eclipse.tm.core/wince/*   | Martin Oberhuber |
| Anna Dushistova   (MontaVista) | RSE terminal subsystems |   org.eclipse.rse.terminal.*   | Martin Oberhuber |


(Migrated from [https://wiki.eclipse.org/TM/Code_Ownership](https://wiki.eclipse.org/TM/Code_Ownership))