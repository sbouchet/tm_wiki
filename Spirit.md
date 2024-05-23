

DSDP/DD/Spirit
==============

< [DSDP](/DSDP "DSDP")‎ | [DD](/DSDP/DD "DSDP/DD")

This is the SPIRIT Sub-group

Lead: Aaron Spear (Mentor Graphics)  
Members:  

Contents
--------

*   [1 Overview](#Overview)
*   [2 Current Status](#Current-Status)
*   [3 What the heck is SPIRIT?](#What-the-heck-is-SPIRIT.3F)
    *   [3.1 What is missing for debugger use](#What-is-missing-for-debugger-use)
*   [4 Current topics of discussion](#Current-topics-of-discussion)
    *   [4.1 Where/How do you want to use target info?](#Where.2FHow-do-you-want-to-use-target-info.3F)
    *   [4.2 SPIRIT vs. a decoupled XML based target description format](#SPIRIT-vs.-a-decoupled-XML-based-target-description-format)
*   [5 Documents](#Documents)

Overview
--------

This sub-group is trying to accomplish some sort of standardization of "target descriptions". It seems that the current state of the art is that every different debugger vendor does the same thing when they want to debug a new target board: they assign some poor soul to do the grunt work of reading a data book from a vendor and writing some kind of proprietary file that contains this info. Due to the sheer magnitude of the information, this is a terribly error prone process and a waste of everyones time and effort. "Wouldn't it be nice if there were a standard and the board vendors gave you the files?" We all asked. So, that is why we are doing this. We don't want to do this any more. (or at least want to be smarter about it)

Note that the higher level notion of target descriptions are now being tracked in bug

[https://bugs.eclipse.org/bugs/show_bug.cgi?id=146090](https://bugs.eclipse.org/bugs/show_bug.cgi?id=146090)

Current Status
--------------

*   6/2/06: Still in a specification stage, trying to gather and understand requirements more clearly before proceding. No work on implementation has been done yet.

*   6/2/06: Per Anthony Berent from ARM, the SPIRIT steering committee has officially added "SPIRIT for debugging" to their agenda. This is a great step forward, because it means that the SPIRIT folks are open to adding debugger specific information to the standard.
    *   10/18/06 (Anthony Berent): SPIRIT now includes a Debug Technical Working Group, it had a public launch meeting on 9/13/06 and has now started technical conference calls. I am interim chairman of the group.

*   7/18/06: Talking with various SPIRIT members to see if we can get a conribution of code capable of parsing SPIRIT files to start playing with. However, everyone is currently scrambling to get ready for DAC, so any progress is going to have to wait until after that.

What the heck is SPIRIT?
------------------------

[SPIRIT](http://www.spiritconsortium.com) stands for "Structure for Packaging, Integrating and Re-using IP within Tool-flows". It is an industry consortium of primarily EDA related companies (Electronic Design Automation) that maintains an XML based standard description of how IP blocks are connected together in a system on chip.

SPIRIT files contain a lot of information useful to debuggers. Information about address spaces, memory maps, memory mapped peripherals (registers), are all in the standard right now.

### What is missing for debugger use

There are some things that are missing. The biggest one is that information about registers inside of a given core are missing (native registers, that is ones that are not memory mapped). There are also other pieces of information that would be very nice to have for debuggers that are not a part of the standard today (things like side effects of register accesses and such).

So moving forward there is an effort to extend the SPIRIT standard to add debug specific information.

Current topics of discussion
----------------------------

### Where/How do you want to use target info?

I think that before any decision is made on whether or not to use SPIRIT or what, we need to identify how various tools plan on using these target descriptions. Are people going to need the info in their debugger back-ends? how do you plan on getting it there? Do we want to have shared file format parsing code that generates interfaces that can be used in Java? What about people that have native debuggers that are stand alone like GDB?

### SPIRIT vs. a decoupled XML based target description format

Depending on the answer to the question above, we may or may not want to directly use SPIRIT information. SPIRIT files tend to be full of information that is not relavent for a debugger, and parsing code can be complex. As such, you would likely not want to write multiple SPIRIT parsers. So, if there is a need for target file parsing in a native debugger back-end, then perhaps instead we should use a decoupled file format, and then write a SPIRIT convertor that can read in SPIRIT files and spit out this other format that we standardize on. (oh boy, a standards effort. hold me down)

Documents
---------

*   [Initial Requirements Doc - version 1.1](https://www.eclipse.org/downloads/download.php?file=/dsdp/dd/Subgroups/SPIRIT/DSDP_target_definition_requirements_1.1.doc)

*   [Presentation given by Hobson Bullman at the 2/22/06 Toronto face to face meeting regarding SPIRIT](http://ftp.osuosl.org/pub/eclipse/dsdp/dd/2006-2-22_Toronto_DD_SPIRIT_ForDebug.ppt)

