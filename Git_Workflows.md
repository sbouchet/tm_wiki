

TM/Git Workflows
================

< [TM](/TM "TM")

Contents
--------

*   [1 Installation](#Installation)
    *   [1.1 Windows Install](#Windows-Install)
    *   [1.2 Linux Install](#Linux-Install)
*   [2 Cloning the Repo](#Cloning-the-Repo)
    *   [2.1 Configure the workspace](#Configure-the-workspace)
    *   [2.2 Configuring the repo](#Configuring-the-repo)
*   [3 TODO](#TODO)
    *   [3.1 Nice-to-have additions](#Nice-to-have-additions)

Installation
============

Windows Install
---------------

1.  Install [Tortoise Git](http://code.google.com/p/tortoisegit/). Not a must-have but helpful. Recommended to install this first.
2.  Install [Msysgit](http://code.google.com/p/msysgit/downloads/list?can=2&q=%22Full+installer+for+official+Git+for+Windows%22) as per the Tortoise Git instructions. Not a must-have but strongly recommended from the start, in order to be consistent between egit and commandline.
3.  Launch Git Bash
    *   If it is slow for you, you may want to set a **HOME** environment variable to a local disk and update the Git Bash program shortcut
        *   For me, the default %HOMEDRIVE%%HOMEPATH% pointed to a non-existing remote folder, making everything dead slow
        *   So I've set HOME=D:/Workspaces/git -- all your git repos will be below there by default, and your user config too
    *   Re-start Git Bash to verify it is fast and HOME is accurate
4.  Set up your user ID on git bash as per [Git#Committers\_new\_to_Git](/Git#Committers_new_to_Git "Git").
    *   Eclipse Committers who don't want to expose their E-Mail Address can use their committerid instead of the E-Mail address.

  git config --global user.email my\_committer\_email@address.com
  git config --global user.name "John Doe"
  git config --global branch.autosetuprebase always

1.  Launch Eclipse SDK and install latest [Egit](https://www.eclipse.org/egit) from [http://download.eclipse.org/egit/updates](http://download.eclipse.org/egit/updates)
    *   Check **Preferences > Team > Git > Configuration** whether it picked up your commandline settings
        *   May need to specify Location of Msysgit install in System Settings
        *   May want to update Default Repository Folder in Git : Cloning Repositories
        *   In user settings, verify **branch.autosetuprebase = always** as per [Platform-releng/Git\_Workflows#Configure\_the_workspace](/Platform-releng/Git_Workflows#Configure_the_workspace "Platform-releng/Git Workflows")
        *   In Preferences > **General > Workspace**, set **New text file line delimiter** to **Unix**
    *   Check **Preferences > General > Network > SSH2** home directory
        *   Set to your $HOME/.ssh in order to share with Msysgit - or copy the $HOME/.ssh folder
        *   Generate a private/public key pair if necessary (in the UI, or on Git Bash as per below link)
        *   Upload your [Gerrit#SSH_Keys](/Gerrit#SSH_Keys "Gerrit") \- using a passphrase is recommended
2.  Set up SSH private key for Tortoise Git (this is re-used by Egit)
    *   Launch **C:\\Program Files\\TortoiseGit\\bin\\puttygen.exe** to load your openssh private key and convert into a putty private key in your home/.ssh
    *   Launch **C:\\Program Files\\TortoiseGit\\bin\\pageant.exe** ; right-click the icon in taskbar and load your putty private key (agent will serve Egit, Msysgit and Tortoisegit)
        *   Recommend placing a link for pageant on your desktop to ensure SSH authentication with your private key
        *   **NOTE** Inside Egit this should also be possible somehow internal with JSch / Jgit but I did not get it to work

Linux Install
-------------

This is a subset of the Windows install since more settings will be appropriate by default.

1.  Set up your user ID on git commandline as per [Git#Committers\_new\_to_Git](/Git#Committers_new_to_Git "Git")

  git config --global user.email my\_committer\_email@address.com
  git config --global user.name "John Doe"
  git config --global branch.autosetuprebase always

1.  Launch Eclipse SDK and install latest [Egit](https://www.eclipse.org/egit) from [http://download.eclipse.org/egit/updates](http://download.eclipse.org/egit/updates)
    *   *   In user settings, set **branch.autosetuprebase = always** as per [Platform-releng/Git\_Workflows#Configure\_the_workspace](/Platform-releng/Git_Workflows#Configure_the_workspace "Platform-releng/Git Workflows")
    *   Upload your [Gerrit#SSH_Keys](/Gerrit#SSH_Keys "Gerrit")

  

Cloning the Repo
================

*   **Optiona A (Recommended)**: Using [EGit](/EGit "EGit") and **File > Import > Team > Team Project Set**:
    *   Committers import [tm-all-committer.psf](http://eclipse.org/tm/development/tm-all-committer.psf)
    *   Users/Contributors import [tm-all-anonymous.psf](http://eclipse.org/tm/development/tm-all-anonymous.psf)

*   **Optiona B - Commandline:**

 cd $HOME/git
 git clone [ssh://userid@git.eclipse.org:29418/tm/org.eclipse.tm.git](ssh://userid@git.eclipse.org:29418/tm/org.eclipse.tm.git)
 #readonly:# git clone [git://git.eclipse.org/gitroot/tm/org.eclipse.tm.git](git://git.eclipse.org/gitroot/tm/org.eclipse.tm.git)
 git clone [ssh://committer_id@git.eclipse.org/gitroot/www.eclipse.org/tm.git](ssh://committer_id@git.eclipse.org/gitroot/www.eclipse.org/tm.git)
 #readonly:# git clone [http://git.eclipse.org/gitroot/www.eclipse.org/tm.git](http://git.eclipse.org/gitroot/www.eclipse.org/tm.git)

*   **Option C - Plain Egit UI** \- Refer to [EGit/User Guide](/EGit/User_Guide "EGit/User Guide") for more detailed instructions
    *   File > Import > Git : Projects from Git
        *   URI, Next, Paste URL: **[ssh://userid@git.eclipse.org:29418/tm/org.eclipse.tm.git](ssh://userid@git.eclipse.org:29418/tm/org.eclipse.tm.git)**, Edit userid, Next
            *   Read-only contributors paste **[git://git.eclipse.org/gitroot/tm/org.eclipse.tm.git](git://git.eclipse.org/gitroot/tm/org.eclipse.tm.git)**
        *   Import projects from file system as needed, next
    *   If desired, import the website repository the same way
*   For contributing to the Simultaneous Release, see [Simrel/Contributing\_to\_Simrel\_Aggregation\_Build#Get\_the\_simrel.build_project](/Simrel/Contributing_to_Simrel_Aggregation_Build#Get_the_simrel.build_project "Simrel/Contributing to Simrel Aggregation Build")

Configure the workspace
-----------------------

\[This section originally copied from [Platform-releng/Git\_Workflows#Configure\_the_workspace](/Platform-releng/Git_Workflows#Configure_the_workspace "Platform-releng/Git Workflows").

Open the **Team > Git > Configuration** preference page and select the **User Settings** tab.

*   Verify entries for **user.name** and **user.email**. If you don't want to share your e-mail you can also use your committer account ID. Note that you will not be able to push changes to the repository if the latter property is not matching with your records at the Eclipse Foundation.
*   Verify entry **branch.autosetuprebase = always**

On the **General > Workspace** preference page, set **New text file line delimiter** to **Unix**.

Set up JRE's, Target Platform and API Baseline as per [TM/Code Streams](/TM/Code_Streams "TM/Code Streams")

Configuring the repo
--------------------

This section originally copied from [Platform-releng/Git\_Workflows#Configuring\_the_repo](/Platform-releng/Git_Workflows#Configuring_the_repo "Platform-releng/Git Workflows").

Make sure that you set **core.autocrlf = false** and on Windows **core.filemode = false**. If you use EGit to clone the repository then the latter is done automatically for you.

Unless you are working on topic branches, we work in a fairly linear history. Please make sure branch.**branchname**.rebase = true is set. If you've set **branch.autosetuprebase = always** as explained in [#Configure\_the\_workspace](#Configure-the-workspace), then this is done automatically.

Otherwise, once you've cloned a repository, you can go to the **Preferences > Team > Git > Configuration** page. Select your repository, select the branch you picked when you cloned the repository, and click **New Entry...**. Append "rebase" to the text in the 'Key' field and enter "true" as value.

![RepositoryConfigurationSettings.png](https://raw.githubusercontent.com/wiki/eclipse-datatools/.github/images/RepositoryConfigurationSettings.png)

TODO
====

*   Git Workflows - for commandline see also [TM/Meetings/30-Oct-2012#Git_Migration](/TM/Meetings/30-Oct-2012#Git_Migration "TM/Meetings/30-Oct-2012")
*   Git Workflows - see [Platform-releng/Git_Workflows](/Platform-releng/Git_Workflows "Platform-releng/Git Workflows") for now

Nice-to-have additions
----------------------

*   Tortoise Git User Setting - synchronized with Git Bash ?!?
*   Convert .cvsignore files into .gitignore
*   Add [Gerrit](/Gerrit "Gerrit") setup info for egit (changeset, push for review)
*   Reduce cdt dependency for tm-terminal-local
*   Terminal ESC-K addition
*   CQ Terminal trim addition
*   Fix Juno version numbers to be 3.4.2 like
*   Promote a Kepler build to Simrel
*   Review .api_description in Tycho
*   Get rid of cvs references from the tm website

