

Eclipse File Service APIs Compared
==================================

This page compares features and use cases for remote file access APIs that are currently found in Eclipse.

**This document is under construction, not finished yet.**

Contents
--------

*   [1 Eclipse Remote File APIs](#Eclipse-Remote-File-APIs)
    *   [1.1 RSE Files API](#RSE-Files-API)
    *   [1.2 Eclipse Filesystem (EFS) API](#Eclipse-Filesystem-.28EFS.29-API)
    *   [1.3 Team/Target Management API](#Team.2FTarget-Management-API)
    *   [1.4 ECF fileshare API](#ECF-fileshare-API)
*   [2 RSE and Remote Files APIs](#RSE-and-Remote-Files-APIs)

Eclipse Remote File APIs
------------------------

### RSE Files API

*   [viewcvs: IFileService.java](http://dev.eclipse.org/viewcvs/index.cgi/org.eclipse.tm.rse/plugins/org.eclipse.rse.services/src/org/eclipse/rse/services/files/IFileService.java?rev=HEAD&cvsroot=DSDP_Project&content-type=text/vnd.viewcvs-markup)
*   [viewcvs: IHostFile.java](http://dev.eclipse.org/viewcvs/index.cgi/org.eclipse.tm.rse/plugins/org.eclipse.rse.services/src/org/eclipse/rse/services/files/IHostFile.java?rev=HEAD&cvsroot=DSDP_Project&content-type=text/vnd.viewcvs-markup)
*   Supports remote move, remote copy operations
*   Categorization of remote files, including support for symbolic links (derived classes of IHostFile)
*   Use Strings as canonical pathes (with '/' file separator)
*   Very lightweight and simple to implement since only Strings and two interfaces
*   Synchronous operations for upload, download (with IProgressMonitor, suitable for jobs)
*   No callbacks or other "watch" facilities
*   Supports remote file encodings different from local
*   RSE implementation does persistent caching of remote files

### Eclipse Filesystem (EFS) API

*   [viewcvs: IFileStore.java](http://dev.eclipse.org/viewcvs/index.cgi/org.eclipse.core.filesystem/src/org/eclipse/core/filesystem/IFileStore.java?rev=HEAD&content-type=text/vnd.viewcvs-markup)
*   Overview on [bug 106176 plan: provide more flexible workspaces](https://bugs.eclipse.org/bugs/show_bug.cgi?id=106176)
*   Existing sample implementations for [ZIP](https://bugs.eclipse.org/bugs/show_bug.cgi?id=138277) and [FTP](https://bugs.eclipse.org/bugs/show_bug.cgi?id=137878) file systems
*   Fully integrated with Platform Resources, allows transparent access to remote files
*   Fully abstract notion of remote pathes through URI for the root, plus parent/child relationships for the siblings
*   Supports remote move, remote copy operations
*   Synchronous operations for upload, download (with IProgressMonitor, suitable for jobs)
*   Originally written for performance optimizations on the local file system (through native calls), plus fully abstract access to remote file stores like databases
*   No notion of symbolic links or other advanced attributes
*   No callbacks or other "watch" facilities
*   URI has been criticized to be heavy-weight (but is only needed to specify the filesystem root, not necessarily the siblings)
*   Registered via extension point - problematic if multiple different implementations for the same access scheme exist, e.g. two implementations for "ftp:" access scheme in URI
*   API for file caching during the current Eclipse session

### Team/Target Management API

*   Will be dropped in favor of EFS, according to the Platform/Team group.
*   Will then provide FTP and WebDAV implementations for EFS

### ECF fileshare API

*   [viewcvs: IFileShare](http://dev.eclipse.org/viewcvs/index.cgi/org.eclipse.ecf/plugins/org.eclipse.ecf.fileshare/src/org/eclipse/ecf/fileshare/IFileShareContainer.java?rev=HEAD&cvsroot=Technology_Project&content-type=text/vnd.viewcvs-markup)
*   asynchronous send and receive with events

RSE and Remote Files APIs
-------------------------

*   Currently, RSE uses the RSE files API on its backend
*   Allows to present whatever backend implementation as an EFS on its frontend
*   Eventually, RSE could also accept EFS providers on its Files backend. The value-add of RSE over plain EFS would then be
    *   persistent caching
    *   access to remote resources outside the workspace
    *   connection and filter management
        *   selection of channels
        *   password/keyring management
    *   association of shell and other channels with the files channel


(Migrated from [https://wiki.eclipse.org/Eclipse_File_Service_APIs_Compared](https://wiki.eclipse.org/Eclipse_File_Service_APIs_Compared))