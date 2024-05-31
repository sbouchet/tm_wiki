

DSDP/TM/Committer Phone Meeting 26-Jun-2007
===========================================

< [DSDP](https://wiki.eclipse.org/DSDP "DSDP")‎ | [TM](./TM "DSDP/TM")

| Meeting Title: | **TM Committer Phone Meeting** |
| --- | --- |
| Date & Time: | Tuesday Jun 26, 2007 at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=6&day=26&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800) |
| Dial-in: | International **+44 (0)1452 567588**   North America **+1 (866) 6161738** (toll free)   UK National **08712460713**   Passcode: **0587322148 #** |

MartinO to start conference call - please dial in using the numbers above.  
**Please be available for Skype Chat in parallel to the call.** MartinO will start Skype chat just prior to call.  
Skype fallback dial-in - only if less than 5 participants: **martin.oberhuber**, ddykstal (or david\_dykstal), david-k-mcknight, kushal.munir, javier.montalvoorus, tedatteddotnet, michael\_scharf, and uwe.stieber.  

Contents
--------

*   [1 Invited Attendees](#Invited-Attendees)
*   [2 Notes](#Notes)
    *   [2.1 News & Review Action Items](#News-.26-Review-Action-Items)
    *   [2.2 Plan for the TM Future](#Plan-for-the-TM-Future)
    *   [2.3 Ramp Down Plan](#Ramp-Down-Plan)
    *   [2.4 Open Work for 2.0](#Open-Work-for-2.0)
    *   [2.5 Work post 2.0](#Work-post-2.0)
*   [3 Vacation, Away](#Vacation.2C-Away)
*   [4 Action Items](#Action-Items)
*   [5 Next Meeting](#Next-Meeting)

Invited Attendees
-----------------

*   IBM - Dave McKnight, Dave Dykstal, Xuan Chen, (Kevin Doyle n/a), (Kushal Munir n/a)
*   Symbian - Javier Montalvo Orús
*   Wind River - Martin Oberhuber, Uwe Stieber, Michael Scharf

This is an Open call, so anyone else can join (though we expect the talk to be interesting for committers only).

Notes
-----

*   Last meeting: [DSDP/TM/Committer Phone Meeting 19-Jun-2007](./Committer_Phone_Meeting_19-Jun-2007 "DSDP/TM/Committer Phone Meeting 19-Jun-2007")

### News & Review Action Items

| Martin | 0% |  | 100% |
| --- | --- | --- | --- |
| DaveD | 90% | some doc fixes, but things went fairly smoothly | 90% |
| DaveM | 0% |  | 30% |
| Javier | 30% |  | 30% |
| Uwe | 5% | - | 5% |
| Michael | 10% | 1 bugfix for terminal | 10% |

### Plan for the TM Future

*   Please review and edit [TM Future Planning](./TM_Future_Planning "TM Future Planning") together with your Requirements / Product Management folk
*   A TM Project Meeting is planned for SEPTEMBER 19th and 20th in Chicago, together with the Members Meeting.

### Ramp Down Plan

*   [TM 2.0 Ramp down Plan for Europa](./TM_2.0_Ramp_down_Plan_for_Europa "TM 2.0 Ramp down Plan for Europa"), based on [Europa Simultaneous Release#Milestones and Release Candidates](./Europa_Simultaneous_Release#Milestones_and_Release_Candidates "Europa Simultaneous Release")
    *   EUROPA -- Jun 29 -- **No more automatic builds** (only on request) - **Wednesday is the absolute final day**
    *   Testing: **Please use RSE recent I-builds yourselves in daily work**

### Open Work for 2.0

*   Reminder: All our API is still declared "provisional". Is this ok for everyone?
*   **All-committer-review required from now on**
*   [Severity Major Bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit):
    *   [193380](https://bugs.eclipse.org/bugs/show_bug.cgi?id=193380) Deleting Connection Refresh's Entire Remote Systems View - not major, assigned 2.0.1
    *   [193858](https://bugs.eclipse.org/bugs/show_bug.cgi?id=193858) RSE folder tree problem - tempfiles do not take connection name or user id on remote side into account; similar to tempfiles structure does not support tunnelling - **AI DaveM** check whether remoteMountPathMappers extension point can be used to change the mapping scheme; for the future, probably subsystems should contribute some means of qualification
    *   [187301](https://bugs.eclipse.org/bugs/show_bug.cgi?id=187301) (Martin) Telnet does not allow multiple shells
        *   Martin wants to apply the (cleaned-up) patch, will affect telnet only
*   Other known bugs:
    *   [192610](https://bugs.eclipse.org/bugs/show_bug.cgi?id=192610) (Javier) Create a link to an RSE folder makes eclipse freeze
        *   Will likely require a note of caution on using EFS remote projects.
        *   Javier could reproduce (with FTP); blocked as long as files were being retrieved from remote server (could be hundreds of files); refreshed file status of hundreds of files (or did it retrieve the files to do some parsing?) - Martin would like to know why it's running in foreground; DaveD: both JDT and CDT are not particularly good at being EFS clients
            *   **AI Javier**: Check FTP Log: Does it download files or just check timestamp? Does it check the same files again and again or always different ones? Also, try a thread dump and attach it to the bug, so we can see who ran it in the UI thread.
            *   **Thread Dump Utility**:
                *   On UNIX, do [kill -SIGQUIT](http://www.google.at/url?sa=t&ct=res&cd=2&url=http%3A%2F%2Fforum.java.sun.com%2Fthread.jspa%3FthreadID%3D658931%26messageID%3D3870534&ei=CDWBRumUDYvO-gKk6KWxAQ&usg=AFQjCNGRxjDpZTipottXxnZkiaZ2D3y9tA&sig2=fCjm0ANtZHKmOPi6axmMDA) in order to get a thread dump on the console
                *   On Windows, use [AdaptJ Java StackTrace](http://www.adaptj.com/root/main/tracehowtos) (click on "Launch StackTrace" on the web page; it's free when launched from the Web. Attach to the program. In the stacktrace, you can copy&paste, or save the trace.
    *   Several Doc issues opened (broken links) - affect doc plugin only; **AI DaveD**
*   DStore: Change the default daemon port for 2.0, since the protocol is not compatible? - Would allow multiple dstore daemons for multiple different versions run in parallel on one host
    *   DaveM: IBM internally uses different daemon ports for different protocol versions right now; different IBM products have different ways of dealing with this, e.g. z/OS has its own daemon; TPF uses rexec; for testing, just pick a port; in the past, administrators just knew what's going on; DaveM slightly in favor of changing the port number but not seen as critical since people typically specifiy their own ports; DaveD thinks it would be a good idea for convenience (increment 4035 to 4036)
        *   IANA Port Numbers: [http://www.iana.org/assignments/port-numbers](http://www.iana.org/assignments/port-numbers) search for Unassigned, e.g. 4370 Unassigned
        *   **AI Martin** file bug for DaveM
*   **New & Noteworthy** \- **AI Martin create, others fill in**
*   **Release Notes**
    *   These will live in the www-tm-development project. Please fill in!

### Work post 2.0

*   Javadoc Reviews: @since tag for new API, missing @param tags, ... better don't change since these force rebuild of many plugins
*   Currently feels like too many bugs are assigned 2.0.1 -- but we'll decide that after 2.0 is released
    *   Kushal some of your assigned are 2.0.1 -- will you be able to work on those?
*   2.0.1 work can be done in branches - e.g. "temp201_dwd"? Merge immediately after 2.0 declared. **Caution:** 2.0.1 must be binary compatible with 2.0.0. Ensure that you have read the Eclipse API Guidelines again to understand what the restrictions are.
    *   Platform has branched 3.3.1 already, and releases 3.3 from the branch
*   Other work
    *   Discouraged Access Warnings: switch off for dstore by using x-friend in Manifest?
        *   subsystems.files.dstore --> dstore.extra: DomainNotifier.addDomainListener(), DomainNotifier.removeDomainListener() - DaveM: This is a dstore-specific thing and should not be public API
        *   DaveD: Friend may be the right thing in many cases; but we might be hiding some stuff that should be API, so we should treat these case by case
        *   Should look at the list of x-friend declarations and check if these still hold
        *   Filed [bug #194475](https://bugs.eclipse.org/bugs/show_bug.cgi?id=194475) to track these
    *   **Kushal**: [174789](https://bugs.eclipse.org/bugs/show_bug.cgi?id=174789) Property pages added to Wizard automatically: **AI Kushal** investigate (will likely be taken by DaveD - Kushal to leave the team?)
    *   **Martin**: [186315](https://bugs.eclipse.org/bugs/show_bug.cgi?id=186315) EFS problematic URIs - would love to see those fixed, supposedly affect efs plugin only
        *   Releng scripts: won't consume Commons Net officially via Orbit for now
*   **Bugzilla**: [Severity Major](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&bug_severity=blocker&bug_severity=critical&bug_severity=major&cmdtype=doit), [hi-priority](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&field0-0-0=priority&type0-0-0=regexp&value0-0-0=P%5B12%5D&field0-0-1=bug_severity&type0-0-1=regexp&value0-0-1=blocker%7Ccritical%7Cmajor)

Vacation, Away
--------------

*   DaveM, DaveD taking a couple weeks in August
*   Javier ooo last two weeks in August

Action Items
------------

*   [Last Meeting](./Committer_Phone_Meeting_19-Jun-2007#Action_Items "DSDP/TM/Committer Phone Meeting 19-Jun-2007") Action Items
*   **Everybody**: Comment / Grant Review on [194442](https://bugs.eclipse.org/bugs/show_bug.cgi?id=194442) default dstore daemon port, [187301](https://bugs.eclipse.org/bugs/show_bug.cgi?id=187301) telnet multiple shells
*   **DaveD**: Doc bugs (broken links)
*   **DaveM**: Check whether mountPathMappers can workaround [193858](https://bugs.eclipse.org/bugs/show_bug.cgi?id=193858), comment on the bug about reason and possible workarounds; [194442](https://bugs.eclipse.org/bugs/show_bug.cgi?id=194442) change dstore daemon default port
*   **Kushal**:
*   **Martin**: [187301](https://bugs.eclipse.org/bugs/show_bug.cgi?id=187301) telnet; create new&notewothy, release notes
*   **Javier**: Investigate [192610](https://bugs.eclipse.org/bugs/show_bug.cgi?id=192610) as mentioned during the meeting, add comments on the bug
*   **Michael**:

Next Meeting
------------

*   [DSDP/TM/Committer Phone Meeting 3-Jul-2007](./Committer_Phone_Meeting_3-Jul-2007 "DSDP/TM/Committer Phone Meeting 3-Jul-2007") at [1500 UTC](http://www.timeanddate.com/worldclock/meetingdetails.html?year=2007&month=7&day=3&hour=15&min=00&sec=0&p1=224&p2=159&p3=250&p4=136&p5=223&iv=1800)
*   Monthly [DSDP/TM/Phone Meeting 4-Jul-2007](./Phone_Meeting_4-Jul-2007 "DSDP/TM/Phone Meeting 4-Jul-2007") at [9am PST / 1600 UTC](http://www.timeanddate.com/worldclock/fixedtime.html?month=7&day=4&year=2007&hour=16&min=00&sec=0&p1=0)


(Migrated from [https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_26-Jun-2007](https://wiki.eclipse.org//DSDP/TM/Committer_Phone_Meeting_26-Jun-2007))