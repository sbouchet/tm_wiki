

DSDP-TM Connector Meeting Salzburg 2005x11x14
=============================================

| Meeting Title: | **Meeting to continue discussion on Target Connection Adapter proposal** |
| --- | --- |
| Date & Time: | Monday November 14, 2005 at 3pm CET |
| Location: | WR Office, Salzburg, Austria |

Attendants
----------

*   Peter Lachner, Intel
*   Martin Oberhuber, Wind River
*   Felix Burton, Wind River
*   Michael Scharf, Wind River

Notes
-----

*   Peter shows [slides with new scenarios](https://www.eclipse.org/dsdp/tm/doc/DSDP-TM_TCA_Scenarios_2005x11x14.ppt) for connectors.
*   Felix: The most difficult thing with the TCA proposal is defining the interfaces.
    *   Hard to think about the generic connector concept
    *   Start by defining only interfaces that TM needs for registering connectors, and defining dependencies between them.
    *   Additional interfaces to be defined by connectors themselves
    *   TM to provide a GUI to show basic services on a target
        *   Selecting a particular entity on a target might reveal new services (with interfaces defined by the parent)
        *   Thought about various approaches to a UI for connector configuration (what is provided by the user? What is computed by the system?) But didnt come up with an agreement. What is the workflow for the user? Stat the debugger first? Or connect the target first? Or define target properties first?
*   We need to separate the protocol from the connection (somebody might want to do a protocol without a connection, just for translating protocols).
    *   We tried to map connectors to the OSI model but that doesn't map well
*   Michael: Connectors are like **resolvers** \- they resolve "I want to... with target" by providing the right connection module and protocols. There might be some preconfigured resolutions, plus some autodetected resolutions.
*   With our connector chain represented by some "black boxes", we want as little intelligence as possible to reside in the individual boxes.
    *   Connectors may be in a hierarchy, but not the services
    *   Selecting a particular entity on a target might enable new services
*   Michael: Interfaces for the various protocols provided by connectors could be specified in an "action-like" manner: each action to be executed is an interface in its own right, which may be available or not
*   Martin: TM should **only hold the meta-information** for connectors (that can also be programs outside Eclipse): provided-protocol, required-protocol. Example: Wind River chain of servers (Eclipse - dfwserver - tgtsvr - target agent) is mostly not Java
*   Felix Burton worked on "Receptacles" 1980 -- showcase that composition and configuration of connection chains can actually work

