

Platform/Team Synchronization on top of RSE
===========================================

< [Platform](/Platform "Platform")

Contents
--------

*   [1 Abstract](#Abstract)
*   [2 Development](#Development)
    *   [2.1 Developers](#Developers)
    *   [2.2 Plug-ins](#Plug-ins)
    *   [2.3 Features](#Features)
    *   [2.4 Resources](#Resources)
    *   [2.5 Bugzilla](#Bugzilla)
*   [3 Current Status](#Current-Status)
*   [4 Download](#Download)
*   [5 Community Proposals](#Community-Proposals)

Abstract
--------

The goal of this project is implementation of synchronization function on top of Remote System Explorer (RSE) using Eclipse Platform/Team Synchronization API. RSE provides transparent access to remote resources, including upload and download of files. Compare/merge of entire directory trees as well as minimal upload of trees thanks to Synchronization is currently a missing and often-asked-for feature. Initial Synchronization is already implemented by import/export so incremental synchronization is needed. The goals would be integrating Platform/Team synchronization APIs on top of RSE file providers first, and then improving the algorithms for performing remote comparisons with minimal data transfer (by using timestamps, file sizes and MD5 hashes eventually).

Development
-----------

### Developers

*   Martin Oberhuber(Mentor)
*   Takuya Miyamoto

### Plug-ins

*   org.eclipse.rse.*
*   org.eclipse.team.*

### Features

*   Provide a Synchronization on RSE.
*   Provide a possibility to re-run Synchronization which was run in the past.
*   Improve transfer performance.
*   Improve comparison method.

### Resources

[RSE Project page](https://www.eclipse.org/dsdp/tm/)

[TM Tutorial Eclipse Con 2008 document(ppt)](https://www.eclipse.org/downloads/download.php?file=/dsdp/tm/presentations/TM_Tutorial_ECon08.ppt)

[Synchronize API Introduction document(ppt)](https://www.eclipse.org/eclipse/platform-team/team3.0/Team%20Synchronization.ppt)

[Synchronize API Eclipse Help](http://dsdp.eclipse.org/help/latest/index.jsp?topic=/org.eclipse.platform.doc.isv/guide/team_synchronize.htm)

[RSE Architecture Eclipse Help](http://dsdp.eclipse.org/help/latest/index.jsp?topic=/org.eclipse.rse.doc.isv/guide/rse_int_architecture.html)

### Bugzilla

[bug 185925](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185925) holds discussions, patches and documents for this feature

Current Status
--------------

As per [6-Feb-2009](/index.php?title=6-Feb-2009&action=edit&redlink=1 "6-Feb-2009 (page does not exist)"), the initial Summer of Code contribution has been merged into RSE HEAD: As per RSE 3.1m5, it is part of the org.eclipse.rse.importexport plugin (which now depends on Java 1.5 due to the contribution). Original [bug 185925](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185925) is now closed, but can still be used for comments and suggestions.

At its current state, the contribution still has many Open Issues (bugs) and is not yet ready for end user consumption. **See [RSESync/Status and Ideas](/RSESync/Status_and_Ideas "RSESync/Status and Ideas") for what currently works or needs to be done.**

Development of the plugin continues - everybody is welcome to contribute, by means of testing, patches, ideas or actually committing some code. Please get in touch with us on the [dsdp-tm-dev](https://dev.eclipse.org/mailman/listinfo/dsdp-tm-dev) mailing list if you are interested.

Download
--------

The plugin is part of RSE 3.1M5 and later.

If you want to use it in Eclipse 3.4 / RSE 3.0, you can still get it from the old SF update site:

*   Update site
    *   [http://eclipse-incub.sourceforge.net/updates-soc/rse-sync/](http://eclipse-incub.sourceforge.net/updates-soc/rse-sync/)

*   Documents
    *   [Demo script](https://bugs.eclipse.org/bugs/attachment.cgi?id=110113)

Community Proposals
-------------------

Feel free to add your comments and ideas here, or on bugzilla [bug 185925](https://bugs.eclipse.org/bugs/show_bug.cgi?id=185925)


(Migrated from [https://wiki.eclipse.org/Platform/Team_Synchronization_on_top_of_RSE](https://wiki.eclipse.org/Platform/Team_Synchronization_on_top_of_RSE))