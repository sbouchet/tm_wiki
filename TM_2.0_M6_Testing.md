

TM 2.0 M6 Testing
=================

Nav: [DSDP/TM](./DSDP/TM "DSDP/TM") | [DSDP/TM/Testing](./DSDP/TM/Testing "DSDP/TM/Testing") | [TM 2.0 Testing](./TM_2.0_Testing "TM 2.0 Testing") | TM 2.0 M6 Testing | [TM 2.0 Test Instructions](./TM_2.0_Test_Instructions "TM 2.0 Test Instructions") | [TM 2.0 Known Issues and Workarounds](./TM_2.0_Known_Issues_and_Workarounds "TM 2.0 Known Issues and Workarounds") | [TM Manual Test Plan](./TM_Manual_Test_Plan "TM Manual Test Plan")

* * *

This is the master coordination page for TM 2.0 M6 Testing, to be done with Target Management 2.0 M6, 3-Apr-2007. Please sign up here for testing particular features of TM 2.0 M6, or a particular host / target combination. It is important for all of us to coordinate our efforts

*   In order to get bugs submitted early, such that we can fix them for the release
*   In order to avoid duplication of testing work
*   In order to get a good test coverage and exposure of TM / RSE.

  

Contents
--------

*   [1 Organization and Signup](#Organization-and-Signup)
*   [2 Test Matrix](#Test-Matrix)
    *   [2.1 Test Features](#Test-Features)
        *   [2.1.1 RSE Features signed up already](#RSE-Features-signed-up-already)
        *   [2.1.2 RSE Features that are particularly important to test](#RSE-Features-that-are-particularly-important-to-test)
        *   [2.1.3 RSE Features to test](#RSE-Features-to-test)
        *   [2.1.4 Features **not to be tested** this time](#Features-not-to-be-tested-this-time)
    *   [2.2 Client Platforms](#Client-Platforms)
    *   [2.3 Target Platforms](#Target-Platforms)
*   [3 Test Reports and Bugs Found](#Test-Reports-and-Bugs-Found)

Organization and Signup
-----------------------

The main focus in this round of testing is to find **obvious showstoppers**, and to **verify** the integration into the Europa Coordinated Update Site (**Note: we need to use the Staging site for testing, see below**).

Most of you took part in an earlier round of testing already, so you'll not need to read all of the [TM 2.0 Test Instructions](./TM_2.0_Test_Instructions "TM 2.0 Test Instructions"). Here is some important information for this round of testing:

*   Please use a customized bug entry template again. If you already have one from an earlier round of testing, change "2.0M5 Testing" into "2.0M6 Testing" and save it as your new bookmark for this round of testing. Otherwise, use [this link to show, modify and save a sample bug entry template](https://bugs.eclipse.org/bugs/enter_bug.cgi?product=Target%20Management&version=2.0&component=RSE&comment=%0D%0A-----------Enter%20bugs%20above%20this%20line-----------%0D%0ATM%202.0M6%20Testing%0D%0Ainstallation%20%3A%20eclipse-platform-3.3M6%20%28I200703__-____%29%2C%20cdt-4.0M6%2C%20emf-2.3M6%0D%0ARSE%20install%20%20%3A%20update-site%20RSE-runtime-all%20%2B%20discovery%20%2B%20efs%0D%0Ajava.runtime%20%3A%20Sun%201.5.0_11-b03%0D%0Aos.name%3A%20%20%20%20%20%3A%20Windows%20XP%205.1%2C%20Service%20Pack%202%0D%0A------------------------------------------------%0D%0Asystemtype%20%20%20%3A%20Unix-ssh%20%28dstore-processes%29%0D%0Atargetos%20%20%20%20%20%3A%20SUSE%20LINUX%2010.1%20%28i586%29%0D%0Atargetuname%20%20%3A%20Linux%20osgiliath%202.6.16.21-0.21-default%20%231%20Tue%20Aug%2029%2016%3A42%3A05%20UTC%202006%20i686%20athlon%20i386%20GNU%2FLinux%0D%0Atargetvm%20%20%20%20%20%3A%20Sun%20Java%20HotSpot%28TM%29%20Client%20VM%20%28build%201.5.0_07-b03%2C%20mixed%20mode%2C%20sharing%29%0D%0A------------------------------------------------%0D%0A&form_name=enter_bug).
*   If possible, please use the JDK versions as signed up in the table below. These are chosen to comply with our [Reference Platforms and JDK versions](https://www.eclipse.org/dsdp/tm/development/plan.php#OperatingEnvironments). Edit the table below if you need to use a different JDK version.
*   Downloads to test are at [I20070406-0930](http://download.eclipse.org/dsdp/tm/downloads/drops/I20070406-0930)
    *   Official Test Platform is **[Eclipse 3.3M6](http://download.eclipse.org/eclipse/downloads/drops/S-3.3M6-200703231616/index.php)** (with use [CDT 4.0.0M6](http://download.eclipse.org/tools/cdt/releases/europa/dist/4.0.0M6) for remotecdt and [EMF 2.3.0M6](http://download.eclipse.org/modeling/emf/emf/downloads/drops/2.3.0/S200703291501) for discovery if you want to test those).
    *   Eclipse 3.2 has problems displaying Property Pages for subsystems so we **do not support it**.
    *   Some scripts that make the job of downloading RSE easier have been [published on the mailing list](http://dev.eclipse.org/mhonarc/lists/dsdp-tm-dev/msg01065.html).
*   Updates Site to test is at [http://download.eclipse.org/dsdp/tm/testUpdates](http://download.eclipse.org/dsdp/tm/testUpdates)
    *   Europa Integration Site will be at [http://download.eclipse.org/releases/europa/staging](http://download.eclipse.org/releases/europa/staging) (we are not integrated yet)
*   Known issues are at [TM 2.0 Known Issues and Workarounds](./TM_2.0_Known_Issues_and_Workarounds "TM 2.0 Known Issues and Workarounds")
    *   Currently open [major, critical, blocker](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit) issues
    *   Currently open [bugs assigned to M6](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=target_milestone&y_axis_field=assigned_to&query_format=report-table&classification=DSDP&product=Target+Management&target_milestone=2.0+M6&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&format=table&action=wrap)
    *   Currently open [bugs detected during testing](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&chfieldfrom=2007-04-03&chfieldto=2007-04-08&chfield=%5BBug+creation%5D&cmdtype=doit)
*   Components affected by fixes for [I20070406-0930](http://download.eclipse.org/dsdp/tm/downloads/drops/I20070406-0930):
    *   **Filters** [181394](https://bugs.eclipse.org/bugs/show_bug.cgi?id=181394) filter shows data from wrong connection
    *   **EFS** [180091](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180091) Use handles to fix EFS project on workbench startup; [177323](https://bugs.eclipse.org/bugs/show_bug.cgi?id=177323) No query from EFS on workbench shutdown; [180874](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180874) Progress monitor for Create Remote Project; [170916](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170916) get rid of separate EFS feature
    *   **Update Site** [175341](https://bugs.eclipse.org/bugs/show_bug.cgi?id=175341)\[nls\] Add NLS strings for tmMilestoneUpdateSite in features
*   Components affected by fixes for [I20070405-1810](http://download.eclipse.org/dsdp/tm/downloads/drops/I20070405-1810):
    *   **Copy&Paste** [181197](https://bugs.eclipse.org/bugs/show_bug.cgi?id=181197) avoid empty list after copy remote -> local
    *   **Remote Browse Dialog** [181222](https://bugs.eclipse.org/bugs/show_bug.cgi?id=181222) prevent null set on SaveAsForm; [181222](https://bugs.eclipse.org/bugs/show_bug.cgi?id=181222) for SystemResoruceSelectionInputProvider (used by file dialog) the initial connection should be set;
    *   **API** [180602](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180602) \[api\] Remove remaining messages for Communications Daemon; [1590939](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150939) added readOnly attribute to IProperty; \[cleanup\] make IRSEDOMExporter & IRSEDOMImporter internal, add package.html;
*   Components affected by fixes for [I20070405-1200](http://download.eclipse.org/dsdp/tm/downloads/drops/I20070405-1200):
    *   **SSH, Update Site** [175686](https://bugs.eclipse.org/bugs/show_bug.cgi?id=175686) Get rid of Platform CVS Dependency;
    *   **Persistence** [177882](https://bugs.eclipse.org/bugs/show_bug.cgi?id=177882) Fixed PropertyFileProvider for garbling of CJK characters
    *   **Dstore Persistence** [181069](https://bugs.eclipse.org/bugs/show_bug.cgi?id=181069) getContextString() for saving shell states;
    *   **API** [179184](https://bugs.eclipse.org/bugs/show_bug.cgi?id=179184) changed preference name to DEFAULT\_PERSISTENCE\_PROVIDER;
*   Components affected by fixes for [I20070405-0600](http://download.eclipse.org/dsdp/tm/downloads/drops/I20070405-0600):
    *   **Dstore Reconnect** [\[1\]](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180994) clean up environment miner variables
    *   **Dstore Shell** [\[2\]](https://bugs.eclipse.org/bugs/show_bug.cgi?id=181006) asynch exec job to avoid endless looping of dstore shell
    *   **API** [\[3\]](https://bugs.eclipse.org/bugs/show_bug.cgi?id=179184)\[api\] Default Persistence Provider Preference; [\[4\]](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180642) make test scripting internal; [\[5\]](https://bugs.eclipse.org/bugs/show_bug.cgi?id=166339) deprecating getVendorAttributes and setVendorAttributes; [\[6\]](https://bugs.eclipse.org/bugs/show_bug.cgi?id=150931)\[api\] added setDescription() method
*   Components affected by fixes for [I20070405-0600](http://download.eclipse.org/dsdp/tm/downloads/drops/I20070405-0600):
    *   **FTP Download** [\[7\]](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180711)\[ftp\] copying files in multiple threads
    *   **Subsystem Properties** [\[8\]](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180933) fix dstore subsystem property pages and discovery.edit/plugin.xml
    *   **System Connect Form/Combo** \[fix\] getHostNames() return String\[\] containing invalid null values
*   Components affected by fixes for [I20070404-1200](http://download.eclipse.org/dsdp/tm/downloads/drops/I20070404-1200):
    *   **Everything** [\[9\]](https://bugs.eclipse.org/bugs/show_bug.cgi?id=175262)\[api\] IHost.getSystemType() should return IRSESystemType;
    *   **dstore** [\[10\]](https://bugs.eclipse.org/bugs/show_bug.cgi?id=180650) moved dstore.miners.miner to dstore.miners;
    *   **Persistence** [\[11\]](https://bugs.eclipse.org/bugs/show_bug.cgi?id=142806)\[api\] refactoring and adding new tracking api for persistence;
    *   **EFS** [\[12\]](https://bugs.eclipse.org/bugs/show_bug.cgi?id=170916) New files could not be created in EFS due to thread blocking

  

*   You'll have two tasks for testing this time:
    *   1\. Sanity check - please use RSE in a "normal" way as you'd usually use it. [RSE 1.0 Test Instructions](./RSE_1.0_Test_Instructions#Step_5:_Basic_Sanity_Check "RSE 1.0 Test Instructions") have a sample sanity check. Please test on your assigned host/target combination. Report any bad behavior. We should try to get most of RSE covered since refactorings might have broken things.
    *   2\. Bug verification - See the [P1, P2, Critical and Major bugs modified](#Test-Reports-and-Bugs-Found) query for verification candidates. I'm not splitting up the bugs to be verified, please take from the query mentioned what you think you can verify; naturally, those reported by yourself are the prime candidates. Change the status soon and refresh the query often to ensure we don't do duplicate work. When you verified a bug OK, set it to VERIFIED. Bugzilla allows you to click on the "next bug" link so you'll be able to move through the list quite quickly.

**Thanks** to everybody who signs up and thus helps making RSE better!

Test Matrix
-----------

| **ok** | **Tester Name (Company)** | **Client Platform** | **Connection types** | **RSE Features** | **Time used**, Comments |
| --- | --- | --- | --- | --- | --- |
| ok | Dave Dykstal (IBM) | MacOS X 10.4.8, Sun 1.5.0_06-112 | Dstore-Mac, Dstore-Linux, Dstore-Win | Macintosh related. Team features. Persistence & model features (filters, filter pools, ...) | 4 hours so far. DND now is initiated on Mac, though it doesn't completely work. [DaveD bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&emailreporter1=1&emailtype1=exact&email1=david_dykstal%40us.ibm.com&chfieldfrom=2007-04-03&chfieldto=2007-04-08&chfield=%5BBug+creation%5D&cmdtype=doit) |
|  | Dave McKnight (IBM) | Linux-GTK (SLES 9), IBMj 1.4.2 sr3 | Dstore-Windows, FTP |  | [DaveM bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&emailreporter1=1&emailtype1=exact&email1=dmcknigh%40ca.ibm.com&chfieldfrom=2007-04-03&chfieldto=2007-04-08&chfield=%5BBug+creation%5D&cmdtype=doit) |
|  | Kushal Munir (IBM) | Windows XP SP2, IBMj 5.0 | Dstore-Unix (on AIX) | Drag&Drop, Copy&Paste, New Connection Wizard, Encodings, Dstore Launch Options, File Access Permissions and Timestamps | [Kushal bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&emailreporter1=1&emailtype1=exact&email1=kmunir%40ca.ibm.com&chfieldfrom=2007-04-03&chfieldto=2007-04-08&chfield=%5BBug+creation%5D&cmdtype=doit) |
| ok | Javier Montalvo (Symbian) | WinXP 2002 SP2, Sun 1.5.0_11 | Windows-local, FTP | ftp filters and views; filtetype filters, deep filters, drag&drop, copy&paste (contexts) | [Javier bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&emailreporter1=1&emailtype1=exact&email1=Javier.MontalvoOrus%40symbian.com&chfieldfrom=2007-04-03&chfieldto=2007-04-08&chfield=%5BBug+creation%5D&cmdtype=doit) |
| ok | Martin Oberhuber (Wind River) | WinXP SP1, Sun 1.4.2_14 | Windows-Local, Linux-dstore-rexec, Linux-ssh | Download, Connection Problems, Discovery, Terminal(Telnet,Ssh,Serial), Shells-Contentassist, Shell-Processes | [Martin bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&emailreporter1=1&emailtype1=exact&email1=martin.oberhuber%40windriver.com&chfieldfrom=2007-04-03&chfieldto=2007-04-08&chfield=%5BBug+creation%5D&cmdtype=doit) |
| ok | Martin Oberhuber (Wind River) | Linux RHEL4, Sun 1.6.0_01 | Linux-Local, Windows-dstore-daemon, Linux-ssh | Update Site, Connection Problems, Discovery, Terminal(Telnet,Ssh,Serial), Shells-Contentassist, Shell-Processes | [Martin bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&emailreporter1=1&emailtype1=exact&email1=martin.oberhuber%40windriver.com&chfieldfrom=2007-04-03&chfieldto=2007-04-08&chfield=%5BBug+creation%5D&cmdtype=doit) |
|  | Tobias Schwarz (Wind River) | WinXP SP2, Sun 1.5.0_11 | Windows-Local, Testsubsys | Verify [Tobias reported bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=RESOLVED&resolution=FIXED&resolution=INVALID&resolution=WONTFIX&resolution=WORKSFORME&emailreporter1=1&emailtype1=exact&email1=tobias.schwarz%40windriver.com&cmdtype=doit); ; Filtering, Extension Points | [Tobias bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&emailreporter1=1&emailtype1=exact&email1=tobias.schwarz%40windriver.com&chfieldfrom=2007-04-03&chfieldto=2007-04-08&chfield=%5BBug+creation%5D&cmdtype=doit) |
|  | Uwe Stieber (Wind River) | openSUSE 10.2 (x86-64), Sun 1.5.0_10 (64Bit) | Linux-Local, Testsubsys | Verify [Uwe reported bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=RESOLVED&resolution=FIXED&resolution=INVALID&resolution=WONTFIX&resolution=WORKSFORME&emailreporter1=1&emailtype1=exact&email1=uwe.stieber%40windriver.com&cmdtype=doit); Extension Points | [Uwe bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&emailreporter1=1&emailtype1=exact&email1=uwe.stieber%40windriver.com&chfieldfrom=2007-04-03&chfieldto=2007-04-08&chfield=%5BBug+creation%5D&cmdtype=doit) |
|  | Lothar Werzinger (Tradescape) | Linux Kubuntu 6.06 x64 GTK, Sun 1.5.0_06 | Linux-ssh, Windows-dstore | ssh filters and views; |  |
| ok | Ewa Matejska (Palmsource) | Linux Ubuntu 6.10, Sun 1.5.0_10 | Linux-ssh, Linux-ftp, Linux-dstore | CDT Remote Launch and Basic Sanity Test | [Ewa bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&emailreporter1=1&emailtype1=exact&email1=Ewa.Matejska%40palmsource.com&chfieldfrom=2007-04-03&chfieldto=2007-04-08&chfield=%5BBug+creation%5D&cmdtype=doit) |
| ok | Burak Kulakli (Cabot) | WinXP SP2, Sun 1.6.0 | Unix-ssh, Windows-Local | (Copy\|Move\|Delete)(File\|Directory) from (LOCAL\|REMOTE) to (LOCAL\|REMOTE) | [Burak bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&emailreporter1=1&emailtype1=exact&email1=kulakli%40yahoo.co.uk&chfieldfrom=2007-04-03&chfieldto=2007-04-08&chfield=%5BBug+creation%5D&cmdtype=doit) |

### Test Features

#### RSE Features signed up already

*   MartinO:
    *   MV Shell Processes Subsystem
    *   Terminal (ssh,telnet,serial)
    *   [Shell Content Assist-Linux](./TM_Manual_Test_Plan#Shell_Content_Assist-Linux "TM Manual Test Plan") (local,ssh,dstore)
    *   [Shell Content Assist-Windows](./TM_Manual_Test_Plan#Shell_Content_Assist-Windows "TM Manual Test Plan") (local,dstore)
    *   [Shell Pattern Matching](./TM_Manual_Test_Plan#Shell_Pattern_Matching "TM Manual Test Plan") (Compiler Error Navigation, Directory and File Navigation)
*   DaveD:
    *   Basic Sanity Test (of course)
    *   Subsystem properties
    *   RSE Views
    *   Connection problems
    *   Preferences

#### RSE Features that are particularly important to test

*   Verifications: [2.0M6 Bugs (by date) fixed but not yet verified](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=RESOLVED&resolution=FIXED&resolution=WONTFIX&resolution=INVALID&resolution=WORKSFORME&chfieldfrom=2007-02-24&chfieldto=2007-04-08&chfield=resolution&cmdtype=doit)

*   [Basic Sanity Test](./TM_Manual_Test_Plan#Basic_Sanity_Test "TM Manual Test Plan") (File Subsystem, dirlist, simple filters, upload/download/edit, Tableview)
*   [File Encodings](./TM_Manual_Test_Plan#File_Encodings "TM Manual Test Plan") (Foreign language files on remote side)
*   [CDT Remote Launch](./TM_Manual_Test_Plan#CDT_Remote_Launch "TM Manual Test Plan")
*   [Drag&Drop, Copy&Paste](./TM_Manual_Test_Plan#Drag.26Drop.2C_Copy.26Paste "TM Manual Test Plan") (RSE <-> RSE, Eclipse Navigator, Windows Explorer, Overwrite vs. Rename)
*   [Discovery](./TM_Manual_Test_Plan#Discovery "TM Manual Test Plan")
*   [EFS](./TM_Manual_Test_Plan#EFS "TM Manual Test Plan")

#### RSE Features to test

*   [Dstore Launch Options](./TM_Manual_Test_Plan#Dstore_Launch_Options "TM Manual Test Plan") (Rlogin, Already-Running, Port Ranges, SSL Connection)
*   [Parallel access](./TM_Manual_Test_Plan#Parallel_access "TM Manual Test Plan") (multiple parallel actions)
*   [Update Site](./TM_Manual_Test_Plan#Update_Site "TM Manual Test Plan"): Install & Upgrade via Update Site
*   [Scalability](./TM_Manual_Test_Plan#Scalability "TM Manual Test Plan") (Really large file lists, lots of events)
*   [Processes Subsystem](./TM_Manual_Test_Plan#Processes_Subsystem "TM Manual Test Plan") (List, Sort, Kill, Remote Monitor)
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

#### Features **not to be tested** this time

*   [Team Support](./TM_Manual_Test_Plan#Team_Support "TM Manual Test Plan") (Share connections, Connection Profiles)
*   [Verify Copyright and Externalized Strings](./TM_Manual_Test_Plan#Verify_Copyright_and_Externalized_Strings "TM Manual Test Plan") (Run automated checks, chkpii)
*   [Verify Legal](./TM_Manual_Test_Plan#Verify_Legal "TM Manual Test Plan") (Feature Descriptions, Licenses in all source features, Overall license)
*   [Verify User Docs](./TM_Manual_Test_Plan#Verify_User_Docs "TM Manual Test Plan") (Walk through tutorial, Context Help, Check Links, Search feature)
*   [Verify ISV Tutorial](./TM_Manual_Test_Plan#Verify_ISV_Tutorial "TM Manual Test Plan") (Walk through ISV tutorial)
*   [Verify ISV Docs](./TM_Manual_Test_Plan#Verify_ISV_Docs "TM Manual Test Plan") (Broken Links, Semantic correctness, Searchable docs, Useful Javadoc)

  

### Client Platforms

| Windows XP | MartinO (SP1; Sun1.4.2\_14); KushalM (SP2; IBM1.5); NorbertP (SP2; Sun1.5.0\_06); SumitS (SP2; Sun1.4.2\_10); MichaelScharf (SP2; Sun1.5.0\_07); |
| --- | --- |
| Windows 2000 | JavierM (Sun 1.4.2_10); |
| Linux-x86-gtk | MartinO (RHEL4, Sun1.6.0\_01); DaveM (SLES9, IBM1.4.2\_sr3); EwaM (Ubuntu 6.10) |
| Linux-x86_64-gtk | LotharW (Kubuntu 6.06); UweS (openSUSE 10.2, Sun 1.5.0_10 (64Bit)) |
| Solaris-gtk | MartinO (Solaris9, Sun 1.5.0_11); |
| Mac OS X | DaveD (10.4.7, Sun1.5.0_06); KushalM |
| Linux-ppc-gtk |  |
| Linux-Motif |  |
| AIX |  |

### Target Platforms

| Windows-dstore | MartinO (XP-SP1, Sun1.4.2\_14); MichaelScharf (XP-SP1, Sun1.5.0\_07); |
| --- | --- |
| Windows-ssh |  |
| Windows-ftp | JavierM (FileZilla 0.9.8b); MichaelScharf (GNU inetutils 1.3.2) |
| Linux-dstore | MartinO (RHEL4, Sun1.4.2\_13); NorbertP (SUSE10.0; Sun1.4.2\_06); UweS (SUSE10.1; Sun1.5.0\_07); EwaM (Ubuntu6.10, Sun1.5.0\_10); MichaelScharf (SUSE10.1; Sun1.6.0-beta2); |
| Linux-ssh | MartinO (RHEL4); MartinO (SUSE Enterprise 10 PPC); UweS (SUSE10.1); EwaM (Ubuntu6.10); BurakK (Fedora5); MichaelScharf (SUSE10.1); |
| Linux-ftp | MichaelScharf (SUSE10.1); EwaM (Ubuntu6.10); |
| Solaris-dstore | MartinO (Sol9, Sun1.5.0\_11); MartinO (Sol10, Sun1.5.0\_11) |
| Solaris-ssh | MartinO (Sol9); |
| Solaris-ftp |  |
| HPUX-dstore |  |
| HPUX-ssh | SumitS (HP-UX11.11); |
| HPUX-ftp |  |
| AIX-dstore | KushalM |
| AIX-ssh |  |
| AIX-ftp |  |
| MacOSX-dstore | DaveD (10.4.7, Sun1.5.0_06); |
| MacOSX-ssh | GregW (10.4.7, Sun1.5.0_06); |
| MacOSX-ftp |  |
| VMS-ftp |  |
| MVS-ftp |  |
| VxWorks-ftp | MartinO (VxSim SIMNT 6.4) |

Test Reports and Bugs Found
---------------------------

*   Test Candidates:
    *   [P1, P2, Critical and Major bugs modified during the test period](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_status=RESOLVED&chfieldfrom=2007-04-03&chfieldto=2007-04-09&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor) but not yet verified
    *   [2.0M6 Bugs (by date) fixed but not yet verified](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=RESOLVED&resolution=FIXED&resolution=WONTFIX&resolution=INVALID&resolution=WORKSFORME&chfieldfrom=2007-02-24&chfieldto=2007-04-08&chfield=resolution&cmdtype=doit)

  

*   Test Results:
    *   [New bugs opened during test period](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&chfieldfrom=2007-04-03&chfieldto=2007-04-08&chfield=%5BBug+creation%5D&cmdtype=doit)
    *   [Bugs reopened during test period](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&chfieldfrom=2007-04-03&chfieldto=2007-04-08&chfield=bug_status&chfieldvalue=REOPENED&cmdtype=doit)
    *   [Bugs verified or closed during test period](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=VERIFIED&bug_status=CLOSED&chfieldfrom=2007-04-03&chfieldto=2007-04-08&chfield=bug_status&cmdtype=doit)

  

*   Internal Reports:
    *   [Bugzilla report: Reporter X Severity by date](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=bug_severity&y_axis_field=reporter&z_axis_field=&query_format=report-table&classification=DSDP&product=Target+Management&chfieldfrom=2007-04-03&chfieldto=2007-04-08&chfield=%5BBug+creation%5D&chfieldvalue=&format=table&action=wrap), reported during test period (2007-04-03 - 2007-04-08)
    *   [Bugzilla report: Reporter X Fix status by date](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=resolution&y_axis_field=reporter&z_axis_field=&query_format=report-table&classification=DSDP&product=Target+Management&chfieldfrom=2007-04-03&chfieldto=2007-04-08&chfield=%5BBug+creation%5D&chfieldvalue=&format=table&action=wrap), for bugs reported during test period (2007-04-03 - 2007-04-08)
    *   [Bugs fixed for 2.0M6 by date](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=RESOLVED&bug_status=VERIFIED&bug_status=CLOSED&resolution=FIXED&resolution=WONTFIX&resolution=INVALID&resolution=WORKSFORME&chfieldfrom=2007-02-24&chfieldto=2007-04-08&chfield=resolution&cmdtype=doit) including verified and closed
    *   [Bugs fixed for 2.0M6 by target milestone](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&target_milestone=2.0+M6&bug_status=RESOLVED&bug_status=VERIFIED&bug_status=CLOSED&resolution=FIXED&resolution=INVALID&resolution=WONTFIX&resolution=WORKSFORME&cmdtype=doit)


(Migrated from [https://wiki.eclipse.org/TM_2.0_M6_Testing](https://wiki.eclipse.org/TM_2.0_M6_Testing))