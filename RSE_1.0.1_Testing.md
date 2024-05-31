

RSE 1.0.1 Testing
=================

Nav: [DSDP/TM](./DSDP/TM "DSDP/TM") | [RSE 1.0 Testing](./RSE_1.0_Testing "RSE 1.0 Testing") | RSE 1.0.1 Testing | [RSE 1.0 Test Instructions](./RSE_1.0_Test_Instructions "RSE 1.0 Test Instructions") | [RSE 1.0 Known Issues and Workarounds](./RSE_1.0_Known_Issues_and_Workarounds "RSE 1.0 Known Issues and Workarounds") | [RSE Manual Test Plan](./RSE_Manual_Test_Plan "RSE Manual Test Plan")

* * *

This is the master coordination page for RSE 1.0.1 Testing, to be done with RSE 1.0.1RC1, 13-Dec-2006. Please sign up here for testing particular features of RSE 1.0.1, or a particular host / target combination. It is important for all of us to coordinate our efforts

*   In order to get bugs submitted early, such that we can fix them for the release
*   In order to avoid duplication of testing work
*   In order to get a good test coverage and exposure of RSE.

  

Contents
--------

*   [1 Organization and Signup](#Organization-and-Signup)
*   [2 Test Matrix](#Test-Matrix)
    *   [2.1 Test Features](#Test-Features)
        *   [2.1.1 RSE Features signed up already](#RSE-Features-signed-up-already)
        *   [2.1.2 RSE Features to test](#RSE-Features-to-test)
        *   [2.1.3 Features **not to be tested** this time](#Features-not-to-be-tested-this-time)
    *   [2.2 Client Platforms](#Client-Platforms)
    *   [2.3 Target Platforms](#Target-Platforms)
*   [3 Test Reports and Bugs Found](#Test-Reports-and-Bugs-Found)

Organization and Signup
-----------------------

The main focus in this round of testing is to find final **obvious showstoppers**, and to **verify** 1.0.1 bug fixes.

Most of you took part in an earlier round of testing already, so you'll not need to read all of the [RSE 1.0 Test Instructions](./RSE_1.0_Test_Instructions "RSE 1.0 Test Instructions"). Here is some important information for this round of testing:

*   Please use a customized bug entry template again. If you already have one from an earlier round of testing, change "1.0 Testing round 2" into "1.0.1 Testing" and save it as your new bookmark for this round of testing. Otherwise, use [this link to show, modify and save a sample bug entry template](https://bugs.eclipse.org/bugs/enter_bug.cgi?product=Target%20Management&version=1.0&component=RSE&rep_platform=PC&op_sys=Windows%20XP&priority=P3&bug_severity=normal&bug_status=NEW&assigned_to=dsdp.tm.rse-inbox%40eclipse.org&qa_contact=martin.oberhuber%40windriver.com&cc=&bug_file_loc=http%3A%2F%2F&short_desc=&comment=%0D%0A-----------Enter%20bugs%20above%20this%20line-----------%0D%0ARSE%201.0.1%20Testing%0D%0Ainstallation%20%3A%20eclipse-platform-3.2.1%20%28M20060921-0945%29%2C%20cdt-3.1.1%2C%20emf-2.1.1%0D%0ARSE%20install%20%20%3A%20update-site%20RSE-runtime-all%20%2B%20discovery%20%2B%20efs%0D%0Ajava.runtime%20%3A%20Sun%201.5.0_08-b03%0D%0Aos.name%3A%20%20%20%20%20%3A%20Windows%20XP%205.1%2C%20Service%20Pack%202%0D%0A------------------------------------------------%0D%0Asystemtype%20%20%20%3A%20Unix-ssh%20%28dstore-processes%29%0D%0Atargetos%20%20%20%20%20%3A%20SUSE%20LINUX%2010.1%20%28i586%29%0D%0Atargetuname%20%20%3A%20Linux%20osgiliath%202.6.16.21-0.21-default%20%231%20Tue%20Aug%2029%2016%3A42%3A05%20UTC%202006%20i686%20athlon%20i386%20GNU%2FLinux%0D%0Atargetvm%20%20%20%20%20%3A%20Sun%20Java%20HotSpot%28TM%29%20Client%20VM%20%28build%201.5.0_07-b03%2C%20mixed%20mode%2C%20sharing%29%0D%0A------------------------------------------------%0D%0A&commentprivacy=0&keywords=&dependson=&blocked=&maketemplate=Remember%20values%20as%20bookmarkable%20template&form_name=enter_bug).
*   If possible, please use the JDK versions as signed up in the table below. These are chosen to comply with our [Reference Platforms and JDK versions](https://www.eclipse.org/dsdp/tm/development/plan.php#OperatingEnvironments). Edit the table below if you need to use a different JDK version.
*   Downloads to test are at [M20061213-0730](http://download.eclipse.org/dsdp/tm/downloads/drops/M20061213-0730)
*   Updates Site to test is at [http://download.eclipse.org/dsdp/tm/testUpdates](http://download.eclipse.org/dsdp/tm/testUpdates)
    *   Please do not use a mirror
*   You'll have two tasks for testing this time:
    *   1\. Bug verification - For verifying your assigned bugs, please click on "your" link in the table. When you verified a bug OK, set it to VERIFIED. Bugzilla allows you to click on the "next bug" link so you'll be able to move through the list quite quickly.
    *   2\. Sanity check - please use RSE in a "normal" way as you'd usually use it. Report any bad behavior.

**Thanks** to everybody who signs up and thus helps making RSE better!

Test Matrix
-----------

| **ok** | **Tester Name (Company)** | **Client Platform** | **Connection types** | **RSE Features** | **Time used**, Comments |
| --- | --- | --- | --- | --- | --- |
| ok | Dave Dykstal (IBM) | MacOS X 10.4.8, Sun 1.5.0_06-112 | Dstore-Mac, Dstore-Linux, Dstore-Win | Verify [DKM's fixes part 1](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&bug_id=142478,142954,142968,148978,150954,159965,162994,162995,163381,163532); Macintosh related. Team features. Persistence & model features (filters, filter pools, ...) | 6h |
|  | Dave McKnight (IBM) | Linux-GTK (SLES 9), IBMj 1.4.2 sr3 | Dstore-Windows, FTP | Verify [FTP related bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&bug_id=161238,162585,164009,164306); Verify [Kushals fixes](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&bug_id=141804,141809,143458,149281,154217,159969,164292,164520) |  |
| ok | Kushal Munir (IBM) | Windows XP SP2, IBMj 5.0 | Dstore-Unix (on AIX) | Verify [DKMs fixes part 2](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&bug_id=164119,164293,164642,165891,166154,166156,166343,166345,166605); | 3h |
| ok | Javier Montalvo (Symbian) | Windows 2000, Sun 1.4.2_12 | Windows-local, FTP | Verify [DaveD Fixes](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&bug_id=142218,142962,150364,150368,150386,150388,150930,153240,158306,162176,164104,164202,166117); ftp filters and views; | 3h |
|  | Martin Oberhuber (Wind River) | Solaris 9-Motif, Sun 1.4.2_10 | Solaris-local, Unix-dstore | Verify [remotecdt](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&bug_id=158784); Profiles, Team Support, Connection Problems, Discovery |  |
|  | Lothar Werzinger (Tradescape) | Linux Kubuntu 6.06 x64 GTK, Sun 1.5.0_06 | Linux-ssh, Windows-dstore | Verify [Martins fixes](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&bug_id=161777,164628); ssh filters and views; | 2.5h |

### Test Features

#### RSE Features signed up already

#### RSE Features to test

*   [Basic Sanity Test](./RSE_Manual_Test_Plan#Basic_Sanity_Test "RSE Manual Test Plan") (File Subsystem, dirlist, simple filters, upload/download/edit, Tableview)
*   [Team Support](./RSE_Manual_Test_Plan#Team_Support "RSE Manual Test Plan") (Share connections, Connection Profiles)
*   [CDT Remote Launch](./RSE_Manual_Test_Plan#CDT_Remote_Launch "RSE Manual Test Plan")
*   [Dstore Launch Options](./RSE_Manual_Test_Plan#Dstore_Launch_Options "RSE Manual Test Plan") (Rlogin, Already-Running, Port Ranges, SSL Connection)
*   [Shell Content Assist-Linux](./RSE_Manual_Test_Plan#Shell_Content_Assist-Linux "RSE Manual Test Plan") (local,ssh,dstore)
*   [Shell Content Assist-Windows](./RSE_Manual_Test_Plan#Shell_Content_Assist-Windows "RSE Manual Test Plan") (local,dstore)
*   [Parallel access](./RSE_Manual_Test_Plan#Parallel_access "RSE Manual Test Plan") (multiple parallel actions)
*   [Drag&Drop, Copy&Paste](./RSE_Manual_Test_Plan#Drag.26Drop.2C_Copy.26Paste "RSE Manual Test Plan") (RSE <-> RSE, Eclipse Navigator, Windows Explorer, Overwrite vs. Rename)
*   [Update Site](./RSE_Manual_Test_Plan#Update_Site "RSE Manual Test Plan"): Install & Upgrade via Update Site
*   [Scalability](./RSE_Manual_Test_Plan#Scalability "RSE Manual Test Plan") (Really large file lists, lots of events)
*   [Shell Pattern Matching](./RSE_Manual_Test_Plan#Shell_Pattern_Matching "RSE Manual Test Plan") (Compiler Error Navigation, Directory and File Navigation)
*   [Processes Subsystem](./RSE_Manual_Test_Plan#Processes_Subsystem "RSE Manual Test Plan") (List, Sort, Kill, Remote Monitor)
*   [Verify Extension Points](./RSE_Manual_Test_Plan#Verify_Extension_Points "RSE Manual Test Plan") (Check docs, use in own code)
*   [Remote Search](./RSE_Manual_Test_Plan#Remote_Search "RSE Manual Test Plan") (dstore only)
*   [Complex Filters](./RSE_Manual_Test_Plan#Complex_Filters "RSE Manual Test Plan") (Multiple filter strings, Filter by filetype, Filter Persistence...)
*   [Preferences](./RSE_Manual_Test_Plan#Preferences "RSE Manual Test Plan") (Walk through each of the Preferences and enable/disable)
*   [Subsystem Properties](./RSE_Manual_Test_Plan#Subsystem_Properties "RSE Manual Test Plan") (Changing Properties of Systems/Subsystems in the RSE Tree)
*   [Synchronous operation](./RSE_Manual_Test_Plan#Synchronous_operation "RSE Manual Test Plan") (Do a sanity check with "Deferred Queries" switched off in Preferences)
*   [Dirty Editors and Merging](./RSE_Manual_Test_Plan#Dirty_Editors_and_Merging "RSE Manual Test Plan") (Editing a Remote File that also changes remotely)
*   [File Access Permissions and Timestamps](./RSE_Manual_Test_Plan#File_Access_Permissions_and_Timestamps "RSE Manual Test Plan") (Read-only files etc.)
*   [RSE Views](./RSE_Manual_Test_Plan#RSE_Views "RSE Manual Test Plan"): Treeview, Tableview, Monitor, Properties, Scratchpad, Editor, Compare (Check for consistency)
*   [RSE Widgets & Dialogs](./RSE_Manual_Test_Plan#RSE_Widgets_.26_Dialogs "RSE Manual Test Plan"): Remote file-browse, Remote move-to
*   [Connection Problems](./RSE_Manual_Test_Plan#Connection_Problems "RSE Manual Test Plan") (Very slow connections, unavailable/unreliable hosts, timeouts, breaking connections)
*   [Discovery](./RSE_Manual_Test_Plan#Discovery "RSE Manual Test Plan")

#### Features **not to be tested** this time

*   [Verify Copyright and Externalized Strings](./RSE_Manual_Test_Plan#Verify_Copyright_and_Externalized_Strings "RSE Manual Test Plan") (Run automated checks, chkpii)
*   [Verify Legal](./RSE_Manual_Test_Plan#Verify_Legal "RSE Manual Test Plan") (Feature Descriptions, Licenses in all source features, Overall license)
*   [Verify User Docs](./RSE_Manual_Test_Plan#Verify_User_Docs "RSE Manual Test Plan") (Walk through tutorial, Context Help, Check Links, Search feature)
*   [Verify ISV Tutorial](./RSE_Manual_Test_Plan#Verify_ISV_Tutorial "RSE Manual Test Plan") (Walk through ISV tutorial)
*   [Verify ISV Docs](./RSE_Manual_Test_Plan#Verify_ISV_Docs "RSE Manual Test Plan") (Broken Links, Semantic correctness, Searchable docs, Useful Javadoc)
*   [File Encodings](./RSE_Manual_Test_Plan#File_Encodings "RSE Manual Test Plan") (Foreign language files on remote side)
*   [EFS](./RSE_Manual_Test_Plan#EFS "RSE Manual Test Plan")

  

### Client Platforms

| Windows XP | MartinO (SP1; Sun1.5.0\_08); KushalM (SP2; IBM1.5); NorbertP (SP2; Sun1.5.0\_06); SumitS (SP2; Sun1.4.2\_10); MichaelScharf (SP2; Sun1.5.0\_07); |
| --- | --- |
| Windows 2000 | JavierM (Sun 1.4.2_10); |
| Linux-x86-gtk | MartinO (RHEL4, Sun1.4.2\_12); DaveM (SLES9, IBM1.4.2\_sr3); |
| Linux-ppc-gtk |  |
| Solaris-motif | MartinO (Solaris9); |
| Mac OS X | DaveD (10.4.7, Sun1.5.0_06); |
| Linux-x86_64-gtk | LotharW (Kubuntu 6.06); |
| Linux-Motif |  |

### Target Platforms

| Windows-dstore | MartinO (XP-SP1, Sun1.5.0\_08); MichaelScharf (XP-SP1, Sun1.5.0\_07); |
| --- | --- |
| Windows-ssh |  |
| Windows-ftp | JavierM (FileZilla 0.9.8b); MichaelScharf (GNU inetutils 1.3.2) |
| Linux-dstore | MartinO (RHEL4, Sun1.4.2\_12); NorbertP (SUSE10.0; Sun1.4.2\_06); UweS (SUSE10.1; Sun1.5.0\_07); EwaM (Ubuntu5.10, Sun1.5.0\_07); MichaelScharf (SUSE10.1; Sun1.6.0-beta2); |
| Linux-ssh | MartinO (RHEL4); UweS (SUSE10.1); EwaM (Ubuntu5.10); BurakK (Fedora5); MichaelScharf (SUSE10.1); |
| Linux-ftp | MichaelScharf (SUSE10.1); |
| Solaris-dstore |  |
| Solaris-ssh | MartinO (Sol7, Sol8, Sol9); |
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
| VxWorks-ftp |  |

Test Reports and Bugs Found
---------------------------

*   Test Candidates:
    *   [Bugs fixed for 1.0.1 by target milestone](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&target_milestone=1.0.1&bug_status=RESOLVED&bug_status=VERIFIED&bug_status=CLOSED&resolution=FIXED&resolution=WONTFIX&resolution=INVALID&resolution=WORKSFORME&cmdtype=doit)
    *   [Bugs fixed for 1.0.1 by date](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=RESOLVED&bug_status=VERIFIED&bug_status=CLOSED&resolution=FIXED&resolution=WONTFIX&resolution=INVALID&resolution=WORKSFORME&chfieldfrom=2006-11-14&chfieldto=2006-12-16&chfield=resolution&cmdtype=doit)
    *   [1.0.1 Bugs (by date) fixed but not yet verified](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=RESOLVED&resolution=FIXED&resolution=WONTFIX&resolution=INVALID&resolution=WORKSFORME&chfieldfrom=2006-11-14&chfieldto=2006-12-16&chfield=resolution&cmdtype=doit)

  

*   Test Results:
    *   [Bugs reopened during test period](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&chfieldfrom=2006-12-13&chfieldto=2006-12-15&chfield=bug_status&chfieldvalue=REOPENED&cmdtype=doit)
    *   [New bugs opened during test period](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&chfieldfrom=2006-12-13&chfieldto=2006-12-15&chfield=%5BBug+creation%5D&cmdtype=doit)
    *   [Bugs verified or closed during test period](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=VERIFIED&bug_status=CLOSED&chfieldfrom=2006-12-13&chfieldto=2006-12-15&chfield=bug_status&cmdtype=doit)

  

*   Internal Reports:
    *   [Bugzilla test report: Reporter X Severity](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=bug_severity&y_axis_field=reporter&z_axis_field=&query_format=report-table&short_desc_type=allwordssubstr&short_desc=&classification=DSDP&product=Target+Management&component=RSE&long_desc_type=casesubstring&long_desc=RSE+1.0.1+Testing&bug_file_loc_type=allwordssubstr&bug_file_loc=&status_whiteboard_type=allwordssubstr&status_whiteboard=&keywords_type=allwords&keywords=&emailtype1=substring&email1=&emailtype2=substring&email2=&bugidtype=include&bug_id=&votes=&chfieldfrom=&chfieldto=Now&chfieldvalue=&format=table&action=wrap&field0-0-0=noop&type0-0-0=noop&value0-0-0=)
    *   [Bugzilla report: Reporter X Severity by date](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=bug_severity&y_axis_field=reporter&z_axis_field=&query_format=report-table&short_desc_type=allwordssubstr&short_desc=&classification=DSDP&product=Target+Management&long_desc_type=casesubstring&long_desc=&bug_file_loc_type=allwordssubstr&bug_file_loc=&status_whiteboard_type=allwordssubstr&status_whiteboard=&keywords_type=allwords&keywords=&emailtype1=substring&email1=&emailtype2=substring&email2=&bugidtype=include&bug_id=&votes=&chfieldfrom=2006-12-13&chfieldto=2006-12-15&chfield=%5BBug+creation%5D&chfieldvalue=&format=table&action=wrap&field0-0-0=noop&type0-0-0=noop&value0-0-0=), 2006-12-13 - 2006-12-15
    *   [Bugzilla report: Buggy Bugz](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=component&y_axis_field=reporter&z_axis_field=&query_format=report-table&short_desc_type=allwordssubstr&short_desc=&classification=DSDP&product=Target+Management&long_desc_type=casesubstring&long_desc=&bug_file_loc_type=allwordssubstr&bug_file_loc=&status_whiteboard_type=allwordssubstr&status_whiteboard=&keywords_type=allwords&keywords=&emailtype1=substring&email1=&emailtype2=substring&email2=&bugidtype=include&bug_id=&votes=&chfieldfrom=2006-12-13&chfieldto=2006-12-15&chfield=%5BBug+creation%5D&chfieldvalue=&format=table&action=wrap&negate0=1&field0-0-0=longdesc&type0-0-0=casesubstring&value0-0-0=RSE+1.0.1+Testing&field0-0-1=longdesc&type0-0-1=substring&value0-0-1=RSE+1.0.1+Testing) \- Bugs reported 2006-12-13 - 2006-12-15 but without the test tag


(Migrated from [https://wiki.eclipse.org/RSE_1.0.1_Testing](https://wiki.eclipse.org/RSE_1.0.1_Testing))