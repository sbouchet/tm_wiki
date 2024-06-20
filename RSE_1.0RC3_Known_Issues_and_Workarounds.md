

RSE 1.0RC3 Known Issues and Workarounds
=======================================

Nav: [DSDP/TM](./TM "DSDP/TM") | [RSE 1.0 Testing](./RSE_1.0_Testing "RSE 1.0 Testing") | [RSE 1.0 Test Instructions](./RSE_1.0_Test_Instructions "RSE 1.0 Test Instructions") | RSE 1.0RC3 Known Issues and Workarounds

* * *

This page lists the **most obvious known issues** with RSE 1.0RC3 and suggests workarounds. By "most obvious" we mean those issues that many testers are likely to encounter. Note that there may be other severe or critical issues not listed here, because they are less likely to occur. See the [Bugzilla: RSE Major and Critical](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit) query to show those.

**We encourage you to enable Wiki Watch for this page:** ensure that you are logged on to the Wiki, then click the little 'watch' tab on top of this page. On your personal "preferences" page (accessible from the top right of your screen) you can also enable E-Mail notifications for changes on this page. This will allow you to get notified when other testers find really bad issues that you might want to work around.

**This is a collaborative page:** Every tester may edit this page and add bugs he has filed, that are very obivious or problematic and that he or she'd like other testers to be able to work around to avoid.

See the [TM Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for queries to get the full list of known bugs out of bugzilla.  
See the [Open P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit) query for most important high-priority issues.

| **Bug #** | **Description** | **Workaround** |
| --- | --- | --- |
| [153652](https://bugs.eclipse.org/bugs/show_bug.cgi?id=153652) | Cannot drag&drop from RSE into C/C++ Projects View;   Various other drag&drop, copy&paste problems | Drag&drop into the Eclipse Project Navigator instead;   See the bug report for details on other drag&drop, copy&paste problems |
| [160084](https://bugs.eclipse.org/bugs/show_bug.cgi?id=160084) | RSE is hanging eclipse and slowing down my system dramatically | Check the Progress View. If there are several RSE "Resolving Filter Strings" jobs that do not go away, quit and re-start RSE. |
| [160111](https://bugs.eclipse.org/bugs/show_bug.cgi?id=160111) | A blocking RSE job "hangs" the entire RSE system | Check the Progress View. If there are several RSE "Resolving Filter Strings" jobs that do not go away, quit and re-start RSE. Disconnect / Reconnect might also work. |
| [160293](https://bugs.eclipse.org/bugs/show_bug.cgi?id=160293) | RSE perspective doesn't start if only Core is installed | Install at least a service plugin (SSH, FTP...) |

Older Known Issues:

*   [RSE 1.0RC1 Known Issues and Workarounds](./RSE_1.0RC1_Known_Issues_and_Workarounds "RSE 1.0RC1 Known Issues and Workarounds")
*   [RSE 1.0M5 Known Issues and Workarounds](./RSE_1.0M5_Known_Issues_and_Workarounds "RSE 1.0M5 Known Issues and Workarounds")

(Back to [RSE 1.0 Testing](./RSE_1.0_Testing "RSE 1.0 Testing") | [RSE 1.0 Test Instructions](./RSE_1.0_Test_Instructions "RSE 1.0 Test Instructions"))


(Migrated from [https://wiki.eclipse.org/RSE_1.0RC3_Known_Issues_and_Workarounds](https://wiki.eclipse.org/RSE_1.0RC3_Known_Issues_and_Workarounds))