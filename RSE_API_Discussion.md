

RSE API Discussion
==================

As we are working towards an RSE 1.0 release, which should contain stable, accepted APIs, we want to expose the RSE APIs to discussion in a broader public.

This page serves as the entry point into those discussions. It will point to overview articles and serve as the starting point to convey the overall picture of RSE APIs.

Individual API discussions will be held on Bugzilla. Please file your requests for API changes as enhancement requests with the String **\[api\]** in the subject. At regular intervals, we will search bugzilla for such requests and sort them into this overview page as appropriate.

The following is an index into bugzilla to show currently ongoing discussions on RSE API.

*   [Bugzilla: All RSE Open API Issues](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=%5Bapi&classification=DSDP&product=Target+Management&component=RSE&long_desc_type=allwordssubstr&long_desc=&bug_file_loc_type=allwordssubstr&bug_file_loc=&status_whiteboard_type=allwordssubstr&status_whiteboard=&keywords_type=allwords&keywords=&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&emailtype1=substring&email1=&emailtype2=substring&email2=&bugidtype=include&bug_id=&votes=&chfieldfrom=&chfieldto=Now&chfieldvalue=&cmdtype=doit&order=Reuse+same+sort+as+last+time&query_based_on=RSE+open+%5Bapi%5D&field0-0-0=noop&type0-0-0=noop&value0-0-0=) query
    *   Clarify Error Handling in Services - [bug 149472](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&bug_id=149472)
    *   Allow empty user id / password - [bug 142471, 147532](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&bug_id=142471,147532)
    *   Clarify multiple parallel service requests - [bug 142478, 149133, 149179](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&bug_id=142478,149133,149179)
        *   Service classes like IFileService are public: any client can get access to the service and issue requests at any time! Therefore, it looks like we probably **have to** make all services thread-safe.
        *   This could be done by implementing a generic queueing class e.g.

 if (fAccessQueue.waitForTicket(IProgressMonitor monitor)) {
    try { /* do some work */ }
    finally {
       fAccessQueue.leave();
    }
 }

*   *   SystemRegistry.createHost() should not persist and allow to specify subsystems - [bug 150168, 150265](https://bugs.eclipse.org/bugs/buglist.cgi?query_format=advanced&bug_id=150168,150265)

  

Contents
--------

*   [1 API Overview](#API-Overview)
    *   [1.1 Core and System Registry API](#Core-and-System-Registry-API)
    *   [1.2 Services API](#Services-API)
        *   [1.2.1 Messaging API](#Messaging-API)
        *   [1.2.2 Files API](#Files-API)
        *   [1.2.3 Shellls API](#Shellls-API)
        *   [1.2.4 Processes API](#Processes-API)
        *   [1.2.5 Persistence Manager](#Persistence-Manager)
        *   [1.2.6 Remote Search API](#Remote-Search-API)
    *   [1.3 UI-Related APIs](#UI-Related-APIs)
        *   [1.3.1 UI Model](#UI-Model)
        *   [1.3.2 Subsystem Configuration](#Subsystem-Configuration)
        *   [1.3.3 Filtering](#Filtering)
        *   [1.3.4 Profiles and Team Management](#Profiles-and-Team-Management)
        *   [1.3.5 Files Subsystem](#Files-Subsystem)
        *   [1.3.6 Processes Subsystem](#Processes-Subsystem)
        *   [1.3.7 Shells Subsystem](#Shells-Subsystem)

API Overview
============

The following is an overview of all RSE API. See also the RSE ISV documentation.

Core and System Registry API
----------------------------

*   org.eclipse.rse.core: IRSECoreRegistry, IRSESystemType
    *   systemTypes.exsd -- missing documentation

Services API
------------

*   org.eclipse.rse.services: IService

### Messaging API

*   [SystemMessage](http://dev.eclipse.org/viewcvs/index.cgi/org.eclipse.tm.rse/plugins/org.eclipse.rse.services/clientserver/org/eclipse/rse/services/clientserver/messages/SystemMessage.java?rev=HEAD&cvsroot=DSDP_Project&content-type=text/vnd.viewcvs-markup) required in SystemMessageException required in IFileService (and others)
    *   Uses XML files for messages, this is not standard Eclipse behavior
    *   It should be possible to write RSE services without depending on SystemMessage

### Files API

*   [Eclipse File Service APIs Compared](/Eclipse_File_Service_APIs_Compared "Eclipse File Service APIs Compared")
*   org.eclipse.rse.services.files: IHostFile, IFileService
*   Check IClassifierConstants (from clientserver)

### Shellls API

*   org.eclipse.rse.services.shells: IShellService, IHostSHell, AbstractHostShell, IHostShellChangeEvent, IHostShellOutput*

### Processes API

*   org.eclipse.rse.services.processes: IProcessService, IHostProcess, IHostProcessFilter
*   API should be moved to single package (currently also ...clientserver)

### Persistence Manager

*   org.eclipse.rse.ui/persistence: IRSEPersistenceProvider, IRSEPersistenceManager, IRSEPersistableContainer
    *   persistenceProviders.exsd
    *   Currently in rse.ui, should go to non-UI (core) plugin?

### Remote Search API

*   org.eclipse.rse.services.search: ISearchService, IHostSearchResultConfiguration, IHostSearchResultSet, IHostSearchResult, ISearchHandler, IHostSearchResultConfigurationFactory
*   Check SystemSearchString (from clientserver)

UI-Related APIs
---------------

To be discussed:

*   org.eclipse.rse.ui
    *   archivehandlers.exsd -- go to services.files?
    *   compile.exsd -- go to services.files or services.shells?
    *   dynamicPopupMenuExtensions.exsd -- replace by Platform popupMenus?
    *   keystoreProviders.exsd
    *   mountPathMappers.exsd
    *   passwordPersistence.exsd
    *   popupMenus.exsd -- replace by Platform popupMenus?
    *   propertyPages.exsd -- replace by Platform propertyPages?
    *   remoteSystemsViewPreferencesAction.exsd -- ??
    *   systemtype.exsd -- obsoleted by systemType ??

### UI Model

*   org.eclipse.rse.ui/org.eclipse.rse.model
    *   IHost, IProperty, IPropertySet, IPropertySetContainer, IRSEModelObject
    *   ISystemModelChangeEvent, ISystemModelChangeListener
    *   ISystemPreferenceChange* -- Replace by Platform equivalent?
    *   ISystemRegistry -- go to rse.core?

### Subsystem Configuration

*   org.eclipse.rse.ui
    *   subsystemConfiguration.exsd -- Still has some com.ibm.etools...
    *   ISubSystemConfiguration, SubSystemConfiguration, ServiceSubSystemConfiguration -- can this large class/interface be splitted?
    *   ISubSystemConfigurationProxy -- can this be made internal?
    *   ISystemValidator
    *   IHost
    *   ISubSystem
    *   IConnectorService, IServerLauncherProperties

### Filtering

*   org.eclipse.rse.ui/org.eclipse.rse.filters
    *   ISystemFilterPoolManagerProvider, ISystemFilter, ISystemFilterConstants, ...
    *   ISystemFilterNamingPolicy, ISystemFilterPool

### Profiles and Team Management

*   org.eclipse.rse.ui/
    *   ISystemFilterPool, ISystemProfile

### Files Subsystem

*   org.eclipse.rse.subsystems.files.core/model
    *   IRemotePath, ISystemFileAPIProvider, ISystemFileRemoteTypes, ISystemFileTransferModeMapping, ISystemFileTransferModeRegistry, ISystemRemoteCommand, ISystemRemoteCommandMessage
    *   IRemoteFile, IRemoteFileContext, IVirtualRemoteFile,...
    *   IHostFileToRemoteFileAdapter

### Processes Subsystem

*   org.eclipse.rse.subsystems.processes.core/subsystem
    *   IHostProcessToRemoteProcessAdapter, IRemoteProcess, IRemoteProcessContext
    *   IRemoteProcessSubSystemConfiguration

### Shells Subsystem

*   org.eclipse.rse.subsystems.shells.core/model
    *   ISystemOutputRemoteTypes
    *   ICandidateCommand, IRemoteCmdSubSystem, IRemoteError, IRemoteOutput
*   Duplication?
*   Push the dstore remote command matchers into core?


(Migrated from [https://wiki.eclipse.org/RSE_API_Discussion](https://wiki.eclipse.org/RSE_API_Discussion))