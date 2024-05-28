

DSDP-TM Boardfile Descriptions at Windriver 2005x12x19
======================================================

In the TM session of the DSDP meeting in Chicago, we came to a point where we noticed that TM wants to provide a common platform for describing the targets (hardware) we are working on.

Currently, every vendor is doing their own hardware descriptions, typically by XML or some other files... they all have to read the specs from silicon vendors, and create their own file formats. That's a lot of wasted work.

We are hoping that at some point it might be possible to create a uniform "standard" file format, or at least provide some converters between various file formats. Ideally, then silicon vendors could provide their specifications in the uniform format (or something convertible). Silicon vendors could become the "experts" for hardware descriptions, users could get patches/updates directly from them... lifting off a lot of work from tool vendors like us.

As a first step, I'm attching a [sample and description of the board file specification that Wind River is currently using](https://www.eclipse.org/dsdp/tm/doc/hwdescriptions/WRBoardfileSyntax.zip).

I'd hope that other companies could follow and put their samples or descriptions to the table, such that we can get a feeling of what features are required from a "unified" format, and find out future steps to take.

