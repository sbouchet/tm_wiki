

TM/Launching
============

< [TM](/TM "TM")

Lead: Martin Oberhuber (Wind River)  
Members: Nokia, Freescale

We want to pursue a component-based approach to Launching.

*   [Presentation](https://www.eclipse.org/downloads/download.php?file=/dsdp/tm/presentations/2006-2-23_Toronto_TM_LaunchActions.ppt) at the 23-Feb-2006 Face-to-face meeting

The idea is to have an additional tab in the Launch, where you see a list of entries. Each entry is of type ILaunchAction, where implementations of ILaunchAction can be contributed through plugin.xml. Each ILaunchAction brings an associated UI for configuring it.

Examples of ILaunchAction could be a RunShellCommandLaunchAction, or a DownloadFileLaunchAction, each of which could use RSE services in turn. The LaunchActionSequencer, which runs one action after the other can even be generic (independent of RSE), just like the LaunchActionManager which would be responsible for persisting the ILaunchAction data into ILaunchConfiguration instances.

Proposed design by Robert Norton:

[Media:LaunchActions.png](/images/7/77/LaunchActions.png "LaunchActions.png") [Media:LaunchActionUI.png](/images/7/73/LaunchActionUI.png "LaunchActionUI.png")

