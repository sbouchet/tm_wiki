

TM/Meetings/8-October-2013
==========================

< [TM](/TM "TM")‎ | [Meetings](/TM/Meetings "TM/Meetings")

Contents
--------

*   [1 When](#When)
*   [2 Agenda](#Agenda)
    *   [2.1 Action items from TM/Meetings/10-September-2013](#Action-items-from-TM.2FMeetings.2F10-September-2013)
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
    *   [3.1 Action items from TM/Meetings/10-September-2013](#Action-items-from-TM.2FMeetings.2F10-September-2013-2)
    *   [3.2 New Action Items](#New-Action-Items)
    *   [3.3 Bugs](#Bugs-2)
    *   [3.4 Community](#Community-2)
*   [4 Info](#Info)

When
----

8 October 2013 (Tuesday) at [1100 Rochester MN](http://www.timeanddate.com/worldclock/fixedtime.html?msg=Eclipse+TM+October+Committer+Call&iso=20131008T11&p1=159&am=30)  
![Html.gif](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/Html.gif)[calendar](http://www.google.com/calendar/embed?src=vn70im36r00qeusu8nme50cils@group.calendar.google.com&ctz=Canada/Toronto) ![Ical.gif](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/Ical.gif)[calendar](http://www.google.com/calendar/ical/vn70im36r00qeusu8nme50cils@group.calendar.google.com/public/basic.ics)

**Skype:** david\_dykstal to call martin.oberhuber, david-k-mcknight, uwe.stieber, anna\_dushistova, and lucas_gamm. All TM committers and interested parties are invited. Interested parties ping **david_dykstal** on Skype chat to be added to the call.

Agenda
------

### Action items from [TM/Meetings/10-September-2013](/TM/Meetings/10-September-2013 "TM/Meetings/10-September-2013")

*   Review bug backlogs (Fix target milestones; review / triage incoming high-severity issues)
    *   AI All
    *   Ongoing
*   Web Site
    *   AI DaveD - Update Website Docs where they refer to CVS (some done, more to do)
    *   AI DaveD - Maybe update the CVS repo putting in a "readme.txt" that project has migrated to git (still to do)
    *   AI DaveD - Webpages partially out-of-date --> migrate to Wiki; Wayne got something "almost done" that can be auto-generated. (done for the most part)
    *   Ongoing
*   Dave continuing as project lead for the time being. Still need to contact Greg Watson re PTP sponsorship.

### Luna

*   Luna is now building out of the master branch
*   Declaring participation in Luna?
*   M2 is out. We did not produce a build for M2. Will do one for M3.

### Kepler

*   Kepler SR1 is out. Built from the TM\_3.5\_maintenance branch.
*   Download page still to be constructed.

### Web site & wiki maintenance

*   Site continues to be updated as time permits

### Bugs

### Community

### Foundation

### Committer status

### Vacations

### Notes

### Next Meeting

*   Tuesday [TM/Meetings/05-Nov-2013](/TM/Meetings/05-Nov-2013 "TM/Meetings/05-Nov-2013")

Minutes
-------

### Action items from [TM/Meetings/10-September-2013](/TM/Meetings/10-September-2013 "TM/Meetings/10-September-2013")

*   AI DaveD - web site cleanup

### New Action Items

*   AI Manuel to write up a brief gerrit "how-to"
*   AI Anna to investigate HIPP for TM - Do we need one? How do we request one? How do we migrate our jobs?

### Bugs

*   Still problems with RSE initialization - probably due to stuff being done by extensions. DaveM and DaveD to follow up.

### Community

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

