

TM/Connection Groups
====================

< [TM](./TM "TM")

Lead: TBD  
Members: Mentor, Freescale, Curtiss-Wright, WindRiver

We want to define groups of connections, and groups of components (cores) on a connection such that actions performed on the group are performed on each element of the group. Such actions may occur on several levels:

*   Synchronous Run-Control (lowest level; synchronous)
*   Downloads to multiple targets (not synchronous; parallel; sequential)
*   Multi-Language Debugging (coordinated Java / JNI debuggers; related to [Inter-Debugger Communications](./Inter-Debugger_Communications "DSDP/TM/Inter-Debugger Communications"))
*   Reservation from a [Shared Board Lab](./Shared_Board_Labs "DSDP/TM/Shared Board Labs")

Related bugs: [159164](https://bugs.eclipse.org/bugs/show_bug.cgi?id=159164)

Related initiatives: [Eclipse Parallel Tools Platform (PTP)](https://www.eclipse.org/ptp)

Contribution from Serge Beauchamp, Freescale Semiconductor: Another use case for connection groups can be described as follows:

Some customers have some hardware setup where different Data Collection Units (DCU) can be physically connected to targets. Because the target to which they are connected can change, or the DCU become temporarily disconnected for any targets, it appears natural to have DCU represented as hosts themselves in the RSE tree that can be grouped under other hosts (or subsystems of hosts) - the targets to which they are connected.

By being grouped under a host in the RSE tree, software components could programatically derive many settings (Core, etc...) required to the configuration of the DCU and configuration of the target.

