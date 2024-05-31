

DSDP-TM Notes 2006x02x06
========================

| Meeting Title: | **Conference Call on Target Management** |
| --- | --- |
| Date & Time: | Monday February 06, 2006 at 9am PST |
| Primary International Dial-in: | **+44 (0)1452 567588** |
| USA Freephone Dial-In: | +1 (866) 6161738 |
| UK National Dial-In: | 08712460713 |
| Passcode: | **0587322148 #** |

Contents
--------

*   [1 Invited Attendants](#Invited-Attendants)
*   [2 Agenda](#Agenda)
    *   [2.1 Action Items from last meeting](#Action-Items-from-last-meeting)
    *   [2.2 New Action Items](#New-Action-Items)
    *   [2.3 Next Meeting](#Next-Meeting)

Invited Attendants
------------------

*   Martin Oberhuber, Wind River
*   David Dykstal and Dave McKnight, IBM
*   Pierre-Alexandre Masse, MontaVista

*   Peter Lachner, Intel
*   Victor Palau, Javier Montalvo and Neil Taylor, Symbian
*   Mark Littlefield and Darian Wong, Curtiss-Wright

Agenda
------

*   RSE available at Bugzilla!
    *   Build problems at Wind River: RSE doesnt work on 3.1, on 3.2M4 it works fine!
    *   Pierre Alexandre: able to browse the local file system, but not able to do any other actions
        *   Remote System View doesnt come up (NullPointerException in GetSystemRoot())
        *   Dave McKnight: Missing dependencies? - Send E-Mail
    *   DaveD: RSE has no notion of "Project" so "build" is not possible

*   Pierre-Alexandre can make it to Toronto!

*   ssh connections via ECF?
    *   JCraft jar going to be exposed as a plugin in its own right
    *   Connectivity as an ECF Service, or as an RSE Service?
        *   DaveD: Potentially want to bring in this technology back into IBM; Given that ECF is currently a technology project, tend to directly doing an ssh service for RSE and not go over ECF.
        *   DaveMcKnight: If we want to bring in ECF, we'd need an RSE service for ssh, wrapping ECF. We might need separate ECF wrappers for each service brought in by ECF anyway. Especially thinking that ssh is not just file transfer but also a shell service (implement RSE IShellService). Summary: whatever ECF provides, we'd either need an ECF wrapper in RSE or a direct wrapper.
        *   MartinO: What do we need to know until the Toronto meeting, in order to decide on pro or against ECF? - Need to know how fast ECF would implement ssh, and when it would potentially become a real project. AI: DaveD investigate
        *   DavidD: Going the ECF line might make it easier for other folks to contribute new protocols. But need to understand where ECF is going as a project as a whole

*   Pierre-Alexandre: Not yet decided which components to get involved in; interesting items are remote debugging, filesystem transfer and browsing (already available); a bit concerned about pulling in all of ECF - there are interesting core components, but dont want to pull in too much. AI MartinO: Find E-Mail from Scott Lewis regarding ECF dependencies

*   Additional Agenda Items for Toronto
    *   Pierre-Alexandre: Possible to get a small design document / architecture overview for RSE before Toronto? - DaveD: Most of the stuff is UI, the services themselves are pretty small; DaveMcK: Was about to write up a small overview anyway;
    *   Discuss Service Type APIs in RSE
    *   MartinO: Drop me an E-Mail

*   TM Website
    *   Phoenix redisign almost done
    *   Using the Wiki for "less official" stuff
    *   using the Web for "official" stuff; stuff may migrate from the Wiki to the Web.

*   Pierre-Alexandre: Try to advertise things more to the dsdp-tm-dev mailing list
    *   MartinO: Agree: copy the dsdp-tm-list on communications that came from outside; ask peers to join the list

### Action Items from last meeting

*   MartinO:
    *   Launch Actions - Initial Design - will bring to Toronto
    *   Contact Greg Watson (LANL, PTP) - open
    *   DSDP-TM Project Plan - in progress for website
    *   Start F2F Meeting Agenda - done
*   George Clark:
    *   Approach ARM regarding Register file definitions - contact made, waiting for feedback
    *   Doug Gaff found that ARM is working on a standard for hardware descriptions as well; will bring documents to Toronto
*   Symbian:
    *   Write up interface description for "Service" as understood by Symbian
*   Pierre-Alexandre
    *   Write up additional use case for STAF - open
*   Everyone:
    *   Bring schema / example for Register Files & Boardfiles - deferred to Toronto

### New Action Items

*   MartinO:
    *   Ask WR contacts to speed up RSE IP process at EMO
    *   Find E-Mail by Scott Lewis regarding ECF dependencies and forward to dsdp-tm-dev
    *   Forward instructions on Website editing to DaveD and DaveMcK
    *   Launch Actions - Initial Design
    *   Contact Greg Watson (LANL, PTP)
    *   DSDP-TM Project Plan - post on website
*   DaveD:
    *   Look at ECF code, investigate to make a recommendation for ssh in RSE at Toronto meeting
*   DaveMcK:
    *   Write up RSE Design Overview Document and post it on the Wiki
    *   Extract the RSE Archive from Bugzilla and find out why there are exceptions
*   George Clark:
    *   Approach ARM regarding Register file definitions - contact made, waiting for feedback
*   Symbian:
    *   Write up interface description for "Service" as understood by Symbian
*   Pierre-Alexandre
    *   Write up additional use case for STAF
*   Everyone
    *   Send E-Mail about additional Toronto Agenda Items to the tm-dev list

### Next Meeting

*   **Face-to-face Meeting** confirmed for Wed, February 22, 2006  \- Fri, February 24, 2006, IBM Labs Toronto (Pete Nicholls)
    *   DD Meetings on Wednesday + Thursday morning
    *   TM Meetings on Thursday afternoon + Friday
    *   Agenda and Notes on [DSDP-TM Face-to-face Toronto 2006x02x23](./DSDP-TM_Face-to-face_Toronto_2006x02x23 "DSDP-TM Face-to-face Toronto 2006x02x23")
*   Next [DSDP/TM/Phone Meeting 10-Apr-2006](./Phone_Meeting_10-Apr-2006 "DSDP/TM/Phone Meeting 10-Apr-2006")


(Migrated from [https://wiki.eclipse.org//DSDP-TM_Notes_2006x02x06](https://wiki.eclipse.org//DSDP-TM_Notes_2006x02x06))