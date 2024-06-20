

RSESync/Status and Ideas
========================

Contents
--------

*   [1 Status of RSE Synchronization Plugin](#Status-of-RSE-Synchronization-Plugin)
*   [2 Open Issues (bugs)](#Open-Issues-.28bugs.29)
    *   [2.1 Filtering folder selection in the Wizard](#Filtering-folder-selection-in-the-Wizard)
    *   [2.2 Wrong synchronize status](#Wrong-synchronize-status)
    *   [2.3 Improve context menu in Team Synchronize View](#Improve-context-menu-in-Team-Synchronize-View)
    *   [2.4 Clarify Text mode vs. Binary mode transfer](#Clarify-Text-mode-vs.-Binary-mode-transfer)
    *   [2.5 Other / UI issues](#Other-.2F-UI-issues)
*   [3 Additional Ideas](#Additional-Ideas)
    *   [3.1 Remote Folder Compare funcitionality](#Remote-Folder-Compare-funcitionality)
    *   [3.2 Create / Improve API for non-UI diff / synchronize](#Create-.2F-Improve-API-for-non-UI-diff-.2F-synchronize)
    *   [3.3 Add Unittest](#Add-Unittest)
    *   [3.4 Backup / Undo functionality](#Backup-.2F-Undo-functionality)
    *   [3.5 Auto synchronization / timer functionality](#Auto-synchronization-.2F-timer-functionality)
    *   [3.6 Dry Run](#Dry-Run)
    *   [3.7 Label decorations for up-to-date status in RSE](#Label-decorations-for-up-to-date-status-in-RSE)
    *   [3.8 Using commands like "rsync", "md5sum" on remote for advanced compare performance](#Using-commands-like-.22rsync.22.2C-.22md5sum.22-on-remote-for-advanced-compare-performance)
    *   [3.9 Version management](#Version-management)

Status of RSE Synchronization Plugin
------------------------------------

As per [6-Feb-2009](/index.php?title=6-Feb-2009&action=edit&redlink=1 "6-Feb-2009 (page does not exist)")

The initial Summer of Code [Platform/Team Synchronization on top of RSE](/Platform/Team_Synchronization_on_top_of_RSE "Platform/Team Synchronization on top of RSE") contribution has been merged into RSE HEAD: **As per RSE 3.1m5**, it is part of the org.eclipse.rse.importexport plugin (which now depends on Java 1.5 due to the contribution). Original [bug 185925](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185925) is now closed, but can still be used for comments and suggestions.

At its current state, the contribution still has many [#Open Issues (bugs)](#Open-Issues-.28bugs.29) and is not yet ready for end user consumption. Community help for resolving the remaining issues is would be much appreciated! In most cases, you should find out what's going wrong if you compare the code against the old FTP plugin. [Bug 185925 comment 11](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185925#c11) has instructions for how to get that into your workspace.

Open Issues (bugs)
------------------

### Filtering folder selection in the Wizard

*   Filters of folder selection in the import/export wizard are not yet observed by the synchronize plugin.

When using the RSE Export wizard to select certain files and folders below a common root for synchronizing only, that selection is not observed by the synchronization plugin. To date, only complete folder trees can be synchronized.

### Wrong synchronize status

The Synchronize perspective shows files as changed even if they are not changed. Correct computation of the difference is a must-have for correct closing of this feature. This issue seems to be caused by 2 problems.

*   **Setting timestamp**. When exporting files, I probably don't set the original timestamp of the file but the timestamp when it's copied up. I must check the Preference setting of RSE and UniversalFileTransferUtility line 1591 (ISystemFilePreferencesConstants.PRESERVETIMESTAMPS).
*   **Comparing method**. Comparing files to see if they are the same, I only compare timestamp. I should at least also compare the size. And when size and timestamp match, then I must make a real diff to see if the binary contents match.

On a similar issue, upload all to "Local:D:\\tmp". Synchronize same project again: There's all conflicts, but it should all be in sync.

### Improve context menu in Team Synchronize View

*   Unnecessary menu pops-up in the Team Synchronize View. For example, in initial export, the menu has "Get". It's confusing for user. If user select in-coming change resource, "Get" shoule be disable. Like this, I must adapt the contents of menu to the situation.
*   Lack of support for managing options completely that are configured in the Import / Export Wizard. For example, there is "Overwrite" option in the menu which overwrite the local resource but no option for overwriting the remote one. At least, I must implement "Overrite Put" as mentioned above.

### Clarify Text mode vs. Binary mode transfer

*   RSE has a Preference to transfer some file types in text mode. This is important for files stored with very different encodings on the host. Need to clarify and specify how such files should be transferred / compared -- use binary transfer and original host encoding or text transfer? Where and how to actually compare?

### Other / UI issues

*   From the *.rexpfd contextmenu, open the Export Wizard. State of the "Review/Synchronize" checkbox is not preserved.
*   Should have a "Resynchronize" context menu on *.rexpfd / *.rimpfd
*   User Docs missing
*   In the "Synchronize" View, choosing "Synchronize" there is no synchronization provider for RSE

Additional Ideas
----------------

*   Avoid Java5 dependency

### Remote Folder Compare funcitionality

Currently there are only synchronization between local and remote resources. Remote Folder Compare functionality makes usability more. There are some techinical issues. First, the RepositoryProvider responsible for configuring a "project" for repository management and providing the necessary hooks for resource modification, but in remote side, there are no "project" ( of course, no workspace). In the remote side, the resources are only file or folder but RepositoryProvider can only manage project. Second, Team Synchronization API are structed as premises for comparison of IResource (local) with ResourceVariant (base, remote). How to solve these problem? And Synchronize Wizard as the Import / Export Wizard may be necessary to select the target and source resources.

### Create / Improve API for non-UI diff / synchronize

On the provider side, it should be possible to plug in algorithms for comparing local with remote data. On the client side, it should be possible to run such a comparison (and/or uptimized upload/download which only transfers modified items) in a non-UI manner.

### Add Unittest

There are little Test Case for non-ui synchronize operation. Current unittest tests only the functions of ISynchronizeConnectionManager. The remaining unittest needs to be done for all other functions completely.

### Backup / Undo functionality

When fatal error occurs or user run wrong synchronization, the undo functionality is necessary such as version management system like svn / cvs has. By storing the data of each synchronization, user can undo the synchronized resources wrongly.

### Auto synchronization / timer functionality

If user is lazy and bothers to Synchronize, this is needed. The auto synchronization can be done using timer or condition user can define. Using timer, once user sets the timer, Auto Synchronization work regularly. Using user condition, when the status of resources matches the condition, they are synchronized. For example, only the resources that have out-going change status and are synchronized more than 1 hour ago are synchornized. In this example, if resources has in-coming change or are synchronized 30 minitues ago, they are not synchronized. This configuration can be set or removed by using context menu or simple UI whenever user wants.

I think that the Platform/Team framework may already provide such a timer -- CVS, at least, does support timed auto synchronization.

### Dry Run

Dry run allows users to confirm that syncronizations will result intended such as rsync. This is to be effective in the cases which user donâ€™t grasp the details of syncronized files or which user's experience is a little for synchronization, or in the case which the synchronized resources are very important and synchronization must be succesful. Actual synchronization can be run based on the previous dry run seamlessly. In other words, dry run can be done with the option flag in the Import / Export Wizard.

### Label decorations for up-to-date status in RSE

"up-to-date/ modified" label decorators in the RSE System View and / or the Eclipse Process Explorer, like CVS does them, based on a previous RSE-synchronization. Synchronization integration might have to register as a Team Provide for that to work, but then, if an existing team provider is registered with a project, the RSE-provider should still be able to decorate the tree with additional decorators.

### Using commands like "rsync", "md5sum" on remote for advanced compare performance

If the remote host has useful commands of "rsync", "md5", et al, they can be used for Syncronization. For example, using md5, we can check compliance between local and remote, so reliability and accurasy of syncronization gain.

### Version management

Like CVS or SVN, the version management is useful functionality for synchronization. However, only version management is not so useful. For this functionality, the "Backup / Undo functionality" and "Label decorations for up-to-date status in RSE" are at least necessary as the same to CVS or SVN. Platform/Team provides some APIs for versioning in the Local History or probably elsewhere.


(Migrated from [https://wiki.eclipse.org/RSESync/Status_and_Ideas](https://wiki.eclipse.org/RSESync/Status_and_Ideas))