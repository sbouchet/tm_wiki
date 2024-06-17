

DSDP/TM/Phone Meeting 10-Apr-2006
=================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Monday April 10, 2006 at 9am PST |
| Primary International Dial-in: | **+44 (0)1452 567588** |
| USA Freephone Dial-In: | +1 (866) 6161738 |
| UK National Dial-In: | 08712460713 |
| Passcode: | **0587322148 #** |

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
    *   [2.1 Action Items still open from last meetings](#Action-Items-still-open-from-last-meetings)
    *   [2.2 New Action Items](#New-Action-Items)
    *   [2.3 Next Meeting](#Next-Meeting)

Attendees
---------

*   Martin Oberhuber - Wind River
*   David Dykstal, Kushal Munir, Dave McKnight, Mike Burger - IBM
*   Doug Schaefer - QNX
*   Aaron Spear, Mentor Graphics

Agenda
------

*   Breaking News: RSE Accepted by Eclipse IP Review!
*   Update on EclipseCon
    *   About 70 people at DSDP-TM long talk; Explicit interest from Siemens (Norbert Ploett), Cisco ("saved him weeks"); a team from Nokia (Ken Ryall?) was very interested in the Datastore stuff, especially the server - wanted to do that in August
    *   CDT was pretty hot at EclipseCon too, especially in terms of Embedded; the whole CDT / DSDP / Embedded talks seemed to be very focused on Debugging
    *   PTP / Parallel guys were very interested in RSE; they need very high scalability; TM has a different angle; especially data transfer to the frontend machine of the Big Iron; for debugging, they are more interested in the changes that have been done to the Platform for DSDP
    *   RSE with ssh plugins to become "committer tool"
    *   Want more "marketing" on the Community as soon as first downloadable milestones of RSE are available
*   Update on RSE Submission, IP Review and [Project Plan](https://www.eclipse.org/dsdp/tm/development/plan.php)
    *   IP Review passed!
    *   Milestone M1 to slip by 2 weeks (new date April 21);
    *   other milestones to stay unchanged; but might need some modification of milestone content as we proceed
    *   MartinO to update the website accordingly, and post a newsgroup item
*   Update on RSE Extensions
    *   Daytime example subsystem - completed, will be added to M1
    *   ssh example service - remote command view working, need some polishing before release; commands part will be released with M1; files part hopefully too; MartinO to submit as bugzilla
    *   ECF filesharing plugin - in work; want technology hooked up, not for M1
    *   CDT Remote Launch - Ewa Matejska agreed to work on it, no current status available
*   Technology sub-groups
    *   [Console View](https://wiki.eclipse.org/DSDP/DD/ConsoleView "DSDP/DD/ConsoleView")
        *   Aaron Spear started discussion; Darin and Debug Group seems to be open to enhancements from DD;
        *   Overlap between TM's terminal and a debugger specific terminal is mostly the Terminal Emulation
        *   Aaron seeking a framework where even non-text-based (graphical) output can be rendered in a contributed terminal view, based on the data the comes through a console stream
    *   TM Sub Groups
        *   No activity so far; everybody's busy with getting RSE out
        *   MartinO to contact PeterL and EwaM
        *   Hope to get more contribution once RSE M1 is out
*   Wind River's Cleanroom Telnet Implementation
    *   Doug Gaff wants to package WR's terminal view contributions with the telnet service, might take some more time therefore
    *   Work towards getting Jakarta Commons telnet in the meantime; start the EMO process immediatly - DaveD has an FTP implementation against Jakarta Commons ready (for M1, want to use URL-based FTP instead of the current Sun FTP which is unstable)
*   Next steps
    *   Get RSE M1 out; prototyping, bugzilla's

### Action Items still open from last meetings

*   Symbian:
    *   Write up interface description for "Service" as understood by Symbian
*   Pierre-Alexandre:
    *   Write up additional use case for STAF

### New Action Items

*   MartinO:
    *   Update Website, send note on M1 schedule changes
    *   Contact PeterL, EwaM
    *   Start EMO process for Jakarta Commons
*   RSE Team:
    *   Get CVS Repository populated, build in place and RSE M1 out

### Next Meeting

*   Next [DSDP/TM/Phone Meeting 3-May-2006](./Phone_Meeting_3-May-2006 "DSDP/TM/Phone Meeting 3-May-2006") (4 weeks)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_10-Apr-2006](https://wiki.eclipse.org//DSDP/TM/Phone_Meeting_10-Apr-2006))