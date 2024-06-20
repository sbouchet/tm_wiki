

TM 2.0 M5 Testing results mob
=============================

Contents
--------

*   [1 Windows X dstore](#Windows-X-dstore)
*   [2 Linux X dstore](#Linux-X-dstore)
*   [3 Found through Code Review](#Found-through-Code-Review)
*   [4 Bugs for EclipseCon](#Bugs-for-EclipseCon)

Windows X dstore
----------------

Verification FAILED during TM 2.0M5 Testing: WinXP SP1, Sun 1.4.2_13, Eclipse-SDK-3.3M5, RSE-SDK I20070219-1615:

*   Download Eclipse 3.3M5, CDT 4.0M5 SDK, EMF 2.3M5 Runtime, RSE 2.0M5 SDK
*   [142712](https://bugs.eclipse.org/bugs/show_bug.cgi?id=142712) REOPEN: No filters on connection in team profile
*   [174771](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174771) NEW Critical: New Connection Wizard works only on 1st invocation
*   [174772](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174772) NEW Enhancement: FTP should do passive mode by default
*   [174774](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174774) NEW Regression: ClassCastException in monitor
*   [174775](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174775) NEW Regression: InvalidThreadAccess in monitor
*   [174776](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174776) NEW Minor: Filter shown twice after creation
*   [174778](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174778) NEW Regression: \[dstore\] Rexec Launcher from New Connection Wizard is not accepted
*   [174789](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174789) NEW \[api\] subsystem wizard pages should not be contributed automatically from property pages
*   [174790](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174790) NEW Minor: icons for TestSubsystem are broken
*   [174948](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174948) NEW Minor: \[terminal-ssh\] Terminal asks for host key
*   [174949](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174949) NEW \[terminal-ssh\] Connection fails consistently after previous timeout
*   [174951](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174951) NEW \[terminal-ssh\] Network Timeout Preferences not considered
*   [174953](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174953) NEW Major: \[terminal\] connect consistently fails after a failed telnet connect
*   [174955](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174955) NEW Minor: \[terminal-ssh\] Terminal doesnt disconnect when typing "exit"

Linux X dstore
--------------

*   Eclipse-platform 3.3M5
*   Update-Site Eclipse-CVS, CDT-4.0M5, EMF-2.3M5
*   Update-Site RSE-Runtime-All, Terminal, Discovery, Remotecdt
*   [174795](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174795) NEW Minor: Update Site asks about optional features
*   [174796](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174796) NEW Minor: Cannot install Terminal from update site on Platform without CVS

  

Found through Code Review
-------------------------

*   [174941](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174941) NEW \[api\] Get rid of AbstractConnectorServiceManager.updateSubSystems(), sharesSystem()
*   [174945](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174945) NEW get rid of unused icons, files and properties

Bugs for EclipseCon
-------------------

*   [174944](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174944) NEW Normal: SystemRemoteFolderDlg.setPreSelection() does not work


(Migrated from [https://wiki.eclipse.org/TM_2.0_M5_Testing_results_mob](https://wiki.eclipse.org/TM_2.0_M5_Testing_results_mob))