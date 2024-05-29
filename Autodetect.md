

TM/Autodetect
=============

< [TM](./TM "TM")

Lead: Javier Montalvo-Orús (Symbian)  
Members: Symbian, Freescale, WR

  

Contents
--------

*   [1 Autodetect through service discovery](#Autodetect-through-service-discovery)
*   [2 Service discovery usage on RSE](#Service-discovery-usage-on-RSE)
*   [3 Use cases for autodetect](#Use-cases-for-autodetect)
*   [4 Discussions](#Discussions)

### Autodetect through service discovery

We want to

*   Autodetect boards on the local network or in a lab
*   Autodetect services on a remote system
*   Autodetect connection mechanisms to a board (connectors)
*   Autodetect remote board registries (related to [Shared Board Labs](./Shared_Board_Labs "DSDP/TM/Shared Board Labs"))

in order to simplify setup of remote system connections for a user.

To enable service discovery to RSE get the plugins from CVS ([/cvsroot/dsdp/org.eclipse.tm.core/discovery/](http://dev.eclipse.org/viewcvs/index.cgi/org.eclipse.tm.core/discovery/?cvsroot=DSDP_Project)) or download the [working 2006/10/10 nightly build](https://www.eclipse.org/downloads/download.php?file=/dsdp/tm/downloads/drops/N20061010-0100/TM-discovery-N20061010-0100.zip)

It contains the following plugins:

*   **org.eclipse.tm.discovery.engine**: Engine for the service discovery process
*   **org.eclipse.tm.discovery.protocol**: Contains the factory, interface and extension point _org.eclipse.tm.discovery.engine.discoveryProtocol_ to define protocols
*   **org.eclipse.tm.discovery.transport**: Contains the factory, interface and extension point _org.eclipse.tm.discovery.engine.discoveryTransport_ to define transports
*   **org.eclipse.tm.discovery.protocol.dnssd**: Implementation of the DNS - Service Discovery protocol
*   **org.eclipse.tm.discovery.transport.udp**: Implementation of the UDP transport
*   **org.eclipse.tm.discovery.view**: View to browse discovered services, independent of RSE and enabled to launch the wizard page to start a new service discovery process.
*   **org.eclipse.tm.discovery.wizard**: Wizard pages for service discovery
*   **org.eclipse.tm.discovery.model, org.eclipse.tm.discovery.mode.edit**: EMF model for Service Discovery (requires EMF 2.2.0)
*   **org.eclipse.rse.discovery**: Link between RSE and the target management packages. Provides a customised wizard for the **Discovery** system type.

### Service discovery usage on RSE

The default plugins contains the implementation of [DNS-SD (Zeroconf/Bonjour)](http://www.dns-sd.org/) over UDP, other implementations can be provided through extension points. The multicast address for DNS-SD is 224.0.0.251, but a specific IP can be used if just querying one device.

The usage of service discovery can be seen on the [service discovery recording](https://bugs.eclipse.org/bugs/attachment.cgi?id=46936)

To test and evaluate the service discovery functionality in RSE 2.0, follow the testing intructions in the [manual test plan](https://wiki.eclipse.org/index.php/TM_Manual_Test_Plan#Discovery)

### Use cases for autodetect

*   New Connection - instead of having to type an IP address, get a list of available systems. Grouped by system type, connection type (serial vs. TCP/IP), LAN/WAN range etc.
*   In the New Connection Wizard, when the remote system is already identified, get available services / subsystems pre-selected as detected on the remote system (or disabled if not available on the remote system).
*   New Board Lab - instead of having to type an IP address, get a list of available board lab servers.

### Discussions

*   Bugzilla [bug 140320](https://bugs.eclipse.org/bugs/show_bug.cgi?id=140320)


(Migrated from [https://wiki.eclipse.org/DSDP/TM/Autodetect](https://wiki.eclipse.org/DSDP/TM/Autodetect))