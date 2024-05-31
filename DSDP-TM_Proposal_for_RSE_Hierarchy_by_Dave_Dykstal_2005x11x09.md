

TM/Proposal for RSE Hierarchy by Dave Dykstal 2005x11x09
========================================================

< [TM](/TM "TM")(Redirected from [DSDP-TM Proposal for RSE Hierarchy by Dave Dykstal 2005x11x09](/index.php?title=DSDP-TM_Proposal_for_RSE_Hierarchy_by_Dave_Dykstal_2005x11x09&redirect=no "DSDP-TM Proposal for RSE Hierarchy by Dave Dykstal 2005x11x09"))

The main UI point of organization in RSE is the Remote Systems View -- the hierarchical view of systems / subsystems / filterpools / filters / resources / ... One thing I've never asked is how you see this structure playing out in the TM world. Here's one way of looking at it, but I'm not sure its what you envision.

Linux System A
Linux System B
Device X (this could be a core, DSP, or whatever - a "targettable entity")
     Processes (subsystem)
           My Processes (filter)
                 Process A (resource)
                       Thread 1
                       Thread 2
                 Process B
                       Thread 1
     Modules (subsystem)
           My Modules (filter)
                 Module 1 (maybe in a different color or decoration if symbols are available or loaded)
                 Module 2
           Kernel Extensions
                 KEXT1
                 KEXT2
     Co-Devices (devices in the same "target group" as Device X -- this is something I just dreamed up to get target groups cheaply)
           Device Type A (filter)
                 Device W
                 Device Y
           Device Type B
     Files (subsystem)
           My Files (filter)
                 Folder F
                       File F1
                 File 1
     Commands
           My Commands
                 Command 1
                 Command 2
           Standard Commands
Device Y

**Note:** [Uwe Stieber](/index.php?title=User:Uwe.stieber.windriver.com&action=edit&redlink=1 "User:Uwe.stieber.windriver.com (page does not exist)") added some important thoughts to the [discussion tab](/Talk:DSDP-TM_Proposal_for_RSE_Hierarchy_by_Dave_Dykstal_2005x11x09 "Talk:DSDP-TM Proposal for RSE Hierarchy by Dave Dykstal 2005x11x09") of this page


(Migrated from [https://wiki.eclipse.org/DSDP-TM_Proposal_for_RSE_Hierarchy_by_Dave_Dykstal_2005x11x09](https://wiki.eclipse.org/DSDP-TM_Proposal_for_RSE_Hierarchy_by_Dave_Dykstal_2005x11x09))