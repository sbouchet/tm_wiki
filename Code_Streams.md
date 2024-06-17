

TM/Code Streams
===============

< [TM](/TM "TM")

This page lists the open code streams in the [RSE / Target Management Project](https://www.eclipse.org/tm), and how to work with them.

Contents
--------

*   [1 Build Schedule](#Build-Schedule)
*   [2 Streams](#Streams)
    *   [2.1 Juno (TM 3.4)](#Juno-.28TM-3.4.29)
    *   [2.2 Indigo (3.3.x)](#Indigo-.283.3.x.29)
    *   [2.3 Helios (3.2.x)](#Helios-.283.2.x.29)
    *   [2.4 Galileo (3.1.x)](#Galileo-.283.1.x.29)
    *   [2.5 Ganymede (3.0.x)](#Ganymede-.283.0.x.29)

Build Schedule
==============

\# I-builds (TM 3.4 Juno) weekdays at 1:30 and 9:00
30 1 * * 1-5    /shared/tools/tm/ws2/doit_irsbuild.sh I
00 9 * * 1-5    /shared/tools/tm/ws2/doit_irsbuild.sh I

\# H-builds (TM 3.3.x Indigo) weekdays at 10:00
00 10 * * 1-5   /shared/tools/tm/ws\_33x/doit\_irsbuild.sh H

\# M-builds (TM 3.2.x Helios) weekdays at 11:00
00 11 * * 1-5   /shared/tools/tm/ws\_32x/doit\_irsbuild.sh M

\# J-builds (TM 3.1.x Galileo) weekdays at 12:00
00 12 * * 1-5   /shared/tools/tm/ws\_31x/doit\_irsbuild.sh J

\# L-builds (TM 3.0.x Ganymede) weekdays at 13:00
00 13 * * 1-5   /shared/tools/tm/ws\_30x/doit\_irsbuild.sh L

Streams
=======

Juno (TM 3.4)
-------------

Juno development should be done against **Eclipse 4.2** although our tests should validate that TM runs against 3.x as well.

*   Required Plugins for Terminal (these are not needed for plain RSE):
    *   Egit team provider ([Update Site](http://download.eclipse.org/egit/updates)) \- project set support requires Eclipse 4.2 or later
    *   For TM-Terminal-Serial: RXTX ([Update Site](http://rxtx.qbang.org/eclipse/) | [ZIP Download](http://rxtx.qbang.org/eclipse/downloads/))
    *   For TM-Terminal-Local: org.eclipse.cdt.core ([CDT Downloads](http://eclipse.org/cdt/downloads.php))
    *   For TM-Terminal CDC execution environment: [J9](/J9 "J9") CDC-1.1/Foundation-1.1 environment, registered via its .ee file
*   Workspace setup
    *   Read [TM/Git Workflows](/TM/Git_Workflows "TM/Git Workflows") for setup
    *   Preferences : Java : Installed JRE's: Add JRE's for J2SE-1.5, J2SE-1.4 (and CDC-1.1/Foundation-1.1 for Terminal)
    *   Preferences : PDE : Download, extract and register [tm\_3.4\_api_baseline.zip](http://archive.eclipse.org/tm/downloads/tm_3.4_api_baseline.zip)
    *   File > Import > Team > Team Project Set: [tm-all-juno.psf](https://www.eclipse.org/tm/development/tm-all-juno.psf)
*   This is the current HEAD stream.
*   Mapfile project: **org.eclipse.tm.releng**
    *   Map projects as well as bundles are used from HEAD until further notice
    *   Release tags: **v201010060830** or similar

Indigo (3.3.x)
--------------

*   Team Project Set: [tm-all-indigo.psf](https://www.eclipse.org/tm/development/tm-all-indigo.psf)
*   Branch name: **R3\_3\_maintenance**
*   Release tags: **R33x_v201106281309** or similar
*   Mapfile project: **org.eclipse.tm.releng** branch **R3\_3\_maintenance**
    *   For feature version updates, use **org.eclipse.rse.updatesite** branch R3\_3\_maintenance.
    *   Build scripts are in **org.eclipse.rse.build** branch R3\_3\_maintenance.
*   Dependencies: Platform 3.7, [RXTX](http://rxtx.qbang.org/eclipse/downloads/) for Terminal-serial, [CDT 8.0](http://eclipse.org/cdt/downloads.php) or later for Terminal-local.
*   API Baseline: [tm\_3.3\_api_baseline.zip](http://archive.eclipse.org/tm/downloads/tm_3.3_api_baseline.zip)

To branch a new plugin for 3.3.x development,

*   Team > Switch to another branch or version: **R3\_3\_1** first, then
*   Team > Branch, **R3\_3\_maintenance**
*   When releasing, use the Platform Releng tool. Ensure that your Mapfile project is on the **R3\_3\_maintenance** branch.

Helios (3.2.x)
--------------

*   Team Project Set: [tm-all-helios.psf](https://www.eclipse.org/tm/development/tm-all-helios.psf)
*   Branch name: **R3\_2\_maintenance**
*   Release tags: **R32x_v201010060830** or similar
*   Mapfile project: **org.eclipse.rse.build** branch **R3\_2\_maintenance**
*   Dependencies: Platform 3.6, [RXTX](http://rxtx.qbang.org/eclipse/downloads/) for Terminal-serial, [CDT 7.0](http://download.eclipse.org/tools/cdt/builds/) or later for Terminal-local, [EMF 2.4](https://www.eclipse.org/modeling/emf/downloads/?project=emf) or later for Discovery, [Subversive](http://eclipse.org/subversive/) for importing the TCF team projects
*   API Baseline: [tm\_3.2\_api_baseline.zip](http://archive.eclipse.org/tm/downloads/tm_3.2_api_baseline.zip)

Galileo (3.1.x)
---------------

*   Team Project Set: [tm-all-galileo.psf](https://www.eclipse.org/tm/development/tm-all-galileo.psf)
*   Branch name: **R3\_1\_maintenance**
*   Release tags: **R31x_v201006030845** or similar
*   Dependencies: Platform 3.5, [RXTX](http://rxtx.qbang.org/eclipse/downloads/) for Terminal-serial, [CDT 6.0](http://download.eclipse.org/tools/cdt/builds/) or later for Remotecdt, [EMF 2.4](https://www.eclipse.org/modeling/emf/downloads/?project=emf) or later for Discovery
*   API Baseline: [tm\_3.1.1\_api_baseline.zip](http://archive.eclipse.org/tm/downloads/tm_3.1.1_api_baseline.zip)

Ganymede (3.0.x)
----------------

*   Team Project Set: [tm-all-ganymede.psf](https://www.eclipse.org/tm/development/tm-all-ganymede.psf)
*   Branch name: **R3\_0\_maintenance**
*   Release tags: **v201010060830** or similar
*   Dependencies: Platform 3.4, [RXTX](http://rxtx.qbang.org/eclipse/downloads/) for Terminal-serial, [CDT 5.0](http://download.eclipse.org/tools/cdt/builds/) or later for Remotecdt, [EMF 2.4](https://www.eclipse.org/modeling/emf/downloads/?project=emf) or later for Discovery
*   API Baseline: [tm\_3.0.1\_baseline_plugins.zip](http://archive.eclipse.org/tm/downloads/tm_3.0.1_baseline_plugins.zip)


(Migrated from [https://wiki.eclipse.org/TM/Code_Streams](https://wiki.eclipse.org/TM/Code_Streams))