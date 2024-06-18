

RSE 1.0M5 Known Issues and Workarounds
======================================

Nav: [DSDP/TM](/DSDP/TM "DSDP/TM") | [RSE 1.0 Testing](/RSE_1.0_Testing "RSE 1.0 Testing") | [RSE 1.0 Test Instructions](/RSE_1.0_Test_Instructions "RSE 1.0 Test Instructions") | RSE 1.0M5 Known Issues and Workarounds

* * *

This page lists the most obvious known issues with RSE 1.0M5.

**We encourage you to enable Wiki Watch for this page:** ensure that you are logged on to the Wiki, then click the little 'watch' tab on top of this page. On your personal "preferences" page (accessible from the top right of your screen) you can also enable E-Mail notifications for changes on this page. This will allow you to get notified when other testers find really bad issues that you might want to work around.

**This is a collaborative page:** Every tester may edit this page and add bugs he has filed, that are very obivious or problematic and that he or she'd like other testers to be able to work around to avoid.

See the [TM Bug Process Page](https://www.eclipse.org/dsdp/tm/development/bug_process.php) for queries to get the full list of known bugs out of bugzilla.  
See the [Open P1, P2 bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&component=RSE&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&priority=P1&priority=P2&cmdtype=doit) query for most important high-priority issues.

| **Bug #** | **Description** | **Workaround** |
| --- | --- | --- |
| [158524](https://bugs.eclipse.org/bugs/show_bug.cgi?id=158524) | IBM 1.5 JVM cannot start RSE - java.lang.VerifyError | Use a different JVM |
| [153652](https://bugs.eclipse.org/bugs/show_bug.cgi?id=153652) | Cannot drag&drop from RSE into C/C++ Projects View;   Various other drag&drop, copy&paste problems | Drag&drop into the Eclipse Project Navigator instead;   See the bug report for details on other drag&drop, copy&paste problems |
| [142953](https://bugs.eclipse.org/bugs/show_bug.cgi?id=142953) | No prompt on linux-dstore shell | Type several commands e.g. "ls", eventually you will get a prompt |
| [158319](https://bugs.eclipse.org/bugs/show_bug.cgi?id=158319) | Remote Resources are not shown although they are there | With filtering in the files tree, when multiple filters evaluate to showing the same resource, it can happen that the resource is not shown under some filters. Workaround: disconnect and reconnect the connection. Expand only one filter at a time. |

(Back to [RSE 1.0 Testing](/RSE_1.0_Testing "RSE 1.0 Testing") | [RSE 1.0 Test Instructions](/RSE_1.0_Test_Instructions "RSE 1.0 Test Instructions"))


(Migrated from [https://wiki.eclipse.org/RSE_1.0M5_Known_Issues_and_Workarounds](https://wiki.eclipse.org/RSE_1.0M5_Known_Issues_and_Workarounds))