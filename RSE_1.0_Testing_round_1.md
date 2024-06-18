

RSE 1.0 Testing round 1
=======================

Nav: [DSDP/TM](./TM "DSDP/TM") | [RSE 1.0 Testing](./RSE_1.0_Testing "RSE 1.0 Testing") | [RSE 1.0 Test Instructions](./RSE_1.0_Test_Instructions "RSE 1.0 Test Instructions") | [RSE 1.0M5 Known Issues and Workarounds](./RSE_1.0M5_Known_Issues_and_Workarounds "RSE 1.0M5 Known Issues and Workarounds") | [RSE Manual Test Plan](./RSE_Manual_Test_Plan "RSE Manual Test Plan")

* * *

This is the master coordination page for RSE 1.0 Testing round 1, to be done with RSE 1.0M5, 25-Sep-2006 - 27-Sep-2006. Please sign up here for testing particular features of RSE 1.0, or a particular host / target combination. It is important for all of us to coordinate our efforts

*   In order to get bugs submitted early, such that we can fix them for the release
*   In order to avoid duplication of testing work
*   In order to get a good test coverage and exposure of RSE.

  

| Click here for the [RSE 1.0 Test Instructions](./RSE_1.0_Test_Instructions "RSE 1.0 Test Instructions") |
| --- |

  

Contents
--------

*   [1 Organization and Signup](#Organization-and-Signup)
*   [2 Test Matrix](#Test-Matrix)
    *   [2.1 Test Features](#Test-Features)
    *   [2.2 Client Platforms](#Client-Platforms)
    *   [2.3 Target Platforms](#Target-Platforms)
*   [3 Test Reports and Bugs Found](#Test-Reports-and-Bugs-Found)
*   [4 Comments from Testers](#Comments-from-Testers)

Organization and Signup
-----------------------

Detailed [RSE 1.0 Test Instructions](./RSE_1.0_Test_Instructions "RSE 1.0 Test Instructions") are being sent out, so don't feel afraid of being signed up to any features you have never heard of before - this might actually help improving your test quality sinc you might tend to try things that nobody else thought about before.

Please put your name in the table below. **Feel free to modify** the host/target combinations, or features of RSE to test as you find yourself fit. Put an "ok" in the first column when you reviewed your assignment. **You may delete assignments or limit your time commitment, but please let us know what you are planning and then stick to your commitment**. The list is sorted by company name, then first name.

Signing up for a testing commitment means **downloading and installing RSE, checking assigned features, and submitting bugzilla reports. A very basic sanity test should be included for each tester in addition to the specific assignment**. I've started assigning 2 hours of testing for contributors / users, and 4 hours of testing for committers, which I think everybody should be able to invest. Of course, doing more testing won't hurt but please try and focus on those areas that you have signed up to.

**Thanks** to everybody who signs up and thus helps making RSE better!

Test Matrix
-----------

| **ok** | **Tester Name (Company)** | **Client Platform** | **Connection types** | **RSE Features** | **Time Commitment**, Comments |
| --- | --- | --- | --- | --- | --- |
| ok | Greg Watson (LANL) | MacOS X 10.4.7, Sun 1.5.0_06-112 | Ssh | Verify known mac-ssh bugs | 2h |
| ok | Sumit Sarkar (HP) | Windows XP SP2, Sun 1.4.2_10 | Dstore-Unix (HP-UX) | CDT Remote Launch | 4h |
| ok | Dave Dykstal (IBM) | Windows XP, IBM 5.0 SP1 | Dstore-Mac, Dstore-Linux | Complex Filters, Preferences, Processes | 2h |
| ok | MacOS X 10.4.7, Sun 1.5.0_06-112 | Dstore-Mac, Dstore-Linux | Complex Filters, Preferences, Processes | 2h |
| ok | Dave McKnight (IBM) | Linux-GTK (SLES 9), IBMj 1.4.2 sr3 | Dstore-Windows | Synchronous Operation, Dirty Editors and Merging | 4h |
| ok | Kushal Munir (IBM) | Windows XP SP2, IBMj 1.4.2 sr3 | Dstore-AIX | File Encodings, RSE Props+Scratchpad | 3h |
| ok | Ewa Matejska (PalmSource) | Linux-GTK (Ubuntu 5.10), Sun 1.5.0_07 | Local-Linux | Subsystem Properties | 2-3h |
| ok | Norbert Ploett (Siemens) | Windows XP, Sun 1.5.0_06 | Dstore-Linux | Shell Content Assist-Linux, DStore Launch Options | 4h |
| ok | Javier Montalvo (Symbian) | Windows 2000, Sun 1.4.2_03-b02 | Windows-local, FTP | Verify ISV Docs, Access Permissions & Timestamps | 4h |
| ok | Martin Oberhuber (Wind River) | Windows XP SP1, Sun 1.5.0_07-b03 | Windows-local, Linux-dstore | Profiles, Team Support, Connection Problems | 4h |
| ok | Linux-GTK (RHWS4), Sun 1.4.2_12-b03 | Linux-local, Windows-dstore | Profiles, Team Support, Connection Problems | 4h |
| ok | Michael Scharf (Wind River) | Windows XP, Sun 1.5.0_07, Eclipse-3.2.1 | DStore-Windows | Team and Daytime examples, Parallel Access | 4h |
| ok | Ted Williams (Wind River) | Windows XP, Sun 1.4.2_11 | Local-Windows | ISV Docs Tutorial, Shell Content Assist | 4h |
| ok | Uwe Stieber (Wind River) | Windows XP SP2, Sun 1.5.0_08-b03 | Ssh-Linux | Scalability, Drag&Drop | 2h |
| ok | Linux-GTK (SUSE 10.1), Sun 1.5.0_07-b03 | Ssh | Scalability, Drag&Drop | 2h |

### Test Features

**RSE Features signed up already**

*   [Basic Sanity Test](./RSE_Manual_Test_Plan#Basic_Sanity_Test "RSE Manual Test Plan") (File Subsystem, dirlist, simple filters, upload/download/edit, Tableview)
*   [Dstore Launch Options](./RSE_Manual_Test_Plan#Dstore_Launch_Options "RSE Manual Test Plan") (Rlogin, Already-Running, Port Ranges, SSL Connection)
*   [Shell Content Assist-Linux](./RSE_Manual_Test_Plan#Shell_Content_Assist-Linux "RSE Manual Test Plan") (local,ssh,dstore)
*   [Shell Content Assist-Windows](./RSE_Manual_Test_Plan#Shell_Content_Assist-Windows "RSE Manual Test Plan") (local,dstore)
*   [Team Support](./RSE_Manual_Test_Plan#Team_Support "RSE Manual Test Plan") (Share connections, Connection Profiles)

**RSE Features to test**

*   [Parallel access](./RSE_Manual_Test_Plan#Parallel_access "RSE Manual Test Plan") (multiple parallel actions)
*   [File Encodings](./RSE_Manual_Test_Plan#File_Encodings "RSE Manual Test Plan") (Foreign language files on remote side)
*   [Drag&Drop, Copy&Paste](./RSE_Manual_Test_Plan#Drag.26Drop.2C_Copy.26Paste "RSE Manual Test Plan") (RSE <-> RSE, Eclipse Navigator, Windows Explorer, Overwrite vs. Rename)
*   [Update Site](./RSE_Manual_Test_Plan#Update_Site "RSE Manual Test Plan"): Install & Upgrade via Update Site
*   [Scalability](./RSE_Manual_Test_Plan#Scalability "RSE Manual Test Plan") (Really large file lists, lots of events)
*   [Shell Pattern Matching](./RSE_Manual_Test_Plan#Shell_Pattern_Matching "RSE Manual Test Plan") (Compiler Error Navigation, Directory and File Navigation)
*   [Processes Subsystem](./RSE_Manual_Test_Plan#Processes_Subsystem "RSE Manual Test Plan") (List, Sort, Kill, Remote Monitor)
*   [Verify User Docs](./RSE_Manual_Test_Plan#Verify_User_Docs "RSE Manual Test Plan") (Walk through tutorial, Context Help, Check Links, Search feature)
*   [Verify Legal](./RSE_Manual_Test_Plan#Verify_Legal "RSE Manual Test Plan") (Feature Descriptions, Licenses in all source features, Overall license)
*   [Verify ISV Tutorial](./RSE_Manual_Test_Plan#Verify_ISV_Tutorial "RSE Manual Test Plan") (Walk through ISV tutorial)
*   [Verify ISV Docs](./RSE_Manual_Test_Plan#Verify_ISV_Docs "RSE Manual Test Plan") (Broken Links, Semantic correctness, Searchable docs, Useful Javadoc)
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
*   [Verify Copyright and Externalized Strings](./RSE_Manual_Test_Plan#Verify_Copyright_and_Externalized_Strings "RSE Manual Test Plan") (Run automated checks, chkpii)
*   [CDT Remote Launch](./RSE_Manual_Test_Plan#CDT_Remote_Launch "RSE Manual Test Plan")
*   [EFS](./RSE_Manual_Test_Plan#EFS "RSE Manual Test Plan")
*   [Discovery](./RSE_Manual_Test_Plan#Discovery "RSE Manual Test Plan")

### Client Platforms

| Windows XP | MartinO (SP1; Sun1.5.0\_08); KushalM (SP2; IBM1.5 / IBM1.4.2); NorbertP (SP2; Sun1.5.0\_06); SumitS (SP2; Sun1.4.2_10); |
| --- | --- |
| Windows 2000 | JavierM (Sun 1.4.2_03); |
| Linux-x86-gtk | MartinO (RHEL4, Sun1.4.2\_12); UweS (Suse10.1, Sun1.5.0\_07); DaveM (SLES9, IBM1.4.2\_sr3); EwaM (Ubuntu5.10, Sun1.5.0\_07); |
| Linux-ppc-gtk | GregW (round2); |
| Solaris-motif | MartinO (Solaris9); |
| Mac OS X | GregW (10.4.7, Sun1.5.0\_06); DaveD (10.4.7, Sun1.5.0\_06); |
| Linux-x86_64-gtk |  |
| Linux-Motif |  |

### Target Platforms

| Windows-dstore | MartinO (XP-SP1, Sun1.5.0_08); |
| --- | --- |
| Windows-ssh |  |
| Windows-ftp |  |
| Linux-dstore | MartinO (RHEL4, Sun1.4.2\_12); NorbertP (SUSE10.0; Sun1.4.2\_06); UweS (SUSE10.1; Sun1.5.0\_07); EwaM (Ubuntu5.10, Sun1.5.0\_07); |
| Linux-ssh | MartinO (RHEL4); UweS (SUSE10.1); EwaM (Ubuntu5.10) |
| Linux-ftp |  |
| Solaris-dstore |  |
| Solaris-ssh | MartinO (Sol7); |
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

*   [Bugzilla test report: Reporter X Severity](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=bug_severity&y_axis_field=reporter&z_axis_field=&query_format=report-table&short_desc_type=allwordssubstr&short_desc=&classification=DSDP&product=Target+Management&component=RSE&long_desc_type=casesubstring&long_desc=RSE+1.0+Testing+round+1&bug_file_loc_type=allwordssubstr&bug_file_loc=&status_whiteboard_type=allwordssubstr&status_whiteboard=&keywords_type=allwords&keywords=&emailtype1=substring&email1=&emailtype2=substring&email2=&bugidtype=include&bug_id=&votes=&chfieldfrom=&chfieldto=Now&chfieldvalue=&format=table&action=wrap&field0-0-0=noop&type0-0-0=noop&value0-0-0=)
*   [Bugzilla test report: Reporter X Status](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=bug_status&y_axis_field=reporter&z_axis_field=&query_format=report-table&short_desc_type=allwordssubstr&short_desc=&classification=DSDP&product=Target+Management&component=RSE&long_desc_type=casesubstring&long_desc=RSE+1.0+Testing+round+1&bug_file_loc_type=allwordssubstr&bug_file_loc=&status_whiteboard_type=allwordssubstr&status_whiteboard=&keywords_type=allwords&keywords=&emailtype1=substring&email1=&emailtype2=substring&email2=&bugidtype=include&bug_id=&votes=&chfieldfrom=&chfieldto=Now&chfieldvalue=&format=table&action=wrap&field0-0-0=noop&type0-0-0=noop&value0-0-0=)
*   [Bugzilla test report: Reporter X Resolution](https://bugs.eclipse.org/bugs/report.cgi?x_axis_field=resolution&y_axis_field=reporter&z_axis_field=&query_format=report-table&short_desc_type=allwordssubstr&short_desc=&classification=DSDP&product=Target+Management&component=RSE&long_desc_type=casesubstring&long_desc=RSE+1.0+Testing+round+1&bug_file_loc_type=allwordssubstr&bug_file_loc=&status_whiteboard_type=allwordssubstr&status_whiteboard=&keywords_type=allwords&keywords=&emailtype1=substring&email1=&emailtype2=substring&email2=&bugidtype=include&bug_id=&votes=&chfieldfrom=&chfieldto=Now&chfieldvalue=&format=table&action=wrap&field0-0-0=noop&type0-0-0=noop&value0-0-0=)

Comments from Testers
---------------------

*   I think the reminders are great! -- [User:Michael.Scharf.windriver.com](https://wiki.eclipse.org/User:Michael.Scharf.windriver.com "User:Michael.Scharf.windriver.com")
*   We should have a formal database with test cases to perform. This could be just Wiki pages grouped by feature and/or use case. -- User:uwe.stieber.windriver.com
*   I thought it was well organized -- better than most. -- User:ted.williams.windriver.com
*   I thought the coverage was good. Also, the test instructions were good. -- User:kmunir.ca.ibm.com
*   FTP was just sanity tested since there are quite a lot of standing issues and the engine is going to be replaced. -- User:Javier.MontalvoOrus.symbian.com
*   Given that all assignment are voluntary it is good that you try to formalize things somewhat. (Haven't seen this in the CDT) -- User:norbert.ploett.siemens.com
*   The testing was very coordinated. -- User:Ewa.Matejska.palmsource.com
*   User:sumit.sarkar.gmail.com writes:
    *   A presentation from RSE team could have really helped to ramp up our testing and know the features. I didn't have much time reading the documentation.  :)
    *   I need to file another bug. I saw when a file name in HP-UX had a ":" in it, the files could not be loaded in the RSE/Eclipse editor.
    *   Didn't like the remote console (term) part. Why command line is separate from the console? It was slow. The lines in the console was selectable, but when I right-clicked, "Open With" was disabled. Did not know what to do? And why this feature is there and what it is supposed to do.
    *   In two separate installation of Eclipse and RSE, after eclipse crashed while opening the remote PPT file, the eclipse installation became unusable. It does not even come up now. Not sure, it is Eclipse problem or RSE. But as a user of RSE, I didn't like it.
    *   About the meeting notice, somehow I didn't get any meeting request. Got the mail only after I came to the office at 9:00am PDT. By the time meeting was over. I am pretty sure, you had the meeting notice somewhere

in the wiki page. But a reminder could have helped.

*   I thought it went very well. -- User:david_dykstal.us.ibm.com
*   Thanks to everybody! -- [Martin Oberhuber](https://wiki.eclipse.org/Martin_Oberhuber "Martin Oberhuber")


(Migrated from [https://wiki.eclipse.org/RSE_1.0_Testing_round_1](https://wiki.eclipse.org/RSE_1.0_Testing_round_1))