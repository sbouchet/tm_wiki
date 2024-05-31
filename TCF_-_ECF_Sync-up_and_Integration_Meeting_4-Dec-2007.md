

TCF/Meetings/Dec 4 2007 TCF-ECF Sync-up and Integration
=======================================================

< [TCF](./TCF "TCF")‎ | [Meetings](./TCF/Meetings "TCF/Meetings")(Redirected from [DSDP/TM/TCF - ECF Sync-up and Integration Meeting 4-Dec-2007](./index.php?title=DSDP/TM/TCF_-_ECF_Sync-up_and_Integration_Meeting_4-Dec-2007&redirect=no "DSDP/TM/TCF - ECF Sync-up and Integration Meeting 4-Dec-2007"))

| Meeting Title: | **TCF / ECF Sync-up and Integration Meeting** |
| --- | --- |
| Date & Time: | Tuesday Dec 4, 2007 at [1700 UTC / 1200 Eastern / 9am PST](http://www.timeanddate.com/worldclock/fixedtime.html?month=12&day=4&year=2007&hour=17&min=00&sec=0&p1=0) |
| Dial-in: | International **+44 (0)1452 567588** / Freephone **+1 (866) 6161738** / UK **08712460713**   Passcode: **0587322148 #** |

Contents
--------

*   [1 Attendees](#Attendees)
*   [2 Agenda](#Agenda)
    *   [2.1 Scope of TCF compared to scope of ECF](#Scope-of-TCF-compared-to-scope-of-ECF)
    *   [2.2 How to move forward](#How-to-move-forward)
    *   [2.3 Clarify overlaps between TCF and ECF](#Clarify-overlaps-between-TCF-and-ECF)
    *   [2.4 Clarify rules/guidelines for when ECF interfaces should be created](#Clarify-rules.2Fguidelines-for-when-ECF-interfaces-should-be-created)
    *   [2.5 Links](#Links)
*   [3 Action Items](#Action-Items)
*   [4 Next Meeting](#Next-Meeting)

Attendees
---------

*   Composent - Scott Lewis
*   Wind River - Martin Oberhuber, Felix Burton

This is an Open call, so anyone is invited to join. Please add yourself on the attendee list and add any agenda meetings you would like to discuss

Agenda
------

### Scope of TCF compared to scope of ECF

*   TCF is an incubating extendable protocol for communication with embedded devices, which allows value-add services to be added transparently into the communication link. Bindings may exist to a variety of languages and environments (plain C, plain Java, Eclipse). Currently, the plain Java binding is usable from Eclipse, but an ECF-based Eclipse specific binding can be added.
*   ECF provides generic APIs and mechanisms for communication from the Eclipse / Java environment, even if actual providers are written in other languages (e.g. Skype / C++).
*   Is the description on [DSDP/TM/TCF FAQ](./DSDP/TM/TCF_FAQ "DSDP/TM/TCF FAQ") sufficient to clarify the scope of TCF, especially compared to ECF? Will users/extenders understand the differences?
*   Is the [DSDP/TM/TCF_FAQ#How does TCF compare to ECF?](./DSDP/TM/TCF_FAQ#How_does_TCF_compare_to_ECF.3F "DSDP/TM/TCF FAQ") section sufficient and accurate?
    *   What do we think about the "vertical" versus "horizontal" description of TCF compared to ECF?
        *   When TCF focuses on the wire protocol, its vertical; when it focuses on transport agnosticism, it's horizontal; from today's statements we don't focus on transport agnosticism at all - we really want to standardize on TCP/IP, with proper enveloping through a protocol for transport conversion by a value-adding server (just a pass-through)

*   What do we think about the name (TCF), is the term "framework" in it too confusing? Are there alternatives?
    *   TCF is not a framework for plugging in client components - it's more a basic protocol specification that can be extended (a "protocol framework") - what about "Target Protocol Framework"?
    *   Want to avoid confusion: especially people seeing that both TCF and ECF have a Channel abstraction
    *   TCF would be another component on TM, not a separate project
    *   Want to further work on the TCF FAQ to finally come up with a correct, concise definition of what TCF really is - Scott: there's a constant struggle about defining APIs that access protocols

  

*   **Discussion:**
    *   Scott: Part of TCF is an asynchronous extensible API ("transport agnostic channel abstraction"). That particular part is overlapping highly with ECF. Also the auto-discovery of targets and services. We should work together on the overlapping things, to allow TCF work on the non-overlapping parts.
    *   The whole purpose of ECF is to create transport agnostic abstractions for communications. One of those is the Channel abstraction, another one the Discovery abstraction and the file transfer abstraction.
    *   The added value of cooperating is: all the code that's been written against the ECF channel abstraction can potentially be re-used on TCF.
    *   Felix: would that be beneficial to anybody? - TCF Channel is commands, replies and events. Registering a Service is a group of commands, events with semantics.
        *   The only kinds of clients that make sense to plug in to this framework is TCF services - the channel is only useful to TCF services.
        *   We would never have Eclipse talk to Serial target directly - we'd rather plug a value-adding server in between that would translate TCP/IP into Serial target communications. Therefore, we'd never have "special conversions" in Eclipse - all value-adding servers would have to know about that. Instead, use TCP/IP as long as we can (**standardize on TCP/IP**), and use a value-adding transport converter as near to the target as possible.
    *   Scott: any provider would need to do that. For example, XMPP - datashare uses XMPP beneath it. In order to do the addressing (refer to an XMPP endpoint), ECF ID interface is used.
*   Why is TCF an Eclipse Project?
    *   Martin - 2 reasons: (a) TCF and a lightweight agent have been requested and are a "missing links" for the embedded tools we have Eclipse-based already. (b) We like the EPL and the legal safety
*   What's the benefit of having an ECF provider for TCF?
    *   People can use an already-known programming model (from ECF) for sending messages and subscribing to events
    *   Ability to exchange underlying protocols is not so much helpful since we're trying to standardize on ONE protocol rather than exchanging protocols

  

### How to move forward

*   One Eclipse binding for TCF should be via ECF, but a plain Java binding should be retained for plain Java environments to use TCF. The ECF binding would allow any ECF/Equinox client to use TCF for datashare (channels) and fileshare.
*   Moving forward, according to [bug 210751 comment 22](https://bugs.eclipse.org/bugs/show_bug.cgi?id=210751#c22), a bridge should be written to **turn TCF into an ECF provider** for datashare (channels) and fileshare. Adding an adapter for directory retrieval to the ECF fileshare APIs could be considered.
*   TCF will live under the DSDP-TM project, including the TCF-ECF bridge (which will have a dependency to ECF obviously). Through the work on TCF, it may be possible that enhancements to ECF are contributed via patches (e.g. ECF fileshare directory retrieval).

### Clarify overlaps between TCF and ECF

*   Some core functionality exists in both TCF and ECF. Is there something (implementation, concepts) in ECF that we should bring into TCF? What would be the benefits?
*   How much of this exists in TCF already? Is there any point in keeping separate implementations such that a TCF Java binding can also run stand-alone?
    *   channels (associating message with response)
    *   name spaces / addressing
    *   filetransfer
    *   discovery
*   **Channels**: What is the Threading Model of ECF?
    *   Might as well pre-answer this question. The threading model for most ECF APIs is asynchronous. What is meant by this? In the context of [datashare](./ECF_API_Docs#Datashare_API "ECF API Docs") this is exposed via non-blocking [IChannel API](https://www.eclipse.org/ecf/org.eclipse.ecf.docs/api/org/eclipse/ecf/datashare/IChannel.html) calls, with a [listener attached to the channel upon construction](https://www.eclipse.org/ecf/org.eclipse.ecf.docs/api/org/eclipse/ecf/datashare/IChannelContainerAdapter.html#createChannel(org.eclipse.ecf.core.identity.ID,%20org.eclipse.ecf.datashare.IChannelListener,%20java.util.Map)). The [IChannelListener interface](https://www.eclipse.org/ecf/org.eclipse.ecf.docs/api/org/eclipse/ecf/datashare/IChannelListener.html) is asynchronously called when messages to the channel are received. The provider implementation of the IChannel and IChannelListener is responsible for implementing the underlying asynchrony via appropriate mechanisms (e.g. jobs or threads, etc). The IChannelListener is documented to allow the provider to call the listener with an arbitrary thread.
        *   Any thread call into ECF APIs; it's up to the provider whether they maintain state and thus need to take care of multi-threaded access.
        *   TCF: Like DSF - can call in on any thread but it's being translated into a single Executor thread

*   **Addressing**: How does ECF handle addressing for transports other than TCP/IP?
    *   One big part of transport agnosticism is addressing.
    *   All addressing in ECF is via ECF IDs. [ECF IDs](https://www.eclipse.org/ecf/org.eclipse.ecf.docs/api/org/eclipse/ecf/core/identity/ID.html) are defined to be unique object instances within an associated Namespace. In many respects they resemble URIs, but do not require the entire URI syntax. Also, ECF's identity bundle exposes a Namespace extension point that allows other plugins to define their own Namespaces, and also define ID construction within that Namespace. With this, plugins that need to address entities (other processes, etc) using something other than tcp/ip...as well as protocols built on tcp/ip...may freely do so.
    *   Packaging: P2 currently using 4 bundles - identity, filetransfer API, filetransfer impl - currently picking binaries from ECF update site; in Eclipse 3.4, they will be part of the Platform.
    *   Addressing in TCF: not yet implemented in TCF; in future, would first connect to value-add, then read from value-add what it can connect to and ask it to forward packets to the next server and so on. Each value-add brings in their own API/UI for addressing and routing. There is no single notion of "address" or "endpoint". User configures the communication link through the APIs / UIs brought in by the value-adders.
    *   TCF "Context" is not an address -- it's on a higher level, for identifying a thread, process, CPU, address space or breakpoint.
        *   Allows queries - hierarchical namespace, e.g.

*   **Filetransfer**: ECF has an [ECF API Refactoring#Create filetransfer plugin, remove fileshare plugin](./ECF_API_Refactoring#Create_filetransfer_plugin.2C_remove_fileshare_plugin "ECF API Refactoring") action item. How does this relate to directory retrievals?
    *   This particular refactoring has been completed some time ago (ECF fileshare is deprecated). RE: directory retrievals...in order to reduce the overall size and complexity of [filetransfer](./ECF_API_Docs#File_Transfer_API "ECF API Docs") as much as possible, directory information/browsing/navigation was initially left out of the file transfer API. This provided some benefits, in terms of size and complexity for the Equinox P2 project. However, using adapters, the file transfer API can (and eventually will) be expanded to include directory navigation. A new directory navigation adapter API contribution would be most welcome, and not technically difficult. Further, for applications that can accept the dependencies involved, EFS already provides directory navigation (and I think TM is already using EFS). Further, an ECF provider implementation \*based upon EFS and the Jobs API\* has already been created, and can be used in combination with the EFS directory/filestore browsing code. Obviously, such applications have to deal with the blocking I/O aspect of EFS directly.
        *   How would an application leverage EFS directory browsing with ECF fileshare? What would the benefit of using ECF be in that case?
    *   Filetransfer: See [API Docs for IRetrieveFileTransferContainerAdapter](https://www.eclipse.org/ecf/org.eclipse.ecf.docs/api/org/eclipse/ecf/filetransfer/IRetrieveFileTransferContainerAdapter.html) in ECF. Also see [here](./ECF_API_Docs#File_Transfer_API "ECF API Docs")

*   **Discovery**:
    *   How does discovery work in TCF? How much is implemented already?
    *   Here is [Bug 209774 for API changes in ECF Discovery 2.0](https://bugs.eclipse.org/bugs/show_bug.cgi?id=209774)
        *   This summary bug and all associated bugs have now been committed to HEAD. See [here for new API](./ECF_Discovery_API_Bundle "ECF Discovery API Bundle").
    *   Does DSDP-TM Discovery relate to this in any way?

### Clarify rules/guidelines for when ECF interfaces should be created

*   JDT is opening their own sockets today for debugging; why not use ECF?
*   Scott: ECF is not set out to replace all existing protocols; its rather for those who want interoperability (e.g. filetransfer - P2 not interested in implementing protocols) Current known deficiency
    *   Another example is Discovery - ECF defined a discovery API (Zeroconf; SLP implementations) - easy creation of interoperable clients
*   Felix: Rather than integrating on Channel level, better integrate on the Filesystem and Discovery levels. TM should have an ECF based fileshare service.
*   ECF Channel abstraction is very low-level - only byte\[\] arrays, no data presentation layer

*   What are the benefits of integrating ECF/TCF?
    *   Discovery makes sense
    *   Fileshare makes sense (but directory browsing is missing)
    *   Datashare: Does it make sense to have an ECF provider for Channel as well, or not?
        *   ECF Datashare API is extendable via Adapters

*   Felix: Chicken-and-egg problem... when RSE has an ECF fileshare service, it makes sense to implement it in TCF but probably not before

### Links

*   [DSDP/TM/TCF FAQ](./DSDP/TM/TCF_FAQ "DSDP/TM/TCF FAQ")

Action Items
------------

*   All: Re-read the FAQ and point out misunderstandings
*   Martin: file a bug for updating the FAQ (Done: [bug 211901](https://bugs.eclipse.org/bugs/show_bug.cgi?id=211901))

Next Meeting
------------

*   Should talk again once a few agenda items are identified - will schedule on-demand via E-Mail


(Migrated from [https://wiki.eclipse.org//DSDP/TM/TCF_-_ECF_Sync-up_and_Integration_Meeting_4-Dec-2007](https://wiki.eclipse.org//DSDP/TM/TCF_-_ECF_Sync-up_and_Integration_Meeting_4-Dec-2007))