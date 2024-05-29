

DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007
================================================

< [DSDP](/DSDP "DSDP")‎ | [TM](/DSDP/TM "DSDP/TM")

The meeting is primarily planned as a hands-on coding camp for contributors, with in-depth discussions about current and future TM/RSE architecture and hard problems, also involving looking right at the code.

We'd also discuss planning issues, additions of new components to the TM offering and the TM strategy moving forward (perhaps revising our Use Cases). See the [#Agenda](#Agenda) below for details about things to be discussed.

Location and Dates
------------------

*   Location:
    *   IBM Toronto Development Labs, Warden Ave between Highway 407 and Highway 7, Markham
    *   Suggested Hotel: [Hilton Suites Hotel & Conference Centre Toronto/Markham](http://www.hilton.com/en/hi/hotels/index.jhtml;jsessionid=4KXATC2AU1HHJJ31AOQMISQ?ctyhocn=YYZAPHF), Phone 905 470-8500
    *   For more hotel options, directions and other details, see the [DD 22-Feb-2006 meeting Logistics](/DSDP-DD_Face-to-face_Toronto_22-Feb-2006#Logistics "DSDP-DD Face-to-face Toronto 22-Feb-2006")
    *   **The meeting is in Toronto Sep 17/18 and NOT in Chicago with the [Eclipse Members Meeting](http://dev.eclipse.org/mhonarc/lists/eclipse.org-committers/msg00377.html) as previously announced!**
*   Exact time and Agenda are tentative, details will follow late July:
    *   Mon Sep/17: 0900-1700, **Planning**
        *   Introductions and Warm-up
        *   Hi-Level Pain Points and Plan Items by Company
        *   Other Items (2.0.2; Java 5; stuff not signed up)
        *   Time Constraints and Milestone Assignments
        *   Individual Bug Discussions
    *   Tue Sep/18: 0900-1700, **Operations**
        *   Introducing our work places
        *   Download Stats / Bugzilla Stats
        *   Improving the Way we Work: Pain-points and Highlights
        *   Interesting stuff to learn (Threads, Projects, Concepts)
        *   Long-Term Vision / Brainstorming
        *   Growing Community / EclipseCon 08
        *   Individual Bug Discussions 3.0/2.0.1
    *   Wed Sep/19: 0900-1200, **Coding Camp**
        *   Break-out sessions for peer programming

Attendees
---------

Please add yourself to this list if you plan to attend.

*   Martin Oberhuber, Wind River
*   Javier Montalvo Orus, Symbian
*   Dave Dykstal, IBM
*   Dave McKnight, IBM
*   Xuan Chen, IBM
*   Kevin Doyle, IBM
*   Kushal Munir, IBM (tentative / part-time)
*   Rupen Mardirossian, IBM (tentative / part-time)

Agenda
------

For each of the topics mentioned below, one presenter will be asked to prepare and look for possible architecture for the future of RSE. During the meeting, we will explore these prosals right with the code. Naturally, the topics are related to the [TM Future Planning](/TM_Future_Planning "TM Future Planning") page. Attendees can request to add topics to the agenda until Friday Sep-7th.

*   Come up with a consistent story around EFS vs. RSync vs. RSE (MartinO) - may be related to RemoteSystemsTempFiles
*   How to improve the RemoteTempFiles cache (DaveM): Put it outside the workspace ([158770](https://bugs.eclipse.org/bugs/show_bug.cgi?id=158770)), do not share between connections ([193858](https://bugs.eclipse.org/bugs/show_bug.cgi?id=193858)), allow characters only valid on the remote ([160103](https://bugs.eclipse.org/bugs/show_bug.cgi?id=160103)), support remote names differing only in case also on Windows ([160100](https://bugs.eclipse.org/bugs/show_bug.cgi?id=160100))
*   RSE Logging - what to log and where ([196317](https://bugs.eclipse.org/bugs/show_bug.cgi?id=196317)) (DaveD)
*   Architecture and changes for **deferred plugin loading** in RSE (DaveD, MartinO)
*   Hard problems with splitting RSE **UI/Non-UI/RCP**
    *   At the time of the F2F meeting, important steps for UI/Non-UI/RCP splitting should have been made in RSE 3.0 HEAD already
*   Architecture / Future of **SubSystemConfiguration componentization**
    *   We had an idea to split SubSystemConfiguration into static and dynamic parts
*   Architecture / Future of **Connection Groups and Multicore** / Multi-System support
*   Architecture / Future of RSE **User Actions** (Dave D)
*   Architecture / Future of RSE **Profiles and Team Support** (Dave D)
*   Architecture / Future of the RSE **Details View (Tableview): non-homogeneous contents, table headings, property descriptors** (Xuan Chen)
*   Architecture / Future of RSE **Wizard UI** (Xuan Chen)([bug 176490](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176490))
*   Unify Remote Monitor and Tableview? (DaveM)

More agenda items may spring off the

*   Bugzilla [open API bugs](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&cmdtype=doit&order=Assignee)
*   Bugzilla [plan items](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&keywords_type=allwords&keywords=plan&classification=DSDP&product=Target+Management&cmdtype=doit&order=Assignee)


(Migrated from [https://wiki.eclipse.org/DSDP/TM/Face-to-face_Meeting_Toronto_17-Sep-2007](https://wiki.eclipse.org/DSDP/TM/Face-to-face_Meeting_Toronto_17-Sep-2007))