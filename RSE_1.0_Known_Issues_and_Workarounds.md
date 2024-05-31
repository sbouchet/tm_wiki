

RSE 1.0 Known Issues and Workarounds
====================================

Nav: [DSDP/TM](./TM "DSDP/TM") | [TM and RSE FAQ](./TM_and_RSE_FAQ "TM and RSE FAQ") | [RSE 1.0 Testing](./RSE_1.0_Testing "RSE 1.0 Testing") | RSE 1.0 Known Issues and Workarounds

* * *

This page lists the **most obvious known issues** with [RSE 1.0](http://download.eclipse.org/dsdp/tm/downloads/drops/R-1.0-200611121600/index.php) and suggests workarounds. By "most obvious" we mean those issues that many users are likely to encounter. Note that there may be other severe or critical issues not listed here, because they are less likely to occur. See the [Bugzilla: RSE Major and Critical, P1 and P2](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor) query to show those.

**We encourage you to enable Wiki Watch for this page:** ensure that you are logged on to the Wiki, then click the little 'watch' tab on top of this page. On your personal "preferences" page (accessible from the top right of your screen) you can also enable E-Mail notifications for changes on this page. This will allow you to get notified when other users find important problems that you might be able to work around.

**This is a collaborative page:** Every user may edit this page and add bugs he or she has filed, that are very obivious or problematic and that he or she'd like other users to be able to work around to avoid. See the [TM Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for queries to get the full list of known bugs out of bugzilla.  

| **Bug #** | **Description** | **Workaround** |
| --- | --- | --- |
| [153652](https://bugs.eclipse.org/bugs/show_bug.cgi?id=153652) | Cannot drag&drop from RSE into C/C++ Projects View;   Various other drag&drop, copy&paste problems | Drag&drop into the Eclipse Project Navigator instead;   See the bug report for details on other drag&drop, copy&paste problems |
| [160293](https://bugs.eclipse.org/bugs/show_bug.cgi?id=160293) | RSE perspective doesn't start if only Core is installed | Install at least a service plugin (SSH, FTP...) |
| [149122](https://bugs.eclipse.org/bugs/show_bug.cgi?id=149122), [164202](https://bugs.eclipse.org/bugs/show_bug.cgi?id=164202), [161308](https://bugs.eclipse.org/bugs/show_bug.cgi?id=161308) | Exception in Properties; Refactoring History Page in weird places | The Refactoring History Property Page can pop up in weird places, and may lead to exceptions. This is a known Platform issue with Eclipse 3.2.1 ([bug 154735](https://bugs.eclipse.org/bugs/show_bug.cgi?id=154735)). Workaround: When you see the Refactoring History page, close the properties dialog and open it again -- it will be gone, and RSE works as expected. This bug has been fixed for Eclipse 3.3M4. |

(Back to [RSE 1.0 Testing](./RSE_1.0_Testing "RSE 1.0 Testing") | [RSE 1.0 Test Instructions](./RSE_1.0_Test_Instructions "RSE 1.0 Test Instructions"))


(Migrated from [https://wiki.eclipse.org/RSE_1.0_Known_Issues_and_Workarounds](https://wiki.eclipse.org/RSE_1.0_Known_Issues_and_Workarounds))