

TM 3.0 RC2 Testing
==================

Nav: [DSDP/TM](./TM "DSDP/TM") | [DSDP/TM/Testing](./Testing "DSDP/TM/Testing") | [TM 3.0 Testing](./TM_3.0_Testing "TM 3.0 Testing") | TM 3.0 RC2 Testing | [TM 2.0 Test Instructions](./TM_2.0_Test_Instructions "TM 2.0 Test Instructions") | [TM 2.0 Known Issues and Workarounds](./TM_2.0_Known_Issues_and_Workarounds "TM 2.0 Known Issues and Workarounds") | [TM Manual Test Plan](./TM_Manual_Test_Plan "TM Manual Test Plan")

* * *

This is the master coordination page for TM 3.0 RC2 Testing. Testing will run from Wednesday 28-May-2008 to 5:00 p.m. (EDT) Friday 30-May-2008. RC2 will be built on Tuesday 27 May 2008. Please sign up here for testing particular features, or a particular host/target combination. It is important for all of us to coordinate our efforts

*   In order to get critical bugs submitted early so that we can fix them for RC3
*   In order to avoid duplication of testing work
*   In order to get a good test coverage and exposure of TM / RSE.

  

Contents
--------

*   [1 Organization](#Organization)
*   [2 Signup Matrix](#Signup-Matrix)
*   [3 Install Scenarios](#Install-Scenarios)
*   [4 Features](#Features)
    *   [4.1 RSE](#RSE)
        *   [4.1.1 Not to be tested](#Not-to-be-tested)
*   [5 Platforms](#Platforms)
    *   [5.1 Client](#Client)
    *   [5.2 Target](#Target)

Organization
------------

The main focus is a good round of **Sanity Test** to find **obvious showstoppers**.

*   [Bugs fixed for 3.0 but not yet verified](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=RESOLVED&resolution=FIXED&resolution=WORKSFORME&chfieldfrom=2007-09-29&chfieldto=2008-05-28&chfield=resolution&chfieldvalue=&cmdtype=doit)

Most of you took part in an earlier round of testing already, so you'll not need to read all of the [TM 2.0 Test Instructions](./TM_2.0_Test_Instructions "TM 2.0 Test Instructions"). Here is some important information for this round of testing:

*   Please use a customized bug entry template again. If you already have one from an earlier round of testing, change it to "3.0RC3 Testing" and save it as your new bookmark for this round of testing. Otherwise, use [this link to show, modify and save a sample bug entry template](https://bugs.eclipse.org/bugs/enter_bug.cgi?product=Target%20Management&version=3.0&component=RSE&comment=%0D%0A-----------Enter%20bugs%20above%20this%20line-----------%0D%0ATM%203.0RC2%20Testing%0D%0Ainstallation%20%3A%20eclipse-SDK-3.4RC2-win32%2C%20cdt-5.0.0RC2%2C%20emf-sdo-xsd-2.4.0RC2%0D%0A%20%20%20%20%20Download%20RSE-RC2%3A%20RSE-SDK%2Ctests%2Cdiscovery%2Cterminal%2Cremotecdt%0D%0Ajava.runtime%20%3A%20Sun%201.5.0_11-b03%2C%20mixed%20mode%0D%0Aos.name%3A%20%20%20%20%20%3A%20Windows%20XP%205.1%2C%20Service%20Pack%201%0D%0A------------------------------------------------%0D%0Asystemtype%20%20%20%3A%20Linux-local%20%2F%20Windows-dstore%20%28Daemon%29%20%2F%20Unix-dstore%20%28RExec%29%0D%0Atargetos1%20%20%20%20%3A%20Linux%20RHEL4%2C%20Sun%201.5.0_11%0D%0Atargetos2%20%20%20%20%3A%20Windows%20XP%20SP1%2C%20Sun%201.5.0_11%0D%0Atargetos3%20%20%20%20%3A%20Solaris-sparc%205.9%2C%20Sun%201.4.2_05%0D%0Atargetuname%20%20%3A%20SunOS%20szg-anar%205.9%20Generic_118558-06%20sun4u%20sparc%20SUNW%2CSun-Blade-1500%0D%0A------------------------------------------------%0D%0A&form_name=enter_bug). The point here is that we'd like to know your JVM version / OS version.
*   Downloads to test are [at the TM download page](http://download.eclipse.org/dsdp/tm/downloads/index.php), [TM S-3.0RC2-200805271940](http://download.eclipse.org/dsdp/tm/downloads/drops/S-3.0RC2-200805271940/)
*   Official Test Platform is the RC2 release from the [Eclipse Platform](http://download.eclipse.org/eclipse/downloads/).
*   Updates Site to test is at [http://download.eclipse.org/dsdp/tm/testUpdates](http://download.eclipse.org/dsdp/tm/testUpdates)
*   Ganymede Integration Staging Site is at [http://download.eclipse.org/releases/ganymede/staging](http://download.eclipse.org/releases/ganymede/staging)
*   Known issues are at [TM 3.0 Known Issues and Workarounds](./3.0_Known_Issues_and_Workarounds "TM 3.0 Known Issues and Workarounds")
    *   Currently open [major, critical, blocker](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit) issues
    *   Currently open [bugs assigned to 3.0RC2](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=&classification=DSDP&product=Target+Management&target_milestone=3.0+RC2&long_desc_type=allwordssubstr&long_desc=&bug_file_loc_type=allwordssubstr&bug_file_loc=&status_whiteboard_type=allwordssubstr&status_whiteboard=&keywords_type=allwords&keywords=&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&emailtype1=substring&email1=&emailtype2=substring&email2=&bugidtype=include&bug_id=&votes=&chfieldfrom=&chfieldto=Now&chfieldvalue=&cmdtype=doit&order=Reuse+same+sort+as+last+time&field0-0-0=noop&type0-0-0=noop&value0-0-0=)
    *   Currently open [bugs detected during testing](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&chfieldfrom=2008-05-28&chfieldto=2008-05-30&chfield=%5BBug+creation%5D&cmdtype=doit)

*   **Sanity check instructions:** please use RSE in a "normal" way as you'd usually use it. [RSE 1.0 Test Instructions](./RSE_1.0_Test_Instructions#Step_5:_Basic_Sanity_Check "RSE 1.0 Test Instructions"). Please test on your selected host/target combination. Try to avoid duplication with others. Report any bad behavior.

**Thanks** to everybody who signs up and thus helps making RSE better!

Signup Matrix
-------------

| Tester Name (Company) | Client Platform | Connection types | RSE Features | Comments |
| --- | --- | --- | --- | --- |
| Dave Dykstal (IBM) | MacOS X 10.5.2 | dstore-mac | Macintosh related. "Team" view. Persistence & model features (filters, filter pools, ...). Import Export. Basic Sanity Testing. Documentation Review. File operations. | none |
| Martin Oberhuber (Wind River) | Solaris 10, Sun 1.5.0_11 | Local | Custom / dynamic system types, filters, actions | none |
| Dave McKnight (IBM) |  |  |  |  |
| Xuan Chen (IBM) | Windows XP, IBM 1.6 JRE | Local, dstore-linux | Sanity Test + User actions + some tryout for Import/Export connections + ftp on I5/OS system |  |
| Kevin Doyle (IBM) | Windows XP | dstore-linux | Sanity Test + verifying bugs | none |
| Rupen Mardirossian (IBM) |  |  |  |  |
| Uwe Stieber (Wind River) |  |  |  |  |
| Felix Burton (Wind River) |  |  |  |  |
| Michael Scharf (Wind River) |  |  |  |  |
| Eugene Tarassov (Wind River) |  |  |  |  |
| Javier Montalvo-Orus () |  |  |  |  |
| Radoslav Gerganov (ProSyst) | Win2k SP4, Sun 1.6.0_05 | ftp | Basic Sanity Test, EFS, Dirty Editors and Merging, File Access Permissions and Timestamps | none |
| Anna Dushistova (Montavista) | SuSE Linux 10.1, Sun 1.5.0_06 | ssh | Remotecdt Launch, Processes subsystem | none |

Install Scenarios
-----------------

Need to test all scenarios, see [bug 231453](https://bugs.eclipse.org/bugs/show_bug.cgi?id=231453)

1\. (standard) TM 3.0 ZIPs into Eclipse-SDK 3.4 dropins/ (including emf, remotecdt)

2\. **Martin** TM 3.0 ZIPs into Eclipse-SDK 3.3.2 (with EMF-2.2.4, CDT-3.1)

3\. **Martin** TM-Updatesite-P2: Eclipse-platform-3.4 plus EMF-2.2.4 from ZIPs; get CDT from CDT-Site; get TM from TM-site

4\. **DaveD** Ganymede-P2: Start from Eclipse-platform-3.4 plain, select TM-all on Ganymede-site, have CDT+EMF autoselectd for install

5\. Update TM-3.0rc3 to TM-3.0rc3++: With the install from (4), "Check for Updates" to ensure get latest TM

6\. **Martin** Update TM-2.0 to TM-3.0 (old UM): Given Eclipse-3.3.2, EMF-2.3.2, CDT-4.0.2; Update to TM 3.0 only by pointing to TM site

Features
--------

### RSE

*   Verifications: [3.0 Bugs (by date) fixed but not yet verified](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=RESOLVED&resolution=FIXED&resolution=WORKSFORME&chfieldfrom=2007-06-29&chfieldto=2008-05-28&chfield=resolution&chfieldvalue=&cmdtype=doit)
*   **Xuan** Import/Export Connections
*   [Basic Sanity Test](./TM_Manual_Test_Plan#Basic_Sanity_Test "TM Manual Test Plan") (File Subsystem, dirlist, simple filters, upload/download/edit, Tableview)
*   [File Encodings](./TM_Manual_Test_Plan#File_Encodings "TM Manual Test Plan") (Foreign language files on remote side)
*   [CDT Remote Launch](./TM_Manual_Test_Plan#CDT_Remote_Launch "TM Manual Test Plan")
*   [Drag&Drop, Copy&Paste](./TM_Manual_Test_Plan#Drag.26Drop.2C_Copy.26Paste "TM Manual Test Plan") (RSE <-> RSE, Eclipse Navigator, Windows Explorer, Overwrite vs. Rename)
*   [Discovery](./TM_Manual_Test_Plan#Discovery "TM Manual Test Plan")
*   [EFS](./TM_Manual_Test_Plan#EFS "TM Manual Test Plan")
*   [Dstore Launch Options](./TM_Manual_Test_Plan#Dstore_Launch_Options "TM Manual Test Plan") (Rlogin, Already-Running, Port Ranges, SSL Connection)
*   [Parallel access](./TM_Manual_Test_Plan#Parallel_access "TM Manual Test Plan") (multiple parallel actions)
*   [Update Site](./TM_Manual_Test_Plan#Update_Site "TM Manual Test Plan"): Install & Upgrade via Update Site (using P2)
*   [Scalability](./TM_Manual_Test_Plan#Scalability "TM Manual Test Plan") (Really large file lists, lots of events)
*   [Processes Subsystem](./TM_Manual_Test_Plan#Processes_Subsystem "TM Manual Test Plan") (List, Sort, Kill, Remote Monitor)
    *   MV Shell Processes Subsystem
*   [Verify Extension Points](./TM_Manual_Test_Plan#Verify_Extension_Points "TM Manual Test Plan") (Check docs, use in own code)
*   [Remote Search](./TM_Manual_Test_Plan#Remote_Search "TM Manual Test Plan") (dstore only)
*   [Complex Filters](./TM_Manual_Test_Plan#Complex_Filters "TM Manual Test Plan") (Multiple filter strings, Filter by filetype, Filter Persistence...)
*   [Preferences](./TM_Manual_Test_Plan#Preferences "TM Manual Test Plan") (Walk through each of the Preferences and enable/disable)
*   [Subsystem Properties](./TM_Manual_Test_Plan#Subsystem_Properties "TM Manual Test Plan") (Changing Properties of Systems/Subsystems in the RSE Tree)
*   [Synchronous operation](./TM_Manual_Test_Plan#Synchronous_operation "TM Manual Test Plan") (Do a sanity check with "Deferred Queries" switched off in Preferences)
*   [Dirty Editors and Merging](./TM_Manual_Test_Plan#Dirty_Editors_and_Merging "TM Manual Test Plan") (Editing a Remote File that also changes remotely)
*   [File Access Permissions and Timestamps](./TM_Manual_Test_Plan#File_Access_Permissions_and_Timestamps "TM Manual Test Plan") (Read-only files etc.)
*   [RSE Views](./TM_Manual_Test_Plan#RSE_Views "TM Manual Test Plan"): Treeview, Tableview, Monitor, Properties, Scratchpad, Editor, Compare (Check for consistency)
*   [RSE Widgets & Dialogs](./TM_Manual_Test_Plan#RSE_Widgets_.26_Dialogs "TM Manual Test Plan"): Remote file-browse, Remote move-to
*   [Connection Problems](./TM_Manual_Test_Plan#Connection_Problems "TM Manual Test Plan") (Very slow connections, unavailable/unreliable hosts, timeouts, breaking connections)
*   [Team Support](./TM_Manual_Test_Plan#Team_Support "TM Manual Test Plan") (Connection Profiles)
*   [Verify User Docs](./TM_Manual_Test_Plan#Verify_User_Docs "TM Manual Test Plan") (Walk through tutorial, Context Help, Check Links, Search feature)
*   [Verify ISV Tutorial](./TM_Manual_Test_Plan#Verify_ISV_Tutorial "TM Manual Test Plan") (Walk through ISV tutorial)
*   [Verify ISV Docs](./TM_Manual_Test_Plan#Verify_ISV_Docs "TM Manual Test Plan") (Broken Links, Semantic correctness, Searchable docs, Useful Javadoc)
*   [Shell Content Assist-Linux](./TM_Manual_Test_Plan#Shell_Content_Assist-Linux "TM Manual Test Plan") (local,ssh,dstore)
*   [Shell Content Assist-Windows](./TM_Manual_Test_Plan#Shell_Content_Assist-Windows "TM Manual Test Plan") (local,dstore)
*   [Shell Pattern Matching](./TM_Manual_Test_Plan#Shell_Pattern_Matching "TM Manual Test Plan") (Compiler Error Navigation, Directory and File Navigation)

#### Not to be tested

*   [Verify Copyright and Externalized Strings](./TM_Manual_Test_Plan#Verify_Copyright_and_Externalized_Strings "TM Manual Test Plan") (Run automated checks, chkpii)
*   [Verify Legal](./TM_Manual_Test_Plan#Verify_Legal "TM Manual Test Plan") (Feature Descriptions, Licenses in all source features, Overall license)

Platforms
---------

### Client

Please fill in your client and java version. Feel free to move yourself around in this table to match your current set up.

| Windows XP | MartinO (SP1; Sun1.4.2\_14); MichaelScharf (SP2; Sun1.5.0\_07) |
| --- | --- |
| Linux-x86-gtk | MartinO (RHEL4, Sun1.6.0\_01); DaveM (SLES9, IBM1.4.2\_sr3); Anna (Suse 10.1, Sun 1.5.0_06) |
| Linux-x86_64-gtk | UweS (openSUSE 10.2, Sun 1.5.0_10 (64Bit)) |
| Solaris-gtk | MartinO (Solaris9, Sun 1.5.0_11); |
| Mac OS X | DaveD (10.5.2, Sun1.5.0_13) |
| Linux-ppc-gtk |  |
| Linux-Motif |  |
| AIX |  |

### Target

Please edit your current set up.

| Windows-dstore | MartinO (XP-SP1, Sun1.4.2\_14); MichaelScharf (XP-SP1, Sun1.5.0\_07); |
| --- | --- |
| Windows-ssh |  |
| Windows-ftp | JavierM (FileZilla 0.9.8b); MichaelScharf (GNU inetutils 1.3.2); Rado (FileZilla 0.9.25 beta) |
| Linux-dstore | MartinO (RHEL4, Sun1.4.2\_13); NorbertP (SUSE10.0; Sun1.4.2\_06); UweS (SUSE10.1; Sun1.5.0_07); MichaelScharf (SUSE10.1; Sun1.6.0-beta2); |
| Linux-ssh | MartinO (RHEL4); MartinO (SUSE Enterprise 10 PPC); UweS (SUSE10.1); MichaelScharf (SUSE10.1); Rado (Debian sarge); Anna (SUSE10.1) |
| Linux-ftp | MichaelScharf (SUSE10.1); EwaM (Ubuntu6.10); |
| Solaris-dstore | MartinO (Sol9, Sun1.5.0\_11); MartinO (Sol10, Sun1.5.0\_11) |
| Solaris-ssh | MartinO (Sol9); |
| Solaris-ftp |  |
| HPUX-dstore |  |
| HPUX-ssh | SumitS (HP-UX11.11); |
| HPUX-ftp |  |
| AIX-dstore |  |
| AIX-ssh |  |
| AIX-ftp |  |
| MacOSX-dstore | DaveD (10.5.2, Sun1.5.0_13); |
| MacOSX-ssh | DaveD (10.5.2, Sun1.5.0_13); |
| MacOSX-ftp | DaveD (10.5.2, Sun1.5.0_13); |
| VMS-ftp |  |
| MVS-ftp |  |
| VxWorks-ftp | MartinO (VxSim SIMNT 6.4) |


(Migrated from [https://wiki.eclipse.org/TM_3.0_RC2_Testing](https://wiki.eclipse.org/TM_3.0_RC2_Testing))