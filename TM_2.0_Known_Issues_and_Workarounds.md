

TM 2.0 Known Issues and Workarounds
===================================

Nav: [DSDP/TM](./DSDP/TM "DSDP/TM") | [TM and RSE FAQ](./TM_and_RSE_FAQ "TM and RSE FAQ") | [TM 2.0 Testing](./TM_2.0_Testing "TM 2.0 Testing") | TM 2.0 Known Issues and Workarounds | [TM 3.0 Known Issues and Workarounds](./TM_3.0_Known_Issues_and_Workarounds "TM 3.0 Known Issues and Workarounds")

* * *

This page lists the **most obvious known issues** with [TM 2.0](http://download.eclipse.org/dsdp/tm/downloads/) and suggests workarounds. By "most obvious" we mean those issues that many users are likely to encounter. Note that there may be other severe or critical issues not listed here, because they are less likely to occur. See the [Bugzilla: TM Major and Critical, P1 and P2](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor) query to show those.

**We encourage you to enable Wiki Watch for this page:** ensure that you are logged on to the Wiki, then click the little 'watch' tab on top of this page. On your personal "preferences" page (accessible from the top right of your screen) you can also enable E-Mail notifications for changes on this page. This will allow you to get notified when other users find important problems that you might be able to work around.

**This is a collaborative page:** Every user may edit this page and add bugs he or she has filed, that are very obivious or problematic and that he or she'd like other users to be able to work around to avoid. See the [TM Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for queries to get the full list of known bugs out of bugzilla.  

Known Problems in TM 2.0.x
--------------------------

[TM 2.0.2](http://download.eclipse.org/dsdp/tm/downloads/drops/R-2.0.2-200711131300/) is the latest official release.

| **Bug #** | **Description** | **Workaround** |
| --- | --- | --- |
| [181458](https://bugs.eclipse.org/bugs/show_bug.cgi?id=181458) | Cannot drag&drop / copy&paste from remote to Windows Explorer | We had to take out the "Download on Copy" workaround again because of [critical bug 189268](https://bugs.eclipse.org/bugs/show_bug.cgi?id=189268). A proper fix will need a fix in SWT. **Workaround:** Copy&Paste to the RSE "Local" file system instead. |
| [153652](https://bugs.eclipse.org/bugs/show_bug.cgi?id=153652) | Cannot drag&drop from remote into the Project Explorer | We had to take out the "Download on Copy" workaround again because of [critical bug 189268](https://bugs.eclipse.org/bugs/show_bug.cgi?id=189268). A proper fix will need support for the "PluginTransfer" method in the Project Explorer. **Workaround:** Open the Resource Navigator in a separate view, then drag&drop to the Resource Navigator instead. |
| [190803](https://bugs.eclipse.org/bugs/show_bug.cgi?id=190803) | Some long-running dstore commands cannot be canceled | When a "list directory" query is extremely slow because of e.g. missing mounted file systems, the dstore server gets unresponsive because it is single-threaded for "list" type queries. Other queries are multi-threaded, so fixing this in the future should not be too hard. Unfortunately, when the client cancels the operation further access to the hanging dstore server may block the UI. **Workaround**: When a dstore connection hangs, cancel the job in the progress view, then disconnect and reconnect the hanging connection. This will restart the dstore server. |

Issues fixed in recent milestones
---------------------------------

| **Bug #** | **Fixed in** | **Description** |
| --- | --- | --- |
| ~~[209656](https://bugs.eclipse.org/bugs/show_bug.cgi?id=209656)~~, ~~[209662](https://bugs.eclipse.org/bugs/show_bug.cgi?id=209662)~~ | [TM 3.0M3](http://download.eclipse.org/dsdp/tm/downloads/drops/S-3.0M3-200711141025/) | **Eclipse 3.4 only**: When running on Eclipse 3.4M3, the TM 2.0.x Terminal leads to ClassCastExceptions, missing menu items and slow operation in general |
| ~~[205393](https://bugs.eclipse.org/bugs/show_bug.cgi?id=205393)~~ | [TM 2.0.2](http://download.eclipse.org/dsdp/tm/downloads/drops/R-2.0.2-200711131300/) | **2.0.1 regression: Terminal causes stack overflow** \-\- has been fixed and promoted to Europa Fall Maintenance Update. |
| ~~[205186](https://bugs.eclipse.org/bugs/show_bug.cgi?id=205186)~~ | [TM 2.0.2](http://download.eclipse.org/dsdp/tm/downloads/drops/R-2.0.2-200711131300/) | **2.0.1 regression**: Terminal does not paint properly on Mac OSX -- has been fixed and promoted to Europa Fall Maintenance Update. |
| ~~[(query)](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=substring&short_desc=%5Befs&classification=DSDP&product=Target+Management&target_milestone=---&target_milestone=2.0.1&target_milestone=Future&cmdtype=doit)~~ | [TM 2.0.1](http://download.eclipse.org/dsdp/tm/downloads/drops/R-2.0.1-200709262145/) | Problems with EFS Integration  All known major EFS related issues have been fixed for TM 2.0.1. In many cases we think that the problem is not with the TM/RSE EFS provider but with the clients not being prepared for remote resources through EFS properly. We encourage all projects to be aware that resources in the workspace are not necessarily fast to access, in the case they actually reside on a remote computer linked in through EFS. TM/RSE is a great toolkit to verify EFS-awareness.   |
| ~~[179937](https://bugs.eclipse.org/bugs/show_bug.cgi?id=179937)~~ | [TM 2.0.1](http://download.eclipse.org/dsdp/tm/downloads/drops/R-2.0.1-200709262145/) | (BIDI) File and Path names in files tree do not honor encoding: For SSH and FTP, this has been fixed in TM 2.0.1; for dstore, it is possible to launch the server with required encoding settings (see the bug for details). For enhanced usbility, dstore should also use the host-wide encoding control in the future. |
| ~~[192741](https://bugs.eclipse.org/bugs/show_bug.cgi?id=192741)~~ | [TM 2.0.0.1](http://download.eclipse.org/dsdp/tm/downloads/drops/R-2.0.0.1-200707061039/) / [I20070705-0600](http://download.eclipse.org/dsdp/tm/downloads/) | **Moving a folder from a ZIP archive fails if > 1 level deep** \- this could mean loss of data.  A patch is provided with TM 2.0.0.1. See [the TM 2.0.0.1 blog](http://tmober.blogspot.com/2007/07/dsdp-tm-rse-2001-critical-patch-release.html) for details.   |
| ~~[194204](https://bugs.eclipse.org/bugs/show_bug.cgi?id=194204)~~ | [TM 2.0.0.1](http://download.eclipse.org/dsdp/tm/downloads/drops/R-2.0.0.1-200707061039/) / [I20070705-0600](http://download.eclipse.org/dsdp/tm/downloads/) | **RSE FTP: Renaming Files/Folders moves them sometimes** \- this could mean loss of data. A patch is provided with TM 2.0.0.1. See [the TM 2.0.0.1 blog](http://tmober.blogspot.com/2007/07/dsdp-tm-rse-2001-critical-patch-release.html) for details. |

  
(Back to [TM 2.0 Testing](./TM_2.0_Testing "TM 2.0 Testing") | [TM 2.0 Test Instructions](./TM_2.0_Test_Instructions "TM 2.0 Test Instructions") | [TM 3.0 Known Issues and Workarounds](./TM_3.0_Known_Issues_and_Workarounds "TM 3.0 Known Issues and Workarounds"))


(Migrated from [https://wiki.eclipse.org//TM_2.0_Known_Issues_and_Workarounds](https://wiki.eclipse.org//TM_2.0_Known_Issues_and_Workarounds))