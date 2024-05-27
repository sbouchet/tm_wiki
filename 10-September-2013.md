

TM/Meetings/10-September-2013
=============================

< [TM](/TM "TM")‎ | [Meetings](/TM/Meetings "TM/Meetings")

Contents
--------

*   [1 When](#When)
*   [2 Agenda](#Agenda)
    *   [2.1 Action items from TM/Meetings/9-July-2013](#Action-items-from-TM.2FMeetings.2F9-July-2013)
    *   [2.2 Luna](#Luna)
    *   [2.3 Kepler](#Kepler)
    *   [2.4 Web site & wiki maintenance](#Web-site-.26-wiki-maintenance)
    *   [2.5 Bugs](#Bugs)
    *   [2.6 Community](#Community)
    *   [2.7 Foundation](#Foundation)
    *   [2.8 Committer status](#Committer-status)
    *   [2.9 Vacations](#Vacations)
    *   [2.10 Notes](#Notes)
    *   [2.11 Next Meeting](#Next-Meeting)
*   [3 Minutes](#Minutes)
    *   [3.1 Action items from TM/Meetings/10-September-2013](#Action-items-from-TM.2FMeetings.2F10-September-2013)
    *   [3.2 Bugs](#Bugs-2)
    *   [3.3 Community](#Community-2)
*   [4 Info](#Info)

When
----

10 September 2013 (Tuesday) at [1100 Rochester MN](http://www.timeanddate.com/worldclock/fixedtime.html?msg=Eclipse+TM+September+Committer+Call&iso=20130910T11&p1=159&am=30)  
![Html.gif](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/Html.gif)[calendar](http://www.google.com/calendar/embed?src=vn70im36r00qeusu8nme50cils@group.calendar.google.com&ctz=Canada/Toronto) ![Ical.gif](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/Ical.gif)[calendar](http://www.google.com/calendar/ical/vn70im36r00qeusu8nme50cils@group.calendar.google.com/public/basic.ics)

**Skype:** david\_dykstal to call martin.oberhuber, david-k-mcknight, uwe.stieber, and anna\_dushistova. All TM committers and interested parties are invited. Interested parties ping **david_dykstal** on Skype chat to be added to the call.

**Backup dial-in:** US & Canada (Toll-Free) 888-426-6840  
Austria (Caller Paid) 0-1-2530601  
For Other Countries: [AT&T Teleconference](https://www.teleconference.att.com/servlet/glbAccess?process=1&accessCode=8703125&accessNumber=2158616239)  
Participant Code: 8703125#

Agenda
------

### Action items from [TM/Meetings/9-July-2013](/TM/Meetings/9-July-2013 "TM/Meetings/9-July-2013")

*   Review bug backlogs (Fix target milestones; review / triage incoming high-severity issues)
    *   AI All
    *   Ongoing
*   Web Site
    *   AI DaveD - Update Website Docs where they refer to CVS (some done, more to do)
    *   AI DaveD - Maybe update the CVS repo putting in a "readme.txt" that project has migrated to git (still to do)
    *   AI DaveD - Webpages partially out-of-date --> migrate to Wiki; Wayne got something "almost done" that can be auto-generated. (done for the most part)
    *   Ongoing

### Luna

*   Luna is now building out of the master branch
*   Declaring participation in Luna?

### Kepler

*   Kepler SR1 build are ongoing from the TM\_3.5\_maintenance branch
*   SR1 releases at the end of September

### Web site & wiki maintenance

*   site continues to be updated as time permits

### Bugs

### Community

### Foundation

### Committer status

### Vacations

### Notes

### Next Meeting

*   Tuesday [TM/Meetings/8-October-2013](/TM/Meetings/8-October-2013 "TM/Meetings/8-October-2013")

Minutes
-------

### Action items from **TM/Meetings/10-September-2013**

*   none

### Bugs

*   continue to concentrate on high priority requests in the backlog

### Community

*   Dave Dykstal will be retiring from IBM at the end of September but can stay on as project lead until December 31. The team will need to work on recruiting a new project lead for Luna.

Info
----

*   Use this URL for committing: **[ssh://userid@git.eclipse.org:29418/tm/org.eclipse.tm.git](ssh://userid@git.eclipse.org:29418/tm/org.eclipse.tm.git)**
*   The Gerrit web UI is here: [https://git.eclipse.org/r/p/tm/org.eclipse.tm.git](https://git.eclipse.org/r/p/tm/org.eclipse.tm.git)
*   Docs for using Gerrit are here: [Gerrit](/Gerrit "Gerrit")
*   Cmdline (See [Git#Committers\_new\_to_Git](/Git#Committers_new_to_Git "Git")):

  git config --global --list
  git config --global user.email my\_committer\_email@address.com
  git config --global user.name "John Doe"
  git clone [ssh://userid@git.eclipse.org:29418/tm/org.eclipse.tm.git](ssh://userid@git.eclipse.org:29418/tm/org.eclipse.tm.git)
  #readonly:# git clone [git://git.eclipse.org/gitroot/tm/org.eclipse.tm.git](git://git.eclipse.org/gitroot/tm/org.eclipse.tm.git)
  <make changes>
  "git status" shows changes
  "git diff" shows difference (like patch format)
  git add <filename> -adds a file
  git rm <filename> removes a file
  then git commit -m"message" --to commit into your local repo
  git push -- to push to the remote repository

*   [TM/Git_Workflows](/TM/Git_Workflows "TM/Git Workflows") cheatsheet on Wiki: Get egit, **Setup egit**, Clone Repo (website / code), Update, Edit, Push, Switch branch

